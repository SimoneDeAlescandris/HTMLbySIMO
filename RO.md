<!-- 
COLORI:
- ROSSO: #DF5452;
- GRIGIO: #252525;
- BLU: #379AD3;
- VERDE: #529E72;
- GIALLO: #FDDC5C.
-->

# Ricerca Operativa  

## Indice  

- [Introduzione](#introduzione)  
  - [MODELLi della Ricerca Operativa](#modelli-della-ricerca-operativa)
- [Bibliografia](#bibliografia)  

## Introduzione  

> "*OR can help you in make better decision and it is clear that there are many, many people and companies out there in the real world that need to make better decision*."  
> - J. E. Bearsley  

<div style="background-color: #252525; border-radius: 10px; padding: 15px; box-shadow: 0.5px 0.5px 2px black; margin-bottom: 1em;">  

La <abbr style="font-weight:bold;" title="dall’inglese Operational Research, OR, o Management Science, MS, o Decision Science, DS">Ricerca Operativa</abbr> si occupa di studiare e <u>gestire i processi decisionali</u> (com’era intuibile dal nome) per valutarne le conseguenze e individuare le decisioni che ottimizzano le loro prestazioni attraverso l’applicazione del metodo scientifico.  

In altre parole, <span style="background-color:#FDDC5C; color:black; padding:1px; border-radius: 4px;">si occupa di trovare la <i>migliore</i> soluzione <i>possibile</i> di un dato problema reale</span>.  

- il termine «***possibile***» richiede di poter distinguere una soluzione che possa essere utilizzata nella pratica, detta «soluzione ammissibile», da una che non può esserla.  
- il termine «***migliore***» richiede di poter confrontare due soluzioni ammissibili, distinguendo la migliore dalla peggiore, o stabilendo che le due soluzioni sono equivalenti.  

<details>  
<summary style="margin-bottom:0.5em; font-weight:bold;">PERCHÉ e QUANDO è nata?</summary>  
<div style="margin-bottom:0.5em; border: 1px solid #aaa; border-radius: 0 0 4px 4px; padding: 1em; margin-top: -1px;">

  > Riassumendo potremmo dire che questa disciplina nasce negli anni appena precedenti alla WWII con la formazione di un team di scienziati (*OR-Team*) per studiare problemi tattici e strategici in operazioni militari.  

  ---

  La RO nasce come disciplina autonoma al fine di progettare e gestire sistemi complessi facendo uso di **strumenti matematici e informatici** anche molto avanzati che permettono di **determinare soluzioni efficienti** nelle diverse realtà applicative.  

  **L’origine e l’etimologia del nome è bellica ed ha sede britannica**:  

  <details>  
  <summary style="margin-bottom:0.5em;">La sua prima iterazione si ebbe nel 1936, pochi anni prima dello scoppio delle bombe atomiche in Giappone, per merito della Royal Air Force (RAF) britannica che stava conducendo un esperimento (<i>Biggin Hill Experiment</i>) sull’uso del radar per la difesa aerea, provando ad integrare i dati ottenuti dai radar con quelli osservati a terra.</summary>  

  > Successivamente, nel 1937 vi fu la prima esercitazione e i **risultati** furono abbastanza **soddisfacenti per la parte tecnica** del radar, ma non lo furono per la parte gestionale. L’intuzione che si ebbe per migliorare la copertura di questi radar fu quella di aggiungere altre 4 stazioni radar nel 1938, anno della seconda esercitazione. Da questa scelta, indirettamente, **aumentò la difficoltà** di integrare la mole di dati che adesso avevano a disposizione, ovvero gli **aspetti operativi**.
  > 
  > Colui che redasse in seguito la relazione conclusiva del progetto utilizzò l’espressione "*Operational Research*" e questa fu la prima volta nella storia che questa espressione venne utilizzata. Nella sua mente ciò doveva significare "*Ricerca nelle Operazioni* (militari)".  
  >    
  > L’ultima esercitazione pre-bellica la si fece nel 1939, con l’ausilio di una buona integrazione dei dati che venivano sia dai radar che dai velivoli. Nel 1940 poi grazie agli studi realizzati dall’***O.R.-Team*** (un gruppo di studiosi appartenenti a tante branchie diverse, a dimostrazione del fatto che questa è una scienza molto interdisciplinare) vennero salvati molti piloti e aerei, riconoscendo definitivamente gli importanti contributi strategi di questa tecnica nel conflitto mondiale. Nel 1941, poi, con la nascita formale della "***Operational Research Section***" abbiamo il primo tentativo di integrare, in un unico gruppo di ricerca, scienziati di origini e competenze diverse, aventi tutti un unico scopo finale. Il successo fu tale da far nascere nuovi gruppi simili anche negli altri paesi e si stima che nel corso della Seconda Guerra Mondiale furono complessivamente impegnati tra Gran Bretagna, USA e Canada oltre 700 scienziati.  
  </details>

  <details>  
  <summary style="margin-bottom:0.5em;">Al termine del conflitto vi fu una «riconversione» dell’approccio verso altri settori diversi da quello militare, ma il suo sviluppo e la sua espansione non furono uniformi poiché richiedevano un alto investimento iniziale in termini di costi dovuti all’acquisito dei <a href="./Architettura.md/#first-generation-1945-1955-vacuum-tubes">primi calcolatori</a></summary>.  

  > In particolare, vi furono differenze abissali nella sua diffusione tra l’Italia e gli USA (che prendiamo come riferimento per indicare il resto del mondo):  
  > 
  > - In **Italia** si resero conto dell’utilità del modello quantitativo, ma non essendoci persone particolarmente esperte della disciplina questi sistemi informativi erano utilizzati in maniera limitate e per lo più gestivano principalmente grossi database, lasciando inoltre la decisione su come risolvere il problema ad una persona con esperienza nell’ambito, rendendo quindi questo solo uno **strumento a supporto delle decisioni**.  
  > - Negli USA, invece, dopo un grande successo (ed entusiasmo) della disciplina, che si ebbe sino agli anni Settanta, vi fu un «ridimensionamento», dovuto alla mancanza di strumenti di calcolo potenti (i pc non sono ancora abbastanza efficienti e convenienti per essere utilizzati dalle aziende) e all’inadeguatezza dei metodi risolutivi utilizzati (soprattutto in relazione a problemi di grandi dimensioni).  
  </details>

  ---

  In anni più recenti nel mondo del lavoro ci sono proprio figure professionali specifiche (come ingegneri informatici o gestionali) per questa disciplina all’interno delle aziende e, attualmente, la richiesta di esperti di RO in ambiti industriali e nei servizi è MOLTO forte.    
</div></details>  

*La sensibilità nei confronti della RO è fortemente cresciuta, assieme alla **consapevolezza che l’accresciuta potenza di calcolo non è da solo sufficiente a permettere la risoluzione dei problemi***.  

<details>  
<summary style="margin-bottom:0.5em;">A dimostrazione della suddetta affermazione propongo il famoso <strong style="color:#529E72;">esperimento di George Dantzig</strong>.</summary>  
  <div style="margin-bottom:0.5em; border: 1px solid #aaa; border-radius: 0 0 4px 4px; padding: 1em; margin-top: -1px;">

  Si tratta di un problema di assegnamento che chiede di assegnare univocamente **70 persone** a 70 mansioni. Ciò che ci interessa è il lavoro utile (profitto) prodotto da una persona nello svolgere la sua mansione, cioè trovare il lavoro che egli è in grado di svolgere meglio.  

  Di seguito ho creato una matrice. Il mio scopo è quindi quello di mettere un asterisco per ogni persona in modo che tutte le righe e colonne alla fine siano completate e abbiano un solo asterisco. Come dati del problema abbiamo inoltre il profitto che la persona $\small i$-esima ottiene nell’essere assegnata alla mansione $\small j$-esima.  

  <img src="./img/ro/Dantzig.png" title="Matrice fra persone e mansioni" width="60%" height=auto style="margin-bottom:1rem;">  

  Se ci affidassimo al buon senso, proveremmo a capire il valore utile che la persona $\small i$-esima ottiene nell’essere assegnata alla mansione $\small j$-esima, per poi provare ogni combinazione fino ad ottenere quella col maggiore profitto possibile. Dovremo quindi confrontare $\small 70! \sim 10^{100}$.  

  Per renderci conto di quanto questo metodo sia inefficace poniamo il seguente quesito: avrebbe esplorato tutti gli assegnamenti possibili...  
  - un computer che esegue un milione di operazioni al secondo, in funzione dal Big Bang (15 miliardi di anni fa) fino ad oggi (1990)? **NO**.  
  - un computer che esegue un miliardo di operazioni ogni nano secondo, in funzione dal Big Bang fino ad oggi? **NO**.  
  - se ricoprissimo la Terra di questi computer che lavorano in parallelo? **NO**.  
  - se ricoprissimo $\small 10^{40}$ Terre di questi computer, in funzione dal Big Bang ad oggi, che lavorano in parallelo?  **FORSE SI**.  
  
  ---
  
  Di fronte all’impossibilità di enumerare tutti i casi possibili per determinare la soluzione migliore, negli anni Trenta, l’unica strada percorribile era quella di adoperare un approccio che Dantzig definì *"AD HOC" GROUND-RULE*: affidarsi al buon senso di persone, che guidate dall’esperienza e dal buon senso stabiliscono regole "ad hoc" da seguire per risolvere il problema.
  </div>
</details>
</div>

Ogni volta che dobbiamo prendere una decisione entrano in gioco i seguenti componenti:  

- **DATI**, che rappresentano tutti i valori noti a priori.  
- **VARIABILI**, che sono le entità controllate dal decisore; al variare di esse varia anche il valore del criterio e tra tutti i possibili valori che possono assumere si devono scegliere quelli che forniscono il miglior valore possibile del criterio.  
- **VINCOLI**, che limitano le possibili scelte del decisore (i possibili valori delle variabili).  
- **OBIETTIVO**, che coincide con il criterio fissato per confrontare le diverse possibili scelte del decisore.  

<details>  
<summary style="margin-bottom:0.5em;">Ad esempio:</summary>  
<div style="margin-bottom:0.5em; border: 1px solid #aaa; border-radius: 0 0 4px 4px; padding: 1em; margin-top: -1px;">  

Supponiamo di dover uscire di casa e poter prendere con voi uno solo dei seguenti tre oggetti: un libro che vale 10€, una macchina fotografica che vale 2000€ ed una borsa da 500€. Dovete decidere quale oggetto portare con voi, tenuto conto che vi interessa prendere un oggetto di valore massimo. L’esempio è molto banale e non c’è bisogno di scomodare la Ricerca Operativa per capire che occorre prendere la macchina fotografica. Tuttavia in esso sono già presenti tutte le componenti tipiche di una decisione:  
- **DATI**: i valori dei tre oggetti;  
- **VARIABILI**: per ogni oggetto il decisore (cioè voi) deve decidere se prenderlo oppure no;  
- **VINCOLI**: può essere preso un solo oggetto;  
- **OBIETTIVO**: prendere l’oggetto di valore massimo.  
</div></details>  

Un metodo per arrivare alla *miglior* soluzione *possibile* è l’<span style="font-weight:bold; background-color:#FDDC5C; color:black; padding:1px; border-radius: 4px;">APPROCCIO MODELLISTICO</span>, diviso in due parti:  

<div style="display:flex; align-items:flex-start;">  
<img src="./img/ro/modello-matematico.png" width="60%" height=auto title="Passaggi per la risoluzione di un problema attraverso l'APPROCCIO MODELLISTICO" style="margin-bottom:1rem;">  

- Rappresentazione del problema attraverso un **modello** matematico;  
- Sviluppo di un **metodo** matematico che permetta di determinare una soluzione ottima.  
</div>  

Un ruolo di fondamentale importanza lo avrà lo studio dei <span style="font-style:italic; font-weight:bold; background-color:#FDDC5C; color:black; padding:2px; border-radius: 4px;">problemi di Ottimizzazione</span>, nei quali si desidera minimizzare o massimizzare una funzione reale, le cui variabili sono vincolate ad appartenere ad una insieme prefissato che è descritto attraverso un numero finito di disuguaglianze o uguaglianze.  

$\small \text{problema di Ottimizzazione} = \begin{cases} \text{min/max} \ f(x) \\ x \in S \end{cases}$

L'approccio modellistico prevede **5 fasi**:  
1. ***ANALISI DELLA STRUTTURA DEL PROBLEMA***, per invididuarne i legami logico-funzionali e gli obiettivi;  
2. ***FORMULAZIONE DEL MODELLO***, in cui si descrivono in termini matematici le caratteristiche principali del problema: DATI, VARIABILI, VINCOLI e OBIETTIVO;  
3. ***ANALISI DEL MODELLO***, che prevede la deduzione, per via analitica, di alcune importanti proprietà:  
   - *esistenza* ed *unicità* della soluzione ottima;  
   - *condizioni di ottimalità*, cioè <abbr title="(necessarie, sufficienti, ecc.)">caratterizzazione</abbr> analitica della soluzione ottima;  
   - *stabilità* delle soluzioni al variare dei dati o di eventuali parametri presenti.  
4. ***SOLUZIONE NUMERICA***, mediante opportuni algoritmi di calcolo;  
5. ***VALIDAZIONE DEL MODELLO***: la soluzione, ammissibile per il modello, deve essere poi <abbr title="attraverso metodi di simulazione o verifica sperimentale">interpretata</abbr> dal punto di vista applicativo in modo da evitare che abbia scarso rilievo pratico.  

La definzione del modello si configura quindi come un processo di raffinamento iterativo, che può essere schematizzato come in Figura 1.4.1.

<img src="./img/ro/5-fasi.png" width="60%" height=auto title="1.4.1 - Fasi dell'approccio modellistico" style="margin-bottom:1rem; display:block; margin:auto;">

### MODELLI della Ricerca Operativa  

Con il termine *modello*, solitamente si fa riferimento a *modelli concreti*, come lo possono essere quelli di una nave, un palazzo o più in generale di una struttura appositamente costruita per mettere in evidenza caratteristiche principali di alcuni oggetti reali.  
Nella Ricerca Operativa, come in tante altre discipline, spesso trarremo invece ***modelli astratti*** (<abbr title="La nozione di modello matematico per rappresentare il mondo reale non è di certo di origine recente: già Pitagora nel IV secolo a.C. tentava di costruire un modello matematico dell'Universo, anche se sotto una luce più esoterica che scientifica." style="font-weight:bold; font-style:italic;">matematici</abbr>), i quali usano il simbolismo dell'algebra per mettere in evidenza un insieme di relazioni che descrivono in modo semplificato, ma sempre rigoroso, uno o più fenomeni del mondo reale.  
La <abbr title="(dagli ambiti più tradizionali a settori lontani come le scienze sociali e la psicologia)">notevole diffusione</abbr> della modellistica matematica è dovuta anche al fatto che essa può essere facilmente studiata grazie all'uso dei moderni calcolatori elettronici.  

I modelli matematici si suddividono poi in ***stocastici*** (considerano grandezze influenzate da fenomeni aleatori, casuali intrinsecamente, come il traffico) e ***deterministici*** (considerano grandezze esatte): inoltre, a seconda delle iterazioni tra grandezze che siano immediate o distribuite nel tempo, si parla di modelli ***statici*** e ***dinamici***.  

Nel seguito analizzeremo i modelli più comunemente usati: determinisici e statici; in particolare si farà riferimento ai *modelli di **programmazione matematica***. Si osservi infine che in questo contesto il termine "programmazione" è inteso nel senso di "pianificazione", non di programmi (codici) scritti in quale linguaggio di programmazione. Questi ultimi sono caratterizzati da tre elementi fondamentali:  
- **variabili** associate alle grandezze reali; sono "esogene" se incontrollabili (prendendo il nome di "parametri o "dati") o "endogene", se controllabili da parte del decisore (e prendono il nome di "variabili di decisione", o semplicemente variabili).  
- **vincoli** (relazioni matematiche) esistenti fra le variabili di decisione e le limitazioni derivanti da considerazioni di varia natura (fisica, economica, ecc.), come nel caso di un budget (che si traduce in "$\small \text{budget} \le 1000$").  
  Una soluzione che rispetti tutti i vincoli si dice *soluzione ammissibile* e l'insieme di queste ultime costituisce la *regione ammissibile* del modello.  
- **obiettivo** da minimizzare (es. costi) o massimizzare (es. profitto).  

<!-- 
Sono a pag. 12/26 della Dispensa della Sapienza `cap0-1-2`.
Sono a pag. 11/46 della slide `cap0`.
-->

<details>
<summary style="font-weight:bold; font-size:24;">TODO</summary>

### Programma

1. Formulazione di problemi decisionali in termini di programmazione matematica.
2. Classificazione dei problemi di programmazione matematica.
3. Teoria della programmazione lineare.
4. Il metodo del simplesso primale.
5. Il metodo delle variabili articificiali.
6. Teoria della dualità nella programmazione lineare.
7. Il metodo del simplesso duale.
8. Il metodo primale-duale.
9. Il linguaggio AMPL.
10. La libreria di algoritmi CPLEX.

Da uno studente viene il **metodo del simplesso**. Un prof un giorno aveva fatto un domanda assurda a degli studenti, ma uno di loro riuscì a rivolvere il problema attraverso un procedimento che il prof poi ha provato a rubargli l’idea ma lui riuscì ad evitarlo e ora questo metodo lo dobbiamo allo studente. Sposta il problema dal calcolo dell’area ad esempio al calcolo dei vertici.
    
Problema che nacque negli anni 70 è che il numero di vertici di quel poliedro poteva essere esponenziale, nel numero di variabili o nei vincoli del sistema.  
Qualche anno dopo, nel 78, sempre dalla scuola russa, un altro ricercatore (Kian Chan) propose un algoritmo che risolvere in tempo polinomiale ($\small n^2$) il numero di vertici del problemi (è esponenziale anche questo algoritmo, anche se di meno). **Metodo dell’Elissoide** (metodo esclusivamente matematica che noi non tratteremo).
  
---
  
L’obiettivo è quello di minimizzare l’$\small f(x)$, quindi devo trovare la q all’interno di quel fascio di rette quella **ammissibile** che avrà la q più piccola.

Devo trovare il modo di cambiare il punto di vista del mio problema per passare da un numero infinito di soluzioni valide, ad un numero finito.
  

---

La nostra esigenza è quella di capire…

Iniziamo col definire la **forma standard della programmazione lineare**. Lineare perché nel primo approccio al problema mi metto in un contesto lineare, assumendo che la mia funzione sia un polinomio di primo grado e tutte le altre funzioni siano problemi di primo grado.
Questa è una forma del problema con $\small A$ la matrice dei coefficienti che abbiamo, $\small x$ la … e $\small b$ il vettore, io li posso scrivere con l’operatore di uguaglianza, e le variabili devono essere tutte maggiori o uguali di 0:
$\small \text{forma standard della programmazion lineare} = \begin{cases} Ax = b \\ x  \ge 0 \end{cases}$.

Prendiamo il primo vincolo: $\small x_1 + x_2 \le 2$.
Se volessi trasformare il mio vincolo con il simbolo di uguaglianza, potremmo scrivere…

- $\small x_1 + x_2 \le (-\infty, 2)$. Soluzione "valida", ma a livello rappresentativo dovrei avere infiniti punti, e quindi la soluzione non è valida.
- $\small \begin{cases} x_1 + x_2 = 2 \\ x  \ge x_1-2x_2=1 \end{cases}$. Soluzione corretta, ma come ci arriviamo attraverso una serie di passaggi?
Quindi come se da un commerciante, andiamo a pagare un prodotto 1.5€, ma diamo 2€, ovviamente ci darà un resto perché il costo del prodotto è minore o uguale dei soldi che abbiamo forniti.
  
  $\small S$ è la variabile di Slack (mancanza), ovvero quello che manca.
  Se io dessi 1.5€, allora S = 0 e x sarebbe positivo.
  Se il costo fosse maggiore invece della mia disponibilità, non avrei più uno Slack, ma un surpluss, tipo 2.5€, costa più di quel che ho.
  

La **forma standard** sarebbe $\small \text{min } x_1 + x_2 = 2 \text{ è} \begin{cases} x_1 + x_2 = 2 \\ x_1-2x_2-S_2 \ge 0 \end{cases}$, con $\small x = [x_{12}, x_{24}, x_{45}, x_{13}, x_{34}]$ (in cui $\small x_{12} \in \{0, 1\}$.

Una soluzione scritta in forma standard è di base ammissibile se presenta le condizioni sotto riportate.

Definizione di **BASE AMMISSIBILE**: 

- di *base* vuol dire che io posso dividere le componenti del vettore in due sottoinsiemi di componenti.
  - Componenti in base, sono tutte formate da componenti positive e sono in numero pari alle righe di $\small A$.
  - Componenti non in base: sono tutte nulle, pari a 0.
  
  Viene specificata la parola "di base" nella soluzione per enfatizzare …
    
- *ammissibile* vuol dire

---

Bogdan consiglia di prepararsi cercando su YT video sul *metodo del simplesso*, il *simplesso a due fasi* e il *simplesso duale*. I termini noti gli metti in colonna sulla sinistra, la funzione obiettivo la metti come prima riga e tutti i vincoli li metti come altri righe.  
</details>

## Bibliografia  

- Caramia Massimiliano (<massimiliano.caramia@uniroma2.eu>), Tor Vergata;  
- [Roma Massimo](#https://youtube.com/playlist?list=PLAQopGWlIcyZankm1hHCSOdBilSGC3Svg&si=VRGG98n4gnqOsjrH), Sapienza;  
- [Alan Turista](#https://youtube.com/playlist?list=PL6ooPzL-5yGFQn6X6pGgxdg7TeIbPH7eA&si=hgFvfD5SpAPOIxpv).  