---
description: 'Usa Registrazione audit come prima posizione per il debug dei problemi dei clienti. '
seo-description: 'Usa Registrazione audit come prima posizione per il debug dei problemi dei clienti. '
seo-title: Registrazione di controllo
title: Registrazione di controllo
uuid: null
translation-type: tm+mt
source-git-commit: 190ba5c1215782e46c8e544c10679d451fbed134

---


# Registrazione di controllo {#audit-logging}

Utilizzate [!UICONTROL  Audit Logging] come prima posizione per il debug dei problemi dei clienti.

> [!NOTE]
>
>[!UICONTROL Audit Logging] è attualmente in fase di sviluppo e soggetta a modifiche. Please log any issues you meet in [!DNL JIRA] ([!DNL UI] team)

![Visualizzazione Registrazione di controllo](assets/audit-logging-img.png)

Nel **selettore** a discesa Tipo di controllo, scegliere tra:

* [!UICONTROL Partner]
* [!UICONTROL User]
* [!UICONTROL Group]
* [!UICONTROL Datasource Summary]
* [!UICONTROL General Datasource]
* [!UICONTROL Merge Rule Datasource]
* [!UICONTROL Data Feed]
* [!UICONTROL Data Feed Subscription]
* [!UICONTROL Trait Summary]
* [!UICONTROL Trait Rule]
* [!UICONTROL Segment Summary]
* [!UICONTROL Destination Summary]
* [!UICONTROL Server to Server Destination]
* [!UICONTROL Derived Signal]
* [!UICONTROL Model]
* [!UICONTROL Segment Test Group]

L'ID **oggetto** è l'ID dell'elemento che stai cercando. Consultate la tabella seguente per quale ID corrisponde all'ID oggetto in ciascun caso:

| Tipo di controllo | ID oggetto |
---------|----------|
| [!UICONTROL Partner] | ID partner - PID |
| [!UICONTROL User] | ID utente |
| [!UICONTROL Group] | B3 |
| [!UICONTROL Datasource Summary] | ID origine dati |
| [!UICONTROL General Datasource] | ID origine dati |
| [!UICONTROL Merge Rule Datasource] | ID origine dati |
| [!UICONTROL Data Feed] | ID feed dati |
| [!UICONTROL Data Feed Subscription] | ID feed dati |
| [!UICONTROL Trait Summary] | SID (caratteristica) |
| [!UICONTROL Trait Rule] | SID (caratteristica) |
| [!UICONTROL Segment Summary] |  |
| [!UICONTROL Destination Summary] |  |
| [!UICONTROL Server-to-Server Destination] | N/D |
| [!UICONTROL Derived Signal] | N/D |
| [!UICONTROL Model] | N/D |
| [!UICONTROL Segment Test Group] | N/D |

Utilizzate [!UICONTROL Start Date] ([!DNL UTC]) e [!UICONTROL End Date] ([!DNL UTC]) per limitare l'intervallo di tempo dei registri.