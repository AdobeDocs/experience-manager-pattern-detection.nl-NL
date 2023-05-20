---
title: INST
description: Help-pagina Patroondetectiecode
exl-id: 9b8129d7-63d7-4975-a68b-9ba704d01532
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# INST {#inst}

Geïnstalleerd artefact

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_overview"
>title="Geïnstalleerd artefact"
>abstract="INST identificeert aangepaste pakketten en bundels van derden die door de klant in AEM zijn geïnstalleerd. Deze worden gerapporteerd om de status van het systeem te beschrijven in het algemene bereik van een upgrade-inspanning. Elk pakket van derden moet voldoen aan de AEM richtsnoeren voor as a Cloud Service ontwikkeling en verpakking."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html" text="Ontwikkelingsrichtsnoeren - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html" text="Richtlijnen voor verpakking - AEM as a Cloud Service"

`INST` identificeert aangepaste pakketten en bundels van derden die in AEM door de klant zijn geïnstalleerd. Deze worden gerapporteerd om de status van het systeem te beschrijven in het algemene bereik van een upgrade-inspanning.

Wanneer meerdere versies van een pakket zijn geïnstalleerd, wordt alleen de laatste versie gerapporteerd.

Pakketten en bundels die worden gedetecteerd, zijn niet noodzakelijkerwijs geoptimaliseerd voor AEM as a Cloud Service. Elk pakket van derden moet met de maker of de Adobe worden gecontroleerd op compatibiliteit met AEM as a Cloud Service.

Subtypes worden gebruikt om verschillende soorten informatie te identificeren:

* `custom.bundle`: Een bundel die in AEM is geïnstalleerd.
* `custom.package`: Een pakket dat is geïnstalleerd in AEM.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_guidance"
>title="Implementatieleiding"
>abstract="Klanten kunnen geen pakketten van derden meer installeren met behulp van CRX Package Manager. Klanten moeten deze geïnstalleerde artefacten controleren en ze moeten een structuur hebben en optimaliseren om met AEM as a Cloud Service te kunnen werken. Elk pakket van derden moet met de maker of de Adobe worden gecontroleerd op compatibiliteit met AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#embeddeds" text="Subpakketten insluiten in het Containerpakket"


* Installatie van pakketten van derden met behulp van CRX Package Manager is niet mogelijk in AEM as a Cloud Service.
* Toepassingen die van pakketten van derden afhankelijk zijn, werken mogelijk pas zoals verwacht wanneer deze correct worden geïmplementeerd om met AEM as a Cloud Service te werken.
* Pakketten van andere leveranciers, die niet zijn geoptimaliseerd voor AEM als cloudservice, kunnen leiden tot ongewenste functionaliteit.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_tools"
>title="Hulpmiddelen &amp; Middelen"
>abstract="Bekijk het WKND-verouderde project om te begrijpen hoe INST-schendingen compatibel kunnen worden gemaakt met AEM Cloud Service. Lees ook het voorbeeld van INST Violation op Github om te begrijpen hoe dit kan worden gecorrigeerd en geïmplementeerd in AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst" text="WKND-verouderd project"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst" text="Voorbeeld van INST-schending - Github"

* Pakketten van derden dienen te worden geïmplementeerd op AEM als onderdeel van het project met gebruik van Cloud Manager [implementatieproces](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/using-cloud-manager/deploy-code.html#deployment-process).
* Controleren hoe [pakketten van derden insluiten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#embedding-3rd-party-packages) in uw project voor AEM as a Cloud Service.
* Pakketten van derden moeten voldoen aan de AEM as a Cloud Service [ontwikkeling](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html) en [verpakking](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html) richtsnoeren.
* Controleren [verouderd](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) projecten en begrijpen hoe [INST-overtredingen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) kan worden gecorrigeerd en verenigbaar worden gemaakt met AEM as a Cloud Service.
* Neem contact op met onze [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
