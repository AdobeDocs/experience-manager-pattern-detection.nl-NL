---
title: FORM
description: Help-pagina Patroondetectiecode
translation-type: tm+mt
source-git-commit: aa44c3ce87496f412191000f1980a7ebbde386cd
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 0%

---


# [!DNL FORMS] {#form}

[!DNL Adobe Experience Manager Forms]

## Achtergrond {#background}

`FORMS` Hiermee worden mogelijke problemen met betrekking tot migratie van  [!DNL Adobe Experience Manager Forms] naar  [!DNL Adobe Experience Manager Form]s aangegeven als een  [!DNL Cloud Service]. Deze problemen verhelpen voordat u naar [!DNL Cloud Service] migreert.

De volgende subtypes helpen u de verschillende soorten kwesties identificeren:

* `modified.feature`: Deze functies, elementen of API&#39;s zijn bijgewerkt of gewijzigd voor Cloud Service. Voordat u naar de Cloud Service gaat, voert u het migratiehulpprogramma uit om deze functies en elementen compatibel te maken met de Cloud Service.
* `unavailable.feature`: Uw omgeving heeft functies en elementen die niet beschikbaar zijn of uit de Cloud Service zijn verwijderd. Migreer dergelijke functies of middelen niet naar een Cloud Service-omgeving.
* `unsupported.feature`: Uw omgeving gebruikt enkele functies die op de Cloud Service nog niet worden ondersteund. Migreer dergelijke functies of middelen niet naar een Cloud Service-omgeving. Houd de maandelijkse opmerkingen bij de release in de gaten voor de beschikbaarheid van de functies.
* `unsupported.api`: Uw omgeving heeft enkele API&#39;s die nog niet worden ondersteund op de Cloud Service. Voordat u naar de Cloud Service gaat, schakelt u deze API&#39;s uit, vervangt of verwijdert u ze uit de code. Houd de maandelijkse opmerkingen bij de release in de gaten voor de beschikbaarheid van de functies.

Zie de [Mogelijke implicaties en risico&#39;s](#implications-and-risks) en [Mogelijke oplossingen](#solutions) secties voor informatie over vervangingen en andere acties die worden vereist om sommige eigenschappen en APIs met de Cloud Service compatibel te maken

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

Beantwoord de volgende problemen voordat u naar [!DNL Adobe Experience Manager Forms as a Cloud Service] migreert. Wanneer de hieronder vermelde implicaties en risico&#39;s niet worden aangepakt, functioneren sommige eigenschappen niet zoals verwacht in het milieu van de Cloud Service.

* De functionaliteit van de coderedacteur van de eigenschap van de regelredacteur is niet beschikbaar. (CODE_EDITOR)

* E-mailondersteuning (SMTP-poort) is standaard uitgeschakeld. (EMAIL_SERVICE_CONFIGURATION)

* De handeling **[!UICONTROL Email PDF]** Verzenden is niet beschikbaar.(EMAIL_PDF_SUBMIT_ACTION)

* Adaptieve Forms op basis van XFA worden nog niet ondersteund. (XFA_BASED_FORM, XDP_BASED_FORM)

* Een handeling Verzenden wordt direct aangeroepen bij het verzenden van een formulier in plaats van te wachten tot alle ondertekenaars de ondertekening hebben voltooid. Het PDF-bestand van de Adobe Sign-overeenkomst dat naar ondertekenaars is verzonden, kan dus niet worden gebruikt of verwerkt door Handelingen verzenden. (FORM_SIGN_INTEGRATION)

* De stap Handtekening is niet beschikbaar. (SIGNATURE_STEP)

* De stap Verifiëren is niet beschikbaar. (VERIFY_STEP)

* De Forms Portal-functie en **[!UICONTROL Forms Portal Submit Action]** zijn nog niet beschikbaar. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL, DRAFT_AUTO_SAVE, DRAFT_SAVE)

* De handeling **[!UICONTROL Submit to Forms Workflow]** Verzenden is niet beschikbaar. Op [!DNL AEM 6.5 Forms] en eerdere versies is de handeling Verzenden gebruikt om aangepaste formuliergegevens te verzenden naar verouderde [!DNL AEM Forms on JEE] Workflows en LiveCycle Workflow. (LC_WORKFLOW_SUBMISSION)

* Het Interactieve Communicatie vermogen is niet beschikbaar.  (FP_PROFILE_INTERACTIVE_COMMUNICATIONS).

* **[!UICONTROL Save as draft]** en  **[!UICONTROL Auto Save]** een adaptieve formulierfunctie worden momenteel niet ondersteund. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* Metagegevensaccordeon is niet beschikbaar. (METADATA_ACCORDION_FORM_CONTAINER)

* De component CAPTCHA gebruikt nu de Google reCAPTCHA-service om CAPTCHA standaard te valideren. De optie voor het valideren van CAPTCHA met Adobe Experience Manager is afgekeurd. (FORMS_CAPTCHA)

* [!DNL AEM Forms] is niet beschikbaar voor  [!DNL Cloud Services]. (AEM_FORMS_APP)

