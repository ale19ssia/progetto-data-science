# Previsione del Customer Churn

Progetto di gruppo per il corso *Introduzione al Pensiero Computazionale e alla Data Science*.

## Team

- Alessia (alessia99deluca@gmail.com)
- Michelle

Numero team: *[inserire numero registrazione dal foglio Google del docente]*

## Descrizione del progetto

L'obiettivo è realizzare un'analisi completa del dataset **Customer Churn**, applicando le tecniche di data science viste a lezione: esplorazione dati, visualizzazione, modellazione predittiva e valutazione critica dei risultati.

## Descrizione del dataset

Il dataset (`data/Customer_Churn.csv`, 7043 righe, 21 colonne) contiene informazioni su clienti di un'azienda di telecomunicazioni:

- **dati demografici**: genere, età (senior citizen), presenza di partner/persone a carico
- **servizi sottoscritti**: telefono, linee multiple, internet, sicurezza online, backup, protezione dispositivo, supporto tecnico, streaming TV/film
- **informazioni contrattuali**: durata contratto (tenure), tipo di contratto, metodo di pagamento, fatturazione, importi mensili/totali
- **target**: `Churn` (Sì/No) — se il cliente ha abbandonato il servizio

Descrizione completa dei campi in `data/Customer_Churn_description.txt`.

Nota: la colonna `TotalCharges` viene fornita come testo e contiene 11 valori vuoti, tutti corrispondenti a clienti con `tenure = 0` (appena iscritti, non ancora fatturati) — vedi dettagli nel notebook di Fase 2.

## Obiettivo

Predire se un cliente abbandonerà il servizio (`Churn`), individuando i fattori più associati all'abbandono.

## Struttura del repository

```
/
├── data/           # dataset e descrizione campi
├── notebooks/      # notebook di analisi (Jupyter/Colab)
│   ├── 01_setup_e_comprensione_dataset.ipynb   # Fase 1-2
│   ├── 02_analisi_esplorativa.ipynb            # Fase 3
│   └── 03_modellazione_e_valutazione.ipynb     # Fase 4-5
├── figures/        # grafici esportati
├── report/         # relazione LaTeX/Overleaf (sorgenti + PDF finale)
└── README.md
```

## Istruzioni per l'esecuzione

1. Aprire i notebook in `notebooks/` in ordine (Google Colab o Jupyter locale)
2. Installare le dipendenze: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`
3. Ogni notebook carica il dataset da `../data/Customer_Churn.csv`
4. Eseguire le celle in ordine

## Riepilogo dei risultati (Fase 4-5)

Modelli addestrati su split stratificato 75/25, con `class_weight="balanced"` per Regressione Logistica e Random Forest:

| Modello | Accuracy | Precision (Churn) | Recall (Churn) | F1-score |
|---|---|---|---|---|
| Regressione Logistica | 0.750 | 0.519 | 0.797 | 0.628 |
| k-NN | 0.752 | 0.534 | 0.516 | 0.525 |
| Random Forest | 0.792 | 0.644 | 0.484 | 0.553 |

La Random Forest ha l'accuracy più alta, ma la Regressione Logistica ottiene la recall più alta sulla classe Churn — la metrica più rilevante in questo contesto, perché individuare i clienti a rischio è l'obiettivo pratico principale.

Fattori più associati al churn (coerenti tra Random Forest e Regressione Logistica): tipo di contratto (in particolare il contratto biennale, fortemente associato alla permanenza), tenure, metodo di pagamento (electronic check).

## Uso di assistenti LLM

Il progetto è stato realizzato con il supporto di un assistente LLM (Claude) come aiuto alla programmazione: scrittura e formattazione del codice, spiegazione dei concetti statistici e di machine learning utilizzati. Ogni ipotesi, ogni scelta di analisi e ogni interpretazione dei risultati presente nei notebook è stata discussa e compresa dal team prima di essere inclusa.

Una prima versione del progetto (Fasi 2-5) era stata realizzata con un altro assistente (ChatGPT) senza un'adeguata comprensione da parte del team dei passaggi svolti. È stata quindi rifatta da zero a partire dalla Fase 2, questa volta con un percorso guidato in cui ogni scelta viene spiegata e verificata.

## Stato del progetto

- [x] Fase 1 — Setup del progetto e del repository
- [x] Fase 2 — Descrizione e comprensione del dataset
- [x] Fase 3 — Analisi esplorativa e visualizzazione
- [x] Fase 4 — Modellazione
- [x] Fase 5 — Valutazione e interpretazione dei risultati
- [ ] Fase 6 — Report scientifico in LaTeX
