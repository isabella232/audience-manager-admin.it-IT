---
description: Creare, modificare ed eliminare destinazioni di Audienci Manager.
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

Creare, modificare ed eliminare destinazioni di Audienci Manager.

<!-- t_company_destinations.xml -->

Per informazioni dettagliate, consulta [Destinazioni](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/destinations.html) nella *Guida utente di Audience Manager*.

## Creare o modificare le destinazioni aziendali {#create-edit-company-destinations}

Scorri le sezioni per istruzioni dettagliate su come creare nuove destinazioni [!DNL Audience Manager] o modificare destinazioni esistenti.

<!-- create-edit-company-destinations.xml -->

Visita la [pagina di integrazione dei partner di Experience Cloud](https://wiki.corp.adobe.com/x/mPIMPw) prima di configurare le destinazioni. La pagina contiene le informazioni specifiche da compilare per ogni integrazione con i partner [!DNL Audience Manager].

Se il cliente desidera utilizzare [!DNL Adobe Media Optimizer] come destinazione in [!DNL Audience Manager] , è necessario impostarlo in [!DNL Adobe Media Optimizer].

## Passa alla scheda Destinazioni {#navigate-destinations}

1. Fai clic su **[!UICONTROL Companies]**, quindi individua e fai clic sulla società desiderata per visualizzare la relativa pagina [!UICONTROL Profile]. Puoi utilizzare la casella [!UICONTROL Search] o i controlli di impaginazione in fondo all’elenco per trovare l’azienda desiderata. Per ordinare ciascuna colonna in ordine crescente o decrescente, fai clic sull’intestazione della colonna desiderata.
1. Fai clic sulla scheda **[!UICONTROL Destinations]** .
1. Per creare una nuova destinazione, fai clic su **[!UICONTROL Add Destination]**. Per modificare una destinazione esistente, fai clic sul nome della destinazione nella colonna **[!UICONTROL Name]** .

## Impostazioni di base {#basic-settings}

Compila i campi nella finestra **[!UICONTROL Basic Settings]**.

* **[!UICONTROL Name]:**  (Obbligatorio) Specifica il nome della destinazione.
* **[!UICONTROL Description]:** specifica le informazioni descrittive sulla destinazione.
* **[!UICONTROL Type]:**  (Obbligatorio) Seleziona il tipo di destinazione desiderato:
   * **[!UICONTROL Bulk ID]**: Sincronizza gli ID tra piattaforme diverse.
   * **[!UICONTROL Bulk Trait]**: Inviare informazioni sulle caratteristiche in blocco a piattaforme diverse.
   * **[!UICONTROL Bulk Segment]**: Invia informazioni sui segmenti in blocco a piattaforme diverse.
   * **[!UICONTROL S2S]**: Utilizza le destinazioni server-to-server per inviare dati in tempo reale e batch a piattaforme diverse.
* **[!UICONTROL Auto-Fill Destination Mapping]:** (  [!UICONTROL S2S] solo) Seleziona un’opzione:
   * **[!UICONTROL Segment ID]:** Se selezioni questa impostazione, la mappatura del valore di destinazione viene compilata con l’ID  [!DNL Audience Manager] segmento.
   * **[!UICONTROL Integration Code Value]:** Se selezioni questa impostazione, la mappatura del valore di destinazione viene compilata con il codice di integrazione del  [!DNL Audience Manager] segmento.
* **[!UICONTROL User ID Key]:**  (Obbligatorio) Seleziona dall’elenco a discesa la chiave ID utente desiderata per la destinazione.

Questo ID viene utilizzato come ID sorgente dati principale. Questo determina gli ID utente da escludere nel file .

>[!NOTE]
>
>Per il tipo di destinazione [!UICONTROL Bulk ID] non è possibile utilizzare l&#39;ID [!DNL Audience Manager] [!UICONTROL User ID] o [!DNL Adobe Experience Cloud].

Se l&#39;ID origine dati ( [!UICONTROL DPID]) non viene visualizzato nell&#39;elenco a discesa, è necessario selezionare la casella di controllo **[!UICONTROL Outbound]** a livello di origine dati nella pagina [Impostazioni origine dati](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/manage-datasources.html).

* **[!UICONTROL Target Data Source]:**  (Obbligatorio) Seleziona dall’elenco a discesa l’origine dati desiderata per la destinazione. Questa impostazione consente l’etichettatura dei dati non vincolati, il che consente l’inserimento in sistemi separati sul lato client.
* **[!UICONTROL Foreign Account ID]:** specifica l’ID account esterno per questa destinazione. Si tratta del valore di identificazione nel sistema del destinatario per questi dati non delimitati.
* **[!UICONTROL Outbound Sample Rate Denominator]:** quando la quantità totale di dati restituiti è sconosciuta, utilizza questa impostazione per restituire solo una quantità di dati campione, anziché la quantità completa. Regola il numero qui per rappresentare una frazione dei dati (ad esempio, un valore di &#39;100&#39; restituisce 1/100 la quantità regolare di dati, un valore di &#39;10&#39; restituisce 1/10 la quantità regolare di dati). Il valore predefinito è &quot;1&quot;, che restituisce tutti i dati.

## Dati in tempo reale (per le destinazioni S2S) {#realtime-s2s}

Se stai creando una destinazione [!UICONTROL S2S], compila i campi seguenti:

**[!UICONTROL Servers]**: Seleziona il  `HTTP` server desiderato per questa destinazione.
**[!UICONTROL Format]**: Seleziona il formato desiderato per la destinazione dall’elenco a discesa:  [!UICONTROL HTTP only].

>[!NOTE]
>
>Solo per [!DNL S2S] è possibile abilitare o disabilitare le destinazioni [!UICONTROL Realtime] o [!UICONTROL Batch] utilizzando i cursori On/Off sullo schermo. Non è possibile disabilitare entrambe le opzioni.

## Dati in batch {#batch-data}

Per le destinazioni [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] o [!UICONTROL Bulk Segment] , compila i campi seguenti:

* **[!UICONTROL Protocol]**: (Obbligatorio) Seleziona il protocollo desiderato per questa destinazione dall&#39;elenco a discesa:
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**: (Obbligatorio) Seleziona il server desiderato per questa destinazione dall’elenco a discesa.
* **[!UICONTROL Format]**: (Obbligatorio) Seleziona il formato desiderato per questa destinazione dall’elenco a discesa:  [!DNL HTTP] o il tipo di file, a seconda del protocollo scelto in precedenza.
* **[!UICONTROL Sync Type]**: (Obbligatorio) Seleziona il tipo di sincronizzazione desiderato per questa destinazione. Questo indica il livello di attività utente che i client vorrebbero includere negli ordini in uscita. Seleziona **[!UICONTROL Customer]** se i clienti sono interessati solo ad analizzare le qualifiche dei segmenti dalle loro proprietà. Seleziona **[!UICONTROL Platform]** se desideri includere le qualifiche dei segmenti dalle attività fuori sito in tutti i clienti [!DNL Audience Manager].
* **[!UICONTROL Customer]**: Il file contiene utenti attivi che hanno almeno 1 realizzazione di caratteristiche solo sulle proprietà del client (associate a  [!UICONTROL PID]) per il periodo di tempo selezionato. I clienti devono utilizzare questa opzione per esporre le loro qualifiche di segmento *in tempo reale* alle destinazioni.
* **[!UICONTROL Platform]**: Il file contiene utenti attivi con almeno 1 interazione in tempo reale, sia che si tratti della sincronizzazione ID o della realizzazione di caratteristiche, in qualsiasi punto delle proprietà  [!DNL Audience Manager] dei client (associate a tutti i PID del client) per il periodo di tempo selezionato. I clienti devono utilizzare questa opzione per esporre le loro qualifiche di segmento *total* alle destinazioni.
* **[!UICONTROL Lifetime]**: Il file contiene gli utenti attivi visualizzati in qualsiasi punto di tutte le proprietà  [!DNL Audience Manager] dei client dalla creazione della destinazione.
* **[!UICONTROL Sync Type Lookback Period]**: Se selezioni  [!UICONTROL Customer] o  [!UICONTROL Platform], seleziona un periodo di tempo. I file contengono utenti attivi per il periodo di tempo selezionato.
Quindi, seleziona il tipo di ordine. Indica la frequenza e l’ambito di ogni integrazione in uscita con i partner. Selezionare tra ordini incrementali e ordini completi.
* **[!UICONTROL Incremental Scheduled Run]**: Per ogni esecuzione,  [!DNL Audience Manager] verranno inviati solo i nuovi utenti netti qualificati dal precedente ordine in uscita. Selezionare il periodo di tempo desiderato [!DNL Audience Manager] per eseguire i processi di sincronizzazione incrementale. Ad esempio, puoi selezionare ogni 24 ore, ogni sette giorni, ogni 30 giorni o mai.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>Il primo ordine incrementale è equivalente a un ordine completo perché nessun utente precedente è stato mai inviato alla destinazione.

* **[!UICONTROL Full Sync Scheduled Run]**: Con ogni esecuzione,  [!DNL Audience Manager] eseguirà l’uscita di tutti gli utenti attivi dalla prima configurazione della destinazione. Selezionare la pianificazione desiderata da utilizzare [!DNL Audience Manager] per eseguire i processi di sincronizzazione completa. Ad esempio, puoi selezionare ogni 24 ore, ogni sette giorni, ogni 30 giorni o mai.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>È consigliabile utilizzare sincronizzazioni incrementali con maggiore frequenza rispetto alle sincronizzazioni complete. Le sincronizzazioni incrementali inviano solo file che contengono nuove realizzazioni delle caratteristiche o sincronizzazioni ID. Le sincronizzazioni complete inviano tutti i file, indipendentemente dal fatto che includano o meno nuove realizzazioni o sincronizzazioni ID. Utilizza la configurazione [!UICONTROL Full Sync Scheduled Run] solo quando i client hanno bisogno di una copia completa di tutti i loro utenti, per ridurre il volume di dati in uscita.

## Configurare Origini dati {#configure-data-sources}

Per le destinazioni [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] o [!UICONTROL Bulk Segment] , compila i campi seguenti. Queste impostazioni consentono di inviare tutti i dati (caratteristiche, segmenti o ID, in base al tipo selezionato) associati alle origini dati.

* **[!UICONTROL All Unrestricted First Party Data]**: Selezionare questa opzione per utilizzare tutte le origini dati di prime parti. Se selezioni questa opzione, le opzioni [!UICONTROL Available Data Sources] sono disabilitate.
* **[!UICONTROL Available Data Sources]**: Utilizza le frecce per spostare le origini dati tra le  **[!UICONTROL Available Data Sources]** caselle e  **[!UICONTROL In File Data Sources]** .

## Salva e completa {#save-and-finalize}

Il pulsante **[!UICONTROL Save]** viene attivato dopo aver compilato tutti i campi obbligatori. Fai clic su **[!UICONTROL Save]** per finalizzare il processo di creazione della destinazione.

## Eliminare le destinazioni aziendali {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

Per eliminare una destinazione:

1. Fai clic su **[!UICONTROL Companies]**, individua e fai clic sulla società desiderata, quindi fai clic sulla scheda **[!UICONTROL Destinations]** .
1. Fai clic su ![](assets/icon_delete.png) nella colonna **[!UICONTROL Actions]** della destinazione desiderata.
1. Fai clic su **[!UICONTROL OK]** per confermare l’eliminazione.

>[!NOTE]
>
>Non puoi eliminare una destinazione se ha dei segmenti mappati su di essa.
