---
description: Informazioni utili per configurare le destinazioni in Audience Manager ed evitare problemi comuni.
seo-description: Informazioni utili per configurare le destinazioni in Audience Manager ed evitare problemi comuni.
seo-title: Risoluzione dei problemi di configurazione
title: Risoluzione dei problemi di configurazione
uuid: 04080 fb 9-6 c 7 b -4 de 7-960 e -54482 be 2 de 83
translation-type: tm+mt
source-git-commit: 118e8fa3f35bc77846c6518268448d57d779a2ee

---


# Risoluzione dei problemi di configurazione {#destination-setup-troubleshooting}

Informazioni utili per configurare le destinazioni in Audience Manager ed evitare problemi comuni.

## I set up a destination, but I don't see any files. Dove sono? {#destination-no-files}

<!-- c_dest_tshooting.xml -->

Problemi comuni di configurazione di destinazione:

### Destinazione non configurata

* **Chiave errata[!UICONTROL UserID]:** [!UICONTROL UserID] La chiave è la [!UICONTROL MasterDPID] posizione di questa destinazione e costituisce la base per i valori ID che verranno modificati. Anche se una [!UICONTROL UserID] chiave è selezionabile tramite l'elenco a discesa, non significa necessariamente che sono presenti ID/caratteristiche/segmenti mappati a questo valore. Se il [!UICONTROL Outbound] processo (che viene eseguito dopo la creazione delle destinazioni) non trova nessun utente mappato a questa [!UICONTROL UserID] chiave, nessun dato viene cancellato.
* **No in Origini dati file selezionata:** Quando scegliete un tipo di destinazione diverso da [!UICONTROL S2S], viene visualizzata una sezione nella parte inferiore dello schermo. [!UICONTROL Configure Data Sources] Quando viene visualizzata la sezione, non vengono selezionati valori. Se dimenticate di fare clic sulla [!UICONTROL All First Party] casella di controllo o di selezionare singolarmente le origini dati dalla [!UICONTROL Available Data Sources] finestra, nessun dato viene cancellato.

### Formato non configurato

Quando si seleziona un formato per i dati non vincolati, è consigliabile riutilizzare un formato esistente. L'utilizzo di un formato già collaudato assicura che i dati in uscita vengano generati correttamente. Per visualizzare esattamente la formattazione di un formato esistente, fate clic sull' [!UICONTROL Formats] opzione nella barra dei menu e cercate il formato per nome o per numero ID. I formati non formattati o le macro utilizzate nei formati forniscono un output formattato in modo errato o impediranno l'output completo delle informazioni.

Per ulteriori informazioni sulla configurazione dei formati e sull'uso delle macro, vedere [Macro Format Macro](formats/file-formats.md#) e [Macro delle macro HTTP](formats/web-formats.md).

