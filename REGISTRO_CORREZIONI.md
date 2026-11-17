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

## Aggiornamento v3 — 17/11/2026

La versione 3 di `sito_numeri_verificati_17nov` sostituisce integralmente v1 e v2. Integra le seguenti sette voci, da aggiungere alle cinque voci iniziali dell'11 novembre e alle correzioni già registrate sulla base della v2.

| Data | Cosa | Prima | Ora | Perché |
|---|---|---|---|---|
| 17/11/2026 | Collegamento di rete fra le macchine | Indicato come valore nominale, con proposta di rimozione | **100 Mbit/s misurati**, su schede che supporterebbero il gigabit | Misura reale dell'inventario del 10 novembre; non è il valore nominale della scheda. |
| 17/11/2026 | Riproducibilità del codice di misura V2/V3 | Confronto a coppia singola (848 prove, 106 risultati) | **30 coppie, 2.265 righe, 0 differenze di esito, 0 differenze nell'insieme delle 8 prove**; una sola differenza d'ordine a pari punteggio, presente anche fra corse dello stesso programma | La forma a coppia singola può essere scambiata per una misura di capacità; la forma a 30 coppie descrive il controllo interno di riproducibilità. |
| 17/11/2026 | Misure sulla qualità delle risposte | Presentate come se il collaudo del 22 ottobre fosse l'unica misura | Due misure distinte: collaudo cieco del 22 ottobre (57,2–68,1%) e insieme 7 del 27 ottobre (46–48/60) | La ricerca delle fonti ha individuato una seconda misura storica. Non vanno sommate né confrontate. |
| 17/11/2026 | 69/90, insieme 5 | In alcuni documenti chiamato «recuperato» | **Frase chiave fra le 8 prove consegnate**, cioè selezione; insieme 5 cieco, dominio nucleare, 23 ottobre 2026 | La fonte primaria e il protocollo definiscono la riuscita come presenza della frase chiave fra le otto prove. |
| 17/11/2026 | 46–48/60, insieme 7 | Presentato come misura cieca senza tutte le avvertenze | Resta come misura storica di risposte giudicate buone, con quattro avvertenze: differenza non significativa (p=0,25); giudici non più in servizio e risultato non ripetibile oggi; cecità valida al 27 ottobre, mentre da novembre l'insieme è sviluppo; distinzione dalle riuscite di selezione di novembre | Senza il perimetro completo il dato può essere confuso con una misura attuale o con le omonime riuscite di selezione. |
| 17/11/2026 | 119/120 citazioni autentiche | Pubblicato come risultato | **Rimosso dal sito**; conservato nel registro come dato storico del 28 ottobre senza fonte primaria ricostruibile | Compare in un riepilogo e in copie successive, ma nessun file di risultato primario lo contiene. Non confonderlo con il distinto 119/120 di accordo fra due giudici Claude. |
| 17/11/2026 | Conteggio delle voci iniziali del registro | Indicate in sei nella v2 | **Cinque** voci iniziali dell'11 novembre | Il documento sorgente contiene cinque righe, non sei; non esiste una sesta voce. |

### Esito della revisione v3

- Le misure 69/90 e 46–48/60 sono riabilitate alla pubblicazione esclusivamente con le formulazioni e le cautele del documento v3.
- Il dato 119/120 sulle citazioni autentiche deve essere assente dal sito in tutte le lingue.
- Le due misure di qualità delle risposte devono essere presentate separatamente, con date e perimetri distinti.
- La dicitura «le uniche percentuali sulla qualità delle risposte» e ogni equivalente devono essere eliminati.
- Il controllo V2/V3, se pubblicato, deve essere descritto come controllo interno di riproducibilità del codice di misura, non come risultato sulle capacità di HYDRA.
- Le sette voci sopra riportate si aggiungono alle cinque voci iniziali effettivamente presenti nel documento dell'11 novembre.

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
| 17/11/2026 | Aggiornamento di `index.html` e controllo delle sette lingue sulla base della v3 | Prima revisione completata nel ramo di lavoro; corretti i numeri principali e aggiunte le misure di novembre in IT, EN, ES, DE, FR, PL e ZH. Verifica puntuale finale ancora in corso. |
| 17/11/2026 | Ricerca su Testa A delle fonti per 69/90, 119/120 e 46/60–48/60 | Completata secondo il documento v3: 69/90 resta come selezione; 46–48/60 resta con quattro avvertenze; 119/120 citazioni autentiche va rimosso dal sito per assenza di fonte primaria. |
| 17/11/2026 | Verifica finale del ramo di lavoro | Controllati i sette dizionari linguistici, la presenza delle nuove chiavi, i numeri obsoleti elencati nella v3 e la corrispondenza dei tag HTML principali. Restano da eseguire il controllo visivo nel browser e il confronto finale con il ramo principale. |
| — | Merge e pubblicazione | Non eseguiti; richiedono approvazione esplicita. |


