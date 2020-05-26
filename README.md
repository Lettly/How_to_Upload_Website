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
- Mail Server:
  * I *Mail server* sono server che, utilizzando le porte 25, 587, 465, 110, 143 e 993, permettono di inviare e smistare mail da un pc all'altro.
- FTP Server:
  * Il *File Transport Protocol* è un server che permette il trasferimento di file tra host e client, lavorando sulla porta 21.
- Web Server:
  * Il *Web Server* è un server in grado di gestire le richieste di trasferimento di pagine web, utilizza la porta 80 e 443.
- DHCP Server:
  * Il *DHCP Server* permette ai dispositivi di una rete locale di ricevere automaticamente la configurazione IP necessaria per stabilire una connessione e operare in rete, svolge questo servizio utilizzando la porta 67.
- [DNS Server](#Cosa-è-un-dominio-e-dove-si-compra):
  * Il *Domain Name System* è un server che fa da rubrica telefonica di internet, svolge questo servizio sulla porta 53.

Ci sono vari sistemi in cui caricare i nostri server, questi variano in base alle diverse necessità delle varie aziende. 

- Per le piccole e medie imprese solitamente viene utilizzato un **server tower**, ovvero un computer assemblato in un case tower appunto, simile ai personal computer ma, con una grande capacità di storage e il supporto RAID. Altre caratteristiche fondamentali di questa tipologia sono: *[la virtualizzazione](#la-virtualizzazione)*, *la gestione dei file e del sito web, delle applicazioni e dei dispositivi condivisi*. 
Somigliando per forma ai personal computer si ha il vantaggio di un facile raffreddamento, possono però, sorgere alcune probblematiche, come la rumorosità, la voluminosità e la complessità nel camblaggio. In questi casi si può optare per delle varianti come il **server rack** e il *server blade**. 
  - Per i **Server Rack** avremo un sistema standard d’installazione per i componenti, questa struttura ha dimensioni specifiche di 48,26cm in larghezza e di 4,445cm in altezza per ogni unità che ospita. I server poggiano su delle slitte in metallo e sono composti da due parti, quella posteriore dove si può agire sui vari collegamenti e, quella anteriore dove si possono maneggiare i comandi fisici, collegando eventualmente un monitor e una tastiera. Tuttavia la riduzione dello spazio occupato porta ad un aumento della densità delle componenti elettriche, la quale a sua volta necessita di un sistema di condizionamento che faccia rimanere la temperatura attorno ai 20 °C.
  
  *Questa soluzione può contenere circa 42 computer*.
  - Mentre, per i **Server Blade** la situazione è leggermente diversa, questa tipologia è pensata per minimizzare al massimo lo spazio occupato. Ogni lama (blade) costituisce una macchina server distinta che, da sola o in concorso con altre, può simulare *N* macchine virtuali. Attualmente questa soluzione è quella con la densità elettronica e la potenza di calcolo maggiori tra quelle disponibili in commercio infatti, i suoi vantaggi e svantaggi sono gli stessi dei rack normali, estremizzati: massime prestazioni, minimo ingombro e cablaggio, necessità di un raffreddamento dedicato, consumi e rumorosità discreti.
  
  *Questa soluzione riesce a raggiungere densità sino a 128 macchine*.

- I **data center** sono soluzioni pensate principalmente per grandi aziende che, in Italia, conosciamo come CED *Centro Elaborazione dati*. Tutti i dati e le informazioni che viaggiano in rete sono conservate in questi data center. All’interno di questi data center vengono collocati una serie di server che prendono il nome di Server Farm o Web-Server. All’interno di questi luoghi spesso viene costituito un sistema di cluster per gestire carichi di lavoro pesanti garantendo affidabilità e tolleranza ai guasti tramite una ridondanza fisica degli apparati.

| Vantaggi di un data center interno | Svantaggi di un data center interno |
| --- | --- |
| Possibilità di agire fisicamente in tempi rapidi in caso di malfunzionamenti. | Necessità di aree da destinare a tale uso, con l’aumento dei costi di affitto degli uffici.|
| Possibilità di avere un rapporto fisico tra l’area amministrativa e operativa di unázienda e l’area sistemi e sviluppo. | Acquisto dell’hardware e delle risorse per gestire i dati. |
| Controllo diretto sulla riservatezza dei dati a garanzia della privacy di dipendenti e clienti. | Costi per l’aggiornamento dei server e per la formazione. |
| Controllo diretto sulla sicurezza dei dati in caso di instrusione e potenziali minacce software (virus). | Costi per la sicurezza anti intrusione, backup e coservazione dell’integrità dei dati. |

- Le **Server Farm** sono aree fisiche, ubicate solitamente nel sottosuolo, che possono ospitare centinaia di macchine server. Queste aree devono avere caratteristiche specifiche:
  - sicurezza fisica e sistemi di anti intrusione;
  - alimentazione ridondata (duplicata), con gruppi di continuità;
  - connettività a Internet stabile, garantita e affidabile;
  - impianto di condizionamento per mantenere la temperatura bassa;
  - sicurezza software tramite firewall e protezione logica delle macchine;

  Questi sistemi generalmente offrono dei servizi detti di hosting, che consistono nell'installare la propria applicazione web in server di proprietà del provider e gestiti dal provider stesso. Ogni hosting può avere costi, prestazioni e opzioni differenti, in base al fornitore. 
  

    Un'altro servizio che offrono queste server farm è il colocation in housing, ovvero un azienda compra il server e pagherà alla server farm solo il prezzo di locazione (affitto, alimentazione, rete, ecc.). In caso di interventi sulla macchina è necessario concordare un appuntamento con il fornitore del servizio, il che potrebbe ritardare l'intervento.

    | Vantaggi della colocation in housing | Svantaggi della colocation in housing |
    | --- | --- |
    | Proprietà dell'hardware e risparmio del canone del noleggio del server dedicato. | Impossibilità di intervenire con rapidità in caso di danno hardware, procedura a carico della server farm in caso di noleggio. |
    | Configurazione totale: il sistema operativo e i software sono installati dell'azienda di housing prima di posizionare la macchina in server farm. | Costo iniziale di startup che comprende l'acquisto della macchina e la configurazione di base. |
    | Possibilità di amministrare totalmente la macchina e di fare aggiornamenti software in qualsiasi momento. | Aggiornamento di sicurezza e dei sistemi a carico del cliente. |


    I data center possono mettere a disposizione delle aziende clienti alcuni server a uso esclusivo. La differenza con il sistema in colocation housing sta nel fatto che in questo caso saremo noi a noleggiare l'hardware messo a disposizione dall'azienda. L'amministrazione software è completamente a carico del cliente, in questo modo nel caso di guasti satà il provider del servizio a doversene occupare; questa tipologia di hosting si è diffusa tra le poccole aziende.

    | Vantaggi del noleggio di server dedicati | Svantaggi del noleggio di server dedicati |
    | --- | --- |
    | Delaga degli aggiornamenti di sicurezza allo staff del supporto sistemistico della server farm o dell'azienda che rivende il servizio. | Delega del funzionamento allo staff della server farm, operazione che richiede fiducia e competenza in caso di applicazioni critiche. |
    | Nessun costo di acquisto iniziale della machhina e di installazione e configurazione iniziale. | Costo di affitto mensile dei server che può risultare alto in caso di applicazioni di rete critiche, in aggiunta al costo di connettività e di affitto dello spazio del rack (colocation). |
    | Costo di affitto dei server noto a priori e distribuito in pagamenti mensili. | Impossibilità di ricevere sin da subito una macchina personalizzata, poiché il noleggio di server dedicati nella maggior parte delle server farm non consente personalizzazioni di default particolari, se non con costi aggiuntivi. |



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

