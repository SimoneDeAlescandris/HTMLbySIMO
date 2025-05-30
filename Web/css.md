<!-- 
COLORI:
- ROSSO: #DF5452;
- GRIGIO: #252525;
- BLU: #379AD3;
- VERDE: #529E72;
- GIALLO: #FDDC5C.
-->

<img src="../img/Web/3_CSS3.png" alt="Architettura dei Sistemi di Elaborazione" title="Architettura dei Sistemi di Elaborazione" width="24px" height=auto style="float:left; margin-right:12px;">  

# **CSS**

Il <abbr title="Cascading Style Sheets">CSS</abbr> è il linguaggio di styiling standard per modificare l'aspetto e la formattazione della pagina web.  

```css
p { /* Selettore di elemento */
    font-size: 16px;
}
.intro { /* Selettore di classe */
    font-weight: bold;
}
#header { /* Selettore di ID */
    background-color: #eee;
}
```

Le regole si applicano in modo generale alla pagina , la parte del codice nelle parentesi si chiama dichiarazione

selettori in css:
Possiamo selezionare tutti gli elementi presenti nella pagina html , semplicemente anteponendo il tag della parte a cui facciamo riferimento
ad esempio header , p , body e così via.

Il secondo selettore che ci interessa è la classe , che ci permette di prendere elementi specifici di un tag.
esempio: h1 class="center" , si può usare la stessa classe per più elementi.
Il nome della clas viene preceduto da un punto --> .class.
Le classi si possono concatenare con il selettore dell'elemento --> p.center

Selettore id , ci permette di identificare in modo univoco un elemento --> <p id="para1".
Il nome dell'id deve essere univoco!!!!
si può poi chiamare nel css con #para1 per attribuire uno stile specifico.

Questi elementi possono essere combinati tra di loro.

possiamo andare a selezionare più selettori , a cui applicare proprietà es:
--> h1 , h2 , header {
    stile
}

-selettori composti

se utilizzo lo spazio tra i selettori vado a selezionare i discendenti di un selettore:
--> ul li , scelgo i figli li di ul.

possiamo anche selezionare con p."classe2 , dove selezioniamo tutti i paragrafi che hanno una certa classe , o con qualsiasi altro tag


per child utilizzo il >
si può selezionare così un singolo elemento figlio --> div > p , tutti i paragrafi p contenuti in div (figli)

per il fratello successivo si usa il "+".

per tutti i fratelli successivi la tilde.

-Pseudo-classi:
Le pseudo-classi servono per selezionare elementi in uno stato particolare o con una caratteristica specifica che non puoi definire solo con classi o tag.
definire gruppi di elementi logici , con il ":".
es --> a:hover (pseudoclasse).
la pseudo classe viene chiamata con selettore:pseudo-classe.
Si scrivono con un solo : davanti e non creano un nuovo elemento, si applicano all'elemento selezionato.


-Pseudo-elementi:
Gli pseudo-elementi servono per creare e stilizzare una parte di un elemento o un elemento virtuale che non esiste nell’HTML.
elementi logici nella pagina --> selettore::pseudo-elemento.
Viene usato il simbolo "::".
gli pseudo-elementi trafromano il contenuto , aggiungendo elementi su cui apllicare regole.

-Selettori con attributi con il simbolo []
--> img[attributo].
si può scrivere anche il valore di un attributo --> [attributo = valore].

si può selezionare parte del valore , esempio fine , inizio classe ecc.

-Ereditarità
Alcune proprietà passano da un elemento ai suoi discendenti , mentre altre no.
Di solito quelle relative a colori e testo si.

-Conflitti
dichiarazioni che incidono sullo stesso elemento.
In generale la seconda dichiarazione sovrascrive la prima , ma non è sempre così.

-Conflitti tra proprietà con diversi selettori
In questo caso , più il selettore è specifico , più quel selettore tende ad essere dominante rispetto agli altri.
Possiamo quindi parlare di una sorta di gerarchia a piramide.

-!important
Permette di modificare l'importanza dei un selettore rispetto a tutti gli altri.

