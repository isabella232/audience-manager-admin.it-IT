---
description: Utilizzare la pagina Client OAuth2 per visualizzare un elenco dei client OAuth2 nella configurazione del Audience Manager . Potete modificare o eliminare i client esistenti o creare nuovi client, a condizione che vi siano stati assegnati i ruoli utente appropriati.
seo-description: Utilizzare la pagina Client OAuth2 per visualizzare un elenco dei client OAuth2 nella configurazione del Audience Manager . Potete modificare o eliminare i client esistenti o creare nuovi client, a condizione che vi siano stati assegnati i ruoli utente appropriati.
seo-title: Client OAuth2
title: Client OAuth2
uuid: 3e654053-fb2f-4d8f-a53c-b5c3b8dbdaaa
translation-type: tm+mt
source-git-commit: 0ee7aa9c13f1b9b8fd64dddff4e52d101055e77c
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 2%

---


# Client OAuth2 {#oauth-clients}

Utilizzare la pagina [!UICONTROL OAuth2 Clients] per visualizzare un elenco dei client [!UICONTROL OAuth2] nella configurazione [!DNL Audience Manager]. Potete modificare o eliminare i client esistenti o creare nuovi client, a condizione che vi siano stati assegnati i ruoli utente appropriati.

## Panoramica {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>Assicurati che il cliente legga la documentazione [OAuth2](https://docs.adobe.com/content/help/en/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) nella Guida utente  Audience Manager.

[!DNL OAuth2] è uno standard aperto per l&#39;autorizzazione che consente l&#39;accesso delegato protetto alle  [!DNL Audience Manager] risorse per conto del proprietario di una risorsa.

![](assets/oauth.png)

Potete ordinare ciascuna colonna in ordine crescente o decrescente facendo clic sull’intestazione della colonna desiderata.

Utilizzare la casella [!UICONTROL Search] o i controlli di impaginazione in fondo all&#39;elenco per trovare il client desiderato.

## Creare o modificare un client OAuth2 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

Utilizzare la pagina [!UICONTROL OAuth2 Clients] nello strumento Audience Manager  [!UICONTROL Admin] per creare un nuovo client [!UICONTROL Oauth2] o per modificare un client esistente.

1. Per creare un nuovo client [!UICONTROL OAuth2], fare clic su **[!UICONTROL OAuth2 Clients]** > **[!UICONTROL Add OAuth2 Client]**. Per modificare un client [!UICONTROL OAuth2] esistente, fare clic sul client desiderato nella colonna **[!UICONTROL Client ID]**.
1. Specificare il nome desiderato per il client [!UICONTROL OAuth2]. Si noti che si tratta di un nome solo per il record.
1. Specificate l&#39;indirizzo e-mail del client [!UICONTROL OAuth2]. Esiste un limite di un indirizzo e-mail.
1. Dall&#39;elenco a discesa **[!UICONTROL Partner]**, selezionare il partner desiderato.
1. Nella casella **[!UICONTROL Client ID]**, specificate l&#39;ID desiderato. Valore utilizzato per l&#39;invio delle richieste [!DNL API]. Il prefisso viene compilato automaticamente quando si inizia a digitare dopo che è stato scelto un [!UICONTROL Partner] dall&#39;elenco a discesa nel passaggio precedente. Il formato corretto è &lt; *`partner subdomain`*> - &lt; *`Audience Manager username`*>.
1. Selezionare o deselezionare la casella di controllo **[!UICONTROL Restrict to Partner Users]**, come desiderato. Se questa casella di controllo è selezionata, l&#39;utente deve essere un [!DNL Audience Manager] utente elencato per il partner selezionato. Come procedura ottimale, si consiglia di selezionare questa opzione.
1. Nella sezione **[!UICONTROL Scope]**, selezionare o deselezionare le caselle di controllo **[!UICONTROL Read]** e **[!UICONTROL Write]**, come desiderato.
1. Nella sezione **[!UICONTROL Grant Type]**, selezionare i mezzi di autorizzazione desiderati. È consigliabile utilizzare le impostazioni predefinite delle opzioni [!UICONTROL Password] e [!UICONTROL Refresh-token].

   * **[!UICONTROL Implicit]**: Se selezionate questa opzione, la  [!UICONTROL Redirect URI] casella è abilitata. Dopo l&#39;autenticazione, all&#39;utente viene assegnato un token di accesso automatico che viene inviato immediatamente al reindirizzamento [!DNL URI].
   * **[!UICONTROL Authorization Code]**: Se selezionate questa opzione, la  [!UICONTROL Redirect URI] casella è abilitata. L&#39;utente viene restituito al client dopo essere stato autenticato e quindi inviato al reindirizzamento [!DNL URI].
   * **[!UICONTROL Password]**: L&#39;utente viene autenticato con una password immessa dall&#39;utente anziché con un tentativo automatico di convalida tramite un server di autorizzazione.
   * **[!UICONTROL Refresh_token]**: Utilizzato per aggiornare un token di accesso scaduto per un periodo di tempo prolungato.

1. Nella casella **[!UICONTROL Redirect URI]**, specificare la [!DNL URI] desiderata. Questa opzione è abilitata solo se si selezionano i tipi di sovvenzione **[!UICONTROL Implicit]** e **[!UICONTROL Authorization_code]**. La casella **[!UICONTROL Redirect URI]** consente di specificare un valore separato da virgole di valori [!DNL URI] accettabili. Questo è il [!DNL URI] a cui viene reindirizzato un utente di un client dopo l&#39;approvazione del client per l&#39;accesso [!DNL API].
1. Specifica il tempo di scadenza desiderato (in secondi) per l’accesso e l’aggiornamento della scadenza del token.

   * **[!UICONTROL Access Token Expiration Time]**: Il numero di secondi di validità di un token di accesso dopo l&#39;emissione. Può essere null per utilizzare il valore predefinito della piattaforma (12 ore). Può anche essere -1 per indicare che il token di accesso non scade.
   * **[!UICONTROL Refresh Token Expiration Time]**: Il numero di secondi di validità di un token di aggiornamento dopo l&#39;emissione. Può essere null per utilizzare il valore predefinito della piattaforma (30 giorni).

1. Clic **[!UICONTROL Save]**.

Per eliminare un client [!UICONTROL OAuth2], fare clic su **[!UICONTROL OAuth2 Clients]**, quindi fare clic su ![](assets/icon_delete.png) nella colonna **[!UICONTROL Actions]** del client desiderato.

>[!MORELIKETHIS]
>
>* [Raccomandazioni e requisiti per l’utilizzo delle API](../admin-oauth2/aam-admin-api-requirements.md)

