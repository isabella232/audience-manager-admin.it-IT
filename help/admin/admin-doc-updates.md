---
description: Tutti gli aggiornamenti (informazioni aggiunte, eliminate e corrette) della Guida per l’amministrazione di Audience Manager, ordinati per data.
seo-description: Tutti gli aggiornamenti (informazioni aggiunte, eliminate e corrette) della Guida per l’amministrazione di Audience Manager, ordinati per data.
seo-title: Aggiornamenti alla documentazione
title: Aggiornamenti alla documentazione
uuid: 1c02dff5-8e3f-42bf-a50c-03b75e121ac7
translation-type: tm+mt
source-git-commit: e60aa0ac341d74454bfe00a4f56add3a9f9e281b
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 100%

---


# Aggiornamenti alla documentazione {#documentation-updates}

Tutti gli aggiornamenti (informazioni aggiunte, eliminate e corrette) della Guida per l’amministrazione di Audience Manager, ordinati per data.

Per informazioni sulle versioni con nuove funzioni, correzioni di bug e miglioramenti, consulta le [note sulla versione di Experience Cloud](https://marketing.adobe.com/resources/help/it_IT/whatsnew/). Per gli annunci precedenti relativi a Experience Cloud, vedi le [note sulle versioni precedenti](https://marketing.adobe.com/resources/help/it_IT/whatsnew/c_legacy_releases.html). Per [!DNL Audience Manager documentation changes, see] [Aggiornamenti alla documentazione](https://docs.adobe.com/content/help/it-IT/audience-manager/user-guide/documentation-updates/docs-2019.html).

## Aggiornamenti alla documentazione di AAM 2019 {#aam-2019-docs-updates}


| Argomento | Descrizione |
---------|----------|
| Macro per il formato HTTP | Sono stati aggiunti una nuova macro, `REGION_ID_LIST`, e tre nuovi campi per la macro `USER_LIST`: `sda`, `sda` e `sda`. |
| Macro per il formato HTTP | Sono state aggiunte due nuove macro: `ECID` e `MCID`. |


## Aggiornamenti alla documentazione di AAM 2018 {#aam-2018-docs-updates}

<!-- c_doc_updates.xml -->

<table id="table_AECF59E131F84E7791A5A421BFB203FA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Argomento </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/create-ftp-server.md#task_BF1DD0E5ECA64AEC87EACABFCAEA2C6D"> Creare o modificare un server FTP</a> </p> </td> 
   <td colname="col2"> <p>Sono state aggiunte ulteriori informazioni sull’autenticazione tramite chiave SSH per i server SFTP (passaggio 5). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-destination-troubleshooting.md#set-up-destinations-export"> Impostare le destinazioni per esportare da Experience Cloud...</a> </p> </td> 
   <td colname="col2"> <p>In questa pagina viene illustrato come impostare le destinazioni per l’esportazione di dati con chiave del tipo ID desiderato in file di dati in uscita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/admin-authorize-s3-cross-bucket.md#task_20B12994C5484A9D8CC40DF6F456CBE7"> Procedura: autorizzare l’accesso multiaccount al bucket Amazon S3 per le destinazioni batch</a> </p> </td> 
   <td colname="col2"> <p>Se preferisci non condividere le chiavi di accesso e le chiavi segrete di Amazon S3, puoi utilizzare le autorizzazioni multiaccount per il bucket Amazon S3 per la consegna di file di dati in uscita. Questo documento mostra come impostare questa procedura alternativa nell’interfaccia di amministrazione di Audience Manager. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Aggiornamenti alla documentazione di AAM 2017 {#aam-2017-docs-updates}

<table id="table_81D2DA9293A9417085C630D00A7C96E1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Argomento </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE"> Macro per il formato HTTP</a> </td> 
   <td colname="col2">La macro <code>segmentId</code> è stata sostituita con <code>legacySegmentId</code> ed è stata aggiunta la macro <code>newSegmentId</code>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-company-limits.md#task_3004C10CB9A9430A8D25E25BB830B5D6"> Gestire i limiti aziendali</a> </td> 
   <td colname="col2"> Nella documentazione sui limiti sono stati aggiunti il numero massimo di cartelle e la profondità della struttura delle caratteristiche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="formats/enable-outbound-seq.md#concept_526744C9433F40BF8269E18245B2F0BD"> Abilitare i trasferimenti di file di sequenza Hadoop per i file in uscita</a> </td> 
   <td colname="col2"> Scopri come consentire ai clienti di inviare file SEQ in uscita all’istanza Hadoop. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967"> Gestire i contenitori</a>  </td> 
   <td colname="col2"> È stata aggiunta una breve istruzione per la creazione dei contenitori. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-manage-company-destinations.md#create-edit-company-destinations"> Creare o modificare le destinazioni aziendali</a> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_527E0E75C03846B0AB39EEE544904BE2"> 
      <li id="li_FC276B34158D44E3A5450C6C8BAF3184">Sono state aggiunte istruzioni sul bilanciamento dell’uso delle sincronizzazioni complete e incrementali. </li> 
      <li id="li_3975DA78DE9E441D8F8CB80F752DD7B7">Il provisioning di <span class="keyword"> Adobe Media Optimizer</span> come destinazione di <span class="keyword"> Audience Manager</span> viene eseguito in <span class="keyword"> Adobe Media Optimizer</span>. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> Gestire le destinazioni aziendali</a> </p> </td> 
   <td colname="col2"> <p>Revisioni minori. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-amo-sync.md#concept_2B5537233DAA4860B3503B344F937D83"> Sincronizzazione ID con Media Optimizer</a> </p> </td> 
   <td colname="col2"> <p>Nuova documentazione che descrive la casella di controllo di sincronizzazione Adobe Media Optimizer in ciascun contenitore aziendale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-device-graph-options.md#concept_563615F1018340C683E0EE075F8F639D"> Opzioni di Device Graph per le società</a> </p> </td> 
   <td colname="col2"> <p>Nuova documentazione che descrive come configurare le opzioni di Device Graph. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-oauth2/aam-admin-api-requirements.md#concept_A7FAC9443CF34974A873E6B787616421"> Raccomandazioni e requisiti per l’utilizzo delle API</a> </p> </td> 
   <td colname="col2"> <p>Nuova documentazione che descrive alcuni requisiti e raccomandazioni utili da trasmettere ai clienti. Queste informazioni sono duplicate nella documentazione pubblica con lo stesso titolo e con modifiche per un pubblico di lettori diverso. Vedi <a href="https://docs.adobe.com/content/help/it-IT/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.translate.html#api-requirements-recommendations" format="https" scope="external">Raccomandazioni e requisiti per l’utilizzo delle API</a> nella documentazione pubblica. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Aggiornamenti alla documentazione di AAM 2016 {#aam-2016-docs-updates}

<table id="table_E9D9810EA8244B58A4F27D56CFE521FD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Argomento </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="admin-servers/create-ftp-server.md#task_BF1DD0E5ECA64AEC87EACABFCAEA2C6D"> Creare o modificare un server FTP</a> </td> 
   <td colname="col2">È stato aggiunto l’IP del protocollo FTP <b>52.44.29.204</b> in uscita. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> Gestire le destinazioni aziendali</a> </p> </td> 
   <td colname="col2"> <p>Revisioni minori. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/create-http-server.md#task_5BF59581868E4144B965D644D36BEACD"> Creare o modificare un server HTTP</a> </p> </td> 
   <td colname="col2"> <p>È stata aggiunta la <b>firma HTTP</b> alla procedura guidata per la creazione della configurazione del server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-beta-environment.md#concept_4AA12E66F49A452C8BA4E91AA28060AA"> Ambiente beta</a> </p> </td> 
   <td colname="col2"> <p>Sono stati aggiornati gli URL e i nomi host nell’ambiente beta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/outbound-active-user-filter.md#task_F5CF8BDDA5DB4D23837B59CADF7A623B"> Filtrare i dati in uscita solo per gli utenti attivi</a> </p> </td> 
   <td colname="col2"> <p>Istruzioni per la generazione di un file di sincronizzazione completo che includa solo gli utenti attivi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE"> Macro per il formato HTTP</a> </p> </td> 
   <td colname="col2" morerows="1"> <p>Nuova documentazione che contiene l’elenco delle macro HTTP con esempi di casi comuni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> Esempi di macro per il formato HTTP</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Aggiornamenti alla documentazione di AAM 2015 {#aam-2015-docs-updates}

<table id="table_90F524BAAED44A45A1F6BF8BBA9F26F9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Data e argomento </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Dicembre 2015 </p> <p><a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> Formati</a> </p> </td> 
   <td colname="col2"> <p>La sezione sulle macro è stata rivista e sono stati aggiunti degli esempi. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Aggiornamenti alla documentazione di AAM 2014 {#aam-2014-docs-updates}

<table id="table_FA9962E19248418BA73D5A794A378C9D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Data e argomento </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>12 novembre 2014 </p> <p> <a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> Formati</a> </p> </td> 
   <td colname="col2"> <p>Sono state aggiunte informazioni sulla macro &lt;MCID&gt;. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>23 ottobre 2014 </p> <p><a href="formats/admin-create-format.md#task_1A51FC9189DB439FB218D91F3875FD67"> Creare o modificare un formato</a> </p> </td> 
   <td colname="col2"> <p>Sono state aggiunte informazioni sull’opzione <span class="wintitle"> .info Receipt</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>23 ottobre 2014 </p> <p><a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> Formati</a> </p> </td> 
   <td colname="col2"> <p>Nuova pagina. Questa pagina è ancora in fase di preparazione e verrà aggiornata nei prossimi giorni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>22 ottobre 2014 </p> <p><a href="admin-destination-troubleshooting.md#"> Risoluzione dei problemi di impostazione della destinazione</a> </p> </td> 
   <td colname="col2"> <p>Nuovo argomento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>21 ottobre 2014 </p> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> Gestire le destinazioni aziendali</a> </p> </td> 
   <td colname="col2"> <p>È stato rielaborato l’intero argomento. Sono state aggiunte ulteriori informazioni e impostazioni aggiuntive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>25 settembre 2014 </p> <p><a href="companies/admin-manage-company-profiles.md"> Creare una società</a> </p> </td> 
   <td colname="col2"> <p>Sono state aggiunte ulteriori informazioni alle sezioni sui <span class="wintitle"> cicli di vita</span> e i <span class="wintitle"> tipi di account</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>25 settembre 2014 </p> <p><a href="companies/admin-manage-company-profiles.md#edit-company-profile"> Modificare un profilo società</a> </p> </td> 
   <td colname="col2"> <p>Sono state aggiunte ulteriori informazioni alle sezioni sui <span class="wintitle"> cicli di vita</span> e i <span class="wintitle"> tipi di account</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>