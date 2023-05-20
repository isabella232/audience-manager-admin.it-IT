---
description: Crea, modifica ed elimina destinazioni Audienci Manager.
seo-description: Create, edit, and delete Audience Manager destinations.
seo-title: Manage Company Destinations
title: Gestire le destinazioni aziendali
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
exl-id: a2e73613-07cd-4ab8-8c6e-be451ed50bfc
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 1%

---

# Gestire le destinazioni aziendali {#manage-company-destinations}

Crea, modifica ed elimina destinazioni Audienci Manager.

<!-- t_company_destinations.xml -->

Per informazioni dettagliate, consulta [Destinazioni](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/destinations.html) nel *Guida utente di Audience Manager*.

## Creare o modificare le destinazioni aziendali {#create-edit-company-destinations}

Scorri le sezioni per istruzioni dettagliate su come creare nuove [!DNL Audience Manager] o modificare le destinazioni esistenti.

<!-- create-edit-company-destinations.xml -->

Visita il [Pagina di integrazione dei partner di Experience Cloud](https://wiki.corp.adobe.com/x/mPIMPw) prima di impostare le destinazioni. La pagina contiene le informazioni specifiche da compilare per ogni [!DNL Audience Manager] integrazione con i partner.

Se il cliente desidera utilizzare [!DNL Adobe Media Optimizer] come destinazione in [!DNL Audience Manager] , è necessario configurarlo in [!DNL Adobe Media Optimizer].

## Passa alla scheda Destinazioni {#navigate-destinations}

1. Clic **[!UICONTROL Companies]**, quindi individuare e fare clic sulla società desiderata per visualizzare [!UICONTROL Profile] pagina. È possibile utilizzare [!UICONTROL Search] o i controlli di impaginazione nella parte inferiore dell&#39;elenco per individuare la società desiderata. Puoi ordinare ogni colonna in ordine crescente o decrescente facendo clic sull’intestazione della colonna desiderata.
1. Fai clic su **[!UICONTROL Destinations]** scheda.
1. Per creare una nuova destinazione, fai clic su **[!UICONTROL Add Destination]**. Per modificare una destinazione esistente, fai clic sul nome della destinazione in **[!UICONTROL Name]** colonna.

## Impostazioni di base {#basic-settings}

Compila i campi nel **[!UICONTROL Basic Settings]** finestra.

* **[!UICONTROL Name]:** (Obbligatorio) Specifica il nome di questa destinazione.
* **[!UICONTROL Description]:** Specifica informazioni descrittive su questa destinazione.
* **[!UICONTROL Type]:** (Obbligatorio) Seleziona il tipo di destinazione desiderato:
   * **[!UICONTROL Bulk ID]**: sincronizza gli ID tra piattaforme diverse.
   * **[!UICONTROL Bulk Trait]**: invia informazioni sulle caratteristiche in blocco a diverse piattaforme.
   * **[!UICONTROL Bulk Segment]**: invia informazioni sui segmenti in blocco a piattaforme diverse.
   * **[!UICONTROL S2S]**: utilizza destinazioni da server a server per inviare dati in tempo reale e in batch a piattaforme diverse.
* **[!UICONTROL Auto-Fill Destination Mapping]:** ( [!UICONTROL S2S] solo) Selezionare un&#39;opzione:
   * **[!UICONTROL Segment ID]:** Se selezioni questa impostazione, la mappatura del valore di destinazione viene compilata con [!DNL Audience Manager] ID segmento.
   * **[!UICONTROL Integration Code Value]:** Se selezioni questa impostazione, la mappatura del valore di destinazione viene compilata con [!DNL Audience Manager] Codice di integrazione del segmento.
* **[!UICONTROL User ID Key]:** (Obbligatorio) Seleziona la chiave ID utente desiderata per questa destinazione dall’elenco a discesa.

Questo ID viene utilizzato come ID sorgente dati principale. Questo determina gli ID utente da escludere nel file.

>[!NOTE]
>
>Per [!UICONTROL Bulk ID] tipo di destinazione, non è possibile utilizzare [!DNL Audience Manager] [!UICONTROL User ID] o [!DNL Adobe Experience Cloud] ID

Se l’ID dell’origine dati ( [!UICONTROL DPID]) non viene visualizzato nell&#39;elenco a discesa, è necessario selezionare il **[!UICONTROL Outbound]** a livello di origine dati sulla [Pagina Impostazioni origine dati](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/manage-datasources.html).

* **[!UICONTROL Target Data Source]:** (Obbligatorio) Seleziona l’origine dati desiderata per questa destinazione dall’elenco a discesa. Questa impostazione consente l’etichettatura dei dati in uscita, che consente l’acquisizione in sistemi separati sul lato dei clienti.
* **[!UICONTROL Foreign Account ID]:** Specifica l&#39;ID account esterno per questa destinazione. Si tratta del valore di identificazione nel sistema del destinatario per questi dati in uscita.
* **[!UICONTROL Outbound Sample Rate Denominator]:** Quando la quantità totale di dati restituiti è sconosciuta, utilizzare questa impostazione per restituire solo una quantità campione di dati, anziché la quantità completa. Regolare qui il numero per rappresentare una frazione di dati (ad esempio, un valore di &#39;100&#39; restituisce 1/100 della quantità regolare di dati, un valore di &#39;10&#39; restituisce 1/10 della quantità regolare di dati). Il valore predefinito è &#39;1&#39;, che restituisce tutti i dati.

## Dati in tempo reale (per destinazioni S2S) {#realtime-s2s}

Se stai creando un’ [!UICONTROL S2S] destinazione, compila i campi seguenti:

**[!UICONTROL Servers]**: seleziona la `HTTP` server per questa destinazione.
**[!UICONTROL Format]**: seleziona il formato desiderato per questa destinazione dall’elenco a discesa: [!UICONTROL HTTP only].

>[!NOTE]
>
>Per [!DNL S2S] solo, puoi abilitare o disabilitare [!UICONTROL Realtime] o [!UICONTROL Batch] destinazioni utilizzando i dispositivi di scorrimento sullo schermo Off/On. Non è possibile disattivare entrambe le opzioni.

## Dati batch {#batch-data}

Per [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] o [!UICONTROL Bulk Segment] destinazioni, compila i campi seguenti:

* **[!UICONTROL Protocol]**: (obbligatorio) seleziona il protocollo desiderato per questa destinazione dall’elenco a discesa:
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**: (obbligatorio) seleziona il server desiderato per questa destinazione dall’elenco a discesa.
* **[!UICONTROL Format]**: (obbligatorio) seleziona il formato desiderato per questa destinazione dall’elenco a discesa: [!DNL HTTP] o tipo di file, a seconda del protocollo scelto in precedenza.
* **[!UICONTROL Sync Type]**: (Obbligatorio) seleziona il tipo di sincronizzazione desiderato per questa destinazione. Indica il livello di attività utente che i clienti desiderano includere negli ordini in uscita. Seleziona **[!UICONTROL Customer]** se i clienti sono interessati solo all’analisi delle qualifiche dei segmenti dalle loro proprietà. Seleziona **[!UICONTROL Platform]** se desiderano includere qualifiche di segmenti da attività off-site in tutti [!DNL Audience Manager] clienti.
* **[!UICONTROL Customer]**: il file contiene utenti attivi che hanno almeno 1 realizzazione delle caratteristiche solo sulle proprietà del client (associate alle proprietà del client) [!UICONTROL PID]) per il periodo selezionato. I clienti devono utilizzare questa opzione per effettuare in uscita le *in tempo reale* qualificazione dei segmenti nelle destinazioni.
* **[!UICONTROL Platform]**: il file contiene utenti attivi che hanno almeno 1 interazione in tempo reale, che si tratti della sincronizzazione ID o della realizzazione delle caratteristiche, ovunque in tutti [!DNL Audience Manager] proprietà dei client (associate a tutti i PID client) per il periodo di tempo selezionato. I clienti devono utilizzare questa opzione per effettuare in uscita le *totale* qualificazione dei segmenti nelle destinazioni.
* **[!UICONTROL Lifetime]**: il file contiene utenti attivi visualizzati ovunque in tutti [!DNL Audience Manager] proprietà dei client dalla creazione della destinazione.
* **[!UICONTROL Sync Type Lookback Period]**: se selezioni [!UICONTROL Customer] o [!UICONTROL Platform], seleziona un periodo di tempo. I file contengono utenti attivi per il periodo di tempo selezionato.
Quindi, selezionare il tipo di ordine. Indica la frequenza e l’ambito di ogni integrazione in uscita con i partner. Seleziona tra ordini incrementali e ordini completi.
* **[!UICONTROL Incremental Scheduled Run]**: a ogni esecuzione, [!DNL Audience Manager] eseguirà l’outbound solo dei nuovi utenti qualificati dall’ordine in uscita precedente. Seleziona il periodo di tempo desiderato [!DNL Audience Manager] per eseguire processi di sincronizzazione incrementale. Ad esempio, puoi selezionare ogni 24 ore, ogni sette giorni, ogni 30 giorni o mai.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>Il primo ordine incrementale in assoluto equivale a un ordine completo perché nessun utente precedente è mai stato inviato alla destinazione.

* **[!UICONTROL Full Sync Scheduled Run]**: a ogni esecuzione, [!DNL Audience Manager] eseguirà l’associazione in uscita di tutti gli utenti attivi dalla prima configurazione della destinazione. Seleziona la pianificazione desiderata [!DNL Audience Manager] da utilizzare per eseguire processi di sincronizzazione completa. Ad esempio, puoi selezionare ogni 24 ore, ogni sette giorni, ogni 30 giorni o mai.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>È consigliabile utilizzare le sincronizzazioni incrementali con maggiore frequenza rispetto alle sincronizzazioni complete. Le sincronizzazioni incrementali inviano solo file che contengono nuove realizzazioni di caratteristiche o sincronizzazioni ID. Le sincronizzazioni complete inviano tutti i file, indipendentemente dal fatto che includano o meno nuove realizzazioni o sincronizzazioni ID. Utilizza solo il [!UICONTROL Full Sync Scheduled Run] configurazione quando i client necessitano di una copia completa di tutti gli utenti, per ridurre il volume di dati in uscita.

## Configurare origini dati {#configure-data-sources}

Per [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] o [!UICONTROL Bulk Segment] destinazioni, compila i campi seguenti. Queste impostazioni ti consentono di inviare tutti i dati (caratteristiche, segmenti o ID, in base al tipo selezionato) associati alle origini dati.

* **[!UICONTROL All Unrestricted First Party Data]**: seleziona per utilizzare tutte le origini dati di prime parti. Se si seleziona questa opzione, il [!UICONTROL Available Data Sources] sono disattivate.
* **[!UICONTROL Available Data Sources]**: utilizza le frecce per spostare le origini dati tra **[!UICONTROL Available Data Sources]** e **[!UICONTROL In File Data Sources]** scatole.

## Salva e finalizza {#save-and-finalize}

Il **[!UICONTROL Save]** dopo aver compilato tutti i campi obbligatori. Clic **[!UICONTROL Save]** per finalizzare il processo di creazione della destinazione.

## Elimina destinazioni società {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

Per eliminare una destinazione:

1. Clic **[!UICONTROL Companies]**, individuare e fare clic sulla società desiderata, quindi fare clic sul pulsante **[!UICONTROL Destinations]** scheda.
1. Clic  ![](assets/icon_delete.png) nel **[!UICONTROL Actions]** della destinazione desiderata.
1. Clic **[!UICONTROL OK]** per confermare l’eliminazione.

>[!NOTE]
>
>Non puoi eliminare una destinazione se ad essa sono mappati dei segmenti.
