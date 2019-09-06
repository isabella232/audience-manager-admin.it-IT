---
description: Utilizza la pagina Società nello strumento Amministrazione di Audience Manager per creare una nuova azienda.
seo-description: Utilizza la pagina Società nello strumento Amministrazione di Audience Manager per creare una nuova azienda.
seo-title: Creare un profilo società
title: Creare un profilo società
uuid: 55 de 18 f 8-883 d -43 fe-b 37 f-e 8805 bb 92 f 7 a
translation-type: tm+mt
source-git-commit: 71bf4cec222428686c1eab0998f66887db06da68

---


# Creare un profilo società {#create-a-company-profile}

Utilizza la [!UICONTROL Companies] pagina nello strumento Amministrazione di Audience Manager per creare una nuova società.

<!-- t_create_company.xml -->

>[!NOTE]
>
>Per creare nuove società dovete **[!UICONTROL DEXADMIN]** avere il ruolo necessario.

1. Click **[!UICONTROL Companies]** &gt; **[!UICONTROL Add Company]**.
1. Compila i campi:

   * **[!UICONTROL Name]**: (Obbligatorio) Specificate il nome della società.
   * **[!UICONTROL Description]**: (Obbligatorio) Fornisci informazioni descrittive sulla società, ad esempio un settore o il suo nome completo.
   * **[!UICONTROL Subdomain]**: (Obbligatorio) Specificate il sottodominio della società. Il testo immesso corrisponde al sottodominio della chiamata dell'evento. Questa operazione non può essere modificata. Deve essere una stringa di [!DNL URL]caratteri -validi.

      Ad esempio, se la società è stata rinominata [!DNL AcmeCorp], il sottodominio [!DNL acmecorp]sarà.

      Audience Manager usa il sottodominio per [!UICONTROL Data Collection Server]([!UICONTROL DCS]). Nell'esempio precedente, se la società [!DNL URL] è [!UICONTROL DCS] completa [!DNL acmecorp.demdex.net].

   * **[!UICONTROL Lifecyle]**: Specificate lo stage desiderato per la società:
      * **[!UICONTROL Active]**: Specifica che la società sarà un client Audience Manager attivo. Un [!UICONTROL Active] account indica un cliente pagatore, non solo per la consulenza, ma per lo SKU Audience Manager.
      * **[!UICONTROL Demo]**: Specificate che la società sarà solo a scopo dimostrativo. I dati di reporting verranno segnalati automaticamente.
      * **[!UICONTROL Prospect]**: Specifica che l'azienda è un potenziale client Audience Manager, ad esempio una società che dispone di una configurazione gratuita [!DNL POC] o di un account per una demo di vendita.
      * **[!UICONTROL Test]**: Specificate che la società sarà solo a scopo di test interno.
   * **[!UICONTROL Account Types]**: Specificate l'intero set di tipi di account per questa società. Nessun tipo di account è mutualmente esclusivo con qualsiasi altro tipo.
      * **[!UICONTROL Full AAM]**: Specifica che l'azienda avrà un account Adobe Audience Manager completo e gli utenti avranno accesso accesso.
      * **[!UICONTROL MMP]**: Specificate che la società è stata attivata per l'uso delle [!UICONTROL Master Marketing Profile] funzionalità ([!UICONTROL MMP]). L'audience [!UICONTROL MMP] può essere condivisa in Experience Cloud utilizzando un [!UICONTROL Experience Cloud ID] ([!DNL MCID]) che viene assegnato a ogni visitatore e quindi utilizzato da Audience Manager. Se selezionate questo tipo di account, viene [!UICONTROL Experience Cloud ID Service] anche selezionato automaticamente.

         Per ulteriori informazioni, consultate [Servizi di audience - Profilo marketing principale](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html).
   * **[!UICONTROL Data Source]**: Specifica che la società è un provider di dati terze parti all'interno di Audience Manager.
   * **[!UICONTROL Targeting Partner]**: Specifica che l'azienda agisce come piattaforma di targeting per i clienti di Audience Manager.
   * **[!UICONTROL Visitor ID Service]**: Specificate che la società è stata attivata [!UICONTROL Experience Cloud Visitor ID Service]per l'utilizzo.

      Fornisce [!UICONTROL Experience Cloud Visitor ID Service] un ID visitatore universale nelle soluzioni Experience Cloud. For more information, see the [Experience Cloud Visitor ID Service user guide](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-overview.html).

   * **[!UICONTROL Agency]**: Specificate che l'azienda avrà [!UICONTROL Agency] un account.



