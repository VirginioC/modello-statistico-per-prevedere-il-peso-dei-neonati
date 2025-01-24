# Modello statistico per prevedere il peso dei neonati

## Descrizione 
Questo progetto, prodotto durante il Master in Data Science di Profession AI, consiste nello sviluppare utilizzando il linguaggio **R** un modello statistico in grado di prevedere il peso dei neonati alla nascita, basandosi su 10 variabili cliniche raccolte da tre ospedali per un totale di 2500 osservazioni. Esso mira a migliorare la gestione delle gravidanze ad alto rischio, ottimizzare le risorse ospedaliere e garantire migliori risultati per la salute neonatale.

## Struttura della repository
La repository contiene i seguenti file e cartelle:

- **`modello_statistico_previsione_peso_neonati.Rmd`**: file R Markdown con il codice e le analisi statistiche.
- **`modello_statistico_previsione_peso_neonati.html`**: versione HTML generata dal file R Markdown.
- **`neonati.csv`**: dataset utilizzato per le analisi.
- **`images/`**: cartella contenente immagini utilizzate nel progetto.

Le variabili presenti nel dataset sono: `Anni.madre`, `N.gravidanze`, `Fumatrici`, `Gestazione`, `Peso`, `Lunghezza`, `Cranio`, `Tipo.parto`, `Ospedale` e `Sesso` (descritte dettagliatamente nei documenti Rmd e html).

## Fasi operative
Il progetto è suddiviso in due parti:
1. **Analisi preliminare**:
  Vengono esplorate le variabili attraverso un'**analisi descrittiva** per comprenderne la distribuzione e identificare eventuali outlier o anomalie. 
  Inoltre vengono saggiate le seguenti ipotesi con i test adatti:
  
    - La media del peso e della lunghezza di questo campione di neonati sono significativamente uguali a quelle della popolazione.
    - Peso e lunghezza del campione di neonati sono significativamente diversi tra i due sessi.
    - In alcuni ospedali si effettuano più parti cesarei.
    
2. **Analisi multidimensionale**:

     - **Matrice di correlazione e boxplot**: Vengono indagate a due a due le relazioni tra le variabili con particolare attenzione alla variabile risposta.
     - **Creazione del modello di regressione**: Viene creato un modello di regressione lineare multipla che include tutte le variabili rilevanti. 
     - **Selezione del modello ottimale**: Attraverso tecniche di selezione del modello, come l'AIC e il BIC, viene selezionato il modello più parsimonioso, eliminando le variabili non significative. Vengono considerati anche modelli con interazioni tra le variabili e possibili effetti non lineari.
     - **Analisi della qualità del modello**: Ottenuto il modello finale, viene valutata la sua capacità predittiva utilizzando metriche come R² e il Root Mean Squared Error (RMSE). Un'attenzione particolare è rivolta all'analisi dei residui e alla presenza di valori influenti, che possono distorcere le previsioni, indagando su di essi.
     - **Previsioni e risultati**: Una volta validato il modello, viene usato per fare previsioni pratiche.
     - **Visualizzazioni**: Vengono costruiti grafici e rappresentazioni visive per comunicare i risultati del modello e mostrare le relazioni più significative tra le variabili.
  
## Risultati sintetici
Al termine delle analisi risulta che il modello più parsimonioso per prevedere il peso dei neonati utilizza come regressori le variabili `Gestazione`, `Lunghezza`, `Cranio` e `Sesso` spiegando il **72.57 %** della variabilità del peso:

- Peso ~ Gestazione + Lunghezza + Cranio + Sesso
- R² (adj) = 0.7257


## Prerequisiti
- **Software richiesti:**
  - [R](https://www.r-project.org/) 
  - [RStudio](https://posit.co/download/rstudio-desktop/)
- **Pacchetti R necessari:**
  - `gghalves`
  - `car`
  - `dplyr`
  - `lmtest`
  - `caret`
  - `rgl`
  - `moments`

## Guida rapida
1. Clona o scarica questa repository sul tuo ambiente locale.
2. Apri il file `modello_statistico_previsione_peso_neonati.Rmd` in RStudio.
3. Esegui le analisi nel file R Markdown.

## Autore
[Virginio Cocciaglia](https://github.com/VirginioC)

---
