---
description: Utilizzare la pagina Server dello strumento Amministrazione Audience Manager  per creare un nuovo server HTTP o per modificare un server esistente.
seo-description: Utilizzare la pagina Server dello strumento Amministrazione Audience Manager  per creare un nuovo server HTTP o per modificare un server esistente.
seo-title: Creare o modificare un server HTTP
title: Creare o modificare un server HTTP
uuid: 1ef0e751-e239-4dc6-a4f6-73cc05686807
translation-type: tm+mt
source-git-commit: d518ba4011f203a7d450ce76d8c1924f7d73a815
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 7%

---


# Creare o modificare un server HTTP {#create-or-edit-an-http-server}

Utilizzate la pagina [!UICONTROL Servers] nello strumento Amministrazione Audience Manager  per creare un nuovo server HTTP o per modificare un server esistente.

>[!NOTE]
>
>Per creare nuovi server o modificare server esistenti è necessario disporre del ruolo [!UICONTROL DEXADMIN].

1. Per creare un nuovo server, passare a **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Per modificare un server esistente, fate clic sul server desiderato nella colonna **[!UICONTROL Label]**.
1. Specificate l&#39;etichetta desiderata per il server.
1. Dall&#39;elenco a discesa **[!UICONTROL Protocol]**, selezionate il protocollo desiderato: [!DNL HTTP].
1. Compila i campi:

   * **[!UICONTROL Domain]:** Specificate il dominio desiderato (host) per questo server.
   * **[!UICONTROL Port]:** Specificate la porta desiderata per questo server. Per ogni tipo di crittografia viene visualizzata la porta predefinita. Se necessario, è possibile modificare la porta predefinita
   * **[!UICONTROL Maximum Users Per Request]:** Specificate il numero massimo di utenti per richiesta consentito per questo server.
   * **[!UICONTROL URL Prefix]:** Specificare il  [!DNL URL] prefisso da utilizzare per il server.
   * **[!UICONTROL Authentication URL]:** Specificate il  [!UICONTROL Authentication URL] nome del  `HTTP` server.
   * **[!UICONTROL Authentication]:** Specificate il metodo di autenticazione desiderato:  **[!UICONTROL None]**,  **[!UICONTROL Username/Password]** o  **[!UICONTROL SSH Key]**.
   * **[!UICONTROL HTTP Signature Header]:** Il nome dell&#39; [!DNL HTTP] intestazione, fornito dal cliente, che contiene la chiave  [!DNL HTTP] della firma. Il valore predefinito è [!UICONTROL X-Signature], come illustrato nell&#39;esempio seguente:

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

   * **[!UICONTROL HTTP Signature Key]:** Chiave utilizzata per firmare la  [!DNL HTTP] richiesta, fornita dal cliente.
   * **[!UICONTROL Show Signature Key]:** Attivare o disattivare la visualizzazione della firma nel browser.
   * **[!UICONTROL HTTP Signature Encryption Method]:** Specificare il metodo utilizzato per cifrare la firma. Utilizzare [!UICONTROL SHA1] a meno che il cliente non preferisca diversamente.

   >[!NOTE]
   >
   >Se si desidera abilitare l&#39;autenticazione [OAuth 2.0 per i trasferimenti di dati in tempo reale](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html) per un partner, compilare i campi come nella tabella seguente. I campi in *corsivo* devono essere compilati esattamente come nella tabella.

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
   | [!UICONTROL Username] | [!UICONTROL *Autorizzazione*] |
   | [!UICONTROL Password] | your_password_here |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. Fare clic su **[!UICONTROL Create]** se si sta creando un nuovo server, oppure fare clic su **[!UICONTROL Update]** se si sta modificando un server esistente.