-cascade
Algortitmo che definisce come cambiare valori di proprietà provenienti da fonti diverse.

-Calcolo della specificità
Si calcola con 4 valori:

A: se il selettore è inline o no.
B: numero di selettori id nel nostro selettore.
C: numero di selettori di tipo classe , attributo , o pseudoclasse.
D: numero di selettori di tipo elemento o pseudo-elemento.

Lezione 20/03/2025

-Formattazione del testo:
Proprietà relative ai font:
i caratteri si dividono in famiglie , a seconda delle loro specifiche grafiche.
N.B. i caratteri dipendono anche dal S.O.!!

@font-face ci permette di importare tramite url diversi caratteri
Si può anche utilizzare un carattere che viene dai server di google --> google-fonts.
si possono importare tramite @import e url
per cambiare la grandezza del testo possiamo usare font-size e impostare i pixel o altrimenti tramite valore.
Si può usare il vw , per restringere la dimesione del font in base alla grandezza della pagina che viene poi visualizzata.
dove vw è la larghezza e vh è l'altezza.

-Font-size e line height:

altezza della riga combinata alla grandezza del font per favorire la leggibilità.
l'altezza della riga si può specificare in relazione alla grandezza del testo.

Esistono proprietà per specificare un insieme di altre proprietà
es --> font che ci permette di specificare un insieme di proprietà con una sola.

-Colore:
il colore può essere specificato in 4 modi:
-Stringa , nome del colore
-con il codice rgb --> #490926
-simile a quella sopra ma con tre numeri --> #467
-funzione rgb con tre parametri --> rgb(129 , 126 , 246)

si può anche usare una funzione particolare per aggiungere una colonna per l'opacità
--> es rgb(129 , 126 , 246 , .5)

-text decoration 
Serve per levare il sottolineato ai link o per aggiungere decorazioni di altri tipi al testo.

-Gestione del box
--> border: 0.5px solid violet;
controllare varie proprietà del rettangolo attorno agli elementi in una pagina.
Di questo rettangolo si possono controllare 4 aree , margine(esterno) , bordo , paddin area(interno) , contenuto.

-Posizionamento e Allineamento

