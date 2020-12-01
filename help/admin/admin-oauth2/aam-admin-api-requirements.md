---
description: Cose di cui dovreste incoraggiare i clienti a essere consapevoli quando lavorano con le API del Audience Manager .
seo-description: Cose di cui dovreste incoraggiare i clienti a essere consapevoli quando lavorano con le API del Audience Manager .
seo-title: Raccomandazioni e requisiti per l’utilizzo delle API
title: Raccomandazioni e requisiti per l’utilizzo delle API
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 3%

---


# Raccomandazioni e requisiti per l’utilizzo delle API {#api-requirements-and-recommendations}

Cose da incoraggiare i clienti a essere consapevoli quando lavorano con il Audience Manager  [!DNL API]s.

## Requisiti {#requirements}

Tenete presente quanto segue quando lavorate con il codice [!DNL Audience Manager] [!DNL API]:

* **Parametri della richiesta:** tutti i parametri della richiesta sono obbligatori, se non diversamente specificato.
* **[!DNL JSON]tipo di contenuto:** specifica  `content-type: application/json` ** `accept: application/json` e specifica il codice.

* **Richieste e risposte:** invia le richieste come  [!DNL JSON] oggetto formattato correttamente. [!DNL Audience Manager] risponde con dati  [!DNL JSON] formattati. Le risposte del server possono contenere i dati richiesti, un codice di stato o entrambi.

* **Accesso:** Il  [!DNL Audience Manager] consulente vi fornirà un ID cliente e una chiave che vi consentirà di effettuare  [!DNL API] richieste.

* **Documentazione ed esempi di codice:** il testo in  ** corsivo rappresenta una variabile che puoi fornire o trasmettere quando crei o ricevi  [!DNL API] dati. Sostituire il testo *in corsivo* con codice, parametri o altre informazioni necessarie.

## Recommendations: Creare un utente API generico {#recommendations}

È consigliabile creare un account utente tecnico separato per lavorare con il Audience Manager  [!DNL API]s. Si tratta di un account generico che non è associato o associato a un utente specifico nell&#39;organizzazione del cliente. Questo tipo di account utente [!DNL API] consente di eseguire due operazioni:

* Identificare quale servizio sta chiamando il [!DNL API] (ad esempio, chiamate da un&#39;app client che utilizza il nostro [!DNL API]s o da modifiche di massa).
* Fornire l&#39;accesso ininterrotto alle [!DNL API]s. Un account legato a un dipendente specifico può essere eliminato quando esce dalla società. Ciò impedirà ai clienti di utilizzare il codice [!DNL API] disponibile. Un account generico che non è legato a un particolare dipendente aiuta a evitare questo problema.

Ad esempio, per questo tipo di account, supponiamo che i clienti vogliano cambiare un sacco di segmenti alla volta con gli [Strumenti di gestione di massa](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html). A tal fine, è necessario che abbiano accesso [!DNL API]. Invece di aggiungere autorizzazioni a un utente specifico, create un account utente [!DNL API] non specifico con le credenziali, la chiave e il segreto appropriati per effettuare chiamate [!DNL API]. Questo è utile anche se il cliente sviluppa applicazioni proprie che utilizzano i [!DNL Audience Manager] [!DNL API]s.
