---
description: Utilizza la pagina Utenti integrazione per visualizzare un elenco degli utenti nella configurazione di Audience Manager. Potete modificare o eliminare utenti esistenti oppure creare nuovi utenti, a condizione che disponiate dei ruoli utente appropriati assegnati.
seo-description: Utilizza la pagina Utenti integrazione per visualizzare un elenco degli utenti nella configurazione di Audience Manager. Potete modificare o eliminare utenti esistenti oppure creare nuovi utenti, a condizione che disponiate dei ruoli utente appropriati assegnati.
seo-title: Utenti integrazione
title: Utenti integrazione
uuid: 13 dcb 3 fb -4561-409 c -84 da -943 d 0 d 390 cf 3
translation-type: tm+mt
source-git-commit: 10adb6b06160f5a5c4068483b407e5798fc10150

---


# Utenti integrazione {#integration-users}

Utilizza la [!UICONTROL Integration Users] pagina per visualizzare un elenco degli utenti nella configurazione di Audience Manager. Potete modificare o eliminare utenti esistenti oppure creare nuovi utenti, a condizione che disponiate dei ruoli utente appropriati assegnati.

<!-- c_integration_users.xml -->

Potete ordinare ciascuna colonna in ordine crescente o decrescente facendo clic sull'intestazione della colonna desiderata.
Utilizzate la [!UICONTROL Search] casella o i controlli di impaginazione in fondo all'elenco per trovare l'utente desiderato.

## Creare o modificare un utente {#create-edit-user}

Utilizza la [!UICONTROL Integration Users] pagina dello strumento Audience Manager [!UICONTROL Admin] per creare un nuovo utente o per modificare un account esistente.

<!-- t_create_user.xml -->

>[!NOTE]
>
>Per creare nuovi utenti è necessario avere [!UICONTROL CREATE_USER] il ruolo desiderato. Per modificare gli utenti esistenti dovete avere [!UICONTROL EDIT_USER] il ruolo necessario.

1. Per creare un nuovo utente, fate clic **[!UICONTROL Integration Users]** su &gt; **[!UICONTROL Create a New User]**. Per modificare un utente esistente, fai clic sull'utente desiderato nella **[!UICONTROL Username]** colonna.
2. Compila i campi:
   * **[!UICONTROL First Name]**: (Obbligatorio) Specifica il nome dell'utente.
   * **[!UICONTROL Last Name]**: (Obbligatorio) Specifica il cognome dell'utente.
   * **[!UICONTROL Username]**: (Obbligatorio) Specificate il nome utente dell'utente.
   * **[!UICONTROL Email Address]**: (Obbligatorio) Specificate l'indirizzo e-mail dell'utente.
   * **[!UICONTROL Phone Number]**: Specificate il numero di telefono dell'utente.
   * **[!UICONTROL IMS ID]**: Specificate [!UICONTROL Internet Messaging Service ID]l'utente.
   * **[!UICONTROL User Roles]**: Selezionate i ruoli utente desiderati:
      * **[!UICONTROL DEXADMIN]**: Fornisce agli amministratori l'accesso per eseguire attività nello [!UICONTROL Admin] strumento Audience Manager. Se non selezionate questa opzione, potete scegliere i singoli ruoli. Questi ruoli consentono agli utenti di eseguire attività utilizzando [!DNL API] chiamate, ma non nello strumento Amministrazione.
      * **[!UICONTROL CREATE_USERS]**: Consente agli utenti di creare nuovi utenti mediante [!DNL API] una chiamata.
      * **[!UICONTROL DELETE_USERS]**: Consente agli utenti di eliminare gli utenti esistenti mediante [!DNL API] una chiamata.
      * **[!UICONTROL EDIT_USERS]**: Consente agli utenti di modificare gli utenti esistenti mediante [!DNL API] una chiamata.
      * **[!UICONTROL VIEW_USERS]**: Consente agli utenti di visualizzare altri utenti nella configurazione di Audience Manager mediante una [!DNL API] chiamata.
      * **[!UICONTROL CREATE_PARTNERS]**: Consente agli utenti di creare partner Audience Manager mediante [!DNL API] una chiamata.
      * **[!UICONTROL DELETE_PARTNERS]**: Consente agli utenti di eliminare i partner Audience Manager mediante [!DNL API] una chiamata.
      * **[!UICONTROL EDIT_PARTNERS]**: Consente agli utenti di modificare i partner Audience Manager mediante [!DNL API] una chiamata.
      * **[!UICONTROL VIEW_PARNTERS]**: Consente agli utenti di visualizzare i partner Audience Manager mediante [!DNL API] una chiamata.
   * **Stato:** Seleziona **[!UICONTROL Active]** questa opzione per rendere l'utente un utente Audience Manager attivato.
3. Fai clic su **[!UICONTROL Submit]**.

## Eliminare un utente {#delete-user}

Utilizzate la [!UICONTROL Integration Users] pagina nello strumento Audience Manager [!UICONTROL Admin] per eliminare un utente esistente.

<!-- t_delete_user.xml -->

>[!NOTE]
>
>Per creare nuovi utenti è necessario avere **[!UICONTROL DELETE_USER]** il ruolo desiderato.

1. Fai clic su **[!UICONTROL Integration Users]**.
2. Fate clic ![](assets/icon_delete.png) nella **[!UICONTROL Actions]** colonna dell'utente desiderato.
3. Click **[!UICONTROL OK]** to confirm the deletion.