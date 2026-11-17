# Registro delle correzioni — revisione 2026-11-17

## Scopo e stato

Questo registro viene istituito in questo ramo perché nel repository, al momento della verifica del 17 novembre 2026, non è stato individuato un registro precedente. Non si presume quindi uno storico che non è stato possibile recuperare.

Ramo di lavoro: `aggiornamento-dati-verificati-2026-11-17`

Stato iniziale: **aperto**. Le voci sotto descrivono le correzioni richieste e i controlli da completare; non attestano che il sito sia già stato aggiornato o pubblicato. Il ramo principale e il sito pubblicato non devono essere modificati in questa fase.

## Correzioni richieste per il sito

| ID | Area | Correzione / dato da usare | Stato |
|---|---|---|---|
| C-001 | Indice generale | Sostituire il vecchio conteggio di 9.993.295 frasi utili (e ogni variante precedente) con **10.048.158 frasi utili ricercabili**, definizione: frasi non marcate come rumore e con testo non vuoto; rilevazione 16/11/2026. | Da applicare e verificare in tutte le lingue |
| C-002 | Indice generale | Distinguere **19.486.768 righe** nella tabella `lotto` di `indice_frasi/frasi.sqlite` da **10.048.158 frasi utili ricercabili**; non presentarli come conteggi equivalenti. | Da applicare |
| C-003 | Indice generale | Indicare **1.200 lotti vettoriali**; **9.987.317** frasi utili nei domini attivi non protetti; **589.833** file attivi fuori dai domini protetti. Rilevazioni del 16/11/2026. | Da applicare |
| C-004 | Dominio nucleare | Dato aggiornato: **110 file attivi, 49.942 frasi utili**, rilevazione 11/11/2026. Non sostituire con il conteggio storico di 58.096 senza spiegare la diversa base di conteggio. | Da applicare |
| C-005 | Infrastruttura | Descrivere l'infrastruttura verificata: **4 PC di recupero**; GPU: una GTX 1660 Super da 6 GB e tre schede da 4 GB (una Quadro P1000 e due Quadro K2200). Rimuovere l'affermazione non verificata sulla rete a 100 Mbit/s. | Da applicare |
| C-006 | Misure novembre | Spiegare che il test misura il recupero delle evidenze: per ogni domanda HYDRA seleziona 8 frasi; successo solo se tutte le frasi chiave attese sono presenti nelle 8. Non è una misura della qualità della risposta finale e il modello generativo non è stato eseguito. Dominio nucleare, 49.942 frasi; 211 domande di sviluppo, non indipendenti né blind. | Da applicare |
| C-007 | Risultato di riferimento | Configurazione del 17/11/2026: Arcangeli attivi, suddivisione deterministica delle domande attiva, sigle e vocabolario disattivati, nessun filtro a grafo. Esito: **161/211** domande riuscite; **268** frasi chiave attese, **259/268** tra i candidati recuperati e **234/268** nelle 8 prove finali. | Da applicare |
| C-008 | Analisi errori | Rendere visibile la ripartizione dei 50 insuccessi: **21 selezione** (frase chiave tra i candidati ma fuori dalle 8 prove), **20 segnalazione di premessa falsa** (trappole non segnalate), **9 recupero**. Non confondere le categorie. | Da applicare |
| C-009 | Set di domande | Specificare: ESPERIENZA45 sviluppo; Set7 60 sviluppo; Set8 106 sviluppo; Set9 224 righe, 86 utilizzabili, passato allo sviluppo il 16/11 e relativo a nucleare/medicina/astronomia; PROVA blind e mai usato; Set5/Set6 sigillati. Le misure di novembre qui riportate usano 211 domande (45+60+106). | Da applicare |
| C-010 | Esperimenti novembre | Riportare i cinque esiti, compresi quelli negativi: 6 modelli embedding e 63 combinazioni senza vantaggio (parità nel set di conferma); 4 piccoli modelli linguistici per la suddivisione senza vantaggio (da −1 a +1); vocabolario sinonimico senza effetto (0); sigle/grafo acronimi effetto minimo (+1); suddivisione deterministica a regole mantenuta (+3, da 158/211 a 161/211). Non generalizzare la selezione di bge-m3: sul set di conferma 47/60, pari a granite. | Da applicare |
| C-011 | Robustezza | Pubblicare i quattro test del 16/11 con cautela: rimozione nomi propri 133/211 (−28; McNemar esatto p=2,5×10⁻⁷); rimozione anni 158/211 (−3, non significativo); sostituzione con sinonimo 160/211 (−1, non significativo); rimozione numeri 160/211 (−1, non significativo). Dei 30 casi persi rimuovendo i nomi, in 22 la frase chiave era ancora tra i candidati. Limitare le conclusioni a queste quattro perturbazioni. | Da applicare |
| C-012 | Multi-RAG medicina/astronomia | Indicare come **esperimento avviato il 17/11/2026, risultato in corso**: 100.023 frasi da 2.285 file (medicina 50.013 frasi/910 file; astronomia 50.010 frasi/1.375 file), sei modelli, quattro macchine. Corpus identificato dal prefisso SHA-256 `d4688477d4c25b3e`. Non anticipare conclusioni. | Da applicare |
| C-013 | Qualità risposta | Se mantenute, isolare le percentuali disponibili dal test blind del 22/10/2026: giudice 1 58,7%; giudice 2 66,7%; lettura conservativa 57,2%; lettura ampia 68,1%. Non sono misure attuali e non va inventato il numero di domande. | Da verificare / eventualmente rimuovere |
| C-014 | Affermazioni non supportate | Eliminare “60–80%”, confronti generali di superiorità rispetto al RAG tradizionale, vantaggi dichiarati dei multi-embedding, certificazioni/conformità, copertura presentata come certificata e grafo presentato come filtro candidati. Non pubblicare nomi interni dei componenti. | Da applicare |
| C-015 | Lingue | Controllare tutte e sette le versioni linguistiche: numeri, date, definizioni, qualifiche dei set di sviluppo, risultati negativi e stato “in corso” devono essere coerenti. | Da completare |

## Regole editoriali

1. Ogni numero deve avere data, ambito e definizione.
2. Separare dati misurati, risultati di sviluppo, test blind indipendenti, ipotesi e attività in corso.
3. Non trasformare un risultato circoscritto in una conclusione generale.
4. Conservare gli esiti negativi e inconcludenti: fanno parte dei risultati.
5. Se un dato non è verificabile, rimuoverlo invece di riscriverlo in modo vago.
6. Le modifiche restano nel ramo di lavoro fino alla verifica completa; pubblicazione e merge richiedono una decisione esplicita.

## Tracciamento delle verifiche

| Data | Attività | Esito |
|---|---|---|
| 17/11/2026 | Verifica iniziale del repository | Individuati `index.html` e `README.md`; nessun registro delle correzioni trovato nel repository. |
| 17/11/2026 | Creazione di questo registro | Prima versione creata nel ramo separato; nessuno storico precedente ricostruito. |
| 17/11/2026 | Revisione delle sette lingue e aggiornamento di `index.html` | Da completare. |
| — | Verifica finale, controllo dei dati e confronto con il ramo principale | Da completare. |
| — | Eventuale merge/pubblicazione | Non autorizzato in questa fase. |
