---
description: Alcuni clienti potrebbero non voler fornire ad Adobe il proprio accesso Amazon Simple Storage Service (Amazon S3) o le chiavi segrete per autorizzare il caricamento dei dati di destinazione nei loro bucket.
seo-description: Alcuni clienti potrebbero non voler fornire ad Adobe il proprio accesso Amazon Simple Storage Service (Amazon S3) o le chiavi segrete per autorizzare il caricamento dei dati di destinazione nei loro bucket.
seo-title: Come autorizzare l'accesso a intervalli tra account Amazon S3 per le destinazioni batch
title: Come autorizzare l'accesso a intervalli tra account Amazon S3 per le destinazioni batch
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# How To Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations{#authorize-cross-account-bucket-batch}

Alcuni clienti potrebbero non voler fornire ad Adobe le chiavi di [!DNL Amazon S3] accesso o di segreto per autorizzare il caricamento dei dati di destinazione nei loro bucket.

Un&#39;alternativa che possiamo offrire ai nostri clienti è [!UICONTROL Cross-Account Bucket Permissions] in [!DNL Amazon S3]. Questo processo è descritto nella documentazione [di](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html)AWS. Per attivare questa alternativa in  Audience Manager, procedere come segue:

1. Vai a **[!UICONTROL Servers]** e seleziona **[!UICONTROL Create Server]**.
1. Seleziona **[!UICONTROL S3]** nella maschera a **[!UICONTROL Protocol/Credentials]** discesa.
1. Selezionare l&#39; **[!UICONTROL Use Internal Adobe Key]** opzione.
1. Utilizza l&#39;account del cliente e il nome del bucket in [!DNL Amazon S3].
1. Accertatevi che il cliente disponga di un elenco bianco [!DNL Amazon S3] dell&#39;account `975822914085` nel [!DNL S3] bucket.

>[!NOTE]
>
>Il nostro editore in uscita garantisce che il livello di autorizzazione `bucket-owner-full-control` sia impostato sui dati caricati, in modo che il cliente possa detenere tali dati.
