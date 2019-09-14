---
description: Utilizzate la pagina Utenti integrazione per visualizzare un elenco degli utenti nella configurazione di Audience Manager. Potete modificare o eliminare utenti esistenti o creare nuovi utenti, a condizione che vi siano stati assegnati i ruoli utente appropriati.
seo-description: Utilizzate la pagina Utenti integrazione per visualizzare un elenco degli utenti nella configurazione di Audience Manager. Potete modificare o eliminare utenti esistenti o creare nuovi utenti, a condizione che vi siano stati assegnati i ruoli utente appropriati.
seo-title: Utenti integrazione
title: Utenti integrazione
uuid: 13dcb3fb-4561-409c-84da-943d0d390cf3
translation-type: tm+mt
source-git-commit: 10adb6b06160f5a5c4068483b407e5798fc10150

---


# Utenti integrazione {#integration-users}

Utilizzate la [!UICONTROL Integration Users] pagina per visualizzare un elenco degli utenti nella configurazione di Audience Manager. Potete modificare o eliminare utenti esistenti o creare nuovi utenti, a condizione che vi siano stati assegnati i ruoli utente appropriati.

<!-- c_integration_users.xml -->

Potete ordinare ciascuna colonna in ordine crescente o decrescente facendo clic sull’intestazione della colonna desiderata.
Utilizzare la [!UICONTROL Search] casella o i controlli di impaginazione in fondo all'elenco per individuare l'utente desiderato.

## Creare o modificare un utente {#create-edit-user}

Utilizzate la [!UICONTROL Integration Users] pagina nello strumento Audience Manager [!UICONTROL Admin] per creare un nuovo utente o per modificare un account utente esistente.

<!-- t_create_user.xml -->

>[!NOTE]
>
>Per creare nuovi utenti è necessario disporre del [!UICONTROL CREATE_USER] ruolo. È necessario avere il [!UICONTROL EDIT_USER] ruolo di modificare gli utenti esistenti.

1. Per creare un nuovo utente, fate clic su **[!UICONTROL Integration Users]** &gt; **[!UICONTROL Create a New User]**. Per modificare un utente esistente, fate clic sull’utente desiderato nella **[!UICONTROL Username]** colonna.
2. Compila i campi:
   * **[!UICONTROL First Name]**: (Obbligatorio) Specificate il nome dell'utente.
   * **[!UICONTROL Last Name]**: (Obbligatorio) Specificate il cognome dell'utente.
   * **[!UICONTROL Username]**: (Obbligatorio) Specificate il nome utente dell'utente.
   * **[!UICONTROL Email Address]**: (Obbligatorio) Specificate l'indirizzo e-mail dell'utente.
   * **[!UICONTROL Phone Number]**: Specificate il numero di telefono dell'utente.
   * **[!UICONTROL IMS ID]**: Specificate le impostazioni dell'utente [!UICONTROL Internet Messaging Service ID].
   * **[!UICONTROL User Roles]**: Selezionate i ruoli utente desiderati:
      * **[!UICONTROL DEXADMIN]**: Fornisce l'accesso dell'amministratore per eseguire attività nello strumento Audience Manager [!UICONTROL Admin] . Se non selezionate questa opzione, potete scegliere i singoli ruoli. Questi ruoli consentono agli utenti di eseguire attività mediante [!DNL API] chiamate, ma non nello strumento Admin.
      * **[!UICONTROL CREATE_USERS]**: Consente agli utenti di creare nuovi utenti tramite una [!DNL API] chiamata.
      * **[!UICONTROL DELETE_USERS]**: Consente agli utenti di eliminare gli utenti esistenti utilizzando una [!DNL API] chiamata.
      * **[!UICONTROL EDIT_USERS]**: Consente agli utenti di modificare gli utenti esistenti utilizzando una [!DNL API] chiamata.
      * **[!UICONTROL VIEW_USERS]**: Consente agli utenti di visualizzare altri utenti nella configurazione di Audience Manager mediante una [!DNL API] chiamata.
      * **[!UICONTROL CREATE_PARTNERS]**: Consente agli utenti di creare partner Audience Manager tramite una [!DNL API] chiamata.
      * **[!UICONTROL DELETE_PARTNERS]**: Consente agli utenti di eliminare i partner Audience Manager utilizzando una [!DNL API] chiamata.
      * **[!UICONTROL EDIT_PARTNERS]**: Consente agli utenti di modificare i partner Audience Manager utilizzando una [!DNL API] chiamata.
      * **[!UICONTROL VIEW_PARNTERS]**: Consente agli utenti di visualizzare i partner Audience Manager utilizzando una [!DNL API] chiamata.
   * **** Stato: Selezionate questa opzione **[!UICONTROL Active]** per rendere questo utente un utente Audience Manager attivato.
3. Fai clic su **[!UICONTROL Submit]**.

## Eliminare un utente {#delete-user}

Usate la [!UICONTROL Integration Users] pagina nello strumento Audience Manager [!UICONTROL Admin] per eliminare un utente esistente.

<!-- t_delete_user.xml -->

>[!NOTE]
>
>Per creare nuovi utenti è necessario disporre del **[!UICONTROL DELETE_USER]** ruolo.

1. Fai clic su **[!UICONTROL Integration Users]**.
2. Fate clic ![](assets/icon_delete.png) nella **[!UICONTROL Actions]** colonna dell’utente desiderato.
3. Click **[!UICONTROL OK]** to confirm the deletion.