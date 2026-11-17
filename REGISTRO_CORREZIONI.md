# Registro delle correzioni — sito HYDRA

## Introduzione

Quando un numero o un'interpretazione pubblicata risulta sbagliata o superata, la correggiamo e lo scriviamo qui: data, cosa è cambiato, perché, e da dove viene il dato corretto. Le modifiche solo grafiche non sono registrate.

Il registro è stato creato nel repository il 17 novembre 2026. Il documento preparatorio dell'11 novembre era rimasto fuori dal repository; le sue voci sono riportate qui come storico iniziale, senza fingere che il registro fosse già stato creato allora.

Ramo di lavoro: `aggiornamento-dati-verificati-2026-11-17`.

**Stato:** registro aggiornato sulla base dei due documenti forniti il 17/11/2026. Le voci descrivono correzioni e verifiche da recepire nel sito; non attestano che tutte le modifiche siano già state applicate o pubblicate. Il ramo principale e il sito pubblico restano invariati fino alla verifica e all'approvazione finale.

## Storico iniziale — 11 novembre 2026

Le seguenti sono tutte le voci effettivamente presenti nella tabella del § 3 di `sito_modifiche_11nov_v1.md`. Il documento allegato contiene **cinque** righe, non sei; non è stata inventata una sesta voce.

| Data | Cosa | Prima | Ora | Perché |
|---|---|---|---|---|
| 11/11/2026 | Correttezza dei fatti estratti da più modelli (pilota del 22/10, 615 fatti) | circa 60–80% | **57,2–68,1%**, secondo il criterio di combinazione dei due arbitri | Il valore precedente veniva da un riepilogo, non dalla misura. Ricalcolato dai voti originali dei due arbitri ciechi. Anche il periodo era indicato male: era il pilota di ottobre, non agosto–settembre. |
| 11/11/2026 | Frasi utili e righe dell'indice | 9,96 milioni; 19,4 milioni | **9,99 milioni; 19,5 milioni** | Il dato precedente era di prima del terzo passaggio della correzione dell'indice. |
| 11/11/2026 | Frasi dei 109 documenti nucleari usate da Hydra Evolution | 49.878 | **49.942** | 49.878 era il numero sull'indice prima della correzione; 49.942 è sull'indice corretto. Il valore precedente resta valido come dato storico. |
| 11/11/2026 | Protocollo di Hydra Evolution | "congelato prima del calcolo" | **congelato in due fasi**: prima del calcolo dei vettori; i programmi di misura prima di qualunque misura | Descrizione più precisa di quanto avvenuto. |
| 11/11/2026 | Storico delle sperimentazioni | la formula "non pianificato per il ripristino" sembrava riferita anche al grafo e all'estrazione dei fatti | riferita **solo** al giudice locale | Grafo ed estrazione dei fatti saranno rimisurati nelle condizioni nuove. |

## Correzioni e aggiornamenti — 17 novembre 2026

