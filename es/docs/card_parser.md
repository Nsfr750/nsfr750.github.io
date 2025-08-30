---
lang: es
lang-niv: fonto
lang-ref: 011-jbk
layout: doc
order: 2
title: 'Analizador de Banda Magnética de Tarjetas de Crédito'
---

# Analizador de Banda Magnética de Tarjetas de Crédito

**Credit Card Stripe Parser** es una biblioteca de Python y una herramienta de línea de comandos para analizar datos de banda magnética de tarjetas de crédito. Es compatible con los formatos de Pista 1 y Pista 2 según los estándares ISO/IEC 7811-2 e ISO/IEC 7813.

> **Nota**
> Esta herramienta está destinada únicamente con fines educativos y de prueba. Siempre maneje los datos de tarjetas de pago de acuerdo con los requisitos de PCI DSS y las leyes y regulaciones aplicables.

## Guía de Uso

Esta guía proporciona ejemplos de cómo utilizar la biblioteca Credit Card Stripe Parser.

### Uso Básico

#### Análisis de Datos de Pista Completa

```python
from credit_card_stripe_parser import FullTrackParser

# Crear una instancia del analizador
parser = FullTrackParser()

# Ejemplo de datos de pista
track_data = "%B5168755544412233^PKMMV/UNEMBOXXXX          ^1807111100000000000000111000000?;5168755544412233=18071111000011100000?"

# Analizar los datos de la pista
result = parser.parse(track_data)

# Acceder a los datos analizados
if result.is_track_one_valid and result.track_one:
    print(f"Titular: {result.track_one.card_holder_name.strip()}")
    print(f"PAN: {result.track_one.pan}")
    print(f"Vencimiento: {result.track_one.expiration_date[:2]}/{result.track_one.expiration_date[2:]}")

if result.is_track_two_valid and result.track_two:
    print(f"Código de servicio: {result.track_two.service_code}")
```

### Análisis de Pistas Individuales

#### Análisis de Pista 1

```python
from credit_card_stripe_parser import FullTrackParser

parser = FullTrackParser()
track1_data = "%B5168755544412233^PKMMV/UNEMBOXXXX          ^1807111100000000000000111000000?"

try:
    track1 = parser.parse_track_one(track1_data)
    print(f"Datos de Pista 1: {track1}")
except Exception as e:
    print(f"Error al analizar Pista 1: {e}")
```

#### Análisis de Pista 2

```python
from credit_card_stripe_parser import FullTrackParser

parser = FullTrackParser()
track2_data = ";5168755544412233=18071111000011100000?"

try:
    track2 = parser.parse_track_two(track2_data)
    print(f"Datos de Pista 2: {track2}")
except Exception as e:
    print(f"Error al analizar Pista 2: {e}")
```

### Manejo de Errores

La biblioteca proporciona excepciones específicas para diferentes escenarios de error:

```python
from credit_card_stripe_parser import (
    FullTrackParser,
    InvalidTrackOneException,
    InvalidTrackTwoException,
    InvalidTrackDataException
)

parser = FullTrackParser()

try:
    result = parser.parse(datos_de_pista_invalidos)
except InvalidTrackOneException as e:
    print(f"Datos de Pista 1 inválidos: {e}")
except InvalidTrackTwoException as e:
    print(f"Datos de Pista 2 inválidos: {e}")
except InvalidTrackDataException as e:
    print(f"Datos de pista inválidos: {e}")
except Exception as e:
    print(f"Error inesperado: {e}")
```

### Uso de los Modelos de Datos

La biblioteca proporciona modelos de datos para trabajar con los datos de pista analizados:

```python
from credit_card_stripe_parser.models import TrackOneModel, TrackTwoModel

# Crear una instancia de TrackOneModel
track1 = TrackOneModel(
    format_code='B',
    pan='5168755544412233',
    card_holder_name='JUAN PEREZ',
    expiration_date='2512',
    service_code='123',
    discretionary_data='123456789012345678901',
    source_string='%B5168755544412233^JUAN PEREZ^251212312345678901234567890?'
)

# Crear una instancia de TrackTwoModel
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

## Uso Avanzado

### Validación Personalizada

Puede implementar una validación personalizada creando una subclase del analizador:

```python
from credit_card_stripe_parser import FullTrackParser

class AnalizadorPersonalizado(FullTrackParser):
    def validate_track_one(self, track_data: str) -> bool:
        # Lógica de validación personalizada para Pista 1
        if not super().validate_track_one(track_data):
            return False
        # Agregar validación personalizada aquí
        return True

    def validate_track_two(self, track_data: str) -> bool:
        # Lógica de validación personalizada para Pista 2
        if not super().validate_track_two(track_data):
            return False
        # Agregar validación personalizada aquí
        return True
```

### Validación LRC

Para habilitar la validación LRC (Comprobación de Redundancia Longitudinal):

```python
parser = FullTrackParser(validate_lrc=True)

# Esto generará una excepción si falla la validación LRC
try:
    result = parser.parse(datos_de_pista_con_lrc)
except Exception as e:
    print(f"Error en validación LRC: {e}")
```
> **Nota**
> La validación LRC requiere que los datos de la pista incluyan el carácter LRC al final.

## Preguntas Frecuentes (FAQ)

### Preguntas Generales

#### ¿Cuál es el propósito de esta biblioteca?
Esta biblioteca está diseñada para analizar datos de bandas magnéticas de tarjetas de crédito con fines educativos y de prueba.

#### ¿Es seguro usarla en producción?
Esta herramienta debe usarse de acuerdo con los requisitos de PCI DSS y las leyes aplicables. Siempre asegúrese de implementar las medidas de seguridad adecuadas al manejar datos de tarjetas de pago.

### Preguntas Técnicas

#### ¿Qué formatos de pista son compatibles?
La biblioteca es compatible con los formatos de Pista 1 y Pista 2 según los estándares ISO/IEC 7811-2 e ISO/IEC 7813.

#### ¿Cómo manejo los errores durante el análisis?
La biblioteca proporciona excepciones específicas para diferentes escenarios de error. Consulte la sección Manejo de Errores para ver ejemplos.

### Consideraciones de Seguridad

#### ¿Cómo debo manejar los datos sensibles de la tarjeta?
Siempre siga los requisitos de PCI DSS al manejar datos de tarjetas de pago. La biblioteca incluye funciones auxiliares para enmascarar información confidencial.

#### Ejemplo de enmascaramiento de PAN:

```python
def enmascarar_pan(pan):
    if len(pan) <= 4:
        return pan
    return '*' * (len(pan) - 4) + pan[-4:]
```

## Licencia

Este proyecto está licenciado bajo la Licencia Pública General de GNU v3.0 - consulte el archivo [LICENCIA](LICENCIA) para más detalles.
