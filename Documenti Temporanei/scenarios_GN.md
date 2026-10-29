# 1 Scenari

## *Scenario 1 — Il visitatore scopre il centro e si registra*
Sara Conti ha appena cambiato città e cerca una piscina vicino casa. Lunedì 2 novembre 2026 apre il sito di SSP dal suo smartphone e visualizza la home page con i servizi del centro: corsi, visite mediche, orari.

Sara seleziona la sezione "Corsi" e visualizza l'elenco dei corsi attivi, con giorni, orari e posti liberi. Sara filtra per la categoria "Acqua", seleziona il corso di Nuoto e visualizza il dettaglio: giovedì e venerdì dalle 19:00 alle 20:00, istruttore Alessio Bianchi, 3 posti liberi su 10.

Sara seleziona "Iscriviti". Il sistema le chiede di accedere o di registrarsi e Sara seleziona "Registrati". Sara inserisce nome Sara, cognome Conti, data di nascita 14/03/2001, e-mail sara.conti01@gmail.com e password Vasca-2001. Sara legge l'informativa sulla privacy, la accetta e conferma.

Il sistema controlla i dati, verifica che l'e-mail non sia già registrata e che Sara non risulti radiata dal centro. Il sistema crea l'account, invia una e-mail di benvenuto a sara.conti01@gmail.com e porta Sara, ora utente registrata, alla pagina del corso di Nuoto.

Sara seleziona di nuovo "Iscriviti". Il sistema registra l'iscrizione al corso di Nuoto, la mostra nell'area personale di Sara e le invia una e-mail di conferma. Sara seleziona "Prenota allenamento", sceglie giovedì 5 novembre nella fascia 19:00–20:00, conferma lo slot delle 19:00 e riceve la e-mail di conferma della prenotazione.

## Scenari alternativi
- L'e-mail sara.conti01@gmail.com è già registrata: il sistema avvisa Sara e le propone di autenticarsi.
- Sara non accetta l'informativa sulla privacy: il sistema non crea l'account.
- Sara usa i dati di una persona radiata dal centro: il sistema blocca la registrazione e mostra il messaggio "Non è possibile registrarsi: rivolgersi alla segreteria".

## *Scenario 2 — L'utente organizza la settimana di allenamento*
Giulia Esposito è iscritta ai corsi di Pilates e Nuoto. Lunedì 2 novembre 2026 si autentica su SSP inserendo username g.esposito@gmail.com e password Pilates-2026. Il sistema mostra l'area personale con le prossime prenotazioni e le notifiche.

Giulia seleziona "Profilo" e imposta la fascia oraria preferita dalle 18:00 alle 20:00, perché lavora fino alle 17:30. Poi seleziona "Collega Google Calendar": il sistema la porta alla pagina di autorizzazione di Google, Giulia autorizza l'accesso e il sistema torna al profilo con il calendario collegato.
Giulia seleziona "Prenota allenamento", sceglie il corso di Pilates, il giorno lunedì 2 novembre e la fascia 18:00–20:00. Il sistema mostra gli slot della fascia: alle 18:00 ci sono 6 posti liberi, alle 19:00 il corso è al completo. Giulia sceglie lo slot delle 18:00 e il sistema mostra il riepilogo: corso Pilates, lunedì 2 novembre, 18:00–19:00, istruttore Marco Rossi. Giulia conferma. Il sistema registra la prenotazione, riduce i posti liberi, invia la e-mail di conferma e aggiunge l'evento al Google Calendar di Giulia.

Martedì Giulia sente dolore al ginocchio dopo la corsa. Seleziona "Prenota visita", sceglie martedì 3 novembre e l'orario libero delle 10:30, inserisce il motivo "Dolore al ginocchio dopo la corsa" e conferma. Il sistema registra la visita, invia la conferma a Giulia e avvisa il medico, dott. Luca Neri.
Mercoledì il medico le consiglia di non nuotare per qualche giorno. Giulia apre "Le mie prenotazioni", seleziona la prenotazione di Nuoto di giovedì 5 novembre alle 19:00 e seleziona "Annulla". Il sistema chiede conferma, Giulia conferma e il sistema annulla la prenotazione, libera il posto, invia la e-mail di annullamento e toglie l'evento dal suo Google Calendar.

Giovedì, in sala pesi, Giulia si accorge che il tapis roulant n. 3 non si avvia. Seleziona "Assistenza" e "Nuovo ticket", sceglie il tipo Segnalazione, l'oggetto "Tapis roulant n. 3 non si avvia", la descrizione "Il display resta spento anche premendo il tasto di accensione" e la priorità Rossa (alta). Il sistema ricorda che per una segnalazione la foto è obbligatoria: Giulia scatta la foto tapis3.jpg (2,1 MB) e la allega. Giulia seleziona "Invia". Il sistema controlla i campi e l'immagine, salva il ticket T-0042 con stato "Aperto" e invia a Giulia la conferma.
Venerdì Giulia riceve una e-mail: il ticket T-0042 è "In lavorazione", con la nota del manager. Giulia apre I miei ticket e visualizza lo stato e la nota.

