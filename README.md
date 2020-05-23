# Pubblicazione di un sito web

## Indice dei passaggi

- [Avere il sito da pubblicare](#Avere-il-sito-da-pubblicare)
- [Comprare un server](#Comprare-un-server)
- [Comprare un dominio](#link-alla-sezione)
- [Configurazione](#link-alla-sezione)
  - [Dominio](#link-alla-sezione)
    - [Cloudfare (spigazione e account)](#link-alla-sezione)
    - [Puntare a cloudfare](#link-alla-sezione)
    - [Configurazione DNS su cloudfare (punta al server)](#link-alla-sezione)
  - [Server](#link-alla-sezione)
    - [Installazione del web server (spiegazione)](#-link-alla-sezione)
    - [Configurazione del web server](#-link-alla-sezione)
    - [Caricamento del sito](#link-alla-sezione)
- [Crash test](#link-alla-sezione)


## Avere il sito da pubblicare

La prima cosa da fare prima di pubblicare il nostro sito è scriverlo, sappiamo tutti come si fa. Attraverso i linguaggi che abbiamo studiato, [HTML](https://en.wikipedia.org/wiki/HTML) & [CSS](https://en.wikipedia.org/wiki/Cascading_Style_Sheets) per la parte visiva e strutturale, [Javascript](https://en.wikipedia.org/wiki/JavaScript) e [PHP](https://en.wikipedia.org/wiki/PHP) per le funzioni logiche e di backend e, ultimo ma non per importanza il [MySQLi](https://en.wikipedia.org/wiki/MySQLi) che ci permette di sviluppare e manipolare il nostro Database.


## Comprare un server

Dopo aver scritto il codice, che costituisce la nostra pagina, possiamo iniziare a capire come pubblicarlo. La prima cosa da fare è acquistare una macchina server. Capiamo però cosa è e cosa fa questa [macchina](https://it.wikipedia.org/wiki/Server).  

## Cosa è un dominio e dove si compra

Ok, adesso che ci siamo procurati un server è il momento di trovare un dominio. Ma prima partiamo spiegando cosa è un dominio.<br>
Un dominio è indirizzo univoco attraverso il quale si richiama un sito internet sulla rete.<br>
Volendo fare un paragone alla vita di tutti i giorni, un dominio è come una via e un numero civico, un modo semplice e facile da ricordare per trovare un determinato posto.<br>
Un dominio è costituito da una serie di stringhe separate da punti. <br><br>
Nei domini è presente una gerarchia molto stringente, prendiamo, per esempio lettly.github.io e analizziamolo da destra verso sinistra.<br>
Il dominio radice è .io detto anche il dominio di primo livello: top-level domain (TLD). I domini di primo livello si distinguono in domini di primo livello nazionali come .it (italia) .fr (francia) .io che indica il Territorio britannico dell'Oceano Indiano o quelli generici come .net (dedicato ai network) .org (dedicato alle organizzazioni) .com (dedicato alle organizzazioni commerciali) e molti altri.<br>
Continuando a muoverci verso sinistra troviamo: github questo è il dominio di secondo livello, questa parte può essere liberamente scelta dall’utente. Se sono presenti altri sottodomini, come in questo caso, il dominio prende il nome di dominio intermedio.<br>
All’estrema sinistra possiamo trovare lettly, questo è un dominio di terzo livello. In questo caso specifico non ci sono altri sottodomini perciò questo dominio viene chiamato dominio radice.<br><br>
I nomi di dominio sono formati dalle regole e dalle procedure del Domain Name System (DNS). <br>
In generale, un nome di dominio rappresenta una risorsa IP, ad esempio un server che ospita un sito web o il sito web stesso.<br><br>
Ma come mi posso procurare un dominio?<br>
Per ottenere un domino bisogna rivolgersi a un domain reseller, questa società, dietro un compenso, si occuperà della registrazione del dominio e fornirà l’infrastruttura necessaria a farlo funzionare. Esistono molte aziende che fanno ciò tra le più famose possiamo menzionare GoDaddy, OVH, NameCheap, e molti altri. Di solito la registrazione di un dominio è annua e univoca, di conseguenza se il dominio google.com è già occupato noi non potremmo compralo.
