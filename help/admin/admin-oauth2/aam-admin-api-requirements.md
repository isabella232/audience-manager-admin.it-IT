---
description: Cose di cui devi incoraggiare i clienti a essere consapevoli quando lavorano con le API di Audience Manager.
seo-description: Things you should encourage your clients to be aware of when they're working with the Audience Manager APIs.
seo-title: API Requirements and Recommendations
title: Raccomandazioni e requisiti per l’utilizzo delle API
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
exl-id: 24f90732-31a6-436d-862b-e6871d279c7a
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 2%

---

# Raccomandazioni e requisiti per l’utilizzo delle API {#api-requirements-and-recommendations}

Cose di cui è necessario incoraggiare i clienti a essere consapevoli quando lavorano con gli Audienci Manager [!DNL API]s.

## Requisiti {#requirements}

Quando lavori con il codice [!DNL Audience Manager] [!DNL API], tieni presente quanto segue:

* **Parametri di richiesta:** tutti i parametri di richiesta sono richiesti, se non diversamente specificato.
* **[!DNL JSON]tipo di contenuto:** specifica  `content-type: application/json` ** `accept: application/json` e nel codice.

* **Richieste e risposte:** invia richieste come  [!DNL JSON] oggetto formattato correttamente. [!DNL Audience Manager] risponde con dati  [!DNL JSON] formattati. Le risposte del server possono contenere dati richiesti, un codice di stato o entrambi.

* **Accesso:** il tuo  [!DNL Audience Manager] consulente ti fornirà un ID cliente e una chiave che ti permetterà di effettuare  [!DNL API] richieste.

* **Documentazione ed esempi di codice:** il testo in  ** corsivo rappresenta una variabile fornita o passata durante la creazione o la ricezione  [!DNL API] dei dati. Sostituisci il testo *in corsivo* con codice, parametri o altre informazioni richieste.

## Recommendations: Creare un utente API generico {#recommendations}

È consigliabile creare un account utente tecnico separato per lavorare con gli Audienci Manager [!DNL API]s. Si tratta di un account generico che non è associato o associato a un utente specifico nell&#39;organizzazione del cliente. Questo tipo di account utente [!DNL API] consente di eseguire 2 operazioni:

* Identifica quale servizio sta chiamando il [!DNL API] (ad esempio, chiamate da un&#39;app client che utilizza i nostri [!DNL API]s o da modifiche in blocco).
* Fornire l&#39;accesso ininterrotto ai [!DNL API]s. Un account associato a un dipendente specifico può essere cancellato quando lascia l&#39;azienda. Questo impedirà ai tuoi clienti di lavorare con il codice [!DNL API] disponibile. Un account generico non legato a un particolare dipendente aiuta a evitare questo problema.

Ad esempio, per questo tipo di account, supponiamo che i clienti desiderino cambiare molti segmenti contemporaneamente con gli [Strumenti di gestione in blocco](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html). A questo scopo, devono avere accesso a [!DNL API] . Invece di aggiungere autorizzazioni a un utente specifico, crea un account utente [!DNL API] non specifico che disponga delle credenziali, della chiave e del segreto appropriati per effettuare chiamate [!DNL API]. Questo è utile anche se i client sviluppano applicazioni personalizzate che utilizzano i [!DNL Audience Manager] [!DNL API]s.
