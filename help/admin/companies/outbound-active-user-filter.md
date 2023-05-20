---
description: Seguire queste istruzioni per generare un file di sincronizzazione completo che includa solo gli utenti attivi di recente. Puoi filtrare i dati per consentire agli utenti attivi di inviarli a un sistema di targeting interno al sito o per limitare le dimensioni dei file inviati a un DSP. Impossibile utilizzare questo filtro con la sincronizzazione incrementale.
seo-description: Follow these instructions to generate a full synchronization file that includes recently active users only. You may want to filter for active users to push relevant data to an on-site targeting system or to limit the size of the files sent to a DSP. You cannot use this filter with incremental synchronization.
seo-title: Filter Outbound Data by Active Users Only
title: Filtrare i dati in uscita solo per gli utenti attivi
uuid: a2b4a385-eee3-458c-b978-09509cacb397
exl-id: d501cfd1-64dd-448e-92c5-180c0081d3e5
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 7%

---

# Filtrare i dati in uscita solo per gli utenti attivi {#filter-outbound-data-by-active-users-only}

Seguire queste istruzioni per generare un file di sincronizzazione completo che includa solo gli utenti attivi di recente. Puoi filtrare i dati per consentire agli utenti attivi di inviarli a un sistema di targeting interno al sito o per limitare le dimensioni dei file inviati a un DSP. Impossibile utilizzare questo filtro con la sincronizzazione incrementale.

>[!NOTE]
>
>Per essere considerato &quot;attivo&quot;, un visitatore non deve necessariamente essere visualizzato sul sito di un cliente selezionato o nel relativo traffico pubblicitario. Possono essere viste da qualsiasi [!DNL Audience Manager] cliente o partner per qualificarsi come &quot;attivi&quot;.

Per filtrare solo in base agli utenti attivi:

1. Clic **[!UICONTROL Companies]**.
1. Seleziona la società con cui desideri lavorare e fai clic su **[!UICONTROL Destinations]**.
1. In [!UICONTROL Batch Data] , impostare le opzioni seguenti:

   * **[!UICONTROL Sync Type]**: Seleziona **[!UICONTROL Customer]** o **[!UICONTROL Platform]**.
   * **[!UICONTROL Sync Type Lookback Period]**: questo intervallo di tempo definisce l’intervallo del file di dati. Le scelte includono **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]**.
   * **[!UICONTROL Incremental Sync Scheduled Run]**: Select **[!UICONTROL Never]**. Questo filtro si applica solo ai file di sincronizzazione completa.
   * **[!UICONTROL Full Sync Scheduled Run]**: questo determina la frequenza con cui desideri ricevere questo file. Le scelte includono **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]**, o **[!UICONTROL Never]** (per disattivare).

1. Clic **[!UICONTROL Save]**.
