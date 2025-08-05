
# Guida all'Installazione e all'Uso - Riconoscimento Emozioni Facciali


Questo file README fornisce le istruzioni passo dopo passo per configurare l'ambiente necessario e avviare il progetto di riconoscimento delle emozioni facciali in tempo reale tramite webcam.

---
### Prerequisito Fondamentale: Anaconda
---

L'intero progetto si basa sulla suite Anaconda. Se non l'hai già installata sul tuo computer, questo è il primo passo da compiere.

- **Azione:** Scarica e installa Anaconda dal sito ufficiale: https://www.anaconda.com/download
  (Scegli la versione adatta al tuo sistema operativo e segui le istruzioni di installazione).

---
### Fase 1: Preparazione dell'Ambiente e della Cartella di Lavoro
---

Per garantire che il progetto funzioni correttamente, è essenziale prima organizzare i file e poi creare un ambiente virtuale isolato.

**1. Organizzazione dei File**

Prima di aprire qualsiasi terminale, è fondamentale preparare la cartella di lavoro.

a. **Crea una cartella principale:** Sul tuo computer (ad esempio, sul Desktop), crea una nuova cartella vuota. Per chiarezza, chiamiamola `Cartella_Principale`.

b. **Inserisci il progetto:** Sposta l'intera cartella del progetto `Computer_Vision` (quella che ti ho fornito e che contiene tutti i file e le sottocartelle) **all'interno** di `Cartella_Principale`.

La tua struttura di file finale dovrà essere simile a questa:
`.../Desktop/Cartella_Principale/Computer_Vision/`

**2. Apri Anaconda Prompt e Naviga alla Cartella `Cartella_Principale`**

a. **Apri Anaconda Prompt:**
   - Su Windows: Cerca "Anaconda Prompt" nel menu Start.
   - Su macOS/Linux: Apri il terminale.

b. **Naviga alla cartella:**
   Usa il comando `cd` (change directory) per spostarti **direttamente dentro la cartella `Cartella_Principale`**.

   Esempio per Windows:
   `cd C:\Users\TuoNome\Desktop\Cartella_Principale`

**3. Crea l'Ambiente con un Singolo Comando**

Una volta che ti trovi *dentro* la cartella, esegui il seguente comando per creare l'ambiente virtuale e installare tutte le dipendenze in un colpo solo:

`conda env create -f Computer_Vision/environment.yml`

**Cosa fa questo comando?** Leggerà il file `environment.yml` (incluso nel progetto), creerà un nuovo ambiente virtuale chiamato `cv` e installerà automaticamente tutti i pacchetti necessari (TensorFlow, OpenCV, etc.). Il processo potrebbe richiedere alcuni minuti.

---
### Fase 2: Avvio dell'Applicazione di Riconoscimento Live
---

Una volta che l'ambiente è stato creato, sei pronto per avviare l'applicazione.

**1. Attiva l'Ambiente Virtuale**

Ogni volta che vuoi eseguire il progetto, devi prima spostarti nella 'Cartella_principale' e attivare l'ambiente corretto. Sempre da Anaconda Prompt, esegui:

`conda activate cv`

Noterai che il prompt dei comandi cambierà, mostrando `(cv)` all'inizio della riga. Questo indica che l'ambiente è attivo.

**2. Avvia Jupyter Notebook**

Assicurandoti di essere ancora nella cartella `Cartella_principale`, lancia Jupyter con il seguente comando:

`jupyter notebook`

Questo comando aprirà una nuova scheda nel tuo browser web, mostrandoti l'interfaccia di Jupyter con i file del progetto.

**3. Esegui l'Applicazione**

a. Nell'interfaccia di Jupyter, naviga nella sottocartella `live_webcam`.
b. Apri il file `Emotions_live_detector.ipynb`.
c. Esegui le celle del notebook (puoi farlo dal menu `Cell > Run All`).
d. Si aprirà una finestra che mostrerà il video della tua webcam con la rilevazione delle emozioni in tempo reale. Per chiudere l'applicazione, premi il tasto 'q' sulla tastiera.

---
### Note Aggiuntive
---

- **File del Progetto:** La cartella `Computer_Vision` contiene diversi file. Per eseguire la demo live, ti serve solo `Emotions_live_detector.ipynb`. Gli altri file (`Emotions_computer_vision.ipynb`, la cartella `dataset`, etc.) sono relativi al processo di preparazione dei dati e di addestramento della rete neurale.

- **Modello Addestrato:** L'applicazione live utilizza un modello già addestrato (`emotion_detector_model.h5` o `.keras`) che deve trovarsi nella cartella corretta per essere caricato.
