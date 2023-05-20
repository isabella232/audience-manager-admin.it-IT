---
description: Alcuni clienti potrebbero non voler fornire l’accesso Amazon Simple Storage Service (Amazon S3) o chiavi segrete ad Adobe per autorizzare il caricamento dei dati di destinazione nei propri bucket.
seo-description: Some customers may not want to provide their Amazon Simple Storage Service (Amazon S3) access or secret keys to Adobe to authorize destination data upload to their buckets.
seo-title: How To  Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations
title: Autorizzare l’accesso multiaccount al bucket Amazon S3 per le destinazioni batch
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
exl-id: f3b97c31-714f-4841-884b-bc507267a932
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Autorizzare l’accesso multiaccount al bucket Amazon S3 per le destinazioni batch{#authorize-cross-account-bucket-batch}

Alcuni clienti potrebbero non voler fornire i propri [!DNL Amazon S3] accesso o chiavi segrete da Adobe per autorizzare il caricamento dei dati di destinazione nei relativi bucket.

Un&#39;alternativa che possiamo offrire ai nostri clienti è [!UICONTROL Cross-Account Bucket Permissions] in [!DNL Amazon S3]. Questo processo è descritto nel [Documentazione di AWS](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html). Per abilitare questa alternativa in Audience Manager, effettua le seguenti operazioni:

1. Vai a **[!UICONTROL Servers]** e seleziona **[!UICONTROL Create Server]**.
1. Seleziona **[!UICONTROL S3]** nel **[!UICONTROL Protocol/Credentials]** maschera a discesa.
1. Controlla la **[!UICONTROL Use Internal Adobe Key]** opzione.
1. Utilizza l’account e il nome del bucket del cliente in [!DNL Amazon S3].
1. Assicurati che il tuo cliente elenchi il [!DNL Amazon S3] account `975822914085` sul loro [!DNL S3] secchio.

>[!NOTE]
>
>Il nostro editore in uscita garantisce che il livello di autorizzazione `bucket-owner-full-control` è impostato sui dati caricati, in modo che il cliente possa essere proprietario di tali dati.