* [Documentservices ](https://experienceleague.adobe.com/docs/experience-manager-65/forms/install-aem-forms/osgi-installation/install-configure-document-services.html?lang=en#deployment-topology) zijn niet beschikbaar in AEM Workflows. (WORKFLOW_DOCSERVICES)

## Mogelijke oplossingen {#solutions}

* Gebruik het migratiehulpprogramma om alle regelscripts in uw omgeving om te zetten in herbruikbare functies. U kunt de herbruikbare functies met de Visuele redacteur van de Regel gebruiken om resultaten te blijven verkrijgen die met regelmanuscripten worden verkregen. (CODE_EDITOR)

* Neem contact op met het ondersteuningsteam om de functionaliteit voor e-mail (open SMTP-poort) voor uw omgeving in te schakelen. Standaard zijn alleen uitgaande HTTP- en HTTPS-verbindingen ingeschakeld. (E-MAIL_SERVICE_CONFIGURATION, stap E-mail)

* Gebruik **[!UICONTROL Email]** Handeling verzenden in plaats van **[!UICONTROL Email PDF]**. De **[!UICONTROL Email]** Handeling verzenden biedt opties voor het verzenden van bijlagen en het toevoegen van Document of Record (DoR) bij e-mail. (EMAIL_PDF_SUBMIT_ACTION)

* Verzonden gegevens bevatten Adobe Sign-overeenkomst-id. U kunt de id van de Overeenkomst ondertekenen gebruiken om een PDF van de Overeenkomst van het Ondertekenen terug te winnen, indien vereist.  (FORM_SIGN_INTEGRATION)

* Verwijder de stap Handtekening uit een bestaand adaptief formulier. Configureer uw adaptieve formulier voor het gebruik van [ondertekeningservaring in de browser](https://medium.com/adobetech/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). De Adobe Sign-overeenkomst wordt weergegeven om de overeenkomst in de browser te ondertekenen wanneer een adaptief formulier wordt verzonden. Ondertekeningservaring in de browser helpt de ondertekenaar sneller te ondertekenen en bespaart tijd. (SIGNATURE_STEP)

* Verwijder de stap Verifiëren uit uw bestaande Adaptieve Forms voordat u dergelijke formulieren naar een [!DNL Cloud Service]-omgeving verplaatst. (VERIFY_STEP)

* Wijzig uw bestaande adaptieve formulieren om [Verzenden naar REST-eindpunt](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#submit-to-rest-endpoint), [E-mail verzenden](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#send-email), [Verzenden met gebruik van formuliergegevensmodel](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#submit-using-form-data-model) en [Een AEM workflow aanroepen](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#invoke-an-aem-workflow) Handelingen verzenden. Forms Portal en Forms Portal verzenden Actie zijn nog niet beschikbaar. Houd de maandelijkse opmerkingen bij de release in de gaten voor de beschikbaarheid van de functies. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL)

* U kunt een AEM-workflow ontwikkelen en uw bestaande adaptieve formulieren aanpassen om [AEM Workflow](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#invoke-an-aem-workflow) Actie verzenden te gebruiken om gegevens naar een AEM-workflow te verzenden in plaats van de **[!UICONTROL Submit to Forms Workflow]** Handeling verzenden te gebruiken. U kunt een aangepaste handeling Verzenden ontwikkelen om gegevens, bijlagen of Document of Record (DoR) naar een LiveCycle-proces te verzenden in plaats van de [!UICONTROL Submit to Forms Workflow] te gebruiken. (LC_WORKFLOW_SUBMISSION)

* Houd een oog op maandelijkse versienota&#39;s voor de beschikbaarheid van de Interactieve eigenschap van Mededelingen. Migreer uw Interactieve Mededelingen, Brieven, en verwante Woordenboeken niet aan een milieu van de Cloud Service tot de eigenschap niet beschikbaar is. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* Schakel de opties **[!UICONTROL Save as draft]** en **[!UICONTROL Enable Auto Save]** in uw adaptieve Forms uit voordat u deze naar de Cloud Service migreert. U kunt deze opties inschakelen zodra de Forms Portal-functie voor de Cloud Service wordt vrijgegeven. Houd de maandelijkse opmerkingen bij de release in de gaten voor de beschikbaarheid van de functies. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* Er is geen vervanging voor metagegevensaccordeon. Verwijder het bestand uit uw formulieren voordat u het naar de Cloud Service verplaatst.(METADATA_ACCORDION_FORM_CONTAINER)

* Gebruik Google reCaptcha in plaats van de CAPTCHA-service die door Adobe Experience Manager wordt aangeboden. (FORMS_CAPTCHA)

* Adaptive Forms biedt een responsief ontwerp. Deze formulieren wijzigen de weergave, het ontwerp en de interactiviteit op basis van het onderliggende apparaat. U kunt Adaptive Forms blijven gebruiken op een mobiel apparaat terwijl u de maandelijkse releaseopmerkingen bijhoudt voor de beschikbaarheid van de [!DNL AEM Forms]-app. (AEM_FORMS_APP)

* Migreer geen model van het Werkschema van AEM die een stap van het Werkschema van de Diensten van het Document gebruikt. Migreer of werk geen Adaptieve Forms bij die gebruikersgegevens naar een Werkstroommodel verzendt dat de stappen van het Werkschema van de Diensten van het Document gebruikt of verander de Submit Actie in [gesteunde één](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html) alvorens de vorm te migreren. (WORKFLOW_DOCSERVICES)

* Ondersteuning voor adaptieve Forms op basis van XFA is niet beschikbaar in de verpakking. Als u van plan bent om op XFA-Gebaseerde AanpassingsForms te gebruiken, contacteer de Steun van de Adobe met details van uw gebruiksgeval en specifieke vereisten.(XFA_BASED_FORM, XDP_BASED_FORM)

Bereik uit aan [Adobe Steun](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om ongerustheid te richten.
