# UNSW-NB15 - File dei passaggi sperimentali

Questo repository contiene tutti i file utilizzati e generati durante la sperimentazione per il rilevamento delle intrusioni di rete tramite tecniche di machine learning, basata sul dataset **UNSW-NB15**.

## 📁 Contenuto del repository

### 📦 Dataset originali

- **`UNSW_NB15 original.zip`**  
  Contiene i file originari forniti dal dataset:
  - `UNSW_NB15_training-set.csv`
  - `UNSW_NB15_testing-set.csv`

### 🧼 Dataset pulito e preprocessato

- **`UNSW-NB15_clean_merged.csv.zip`**  
  Contiene il dataset ottenuto dall’unione e pulizia dei file originali.

- **`UNSW-NB15_final_preprocessed.csv.zip`**  
  Contiene il dataset preprocessato finale, ottenuto tramite:
  - Pulizia e rimozione outlier
  - Min-Max Scaling
  - Encoding delle variabili categoriali
  - Bilanciamento tramite SMOTE
  Il file risultante è pronto per l’addestramento.

- **`UNSW-NB15_train_val_test.zip`**  
  Contiene la suddivisione finale del dataset preprocessato:
  - `UNSW-NB15_train.csv` (70%): training
  - `UNSW-NB15_val.csv` (15%): validazione
  - `UNSW-NB15_test.csv` (15%): test

---

## 🧠 Modelli addestrati

- **Random Forest**
  - `random_forest_model.pkl`
  - `random_forest_results.txt`

- **Support Vector Machine**
  - Base:  
    - `svm_model.pkl`  
    - `svm_results.txt`  
  - Ottimizzata:  
    - `svm_optimized_model.pkl`  
    - `svm_optimized_results.txt`  

- **Deep Neural Network**
  - Base:  
    - `dnn_model.h5`  
    - `dnn_results.txt`  
  - Ottimizzata:  
    - `dnn_optimized_model.h5`  
    - `dnn_optimized_results.txt`  

---

## 🧪 Note

Le metriche di valutazione (Accuracy, Precision, Recall, F1-score) e le matrici di confusione sono riportate nei file `.txt`.  
Le architetture e configurazioni utilizzate sono descritte nella documentazione allegata al progetto.

---

## 📎 Licenza

Distribuito solo per scopi accademici e di ricerca.
