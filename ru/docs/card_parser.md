---
lang: ru
lang-niv: fonto
lang-ref: 011-jbk
layout: page
title: 'Парсер магнитных полос банковских карт'
---

# Парсер магнитных полос банковских карт

**Credit Card Stripe Parser** — это библиотека Python и инструмент командной строки для разбора и анализа данных с магнитных полос банковских карт. Поддерживает форматы как первой, так и второй дорожки в соответствии со стандартами ISO/IEC 7811-2 и ISO/IEC 7813.

> **Примечание**
> Данный инструмент предназначен исключительно для образовательных целей и тестирования. Всегда обрабатывайте данные платежных карт в соответствии с требованиями PCI DSS и применимыми законами и нормативными актами.

## Руководство по использованию

В этом руководстве приведены примеры использования библиотеки Credit Card Stripe Parser.

### Базовое использование

#### Разбор полных данных дорожки

```python
from credit_card_stripe_parser import FullTrackParser

# Создаем экземпляр парсера
parser = FullTrackParser()

# Пример данных дорожки
track_data = "%B5168755544412233^PKMMV/UNEMBOXXXX          ^1807111100000000000000111000000?;5168755544412233=18071111000011100000?"

# Разбираем данные дорожки
result = parser.parse(track_data)

# Доступ к разобранным данным
if result.is_track_one_valid and result.track_one:
    print(f"Владелец карты: {result.track_one.card_holder_name.strip()}")
    print(f"PAN: {result.track_one.pan}")
    print(f"Срок действия: {result.track_one.expiration_date[:2]}/{result.track_one.expiration_date[2:]}")

if result.is_track_two_valid and result.track_two:
    print(f"Сервисный код: {result.track_two.service_code}")
```

### Разбор отдельных дорожек

#### Разбор первой дорожки

```python
from credit_card_stripe_parser import FullTrackParser

parser = FullTrackParser()
track1_data = "%B5168755544412233^PKMMV/UNEMBOXXXX          ^1807111100000000000000111000000?"

try:
    track1 = parser.parse_track_one(track1_data)
    print(f"Данные первой дорожки: {track1}")
except Exception as e:
    print(f"Ошибка разбора первой дорожки: {e}")
```

#### Разбор второй дорожки

```python
from credit_card_stripe_parser import FullTrackParser

parser = FullTrackParser()
track2_data = ";5168755544412233=18071111000011100000?"

try:
    track2 = parser.parse_track_two(track2_data)
    print(f"Данные второй дорожки: {track2}")
except Exception as e:
    print(f"Ошибка разбора второй дорожки: {e}")
```

### Обработка ошибок

Библиотека предоставляет специфические исключения для различных сценариев ошибок:

```python
from credit_card_stripe_parser import (
    FullTrackParser,
    InvalidTrackOneException,
    InvalidTrackTwoException,
    InvalidTrackDataException
)

parser = FullTrackParser()

try:
    result = parser.parse(invalid_track_data)
except InvalidTrackOneException as e:
    print(f"Неверные данные первой дорожки: {e}")
except InvalidTrackTwoException as e:
    print(f"Неверные данные второй дорожки: {e}")
except InvalidTrackDataException as e:
    print(f"Неверные данные дорожки: {e}")
except Exception as e:
    print(f"Непредвиденная ошибка: {e}")
```

### Использование моделей данных

Библиотека предоставляет модели данных для работы с разобранными данными дорожек:

```python
from credit_card_stripe_parser.models import TrackOneModel, TrackTwoModel

# Создаем экземпляр TrackOneModel
track1 = TrackOneModel(
    format_code='B',
    pan='5168755544412233',
    card_holder_name='ИВАН ИВАНОВ',
    expiration_date='2512',
    service_code='123',
    discretionary_data='123456789012345678901',
    source_string='%B5168755544412233^ИВАН ИВАНОВ^251212312345678901234567890?'
)

# Создаем экземпляр TrackTwoModel
track2 = TrackTwoModel(
    pan='5168755544412233',
    expiration_date='2512',
    service_code='123',
    pvki=None,
    pvv_or_cvv='1234',
    discretionary_data='123456789012345678901234567890',
    source_string=';5168755544412233=2512123123412345678901234567890?'
)
```

## Продвинутое использование

### Пользовательская валидация

Вы можете реализовать собственную валидацию, создав подкласс парсера:

```python
from credit_card_stripe_parser import FullTrackParser

class CustomTrackParser(FullTrackParser):
    def validate_track_one(self, track_data: str) -> bool:
        # Пользовательская логика валидации для первой дорожки
        if not super().validate_track_one(track_data):
            return False
        # Добавьте пользовательскую валидацию здесь
        return True

    def validate_track_two(self, track_data: str) -> bool:
        # Пользовательская логика валидации для второй дорожки
        if not super().validate_track_two(track_data):
            return False
        # Добавьте пользовательскую валидацию здесь
        return True
```

### Валидация LRC

Для включения проверки контрольной суммы (Longitudinal Redundancy Check):

```python
parser = FullTrackParser(validate_lrc=True)

# Вызовет исключение при неудачной проверке LRC
try:
    result = parser.parse(track_data_with_lrc)
except Exception as e:
    print(f"Ошибка проверки LRC: {e}")
```
> **Примечание**
> Для проверки LRC данные дорожки должны включать символ LRC в конце.

## Часто задаваемые вопросы (FAQ)

### Общие вопросы

#### Каково назначение этой библиотеки?
Эта библиотека предназначена для разбора и анализа данных с магнитных полос банковских карт в образовательных целях и для тестирования.

#### Безопасно ли использовать её в продакшене?
Этот инструмент следует использовать в соответствии с требованиями PCI DSS и применимыми законами. Всегда обеспечивайте надлежащие меры безопасности при работе с данными платежных карт.

### Технические вопросы

#### Какие форматы дорожек поддерживаются?
Библиотека поддерживает форматы как первой, так и второй дорожки в соответствии со стандартами ISO/IEC 7811-2 и ISO/IEC 7813.

#### Как обрабатывать ошибки при разборе?
Библиотека предоставляет специфические исключения для различных сценариев ошибок. Примеры смотрите в разделе "Обработка ошибок".

### Вопросы безопасности

#### Как следует обрабатывать конфиденциальные данные карт?
Всегда соблюдайте требования PCI DSS при работе с данными платежных карт. Библиотека включает вспомогательные функции для маскирования конфиденциальной информации.

#### Пример маскирования PAN:

```python
def mask_pan(pan: str) -> str:
    if len(pan) < 10:
        return pan
    return pan[:6] + '*' * (len(pan) - 10) + pan[-4:]

print(mask_pan("5168755544412233"))  # Выведет: 516875******2233
```