## Scenari alternativi

- Lunedì Giulia sbaglia la password: il sistema mostra "username o password non corretti". Al quinto errore di seguito l'account viene bloccato per 15 minuti e Giulia riceve una e-mail di avviso.
- Mentre Giulia è sul riepilogo, un altro utente occupa l'ultimo posto delle 18:00, alla conferma il sistema avvisa Giulia e le mostra di nuovo gli slot liberi.
- Nella fascia scelta non ci sono slot liberi: il sistema propone gli slot più vicini.
- Giulia nega a Google l'accesso al calendario: il sistema mostra "Google Calendar non collegato" e le prenotazioni restano valide.
- Giulia allega una foto da 8 MB: il sistema rifiuta il file e mostra "Formato non valido o file troppo grande (JPG o PNG, massimo 5 MB)".
- Giulia invia un suggerimento ("Più orari serali per Total Body") con priorità Verde: per un suggerimento la foto è facoltativa.

# 2 Casi d'Uso

## *UC1: Consultazione dei servizi e registrazione*

**Attore:** Visitatore

**Entry condition:** Il visitatore si trova sulla homepage di SSP e non è autenticato.

**Flusso di eventi:**
1. Il visitatore seleziona la sezione "Corsi".
2. Il sistema mostra l'elenco dei corsi attivi con giorni, orari e posti liberi.
3. Il visitatore filtra per categoria (opzionale) e seleziona un corso.
4. Il sistema mostra il dettaglio del corso: descrizione, giorni, orari, istruttore e posti liberi.
5. Il visitatore seleziona "Iscriviti".
6. Il sistema chiede di autenticarsi o di registrarsi e il visitatore sceglie "Registrati".
7. Il sistema mostra il modulo di registrazione e l'informativa sulla privacy.
8. Il visitatore inserisce nome, cognome, data di nascita, email e password, accetta l'informativa e conferma.
9. Il sistema controlla i dati, verifica che l'e-mail non sia già registrata e che la persona non risulti radiata.
10. Il sistema crea l'account, invia una e-mail di benvenuto e riporta il nuovo utente alla pagina del corso scelto

**Exit condition:** L'account è creato; il visitatore ora è un utente autenticato e si trova sulla pagina del corso.

**Flussi alternativi / Eccezioni:**
Se al punto 4 il visitatore non vuole iscriversi, il caso d'uso termina con la sola consultazione.

Se al punto 9 i dati non sono validi, l'e-mail è già registrata, la persona è radiata o l'informativa non è accettata, verrà eseguito il caso d'uso UC 1.1 Registrazione non riuscita.

## *UC1.1: Registrazione non riuscita*

**Attore:** Visitatore

**Entry condition:** Il visitatore ha inviato dati di registrazione che il sistema non accetta

