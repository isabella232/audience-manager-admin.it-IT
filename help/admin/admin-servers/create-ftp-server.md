---
description: Utilizza la pagina Server nello strumento Amministrazione di Audience Manager per creare un nuovo server FTP o per modificare un server esistente.
seo-description: Utilizza la pagina Server nello strumento Amministrazione di Audience Manager per creare un nuovo server FTP o per modificare un server esistente.
seo-title: Creare o modificare un server FTP
title: Creare o modificare un server FTP
uuid: 9273 abb 2-963 d -4 d 83-bf 5 a-b 3817 f 0 b 90 e 6
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# Creare o modificare un server FTP {#create-or-edit-an-ftp-server}

Utilizza la [!UICONTROL Servers] pagina nello strumento Amministrazione di Audience Manager per creare un nuovo server FTP o per modificare un server esistente.

>[!NOTE]
>
>Per creare nuovi server o modificare quelli esistenti, [!UICONTROL DEXADMIN] dovete avere il ruolo desiderato.

1. Per creare un nuovo server, fate clic **[!UICONTROL Servers]** su &gt; **[!UICONTROL Create Server]**. Per modificare un server esistente, fai clic sul server desiderato nella **[!UICONTROL Label]** colonna.
1. Specificate l'etichetta desiderata per il server.
1. Dall'elenco **[!UICONTROL Protocol]** a discesa, selezionate il protocollo desiderato: **FTP**.

   >[!NOTE]
   >
   >Come procedura ottimale, consigliamo di usare [!DNL Amazon S3] come metodo per ottenere file e inviare file ai partner. [!DNL Amazon S3] fornisce una semplice interfaccia dei servizi Web che può essere utilizzata per archiviare e recuperare qualsiasi quantità di dati in qualsiasi punto del Web. Per ulteriori informazioni, vedi [Informazioni su Amazon S 3](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html) nella Guida utente *di Audience Manager*.

1. Compila i campi:

   * **[!UICONTROL Type]:** Selezionare il tipo di cifratura desiderato: **[!UICONTROL SFTP]** oppure **[!UICONTROL FTPs/TLS]**.
   * **[!UICONTROL Domain]:** Specificate il dominio desiderato (ospitante) per questo server.
   * **[!UICONTROL Port]:** Specificate la porta desiderata per il server. La porta predefinita viene visualizzata per ogni tipo di cifratura. Se necessario, potete modificare la porta predefinita.
   * **[!UICONTROL Remote Path]:** Specifica il percorso remoto desiderato per il server. Se lasciate vuoto questo campo, Audience Manager colloca i file nella directory predefinita.
   * **[!UICONTROL .tmp File Rename on Completion]:** Abilitare questa opzione per rinominare `.tmp` il file al termine.
   * **[!UICONTROL Filename Suffix]:** Specificate il testo da aggiungere al trasferimento dei file.
   * **[!UICONTROL Moved to When Finished]:** Specificate il percorso del percorso in cui desiderate spostare il file di trasferimento al termine.
   * **[!UICONTROL Authentication]:** Specificate il metodo di autenticazione server desiderato: **[!UICONTROL Username/Password]** oppure **[!UICONTROL SSH Key]**.
   >[!NOTE]
   >
   >Ricorda di inserire il nostro eglet [!DNL FTP][!DNL IP]: **52.44.29.204**.

1. Per **[!UICONTROL SSH Key]** l'autenticazione:
   1. Genera la coppia di chiave pubblica/privata da qualsiasi [!DNL Linux][!DNL Mac] o computer.
   1. Assegna la **chiave** pubblica al client da aggiornare sul [!DNL SFTP] server. Devono includere tutto il testo della chiave pubblica sul server, incluso `-----BEGIN RSA PRIVATE KEY-----` e `-----END RSA PRIVATE KEY-----` . In sostituzione, devono fornire il nome utente in cui stanno installando la chiave.
   1. Aggiorna il campo nome utente con quello fornito dal client e il campo chiave con la **chiave privata**.
1. Fate clic **[!UICONTROL Create]** su un nuovo server o fate clic **[!UICONTROL Update]** su di esso per modificare un server esistente.
