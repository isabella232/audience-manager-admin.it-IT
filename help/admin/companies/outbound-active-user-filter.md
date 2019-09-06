---
description: Per generare un file di sincronizzazione completo che includa solo gli utenti attivi di recente, effettuate le seguenti operazioni. Potrebbe essere utile filtrare gli utenti attivi per inviare dati pertinenti a un sistema di targeting on-site o per limitare le dimensioni dei file inviati a una DSP. Non potete usare questo filtro con sincronizzazione incrementale.
seo-description: Per generare un file di sincronizzazione completo che includa solo gli utenti attivi di recente, effettuate le seguenti operazioni. Potrebbe essere utile filtrare gli utenti attivi per inviare dati pertinenti a un sistema di targeting on-site o per limitare le dimensioni dei file inviati a una DSP. Non potete usare questo filtro con sincronizzazione incrementale.
seo-title: Filtrare i dati in uscita solo per utenti attivi
title: Filtrare i dati in uscita solo per utenti attivi
uuid: a 2 b 4 a 385-eee 3-458 c-b 978-09509 cacb 397
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Filtrare i dati in uscita solo per utenti attivi {#filter-outbound-data-by-active-users-only}

Per generare un file di sincronizzazione completo che includa solo gli utenti attivi di recente, effettuate le seguenti operazioni. Potrebbe essere utile filtrare gli utenti attivi per inviare dati pertinenti a un sistema di targeting on-site o per limitare le dimensioni dei file inviati a una DSP. Non potete usare questo filtro con sincronizzazione incrementale.

>[!NOTE]
>
>Un visitatore non deve essere visualizzato su un sito cliente selezionato o nel traffico pubblicitario per qualificarlo come «attivo». Possono essere visti da [!DNL Audience Manager] qualsiasi cliente o partner per qualificarlo come «attivo».

Per filtrare solo gli utenti attivi:

1. Fai clic su **[!UICONTROL Companies]**.
1. Selezionate la società con cui desiderate lavorare e fate clic **[!UICONTROL Destinations]** su.
1. Nella [!UICONTROL Batch Data] sezione, impostate le seguenti opzioni:

   * **[!UICONTROL Sync Type]**: Seleziona **[!UICONTROL Customer]** o **[!UICONTROL Platform]**.
   * **[!UICONTROL Sync Type Lookback Period]**: Questo intervallo di tempo definisce l'intervallo del file di dati. Le opzioni includono **[!UICONTROL 24 hours]****[!UICONTROL 7 days]****[!UICONTROL 30 days]**.
   * **[!UICONTROL Incremental Sync Scheduled Run]**: Seleziona **[!UICONTROL Never]**. Ricorda che questo filtro si applica solo ai file di sincronizzazione completi.
   * **[!UICONTROL Full Sync Scheduled Run]**: Questo determina la frequenza con cui si desidera ricevere questo file. Le scelte includono **[!UICONTROL 24 hours]****[!UICONTROL 7 days]****[!UICONTROL 30 days]**, o **[!UICONTROL Never]** (per disabilitare).

1. Fai clic su **[!UICONTROL Save]**.
