
# 1. Requisiti funzionali (Giuseppe Nocerino)

## 1.1 Utente
### 1.1.1 Area Personale

- **RF-U-01:** Il sitema deve permettere di gestire il proprio profilo, prenotare servizi offerti dal centro e restare informati sulle variazioni che li riguardano.
- **RF-U-02:** Il sistema deve consentire l'accesso all'area personale solo ai clienti registrati al centro sportivo.
- **RF-U-03:** Il sitema deve consentire l'accesso all'area personale ai clienti solo dopo che essi abbiano effettuato l'autenticazione.
- **RF-U-04:** Il sistema deve mantenere lo stato di salute di ciascun utente iscritto al centro sportivo.
- **RF-U-05:** Il sistema deve tenere traccia dei corsi a cui l'utente è iscritto.

### 1.1.2 Autenticazione

- **RF-U-06:** Il sistema deve impedire ad un cliente radiato dal centro sportivo di registrarsi nuovamente alla piattaforma.
- **RF-U-07:** Il sistema deve conservare i dati inseriti al momento della registrazione in modo da poterli gestire in futuro.

### 1.1.3 Interazione con i Corsi di Allenamento

- **RF-U-08** Il sistema deve suddividere le prenotazioni in slot temporali, ciascuno con una capienza massima.
- **RF-U-09:** Il sistema deve consentire al cliente di prenotare un preciso slot solo se disponibile.
- **RF-U-10:** Il sistema deve mostrare che uno slot non è disponibile quando questo raggiunge la capienza massima.
- **RF-U-11:** Il sistema deve consentire al cliente di annullare in qualsiasi momento una propria prenotazione.
- **RF-U-12:** Il sistema deve rendere uno slot nuovamente disponibe quando questo si libera.
- **RF-U-13:** Il sistema deve consentire al cliente di consultare l’elenco di tutte le proprie prenotazioni.
- **RF-U-14:** Il sistema deve inviare una notifica all'area personale e alla casella di posta elettronica dell'utente qualora una qualsiasi informazione relativa ad una sua prenotazione subisce un cambiamento.
- **RF-U-15:** Il sistema deve consentire all'utente di prenotare un slot di un corso solamente se iscritto a tale corso.

### 1.1.5 Le Prenotazioni delle Visite Mediche

- **RF-U-16** Il sistema permette ai clienti di prenotare da soli una visita medica, scegliendo un giorno e orario disponibile

## 1.2 Infermeria
### 1.2.1 Servizio di Infermeria

- **RF-INF-01:**Il sistema deve consentire l'accesso all'area dedicata all'infermeria solamente ai medici del centro sportivo.
- **RF-INF-02:**Il sistema deve permettere ai medici di gestire le visite mediche dei clienti.
- **RF-INF-03:**Il sistema deve proibire l'assegnazione di una visita in un giorno o orario già occupati da un’altra visita medica.

### 1.2.2 Il Medico
- **RF-INF-04:** Il sistema deve permettere al medico di visualizzare l'elenco di tutti i clienti iscritti al centro sportivo.
- **RF-INF-05:** Il sistema deve permettere al medico di visualizzare lo stato di salute del cliente(infortuato, guarito, in guarigione).
- **RF-INF-06:** Il sistema deve consentire al medico di aggiornare lo stato del cliente.
- **RF-INF-07:** Il sistema deve consentire al medico di visualizzare tutte le prenotazioni.
- **RF-INF-08:** Il sistema deve consentire al medico di organizzare una visita medica per conto di un cliente.
- **RF-INF-09:** Ogni volta che il cliente prenota o annulla una visita medica, il sistema invia un avviso al medico sulla sua e-mail registrata.

## 1.3 Segreteria
### 1.3.1 Servizio di Segreteria
- **RF-S-01:** Il sistema deve consentire l'accesso all'area dedicata alla segreteria solamente agli addetti segreteria.
- **RF-S-02:** Il sistema deve permettere agli addetti segreteria di visualizzare i clienti iscritti ai corsi.
- **RF-S-03:** Il sistema deve permettere agli addetti segreteria di modificare i dati di un cliente esistente.
- **RF-S-04:** Il sistema deve permettere agli addetti segreteria di modificare le prenotazioni dei clienti.
- **RF-S-05:** Il sistema deve tenere traccia dell'adetto segreteria che effettua un'operazione all'interno del sistema.

## 1.4 Responsabile del Corso
### 1.4.1 Area Professionale
- **RF-RS-01:** Il sistema deve consentire l'accesso all'area personale solamente ai responsabili del corso.
- **RF-RS-02**  Il sistema deve permettere ai responsabili di consultare i clienti iscritti al proprio corso.
- **RF-RS-03:** Il sistema deve permettere ai responsabili di consultare le prenotazioni dei clienti iscritti.
- **RF-RS-04:** Il sistema deve notificare via email i responsabili ad ogni variazione del corso di loro pertinenza.
- **RF-RS-05:** Il sistema non deve permettere al responsabile di modificare le prenotazioni dei clienti.
- **RF-RS-06:** Il sistema deve tenere traccia dei corsi che un responsabile gestisce.

### 1.4.2 Multi-utenza
- **RF-RS-07:**Il sistema deve mostrare, al responsabile del corso, soltanto i clienti del corso a esso associato, e non quelli degli altri corsi.

