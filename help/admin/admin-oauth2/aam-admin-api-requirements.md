---
description: Cose che consigliate ai clienti di essere consapevoli quando lavorano con le API Audience Manager .
seo-description: Cose che consigliate ai clienti di essere consapevoli quando lavorano con le API Audience Manager .
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

Cose che devi incoraggiare i clienti a essere consapevoli quando lavorano con i Audience Manager  [!DNL API]e

## Requisiti {#requirements}

Quando lavorate con [!DNL Audience Manager] il [!DNL API] codice, tenete presente quanto segue:

* **Parametri di richiesta:** Tutti i parametri di richiesta sono obbligatori, se non diversamente specificato.
* **[!DNL JSON]tipo di contenuto:**Specificate`content-type: application/json`e *inserite*`accept: application/json`nel codice.

* **Richieste e risposte:** Invia le richieste come un [!DNL JSON] oggetto formattato correttamente. [!DNL Audience Manager] risponde con dati [!DNL JSON] formattati. Le risposte del server possono contenere i dati richiesti, un codice di stato o entrambi.

* **Accesso:** Il [!DNL Audience Manager] consulente vi fornirà un ID cliente e una chiave che vi consentirà di effettuare [!DNL API] richieste.

* **Documentazione ed esempi di codice:** Il testo in *corsivo* rappresenta una variabile fornita o passata durante la creazione o la ricezione di [!DNL API] dati. Sostituite il testo *in corsivo* con codice, parametri o altre informazioni personali.

## Recommendations: Creare un utente API generico {#recommendations}

È consigliabile creare un account utente tecnico separato per lavorare con gli Audience Manager  [!DNL API]s. Si tratta di un account generico che non è associato o associato a un utente specifico nell&#39;organizzazione del cliente. Questo tipo di account [!DNL API] utente consente di eseguire due operazioni:

* Identificare il servizio che sta chiamando [!DNL API] (ad esempio, chiamate da un&#39;app client che utilizza i nostri [!DNL API]s o da modifiche collettive).
* Fornire l&#39;accesso ininterrotto agli [!DNL API]s. Un account legato a un dipendente specifico può essere eliminato quando esce dalla società. Ciò impedirà ai clienti di utilizzare il [!DNL API] codice disponibile. Un account generico che non è legato a un particolare dipendente aiuta a evitare questo problema.

Ad esempio, per questo tipo di account, supponiamo che i clienti vogliano cambiare molti segmenti alla volta con gli strumenti [di gestione](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html)di massa. Per fare ciò, hanno bisogno di [!DNL API] accesso. Invece di aggiungere autorizzazioni a un utente specifico, create un account utente non specifico [!DNL API] con le credenziali, la chiave e il segreto appropriati per effettuare [!DNL API] le chiamate. Questo è utile anche se il cliente sviluppa le proprie applicazioni che utilizzano gli [!DNL Audience Manager] [!DNL API]s.
