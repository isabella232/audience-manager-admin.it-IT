---
description: Elenca le macro utilizzabili per creare file di dati basati su FTP. Alcune macro possono essere utilizzate per tutti i campi e le righe di file dati. Altre macro sono specifiche dell'intestazione e delle righe dati.
seo-description: Elenca le macro utilizzabili per creare file di dati basati su FTP. Alcune macro possono essere utilizzate per tutti i campi e le righe di file dati. Altre macro sono specifiche dell'intestazione e delle righe dati.
seo-title: Macro formato file
title: Macro formato file
uuid: f 91 c 91 b 6-6581-4 ed 7-8 d 7 f-f 8532 bd 41 df 9
translation-type: tm+mt
source-git-commit: e1122a7f3d3e8c2d67616eb56cb186a4750ed29b

---


# Macro formato file {#file-format-macros}

Elenca le macro utilizzabili per creare [!DNL FTP]file di dati basati su file. Alcune macro possono essere utilizzate per tutti i campi e le righe di file dati. Altre macro sono specifiche dell'intestazione e delle righe dati.

## Macro comuni {#common-macros}

Queste macro possono essere utilizzate in qualsiasi campo di formato. Per esempi, consultate [Esempi di macro di macro](../formats/file-format-examples.md).

<table id="table_A3309E175ABF4651BD11CE3632B3C553"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>ASCII_ SOH</code> </p> </td> 
   <td colname="col2"> <p>Un carattere ASCII non stampabile. Indica l'inizio di una riga o di una sezione di contenuto. Può essere utilizzato anche per separare le colonne di dati in un file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p>ID provider dati di Target. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_ DPID</code> </p> </td> 
   <td colname="col2"> <p>ID provider dati chiave ID utente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ ID</code> </p> </td> 
   <td colname="col2"> <p>ID ordine/destinazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PIDALIAS</code> </p> </td> 
   <td colname="col2"> <p>Alias per un ID ordine/di destinazione. </p> <p>Il valore per questo alias viene impostato <span class="wintitle"> nel campo ID </span> account esterno per una destinazione (nella sezione Impostazioni <span class="wintitle"></span> di base). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_ MODE</code> </p> </td> 
   <td colname="col2"> <p>Indica il tipo di sincronizzazione. Accetta le seguenti variabili facoltative: </p> 
    <ul id="ul_87E8E3CE6565447A9810B5119298CC7B"> 
     <li id="li_66F4889FB84E40AC92F69F3FF6B0042C"> <code>full</code>: Sincronizzazione completa. </li> 
     <li id="li_BFE2C2D9A33A44FB9A840A7232ECCFFF"> <code>iter</code>: Sincronizzazione incrementale. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_ TYPE</code> </p> </td> 
   <td colname="col2"> <p>Indica il metodo di trasferimento dati. Accetta le seguenti variabili facoltative: </p> 
    <ul id="ul_13BE35BBBF7C4C67AEFC514C5D192902"> 
     <li id="li_195FE9B4C5494600BD17D7172A8FB630"> <code>ftp</code> </li> 
     <li id="li_751AD59C4C934D66BC530D9806B500AF"> <code>http</code> </li> 
     <li id="li_4638AF7D1FB54E2C890045048B85309C"> <code>s3</code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIMESTAMP</code> </p> </td> 
   <td colname="col2"> <p>Un timestamp di 10 cifre, UTC, Unix. </p> <p>Può anche essere formattata come <code>yyyymmddhhmss</code> in seguito alle regole di formattazione data/ora di Java. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Macro dei campi intestazione {#header-field-macros}

Macro utilizzate solo nei campi dell'intestazione. Per esempi, consultate [Esempi di macro di macro](../formats/file-format-examples.md).

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
   <td colname="col2"> <p>Utilizzato come separatore, questa macro inserisce una scheda tra i campi. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Macro riga dati {#data-row-macros}

Macro utilizzate solo nelle righe dati. Per esempi, consultate [Esempi di macro di macro](../formats/file-format-examples.md).

<table id="table_E378F94A3907407AA8110C8EE6C10909"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>CLOSE_ CURLY_ BRACKET</code> </p> </td> 
   <td colname="col2"> <p>Inserisce un carattere parentesi graffa chiusa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>VIRGOLA</code> </p> </td> 
   <td colname="col2"> <p>Inserisce una virgola. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_ UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="term"> Data Partner Unique User Identifier </span>. Restituisce l'ID assegnato a un visitatore utente/sito se tale ID è già stato sincronizzato con un <span class="keyword"> ID </span> dispositivo Audience Manager. </p> <p>Se il DPID è 0, questa macro restituirà l'ID <span class="keyword"> Audience Manager </span> invece dell'ID dell'utente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_ UUID_ LIST</code> </p> </td> 
   <td colname="col2"> <p>Restituisce un elenco contenente più ID per un partner dati. Questa funzione è utile se si dispone di un'organizzazione di grandi dimensioni con più suddivisioni o altri gruppi organizzativi con cui condividere i dati. Questa macro restituisce un elenco degli ID per i gruppi subordinate. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPUUIDS</code> </p> </td> 
   <td colname="col2"> <p>L'output di questa macro mappa l'ID del provider di dati (DPID) su ID utente univoci correlati (DPUUID). Questa macro deve disporre di una stringa di formattazione per controllare l'output. L'output di esempio sarà simile a quello seguente: </p> <p> <code>" dpids = dpid 1, dpid 2,… dpid n | maxmappings = n | format = json "</code> </p> <p>L'impostazione <code>maxmappings</code> determina quante mappature desiderate che la macro restituisca. Quando <code>maxmappings = 0</code>, questa macro restituisce tutte le mappature per ogni DPID specificato. I dati sono ordinati per marca temporale (prima più recente) e restituiscono prima i risultati con la marca temporale più elevata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>endif</code> </p> </td> 
   <td colname="col2"> <p>Obbligatorio quando si utilizza la condizionale <code>if</code> and the <code>SEGMENT_ LIST</code> and <code>REMOVED_ SEGMENT_ LIST</code> macro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>if (SEGMENT_ LIST &amp; &amp; REMOVED_ SEGMENT_ LIST) endif</code> </p> </td> 
   <td colname="col2"> <p>Questa combinazione di macro crea un'istruzione condizionale in cui sono elencati i segmenti a cui <i>appartengono e</i> sono stati rimossi. Restituisce una stringa vuota se entrambe le condizioni non sono soddisfatte o se non sono presenti dati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Experience Cloud </span> ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPEN_ CURLY_ BRACKET</code> </p> </td> 
   <td colname="col2"> <p>Inserisce una parentesi graffa aperta {carattere. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPT_ OUT</code> </p> </td> 
   <td colname="col2"> <p>Obsoleto. Non utilizzate. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ ATTRIBUTE_ TYPE</code> </p> </td> 
   <td colname="col2"> <p>Obsoleto. Non utilizzate. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ ATTRIBUTE_ VALUE</code> </p> </td> 
   <td colname="col2"> <p>Restituisce <code>1</code> come valore statico e codificato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID</code> </p> </td> 
   <td colname="col2"> <p>ID partner (PID). Il PID viene visualizzato sotto la scheda <span class="wintitle"> Profilo </span> nell'interfaccia utente di amministrazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_ SEGMENT_ LIST</code> </p> </td> 
   <td colname="col2"> <p>Restituisce un elenco di segmenti eventualmente rimossi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_ LIST</code> </p> </td> 
   <td colname="col2"> <p>Restituisce un elenco di segmenti in un elenco. Accetta le seguenti variabili facoltative: </p> 
    <ul id="ul_B111AA0D6C18445598A1444B8B7E9325"> 
     <li id="li_8603B40229624856AF1FBC434DB8F16A"> <code>Segmentid</code>: ID legacy. Obsoleto. Usa <code>sid</code> (solo lettere minuscole). </li> 
     <li id="li_1EF40DDCA3C5447586904CF021D8F912"> <code>csegid</code>: ID legacy. Obsoleto. Usa <code>sid</code> (solo lettere minuscole). </li> 
     <li id="li_D85F0A5D16AE4DAFB55C17DBB35EA66E"> <code>sid</code>: ID segmento. </li> 
     <li id="li_9BE103EFD8384464B46FAC00422431DB"> <code>type</code>: Restituisce <code>5</code>, un valore statico e hardcoded che identifica i dati come dati del segmento. </li> 
     <li id="li_FE5049089F2944FA9DB9F9D546DBA167"> <code>alias</code>: Mappatura del segmento. Obsoleto. Usa <code>sid</code> (solo lettere minuscole). </li> 
     <li id="li_DD778AA2D1DB4D409CF5026B5D9DBD27"> <code>Lastupdatetime</code>: Una marca temporale Unix che indica l'ultima volta che è stato realizzato un segmento. </li> 
    </ul> <p>Inserire queste variabili tra parentesi graffe dopo la macro. Ad esempio, questo codice separa i risultati con una barra verticale|" character: <code>&lt; SEGMENT_ LIST: {seg|&lt; seg. type &gt;, &lt; seg. sid &gt;}; separator = "|" &gt;</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ ATTRIBUTES</code> </p> </td> 
   <td colname="col2"> <p>Restituisce <code>1</code> come valore statico e codificato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>Inserisce un separatore di tabulazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_ LIST</code> </p> </td> 
   <td colname="col2"> <p>Restituisce un elenco di caratteristiche. Accetta i seguenti argomenti facoltativi: </p> 
    <ul id="ul_757DEB56E4F849768468F3C166B0D171"> 
     <li id="li_859E1F4F21D645519F150DC512B3EB1A"> <code>type</code>: Tipi di caratteristiche identificati da un ID numerico. Questa variabile restituisce: 
      <ul id="ul_C9839266783D42CCADAAC3FEA33BE4D7"> 
       <li id="li_6996A218E3F04EC3BC70032559DD87FC"> <code>10</code> che identifica una caratteristica DPM (offline, registrata da un processo in entrata). </li> 
       <li id="li_831FF929BF50434C8804C13E5786DF79"> <code>3</code> che identifica una caratteristica basata su regole (tempo reale; caricati nel <span class="wintitle"> DCS </span>. </li> 
      </ul> </li> 
     <li id="li_E84D6BC80AEE4F10963C9882C4151ED4"> <code>Traitid</code>: ID caratteristica. </li> 
     <li id="li_D30A849BA35248E6B9110FA3ADEFC332"> <code>Lastrealized</code>: L'ultima volta che è stata creata la caratteristica. Marca temporale Unix. </li> 
    </ul> <p>Inserire queste variabili tra parentesi graffe dopo la macro. Ad esempio, questo codice separa i risultati con una barra verticale. |" character: <code>TRAIT_ LIST {type | traitid}; separator = "|" "</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> ID </span> utente Audience Manager. </p> </td> 
  </tr> 
 </tbody> 
</table>