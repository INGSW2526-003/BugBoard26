## Funzionalità del Sistema
`BugBoard26` è una piattaforma per la gestione collaborativa di issue in progetti software. Il sistema consente a team di sviluppo di segnalare problemi relativi a un progetto, monitorarne lo stato, assegnarli a membri del team e tenere traccia delle attività di risoluzione. Il sistema deve consistere in un’applicazione (mobile, desktop o web-based) performante e affidabile, attraverso cui gli utenti possono fruire delle funzionalità in modo intuitivo e rapido.

3.1
Funzionalità del sistema `BugBoard26`

#### Funzionalità 1
Deve essere implementato un sistema di autenticazione semplice e sicuro, basato su email e
password. Le informazioni gestite dall’applicazione sono critiche per l’azienda, ed è fondamentale
preservarne l’integrità e la segretezza.
- è necessario un sistema di encryption dei dati sensibili
Il sistema viene fornito con un account da amministratore già attivo, con credenziali di default. Un amministratore può creare ulteriori utenze, specificando una email, una password, e indicando se quell’utenza sarà “normale” oppure “di amministrazione”.
- Questo significa che l'amministratore iniziale può creare altri account amministratori
	- decidere se questi sono sullo stesso livello
	- stabilire se ogni amministratore ha un team di sviluppo e un progetto da gestire
	- Si può considerare che il prodotto offra la gestione di più di un progetto all'interno della stessa azienda software che l'acquista. Ad esempio può esistere un amministratore centrale, che è un po la root del sistema. E poi ci sono diversi progetti da gestire, ognuno con il suo amministratore di progetto e il suo team di sviluppo.
#### Funzionalità 2
 Tutti gli utenti autenticati possono segnalare una issue indicando almeno un titolo e una
descrizione. Alcuni utenti potrebbero voler specificare anche una priorità e sarebbe gradita la
possibilità di allegare un’immagine. Le issue possono essere di diverso tipo: question (per
richieste di chiarimenti), bug (per segnalare malfunzionamenti), documentation (per segnalare
problemi relativi alla documentazione), e feature (per indicare la richiesta o il suggerimento di
nuove funzionalità). Le issue create sono inizialmente nello stato “todo”.

#### Funzionalità 3
 Il sistema deve offrire una vista riepilogativa delle issue, con la possibilità di filtrare o ordinare i risultati in base a criteri come tipologia, stato, priorità o altri parametri rilevanti.

#### Funzionalità 4
 Deve essere prevista una sezione per commenti associata a ciascun bug, in cui tutti gli utenti
possano lasciare messaggi, aggiornamenti o richieste di chiarimento.

### Obiettivi del Prodotto
Il prodotto è un sistema di gestione degli issue relativi ad un singolo progetto software.
La gestione è interna: un amministratore gestisce il suo team di sviluppo e tutti lavorano soltanto ad un software. Non c'è comunicazione tra diversi team di sviluppo che sono totalmente indipendenti tra loro e utilizzano istanze differenti del prodotto.

### Acquisto del Prodotto
Lo scenario di acquisto è il seguente: 
- esiste un team di sviluppo interessato ad utilizzare il prodotto
- effettua l'acquisto
- all'acquisto, al team di sviluppo saranno fornite: 
	- una copia/istanza privata dell'applicativo che permette la gestione interna di un singolo progetto software 
	- un dominio di rete per l'istallazione del server nel cloud
	- un account amministratore già attivo

### Implementazione
Il sistema deve essere un sistema distribuito.
Non esiste nessun server centrale che mette in comunicazione le diverse istanze del prodotto tra loro in quanto non è necessario: il prodotto serve alla gestione interna di un progetto software, non serve a diversi team che lavorano su diversi progetti di comunicare tra loro.


