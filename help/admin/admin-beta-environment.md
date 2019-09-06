---
description: L'ambiente beta consente di testare le implementazioni di Audience Manager. Le modifiche apportate in beta non influiscono sui dati di produzione. L'ambiente beta di Audience Manager è una versione indipendente e standalone dell'ambiente di produzione. Tutti i dati da sottoporre a test devono essere inseriti e raccolti in questo ambiente.
seo-description: L'ambiente beta consente di testare le implementazioni di Audience Manager. Le modifiche apportate in beta non influiscono sui dati di produzione. L'ambiente beta di Audience Manager è una versione indipendente e standalone dell'ambiente di produzione. Tutti i dati da sottoporre a test devono essere inseriti e raccolti in questo ambiente.
seo-title: Ambiente beta
solution: Audience Manager
title: Ambiente beta
uuid: 6 a 253 f 4 e -96 e 7-4395-a 783-a 8 eb 213 b 7 daf
translation-type: tm+mt
source-git-commit: 7765dbf79c2fb6ca8c4b52fe8090c1fd11f9db27

---


# Ambiente beta {#beta-environment}

L'ambiente beta consente di testare le implementazioni di Audience Manager. Le modifiche apportate in beta non influiscono sui dati di produzione. L'ambiente beta di Audience Manager è una versione indipendente e standalone dell'ambiente di produzione. Tutti i dati da sottoporre a test devono essere inseriti e raccolti in questo ambiente.

## Panoramica {#overview}

<!-- beta_environment_admin.xml -->

| Servizio | URL/Nome host | Passaggi per la fornitura |
|--- |--- |--- |
| S3 |  | Consultate [Distribuzione di bucket Amazon S 3](admin-beta-environment.md#provision-s3-buckets). |
| DCS | https &amp; amp; due punti; // dcs-beta.demdex.net/.. | Non sono necessari passaggi aggiuntivi da parte nostra. Consultate [Accedere al DCS nell'ambiente Beta](admin-beta-environment.md#access-dcs-beta-environment). |
| Interfaccia | https &amp; amp; due punti; //bank-beta.demdex.com | I dati vengono copiati dalla produzione nell'ambiente beta su base mensile. Le credenziali di produzione sono valide per la versione beta. |
| API | https &amp; amp; due punti; // api-beta.demdex.com/.. | I dati vengono copiati dalla produzione nell'ambiente beta su base mensile. Le credenziali di produzione sono valide per la versione beta. |

## Fornitura di bucket Amazon S 3 {#provision-s3-buckets}

>[!NOTE]
>
>Ci stiamo allontanando dall'uso [!DNL FTP/SFTP]. Inoltre, tenete presente che i trasferimenti di dati in uscita non funzionano per l'ambiente beta.

Per i [!DNL S3] bucket per i dati in entrata:

1. Utilizzate la funzione [**SKMS Request techops Help**](https://skms.adobe.com/) .
1. Andate nella **[!UICONTROL Request TechOps Help]** barra di navigazione a sinistra.
1. In **[!UICONTROL Request Search]**, digita Audience Manager nel campo di ricerca.
1. Scorri verso il basso nei risultati della ricerca e fai clic in **Audience Manager - S 3 In ingresso/Provisioning account in uscita**.
1. Compilare i campi nella finestra di provisioning e specificare **l'ambiente Sandbox** nel **[!UICONTROL Environment]** campo.

>[!NOTE]
>
>Non incoraggiamo l'utilizzo [!DNL FTP/SFTP][!UICONTROL Amazon S3]e incoraggiamo l'utilizzo. I motivi per cui incoraggiamo l'utilizzo [!UICONTROL Amazon S3] sono elencati in [Amazon S 3: Informazioni](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html).

## Accesso al DCS nell'ambiente Beta {#access-dcs-beta-environment}

Per accedere all' [!UICONTROL DCS] ambiente Beta:

1. [!UICONTROL DCS] Effettuare una chiamata utilizzando il [!DNL curl][comando](https://curl.haxx.se/docs/manpage.html). [!DNL Curl] è uno strumento che consente di trasferire dati da o su un server utilizzando uno dei numerosi protocolli supportati.

   Ad esempio: `curl -v https://dcs-beta.demdex.net/event`

1. Verificate che la versione beta sia stata servita dalla versione beta [!UICONTROL DCS] cercando «[!DNL sandbox]nell'intestazione [!UICONTROL DCS] della risposta.

   Ad esempio:

   ```
   curl -v http://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```

<!--
1. Determine the load balancer's endpoint IP addresses.

   Run the `dig` [command](https://en.wikipedia.org/wiki/Dig_(command)) to determine the IP address of the nearest load balancer. The `dig` command queries the Domain Name System and returns the name and IP addresses of the Audience Manager [!UICONTROL Data Collection Servers (DCS)].

   ```
   dig dcs-beta.demdex.net
   ...
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.87.15.51
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 50.16.150.8
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.2.228.100
   ```

1. Using one of the addresses in the above table, add a static DNS entry in the [!DNL `/etc/hosts`] file.

   On Windows, modify [!DNL `c:\WINDOWS\system32\drivers\etc\hosts`].

   For example:

[!DNL `52.87.15.51 samplepartner.demdex.net`]

   >[!NOTE]
   >
   >The addresses change occasionally, so you must keep your [!DNL /etc/hosts] file up to date.

   Additionally, if you need to set up ID synchronization, you must add a similar entry for [!DNL dpm.demdex.net.]

[!DNL `52.87.15.51 dpm.demdex.net`] [!DNL]. 

1. Make a [!UICONTROL DCS] call, using the `curl` [command](https://curl.haxx.se/docs/manpage.html). Curl is a tool to transfer data from or to a server, using one of many supported protocols.

   For example:

[!DNL `https://<domain>/event?product=camera`] 

1. Verify that your request was served by the beta [!UICONTROL DCS] by looking for "sandbox" in the [!UICONTROL DCS] response header.

   For example:

   ```
   curl -v https://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```
-->