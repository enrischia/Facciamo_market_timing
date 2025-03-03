# Analisi del Codice per l'ETF

Questo repository contiene uno script Python sviluppato per analizzare i dati storici di un ETF utilizzando le librerie **pandas**, **matplotlib** e **yfinance**.

---

## Funzionalità Principali

### 1. Download dei Dati dell'ETF
- **Funzione:** `scarica_dati_etf()`
- **Descrizione:** Utilizza la libreria **yfinance** per scaricare i dati storici di un ETF.
- **Operazioni:**
  - Estrae le colonne "Date" e "Close", rinominandole rispettivamente in "Data" e "Valore".
  - Salva i dati in un file CSV denominato `dati_etf.csv`.

### 2. Calcolo del Rendimento Netto
- **Funzione:** `calcola_rendimento()`
- **Descrizione:** Calcola il rendimento netto dell'ETF in un intervallo di date specifico.
- **Operazioni:**
  - Filtra il DataFrame per il periodo selezionato.
  - Calcola il rendimento lordo basato sulla variazione tra il primo e l'ultimo valore.
  - Considera l'investimento iniziale, i costi delle transazioni (passati come lista) e le tasse (come percentuale).
  - Restituisce il rendimento netto finale in percentuale.

### 3. Analisi della Variazione Percentuale e Media Mobile
- **Operazioni:**
  - Calcola la variazione percentuale giornaliera del valore dell'ETF.
  - Calcola una **media mobile sui giorni** basata sul prodotto cumulativo dei rendimenti giornalieri.
  - Individua i punti in cui la media mobile supera una soglia specifica, segnalandole.

### 4. Visualizzazione dei Dati
- **Strumento:** `matplotlib`
- **Descrizione:** Traccia un grafico temporale del valore dell'ETF.
- **Dettagli:**
  - Il grafico mostra l'andamento storico dell'ETF.
  - Evidenzia con punti rossi i momenti in cui la media mobile a 7 giorni supera la soglia impostata.

### 5. Analisi di Finestre Temporali
- **Descrizione:** 
  - Definisce due finestre temporali di analisi, modificabili a piacre.  
  - Per ciascuna finestra, calcola il rendimento netto tenendo conto dell'investimento iniziale, dei costi di transazione e delle tasse.
  - I rendimenti netti vengono stampati a video.

---

## Come Usare il Codice

### Requisiti
Assicurati di avere installato le seguenti librerie:
- **pandas**
- **matplotlib**
- **yfinance**

### Personalizza
Si possonon personalizzare le seguenti:
- Cambia il ticker per analizzare un altro ETF
- Modifica il periodo e le finsestre di analisi
- Aggiorna l'investimento iniziale e i costi di transazione

---

## Conclusioni
Questo script permette di giocare e osservare l'andamento di un ETF, scarica i dati suoi storici da Yahoo Finance,ne calcola il rendimento netto su specifici periodi considerando tasse e costi di transazione e identifica variazioni significative tramite una media mobile a 7 giorni. Infine visualizza l'andamento dell'ETF con un grafico evidenziando giorni che hanno delle particolari variazioni. 


