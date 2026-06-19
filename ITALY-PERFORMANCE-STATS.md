# Italy Intraday — Statistiche di Performance

> Ultimo aggiornamento: 2026-06-19 17:00 Europe/Rome  
> ⚠️ DISCLAIMER: Backtest/forward-test a scopo esclusivamente educativo e di ricerca. NON costituisce consulenza finanziaria, raccomandazione di investimento o sollecitazione all'acquisto/vendita di strumenti finanziari. Il trading intraday comporta rischi elevati di perdita totale o parziale del capitale.

---

## 1. METRICA SEGNALE GREZZO (entry_ref → 17:00, senza gestione stop/target)

> Nota: esclude righe ND (IGD.MI 18/6 e FBK.MI 19/6 — dati prezzo non reperiti). N totale calcolabile = 8.  
> Il segnale grezzo e il piano divergono su MT.MI 19/6: lo stop è stato toccato intraday ma il titolo ha chiuso sopra l'entry_ref (+0.33% segnale vs -3.97% piano).

### Per Direzione

| Direzione | N | Win Rate % | Guadagno medio % (win) | Perdita media % (loss) | P&L cumulato % | Miglior trade | Peggior trade |
|---|---|---|---|---|---|---|---|
| LONG | 5 | 60.0% | +1.14% | -2.75% | -2.08% | AVIO.MI 18/6 +2.01% | OVS.MI 18/6 -3.89% |
| SHORT | 3 | 33.3% | +1.99% | -1.34% | -0.69% | PIA.MI 18/6 +1.99% | FBK.MI 18/6 -1.35% |
| **TOTALE** | **8** | **50.0%** | **+1.35%** | **-2.04%** | **-2.77%** | **AVIO.MI 18/6 +2.01%** | **OVS.MI 18/6 -3.89%** |

> LONG wins: IGD.MI 17/6 +1.07%; AVIO.MI 18/6 +2.01%; MT.MI 19/6 +0.33%.  
> SHORT wins: PIA.MI 18/6 +1.99%.

---

## 2. METRICA PIANO (trade gestito con Stop/Target — principale)

> Prima giornata con uno STOP attivato (MT.MI 19/6): le due metriche ora divergono.  
> Esclude righe ND (IGD.MI 18/6 e FBK.MI 19/6). N totale = 8.

### Per Direzione

| Direzione | N | Win Rate % | Guadagno medio % (win) | Perdita media % (loss) | P&L cumulato % | Miglior trade | Peggior trade |
|---|---|---|---|---|---|---|---|
| LONG | 5 | 40.0% | +1.54% | -3.15% | -6.38% | AVIO.MI 18/6 +2.01% | MT.MI 19/6 -3.97% |
| SHORT | 3 | 33.3% | +1.99% | -1.34% | -0.69% | PIA.MI 18/6 +1.99% | FBK.MI 18/6 -1.35% |
| **TOTALE** | **8** | **37.5%** | **+1.69%** | **-2.43%** | **-7.07%** | **AVIO.MI 18/6 +2.01%** | **MT.MI 19/6 -3.97%** |

> LONG wins (piano): IGD.MI 17/6 +1.07%; AVIO.MI 18/6 +2.01%.  
> SHORT wins (piano): PIA.MI 18/6 +1.99%.

### Breakdown per Grade (P&L piano)

| Grade | N (calcolabili) | P&L medio piano % | Win Rate % |
|---|---|---|---|
| A | 0 | — | — |
| B | 2 | -1.41% | 50.0% |
| C | 6 | -0.71% | 33.3% |

> Grade B: IGD.MI 17/6 +1.07% (WIN) + OVS.MI 18/6 -3.89% (LOSS). [IGD 18/6 ND; FBK 19/6 ND escluse]  
> Grade C: LTMC.MI -1.60% (LOSS) + AVIO.MI +2.01% (WIN) + FBK.MI 18/6 SHORT -1.35% (LOSS) + PIA.MI +1.99% (WIN) + MT.MI -3.97% (LOSS) + TEN.MI -1.33% (LOSS).

---

## 3. EQUITY CURVE (P&L cumulato piano, giorno per giorno)

| Data | P&L giorno % | P&L cumulato % | Trade del giorno |
|---|---|---|---|
| 2026-06-17 | +1.07% | **+1.07%** | IGD.MI LONG CLOSE +1.07% |
| 2026-06-18 | -2.84% | **-1.77%** | OVS -3.89%; LTMC -1.60%; AVIO +2.01%; FBK SHORT -1.35%; PIA SHORT +1.99% [IGD ND esclusa] |
| 2026-06-19 | **-5.30%** | **-7.07%** | MT.MI LONG STOP -3.97%; TEN.MI SHORT CLOSE -1.33% [FBK ND esclusa] |

