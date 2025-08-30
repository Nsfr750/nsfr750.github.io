---
lang: it
lang-niv: fonto
lang-ref: 018-jbk
layout: page
title: 'OpenPGP'
---

# Documentazione dell'App OpenPGP GUI

Benvenuto nella documentazione ufficiale di **OpenPGP GUI App**.

## Panoramica
Questa applicazione fornisce un'interfaccia moderna e intuitiva per la gestione delle chiavi OpenPGP, crittografia, decrittografia, firma di messaggi, verifica e generazione di certificati SSL. Tutte le operazioni crittografiche vengono eseguite localmente per garantire la massima privacy.

# Funzionalità

- Interfaccia utente moderna con ttkbootstrap (tema Superhero)
- Genera, carica ed esporta coppie di chiavi OpenPGP
- Imposta nome, email, passphrase della chiave e visualizza l'impronta digitale
- Critta e decifra messaggi
- Firma e verifica messaggi (firme staccate)
- Esporta la chiave pubblica in formato ASCII-armor (.asc)
- Visualizza l'impronta digitale della chiave per i controlli di sicurezza
- Genera certificati SSL con CN personalizzato
- Pulisci/azzera tutti i campi con un clic
- **Sistema di registrazione centralizzato** (info, avvisi, errori, eccezioni non gestite)
- **Visualizzatore di log con filtraggio in tempo reale** (TUTTO, INFO, AVVISO, ERRORE)
- Usa `log_info`, `log_warning`, `log_error` per voci di log personalizzate
- Acquisizione e visualizzazione automatica dei traceback nel visualizzatore di log
- Barra dei menu dinamica con finestre di dialogo Informazioni, Aiuto, Visualizzatore Log, Sponsor, Versione
- Versionamento semantico e informazioni sulla versione
- Struttura modulare (`struttura`, `gui`, ecc.)
- Facilità di estensione e personalizzazione del tema (tramite ttkbootstrap)

# Guida Rapida

## Requisiti
- Python 3.9 o superiore
- PySide6 (incluso nei requisiti)
- pgpy (incluso nei requisiti)
- cryptography (incluso nei requisiti)
- pyperclip (incluso nei requisiti)

> **Nota**: L'applicazione è stata migrata da Tkinter/ttkbootstrap a PySide6 per un'interfaccia utente più moderna e mantenibile.

## Installazione
1. Clona o scarica questo repository.
2. (Facoltativo) Crea un ambiente virtuale:
   ```
   python -m venv venv
   venv\Scripts\activate
   ```
3. Installa le dipendenze:
   ```
   pip install -r requirements.txt
   ```

## Esecuzione dell'App
Esegui dalla radice del progetto:
```
python main.py
```

Se vedi errori di importazione, assicurati di eseguire dalla radice e non da una sottocartella.

# Guida Utente

## Panoramica della Finestra Principale
- Inserisci nome, email e passphrase per la generazione della chiave.
- Seleziona l'algoritmo (attualmente RSA; altri in arrivo).
- Usa i pulsanti per generare, caricare o esportare le chiavi.
- Viene mostrata l'impronta digitale della chiave caricata/generata per la verifica.
- Usa l'area di testo per inserire messaggi da crittografare, decifrare, firmare o verificare.
- Esporta la tua chiave pubblica per condividerla in modo sicuro.
- Genera certificati SSL dall'interfaccia grafica.
- Usa il pulsante 'Pulisci' per azzerare tutti i campi.

## Barra dei Menu
- **File**: Esporta chiave pubblica, Esci
- **Log**: Visualizza log (con filtri per TUTTO, INFO, AVVISO, ERRORE)
- **Aiuto**: Guida, Informazioni, Sponsor

