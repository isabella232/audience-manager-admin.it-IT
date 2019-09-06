---
description: Alcuni clienti potrebbero non voler fornire i propri accessi Amazon Simple Storage Service (Amazon S 3) o segreti ad Adobe per autorizzare i dati di destinazione nei loro bucket.
seo-description: Alcuni clienti potrebbero non voler fornire i propri accessi Amazon Simple Storage Service (Amazon S 3) o segreti ad Adobe per autorizzare i dati di destinazione nei loro bucket.
seo-title: Come autorizzare l'accesso incrociato Amazon S 3 Bucket per destinazioni batch
title: Come autorizzare l'accesso incrociato Amazon S 3 Bucket per destinazioni batch
uuid: da 2 bcbda-a 765-437 a-bfe 9-4355383 a 4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Come autorizzare l'accesso incrociato Amazon S 3 Bucket per destinazioni batch{#authorize-cross-account-bucket-batch}

Alcuni clienti potrebbero non voler fornire ad Adobe la propria [!DNL Amazon S3] chiave segreta o segreta per autorizzare i dati di destinazione.

Un'alternativa in cui possiamo offrire [!UICONTROL Cross-Account Bucket Permissions] i nostri clienti [!DNL Amazon S3]. Questo processo è descritto nella documentazione [AWS](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html). Per abilitare questa alternativa in Audience Manager, segui i passaggi seguenti:

1. Vai a **[!UICONTROL Servers]** e seleziona **[!UICONTROL Create Server]**.
1. Selezionate **[!UICONTROL S3]** nella maschera **[!UICONTROL Protocol/Credentials]** a discesa.
1. Controllare **[!UICONTROL Use Internal Adobe Key]** l'opzione.
1. Utilizzate l'account del cliente e il nome del bucket in [!DNL Amazon S3].
1. Accertatevi che il white list del cliente sia in grado di elencare [!DNL Amazon S3] l'account `975822914085` sul [!DNL S3] suo bucket.

>[!NOTE]
>
>Il nostro editore in uscita garantisce che il livello di autorizzazione `bucket-owner-full-control` sia impostato sui dati caricati, in modo che il cliente possa possedere tali dati.
