---
description: Informazioni utili per impostare le destinazioni in Audience Manager ed evitare problemi comuni.
seo-description: Information to help you set up destinations in Audience Manager and avoid common problems.
seo-title: Destination Setup Troubleshooting
title: Risoluzione dei problemi di impostazione della destinazione
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
exl-id: 53c72b1a-f1a1-4266-a595-e4821c2640b2
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 4%

---

# Risoluzione dei problemi di impostazione della destinazione {#destination-setup-troubleshooting}

Informazioni utili per impostare le destinazioni in Audience Manager ed evitare problemi comuni.

## Ho impostato una destinazione, ma non vedo alcun file. Dove sono? {#destination-no-files}

<!-- c_dest_tshooting.xml -->

I problemi comuni di configurazione della destinazione includono i seguenti problemi:

### Destinazione non configurata

* **[!UICONTROL UserID] Chiave errata:** la  [!UICONTROL UserID] chiave è la  [!UICONTROL MasterDPID] della destinazione e costituisce la base per i valori ID che verranno esclusi dai limiti. Anche se una chiave [!UICONTROL UserID] è selezionabile tramite l’elenco a discesa, non significa necessariamente che ci sono ID/caratteristiche/segmenti mappati a questo valore. Se il processo [!UICONTROL Outbound] (che viene eseguito dopo la creazione delle destinazioni) non individua utenti mappati a questa chiave [!UICONTROL UserID], non verrà generato alcun limite per i dati.
* **Nessuna in Origini dati file selezionata:** quando si sceglie un tipo di destinazione diverso da  [!UICONTROL S2S], viene visualizzata una sezione nella parte inferiore dello schermo contrassegnata  [!UICONTROL Configure Data Sources]. Quando questa sezione viene visualizzata per la prima volta, non viene selezionato alcun valore. Se si dimentica di fare clic sulla casella di controllo [!UICONTROL All First Party] o di selezionare singolarmente le origini dati dalla finestra [!UICONTROL Available Data Sources], non verrà visualizzato alcun limite per i dati.

### Formato non configurato

Quando selezioni un formato per i dati non delimitati, è meglio, se possibile, riutilizzare un formato esistente. L’utilizzo di un formato già collaudato garantisce la corretta generazione dei dati in uscita. Per visualizzare esattamente il formato di un formato esistente, fai clic sull&#39;opzione [!UICONTROL Formats] nella barra dei menu e cerca il formato per nome o per numero di ID. I formati o le macro errati utilizzati nei formati forniscono un output formattato in modo errato o impediranno l’output completo delle informazioni.

Per ulteriori informazioni sull&#39;impostazione dei formati e sull&#39;utilizzo delle macro, vedere [Macro in formato file](formats/file-formats.md#) e [Macro in formato HTTP](formats/web-formats.md).

