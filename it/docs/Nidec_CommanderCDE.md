---
lang: it
lang-niv: fonto
lang-ref: 017-jbk
layout: page
title: 'Nidec CommanderCDE'
---

# Nidec CommanderCDE

Un'applicazione GUI Python completa per il controllo e il monitoraggio degli azionamenti Nidec Commander CDE tramite Modbus RTU.

## ✨ Funzionalità

- **Supporto multilingua**: Interfaccia completa in inglese e italiano con cambio lingua dinamico
- **Supporto multi-modello**: Compatibile con i modelli di azionamento CDE400, CDE550, CDE750 e CDE1100S
- **Controllo azionamento**:
  - Connessione agli azionamenti Nidec Commander CDE via RS-485/Modbus RTU
  - Controllo della velocità e della direzione del motore
  - Avvio/Arresto dell'azionamento
  - Monitoraggio in tempo reale dello stato e della diagnostica dell'azionamento
  - Rilevamento guasti e funzionalità di ripristino
  - Backup e ripristino dei parametri
- **Interfaccia utente**:
  - Interfaccia a schede moderna con controlli intuitivi
  - Dashboard completa con metriche in tempo reale
  - Barra di stato con informazioni su connessione e stato dell'azionamento
  - Design reattivo con supporto per temi Chiaro/Scuro
  - Elementi dell'interfaccia personalizzabili
- **Gestione dati**:
  - Monitoraggio e registrazione in tempo reale dei parametri dell'azionamento
  - Esportazione dati in CSV/Excel
  - Visualizzazione grafica delle tendenze dei parametri
  - Intervalli di registrazione dati configurabili
- **Diagnostica**:
  - Monitoraggio completo dei parametri
  - Cronologia guasti e registrazione
  - Indicatori di stato del sistema
  - Metriche delle prestazioni in tempo reale

## 🆕 Novità nella versione 0.0.4

### Nuove funzionalità
- Aggiunto supporto per più modelli di azionamento Nidec (CDE400, CDE550, CDE750, CDE1100S)
- Traduzione completa in italiano per tutti gli elementi dell'interfaccia
- Sistema di aiuto migliorato con documentazione dettagliata
- Tema blu per una migliore leggibilità nelle sezioni di aiuto

### Miglioramenti
- Interfaccia utente aggiornata per una migliore esperienza utente
- Messaggi di errore e registrazione migliorati
- Prestazioni ottimizzate per il monitoraggio in tempo reale
- Risolti problemi di compatibilità con PyQt6
- Risolto il cambio lingua nelle finestre di aiuto

## 🚀 Requisiti

- Python 3.8 o superiore
- PyQt6 >= 6.6.1
- pyserial >= 3.5
- pymodbus >= 3.5.4
- PyQt6-QScintilla >= 2.14.1
- python-dotenv >= 1.0.0

## 🛠 Installazione e Configurazione

1. Clona il repository:

   ```bash
   git clone https://github.com/Nsfr750/nidec-commandercde.git
   cd nidec-commandercde
   ```

2. Crea e attiva un ambiente virtuale (consigliato):

   ```bash
   python -m venv venv
   # Su Windows:
   .\venv\Scripts\activate
   # Su Unix o MacOS:
   # source venv/bin/activate
   ```

3. Installa i pacchetti richiesti:

   ```bash
   pip install -r requirements.txt
   ```

## 🚀 Utilizzo di Base

1. Collega il tuo azionamento Nidec Commander CDE al computer tramite adattatore RS-485
2. Avvia l'applicazione:

   ```bash
   python main.py
   ```

3. Seleziona la porta COM appropriata e la velocità in baud
4. Fai clic su 'Connetti' per stabilire la comunicazione con l'azionamento
5. Utilizza l'interfaccia per controllare e monitorare l'azionamento

## Impostazioni di Connessione

- Velocità in baud: 9600
- Bit di dati: 8
- Parità: Pari
- Bit di stop: 1
- Indirizzo Modbus: 1 (predefinito, può essere modificato nei parametri dell'azionamento)

## Note Importanti

- Questo software è fornito "così com'è" senza alcuna garanzia
- Assicurarsi sempre di effettuare le connessioni elettriche correttamente e di adottare le opportune misure di sicurezza quando si lavora con azionamenti per motori
- Gli indirizzi dei registri predefiniti si basano sulle configurazioni tipiche degli azionamenti Nidec ma potrebbero richiedere modifiche per il modello specifico in uso
- Fare riferimento al manuale Nidec CDE 400 Commander per informazioni dettagliate su parametri e indirizzi dei registri
