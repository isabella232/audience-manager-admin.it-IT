---
description: Elenca le macro utilizzabili per creare file di dati basati su FTP. Alcune macro possono essere utilizzate per tutti i campi e le righe del file di dati. Altre macro sono specifiche solo per righe di intestazione e dati.
seo-description: Elenca le macro utilizzabili per creare file di dati basati su FTP. Alcune macro possono essere utilizzate per tutti i campi e le righe del file di dati. Altre macro sono specifiche solo per righe di intestazione e dati.
seo-title: Macro formato file
title: Macro formato file
uuid: f91c91b6-6581-4ed7-8d7f-f8532bd41df9
translation-type: tm+mt
source-git-commit: e1122a7f3d3e8c2d67616eb56cb186a4750ed29b

---


# Macro formato file {#file-format-macros}

Elenca le macro utilizzabili per creare file di dati [!DNL FTP]basati su. Alcune macro possono essere utilizzate per tutti i campi e le righe del file di dati. Altre macro sono specifiche solo per righe di intestazione e dati.

## Macro comuni {#common-macros}

Tali macro possono essere utilizzate in qualsiasi campo di formato. Ad esempio, vedere Esempi [di macro](../formats/file-format-examples.md)Formato file.

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
   <td colname="col2"> <p>Un carattere ASCII non stampabile. Indica l'inizio di una riga o di una sezione di contenuto. Può essere utilizzato anche per separare le colonne di dati in un file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p>ID provider dati di destinazione. </p> </td> 
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
   <td colname="col2"> <p>Alias per un ID ordine/destinazione. </p> <p>Il valore di questo alias è impostato nel campo ID account <span class="wintitle"> esterno </span> per una destinazione (nella sezione <span class="wintitle"> Impostazioni di base </span> ). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_MODE</code> </p> </td> 
   <td colname="col2"> <p>Indica il tipo di sincronizzazione. Accetta le seguenti variabili facoltative: </p> 
    <ul id="ul_87E8E3CE6565447A9810B5119298CC7B"> 
     <li id="li_66F4889FB84E40AC92F69F3FF6B0042C"> <code>full</code>: Sincronizzazione completa. </li> 
     <li id="li_BFE2C2D9A33A44FB9A840A7232ECCFFF"> <code>iter</code>: Sincronizzazione incrementale. </li> 
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
   <td colname="col2"> <p>Una marca temporale di 10 cifre, UTC e Unix. </p> <p>Può anche essere formattato come <code>YYYYMMDDhmmss</code> dopo le regole di formattazione data/timestamp Java. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Macro dei campi di intestazione {#header-field-macros}

Macro utilizzate solo nei campi di intestazione. Ad esempio, vedere Esempi [di macro](../formats/file-format-examples.md)Formato file.

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
   <td colname="col2"> <p>Utilizzata come separatore, questa macro inserisce una scheda tra i campi. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Macro di righe dati {#data-row-macros}

Macro utilizzate solo nelle righe di dati. Ad esempio, vedere Esempi [di macro](../formats/file-format-examples.md)Formato file.

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
   <td colname="col2"> <p>Inserisce una parentesi graffa chiusa }. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>COMMA</code> </p> </td> 
   <td colname="col2"> <p>Inserisce una virgola. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="term"> Identificatore Utente Univoco Partner Dati </span>. Restituisce l’ID assegnato a un visitatore utente/sito se l’ID è già stato sincronizzato con un ID dispositivo <span class="keyword"> Audience Manager </span> . </p> <p>Se il DPID è pari a 0, questa macro restituirà l’ID <span class="keyword"> Audience Manager </span> invece dell’ID per l’utente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID_LIST</code> </p> </td> 
   <td colname="col2"> <p>Restituisce un elenco che contiene più ID per un partner dati. Questa funzione è utile se si dispone di un’organizzazione di grandi dimensioni con più suddivisioni o altri gruppi organizzativi con cui è possibile condividere i dati. Questa macro restituisce un elenco degli ID per tali gruppi subordinati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPUUIDS</code> </p> </td> 
   <td colname="col2"> <p>L'output di questa macro mappa l'ID del provider di dati (DPID) con gli ID utente univoci correlati (DPUUID). Questa macro deve avere una stringa di formattazione per controllarne l'output. L'output di esempio sarà simile al seguente: </p> <p> <code>"dpids=dpid1,dpid2,...dpid n|maxMappings= n|format=json"</code> </p> <p>L'impostazione <code>maxMappings</code> determina il numero di mappature da restituire dalla macro. Quando <code>maxMappings=0</code>, questa macro restituisce tutti i mapping per ogni DPID specificato. I dati vengono ordinati per marca temporale (la prima più recente) e restituiscono prima i risultati con la marca temporale più grande. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>endif</code> </p> </td> 
   <td colname="col2"> <p>Obbligatorio quando si utilizzano le macro condizionale <code>if</code> e <code>SEGMENT_LIST</code> e <code>REMOVED_SEGMENT_LIST</code> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>if(SEGMENT_LIST &amp;&amp; REMOVED_SEGMENT_LIST)endif</code> </p> </td> 
   <td colname="col2"> <p>Questa combinazione di macro crea un'istruzione condizionale in cui sono elencati i segmenti a cui appartengono gli utenti <i>e da cui</i> sono stati rimossi. Restituisce una stringa vuota se entrambe le condizioni non sono soddisfatte o se non sono presenti dati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Experience Cloud </span> ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPEN_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>Inserisce una parentesi graffa aperta { carattere. </p> </td> 
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
   <td colname="col2"> <p>Restituisce <code>1</code> come valore statico e hardcoded. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID</code> </p> </td> 
   <td colname="col2"> <p>ID partner (PID). Il PID viene visualizzato nella <span class="wintitle"> scheda Profilo </span> nell'interfaccia utente di amministrazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Restituisce un elenco degli eventuali segmenti rimossi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Restituisce un elenco di segmenti in un elenco. Accetta le seguenti variabili facoltative: </p> 
    <ul id="ul_B111AA0D6C18445598A1444B8B7E9325"> 
     <li id="li_8603B40229624856AF1FBC434DB8F16A"> <code>segmentId</code>: ID legacy. Obsoleto. Utilizzate <code>sid</code> (solo in lettere minuscole). </li> 
     <li id="li_1EF40DDCA3C5447586904CF021D8F912"> <code>csegid</code>: ID legacy. Obsoleto. Utilizzate <code>sid</code> (solo in lettere minuscole). </li> 
     <li id="li_D85F0A5D16AE4DAFB55C17DBB35EA66E"> <code>sid</code>: ID segmento. </li> 
     <li id="li_9BE103EFD8384464B46FAC00422431DB"> <code>type</code>: Restituisce <code>5</code>, un valore statico e hardcoded che identifica i dati come dati del segmento. </li> 
     <li id="li_FE5049089F2944FA9DB9F9D546DBA167"> <code>alias</code>: Mapping del segmento. Obsoleto. Utilizzate <code>sid</code> (solo in lettere minuscole). </li> 
     <li id="li_DD778AA2D1DB4D409CF5026B5D9DBD27"> <code>lastUpdateTime</code>: Una marca temporale Unix che indica l’ultima volta che un segmento è stato realizzato. </li> 
    </ul> <p>Inserire queste variabili tra parentesi graffe dopo la macro. Ad esempio, questo codice separa i risultati con un carattere "|" pipe: <code>&lt;SEGMENT_LIST:{seg|&lt;seg.type&gt;,&lt;seg.sid&gt;}; separator="|"&gt;</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ATTRIBUTES</code> </p> </td> 
   <td colname="col2"> <p>Restituisce <code>1</code> come valore statico e hardcoded. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>Inserisce un separatore di tabulazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Restituisce un elenco di caratteristiche. Accetta i seguenti argomenti facoltativi: </p> 
    <ul id="ul_757DEB56E4F849768468F3C166B0D171"> 
     <li id="li_859E1F4F21D645519F150DC512B3EB1A"> <code>type</code>: Tipi di caratteristiche identificati da un ID numerico. Questa variabile restituisce: 
      <ul id="ul_C9839266783D42CCADAAC3FEA33BE4D7"> 
       <li id="li_6996A218E3F04EC3BC70032559DD87FC"> <code>10</code> che identifica una caratteristica DPM (offline, configurata da un processo in ingresso). </li> 
       <li id="li_831FF929BF50434C8804C13E5786DF79"> <code>3</code> che identifica una caratteristica basata su regole (in tempo reale, integrata attraverso il <span class="wintitle"> DCS </span>). </li> 
      </ul> </li> 
     <li id="li_E84D6BC80AEE4F10963C9882C4151ED4"> <code>traitId</code>: ID caratteristica. </li> 
     <li id="li_D30A849BA35248E6B9110FA3ADEFC332"> <code>lastRealized</code>: L'ultima volta che il tratto è stato realizzato. Timestamp Unix. </li> 
    </ul> <p>Inserire queste variabili tra parentesi graffe dopo la macro. Ad esempio, questo codice separa i risultati con un carattere "|" pipe: <code>TRAIT_LIST{type|traitId};separator="|"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> ID </span> utente di Audience Manager. </p> </td> 
  </tr> 
 </tbody> 
</table>