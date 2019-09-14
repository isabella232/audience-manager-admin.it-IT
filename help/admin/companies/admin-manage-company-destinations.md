---
description: Creare, modificare ed eliminare destinazioni Audience Manager.
seo-description: Creare, modificare ed eliminare destinazioni Audience Manager.
seo-title: Gestione delle destinazioni aziendali
title: Gestione delle destinazioni aziendali
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# Gestione delle destinazioni aziendali {#manage-company-destinations}

Creare, modificare ed eliminare destinazioni Audience Manager.

<!-- t_company_destinations.xml -->

Per informazioni dettagliate, consultate [Destinazioni](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html) nella Guida *utente di* Audience Manager.

## Creazione o modifica delle destinazioni aziendali {#create-edit-company-destinations}

Scorri le sezioni per istruzioni dettagliate su come creare nuove [!DNL Audience Manager] destinazioni o modificare destinazioni esistenti.

<!-- create-edit-company-destinations.xml -->

Visita la pagina [di integrazione dei partner](https://wiki.corp.adobe.com/x/mPIMPw) Experience Cloud prima di configurare le destinazioni. La pagina contiene le informazioni specifiche da compilare per ogni integrazione con [!DNL Audience Manager] i partner.

Se il cliente desidera utilizzare [!DNL Adobe Media Optimizer] come destinazione in [!DNL Audience Manager] , è necessario impostare in [!DNL Adobe Media Optimizer].

## Passare alla scheda Destinazioni {#navigate-destinations}

1. Fate clic **[!UICONTROL Companies]**, quindi individuate e fate clic sulla società desiderata per visualizzare la [!UICONTROL Profile] pagina. È possibile utilizzare la [!UICONTROL Search] casella o i controlli di impaginazione in fondo all'elenco per individuare la società desiderata. Potete ordinare ciascuna colonna in ordine crescente o decrescente facendo clic sull’intestazione della colonna desiderata.
1. Click the **[!UICONTROL Destinations]** tab.
1. Per creare una nuova destinazione, fai clic su **[!UICONTROL Add Destination]**. To edit an existing destination, click the destination's name in the **[!UICONTROL Name]** column.

## Impostazioni di base {#basic-settings}

Fill in the fields in the **[!UICONTROL Basic Settings]** window.

* **[!UICONTROL Name]** : (Obbligatorio) Specifica il nome di questa destinazione.
* **[!UICONTROL Description]** : Specificate informazioni descrittive sulla destinazione.
* **[!UICONTROL Type]** : (Obbligatorio) Selezionare il tipo di destinazione desiderato:
   * **[!UICONTROL Bulk ID]**: Sincronizzare gli ID tra diverse piattaforme.
   * **[!UICONTROL Bulk Trait]**: Invia informazioni sulle caratteristiche in massa a piattaforme diverse.
   * **[!UICONTROL Bulk Segment]**: Invia le informazioni sui segmenti in massa a piattaforme diverse.
   * **[!UICONTROL S2S]**: Utilizza le destinazioni server-to-server per inviare dati in tempo reale e batch a diverse piattaforme.
* **[!UICONTROL Auto-Fill Destination Mapping]** : ( [!UICONTROL S2S] Solo) Selezionate un’opzione:
   * **[!UICONTROL Segment ID]** : Se selezionate questa impostazione, la mappatura del valore di destinazione viene compilata con l’ID [!DNL Audience Manager] segmento.
   * **[!UICONTROL Integration Code Value]** : Se si seleziona questa impostazione, la mappatura del valore di destinazione viene compilata con il codice di integrazione [!DNL Audience Manager] del segmento.
* **[!UICONTROL User ID Key]** : (Obbligatorio) Seleziona dall'elenco a discesa la chiave ID utente desiderata per questa destinazione.

Questo ID viene utilizzato come ID origine dati principale. Questo determina gli ID utente da escludere dal file.

>[!NOTE]
>
>Per il tipo di [!UICONTROL Bulk ID] destinazione non è possibile utilizzare l' [!DNL Audience Manager] ID [!UICONTROL User ID] o l' [!DNL Adobe Experience Cloud] ID.

Se l'ID origine dati ( [!UICONTROL DPID]) non viene visualizzato nell'elenco a discesa, devi selezionare la **[!UICONTROL Outbound]** casella di controllo a livello di origine dati nella pagina [Impostazioni origine](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/data-sources/manage-datasources.html)dati.

* **[!UICONTROL Target Data Source]** : (Obbligatorio) Selezionare dall'elenco a discesa l'origine dati desiderata per la destinazione. Questa impostazione consente l'etichettatura di dati fuori limite, che consente l'inserimento in sistemi separati sul lato client.
* **[!UICONTROL Foreign Account ID]** : Specifica l'ID account esterno per questa destinazione. Si tratta del valore di identificazione nel sistema del destinatario per questi dati non consentiti.
* **[!UICONTROL Outbound Sample Rate Denominator]** : Quando la quantità totale di dati restituiti è sconosciuta, utilizzate questa impostazione per restituire solo una quantità di dati campione, anziché l'intero importo. Regolate qui il numero per rappresentare una frazione dei dati (ad esempio, un valore di '100' restituisce 1/100 la quantità regolare di dati, un valore di '10' restituisce 1/10 la quantità regolare di dati). Il valore predefinito è '1', che restituisce tutti i dati.

## Dati in tempo reale (per le destinazioni S2S) {#realtime-s2s}

Se stai creando una [!UICONTROL S2S] destinazione, compila i campi seguenti:

**[!UICONTROL Servers]**: Selezionare il `HTTP` server desiderato per la destinazione.
**[!UICONTROL Format]**: Dall’elenco a discesa, selezionate il formato desiderato per la destinazione: [!UICONTROL HTTP only].

>[!NOTE]
>
>Solo [!DNL S2S] per attivare o disattivare una [!UICONTROL Realtime] o [!UICONTROL Batch] più destinazioni utilizzando i cursori Disattivato/Attivato sullo schermo. Non potete disabilitare entrambe le opzioni.

## Dati batch {#batch-data}

Per [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] o [!UICONTROL Bulk Segment] destinazioni, compila i campi seguenti:

* **[!UICONTROL Protocol]**: (Obbligatorio) Dall'elenco a discesa, selezionare il protocollo desiderato per la destinazione:
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**: (Obbligatorio) Dall’elenco a discesa, selezionate il server desiderato per questa destinazione.
* **[!UICONTROL Format]**: (Obbligatorio) Dall’elenco a discesa, selezionate il formato desiderato per la destinazione: [!DNL HTTP] o tipo di file, a seconda del protocollo scelto in precedenza.
* **[!UICONTROL Sync Type]**: (Obbligatorio) Selezionate il tipo di sincronizzazione desiderato per questa destinazione. Indica il livello di attività utente che i client dovrebbero includere negli ordini in uscita. Selezionate **[!UICONTROL Customer]** se i clienti sono interessati solo ad analizzare le qualifiche dei segmenti dalle loro proprietà. Selezionate **[!UICONTROL Platform]** se desiderano includere le qualifiche del segmento dalle attività fuori sede in tutti i [!DNL Audience Manager] clienti.
* **[!UICONTROL Customer]**: Il file contiene utenti attivi con almeno 1 caratteristica realizzata solo sulle proprietà del client (associate a quelle del client [!UICONTROL PID]) per il periodo di tempo selezionato. I clienti devono utilizzare questa opzione per trasferire le loro qualifiche del segmento in tempo ** reale alle destinazioni.
* **[!UICONTROL Platform]**: Il file contiene utenti attivi con almeno 1 interazione in tempo reale, sia che si tratti della sincronizzazione ID o della realizzazione delle caratteristiche, ovunque nelle proprietà [!DNL Audience Manager] del client (associate a tutti i PID del client) per il periodo di tempo selezionato. I clienti devono utilizzare questa opzione per trasferire le qualifiche *totali* del segmento alle destinazioni.
* **[!UICONTROL Lifetime]**: Il file contiene gli utenti attivi visualizzati ovunque nelle proprietà [!DNL Audience Manager] dei client dalla creazione della destinazione.
* **[!UICONTROL Sync Type Lookback Period]**: Se selezionate [!UICONTROL Customer] o [!UICONTROL Platform], selezionate un periodo di tempo. I file contengono utenti attivi per il periodo di tempo selezionato.
Quindi, selezionate il tipo di ordine. Indica la frequenza e la portata di ogni integrazione in uscita con i partner. Selezionare tra ordini incrementali e ordini completi.
* **[!UICONTROL Incremental Scheduled Run]**: Per ogni esecuzione, [!DNL Audience Manager] verranno inviati solo i nuovi utenti netti qualificati dall'ordine in uscita precedente. Selezionare il periodo di tempo desiderato per [!DNL Audience Manager] eseguire i processi di sincronizzazione incrementale. Ad esempio, potete selezionare ogni 24 ore, ogni sette giorni, ogni 30 giorni o mai.

>[!NOTE] {important="high"}
>
>Il primo ordine incrementale è equivalente a un ordine completo perché nessun utente precedente è mai stato inviato alla destinazione.

* **[!UICONTROL Full Sync Scheduled Run]**: Per ogni esecuzione, [!DNL Audience Manager] verrà eseguito l'uscita di tutti gli utenti attivi dalla prima configurazione della destinazione. Selezionate la pianificazione da usare [!DNL Audience Manager] per eseguire i processi di sincronizzazione completi. Ad esempio, potete selezionare ogni 24 ore, ogni sette giorni, ogni 30 giorni o mai.

>[!NOTE] {important="high"}
>
>È consigliabile utilizzare sincronizzazioni incrementali più frequentemente che sincronizzazioni complete. Le sincronizzazioni incrementali inviano solo file che contengono nuove realizzazioni o sincronizzazioni ID. Le sincronizzazioni complete inviano tutti i file, anche se includono nuove realizzazioni o sincronizzazioni ID. Utilizzate la [!UICONTROL Full Sync Scheduled Run] configurazione solo quando i client necessitano di una copia completa di tutti gli utenti, per ridurre il volume dei dati in uscita.

## Configura origini dati {#configure-data-sources}

Per [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] o [!UICONTROL Bulk Segment] le destinazioni, compila i campi seguenti. Queste impostazioni consentono di inviare tutti i dati (caratteristiche, segmenti o ID, in base al tipo selezionato) associati alle origini dati.

* **[!UICONTROL All Unrestricted First Party Data]**: Selezionare per utilizzare tutte le origini dati di prime parti. Se selezionate questa opzione, le [!UICONTROL Available Data Sources] opzioni sono disattivate.
* **[!UICONTROL Available Data Sources]**: Utilizzare le frecce per spostare le origini dati tra le **[!UICONTROL Available Data Sources]** e **[!UICONTROL In File Data Sources]** le caselle.

## Salva e finalizza {#save-and-finalize}

Il **[!UICONTROL Save]** pulsante viene attivato dopo aver compilato tutti i campi richiesti. Fare clic **[!UICONTROL Save]** per finalizzare il processo di creazione della destinazione.

## Elimina destinazioni società {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

Per eliminare una destinazione:

1. Fate clic **[!UICONTROL Companies]**, individuate e fate clic sulla società desiderata, quindi fate clic sulla **[!UICONTROL Destinations]** scheda.
1. Fate clic ![](assets/icon_delete.png) nella **[!UICONTROL Actions]** colonna della destinazione desiderata.
1. Click **[!UICONTROL OK]** to confirm the deletion.

>[!NOTE]
>
>Non è possibile eliminare una destinazione se vi sono segmenti mappati.