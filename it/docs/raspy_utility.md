---
lang: it
lang-niv: font
lang-ref: 021-jbk
layout: doc
order: 12
title: 'RasPY Utility'
---

# RasPY Utility

<div align="center">
  <img src="../images/logo.png" alt="Logo di RasPY Utility" width="50%">
</div>

## Benvenuti nella Documentazione di RasPY Utility

RasPY Utility è un'applicazione completa per il controllo e il monitoraggio dei pin GPIO del Raspberry Pi attraverso un'interfaccia grafica intuitiva o un'API REST.

## Indice

### Introduzione
- [Installazione](installazione.md)
- [Guida](guida.md)

### Sviluppo
- [Sviluppo](sviluppo.md)
- [API](api.md)
- [Interfaccia Grafica](gui.md)
- [Esempi](esempi.md)

### Risorse Aggiuntive
- [Registro delle Modifiche](changelog.md)
- [Domande Frequenti](faq.md)

### Comunità
- [Contribuisci](contribuire.md)
- [Ringraziamenti](ringraziamenti.md)

## Funzionalità Principali

### ✅ **Interfaccia Grafica Moderna**
- Tema chiaro/scuro
- Supporto multilingua
- Visualizzazione in tempo reale dello stato dei pin
- Integrazione con la barra delle applicazioni

### 🔌 **Supporto Completo GPIO**
- Controllo pin I/O digitali
- Simulatore integrato per lo sviluppo
- Rilevamento automatico dell'hardware
- Supporto GPIO remoto

### 🌐 **Interfaccia Web**
- Server web integrato
- Design reattivo per dispositivi mobili/desktop
- Aggiornamenti in tempo reale
- Documentazione API integrata

## Guida Rapida

1. [Installazione](installazione.md) - Come installare e configurare RasPY Utility
2. [Guida](guida.md) - Guida all'utilizzo dell'applicazione
3. [API](api.md) - Documentazione API per sviluppatori
4. [Sviluppo](sviluppo.md) - Guida allo sviluppo e ai contributi

## Guida Utente

### Interfaccia Grafica

L'interfaccia grafica di RasPY 4 Utility è progettata per essere intuitiva e facile da usare.

#### Menu Principale

- **File**: Controlli generali dell'applicazione
- **GPIO**: Gestione pin GPIO e simulatore
- **Visualizza**: Personalizzazione dell'interfaccia
- **Aiuto**: Documentazione e informazioni

#### Controllo GPIO

1. Apri la finestra di controllo GPIO dal menu
2. Seleziona il pin da controllare
3. Usa i pulsanti per attivare/disattivare i pin
4. Monitora lo stato in tempo reale

#### Simulatore GPIO
Il simulatore consente di testare il codice senza hardware fisico:

1. Avvia il simulatore dal menu GPIO
2. Usa l'interfaccia per simulare input/output
3. Le modifiche si riflettono in tempo reale

### Registro e Debug
L'applicazione registra gli eventi importanti nel file `logs/app.log`. Usa il Visualizzatore di Log integrato per:

- Filtrare i messaggi per livello (INFO, AVVISO, ERRORE)
- Cercare messaggi specifici
- Esportare i log per l'analisi

### Scorciatoie da Tastiera

- **Ctrl+Q**: Esci dall'applicazione
- **F1**: Mostra aiuto
- **Ctrl+L**: Apri il visualizzatore di log
- **F5**: Aggiorna l'interfaccia

## Riferimento API

### Panoramica

L'API REST di RasPY 4 Utility consente di controllare i pin GPIO tramite richieste HTTP.
Tutte le risposte sono in formato JSON.

### Endpoint Disponibili

#### `GET /api/gpio`

Restituisce lo stato di tutti i pin GPIO configurati.

**Esempio di risposta:**

```json
{
  "17": {"stato": 0, "modalita": "out", "descrizione": "LED Rosso"},
  "18": {"stato": 1, "modalita": "in", "descrizione": "Pulsante"}
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
  "stato": 0,
  "modalita": "out",
  "descrizione": "LED Rosso"
}
```

#### `POST /api/gpio/<int:pin>/on`

Attiva il pin specificato.

**Parametri:**
- `pin`: Numero del pin GPIO

**Codici di stato:**
- 200: Operazione riuscita
- 400: Pin non valido o non scrivibile

#### `POST /api/gpio/<int:pin>/off`

Disattiva il pin specificato.

**Parametri:**
- `pin`: Numero del pin GPIO

**Codici di stato:**
- 200: Operazione riuscita
- 400: Pin non valido o non scrivibile

## Esempi di Utilizzo

### Controllo GPIO con Python

```python
import requests

URL_BASE = "http://localhost:5000/api/gpio"

# Ottieni lo stato di tutti i pin
risposta = requests.get(f"{URL_BASE}")
print("Stato attuale:", risposta.json())

# Attiva il pin 17
risposta = requests.post(f"{URL_BASE}/17/on")
print("Risposta attivazione:", risposta.status_code)
```

## Risorse Utili

- [Sito Ufficiale Raspberry Pi](https://www.raspberrypi.org/)
- [Documentazione Python](https://www.python.org/)
