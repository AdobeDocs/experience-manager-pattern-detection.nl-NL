---
title: FORM
description: Help-pagina Patroondetectiecode.
exl-id: ac28760b-b0ab-4082-b7ce-730cddc4ad83
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '968'
ht-degree: 0%

---

# [!DNL FORMS] {#form}

[!DNL Adobe Experience Manager Forms]

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_overview"
>title="FORMS"
>abstract="De Forms-code identificeert mogelijke problemen met betrekking tot migratie van AEM (Adobe Experience Manager) Forms naar AEM Forms as a Cloud Service. Bekijk de mogelijke implicaties en risico&#39;s die aan deze problemen zijn verbonden en bespreek deze voordat u naar de Cloud Service gaat."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-pattern-detection/table-of-contents/forms#implications-and-risks" text="Mogelijke gevolgen en risico&#39;s"

`FORMS` Hiermee worden mogelijke problemen met betrekking tot migratie van [!DNL Adobe Experience Manager Forms] naar [!DNL Adobe Experience Manager Forms] aangegeven als een [!DNL Cloud Service] . Los deze problemen op voordat u naar [!DNL Cloud Service] migreert.

De volgende subtypes helpen u de verschillende soorten kwesties identificeren:

* `modified.feature`: Deze functies, elementen of API&#39;s zijn bijgewerkt of gewijzigd voor Cloud Service. Voordat u naar de Cloud Service gaat, voert u het migratiehulpprogramma uit om deze functies en elementen compatibel te maken met de Cloud Service.
* `unavailable.feature`: Uw omgeving bevat functies en elementen die niet beschikbaar zijn of uit de Cloud Service zijn verwijderd. Migreer dergelijke functies of middelen niet naar een Cloud Service-omgeving.
* `unsupported.feature`: uw omgeving gebruikt enkele functies die op de Cloud Service nog niet worden ondersteund. Migreer dergelijke functies of middelen niet naar een Cloud Service-omgeving. Raadpleeg de maandelijkse releaseopmerkingen voor informatie over de beschikbaarheid van de functies.
* `unsupported.api`: Uw omgeving heeft enkele API&#39;s die nog niet worden ondersteund op de Cloud Service. Voordat u naar de Cloud Service gaat, schakelt u deze API&#39;s uit, vervangt of verwijdert u ze uit de code. Raadpleeg de maandelijkse releaseopmerkingen voor informatie over de beschikbaarheid van de functies.

Zie [ Mogelijke implicaties en risico&#39;s ](#implications-and-risks) en [ Mogelijke oplossingen ](#solutions) secties voor informatie over vervangingen en andere acties die worden vereist om sommige eigenschappen en APIs compatibel te maken met de Cloud Service

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

Beantwoord de volgende problemen voordat u gaat migreren naar [!DNL Adobe Experience Manager Forms as a Cloud Service] . Wanneer de hieronder vermelde implicaties en risico&#39;s niet worden aangepakt, functioneren sommige eigenschappen niet zoals verwacht in het milieu van de Cloud Service.

* De functionaliteit van de coderedacteur van de eigenschap van de regelredacteur is niet beschikbaar. (CODE_EDITOR)

* E-mailondersteuning (SMTP-poort) is standaard uitgeschakeld. (EMAIL_SERVICE_CONFIGURATION)

* De handeling **[!UICONTROL Email PDF]** Verzenden is niet beschikbaar. (EMAIL_PDF_SUBMIT_ACTION)

* Adaptieve Forms op basis van XFA worden nog niet ondersteund. (XFA_BASED_FORM, XDP_BASED_FORM)

* Een handeling Verzenden wordt direct aangeroepen bij het verzenden van een formulier in plaats van te wachten tot alle ondertekenaars de ondertekening hebben voltooid. De PDF van de Adobe Sign-overeenkomst die naar ondertekenaars is verzonden, kan dus niet worden gebruikt of verwerkt door Handelingen verzenden. (FORM_SIGN_INTEGRATION)

* De stap Handtekening is niet beschikbaar. (SIGNATURE_STEP)

* De stap Verifiëren is niet beschikbaar. (VERIFY_STEP)

* De handeling **[!UICONTROL Submit to Forms Workflow]** Verzenden is niet beschikbaar. Op AEM 6.5 Forms en eerdere versies werd de handeling Verzenden gebruikt om adaptieve formuliergegevens naar verouderde AEM Forms te verzenden over JEE Workflows en LiveCycle Workflows. (LC_WORKFLOW_SUBMISSION)

* Het Interactieve Communicatie vermogen is niet beschikbaar. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS).

* Metagegevensaccordeon is niet beschikbaar. (METADATA_ACCORDION_FORM_CONTAINER)

* De component CAPTCHA gebruikt nu de Google reCAPTCHA-service om CAPTCHA standaard te valideren. De optie voor het valideren van CAPTCHA met Adobe Experience Manager is afgekeurd. (FORMS_CAPTCHA)

* [!DNL AEM Forms] is niet beschikbaar voor [!DNL Cloud Services] . (AEM_FORMS_APP)

