---
description: Creare, modificare ed eliminare  destinazioni di Audienci Manager.
seo-description: Creare, modificare ed eliminare  destinazioni di Audienci Manager.
seo-title: Gestire le destinazioni aziendali
title: Gestire le destinazioni aziendali
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
translation-type: tm+mt
source-git-commit: f247457004a624297ddc8847dd256dbb7d8da418
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 1%

---


# Gestire le destinazioni aziendali {#manage-company-destinations}

Creare, modificare ed eliminare  destinazioni di Audienci Manager.

<!-- t_company_destinations.xml -->

Per informazioni dettagliate, vedere [Destinazioni](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html) nella *Guida utente  Audience Manager*.

## Creare o modificare le destinazioni aziendali {#create-edit-company-destinations}

Scorri le sezioni per istruzioni dettagliate su come creare nuove destinazioni [!DNL Audience Manager] o modificare destinazioni esistenti.

<!-- create-edit-company-destinations.xml -->

Visita la [ pagina di integrazione dei partner di Experience Cloud](https://wiki.corp.adobe.com/x/mPIMPw) prima di configurare le destinazioni. La pagina contiene le informazioni specifiche da compilare per ogni integrazione con [!DNL Audience Manager] partner.

Se il cliente desidera utilizzare [!DNL Adobe Media Optimizer] come destinazione in [!DNL Audience Manager], è necessario impostarlo in [!DNL Adobe Media Optimizer].

## Passare alla scheda Destinazioni {#navigate-destinations}

1. Fare clic su **[!UICONTROL Companies]**, quindi individuare e fare clic sulla società desiderata per visualizzare la relativa pagina [!UICONTROL Profile]. È possibile utilizzare la casella [!UICONTROL Search] o i controlli di impaginazione in fondo all&#39;elenco per trovare la società desiderata. Potete ordinare ciascuna colonna in ordine crescente o decrescente facendo clic sull’intestazione della colonna desiderata.
1. Fare clic sulla scheda **[!UICONTROL Destinations]**.
1. Per creare una nuova destinazione, fare clic su **[!UICONTROL Add Destination]**. Per modificare una destinazione esistente, fare clic sul nome della destinazione nella colonna **[!UICONTROL Name]**.

## Impostazioni di base {#basic-settings}

Compila i campi nella finestra **[!UICONTROL Basic Settings]**.

* **[!UICONTROL Name]:** (Obbligatorio) Specificate il nome di questa destinazione.
* **[!UICONTROL Description]:** Specificate informazioni descrittive sulla destinazione.
* **[!UICONTROL Type]:** (Obbligatorio) Selezionare il tipo di destinazione desiderato:
   * **[!UICONTROL Bulk ID]**: Sincronizzare gli ID tra diverse piattaforme.
   * **[!UICONTROL Bulk Trait]**: Inviare informazioni sulle caratteristiche in massa a piattaforme diverse.
   * **[!UICONTROL Bulk Segment]**: Invia le informazioni sui segmenti in massa a piattaforme diverse.
   * **[!UICONTROL S2S]**: Utilizza le destinazioni server-to-server per inviare dati in tempo reale e batch a diverse piattaforme.
* **[!UICONTROL Auto-Fill Destination Mapping]:** (  [!UICONTROL S2S] solo) Selezionate un’opzione:
   * **[!UICONTROL Segment ID]:** Se selezionate questa impostazione, la mappatura del valore di destinazione viene compilata con l’ID  [!DNL Audience Manager] segmento.
   * **[!UICONTROL Integration Code Value]:** Se selezionate questa impostazione, la mappatura del valore di destinazione viene compilata con il codice di integrazione del  [!DNL Audience Manager] segmento.
* **[!UICONTROL User ID Key]:** (Obbligatorio) Seleziona dall&#39;elenco a discesa la chiave ID utente desiderata per questa destinazione.

Questo ID viene utilizzato come ID origine dati principale. Questo determina gli ID utente da escludere dal file.

>[!NOTE]
>
>Per il tipo di destinazione [!UICONTROL Bulk ID] non è possibile utilizzare l&#39;ID [!DNL Audience Manager] [!UICONTROL User ID] o [!DNL Adobe Experience Cloud].

Se l&#39;ID origine dati ( [!UICONTROL DPID]) non viene visualizzato nell&#39;elenco a discesa, è necessario selezionare la casella di controllo **[!UICONTROL Outbound]** a livello di origine dati nella pagina [Impostazioni origine dati](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/data-sources/manage-datasources.html).

* **[!UICONTROL Target Data Source]:** (Obbligatorio) Selezionare dall&#39;elenco a discesa l&#39;origine dati desiderata per la destinazione. Questa impostazione consente l&#39;etichettatura di dati fuori limite, che consente l&#39;inserimento in sistemi separati sul lato client.
* **[!UICONTROL Foreign Account ID]:** Specificate l&#39;ID account esterno per questa destinazione. Si tratta del valore di identificazione nel sistema del destinatario per questi dati non consentiti.
* **[!UICONTROL Outbound Sample Rate Denominator]:** Quando la quantità totale di dati restituiti è sconosciuta, utilizzate questa impostazione per restituire solo una quantità di dati di esempio, anziché l&#39;intera quantità. Regolate qui il numero per rappresentare una frazione dei dati (ad esempio, un valore di &#39;100&#39; restituisce 1/100 la quantità regolare di dati, un valore di &#39;10&#39; restituisce 1/10 la quantità regolare di dati). Il valore predefinito è &#39;1&#39;, che restituisce tutti i dati.

## Dati in tempo reale (per le destinazioni S2S) {#realtime-s2s}

Se stai creando una destinazione [!UICONTROL S2S], compila i campi seguenti:

**[!UICONTROL Servers]**: Selezionare il  `HTTP` server desiderato per la destinazione.
**[!UICONTROL Format]**: Dall’elenco a discesa, selezionate il formato desiderato per la destinazione:  [!UICONTROL HTTP only].

>[!NOTE]
>
>Solo per [!DNL S2S], è possibile abilitare o disabilitare le destinazioni [!UICONTROL Realtime] o [!UICONTROL Batch] utilizzando i cursori Attivato/Disattivato sullo schermo. Non potete disabilitare entrambe le opzioni.

## Dati batch {#batch-data}

Per le destinazioni [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] o [!UICONTROL Bulk Segment], compilare i campi seguenti:

* **[!UICONTROL Protocol]**: (Obbligatorio) Dall&#39;elenco a discesa, selezionare il protocollo desiderato per la destinazione:
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**: (Obbligatorio) Dall’elenco a discesa, selezionate il server desiderato per questa destinazione.
* **[!UICONTROL Format]**: (Obbligatorio) Dall’elenco a discesa, selezionate il formato desiderato per la destinazione:  [!DNL HTTP] o tipo di file, a seconda del protocollo scelto in precedenza.
* **[!UICONTROL Sync Type]**: (Obbligatorio) Selezionate il tipo di sincronizzazione desiderato per questa destinazione. Indica il livello di attività utente che i client dovrebbero includere negli ordini in uscita. Selezionare **[!UICONTROL Customer]** se i client sono interessati solo ad analizzare le qualifiche dei segmenti dalle loro proprietà. Selezionare **[!UICONTROL Platform]** se si desidera includere le qualifiche del segmento dalle attività fuori sede in tutti i [!DNL Audience Manager] clienti.
* **[!UICONTROL Customer]**: Il file contiene utenti attivi con almeno 1 caratteristica realizzata solo sulle proprietà del client (associate a quelle del client  [!UICONTROL PID]) per il periodo di tempo selezionato. I clienti devono utilizzare questa opzione per trasferire le loro qualifiche di segmento *in tempo reale* alle destinazioni.
* **[!UICONTROL Platform]**: Il file contiene utenti attivi con almeno 1 interazione in tempo reale, sia che si tratti della sincronizzazione ID o della realizzazione delle caratteristiche, ovunque nelle proprietà  [!DNL Audience Manager] dei client (associate a tutti i PID del client) per il periodo di tempo selezionato. I clienti devono utilizzare questa opzione per trasferire le qualifiche del segmento *total* alle destinazioni.
* **[!UICONTROL Lifetime]**: Il file contiene gli utenti attivi visualizzati ovunque nelle proprietà  [!DNL Audience Manager] dei client dalla creazione della destinazione.
* **[!UICONTROL Sync Type Lookback Period]**: Se si seleziona  [!UICONTROL Customer] o  [!UICONTROL Platform], selezionare un periodo di tempo. I file contengono utenti attivi per il periodo di tempo selezionato.
Quindi, selezionate il tipo di ordine. Indica la frequenza e la portata di ogni integrazione in uscita con i partner. Selezionare tra ordini incrementali e ordini completi.
* **[!UICONTROL Incremental Scheduled Run]**: Per ogni esecuzione,  [!DNL Audience Manager] verranno inviati solo i nuovi utenti netti qualificati dall&#39;ordine in uscita precedente. Selezionare il periodo di tempo desiderato per [!DNL Audience Manager] eseguire i processi di sincronizzazione incrementale. Ad esempio, potete selezionare ogni 24 ore, ogni sette giorni, ogni 30 giorni o mai.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>Il primo ordine incrementale è equivalente a un ordine completo perché nessun utente precedente è mai stato inviato alla destinazione.

* **[!UICONTROL Full Sync Scheduled Run]**: Per ogni esecuzione,  [!DNL Audience Manager] verranno inviati tutti gli utenti attivi dalla prima configurazione della destinazione. Selezionare la pianificazione desiderata che si desidera utilizzare [!DNL Audience Manager] per eseguire i processi di sincronizzazione completi. Ad esempio, potete selezionare ogni 24 ore, ogni sette giorni, ogni 30 giorni o mai.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>È consigliabile utilizzare sincronizzazioni incrementali più frequentemente che sincronizzazioni complete. Le sincronizzazioni incrementali inviano solo file che contengono nuove realizzazioni o sincronizzazioni ID. Le sincronizzazioni complete inviano tutti i file, che includano o meno nuove realizzazioni o sincronizzazioni ID. Utilizzate la configurazione [!UICONTROL Full Sync Scheduled Run] solo quando i client necessitano di una copia completa di tutti gli utenti, per ridurre il volume dei dati in uscita.

## Configurare le origini dati {#configure-data-sources}

Per le destinazioni [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] o [!UICONTROL Bulk Segment], compilare i campi riportati di seguito. Queste impostazioni consentono di inviare tutti i dati (caratteristiche, segmenti o ID, in base al tipo selezionato) associati alle origini dati.

* **[!UICONTROL All Unrestricted First Party Data]**: Selezionare per utilizzare tutte le origini dati di prime parti. Se selezionate questa opzione, le opzioni [!UICONTROL Available Data Sources] sono disattivate.
* **[!UICONTROL Available Data Sources]**: Utilizzare le frecce per spostare le origini dati tra le  **[!UICONTROL Available Data Sources]** e  **[!UICONTROL In File Data Sources]** le caselle.

## Salva e finalizza {#save-and-finalize}

Il pulsante **[!UICONTROL Save]** viene attivato dopo aver compilato tutti i campi richiesti. Fare clic su **[!UICONTROL Save]** per finalizzare il processo di creazione della destinazione.

## Elimina destinazioni società {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

Per eliminare una destinazione:

1. Fare clic su **[!UICONTROL Companies]**, individuare e fare clic sulla società desiderata, quindi fare clic sulla scheda **[!UICONTROL Destinations]**.
1. Fare clic su ![](assets/icon_delete.png) nella colonna **[!UICONTROL Actions]** della destinazione desiderata.
1. Fare clic su **[!UICONTROL OK]** per confermare l&#39;eliminazione.

>[!NOTE]
>
>Non è possibile eliminare una destinazione se vi sono segmenti mappati.