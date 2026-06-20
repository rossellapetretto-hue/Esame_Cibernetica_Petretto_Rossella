
# 000_Info - Diario di Bordo e Flusso di Lavoro

Questo documento costituisce la relazione tecnica obbligatoria relativa allo stream di lavoro adottato, all'architettura logica dei prompt e alla risoluzione degli imprevisti tecnici emersi durante la realizzazione dell'elaborato per l'esame di Cibernetica e Teoria delle Informazioni (Giugno 2026).

---

## Analisi dello Stream di Lavoro (Workflow)
L'obiettivo strategico del progetto è stato la verticalizzazione di strumenti di Intelligenza Artificiale Generativa (Google NotebookLM e Gemini GEM) per la creazione di assistenti operativi e specialistici, integrando l'intero flusso documentale all'interno di un ecosistema locale razionale (Obsidian Vault) sincronizzato in cloud (GitHub).

Il flusso ha previsto tre macro-fasi:
1. **Analisi e Ingestione:** Selezione e pulizia delle fonti documentali (guide ufficiali di prompting per il video ed espansioni e regolamenti ufficiali per il tema ludico "Root").
2. **Generazione e Ottimizzazione:** Interrogazione guidata dei modelli per l'estrazione di 9 tipologie differenziate di artefatti per ciascun notebook, evitando la duplicazione dei formati.
3. **Ingegnerizzazione del Vault:** Strutturazione gerarchica delle cartelle per garantire la massima granularità e consultabilità dei materiali da parte della commissione d'esame.

---

## Gestione degli Imprevisti e Problem Solving Tecnico

Durante lo sviluppo del progetto sono emerse tre criticità strutturali, superate attraverso specifiche strategie di Prompt Engineering e ottimizzazione dei dati:

### Criticità A: Assenza di System Instructions native in Google NotebookLM
* **Problema:** A differenza dei Gemini GEM, l'interfaccia di NotebookLM non presenta un campo nativo per l'inserimento di "Istruzioni di Sistema" rigide. Questo rischiava di far deviare il modello verso risposte teoriche o storiche, violando il vincolo tassativo di "natura esclusivamente pratica" richiesto dalla consegna.
* **Risoluzione:** È stata adottata una strategia avanzata di *Data Anchoring*. Sono stati sintetizzati due file di testo operativi (`Inizializzazione_Guida_Operativa_VideoAI.txt` e `Inizializzazione_Root_Esperto.txt`) contenenti stringenti direttive di ruolo, glossari cinematici e limitazioni comportamentali. L'iniezione di questi file direttamente nel database delle fonti ha forzato stabilmente l'ancoraggio semantico dei modelli su output esclusivamente pratici e operativi.

### Criticità B: Limiti di esportazione dell'interfaccia interattiva dell'Artifact "Quiz"
* **Problema:** L'artifact "Quiz" generato nativamente dal pannello "Studio" di NotebookLM produce un'interfaccia web interattiva non riproducibile nativamente all'interno di Obsidian in formato testuale Markdown, ostacolando la centralizzazione dei contenuti nel Vault.
* **Risoluzione:** L'ostacolo è stato aggirato bypassando l'interfaccia grafica attraverso un prompt di chat customizzato. È stato imposto al modello il vincolo di output in puro codice Markdown, forzando la formattazione dei quesiti tramite sintassi checkbox (`- [ ]`). Questo ha permesso il trasferimento speculare dell'artefatto su Obsidian, mantenendo l'interattività per l'utente finale e preservando la razionalità del file.

### Criticità C: Limitazioni di peso (Overflow) del Vault per il caricamento su GitHub
* **Problema:** L'esportazione in locale di file binari pesanti (nello specifico, il file podcast dell'Audio Overview in formato `.wav`) ha causato un incremento esponenziale del peso del Vault, superando le soglie di upload fluido della piattaforma web di GitHub.
* **Risoluzione:** Ho rimosso i file più pesanti da vault e li ho caricati su una cartella Drive e ho messo un link direttamente collegato

---
## Struttura del Vault

* 📁 **01_NotebookLM**: Contiene i dettagli, i prompt di inizializzazione e tutti gli artefatti (generati uno per tipo) per il NotebookLM Libero (Esperto di Giochi da tavolo) e il NotebookLM Obbligatorio (Text-Video).
* 📁 **02_Gemini_GEM**: Contiene le istruzioni di sistema e i link operativi per il GEM Obbligatorio (Sceneggiatore/Regista) e il GEM Libero (Dungeon Pokémon).
* 📁 **03_Prompt_Corso**: Archivio di prompt realizzati che ho ritenuto interessanti da presentare  (es. Dungeon Master 1.0), rigorosamente formattati in blocchi di codice testuale.
* 📁 **04_Allegati**: Contiene i file di supporto, come immagini e documenti PDF, generati a corredo degli artefatti e dei NLM.
