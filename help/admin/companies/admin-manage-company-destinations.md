---
description: Creare, modificare ed eliminare le destinazioni di Audience Manager.
seo-description: Creare, modificare ed eliminare le destinazioni di Audience Manager.
seo-title: Gestisci destinazioni società
title: Gestisci destinazioni società
uuid: d 9 a 6 bfb 1-7629-44 e 0-b 7 d 7-ece 44 f 65 ea 2 b
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# Gestisci destinazioni società {#manage-company-destinations}

Creare, modificare ed eliminare le destinazioni di Audience Manager.

<!-- t_company_destinations.xml -->

Per informazioni dettagliate, vedi [Destinazioni](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html) nella Guida utente *di Audience Manager*.

## Creare o modificare destinazioni società {#create-edit-company-destinations}

Scorrete le sezioni per istruzioni dettagliate su come creare nuove [!DNL Audience Manager] destinazioni o modificare le destinazioni esistenti.

<!-- create-edit-company-destinations.xml -->

Visita la pagina di integrazione dei partner [di Experience Cloud](https://wiki.corp.adobe.com/x/mPIMPw) prima di impostare le destinazioni. La pagina contiene le informazioni specifiche necessarie per l'integrazione [!DNL Audience Manager] dei partner.

Se il client desidera utilizzare [!DNL Adobe Media Optimizer] come destinazione, [!DNL Audience Manager] è necessario impostarlo in [!DNL Adobe Media Optimizer].

## Passare alla scheda Destinazioni {#navigate-destinations}

1. Fate clic **[!UICONTROL Companies]**, individuate e fate clic sulla società desiderata per visualizzarne [!UICONTROL Profile] la pagina. Per trovare la società desiderata, è possibile utilizzare la [!UICONTROL Search] casella o i controlli di impaginazione in fondo all'elenco. Potete ordinare ciascuna colonna in ordine crescente o decrescente facendo clic sull'intestazione della colonna desiderata.
1. Click the **[!UICONTROL Destinations]** tab.
1. Per creare una nuova destinazione, fate clic **[!UICONTROL Add Destination]** su. To edit an existing destination, click the destination's name in the **[!UICONTROL Name]** column.

## Impostazioni di base {#basic-settings}

Fill in the fields in the **[!UICONTROL Basic Settings]** window.

* **[!UICONTROL Name]:** (Obbligatorio) Specificate il nome di questa destinazione.
* **[!UICONTROL Description]:** Specificate informazioni descrittive su questa destinazione.
* **[!UICONTROL Type]:** (Obbligatorio) Seleziona il tipo di destinazione desiderato:
   * **[!UICONTROL Bulk ID]**: Sincronizzazione ID tra piattaforme diverse.
   * **[!UICONTROL Bulk Trait]**: Inviate informazioni di caratteristica in massa a diverse piattaforme.
   * **[!UICONTROL Bulk Segment]**: Invia le informazioni sul segmento in massa a diverse piattaforme.
   * **[!UICONTROL S2S]**: Utilizzate le destinazioni server-to-server per inviare dati in tempo reale e in batch a piattaforme diverse.
* **[!UICONTROL Auto-Fill Destination Mapping]:** ( [!UICONTROL S2S] solo) Selezionate un'opzione:
   * **[!UICONTROL Segment ID]:** Se selezionate questa impostazione, la mappatura del valore di destinazione viene riempita con l'ID [!DNL Audience Manager] segmento.
   * **[!UICONTROL Integration Code Value]:** Se selezionate questa impostazione, la mappatura del valore di destinazione viene compilata con il codice di integrazione [!DNL Audience Manager] Segmenti.
* **[!UICONTROL User ID Key]:** (Obbligatorio) Seleziona il tasto ID utente desiderato per questa destinazione dall'elenco a discesa.

Questo ID viene usato come ID di origine dati principale. Ciò determina l'outboxing degli ID utente nel file.

>[!NOTE]
>
>Per il tipo [!UICONTROL Bulk ID] di destinazione, non potete utilizzare l' [!DNL Audience Manager][!UICONTROL User ID] ID o l' [!DNL Adobe Experience Cloud] ID.

Se l'ID di origine dati ( [!UICONTROL DPID]) non viene visualizzato nell'elenco a discesa, devi selezionare la **[!UICONTROL Outbound]** casella di controllo a livello di data-source nella pagina Impostazioni origine [dati](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/data-sources/manage-datasources.html).

* **[!UICONTROL Target Data Source]:** (Obbligatorio) Seleziona l'origine dati desiderata per questa destinazione dall'elenco a discesa. Questa impostazione consente di etichettare i dati in uscita, che consentono l'inserimento in sistemi separati sul lato client.
* **[!UICONTROL Foreign Account ID]:** Specificate l'ID account esterno per questa destinazione. Questo è il valore identificativo nel sistema del destinatario per i dati non vincolati.
* **[!UICONTROL Outbound Sample Rate Denominator]:** Quando la quantità totale di dati restituiti è sconosciuta, utilizzare questa impostazione per restituire solo una quantità di dati di esempio, anziché l'intero importo. Regolate qui il numero per rappresentare una frazione dei dati (ad esempio, un valore pari a '100 'restituisce la quantità regolare di dati, con un valore pari a '10 'viene restituita la quantità regolare di dati da a. Il valore predefinito è "1", che restituisce tutti i dati.

## Dati in tempo reale (per destinazioni S 2 S) {#realtime-s2s}

Se state creando [!UICONTROL S2S] una destinazione, compilate i campi seguenti:

**[!UICONTROL Servers]**: Selezionate il `HTTP` server desiderato per questa destinazione.
**[!UICONTROL Format]**: Seleziona il formato desiderato per questa destinazione dall'elenco a discesa: [!UICONTROL HTTP only].

>[!NOTE]
>
>Ad [!DNL S2S] esempio, potete abilitare o disabilitare o [!UICONTROL Realtime][!UICONTROL Batch] le destinazioni utilizzando i cursori Disattiva/Attivato. Non potete disattivare entrambe le opzioni.

## Dati batch {#batch-data}

Per [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] o [!UICONTROL Bulk Segment] destinazioni, compilare i campi seguenti:

* **[!UICONTROL Protocol]**: (Obbligatorio) Seleziona il protocollo desiderato per questa destinazione dall'elenco a discesa:
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**: (Obbligatorio) Seleziona il server desiderato per questa destinazione dall'elenco a discesa.
* **[!UICONTROL Format]**: (Obbligatorio) Seleziona il formato desiderato per questa destinazione dall'elenco a discesa: [!DNL HTTP] o tipo di file, a seconda del protocollo scelto.
* **[!UICONTROL Sync Type]**: (Obbligatorio) Seleziona il tipo di sincronizzazione desiderato per questa destinazione. Ciò indica il livello di attività che i client dovranno includere negli ordini in uscita. Seleziona **[!UICONTROL Customer]** se i clienti sono interessati solo all'analisi delle qualifiche dei segmenti dalle loro proprietà. Seleziona **[!UICONTROL Platform]** se desiderano includere le qualifiche dei segmenti da attività fuori sede in tutti [!DNL Audience Manager] i clienti.
* **[!UICONTROL Customer]**: Il file contiene utenti attivi che hanno almeno 1 caratteristiche in realizzazione solo sui client (associati ai client [!UICONTROL PID]) per il periodo di tempo selezionato. I clienti devono utilizzare questa opzione per associare le qualifiche del segmento *in tempo reale* alle destinazioni.
* **[!UICONTROL Platform]**: Il file contiene utenti attivi che dispongono di almeno 1 interazione in tempo reale, che siano sincronizzazione ID o realizzazione delle caratteristiche, ovunque in tutte le proprietà [!DNL Audience Manager] dei clienti (associate a tutti i client client) per il periodo di tempo selezionato. I clienti devono utilizzare questa opzione per associare le qualifiche *totali* del segmento alle destinazioni.
* **[!UICONTROL Lifetime]**: Il file contiene utenti attivi visualizzati in qualsiasi punto delle proprietà [!DNL Audience Manager] dei clienti, dalla creazione della destinazione.
* **[!UICONTROL Sync Type Lookback Period]**: Se selezionate [!UICONTROL Customer] o [!UICONTROL Platform]fate clic su un periodo di tempo, I file contengono utenti attivi per il periodo di tempo selezionato.
Quindi, selezionate il tipo d'ordine. Ciò indica la frequenza e l'ambito di ogni integrazione in uscita con i partner. Seleziona tra incremental e ordini completi.
* **[!UICONTROL Incremental Scheduled Run]**: Con ogni esecuzione, [!DNL Audience Manager] i nuovi utenti possono essere in uscita solo dopo l'ordine in uscita precedente. Selezionate il periodo di tempo desiderato per [!DNL Audience Manager] eseguire i processi di sincronizzazione incrementali. Ad esempio, puoi selezionare ogni 24 ore ogni sette giorni ogni 30 giorni o mai.

>[!NOTE] {importance = "high"}
>
>Il primo ordine incrementale mai è equivalente a un ordine completo, perché nessun utente precedente veniva mai inviato alla destinazione.

* **[!UICONTROL Full Sync Scheduled Run]**: Con ogni esecuzione, [!DNL Audience Manager] l'utente avrà in uscita tutti gli utenti attivi dall'impostazione della destinazione. Selezionate la pianificazione desiderata da usare [!DNL Audience Manager] per eseguire i processi completi di sincronizzazione. Ad esempio, puoi selezionare ogni 24 ore ogni sette giorni ogni 30 giorni o mai.

>[!NOTE] {importance = "high"}
>
>Consigliamo di utilizzare sincronizzazioni incrementali più frequenti delle sincronizzazioni complete. Le sincronizzazioni incrementali inviano solo file che contengono nuove implementazioni di caratteristica o sincronizzazioni ID. Le sincronizzazioni complete inviano tutti i file, indipendentemente dalla disponibilità di nuove sincronizzazioni o sincronizzazioni ID. Usate la [!UICONTROL Full Sync Scheduled Run] configurazione solo quando i client necessitano di una copia completa di tutti i loro utenti per ridurre il volume dei dati in uscita.

## Configurare le origini dati {#configure-data-sources}

Per [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] o [!UICONTROL Bulk Segment] destinazioni, compila i campi sottostanti. Queste impostazioni consentono di inviare tutti i dati (caratteristiche, segmenti o ID, in base al tipo selezionato) associati alle origini dati.

* **[!UICONTROL All Unrestricted First Party Data]**: Seleziona per utilizzare tutte le origini dati di prime parti. Se selezionate questa opzione, le [!UICONTROL Available Data Sources] opzioni sono disattivate.
* **[!UICONTROL Available Data Sources]**: Utilizzare le frecce per spostare le origini dati tra le **[!UICONTROL Available Data Sources]****[!UICONTROL In File Data Sources]** caselle.

## Salva e finalizza {#save-and-finalize}

Il **[!UICONTROL Save]** pulsante viene attivato dopo aver compilato tutti i campi obbligatori. Fate clic su **[!UICONTROL Save]** per finalizzare il processo di destinazione.

## Elimina destinazioni società {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

Per eliminare una destinazione:

1. Fate clic **[!UICONTROL Companies]**, individuate e fate clic sulla società desiderata, quindi fate clic sulla **[!UICONTROL Destinations]** scheda.
1. Fate clic ![](assets/icon_delete.png) nella **[!UICONTROL Actions]** colonna della destinazione desiderata.
1. Click **[!UICONTROL OK]** to confirm the deletion.

>[!NOTE]
>
>Se vi sono segmenti mappati, non è possibile eliminare una destinazione.