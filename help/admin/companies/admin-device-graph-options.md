---
description: Le opzioni di Device Graph sono disponibili per le società che partecipano ad Adobe Experience Cloud Device Co-op. Se un cliente ha anche una relazione contrattuale con un fornitore di grafici per dispositivi di terze parti integrato con  Audience Manager, questa sezione mostrerà le opzioni per quel grafico per dispositivi. Queste opzioni si trovano in Società > Nome società > Profilo > Opzioni di Device Graph.
seo-description: Le opzioni di Device Graph sono disponibili per le società che partecipano ad Adobe Experience Cloud Device Co-op. Se un cliente ha anche una relazione contrattuale con un fornitore di grafici per dispositivi di terze parti integrato con  Audience Manager, questa sezione mostrerà le opzioni per quel grafico per dispositivi. Queste opzioni si trovano in Società > Nome società > Profilo > Opzioni di Device Graph.
seo-title: Opzioni di Device Graph per le società
title: Opzioni di Device Graph per le società
uuid: a8ced843-710c-4a8f-a0d7-ea89d010a7a5
translation-type: tm+mt
source-git-commit: 2998dc049971b2fac8c45ca6e3118ea607ae3f92
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 3%

---


# Opzioni di Device Graph per le società {#device-graph-options-for-companies}

Le [!UICONTROL Device Graph Options] sono disponibili per le società che partecipano alla [!DNL Adobe Experience Cloud Device Co-op]. Se un cliente ha anche una relazione contrattuale con un fornitore di grafici per dispositivi di terze parti integrato con  Audience Manager, questa sezione mostrerà le opzioni per quel grafico per dispositivi. Queste opzioni si trovano in [!UICONTROL Companies] > nome società > [!UICONTROL Profile] > [!UICONTROL Device Graph Options].

![](assets/adminUIdataSource.png)

Nell&#39;illustrazione sono utilizzati nomi generici per le opzioni del grafico del dispositivo di terze parti. In produzione, questi nomi provengono dal provider di grafici del dispositivo e possono variare da quanto mostrato qui. Ad esempio, le opzioni [!DNL LiveRamp] in genere (ma non sempre):

* Inizia con &quot;[!DNL LiveRamp]&quot;
* Contiene un secondo nome che varia
* Fine con &quot;[!UICONTROL - Household]&quot; o &quot;[!UICONTROL -Person]&quot;

## Opzioni di Device Graph definite {#device-graph-options-defined}

Le opzioni del grafico del dispositivo selezionate qui espongono o nascondono le scelte [!UICONTROL Device Options] disponibili per un cliente [!DNL Audience Manager] quando crea un [!UICONTROL Profile Merge Rule].

### Co-op Device Graph {#co-op-graph}

I clienti che partecipano a [Adobe Experience Cloud Device Co-op](https://marketing.adobe.com/resources/help/en_US/mcdc/) utilizzano queste opzioni per creare un [!UICONTROL Profile Merge Rule] con [dati deterministici e probabilistici](https://marketing.adobe.com/resources/help/en_US/mcdc/mcdc-links.html). L&#39;opzione [!DNL Corporate Provisioning Team] attiva e disattiva questa opzione tramite una chiamata back-end [!DNL API]. Non è possibile selezionare o deselezionare queste caselle in [!DNL Admin UI]. Inoltre, le opzioni **[!UICONTROL Co-op Device Graph]** e **[!UICONTROL Company Device Graph]** si escludono a vicenda. I clienti possono chiederci di attivare uno o l&#39;altro, ma non entrambi. Se questa opzione è selezionata, il controllo **[!UICONTROL Co-op Device Graph]** viene esposto nelle impostazioni [!UICONTROL Device Options] per un [!UICONTROL Profile Merge Rule].

![](assets/adminUI1.png)

### Grafico del dispositivo della società {#company-graph}

Questa opzione è destinata ai clienti [!DNL Analytics] che utilizzano la metrica [!UICONTROL People] nella suite di rapporti [!DNL Analytics]. L&#39;opzione [!DNL Corporate Provisioning Team] attiva e disattiva questa opzione tramite una chiamata back-end [!DNL API]. Non è possibile selezionare o deselezionare queste caselle in [!DNL Admin UI]. Inoltre, le opzioni **[!UICONTROL Company Device Graph]** e **[!UICONTROL Co-op Device Graph]** si escludono a vicenda. I clienti possono chiederci di attivare uno o l&#39;altro, ma non entrambi. Se selezionato:

* Questo grafico del dispositivo utilizza dati deterministici appartenenti alla società che si sta configurando (nessun dato probabilistico).
* [!DNL Audience Manager] crea automaticamente un  [!UICONTROL Data Source] nome  `*`partner`*-Company Device Graph-Person`. Nella pagina [!UICONTROL Data Source] dei dettagli, [!DNL Audience Manager] i clienti possono cambiare il nome del partner, la descrizione e applicare [Controlli sull&#39;esportazione dei dati](https://marketing.adobe.com/resources/help/en_US/aam/c_dec.html) a questa origine dati.
* [!DNL Audience Manager] i clienti  *non* visualizzano una nuova impostazione nella  [!UICONTROL Device Options] sezione per un  [!UICONTROL Profile Merge Rule].

### Grafico dispositivo LiveRamp (Persona o Famiglia) {#liveramp-device-graph}

Queste caselle di controllo sono abilitate in [!DNL Admin UI] quando un partner crea un [!UICONTROL Data Source] e seleziona **[!UICONTROL Use as an Authenticated Profile]** e/o **[!UICONTROL Use as a Device Graph]**. I nomi di queste impostazioni sono determinati dal provider di grafici per dispositivi di terze parti (ad esempio, [!DNL LiveRamp], [!DNL TapAd], ecc.). Se questa opzione è selezionata, la società che si sta configurando utilizzerà i dati forniti da questi grafici del dispositivo.

![](assets/adminUI2.png)

>[!MORELIKETHIS]
>
>* [Definizione delle opzioni delle regole di unione profili](https://marketing.adobe.com/resources/help/en_US/aam/merge-rule-definitions.html).
>* [Impostazioni origine dati e opzioni menu](https://marketing.adobe.com/resources/help/en_US/aam/datasource-settings-definitions.html)

