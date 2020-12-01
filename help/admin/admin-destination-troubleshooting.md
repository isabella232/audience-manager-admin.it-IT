---
description: Informazioni utili per configurare le destinazioni in  Audience Manager ed evitare problemi comuni.
seo-description: Informazioni utili per configurare le destinazioni in  Audience Manager ed evitare problemi comuni.
seo-title: Risoluzione dei problemi di impostazione della destinazione
title: Risoluzione dei problemi di impostazione della destinazione
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
translation-type: tm+mt
source-git-commit: 118e8fa3f35bc77846c6518268448d57d779a2ee
workflow-type: tm+mt
source-wordcount: '1331'
ht-degree: 4%

---


# Risoluzione dei problemi di impostazione della destinazione {#destination-setup-troubleshooting}

Informazioni utili per configurare le destinazioni in  Audience Manager ed evitare problemi comuni.

## Ho impostato una destinazione, ma non vedo alcun file. Dove sono? {#destination-no-files}

<!-- c_dest_tshooting.xml -->

I problemi comuni di configurazione della destinazione includono i seguenti problemi:

### Destinazione non configurata

* **[!UICONTROL UserID] Chiave errata:** la  [!UICONTROL UserID] chiave è il nome  [!UICONTROL MasterDPID] di questa destinazione ed è la base per i valori ID che verranno ignorati. Anche se una chiave [!UICONTROL UserID] è selezionabile tramite l&#39;elenco a discesa, non significa necessariamente che vi sono ID/caratteristiche/segmenti mappati a questo valore. Se il processo [!UICONTROL Outbound] (che viene eseguito dopo la creazione delle destinazioni) non rileva alcun utente mappato a questa chiave [!UICONTROL UserID], nessun dato verrà escluso.
* **Nessuna origine dati file selezionata:** quando si sceglie un tipo di destinazione diverso da  [!UICONTROL S2S], viene visualizzata una sezione nella parte inferiore della schermata con l&#39;etichetta  [!UICONTROL Configure Data Sources]. Quando questa sezione viene visualizzata per la prima volta, non viene selezionato alcun valore. Se si dimentica di fare clic sulla casella di controllo [!UICONTROL All First Party] o di selezionare singolarmente le origini dati dalla finestra [!UICONTROL Available Data Sources], nessun dato verrà escluso.

### Formato non configurato

Quando si seleziona un formato per i dati non delimitati, è consigliabile, se possibile, riutilizzare un formato esistente. L&#39;utilizzo di un formato già collaudato garantisce la generazione dei dati in uscita. Per visualizzare esattamente la formattazione di un formato esistente, fate clic sull&#39;opzione [!UICONTROL Formats] nella barra dei menu e cercate il formato per nome o per numero di ID. I formati errati o le macro utilizzate nei formati forniranno un output formattato in modo errato o impediranno l&#39;output completo delle informazioni.

Per ulteriori informazioni sull&#39;impostazione dei formati e l&#39;utilizzo delle macro, vedere [Macro di formati file](formats/file-formats.md#) e [Macros di formato HTTP](formats/web-formats.md).

