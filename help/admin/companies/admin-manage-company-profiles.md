---
description: Utilizzate la pagina Aziende dello strumento di amministrazione di Audience Manager per creare una nuova società.
seo-description: Utilizzate la pagina Aziende dello strumento di amministrazione di Audience Manager per creare una nuova società.
seo-title: Creazione di un profilo società
title: Creazione di un profilo società
uuid: 55de18f8-883d-43fe-b37f-e8805bb92f7a
translation-type: tm+mt
source-git-commit: 71bf4cec222428686c1eab0998f66887db06da68

---


# Creazione di un profilo società {#create-a-company-profile}

Utilizzate la [!UICONTROL Companies] pagina nello strumento di amministrazione di Audience Manager per creare una nuova società.

<!-- t_create_company.xml -->

>[!NOTE]
>
>Per creare nuove società è necessario disporre del **[!UICONTROL DEXADMIN]** ruolo.

1. Click **[!UICONTROL Companies]** &gt; **[!UICONTROL Add Company]**.
1. Compila i campi:

   * **[!UICONTROL Name]**: (Obbligatorio) Specificate il nome della società.
   * **[!UICONTROL Description]**: (Obbligatorio) Fornire informazioni descrittive sulla società, come l'industria o il suo nome completo.
   * **[!UICONTROL Subdomain]**: (Obbligatorio) Specifica il sottodominio della società. Il testo immesso è quello che viene visualizzato come sottodominio della chiamata dell’evento. Questo non può essere cambiato. Deve essere una stringa di caratteri [!DNL URL]validi.

      Ad esempio, se la società è stata denominata [!DNL AcmeCorp], il sottodominio sarà [!DNL acmecorp].

      Audience Manager utilizza il sottodominio per il [!UICONTROL Data Collection Server]([!UICONTROL DCS]). Nell'esempio precedente, se la società è piena [!DNL URL] in [!UICONTROL DCS] sarebbe [!DNL acmecorp.demdex.net].

   * **[!UICONTROL Lifecyle]**: Specificate la fase desiderata per la società:
      * **[!UICONTROL Active]**: Specifica che la società sarà un client Audience Manager attivo. Per [!UICONTROL Active] account si intende un cliente pagante, non solo per la consulenza, ma per lo SKU di Audience Manager.
      * **[!UICONTROL Demo]**: Specifica che la società sarà solo a scopo dimostrativo. I dati di reporting verranno automaticamente falsificati.
      * **[!UICONTROL Prospect]**: Specifica che la società è un potenziale client Audience Manager, ad esempio una società alla quale viene concesso un account gratuito [!DNL POC] o un account impostato per una demo delle vendite.
      * **[!UICONTROL Test]**: Specificate che la società sarà solo a scopo di test interno.
   * **[!UICONTROL Account Types]**: Specifica l'intero set di tipi di account per la società. Nessun tipo di account si esclude a vicenda con qualsiasi altro tipo.
      * **[!UICONTROL Full AAM]**: Specifica che la società avrà un account Adobe Audience Manager completo e gli utenti avranno accesso.
      * **[!UICONTROL MMP]**: Specificate che la società è stata abilitata per utilizzare le funzionalità [!UICONTROL Master Marketing Profile] ([!UICONTROL MMP]). Consente [!UICONTROL MMP] di condividere i tipi di pubblico in Experience Cloud utilizzando un [!UICONTROL Experience Cloud ID] ([!DNL MCID]) assegnato a ogni visitatore e quindi utilizzato da Audience Manager. Se si seleziona questo tipo di account, [!UICONTROL Experience Cloud ID Service] viene selezionata automaticamente anche l'opzione.

         Per ulteriori informazioni, vedi [Audiences Services - Master Marketing Profile](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html).
   * **[!UICONTROL Data Source]**: Specifica che la società è un fornitore di dati di terze parti in Audience Manager.
   * **[!UICONTROL Targeting Partner]**: Specificate che la società funga da piattaforma di targeting per i clienti di Audience Manager.
   * **[!UICONTROL Visitor ID Service]**: Specificate che la società è stata abilitata per l'utilizzo del [!UICONTROL Experience Cloud Visitor ID Service].

      Fornisce [!UICONTROL Experience Cloud Visitor ID Service] un ID visitatore universale nelle soluzioni Experience Cloud. For more information, see the [Experience Cloud Visitor ID Service user guide](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-overview.html).

   * **[!UICONTROL Agency]**: Specificate che la società avrà un [!UICONTROL Agency] account.



