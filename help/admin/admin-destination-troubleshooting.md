---
description: Informazioni su come impostare le destinazioni in Audience Manager ed evitare problemi comuni.
seo-description: Information to help you set up destinations in Audience Manager and avoid common problems.
seo-title: Destination Setup Troubleshooting
title: Risoluzione dei problemi di impostazione della destinazione
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
exl-id: 53c72b1a-f1a1-4266-a595-e4821c2640b2
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 4%

---

# Risoluzione dei problemi di impostazione della destinazione {#destination-setup-troubleshooting}

Informazioni su come impostare le destinazioni in Audience Manager ed evitare problemi comuni.

## Ho impostato una destinazione, ma non vedo alcun file. Dove sono? {#destination-no-files}

<!-- c_dest_tshooting.xml -->

I problemi comuni di configurazione della destinazione includono:

### Destinazione non configurata correttamente

* **Errato [!UICONTROL UserID] Chiave:** Il [!UICONTROL UserID] chiave è la [!UICONTROL MasterDPID] di questa destinazione e rappresenta la base per i valori ID che verranno esclusi. Anche se un [!UICONTROL UserID] Key è selezionabile tramite l’elenco a discesa, non significa necessariamente che siano presenti ID, caratteristiche o segmenti mappati a questo valore. Se il [!UICONTROL Outbound] Il processo (che viene eseguito dopo la creazione delle destinazioni) non trova alcun utente mappato a questo [!UICONTROL UserID] chiave, nessun dato sarà in uscita.
* **Nessuna Origine Dati In File Selezionata:** Quando si sceglie un tipo di destinazione diverso da [!UICONTROL S2S], nella parte inferiore della schermata viene visualizzata una sezione con l’etichetta [!UICONTROL Configure Data Sources]. Quando questa sezione viene visualizzata per la prima volta, non viene selezionato alcun valore. Se dimentica di fare clic su [!UICONTROL All First Party] o di selezionare singolarmente le origini dati dall&#39; [!UICONTROL Available Data Sources] , nessun dato risulterà in uscita.

### Formato non configurato correttamente

Quando selezioni un formato per i dati in uscita, è consigliabile, se possibile, riutilizzare un formato esistente. L’utilizzo di un formato già collaudato garantisce che i dati in uscita vengano generati correttamente. Per visualizzare esattamente la formattazione di un formato esistente, fare clic sul pulsante [!UICONTROL Formats] nella barra dei menu e cercare il formato in base al nome o al numero ID. I formati non validi o le macro utilizzate nei formati forniscono un output formattato in modo errato o impediscono la trasmissione completa delle informazioni.

Per ulteriori informazioni sulla configurazione dei formati e sull&#39;utilizzo delle macro, vedere [Macro per formati file](formats/file-formats.md#) e [Macro per il formato HTTP](formats/web-formats.md).