-Allineamento con float
La proprietà float permette di far “galleggiare” un elemento (es. un'immagine) a destra o sinistra del contenuto, facendo sì che il testo gli scorra intorno.

Sintassi: float: left; oppure float: right;.

Nota: Quando si usa float, l’elemento viene tolto dal normale flusso del documento, quindi il contenuto successivo non lo riconosce come “ostacolo” a meno che non si usi clear: both; o si crei un clearfix.

-Posizionamento con position
La proprietà position serve per posizionare elementi in modo preciso nella pagina. Le sue varianti:

Tipo	Descrizione
static	    L'elemento segue il normale flusso del documento.
Relative  L’elemento viene posizionato relativamente alla sua posizione originale (quella che avrebbe con static).
Absolute  L’elemento viene rimosso dal flusso e posizionato rispetto al primo antenato con posizione diversa da static. Se non trova nessun antenato posizionato, si riferisce al <html>.
fixed	L’elemento è fissato rispetto al viewport, quindi resta sempre visibile anche durante lo scroll.
sticky (opzionale)	Combina relative e fixed: si comporta come relative, ma diventa fixed una volta superata una certa soglia di scroll. Utile per intestazioni fisse.

-Proprietà collegate:
top, right, bottom, left: servono a specificare la distanza dell’elemento dai lati del contenitore di riferimento.

Esempio:

.positioned {
  position: absolute;
  top: 20px;
  left: 30px;
}

-Visibilità con hover
Per far apparire un elemento al passaggio del mouse, si può usare il selettore :hover combinato con display.

Esempio:

```css
.hidden-box {
  display: none;
}

.container:hover .hidden-box {
  display: block;
}
```

-Flexbox (`display: flex`)
Flexbox è un potente sistema per creare layout monodimensionali (su riga oppure su colonna).

-Caratteristiche principali:
Si applica all’elemento contenitore (`display: flex`) e agisce sui suoi figli diretti.

Di default, gli elementi si dispongono in riga (`flex-direction: row`).

Per cambiare orientamento, si può usare:

`flex-direction: column; // disposizione verticale`

-Proprietà utili:
`flex-wrap: wrap;` → fa andare a capo gli elementi se non c’è spazio sufficiente.

`justify-content:` → allinea gli elementi lungo l’asse principale (es. da sinistra a destra).



Valori comuni:

`flex-start`, `flex-end`, `center`, `space-between`, `space-around`, `space-evenly`.

`align-items`: → allinea gli elementi lungo l’asse trasversale (perpendicolare rispetto a justify-content).
Valori: `stretch`, `center`, flex-start, flex-end, baseline.

align-content: → simile a align-items, ma agisce quando c’è wrapping, ovvero su più righe o colonne.

-Layout e Responsive Design in CSS

-Layout della Pagina
Il layout determina come i contenuti occupano lo spazio disponibile nel browser. Esistono due approcci principali:

1. Layout Fluido
I contenuti si adattano dinamicamente alla larghezza del browser.

Utilizza generalmente unità percentuali (%) per la larghezza degli elementi.

Spesso implementato con Flexbox o CSS Grid.

-Vantaggi:
Maggiore flessibilità su schermi di dimensioni diverse.

Buona base per la creazione di siti responsive.

-Svantaggi:
Può causare problemi di leggibilità o impaginazione su schermi molto piccoli.

-Esempio:
```css
.container {
  display: flex;
}

.box {
  width: 33.33%; /* 3 colonne = 100% */
}
```

2. Layout Fisso
I contenuti hanno una larghezza predefinita (in pixel) che non cambia al variare della finestra del browser.

-Vantaggi:
Più controllo sulla disposizione e dimensione degli elementi.

Layout più prevedibile.

-Svantaggi:
Non si adatta ai dispositivi mobili o agli schermi piccoli.

Può generare scroll orizzontali indesiderati.

-Esempio:
```css
.container {
  width: 960px;
  margin: 0 auto;
}
```
-Siti Responsive
Un sito è responsive quando si adatta a diverse dimensioni di schermo usando lo stesso HTML, ma CSS differenziato.

-Obiettivi:
Adattare l’interfaccia a diverse larghezze (mobile, tablet, desktop).

Fornire una buona esperienza utente indipendentemente dal dispositivo.

Usare tecniche che mantengano il layout leggibile e navigabile.

-Tecniche di base per il Responsive Design

1. Controllare il viewport
Inserire nel <head> del file HTML questo meta tag:

<meta name="viewport" content="width=device-width, initial-scale=1.0">
Serve per informare il browser che deve adattare la larghezza della pagina a quella del dispositivo.

-2. Usare le Media Query
Permettono di applicare regole CSS condizionali, in base alla dimensione o caratteristiche del dispositivo.

Sintassi:
```css
@media only screen and (max-width: 768px) {
  body {
    background-color: lightblue;
  }
}
```
Parti di una media query:
media type: ad esempio screen o print.

media feature: ad esempio max-width, min-width, orientation, ecc.

Esempio con il tag <link>:

<link rel="stylesheet" media="screen and (max-width: 768px)" href="mobile.css">

-Breakpoints
I breakpoint sono i punti in cui il layout deve cambiare per adattarsi al dispositivo.

-Tipici intervalli:
Mobile: < 600px

Tablet: 600px – 1024px

Desktop: > 1024px

-Strategie:
Mobile First: si scrivono le regole CSS per gli schermi piccoli, e si usano media query con min-width per adattare i layout a schermi più grandi.

Desktop First: si parte da layout grandi e si adatta con max-width a schermi più piccoli.

-Esempio Mobile First:
```css
.element {
  font-size: 14px;
}

@media (min-width: 768px) {
  .element {
    font-size: 18px;
  }
}
```
-CSS Variables (Variabili CSS)
Le variabili CSS permettono di riutilizzare valori (es. colori, dimensioni, font, ecc.) in più punti del foglio di stile, mantenendo il codice più ordinato, leggibile e facilmente modificabile.

-Sintassi base
```css
:root {
  --blue: #3498db; /* Definizione variabile globale */
}

body {
  background-color: var(--blue); /* Utilizzo della variabile */
}
```
-Note importanti:
Le variabili CSS iniziano sempre con – e vengono richiamate con var(--nome).

Il selettore :root è la radice dell’albero DOM, quindi le variabili dichiarate lì sono globali.

Possiamo anche definire variabili locali all’interno di un selettore:
```css
.box {
  --padding: 10px;
}
Tutti i discendenti di .box potranno usare var(--padding).
```
-Valori di fallback (default):
È possibile specificare un valore di default da usare se la variabile non è definita:

color: var(--main-color, black);

-Grid Layout e Bootstrap

Griglia (concetto generale)
Il layout a griglia è un pattern comune per organizzare contenuti in una pagina web, ispirato alla stampa editoriale.

Caratteristiche:
Composto da righe (rows) e colonne (columns).

Le colonne sono contenute in un container e separate da gutter (gli spazi vuoti).

Le griglie moderne sono responsive e usano percentuali anziché valori fissi in pixel.

-CSS Grid Layout (nativo)

Il CSS Grid è un sistema di layout bidimensionale che consente di controllare righe e colonne in modo preciso.

-Concetti chiave:
Basato su grid lines, linee numerate per riga e colonna.

Può essere usato per creare layout complessi, sia orizzontali che verticali.

-Proprietà utili:

display: grid;
grid-template-columns: repeat(4, 100px);
grid-template-rows: 1fr 2fr 1fr;
gap: 20px;

repeat(n, valore): crea ripetizioni regolari.

minmax(min, max): imposta un range flessibile.

fr (fraction unit): divide lo spazio in porzioni proporzionali.

-Esempio:

grid-template-columns: 1fr 2fr 1fr;
Qui si hanno tre colonne, dove quella centrale occupa il doppio dello spazio delle altre.

-Bootstrap Grid System

Bootstrap fornisce un sistema a griglia preimpostato basato su Flexbox, con regole e classi già pronte.

-Caratteristiche:
Layout diviso in 12 colonne.

Si usano classi come .container, .row, .col.

Le colonne possono avere dimensioni fisse o fluide (.col-6, .col-md-4, ecc.).

Include breakpoint per adattarsi a dispositivi differenti.


-Container in Bootstrap:
Fluidi per schermi piccoli (.container-fluid)

Fissi per schermi medi e grandi (.container)

-Conclusione:
CSS Grid è ottimo quando vuoi controllo totale e layout complessi.

Bootstrap è perfetto se vuoi andare veloce, seguire uno standard già pronto, e non hai bisogno di layout troppo articolati.

---
---
---

## Appunti delle lezioni

Dopo aver visto i tipi di stili ciò che a noi interessa sono i selettori
3 tipologie di selettori

-selettore di tag, che lavoro sul tag specificato, quindi ogni tag di quel tipo prende quelle proprietà
-selettore di classe che identifica una classe di elementi, ciò ci consente di lavorare su più tag che appartengono a tale class
due modalità di definizione .class oppure tag.class

nel file .css
.class{
    proprietà1:valore1;
    proprietà2:valore2;
    -------------------
}

-selettore id=attributo univoco per quel elemento seleziona l'elemento con quel id, possiamo dare una qualsiasi stringa come id
come sintassi nel css bisogna usare #id
esempio 
<p id="ciao">Questo paragrafo</p>

nel css
#ciao{  proprietà1:valore1;
        proprietà2:valore2;
        -------------------
}

