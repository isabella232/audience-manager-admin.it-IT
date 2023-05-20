---
description: Utilizza la pagina Società nello strumento di amministrazione Audience Manager per creare una nuova società.
seo-description: Use the Companies page in the Audience Manager Admin tool to create a new company.
seo-title: Create a Company Profile
title: Creare un profilo società
uuid: 55de18f8-883d-43fe-b37f-e8805bb92f7a
exl-id: 80bb8a89-0207-4645-ac42-e73cd10561de
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 2%

---

# Creare un profilo società {#create-a-company-profile}

Utilizza il [!UICONTROL Companies] nello strumento di amministrazione Audience Manager per creare una nuova società.

<!-- t_create_company.xml -->

>[!NOTE]
>
>È necessario disporre di **[!UICONTROL DEXADMIN]** ruolo per creare nuove società.

1. Clic **[!UICONTROL Companies]** > **[!UICONTROL Add Company]**.
1. Compila i campi:

   * **[!UICONTROL Name]**: (Obbligatorio) specifica il nome dell’azienda.
   * **[!UICONTROL Description]**: (Obbligatorio) fornisci informazioni descrittive sull’azienda, ad esempio il settore o la sua ragione sociale completa.
   * **[!UICONTROL Subdomain]**: (Obbligatorio) specifica il sottodominio della società. Il testo immesso è il sottodominio della chiamata dell’evento. Questo non può essere modificato. Deve essere una stringa di [!DNL URL]-caratteri validi.

      Ad esempio, se la società è stata denominata [!DNL AcmeCorp], il sottodominio sarà [!DNL acmecorp].

      Audience Manager utilizza il sottodominio per [!UICONTROL Data Collection Server] (DCS) Nell&#39;esempio precedente, se l&#39;azienda è piena [!DNL URL] in [!UICONTROL DCS] sarebbe [!DNL acmecorp.demdex.net].

   * **[!UICONTROL Lifecyle]**: specifica la fase desiderata per l’azienda:
      * **[!UICONTROL Active]**: specifica che la società sarà un client di Audience Manager attivo. Un [!UICONTROL Active] per account si intende un cliente pagante, non solo per consulenza, ma per SKU di Audience Manager.
      * **[!UICONTROL Demo]**: specifica che la società sarà solo a scopo dimostrativo. I dati di reporting verranno contraffatti automaticamente.
      * **[!UICONTROL Prospect]**: specifica che la società è un potenziale cliente Audience Manager, ad esempio una società a cui viene dato un [!DNL POC] o una configurazione account per una demo vendite.
      * **[!UICONTROL Test]**: specifica che la società verrà utilizzata solo per test interni.
   * **[!UICONTROL Account Types]**: specifica il set completo dei tipi di account per questa società. Nessun tipo di account si esclude a vicenda con altri tipi.
      * **[!UICONTROL Full AAM]**: specifica che l’azienda avrà un account Adobe Audience Manager completo e che gli utenti avranno accesso.
      * **[!UICONTROL MMP]**: specifica che l’azienda è stata abilitata per utilizzare il [!UICONTROL Master Marketing Profile] ([!UICONTROL MMP]). Il [!UICONTROL MMP] consente di condividere i tipi di pubblico in tutto l’Experience Cloud utilizzando [!UICONTROL Experience Cloud ID] ([!DNL MCID]) che viene assegnato a ogni visitatore e quindi utilizzato da Audience Manager. Se si seleziona questo tipo di account, [!UICONTROL Experience Cloud ID Service] viene selezionato automaticamente.

         Per ulteriori informazioni, consulta [Tipi di pubblico di Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=en).
   * **[!UICONTROL Data Source]**: specifica che l’azienda è un provider di dati di terze parti all’interno di Audience Manager.
   * **[!UICONTROL Targeting Partner]**: specifica che l’azienda funge da piattaforma di targeting, ad Audience Manager per i clienti.
   * **[!UICONTROL Visitor ID Service]**: specifica che l’azienda è stata abilitata per utilizzare il [!UICONTROL Experience Cloud Visitor ID Service].

      Il [!UICONTROL Experience Cloud Visitor ID Service] fornisce un ID visitatore universale per tutte le soluzioni Experience Cloud. Per ulteriori informazioni, vedere [Guida utente di Experience Cloud Visitor ID Service](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=en).

   * **[!UICONTROL Agency]**: specifica che l’azienda avrà un [!UICONTROL Agency] account.



