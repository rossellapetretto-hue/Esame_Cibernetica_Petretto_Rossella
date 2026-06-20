## Prompt di Inizializzazione
Agisci come un Lead Prompt Engineer. Crea un report tecnico e operativo intitolato "La Struttura del Prompt Perfetto per AI Video". Basandoti sulle guide fornite, il report deve spiegare come segmentare logicamente un prompt testuale (Movimento Camera -> Soggetto -> Ambiente -> Illuminazione/Stile) per minimizzare le allucinazioni visive del modello.

# La Struttura del Prompt Perfetto per AI Video

## 1. Fondamenti del Prompting per Modelli Video Generativi

L’evoluzione tecnologica ci ha portato dal prompting testuale statico alla necessità di un linguaggio dinamico e multidimensionale. Comunicare con i moderni "World Models" — come **Runway Gen-4.5**, **Adobe Firefly Video** e **Kling Professional Mode** — richiede una struttura rigorosa per mappare non solo i pixel, ma la loro evoluzione spazio-temporale. Un prompt architettato correttamente agisce come un binario per l'IA, riducendo drasticamente le incoerenze visive e le allucinazioni, trasformando il processo da un "gioco probabilistico" a una produzione professionale controllata.

### Principi Cardine della Chiarezza

- **Linguaggio Naturale vs Parole Chiave:** Sebbene le keyword siano utili per impostare una direzione, il linguaggio naturale offre un controllo superiore. Scrivere in frasi complete fornisce il contesto necessario al modello per integrare gli elementi. Le parole chiave vanno intese come descrittori tecnici inseriti in una narrazione fluida.
- **Frasario Positivo:** I modelli video spesso ignorano le negazioni. Inserire "senza nuvole" può paradossalmente generare nuvole. È fondamentale essere diretti: usate "cielo limpido" o, per indicare l'assenza di movimento, termini come "Static" o "Camera fissa" (evitando "la camera non si muove").
- **Dettaglio Visivo vs Concettuale:** I modelli non comprendono le astrazioni poetiche. Non descrivete "cosa si prova" (es. "un'atmosfera triste"), ma descrivete "cosa si vede" (es. "illuminazione fioca, tonalità bluastre, pioggia sottile su un vetro").
- **Reinforcement (Rinforzo):** Per aumentare l'aderenza, è strategico ripetere o rinforzare concetti chiave in diverse sezioni del prompt (es. specificare "hyperspeed" sia nel movimento della camera che nell'azione ambientale).

Questa base metodologica è il prerequisito per implementare una segmentazione logica che guidi il modello senza ambiguità.

## 2. Anatomia della Segmentazione Logica (Il Metodo Sequenziale)

L'architettura di un prompt efficace non è un semplice elenco, ma una gerarchia di informazioni dove ogni segmento imposta i parametri del "mondo" prima di definire i dettagli. Questo metodo è una sintesi avanzata della formula di **Firefly** (_Shot Type + Character + Action + Location + Aesthetic_) e della struttura professionale di **Kling**.

### Le Quattro Fasi della Segmentazione

1. **Movimento Camera e Inquadratura (The Eye):** È il primo passo per ancorare la scena. Specificare lo _Shot Size_ e l'angolazione permette di stabilire la prospettiva. Definire il movimento (es. _Pan_, _Tilt_, _SnorriCam_) stabilisce il punto di vista prima che il soggetto entri in azione.
2. **Il Soggetto e l'Azione (The Focus):** Descrivete l'aspetto fisico e il movimento specifico (_Subject Movement_). È cruciale differenziare tra l'azione del soggetto e il movimento ambientale per mantenere la coerenza dei pixel durante la trasformazione.
3. **L'Ambiente e il Contesto (The World):** Definite lo spazio, il meteo e gli elementi di sfondo/primo piano. Questo impedisce all'IA di riempire i vuoti con elementi casuali.
4. **Illuminazione, Stile e Atmosfera (The Mood):** L'impatto dei termini cinematografici (_Cinematic_, _Golden Hour_, _Venetian lighting_) determina il rendering finale e la profondità emotiva.

### Esempio Pratico: Ottimizzazione del Prompt

|   |   |
|---|---|
|Stato del Prompt|Esempio di Testo|
|**Prima (Conversazionale/Chatty)**|"Ciao AI, puoi farmi un video fighissimo di un cowboy che cade da cavallo nel deserto mentre c'è il tramonto? Metti tanta polvere e fai sembrare tutto un film western, grazie!"|
|**Dopo (Tecnico/Segmentato)**|"**[Shot Type]:** Medium shot, camera fissa. **[Character]:** Cowboy con abiti logori su un cavallo che si impenna. **[Action]:** Il cavallo si agita violentemente; il cowboy perde l'equilibrio e cade lateralmente verso sinistra. **[Location]:** Deserto polveroso, cespugli secchi in primo piano. **[Aesthetic]:** Cinematic, controluce (backlit), high contrast, ora d'oro (golden hour), atmosfera epica."|

Questa struttura agisce come una "gabbia di contenimento" per le allucinazioni, obbligando il modello a processare ogni token in modo gerarchico.

## 3. Tassonomia Tecnica e Controllo del Movimento

