---
title: INST
description: Help-pagina Patroondetectiecode
exl-id: 9b8129d7-63d7-4975-a68b-9ba704d01532
translation-type: tm+mt
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
>abstract="INST identificeert aangepaste pakketten en bundels van derden die door de klant in AEM zijn geïnstalleerd. Deze worden gerapporteerd om de status van het systeem te beschrijven in het algemene bereik van een upgrade-inspanning. Elk pakket van derden moet zich aan de AEM houden als richtsnoeren voor de ontwikkeling en verpakking van Cloud Servicen."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html" text="Ontwikkelingsrichtsnoeren - AEM als Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html" text="Richtlijnen voor verpakking - AEM als Cloud Service"

`INST` identificeert aangepaste pakketten en bundels van derden die in AEM door de klant zijn geïnstalleerd. Deze worden gerapporteerd om de status van het systeem te beschrijven in het algemene bereik van een upgrade-inspanning.

Wanneer meerdere versies van een pakket zijn geïnstalleerd, wordt alleen de laatste versie gerapporteerd.

Pakketten en bundels die worden gedetecteerd, zijn niet noodzakelijkerwijs geoptimaliseerd voor AEM als Cloud Service. Elk pakket van derden moet met de maker of de Adobe worden gecontroleerd op compatibiliteit met AEM als Cloud Service.

Subtypes worden gebruikt om verschillende soorten informatie te identificeren:

* `custom.bundle`: Een bundel die in AEM is geïnstalleerd.
* `custom.package`: Een pakket dat is geïnstalleerd in AEM.

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_guidance"
>title="Implementatieleiding"
>abstract="Klanten kunnen geen pakketten van derden meer installeren met behulp van CRX Package Manager. Klanten moeten deze geïnstalleerde artefacten controleren en ze moeten een structuur hebben en optimaliseren om met AEM als Cloud Service te werken. Elk pakket van derden moet met de maker of de Adobe worden gecontroleerd op compatibiliteit met AEM als Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#embeddeds" text="Subpakketten insluiten in het Containerpakket"


* Installatie van pakketten van derden met behulp van CRX Package Manager is niet mogelijk in AEM als Cloud Service.
* Toepassingen die van pakketten van derden afhankelijk zijn, werken mogelijk pas zoals verwacht wanneer deze correct worden geïmplementeerd om als Cloud Service met AEM te werken.
* Pakketten van andere leveranciers, die niet zijn geoptimaliseerd voor AEM als cloudservice, kunnen leiden tot ongewenste functionaliteit.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_tools"
>title="Hulpmiddelen &amp; Middelen"
>abstract="Het WKND-erfenisproject van het overzicht om te begrijpen hoe de schendingen van INST met AEM Cloud Service compatibel kunnen worden gemaakt. Lees ook het voorbeeld van INST Violation op Github om te begrijpen hoe dit kan worden gecorrigeerd en geïmplementeerd in AEM als Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst" text="WKND-verouderd project"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst" text="Voorbeeld van INST-schending - Github"

* Pakketten van derden moeten worden geïmplementeerd om als onderdeel van het project te worden AEM met behulp van het implementatieproces [van Cloud Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/using-cloud-manager/deploy-code.html#deployment-process).
* Bekijk hoe u pakketten van derden](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#embedding-3rd-party-packages) voor AEM als Cloud Service kunt insluiten in uw project.[
* Pakketten van derden moeten zich aan de AEM houden als een Cloud Service [development](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html) en [packaging](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html) richtlijnen.
* Bekijk het [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst)-project en begrijp hoe [INST-schendingen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) kunnen worden gecorrigeerd en compatibel kunnen worden gemaakt met AEM als Cloud Service.
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