### Server non configurato

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * Non immettere alcun prefisso per i nomi host. Se ti viene assegnato un account [!DNL ftp://hello.com], immetti semplicemente [!DNL hello.com] in questo campo.
   * **[!UICONTROL Port/Type Combination]**
      * Per un trasferimento [!DNL FTP], il tipo di trasferimento preferito è [!DNL SFTP].
      * Quando si seleziona il tipo [!DNL SFTP], la porta è quasi sempre 22.
      * Quando si seleziona il tipo [!DNL FTPs/TLS], la porta è quasi sempre 21.
      * Il tipo [!DNL FTPs/TLS] non equivale a un normale [!DNL FTP] trasferimento. I trasferimenti [!DNL FTP] regolari (non protetti) non sono supportati.
   * **[!UICONTROL Remote Path]**
      * Quando si sceglie un sottopercorso remoto, questo deve essere immesso senza barra di scorrimento iniziale.
      * Se il file trasferito deve essere inserito nella sottocartella [!DNL (root)/inbound], è sufficiente aggiungere [!DNL inbound] per il percorso remoto, non [!DNL /inbound].
      * Se inviate i file a più directory lungo il percorso, immettete delle barre tra ciascuna directory. Se viene indicata la posizione di [!DNL /inbound/subdirectory1/subdirectory2], immettere [!DNL inbound/subdirectory1/subdirectory2] in questo campo.
      * Se il file deve essere inserito nella directory automaticamente instradato dal server esterno, è possibile lasciare vuoto questo spazio. Non inserire un punto ( . ), barra ( / ) o altro.

* **[!DNL S3]**
   * [!DNL S3] è il protocollo di trasferimento preferito (sopra  [!DNL FTP] o  [!DNL HTTP]).
      * **[!UICONTROL Bucket]**
         * Il nome del bucket deve essere elencato senza barre, prefissi, suffissi, ecc. Se hai l&#39;indirizzo [!DNL s3://your-bucket] devi semplicemente aggiungere [!DNL your-bucket] a questo campo.
      * **[!UICONTROL Directory]**
         * Lasciare vuoto questo campo a meno che non venga specificatamente specificata una sottodirectory in cui inserire i dati. Se si dispone dell&#39;indirizzo [!DNL s3://your-bucket/your-subdirectory], immettere [!DNL your-bucket] nel campo [!UICONTROL Bucket] e [!DNL your-subdirectory] aggiungere [!UICONTROL Directory] nel campo &lt;a4/>. Non aggiungere barre precedenti.
         * Se è necessario scorrere più directory lungo il percorso, è consigliabile utilizzare solo le barre come separatori. Pertanto, una posizione di [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] avrebbe [!DNL your-bucket] nel campo [!UICONTROL Bucket] e [!DNL your-subdirectory1/your-subdirectory2] inserito nel campo [!UICONTROL Directory].
      * **[!UICONTROL Access / Secret Keys]**
         * Quando [!DNL TechOps] crea un bucket e fornisce chiavi di accesso/segreto a un consulente, tali credenziali in genere sono `READ-ONLY` che devono essere consegnate al client. Queste credenziali non devono essere inserite nei campi [!UICONTROL Access / Secret Key], perché questo causerà il mancato trasferimento (perché tali credenziali sono di sola lettura, non scrivibili). Nel caso in cui [!DNL TechOps] crei un bucket e fornisca le credenziali, il consulente deve anche richiedere una coppia di chiavi di Adobe  - NON DA DARE AL CLIENT - che consenta di scrivere i file in questo bucket. Tale chiave dovrebbe essere aggiunta in questi campi.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * Non immettere informazioni di prefisso per le voci [!DNL HTTP]. Se ti è stato assegnato un account [!DNL https://superduper.com], immetti [!DNL https://superduper.com] in questo campo.
      * **[!UICONTROL URL Prefix]**
         * Quando aggiungete un prefisso [!DNL URL], lasciate disattivata la barra precedente. Un indirizzo di [!DNL https://hello.com/r/x/y/z] deve essere [!DNL https://hello.com] immesso nel campo [!UICONTROL Domain] e [!DNL r/x/y/z] immesso qui nel campo [!UICONTROL URL Prefix].
         * Se non è necessario un valore [!UICONTROL URL Prefix], lasciare vuoto questo valore.
      * **[!UICONTROL Authentication - SSH Key]**
         * Immettete il valore chiave `SSH PRIVATE` completo in questa casella, comprese intestazioni, piè di pagina e interruzioni di riga, per garantire la corretta crittografia o archiviazione delle chiavi.

### Tempo insufficiente per la generazione in uscita

Il processo di outbounding viene eseguito due volte al giorno e più processi (outbounding, publishing, push a posizioni esterne, ecc.) deve essere eseguito prima che un file venga inviato alla destinazione finale. Una buona regola è che una destinazione deve essere configurata completamente almeno 24 ore prima di poter prevedere che i dati vengano inviati a una posizione esterna.

### Dimensioni di divisione file troppo grandi

Quando si estendono i file alle destinazioni, è possibile suddividere i file in uscita di maggiori dimensioni in blocchi di file. Accertatevi che i singoli blocchi di file non superino i 10 GB. Vedere anche, [Nome file dati in uscita: Sintassi ed esempi](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html).


## Come impostare le destinazioni per l&#39;esportazione  ID Experience Cloud, ID cliente o ID  Audience Manager nei file di dati in uscita {#set-up-destinations-export}

In questa pagina viene illustrato come impostare le destinazioni per l&#39;esportazione di dati con chiave del tipo di ID desiderato in [!UICONTROL Outbound Data Files].

<!-- set-up-destinations-mcid-aamid.xml -->

Le destinazioni consentono ai nostri clienti di attivare i loro dati su qualsiasi numero di canali digitali. Ad esempio, possono esportare i dati del pubblico in altre soluzioni [!DNL Adobe Experience Cloud] ([!DNL Target], [!DNL Campaign], ecc.). Oppure, possono inviare dati a [!UICONTROL DSP]s, [!UICONTROL SSP]s, o a qualsiasi piattaforma integrata con  Audience Manager. Teniamo un elenco dei partner con cui lavoriamo sulla nostra [pagina Wiki Integrations](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>Per informazioni dettagliate sulla creazione di destinazioni nell&#39;interfaccia utente Amministratore, consultate l&#39;articolo [Crea o modifica destinazioni società](companies/admin-manage-company-destinations.md#create-edit-company-destinations).

I clienti desiderano esportare tipi di ID diversi, a seconda della destinazione. Il grafico di configurazione seguente mostra le opzioni che è necessario selezionare per esportare le informazioni di profilo relative ai diversi tipi di ID. È inoltre consigliabile fare riferimento al [Indice di ID in  Audience Manager](https://marketing.adobe.com/resources/help/en_US/aam/ids-in-aam.html). Sono disponibili tre impostazioni importanti: [!UICONTROL User ID Key], [!UICONTROL Data Source Type] e [!UICONTROL Format]. Di seguito li descriviamo tutti in dettaglio.

* [!UICONTROL User ID Key]. In [!UICONTROL Admin UI], passare a **[!UICONTROL Companies]**. Cerca la società del cliente e fai clic su di essa. Cercare la scheda **[!UICONTROL Destinations]** e premere **[!UICONTROL Add Destination]**. Nel flusso di lavoro **[!UICONTROL Add Destination]**, selezionare [!UICONTROL User ID Key]. Gli [!UICONTROL User ID Key] filtreranno gli ID in entrata dall&#39;origine dati di destinazione e consentiranno solo il passaggio degli ID.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]. Selezionate questa opzione quando create una destinazione nell’interfaccia utente del Audience Manager . Innanzitutto, selezionare [!UICONTROL Inbound], quindi selezionare il tipo di ID desiderato. Le opzioni sono:

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]. Questa opzione determina il formato di file che verrà esportato. Nel flusso di lavoro **[!UICONTROL Add Destination]**, in **[!UICONTROL Batch Data]**, selezionare il formato.

Per analizzare un formato, andate a **[!UICONTROL Admin UI > Formats]** e cercate l&#39;elemento [!UICONTROL Data Row]. Questo elemento contiene una macro del formato di file, &lt;MCID> nell&#39;esempio seguente.

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> N. configurazione </th> 
   <th colname="col1" class="entry"> <p>Chiave utente </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo origine dati </p> </th> 
   <th colname="col3" class="entry"> <p>Formato </p> </th> 
   <th colname="col4" class="entry"> <p>Tipo di ID esportato </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> 1 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>ID Experience Cloud  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID Experience Cloud  </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p> UUID Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID Experience Cloud  </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>ID Experience Cloud  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID Audience Manager  </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p> UUID Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID Audience Manager  </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>ID Experience Cloud  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID Audience Manager  </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p> UUID Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine dati a cui la società ha accesso) </p> </td> 
   <td colname="col2"> <p>ID cliente </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>ID cliente (DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine dati a cui la società ha accesso) </p> </td> 
   <td colname="col2"> <p>ID cliente </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>ID Experience Cloud  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine dati a cui la società ha accesso) </p> </td> 
   <td colname="col2"> <p>ID cliente </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p> UUID Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine dati a cui la società ha accesso) </p> </td> 
   <td colname="col2"> <p>ID Audience Manager  </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p> UUID Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine dati a cui la società ha accesso) </p> </td> 
   <td colname="col2"> <p>ID Audience Manager  </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>ID Experience Cloud  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine dati a cui la società ha accesso) </p> </td> 
   <td colname="col2"> <p>ID Audience Manager  </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p> UUID Audience Manager </p> </td> 
  </tr> 
 </tbody> 
</table>

## Casi d&#39;uso

Supponiamo che tu utilizzi  Audience Manager e [!DNL Campaign]. Per rendere i dati del cliente fruibili in [!DNL Campaign], si desidera esportare [!UICONTROL Experience Cloud IDs]. In questo caso, devi usare il numero di configurazione 3.