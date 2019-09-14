---
description: L’ambiente beta è destinato a testare le implementazioni di Audience Manager. Le modifiche apportate nella versione beta non influiscono sui dati di produzione. L’ambiente beta di Audience Manager è una versione autonoma e su scala ridotta dell’ambiente di produzione. Tutti i dati da sottoporre a test devono essere immessi e raccolti in questo ambiente.
seo-description: L’ambiente beta è destinato a testare le implementazioni di Audience Manager. Le modifiche apportate nella versione beta non influiscono sui dati di produzione. L’ambiente beta di Audience Manager è una versione autonoma e su scala ridotta dell’ambiente di produzione. Tutti i dati da sottoporre a test devono essere immessi e raccolti in questo ambiente.
seo-title: Ambiente beta
solution: Audience Manager
title: Ambiente beta
uuid: 6a253f4e-96e7-4395-a783-a8eb213b7daf
translation-type: tm+mt
source-git-commit: 7765dbf79c2fb6ca8c4b52fe8090c1fd11f9db27

---


# Ambiente beta {#beta-environment}

L’ambiente beta è destinato a testare le implementazioni di Audience Manager. Le modifiche apportate nella versione beta non influiscono sui dati di produzione. L’ambiente beta di Audience Manager è una versione autonoma e su scala ridotta dell’ambiente di produzione. Tutti i dati da sottoporre a test devono essere immessi e raccolti in questo ambiente.

## Panoramica {#overview}

<!-- beta_environment_admin.xml -->

| Servizio | URL/Nome host | Passaggi per il provisioning |
|--- |--- |--- |
| S3 |  | Consultate [Provisioning dei rilegi Amazon S3](admin-beta-environment.md#provision-s3-buckets). |
| DCS | https&amp;due punti;//dcs-beta.demdex.net/... | Non sono necessari ulteriori passi da parte nostra. Consultate [Accedere al DCS in ambiente](admin-beta-environment.md#access-dcs-beta-environment)Beta. |
| Interfaccia | https&amp;due punti;//bank-beta.demdex.com | I dati vengono copiati mensilmente dalla produzione all'ambiente Beta. Le credenziali di produzione sono valide per la versione beta. |
| API | https&amp;due punti;//api-beta.demdex.com/... | I dati vengono copiati mensilmente dalla produzione all'ambiente Beta. Le credenziali di produzione sono valide per la versione beta. |

## Provisioning di pacchetti Amazon S3 {#provision-s3-buckets}

>[!NOTE]
>
>Ci stiamo allontanando dall'uso [!DNL FTP/SFTP]. Inoltre, i trasferimenti di dati in uscita non funzionano per l'ambiente Beta.

Per eseguire il provisioning dei [!DNL S3] bucket per i dati in entrata:

1. Utilizzate la funzione [**SKMS Request TechOps Help**](https://skms.adobe.com/) .
1. Passate **[!UICONTROL Request TechOps Help]** alla barra di navigazione a sinistra.
1. In **[!UICONTROL Request Search]**, digitate in Audience Manager nel campo di ricerca.
1. Scorri verso il basso nei risultati della ricerca e fai clic su **Audience Manager - S3 Inbound / Outbound Account Provisioning**.
1. Compilate i campi nella finestra di provisioning e specificate l'ambiente **** sandbox nel **[!UICONTROL Environment]** campo.

>[!NOTE]
>
>Scoraggiamo l'uso [!DNL FTP/SFTP] e incoraggiamo l'uso di [!UICONTROL Amazon S3]. I motivi per cui incoraggiamo l'uso di [!UICONTROL Amazon S3] sono elencati in [Amazon S3:About](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html).

## Accesso al DCS in ambiente Beta {#access-dcs-beta-environment}

Per accedere all'ambiente [!UICONTROL DCS] Beta:

1. Effettuare una [!UICONTROL DCS] chiamata utilizzando il [!DNL curl][comando](https://curl.haxx.se/docs/manpage.html). [!DNL Curl] è uno strumento per trasferire dati da o verso un server, utilizzando uno dei numerosi protocolli supportati.

   Ad esempio: `curl -v https://dcs-beta.demdex.net/event`

1. Verificate che la richiesta sia stata trasmessa dalla versione beta [!UICONTROL DCS] cercando "[!DNL sandbox]" nell’intestazione della [!UICONTROL DCS] risposta.

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