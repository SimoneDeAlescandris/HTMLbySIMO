<style>
        body {
            font-family: default;
            /* text-align: justify; */
            margin-top: 2%;
            margin-left: 2%;
            margin-right: 2%;
            margin-bottom: 2%;
        }
        .callout {
          background-color: #252525; 
          border-radius: 10px; 
          padding: 15px; 
          color: #f0f0f0; 
          font-size: 16px;
        }
        details {
            padding: 0.5em 0.5em 0;
            border: 1px solid #aaa;
            border-radius: 4px;
            margin-bottom: 1em;
        }
        summary {
            margin: -0.5em -0.5em 0;
            padding: 0.5em;
        }
        details[open] {
            padding: 0.5em;
            border-bottom: 1px solid #aaa;
        }
        details[open] summary {
            border-bottom: 1px solid #aaa;
            margin-bottom: 0.5em;
        }
        /*.ombra {
            box-shadow: 0.5px 0.5px 2px black;
        }*/
    </style>

<img src="./img/Architettura/001-Architettura.jpg" alt="Architettura dei Sistemi di Elaborazione" title="Architettura dei Sistemi di Elaborazione" width="34px" style="float:left; margin-right:12px;">

# Cap. 1  

## Cap. **<span style="color:#529E72;">1.1</span>** - Cos’è un Sistema Operativo?  

<div class="callout">

**<span style="color:#DF5452;">Riassumendo</span>**, *i computer sono progettati come una serie di livelli, ciascuno costruito su quelli che lo precedono*.  

Ogni livello rappresenta un'**astrazione** diversa, con oggetti e operazioni proprie, consentendo di semplificare la complessità dell'intero sistema.  

L’insieme dei tipi di dati, delle operazioni e delle funzionalità di ciascun livello è chiamato **architettura**. Essa riguarda gli aspetti visibili agli utenti (come la quantità di memoria RAM disponibile per eseguire un determinato programma), ma non gli aspetti tecnici di implementazione (come la tecnologia con cui è realizzata la memoria RAM).  

L'**architettura degli elaboratori** (o calcolatori) è lo studio dell'organizzazione e del funzionamento dei componenti hardware di un computer.  

</div><br>

Serve un intermediario tra l'utente e l'hardware: il **Sistema Operativo**.  

<details>
<summary>🖥️ Un moderno calcolatore e tipicamente formato da:</summary>
<div style="display: flex; justify-content: center; width: 100%;">
  <img src="./img/Architettura/002-Componenti.png" alt="Componenti di un computer moderno (1)" title="Componenti di un computer moderno (1)" style="width: 48%; height: auto; padding: 1%">
  <img src="./img/Architettura/003-ComputerModerno.png" alt="Componenti di un computer moderno (2)" title="Componenti di un computer moderno (2)" style="width: 48%; height: auto; padding: 1%">
</div>

<!-- QUI VOGLIO METTERCI QUELLA PARTE PER ABBREVIARE. -->

</details>

Dalla loro nascita ad oggi i calcolatori si sono complicati esponenzialmente, incrementando, fortunatamente, anche la loro potenza: basti pensare che c’era più potenza di calcolo nel [COMODOR-64](https://it.wikipedia.org/wiki/Commodore_64) (1982) che per i PC usati dalla NASA per mandare l’uomo sulla Luna (1969).  

Data la crescente complessità costruttiva della macchina, se tutti i programmatori di applicazioni dovessero essere in grado di comprendere nel dettaglio il funzionamento di tutti questi componenti, nessuno avrebbe il tempo di scrivere codice. A questo scopo, è nato il **Sistema Operativo**, uno strato di software il cui compito è di fornire ai programmi utente un modello del computer migliore, più semplice e più chiaro e di gestire tutte le risorse appena citate.  

Il SO ci mette a disposizione delle librerie che ci permettono di interagire con la macchina, attraverso le **System Call**. Quindi se dall’alto noi eseguiamo un programma, sotto c’è l’hardware, ma nel mezzo abbiamo il nostro SO, colui che si occupa di gestire le risorse e ci permette di **astrarre** dall’hardware (suo obiettivo principale).  

> ***Obiettivo di un sistema operativo***: astrarre il pezzo di ferro che sta sotto, mentre il SO si occupa della gestione di risorse e dei permessi in maniera controllata.  

- *I sistemi operativi trasformano gli orrori dell’hardware in eleganti astrazioni*.
    
<img src="./img/Architettura/004-SOvsHardware.png" alt="Componenti di un computer moderno (2)" title="Componenti di un computer moderno (2)" style="width: 48%; height: auto; padding: 1%">