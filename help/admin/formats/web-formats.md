---
description: Elenca le macro utilizzabili per creare file di dati HTTP. HTTP invia dati in un formato JSON.
seo-description: Elenca le macro utilizzabili per creare file di dati HTTP. HTTP invia dati in un formato JSON.
seo-title: Macro di formato HTTP
title: Macro di formato HTTP
uuid: 91021 f 60-75 d 0-4 b 1 d -86 ca -91 c 9 dadafac 1
translation-type: tm+mt
source-git-commit: 1a547e421346a6bf281e2b3ff3a0bcb5cf1d78df

---


# Macro di formato HTTP {#http-format-macros}

Elenca le macro utilizzabili per creare [!DNL HTTP] file di dati. [!DNL HTTP] invia dati in un [!DNL JSON] formato.

Consultate Esempi di macro [HTTP per](../formats/web-format-examples.md) un elenco ed esempi di combinazioni di macro comunemente utilizzate.

<table id="table_72A72EA63C3643FB84B47A76CD2CC1CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Tipo metodo </th> 
   <th colname="col3" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>AAM_ UUID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p> <span class="keyword"> ID Audience Manager </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_ UUID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>User Partner Unique User ID. Questa macro restituisce l'ID assegnato a un utente se il relativo ID è già stato sincronizzato con un <span class="keyword"> ID </span> dispositivo Audience Manager. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>ID provider dati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ECID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>ID provider dati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>GENERATION_ TIME</code> </p> </td> 
   <td colname="col2"> <p> <code>GET, POST</code> </p> </td> 
   <td colname="col3"> <p>Marca temporale Unix UTC. Un timestamp interno rappresenta l'ora in cui AAM è stato notificato per pubblicare la destinazione <span class="wintitle"> S 2 S </span> ai nostri partner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>IP</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Indirizzo IP dell'utente. </p> </td> 
  </tr>
    <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Experience Cloud ID. (MCID sta per Marketing Cloud, che è il nome legacy di Experience Cloud) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>NUM_ REMOVED_ SEGMENTS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Il numero (numero intero) dei segmenti a cui l'utente non appartiene più. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>NUM_ SEGMENTS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Numero di segmenti a cui appartiene un utente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ ID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET, POST</code> </p> </td> 
   <td colname="col3"> <p>Ordine o ID di destinazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID_ ALIAS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET, POST</code> </p> </td> 
   <td colname="col3"> <p>Alias per l'ID partner. Noto anche come ID account esterno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>RANDOM</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Genera un numero casuale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REGION_ ID_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>L'area DCS <a href="https://docs.adobe.com/help/en/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-regions.html"> Audience Manager </a> in cui è stata creata l'attività.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_ SEGMENT_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Restituisce un elenco di ID segmento, se disponibili, che un utente non qualifica più. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_ SEGMENTS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Un elenco di segmenti non più qualificabili da un utente. Puoi anche restituire campi segmenti specifici che includono: </p> <p> 
     <ul id="ul_29B83093A7624A908F0C06F2A248981A"> 
      <li id="li_57A60A54F5D44E38ACB4E2648095F246"> <code>Traitaliani</code> </li> 
      <li id="li_4079F646493F40DBA0CE75D662A69454"> <code>Legacysegmentid (ex segmentid)</code> </li> 
      <li id="li_D3509A2D379E4C1FB3BC1B5E7D45A916"> <code>Newsegmentid</code> </li> 
      <li id="li_EA901C20EEEB4CFAA39A5E0E822D2394"> <code>status</code> </li> 
      <li id="li_6310E21F88CC4691980DD3C9D551409F"> <code>Datetime</code> </li> 
     </ul> </p> <p>Specificate questi campi in un array come illustrato nell'esempio: </p> <p> <code>[&lt; REMOVED_ SEGMENTS: {seg|&lt; OPEN_ BRACKET &gt; "Mapping": &lt; seg. traitaliani &gt;, "Status: " &lt; seg. status &gt;, "Time": &lt; seg. datetime &gt;, "legacysegmentid": &lt; seg. legacysegmentid &gt;, "newsegmentid": &lt; seg. newsegmentid &gt; &lt; CLOSE_ BRACKET &gt;}; " separator = "," &gt;]</code> </p> <p>Vedere anche <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> Esempi </a>di macro HTTP. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_ TIME_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> Un elenco di ultime realizzazioni per segmenti che l'utente non qualifica più. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_ TRAITALIAS_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Elenco di nomi con alias di segmenti che l'utente non qualifica più. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Restituisce un elenco degli ID del segmento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENTI</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Un elenco di segmenti per i quali l'utente è idoneo. Puoi anche restituire campi segmenti specifici che includono: </p> <p> 
     <ul id="ul_9209683A8E0A4B8081E5EFA4602F743F"> 
      <li id="li_D796526C1C9E45BEA891D619539888C4"> <code>Traitaliani</code> </li> 
      <li id="li_BF12E010E1AD432C84605B9817F209DD"> <code>Legacysegmentid (ex segmentid)</code> </li> 
      <li id="li_4A81E3B715254549B9EADB983A2FC32B"> <code>Newsegmentid</code> </li> 
      <li id="li_1F01A60829DF4C87879D94299E1D589C"> <code>status</code> </li> 
      <li id="li_E52F10CD5A04487D81A4B1750B0DC4E3"> <code>Datetime</code> </li> 
     </ul> </p> <p>Specificate questi campi in un array come illustrato nell'esempio: </p> <p> <code>[&lt; SEGMENTI: {seg|&lt; OPEN_ BRACKET &gt; "Mapping": &lt; seg. traitaliani &gt;, "Status: " &lt; seg. status &gt;, "Time": &lt; seg. datetime &gt;, "legacysegmentid": &lt; seg. legacysegmentid &gt;, "newsegmentid": &lt; seg. newsegmentid &gt; &lt; CLOSE_ BRACKET &gt;}; " separator = "," &gt;]</code> </p> <p>Vedere anche <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> Esempi </a>di macro HTTP. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIME_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Un elenco delle ultime realizzazioni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIMESTAMP</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Unix, marca temporale UTC. Rappresenta l'ultima rappresentazione del segmento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAITALIAS_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Elenco di nomi alias per un particolare segmento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>USER_ AGENT</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Agente utente della richiesta iniziale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>USER_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>POST</code> </p> </td> 
   <td colname="col3"> <p>Elenco degli <span class="keyword"> ID </span> utente di Audience Manager. È inoltre possibile restituire campi specifici che includono quanto segue: </p> 
    <ul id="ul_B6857D809FDC46749B7E745BD8C45F8E"> 
     <li id="li_F31CD82D16ED41FD82518141D90B5B35"> <code>user. aamuuid</code> </li> 
     <li id="li_623FA758C84D4A2D9B25C7FBE90F62B7"> <code>user. dpuuid</code> </li> 
     <li id="li_976B941908EB494EB476B5FB68B8972D"> <code>user. segments</code> </li> 
     <li id="li_D7E129833D1E4D59A554FFCE353924EE"> <code>user. removedsegments</code> </li> 
     <li id="li_8B3DD69D3FE3493492FC9F162812FCD5"> <code>user. useragent</code> </li> 
     <li id="li_8C7EA05585A64141876DF169C31322FE"> <code>user. ip</code> </li> 
     <li id="li_678076A31A7743C480F718C9E7A07E99"> <code>user. dpuuids</code> </li> 
     <li id="li_B598A5AED28C4304972E51DBD4E480D8"> <code>user. timestamp</code> </li> 
     <li id="li_8424D540282F449CA5AF6B3CC343DDCB"> <code>user. random</code> </li>
     <li><code>user. regionids</code></li> 
    </ul> <p>Specificate questi campi come illustrato nell'esempio: </p> <p> 
     <codeblock>
       " AAM_ UUID ": " &lt; user. aamuuid &gt; "datapartner_ 
UUID": " &lt; user. dpuuid &gt; " 
     </codeblock> </p> <p>Consultate anche <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> Esempi </a> di macro HTTP per un esempio completo. </p> </td> 
  </tr>
 </tbody>
</table>