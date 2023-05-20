---
description: Utilizza la pagina Client OAuth2 per visualizzare un elenco di client OAuth2 nella configurazione dell'Audience Manager. È possibile modificare o eliminare i client esistenti o crearne di nuovi, purché siano stati assegnati i ruoli utente appropriati.
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

Utilizza il [!UICONTROL OAuth2 Clients] pagina per visualizzare un elenco di [!UICONTROL OAuth2] client nel tuo [!DNL Audience Manager] configurazione. È possibile modificare o eliminare i client esistenti o crearne di nuovi, purché siano stati assegnati i ruoli utente appropriati.

## Panoramica {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>Assicurati che il cliente legga [OAuth2](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) nella Guida utente di Audience Manager.

[!DNL OAuth2] è uno standard aperto per l&#39;autorizzazione a fornire accesso delegato protetto a [!DNL Audience Manager] risorse per conto di un proprietario di risorse.

![](assets/oauth.png)

Puoi ordinare ogni colonna in ordine crescente o decrescente facendo clic sull’intestazione della colonna desiderata.

Utilizza il [!UICONTROL Search] o i controlli di impaginazione nella parte inferiore dell&#39;elenco per trovare il client desiderato.

## Creare o modificare un client OAuth2 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

Utilizza il [!UICONTROL OAuth2 Clients] pagina nell’Audience Manager [!UICONTROL Admin] strumento per creare un nuovo [!UICONTROL Oauth2] o per modificare un client esistente.

1. Per creare un nuovo [!UICONTROL OAuth2] client, fai clic su **[!UICONTROL OAuth2 Clients]** > **[!UICONTROL Add OAuth2 Client]**. Per modificare un [!UICONTROL OAuth2] , fare clic sul client desiderato nella **[!UICONTROL Client ID]** colonna.
1. Specifica il nome desiderato [!UICONTROL OAuth2] client. Tieni presente che questo è un nome solo per il record.
1. Specifica la [!UICONTROL OAuth2] indirizzo e-mail del cliente. Esiste un limite di un indirizzo e-mail.
1. Dalla sezione **[!UICONTROL Partner]** selezionare il partner desiderato.
1. In **[!UICONTROL Client ID]** , specifica l’ID desiderato. Questo è il valore utilizzato per l’invio [!DNL API] richieste. Il prefisso si compila automaticamente quando si inizia a digitare dopo aver scelto un [!UICONTROL Partner] dall’elenco a discesa nel passaggio precedente. Il formato corretto è &lt; *`partner subdomain`*> - &lt; *`Audience Manager username`*>.
1. Seleziona o deseleziona la **[!UICONTROL Restrict to Partner Users]** , come desiderato. Se questa casella di controllo è selezionata, l&#39;utente deve essere un [!DNL Audience Manager] utente elencato per il partner selezionato. Come best practice, è consigliabile selezionare questa opzione.
1. In **[!UICONTROL Scope]** sezione, seleziona o deseleziona la **[!UICONTROL Read]** e **[!UICONTROL Write]** caselle di controllo, come desiderato.
1. In **[!UICONTROL Grant Type]** , selezionare il mezzo di autorizzazione desiderato. È consigliabile utilizzare le impostazioni predefinite di [!UICONTROL Password] e [!UICONTROL Refresh-token] opzioni.

   * **[!UICONTROL Implicit]**: se selezioni questa opzione, il [!UICONTROL Redirect URI] è attivato. L’utente riceve un token di accesso automatico dopo l’autenticazione e viene inviato immediatamente al reindirizzamento [!DNL URI].
   * **[!UICONTROL Authorization Code]**: se selezioni questa opzione, il [!UICONTROL Redirect URI] è attivato. L’utente viene restituito al client dopo essere stato autenticato e quindi inviato al reindirizzamento [!DNL URI].
   * **[!UICONTROL Password]**: l’utente viene autenticato con una password inserita dall’utente anziché con un tentativo di convalida automatica tramite un server di autorizzazione.
   * **[!UICONTROL Refresh_token]**: utilizzato per aggiornare un token di accesso scaduto per un periodo di tempo prolungato.

1. In **[!UICONTROL Redirect URI]** , specificare il valore desiderato [!DNL URI]. Questa opzione è abilitata solo se selezioni **[!UICONTROL Implicit]** e **[!UICONTROL Authorization_code]** tipi di sovvenzione. Il **[!UICONTROL Redirect URI]** consente di specificare un valore separato da virgole di accettabile [!DNL URI] valori. Questo è il [!DNL URI] l&#39;utente di un client viene reindirizzato a dopo l&#39;approvazione del client per [!DNL API] accesso.
1. Specifica il tempo di scadenza (in secondi) desiderato per l’accesso e la scadenza del token di aggiornamento.

   * **[!UICONTROL Access Token Expiration Time]**: numero di secondi di validità di un token di accesso dopo il rilascio. Può essere null per utilizzare il valore predefinito della piattaforma (12 ore). Inoltre, può essere -1 per indicare che il token di accesso non scade.
   * **[!UICONTROL Refresh Token Expiration Time]**: numero di secondi di validità di un token di aggiornamento dopo l’emissione. Può essere null per utilizzare il valore predefinito della piattaforma (30 giorni).

1. Clic **[!UICONTROL Save]**.

Per eliminare un [!UICONTROL OAuth2] client, fai clic su **[!UICONTROL OAuth2 Clients]**, quindi fai clic su  ![](assets/icon_delete.png) nel **[!UICONTROL Actions]** per il client desiderato.

>[!MORELIKETHIS]
>
>* [Raccomandazioni e requisiti per l’utilizzo delle API](../admin-oauth2/aam-admin-api-requirements.md)

