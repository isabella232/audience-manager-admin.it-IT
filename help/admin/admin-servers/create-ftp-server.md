---
description: Utilizzare la pagina Server di Audience Manager Admin Tool per creare un nuovo server FTP o per modificare un server esistente.
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new FTP server or to edit an existing server.
seo-title: Create or Edit an FTP Server
title: Creare o modificare un server FTP
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
exl-id: 9eae4ecf-ccde-483a-ae53-1cbac033d8d6
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 4%

---

# Creare o modificare un server FTP {#create-or-edit-an-ftp-server}

Utilizza il [!UICONTROL Servers] nello strumento di amministrazione Audience Manager per creare un nuovo server FTP o per modificare un server esistente.

>[!NOTE]
>
>È necessario disporre di [!UICONTROL DEXADMIN] per creare nuovi server o modificare quelli esistenti.

1. Per creare un nuovo server, fare clic su **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Per modificare un server esistente, fare clic sul server desiderato nella **[!UICONTROL Label]** colonna.
1. Specificare l&#39;etichetta desiderata per il server.
1. Dalla sezione **[!UICONTROL Protocol]** dall&#39;elenco a discesa, selezionare il protocollo desiderato: **FTP**.

   >[!NOTE]
   >
   >Come best practice, si consiglia di utilizzare [!DNL Amazon S3] come metodo per ottenere file da e consegnarli ai partner. [!DNL Amazon S3] fornisce una semplice interfaccia di servizi web che può essere utilizzata per memorizzare e recuperare qualsiasi quantità di dati, in qualsiasi momento, da qualsiasi punto del web. Per ulteriori informazioni, consulta [Informazioni su Amazon S3](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html) nel *Guida utente di Audience Manager*.

1. Compila i campi:

   * **[!UICONTROL Type]:** Selezionare il tipo di crittografia desiderato: **[!UICONTROL SFTP]** o **[!UICONTROL FTPs/TLS]**.
   * **[!UICONTROL Domain]:** Specificare il dominio (host) desiderato per il server.
   * **[!UICONTROL Port]:** Specificare la porta desiderata per il server. Viene visualizzata la porta predefinita per ogni tipo di crittografia. Se necessario, è possibile modificare la porta predefinita.
   * **[!UICONTROL Remote Path]:** Specificare il percorso remoto desiderato per il server. Se si lascia vuoto questo campo, Audience Manager inserisce i file nella directory predefinita.
   * **[!UICONTROL .tmp File Rename on Completion]:** Abilita questa opzione per rinominare `.tmp` al completamento.
   * **[!UICONTROL Filename Suffix]:** Specificare il testo che si desidera aggiungere per trasferire i file.
   * **[!UICONTROL Moved to When Finished]:** Specificare il percorso del percorso in cui si desidera spostare il file di trasferimento al termine dell&#39;operazione.
   * **[!UICONTROL Authentication]:** Specificare il metodo di autenticazione server desiderato: **[!UICONTROL Username/Password]** o **[!UICONTROL SSH Key]**.

   >[!NOTE]
   >
   >Ricordati di aggiungere la nostra uscita [!DNL FTP] [!DNL IP] nell’elenco degli IP consentiti: **52.44.29.204**.

1. Per **[!UICONTROL SSH Key]** autenticazione:
   >[!NOTE]
   >
   >Durante la configurazione dell’autenticazione della chiave SSH, assicurati di generare sempre le chiavi pubbliche e private solo in formato OpenSSH.
   1. Genera la coppia di chiavi pubblica/privata da qualsiasi [!DNL Linux] o [!DNL Mac] macchina.
   1. Assegna a **chiave pubblica** al cliente per aggiornare il [!DNL SFTP] server. Devono includere tutto il testo della chiave pubblica sul loro server, incluso `-----BEGIN RSA PRIVATE KEY-----` e  `-----END RSA PRIVATE KEY-----` . In cambio, devono fornire il nome utente con cui stanno installando la chiave.
   1. Aggiorna il campo del nome utente con quello fornito dal client e il campo chiave con **chiave privata**.
1. Clic **[!UICONTROL Create]** se si sta creando un nuovo server o fare clic su **[!UICONTROL Update]** se si modifica un server esistente.
