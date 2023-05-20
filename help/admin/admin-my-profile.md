---
description: Modifica i dettagli del tuo profilo Audience Manager Admin Tool o modifica la password.
seo-description: Edit the details of your Audience Manager Admin tool profile or change your password.
seo-title: My Profile
title: Il mio profilo
uuid: ccaa611d-c855-484e-9696-081d9b4e0935
exl-id: d213f734-af52-4f43-8733-af67ce6f4e98
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 3%

---

# Il mio profilo {#my-profile}

Modifica i dettagli del tuo profilo Audience Manager Admin Tool o modifica la password.

<!-- c_my_profile.xml -->

## Modifica profilo {#edit-profile}

Visualizzare e modificare il profilo dello strumento di amministrazione di Audience Manager, compresi nome e cognome, nome utente, indirizzo e-mail, numero di telefono, [!UICONTROL IMS ID], ruoli utente e stato.

<!-- t_edit_profile.xml -->

1. Clic **[!UICONTROL My Profile]**.

   ![Risultato passaggio](assets/profile.png)

2. Compila i campi:
   * **[!UICONTROL First Name]:** (Obbligatorio) Specifica il nome.
   * **[!UICONTROL Last Name]:** (Obbligatorio) Specifica il cognome.
   * **[!UICONTROL Username]:** (Obbligatorio) Specifica il nome utente.
   * **[!UICONTROL Email Address]:** (Obbligatorio) Specifica il tuo indirizzo e-mail.
   * **[!UICONTROL Phone Number]:** Specifica il numero di telefono.
   * **[!UICONTROL IMS ID]:** Specificare l&#39;ID del servizio di messaggistica Internet.
   * **[!UICONTROL User Roles]:** Seleziona i ruoli utente desiderati:
      * **[!UICONTROL DEXADMIN]:** Fornisce all’amministratore l’accesso per eseguire attività nello strumento di amministrazione Audience Manager. Se non si seleziona questa opzione, è possibile scegliere singoli ruoli. Questi ruoli consentono agli utenti di eseguire attività tramite [!DNL API] ma non nello strumento di amministrazione.
      * **[!UICONTROL CREATE_USERS]:** Consente agli utenti di creare nuovi utenti utilizzando un [!DNL API] chiamare.
      * **[!UICONTROL DELETE_USERS]:** Consente agli utenti di eliminare gli utenti esistenti utilizzando una [!DNL API] chiamare.
      * **[!UICONTROL EDIT_USERS]:** Consente agli utenti di modificare gli utenti esistenti utilizzando un [!DNL API] chiamare.
      * **[!UICONTROL VIEW_USERS]:** Consente agli utenti di visualizzare altri utenti nella configurazione dell’Audience Manager utilizzando un [!DNL API] chiamare.
      * **[!UICONTROL CREATE_PARTNERS]:** Consente agli utenti di creare partner Audienci Manager utilizzando un [!DNL API] chiamare.
      * **[!UICONTROL DELETE_PARTNERS]:** Consente agli utenti di eliminare i partner Audienci Manager utilizzando un [!DNL API] chiamare.
      * **[!UICONTROL EDIT_PARTNERS]:** Consente agli utenti di modificare i partner di Audience Manager utilizzando un [!DNL API] chiamare.
      * **[!UICONTROL VIEW_PARNTERS]:** Consente agli utenti di visualizzare i partner Audienci Manager utilizzando un [!DNL API] chiamare.
   * **[!UICONTROL Status]:** Seleziona lo stato desiderato:
      * **[!UICONTROL Active]:** Specifica che questo utente si trova in un utente Audience Manager attivo.
      * **[!UICONTROL Deactivated]:** Specifica che questo utente è un utente disattivato in Gestione dell&#39;audience.
      * **[!UICONTROL Expired]:** Specifica che l&#39;account dell&#39;utente in Audience Manager è scaduto.
      * **[!UICONTROL Locked Out]:** Specifica che l&#39;account di questo utente in Audience Manager è bloccato.
3. Clic **[!UICONTROL Submit]**.

## Cambia password {#change-password}

Cambia la password dello strumento di amministrazione Audience Manager.

<!-- t_change_password.xml -->

1. Clic **[!UICONTROL My Profile]**.
1. Clic **[!UICONTROL Change Password]**.

   ![](assets/change_password.png)

   La password di Audience Manager deve essere:

   * Lunghezza minima di otto caratteri;
   * contenere almeno un carattere maiuscolo;
   * contenere almeno un carattere minuscolo;
   * contenere almeno un numero;
   * contenere almeno un carattere speciale;
   * Iniziare e terminare con un carattere alfanumerico;
   * Iniziare e terminare con un carattere alfanumerico.

1. Specifica la vecchia password.
1. Specifica la nuova password, quindi conferma la nuova password.
1. Clic **[!UICONTROL OK]**.
