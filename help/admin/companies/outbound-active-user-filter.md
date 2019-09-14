---
description: Seguite queste istruzioni per generare un file di sincronizzazione completo che includa solo gli utenti attivi di recente. È possibile filtrare gli utenti attivi per inviare i dati rilevanti a un sistema di targeting locale o per limitare le dimensioni dei file inviati a un DSP. Non potete usare questo filtro con sincronizzazione incrementale.
seo-description: Seguite queste istruzioni per generare un file di sincronizzazione completo che includa solo gli utenti attivi di recente. È possibile filtrare gli utenti attivi per inviare i dati rilevanti a un sistema di targeting locale o per limitare le dimensioni dei file inviati a un DSP. Non potete usare questo filtro con sincronizzazione incrementale.
seo-title: Filtra dati in uscita solo per utenti attivi
title: Filtra dati in uscita solo per utenti attivi
uuid: a2b4a385-eee3-458c-b978-09509cacb397
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Filtra dati in uscita solo per utenti attivi {#filter-outbound-data-by-active-users-only}

Seguite queste istruzioni per generare un file di sincronizzazione completo che includa solo gli utenti attivi di recente. È possibile filtrare gli utenti attivi per inviare i dati rilevanti a un sistema di targeting locale o per limitare le dimensioni dei file inviati a un DSP. Non potete usare questo filtro con sincronizzazione incrementale.

>[!NOTE]
>
>Per qualificarsi come "attivo", non è necessario che un visitatore sia visto in un sito cliente selezionato o nel traffico dell'annuncio. Possono essere considerati "attivi" da qualsiasi [!DNL Audience Manager] cliente o partner.

Per filtrare solo per utenti attivi:

1. Fai clic su **[!UICONTROL Companies]**.
1. Selezionate la società con cui desiderate lavorare e fate clic **[!UICONTROL Destinations]**.
1. Nella [!UICONTROL Batch Data] sezione , impostate le seguenti opzioni:

   * **[!UICONTROL Sync Type]**: Selezionare **[!UICONTROL Customer]** o **[!UICONTROL Platform]**.
   * **[!UICONTROL Sync Type Lookback Period]**: Questo intervallo di tempo definisce l'intervallo del file di dati. Le scelte includono **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]**.
   * **[!UICONTROL Incremental Sync Scheduled Run]**: Selezionare **[!UICONTROL Never]**. Tenete presente che questo filtro si applica solo ai file di sincronizzazione completi.
   * **[!UICONTROL Full Sync Scheduled Run]**: Questo determina la frequenza di ricezione del file. Le scelte includono **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]** o **[!UICONTROL Never]** (per disattivare).

1. Fai clic su **[!UICONTROL Save]**.