## Registrazione e Visualizzatore Log
- Tutte le informazioni, avvisi, errori ed eccezioni non gestite vengono registrati automaticamente.
- Usa `log_info(msg)`, `log_warning(msg)`, `log_error(msg)` nei tuoi script per voci di log personalizzate.
- Il Visualizzatore Log (Log > Visualizza Log) ti consente di filtrare e visualizzare i log per livello.
- Se il file di log è mancante, viene mostrato l'ultimo traceback di runtime disponibile.

## Suggerimenti
- Tutte le operazioni crittografiche sono locali (nessun cloud).
- Per i migliori risultati, utilizza passphrase complesse.
- La finestra dei log fornisce feedback e dettagli sugli errori.

# Utilizzo Avanzato

## Esportazione Chiavi Pubbliche
- Usa il pulsante 'Esporta Chiave Pubblica' o la voce di menu per salvare la tua chiave pubblica in formato ASCII-armor (.asc).

## Verifica dell'Impronta Digitale
- Controlla sempre l'impronta digitale prima di condividere la tua chiave pubblica per una maggiore sicurezza.

## Generazione Certificati SSL
- Inserisci il Nome Comune (CN) desiderato nel campo nome.
- Fai clic sul pulsante 'Genera Certificato SSL' per creare un certificato autofirmato.

## Estensione dell'Applicazione
- Puoi aggiungere il supporto per più algoritmi (ECC, Ed25519) estendendo la logica di generazione delle chiavi in `main_window.py`.
- L'interfaccia grafica utilizza ttkbootstrap per una facile personalizzazione del tema.

## Registrazione e Debug
- Tutte le azioni, avvisi, errori ed eccezioni non gestite vengono registrati in `traceback.log`.
- Usa `log_info`, `log_warning`, `log_error` per voci di log personalizzate nel tuo codice.
- Il Visualizzatore Log supporta il filtraggio per TUTTO, INFO, AVVISO, ERRORE.
- Le eccezioni non gestite vengono registrate automaticamente e mostrate nel Visualizzatore Log (con traceback).

## Risoluzione dei Problemi
- Se incontri errori di importazione, assicurati di eseguire dalla radice del progetto.
- Per problemi con le dipendenze, controlla `requirements.txt` o reinstalla i pacchetti necessari.

# Guida per Sviluppatori

Benvenuto, sviluppatore! Questa guida fornisce le informazioni essenziali per contribuire e estendere l'App OpenPGP GUI.

---

## Struttura del Progetto
- `main.py` — Punto di ingresso, avvia la finestra principale.
- `gui/` — Tutti i componenti dell'interfaccia grafica (finestra principale, widget, finestre di dialogo).
- `struttura/` — Logica principale, finestre di dialogo, utilità, gestione versioni, aiuto/informazioni, ecc.
- `docs/` — Documentazione.
- `requirements.txt` — Dipendenze Python.

## Tecnologie Chiave
- **Python 3.x**
- **Tkinter** — Framework per l'interfaccia grafica (con ttkbootstrap per i temi)
- **pgpy** — Crittografia OpenPGP
- **cryptography** — Generazione di certificati SSL
- **Pillow** — (opzionale) per le icone

## Come Contribuire
1. Effettua un fork e clona il repository.
2. Crea un ambiente virtuale e installa le dipendenze.
3. Segui le linee guida PEP8 e mantieni il codice modulare.
4. Documenta le nuove funzionalità e aggiorna `CHANGELOG.md`.
5. Aggiungi o aggiorna i test se possibile.
6. Apri una pull request con una descrizione chiara.

## Aggiunta di Funzionalità
- Per aggiungere nuovi algoritmi (es. ECC), estendi la logica di generazione delle chiavi in `main_window.py`.
- Per nuovi componenti dell'interfaccia, aggiungi widget in `gui/` e mantieni la logica separata dall'interfaccia.
- Usa gli stili `ttkbootstrap` per un aspetto coerente.

## Test
- Aggiungi test per nuove funzionalità e correzioni di bug.
- Test manuale: esegui `python main.py` e utilizza tutte le funzioni dell'interfaccia.
- (Opzionale) Integra con CI/CD per test automatizzati.