L'id si usa nei casi strettamente necessari, all'esame "fate come vi pare" cit Loreti.


Raggruppamento selettore

Spesso possiamo Raggruppare gli selettori con le stesse proprietà
usando la virgola 
esempio 
h1{
  color:black;    
}

p{
    color: black;
}

possiamo fare direttamente, (scrivendo meno)

h1, p{
    color:black;
}


Relazione DOM (Document Object Model)

Bisogna iniziare ad avere in testa il fatto che i tag sono rappresentati come un albero radicato
con <html> come root e figli <head> <body>
a loro volta head e body hanno dei figli
Valgono proprietà degli alberi come figli, fratelli, un padre etc...

A cosa serve?
In css per ereditare oppure assegnare specifiche proprietà a paricolari nodi figli o fratelli 
Servirà anche in JavaScript....

Come creare selettori che lavorano sul DOM????

1 selettori per discendenti (lo spazio)

    header p{
        proprietà:valori;
        ----------------
    }
dice tutti i discendenti del header che hanno il tag p (ricevono quelle proprietà)
Conviene leggere da destra verso sinistra
tutti i paragrafi discendenti dal header ricevono quelle proprietà.


2 Selettore per figlio (>)

div >p {
    proprietà:valore;
}
Dice tutti i p figli (child) del tag div...
Spesso si usa nelle tabelle


