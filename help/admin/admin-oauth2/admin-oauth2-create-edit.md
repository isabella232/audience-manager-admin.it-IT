---
description: Utilizzate la pagina Client OAuth2 per visualizzare un elenco dei client OAuth2 nella configurazione di Audience Manager. Potete modificare o eliminare i client esistenti o creare nuovi client, a condizione che vi siano stati assegnati i ruoli utente appropriati.
seo-description: Utilizzate la pagina Client OAuth2 per visualizzare un elenco dei client OAuth2 nella configurazione di Audience Manager. Potete modificare o eliminare i client esistenti o creare nuovi client, a condizione che vi siano stati assegnati i ruoli utente appropriati.
seo-title: Client OAuth2
title: Client OAuth2
uuid: 3e654053-fb2f-4d8f-a53c-b5c3b8dbdaaa
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Client OAuth2 {#oauth-clients}

Utilizzate la [!UICONTROL OAuth2 Clients] pagina per visualizzare un elenco dei [!UICONTROL OAuth2] client nella [!DNL Audience Manager] configurazione. Potete modificare o eliminare i client esistenti o creare nuovi client, a condizione che vi siano stati assegnati i ruoli utente appropriati.

## Panoramica {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>Assicurati che il cliente legga la documentazione [OAuth2](https://docs.adobe.com/content/help/en/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) nella Guida utente di [!DNL Audience Manager.

[!DNL OAuth2] è uno standard aperto per l'autorizzazione che consente l'accesso delegato protetto alle [!DNL Audience Manager] risorse per conto del proprietario di una risorsa.

![](assets/oauth.png)

Potete ordinare ciascuna colonna in ordine crescente o decrescente facendo clic sull’intestazione della colonna desiderata.

Utilizzare la [!UICONTROL Search] casella o i controlli di impaginazione in fondo all'elenco per trovare il client desiderato.

## Creare o modificare un client OAuth2 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

Utilizzate la [!UICONTROL OAuth2 Clients] pagina nello strumento Audience Manager [!UICONTROL Admin] [!UICONTROL Oauth2] per creare un nuovo client o per modificare un client esistente.

1. Per creare un nuovo [!UICONTROL OAuth2] client, fate clic su **[!UICONTROL OAuth2 Clients]** &gt; **[!UICONTROL Add OAuth2 Client]**. Per modificare un [!UICONTROL OAuth2] client esistente, fate clic sul client desiderato nella **[!UICONTROL Client ID]** colonna.
1. Specificate il nome desiderato per questo [!UICONTROL OAuth2] client. Si noti che si tratta di un nome solo per il record.
1. Specificate l'indirizzo e-mail del [!UICONTROL OAuth2] cliente. Esiste un limite di un indirizzo e-mail.
1. Dall’elenco a **[!UICONTROL Partner]** discesa, selezionate il partner desiderato.
1. Nella **[!UICONTROL Client ID]** casella, specificate l’ID desiderato. Valore utilizzato per l'invio delle [!DNL API] richieste. Il prefisso viene compilato automaticamente quando si inizia a digitare dopo che è stato scelto un [!UICONTROL Partner] elemento dall'elenco a discesa nel passaggio precedente. Il formato corretto è &lt; *`partner subdomain`*&gt; - &lt; *`Audience Manager username`*&gt;.
1. Selezionate o deselezionate la **[!UICONTROL Restrict to Partner Users]** casella di controllo come desiderato. Se questa casella di controllo è selezionata, l'utente deve essere un [!DNL Audience Manager] utente elencato per il partner selezionato. Come procedura ottimale, si consiglia di selezionare questa opzione.
1. Nella **[!UICONTROL Scope]** sezione, selezionate o deselezionate le caselle **[!UICONTROL Read]** e **[!UICONTROL Write]** di controllo desiderate.
1. Nella **[!UICONTROL Grant Type]** sezione selezionare i mezzi di autorizzazione desiderati. È consigliabile utilizzare le impostazioni predefinite di [!UICONTROL Password] e [!UICONTROL Refresh-token] opzioni.

   * **[!UICONTROL Implicit]**: Se selezionate questa opzione, la [!UICONTROL Redirect URI] casella è abilitata. Dopo l'autenticazione, all'utente viene assegnato un token di accesso automatico che viene inviato immediatamente al reindirizzamento [!DNL URI].
   * **[!UICONTROL Authorization Code]**: Se selezionate questa opzione, la [!UICONTROL Redirect URI] casella è abilitata. L'utente viene restituito al client dopo essere stato autenticato e quindi inviato al reindirizzamento [!DNL URI].
   * **[!UICONTROL Password]**: L'utente viene autenticato con una password immessa dall'utente anziché con un tentativo automatico di convalida tramite un server di autorizzazione.
   * **[!UICONTROL Refresh_token]**: Utilizzato per aggiornare un token di accesso scaduto per un periodo di tempo prolungato.

1. Nella **[!UICONTROL Redirect URI]** casella, specificate il [!DNL URI]valore desiderato. Questa opzione è abilitata solo se si selezionano i tipi **[!UICONTROL Implicit]** e **[!UICONTROL Authorization_code]** sovvenzione. La **[!UICONTROL Redirect URI]** casella consente di specificare un valore separato da virgole di [!DNL URI] valori accettabili. Questo è l' [!DNL URI] utente a cui viene reindirizzato un client dopo aver approvato il client per l' [!DNL API] accesso.
1. Specifica il tempo di scadenza desiderato (in secondi) per l’accesso e l’aggiornamento della scadenza del token.

   * **[!UICONTROL Access Token Expiration Time]**: Il numero di secondi di validità di un token di accesso dopo l'emissione. Può essere null per utilizzare il valore predefinito della piattaforma (12 ore). Può anche essere -1 per indicare che il token di accesso non scade.
   * **[!UICONTROL Refresh Token Expiration Time]**: Il numero di secondi di validità di un token di aggiornamento dopo l'emissione. Può essere null per utilizzare il valore predefinito della piattaforma (30 giorni).

1. Fai clic su **[!UICONTROL Save]**.

Per eliminare un [!UICONTROL OAuth2] client, fate clic su **[!UICONTROL OAuth2 Clients]**, quindi fate clic ![](assets/icon_delete.png) nella **[!UICONTROL Actions]** colonna relativa al client desiderato.

>[!MORE_LIKE_this]
>
>* [Requisiti API e raccomandazioni](../admin-oauth2/aam-admin-api-requirements.md)

