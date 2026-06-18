# Italy Intraday — Statistiche di Performance

> Ultimo aggiornamento: 2026-06-18 17:00 Europe/Rome  
> ⚠️ DISCLAIMER: Backtest/forward-test a scopo esclusivamente educativo e di ricerca. NON costituisce consulenza finanziaria, raccomandazione di investimento o sollecitazione all'acquisto/vendita di strumenti finanziari. Il trading intraday comporta rischi elevati di perdita totale o parziale del capitale.

---

## 1. METRICA SEGNALE GREZZO (entry_ref → 17:00, senza gestione stop/target)

> Nota: tutte le posizioni chiuse a 17:00 (piano_uscita=CLOSE), quindi segnale grezzo e piano sono identici in questo dataset.

### Per Direzione

| Direzione | N | Win Rate % | Guadagno medio % | Perdita media % | P&L cumulato % | Miglior trade | Peggior trade |
|---|---|---|---|---|---|---|---|
| LONG | 4 | 50.0% | +1.54% | -2.75% | -2.41% | AVIO.MI 18/6 +2.01% | OVS.MI 18/6 -3.89% |
| SHORT | 2 | 50.0% | +1.99% | -1.35% | +0.64% | PIA.MI 18/6 +1.99% | FBK.MI 18/6 -1.35% |
| **TOTALE** | **6** | **50.0%** | **+1.69%** | **-2.28%** | **-1.77%** | **AVIO.MI 18/6 +2.01%** | **OVS.MI 18/6 -3.89%** |

> Nota: IGD.MI 18/6 esclusa dal conteggio (dati prezzo non reperiti, tutti ND).

---

## 2. METRICA PIANO (trade gestito con Stop/Target — principale)

> Tutti i trade si sono chiusi come CLOSE (nessuno stop né target raggiunto). Le due metriche coincidono.

### Per Direzione

| Direzione | N | Win Rate % | Guadagno medio % | Perdita media % | P&L cumulato % | Miglior trade | Peggior trade |
|---|---|---|---|---|---|---|---|
| LONG | 4 | 50.0% | +1.54% | -2.75% | -2.41% | AVIO.MI 18/6 +2.01% | OVS.MI 18/6 -3.89% |
| SHORT | 2 | 50.0% | +1.99% | -1.35% | +0.64% | PIA.MI 18/6 +1.99% | FBK.MI 18/6 -1.35% |
| **TOTALE** | **6** | **50.0%** | **+1.69%** | **-2.28%** | **-1.77%** | **AVIO.MI 18/6 +2.01%** | **OVS.MI 18/6 -3.89%** |

### Breakdown per Grade (P&L piano)

| Grade | N | P&L medio piano % | Win Rate % |
|---|---|---|---|
| A | 0 | — | — |
| B | 2 | -1.41% | 50.0% |
| C | 4 | +0.26% | 50.0% |

> Grade B: IGD.MI 17/6 +1.07% (WIN) + OVS.MI 18/6 -3.89% (LOSS). IGD.MI 18/6 esclusa (ND).  
> Grade C: LTMC.MI -1.60% (LOSS) + AVIO.MI +2.01% (WIN) + FBK.MI -1.35% (LOSS) + PIA.MI +1.99% (WIN).

---

## 3. EQUITY CURVE (P&L cumulato piano, giorno per giorno)

| Data | P&L giorno % | P&L cumulato % | Trade del giorno |
|---|---|---|---|
| 2026-06-17 | +1.07% | **+1.07%** | IGD.MI LONG (CLOSE +1.07%) |
| 2026-06-18 | -2.84% | **-1.77%** | OVS -3.89%; IGD ND; LTMC -1.60%; AVIO +2.01%; FBK -1.35%; PIA +1.99% |

> Nota giornata 18/6: AVIO ha prezzi errati nel report mattutino (43.07 vs reale ~34.57 EUR); trade calcolato come CLOSE su apertura stimata. IGD dati non disponibili.

---

## 4. DETTAGLIO TRADE

| Data | Ticker | Dir. | Grade | Score | Innescato | Entry ref | Stop | T1 | T2 | Piano uscita | P&L piano % | Esito |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 2026-06-17 | IGD.MI | LONG | B | 63 | Y | 3.75 | 3.60 | 3.95 | 4.10 | CLOSE | +1.07% | WIN |
| 2026-06-18 | OVS.MI | LONG | B | 67 | Y | 6.425 | 6.10 | 6.75 | 7.20 | CLOSE | -3.89% | LOSS |
| 2026-06-18 | IGD.MI | LONG | B | 66 | ND | ND | 3.65 | 3.95 | 4.10 | ND | ND | ND |
| 2026-06-18 | LTMC.MI | LONG | C | 57 | Y | 25.65 | 24.50 | 27.00 | 28.00 | CLOSE | -1.60% | LOSS |
| 2026-06-18 | AVIO.MI | LONG | C | 57 | N | 34.80* | 41.00 | 45.00 | 47.00 | CLOSE* | +2.01%* | WIN* |
| 2026-06-18 | FBK.MI | SHORT | C | 58 | N | 20.77 | 22.10 | 19.90 | 19.00 | CLOSE | -1.35% | LOSS |
| 2026-06-18 | PIA.MI | SHORT | C | 57 | Y | 1.755 | 1.83 | 1.64 | 1.50 | CLOSE | +1.99% | WIN |

> \* AVIO: prezzi report errati (43.07 citato vs ~34.57 reale); entry zone 42-43.5 mai raggiunta; stop/target ineseguibili; CLOSE su apertura stimata.

---

## 5. NOTE METODOLOGICHE GIORNATA 18/6

- **OVS.MI**: Classico "sell the news" post-Q1 2026/27 (ricavi +12.1%, EBITDA +27.1%) — il titolo aveva già scontato i risultati con RSI 88.1 pre-annuncio. Apertura e max stimati; prezzo 17:00 a 6.175 EUR (-2.29%) confermato da fonti multiple.
- **IGD.MI**: Impossibile recuperare dati intraday 18/6; le fonti web restituiscono solo la seduta del 17/6. Riga inserita come ND. Il catalyst (rebalancing FTSE MidCap, giorno 2/3) era ancora attivo ma i dati non sono verificabili.
- **LTMC.MI**: Chiusura -1.60% a 25.24 confermata. Apertura/max/min stimati. Stop 24.50 non raggiunto.
- **AVIO.MI**: **Anomalia dati**: il report mattutino citava €43.07 come chiusura del 17/6, ma il prezzo reale sul mercato era ~€34.57 (errore dati nel feed del report). La seduta del 18/6 ha visto AVIO salire +2.69% a 35.5 EUR grazie al lancio di 36 satelliti Amazon con Ariane 6 (booster P160C di Avio). Entry zone 42-43.5 mai raggiunta; stop e target tutti sopra il range effettivo (35.2-38.12 EUR). Trade calcolato come CLOSE su apertura stimata. Da monitorare e correggere nella prossima seduta.
- **FBK.MI**: L'ambiente "risk-on" post-Fed (Warsh "on hold") ha favorito un rimbalzo di FBK (+1.35%). Il max intraday di 21.19 ha sfiorato per 1 centesimo l'entry zone short (21.20), ma innescato = N per formula. Lo short ha perso.
- **PIA.MI**: Il titolo ha aperto in area 1.752 (entro la entry zone short 1.73-1.78) e ha ceduto a 1.720 a fine seduta (-1.94%). Lo short ha funzionato pur con P&L contenuto (+1.99%).

---

*Generato automaticamente dal modulo Italy Intraday Tracking Bot.*
