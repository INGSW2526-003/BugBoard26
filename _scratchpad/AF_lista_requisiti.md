#### Nota
Alcuni dettagli del sistema sono ancora da definire quindi questi requisiti non sono ancora completi e potrebbero essere inconsistenti.

1. #UserRequirement `BugBoard26` è una piattaforma per la gestione collaborativa di issue in progetti software. Il sistema consente a team di sviluppo di segnalare problemi relativi a un progetto, monitorarne lo stato, assegnarli a membri del team e tenere traccia delle attività di risoluzione. Il sistema deve consistere in un’applicazione (mobile, desktop o web-based) performante e affidabile, attraverso cui gli utenti possono fruire delle funzionalità in modo intuitivo e rapido.

2. #UserRequirement essere implementato un sistema di autenticazione semplice e sicuro, basato su email e password. 
	1.  La gestione della password dovrebbe essere conforme allo standard ISO 27001/27002 oppure allo standard NIST per garantirne una gestione sicura. La password iniziale sarà generata dal sistema secondo questi standard.
	2. Il sistema non fornisce un servizio email, dunque sarà responsabilità dell'amministratore quella di fornire un indirizzo email valido e funzionante (ad esempio se l'azienda ha un servizio email, quello potrà essere usato)

3. #UserRequirement Le informazioni gestite dall’applicazione sono critiche per l’azienda, ed è fondamentale. preservarne l’integrità e la segretezza.
	1. Le informazioni che un utente può visualizzare sono accessibili soltanto dopo il login e dipendono dalla tipologia di utente che effettua l'accesso.
	2. Le comunicazioni via rete con il server on the cloud dovrebbero usare il protocollo HTTPS per garantire la sicurezza delle comunicazioni client-server

4. #UserRequirement un amministratore può creare ulteriori utenze, specificando una email, una password, e indicando se quell’utenza sarà “normale” oppure “di amministrazione”.

5. Una issue dovrebbe contenere le seguenti informazioni:
	- **Id**: identificativo generato dal sistema, identifica univocamente la issue nel sistema
	- **Title**: un nome conciso e descrittivo del problema
	- **Descrizione**: una descrizione dettagliata del problema, include i seguenti campi:
		- step necessari per riprodurre la issue
		- risultati attesi
		- risultati ottenuti
	- **Priority**: l'urgenza con cui la issue deve essere risolta 
	- **Stato**: descrive lo stato corrente della issue. Lo stato può assumere i seguenti valori: 
		- `todo`: la issue è stata segnalata e ancora non è stata presa in carico
		- `assigned`: la issue è stata assegnata ad un utente per la risoluzione
		-  `in_progress`: l'utente che ha in carico la issue ha iniziato a lavorarci
		- `review`: una soluzione è stata proposta ed è in attesa di approvazione
		- `done`:  la soluzione è stata approvata
		- `blocked`: la issue viene chiusa in quanto ritenuta non opportuna
	- **Reporter**: utente che segnala la issue
	- **Fixer**: utente che prende in carico la issue con l'obiettivo di risolverla
	- **Resolution**: descrizione della risoluzione dello issue
	- **Type**: definisce il tipo della issue e può assumere i seguenti valori:
		- `bug`: segnala malfunzionamenti
		- `question`: per richieste di chiarimenti
		- `documentation`: segnala problemi relativi alla documentazione
		- `feature`: indicare richiesta o suggerimento di nuove funzionalità
	- **Attachments**: file necessari per fornire evidenze visive del problema o anche dettagli tecnici (ad esempio logs, immagini, screenshots, code...)

	1. La priority dovrebbe poter essere settata soltanto da utenti di che tipo?
	2. Il Fixer dovrebbe essere assegnato da chi? 

6. #UserRequirement Tutti gli utenti autenticati possono segnalare una issue indicando almeno un titolo e una descrizione.
	1. Di una issue dovrebbero essere specificati i seguenti campi in **fase di segnalazione**:
		- **Id**: identificativo generato dal sistema, identifica univocamente la issue nel sistema
		- **Title**: un nome conciso e descrittivo del problema
		- **Descrizione**: una descrizione dettagliata del problema
			1. La descrizione della issue dovrebbe includere: 
				- gli step per riprodurre la issue
				- i risultati attesi
				- i risultati attuali
		- **Priority**: l'urgenza con cui la issue deve essere risolta
			1. 
	2. Una issue dovrebbe avere un campo **Stato** che descrive lo stato corrente della issue. Lo stato può assumere i seguenti valori: `todo`, `in_progress`, `review`, `done`, `blocked`
		1. Lo stato di una issue appena creata è `todo`

7.  #UserRequirement Il sistema deve offrire una vista riepilogativa delle issue, con la possibilità di filtrare o ordinare i risultati in base a criteri come tipologia, stato, priorità o altri parametri rilevanti. 
	1. #FunctionalRequirement Per una vista riepilogativa i seguenti filtri dovrebbero essere disponibili:
		- `title`
		- `priority`
		- `stato`
		- `reporter`
		- `fixer`
		- `type`
		- #Decidere `other teams`: se selezionato dovrebbe inserire nella ricerca anche le issue degli altri team. Dovrebbe essere possibile selezionare quali team aggiungere nella ricerca.
		Più di un filtro può essere selezionato simultaneamente.
	2. Dovrebbe essere possibile ordinare i risultati di una visita riepilogativa in ordine ascendente o discendente selezionando tra i filtri disponibili.
	3. #Decidere Se ci sono più team, l'utente che effettua la ricerca (che non sia l'utente root) dovrebbe ottenere una vista delle issue che appartengono al suo team. Nel caso voglia vedere le issue degli altri team deve selezionare i team da includere nella ricerca tra i filtri disponibili. 
	4. #Decidere Se ci sono più team, se l'utente che fa la ricerca è l'utente amministratore root, nel momento in cui effettua una ricerca questa automaticamente dovrebbe essere fatta su tutti i team, essendo che questo utente non appartiene a nessun team specifico.

8. #UserRequirement  Deve essere prevista una sezione per commenti associata a ciascun bug, in cui tutti gli utenti possano lasciare messaggi, aggiornamenti o richieste di chiarimento.