| Data | Cosa | Prima / formulazione da correggere | Dato o formulazione corretta | Motivo, fonte e stato |
|---|---|---|---|---|
| 17/11/2026 | Conteggio delle frasi utili/cercabili | 9.993.295 (in precedenza anche 9,96 milioni) | **10.048.158 frasi cercabili**: righe dell'indice non marcate come rumore e con testo non vuoto; misura del 16/11 | La definizione di "utile" è diversa rispetto ai conteggi precedenti. Sul sito usare solo il dato del 16/11 con la definizione esplicita. Fonte: `conta_frasi_domini_v1.py`, Testa A. **Da applicare e verificare nelle sette lingue.** |
| 17/11/2026 | Righe dell'indice e lotti vettoriali | Dato arrotondato o confuso con il numero di frasi utili | **19.486.768 righe** nella tabella `lotto` di `indice_frasi/frasi.sqlite`; **1.200 lotti** | Sono conteggi distinti dalle frasi cercabili. Fonte: `lotti_indice_v1.txt`, 16/11. **Da applicare.** |
| 17/11/2026 | Altri conteggi dell'indice | Non specificati o non distinti | **9.987.317** frasi utili in domini attivi non protetti; **589.833** file attivi fuori dai domini protetti | Conteggi del 16/11 prodotti da `conta_frasi_domini_v1.py`. **Da applicare.** |
| 17/11/2026 | Dominio nucleare | Conteggi storici non accompagnati dalla definizione/perimetro aggiornato | **110 file attivi; 49.942 frasi utili**, misura dell'11/11 | Fonte: `verifica_base_fase2_v8.py`. Non confondere con conteggi storici ottenuti con criteri diversi. **Da applicare.** |
| 17/11/2026 | Collegamento di rete fra le macchine | "100 Mbit/s nominali" oppure proposta precedente di eliminare il dato | **100 Mbit/s misurati** fra le macchine, su schede che supporterebbero il gigabit | La v2 del documento numeri chiarisce che il valore è una misura reale dell'inventario del 10/11, non la velocità nominale delle schede. La precedente indicazione di rimuoverlo era errata. **Da correggere nel sito.** |
| 17/11/2026 | Perimetro delle misure di novembre | Risultati presentati senza chiarire che cosa misurano | Misurano il recupero delle evidenze: una domanda riesce solo se tutte le frasi chiave attese sono incluse nelle 8 frasi selezionate | Non misura la qualità della risposta finale; il modello generativo non gira. Solo dominio nucleare (49.942 frasi) e insiemi di sviluppo, non prove indipendenti. **Da esplicitare accanto ai risultati.** |
| 17/11/2026 | Risultato di riferimento | Baseline precedente di 158/211 senza divisione deterministica della domanda | **161/211** con Arcangeli attivi, divisione della domanda a regole fisse attiva, sigle e vocabolario spenti, nessun grafo come filtro; 259/268 frasi chiave fra i candidati e 234/268 fra le 8 prove | Misura del 17/11 su 211 domande di sviluppo. **Da pubblicare con perimetro e configurazione.** |
| 17/11/2026 | Ripartizione degli insuccessi | Mancava una diagnosi distinta dei punti di perdita | **21 selezione; 20 segnale di premessa falsa; 9 recupero** | Le 50 domande fallite sono ripartite per il punto in cui si perde l'evidenza o manca il segnale. Fonte: risultato di riferimento del 17/11. **Da aggiungere.** |
| 17/11/2026 | Esperimenti comparativi di novembre | Rischio di presentare solo gli esperimenti favorevoli o di attribuire vantaggi generali | Cinque esiti: 63 combinazioni di 6 embedding senza vantaggio (pareggio sul set di conferma); 4 piccoli modelli linguistici per la scomposizione senza vantaggio (da −1 a +1); vocabolario sinonimico 0; sigle +1; divisione a regole fisse +3, mantenuta | Base 158/211 senza divisione, 161/211 dopo. Il vantaggio di bge-m3 non si conferma: 47/60, pari a granite, sul set di conferma. **Da aggiungere includendo gli esiti negativi.** |
| 17/11/2026 | Test di robustezza | Nessuna distinzione tra le perturbazioni testate | Rimozione nomi propri: 133/211 (−28; McNemar esatto p=2,5×10⁻⁷); rimozione anni: 158/211 (−3, non significativo); sinonimo: 160/211 (−1, non significativo); rimozione numeri: 160/211 (−1, non significativo) | Dei 30 casi persi togliendo i nomi, in 22 la frase chiave era ancora fra i candidati. Sono state provate quattro perturbazioni soltanto: non concludere che solo i nomi contino. **Da aggiungere con cautela.** |
| 17/11/2026 | Riproducibilità del codice di misura V2/V3 | Vecchia formulazione: 848 prove e 106 risultati identici in una singola corsa | **30 coppie di corse; 2.265 righe confrontate; 0 differenze di esito; 0 differenze nell'insieme delle 8 prove; 1 differenza di solo ordine** fra prove a pari punteggio | La differenza d'ordine si ripresenta anche fra due corse dello stesso programma e dipende dalle librerie di calcolo. Va descritto come controllo interno di riproducibilità del codice di misura, non come prestazione/capacità di HYDRA. **Sostituire la vecchia forma; pubblicare solo se la distinzione è chiara in tutte le lingue.** |
| 17/11/2026 | Avvio Multi-RAG medicina/astronomia | Stato non indicato o risultato anticipato | Esperimento avviato il 17/11, **risultato in corso**: 100.023 frasi, 2.285 file (910 medicina, 1.375 astronomia), sei modelli, quattro macchine; SHA-256 iniziale `d4688477d4c25b3e` | Non è ancora possibile affermare che l'ipotesi sia confermata o smentita. **Da aggiungere come attività in corso, senza anticipare esiti.** |
| 17/11/2026 | Percentuali di qualità delle risposte | Percentuali senza data o perimetro, oppure generica indicazione "60–80%" | Unico riferimento disponibile: collaudo cieco del 22/10/2026, arbitro 1 58,7%; arbitro 2 66,7%; lettura prudente 57,2%; lettura larga 68,1% | Si riferiscono a quel collaudo e a quel corpus, non sono una misura attuale. Il numero di domande non è indicato nel documento v2; non inventarlo. **Verificare il testo attuale e accompagnare ogni dato con data e perimetro.** |
| 17/11/2026 | Risultati storici 69/90, 119/120 e 46/60–48/60 | Numeri presenti nel sito, ma non inclusi nel documento dei numeri verificati v2 | **Nessuna correzione numerica autorizzata per ora** | La loro assenza dal documento v2 significa che non sono stati verificati in questa revisione, non che siano falsi. Galliano deve cercarne le fonti su Testa A. Se fonte con data e perimetro: mantenere con tali dettagli; se fonte senza perimetro: rimuovere dal sito e registrare come storico senza perimetro; se nessuna fonte: rimuovere numero e frase. **In attesa della ricerca su Testa A.** |
| 17/11/2026 | Affermazioni non supportate | "60–80%", superiorità generale sul RAG tradizionale, vantaggio generale multi-embedding, certificazioni/conformità, copertura presentata come certificata, grafo come filtro candidati, nomi interni | Eliminare tali affermazioni; non usare "Lucifero" o nomi interni nella comunicazione pubblica | Il documento numeri v2 non fornisce supporto per queste affermazioni; il grafo come filtro è stato provato e abbandonato perché peggiorava. Tracciabilità e ripetibilità possono essere descritte come principi di progetto, non certificazioni. **Controllare tutte le sette lingue.** |

