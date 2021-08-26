---
description: Le opzioni di Device Graph sono disponibili per le aziende che partecipano a Adobe Experience Cloud Device Co-op. Se un cliente ha anche una relazione contrattuale con un provider di grafici dei dispositivi di terze parti integrato con Audience Manager, questa sezione mostrerà le opzioni per quel grafico dei dispositivi. Queste opzioni si trovano in Aziende > nome società > Profilo > Opzioni grafico dei dispositivi.
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

Le [!UICONTROL Device Graph Options] sono disponibili per le aziende che partecipano al [!DNL Adobe Experience Cloud Device Co-op]. Se un cliente ha anche una relazione contrattuale con un provider di grafici dei dispositivi di terze parti integrato con Audience Manager, questa sezione mostrerà le opzioni per quel grafico dei dispositivi. Queste opzioni si trovano in [!UICONTROL Companies] > nome società > [!UICONTROL Profile] > [!UICONTROL Device Graph Options].

![](assets/adminUIdataSource.png)

Questa illustrazione utilizza nomi generici per le opzioni del grafico dei dispositivi di terze parti. In produzione, questi nomi provengono dal provider del grafico dei dispositivi e possono variare da quanto mostrato qui. Ad esempio, le opzioni [!DNL LiveRamp] di solito (ma non sempre):

* Inizia con &quot;[!DNL LiveRamp]&quot;
* Contiene un secondo nome che varia
* Fine con &quot;[!UICONTROL - Household]&quot; o &quot;[!UICONTROL -Person]&quot;

## Opzioni del grafico dei dispositivi definite {#device-graph-options-defined}

Le opzioni del grafico dei dispositivi selezionate qui espongono o nascondono le scelte [!UICONTROL Device Options] disponibili per un cliente [!DNL Audience Manager] quando crea un [!UICONTROL Profile Merge Rule].

### Co-op Device Graph {#co-op-graph}

I clienti che partecipano a [Adobe Experience Cloud Device Co-op](https://experienceleague.adobe.com/docs/device-co-op/using/about/overview.html?lang=en) utilizzano queste opzioni per creare un [!UICONTROL Profile Merge Rule] con [dati deterministici e probabilistici](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=en). L’ [!DNL Corporate Provisioning Team] attiva e disattiva questa opzione tramite una chiamata back-end [!DNL API] . Non è possibile selezionare o deselezionare queste caselle in [!DNL Admin UI]. Inoltre, le opzioni **[!UICONTROL Co-op Device Graph]** e **[!UICONTROL Company Device Graph]** si escludono a vicenda. I clienti possono chiedere di attivare uno o l’altro, ma non entrambi. Se questa opzione è selezionata, il controllo **[!UICONTROL Co-op Device Graph]** viene esposto nelle impostazioni [!UICONTROL Device Options] per un valore [!UICONTROL Profile Merge Rule].

![](assets/adminUI1.png)

### Grafico dei dispositivi aziendali {#company-graph}

Questa opzione è destinata ai clienti [!DNL Analytics] che utilizzano la metrica [!UICONTROL People] nella suite di rapporti [!DNL Analytics]. L’ [!DNL Corporate Provisioning Team] attiva e disattiva questa opzione tramite una chiamata back-end [!DNL API] . Non è possibile selezionare o deselezionare queste caselle in [!DNL Admin UI]. Inoltre, le opzioni **[!UICONTROL Company Device Graph]** e **[!UICONTROL Co-op Device Graph]** si escludono a vicenda. I clienti possono chiedere di attivare uno o l’altro, ma non entrambi. Se selezionata:

* Questo grafico dei dispositivi utilizza dati deterministici appartenenti alla società che stai configurando (nessun dato probabilistico).
* [!DNL Audience Manager] crea automaticamente un  [!UICONTROL Data Source] nome  `*`partner`*-Company Device Graph-Person`. Nella pagina dei dettagli [!UICONTROL Data Source] i clienti [!DNL Audience Manager] possono modificare il nome e la descrizione del partner e applicare [Controlli sull&#39;esportazione dei dati](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=en) a questa origine dati.
* [!DNL Audience Manager] i clienti  *non* vedono una nuova impostazione nella  [!UICONTROL Device Options] sezione per una  [!UICONTROL Profile Merge Rule].

### Grafico dei dispositivi LiveRamp (persona o famiglia) {#liveramp-device-graph}

Queste caselle di controllo sono abilitate in [!DNL Admin UI] quando un partner crea un [!UICONTROL Data Source] e seleziona **[!UICONTROL Use as an Authenticated Profile]** e/o **[!UICONTROL Use as a Device Graph]**. I nomi di queste impostazioni sono determinati dal provider di grafici dei dispositivi di terze parti (ad esempio, [!DNL LiveRamp], [!DNL TapAd], ecc.). Se questa opzione è selezionata, la società che si sta configurando utilizzerà i dati forniti da questi grafici dei dispositivi.

![](assets/adminUI2.png)

>[!MORELIKETHIS]
>
>* [Definizione delle opzioni delle regole di unione profili](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/merge-rule-definitions.html?lang=en).
>* [Impostazioni origine dati e opzioni menu](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html?lang=en)

