---
title: Forms
description: Help-pagina Patroondetectiecode
translation-type: tm+mt
source-git-commit: a6ba6e93c89644160650882ecbf17028bec35068
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 0%

---


# [!DNL FORMS] {#forms}

[!DNL Adobe Experience Manager Forms]

## Achtergrond {#background}

`FORMS` wijst potentiële problemen met betrekking tot migratie van Adobe Experience Manager Forms naar Adobe Experience Manager Forms als Cloud Service aan. Deze problemen verhelpen voordat u naar de Cloud Service migreert.

De volgende subtypes helpen u de verschillende soorten kwesties identificeren:

* `modified.feature`: Deze functies, elementen of API&#39;s zijn bijgewerkt of gewijzigd voor Cloud Service. Voordat u naar de Cloud Service gaat, voert u het migratiehulpprogramma uit om deze functies en elementen compatibel te maken met de Cloud Service.
* `unavailable.feature`: Uw omgeving heeft functies en elementen die niet beschikbaar zijn of uit de Cloud Service zijn verwijderd. Migreer dergelijke functies of middelen niet naar een Cloud Service-omgeving.
* `unsupported.feature`: Uw omgeving gebruikt enkele functies die op de Cloud Service nog niet worden ondersteund. Migreer dergelijke functies of middelen niet naar een Cloud Service-omgeving. Houd de maandelijkse opmerkingen bij de release in de gaten voor de beschikbaarheid van de functies.
* `unsupported.api`: Uw omgeving heeft enkele API&#39;s die nog niet worden ondersteund op de Cloud Service. Voordat u naar de Cloud Service gaat, schakelt u deze API&#39;s uit, vervangt of verwijdert u ze uit de code. Houd de maandelijkse opmerkingen bij de release in de gaten voor de beschikbaarheid van de functies.

Zie de [Mogelijke implicaties en risico&#39;s](#implications-and-risks) en [Mogelijke oplossingen](#solutions) secties voor informatie over vervangingen en andere acties die worden vereist om sommige eigenschappen en APIs met de Cloud Service compatibel te maken

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

Neem de volgende problemen op voordat u als Cloud Service naar Adobe Experience Manager Forms migreert. Wanneer de hieronder vermelde implicaties en risico&#39;s niet worden aangepakt, functioneren sommige eigenschappen niet zoals verwacht in het milieu van de Cloud Service.

* De functionaliteit van de coderedacteur van de eigenschap van de regelredacteur is niet beschikbaar. (CODE_EDITOR)

* E-mailondersteuning (SMTP-poort) is standaard uitgeschakeld. (EMAIL_SERVICE_CONFIGURATION)

* De verzendactie **[!UICONTROL Email PDF]** is niet beschikbaar.(EMAIL_PDF_SUBMIT_ACTION)

* Aangepaste XDP-formulieren worden nog niet ondersteund. (XDP_BASED_FORM)

* Een verzendactie wordt direct aangeroepen bij het verzenden van een formulier in plaats van te wachten tot alle ondertekenaars de ondertekening hebben voltooid. Het adaptieve document met een formulierhandtekening (PDF-overeenkomst van Adobe Sign verzonden naar ondertekenaars) is dus niet beschikbaar voor het verzenden van handelingen voor gebruik of verwerking. (FORM_SIGN_INTEGRATION)

* De stap Handtekening is niet beschikbaar. (SIGNATURE_STEP)

* De stap Verifiëren is niet beschikbaar. (VERIFY_STEP)

* De Forms Portal-functie en **[!UICONTROL Forms Portal submit action]** zijn niet beschikbaar. Met Forms Portal kunt u geen formulieren weergeven, concepten opslaan of verzonden formulieren weergeven. U kunt geen gegevens verzenden (gebruik **[!UICONTROL Forms Portal submit action]**) die naar een adaptief formulier zijn verzonden naar een Forms Portal. [!UICONTROL Save as draft] en  [!UICONTROL Auto Save] een adaptieve formulierfunctie worden momenteel niet ondersteund. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL, DRAFT_AUTO_SAVE, DRAFT_SAVE)

* De verzendactie **[!UICONTROL Submit to Forms workflow]** is niet beschikbaar. Op AEM 6.5 Forms en eerdere versies werd de verzendactie gebruikt om adaptieve formuliergegevens naar verouderde AEM Forms te verzenden over JEE Workflows en LiveCycle Workflow. (LC_WORKFLOW_SUBMISSION)