----- i ultimi due successivi vederli da soli, il prof non li ha fatto 
3 Selettore per frattelli successivi (+)

4 Selettore per fratelli generici



Le pseudo classi, vengono utilizzate per definire uno stato speciale di un elemento 
spesso si usano nei tag a oppure img 

sintassi

selettore:pseudo-classe{ 
    proprietà: valori;
}

esistono pseudo-classi già definite 

:root:only-child
:visited
:hover:
:focus
:nth-child()  // questa prende un parametro
:nth-last-child() // questa prende un parametro
-------

Vedere elenco delle pseudo-classi, non le faremo tutte.


I pseudo-elementi vengono utilizzati per dare uno stile alle parti specifiche di un elemento
sintassi
selettore::pseudo-elemento{
    proprietà: valori;

}

utili perchè altrimenti dovrei usare tag annidati

trasformazione contenuti degli elementi, 

::after
::before 
::first-letter // proprietà sulla prima lettera del selettore
::first-line


--Selettore per attributi 

sintassi

[attributo ] {
    proprietà:valori;
}


posso speficifare il valore/i che voglio modificare

[attributo=valore]{
    proprietà:valori;
}

due sintassi o  come sopra oppure aggiunendo il selettore prima dell'attributo

esempio

img[alt]{
    background-color: black;
}

oppure

[alt]{
    background-color: black;
}

Qualche volta si usa dipende dalle nostre necessità.


------------
Ereditarietà

Alcune proprietà sono ereditate dai discendenti !!!!!!!!!

Spesso si hanno dentro i tag annidati, specialmente se i tag esterni hanno delle proprietà.

I tag spaziatura non ereditano 

Vedere lista di proprietà erediate, a noi interssa quelle proprietà in rosso che useremo


conflitti nella dichiarazione.

ad esempio due dichiarazioni di un tag, nella stessa pagina,  chi vince??

p{
    color: black;
    background-color:yellow;
}

--
p{
    color:red;
}


In maggior parte dei casi vince la seconda
attenzione solo le proprietà sovrascritte vincono
il background color rimane...

tale situazione meglio evitare, perchè il browser distribuisce su più file i stili
vedere nella parte style sul browser. 

comunque non si usa.


Ma tra un id, una classe e un selettore chi vince ??

p{
    proprietà:valore;
}

#param{
    proprietà:valore;
}
.red{
    proprietà:valore;
}


<p class="red">testo paragrafo</p>

<p id="par3">testo paragrafo2</p>


Il selettore elemento è meno speficico
Il selettore di classe è più specifico del selettore elemento 
Il selettore di tipo id è il più forte del selettore di classe

Quindi dove c'è collisione tra id, class e elemento ora sappiamo chi vince.



parola chiave !important
se dichiaro una proprietà come !important allora essa diventa la più importante di tutti
i selettori id, classe, elemento 


p{
    color:yellow !important;
}

#param{
    color:green;
}
.red{
    color:red;
}

In questo caso anche se il selettore di elemento è meno importante, la
proprietà del selettore p diventa la più importante. 


Il cascade è un algoritmo che definisce come combinare valori di proprietà provenienti da fonti esterne
i stili sono 

-browser  user-agent stylesheets
-author  quello che scriviamo noi
-reader  utenti del browser, aggiungere estensioni 

Per ogni sito abbiamo sempre due stili browser e author