## 1.5 Manager
### 1.5.1 Area Management
- **RF-MG-01:** Il sistema deve consentire l'accesso all'Area Management solamente al manager generale del centro.
- **RF-MG-02:** Il sistema deve permettere al manager di visualizzare ed aggiornare i servizi offerti.
- **RF-MG-03:** Il sistema deve permettere al manager di visualizzare ed aggiornare i clienti.
- **RF-MG-04:** Il sistema deve permettere al manager di visualizzare ed aggiornare i dipendenti.


# 2. Requisiti non funzionali (Salvatore Moccia)

Ogni requisito ha un codice e una priorità. Qui ci sono solo i requisiti con priorità Alta. I numeri sono proposte del gruppo, da confermare con il cliente.

---

## 2.1 Usabilità

L'usabilità è divisa per utente: Cliente e Dipendente. In fondo ci sono i requisiti comuni a entrambi.

### 2.1.1 Usabilità — Cliente

- **RNF-U-C1:** Un cliente che sa usare smartphone e browser deve poter usare il sistema senza leggere un manuale.
- **RNF-U-C2:** Dalla schermata principale, il cliente vede servizi, orari e disponibilità in al massimo tre passi.
- **RNF-U-C3:** Il cliente prenota un servizio in al massimo cinque passaggi, con un riepilogo e una conferma finale.

### 2.1.2 Usabilità — Dipendente

- **RNF-U-D1:** Il dipendente svolge da solo le operazioni di ogni giorno: prenotazioni in sede, calendario del giorno, comunicazioni standard.

### 2.1.3 Usabilità — Comuni

- **RNF-U-T1:** Il sistema è in italiano, con date, orari e valute in formato italiano.
- **RNF-U-T2:** Il sistema funziona su smartphone, tablet e computer, senza scorrimento laterale da 360 px in su.

---

## 2.2 Affidabilità

- **RNF-A1:** Il sistema è disponibile sempre, salvo manutenzioni di notte o guasti.
- **RNF-A2:** Una prenotazione confermata non si perde se il server o il database hanno un guasto. Ogni operazione sul database va a buon fine del tutto o non viene salvata.
- **RNF-A3:** Uno stesso orario di un servizio non può essere prenotato più volte del limite previsto, anche con richieste contemporanee.

### 2.2.1 Sicurezza

- **RNF-R7:** Per entrare serve un account personale (e-mail e password). Le password sono sempre cifrate e mai visibili.
- **RNF-R8:** Ogni utente vede solo ciò che gli spetta: il cliente solo i propri dati e prenotazioni, il dipendente le funzioni del centro.
- **RNF-R9:** Tutte le comunicazioni usano HTTPS (TLS 1.2 o superiore).
- **RNF-R10:** Dopo cinque accessi sbagliati di seguito, l'account si blocca per 15 minuti.

---

## 2.3 Prestazioni

- **RNF-P1:** Il sistema regge almeno 100 utenti contemporanei (da confermare con il cliente).

---

## 2.4 Facilità di modifica

- **RNF-S1:** Il sistema è diviso in tre parti separate (interfaccia, logica, database): si può cambiare una parte senza toccare le altre.

---

## 2.5 Tecnologia

- **RNF-I1:** Il sistema ha tre livelli: client (interfaccia), server (logica) e database (dati).

---

## 2.7 Operazioni

- **RNF-O1:** Il personale del centro può fare backup e ripristino seguendo una procedura scritta, senza competenze tecniche avanzate.

---

## 2.8 Installazione

- **RNF-PK1:** Client, server e database si possono installare su tre computer diversi.

---

## 2.9 Aspetti legali

- **RNF-L1:** I dati personali rispettano il GDPR (Reg. UE 2016/679) e il D.Lgs. 196/2003. Il cliente riceve l'informativa privacy e dà il consenso prima di registrarsi, e può vedere, correggere o cancellare i propri dati.

---


# 3. Vincoli (Sebastiano Lo Sapio)

Ogni requisito ha un codice e una priorità. Qui ci sono solo i requisiti con priorità Alta. I numeri sono proposte del gruppo, da confermare con il cliente.

---

## 3.1 Accessibilità
- Il sistema funziona sui browser più usati (ultime due versioni).

---

## 3.2 Interfacce con altri sistemi

- **V-IF1 — Google Calendar:** Le prenotazioni confermate possono essere sincronizzate con il Google Calendar del cliente tramite Google Calendar API, previa autorizzazione esplicita dell'utente (OAuth 2.0). Modifiche o annullamenti in SSP aggiornano l'evento entro 5 minuti.

- **V-IF2 — Posta elettronica:** Il sistema genera messaggi standard pre-formulati (conferma, promemoria, annullamento, comunicazione del centro) a partire da modelli modificabili, compilati automaticamente con i dati della prenotazione. Il dipendente può inoltrare il messaggio pre-formulato al destinatario con una sola azione; le conferme sono inviate automaticamente.

---

## 3.2 Pianificazione delle scadenze

- **Problem Statement** : 15/10/2026
- **Requisiti e Casi d'Uso** : 17/10/2026
- **Requirement Analysis Document** : 11/11/2026
- **System Design Document** : 24/11/2026
- **Object Design Document (Parziale)** : 15/12/2026
- **Testing** : 17/12/2026