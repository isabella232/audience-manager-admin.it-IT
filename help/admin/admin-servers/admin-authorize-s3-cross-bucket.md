---
description: Alcuni clienti potrebbero non voler fornire il proprio accesso  Amazon Simple Storage Service ( Amazon S3) o le chiavi segrete per  Adobe per autorizzare il caricamento dei dati di destinazione nei loro bucket.
seo-description: Alcuni clienti potrebbero non voler fornire il proprio accesso  Amazon Simple Storage Service ( Amazon S3) o le chiavi segrete per  Adobe per autorizzare il caricamento dei dati di destinazione nei loro bucket.
seo-title: Come autorizzare l'accesso a intervalli  conto incrociato per Amazon S3 per le destinazioni batch
title: Come autorizzare l'accesso a intervalli  conto incrociato per Amazon S3 per le destinazioni batch
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# Come autorizzare l&#39;accesso a intervalli di  Amazon S3 per le destinazioni batch{#authorize-cross-account-bucket-batch}

Alcuni clienti potrebbero non voler fornire le chiavi di accesso o di segreto [!DNL Amazon S3] al Adobe per  di autorizzare il caricamento dei dati di destinazione nei loro bucket.

Un&#39;alternativa che possiamo offrire ai nostri clienti è [!UICONTROL Cross-Account Bucket Permissions] in [!DNL Amazon S3]. Questo processo è descritto nella [documentazione AWS](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html). Per attivare questa alternativa in  Audience Manager, procedere come segue:

1. Fare clic su **[!UICONTROL Servers]** e selezionare **[!UICONTROL Create Server]**.
1. Selezionare **[!UICONTROL S3]** nella maschera a discesa **[!UICONTROL Protocol/Credentials]**.
1. Selezionare l&#39;opzione **[!UICONTROL Use Internal Adobe Key]**.
1. Utilizza l&#39;account del cliente e il nome del bucket in [!DNL Amazon S3].
1. Accertatevi che il cliente disponga di un elenco bianco dell&#39;account [!DNL Amazon S3] `975822914085` nel periodo fisso [!DNL S3].

>[!NOTE]
>
>Il nostro editore in uscita garantisce che il livello di autorizzazione `bucket-owner-full-control` sia impostato sui dati caricati, in modo che il cliente possa detenere tali dati.
