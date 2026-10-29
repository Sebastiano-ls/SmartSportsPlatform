## 1. Attori

- **Manager:** gestisce i corsi e i ticket dall'Area Management.
- **Responsabile corso:** consulta prenotazioni, iscritti e variazioni dei corsi che gli sono assegnati, dall'Area Professionale.

---

## 2. Scenari

### Scenario 1 — Il responsabile del corso controlla il proprio corso

Mercoledì 4 novembre 2026 Anna Verdi, responsabile del corso di Spinning, riceve una e-mail: il manager ha spostato la lezione del venerdì dalle 19:00 alle 19:30.

Anna seleziona il link nella e-mail e si autentica su SSP con username a.verdi@gmail.com e password Spinning-2026. Il sistema mostra il dettaglio della variazione: orario precedente, nuovo orario e l'elenco dei 7 clienti la cui prenotazione è stata spostata.

Anna apre l'Area Professionale, seleziona Spinning e la data di oggi: il sistema mostra che alla lezione delle 18:00 sono prenotati 14 clienti su 20. Anna seleziona la lezione e visualizza l'elenco dei prenotati, in sola lettura. Poi apre la sezione Iscritti e visualizza i 42 iscritti al corso.

**Scenari alternativi**

- Anna inserisce una password sbagliata: il sistema mostra "username o password non corretti" e ripresenta la schermata di autenticazione.
- Anna prova a cancellare la prenotazione di un cliente: il sistema non lo permette e mostra "Le prenotazioni sono gestite dalla segreteria".

---

### Scenario 2 — Il manager gestisce corsi e ticket

Lunedì 2 novembre 2026 il manager Roberto Fontana si autentica su SSP con username r.fontana@outlook.it e password Gestione-2026 e accede all'Area Management.

**Nuovo corso.** Il manager seleziona Aggiungi corso e inserisce il nome Total Body, i giorni martedì e giovedì dalle 17:00 alle 18:00, 12 posti e la responsabile Anna Verdi, poi seleziona Salva. Il sistema controlla i dati e mostra l'anteprima del corso. Il manager conferma; il sistema pubblica il corso nel catalogo e avvisa Anna Verdi via e-mail.

**Modifica di un corso.** Mercoledì il manager seleziona Modifica accanto a Spinning e sposta la lezione del venerdì dalle 19:00 alle 19:30. Il sistema avvisa che 7 clienti sono già prenotati e chiede conferma. Il manager conferma; il sistema sposta le prenotazioni e avvisa via e-mail i 7 clienti e Anna Verdi.

**Ticket.** Giovedì il manager apre la sezione Ticket: il ticket T-0042 "Tapis roulant n. 3 non si avvia" è in cima con priorità rossa. Il manager lo apre, visualizza la foto allegata, cambia lo stato in "In lavorazione" con la nota "Tecnico chiamato per venerdì" e salva. Il sistema avvisa via e-mail l'autore del ticket.

**Scenari alternativi**

- Il manager dimentica di inserire il nome del nuovo corso: il sistema evidenzia il campo e non salva.
- Al momento di confermare la modifica di Spinning il manager annulla: il corso e le prenotazioni restano invariati.

---

## 3. Casi d'uso

### UC 1: Autenticazione

**Attori:** Manager, Responsabile corso
**Entry Condition:** L'attore si trova sulla schermata di autenticazione di SSP
**Flusso di eventi:**

1. L'attore inserisce username (e-mail) e password
2. L'attore invia i dati al sistema
3. Il sistema controlla le credenziali e il controllo ha esito positivo
4. Il sistema reindirizza l'attore alla sua area: Area Management (Manager) o Area Professionale (Responsabile corso)

**Exit Condition:** L'attore è autenticato e si trova nella sua area
**Flussi alternativi / Eccezioni:**
Se al punto 3 le credenziali non sono corrette, verrà eseguito il caso d'uso UC 1.1 Autenticazione fallita.
Se l'attore arriva da un link ricevuto via e-mail, al punto 4 il sistema lo porta direttamente alla pagina del link.

### UC 1.1: Autenticazione fallita

**Attori:** Manager, Responsabile corso
**Entry Condition:** L'attore ha provato ad autenticarsi e le credenziali non erano corrette
**Flusso di eventi:**

