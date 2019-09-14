---
description: Utilizzate la pagina Server dello strumento di amministrazione di Audience Manager per creare un nuovo server HTTP o per modificare un server esistente.
seo-description: Utilizzate la pagina Server dello strumento di amministrazione di Audience Manager per creare un nuovo server HTTP o per modificare un server esistente.
seo-title: ' Creare o modificare un server HTTP'
title: ' Creare o modificare un server HTTP'
uuid: 1ef0e751-e239-4dc6-a4f6-73cc05686807
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# Creare o modificare un server HTTP {#create-or-edit-an-http-server}

Utilizzate la [!UICONTROL Servers] pagina nello strumento di amministrazione di Audience Manager per creare un nuovo server HTTP o per modificare un server esistente.

>[!NOTE]
>
>È necessario disporre del [!UICONTROL DEXADMIN] ruolo per creare nuovi server o modificare server esistenti.

1. Per creare un nuovo server, passate a **[!UICONTROL Servers]** &gt; **[!UICONTROL Create Server]**. Per modificare un server esistente, fate clic sul server desiderato nella **[!UICONTROL Label]** colonna.
1. Specificate l'etichetta desiderata per il server.
1. Dall'elenco a **[!UICONTROL Protocol]** discesa, selezionate il protocollo desiderato: [!DNL HTTP].
1. Compila i campi:

   * **[!UICONTROL Domain]** : Specificare il dominio desiderato (host) per il server.
   * **[!UICONTROL Port]** : Specificare la porta desiderata per il server. Per ogni tipo di crittografia viene visualizzata la porta predefinita. Se necessario, potete modificare la porta predefinita
   * **[!UICONTROL Maximum Users Per Request]** : Specificate il numero massimo di utenti per richiesta consentito per questo server.
   * **[!UICONTROL URL Prefix]** : Specificare il [!DNL URL] prefisso da utilizzare per il server.
   * **[!UICONTROL Authentication URL]** : Specificare il [!UICONTROL Authentication URL] server per il `HTTP` server.
   * **[!UICONTROL Authentication]** : Specificate il metodo di autenticazione desiderato: **[!UICONTROL None]**, **[!UICONTROL Username/Password]** o **[!UICONTROL SSH Key]**.
   * **[!UICONTROL HTTP Signature Header]** : Il nome dell' [!DNL HTTP] intestazione, fornito dal cliente, che contiene la chiave di [!DNL HTTP] firma. Il valore predefinito è [!UICONTROL X-Signature], come illustrato nell'esempio seguente:

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

   * **[!UICONTROL HTTP Signature Key]** : Chiave utilizzata per firmare la [!DNL HTTP] richiesta, fornita dal cliente.
   * **[!UICONTROL Show Signature Key]** : Attivare o disattivare la visualizzazione della firma nel browser.
   * **[!UICONTROL HTTP Signature Encryption Method]** : Specificare il metodo utilizzato per cifrare la firma. Utilizzarlo [!UICONTROL SHA1] a meno che il cliente non preferisca diversamente.
   >[!NOTE]
   >
   >Se desideri abilitare l'autenticazione [OAuth 2.0 per i trasferimenti](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html) di dati in tempo reale per un partner, compila i campi come nella tabella seguente. I campi in *corsivo* devono essere compilati esattamente come nella tabella.

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
   | [!UICONTROL Password] | your_password_here |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. Fate clic su **[!UICONTROL Create]** se state creando un nuovo server, oppure su **[!UICONTROL Update]** se state modificando un server esistente.