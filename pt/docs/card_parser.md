---
lang: pt
lang-niv: fonto
lang-ref: 011-jbk
layout: doc
order: 2
title: 'Analisador de Tarja Magnética de Cartões de Crédito'
---

# Analisador de Tarja Magnética de Cartões de Crédito

**Credit Card Stripe Parser** é uma biblioteca Python e ferramenta de linha de comando para análise de dados de tarja magnética de cartões de crédito. Suporta os formatos de Trilha 1 e Trilha 2 conforme especificados nos padrões ISO/IEC 7811-2 e ISO/IEC 7813.

> **Nota**
> Esta ferramenta destina-se apenas a fins educacionais e de teste. Sempre manipule dados de cartões de pagamento em conformidade com os requisitos do PCI DSS e leis e regulamentos aplicáveis.

## Guia de Uso

Este guia fornece exemplos de como usar a biblioteca Credit Card Stripe Parser.

### Uso Básico

#### Análise de Dados de Trilha Completa

```python
from credit_card_stripe_parser import FullTrackParser

# Criar uma instância do analisador
parser = FullTrackParser()

# Exemplo de dados de trilha
track_data = "%B5168755544412233^PKMMV/UNEMBOXXXX          ^1807111100000000000000111000000?;5168755544412233=18071111000011100000?"

# Analisar os dados da trilha
result = parser.parse(track_data)

# Acessar dados analisados
if result.is_track_one_valid and result.track_one:
    print(f"Titular: {result.track_one.card_holder_name.strip()}")
    print(f"PAN: {result.track_one.pan}")
    print(f"Validade: {result.track_one.expiration_date[:2]}/{result.track_one.expiration_date[2:]}")

if result.is_track_two_valid and result.track_two:
    print(f"Código de serviço: {result.track_two.service_code}")
```

### Análise de Trilhas Individuais

#### Análise da Trilha 1

```python
from credit_card_stripe_parser import FullTrackParser

parser = FullTrackParser()
track1_data = "%B5168755544412233^PKMMV/UNEMBOXXXX          ^1807111100000000000000111000000?"

try:
    track1 = parser.parse_track_one(track1_data)
    print(f"Dados da Trilha 1: {track1}")
except Exception as e:
    print(f"Erro ao analisar Trilha 1: {e}")
```

#### Análise da Trilha 2

```python
from credit_card_stripe_parser import FullTrackParser

parser = FullTrackParser()
track2_data = ";5168755544412233=18071111000011100000?"

try:
    track2 = parser.parse_track_two(track2_data)
    print(f"Dados da Trilha 2: {track2}")
except Exception as e:
    print(f"Erro ao analisar Trilha 2: {e}")
```

### Tratamento de Erros

A biblioteca fornece exceções específicas para diferentes cenários de erro:

```python
from credit_card_stripe_parser import (
    FullTrackParser,
    InvalidTrackOneException,
    InvalidTrackTwoException,
    InvalidTrackDataException
)

parser = FullTrackParser()

try:
    result = parser.parse(dados_de_trilha_invalidos)
except InvalidTrackOneException as e:
    print(f"Dados inválidos da Trilha 1: {e}")
except InvalidTrackTwoException as e:
    print(f"Dados inválidos da Trilha 2: {e}")
except InvalidTrackDataException as e:
    print(f"Dados de trilha inválidos: {e}")
except Exception as e:
    print(f"Erro inesperado: {e}")
```

### Usando os Modelos de Dados

A biblioteca fornece modelos de dados para trabalhar com os dados de trilha analisados:

```python
from credit_card_stripe_parser.models import TrackOneModel, TrackTwoModel

# Criar uma instância de TrackOneModel
track1 = TrackOneModel(
    format_code='B',
    pan='5168755544412233',
    card_holder_name='JOAO SILVA',
    expiration_date='2512',
    service_code='123',
    discretionary_data='123456789012345678901',
    source_string='%B5168755544412233^JOAO SILVA^251212312345678901234567890?'
)

# Criar uma instância de TrackTwoModel
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

## Uso Avançado

### Validação Personalizada

Você pode implementar validação personalizada criando uma subclasse do analisador:

```python
from credit_card_stripe_parser import FullTrackParser

class AnalisadorPersonalizado(FullTrackParser):
    def validate_track_one(self, track_data: str) -> bool:
        # Lógica de validação personalizada para Trilha 1
        if not super().validate_track_one(track_data):
            return False
        # Adicionar validação personalizada aqui
        return True

    def validate_track_two(self, track_data: str) -> bool:
        # Lógica de validação personalizada para Trilha 2
        if not super().validate_track_two(track_data):
            return False
        # Adicionar validação personalizada aqui
        return True
```

### Validação LRC

Para habilitar a validação LRC (Verificação de Redundância Longitudinal):

```python
parser = FullTrackParser(validate_lrc=True)

# Isso lançará uma exceção se a validação LRC falhar
try:
    result = parser.parse(dados_de_trilha_com_lrc)
except Exception as e:
    print(f"Falha na validação LRC: {e}")
```
> **Nota**
> A validação LRC requer que os dados da trilha incluam o caractere LRC no final.

## Perguntas Frequentes (FAQ)

### Perguntas Gerais

#### Qual é o objetivo desta biblioteca?
Esta biblioteca foi projetada para analisar dados de tarjas magnéticas de cartões de crédito para fins educacionais e de teste.

#### É seguro usar em produção?
Esta ferramenta deve ser usada em conformidade com os requisitos do PCI DSS e leis aplicáveis. Sempre garanta que as medidas de segurança adequadas estejam em vigor ao lidar com dados de cartões de pagamento.

### Perguntas Técnicas

#### Quais formatos de trilha são suportados?
A biblioteca suporta os formatos de Trilha 1 e Trilha 2 conforme especificados nos padrões ISO/IEC 7811-2 e ISO/IEC 7813.

#### Como lidar com erros durante a análise?
A biblioteca fornece exceções específicas para diferentes cenários de erro. Consulte a seção Tratamento de Erros para obter exemplos.

### Considerações de Segurança

#### Como devo lidar com dados sensíveis de cartão?
Sempre siga os requisitos do PCI DSS ao lidar com dados de cartões de pagamento. A biblioteca inclui funções auxiliares para mascarar informações confidenciais.

#### Exemplo de mascaramento de PAN:

```python
def mascarar_pan(pan):
    if len(pan) <= 4:
        return pan
    return '*' * (len(pan) - 4) + pan[-4:]
```

## Licença

Este projeto está licenciado sob a Licença Pública Geral GNU v3.0 - consulte o arquivo [LICENÇA](LICENÇA) para obter detalhes.