> Nota 18/6: AVIO ha prezzi errati nel report mattutino (43.07 vs reale ~34.57 EUR); P&L calcolato su apertura reale stimata.  
> Nota 19/6: giornata di scadenza futures FTSE MIB. MT.MI: titolo salito +6.69% a chiusura ma con stop intraday a 14.37 (<14.50); STOP per regola conservativa. TEN.MI: petrolio rimbalzato a ~$77-80/bbl, short in perdita.

---

## 4. DETTAGLIO TRADE

| Data | Ticker | Dir. | Grade | Score | Innescato | Entry ref | Stop | T1 | T2 | Piano uscita | P&L segnale % | P&L piano % | Esito |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 2026-06-17 | IGD.MI | LONG | B | 63 | Y | 3.75 | 3.60 | 3.95 | 4.10 | CLOSE | +1.07% | +1.07% | WIN |
| 2026-06-18 | OVS.MI | LONG | B | 67 | Y | 6.425 | 6.10 | 6.75 | 7.20 | CLOSE | -3.89% | -3.89% | LOSS |
| 2026-06-18 | IGD.MI | LONG | B | 66 | ND | ND | 3.65 | 3.95 | 4.10 | ND | ND | ND | ND |
| 2026-06-18 | LTMC.MI | LONG | C | 57 | Y | 25.65 | 24.50 | 27.00 | 28.00 | CLOSE | -1.60% | -1.60% | LOSS |
| 2026-06-18 | AVIO.MI | LONG | C | 57 | N | 34.80* | 41.00 | 45.00 | 47.00 | CLOSE* | +2.01%* | +2.01%* | WIN* |
| 2026-06-18 | FBK.MI | SHORT | C | 58 | N | 20.77 | 22.10 | 19.90 | 19.00 | CLOSE | -1.35% | -1.35% | LOSS |
| 2026-06-18 | PIA.MI | SHORT | C | 57 | Y | 1.755 | 1.83 | 1.64 | 1.50 | CLOSE | +1.99% | +1.99% | WIN |
| 2026-06-19 | FBK.MI | LONG | B | 70 | ND | ND | 20.00 | 22.50 | 24.00 | ND | ND | ND | ND |
| 2026-06-19 | MT.MI | LONG | C | 56 | Y | 15.10 | 14.50 | 16.00 | 16.80 | **STOP** | +0.33% | **-3.97%** | **LOSS** |
| 2026-06-19 | TEN.MI | SHORT | C | 55 | Y | 24.90 | 25.80 | 23.40 | 22.00 | CLOSE | -1.33% | -1.33% | LOSS |

> \* AVIO: prezzi report errati (43.07 citato vs ~34.57 reale); entry zone 42-43.5 mai raggiunta; CLOSE su apertura stimata.

---

## 5. NOTE METODOLOGICHE

### Giornata 17/6
- **IGD.MI**: +1.07% confermato; prezzo apertura stimato al prev. close.

### Giornata 18/6
- **OVS.MI**: "Sell the news" post-Q1 2026/27; stop 6.10 non raggiunto (min 6.16).
- **IGD.MI**: Dati non reperiti; riga ND.
- **LTMC.MI**: Chiusura -1.60%; stop 24.50 non raggiunto.
- **AVIO.MI**: Anomalia dati (report citava €43.07 vs reale ~€34.57). Catalyst: lancio 36 sat Amazon con Ariane 6 (+2.69% reale).
- **FBK.MI SHORT**: Stock +1.35% in risk-on post-Fed; max 21.19 sfiorato entry zone 21.20 per 1 cent (innescato=N).
- **PIA.MI SHORT**: Aperto in entry zone; ceduto a 1.720 close; short funzionato.

### Giornata 19/6 (scadenza futures FTSE MIB — alta volatilità mattutina)
- **FBK.MI LONG**: Dati 19/6 non verificabili con certezza (fonti restituiscono ripetutamente i dati 18/6 già nel CSV). Riga ND esclusa dalle statistiche.
- **MT.MI LONG**: Titolo in forte rialzo +6.69% a €15.15 (prev. close ~€14.20). Il minimo di €14.37 ha infranto lo stop di €14.50 → STOP per regola backtesting, P&L piano = -3.97%. Il segnale grezzo è però +0.33% (chiusura €15.15 > entry_ref €15.10), evidenziando il disallineamento da path-dependency (il minimo è probabilmente avvenuto prima dell'ingresso nella zona entry, durante la volatilità da scadenza futures; il titolo è poi salito in modo quasi monotono). Stop/target ambiguità: solo stop toccato, nessun target, regola STOP applicata direttamente.
- **TEN.MI SHORT**: Petrolio ha rimbalzato a ~$77-80/bbl (accordo USA-Iran ridimensionato nei mercati), Tenaris +2.23% a €25.23. Short in perdita. Stop €25.80 non raggiunto (stima); se il max giornaliero avesse raggiunto €25.80, il P&L piano sarebbe stato -3.61%.

---

*Generato automaticamente dal modulo Italy Intraday Tracking Bot.*
