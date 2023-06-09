---
title: WRK
description: Help-pagina Patroondetectiecode
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---

# WRK {#wrk}

Workflow

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="Workflow"
>abstract="De code van het WRK identificeert een bevinding met betrekking tot een werkschemamodel of een lancerer. Deze worden gerapporteerd omdat workflowmodellen met aangepaste elementen moeten worden gemigreerd wanneer u een upgrade uitvoert naar AEM as a Cloud Service. Met AEM as a Cloud Service, wordt de activaverwerking nu uitgevoerd door activa microservices."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html" text="Asset Microservices"

`WRK` identificeert een bevinding met betrekking tot een workflowmodel of draagprogramma. Deze worden gerapporteerd omdat workflowmodellen met aangepaste elementen moeten worden gemigreerd wanneer u een upgrade uitvoert naar AEM as a Cloud Service.

Een subtype wordt gebruikt om het type werkschemaprobleem te identificeren dat momenteel wordt ontdekt.

* `custom.asset.workflow`: Detection of a custom asset workflow model or launch.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="Implementatieleiding"
>abstract="Aangezien de standaard werkschema&#39;s van activa automatisch mijn activa microservices worden gesteund, is de beste praktijken al model of de lancering van het douaneactiva te herzien om te zien of zijn zij nodig zodra wij overgang aan AEM as a Cloud Service. Aanpassingen aan workflows voor bedrijfsmiddelen vereisen migratie om te kunnen werken met AEM as a Cloud Service met de hulp van het Hulpprogramma voor migratie van bedrijfsmiddelen"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html" text="Aan de slag - Asset Microservices"

* Middelenverwerking is traditioneel uitgevoerd met middelenwerkstromen die worden uitgevoerd op de AEM Auteur-instantie. Met AEM as a Cloud Service, wordt de activaverwerking nu uitgevoerd door activa microservices. (Zie de [Overzicht van asset microservices](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html) voor meer informatie .
* Workflows met standaardmiddelen worden automatisch ondersteund door mijn assetmicroservices.
* Voor aanpassingen aan werkstromen met middelen is migratie vereist om met AEM as a Cloud Service te kunnen werken.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="Hulpmiddelen &amp; Middelen"
>abstract="Reviseren en plannen om het Asset Workflow Migration Tool uit te voeren zodra een aangepast workflowmodel of een startprogramma voor middelen is geïdentificeerd. Neem contact op met Adobe Support voor hulp en uitleg"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html" text="De tool Asset Workflow Migration"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-ondersteuning"

* Als er een workflowmodel voor aangepaste middelen of een startprogramma is geïdentificeerd, kunt u het programma [Hulpprogramma voor migratie van workflows](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html).
* Controleer de [Aan de slag met middelenmicroservices](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html) voor meer informatie .
* Neem contact op met onze [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