### Server non configurato

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * Non inserite prefissi per i nomi host. Se vi viene assegnato un account [!DNL ftp://hello.com], immettete [!DNL hello.com] semplicemente questo campo.
   * **[!UICONTROL Port/Type Combination]**
      * Per un [!DNL FTP] trasferimento, il tipo di trasferimento preferito [!DNL SFTP]è.
      * Quando si seleziona il [!DNL SFTP] tipo, la porta è quasi sempre 22.
      * Quando si seleziona il [!DNL FTPs/TLS] tipo, la porta è quasi sempre 21.
      * [!DNL FTPs/TLS] Il tipo non equivale [!DNL FTP] a un trasferimento regolare. Non sono supportati [!DNL FTP] trasferimenti regolari (non protetti).
   * **[!UICONTROL Remote Path]**
      * Quando si sceglie un sottotracciato remoto, è necessario inserirlo senza barra iniziale.
      * Se il file trasferito deve essere inserito nella [!DNL (root)/inbound] sottocartella, dovete semplicemente aggiungere [!DNL inbound] solo [!DNL /inbound]il percorso remoto.
      * Se inviate più directory al percorso, inserite slash tra ciascuna directory. Se ti viene assegnata la posizione di [!DNL /inbound/subdirectory1/subdirectory2], devi immettere [!DNL inbound/subdirectory1/subdirectory2] in questo campo.
      * Se il file deve essere inserito nella directory instradata automaticamente dal server esterno, potete lasciare vuoto questo spazio. Non inserite un punto (. ), barra (/) o altro.

* **[!DNL S3]**
   * [!DNL S3] è il protocollo di trasferimento preferito (over [!DNL FTP] o [!DNL HTTP]).
      * **[!UICONTROL Bucket]**
         * Il nome del bucket deve essere elencato senza barre, prefissi, suffissi ecc. Se ti viene assegnato l'indirizzo [!DNL s3://your-bucket] , devi semplicemente aggiungere [!DNL your-bucket] a questo campo.
      * **[!UICONTROL Directory]**
         * Lasciare vuoto questo campo a meno che non venga espressamente specificata una sottodirectory in cui inserire i dati. Se vi viene assegnato l'indirizzo [!DNL s3://your-bucket/your-subdirectory], inserite [!DNL your-bucket] nel [!UICONTROL Bucket] campo e [!DNL your-subdirectory] deve essere aggiunto al [!UICONTROL Directory] campo. Non aggiungete barre precedenti.
         * Se dovete spostare più directory verso il basso, usate solo le barre come separatori. Pertanto, una posizione di [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] verrebbe inserita [!DNL your-bucket] nel [!UICONTROL Bucket] campo e [!DNL your-subdirectory1/your-subdirectory2] inserita nel [!UICONTROL Directory] campo.
      * **[!UICONTROL Access / Secret Keys]**
         * Quando [!DNL TechOps] si crea un bucket e si forniscono chiavi di accesso/segreto a un consulente, le credenziali sono in genere `READ-ONLY` credenti da consegnare al client. Queste credenziali non devono essere inserite nei [!UICONTROL Access / Secret Key] campi, perché questo determinerà errori nel trasferimento (poiché le credenziali sono di sola lettura, non scrivibili). Se [!DNL TechOps] si crea un bucket e si fornisce credenziali, il consulente deve richiedere anche una coppia di chiavi Adobe - NOT DA NON DATA a CLIENT - che consente di scrivere file su questo intervallo. Tale chiave deve essere aggiunta in questi campi.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * Immettete le informazioni di prefisso per [!DNL HTTP] le voci. Se vi viene assegnato un account [!DNL https://superduper.com], immettete questo [!DNL https://superduper.com] campo.
      * **[!UICONTROL URL Prefix]**
         * Quando aggiungete un [!DNL URL] prefisso, lasciate disattivata la barra precedente. Un indirizzo di [!DNL https://hello.com/r/x/y/z] deve [!DNL https://hello.com] essere inserito nel [!UICONTROL Domain] campo e [!DNL r/x/y/z] inserito qui nel [!UICONTROL URL Prefix] campo.
         * Se non [!UICONTROL URL Prefix] è necessario, lasciate vuoto questo valore.
      * **[!UICONTROL Authentication - SSH Key]**
         * Inserire il valore `SSH PRIVATE` chiave completo in questa casella, compresi intestazioni, piè di pagina e interruzioni di riga per garantire la corretta cifratura/archiviazione chiave.

### Tempo insufficiente per la generazione in uscita

Il processo di esclusione viene eseguito due volte al giorno e più processi (outbounding, pubblicazione, push in posizioni esterne, ecc.) deve essere eseguito prima che un file venga inviato alla destinazione finale. Una regola di thumb valida è che una destinazione deve essere configurata completamente almeno 24 ore prima che i dati vengano inviati in una posizione esterna.

### Dimensioni suddivisione file eccessive

Quando si aprono i file in destinazioni, è possibile suddividere i file in uscita più grandi in blocchi di file. Verificate che i singoli blocchi di file non superino i 10 GB. Vedere anche Nome file dati [in uscita: Sintassi ed esempi](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html).


## Come impostare le destinazioni per esportare gli ID di Experience Cloud, gli ID cliente o gli ID di Audience Manager nei file di dati in uscita {#set-up-destinations-export}

In [!UICONTROL Outbound Data Files]questa pagina viene illustrato come impostare le destinazioni per esportare i dati in base al tipo di ID desiderato.

<!-- set-up-destinations-mcid-aamid.xml -->

Le destinazioni consentono ai nostri clienti di attivare i dati su qualsiasi numero di canali digitali. Ad esempio, possono esportare dati di audience in altre [!DNL Adobe Experience Cloud] soluzioni ([!DNL Target], [!DNL Campaign]ecc.). Oppure, possono inviare dati a [!UICONTROL DSP]s, [!UICONTROL SSP]s o qualsiasi piattaforma integrata con Audience Manager. Teniamo un elenco dei partner con cui lavoriamo sulla nostra pagina Wiki [per le integrazioni](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>Per una descrizione dettagliata sulla creazione delle destinazioni nell'interfaccia utente Amministratore, consulta l'articolo [Crea o modifica destinazioni](companies/admin-manage-company-destinations.md#create-edit-company-destinations) società.

I clienti desiderano esportare diversi tipi di ID, a seconda della destinazione. Il grafico di configurazione seguente mostra le opzioni da selezionare per esportare le informazioni sul profilo correlate a diversi tipi di ID. È consigliabile fare riferimento anche all' [Indice degli ID in Audience Manager](https://marketing.adobe.com/resources/help/en_US/aam/ids-in-aam.html). Sono disponibili tre impostazioni importanti [!UICONTROL User ID Key][!UICONTROL Data Source Type][!UICONTROL Format]da considerare. I dettagli sono descritti qui sotto.

* [!UICONTROL User ID Key]. In [!UICONTROL Admin UI], andate a **[!UICONTROL Companies]**. Cerca la società del cliente e fai clic su di essa. Cercare **[!UICONTROL Destinations]** la scheda e premere **[!UICONTROL Add Destination]**. Nel **[!UICONTROL Add Destination]** flusso di lavoro, selezionate l' [!UICONTROL User ID Key]icona. Il [!UICONTROL User ID Key] filtro degli ID in entrata verrà filtrato dall'origine dati di destinazione e consente solo la trasmissione degli ID.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]. Seleziona questa opzione quando crei una destinazione nell'interfaccia utente di Audience Manager. Innanzitutto, selezionate [!UICONTROL Inbound], quindi selezionate il tipo di ID desiderato. Le opzioni sono:

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]. Questa opzione determina il formato di file da esportare. Nel **[!UICONTROL Add Destination]** flusso di lavoro, sotto **[!UICONTROL Batch Data]**, selezionate il formato.

Per esaminare un formato, accedete **[!UICONTROL Admin UI > Formats]** e cercate l [!UICONTROL Data Row] 'elemento. Questo elemento contiene una macro del formato file, &lt; MCID &gt; nell'esempio di seguito.

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> Configurazione No. </th> 
   <th colname="col1" class="entry"> <p>Chiave utente </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo origine dati </p> </th> 
   <th colname="col3" class="entry"> <p>Formato </p> </th> 
   <th colname="col4" class="entry"> <p>Tipo ID esportato </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> 1 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>&lt; DP_ UUID &gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>UUID Audience Manager </p> </td> 
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
   <td colname="col2"> <p>ID Audience Manager </p> </td> 
   <td colname="col3"> <p>&lt; DP_ UUID &gt; </p> </td> 
   <td colname="col4"> <p>UUID Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID Audience Manager </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID Audience Manager </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine dati a cui l'azienda ha accesso) </p> </td> 
   <td colname="col2"> <p>ID cliente </p> </td> 
   <td colname="col3"> <p>&lt; DP_ UUID &gt; </p> </td> 
   <td colname="col4"> <p>ID cliente (DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine dati a cui l'azienda ha accesso) </p> </td> 
   <td colname="col2"> <p>ID cliente </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine dati a cui l'azienda ha accesso) </p> </td> 
   <td colname="col2"> <p>ID cliente </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine dati a cui l'azienda ha accesso) </p> </td> 
   <td colname="col2"> <p>ID Audience Manager </p> </td> 
   <td colname="col3"> <p>&lt; DP_ UUID &gt; </p> </td> 
   <td colname="col4"> <p>UUID Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine dati a cui l'azienda ha accesso) </p> </td> 
   <td colname="col2"> <p>ID Audience Manager </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine dati a cui l'azienda ha accesso) </p> </td> 
   <td colname="col2"> <p>ID Audience Manager </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID Audience Manager </p> </td> 
  </tr> 
 </tbody> 
</table>

## Casi d'uso

Supponiamo che usi Audience Manager e [!DNL Campaign]. Per rendere i dati del cliente fruibili, [!DNL Campaign]esportate [!UICONTROL Experience Cloud IDs]. In questo caso dovreste utilizzare il numero di configurazione 3.