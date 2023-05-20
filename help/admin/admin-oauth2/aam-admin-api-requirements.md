---
description: Aspetti di cui dovresti incoraggiare i tuoi clienti a essere consapevoli quando utilizzano le API Audience Manager.
seo-description: Things you should encourage your clients to be aware of when they're working with the Audience Manager APIs.
seo-title: API Requirements and Recommendations
title: Raccomandazioni e requisiti per l’utilizzo delle API
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
exl-id: 24f90732-31a6-436d-862b-e6871d279c7a
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 2%

---

# Raccomandazioni e requisiti per l’utilizzo delle API {#api-requirements-and-recommendations}

Aspetti di cui dovresti incoraggiare i tuoi clienti a essere consapevoli quando lavorano con l’Audience Manager [!DNL API]s.

## Requisiti {#requirements}

Quando si lavora con [!DNL Audience Manager] [!DNL API] codice:

* **Parametri di richiesta:** Tutti i parametri di richiesta sono obbligatori se non specificato diversamente.
* **[!DNL JSON]tipo di contenuto:** Specifica `content-type: application/json` *e* `accept: application/json` nel codice.

* **Richieste e risposte:** Inviare richieste come formattate correttamente [!DNL JSON] oggetto. [!DNL Audience Manager] risponde con [!DNL JSON] dati formattati. Le risposte del server possono contenere i dati richiesti, un codice di stato o entrambi.

* **Accesso:** Il tuo [!DNL Audience Manager] il consulente ti fornirà un ID cliente e una chiave che ti consentano di [!DNL API] richieste.

* **Documentazione ed esempi di codice:** Testo in *corsivo* rappresenta una variabile fornita o trasmessa quando si crea o si riceve [!DNL API] dati. Sostituisci *corsivo* testo con codice, parametri o altre informazioni obbligatorie.

## Recommendations: creare un utente API generico {#recommendations}

È consigliabile creare un account utente tecnico separato per l’utilizzo dell’Audience Manager [!DNL API]s. Si tratta di un account generico non associato o associato a un utente specifico nell&#39;organizzazione del cliente. Questo tipo di [!DNL API] l’account utente consente di eseguire 2 operazioni:

* Identifica il servizio che chiama [!DNL API] (ad esempio, chiamate da un’app client che utilizzano [!DNL API]s o di apportare modifiche in blocco).
* Fornire accesso ininterrotto al [!DNL API]s. Un conto associato a uno specifico dipendente può essere cancellato quando questi lascia la società. In questo modo i clienti non potranno utilizzare [!DNL API] codice. Un account generico non legato a un dipendente specifico aiuta a evitare questo problema.

Come esempio o caso d’uso per questo tipo di account, supponiamo che i tuoi clienti vogliano cambiare molti segmenti contemporaneamente con [Strumenti di gestione in blocco](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/bulk-management-tools/bulk-management-intro.html?lang=en). Per fare questo, hanno bisogno di [!DNL API] accesso. Invece di aggiungere le autorizzazioni a un utente specifico, crea un’ [!DNL API] account utente con credenziali, chiave e segreto appropriati [!DNL API] chiamate. Questa funzione è utile anche se i clienti sviluppano applicazioni personalizzate che utilizzano [!DNL Audience Manager] [!DNL API]s.
