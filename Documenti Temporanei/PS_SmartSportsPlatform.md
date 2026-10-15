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