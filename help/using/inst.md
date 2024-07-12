---
title: INST
description: Help-pagina Patroondetectiecode.
exl-id: 9b8129d7-63d7-4975-a68b-9ba704d01532
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 0%

---

# INST {#inst}

Geïnstalleerd artefact

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_overview"
>title="Geïnstalleerd artefact"
>abstract="INST identificeert aangepaste pakketten en bundels van derden die in AEM door de klant zijn geïnstalleerd. Dergelijke pakketten en bundels worden gerapporteerd om de toestand van het systeem en het algemene bereik van een upgrade-inspanning te helpen karakteriseren. Elk pakket van derden moet voldoen aan de AEM as a Cloud Service-richtlijnen voor ontwikkeling en verpakking."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="Ontwikkelingsrichtsnoeren - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/repository-structure-package" text="Richtlijnen voor verpakking - AEM as a Cloud Service"

`INST` Identificeert aangepaste pakketten en bundels van derden die door de klant in AEM zijn geïnstalleerd. Dergelijke pakketten en bundels worden gerapporteerd om de toestand van het systeem en het algemene bereik van een upgrade-inspanning te helpen karakteriseren.

Wanneer meerdere versies van een pakket zijn geïnstalleerd, wordt alleen de laatste versie gerapporteerd.

Pakketten en bundels die worden gedetecteerd, zijn niet noodzakelijkerwijs geoptimaliseerd voor AEM as a Cloud Service. Elk pakket van derden moet met de maker of Adobe ervan worden gecontroleerd op compatibiliteit met AEM as a Cloud Service.

Subtypes worden gebruikt om verschillende soorten informatie te identificeren:

* `custom.bundle`: Een bundel die is geïnstalleerd in AEM.
* `custom.package`: Een pakket dat is geïnstalleerd in AEM.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_guidance"
>title="Implementatieleiding"
>abstract="Klanten kunnen geen pakketten van derden meer installeren met CRX Package Manager. Klanten moeten deze geïnstalleerde artefacten die moeten worden gestructureerd, controleren en optimaliseren om met AEM as a Cloud Service te werken. Verifieer om het even welk derspakket met of zijn schepper of met Adobe voor verenigbaarheid met AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#embeddeds" text="Subpakketten insluiten in het Containerpakket"


* Installatie van pakketten van derden met CRX Package Manager is niet mogelijk in AEM as a Cloud Service.
* Toepassingen die van pakketten van derden afhankelijk zijn, werken mogelijk pas zoals verwacht als ze op de juiste wijze zijn geïmplementeerd om met AEM as a Cloud Service te werken.
* Pakketten van andere leveranciers, die niet zijn geoptimaliseerd voor AEM als cloudservice, kunnen leiden tot ongewenste functionaliteit.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_tools"
>title="Hulpmiddelen en Middelen"
>abstract="Bekijk het WKND-verouderde project om te begrijpen hoe INST-schendingen compatibel kunnen worden gemaakt met AEM Cloud Service. Lees ook het INST Violation Example op GitHub om te begrijpen hoe deze kwestie kan worden gecorrigeerd en geïmplementeerd in AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst" text="WKND-verouderd project"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst" text="Voorbeeld van INST-schending - GitHub"

* De pakketten van de derde zouden aan AEM als deel van het project moeten worden opgesteld gebruikend het Cloud Manager [ plaatsingsproces ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deployment-process).
* Herzie hoe te om [ derdepakketten ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#embedding-3rd-party-packages) in uw project voor AEM as a Cloud Service in te bedden.
* De pakketten van de derde moeten aan de ontwikkeling van AEM as a Cloud Service [ ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines) en [ verpakken ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/repository-structure-package) richtlijnen naleven.
* Het overzicht [ wknd-erfenis ](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) project en begrijpt hoe [ de schendingen van INST ](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) kunnen worden verbeterd en compatibel gemaakt met AEM as a Cloud Service.
* Contacteer het [ AEM Team van de Steun ](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om kwesties te hebben die worden gericht.