### Server non configurato

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * Non inserire prefissi per i nomi host. Se ti viene assegnato un account [!DNL ftp://hello.com], inserisci semplicemente [!DNL hello.com] in questo campo.
   * **[!UICONTROL Port/Type Combination]**
      * Per un trasferimento [!DNL FTP], il tipo di trasferimento preferito è [!DNL SFTP].
      * Quando si seleziona il tipo [!DNL SFTP], la porta è quasi sempre 22.
      * Quando si seleziona il tipo [!DNL FTPs/TLS], la porta è quasi sempre 21.
      * Il tipo [!DNL FTPs/TLS] non è lo stesso di un normale [!DNL FTP] trasferimento. Non sono supportati trasferimenti regolari (non protetti) [!DNL FTP].
   * **[!UICONTROL Remote Path]**
      * Quando si sceglie un sottopercorso remoto, questo deve essere inserito senza barra verticale.
      * Se il file trasferito deve essere posizionato nella sottocartella [!DNL (root)/inbound], è sufficiente aggiungere [!DNL inbound] per il percorso remoto, non [!DNL /inbound].
      * Se invii i file con più directory lungo il percorso, immetti barre tra ciascuna directory. Se ti viene indicata la posizione di [!DNL /inbound/subdirectory1/subdirectory2], immetti [!DNL inbound/subdirectory1/subdirectory2] in questo campo.
      * Se il file deve essere inserito nella directory automaticamente indirizzata a dal server esterno, puoi lasciare vuoto questo spazio. Non inserire un punto ( . ), barra ( / ) o altro.

* **[!DNL S3]**
   * [!DNL S3] è il protocollo di trasferimento preferito (sopra  [!DNL FTP] o  [!DNL HTTP]).
      * **[!UICONTROL Bucket]**
         * Il nome del bucket deve essere elencato senza barre, prefissi, suffissi, ecc. Se ti viene assegnato l&#39;indirizzo [!DNL s3://your-bucket] devi semplicemente aggiungere [!DNL your-bucket] a questo campo.
      * **[!UICONTROL Directory]**
         * Lasciare vuoto questo campo a meno che non venga specificatamente specificata una sottodirectory in cui inserire i dati. Se ti viene assegnato l&#39;indirizzo [!DNL s3://your-bucket/your-subdirectory], immetti [!DNL your-bucket] nel campo [!UICONTROL Bucket] e [!DNL your-subdirectory] deve essere aggiunto al campo [!UICONTROL Directory] . Non aggiungere barre precedenti.
         * Se devi spostare più directory lungo il percorso, usa solo le barre come separatori. Pertanto, una posizione di [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] avrebbe [!DNL your-bucket] nel campo [!UICONTROL Bucket] e [!DNL your-subdirectory1/your-subdirectory2] inserito nel campo [!UICONTROL Directory].
      * **[!UICONTROL Access / Secret Keys]**
         * Quando [!DNL TechOps] crea un bucket e fornisce chiavi di accesso/segreto a un consulente, tali credenziali sono in genere `READ-ONLY` credenziali che devono essere consegnate al client. Queste credenziali non devono essere immesse nei campi [!UICONTROL Access / Secret Key], perché questo causerà un errore nel trasferimento (perché tali credenziali sono di sola lettura, non scrivibili). Nel caso in cui [!DNL TechOps] crei un bucket e fornisca le credenziali, il consulente deve anche richiedere una coppia di chiavi di Adobe - DA NON DARE AL CLIENT - che consenta la scrittura di file in questo bucket. Tale chiave deve essere aggiunta in questi campi.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * Immettere le informazioni sul prefisso per le voci [!DNL HTTP]. Se ti viene assegnato un account [!DNL https://superduper.com], immetti [!DNL https://superduper.com] in questo campo.
      * **[!UICONTROL URL Prefix]**
         * Quando aggiungi un prefisso [!DNL URL] , lascia disattivata la barra precedente. Un indirizzo di [!DNL https://hello.com/r/x/y/z] deve essere [!DNL https://hello.com] inserito nel campo [!UICONTROL Domain] e [!DNL r/x/y/z] inserito qui nel campo [!UICONTROL URL Prefix].
         * Se non è necessario un valore [!UICONTROL URL Prefix], lasciare vuoto questo valore.
      * **[!UICONTROL Authentication - SSH Key]**
         * Immetti il valore chiave `SSH PRIVATE` completo in questa casella, comprese intestazioni, piè di pagina e interruzioni di riga per garantire una crittografia accurata/archiviazione delle chiavi.

### Tempo insufficiente per la generazione in uscita

Il processo di definizione dei limiti viene eseguito due volte al giorno e più processi (outbounding, pubblicazione, push a posizioni esterne, ecc.) deve essere eseguito prima del push di un file alla destinazione finale. Una buona regola è che una destinazione deve essere completamente configurata almeno 24 ore prima di poter prevedere che i dati vengano inviati a una posizione esterna.

### Dimensioni di suddivisione file troppo grandi

Quando si estendono file alle destinazioni, è possibile dividere file in uscita di dimensioni maggiori in blocchi di file. Assicurati che i singoli blocchi di file non superino i 10 GB. Vedere anche [Nome file dati in uscita: Sintassi ed esempi](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html?lang=en).


## Come impostare le destinazioni per esportare ID Experience Cloud, ID cliente o ID Audience Manager in file di dati in uscita {#set-up-destinations-export}

Questa pagina mostra come impostare le destinazioni per l’esportazione di dati con chiave del tipo ID desiderato in [!UICONTROL Outbound Data Files].

<!-- set-up-destinations-mcid-aamid.xml -->

Le destinazioni consentono ai nostri clienti di attivare i loro dati su qualsiasi numero di canali digitali. Ad esempio, possono esportare i dati del pubblico in altre soluzioni [!DNL Adobe Experience Cloud] ([!DNL Target], [!DNL Campaign], ecc.). Oppure possono inviare dati a [!UICONTROL DSP]s, [!UICONTROL SSP]s o a qualsiasi piattaforma integrata con Audience Manager. Teniamo un elenco dei partner con cui lavoriamo sulla nostra [pagina Wiki Integrazioni](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>Per informazioni dettagliate sulla creazione delle destinazioni nell’interfaccia utente amministratore, consulta l’articolo [Creare o modificare le destinazioni aziendali](companies/admin-manage-company-destinations.md#create-edit-company-destinations) .

I clienti desiderano esportare diversi tipi di ID, a seconda della destinazione. Il grafico di configurazione seguente mostra le opzioni che devi selezionare per esportare le informazioni di profilo relative a diversi tipi di ID. Si consiglia inoltre di fare riferimento al [Indice degli ID in Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html?lang=en). Ci sono tre impostazioni importanti da considerare: [!UICONTROL User ID Key], [!UICONTROL Data Source Type] e [!UICONTROL Format]. Li descriviamo tutti nel dettaglio qui sotto.

* [!UICONTROL User ID Key]. In [!UICONTROL Admin UI], vai a **[!UICONTROL Companies]**. Cerca l’azienda del cliente e fai clic su di essa. Cerca la scheda **[!UICONTROL Destinations]** e premi **[!UICONTROL Add Destination]**. Nel flusso di lavoro **[!UICONTROL Add Destination]**, seleziona il [!UICONTROL User ID Key]. Gli [!UICONTROL User ID Key] filtrano gli ID in entrata dall’origine dati di destinazione e consentono solo il trasferimento degli ID.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]. Seleziona questa opzione quando crei una destinazione nell’interfaccia utente di Audience Manager. Prima di tutto, seleziona [!UICONTROL Inbound], quindi seleziona il tipo di ID desiderato. Le opzioni sono:

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]. Questa opzione determina il formato di file da esportare. Nel flusso di lavoro **[!UICONTROL Add Destination]**, in **[!UICONTROL Batch Data]**, seleziona il formato .

Per ispezionare un formato, vai su **[!UICONTROL Admin UI > Formats]** e cerca l&#39;elemento [!UICONTROL Data Row]. Questo elemento contiene una macro del formato di file, &lt;MCID> nell&#39;esempio seguente.

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> N. configurazione </th> 
   <th colname="col1" class="entry"> <p>Chiave utente </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo di origine dati </p> </th> 
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
   <td colname="col4"> <p>ID Experience Cloud </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID Experience Cloud </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>UUID Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID Experience Cloud </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>ID Experience Cloud </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID Audience Manager </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>UUID Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID Audience Manager </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>ID Experience Cloud </p> </td> 
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
   <td colname="col1"> <p>DPID (qualsiasi origine di dati a cui l'azienda ha accesso) </p> </td> 
   <td colname="col2"> <p>ID cliente </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>ID cliente (DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine di dati a cui l'azienda ha accesso) </p> </td> 
   <td colname="col2"> <p>ID cliente </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>ID Experience Cloud </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine di dati a cui l'azienda ha accesso) </p> </td> 
   <td colname="col2"> <p>ID cliente </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine di dati a cui l'azienda ha accesso) </p> </td> 
   <td colname="col2"> <p>ID Audience Manager </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>UUID Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine di dati a cui l'azienda ha accesso) </p> </td> 
   <td colname="col2"> <p>ID Audience Manager </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>ID Experience Cloud </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID (qualsiasi origine di dati a cui l'azienda ha accesso) </p> </td> 
   <td colname="col2"> <p>ID Audience Manager </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID Audience Manager </p> </td> 
  </tr> 
 </tbody> 
</table>

## Casi d&#39;uso

Supponiamo che tu utilizzi l’Audience Manager e [!DNL Campaign]. Per rendere i dati del cliente fruibili in [!DNL Campaign], devi esportare [!UICONTROL Experience Cloud IDs]. In questo caso devi utilizzare il numero di configurazione 3.
