---
description: Utilizzate la pagina Server nello strumento Amministrazione di Audience Manager per creare un nuovo server HTTP o per modificare un server esistente.
seo-description: Utilizzate la pagina Server nello strumento Amministrazione di Audience Manager per creare un nuovo server HTTP o per modificare un server esistente.
seo-title: Creare o modificare un server HTTP
title: Creare o modificare un server HTTP
uuid: 1 ef 0 e 751-e 239-4 dc 6-a 4 f 6-73 cc 05686807
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# Creare o modificare un server HTTP {#create-or-edit-an-http-server}

Utilizza la [!UICONTROL Servers] pagina nello strumento Amministrazione di Audience Manager per creare un nuovo server HTTP o per modificare un server esistente.

>[!NOTE]
>
>Per creare nuovi server o modificare quelli esistenti, [!UICONTROL DEXADMIN] dovete avere il ruolo desiderato.

1. Per creare un nuovo server, accedete **[!UICONTROL Servers]** a &gt; **[!UICONTROL Create Server]**. Per modificare un server esistente, fai clic sul server desiderato nella **[!UICONTROL Label]** colonna.
1. Specificate l'etichetta desiderata per il server.
1. Dall'elenco **[!UICONTROL Protocol]** a discesa, selezionate il protocollo desiderato: [!DNL HTTP].
1. Compila i campi:

   * **[!UICONTROL Domain]:** Specificate il dominio desiderato (ospitante) per questo server.
   * **[!UICONTROL Port]:** Specificate la porta desiderata per il server. La porta predefinita viene visualizzata per ogni tipo di cifratura. Se necessario, potete modificare la porta predefinita
   * **[!UICONTROL Maximum Users Per Request]:** Specificate il numero massimo di utenti per richiesta consentito per questo server.
   * **[!UICONTROL URL Prefix]:** Specificate il [!DNL URL] prefisso da utilizzare per il server.
   * **[!UICONTROL Authentication URL]:** Specificate il [!UICONTROL Authentication URL] server per questo `HTTP` server.
   * **[!UICONTROL Authentication]:** Specificate il metodo di autenticazione desiderato: **[!UICONTROL None]****[!UICONTROL Username/Password]**, o **[!UICONTROL SSH Key]**.
   * **[!UICONTROL HTTP Signature Header]:** Nome dell' [!DNL HTTP] intestazione, fornito dal cliente, contenente la [!DNL HTTP] chiave di firma. Il valore predefinito è [!UICONTROL X-Signature], come illustrato nell'esempio di seguito:

      ```
      * Connected to partner.website.com (127.0.0.1) port 80 (#0)
      > POST /webpage HTTP/1.1
      > Host: partner.host.com
      > Accept: */*
      > Content-Type: application/json
      > Content-Length: 20
      > X-Signature: wxa2ByMWhhP328EvHQsVlOD5jTc=
      POST message content
      ```

   * **[!UICONTROL HTTP Signature Key]:** La chiave utilizzata per firmare [!DNL HTTP] la richiesta, fornita dal cliente.
   * **[!UICONTROL Show Signature Key]:** Attivare o disattivare la visualizzazione della firma nel browser.
   * **[!UICONTROL HTTP Signature Encryption Method]:** Specificare il metodo utilizzato per la cifratura della firma. Utilizzate [!UICONTROL SHA1] , a meno che il cliente preferisca in caso contrario.
   >[!NOTE]
   >
   >Se desiderate abilitare [l'autenticazione oauth 2.0 per trasferimenti di dati in tempo reale](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html) per un partner, compilate i campi come descritto nella tabella seguente. I campi *in corsivo* devono essere compilati esattamente come nella tabella.

   | Nome | Valore |
   |---|---|
   | [!UICONTROL Label] | [!UICONTROL Server with OAuth 2.0 enabled] |
   | [!UICONTROL Protocol] | [!UICONTROL HTTP] |
   | [!UICONTROL Domain] | [!UICONTROL api.partner.com] |
   | [!UICONTROL Port] | [!UICONTROL 443] |
   | [!UICONTROL Maximum Users per Request] | [!UICONTROL 10] |
   | [!UICONTROL URL Prefix] | [!UICONTROL /segments/aam] |
   | [!UICONTROL Authentication URL] | [!UICONTROL api.partner.com/oauth2/token] |
   | [!UICONTROL Authentication] | [!UICONTROL Username/Password] |
   | [!UICONTROL Username] | [!UICONTROL *Autorizzazione *] |
   | [!UICONTROL Password] | your_ password_ here |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. Fate clic **[!UICONTROL Create]** su un nuovo server o fate clic **[!UICONTROL Update]** su di esso per modificare un server esistente.