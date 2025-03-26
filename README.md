# Termostato con Arduino e Componenti

## Autori
- **BASSITE SOUHEL**
- **PARMIGIANI FILIPPO**
- **HU JANG VWEI**

## Descrizione del Progetto
Questo progetto consiste nella realizzazione di un **termometro con Arduino** in grado di monitorare temperatura e umidità, gestire un sistema di LED in base alle soglie di temperatura, e visualizzare i dati raccolti in **un'applicazione desktop** con grafici interattivi, sviluppata utilizzando **Dear PyGui**.

---
## Link PRESENTAZIONE
https://www.canva.com/design/DAGiQMe7qAM/-FHpO94gQZtwW77Eky3qPQ/edit?utm_content=DAGiQMe7qAM&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton

---
## Obiettivo
Creare un sistema di controllo della temperatura basato su Arduino che:
1. **Misuri** temperatura e umidità in tempo reale.
2. **Visualizzi** i dati su un'app desktop.
3. **Gestisca automaticamente i LED** per indicare lo stato della temperatura.
4. **Campioni i dati periodicamente** e li salvi in un file JSON.
5. **Generi un grafico dinamico** dell'andamento della temperatura nel tempo.

---

## Step di sviluppo
### **Step 1: Termostato On-Off**
- Utilizzare il sensore **DHT11** per misurare temperatura e umidità.
- Inviare i dati ad un'applicazione desktop via **porta seriale**.
- Permettere il **controllo manuale** del termostato.

### **Step 2: Gestione LED e Stato Visuale**
- Gestire i LED in base alle soglie di temperatura:
  - **Temperatura alta** → LED **rosso** acceso.
  - **Temperatura normale** → LED **verde** acceso.
  - **Temperatura bassa** → LED **spento**.
- Aggiornare la GUI per mostrare lo stato dei LED con **icone o messaggi**.

### **Step 3: Campionamento Dati**
- Il codice Python raccoglie automaticamente la temperatura a intervalli di **10-20 secondi**.
- I dati vengono **salvati in un file JSON** per mantenerne lo storico.

### **Step 4: Creazione e Visualizzazione del Grafico**
- Utilizzare **Dear PyGui** per creare un **grafico in tempo reale** dell'andamento della temperatura.

---

## Tecnologie utilizzate
- **Arduino Uno** con sensore **DHT11**.
- **Libreria DHT** per Arduino.
- **Python 3** per l'elaborazione dei dati.
- **Serial Communication (PySerial)** per la connessione tra Arduino e PC.
- **Dear PyGui** per l'interfaccia grafica.

---

## Consegna
- **Caricamento del progetto su GitHub**, con:
  - Il **codice sorgente** (Arduino e Python).
  - Un file **README.md** (questo documento).
  - Una **wiki** per la raccolta delle informazioni tecniche.
  - Issue per la gestione dei bug.
- **Presentazione finale del progetto**.
- (Facoltativo) **Video dimostrativo** del funzionamento.

---

## Installazione e utilizzo
### **1. Configurazione Hardware**
- Collegare il sensore **DHT11** alla porta **7** di Arduino.
- Collegare i LED ai pin **2 (rosso), 3 (verde), 4 (blu)**.
- Collegare il relè al pin **8**.
- Collegare Arduino al PC tramite **porta USB**.

### **2. Installazione Software**
- **Arduino IDE**: caricare il codice su Arduino.
- **Python 3**: installare i pacchetti richiesti:
  ```sh
  pip install pyserial dearpygui
  ```
- **Eseguire il programma Python**:
  ```sh
  python main.py
  ```