## Stile del Codice
- Segui le linee guida PEP8.
- Usa i docstring per funzioni/classi pubbliche.
- Mantieni l'interfaccia e la logica il più separate possibile.

## Registrazione e Debug
- Usa `log_info(msg)`, `log_warning(msg)`, `log_error(msg)` ovunque nel codice per voci di log personalizzate.
- Tutti i log vengono salvati in `traceback.log` e mostrati nel Visualizzatore Log.
- Il Visualizzatore Log supporta il filtraggio per TUTTO, INFO, AVVISO, ERRORE.
- Le eccezioni non gestite vengono registrate automaticamente e mostrate nel Visualizzatore Log (con traceback).

## Supporto e Domande
- Apri issue su GitHub per segnalare bug o richiedere funzionalità.
- Vedi `README.md` per informazioni sui contatti e i contributi.

---

## Argomenti Avanzati

### Riferimento API

L'applicazione è modulare: la logica principale è in `struttura/`, l'interfaccia grafica in `gui/`.

**Classi e funzioni principali:**
- `MainWindow` (`gui/main_window.py`): Logica principale dell'interfaccia e gestione eventi.
- `gen_key`, `export_pubkey`, `clear_fields`, ecc.: Metodi per le operazioni crittografiche.
- `Help`, `About`, `LogViewer`, ecc.: Finestre di dialogo e utilità in `struttura/`.
- `get_version()` (`struttura/version.py`): Restituisce la stringa della versione corrente.

Per maggiori informazioni, leggi i docstring nel codice e consulta `docs/user_guide.md` per il flusso di utilizzo.

### Esempi di Estensione

#### Aggiunta di un Nuovo Algoritmo di Chiave
1. In `gui/main_window.py`, individua il menu a tendina per la selezione dell'algoritmo.
2. Aggiungi il tuo nuovo algoritmo (es. ECC, Ed25519) alle opzioni del menu a tendina.
3. Nella logica di generazione delle chiavi, implementa la gestione per il nuovo algoritmo utilizzando `pgpy`.
4. Esegui test accurati e aggiorna la documentazione.

#### Aggiunta di un Widget Personalizzato
1. Crea il tuo widget in `gui/widgets.py` o in un nuovo file.
2. Importalo e utilizzalo in `main_window.py` dove necessario.
3. Segui le convenzioni di stile ttkbootstrap per la coerenza.

### Diagramma Architetturale

Di seguito una panoramica testuale dell'architettura:

```
OpenPGP GUI App
│
├── main.py (punto di ingresso)
│
├── gui/
│   ├── main_window.py (classe MainWindow, logica eventi)
│   ├── widgets.py (widget personalizzati)
│   └── ...
│
├── struttura/
│   ├── help.py, about.py, version.py (finestre di dialogo, gestione versioni)
│   ├── menu.py (logica barra dei menu)
│   └── ...
│
├── docs/ (documentazione)
├── requirements.txt
└── ...
```

Per un diagramma visivo, vedi [docs/architecture.png](architecture.png) (aggiungi il tuo PNG per maggiori dettagli).

# Domande Frequenti

**D: Posso usare questa app senza connessione internet?**  
R: Sì! Tutte le operazioni crittografiche vengono eseguite localmente per la privacy.

**D: Come posso esportare la mia chiave pubblica?**  
R: Usa il pulsante 'Esporta Chiave Pubblica' o la voce di menu nel menu File.

**D: Quali algoritmi sono supportati?**  
R: Attualmente RSA; altri (ECC, Ed25519) sono in programma.

**D: Dove vengono memorizzate le mie chiavi?**  
R: Le chiavi vengono salvate solo dove decidi tu. Nessun caricamento automatico o archiviazione cloud.

**D: Come posso ottenere aiuto?**  
R: Usa il menu Aiuto o leggi la documentazione nella cartella docs/.
