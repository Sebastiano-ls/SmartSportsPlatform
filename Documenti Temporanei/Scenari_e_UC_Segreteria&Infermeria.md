
# 1. Scenari

## 1.1 Segreteria

Mercoledì 4 novembre 2026 l'addetta di segreteria Paola Ferri si autentica su SSP con username p.ferri@gmail.com e password Segreteria-2026 ed accede alla homepage dedicata agli utenti registrati aventi il ruolo di Addetto Segreteria.
La segretaria Paola Ferri accede all'area Segreteria dove sono presenti le voci "Clienti", "Aggiungi Cliente", "Prenotazioni del GIorno" e "Assistenza".
Il sistema mostra di base la lista dei clienti con la possibilità di cercarne uno in particolare.
Alle 9:00 si presenta al bancone Davide Russo, che vuole iscriversi al corso di Spinning ma non ha ancora effettuato la registrazione nel sistema. 
Paola seleziona Aggiungi cliente e inserisce nome, cognome, codice fiscale, data di nascita ed e-mail d.russo@libero.it. Il sistema verifica che l'e-mail non sia già registrata e che Davide non risulti radiato confrontando il proprio codice fiscale con lo storico dei codici fiscali dei clienti che sono stati radiati dal centro, crea l'account e invia a Davide una e-mail per impostare la password. Paola apre la sezione Iscrizioni della scheda di Davide, seleziona Aggiungi iscrizione e sceglie Spinning. 
Il sistema registra l'iscrizione e salva che l'operazione è stata fatta da Paola Ferri.
Alle 11:00 telefona Mario Rossi: è prenotato al corso di Nuoto giovedì 5 novembre alle 19:00, ma vuole spostarsi a venerdì 6 novembre alla stessa ora. 
Paola cerca "Mario Rossi", apre la sezione Prenotazioni, seleziona la prenotazione di giovedì e la funzionalità Sposta. 
Il sistema mostra gli slot liberi del corso di Nuoto. 
Paola sceglie venerdì 6 novembre alle 19:00, dove ci sono 3 posti liberi. 
Il sistema mostra il riepilogo dello spostamento e Paola conferma.
Il sistema libera il posto di giovedì, registra quello di venerdì, salva che l'operazione è stata fatta da Paola Ferri, invia a Mario una e-mail con la nuova data e aggiorna l'evento nel suo Google Calendar.
Alle 12:00 Paola aggiorna il numero di telefono di Mario nella sua scheda. Il sistema salva il dato, registra la modifica e salva che l’operazione è stata fatta da Paola Ferri.
Alle 15:00 Paola nota la presenza di un nuovo ticket all'interno dell'area dedicata "Assisetnza", il Ticket presenta un bollino rosso (priorità alta), il tipo "Segnalazione", un'oggetto "Cattiva condotta nei confronti della buona cura della struttura ospitante" ed una descrizione in cui, l'atleta Luca Bianchi, segnala che un altro utente di nome Domenico Ricci, in seguito ad un eccesso di ira ha scaraventato a terra degli armadietti dello spogliatoio e danneggiato una doccia.
Paola, vista la particolare gravità dell'accaduto decide di inoltrare il ticket al Manager del centro, attraverso una selezione dedicata, per lasciare che egli possa prendere i giusti provvedimenti, ed eventualmente decidere di radiarlo dal centro sportivo. 
Il sistema procede a recapitare il ticket nella area di gestione ticket del Manager.
Successivamente genera un nuovo ticket di media priorità (colore giallo), di tipo "Segnalazione", con oggetto "Necessità di riparazione doccia nello spogliatoio maschile della sala pesi" e una descrizione breve e chiara, e la inoltra al Manager perchè possa chiamare le figure di competenza.
Il sistema procede a recapitare il ticket nella area di gestione ticket del Manager.
Scenari alternativi
•	Lo slot di venerdì alle 19:00 è al completo: Paola propone a Mario lunedì 9 novembre alle 19:00.
•	Mario chiede di annullare la prenotazione invece di spostarla: Paola seleziona Annulla e il sistema libera il posto, avvisa Mario e salva che l’operazione è stata fatta da Paola Ferri.
•	Paola prova a registrare una persona radiata dal centro: il sistema blocca l'inserimento e mostra il motivo.
•	Paola prova a registrare una persona il cui indirizzo di posta elettronica è gia associato ad un altro cliente: il sistema blocca l'inserimento e mostra il motivo.
•	Paola legge il ticket inviato da un cliente, e poichè si tratta di una situazione di cui essa si può occupare: compila una risposta che il sistema inoltrerà al cliente e interagisce con la selezione che conferma che il ticket è risolto facendo in modo che il sistema ne memorizzi lo stato di risoluzione.