1. Fai clic su **[!UICONTROL Create]**. Seguite le istruzioni riportate in [Modifica profilo](../companies/admin-manage-company-profiles.md#edit-company-profile)società.

   ![Risultato del passaggio](assets/add_company.png)

## Modifica di un profilo società {#edit-company-profile}

Modifica il profilo di una società, incluso nome, descrizione, sottodominio, ciclo di vita e altro.

<!-- t_edit_company_profile.xml -->

1. Fate clic **[!UICONTROL Companies]**, quindi individuate e fate clic sulla società desiderata per visualizzare la [!UICONTROL Profile] pagina.

   Utilizzate la [!UICONTROL Search] casella o i controlli di impaginazione in fondo all’elenco per trovare la società desiderata. Potete ordinare ciascuna colonna in ordine crescente o decrescente facendo clic sull’intestazione della colonna desiderata.

   ![Risultato del passaggio](assets/profile_company.png)

1. Modificate i campi come necessario:

   * **[!UICONTROL Name]**: Modificate il nome della società. Questo campo è obbligatorio.
   * **[!UICONTROL Description]**: Modificate la descrizione della società. Questo campo è obbligatorio.
   * **[!UICONTROL Subdomain]**: (Obbligatorio) Specifica il sottodominio della società. Il testo immesso è quello che viene visualizzato come sottodominio della chiamata dell’evento. Questo non può essere cambiato. Deve essere una stringa di caratteri [!DNL URL]validi.

      Ad esempio, se la società è stata denominata [!DNL AcmeCorp], il sottodominio sarà [!DNL acmecorp].

      Audience Manager utilizza il sottodominio per [!UICONTROL Data Collection Server] ([!UICONTROL DCS]). Nell'esempio precedente, se la società è piena [!DNL URL] in [!UICONTROL DCS] sarebbe [!DNL acmecorp.demdex.net].

   * **[!UICONTROL imsOrgld]**: ([!UICONTROL Identity Management System Organization ID]) Questo ID consente di collegare la società ad Adobe Experience Cloud.
   * **[!UICONTROL Lifecyle]**: Specificate la fase desiderata per la società:
      * **[!UICONTROL Active]**: Specifica che la società sarà un client Audience Manager attivo. Per account attivo si intende un cliente pagante, non solo per la consulenza, ma per lo SKU di Audience Manager.
      * **[!UICONTROL Demo]**: Specifica che la società sarà solo a scopo dimostrativo. I dati di reporting verranno automaticamente falsificati.
      * **[!UICONTROL Prospect]**: Specifica che la società è un potenziale client Audience Manager, ad esempio una società alla quale viene concesso un account gratuito [!DNL POC] o un account impostato per una demo delle vendite.
      * **[!UICONTROL Test]**: Specificate che la società sarà solo a scopo di test interno.
   * **[!UICONTROL Account Types]**: Specifica l'intero set di tipi di account per la società. Nessun tipo di account si esclude a vicenda con qualsiasi altro tipo.
      * **[!UICONTROL Full AAM]**: Specifica che la società avrà un account Adobe Audience Manager completo e gli utenti avranno accesso.
      * **[!UICONTROL MMP]**: Specificate che la società è stata abilitata per utilizzare le funzionalità del profilo marketing principale ([!UICONTROL MMP]).

         Se selezionate questo tipo di account, **[!UICONTROL Visitor ID Service]** viene selezionato automaticamente anche.
Per ulteriori informazioni, vedi [Audiences Services - Master Marketing Profile](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html).
   * **[!UICONTROL Data Source]**: Specifica che la società è un fornitore di dati di terze parti in Audience Manager.
   * **[!UICONTROL Targeting Partner]**: Specificate che la società funga da piattaforma di targeting per i clienti di Audience Manager.
   * **[!UICONTROL Visitor ID Service]**: Specifica che la società è stata abilitata per l’utilizzo del servizio ID visitatori di Experience Cloud.

      Il servizio ID visitatori di Experience Cloud fornisce un ID visitatore universale nelle soluzioni Experience Cloud. For more information, see the [Experience Cloud Visitor ID Service user guide](https://microsite.omniture.com/t2/help/en_US/mcvid/mcvid_service.html).

   * **[!UICONTROL Agency]**: Specificate che la società avrà un account Agenzia.
   * **[!UICONTROL Features]**: Selezionate le opzioni desiderate:
      * **[!UICONTROL Password Expiration]**: Imposta la scadenza di tutte le password utente all’interno della società dopo 90 giorni per aumentare la sicurezza di Audience Manager.
      * **[!UICONTROL Reporting]**: Abilita il reporting di Audience Manager per questa società.
      * **[!UICONTROL Role Based Access Controls]**: Abilita controlli di accesso basati sui ruoli per questa società. I controlli di accesso basati sul ruolo consentono di creare gruppi di utenti con autorizzazioni di accesso diverse. I singoli utenti all'interno di questi gruppi possono quindi accedere solo a funzioni specifiche in Audience Manager.


1. Fai clic su **[!UICONTROL Submit Updates]**.

## Eliminare un profilo società {#delete-company-profile}

Utilizzate la [!UICONTROL Companies] pagina nello strumento Audience Manager [!UICONTROL Admin] per eliminare una società esistente.

<!-- t_delete_company.xml -->

>[!NOTE]
>
>È necessario avere il [!UICONTROL DEXADMIN] ruolo per eliminare le società esistenti.

1. Per eliminare una società esistente, fate clic su **[!UICONTROL Companies]**.

   ![Risultato del passaggio](assets/companies.png)

1. Fate clic ![](assets/icon_delete.png) nella **[!UICONTROL Actions]** colonna della società desiderata.
1. Click **[!UICONTROL OK]** to confirm the deletion.