### Server non configurato correttamente

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * Non immettere prefissi per i nomi host. Se ti viene fornito un account [!DNL ftp://hello.com], inserisci semplicemente [!DNL hello.com] in questo campo.
   * **[!UICONTROL Port/Type Combination]**
      * Per un [!DNL FTP] trasferimento, il tipo di trasferimento preferito è [!DNL SFTP].
      * Quando si seleziona [!DNL SFTP] tipo, la porta è quasi sempre 22.
      * Quando si seleziona [!DNL FTPs/TLS] tipo, la porta è quasi sempre 21.
      * Il [!DNL FTPs/TLS] tipo non è uguale a un normale [!DNL FTP] trasferimento. Non sono supportati i servizi regolari (non sicuri) [!DNL FTP] trasferimenti.
   * **[!UICONTROL Remote Path]**
      * Quando si sceglie un percorso secondario remoto, questo deve essere immesso senza barra iniziale.
      * Se il file trasferito deve essere inserito nel [!DNL (root)/inbound] sottocartella, aggiungi semplicemente [!DNL inbound] per il percorso remoto, non [!DNL /inbound].
      * Se si inviano i file in più directory lungo il percorso, inserire delle barre tra ciascuna directory. Se ti è stata data la posizione di [!DNL /inbound/subdirectory1/subdirectory2], devi immettere [!DNL inbound/subdirectory1/subdirectory2] in questo campo.
      * Se il file deve essere inserito nella directory automaticamente indirizzata al server esterno, è possibile lasciare vuoto questo spazio. Non inserire un punto ( . ), barra ( / ) o qualsiasi altra cosa.

* **[!DNL S3]**
   * [!DNL S3] è il protocollo di trasferimento preferito (rispetto [!DNL FTP] o [!DNL HTTP]).
      * **[!UICONTROL Bucket]**
         * Il nome del bucket deve essere elencato senza barre, prefissi, suffissi e così via. Se ti viene fornito l’indirizzo [!DNL s3://your-bucket] devi semplicemente aggiungere [!DNL your-bucket] in questo campo.
      * **[!UICONTROL Directory]**
         * Lascia questo campo vuoto a meno che non ti venga specificamente assegnata una sottodirectory in cui inserire i dati. Se ti viene fornito l’indirizzo [!DNL s3://your-bucket/your-subdirectory], immetti [!DNL your-bucket] nel [!UICONTROL Bucket] campo e [!DNL your-subdirectory] deve essere aggiunto al [!UICONTROL Directory] campo. Non aggiungere barre precedenti.
         * Se devi percorrere più directory lungo il percorso, utilizza le barre come separatori. Quindi una posizione di [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] avrebbe [!DNL your-bucket] nel [!UICONTROL Bucket] campo e [!DNL your-subdirectory1/your-subdirectory2] è entrato nel [!UICONTROL Directory] campo.
      * **[!UICONTROL Access / Secret Keys]**
         * Quando [!DNL TechOps] crea un bucket e fornisce a un consulente le chiavi di accesso/segreto; in genere, si tratta di credenziali `READ-ONLY` credenziali che devono essere consegnate al client. Queste credenziali non devono essere immesse in [!UICONTROL Access / Secret Key] , perché questo causerà un errore nel trasferimento (perché le credenziali sono di sola lettura, non scrivibili). Nel caso in cui [!DNL TechOps] crea un bucket e fornisce le credenziali. Il consulente deve inoltre richiedere una coppia di chiavi di Adobe, DA NON FORNIRE AL CLIENT, che consenta la scrittura di file in questo bucket. Tale chiave deve essere aggiunta in questi campi.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * Immetti le informazioni sul prefisso per [!DNL HTTP] voci. Se ti viene fornito un account [!DNL https://superduper.com], immetti [!DNL https://superduper.com] in questo campo.
      * **[!UICONTROL URL Prefix]**
         * Quando si aggiunge una [!DNL URL] prefisso, lascia deselezionata la barra precedente. Un indirizzo di [!DNL https://hello.com/r/x/y/z] dovrebbe avere [!DNL https://hello.com] immessi nel [!UICONTROL Domain] campo e [!DNL r/x/y/z] immessi qui nel [!UICONTROL URL Prefix] campo.
         * Se un [!UICONTROL URL Prefix] non è necessario, lascia vuoto questo valore.
      * **[!UICONTROL Authentication - SSH Key]**
         * Inserisci il valore completo `SSH PRIVATE` valore chiave in questa casella, inclusi intestazioni, piè di pagina e interruzioni di riga per garantire una crittografia accurata/archiviazione delle chiavi.

### Tempo insufficiente per la generazione in uscita

Il processo di outbounding viene eseguito due volte al giorno e più processi (outbounding, pubblicazione, push in posizioni esterne, ecc.) deve essere eseguito prima che un file venga inviato alla relativa destinazione finale. Una buona regola è che una destinazione deve essere completamente configurata almeno 24 ore prima di poter prevedere che i dati vengano inviati a una posizione esterna.

### Dimensioni di suddivisione file troppo grandi

Quando esegui l’outbounding di file nelle destinazioni, puoi suddividere file in uscita di dimensioni maggiori in blocchi di file. Assicurati che i singoli blocchi di file non superino i 10 GB. Vedi anche, [Nome dei file di dati in uscita: sintassi ed esempi](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html?lang=en).


## Come impostare le destinazioni per esportare ID Experience Cloud, ID cliente o ID Audience Manager in file di dati in uscita {#set-up-destinations-export}

Questa pagina mostra come impostare le destinazioni per esportare dati con chiave del tipo ID desiderato in [!UICONTROL Outbound Data Files].

<!-- set-up-destinations-mcid-aamid.xml -->

Le destinazioni consentono ai nostri clienti di attivare i propri dati su qualsiasi numero di canali digitali. Ad esempio, possono esportare i dati del pubblico in altri [!DNL Adobe Experience Cloud] soluzioni ([!DNL Target], [!DNL Campaign], ecc.). Oppure, possono inviare dati a [!UICONTROL DSP]s [!UICONTROL SSP]s o qualsiasi piattaforma integrata con Audience Manager. Abbiamo una lista di partner con cui lavoriamo [Pagina wiki Integrazioni](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>Per una procedura dettagliata sulla creazione di destinazioni nell’interfaccia utente di amministrazione, consulta [Creare o modificare le destinazioni aziendali](companies/admin-manage-company-destinations.md#create-edit-company-destinations) articolo.

I clienti vogliono esportare diversi tipi di ID, a seconda della destinazione. Il grafico di configurazione seguente mostra le opzioni da selezionare per esportare le informazioni di profilo relative a diversi tipi di ID. Si consiglia inoltre di consultare il [Indice degli ID in Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html?lang=en). Sono disponibili tre importanti impostazioni da considerare: [!UICONTROL User ID Key], il [!UICONTROL Data Source Type] e [!UICONTROL Format]. Di seguito vengono fornite informazioni dettagliate su tutti i dettagli.

* [!UICONTROL User ID Key]. In [!UICONTROL Admin UI], vai a **[!UICONTROL Companies]**. Cerca l’azienda del cliente e fai clic su di essa. Cerca **[!UICONTROL Destinations]** Tab e premere **[!UICONTROL Add Destination]**. In **[!UICONTROL Add Destination]** flusso di lavoro, seleziona la [!UICONTROL User ID Key]. Il [!UICONTROL User ID Key] filtra gli ID in arrivo dall’origine dati di destinazione e consente solo il passaggio degli ID.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]. Seleziona questa opzione durante la creazione di una destinazione nell’interfaccia utente di Audience Manager. Prima di tutto, seleziona [!UICONTROL Inbound], quindi seleziona il tipo di ID desiderato. Le opzioni sono:

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]. Questa opzione determina il formato del file da esportare. In **[!UICONTROL Add Destination]** workflow, in **[!UICONTROL Batch Data]**, seleziona il formato.

Per esaminare un formato, passare a **[!UICONTROL Admin UI > Formats]** e cerca il [!UICONTROL Data Row] elemento. Questo elemento contiene una macro del formato file, &lt;mcid> nell’esempio seguente.

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> Nr. configurazione </th> 
   <th colname="col1" class="entry"> <p>Chiave utente </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo di origine dati </p> </th> 
   <th colname="col3" class="entry"> <p>Formato </p> </th> 
   <th colname="col4" class="entry"> <p>Tipo ID esportato </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> 1 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>UUID AUDIENCE MANAGER </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID AUDIENCE MANAGER </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>UUID AUDIENCE MANAGER </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID AUDIENCE MANAGER </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID AUDIENCE MANAGER </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID AUDIENCE MANAGER </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine dati a cui l’azienda ha accesso) </p> </td> 
   <td colname="col2"> <p>ID cliente </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>ID cliente (DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine dati a cui l’azienda ha accesso) </p> </td> 
   <td colname="col2"> <p>ID cliente </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine dati a cui l’azienda ha accesso) </p> </td> 
   <td colname="col2"> <p>ID cliente </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID AUDIENCE MANAGER </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine dati a cui l’azienda ha accesso) </p> </td> 
   <td colname="col2"> <p>ID AUDIENCE MANAGER </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>UUID AUDIENCE MANAGER </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine dati a cui l’azienda ha accesso) </p> </td> 
   <td colname="col2"> <p>ID AUDIENCE MANAGER </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine dati a cui l’azienda ha accesso) </p> </td> 
   <td colname="col2"> <p>ID AUDIENCE MANAGER </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID AUDIENCE MANAGER </p> </td> 
  </tr> 
 </tbody> 
</table>

## Casi d&#39;uso

Supponiamo che utilizzi Audience Manager e [!DNL Campaign]. Per rendere utilizzabili i dati del cliente in [!DNL Campaign], si desidera esportare [!UICONTROL Experience Cloud IDs]. In questo caso, utilizza il numero di configurazione 3.