* Het Interactieve Communicatie vermogen is niet beschikbaar.  (FP_PROFILE_INTERACTIVE_COMMUNICATIONS).

* **[!UICONTROL Save as draft]** en  **[!UICONTROL Auto Save]** een adaptieve formulierfunctie worden momenteel niet ondersteund. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* Metagegevensaccordeon is niet beschikbaar. (METADATA_ACCORDION_FORM_CONTAINER)

* De component CAPTCHA gebruikt nu de Google reCAPTCHA-service om CAPTCHA standaard te valideren. De optie voor het valideren van CAPTCHA met Adobe Experience Manager is niet beschikbaar. (FORMS_CAPTCHA)

## Mogelijke oplossingen {#solutions}

* Gebruik het migratiehulpprogramma om alle regelscripts in uw omgeving om te zetten in herbruikbare functies. U kunt de herbruikbare functies met de Visuele redacteur van de Regel gebruiken om resultaten te blijven verkrijgen die met regelmanuscripten worden verkregen. (CODE_EDITOR)

* Neem contact op met het ondersteuningsteam om de functionaliteit voor e-mail (open SMTP-poort) voor uw omgeving in te schakelen. Standaard zijn alleen uitgaande HTTP- en HTTPS-verbindingen ingeschakeld. (EMAIL_SERVICE_CONFIGURATION)

* Gebruik **[!UICONTROL Email]** verzendt actie in plaats van **[!UICONTROL Email PDF]**. De verzendactie **[!UICONTROL Email]** biedt opties om bijlagen te verzenden en Document of Record (DoR) bij e-mail te voegen. (EMAIL_PDF_SUBMIT_ACTION)

* Migreer adaptieve formulieren op basis van XDP niet naar een Cloud Service-omgeving. Houd de maandelijkse opmerkingen bij de release in de gaten voor de beschikbaarheid van de functies. (XDP_BASED_FORM)

* Verzonden gegevens bevatten ondertekeningsovereenkomst-id. U kunt de id van de Overeenkomst ondertekenen gebruiken om een PDF van de Overeenkomst van het Ondertekenen terug te winnen, indien vereist.  (FORM_SIGN_INTEGRATION)

* Vervang de stap Handtekening in uw aangepaste formulieren door de optie om een aangepast formulier na verzending te ondertekenen in hetzelfde venster. Hiermee kunt u een [ondertekeningservaring in de browser](https://medium.com/adobetech/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684) blijven bieden. (SIGNATURE_STEP)

* Verwijder de stap Verifiëren uit uw bestaande adaptieve formulieren voordat u deze naar een Cloud Service-omgeving verplaatst. (VERIFY_STEP)

* Er is geen alternatief voor **[!UICONTROL Forms Portal submit action]**. U kunt deze verzendactie gebruiken als de Forms Portal-functie voor de Cloud Service is uitgebracht. Houd de maandelijkse opmerkingen bij de release in de gaten voor de beschikbaarheid van de functies. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL)

* Er is geen alternatieve verzendactie om acties te verzenden **[!UICONTROL Submit to Forms workflow]**. U kunt een aangepaste verzendactie ontwikkelen om gegevens, bijlagen of Document of Record (DoR) naar een LiveCycle-proces te verzenden. (LC_WORKFLOW_SUBMISSION)

* Migreer uw Interactieve Mededelingen, Brieven, en verwante Woordenboeken niet aan een milieu van de Cloud Service. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* Schakel de opties **[!UICONTROL Save as draft]** en **[!UICONTROL Enable Auto Save]** in de aangepaste formulieren uit voordat u deze naar de Cloud Service verplaatst. U kunt deze opties inschakelen zodra de Forms Portal-functie voor de Cloud Service wordt vrijgegeven. Houd de maandelijkse opmerkingen bij de release in de gaten voor de beschikbaarheid van de functies. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* Er is geen vervanging voor metagegevensaccordeon. Verwijder het bestand uit uw formulieren voordat u het naar de Cloud Service verplaatst.(METADATA_ACCORDION_FORM_CONTAINER)

* Gebruik Google reCaptcha in plaats van de CAPTCHA-service die door Adobe Experience Manager wordt aangeboden. (FORMS_CAPTCHA)

Bereik uit aan [Adobe Steun](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om ongerustheid te richten.
