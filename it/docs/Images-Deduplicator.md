---
lang: it
lang-niv: fonto
lang-ref: 014-jbk
layout: doc
order: 5
title: 'Images Deduplicator'
---

# Images Deduplicator

Images Deduplicator è un'applicazione Python avanzata progettata per la gestione e la rimozione efficiente di immagini duplicate. Sfruttando la libreria Wand (ImageMagick) per l'elaborazione delle immagini, questo strumento offre tecniche avanzate di confronto visivo per identificare e gestire i duplicati con elevata precisione.

## Caratteristiche Principali

- **Elaborazione Avanzata delle Immagini**: Basata su Wand/ImageMagick per un supporto superiore dei formati immagine
- **Rilevamento Visivo dei Duplicati**: Utilizzo di hash percettivi per identificare immagini visivamente simili
- **Supporto Completo dei Formati**: Gestisce tutti i principali formati tra cui JPEG, PNG, WEBP, PSD e altri
- **Interfaccia Intuitiva**: Interfaccia grafica user-friendly con supporto per temi chiaro/scuro
- **Supporto Multilingua**: Internazionalizzazione integrata con inglese e italiano
- **Elaborazione in Batch**: Elabora efficientemente migliaia di immagini
- **Anteprima e Confronto**: Confronto affiancato delle immagini prima di intraprendere azioni
- **Operazioni Sicure**: Spostamento nel cestino invece di eliminazione definitiva
- **Registrazione Dettagliata**: Registrazione completa delle operazioni per la tracciabilità

## Requisiti di Sistema