## Aggiornamento v4 — sera del 17 novembre 2026

La versione 4 del documento `sito_numeri_verificati_17nov` sostituisce integralmente v1, v2 e v3 come fonte editoriale. Le seguenti cinque correzioni serali si aggiungono allo storico; non cancellano le formulazioni precedenti, ma ne registrano il superamento.

| Data | Cosa | Prima | Ora | Perché e fonte |
|---|---|---|---|---|
| 17/11/2026 sera | Riga «Segnale» dei 50 insuccessi | Le 20 domande erano descritte come 20 fallimenti indistinti del sistema | Le 20 domande avevano tutte le 8 prove complete; nella campagna del lettore circa 10 delle 17 giudicabili hanno avuto risposta finale corretta secondo il controllo automatico numerico. Il riferimento resta **161/211**. | La campagna del lettore mostra che la riga misura il mancato segnale automatico, non necessariamente un errore della risposta finale. I conteggi automatici non sono una misura generale di qualità e non vanno convertiti in percentuali pubbliche. |
| 17/11/2026 sera | Esperimenti di novembre | Cinque esperimenti | **Sette esperimenti**: sei senza vantaggio misurabile o con effetto minimo/non adottato; uno mantenuto, la divisione deterministica della domanda (**+3**, da 158/211 a 161/211). | Aggiunti l'irrigidimento della regola sulla premessa (0 recuperi su 17, 7 falsi segnali) e il confronto delle istruzioni del lettore (28/45 con entrambe, p = 1). Conservare gli esiti negativi. |
| 17/11/2026 sera | Esperimento medicina/astronomia | Vettorializzazione indicata come «in corso» | **Vettorializzazione completata**: 100.023 frasi, 2.285 file, sei modelli, quattro macchine; 3 h 21 min, 581 minuti GPU cumulati, parallelismo 2,9×. Le 86 domande utilizzabili dell'insieme 9 sono state vettorializzate con tutti e sei i modelli. La misura comparativa non è stata eseguita. | Le sei corse sono terminate alle 17:00 circa del 17/11; nessuna conclusione sulle prestazioni dei modelli è ancora disponibile. Fonte: verbale `verbale_vettorializzazione_17nov_v2.md` e registri delle corse. |
| 17/11/2026 sera | Qualità del corpus selezionato | Qualità del sottoinsieme non dichiarata | **0 frasi doppie su 100.023 (0,000%)**, secondo la definizione congelata, e 0 anomalie; 608 note senza punto (0,608%); stima delle doppie nascoste fra queste circa 155, pari allo **0,155%** (intervallo 0,115–0,195%). | Misura eseguita sul campione effettivamente vettorializzato. Il precedente 0,00% sui domini interi non sostituiva il controllo sul sottoinsieme. |
| 17/11/2026 sera | Riproducibilità dei vettori | Registri a schermo arrotondavano il coseno minimo a 1,000000 | **0,99999997** per i cinque modelli ricalcolati; granite è stato copiato dall'indice, con perdita float16 0,00. Soglia del protocollo: 0,9999. | Riportare il valore non arrotondato. La copia di granite non va descritta come una nuova corsa di calcolo. |

### Chiarimenti editoriali vincolanti della v4

- La nota accanto alla riga «Segnale» deve chiarire che le 20 prove erano complete e che i risultati della campagna del lettore sono diagnostici, non una misura generale di qualità delle risposte.
- Non pubblicare percentuali derivate dai voti automatici del lettore.
- Non scrivere che HYDRA «riconosce le premesse false» come capacità acquisita: il controllo attuale verifica la presenza di numeri, anni e nomi, non la loro attribuzione.
- La vettorializzazione di medicina e astronomia è conclusa; la valutazione comparativa è ancora da eseguire. Non anticipare risultati.
- La v4 del documento dei numeri verificati è la fonte corrente per tutte le sette lingue. Ogni numero non elencato richiede verifica prima della pubblicazione.


### Nota di verifica editoriale — denominatore della campagna del lettore

Nel documento v4 il § 5 riporta «28 contro 28 su 51 trappole», mentre la tabella analitica del § 7bis riporta «28 su 45 giudicabili» per ciascuna istruzione. I due denominatori non sono conciliati esplicitamente nel documento. In attesa di chiarimento, sul sito il confronto è riportato come **28 contro 28, p = 1**, senza denominatore; resta esplicitato il dato distinto **10/17** e **13/17** per i soli casi giudicabili di fallimento del segnale. Non si assume che i 6 casi di differenza siano semplicemente non giudicabili.
