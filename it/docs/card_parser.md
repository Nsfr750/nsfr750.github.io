---
lang: it
lang-niv: fonto
lang-ref: 011-jbk
layout: pagelayout: doc
layout: doc
order: 2
title: 'Analizzatore di Bande Magnetiche Carte di Credito'
---

# Analizzatore di Bande Magnetiche Carte di Credito

**Analizzatore di Bande Magnetiche Carte di Credito** è una libreria Python e uno strumento da riga di comando per l'analisi e l'elaborazione dei dati delle bande magnetiche delle carte di credito. Supporta i formati Traccia 1 e Traccia 2 come specificato negli standard ISO/IEC 7811-2 e ISO/IEC 7813.

> **Nota**
> Questo strumento è destinato esclusivamente a scopi didattici e di test. Gestisci sempre i dati delle carte di pagamento in conformità con i requisiti PCI DSS e le leggi e i regolamenti applicabili.

## Guida all'Utilizzo

Questa guida fornisce esempi su come utilizzare la libreria di analisi delle bande magnetiche delle carte di credito.

### Utilizzo di Base

#### Analisi Completa dei Dati della Banda

```python
from credit_card_stripe_parser import FullTrackParser

# Crea un'istanza del parser
parser = FullTrackParser()

# Dati di esempio della traccia
track_data = "%B5168755544412233^PKMMV/UNEMBOXXXX          ^1807111100000000000000111000000?;5168755544412233=18071111000011100000?"

# Analizza i dati della traccia
result = parser.parse(track_data)

# Accedi ai dati analizzati
if result.is_track_one_valid and result.track_one:
    print(f"Intestatario: {result.track_one.card_holder_name.strip()}")
    print(f"PAN: {result.track_one.pan}")
    print(f"Scadenza: {result.track_one.expiration_date[:2]}/{result.track_one.expiration_date[2:]}")

if result.is_track_two_valid and result.track_two:
    print(f"Codice di Servizio: {result.track_two.service_code}")
```

### Analisi delle Tracce Singole

#### Analisi Traccia 1

```python
from credit_card_stripe_parser import FullTrackParser

parser = FullTrackParser()
track1_data = "%B5168755544412233^PKMMV/UNEMBOXXXX          ^1807111100000000000000111000000?"

try:
    track1 = parser.parse_track_one(track1_data)
    print(f"Dati Traccia 1: {track1}")
except Exception as e:
    print(f"Errore nell'analisi della Traccia 1: {e}")
```

#### Analisi Traccia 2

```python
from credit_card_stripe_parser import FullTrackParser

parser = FullTrackParser()
track2_data = ";5168755544412233=18071111000011100000?"

try:
    track2 = parser.parse_track_two(track2_data)
    print(f"Dati Traccia 2: {track2}")
except Exception as e:
    print(f"Errore nell'analisi della Traccia 2: {e}")
```

### Gestione degli Errori

La libreria fornisce eccezioni specifiche per diversi scenari di errore:

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
    print(f"Dati Traccia 1 non validi: {e}")
except InvalidTrackTwoException as e:
    print(f"Dati Traccia 2 non validi: {e}")
except InvalidTrackDataException as e:
    print(f"Dati traccia non validi: {e}")
except Exception as e:
    print(f"Errore imprevisto: {e}")
```

### Utilizzo dei Modelli di Dati

La libreria fornisce modelli di dati per lavorare con i dati delle tracce analizzate:

```python
from credit_card_stripe_parser.models import TrackOneModel, TrackTwoModel

# Crea un'istanza di TrackOneModel
track1 = TrackOneModel(
    format_code='B',
    pan='5168755544412233',
    card_holder_name='MARIO ROSSI',
    expiration_date='2512',
    service_code='123',
    discretionary_data='123456789012345678901',
    source_string='%B5168755544412233^MARIO ROSSI^251212312345678901234567890?'
)

# Crea un'istanza di TrackTwoModel
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

## Utilizzo Avanzato

### Validazione Personalizzata

Puoi implementare una validazione personalizzata creando una sottoclasse del parser:

```python
from credit_card_stripe_parser import FullTrackParser

class CustomTrackParser(FullTrackParser):
    def validate_track_one(self, track_data: str) -> bool:
        # Logica di validazione personalizzata per la Traccia 1
        if not super().validate_track_one(track_data):
            return False
        # Aggiungi qui la validazione personalizzata
        return True

    def validate_track_two(self, track_data: str) -> bool:
        # Logica di validazione personalizzata per la Traccia 2
        if not super().validate_track_two(track_data):
            return False
        # Aggiungi qui la validazione personalizzata
        return True
```

### Validazione LRC

Per abilitare la validazione LRC (Longitudinal Redundancy Check):

```python
parser = FullTrackParser(validate_lrc=True)

# Questo genererà un'eccezione se la validazione LRC fallisce
try:
    result = parser.parse(track_data_with_lrc)
except Exception as e:
    print(f"Validazione LRC fallita: {e}")
```
> **Nota**
> La validazione LRC richiede che i dati della traccia includano il carattere LRC alla fine.

## Domande Frequenti (FAQ)

### Domande Generali

#### Qual è lo scopo di questa libreria?
Questa libreria è progettata per analizzare ed elaborare i dati delle bande magnetiche delle carte di credito a scopo didattico e di test.

#### È sicuro utilizzarla in produzione?
Questo strumento dovrebbe essere utilizzato in conformità con i requisiti PCI DSS e le leggi applicabili. Assicurati sempre che siano in atto le opportune misure di sicurezza quando gestisci i dati delle carte di pagamento.

### Domande Tecniche

#### Quali formati di tracce sono supportati?
La libreria supporta i formati Traccia 1 e Traccia 2 come specificato negli standard ISO/IEC 7811-2 e ISO/IEC 7813.

#### Come gestisco gli errori durante l'analisi?
La libreria fornisce eccezioni specifiche per diversi scenari di errore. Vedi la sezione Gestione degli Errori per esempi.

### Considerazioni sulla Sicurezza

#### Come devo gestire i dati sensibili delle carte?
Segui sempre i requisiti PCI DSS quando gestisci i dati delle carte di pagamento. La libreria include funzioni di supporto per mascherare le informazioni sensibili.

#### Esempio di mascheramento del PAN:

```python
def maschera_pan(pan):
    if len(pan) <= 4:
        return pan
    return '*' * (len(pan) - 4) + pan[-4:]
```

## Licenza

Questo progetto è concesso in licenza con la Licenza GPLv3 - vedi il file [LICENZA](LICENZA) per i dettagli.
