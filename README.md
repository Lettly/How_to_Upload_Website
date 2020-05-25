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

Dopo aver scritto il codice, che costituisce la nostra pagina, possiamo iniziare a capire come pubblicarlo. La prima cosa da fare è acquistare una macchina server. Capiamo però cos'è questa [macchina](https://it.wikipedia.org/wiki/Server).

Il server è un programma o, un dispositivo, che fornisce un servizio a un altro computer, detto client. Queste macchine e/o programmi attendono e soddisfano richieste. Vengono classificate in base al tipo di servizio che offrono, molti di questi li usiamo quotidianamente anche senza rendercene conto, di altri ne abbiamo più consapebolezza. 
Di seguito sono elecanti quelli più comuni:
 - [Mail Server](#Mail-Server)
 - [FTP Server](#FTP-Server)
 - [Web Server](#Web-Server)
 - [DHCP Server](#DHCP-Server)
 - [DNS Server](#DNS-Server)

Ci sono vari sistemi in cui caricare i nostri server, questi variano in base alle diverse necessità delle varie aziende. 

- Per le piccole e medie imprese solitamente viene utilizzato un **server tower**, ovvero un computer assemblato in un case tower appunto, simile ai personal computer ma, con una grande capacità di storage e il supporto RAID. Altre caratteristiche fondamentali di questa tipologia sono: *[la virtualizzazione](#la-virtualizzazione)*, *la gestione dei file e del sito web, delle applicazioni e dei dispositivi condivisi*. 
Somigliando per forma ai personal computer si ha il vantaggio di un facile raffreddamento, possono però, sorgere alcune probblematiche, come la rumorosità, la voluminosità e la complessità nel camblaggio. In questi casi si può optare per delle varianti come il **server rack** e il *server blade**. 
  - Per i **Server Rack** avremo un sistema standard d’installazione per i componenti, questa struttura ha dimensioni specifiche di 48,26cm in larghezza e di 4,445cm in altezza per ogni unità che ospita. I server poggiano su delle slitte in metallo e sono composti da due parti, quella posteriore dove si può agire sui vari collegamenti e, quella anteriore dove si possono maneggiare i comandi fisici, collegando eventualmente un monitor e una tastiera. Tuttavia la riduzione dello spazio occupato porta ad un aumento della densità delle componenti elettriche, la quale a sua volta necessita di un sistema di condizionamento che faccia rimanere la temperatura attorno ai 20 °C.
  
  *Questa soluzione può contenere circa 42 computer*.
  - Mentre, per i **Server Blade** la situazione è leggermente diversa, questa tipologia è pensata per minimizzare al massimo lo spazio occupato. Ogni lama (blade) costituisce una macchina server distinta che, da sola o in concorso con altre, può simulare *N* macchine virtuali. Attualmente questa soluzione è quella con la densità elettronica e la potenza di calcolo maggiori tra quelle disponibili in commercio infatti, i suoi vantaggi e svantaggi sono gli stessi dei rack normali, estremizzati: massime prestazioni, minimo ingombro e cablaggio, necessità di un raffreddamento dedicato, consumi e rumorosità discreti.
  
  *Questa soluzione riesce a raggiungere densità sino a 128 macchine*.

- 
  

## Cosa è un dominio e dove si compra

Ok, adesso che ci siamo procurati un server è il momento di trovare un dominio. Ma prima partiamo spiegando cosa è un dominio.<br>
Un dominio è indirizzo univoco attraverso il quale si richiama un sito internet sulla rete.<br>
Volendo fare un paragone alla vita di tutti i giorni, un dominio è come una via e un numero civico, un modo semplice e facile da ricordare per trovare un determinato posto.<br>
Un dominio è costituito da una serie di stringhe separate da punti. <br><br>
Nei domini è presente una gerarchia molto stringente, prendiamo, per esempio www.google.com e analizziamolo da destra verso sinistra.<br>
Il dominio radice è .com detto anche il dominio di primo livello: top-level domain (TLD). I domini di primo livello si distinguono in domini di primo livello nazionali come .it (italia) .fr (francia) o quelli generici come .net (dedicato ai network) .org (dedicato alle organizzazioni) .com (dedicato alle organizzazioni commerciali) e molti altri.<br>
Continuando a muoverci verso sinistra troviamo: google questo è il dominio di secondo livello, questa parte può essere liberamente scelta dall’utente. Se sono presenti altri sottodomini, come in questo caso, il dominio prende il nome di dominio intermedio.<br>
All’estrema sinistra possiamo trovare www, questo è un dominio di terzo livello. In questo caso specifico non ci sono altri sottodomini perciò questo dominio viene chiamato dominio radice.<br><br>
I nomi di dominio sono formati dalle regole e dalle procedure del Domain Name System (DNS). <br>
In generale, un nome di dominio rappresenta una risorsa IP, ad esempio un server che ospita un sito web o il sito web stesso.<br><br>
Ma come mi posso procurare un dominio?<br>
Per ottenere un domino bisogna rivolgersi a un domain reseller, questa società, dietro un compenso, si occuperà della registrazione del dominio e fornirà l’infrastruttura necessaria a farlo funzionare. Esistono molte aziende che fanno ciò tra le più famose possiamo menzionare GoDaddy, OVH, NameCheap, e molti altri. Di solito la registrazione di un dominio è annua e univoca, di conseguenza se il dominio google.com è già occupato noi non potremmo compralo.