---

## 1.2 Infermeria

Martedì 3 novembre 2026 il dott. Luca Neri si autentica su SSP con username l.neri@gmail.com e password Infermeria-2026 ed accede alla homepage dedicata agli utenti registrati aventi il ruolo di Medico.
Il medico accede all'area Infermeria dove sono presenti le voci "Clienti del Centro" e "Calendario delle Visite". 
Il sistema mostra di base il calendario delle visite del giorno, con un colore per le visite confermate e uno per quelle da confermare, e gli orari liberi.
Alle 10:30 il medico visita Giulia Esposito. Al termine apre la sezione Clienti, cerca "Giulia Esposito", ne cambia lo stato di salute da "guarito" a "in guarigione" e carica il referto medico aggiornato. 
Il sistema salva il nuovo stato, il referto e la data della modifica.
Nel pomeriggio la segreteria gli comunica che il cliente Mario Rossi si è fatto male al ginocchio durante l'allenamento. Il medico seleziona l'orario libero di giovedì 5 novembre alle 10:00, seleziona il cliente Mario Rossi e inserisce il motivo "Controllo dopo infortunio al ginocchio". 
Il sistema confronta l'orario con la fascia preferita di Mario (18:00–20:00) e avvisa il medico che la visita sarà "da confermare". 
Il medico seleziona Registra.
Il sistema salva la visita con stato "da confermare", la mostra nel calendario con un colore diverso e invia a Mario una e-mail con data, ora, motivo e un link per confermare. Mario apre il link, si autentica con username m.rossi@gmail.com e password Nuoto-1990, visualizza nella bacheca delle notifiche i dettagli e seleziona Conferma. 
Il sistema passa la visita a "confermata", aggiorna il colore nel calendario e avvisa il medico.
Giovedì, dopo la visita, il medico cambia lo stato di salute di Mario da "infortunato" a "in guarigione".
Scenari alternativi
•	Il medico sceglie un orario dentro la fascia di Mario (18:30): la visita è subito confermata e Mario riceve solo una e-mail di notifica.
•	Mario rifiuta la visita: il sistema la annulla, libera l'orario e avvisa il medico.
•	Il medico annulla una visita del giorno: il sistema chiede conferma, libera l'orario e avvisa il cliente.

---

---

# 2. Casi d'Uso
## 2.1 Segreteria
### UC 1: Gestione dell'anagrafica e delle iscrizioni
Attore: Segreteria
Entry Condition: L'addetto è autenticato e si trova nell'area Segreteria
Flusso di eventi:
1.	L'addetto seleziona Aggiungi cliente
2.	L'addetto inserisce nome, cognome, data di nascita ed e-mail
3.	Il sistema verifica che l'e-mail non sia già registrata e che la persona non risulti radiata
4.	Il sistema crea l'account e invia all'utente una e-mail per impostare la password
5.	L'addetto apre la sezione Iscrizioni della scheda, seleziona Aggiungi iscrizione e sceglie un corso
6.	Il sistema registra l'iscrizione e invia all'utente una e-mail di conferma
7.	Il sistema salva il nome dell'addetto che ha eseguito ogni operazione
Exit Condition: L'utente è registrato e iscritto al corso; l'addetto visualizza la sua scheda
Flussi alternativi / Eccezioni:
Se l'utente è già registrato, l'addetto lo cerca per nome o e-mail, apre la scheda, modifica i dati e salva; il flusso prosegue dal punto 5 se serve un'iscrizione.
Se al punto 3 la persona risulta radiata, verrà eseguito il caso d'uso UC 10.1 Persona radiata.
Se al punto 5 l'addetto rimuove un'iscrizione, il sistema chiede conferma, annulla anche le prenotazioni future dell'utente a quel corso e lo avvisa.
Se al punto 5 l'utente è già iscritto al corso, il sistema lo comunica

#### UC 1.1: Persona radiata
Attore: Segreteria
Entry Condition: L'addetto ha provato a registrare una persona radiata dal centro
Flusso di eventi:
1.	Il sistema non crea l'account
2.	Il sistema mostra il messaggio "Persona radiata dal centro" con la data e il motivo della radiazione
Exit Condition: L'addetto si trova sul modulo di inserimento del cliente

