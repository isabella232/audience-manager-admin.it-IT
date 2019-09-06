---
description: Elementi da incoraggiare i clienti a sapere quando lavorano con le API di Audience Manager.
seo-description: Elementi da incoraggiare i clienti a sapere quando lavorano con le API di Audience Manager.
seo-title: Requisiti API e Recommendations
title: Requisiti API e Recommendations
uuid: eba 9 cf 92-f 0 c 8-4394-8532-0 de 9 a 2 e 7 b 103
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Requisiti API e Recommendations {#api-requirements-and-recommendations}

Elementi da incoraggiare i clienti a capire quando lavorano con Audience Manager [!DNL API].

## Requisiti {#requirements}

Quando lavorate con [!DNL Audience Manager][!DNL API] il codice, tenete presente quanto segue:

* **Parametri di richiesta:** Tutti i parametri di richiesta sono obbligatori, se non diversamente specificato.
* **[!DNL JSON]tipo di contenuto:** Specificate `content-type: application/json`*e* `accept: application/json` nel codice.

* **Richieste e risposte:** Invia richieste come oggetto formattato [!DNL JSON] correttamente. [!DNL Audience Manager] risponde con [!DNL JSON] dati formattati. Le risposte al server possono contenere dati richiesti, un codice di stato o entrambi.

* **Accesso:** [!DNL Audience Manager] Il vostro consulente fornirà un ID client e una chiave che vi consentirà di [!DNL API] effettuare richieste.

* **Documentazione ed esempi di codice:** Il testo *in corsivo* rappresenta una variabile che viene fornita o passata durante la creazione o la ricezione [!DNL API] di dati. Sostituire *il testo in corsivo* con codice, parametri o altre informazioni richieste.

## Recommendations: Creare un utente API generico {#recommendations}

Consigliamo di creare un account utente tecnico separato per lavorare con Audience Manager [!DNL API]. Si tratta di un account generico non collegato o associato a un utente specifico nell'organizzazione del client. Questo tipo di [!DNL API] account utente consente di ottenere 2 elementi:

* Identifica quale servizio chiama il servizio [!DNL API] (ad es., chiama da un'app client che utilizza i nostri [!DNL API]s o che effettua modifiche in massa).
* Accesso ininterrotto agli [!DNL API]s. Un account associato a un dipendente specifico può essere eliminato quando esce dalla società. In questo modo i clienti non potranno lavorare con il [!DNL API] codice disponibile. Un account generico non legato a un particolare dipendente contribuisce a evitare questo problema.

Come esempio o utilizzo di questo tipo di account, diciamo che i clienti desiderano cambiare molti segmenti contemporaneamente con strumenti di gestione [di massa](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html). A tal fine, è [!DNL API] necessario accedervi. Invece di aggiungere autorizzazioni a un utente specifico, create un account [!DNL API] utente non specifico che disponga delle credenziali, chiave e segreto appropriati per [!DNL API] effettuare chiamate. Ciò è utile anche se il cliente sviluppa le proprie applicazioni che utilizzano [!DNL Audience Manager][!DNL API]gli s.
