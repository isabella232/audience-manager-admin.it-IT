---
description: Per evitare l’onboarding accidentale di file e dati nelle origini dati di destinazione di proprietà di altri partner o clienti, Audience Manager ha aggiunto un requisito di mappatura tra l’ID partner (PID) e le origini dati di proprietà di altri partner.
title: Gestire l’accesso all’onboarding per i dati di seconde parti
exl-id: 03bec978-dd31-41cc-a3aa-d67fbb98963c
source-git-commit: cc04863272005964cfbf1bb2319cc0dd86863680
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Gestire l’accesso all’onboarding per i dati di seconde parti {#manage-onboarding-access-for-second-party-data}

>[!IMPORTANT]
>
> Il pubblico di questa pagina è composto da dipendenti interni agli Adobi. Se sei un cliente Audience Manager che richiede una mappatura dell’origine dati di seconde parti come descritto in questa pagina, contatta l’Assistenza clienti o il tuo Account Manager tecnico.
> Non è necessario richiedere una mappatura per le relazioni di condivisione dei dati esistenti. La mappatura non è necessaria anche durante l’onboarding dei dati nelle origini dati di destinazione che appartengono al tuo PID.

Per evitare l’onboarding accidentale di file e dati nelle origini dati target di proprietà di altri partner, Audience Manager ha aggiunto un requisito di mappatura tra l’ID partner (PID) e le origini dati (DPID) di proprietà di altri partner. Ulteriori informazioni su PID e DPID in [indice degli ID di Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html).

A scopo di condivisione dei dati di seconde parti, se un partner o un cliente di Audience Manager desidera acquisire file in un’origine dati di destinazione che non possiede, deve richiedere una mappatura tra il proprio ID partner (PID) e quella specifica origine dati (DPID). Se la mappatura è mancante, i file non verranno elaborati dal processo di dati in entrata e i dati non saranno caricati in Audience Manager.

Per creare la mappatura, invia un ticket Jira al team di ingegneria di Audience Manager. Visualizza un esempio di biglietto Jira [qui](https://jira.corp.adobe.com/browse/AAM-60353). Non è necessario creare mappature per le relazioni di condivisione dei dati esistenti.
