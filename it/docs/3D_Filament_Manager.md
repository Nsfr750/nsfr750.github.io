---
lang: it
lang-niv: fonto
lang-ref: 010-jbk
layout: page
title: '3D Filament Manager'
---

# 3D Filament Manager

![3D Filament Manager](assets/logo.png)

Un'applicazione desktop per gestire il tuo inventario di filamenti per stampa 3D. Tieni traccia di materiali, colori, utilizzo, costi e impostazioni del slicer in un unico posto.

## ✨ Funzionalità

* **🌐 Supporto multilingua**: Disponibile in inglese e italiano
* **🎨 Interfaccia utente moderna**: Interfaccia pulita con icone emoji e supporto per temi (modalità chiara/scura)
* **📊 Gestione completa dei filamenti**:
  * Memorizza informazioni dettagliate sui filamenti (marca, materiale, colore, diametro, ecc.)
  * Tieni traccia dell'utilizzo e della quantità rimanente
  * Calcola i costi del materiale
  * Monitoraggio prezzi e storico
  * Analisi interattiva dei prezzi con visualizzazioni
  * Confronto prezzi tra fornitori
* **⚙️ Integrazione con lo slicer**:
  * Salva e gestisci profili slicer (Cura, PrusaSlicer, eQuidiSlicer)
  * Profili di stampa personalizzati per diverse stampanti
* **🔍 Ricerca e filtraggio avanzati**:
  * Cerca per qualsiasi proprietà del filamento
  * Ordina per qualsiasi colonna
  * Filtra per tipo di materiale, colore o tag personalizzati
* **📂 Importa/Esporta**:
  * Esegui backup e ripristina la tua libreria di filamenti
  * Condividi profili con altri
  * Supporto per importazione/esportazione multipla
* **🔒 Sicurezza dei dati**:
  * Impostazioni salvate nella directory `config/`
  * Nessuna connessione internet richiesta
  * Archiviazione dati locale

## 🚀 Requisiti

* Python 3.8+
* Pacchetti richiesti (installati automaticamente):
  * `lxml` - Elaborazione XML veloce
  * `pillow` - Elaborazione immagini per le icone
  * `matplotlib` - Visualizzazione dati per l'analisi dei prezzi

## 🛠️ Installazione

### Prerequisiti

* Python 3.8 o superiore
* Git (opzionale, per lo sviluppo)

### Passaggi di installazione

1. **Clona il repository** (o scaricalo come ZIP):

   ```bash
   git clone https://github.com/Nsfr750/3D_Filament_Manager.git
   cd 3D_Filament_Manager
   ```

2. **Crea e attiva un ambiente virtuale** (consigliato):

   ```bash
   # Su Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # Su macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Installa le dipendenze**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Avvia l'applicazione**:

   ```bash
   python main.py
   ```

### Archiviazione dati

* I profili dei filamenti sono memorizzati nella directory `fdm/`
* Le impostazioni dell'applicazione sono salvate nella directory `config/`
* I log vengono scritti nella directory `logs/`

## 🤝 Contributi

Siamo aperti ai contributi! Ecco come puoi aiutare:

* Segnala bug aprendo una [issue](https://github.com/Nsfr750/3D_Filament_Manager/issues)
* Suggerisci nuove funzionalità o miglioramenti
* Invia pull request con modifiche al codice
* Aiuta a migliorare la documentazione
* Traduci l'applicazione in nuove lingue

### Configurazione per lo sviluppo

1. Fai un fork del repository
2. Crea un branch per la tua funzionalità (`git checkout -b feature/feature-straordinaria`)
3. Fai il commit delle tue modifiche (`git commit -m 'Aggiungi una funzionalità straordinaria'`)
4. Esegui il push sul branch (`git push origin feature/feature-straordinaria`)
5. Apri una Pull Request

### Stile del codice

* Segui le linee guida [PEP 8](https://www.python.org/dev/peps/pep-0008/)
* Usa i type hint per una migliore chiarezza del codice
* Scrivi docstring per tutte le funzioni e classi pubbliche

## 📜 Licenza

Questo progetto è concesso in licenza con la **GNU General Public License v3.0**. Vedi il file [LICENSE](LICENSE) per i dettagli.

## 🙏 Supporto

Se trovi utile questo progetto, considera di supportarne lo sviluppo:

* ⭐ Metti una stella al repository
* 🐛 Segnala problemi
* 💡 Suggerisci nuove funzionalità
* 💰 [Supporta il progetto su GitHub](https://github.com/sponsors/Nsfr750)

## 📞 Contatti

* GitHub: [@Nsfr750](https://github.com/Nsfr750)
* Email: nsfr750@yandex.com

---

### Supporta lo sviluppatore

Se trovi utile questa applicazione, per favore considera di supportare lo sviluppatore:

* **PayPal**: [https://paypal.me/3dmega](https://paypal.me/3dmega)
* **GitHub**: [https://github.com/Nsfr750](https://github.com/Nsfr750)