**Flusso di eventi:**
1. Il sistema non crea l'account.
2. Il sistema mostra il motivo: campo non valido (evidenziato), "Questa e-mail è già registrata" (con il collegamento all'autenticazione), "Non è possibile registrarsi: rivolgersi alla segreteria" (persona radiata) oppure "Per registrarti devi accettare l'informativa".
3. Il sistema ripresenta il modulo con i dati già inseriti.

**Exit condition:** Il visitatore si trova sul modulo di registrazione o sulla schermata di autenticazione

## *UC2: Autenticazione e uscita dal sistema*

**Attore:** Utente, Medico, Segreteria, Responsabile corso, Manager

**Entry condition:** L'attore si trova sulla schermata di autenticazione di SSP.

**Flusso di eventi:**
1. L'attore inserisce username (e-mail) e password e li invia al sistema
2. Il sistema controlla le credenziali e il controllo ha esito positivo
3. Il sistema riconosce il ruolo e reindirizza l'attore alla sua area: area personale (Utente), Infermeria (Medico), Segreteria, Area Professionale (Responsabile corso), Area Management (Manager)
4. Al termine del lavoro l'attore seleziona "Esci"
5. Il sistema chiude la sessione e mostra la home page

**Exit condition:** L'attore è uscito dal sistema e si trova sulla home page

**Flussi alternativi / Eccezioni:**
Se al punto 2 le credenziali non sono corrette, verrà eseguito il caso d'uso UC 2.1 Autenticazione fallita.

Se l'attore arriva da un link ricevuto via e-mail, al punto 3 il sistema lo porta direttamente alla pagina del link.

## *UC2.1: Autenticazione fallita*

**Attore:** Utente, Medico, Segreteria, Responsabile corso, Manager

**Entry condition:** L'attore ha inserito credenziali non corrette

**Flusso di eventi:**
1. Il sistema mostra il messaggio "username o password non corretti" e ripresenta la schermata di autenticazione
2. Se è il quinto tentativo errato di seguito, il sistema blocca l'account per 15 minuti, mostra il messaggio "Account bloccato per 15 minuti" e invia una e-mail di avviso

**Exit condition:** L'attore si trova sulla schermata di autenticazione; l'account è bloccato se ha raggiunto i cinque tentativi.

## *UC3: Iscrizione a un corso e prenotazione di un allenamento*

**Attore:** Utente

**Entry condition:** L'utente è autenticato e si trova nella sua area personale

**Flusso di eventi:**
1. L'utente seleziona Prenota allenamento
2. Il sistema mostra i corsi a cui l'utente è iscritto
3. L'utente sceglie il corso, il giorno e la fascia oraria (proposta in automatico dalla fascia preferita del profilo)
4. Il sistema mostra gli slot della fascia con i posti liberi
5. L'utente sceglie uno slot libero
6. Il sistema mostra il riepilogo: corso, data, orario, istruttore
7. L'utente conferma
8. Il sistema verifica che lo slot abbia ancora posti, registra la prenotazione e riduce i posti liberi
9. Il sistema invia la e-mail di conferma e, se l'agenda è collegata, aggiunge l'evento a Google Calendar

**Exit condition:** La prenotazione è registrata e l'utente visualizza la conferma.

**Flussi alternativi / Eccezioni:**
Se al punto 2 l'utente non è iscritto al corso che cerca, seleziona il corso dal catalogo e seleziona Iscriviti: il sistema registra l'iscrizione, invia una e-mail di conferma e il flusso riprende dal punto 3.

Se al punto 4 nella fascia non ci sono slot liberi, verrà eseguito il caso d'uso UC 3.1 Nessuno slot disponibile.

Se al punto 8 lo slot si è riempito nel frattempo, verrà eseguito il caso d'uso UC 3.2 Slot esaurito.

## *UC3.1: Nessuno slot disponibile*

**Attore:** Utente

**Entry condition:** L'utente ha scelto una fascia oraria senza slot liberi

**Flusso di eventi:**
1. Il sistema mostra il messaggio "Nessuno slot libero in questa fascia"
2. Il sistema propone gli slot liberi più vicini alla fascia scelta

**Exit condition:** L'utente visualizza gli slot alternativi o sceglie un'altra fascia

## *UC3.2: Slot esaurito*

**Attore:** Utente

**Entry condition:** L'utente ha confermato una prenotazione su uno slot che nel frattempo è diventato completo

**Flusso di eventi:**
1. Il sistema non registra la prenotazione
2. Il sistema mostra il messaggio "Lo slot scelto non è più disponibile"
3. Il sistema mostra di nuovo gli slot liberi della fascia

**Exit condition:** L'utente si trova sulla scelta dello slot

## *UC4: Gestione delle proprie prenotazioni e visite*

**Attore:** Utente

**Entry condition:** L'utente è autenticato e si trova nella sua area personale

**Flusso di eventi:**
1. L'utente seleziona "Le mie prenotazioni"
2. Il sistema mostra prenotazioni e visite, divise in future e passate, con data, ora, servizio e stato (confermata, da confermare, annullata)
3. L'utente seleziona una prenotazione futura e seleziona Annulla
4. Il sistema chiede di confermare la scelta e l'utente conferma
5. Il sistema annulla la prenotazione, rende di nuovo disponibile il posto, invia la e-mail di annullamento e aggiorna Google Calendar
6. L'utente seleziona una visita "da confermare" (fissata dal medico fuori dalla sua fascia oraria)
7. Il sistema mostra data, ora, medico e motivo
8. L'utente seleziona Conferma
9. Il sistema passa la visita a "confermata", aggiorna il colore nel calendario del medico e lo avvisa via e-mail

**Exit condition:** Le modifiche sono salvate e l'utente visualizza l'elenco aggiornato

**Flussi alternativi / Eccezioni:**
Se al punto 2 l'utente non ha prenotazioni, il sistema mostra "Nessuna prenotazione" e propone il catalogo dei corsi.

Al passo 4 l'utente sceglie di non confermare: la prenotazione resta attiva.

Se al punto 8 l'utente seleziona Rifiuta, il sistema chiede conferma, annulla la visita, libera l'orario e avvisa il medico.

Se l'utente arriva al punto 6 dal link nella e-mail del medico, prima si autentica (UC 2).

## *UC5: Prenotazione di una visita medica*

**Attore:** Utente

**Entry condition:** L'utente è autenticato e si trova nella sua area personale

**Flusso di eventi:**
1. L'utente seleziona Prenota visita
2. Il sistema mostra un calendario con i giorni e gli orari liberi del medico
3. L'utente sceglie giorno e orario e inserisce il motivo della visita
4. Il sistema mostra il riepilogo e l'utente conferma
5. Il sistema verifica che l'orario sia ancora libero e registra la visita come "confermata"
6. Il sistema invia la conferma all'utente e una notifica al medico

**Exit condition:** La visita è registrata e compare tra le prenotazioni dell'utente.

**Flussi alternativi / Eccezioni:**
Se al punto 5 l'orario è stato occupato nel frattempo, il sistema non registra la visita, mostra un messaggio di errore e ripresenta gli orari liberi.

## *UC6: Gestione del profilo e dell'agenda digitale*

**Attore:** Utente

**Entry condition:** L'utente è autenticato e si trova nella sezione Profilo

**Flusso di eventi:**
1. Il sistema mostra dati personali, fascia oraria preferita, stato del collegamento a Google Calendar e opzioni sulla privacy
2. L'utente modifica e-mail, telefono o fascia oraria preferita e seleziona Salva
3. Il sistema controlla i dati e li salva
4. L'utente seleziona Collega Google Calendar
5. Il sistema reindirizza l'utente alla pagina di autorizzazione di Google e l'utente autorizza l'accesso
6. Il sistema riceve l'autorizzazione, salva il collegamento e aggiunge al calendario le prenotazioni confermate future

**Exit condition:** Profilo e collegamento all'agenda sono aggiornati e l'utente si trova nella sezione Profilo.

**Flussi alternativi / Eccezioni:**
Se al punto 3 un dato non è valido, il sistema evidenzia il campo e ripresenta il modulo.

Se al punto 2 l'utente seleziona Cambia password, il sistema chiede la password attuale prima di salvare quella nuova.

Se al punto 4 l'agenda è già collegata, l'utente può selezionare Scollega e il sistema rimuove l'autorizzazione.

Se al punto 5 l'utente nega l'autorizzazione, il sistema mostra "Google Calendar non collegato" e riporta l'utente al profilo.

Se l'utente seleziona Cancella account, il sistema chiede conferma, cancella i dati personali (GDPR), annulla le prenotazioni future e chiude la sessione.

## *UC7: Invio e monitoraggio di un ticket*

**Attore:** Utente, Medico, Segreteria, Responsabile corso

**Entry condition:** L'attore è autenticato e si trova nella sezione Assistenza

**Flusso di eventi:**
1. L'attore seleziona "Nuovo ticket"
2. Il sistema mostra il modulo con i campi: tipo (Segnalazione o Suggerimento), oggetto, descrizione, priorità e immagine
3. L'attore sceglie il tipo "Segnalazione", inserisce l'oggetto (massimo 100 caratteri) e la descrizione (massimo 1000 caratteri)
4. L'attore sceglie la priorità: Rossa (alta), Gialla (media) o Verde (bassa)
5. L'attore allega la foto dell'attrezzo o dell'apparecchiatura rotta e il sistema ne mostra l'anteprima
6. L'attore seleziona Invia
7. Il sistema controlla i campi e verifica che l'immagine sia JPG o PNG e non superi i 5 MB
8. Il sistema salva il ticket con un numero progressivo e lo stato "Aperto", invia la conferma all'attore e una notifica al manager
9. In seguito l'attore seleziona "I miei ticket"
10. Il sistema mostra i suoi ticket con numero, oggetto, bollino di priorità, stato (Aperto, In lavorazione, Chiuso) e le note del manager

**Exit condition:** Il ticket è salvato e l'attore ne visualizza lo stato.

**Flussi alternativi / Eccezioni:**
Se al punto 3 l'attore sceglie il tipo ""Suggerimento", l'immagine è facoltativa e il punto 5 si può saltare.

Se al punto 7 la segnalazione non ha un'immagine, o l'immagine non è JPG/PNG o supera i 5 MB, verrà eseguito il caso d'uso UC 7.1 Immagine non valida.

Se al punto 7 oggetto, descrizione o priorità mancano, il sistema evidenzia i campi e ripresenta il modulo con i dati inseriti.

Al passo 6 l'attore sceglie di annullare l'operazione: il ticket non viene salvato.

## *UC7.1: Immagine non valida*

**Attore:** Utente, Medico, Segreteria, Responsabile corso

**Entry condition:** L'attore ha inviato una segnalazione senza immagine, o con un file non JPG/PNG o più grande di 5 MB

**Flusso di eventi:**
1. Il sistema non salva il ticket
2. Il sistema mostra il messaggio "Per una segnalazione è obbligatorio allegare una foto (JPG o PNG, massimo 5 MB)"
3. Il sistema ripresenta il modulo con i dati già inseriti e il campo immagine evidenziato

**Exit condition:** L'attore si trova sul modulo del ticket.