---
lang: it
lang-niv: fonto
lang-ref: 023-jbk
layout: doc
order: 14 # Opzionale: per l'ordinamento nel menu
title: 'benchmark'
---

[![Licenza: GPL v3](https://img.shields.io/badge/Licenza-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Stile del codice: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Uno strumento di benchmarking Python moderno realizzato con PySide6, che fornisce un'interfaccia utente intuitiva per eseguire e analizzare test Pystone e altri benchmark.

## 📥 Installazione

### Prerequisiti

- Python 3.9 o superiore
- Windows o Linux

### Avvio rapido

1. Clona il repository:

   ```bash
   git clone https://github.com/Nsfr750/benchmark.git
   cd benchmark
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

## ✨ Funzionalità

- **Interfaccia utente moderna**: Interfaccia pulita e reattiva realizzata con PySide6
- **Benchmark completo**:
  - Durata del test personalizzabile
  - Monitoraggio del progresso in tempo reale
  - Risultati dettagliati con statistiche
  - Confronto con dati storici
- **Registrazione**:
  - Log dettagliati delle operazioni
  - Filtraggio dei log per livello
  - Rotazione automatica dei file di log
- **Supporto multilingua**:
  - Inglese (en)
  - Italiano (it)
- **Accessibilità**:
  - Scorciatoie da tastiera
  - Modalità ad alto contrasto
  - Dimensione del testo regolabile

## ⌨️ Scorciatoie da tastiera

- `Ctrl+L`: Visualizza i log dell'applicazione
- `F1`: Mostra la guida
- `Esc`: Chiudi le finestre di dialogo
- `Ctrl+Q`: Esci dall'applicazione

## 📊 Utilizzo

1. Imposta il numero di iterazioni per il benchmark
2. Fai clic su "Avvia Benchmark" per iniziare
3. Monitora l'avanzamento in tempo reale
4. Visualizza i risultati dettagliati e le statistiche
5. Accedi ai log per la risoluzione dei problemi

## 📂 Struttura del progetto

```
benchmark/
├── .github/                            # GitHub Actions
│   ├── workflows/                      # Workflow di GitHub Actions
│   │   └── ci-cd.yml                   # Pipeline CI/CD
│   ├── issues/                         # Issue di GitHub
│   |   └── templates/                  # Modelli per le issue di GitHub
│   └── FUNDING.yml                     # File di finanziamento
├── assets/                             # File delle risorse
├── config/                             # File di configurazione
│   ├── config.json                     # File di configurazione
│   └── updates.json                    # Cache degli aggiornamenti
├── docs/                               # Documentazione
│   ├── images/                         # Immagini della documentazione
│   ├── pdf/                            # Documentazione in PDF
│   └── USER_GUIDE.md                   # Guida utente
├── lang/                               # File delle lingue
│   ├── en.json                         # File in inglese
│   └── it.json                         # File in italiano
├── logs/                               # File di log
├── script/                             # Codice sorgente
│   ├── __init__.py                     # Inizializzazione del pacchetto
│   ├── about.py                        # Finestra "Informazioni su"
│   ├── benchmark_history.py            # Cronologia dei benchmark
│   ├── benchmark_tests.py              # Test di benchmark
│   ├── CLI_pystone.py                  # Benchmark Pystone da riga di comando
│   ├── config_manager.py               # Gestore della configurazione
│   ├── export_results.py               # Esportazione risultati
│   ├── hardware_monitor.py             # Monitor hardware
│   ├── help.py                         # Finestra di aiuto
│   ├── history_dialog.py               # Finestra della cronologia
│   ├── lang_mgr.py                     # Gestore delle lingue
│   ├── logger.py                       # Configurazione dei log
│   ├── menu.py                         # Funzionalità della barra dei menu
│   ├── settings.py                     # Finestra delle impostazioni
│   ├── sponsor.py                      # Finestra degli sponsor
│   ├── system_info.py                  # Informazioni di sistema
│   ├── test_menu.py                    # Menu dei test
│   ├── theme_manager.py                # Gestore dei temi
│   ├── updates.py                      # Sistema di aggiornamento
│   ├── version.py                      # Sistema di versioning
│   ├── view_log.py                     # Visualizzatore di log
│   └── visualization.py                # Visualizzazione dei benchmark
├── tests/                              # File di test
│   ├── test_benchmark.py               # Test del benchmark
│   ├── test_hardware_monitor.py        # Test del monitor hardware
│   ├── test_monitor_manual.py          # Test manuale del monitor
│   ├── test_monitor.py                 # Test del monitor
│   └── TEST_README.md                  # README dei test
├── .gitignore                          # File .gitignore
├── CHANGELOG.md                        # Registro delle modifiche
├── CONTRIBUTING.md                     # Linee guida per i contributi
├── LICENSE                             # File della licenza GPLv3
├── main.py                             # Applicazione principale
├── README.md                           # Questo file
├── requirements.txt                    # File delle dipendenze
└── TO_DO.md                            # Lista delle cose da fare
```
