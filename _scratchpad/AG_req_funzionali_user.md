# Requisiti funzionali

Attenendomi all'ambiente su cui si sta progettando, ho ricavato per ogni funzionalità date da [AF_descrizione_generale](https://github.com/INGSW2526-003/BugBoard26/blob/main/_scratchpad/AF_descrizione_generale.md), ho suddiviso per interazione dell'utente e tipologia dell'utente, le varie funzionalità ai vari livelli. (I livelli vanno interpetrati pensando ai possibili mock-up).

*Template utilizzato per le funzionalità: <_user> ha/può <_function>*

## Livello 0
Esempio: L'utente si è appena interfacciato all'applicazione
Utente : User
Interazione: Login

1. L'utente effettua il login con credenziali offerta dall'admin composte da email e password
2. L'utente ha la possibilità di selezionare "Crea dominio"
3. L'utente ha la possibilità di selezionare "Partecipa a dominio"

## Livello 1
Esempio: L'utente si è appena autenticato con partecipazione ad un dominio
Utente: User
Precondizione: L'utente fa parte del team di sviluppo
Interazione: Autenticato ad un dominio

1. L'utente può segnalare un issue indicando titolo e una descrizione 
2. L'utente può visualizzare il suo team di sviluppo di appartenenza -> il progetto affidato -> il lavoro affidato
3. L'utente può visualizzare altri progetti, filtrando o ricercando, su cui il team sta lavorando - anche se non inerente al suo lavoro
4. L'utente può selezionare l'apposita sezione dedicata ad issue e visualizzare quelle rese note
5. L'utente può commentare tutte le le issue visualizzate da (4)
6. L'utente ha una sezione "Ticket" che mostra le sue issue segnalate e vederne lo stato (to do, etc..)
7. L'utente può ricercare nomi di altri collaboratori e selezionarli.
8. Ogni utente ha un proprio profilo con descrizione, contatti e progetti su cui sta lavorando
9. L'utente ha nel suo profilo sezione dedicata a issue segnalate da lui con lo stato "closed" con commenti fatti nei stati precedenti
10. L'utente non può commentare lo stato closed (nn penso sia funzionale)

