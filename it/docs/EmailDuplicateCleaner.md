---
lang: it
lang-niv: fonto
lang-ref: 013-jbk
layout: doc
order: 4
title: 'Email Duplicate Cleaner'
---

# 📧 Email Duplicate Cleaner

Un potente strumento Python progettato per scansionare, identificare e rimuovere email duplicate tra diversi client di posta elettronica. Include interfacce web, desktop e a riga di comando.

## 🚀 Versione

**Versione corrente:**
[![GitHub release](https://img.shields.io/badge/release-v2.5.2-green)](https://github.com/Nsfr750/EmailDuplicateCleaner)
[![Documentation](https://img.shields.io/badge/docs-disponibile-brightgreen)](https://github.com/Nsfr750/EmailDuplicateCleaner/blob/master/README.md)
[![Python Versions](https://img.shields.io/badge/python-3.8%20|%203.9%20|%203.10%20|%203.11%20|%203.12-blue)](https://www.python.org/)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![PyPI](https://img.shields.io/pypi/v/email-duplicate-cleaner)](https://pypi.org/project/email-duplicate-cleaner/)
[![Donate](https://img.shields.io/badge/Donazione-PayPal-green.svg)](https://paypal.me/3dmega)
[![Supporto](https://img.shields.io/badge/Supporto-Patreon-ff69b4.svg)](https://www.patreon.com/Nsfr750)

## ✨ Novità nella 2.5.2

- 🚀 Aggiornamento alla versione 2.5.2
- 🐛 Corretto il numero di versione nella finestra "Informazioni su"
- 📚 Aggiornata la documentazione per riflettere le ultime modifiche

## ✨ Novità nella 2.5.1

- 🐛 Risolto l'errore di importazione QAction in PySide6 GUI
- 🌐 Aggiunte traduzioni complete in inglese
- 📄 Incluso il file di licenza GPL-3.0
- 🔄 Migliorata la gestione degli errori nell'inizializzazione della GUI
- ⬆️ Aggiornate le dipendenze per una migliore stabilità

## ✨ Funzionalità

### 🔍 Rilevamento Duplicati

- Metodi di rilevamento multipli:
  - Rigoroso: Confronto completo
  - Solo Contenuto: Analisi del corpo del messaggio
  - Intestazioni: Confronto basato sui metadati
  - Oggetto+Mittente: Identificazione mirata

### 📊 Analisi Email

- Analisi avanzata delle email:
  - Analisi mittenti: Identifica i mittenti e i domini principali
  - Analisi temporale: Visualizza i modelli di invio nel tempo
  - Analisi allegati: Tipi di file, dimensioni e frequenze
  - Analisi conversazioni: Visualizza e gestisci i thread di conversazione
  - Analisi duplicati: Dettagli sul rilevamento dei duplicati
  - Report esportabili in più formati (Testo, HTML, JSON)

### 🖥️ Supporto Multi-Interfaccia

- **Interfaccia Web** - Design moderno e reattivo con tema chiaro/scuro
- **GUI Desktop** - Esperienza desktop nativa con PySide6
- **Interfaccia a Righe di Comando** - Supporto per automazione e scripting avanzato

### 🌓 Esperienza Utente Migliorata

- Interfaccia web moderna con tema chiaro/scuro
- Anteprima interattiva con aggiornamenti in tempo reale
- Sistema di aiuto completo
- Modalità debug con registrazione dettagliata
- Modalità dimostrativa per test e apprendimento

### 🔒 Compatibilità con i Client di Posta

Supporta:

- Mozilla Thunderbird
- Apple Mail
- Microsoft Outlook
- Formati generici mbox/maildir

### 🏗️ Caratteristiche Tecniche

- Interfaccia web moderna realizzata con Flask
- SQLAlchemy per la gestione del database
- Sistema di aiuto completo con contenuti dinamici
- Architettura modulare con chiara separazione delle responsabilità
- Compatibilità cross-piattaforma
- Gestione completa degli errori e registrazione

## 🛠️ Prerequisiti

- Python 3.8+
- pip
- Sistemi operativi supportati: Windows, macOS, Linux

## 🚀 Guida Rapida

### 💰 Supporta Questo Progetto

Se trovi utile questo strumento, considera di supportarne lo sviluppo:

- [![Donate](https://img.shields.io/badge/Donazione-PayPal-green.svg)](https://paypal.me/3dmega) Supporta tramite PayPal
- [![Support](https://img.shields.io/badge/Supporto-Patreon-ff69b4.svg)](https://www.patreon.com/Nsfr750) Diventa un Patreon
- :money_with_wings: **Monero (XMR)**: 
  ```
  47Jc6MC47WJVFhiQFYwHyBNQP5BEsjUPG6tc8R37FwcTY8K5Y3LvFzveSXoGiaDQSxDrnCUBJ5WBj6Fgmsfix8VPD4w3gXF
  ```

## 📦 Installazione

1.  Clona il repository:

    ```bash
    git clone https://github.com/Nsfr750/EmailDuplicateCleaner.git
    cd EmailDuplicateCleaner
    ```

2.  Installa le dipendenze:

    ```bash
    pip install -r requirements.txt
    ```

### Esecuzione dell'Applicazione

#### Interfaccia Web

```bash
python app.py
```

Accessibile all'indirizzo `http://localhost:5000`

#### GUI Desktop

```bash
python email_cleaner_gui.py
```

#### Demo da Righe di Comando

```bash
python email_duplicate_cleaner.py --demo
```

## 🤝 Contributi

Interessato a contribuire? Consulta le nostre [Linee Guida per i Contributi](CONTRIBUTING.md)!

## 📄 Licenza

Questo progetto è concesso in licenza con la licenza MIT.

## 🐛 Segnalazione Problemi

Hai trovato un bug? [Apri una segnalazione](https://github.com/Nsfr750/EmailDuplicateCleaner/issues)

## 📊 Metodi di Rilevamento

- `strict`: Message-ID + Data + Mittente + Oggetto + Contenuto
- `content`: Solo contenuto
- `headers`: Message-ID + Data + Mittente + Oggetto
- `subject-sender`: Solo campi Oggetto e Mittente

## Funzionalità di Sicurezza

- Conserva sempre almeno una copia di ogni email
- Mantiene l'email più vecchia per impostazione predefinita
- Le email originali sono recuperabili dal cestino
- Modalità dimostrativa per test sicuri

## Struttura del Progetto

- `email_cleaner_web.py`: Interfaccia web
- `email_cleaner_gui.py`: GUI desktop
- `email_duplicate_cleaner.py`: Funzionalità principale e CLI
- `static/`: Risorse web (CSS, JS)
- `templates/`: Modelli HTML

## Flussi di Lavoro

- Modalità Demo: Esegue con email di test
- Aiuto: Mostra le informazioni sull'utilizzo
- Modalità GUI: Avvia l'interfaccia desktop
- Modalità Web: Avvia il server web

## Struttura della GUI

- **GUI (`email_cleaner_gui.py`)**: Un'interfaccia grafica intuitiva realizzata con Tkinter. Fornisce un modo semplice per selezionare i client di posta, scansionare le cartelle e gestire i duplicati.
- **CLI (`email_cleaner_cli.py`)**: Un'interfaccia a riga di comando per chi preferisce lavorare nel terminale.
- **Web (`app.py`)**: Un'interfaccia web basata su Flask, accessibile da qualsiasi browser.

### Moduli Ausiliari (`struttura/`)

La directory `struttura/` contiene tutti i moduli ausiliari che supportano la GUI, come finestre di dialogo e menu.

- **`menu.py`**: Gestisce la creazione e la funzionalità della barra dei menu principale, mantenendo il file GUI principale pulito e focalizzato sul suo layout principale.
- **`about.py`**, **`help.py`**, **`sponsor.py`**: Definiscono le finestre di dialogo `Informazioni su`, `Aiuto` e `Sponsor`, ciascuna incapsulata nella propria classe.
- **`log_viewer.py`**: Un semplice visualizzatore di log per mostrare i log dell'applicazione.

## Caratteristiche della GUI

- **Interfaccia Intuitiva**: Un'interfaccia grafica pulita e facile da usare per gestire gli account email e scansionare i duplicati.
- **Selezione Multipla**: Usa `Maiusc+Freccie` e `Ctrl+Freccie` per selezionare più caselle di posta e cartelle.
- **Supporto Multilingua**: Disponibile in inglese e italiano.
