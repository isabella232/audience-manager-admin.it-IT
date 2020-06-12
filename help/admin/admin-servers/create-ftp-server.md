---
description: Utilizzate la pagina Server dello strumento di amministrazione di Audience Manager per creare un nuovo server FTP o per modificare un server esistente.
seo-description: Utilizzate la pagina Server dello strumento di amministrazione di Audience Manager per creare un nuovo server FTP o per modificare un server esistente.
seo-title: Creare o modificare un server FTP
title: Creare o modificare un server FTP
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
translation-type: tm+mt
source-git-commit: e0dc190f8765ec91431a2c02a62c6bf5458c7e3d
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 5%

---


# Creare o modificare un server FTP {#create-or-edit-an-ftp-server}

Utilizzate la [!UICONTROL Servers] pagina nello strumento di amministrazione di Audience Manager per creare un nuovo server FTP o per modificare un server esistente.

>[!NOTE]
>
>È necessario disporre del [!UICONTROL DEXADMIN] ruolo per creare nuovi server o modificare server esistenti.

1. Per creare un nuovo server, fate clic su **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Per modificare un server esistente, fate clic sul server desiderato nella **[!UICONTROL Label]** colonna.
1. Specificate l&#39;etichetta desiderata per il server.
1. Dall&#39;elenco a **[!UICONTROL Protocol]** discesa, selezionate il protocollo desiderato: **FTP**.

   >[!NOTE]
   >
   >Come procedura ottimale, si consiglia di utilizzare [!DNL Amazon S3] come metodo per ottenere i file da e consegnare i file ai partner. [!DNL Amazon S3] fornisce una semplice interfaccia di servizi Web che può essere utilizzata per archiviare e recuperare qualsiasi quantità di dati, in qualsiasi momento, da qualsiasi punto del web. Per ulteriori informazioni, consulta [Informazioni su Amazon S3](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html) nella Guida utente di *Audience Manager*.

1. Compila i campi:

   * **[!UICONTROL Type]:**Selezionare il tipo di crittografia desiderato:**[!UICONTROL SFTP]**o **[!UICONTROL FTPs/TLS]**.
   * **[!UICONTROL Domain]:**Specificare il dominio desiderato (host) per il server.
   * **[!UICONTROL Port]:**Specificare la porta desiderata per il server. Per ogni tipo di crittografia viene visualizzata la porta predefinita. Se necessario, potete modificare la porta predefinita.
   * **[!UICONTROL Remote Path]:**Specificare il percorso remoto desiderato per il server. Se lasciate vuoto questo campo, Audience Manager inserisce i file nella directory predefinita.
   * **[!UICONTROL .tmp File Rename on Completion]:**Abilitate questa opzione per rinominare il`.tmp`file al termine.
   * **[!UICONTROL Filename Suffix]:**Specificate il testo da aggiungere per trasferire i file.
   * **[!UICONTROL Moved to When Finished]:**Specificare il percorso del percorso in cui spostare il file di trasferimento al termine.
   * **[!UICONTROL Authentication]:**Specificate il metodo di autenticazione del server desiderato:**[!UICONTROL Username/Password]**o **[!UICONTROL SSH Key]**.
   >[!NOTE]
   >
   >Ricorda di aggiungere la nostra uscita [!DNL FTP][!DNL IP] alla tua lista di IP consentiti: **52.44.29.2004**.

1. Per **[!UICONTROL SSH Key]** l&#39;autenticazione:
   1. Generare la coppia chiave pubblica/privata da qualsiasi [!DNL Linux] computer o [!DNL Mac] computer.
   1. Attribuite la chiave **** pubblica al client per l&#39;aggiornamento sul [!DNL SFTP] server. Devono includere tutto il testo della chiave pubblica sul loro server, compresi `-----BEGIN RSA PRIVATE KEY-----` e `-----END RSA PRIVATE KEY-----` . In cambio, devono fornire il nome utente con cui stanno installando la chiave.
   1. Aggiornate il campo nome utente con quello fornito dal client e il campo chiave con la chiave **** privata.
1. Fate clic su **[!UICONTROL Create]** se state creando un nuovo server, oppure su **[!UICONTROL Update]** se state modificando un server esistente.
