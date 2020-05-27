# Pubblicazione di un sito web

## Indice dei passaggi

- [Avere il sito da pubblicare](#Avere-il-sito-da-pubblicare)
- [Comprare un server](#Comprare-un-server)
- [Comprare un dominio](#Il-dominio)
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

Prima di pubblicare un sito web dobbiamo necessariamente averne uno, in caso contrario lo si dovrà scrivere. Questo può avvenire attraverso linguaggi come: [HTML](https://en.wikipedia.org/wiki/HTML) & [CSS](https://en.wikipedia.org/wiki/Cascading_Style_Sheets) per la parte grafica, [Javascript](https://en.wikipedia.org/wiki/JavaScript) e [PHP](https://en.wikipedia.org/wiki/PHP) per il backend, mentre, per sviluppare il nostro Database potremmo sfruttare il [MySQLi](https://en.wikipedia.org/wiki/MySQLi).

## Comprare un server

Dopo aver scritto il codice, che costituisce la nostra pagina, possiamo iniziare a capire come pubblicarlo. La prima cosa da fare è acquistare una macchina server. Capiamo però cos'è questa macchina.

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
- [DNS Server](#Il-dominio):
  * Il *Domain Name System* è un server che fa da rubrica telefonica di internet, svolge questo servizio sulla porta 53.

Ci sono molti sistemi in cui caricare i nostri server, questi cambiano in base alle diverse necessità delle varie aziende. 

- Per le piccole e medie imprese solitamente viene utilizzato un **server tower**, ovvero un computer assemblato in un case tower appunto, simile ai personal computer ma, con una grande capacità di storage e il supporto RAID. Altre caratteristiche fondamentali di questa tipologia sono: *la virtualizzazione*, *la gestione dei file e del sito web, delle applicazioni e dei dispositivi condivisi*. 
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
  

  Un'altro servizio che offrono queste server farm è il **colocation in housing**, ovvero un azienda compra il server e pagherà alla server farm solo il prezzo di locazione (affitto, alimentazione, rete, ecc.). In caso di interventi sulla macchina è necessario concordare un appuntamento con il fornitore del servizio, il che potrebbe ritardare l'intervento.

  | Vantaggi della colocation in housing | Svantaggi della colocation in housing |
  | --- | --- |
  | Proprietà dell'hardware e risparmio del canone del noleggio del server dedicato. | Impossibilità di intervenire con rapidità in caso di danno hardware, procedura a carico della server farm in caso di noleggio. |
  | Configurazione totale: il sistema operativo e i software sono installati dell'azienda di housing prima di posizionare la macchina in server farm. | Costo iniziale di startup che comprende l'acquisto della macchina e la configurazione di base. |
  | Possibilità di amministrare totalmente la macchina e di fare aggiornamenti software in qualsiasi momento. | Aggiornamento di sicurezza e dei sistemi a carico del cliente. |


  I data center possono mettere a disposizione delle aziende clienti alcuni **server a uso esclusivo**. La differenza con il sistema in colocation housing sta nel fatto che in questo caso saremo noi a noleggiare l'hardware messo a disposizione dall'azienda. L'amministrazione software è completamente a carico del cliente, in questo modo nel caso di guasti satà il provider del servizio a doversene occupare; questa tipologia di hosting si è diffusa tra le poccole aziende.

  | Vantaggi del noleggio di server dedicati | Svantaggi del noleggio di server dedicati |
  | --- | --- |
  | Delaga degli aggiornamenti di sicurezza allo staff del supporto sistemistico della server farm o dell'azienda che rivende il servizio. | Delega del funzionamento allo staff della server farm, operazione che richiede fiducia e competenza in caso di applicazioni critiche. |
  | Nessun costo di acquisto iniziale della machhina e di installazione e configurazione iniziale. | Costo di affitto mensile dei server che può risultare alto in caso di applicazioni di rete critiche, in aggiunta al costo di connettività e di affitto dello spazio del rack (colocation). |
  | Costo di affitto dei server noto a priori e distribuito in pagamenti mensili. | Impossibilità di ricevere sin da subito una macchina personalizzata, poiché il noleggio di server dedicati nella maggior parte delle server farm non consente personalizzazioni di default particolari, se non con costi aggiuntivi. |

  
  I **server virtuali** o *VPS (Virtual Private Server)* permettono di avere una porzione di hardware condiviso con altri sistemi virtuali. Il provider del servizio mette a disposizione una macchina virtuale collocata su un server fisico che conterrà altre macchine virtuali. Il cliente gestirà la sua macchina virtuale mentre, il fornitore del servizio penserà alla macchina fisica. I software attualmente utilizzati permettono anche di dividere il carico di CPU e RAM allocati a ogni cliente, assicurando così a ognuno l'adeguata capacità di elaborazione.

  | Vantaggi del server virtuale | Svantaggi del server virtuale |
  | --- | --- |
  | Costi bassi. | Mancanza di una macchina fisica a uso esclusivo come server. |
  | Delega di cura tecnica e sicurezza del server fisico alla società che fornisce il servizio. | Possibilità di problemi legati allo scarso setup della virtualizzazione di uno degli utenti presenti sul server virtuali. |
  | Separazione netta tra gli ambienti occupati da diverse aziende che affittano lo stesso server fisico. | La garanzia delle prestazioni dipende dalla capacità di dividere il carico di lavoro tra gli utenti senza personalizzazioni. |

***Come comprare un server?***<br />
//DA COREGGERE
Come abbiamo visto dobbiamo scegliere il server a noi più funzionale e conveniente, in questo caso nè abbiamo scelto uno di tipo virtuale. 

Ok, ma partiamo dall'inizio, prima di tutto bisogna scegliere un hosting, ci solo tante scelte li fuori, alcuni dei principali hosting italiani e non, sono: Aruba, GameHosting, OVH, NFOServer. Noi personalmente abbiamo utilizzato Contabo poiche ha un ottimo rapporto qualità prezzo. In questo caso, non avendo bisogno di tanta potenza abbiamo deciso di adottare il paino più economico. Adesso che ci siamo procurati una VPS, possiamo prosegure.


## Il dominio

Il secondo punto, per caricare il nostro sito web nella rete appunto, è la compera di un dominio; ovvero di un indirizzo univoco attraverso il quale richiameremo il sito in internet. 

Un dominio è costituito da una serie di stringhe separate da punti, in cui è presente una gerarchia molto rigida. Nel dominio che tutti noi conosciamo, `www.google.com`, il dominio radice è `.com` detto anche il di primo livello, *top-level domain (TLD)*. Questi si distinguono in nazionali come `.it` (italia), `.fr` (francia) o quelli generici come `.net` (per i network), `.org` (dedicato alle organizzazioni), `.com` (per le organizzazioni commerciali) e molti altri. Il dominio di secondo livello, riamendo nell'esempio sopracitato, è `google`; questo, può, in caso si presentino altri sottodomini, prendere il nome di *intermedio*. Questa sezione può essere liberamente scelta dall’utente. All’estrema sinistra troviamo `www.`, ovvero un dominio di terzo livello; non essendoci altri sottodomini, questo, prende il nome di *dominio radice*.


I nomi di dominio sono formati dalle regole e dalle procedure del *Domain Name System (DNS)*. Quest'ultimo rappresenta una risorsa IP, come un server che ospita un sito web o il sito web stesso.


***Come comprare un dominio?***<br />
Per ottenere uno bisogna rivolgersi a un *domain reseller*, ovvero, un rivenditore autorizzato di domini; si occuperà della registrazione e fornirà l’infrastruttura necessaria a renderlo funzionante. Molte aziende svolgono questo servizio, tra le più famose possiamo citare [GoDaddy](https://it.godaddy.com/domains/), [OVH](https://www.ovh.it/domini/), [NameCheap](https://www.namecheap.com/domains/), e molti altri. La registrazione è univoca e, solitamente, annua.

## Capiamo cosa è cloudflare (Opzionale)
//DA COREGGERE
CloudFlare è un caching reverse proxy, ovvero un server che si pone tra il server dove risiede il tuo sito e il visitatore.
CloudFlare, in questo modo, si occupa dell'ottimizzazzione dei tempi di caricamento: minimizzando css, il js e memorizzandeli nelle proprie cache in modo da ridurre drasticamente i tempo richiesto per visualizzare una paggina e riducendo il carico sui propri server.
Ma CloudFlare non ha solo questa funzione. Cloudflare si pone fra il sito e il visitatore filtrando il traffico e frapponedosi a mo'di firewall. In questo modo riesce a fornire una protezione agli attacchi Dos o DDos, nascondendo il reale ip della macchina e reidirizzando tutto il traffico in arrivo prima su i suoi server. In questo modo cloudflare riesce a scindere il traffico reale da un traffico fittizzio, e procede ad inoltrare solo il promo e rifiutando il secondo. Ciò vuol dire che fintato il reale ip della macchina rimane sconosciuto al pubblico, le possibilità di ricevere un attacco Ddos sono praticamente pari a 0.
Oltre a tutto ciò il piano base di cloudflare è gratuito.

## Configurazione dominio e cloudflare
***Come posso cominciare ad usare cloudflare?***
Prima di tutto bisognerà crearci un account cloudflare e registrarci un dominio. Una volta registrato il dominio su cloudflare, esso ti fornirà dei Name Server (NS) da usare per il proprio dominio. 
Adesso bisognera andare nel pannello fornito dal proprio hosting e modificare i NS del dominio. 

***Come posso cofigurare i dns?***
Cambiati i Name Server, il proprio dominio sarà completamente configurabile attraverso cloudflare.  
Bisognerà, adesso, impostare un record A che punti all'ip della macchina, o nel nostro caso alla VPS. 