1. Clic **[!UICONTROL Create]**. Continua con le istruzioni in [Modificare un profilo società](../companies/admin-manage-company-profiles.md#edit-company-profile).

   ![Risultato passaggio](assets/add_company.png)

## Modificare un profilo società {#edit-company-profile}

Modifica il profilo di un’azienda, compresi nome, descrizione, sottodominio, ciclo di vita e altro ancora.

<!-- t_edit_company_profile.xml -->

1. Clic **[!UICONTROL Companies]**, quindi individuare e fare clic sulla società desiderata per visualizzare [!UICONTROL Profile] pagina.

   Utilizza il [!UICONTROL Search] o i controlli di impaginazione nella parte inferiore dell&#39;elenco per individuare la società desiderata. Puoi ordinare ogni colonna in ordine crescente o decrescente facendo clic sull’intestazione della colonna desiderata.

   ![Risultato passaggio](assets/profile_company.png)

1. Modifica i campi come necessario:

   * **[!UICONTROL Name]**: modifica il nome dell’azienda. Questo campo è obbligatorio.
   * **[!UICONTROL Description]**: modifica la descrizione dell’azienda. Questo campo è obbligatorio.
   * **[!UICONTROL Subdomain]**: (Obbligatorio) specifica il sottodominio della società. Il testo immesso è il sottodominio della chiamata dell’evento. Questo non può essere modificato. Deve essere una stringa di [!DNL URL]-caratteri validi.

      Ad esempio, se la società è stata denominata [!DNL AcmeCorp], il sottodominio sarà [!DNL acmecorp].

      Audience Manager utilizza il sottodominio per [!UICONTROL Data Collection Server] (DCS) Nell&#39;esempio precedente, se l&#39;azienda è piena [!DNL URL] in [!UICONTROL DCS] sarebbe [!DNL acmecorp.demdex.net].

   * **[!UICONTROL imsOrgld]**: ([!UICONTROL Identity Management System Organization ID]) Questo ID consente di collegare la società con Adobe Experience Cloud.
   * **[!UICONTROL Lifecyle]**: specifica la fase desiderata per l’azienda:
      * **[!UICONTROL Active]**: specifica che la società sarà un client di Audience Manager attivo. Per account attivo si intende un cliente pagante, non solo per consulenza, ma per SKU di Audience Manager.
      * **[!UICONTROL Demo]**: specifica che la società sarà solo a scopo dimostrativo. I dati di reporting verranno contraffatti automaticamente.
      * **[!UICONTROL Prospect]**: specifica che la società è un potenziale cliente Audience Manager, ad esempio una società a cui viene dato un [!DNL POC] o una configurazione account per una demo vendite.
      * **[!UICONTROL Test]**: specifica che la società verrà utilizzata solo per test interni.
   * **[!UICONTROL Account Types]**: specifica il set completo dei tipi di account per questa società. Nessun tipo di account si esclude a vicenda con altri tipi.
      * **[!UICONTROL Full AAM]**: specifica che l’azienda avrà un account Adobe Audience Manager completo e che gli utenti avranno accesso.
      * **[!UICONTROL MMP]**: specifica che la società è stata abilitata per l’utilizzo del profilo marketing principale ([!UICONTROL MMP]).

         Se si seleziona questo tipo di account, **[!UICONTROL Visitor ID Service]** viene selezionato automaticamente.
Per ulteriori informazioni, consulta [Tipi di pubblico di Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=en).
   * **[!UICONTROL Data Source]**: specifica che l’azienda è un provider di dati di terze parti all’interno di Audience Manager.
   * **[!UICONTROL Targeting Partner]**: specifica che l’azienda funge da piattaforma di targeting, ad Audience Manager per i clienti.
   * **[!UICONTROL Visitor ID Service]**: specifica che la società è stata abilitata per utilizzare il servizio ID visitatore di Experience Cloud.

      Il servizio ID visitatore di Experience Cloud fornisce un ID visitatore universale per tutte le soluzioni Experience Cloud. Per ulteriori informazioni, vedere [Guida utente del servizio ID Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en).

   * **[!UICONTROL Agency]**: specifica che la società avrà un account Agenzia.
   * **[!UICONTROL Features]**: seleziona le opzioni desiderate:
      * **[!UICONTROL Password Expiration]**: imposta la scadenza di tutte le password utente di questa società dopo 90 giorni per aumentare la sicurezza di Audience Manager.
      * **[!UICONTROL Reporting]**: abilita la generazione di rapporti di Audience Manager per questa società.
      * **[!UICONTROL Role Based Access Controls]**: abilita i controlli dell’accesso basati sul ruolo per questa azienda. I controlli dell’accesso basati sul ruolo consentono di creare gruppi di utenti con autorizzazioni di accesso diverse. I singoli utenti all’interno di questi gruppi possono quindi accedere solo a funzioni specifiche di Audience Manager.


1. Clic **[!UICONTROL Submit Updates]**.

## Eliminare un profilo società {#delete-company-profile}

Utilizza il [!UICONTROL Companies] pagina nell’Audience Manager [!UICONTROL Admin] per eliminare una società esistente.

<!-- t_delete_company.xml -->

>[!NOTE]
>
>È necessario disporre di [!UICONTROL DEXADMIN] per eliminare le società esistenti.

1. Per eliminare una società esistente, fai clic su **[!UICONTROL Companies]**.

   ![Risultato passaggio](assets/companies.png)

1. Clic  ![](assets/icon_delete.png) nel **[!UICONTROL Actions]** della società desiderata.
1. Clic **[!UICONTROL OK]** per confermare l’eliminazione.