1. Il sistema mostra il messaggio "username o password non corretti"
2. Il sistema ripresenta la schermata di autenticazione

**Exit Condition:** L'attore si trova sulla schermata di autenticazione

### UC 2: Monitoraggio dei propri corsi

**Attore:** Responsabile corso
**Entry Condition:** Il responsabile è autenticato e si trova nell'Area Professionale
**Flusso di eventi:**

1. Il sistema mostra solo i corsi assegnati al responsabile e le variazioni recenti
2. Il responsabile seleziona una variazione
3. Il sistema mostra il dato precedente, il dato nuovo e i clienti la cui prenotazione è stata spostata
4. Il responsabile seleziona un corso e un giorno
5. Il sistema mostra le lezioni del giorno con i posti occupati
6. Il responsabile seleziona una lezione
7. Il sistema mostra l'elenco dei prenotati, in sola lettura
8. Il responsabile seleziona la sezione Iscritti
9. Il sistema mostra gli iscritti al corso

**Exit Condition:** Il responsabile visualizza variazioni, prenotazioni e iscritti dei propri corsi
**Flussi alternativi / Eccezioni:**
Se il responsabile arriva al punto 2 dal link nella e-mail di variazione, prima si autentica (UC 1).
Se al punto 7 il responsabile prova a modificare una prenotazione, il sistema non esegue l'operazione e mostra "Le prenotazioni sono gestite dalla segreteria".

### UC 3: Gestione dei corsi

**Attore:** Manager
**Entry Condition:** Il manager è autenticato e visualizza l'elenco dei corsi nell'Area Management
**Flusso di eventi:**

*Inserimento di un corso*

1. Il manager seleziona Aggiungi corso
2. Il sistema mostra il modulo di inserimento
3. Il manager inserisce nome, giorni e orari, posti per lezione e responsabile, e seleziona Salva
4. Il sistema controlla i dati e mostra l'anteprima del corso
5. Il manager conferma
6. Il sistema pubblica il corso nel catalogo e avvisa il responsabile via e-mail

*Modifica di un corso*

7. Il manager seleziona Modifica accanto a un corso e cambia giorni, orari o posti
8. Il sistema mostra quante prenotazioni sono coinvolte e chiede conferma
9. Il manager conferma
10. Il sistema salva la modifica, sposta le prenotazioni e avvisa via e-mail i clienti coinvolti e il responsabile

**Exit Condition:** Il corso è pubblicato o aggiornato e il manager visualizza l'elenco dei corsi
**Flussi alternativi / Eccezioni:**
Se al punto 4 mancano dati o i dati non sono validi, verrà eseguito il caso d'uso UC 3.1 Dati del corso non validi.
Al punto 5 o al punto 9 il manager sceglie di annullare: nessuna modifica viene salvata.

### UC 3.1: Dati del corso non validi

**Attore:** Manager
**Entry Condition:** Il manager ha salvato un corso con dati mancanti o non validi
**Flusso di eventi:**

1. Il sistema non salva il corso
2. Il sistema evidenzia i campi da correggere
3. Il sistema ripresenta il modulo con i dati già inseriti

**Exit Condition:** Il manager si trova sul modulo del corso

### UC 4: Gestione dei ticket

**Attore:** Manager
**Entry Condition:** Il manager è autenticato e si trova nell'Area Management
**Flusso di eventi:**

1. Il manager seleziona la sezione Ticket
2. Il sistema mostra i ticket ordinati per priorità (rossa, gialla, verde)
3. Il manager seleziona un ticket
4. Il sistema mostra oggetto, descrizione, immagine e autore
5. Il manager cambia lo stato (In lavorazione o Chiuso), scrive una nota e seleziona Salva
6. Il sistema salva stato e nota e avvisa l'autore via e-mail

**Exit Condition:** Il ticket è aggiornato e il manager visualizza l'elenco dei ticket
**Flussi alternativi / Eccezioni:**
Al punto 5 il manager sceglie di annullare: lo stato del ticket resta invariato.

---

## 4. Corrispondenza tra scenari e casi d'uso

- **Scenario 1:** UC 1, UC 2; scenari alternativi UC 1.1 e il flusso alternativo di UC 2.
- **Scenario 2:** UC 1, UC 3, UC 4; scenari alternativi UC 3.1 e l'annullamento in UC 3.
