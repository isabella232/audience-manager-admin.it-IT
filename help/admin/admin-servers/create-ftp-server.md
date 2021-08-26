---
description: Utilizza la pagina Server nello strumento Amministratore Audience Manager per creare un nuovo server FTP o per modificare un server esistente.
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

Utilizza la pagina [!UICONTROL Servers] nello strumento Amministratore Audience Manager per creare un nuovo server FTP o per modificare un server esistente.

>[!NOTE]
>
>È necessario disporre del ruolo [!UICONTROL DEXADMIN] per creare nuovi server o modificare quelli esistenti.

1. Per creare un nuovo server, fai clic su **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Per modificare un server esistente, fai clic sul server desiderato nella colonna **[!UICONTROL Label]** .
1. Specifica l&#39;etichetta desiderata per il server.
1. Dall’elenco a discesa **[!UICONTROL Protocol]** , seleziona il protocollo desiderato: **FTP**.

   >[!NOTE]
   >
   >Come best practice, si consiglia di utilizzare [!DNL Amazon S3] come metodo per ottenere file da e consegnare file ai partner. [!DNL Amazon S3] fornisce una semplice interfaccia di servizi web che può essere utilizzata per memorizzare e recuperare qualsiasi quantità di dati, in qualsiasi momento, da qualsiasi punto del web. Per ulteriori informazioni, consulta [Informazioni su Amazon S3](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html) nella *Guida utente di Audience Manager*.

1. Compila i campi:

   * **[!UICONTROL Type]:** Seleziona il tipo di crittografia desiderato:  **[!UICONTROL SFTP]** o  **[!UICONTROL FTPs/TLS]**.
   * **[!UICONTROL Domain]:** specifica il dominio desiderato (host) per questo server.
   * **[!UICONTROL Port]:** specifica la porta desiderata per questo server. Viene visualizzata la porta predefinita per ogni tipo di crittografia. Se necessario, puoi modificare la porta predefinita.
   * **[!UICONTROL Remote Path]:** specifica il percorso remoto desiderato per questo server. Se si lascia vuoto questo campo, Audience Manager inserisce i file nella directory predefinita.
   * **[!UICONTROL .tmp File Rename on Completion]:** Abilita questa opzione per rinominare il  `.tmp` file al termine.
   * **[!UICONTROL Filename Suffix]:** specifica il testo da aggiungere per trasferire i file.
   * **[!UICONTROL Moved to When Finished]:** specifica il percorso della posizione in cui vuoi spostare il file di trasferimento al termine.
   * **[!UICONTROL Authentication]:** specifica il metodo di autenticazione del server desiderato:  **[!UICONTROL Username/Password]** o  **[!UICONTROL SSH Key]**.

   >[!NOTE]
   >
   >Ricorda di aggiungere il nostro indirizzo [!DNL FTP] [!DNL IP] all’elenco degli IP consentiti : **52.44.29.204**.

1. Per l&#39;autenticazione **[!UICONTROL SSH Key]**:
   >[!NOTE]
   >
   >Durante la configurazione dell’autenticazione della chiave SSH, assicurati di generare sempre le chiavi pubbliche e private solo in formato OpenSSH.
   1. Generare la coppia di chiavi pubblica/privata da qualsiasi computer [!DNL Linux] o [!DNL Mac].
   1. Assegnare la **chiave pubblica** al client per l&#39;aggiornamento sul server [!DNL SFTP]. Devono includere tutto il testo della chiave pubblica sul server, compresi `-----BEGIN RSA PRIVATE KEY-----` e `-----END RSA PRIVATE KEY-----` . In cambio, devono fornire il nome utente con cui stanno installando la chiave.
   1. Aggiorna il campo nome utente con quello fornito dal client e il campo chiave con la **chiave privata**.
1. Fare clic su **[!UICONTROL Create]** se si sta creando un nuovo server oppure fare clic su **[!UICONTROL Update]** se si sta modificando un server esistente.
