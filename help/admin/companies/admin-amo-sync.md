---
description: Per impostazione predefinita, tutte le aziende sincronizzano i dati con Adobe Media Optimizer (AMO). Nell’interfaccia utente di amministrazione, ogni contenitore aziendale dispone di un’origine dati che gestisce questo processo. Questa origine dati è Adobe AMO (ID 411). Fai clic su una riga contenitore (sotto la scheda Contenitori) per consentire a una società selezionata di disabilitare questa sincronizzazione predefinita o di aggiungere e rimuovere altre origini dati al processo di sincronizzazione AMO.
seo-description: By default, all companies sync data with Adobe Media Optimizer (AMO). In the Admin UI, each company container has a data source that manages this process. This data source is Adobe AMO (ID 411). Click a container row (under the Containers tab) for a selected company to disable this default sync or to add and remove other data sources to the AMO sync process.
seo-title: ID Syncing with Media Optimizer
title: Sincronizzazione ID con Media Optimizer
uuid: b741dfa7-2947-4288-b214-79eccf18d53a
exl-id: ebd978ef-3825-4a96-94bd-5cdae269cf7c
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 6%

---

# Sincronizzazione ID con Media Optimizer {#id-syncing-with-media-optimizer}

Per impostazione predefinita, tutte le aziende sincronizzano i dati con [!DNL Adobe Media Optimizer] ([!DNL AMO]). In [!UICONTROL Admin UI], ogni contenitore aziendale dispone di un’origine dati che gestisce questo processo. Questa origine dati è [!UICONTROL Adobe AMO] ([!UICONTROL ID] 411). Fai clic su una riga contenitore (sotto [!UICONTROL Containers] ) per consentire a una società selezionata di disabilitare questa sincronizzazione predefinita o di aggiungere e rimuovere altre origini dati [!DNL AMO] processo di sincronizzazione.

![](assets/id-sync.png)

## Stato sincronizzazione ID {#id-sync-status}

Nella tabella seguente viene descritto lo stato di sincronizzazione di un&#39;origine dati.

| Stato | Descrizione |
|------ | -------- |
| Disattivato | Rimuovi tutte le origini dati da [!UICONTROL Selected Data Sources] affinché questo contenitore possa disabilitare le sincronizzazioni ID con [!DNL AMO] |
| Attivato (a prescindere dalla versione del servizio ID) | Un’origine dati si sincronizza con [!DNL AMO] indipendentemente dalla versione del servizio ID quando: <ul><li>L&#39;origine dati viene visualizzata nella [!UICONTROL Selected Data Sources] elenco.</li><li>Il [!DNL AMO] casella di controllo *non è* selezionato.</li></ul> |
| Attivato (a prescindere dalla versione del servizio ID) | Un’origine dati verrà sincronizzata con [!DNL AMO] con la versione 2.0 (o successiva) del servizio ID quando: <ul><li>L&#39;origine dati viene visualizzata nella [!UICONTROL Selected Data Sources] elenco.</li><li>Il [!DNL AMO] casella di controllo *è* selezionato.</li></ul> |

>[!MORELIKETHIS]
>
>* [Gestire i contenitori](../companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967)