- **Python**: 3.8 o superiore (consigliato 3.10+)
- **ImageMagick**: Richiesto per l'elaborazione delle immagini con Wand
  - Windows: Installare da [ImageMagick Windows](https://imagemagick.org/script/download.php#windows)
  - macOS: `brew install imagemagick`
  - Linux: `sudo apt-get install libmagickwand-dev`
- **Memoria**: Minimo 4GB, consigliati 8GB+ per grandi collezioni di immagini
- **Spazio di Archiviazione**: Spazio sufficiente per le immagini in elaborazione + file temporanei
- **Sistemi Operativi Supportati**:
  - Windows 10/11
  - macOS 10.15+
  - Linux con X11/Wayland

## Perché Wand/ImageMagick?

Images Deduplicator utilizza Wand (un binding Python per ImageMagick) per diversi vantaggi:

- Supporto più ampio di formati inclusi PSD, GIF e BMP
- Migliore gestione della memoria per immagini di grandi dimensioni
- Comportamento più coerente su diverse piattaforme
- Capacità avanzate di manipolazione delle immagini
- Manutenzione attiva e aggiornamenti di sicurezza

## Utilizzo

### Interfaccia Principale

L'applicazione presenta un'interfaccia moderna e intuitiva con i seguenti componenti principali:

1. **Barra dei Menu**: Accesso a tutte le funzioni e impostazioni dell'applicazione
2. **Barra degli Strumenti**: Accesso rapido alle funzioni più utilizzate
3. **Esplora Cartelle**: Naviga e seziona le directory da analizzare
4. **Pannello Anteprima**: Visualizza e confronta le immagini affiancate
5. **Pannello Risultati**: Mostra i duplicati trovati con punteggi di somiglianza
6. **Barra di Stato**: Mostra lo stato dell'operazione e le informazioni di sistema

### Flusso di Lavoro Base

1. **Seleziona la Cartella Sorgente**
   - Fai clic su "Apri Cartella" o usa `File > Apri Cartella`
   - L'applicazione scannerizzerà i formati immagine supportati
   - Formati supportati: JPEG, PNG, WEBP, PSD, BMP, GIF e altri (tramite Wand/ImageMagick)

2. **Configura le Impostazioni di Scansione**
   - Regola la soglia di somiglianza (predefinita: 90%)
   - Imposta la dimensione minima delle immagini da considerare
   - Scegli quali proprietà confrontare (dimensione, data, hash del contenuto)

3. **Avvia la Scansione**
   - Fai clic su "Avvia Scansione" per iniziare il rilevamento dei duplicati
   - Lo stato di avanzamento viene mostrato nella barra di stato
   - Puoi mettere in pausa o interrompere la scansione in qualsiasi momento

4. **Rivedi i Risultati**
   - I gruppi di duplicati vengono visualizzati con anteprime
   - Ordina per dimensione, data o punteggio di somiglianza
   - Usa lo strumento di confronto affiancato per la verifica

5. **Gestisci i Duplicati**
   - Seleziona le immagini da conservare o eliminare
   - Sposta i duplicati nel cestino (recuperabili) o eliminali definitivamente
   - Esporta i risultati in CSV/JSON per riferimento

### Funzionalità Avanzate

#### Elaborazione in Batch

- Elabora più cartelle in sequenza
- Salva e carica configurazioni di scansione
- Pianifica scansioni automatiche

#### Selezione Intelligente

- Selezione automatica di immagini in base a criteri (più vecchie, più piccole, ecc.)
- Mantieni la versione con la risoluzione più alta
- Conserva immagini con modelli di denominazione specifici

#### Strumenti di Confronto Immagini

- Modalità di confronto affiancato e in sovrapposizione
- Zoom e panoramica sincronizzati tra le immagini
- Confronto di istogrammi e dati EXIF

#### Filtri Personalizzati

- Filtra per dimensioni dell'immagine
- Filtra per data di creazione/modifica
- Filtra per formato immagine o profilo colore

#### Integrazione con Wand/ImageMagick

- Supporto avanzato per i formati immagine
- Migliore gestione dei profili colore e dei metadati
- Supporto per formati RAW delle fotocamere quando abilitato in ImageMagick

### Scorciatoie da Tastiera

| Scorciatoia  | Azione                           |
|--------------|----------------------------------|
| `Ctrl+O`    | Apri cartella                    |
| `Ctrl+F`    | Avvia nuova scansione            |
| `Spazio`    | Seleziona/deseleziona immagine corrente |
| `Canc`      | Sposta la selezione nel cestino  |
| `Ctrl+Z`    | Annulla l'ultima azione          |
| `F5`        | Aggiorna la vista                |

## Ottimizzazione delle Prestazioni

### Per Grandi Collezioni

- Utilizza la modalità "Confronto Rapido" per un filtraggio iniziale
- Aumenta la dimensione minima del file per saltare le miniature
- Pianifica le scansioni durante le ore di minore attività per grandi collezioni

### Gestione della Memoria

- Chiudi altre applicazioni che consumano molta memoria
- Regola i limiti delle risorse di ImageMagick se necessario (vedi Installazione)
- Elabora le immagini in lotti più piccoli

### Considerazioni sullo Spazio di Archiviazione

- Assicurati di avere spazio libero sufficiente per i file temporanei
- Elabora le immagini direttamente dall'unità sorgente quando possibile
- Considera l'utilizzo di un SSD veloce per prestazioni migliori

## Risoluzione dei Problemi

### Prestazioni Lente

- Controlla le impostazioni dei criteri di ImageMagick (vedi Installazione)
- Riduci il numero di operazioni concorrenti
- Disattiva l'anteprima in tempo reale per grandi collezioni

### Immagini Mancanti

- Verifica che ImageMagick supporti il formato dell'immagine
- Controlla i permessi dei file
- Cerca messaggi di errore nel visualizzatore di log

### Risultati Inaspettati

- Regola la soglia di somiglianza
- Verifica che i filtri non siano troppo restrittivi
- Controlla che i metadati delle vengano letti correttamente

## Configurazione

### Opzioni Principali

#### Precisione del Confronto

- **Livello di precisione (1-100)**:
  - Valori più bassi trovano più duplicati
  - Valori più alti trovano solo duplicati quasi identici

#### Dimensioni Minime

- **Ignora immagini al di sotto di**:
  - Larghezza minima (pixel)
  - Altezza minima (pixel)
  - Dimensione minima (KB)

#### Formati Supportati

- **Estensioni consentite**:
  - .jpg, .jpeg
  - .png
  - .gif
  - .bmp
  - .webp

#### Cartelle Escluse

- **Elenco delle cartelle da ignorare**:
  - Cartelle di sistema
  - Cartelle temporanee
  - Cartelle specifiche

### Suggerimenti per la Configurazione

1. **Precisione**
   - Livello 70-80 per un buon equilibrio
   - Livello 90+ per confronti molto rigorosi

2. **Memoria**
   - Monitora l'utilizzo della RAM
   - Riduci la cache se necessario

3. **Backup**
   - Salva sempre le configurazioni
   - Esporta i report prima di eliminare le immagini