### UC 2: Gestione del corso per conto di un utente
Attore: Segreteria
Entry Condition: L'addetto è autenticato e sta visualizzando la scheda di un utente
Flusso di eventi:
1.	L'addetto seleziona la sezione Prenotazioni
2.	Il sistema mostra le prenotazioni dell'utente
3.	L'addetto seleziona una prenotazione e la funzionalità Sposta
4.	Il sistema mostra gli slot liberi dello stesso corso
5.	L'addetto sceglie il nuovo slot
6.	Il sistema mostra il riepilogo dello spostamento e chiede conferma
7.	L'addetto conferma
8.	Il sistema libera il vecchio posto, registra il nuovo e salva il nome dell'addetto
9.	Il sistema invia all'utente una e-mail con la nuova data e aggiorna Google Calendar, se collegato
Exit Condition: La prenotazione è spostata e l'addetto visualizza le prenotazioni dell'utente
Flussi alternativi / Eccezioni:
Se al punto 3 l'addetto seleziona Nuova prenotazione, sceglie un corso a cui l'utente è iscritto e il flusso prosegue dal punto 4 senza un posto da liberare.
Se al punto 3 l'addetto seleziona Annulla, il sistema chiede conferma, annulla la prenotazione, libera il posto e avvisa l'utente.
Se al punto 8 lo slot si è riempito nel frattempo, verrà eseguito il caso d'uso UC 3.2 Slot esaurito.


## 2.2 Infermeria
### UC 1: Gestione delle visite mediche
Attore: Medico
Entry Condition: Il medico è autenticato e si trova nell'area Infermeria
Flusso di eventi:
1.	Il sistema mostra il calendario delle visite del giorno, con un colore per le visite confermate e uno per quelle da confermare, e gli orari liberi
2.	Il medico cambia giorno o passa alla vista settimanale (opzionale)
3.	Il medico seleziona un orario libero
4.	Il sistema mostra il modulo della nuova visita
5.	Il medico seleziona l'utente e inserisce il motivo
6.	Il sistema verifica che l'orario sia libero e lo confronta con la fascia preferita dell'utente: l'orario è dentro la fascia
7.	Il medico seleziona Registra
8.	Il sistema salva la visita come "confermata" e invia all'utente una e-mail con data, ora e motivo
Exit Condition: La visita è registrata e il medico visualizza il calendario aggiornato
Flussi alternativi / Eccezioni:
Se al punto 6 l'orario è fuori dalla fascia preferita dell'utente, verrà eseguito il caso d'uso UC 8.1 Visita fuori fascia.
Se al punto 6 l'orario è già occupato, il sistema mostra un messaggio di errore e ripresenta il calendario.
Se al punto 3 il medico seleziona una visita esistente, il sistema ne mostra i dettagli; il medico può annullarla: il sistema chiede conferma, libera l'orario e avvisa l'utente.
UC 8.1: Visita fuori fascia
Attore: Medico
Entry Condition: Il medico ha scelto un orario fuori dalla fascia preferita dell'utente
Flusso di eventi:
1.	Il sistema avvisa il medico che la visita sarà "da confermare"
2.	Il medico seleziona Registra
3.	Il sistema salva la visita con stato "da confermare" e la mostra nel calendario con un colore diverso
4.	Il sistema invia all'utente una e-mail con il link per confermare o rifiutare la visita (UC 4)
Exit Condition: La visita è "da confermare" e il medico visualizza il calendario

### UC 2: Gestione dello stato di salute degli utenti
UC 9: Gestione dello stato di salute degli utenti
Attore: Medico
Entry Condition: Il medico è autenticato e si trova nell'area Infermeria
Flusso di eventi:
1.	Il medico seleziona la sezione Clienti
2.	Il sistema mostra l'elenco degli utenti con il loro stato di salute (infortunato, in guarigione, guarito) e i totali per stato
3.	Il medico cerca un utente per nome o filtra per stato
4.	Il medico seleziona un utente
5.	Il sistema mostra la scheda con lo stato attuale e lo storico delle visite
6.	Il medico seleziona Aggiorna stato, sceglie il nuovo stato e seleziona Salva
7.	Il sistema salva il nuovo stato e la data della modifica
Exit Condition: Lo stato di salute è aggiornato e il medico visualizza la scheda dell'utente
Flussi alternativi / Eccezioni:
Se al punto 3 nessun utente corrisponde alla ricerca, il sistema mostra "Nessun cliente trovato".