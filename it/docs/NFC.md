---
lang: it
lang-niv: fonto
lang-ref: 016-jbk
layout: page
title: 'NFC'
---

# 🚀 Applicazione Lettore/Scrittore NFC

[![Licenza: GPL v3](https://img.shields.io/badge/Licenza-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Stile del codice: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Un'applicazione potente basata su PySide6 per leggere e scrivere su vari tipi di tag NFC con funzionalità avanzate e un'interfaccia utente intuitiva.

## Installazione

### Prerequisiti

- Python 3.9 o superiore
- Hardware lettore NFC (ACR122U, ACR1252U, ecc.)

### Guida Rapida

1. Clona il repository:

   ```bash
   git clone https://github.com/Nsfr750/NFC.git
   cd NFC
   ```

2. Crea e attiva un ambiente virtuale:

   ```bash
   python -m venv venv
   .\venv\Scripts\activate  # Windows
   source venv/bin/activate  # Linux/Mac
   ```

3. Installa le dipendenze:

   ```bash
   pip install -r requirements.txt
   ```

4. Avvia l'applicazione:

   ```bash
   python main.py
   ```

Per istruzioni dettagliate di installazione, consulta [PREREQUISITI.md](PREREQUISITI.md).

## Funzionalità

- **Supporto Multi-tag**: Supporto completo per vari tipi di tag NFC tra cui:
  - NTAG (NTAG213, NTAG215, NTAG216)
  - MIFARE Classic (1K, 4K)
  - MIFARE Ultralight
  - FeliCa (Sony)
  - Carte ISO 14443 Tipo A/B

- **Supporto Completo dei Tag**: [Visualizza le operazioni supportate](docs/operazioni_supportate.md) per tutti i tipi di tag

- **Operazioni NDEF**:
  - Leggi e scrivi record NDEF
  - Crea e gestisci più record NDEF
  - Supporto per vari tipi di record NDEF (Testo, URI, Smart Poster, ecc.)
  - Visualizzazione esadecimale per l'ispezione dei dati grezzi

- **Gestione Tag**:
  - Leggi le informazioni del tag (UID, layout della memoria, capacità)
  - Scrivi dati sui tag con validazione
  - Blocca i tag per prevenire scritture non autorizzate
  - Formatta i tag per l'uso con NDEF

- **Interfaccia Utente**:
  - Design moderno e reattivo con tema sphinx_rtd_theme
  - Supporto per temi Chiaro/Scuro/Sistema
  - Rilevamento tag in tempo reale e aggiornamenti di stato
  - Pannello informazioni dettagliate sul tag
  - Visualizzatore di log con opzioni di filtraggio
  - Documentazione completa in inglese e italiano

- **Funzionalità di Sicurezza**:
  - 🔒 Protezione con password per operazioni sensibili
  - 🔑 Hashing sicuro delle password con PBKDF2
  - 🔄 Funzionalità di modifica password
  - ⚙️ Opzione per abilitare/disabilitare la protezione con password
  - 🔐 Operazioni protette includono Strumenti Tag, Database e Cloner

- **Funzionalità Avanzate**:
  - Modalità emulazione tag (sperimentale)
  - Operazioni in batch per l'elaborazione di più tag
  - Esecuzione di comandi personalizzati
  - Sistema di registrazione con più livelli di dettaglio
  - Documentazione API per sviluppatori
  - Guida alla risoluzione dei problemi comuni
  - Linee guida per la collaborazione open-source

## 🚀 Requisiti

- Python 3.8 o superiore
- Hardware Lettore/Scrittore NFC supportato:
  - ACR122U
  - PN532 (tramite USB/UART)
  - Lettori compatibili PC/SC
- Windows 10/11 o Linux con supporto PC/SC
- Pacchetti Python richiesti (vedi `requirements.txt`)

## 📖 Documentazione

La documentazione completa è disponibile sia in inglese che in italiano, inclusi:

- Guida Utente
- Riferimento API
- Guida alla Risoluzione dei Problemi
- FAQ
- Linee Guida per i Collaboratori

Per compilare la documentazione in locale:

```bash
# Installa i requisiti per la documentazione
pip install -r requirements-docs.txt

# Compila la documentazione in inglese
cd docs/ENG
make html

# Compila la documentazione in italiano
cd ../ITA
make html
```

La documentazione sarà disponibile nella directory `_build/html` di ciascuna cartella della lingua.

## 📦 Installazione

1. Clona questo repository:

   ```bash
   git clone https://github.com/Nsfr750/NFC.git
   cd NFC
   ```

2. Crea e attiva un ambiente virtuale (consigliato):

   ```bash
   # Windows
   python -m venv venv
   .\venv\Scripts\activate

   # Linux/macOS
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Installa i pacchetti richiesti:

   ```bash
   pip install -r requirements.txt
   ```

4. (Opzionale) Installa i driver PC/SC se non già installati:
   - Windows: Installa i [driver CCID](https://ccid.apdu.fr/)
   - Linux: Installa i pacchetti `pcscd` e `libpcsclite-dev`

5. Avvia l'applicazione:

   ```bash
   python main.py
   ```

## 🚀 Utilizzo

### Operazioni di Base

1. **Collega il tuo lettore NFC**
   - L'applicazione rileverà automaticamente i dispositivi supportati
   - Lo stato della connessione è mostrato nella barra di stato

2. **Leggi un tag**
   - Avvicina un tag NFC al lettore
   - Le informazioni del tag verranno visualizzate nella finestra principale
   - Visualizza il layout dettagliato della memoria nell'editor esadecimale

3. **Scrivi su un tag**
   - Vai alla scheda "Scrivi"
   - Seleziona il tipo di record (Testo, URI, ecc.)
   - Inserisci il contenuto e fai clic su "Scrivi sul Tag"

4. **Blocca un tag**
   - Usa il pulsante "Blocca" per prevenire ulteriori scritture
   - Alcuni tag supportano il blocco permanente (fai attenzione!)

### 🛠️ Funzionalità Avanzate

- **Emulazione Tag**: Emula un tag NFC (sperimentale)
- **Comandi Personalizzati**: Invia comandi APDU grezzi al tag
- **Visualizzazione Memoria**: Ispeziona e modifica la memoria grezza del tag
- **Registrazione**: Visualizza log dettagliati delle operazioni con opzioni di filtraggio

### ⚙️ Impostazioni

Accedi alle impostazioni tramite `Strumenti > Impostazioni` o premi `Ctrl+,`:

- **Generale**:
  - Connessione automatica all'avvio
  - Selezione della lingua
  - Controllo aggiornamenti

- **NFC**:
  - Timeout del lettore
  - Lettura automatica al rilevamento del tag
  - Segnale acustico al rilevamento del tag

- **Interfaccia**:
  - Tema (Chiaro/Scuro/Sistema)
  - Dimensione e tipo di carattere
  - Comportamento della finestra

- **Avanzate**:
  - Livello di registrazione
  - Comandi personalizzati
  - Opzioni per sviluppatori

### ⌨️ Scorciatoie da Tastiera

| Tasti           | Azione                     |
|----------------|----------------------------|
| `Ctrl+N`       | Nuovo progetto             |
| `Ctrl+O`       | Apri file                  |
| `Ctrl+S`       | Salva dati correnti        |
| `Ctrl+Maiusc+S`| Salva con nome...          |
| `Ctrl+L`       | Leggi tag                  |
| `Ctrl+W`       | Scrivi sul tag             |
| `Ctrl+E`       | Cancella tag               |
| `Ctrl+B`       | Blocca tag                 |
| `Ctrl+,`       | Apri impostazioni          |
| `F1`           | Mostra aiuto               |
| `F5`           | Aggiorna tag               |
| `Ctrl+Q`       | Esci dall'applicazione     |

## 🤝 Collaborazione

I contributi sono benvenuti! Ecco come puoi aiutare:

1. Segnala bug aprendo un'issue
2. Suggerisci nuove funzionalità o miglioramenti
3. Invia pull request
4. Migliora la documentazione
5. Condividi il tuo feedback e le tue idee

## 📝 Licenza

Questo progetto è concesso in licenza con la Licenza GPL-3.0

## 👤 Autore

- **Nsfr750**
  - Email: [nsfr750@yandex.com](mailto:nsfr750@yandex.com)
  - GitHub: [@Nsfr750](https://github.com/Nsfr750)
  - Discord: [Unisciti alla nostra community](https://discord.gg/ryqNeuRYjD)

## 💖 Supporto

Se trovi utile questo progetto, considera di supportarne lo sviluppo:

- [Diventa un Patron](https://www.patreon.com/Nsfr750)
- [Dona tramite PayPal](https://paypal.me/3dmega)
- Dona Monero:

  ```text
  47Jc6MC47WJVFhiQFYwHyBNQP5BEsjUPG6tc8R37FwcTY8K5Y3LvFzveSXoGiaDQSxDrnCUBJ5WBj6Fgmsfix8VPD4w3gXF
  ```

## 📞 Contatti

Per supporto, richieste di funzionalità o domande, apri un'issue su [GitHub](https://github.com/Nsfr750/NFC/issues) o unisciti al nostro [server Discord](https://discord.gg/ryqNeuRYjD).
