# Dataset, modelli e risultati sperimentali - UNSW-NB15

Questa repository contiene i **file utilizzati e generati** durante la sperimentazione condotta sul dataset UNSW-NB15 per la tesi di laurea triennale:  
**"IDENTIFICAZIONE DI ATTACCHI WEB CON INTELLIGENZA ARTIFICIALE"** di Veronica Tavazzi (12247A).

I file inclusi documentano l'intero flusso operativo di una pipeline di rilevamento delle intrusioni basata sul dataset **UNSW-NB15**, dalla fase di preprocessing all’addestramento e valutazione dei modelli supervisionati.  
La repository è suddivisa in tre sezioni principali:
- Dataset originali, puliti e preprocessati.
- Modelli addestrati in formato serializzato.
- Risultati delle valutazioni sperimentali, sia standard che ottimizzate.

---

## Struttura della repository

| File                                  | Descrizione                                                                 |
|--------------------------------------|-----------------------------------------------------------------------------|
| `UNSW_NB15 original.zip`             | Contiene i file originali del dataset: `UNSW_NB15_training-set.csv`, `UNSW_NB15_testing-set.csv` |
| `UNSW-NB15_clean_merged.csv.zip`     | Versione unificata e pulita del dataset, ottenuta dalla fusione e pulizia dei file originali     |
| `UNSW-NB15_final_preprocessed.csv.zip` | Dataset preprocessato finale (encoding, scaling, bilanciamento con SMOTE)  |
| `UNSW-NB15_train_val_test.zip`       | Contiene i tre file derivati dal dataset preprocessato: `train`, `val`, `test` con split 70/15/15 |

| File modello                         | Descrizione                                                                 |
|--------------------------------------|-----------------------------------------------------------------------------|
| `random_forest_model.pkl`            | Modello Random Forest addestrato sul dataset UNSW-NB15                      |
| `svm_model.pkl`                      | Modello SVM (RBF kernel, base)                                              |
| `svm_optimized_model.pkl`            | Modello SVM ottimizzato (C=1.0, gamma='scale')                              |
| `dnn_model.h5`                       | Modello Deep Neural Network (base) in formato HDF5                          |
| `dnn_optimized_model.h5`            | Modello DNN ottimizzato (epochs=30, batch=32, dropout=0.3, optimizer=rmsprop) |

| File risultati                       | Descrizione                                                                 |
|--------------------------------------|-----------------------------------------------------------------------------|
| `random_forest_results.txt`          | Risultati del modello Random Forest (accuracy, precision, recall, f1-score) |
| `svm_results.txt`                    | Risultati del modello SVM base                                              |
| `svm_optimized_results.txt`          | Risultati del modello SVM ottimizzato                                       |
| `dnn_results.txt`                    | Risultati del modello DNN base                                              |
| `dnn_optimized_results.txt`          | Risultati del modello DNN ottimizzato                                       |

---

## Note metodologiche

Tutti i file contenuti sono **stati generati o ricostruiti** in modo da riflettere fedelmente la pipeline descritta nei capitoli metodologici e sperimentali della tesi.  
In particolare:
- I file `.csv.zip` rappresentano versioni originali, pulite o preprocessate del dataset.
- I file `.pkl` e `.h5` contengono i modelli addestrati esattamente secondo le configurazioni indicate in tesi.
- I file `.txt` riportano le metriche finali (accuracy, precision, recall, f1-score) corrispondenti alle **matrici di confusione presentate nel Capitolo 3**.

Per motivi di compatibilità con GitHub, i file di grandi dimensioni sono stati compressi in formato `.zip`.  
Tutti i contenuti sono utilizzabili a scopo di verifica, replicazione o approfondimento didattico.

---

## Disclaimer

Il contenuto di questa repository è stato pubblicato esclusivamente per **fini accademici e documentali**.  
Tutti i file inclusi rappresentano il lavoro originale svolto per la redazione della tesi di laurea e sono resi disponibili **unicamente a titolo consultativo**.  
È espressamente vietata qualsiasi forma di **replicazione, distribuzione o utilizzo per scopi diversi da quelli di verifica accademica**.