## Regole editoriali e di verifica

1. Una sola fonte per ogni numero. Se un numero appare in più punti o lingue, deve essere identico e provenire dalla stessa fonte indicata.
2. Ogni numero deve avere data, perimetro e definizione; non inventare date o periodi per misure precedenti.
3. Distinguere dati misurati, risultati su insiemi di sviluppo, prove cieche indipendenti, ipotesi e attività in corso.
4. Conservare anche gli esiti negativi e inconcludenti.
5. Non presentare i risultati di sviluppo come risultati indipendenti né come punteggio complessivo di HYDRA.
6. Se un dato non è verificabile, rimuovere la frase dal sito invece di riscriverla in modo più vago.
7. I dati storici non si cancellano dal registro: si annota quando e perché sono stati sostituiti.
8. Le traduzioni nelle sette lingue devono mantenere le stesse cautele e lo stesso perimetro, non soltanto gli stessi numeri.

## Tracciamento delle verifiche

| Data | Attività | Esito |
|---|---|---|
| 11/11/2026 | Preparazione del documento `sito_modifiche_11nov_v1.md` | Registro progettato e cinque prime voci redatte nel documento; il registro non fu creato nel repository in quella data. |
| 17/11/2026 | Verifica del repository | Nessun registro precedente trovato; presenti `index.html` e `README.md`. |
| 17/11/2026 | Creazione del registro nel repository | Creato nel ramo `aggiornamento-dati-verificati-2026-11-17`, includendo le cinque voci storiche effettivamente presenti nell'allegato. |
| 17/11/2026 | Revisione sulla base di `sito_numeri_verificati_17nov_v2.md` | Integrate le correzioni della v2, inclusi rete misurata, controllo V2/V3 su 30 coppie e stato di verifica dei tre risultati storici. |
| — | Aggiornamento di `index.html` e controllo delle sette lingue | Da completare. |
| — | Ricerca su Testa A delle fonti per 69/90, 119/120 e 46/60–48/60 | Da eseguire da Galliano; nessuna decisione di rimozione presa. |
| — | Verifica finale e confronto con il ramo principale | Da completare. |
| — | Merge e pubblicazione | Non eseguiti; richiedono approvazione esplicita. |