* {de diensten van het 0} Document ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/forms/install-aem-forms/osgi-installation/install-configure-document-services#deployment-topology) stappen zijn niet beschikbaar in AEM Werkschema&#39;s. [ (WORKFLOW_DOCSERVICES)

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_guidance"
>title="Implementatieleiding"
>abstract="Informatie die via FORMS-code wordt weergegeven, kan u helpen bij vervangingen en andere acties die nodig zijn om bepaalde functies en API&#39;s compatibel te maken met de Cloud Service. Neem contact op met de ondersteuning van de Adobe voor hulp of verduidelijking."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Gebruik een migratiehulpprogramma om alle regelscripts in uw omgeving om te zetten in herbruikbare functies. U kunt de herbruikbare functies met de Visuele Redacteur van de Regel gebruiken om resultaten te blijven verkrijgen die met regelmanuscripten worden verkregen. (CODE_EDITOR)

* Neem contact op met het ondersteuningsteam zodat u de e-mailfunctionaliteit kunt inschakelen (open SMTP-poort) voor uw omgeving. Alleen uitgaande HTTP- en HTTPS-verbindingen zijn standaard ingeschakeld. (E-MAIL_SERVICE_CONFIGURATION, stap E-mail)

* Gebruik **[!UICONTROL Email]** Handeling verzenden in plaats van **[!UICONTROL Email PDF]** . De handeling **[!UICONTROL Email]** Verzenden bevat opties voor het verzenden van bijlagen en het toevoegen van Document of Record (DoR) met e-mail. (EMAIL_PDF_SUBMIT_ACTION)

* Verzonden gegevens bevatten Adobe Sign-overeenkomst-id. U kunt de id van de Overeenkomst van het Ondertekenen gebruiken om een PDF van de Overeenkomst van het Ondertekenen terug te winnen, indien nodig. (FORM_SIGN_INTEGRATION)

* Verwijder de stap Handtekening uit een bestaand adaptief formulier. Vorm uw Aangepaste Vorm om een [ in-browser ondertekenende ervaring ](https://blog.developer.adobe.com/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684) te gebruiken. Er wordt Adobe Sign-overeenkomst weergegeven om de overeenkomst in de browser te ondertekenen wanneer een adaptief formulier wordt verzonden. Ondertekeningservaring in de browser helpt de ondertekenaar sneller te ondertekenen en bespaart tijd. (SIGNATURE_STEP)

* Verwijder de verificatiestap uit de bestaande Adaptive Forms voordat u dergelijke formulieren naar een [!DNL Cloud Service] -omgeving verplaatst. (VERIFY_STEP)

* Bewerk uw bestaande adaptieve vormen zodat kunt u [ gebruiken voorleggen aan REST eindpunt ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#submit-to-rest-endpoint), [ verzendt e-mail ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#send-email), [ voorlegt gebruikend het Model van Gegevens van de Vorm ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#submit-using-form-data-model), en [ roept een AEM Werkschema ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#invoke-an-aem-workflow) op Voorlegt Acties.

* U kunt een AEM Werkschema ontwikkelen en uw bestaande adaptieve vormen uitgeven om [ AEM van het Werkschema ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#invoke-an-aem-workflow) te gebruiken verzendt Actie om gegevens naar een AEM Werkschema in plaats van het gebruiken van **[!UICONTROL Submit to Forms Workflow]** te verzenden Actie. U kunt een aangepaste handeling Verzenden ontwikkelen om gegevens, bijlagen of Document of Record (DoR) naar een LiveCycle-proces te verzenden in plaats van [!UICONTROL Submit to Forms Workflow] te gebruiken. (LC_WORKFLOW_SUBMISSION)

* Zoek maandelijkse versienota&#39;s voor informatie over beschikbaarheid van de Interactieve eigenschap van Mededelingen. Migreer uw Interactieve Mededelingen, Brieven, en verwante Woordenboeken niet aan een milieu van de Cloud Service tot de eigenschap niet beschikbaar is. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* Er is geen vervanging voor metagegevensaccordeon. Verwijder het bestand uit uw formulieren voordat u het naar de Cloud Service migreert.(METADATA_ACCORDION_FORM_CONTAINER)

* Gebruik de Google reCAPTCHA in plaats van de CAPTCHA-service van Adobe Experience Manager. (FORMS_CAPTCHA)

* Migreer niet naar een AEM workflowmodel dat gebruikmaakt van een workflowstap voor documentservices. Ook, migreer of werk geen Adaptieve Forms bij die gebruikersgegevens naar een Model van het Werkschema verzenden dat de stappen van het Werkschema van de documentdiensten gebruikt of **`Submit Action`** aan a [ gesteunde ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions) alvorens de vorm te migreren. (WORKFLOW_DOCSERVICES)

* Adaptive Forms biedt een responsief ontwerp. Deze formulieren wijzigen de weergave, het ontwerp en de interactiviteit op basis van het onderliggende apparaat. U kunt Adaptive Forms blijven gebruiken op een mobiel apparaat. Raadpleeg de maandelijkse releaseopmerkingen voor informatie over de beschikbaarheid van de app [!DNL AEM Forms] . (AEM_FORMS_APP)

* Ondersteuning voor adaptieve Forms op basis van XFA is niet beschikbaar in de verpakking. Als u van plan bent om op XFA-Gebaseerde Aangepaste Forms te gebruiken, contacteer de Steun van de Adobe met details van uw gebruiksgeval en specifieke vereisten.(XFA_BASED_FORM, XDP_BASED_FORM)

Contacteer [ de Steun van de Adobe ](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) als u behandelde verduidelijkingen of bekommernissen nodig hebt.
