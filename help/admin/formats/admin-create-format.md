---
description: Utilizza la pagina Formati nello strumento Amministratore Audience Manager per creare un nuovo formato o per modificare un formato esistente.
seo-description: Use the Formats page in the Audience Manager Admin tool to create a new format or to edit an existing format.
seo-title: Create or Edit a Format
title: Creare o modificare un formato
uuid: ca1b1feb-bcd3-4a41-b1e8-80565f6c23ae
exl-id: 3c97d1e9-8093-4181-a1fd-fb1816cdaa3d
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 3%

---

# Creare o modificare un formato {#create-or-edit-a-format}

Utilizza la pagina [!UICONTROL Formats] nello strumento Amministratore Audience Manager per creare un nuovo formato o per modificare un formato esistente.

<!-- t_create_format.xml -->

>[!TIP]
>
>Quando selezioni un formato per i dati non delimitati, è meglio, se possibile, riutilizzare un formato esistente. L’utilizzo di un formato già collaudato garantisce la corretta generazione dei dati in uscita. Per visualizzare esattamente il formato di un formato esistente, fai clic sull&#39;opzione [!UICONTROL Formats] nella barra dei menu e cerca il formato per nome o per numero di ID. I formati o le macro errati utilizzati nei formati forniscono un output formattato in modo errato o impediranno l’output completo delle informazioni.

1. Per creare un nuovo formato, fai clic su **[!UICONTROL Formats]** > **[!UICONTROL Add Format]**. Per modificare un formato esistente, fai clic sul formato desiderato nella colonna **[!UICONTROL Name]** .

   ![](assets/create_format.png)

1. Compila i campi:
   * **Nome:**  (obbligatorio) specifica un nome descrittivo per il formato.
   * **Tipo:**  (obbligatorio) seleziona il formato desiderato:
      * **[!UICONTROL File]**: Invia dati tramite  [!DNL FTP] file.
      * **[!UICONTROL HTTP]**: Racchiude i dati in un  [!DNL JSON] wrapper.

1. (Condizionale) Se hai scelto **[!UICONTROL File]**, compila i campi:

   >[!NOTE]
   >
   >Per un elenco delle macro disponibili, vedere [Macro per formati file](../formats/file-formats.md#concept_A867101505074418A58DE325949E5089) e [Macro per formati HTTP](../formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE).

   * **[!UICONTROL File Name]:** specifica il nome del file per il file di trasferimento dati.
   * **Intestazione:** specifica il testo visualizzato nella prima riga del file di trasferimento dati.
   * **[!UICONTROL Data Row]:** Specifica il testo che viene visualizzato in ogni riga esterna del file.
   * **[!UICONTROL Maximum File Size (In MB)]:** specifica la dimensione massima del file per i file di trasferimento dati. I file compressi devono essere più piccoli di 100 MB. Non esiste alcun limite alle dimensioni del file non compresso.
   * **[!UICONTROL Compression]:** Selezionare il tipo di compressione desiderato: gz o zip per i file di dati. Per la consegna a [!UICONTROL AWS S3], è necessario utilizzare file .gz o non compressi.
   * **[!UICONTROL .info Receipt]:** Specifica che viene generato un file di controllo del trasferimento ([!DNL .info]). Il file [!DNL .info] fornisce informazioni sui metadati sui trasferimenti di file in modo che i partner possano verificare che Audience Manager gestisca correttamente i trasferimenti di file. Per ulteriori informazioni, vedere [File di trasferimento-controllo per trasferimenti di file di registro](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/transfer-control-files.html?lang=en).
   * **[!UICONTROL MD5 Checksum Receipt]:** Specifica che viene generata una ricezione  [!DNL MD5] checksum. La ricevuta di checksum [!DNL MD5] in modo che i partner possano verificare che l’Audience Manager abbia gestito correttamente il trasferimento completo.

1. (Condizionale) Se hai scelto **[!UICONTROL HTTP]**, compila i campi:

   * **[!UICONTROL Method]:** Scegli il  [!DNL API] metodo che desideri utilizzare per il processo di trasferimento:
      * **[!UICONTROL POST]:** Se selezioni  [!DNL POST], seleziona il tipo di contenuto ([!DNL XML] o  [!DNL JSON]), quindi specifica il corpo della richiesta.
      * **[!UICONTROL GET]:** Se selezioni  [!DNL GET], specifica i parametri di query.

1. Fare clic su **[!UICONTROL Create]** se si sta creando un nuovo formato oppure fare clic su **[!UICONTROL Save Updates]** se si sta modificando un formato esistente.

## Eliminare un formato {#delete-format}

1. Clic **[!UICONTROL Formats]**.
2. Fare clic su ![](assets/icon_delete.png) nella colonna **[!UICONTROL Actions]** del formato desiderato.
3. Fai clic su **[!UICONTROL OK]** per confermare l’eliminazione.
