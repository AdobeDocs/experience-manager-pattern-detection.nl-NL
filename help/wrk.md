---
title: WRK
description: Help-pagina Patroondetectiecode
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
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
>abstract="De code van het WRK identificeert een bevinding met betrekking tot een werkschemamodel of een lancerer. Deze worden gerapporteerd omdat workflowmodellen voor aangepaste elementen moeten worden gemigreerd wanneer u een upgrade naar AEM als Cloud Service uitvoert. Met AEM als Cloud Service, wordt de activaverwerking nu uitgevoerd door activa microservices."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html" text="Asset Microservices"

`WRK` identificeert een bevinding met betrekking tot een workflowmodel of draagprogramma. Deze worden gerapporteerd omdat workflowmodellen voor aangepaste elementen moeten worden gemigreerd wanneer u een upgrade naar AEM als Cloud Service uitvoert.

Een subtype wordt gebruikt om het type werkschemaprobleem te identificeren dat momenteel wordt ontdekt.

* `custom.asset.workflow`: Detection of a custom asset workflow model or launch.

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="Implementatieleiding"
>abstract="Aangezien de standaard werkschema&#39;s van activa automatisch mijn activa microservices worden gesteund, is de beste praktijken al model of de lancering van het douaneactiva te herzien om te zien of zijn zij nodig zodra wij overgang aan AEM als Cloud Service. Aanpassingen aan workflows voor bedrijfsmiddelen vereisen migratie om te kunnen werken met AEM als Cloud Service met behulp van het Asset Workflow Migration Tool"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html" text="Aan de slag - Asset Microservices"

* Middelenverwerking is traditioneel uitgevoerd met middelenwerkstromen die worden uitgevoerd op de AEM Auteur-instantie. Met AEM als Cloud Service, wordt de activaverwerking nu uitgevoerd door activa microservices. (Zie het [overzicht van elementmicroservices](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html) voor meer informatie.
* Workflows met standaardmiddelen worden automatisch ondersteund door mijn assetmicroservices.
* Aanpassingen aan werkstromen van bedrijfsmiddelen vereisen migratie om met AEM als Cloud Service te werken.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="Hulpmiddelen &amp; Middelen"
>abstract="Reviseren en plannen om het Asset Workflow Migration Tool uit te voeren zodra een aangepast workflowmodel of een startprogramma voor middelen is geïdentificeerd. Neem contact op met Adobe Support voor hulp en uitleg"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html" text="De tool Asset Workflow Migration"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-ondersteuning"

* Als een model of een startprogramma voor een aangepaste asset-workflow wordt geïdentificeerd, is u van plan om het [Workflow-migratiehulpprogramma voor bedrijfsmiddelen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html) uit te voeren.
* Lees [Aan de slag met gebruik van elementmicroservices](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html) voor meer informatie.
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
