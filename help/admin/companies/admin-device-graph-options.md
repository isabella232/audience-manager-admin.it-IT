---
description: Le opzioni di Device Graph sono disponibili per le aziende che partecipano a Adobe Experience Cloud Device Co-op. Se un cliente ha anche una relazione contrattuale con un fornitore di grafico dei dispositivi di terze parti integrato con Audience Manager, questa sezione mostrerà le opzioni per tale grafico dei dispositivi. Queste opzioni si trovano in Aziende > Nome società > Profilo > Opzioni del grafico dei dispositivi.
seo-description: The Device Graph Options are available to companies that participate in the Adobe Experience Cloud Device Co-op. If a customer also has a contractual relationship with a third-party device graph provider that is integrated with Audience Manager, this section will show options for that device graph. These options are located in Companies > company name > Profile > Device Graph Options.
seo-title: Device Graph Options for Companies
title: Opzioni di Device Graph per le società
uuid: a8ced843-710c-4a8f-a0d7-ea89d010a7a5
exl-id: 2502f3d2-b43c-410c-acb6-03c2a2ba2c1d
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 3%

---

# Opzioni di Device Graph per le società {#device-graph-options-for-companies}

Il [!UICONTROL Device Graph Options] sono disponibili per le aziende che partecipano al [!DNL Adobe Experience Cloud Device Co-op]. Se un cliente ha anche una relazione contrattuale con un fornitore di grafico dei dispositivi di terze parti integrato con Audience Manager, questa sezione mostrerà le opzioni per tale grafico dei dispositivi. Queste opzioni si trovano in [!UICONTROL Companies] > nome dell&#39;azienda > [!UICONTROL Profile] > [!UICONTROL Device Graph Options].

![](assets/adminUIdataSource.png)

Questa illustrazione utilizza nomi generici per le opzioni del grafico dei dispositivi di terze parti. In produzione, questi nomi provengono dal provider del grafico dei dispositivi e possono variare rispetto a quanto mostrato qui. Ad esempio, il [!DNL LiveRamp] opzioni di solito (ma non sempre):

* Inizia con &quot;[!DNL LiveRamp]&quot;
* Contengono un secondo nome che varia
* Termina con &quot;[!UICONTROL - Household]&quot; o &quot;[!UICONTROL -Person]&quot;

## Opzioni di Device Graph definite {#device-graph-options-defined}

Le opzioni del grafico dei dispositivi selezionate qui espongono o nascondono il [!UICONTROL Device Options] opzioni disponibili per un [!DNL Audience Manager] cliente quando crea un [!UICONTROL Profile Merge Rule].

### Grafico dei dispositivi Co-op {#co-op-graph}

Clienti che partecipano al [Adobe Experience Cloud Device Co-op](https://experienceleague.adobe.com/docs/device-co-op/using/about/overview.html?lang=en) utilizzare queste opzioni per creare un [!UICONTROL Profile Merge Rule] con [dati deterministici e probabilistici](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=en). Il [!DNL Corporate Provisioning Team] attiva e disattiva questa opzione tramite un back-end [!DNL API] chiamare. Non è possibile selezionare o deselezionare queste caselle nella [!DNL Admin UI]. Inoltre, il **[!UICONTROL Co-op Device Graph]** e **[!UICONTROL Company Device Graph]** le opzioni si escludono a vicenda. I clienti possono chiederci di attivare uno o l’altro, ma non entrambi. Se questa opzione è selezionata, il messaggio mostra **[!UICONTROL Co-op Device Graph]** controllo in [!UICONTROL Device Options] impostazioni per un [!UICONTROL Profile Merge Rule].

![](assets/adminUI1.png)

### Grafico dei dispositivi della società {#company-graph}

Questa opzione è per [!DNL Analytics] clienti che utilizzano [!UICONTROL People] metrica nella loro [!DNL Analytics] suite di rapporti. Il [!DNL Corporate Provisioning Team] attiva e disattiva questa opzione tramite un back-end [!DNL API] chiamare. Non è possibile selezionare o deselezionare queste caselle nella [!DNL Admin UI]. Inoltre, il **[!UICONTROL Company Device Graph]** e **[!UICONTROL Co-op Device Graph]** le opzioni si escludono a vicenda. I clienti possono chiederci di attivare uno o l’altro, ma non entrambi. Se questa opzione è selezionata:

* Questo grafico dei dispositivi utilizza dati deterministici che appartengono all’azienda che stai configurando (nessun dato probabilistico).
* [!DNL Audience Manager] crea automaticamente un [!UICONTROL Data Source] ha chiamato `*`nome partner`*-Company Device Graph-Person`. In [!UICONTROL Data Source] pagina dei dettagli, [!DNL Audience Manager] i clienti possono modificare il nome, la descrizione e applicare il partner [Controlli sull’esportazione dei dati](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=en) a questa origine dati.
* [!DNL Audience Manager] clienti *non* visualizzare una nuova impostazione in [!UICONTROL Device Options] sezione per un [!UICONTROL Profile Merge Rule].

### Grafico dei dispositivi LiveRamp (persona o famiglia) {#liveramp-device-graph}

Queste caselle di controllo sono attivate nel [!DNL Admin UI] quando un partner crea un [!UICONTROL Data Source] e seleziona **[!UICONTROL Use as an Authenticated Profile]** e/o **[!UICONTROL Use as a Device Graph]**. I nomi di queste impostazioni sono determinati dal provider del grafico dei dispositivi di terze parti (ad esempio, [!DNL LiveRamp], [!DNL TapAd], ecc.). Se questa opzione è selezionata, significa che l’azienda che stai configurando utilizzerà i dati forniti da questi grafici dei dispositivi.

![](assets/adminUI2.png)

>[!MORELIKETHIS]
>
>* [Definizione delle opzioni delle regole di unione profili](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/merge-rule-definitions.html?lang=en).
>* [Impostazioni origine dati e opzioni menu](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html?lang=en)

