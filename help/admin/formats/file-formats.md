---
description: Elenca le macro utilizzabili per creare file di dati basati su FTP. Alcune macro possono essere utilizzate per tutti i campi e le righe dei file di dati. Altre macro sono specifiche solo per le righe di intestazione e di dati.
seo-description: Lists the macros you can use to create FTP-based data files. Some macros can be used for all data file fields and rows. Other macros are specific to header and data rows only.
seo-title: File Format Macros
title: Macro per formati file
uuid: f91c91b6-6581-4ed7-8d7f-f8532bd41df9
exl-id: e686bc33-da3e-49a9-8c71-2bc6ca399bfb
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 1%

---

# Macro per formati file {#file-format-macros}

Elenca le macro che è possibile creare [!DNL FTP]file di dati basati su. Alcune macro possono essere utilizzate per tutti i campi e le righe dei file di dati. Altre macro sono specifiche solo per le righe di intestazione e di dati.

## Macro comuni {#common-macros}

Queste macro possono essere utilizzate in qualsiasi campo di formato. Per esempi, consulta [Esempi di macro per formati file](../formats/file-format-examples.md).

<table id="table_A3309E175ABF4651BD11CE3632B3C553"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>ASCII_SOH</code> </p> </td> 
   <td colname="col2"> <p>Carattere ASCII non stampabile. Indica l’inizio di una riga o di una sezione di contenuto. Può anche essere utilizzato per separare le colonne di dati in un file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p>ID del provider di dati di destinazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_DPID</code> </p> </td> 
   <td colname="col2"> <p>ID utente ID provider dati chiave. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ID</code> </p> </td> 
   <td colname="col2"> <p>ID ordine/destinazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PIDALIAS</code> </p> </td> 
   <td colname="col2"> <p>Alias per un ID ordine/destinazione. </p> <p>Il valore di questo alias è impostato in <span class="wintitle"> ID account esterno </span> per una destinazione (nel campo <span class="wintitle"> Impostazioni di base </span> sezione ). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_MODE</code> </p> </td> 
   <td colname="col2"> <p>Indica il tipo di sincronizzazione. Accetta le seguenti variabili facoltative: </p> 
    <ul id="ul_87E8E3CE6565447A9810B5119298CC7B"> 
     <li id="li_66F4889FB84E40AC92F69F3FF6B0042C"> <code>full</code>: sincronizzazione completa. </li> 
     <li id="li_BFE2C2D9A33A44FB9A840A7232ECCFFF"> <code>iter</code>: sincronizzazione incrementale. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_TYPE</code> </p> </td> 
   <td colname="col2"> <p>Indica il metodo di trasferimento dei dati. Accetta le seguenti variabili facoltative: </p> 
    <ul id="ul_13BE35BBBF7C4C67AEFC514C5D192902"> 
     <li id="li_195FE9B4C5494600BD17D7172A8FB630"> <code>ftp</code> </li> 
     <li id="li_751AD59C4C934D66BC530D9806B500AF"> <code>http</code> </li> 
     <li id="li_4638AF7D1FB54E2C890045048B85309C"> <code>s3</code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIMESTAMP</code> </p> </td> 
   <td colname="col2"> <p>Timestamp a 10 cifre, UTC, Unix. </p> <p>Può anche essere formattato come <code>YYYYMMDDhhmmss</code> seguenti regole di formattazione Java per data/timestamp. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Macro per campi intestazione {#header-field-macros}

Macro utilizzate solo nei campi intestazione. Per esempi, consulta [Esempi di macro per formati file](../formats/file-format-examples.md).

<table id="table_1A8BD1750F4940B3A34E3F80371A447A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>Utilizzata come separatore, questa macro inserisce una tabulazione tra i campi. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Macro righe dati {#data-row-macros}

Macro utilizzate solo nelle righe di dati. Per esempi, consulta [Esempi di macro per formati file](../formats/file-format-examples.md).

<table id="table_E378F94A3907407AA8110C8EE6C10909"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>CLOSE_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>Inserisce una parentesi graffa chiusa <code>}</code> carattere. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>COMMA</code> </p> </td> 
   <td colname="col2"> <p>Inserisce una virgola. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="term"> Identificatore utente univoco del partner dati </span>. Restituisce l'ID assegnato a un utente/visitatore del sito se tale ID è già stato sincronizzato con un <span class="keyword"> Audience Manager </span> ID dispositivo. </p> <p>Se il DPID è 0, questa macro restituirà il valore <span class="keyword"> Audience Manager </span> ID invece dell’ID dell’utente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID_LIST</code> </p> </td> 
   <td colname="col2"> <p>Restituisce un elenco che contiene più ID per un partner dati. Questa funzione è utile se hai un’organizzazione di grandi dimensioni con più suddivisioni o altri gruppi organizzativi con cui puoi condividere i dati. Questa macro restituisce un elenco degli ID per tali gruppi subordinati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPUUIDS</code> </p> </td> 
   <td colname="col2"> <p>L'output di questa macro mappa l'ID del provider di dati (DPID) agli ID utente univoci correlati (DPUUID). Per controllare l'output di questa macro è necessario disporre di una stringa di formattazione. L’output di esempio sarà simile al seguente: </p> <p> <code>"dpids=dpid1,dpid2,...dpid n|maxMappings= n|format=json"</code> </p> <p>Il <code>maxMappings</code> l'impostazione determina il numero di mappature da restituire con la macro. Quando <code>maxMappings=0</code>, questa macro restituisce tutte le mappature per ogni DPID specificato. I dati sono ordinati per marca temporale (la prima più recente) e restituisce i risultati con la prima marca temporale più grande. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>endif</code> </p> </td> 
   <td colname="col2"> <p>Obbligatorio quando si utilizza il condizionale <code>if</code> e <code>SEGMENT_LIST</code> e <code>REMOVED_SEGMENT_LIST</code> macro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>if(SEGMENT_LIST &amp;&amp; REMOVED_SEGMENT_LIST)endif</code> </p> </td> 
   <td colname="col2"> <p>Questa combinazione di macro crea un'istruzione condizionale che elenca i segmenti a cui appartengono gli utenti <i>e</i> sono stati rimossi da. Restituisce una stringa vuota se entrambe le condizioni non sono soddisfatte o se non sono presenti dati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Experience Cloud ID.</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPEN_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>Inserisce una parentesi graffa <code>{</code> carattere. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPT_OUT</code> </p> </td> 
   <td colname="col2"> <p>Obsoleto. Non utilizzare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_TYPE</code> </p> </td> 
   <td colname="col2"> <p>Obsoleto. Non utilizzare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_VALUE</code> </p> </td> 
   <td colname="col2"> <p>Restituisce <code>1</code> come valore statico di codifica fissa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID</code> </p> </td> 
   <td colname="col2"> <p>ID partner (PID). Il PID viene visualizzato sotto <span class="wintitle"> Profilo </span> nell’interfaccia utente di amministrazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Restituisce un elenco degli eventuali segmenti rimossi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Restituisce un elenco di segmenti in un elenco. Accetta le seguenti variabili facoltative: </p> 
    <ul id="ul_B111AA0D6C18445598A1444B8B7E9325"> 
     <li id="li_8603B40229624856AF1FBC434DB8F16A"> <code>segmentId</code>: ID legacy. Obsoleto. Utilizzare <code>sid</code> (solo lettere minuscole). </li> 
     <li id="li_1EF40DDCA3C5447586904CF021D8F912"> <code>csegid</code>: ID legacy. Obsoleto. Utilizzare <code>sid</code> (solo lettere minuscole). </li> 
     <li id="li_D85F0A5D16AE4DAFB55C17DBB35EA66E"> <code>sid</code>: ID segmento. </li> 
     <li id="li_9BE103EFD8384464B46FAC00422431DB"> <code>type</code>: Restituisce <code>5</code>: valore statico e di codifica fissa che identifica i dati come dati del segmento. </li> 
     <li id="li_FE5049089F2944FA9DB9F9D546DBA167"> <code>alias</code>: mappatura del segmento. Obsoleto. Utilizzare <code>sid</code> (solo lettere minuscole). </li> 
     <li id="li_DD778AA2D1DB4D409CF5026B5D9DBD27"> <code>lastUpdateTime</code>: marca temporale Unix che indica l’ultima volta che un segmento è stato realizzato. </li> 
    </ul> <p>Inserire queste variabili tra parentesi graffe dopo la macro. Ad esempio, questo codice separa i risultati con una barra "|": <code>&lt;SEGMENT_LIST:{seg|&lt;seg.type&gt;,&lt;seg.sid&gt;}; separator="|"&gt;</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ATTRIBUTES</code> </p> </td> 
   <td colname="col2"> <p>Restituisce <code>1</code> come valore statico di codifica fissa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>Inserisce un separatore di tabulazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Restituisce un elenco di caratteristiche. Accetta i seguenti argomenti facoltativi: </p> 
    <ul id="ul_757DEB56E4F849768468F3C166B0D171"> 
     <li id="li_859E1F4F21D645519F150DC512B3EB1A"> <code>type</code>: tipi di caratteristiche identificati da un ID numerico. Questa variabile restituisce: 
      <ul id="ul_C9839266783D42CCADAAC3FEA33BE4D7"> 
       <li id="li_6996A218E3F04EC3BC70032559DD87FC"> <code>10</code> che identifica una caratteristica di DPM (offline, onboarding da un processo in entrata). </li> 
       <li id="li_831FF929BF50434C8804C13E5786DF79"> <code>3</code> che identifica una caratteristica basata su regole (in tempo reale, onboarding tramite <span class="wintitle"> DCS </span>). </li> 
      </ul> </li> 
     <li id="li_E84D6BC80AEE4F10963C9882C4151ED4"> <code>traitId</code>: ID caratteristica. </li> 
     <li id="li_D30A849BA35248E6B9110FA3ADEFC332"> <code>lastRealized</code>: l’ultima volta che la caratteristica è stata realizzata. Timestamp Unix. </li> 
    </ul> <p>Inserire queste variabili tra parentesi graffe dopo la macro. Ad esempio, questo codice separa i risultati con una barra "|": <code>TRAIT_LIST{type|traitId};separator="|"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Audience Manager </span> ID utente. </p> </td> 
  </tr> 
 </tbody> 
</table>
