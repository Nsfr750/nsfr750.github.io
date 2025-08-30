---
lang: it
lang-niv: fonto
lang-ref: 020-jbk
layout: page
title: 'PySnoop'
---

# PySnoop

[![Licenza: GPL v3](https://img.shields.io/badge/Licenza-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.7+](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/)
[![Stile del codice: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Un'applicazione moderna basata su Python per leggere, scrivere e analizzare i dati delle carte a striscia magnetica. Questo progetto è una continuazione del progetto originale StripeSnoop, ricostruito con Python moderno e un'interfaccia utente intuitiva.

## ✨ Funzionalità

- **Lettura Carte**: Leggi le carte a striscia magnetica utilizzando lettori compatibili
- **Gestione Database**: Archivia e gestisci in modo sicuro i dati delle carte
- **Multi-formato**: Esporta/Importa i dati delle carte in vari formati
- **Interfaccia Grafica Moderna**: Interfaccia utente intuitiva con supporto ai temi
- **Cross-Platform**: Funziona su Windows, macOS e Linux
- **Eseguibile Autonomo**: Compilabile come singolo file eseguibile per una facile distribuzione
- **Build di Debug**: Configurazione speciale per la risoluzione dei problemi
- **Sicurezza**: Archiviazione sicura per i dati sensibili delle carte
- **Validazione**: Validazione integrata dei numeri di carta (C10/Luhn)
- **Documentazione**: Documentazione completa ed esempi

## 🚀 Installazione

### Prerequisiti

- Python 3.7 o superiore
- pip (gestore pacchetti Python)
- Git (opzionale, per lo sviluppo)

### Guida Rapida

1. Clona il repository:

   ```bash
   git clone https://github.com/Nsfr750/PySnoop.git
   cd PySnoop
   ```

2. Crea e attiva un ambiente virtuale:

   ```bash
   # Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Installa le dipendenze:

   ```bash
   pip install -r requirements.txt
   ```

## 🏗️ Compilazione dell'Applicazione

PySnoop può essere compilato in un eseguibile autonomo utilizzando Nuitka. Forniamo due script di compilazione:

### Build di Debug

```bash
.\snoop_debug.bat
```

Crea una versione di debug dell'applicazione con la finestra della console abilitata per la risoluzione dei problemi.

### Build di Rilascio

```bash
.\snoop.bat
```

Crea una versione ottimizzata dell'applicazione per il rilascio.

### Output della Compilazione

- Build di debug: `build\PySnoop_debug.exe`
- Build di rilascio: `build\PySnoop.exe`

## 🛠️ Sviluppo
   ```bash
   pip install -r requirements.txt
   ```

## 💻 Utilizzo

### Modalità Grafica (Consigliata)

```bash
python pysnoop_gui.py
```

### Interfaccia a Riga di Comando

```bash
python pysnoop.py [opzioni]
```

### Opzioni Disponibili

```bash
-h, --help      Mostra il messaggio di aiuto ed esci
-v, --verbose   Abilita l'output dettagliato
--version       Mostra le informazioni sulla versione
```

## 🔌 Dispositivi Supportati

- Lettore/Scrittore di Carte a Banda Magnetica MSR605
- Altri lettori di carte compatibili HID (sperimentale)

## 📚 Documentazione

Per la documentazione dettagliata, inclusi i riferimenti alle API e esempi di utilizzo, visita la [documentazione](https://nsfr750.github.io/PySnoop/ "Documentazione di PySnoop").

## 🤝 Collaborazione

I contributi sono benvenuti! Leggi le nostre [linee guida per i contributi](CONTRIBUTING.md) per iniziare.

## 📄 Licenza

Questo progetto è concesso in licenza con la Licenza GPLv3 - vedi il file [LICENZA](LICENZA) per i dettagli.

## 🙏 Supporto

Se trovi utile questo progetto, considera di supportarne lo sviluppo:

[![Dona tramite PayPal](https://img.shields.io/badge/Dona-PayPal-blue.svg)](https://paypal.me/3dmega)
[![Diventa un Patreon](https://img.shields.io/badge/Supporto-Patreon-orange.svg)](https://www.patreon.com/Nsfr750)

## 📧 Contatti

Per domande o supporto, apri una issue o contatta [Nsfr750](mailto:nsfr750@yandex.com).

## Crediti

- Basato sul progetto originale StripeSnoop (http://stripesnoop.sourceforge.net)

## Collaborazione

I contributi sono benvenuti! Sentiti libero di inviare una Pull Request.