Un Lead Architect deve utilizzare un vocabolario condiviso per guidare il modello con precisione chirurgica, riducendo la dipendenza dai seed casuali.

### Tabelle di Riferimento Tecnico

**Tabella 1: Stili di Camera (The Eye)** | Termine | Effetto Visivo | | :--- | :--- | | **SnorriCam** | Camera ancorata al corpo del soggetto, creando un effetto di isolamento dinamico. | | **Over the shoulder** | Inquadratura da dietro la spalla di un personaggio verso il soggetto. | | **Establishing wide** | Inquadratura molto ampia per stabilire la geografia della scena. | | **Low angle** | Dal basso verso l'alto; conferisce potere e monumentalità al soggetto. | | **FPV / POV** | Prospettiva in prima persona; simula il movimento soggettivo. | | **Macro** | Dettaglio estremo su texture (es. iride, fibre di tessuto). | | **Dolly in** | La camera si sposta fisicamente verso il soggetto, aumentando la tensione. |

**Tabella 2: Dinamiche di Movimento (The Motion)** | Verbo | Impatto sulla Scena | | :--- | :--- | | **Undulates** | Movimento ondulatorio fluido e costante (es. tessuti o creature marine). | | **Shatters** | Frammentazione violenta e improvvisa di un oggetto solido. | | **Vortex** | Movimento rotatorio che converge verso un centro focale. | | **Explodes** | Espansione rapida di particelle dal centro verso l'esterno. | | **Ripples** | Piccole onde concentriche che si propagano su una superficie. | | **Transforms** | Mutazione fluida della geometria di un oggetto in un altro. | | **Slow motion** | Espansione del tempo per enfatizzare la micro-azione. |

**Tabella 3: Lighting & Aesthetic (The Mood)** | Keyword | Atmosfera | | :--- | :--- | | **Venetian lighting** | Luce filtrata attraverso persiane o feritoie, creando strisce d'ombra nette. | | **Iridescent** | Superfici che cambiano colore in base all'angolo della luce (es. bolle di sapone). | | **Glitchcore** | Estetica digitale corrotta, con artefatti visivi e colori saturati. | | **Tyndall effect** | Raggi di luce visibili che filtrano attraverso nebbia o polvere. | | **Backlit** | Illuminazione posteriore che crea un profilo luminoso (rim light) o silhouette. | | **Cyberpunk** | Urbana futuristica, luci neon, pioggia, contrasti cromatici teal e orange. | | **Cinematic** | Resa da film ad alto budget, illuminazione drammatica e composizione curata. |

## 4. Tecniche Avanzate di Ottimizzazione e Iterazione

La produzione video AI è intrinsecamente iterativa. Il primo prompt è una bozza; l'output va analizzato per correggere i segmenti ignorati dal modello.

1. **Timestamp Prompting (Gen-4.5):** Permette di sequenziare le azioni con precisione temporale. Esempio: `[00:00 - 00:02] il soggetto guarda a destra, [00:02 - 00:05] il soggetto sorride e fa un cenno`. È vitale stimare tempi realistici affinché l'azione si svolga naturalmente.
2. **Riferimenti Visivi (@character / @style):** Utilizzati in **Luma Dream Machine**, permettono di caricare un'immagine guida. Usate il tag `@character` per mantenere la coerenza del volto tra diverse scene o `@style` per ereditare una palette cromatica specifica.
3. **Context Retention via Boards:** Sfruttate la memoria dei "Board" per evoluzioni narrative. Esempio iterativo:
    - Prompt 1: "Un prato tranquillo."
    - Prompt 2: "Aggiungi una luce dorata al tramonto (Add a golden hour glow)."
    - Prompt 3: "Inserisci un piccolo cottage in lontananza (Include a small cottage in the distance)."
    - Prompt 4: "Trasforma la scena in una notte stellata con lucciole (Transition into a starry night with fireflies)."

## 5. Guida alla Risoluzione dei Problemi: Ridurre le Allucinazioni

La struttura proposta non è solo creativa, ma è il principale strumento di debugging. Se il video presenta artefatti, verificate i seguenti parametri tecnici.

### Checklist di Validazione

- **Conflitto Camera/Soggetto:** Il movimento della camera è fisicamente compatibile con l'azione? Un movimento FPV ad alta velocità spesso confligge con azioni lente e minuziose del soggetto.
- **Soggetti Eccessivi:** Avete superato il limite di **4 soggetti**? Oltre questa soglia, i modelli tendono a fondere i pixel o a creare deformazioni anatomiche.
- **Conversational Fillers:** Avete incluso termini come "per favore", "crea un video di", "vorrei"? Questi sono "low-value tokens" che sprecano la finestra di contesto del modello; eliminateli.
- **Insensibilità ai Numeri:** Ricordate che modelli come Kling non sono sensibili ai conteggi precisi. Evitate "10 cuccioli"; preferite "un gruppo di cuccioli".
- **Astrazione vs Concretezza:** Se il modello allucina, sostituite termini poetici ("un'alba di speranza") con descrizioni fisiche ("luce arancione calda che sorge sopra l'orizzonte, ombre lunghe").

La padronanza di questa architettura trasforma l'AI Video in uno strumento di produzione professionale, dove ogni termine è un comando intenzionale verso la creazione della realtà sintetica.