1. Fai clic su **[!UICONTROL Create]**. Continua con le istruzioni in [Modifica un profilo società](../companies/admin-manage-company-profiles.md#edit-company-profile).

   ![Risultato passaggio](assets/add_company.png)

## Modifica di un profilo società {#edit-company-profile}

Modifica il profilo di una società, incluso nome, descrizione, sottodominio, ciclo di vita e altro.

<!-- t_edit_company_profile.xml -->

1. Fate clic **[!UICONTROL Companies]**, individuate e fate clic sulla società desiderata per visualizzarne [!UICONTROL Profile] la pagina.

   Utilizzate la [!UICONTROL Search] casella o i controlli di impaginazione in fondo all'elenco per trovare la società desiderata. Potete ordinare ciascuna colonna in ordine crescente o decrescente facendo clic sull'intestazione della colonna desiderata.

   ![Risultato passaggio](assets/profile_company.png)

1. Modificate i campi in base alle necessità:

   * **[!UICONTROL Name]**: Modificate il nome della società. Questo campo è obbligatorio.
   * **[!UICONTROL Description]**: Modificare la descrizione della società. Questo campo è obbligatorio.
   * **[!UICONTROL Subdomain]**: (Obbligatorio) Specificate il sottodominio della società. Il testo immesso corrisponde al sottodominio della chiamata dell'evento. Questa operazione non può essere modificata. Deve essere una stringa di [!DNL URL]caratteri -validi.

      Ad esempio, se la società è stata rinominata [!DNL AcmeCorp], il sottodominio [!DNL acmecorp]sarà.

      Audience Manager usa il sottodominio per [!UICONTROL Data Collection Server] ([!UICONTROL DCS]). Nell'esempio precedente, se la società [!DNL URL] è [!UICONTROL DCS] completa [!DNL acmecorp.demdex.net].

   * **[!UICONTROL imsOrgld]**: ([!UICONTROL Identity Management System Organization ID]) Questo ID consente di collegare la tua società con Adobe Experience Cloud.
   * **[!UICONTROL Lifecyle]**: Specificate lo stage desiderato per la società:
      * **[!UICONTROL Active]**: Specifica che la società sarà un client Audience Manager attivo. Un account Attivo indica un cliente pagatore, non solo per la consulenza, ma per lo SKU Audience Manager.
      * **[!UICONTROL Demo]**: Specificate che la società sarà solo a scopo dimostrativo. I dati di reporting verranno segnalati automaticamente.
      * **[!UICONTROL Prospect]**: Specifica che l'azienda è un potenziale client Audience Manager, ad esempio una società che dispone di una configurazione gratuita [!DNL POC] o di un account per una demo di vendita.
      * **[!UICONTROL Test]**: Specificate che la società sarà solo a scopo di test interno.
   * **[!UICONTROL Account Types]**: Specificate l'intero set di tipi di account per questa società. Nessun tipo di account è mutualmente esclusivo con qualsiasi altro tipo.
      * **[!UICONTROL Full AAM]**: Specifica che l'azienda avrà un account Adobe Audience Manager completo e gli utenti avranno accesso accesso.
      * **[!UICONTROL MMP]**: Specificate che l'azienda è stata attivata per utilizzare le funzionalità Profilo marketing principale ([!UICONTROL MMP]).

         Se selezionate questo tipo di account, **[!UICONTROL Visitor ID Service]** viene selezionato automaticamente anche.
Per ulteriori informazioni, consultate [Servizi di audience - Profilo marketing principale](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html).
   * **[!UICONTROL Data Source]**: Specifica che la società è un provider di dati terze parti all'interno di Audience Manager.
   * **[!UICONTROL Targeting Partner]**: Specifica che l'azienda agisce come piattaforma di targeting per i clienti di Audience Manager.
   * **[!UICONTROL Visitor ID Service]**: Specifica che la società è stata abilitata per l'utilizzo del servizio ID visitatori di Experience Cloud.

      Il servizio ID visitatori di Experience Cloud fornisce un ID visitatore universale nelle soluzioni Experience Cloud. For more information, see the [Experience Cloud Visitor ID Service user guide](https://microsite.omniture.com/t2/help/en_US/mcvid/mcvid_service.html).

   * **[!UICONTROL Agency]**: Specificate che l'azienda avrà un account Agenzia.
   * **[!UICONTROL Features]**: Selezionate le opzioni desiderate:
      * **[!UICONTROL Password Expiration]**: Imposta tutte le password utente all'interno di questa società per scadere dopo 90 giorni per aumentare la sicurezza di Audience Manager.
      * **[!UICONTROL Reporting]**: Abilita la generazione di rapporti Audience Manager per questa società.
      * **[!UICONTROL Role Based Access Controls]**: Abilitare i controlli di accesso basati su ruolo per questa società. I controlli di accesso basati su ruolo consentono di creare gruppi di utenti con autorizzazioni di accesso diverse. I singoli utenti all'interno di questi gruppi possono quindi accedere solo a specifiche funzionalità di Audience Manager.


1. Fai clic su **[!UICONTROL Submit Updates]**.

## Eliminare un profilo società {#delete-company-profile}

Utilizzate la [!UICONTROL Companies] pagina dello strumento Audience Manager [!UICONTROL Admin] per eliminare una società esistente.

<!-- t_delete_company.xml -->

>[!NOTE]
>
>Per eliminare le società esistenti dovete avere [!UICONTROL DEXADMIN] il ruolo necessario.

1. Per eliminare una società esistente, fate clic **[!UICONTROL Companies]** su.

   ![Risultato passaggio](assets/companies.png)

1. Fate clic ![](assets/icon_delete.png) nella **[!UICONTROL Actions]** colonna della società desiderata.
1. Click **[!UICONTROL OK]** to confirm the deletion.
