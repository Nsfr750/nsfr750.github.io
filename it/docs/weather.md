---
lang: it
lang-niv: fonto
lang-ref: 022-jbk
layout: page
title: 'Meteo'
---

# Documentazione dell'App Meteo (v1.6.0)

Benvenuti nella documentazione dell'App Meteo! Questa applicazione fornisce informazioni meteorologiche in tempo reale e previsioni da molteplici fornitori di dati meteo.

## Funzionalità

- 🌦️ Condizioni meteo attuali con metriche dettagliate
- 📅 Previsioni meteo a 7 giorni con dettagli orari
- 📖 Visualizzatore di documentazione integrato in Markdown
- 📊 Visualizzatore di log dell'applicazione per la diagnostica
- 🌍 Supporto per più fornitori di dati meteo
- 🌐 Supporto multilingua
- ⭐ Località preferite con cronologia avanzata
- ⚙️ Impostazioni e temi personalizzabili

## Aggiornamenti Recenti

Per un elenco dettagliato delle modifiche, consultare il file [CHANGELOG.md](CHANGELOG.md).

## Per Iniziare

1. [Guida all'Installazione](installazione.md) - Come installare e configurare l'applicazione
2. [Guida Utente](utilizzo.md) - Come utilizzare l'applicazione
3. [Configurazione](configurazione.md) - Come configurare l'applicazione

## Argomenti Avanzati

- [Fornitori Meteo](fornitori.md) - Informazioni sui fornitori di dati meteo supportati
- [Traduzioni](traduzioni.md) - Come aggiungere o modificare le traduzioni
- [Guida allo Sviluppo](sviluppo.md) - Come contribuire al progetto
- [Risoluzione dei Problemi](risoluzione_problemi.md) - Problemi comuni e soluzioni

## Supporto

Per supporto, apri un'issue sul nostro [repository GitHub](https://github.com/Nsfr750/weather).

## Licenza

Questo progetto è concesso in licenza con la licenza GPLv3 - vedere il file [LICENZA](https://github.com/Nsfr750/weather/blob/main/LICENSE) per i dettagli.

# Guida Utente

## Per Iniziare

1. **Avvia l'Applicazione**
   - Fai doppio clic sull'icona dell'applicazione o eseguila dalla riga di comando
   - Si aprirà la finestra principale con il meteo della località predefinita
   - Al primo avvio, verrai guidato attraverso la configurazione iniziale

2. **Cerca una Località**
   - Digita il nome di una città nella barra di ricerca
   - Premi Invio o fai clic sul pulsante di ricerca (🔍)
   - Per risultati più precisi, includi il codice paese (es. "Roma, IT")
   - Fai clic destro sulla mappa per selezionare una posizione

## Interfaccia Principale

### Visualizzazione Meteo

- **Meteo Attuale**: Mostra temperatura, condizioni e dettagli aggiuntivi
  - Fai clic su qualsiasi metrica per passare da un'unità all'altra (es. °C/°F, km/h/mph)
  - Passa il mouse sulle icone per maggiori informazioni

- **Previsioni a 7 Giorni**: Mostra le previsioni meteo per i prossimi 7 giorni
  - Fai clic su un giorno per vedere le previsioni orarie
  - Probabilità di precipitazioni con codifica a colori
  - Include intervalli di temperatura e condizioni meteo per ogni giorno

- **Dettagli Meteo**: Include:
  - Temperatura percepita
  - Umidità e punto di rugiada
  - Velocità e direzione del vento
  - Pressione e visibilità
  - Indice UV e qualità dell'aria
  - Orari di alba e tramonto

### Navigazione

- **Barra di Ricerca**: Trova il meteo per qualsiasi località
  - Le ricerche recenti vengono salvate automaticamente
  - Cerca per nome città, CAP o coordinate

- **Tema**: Passa tra tema chiaro, scuro o sistema

- **Menu**: Accedi a funzionalità aggiuntive e impostazioni
  - File: Nuova finestra, impostazioni, esci
  - Visualizza: Mostra/nascondi elementi dell'interfaccia, aggiorna dati, mappe meteo e radar
  - Preferiti: Gestisci le località salvate
  - Aiuto: Visualizzatore documentazione, visualizzatore log, informazioni, verifica aggiornamenti

## Mappe Meteo e Radar

La funzione Mappe Meteo e Radar fornisce visualizzazioni interattive delle condizioni meteorologiche.

### Accesso alle Mappe Meteo

1. Fai clic su **Visualizza** nella barra dei menu
2. Seleziona **Mappe Meteo e Radar**
3. Si aprirà la finestra Mappe Meteo con più schede

### Funzionalità

#### Scheda Radar
- **Tipo Mappa**: Passa tra diverse mappe di base (OpenStreetMap, OpenTopoMap, Stamen Terrain)
- **Livello**: Attiva/disattiva sovrapposizioni radar e satellitari
- **Cerca**: Trova località per nome o coordinate

#### Scheda Temperatura
- Visualizza le variazioni di temperatura tra le regioni
- Passa tra Celsius e Fahrenheit
- Regola l'opacità della sovrapposizione temperatura

#### Scheda Precipitazioni
- Visualizza le precipitazioni attuali e previste
- Attiva/disattiva diversi livelli di precipitazioni
- Visualizza pioggia, neve e altri tipi di precipitazioni

#### Scheda Vento
- Visualizza velocità e direzione del vento
- Attiva/disattiva le frecce del vento o le linee di flusso
- Regola le unità di velocità del vento (km/h, m/s, mph, nodi)

### Utilizzo della Mappa
- **Zoom**: Usa la rotellina del mouse o i pulsanti +/-
- **Panoramica**: Fai clic e trascina la mappa
- **Ricerca**: Inserisci una località nella barra di ricerca e premi Invio
- **Livelli**: Attiva/disattiva diversi livelli meteo
- **Schermo intero**: Fai clic sul pulsante a schermo intero per una visualizzazione più ampia

### Suggerimenti
- La mappa si centrerà automaticamente sulla tua posizione se i servizi di localizzazione sono attivi
- Fai clic sulla mappa per ottenere informazioni meteo dettagliate per quella posizione
- Usa i controlli della linea temporale per visualizzare i dati delle previsioni in momenti diversi
- Fai clic destro sulla mappa per impostare un segnaposto o ottenere le coordinate

## Funzionalità

### Preferiti

- **Aggiungi ai Preferiti**: Fai clic sulla stella (☆) per salvare una località
- **Visualizza Preferiti**: Accedi alle località salvate dal menu Preferiti
  - Riordina i preferiti con il trascinamento
  - Fai clic destro per azioni rapide
- **Sincronizza Preferiti**: Attiva la sincronizzazione cloud nelle impostazioni
- **Rimuovi dai Preferiti**: Fai clic sulla stella piena (★) per rimuovere

### Impostazioni

1. Fai clic sull'icona dell'ingranaggio (⚙️) o vai su Menu > Impostazioni
2. Configura opzioni come:
   - **Generale**: Lingua, tema, unità di misura
   - **Meteo**: Impostazioni del fornitore, frequenza di aggiornamento
   - **Visualizzazione**: Layout, animazioni, dimensione carattere
   - **Notifiche**: Avvisi meteo, avvisi pioggia
   - **Avanzate**: Cache, registrazione, opzioni sviluppatore
3. Fai clic su "Salva" per applicare le modifiche

### Interfaccia a Righe di Comando

```bash
# Utilizzo di base
app-meteo [località] [opzioni]

# Esempi
app-meteo "Roma, IT"
app-meteo --provider openweathermap --units metric
app-meteo --config ~/.config/meteo/config.ini

# Opzioni
  -h, --help            Mostra il messaggio di aiuto ed esci
  -v, --version         Mostra informazioni sulla versione
  -c, --config FILE     Specifica il file di configurazione
  -d, --debug           Abilita la modalità debug
  --provider FORNITORE  Imposta il fornitore meteo
  --units {metric,imperial}
                        Imposta il sistema di unità
  --lang LINGUA         Imposta il codice lingua
  --theme {chiaro,scuro,sistema}
                        Imposta il tema colore
  --no-gui              Esegui in modalità console
```

## Scorciatoie da Tastiera

### Scorciatoie Globali

| Scorciatoia | Azione |
|-------------|--------|
| `Ctrl + F` | Attiva la barra di ricerca |
| `Ctrl + ,` | Apri Impostazioni |
| `Ctrl + Q` | Esci dall'applicazione |
| `F1` | Mostra Aiuto |
| `Esc` | Chiudi le finestre o cancella la ricerca |
| `F5` | Aggiorna i dati meteo |
| `Ctrl + R` | Aggiorna tutti i dati |
| `Ctrl + W` | Chiudi la finestra corrente |
| `Ctrl + N` | Nuova finestra |

### Scorciatoie di Navigazione

| Scorciatoia | Azione |
|-------------|--------|
| `Ctrl + Tab` | Passa tra le località |
| `Ctrl + F` | Mostra/nascondi preferiti |
| `Ctrl + L` | Mostra/nascondi elenco località |
| `Ctrl + M` | Mostra/nascondi vista mappa |

## Suggerimenti e Trucchi

- **Clic destro** su qualsiasi scheda meteo per azioni rapide
- **Doppio clic** sulla temperatura per passare tra Celsius e Fahrenheit
- **Clic centrale** sulla mappa per impostare una posizione personalizzata
- Usa la **rotellina del mouse** sulle previsioni per scorrere tra le ore
- **Trascina e rilascia** per riordinare le località preferite
- **Appunta** la finestra per tenerla in primo piano
- Usa l'**icona nella barra delle applicazioni** per un accesso rapido

### Visualizzatore Documentazione

- Accedi alla documentazione integrata in Markdown dal menu Aiuto
- Sfoglia la documentazione completa
- Funzionalità di ricerca per trovare argomenti specifici
- Zoom avanti/indietro per una migliore leggibilità
- Indice per una navigazione semplice

### Visualizzatore Log

- Visualizza i log dell'applicazione dal menu Aiuto
- Filtra i log per livello (Debug, Info, Avviso, Errore)
- Cerca tra i messaggi di log
- Copia i log negli appunti per la risoluzione dei problemi

### Mappe Meteo
- Accedi alle mappe meteo dal menu Visualizza
- Mappa interattiva con più livelli:
  - Temperatura
  - Precipitazioni
  - Velocità del vento
  - Copertura nuvolosa
- Sposta e zoomma per esplorare diverse regioni
- Fai clic sulla mappa per ottenere il meteo per quella posizione

## Risoluzione dei Problemi

Se riscontri problemi:
1. Controlla la connessione Internet
2. Verifica le tue chiavi API nelle Impostazioni
3. Prova a passare a un fornitore meteo diverso
4. Controlla i log dell'applicazione per errori
5. Riavvia l'applicazione
6. Reimposta le impostazioni se necessario

Per ulteriore aiuto, visita il nostro [repository GitHub](https://github.com/Nsfr750/weather) o consulta la [Guida alla Risoluzione dei Problemi](risoluzione_problemi.md).

## Feedback

Accogliamo con favore il tuo feedback! Facci sapere:
- Quali funzionalità vorresti vedere
- Eventuali bug che riscontri
- La tua esperienza con l'applicazione

Puoi inviare feedback tramite l'applicazione (Aiuto > Invia Feedback) o sulla nostra pagina [GitHub Issues](https://github.com/Nsfr750/weather/issues).

# Guida alla Risoluzione dei Problemi

Questa guida ti aiuta a risolvere i problemi comuni che potresti incontrare utilizzando l'App Meteo.

## Indice
- [Problemi Comuni](#problemi-comuni)
- [File di Log](#file-di-log)
- [Debug](#debug)
- [Problemi di Prestazioni](#problemi-di-prestazioni)
- [Domande Frequenti](#domande-frequenti)
- [Ottenere Aiuto](#ottenere-aiuto)

## Problemi Comuni

### 1. L'Applicazione Non Si Avvia

**Sintomi**:
- L'applicazione si chiude immediatamente dopo l'avvio
- Viene visualizzato un messaggio di errore su dipendenze mancanti
- La finestra dell'applicazione non appare

**Soluzioni**:
1. **Verifica i Requisiti di Sistema**:
   - Assicurati di avere Python 3.10 o successivo installato
   - Verifica che tutte le dipendenze di sistema siano installate
   - Controlla lo spazio su disco e i permessi

2. **Reinstalla le Dipendenze**:
   ```bash
   # Attiva prima il tuo ambiente virtuale
   pip install --upgrade -r requirements.txt
   ```

3. **Controlla Software in Conflitto**:
   - Disattiva temporaneamente l'antivirus/firewall
   - Chiudi altre applicazioni che potrebbero essere in conflitto

4. **Reimposta la Configurazione**:
   ```bash
   # Prima fai un backup della configurazione
   mv ~/.config/AppMeteo/config.ini ~/.config/AppMeteo/config.ini.bak
   ```

### 2. Nessun Dato Meteo Visualizzato

**Sintomi**:
- L'app si apre ma mostra "Nessun dato disponibile"
- Le informazioni meteo non si aggiornano
- Impossibile trovare la località

**Soluzioni**:
1. **Controlla la Connessione Internet**:
   - Verifica che il dispositivo sia connesso a Internet
   - Prova ad accedere a un sito web nel browser

2. **Verifica le Chiavi API**:
   - Controlla se la tua chiave API è valida e non scaduta
   - Assicurati che la chiave API abbia i permessi corretti
   - Prova a rigenerare la chiave API

3. **Stato del Fornitore**:
   - Verifica se il servizio meteo sta avendo problemi
   - Prova a passare a un fornitore meteo diverso

4. **Servizi di Localizzazione**:
   - Assicurati che i servizi di localizzazione siano attivi
   - Prova a inserire manualmente la località

### 3. Utilizzo Elevato di CPU o Memoria

**Sintomi**:
- L'app diventa lenta o non risponde
- La ventola del computer si attiva rumorosamente
- Altre applicazioni diventano lente

**Soluzioni**:
1. **Riduci la Frequenza di Aggiornamento**:
   - Aumenta l'intervallo di aggiornamento in Impostazioni > Meteo
   - Disattiva gli aggiornamenti automatici della posizione se non necessari

2. **Disattiva le Animazioni**:
   - Vai a Impostazioni > Visualizzazione
   - Disattiva "Abilita animazioni"

3. **Svuota la Cache**:
   ```bash
   # Linux/macOS
   rm -rf ~/.cache/AppMeteo
   
   # Windows
   rmdir /s /q %LOCALAPPDATA%\AppMeteo\Cache
   ```

4. **Controlla i Memory Leak**:
   - Monitora l'utilizzo della memoria nel Task Manager
   - Segnala qualsiasi crescita costante della memoria

## File di Log

I file di log contengono informazioni dettagliate sugli eventi e sugli errori dell'applicazione. Sono essenziali per la risoluzione dei problemi.

### Posizioni dei Log

- **Linux/macOS**: `~/.local/share/AppMeteo/logs/`
- **Windows**: `%APPDATA%\AppMeteo\logs\`
- **macOS**: `~/Library/Logs/AppMeteo/`

### Livelli di Log

- **DEBUG**: Informazioni dettagliate per il debug
- **INFO**: Eventi generali dell'applicazione
- **WARNING**: Situazioni potenzialmente problematiche
- **ERROR**: Errori che potrebbero permettere all'app di continuare
- **CRITICAL**: Errori gravi che causano l'arresto dell'app

### Visualizzazione dei Log

1. **Dall'Applicazione**:
   - Vai su Aiuto > Visualizza Log
   - Filtra per livello di log
   - Cerca termini specifici

2. **Da Righe di Comando**:
   ```bash
   # Linux/macOS
   tail -f ~/.local/share/AppMeteo/logs/app.log
   ```

## Documentazione Aggiuntiva

1. **Consulta la Documentazione**:
   - [Guida Utente](utilizzo.md)
   - [Configurazione](configurazione.md)
   - [Documentazione API](api.md)

## Domande Frequenti

### Come posso cambiare il fornitore di dati meteo?

Vai su Impostazioni > Meteo e seleziona il fornitore desiderato dall'elenco a discesa. Potrebbe essere necessario configurare una chiave API per alcuni fornitori.

### Posso usare l'applicazione senza connessione Internet?

L'applicazione richiede una connessione Internet per recuperare i dati meteo aggiornati. Tuttavia, alcune funzionalità di base potrebbero essere disponibili offline utilizzando i dati memorizzati nella cache.

### Come posso segnalare un bug o richiedere una funzionalità?

Puoi segnalare bug o richiedere nuove funzionalità aprendo una issue sul nostro [repository GitHub](https://github.com/Nsfr750/weather/issues). Per favore, includi quante più informazioni possibili, inclusi i passaggi per riprodurre il problema e i log rilevanti.

## Ottenere Aiuto

Se hai bisogno di ulteriore assistenza, non esitare a contattarci:

- **Forum della Community**: [Link al forum]
- **Email di Supporto**: supporto@esempio.com
- **Canale Discord**: [Link al server Discord]

Siamo qui per aiutarti a risolvere qualsiasi problema tu possa incontrare con l'App Meteo!
