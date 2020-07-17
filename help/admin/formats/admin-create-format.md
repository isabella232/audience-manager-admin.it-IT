---
description: Utilizzare la pagina Formati dello strumento  Audience Manager Admin per creare un nuovo formato o per modificare un formato esistente.
seo-description: Utilizzare la pagina Formati dello strumento  Audience Manager Admin per creare un nuovo formato o per modificare un formato esistente.
seo-title: Creare o modificare un formato
title: Creare o modificare un formato
uuid: ca1b1feb-bcd3-4a41-b1e8-80565f6c23ae
translation-type: tm+mt
source-git-commit: 71bf4cec222428686c1eab0998f66887db06da68
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 4%

---


# Creare o modificare un formato {#create-or-edit-a-format}

Utilizzare la [!UICONTROL Formats] pagina nello strumento Amministrazione Audience Manager  per creare un nuovo formato o per modificare un formato esistente.

<!-- t_create_format.xml -->

>[!TIP]
>
>Quando si seleziona un formato per i dati non delimitati, è consigliabile, se possibile, riutilizzare un formato esistente. L&#39;utilizzo di un formato già collaudato garantisce la generazione dei dati in uscita. Per visualizzare esattamente la formattazione di un formato esistente, fate clic sull’ [!UICONTROL Formats] opzione nella barra dei menu e cercate il formato per nome o per numero di ID. I formati errati o le macro utilizzate nei formati forniranno un output formattato in modo errato o impediranno l&#39;output completo delle informazioni.

1. Per creare un nuovo formato, fate clic su **[!UICONTROL Formats]** > **[!UICONTROL Add Format]**. Per modificare un formato esistente, fate clic sul formato desiderato nella **[!UICONTROL Name]** colonna.

   ![](assets/create_format.png)

1. Compila i campi:
   * **Nome:** (Obbligatorio) Fornire un nome descrittivo per il formato.
   * **Tipo:** (Obbligatorio) Selezionate il formato desiderato:
      * **[!UICONTROL File]**: Invia i dati tramite [!DNL FTP] file.
      * **[!UICONTROL HTTP]**: Racchiude i dati in un [!DNL JSON] wrapper.

1. (Condizionale) Se avete scelto **[!UICONTROL File]**, compilate i campi:

   >[!NOTE]
   >
   >Per un elenco delle macro disponibili, vedere Macro [in formato](../formats/file-formats.md#concept_A867101505074418A58DE325949E5089) file e Macro in formato [HTTP](../formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE).

   * **[!UICONTROL File Name]:**Specificare il nome file per il file di trasferimento dati.
   * **Intestazione:** Specificare il testo che viene visualizzato nella prima riga del file di trasferimento dati.
   * **[!UICONTROL Data Row]:**Specificate il testo che viene visualizzato in ciascuna riga esterna del file.
   * **[!UICONTROL Maximum File Size (In MB)]:**Specificate la dimensione massima del file per i file di trasferimento dati. I file compressi devono essere inferiori a 100 MB. Non esiste alcun limite per la dimensione del file non compresso.
   * **[!UICONTROL Compression]:**Selezionare il tipo di compressione desiderato: gz o zip per i file di dati. Per la consegna a[!UICONTROL AWS S3], dovete usare file .gz o non compressi.
   * **[!UICONTROL .info Receipt]:**Specifica che viene generato un file transfer-control ([!DNL .info]). Il[!DNL .info]file fornisce informazioni sui metadati relativi ai trasferimenti di file in modo che i partner possano verificare che  trasferimenti di file gestiti da Audience Manager siano corretti. Per ulteriori informazioni, vedere File di[trasferimento-controllo per trasferimenti](https://marketing.adobe.com/resources/help/en_US/aam/c_s2s_add_transfer_control_files.html)di file di registro.
   * **[!UICONTROL MD5 Checksum Receipt]:**Specifica che viene generata una ricevuta[!DNL MD5]checksum. La ricevuta[!DNL MD5]checksum in modo che i partner possano verificare che  Audience Manager abbia gestito correttamente il trasferimento completo.

1. (Condizionale) Se avete scelto **[!UICONTROL HTTP]**, compilate i campi:

   * **[!UICONTROL Method]:**Scegliere il[!DNL API]metodo da utilizzare per il processo di trasferimento:
      * **[!UICONTROL POST]:**Se selezionate[!DNL POST], selezionate il tipo di contenuto ([!DNL XML]o[!DNL JSON]), quindi specificate il corpo della richiesta.
      * **[!UICONTROL GET]:**Se si seleziona[!DNL GET], specificare i parametri della query.

1. Fate clic su **[!UICONTROL Create]** se state creando un nuovo formato, oppure su **[!UICONTROL Save Updates]** se state modificando un formato esistente.

## Eliminare un formato {#delete-format}

1. Clic **[!UICONTROL Formats]**.
2. Fate clic ![](assets/icon_delete.png) nella **[!UICONTROL Actions]** colonna del formato desiderato.
3. Click **[!UICONTROL OK]** to confirm the deletion.
