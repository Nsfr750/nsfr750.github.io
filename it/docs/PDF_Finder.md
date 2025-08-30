---
lang: it
lang-niv: fonto
lang-ref: 019-jbk
layout: page
title: 'Cerca PDF'
---

# Cerca Duplicati PDF

[![Licenza: GPL v3](https://img.shields.io/badge/Licenza-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Stile del codice: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Uno strumento potente per trovare e gestire file PDF duplicati sul tuo computer. Cerca Duplicati PDF ti aiuta a identificare e rimuovere documenti PDF duplicati, risparmiando spazio su disco e organizzando i tuoi file in modo più efficiente.

## ✨ Funzionalità

- 🔍 **Confronto Intelligente PDF**: Trova PDF duplicati in base al contenuto, non solo ai nomi o alle dimensioni dei file
- 📝 **Confronto Basato sul Testo**: Identifica duplicati anche con piccole differenze visive utilizzando l'analisi avanzata del testo
- 👁 **Visualizzatore PDF Integrato**: Anteprima i PDF direttamente all'interno dell'applicazione
- 📋 **Interfaccia a Doppia Visualizzazione**: Visualizza sia l'elenco dei file che i gruppi di duplicati in schede separate
- 🎯 **Filtri Avanzati**: Filtra per dimensione del file, data di modifica e modelli di nomi
- 🚀 **Scansione Veloce**: Algoritmi ottimizzati per la scansione rapida di grandi raccolte di PDF
- 🎨 **Interfaccia Intuitiva**: Interfaccia pulita e facile da usare con supporto per temi chiaro/scuro
- 🔄 **Elaborazione in Batch**: Elabora più file o intere cartelle contemporaneamente
- 📊 **Analisi Dettagliata**: Visualizza dettagli dei file, anteprime e risultati del confronto
- 🛠 **Strumenti Avanzati**: Modalità di selezione multipla, filtri e opzioni di ordinamento
- 🌍 **Supporto Multilingua**: Disponibile in più lingue
- 📊 **Monitoraggio Avanzamento**: Barra di avanzamento in tempo reale per le operazioni di elaborazione file
- ⏱ **File Recenti**: Accesso rapido ai file aperti di recente con opzioni del menu contestuale

## 📦 Installazione

### Prerequisiti

- Python 3.8 o superiore
- pip (gestore pacchetti Python)
- Backend opzionali per il rendering PDF (il fallback è automatico e sicuro):
  - PyMuPDF (fitz) — predefinito e incluso nei requisiti
  - Ghostscript (per Wand) — installa Ghostscript e imposta il percorso dell'eseguibile nelle Impostazioni

Vedi [PREREQUISITI.md](PREREQUISITI.md) per la configurazione specifica della piattaforma.

### Installazione dal Sorgente

1. Clona il repository:

   ```bash
   git clone https://github.com/Nsfr750/PDF_finder.git
   cd PDF_finder
   ```

2. Crea e attiva un ambiente virtuale (consigliato):

   ```bash
   python -m venv venv
   .\venv\Scripts\activate  # Windows
   source venv/bin/activate  # Linux/Mac
   ```

3. Installa le dipendenze richieste:

   ```bash
   pip install -r requirements.txt
   ```

## Utilizzo

1. Avvia l'applicazione:

   ```bash
   python main.py
   ```

2. Fai clic su "Scansiona Cartella" per selezionare una directory da analizzare alla ricerca di PDF duplicati.

3. Rivedi i risultati nella finestra principale. Dopo il completamento della scansione, l'elenco dei file viene automaticamente popolato con i PDF scansionati e i gruppi di duplicati.

4. Utilizza gli strumenti per gestire i duplicati:
   - Segna i file da conservare
   - Elimina i duplicati indesiderati
   - Visualizza l'anteprima dei file prima di agire

## Funzionalità Principali in Dettaglio

### Confronto Intelligente PDF

- Confronta il contenuto dei PDF utilizzando algoritmi avanzati di hashing
- Rileva documenti simili anche con nomi o metadati diversi
- Soglia di somiglianza configurabile per risultati ottimizzati

### Ottimizzazioni delle Prestazioni

- Scansione multithreading per un'elaborazione più veloce
- Gestione efficiente della memoria per file PDF di grandi dimensioni
- Monitoraggio dell'avanzamento e supporto per l'annullamento

### Esperienza Utente

- Interfaccia moderna e reattiva
- Opzioni di visualizzazione personalizzabili
- Scorciatoie da tastiera complete
- Informazioni dettagliate e anteprime dei file
- Barra degli strumenti con spaziatura migliorata e chiarezza visiva
- La finestra delle impostazioni include un pulsante "Testa backend" per verificare la disponibilità di PyMuPDF e Ghostscript

### Backend PDF e Fallback

- Scegli il tuo backend preferito in Impostazioni → Rendering PDF
- Usa "Testa backend" per verificare se Ghostscript è configurato correttamente
- Se il backend selezionato non è disponibile, l'applicazione passa automaticamente a un backend disponibile e mostra un avviso nella barra di stato (localizzato)

## Cronologia delle Versioni

Vedi [CHANGELOG.md](CHANGELOG.md) per un elenco completo delle modifiche in ciascuna versione.

## Collaborazione

I contributi sono benvenuti! Leggi le nostre [Linee Guida per i Collaboratori](CONTRIBUTING.md) per i dettagli su come contribuire a questo progetto.

## 📄 Licenza

Questo progetto è concesso in licenza con la Licenza Pubblica Generale GNU v3.0 - vedi il file [LICENZA](LICENZA) per i dettagli.

## 🙏 Ringraziamenti

- Grazie a tutti i collaboratori che hanno contribuito a migliorare Cerca Duplicati PDF
- Sviluppato con ❤️ utilizzando Python e PyQt6

## 🐛 Bug Conosciuti

- La selezione della lingua non funziona

---

📅 **Ultimo Aggiornamento**: Agosto 2025  
🐍 **Versione Python**: 3.8+  
📜 **Licenza**: GPL-3.0
