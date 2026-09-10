# Calcetto Manager 2026/27

Gestore web per il calcetto del giovedì.

## Stato

La versione attuale è una web app statica con persistenza locale nel browser. Include dashboard, partite, statistiche, classifica, pagelle, ricordi, schede giocatore, gestione giocatori, regolamento, luogo e impostazioni.

## Avvio

È sufficiente pubblicare i file statici con GitHub Pages o un qualsiasi hosting statico. `index.html` carica `styles.css` e `app.js`.

## Dati

I dati della stagione 2026/27 sono memorizzati in `localStorage` con chiave `calcetto-manager-2026-27-v2`. Sono disponibili esportazione e importazione di un backup JSON.

**Nota:** localStorage non è un database condiviso tra utenti/dispositivi. Per rendere l'app multi-dispositivo e permettere a più persone di vedere gli stessi dati serve un backend/database online (ad esempio Supabase/Postgres) e relative credenziali.

## Funzioni principali

- 16 giocatori iniziali, modificabili.
- Creazione e cancellazione partite.
- Formati 5v5, 6v6, 7v7, 8v8.
- Squadre A/B e arbitro.
- Statistiche: gol, assist, gialli, rossi, autogol, rigori, gol subiti, cambi.
- Classifica calcolata automaticamente dalle partite.
- Pagella con voti 0–10 e selezione automatica del voto più alto.
- Nessuna voce MVP.
- Scheda individuale giocatore.
- Ricordi testuali.
- Gestione quote, stato, infortunio e disponibilità arbitro.
- Regolamento e luogo modificabili.
- Dark mode.
- Backup JSON.
- Layout responsive per desktop e smartphone.

## Prossimo salto architetturale

Per una versione realmente condivisa e utilizzabile come il sito originale, sostituire il layer `localStorage` con un database online e autenticazione admin. La struttura dati dell'app è già separata concettualmente per rendere questa migrazione possibile senza cambiare il modello delle statistiche.