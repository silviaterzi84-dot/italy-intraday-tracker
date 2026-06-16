# Italy Intraday — Statistiche di Performance

**Ultimo aggiornamento:** 2026-06-16 17:00 Europe/Rome
**Periodo coperto:** 2026-06-16 → 2026-06-16
**Totale trade tracciati:** 2

---

> ⚠️ **DISCLAIMER:** Analisi AI a scopo educativo e di ricerca. NON è consulenza finanziaria. I risultati rappresentano un backtest/forward-test simulato. Il trading intraday comporta rischi elevati di perdita del capitale. Past performance is not indicative of future results.

---

## 1. METRICA SEGNALE GREZZO (Entry → 17:00, senza gestione stop/target)

### Totale (LONG + SHORT)

| Metrica | Valore |
|---|---|
| N trade | 2 |
| Win rate | 0% (0/2) |
| Guadagno medio % (vincenti) | n/a |
| Perdita media % (perdenti) | -0.94% (media: AVIO -1.80% + BMED -0.08%) |
| P&L cumulato % | -1.88% |
| Miglior trade | BMED.MI -0.08% |
| Peggior trade | AVIO.MI -1.80% |

### Per Direzione

| Direzione | N | Win% | P&L medio | P&L cumulato |
|---|---|---|---|---|
| LONG | 2 | 0% | -0.94% | -1.88% |
| SHORT | 0 | — | — | — |

---

## 2. METRICA PIANO (Trade gestito con Stop/Target)

### Totale (LONG + SHORT)

| Metrica | Valore |
|---|---|
| N trade | 2 |
| WIN | 0 (0%) |
| LOSS | 1 (AVIO.MI -1.80%) |
| BE | 1 (BMED.MI -0.08%) |
| Win rate | 0% |
| Guadagno medio % (vincenti) | n/a |
| Perdita media % (perdenti) | -1.80% (solo AVIO) |
| P&L cumulato % | -1.88% |
| Miglior trade | BMED.MI -0.08% (BE) |
| Peggior trade | AVIO.MI -1.80% (LOSS) |

### Per Direzione (Piano)

| Direzione | N | WIN | LOSS | BE | Win% | P&L medio | P&L cum. |
|---|---|---|---|---|---|---|---|
| LONG | 2 | 0 | 1 | 1 | 0% | -0.94% | -1.88% |
| SHORT | 0 | — | — | — | — | — | — |

---

## 3. BREAKDOWN PER GRADE (Metrica Piano)

| Grade | N | P&L medio piano | Esiti |
|---|---|---|---|
| A | 1 | -1.80% | AVIO.MI — LOSS (CLOSE sotto entry) |
| B | 0 | — | — |
| C | 1 | -0.08% | BMED.MI — BE (CLOSE sostanzialmente flat) |

---

## 4. DETTAGLIO TRADE

| Data | Ticker | Dir | Grade | Score | Entry ref | Stop | T1 | T2 | Innesc. | P17:00 | PnL Segn% | PnL Piano% | Uscita | Esito |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 2026-06-16 | AVIO.MI | LONG | A | 81 | 36.05 | 34.00 | 38.50 | 41.00 | Y | 35.40 | -1.80% | -1.80% | CLOSE | LOSS |
| 2026-06-16 | BMED.MI | LONG | C | 56 | 19.75 | 18.70 | 21.00 | 22.00 | Y | 19.735 | -0.08% | -0.08% | CLOSE | BE |

**Nota AVIO.MI:** Apertura gap-up a 36.64 grazie a SpaceX, max intraday 37.07 (T1 a 38.50 non raggiunto), poi inversione con chiusura a 35.40 (-0.25%). Stop a 34.00 non toccato (min 35.20). Sessione nervosa nonostante il bias RISK-ON.

**Nota BMED.MI:** Max 20.30, min 19.585. T1 a 21.00 non raggiunto. Chiusura a 19.735 sostanzialmente flat rispetto all'entry ref (19.75). Apertura non disponibile (ND).

---

## 5. EQUITY CURVE TESTUALE (P&L Piano cumulato per giorno)

| Data | Trade | P&L Giorno (piano) | P&L Cumulato |
|---|---|---|---|
| 2026-06-16 | AVIO.MI -1.80% / BMED.MI -0.08% | -1.88% | -1.88% |

*Un solo giorno di dati — insufficiente per conclusioni statistiche robuste.*

---

## 6. NOTE METODOLOGICHE

- **Universo:** FTSE Italia MidCap + SmallCap. Shortlist operativa Score >= 55.
- **Entry ref:** media zona entry (entry_low+entry_high)/2 se innescato; altrimenti prezzo_apertura.
- **Gestione piano:** Stop pieno se min_giornata <= stop (LONG). Poi T2, T1+CLOSE (50/50), altrimenti CLOSE a prezzo_1700.
- **Ambiguità stop/target:** conservativamente assunto stop per primo.
- **Dati prezzo:** ricavati da ricerche web (Soldionline, BorsaInsida, Google Finance, Investing.com). Possibili approssimazioni segnalate in note CSV.
- **Data inizio tracking:** 2026-06-16

---

*Generato automaticamente da Italy Intraday Tracking Bot — 2026-06-16*
