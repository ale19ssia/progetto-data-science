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

## Obiettivo

Predire se un cliente abbandonerà il servizio (`Churn`), individuando i fattori più associati all'abbandono.

## Struttura del repository

```
/
├── data/           # dataset e descrizione campi
├── notebooks/      # notebook di analisi (Jupyter/Colab)
├── figures/        # grafici esportati
├── report/         # relazione LaTeX/Overleaf (sorgenti + PDF finale)
└── README.md
```

## Istruzioni per l'esecuzione

1. Aprire `notebooks/01_setup_e_comprensione_dataset.ipynb` (Google Colab o Jupyter locale)
2. Installare le dipendenze: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`
3. Il notebook carica il dataset da `../data/Customer_Churn.csv`
4. Eseguire le celle in ordine

## Uso di assistenti LLM

*[Da compilare: indicare dove e come sono stati eventualmente usati assistenti LLM nel progetto]*

## Stato del progetto

- [x] Fase 1 — Setup del progetto e del repository
- [ ] Fase 2 — Descrizione e comprensione del dataset
- [ ] Fase 3 — Analisi esplorativa e visualizzazione
- [ ] Fase 4 — Modellazione
- [ ] Fase 5 — Valutazione e interpretazione dei risultati
- [ ] Fase 6 — Report scientifico in LaTeX
