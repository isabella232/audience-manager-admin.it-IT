---
description: Utilizza la pagina Client OAuth2 per visualizzare un elenco dei client OAuth2 nella configurazione dell’Audience Manager. È possibile modificare o eliminare i client esistenti o creare nuovi client, a condizione che siano stati assegnati i ruoli utente appropriati.
seo-description: Use the OAuth2 Clients page to view a list of OAuth2 clients in your Audience Manager configuration. You can edit or delete existing clients or create new clients, providing that you have the appropriate user roles assigned.
seo-title: OAuth2 Clients
title: Client OAuth2
uuid: 3e654053-fb2f-4d8f-a53c-b5c3b8dbdaaa
exl-id: 993eae04-02e8-4554-a6fe-cf599053bfc9
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 1%

---

# Client OAuth2 {#oauth-clients}

Utilizza la pagina [!UICONTROL OAuth2 Clients] per visualizzare un elenco dei client [!UICONTROL OAuth2] nella configurazione [!DNL Audience Manager]. È possibile modificare o eliminare i client esistenti o creare nuovi client, a condizione che siano stati assegnati i ruoli utente appropriati.

## Panoramica {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>Assicurati che il tuo cliente legga la documentazione [OAuth2](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) nella Guida utente di Audience Manager.

[!DNL OAuth2] è uno standard aperto per l’autorizzazione a fornire accesso delegato protetto alle  [!DNL Audience Manager] risorse per conto del proprietario di una risorsa.

![](assets/oauth.png)

Per ordinare ciascuna colonna in ordine crescente o decrescente, fai clic sull’intestazione della colonna desiderata.

Utilizzare la casella [!UICONTROL Search] o i controlli di impaginazione in fondo all&#39;elenco per trovare il client desiderato.

## Creare o modificare un client OAuth2 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

Utilizza la pagina [!UICONTROL OAuth2 Clients] nello strumento Audience Manager [!UICONTROL Admin] per creare un nuovo client [!UICONTROL Oauth2] o per modificare un client esistente.

1. Per creare un nuovo client [!UICONTROL OAuth2], fai clic su **[!UICONTROL OAuth2 Clients]** > **[!UICONTROL Add OAuth2 Client]**. Per modificare un client esistente [!UICONTROL OAuth2], fai clic sul client desiderato nella colonna **[!UICONTROL Client ID]** .
1. Specifica il nome desiderato per il client [!UICONTROL OAuth2]. Tieni presente che si tratta di un nome solo per il record.
1. Specifica l&#39;indirizzo e-mail del client [!UICONTROL OAuth2]. Esiste un limite di un indirizzo e-mail.
1. Dall’elenco a discesa **[!UICONTROL Partner]** , seleziona il partner desiderato.
1. Nella casella **[!UICONTROL Client ID]** , specifica l’ID desiderato. Questo è il valore utilizzato per inviare le richieste [!DNL API]. Il prefisso viene compilato automaticamente quando inizi a digitare dopo aver scelto un [!UICONTROL Partner] dall’elenco a discesa nel passaggio precedente. Il formato corretto è &lt; *`partner subdomain`*> - &lt; *`Audience Manager username`*>.
1. Seleziona o deseleziona la casella di controllo **[!UICONTROL Restrict to Partner Users]** come desiderato. Se questa casella di controllo è selezionata, l&#39;utente deve essere un [!DNL Audience Manager] utente elencato per il partner selezionato. Come best practice, è consigliabile selezionare questa opzione.
1. Nella sezione **[!UICONTROL Scope]**, seleziona o deseleziona le caselle di controllo **[!UICONTROL Read]** e **[!UICONTROL Write]** a seconda delle tue esigenze.
1. Nella sezione **[!UICONTROL Grant Type]** , seleziona i mezzi di autorizzazione desiderati. È consigliabile utilizzare le impostazioni predefinite delle opzioni [!UICONTROL Password] e [!UICONTROL Refresh-token].

   * **[!UICONTROL Implicit]**: Se selezioni questa opzione, la  [!UICONTROL Redirect URI] casella è abilitata. All&#39;utente viene assegnato un token di accesso automatico dopo l&#39;autenticazione e viene inviato immediatamente al reindirizzamento [!DNL URI].
   * **[!UICONTROL Authorization Code]**: Se selezioni questa opzione, la  [!UICONTROL Redirect URI] casella è abilitata. L&#39;utente viene restituito al client dopo essere stato autenticato e quindi inviato al reindirizzamento [!DNL URI].
   * **[!UICONTROL Password]**: L’utente viene autenticato con una password immessa dall’utente anziché con un tentativo di convalida automatica tramite un server di autorizzazione.
   * **[!UICONTROL Refresh_token]**: Utilizzato per aggiornare un token di accesso scaduto per un periodo di tempo prolungato.

1. Nella casella **[!UICONTROL Redirect URI]**, specifica il [!DNL URI] desiderato. Questa opzione è abilitata solo se hai selezionato i tipi di sovvenzione **[!UICONTROL Implicit]** e **[!UICONTROL Authorization_code]** . La casella **[!UICONTROL Redirect URI]** consente di specificare un valore separato da virgole di valori accettabili [!DNL URI]. Questo è il [!DNL URI] a cui viene reindirizzato l&#39;utente di un client dopo aver approvato il client per l&#39; [!DNL API] accesso.
1. Specifica il tempo di scadenza desiderato (in secondi) per l’accesso e l’aggiornamento della scadenza del token.

   * **[!UICONTROL Access Token Expiration Time]**: Il numero di secondi in cui un token di accesso è valido dopo l&#39;emissione. Può essere null per utilizzare la piattaforma predefinita (12 ore). Può anche essere -1 per indicare che il token di accesso non scade.
   * **[!UICONTROL Refresh Token Expiration Time]**: Il numero di secondi in cui un token di aggiornamento è valido dopo essere stato rilasciato. Può essere null per utilizzare la piattaforma predefinita (30 giorni).

1. Clic **[!UICONTROL Save]**.

Per eliminare un client [!UICONTROL OAuth2], fai clic su **[!UICONTROL OAuth2 Clients]**, quindi fai clic su ![](assets/icon_delete.png) nella colonna **[!UICONTROL Actions]** del client desiderato.

>[!MORELIKETHIS]
>
>* [Raccomandazioni e requisiti per l’utilizzo delle API](../admin-oauth2/aam-admin-api-requirements.md)

