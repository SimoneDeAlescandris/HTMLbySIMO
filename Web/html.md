<!-- 
COLORI:
- ROSSO: #DF5452;
- GRIGIO: #252525;
- BLU: #379AD3;
- VERDE: #529E72;
- GIALLO: #FDDC5C.
-->

<img src="../img/Web/1_HTML5.png" alt="Architettura dei Sistemi di Elaborazione" title="Architettura dei Sistemi di Elaborazione" width="34px" style="float:left; margin-right:12px;">  

# HTML  

## Indice  

- [Introduzione](#introduzione)  
- [Struttura di documenti HTML](#struttura-di-documenti-html)
- [Bibliografia](#bibliografia)  
<br>

## Introduzione  

Un file **HTML** utilizza dei **tag** (marcatori) per dire al browser come è strutturato; al loro interno vi sono gli **elementi** da mostrare, che possono anche essere ulteriori tag annidati. Il codice HTML viene quindi interpretato per generare la pagina visualizzabile dall'utente.  

<details>  
<summary style="margin-bottom:0.5em;">Internet e HTML</summary>  
<div style="border: 1px solid #aaa; border-radius: 0 0 4px 4px; padding: 1em; margin-top: -1px; margin-bottom:0.5em;">  

L'<abbr title="HyperText Markup Language">HTML</abbr> fu sviluppato nel 1991 da Tim Berners-Lee e la sua sintassi è stabilita dal World Wide Web Consortium (W3C). È il linguaggio di markup più usato per la realizzazione di pagine web (documenti digitali identificati da un <abbr title ="Uniform Resource Locator">URL</abbr>).  

L'Internet è una serie di dispositivi elettronici interconnessi attraverso un indirizzo <abbr title="Internet Protocol">IP</abbr> univoco per ogni dispositivo connesso alla rete (scopri il tuo su [WhatsMyIP.org](https://www.whatsmyip.org/)). Solo chi è connesso è in grado di condividere informazioni e uno dei modi in cui è possibile farlo è attraverso il <abbr title="World Wide Web">WWW</abbr>, un insieme di pagine web e documenti collegati fra loro attraverso collegamenti ipertestuali (link).  

<img src="../img/Web/2_URL.png" title="Struttura di un URL" alt="URL" width="75%" height=auto style="padding:0.5rem; display:block; margin:auto;">

Il **web** è uno dei servizi che utilizzano che utilizzano l'infrastruttura internet, altri sono email e messaggistica istantanea.  

Per navigare nel WWW, gli utenti utilizzano un **browser** web (come Chrome, Firefox, Safari), che agisce da **client** web, ovvero un software che invia richieste ai **server web** (come Apache o nginx) e interpreta i linguaggi web, visualizzando le pagine ricevute.  

I protocolli di comunicazione principali per scambiare documenti sono <abbr title="HyperText Transfer Protocol">HTTP</abbr> e <abbr title="versione sicura di HTTP con crittografia SSL/TLS">HTTPS</abbr>: definiscono come devono essere formattati e trasmessi i messaggi.  

Il <abb title="Domain Name System">DNS</abbr> traduce i nomi di dominio (es. `www.google.com`) in indirizzi IP numerici, necessari per identificare univocamente i server su Internet (possiamo considerla come una rubrica). <u>Quando un utente inserisce un URL nel browser</u>, il browser contatta un server DNS per ottenere l'indirizzo IP corrispondente. Se l'indirizzo IP è già stato memorizzato nella cache locale, il browser lo utilizza direttamente, accelerando il caricamento della pagina.  

Nel concentro un Browser:  
1. Scopre dove si trova la pagina web, utilizzando il DNS per tradurre URL in indirizzo IP numerico;  
2. Richiede che la pagina venga inviata (GET verso il server);  
3. Controlla e verifica ciò che riceve;  
4. Mostra la pagina all'utente.  
</div></details>

<details>  
<summary style="margin-bottom:0.5em;">Origini di Internet</summary>  
<div style="border: 1px solid #aaa; border-radius: 0 0 4px 4px; padding: 1em; margin-top: -1px; margin-bottom:0.5em;">  

Ripercorrendo brevemente la storia di Internet, l'idea nacque negli Stati Uniti, anni Cinquata, durante la Guerra Fredda, quando si resero conto che sarebbe stato comodo avere un sistema di comunicazione che non potesse essere colpito da un attacco nucleare sovietico.  
Nel 1958, il presidente Eisenhower istituì la <abbr title="Defense Advanced Research Projects Agency">DARPA</abbr>, con l'obiettivo di sviluppare una rete di computer decentralizzata chiamata **ARPANET**. Nel 1969, Leonard Kleinrock riuscì a inviare il primo messaggio tra due computer situati presso l'Università della California e l'Università di Stanford, segnando l'inizio della comunicazione tra computer distanti.  

- **Sviluppo dei protocolli**:  
  Nel 1974, gli informatici Bob Kahn e Vint Cerf introdussero il **protocollo TCP/IP**, che suddivide i dati in pacchetti per una trasmissione efficiente e sicura, diventando la base della comunicazione su Internet.  
- **Nascita del World Wide Web**:  
  Il 6 agosto 1991, al CERN di Ginevra, Tim Berners-Lee sviluppò il primo sito web della storia: il [**World Wide Web**](https://info.cern.ch/hypertext/WWW/TheProject.html), introducendo strumenti fondamentali come **HTML**, **HTTP** e gli **URL** e rendendo accessibili informazioni a livello globale.  
  Nel 1992 poi i server web divennero 50 e con la nascita di NCSA Mosaic, il primo Browser grafico, il Web iniziò ad essere "di massa".  
  Approfondimenti su [W3C's History Archives](https://www.w3.org/History/).  
- **Diffusione in Italia**:  
  Il 30 aprile 1986, l'Italia si collegò per la prima volta ad ARPANET, segnando l'inizio dell'era di Internet nel paese.  
</div></details>  

## Struttura di documenti HTML

Come standard, si nomina `index.html` la pagina principale di ogni sito perché i server web lo cercano automaticamente nella cartella principale, quindi questo permetterebbe di accedere al sito senza dover digitare il <abbr title='Digiterebbero "https://www.miosito.com/" invece di "https://www.miosito.com/index.html".'>nome del file</abbr>, rendendo gli URL più puliti e migliorando l'esperienza utente.  

- `<!DOCTYPE> html`: ogni file HTML inizia con questa dichiarazione (NON è un tag e NON è <abbr title="L'unica versione corretta è `<!DOCTYPE> html`, tutte le altre non vanno bene (ad esempio: `<!DOCTYPE> HTML`, `<!doctype> html` e così via...).">case sensitive</abbr>), fondamentale per indicare al browser la versione dell'HTML da utilizzare.  

Gli elementi all'interno di un documento HTML vanno a formare un albero, la cui radice (che contiene tutti gli altri elementi) è `<html lang="it">`: tag che rappresenterà la radice della nostra pagina. L'attributo `lang` specifica la lingua del documento, per migliorare l'accessibilità.  

- `<head>`: contiene i metadati (dati sui dati). Tipicamente definisce:  
  - `<title>` (necessario e univoco): specifica il titolo della pagina HTML (visualizzato nella toolbar del browser, usato dai motori di ricerca e quando si memorizza nei preferiti una pagina).  
  - `<meta>` in genere specifica il set di caratteri, la descrizione della pagina, le parole chiavi, l'autore del documento e le impostazioni della finestra di visualizzazione.  
  - `<link>` collega la pagina HTML ad altri documenti o risorse esterno. In genere lo si usa per lo "style sheets" esterno o per aggiungere la **favicon** al sito web (una piccola immagine mostrata vicino al titolo nella toolbar del browser)
  - [`<base>`](https://www.w3schools.com/tags/tag_base.asp) specifica un URL di default e un target per ogni link nella pagina.  
  - `<style>`, definisce informazioni sulle stile (CSS) senza dover ricorrere ad un file esterno.  
  - `<script>` incorpora un client-side script (JavaScript).  
  - `<noscript>` mostra un messaggio all'utente se il suo browser non supporta script JavaScript.  

HTML5 introduce il concetto di **markup semantico**, che consiste nel scegliere l'elemento HTML che meglio descrive il contenuto. Questa distinzione è nata perché Google così possa indicizzare al meglio il nostro sito.  

<img src="../img/Web/standard.png" title="Standard per HTML5 da Google" alt="Standard per HTML5 da Google" width="60%" height=auto style="padding:0.5rem; display:block; margin:auto;">

Il `<body>` contiene la parte visibile della pagina ed è diviso nelle sezioni:  
- `<header>`: elementi introduttivi come il logo e il menu di navigazione.  
  - `<nav>`: insieme di collegamenti per la navigazione del sito. Tipicamente vi si mettono delle liste, ma non è detto che tutte le liste debbano andare qui. Nei siti responsivi spesso viene compressa per i dispositivi mobile.  
- `<main>`: Contenuto principale della pagina.  
  - `<section>`: raggruppa contenuti correlati all'interno della pagina, come argomenti diversi all'interno di un articolo.  
  - `<article>`: contenuto indipendente, come un post di blog o un articolo di giornale.  
  - `<figure>`: raggruppa immagine (`<img>`) e didascalia (`<figcaption>`). Esempio [qui](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_figcaption).  
- `<aside>` (sidebar): elementi correlati ma "marginale" rispetto al contenuto, quindi senza necessità che vengano indicizzati da Google. Tipicamente usato per sondaggi, citazioni, informazioni aggiuntive, annunci, donazioni o link. Non ha un aspetto di default.  
- `<footer>`: Include informazioni di chiusura, come copyright o link ai social.  

<details>
<summary style="font-weight:bold;">Esempio di una pagina conforme agli standard:</summary>

```html  
<!DOCTYPE html>
<html lang="it">
<head>
  <title>Titolo della pagina</title>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Free Web tutorials">
  <meta name="keywords" content="HTML, CSS, JavaScript">
  <meta name="author" content="Simone">
  <link rel="icon" type="image/gif" href="../img/Web/favicon.gif">
  <link rel="stylesheet" href="styles.css">
  <script defer src="script.js"></script>
  <noscript>Your browser does not support JavaScript!</noscript>
</head>
<body>
  <header>
    <img src="/images/logo.png">
    <h1>Intestazione principale</h1>
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Chi siamo</a></li>
        <li><a href="#">Contatti</a></li>
      </ul>
    </nav>
  </header>
  <main>
    <section>
      <h2>Sottotitolo</h2>
      <p>Testo del contenuto.</p>
    </section>
    <article>
      <h2>Articolo</h2>
      <p>Testo dell’articolo.</p>
    </article>
  </main>
  <footer>
    <p><small>Copyright &copy;2025 Nome Sito/Nome autore</small></p>
    <nav>
      <ul>
        <li><a href="">Previous</a></li>
        <li><a href="">Next</a></li>
      </ul>
    </nav>
  </footer>
</body>
</html>
```  
</details>

-html heading , sono le intestazioni per fare i titoli , dove da 1 , 2 , ...6 va a diminuire la dimensione del titolo.
la maggior parte dell'indicizzazione della pagine viene fatta sui tioli.

-tag per raggruppare il contenuto (altri tag) , per dare senso ad un insieme di altri elementi 

alcuni esempi:

<p></p> , per i paragrafi , può contenere testo e immagini , meglio evitare di inserirvi altri paragrafi . head e main.

elemento <pre> , per il testo con gli spazi.

elemento <blockquote> , serve per dire da dove è stata presa una sezione , come un articolo , mettendo il sito da dove proviene.

-Liste:
abbiamo liste ordinate non e descrittive. si ottengono con una combiinazione di tag.
una lista può contenere altre liste (liste annidate)

Liste descrittive , composte da descrizione e valore.

text-level semantic elements:

gli spazi e gli "a capo" devono essere segnalati da specifici tag , altrimenti non vengono visualizzati

---

I tag importanti sono:

- HEADING (`<H1>` to `<H6>`).  
- LINE BREAK (`<br>`): aggiunge una linea di spazio fra un paragrafo e l'altro.  
- (`<center>`).  
- The `<h1>` element defines a large heading
- `<p>` element defines a paragraph
- `<hgroup>` indica che il titolo e il paragrafo che segue sono correlati:  
  ```html
  <hgroup>
    <h2>Norway</h2>
    <p>The land with the midnight sun.</p>
  </hgroup>
  ```

&lt;&gt;    

## HTML Attributes

Ogni tag può avere <b>attributi</b>, che forniscono informazioni aggiuntive sugli elementi. Gli attributi sono definiti nei tag di apertura e seguono la sintassi <code>chiave="valore"</code>. Se il valore contiene gli apici doppi si usano i singoli, e viceversa.  

- `class`: ...  
- `id`: ...  
- `title`: specifica informazioni extra sull'argomento.  
  <pre><code>&lt;abbr title="HyperText Markup Language"&gt;HTML&lt;/abbr&gt;</code></pre>  
lang

<!-- 
Parlare di
<dt>Esempio</dt>
<dd>Commento</dd>
-->

<!-- Questo è un commento in HTML. Toglierlo e parlarne mettendo un qualsiasi codice e scriverci vicino: -->
<!-- Commento -->

## Bibliografia  

- [W3CSchools HTML](#https://www.w3schools.com/html/default.asp);  
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

Javascript:  
- [W3CSchools JavaScript](https://www.w3schools.com/js/default.asp);  
- [javascript.info](https://javascript.info/).  

MongoDB:  
- <https://www.javatpoint.com/mongodb-tutorial>.  

Node JS:  
- <https://nodejs.org/en/docs/guides/>.  

---
---
---
---
---

Per lavorare come Web Developer consigliano di imparare:
- HTML
- CSS
- JavaScript
Framework:
- Bootstrap
- React js
- Tailwind css
Design:
- Figma
- Adobe XD
- Photoshop
Backend:
- Node js
- MangoDB
- Express js
Extra:
- Git
- Github
- Gsap js

## Esami

25/06  
18/07  

## TODO

Converrebbe in futuro realizzare il mio sito web in modo da renderlo più inclusivo e accessibile, rispettando quindi l’AGID e dando la possibilità di far scegliere all’utente le dimensioni degli elementi a schermo (come il testo), il contrasto e i colori a schermo (per le persone con un handicap visivo), la possibilità di scegliere se avere uno schermo bianco o nero, rendere evidenti i link (magari sottolineandoli) e poi la possibilità di caratteri ata-leggibili.

> Chiedere a ChatGPT come migliorerebbe questa pagina e perché farebbe queste modifiche seguendo lo standard dettato da Google  
> Ricontrollare le estensioni di vscode e riscriverle su Notion.  
> Su ChatGPT ho esplorato come mettere la modalità notte e impedire la copia-screen del testo sulla mia pagina. Dovrò esplorare meglio l'argomento.  
> Capire come funzione sto sito: https://www.codegrind.it/documentazione.  
> La linea orizzonale in HTMl si fa con il tag "`<hr>`".  