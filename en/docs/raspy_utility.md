# RasPY Utility

<div align="center">
  <img src="../images/logo.png" alt="RasPY Utility Logo" width="50%">
</div>

## Benvenuti nella documentazione di RasPY Utility

RasPY Utility è un'applicazione completa per il controllo e il monitoraggio dei pin GPIO del Raspberry Pi attraverso un'interfaccia grafica intuitiva o un'API REST.

## Indice

### Introduzione
- [Installazione](installazione.md)
- [Guida](guida.md)

### Sviluppo
- [Sviluppo](sviluppo.md)
- [API](api.md)
- [GUI](gui.md)
- [Esempi](esempi.md)

### Altre risorse
- [Changelog](changelog.md)
- [FAQ](faq.md)

### Community
- [Contribuire](contribuire.md)
- [Ringraziamenti](ringraziamenti.md)

## Caratteristiche principali

### ✅ **Interfaccia Grafica Moderna**
- Tema scuro/chiaro
- Supporto multi-lingua
- Visualizzazione in tempo reale dello stato dei pin
- Integrazione con la system tray

### 🔌 **Supporto GPIO Completo**
- Controllo pin digitali I/O
- Simulatore integrato per sviluppo
- Rilevamento automatico hardware
- Supporto GPIO remoto

### 🌐 **Interfaccia Web**
- Server web integrato
- Design responsive per mobile/desktop
- Aggiornamenti in tempo reale
- Documentazione API integrata

## Guida rapida

1. [Installazione](installazione.md) - Come installare e configurare RasPY Utility
2. [Guida](guida.md) - Guida all'utilizzo dell'applicazione
3. [API](api.md) - Documentazione dell'API per sviluppatori
4. [Sviluppo](sviluppo.md) - Guida allo sviluppo e contributi

## Guida all'utilizzo

### Interfaccia Grafica

L'interfaccia grafica di RasPY 4 Utility è progettata per essere intuitiva e facile da usare.

#### Menu Principale

- **File**: Controlli generali dell'applicazione
- **GPIO**: Gestione dei pin GPIO e del simulatore
- **Visualizza**: Personalizzazione dell'interfaccia
- **Aiuto**: Documentazione e informazioni

#### Controllo GPIO

1. Apri la finestra di controllo GPIO dal menu
2. Seleziona il pin da controllare
3. Usa i pulsanti per attivare/disattivare i pin
4. Monitora lo stato in tempo reale

#### Simulatore GPIO

Il simulatore ti permette di testare il codice senza un dispositivo fisico:

1. Avvia il simulatore dal menu GPIO
2. Usa l'interfaccia per simulare l'input/output
3. I cambiamenti si riflettono in tempo reale

### Log e Debug

L'applicazione registra eventi importanti nel file `logs/app.log`. Usa il Visualizzatore Log integrato per:

- Filtrare i messaggi per livello (INFO, WARNING, ERROR)
- Cercare messaggi specifici
- Esportare i log per l'analisi

### Tasti rapidi

- **Ctrl+Q**: Esci dall'applicazione
- **F1**: Mostra la guida
- **Ctrl+L**: Apri il visualizzatore log
- **F5**: Aggiorna l'interfaccia

## API Reference

### Panoramica

L'API REST di RasPY 4 Utility permette di controllare i pin GPIO tramite richieste HTTP. 
Tutte le risposte sono in formato JSON.

### Endpoint disponibili

#### `GET /api/gpio`

Restituisce lo stato di tutti i pin GPIO configurati.

**Esempio di risposta:**

```json
{
  "17": {"state": 0, "mode": "out", "description": "LED Rosso"},
  "18": {"state": 1, "mode": "in", "description": "Pulsante"}
}
```

#### `GET /api/gpio/<int:pin>`

Restituisce lo stato di un pin specifico.

**Parametri:**
- `pin`: Numero del pin GPIO

**Codici di stato:**
- 200: Operazione riuscita
- 404: Pin non trovato

**Esempio di risposta:**

```json
{
  "state": 0,
  "mode": "out",
  "description": "LED Rosso"
}
```

#### `POST /api/gpio/<int:pin>/on`

Accende il pin specificato.

**Parametri:**
- `pin`: Numero del pin GPIO

**Codici di stato:**
- 200: Operazione riuscita
- 400: Pin non valido o non scrivibile

#### `POST /api/gpio/<int:pin>/off`

Spegne il pin specificato.

**Parametri:**
- `pin`: Numero del pin GPIO

**Codici di stato:**
- 200: Operazione riuscita
- 400: Pin non valido o non scrivibile

## Esempi di utilizzo

### Controllo GPIO con Python

```python
import requests

BASE_URL = "http://localhost:5000/api/gpio"

# Ottenere lo stato di tutti i pin
response = requests.get(f"{BASE_URL}")
print("Stato attuale:", response.json())

# Accendere il pin 17
response = requests.post(f"{BASE_URL}/17/on")
print("Risposta accensione:", response.status_code)
```

## Risorse utili

- [Sito ufficiale Raspberry Pi](https://www.raspberrypi.org/)
- [Documentazione Python](https://www.python.org/)
