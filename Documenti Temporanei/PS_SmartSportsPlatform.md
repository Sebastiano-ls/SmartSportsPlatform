# 4. Requisiti non funzionali (Salvatore Moccia)

**Progetto:** Smart Sports Platform (SSP)

Ogni requisito ha un codice e una priorità. Qui ci sono solo i requisiti con priorità Alta. I numeri sono proposte del gruppo, da confermare con il cliente.

---

## 4.1 Usabilità

L'usabilità è divisa per utente: Cliente e Dipendente. In fondo ci sono i requisiti comuni a entrambi.

### 4.1.1 Usabilità — Cliente

- **RNF-U-C1 (Alta):** Un cliente che sa usare smartphone e browser deve poter usare il sistema senza leggere un manuale.
- **RNF-U-C2 (Alta):** Dalla schermata principale, il cliente vede servizi, orari e disponibilità in al massimo tre passi.
- **RNF-U-C3 (Alta):** Il cliente prenota un servizio in al massimo cinque passaggi, con un riepilogo e una conferma finale.

### 4.1.2 Usabilità — Dipendente

- **RNF-U-D1 (Alta):** Il dipendente svolge da solo le operazioni di ogni giorno: prenotazioni in sede, calendario del giorno, comunicazioni standard.

### 4.1.3 Usabilità — Comuni

- **RNF-U-T1 (Alta):** Il sistema è in italiano, con date, orari e valute in formato italiano.
- **RNF-U-T2 (Alta):** Il sistema funziona su smartphone, tablet e computer, senza scorrimento laterale da 360 px in su.

---

## 4.2 Affidabilità

- **RNF-A1 (Alta):** Il sistema è disponibile sempre, salvo manutenzioni di notte o guasti.
- **RNF-A2 (Alta):** Una prenotazione confermata non si perde se il server o il database hanno un guasto. Ogni operazione sul database va a buon fine del tutto o non viene salvata.
- **RNF-A3 (Alta):** Uno stesso orario di un servizio non può essere prenotato più volte del limite previsto, anche con richieste contemporanee.

### 4.2.1 Sicurezza

- **RNF-R7 (Alta):** Per entrare serve un account personale (e-mail e password). Le password sono sempre cifrate e mai visibili.
- **RNF-R8 (Alta):** Ogni utente vede solo ciò che gli spetta: il cliente solo i propri dati e prenotazioni, il dipendente le funzioni del centro.
- **RNF-R9 (Alta):** Tutte le comunicazioni usano HTTPS (TLS 1.2 o superiore).
- **RNF-R10 (Alta):** Dopo cinque accessi sbagliati di seguito, l'account si blocca per 15 minuti.

---

## 4.3 Prestazioni

- **RNF-P1 (Alta):** Il sistema regge almeno 100 utenti contemporanei (da confermare con il cliente).

---

## 4.4 Facilità di modifica

- **RNF-S1 (Alta):** Il sistema è diviso in tre parti separate (interfaccia, logica, database): si può cambiare una parte senza toccare le altre.

---

## 4.5 Tecnologia

- **RNF-I1 (Alta):** Il sistema ha tre livelli: client (interfaccia), server (logica) e database (dati).

---

## 4.7 Operazioni

- **RNF-O1 (Alta):** Il personale del centro può fare backup e ripristino seguendo una procedura scritta, senza competenze tecniche avanzate.

---

## 4.8 Installazione

- **RNF-PK1 (Alta):** Client, server e database si possono installare su tre computer diversi.

---

## 4.9 Aspetti legali

- **RNF-L1 (Alta):** I dati personali rispettano il GDPR (Reg. UE 2016/679) e il D.Lgs. 196/2003. Il cliente riceve l'informativa privacy e dà il consenso prima di registrarsi, e può vedere, correggere o cancellare i propri dati.

---

## 4.10 Vincoli

- Il sistema funziona sui browser più usati (ultime due versioni).
