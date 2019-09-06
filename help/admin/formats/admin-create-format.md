---
description: Utilizzate la pagina Formati dello strumento Amministrazione di Audience Manager per creare un nuovo formato o per modificare un formato esistente.
seo-description: Utilizzate la pagina Formati dello strumento Amministrazione di Audience Manager per creare un nuovo formato o per modificare un formato esistente.
seo-title: Creare o modificare un formato
title: Creare o modificare un formato
uuid: ca 1 b 1 feb-bcd 3-4 a 41-b 1 e 8-80565 f 6 c 23 ae
translation-type: tm+mt
source-git-commit: 71bf4cec222428686c1eab0998f66887db06da68

---


# Creare o modificare un formato {#create-or-edit-a-format}

Utilizza la [!UICONTROL Formats] pagina nello strumento Amministrazione di Audience Manager per creare un nuovo formato o per modificare un formato esistente.

<!-- t_create_format.xml -->

>[!TIP]
>
>Quando si seleziona un formato per i dati non vincolati, è consigliabile riutilizzare un formato esistente. L'utilizzo di un formato già collaudato assicura che i dati in uscita vengano generati correttamente. Per visualizzare esattamente la formattazione di un formato esistente, fate clic sull' [!UICONTROL Formats] opzione nella barra dei menu e cercate il formato per nome o per numero ID. I formati non formattati o le macro utilizzate nei formati forniscono un output formattato in modo errato o impediranno l'output completo delle informazioni.

1. Per creare un nuovo formato, fate clic **[!UICONTROL Formats]** su &gt; **[!UICONTROL Add Format]**. Per modificare un formato esistente, fai clic sul formato desiderato nella **[!UICONTROL Name]** colonna.

   ![](assets/create_format.png)

1. Compila i campi:
   * **Nome:** (Obbligatorio) Fornisci un nome descrittivo per il formato.
   * **Tipo:** (Obbligatorio) Selezionate il formato desiderato:
      * **[!UICONTROL File]**: Invia i dati tramite [!DNL FTP] file.
      * **[!UICONTROL HTTP]**: Racchiude i dati in un [!DNL JSON] wrapper.

1. (Condizionale) Se hai scelto **[!UICONTROL File]**, compila i campi:

   >[!NOTE]
   >
   >Per un elenco delle macro disponibili, vedere [Macro Format Macro](../formats/file-formats.md#concept_A867101505074418A58DE325949E5089) e [Macro di formato HTTP](../formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE).

   * **[!UICONTROL File Name]:** Specificare il nome del file per il file di trasferimento dati.
   * **Intestazione:** Specificare il testo che viene visualizzato nella prima riga del file di trasferimento dati.
   * **[!UICONTROL Data Row]:** Specificare il testo che viene visualizzato in ciascuna riga delimitata del file.
   * **[!UICONTROL Maximum File Size (In MB)]:** Specificate la dimensione massima del file per i file di trasferimento dati. I file compressi devono essere inferiori a 100 MB. Non esiste alcun limite per le dimensioni del file non compresso.
   * **[!UICONTROL Compression]:** Seleziona il tipo di compressione desiderato: gz o zip per i file di dati. Per la consegna, [!UICONTROL AWS S3]è necessario utilizzare.gz o file non compressi.
   * **[!UICONTROL .info Receipt]:** Specifica che viene generato un file transfer-control ([!DNL .info]). [!DNL .info] Il file fornisce metadati sui trasferimenti di file, in modo che i partner possano verificare che Audience Manager sia stato gestito correttamente. Per ulteriori informazioni, consultate [File di controllo trasferimento per trasferimenti di file di registro](https://marketing.adobe.com/resources/help/en_US/aam/c_s2s_add_transfer_control_files.html).
   * **[!UICONTROL MD5 Checksum Receipt]:** Specifica che viene [!DNL MD5] generata una ricevuta checksum. La [!DNL MD5] ricevuta checksum in modo che i partner possano verificare che Audience Manager gestisca correttamente il trasferimento completo.

1. (Condizionale) Se hai scelto **[!UICONTROL HTTP]**, compila i campi:

   * **[!UICONTROL Method]:** Scegliete il [!DNL API] metodo da utilizzare per il processo di trasferimento:
      * **[!UICONTROL POST]:** Se selezionate [!DNL POST], selezionate il tipo di contenuto ([!DNL XML] o [!DNL JSON]), quindi specificate il corpo della richiesta.
      * **[!UICONTROL GET]:** Se selezionate [!DNL GET], specificate i parametri di query.

1. Fate clic **[!UICONTROL Create]** su un nuovo formato o fate clic **[!UICONTROL Save Updates]** per modificare un altro formato.

## Eliminare un formato {#delete-format}

1. Fai clic su **[!UICONTROL Formats]**.
2. Fate clic nella ![](assets/icon_delete.png)**[!UICONTROL Actions]** colonna del formato desiderato.
3. Click **[!UICONTROL OK]** to confirm the deletion.