Le regole che vincono sono le nostre (author)


Caclolo delle specificità (può chiedere all'esame)

Per ogni selettore ci sono 4 numeri [a,b,c,d]

calcolo valori

a--- selettore in line 1 oppure no 0
b--- Numero selettori id
c--- Numero di selettori di classe, attributo o pseudo-classi
d--- Numero di selettori elemento o psudo-elementi 


esempi

*{}   ---> specificità = [0,0,0,0]
ul li{}  -----> specificità = [0,0,0,2]

li.red.level{} (definito come una classe dentro l'altra)--->  specificità= [0,0,2,1].


idea partire sempre dal conteggio elementi (d)
poi calcolare numero elementi classe, attributo o pseudo-classi (c)

poi numero selettore id (b)
infine a.

---
---
---

[Proprietà CSS del div](https://www.w3schools.com/html/html_div.asp)

---
---
---

- [Custom Cursor CSS](https://www.instagram.com/reel/C-aMii8NGga/?igsh=MTJrNGlsb3J2YzM1dw==).
## Bibliografia:  

- [W3CSchools CSS](#https://www.w3schools.com/css/default.asp);  
- [Mozilla Web Docs](#https://developer.mozilla.org/en-US/docs/Learn/HTML);  
- Programmazione Web, Pierpaolo **Loreti**, 2024-2025.  
  <details style="background-color: #252525; color:white; border-radius: 10px; padding: 15px; box-shadow: 0.5px 0.5px 2px black; margin-bottom: 1em;">
    <summary style="cursor:pointer; font-weight:bold;">Testi e siti di riferimento</summary>

    <div style="display:flex; align-items:flex-start; gap:20px;">
      <img src="https://m.media-amazon.com/images/I/61HorcFwL5L.jpg" alt="copertina libro HTML5" width="40px" height="auto">
      <p style="font-size: 0.75rem;"><a href="https://amzn.eu/d/7e6HZ2H"><i>The Definitive Guide to HTML5</i></a> - Adam Freeman</p>
    </div>
    <div style="display:flex; align-items:flex-start; gap:20px;">
      <img src="https://m.media-amazon.com/images/I/91xorHXzWbL._SL1500_.jpg" alt="copertina libro Javascript" width="40px" height="auto">
      <p style="font-size: 0.75rem;"><a href="https://amzn.eu/d/cbg9eA1"><i>Javascript - The Definitive Guide 6th Edition</a></i> - David Flanagan</p>
    </div>
    <div style="display:flex; align-items:flex-start; gap:20px;">
        <img src="https://learningwebdesign.com/images/lwd5_cover.png" alt="copertina libro Learning Web Design" width="40px" height="auto">
        <p style="font-size: 0.75rem;"><a href="https://learningwebdesign.com/"><i>Learning Web Design - A Beginner's Guide to HTML, CSS, JavaScript, and Web Graphics</i></a></p>
    </div>
    <div style="display:flex; align-items:flex-start; gap:20px;">
      <img src="https://m.media-amazon.com/images/I/91oLbKMEadL._SL1500_.jpg" alt="copertina libro quattro (quello gratis)" width="40px" height="auto">
      <p style="font-size: 0.75rem;"><a href="https://womengovtcollegevisakha.ac.in/departments/Learning%20PHP,%20MySQL,%20JavaScript,%20CSS%20&%20HTML5_%20A%20Step-by-Step%20Guide%20to%20Creating%20Dynamic%20Websites%20(%20PDFDrive%20).pdf"><i>Learning PHP, MySQL, JavaScript, CSS & HTML5</i></a> - Robin Nixon</p>
    </div>
    <div style="display:flex; align-items:flex-start; gap:20px;">
      <img src="https://m.media-amazon.com/images/I/81FkghfrfXL._SL1500_.jpg" alt="copertina libro cinque" width="40px" height="auto">
      <p style="font-size: 0.75rem;"><a href="https://amzn.eu/d/adcmSWw"><i>Full-Stack Web Development with Vue.js and Node</i></a> - Aneeta Sharma</p>
    </div>
  </details>