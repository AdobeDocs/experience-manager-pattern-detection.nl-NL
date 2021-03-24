---
title: WRK
description: Help-pagina Patroondetectiecode
translation-type: tm+mt
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# WRK {#wrk}

Workflow

## Achtergrond {#background}

`WRK` identificeert een bevinding met betrekking tot een workflowmodel of draagprogramma. Deze worden gerapporteerd omdat workflowmodellen voor aangepaste elementen moeten worden gemigreerd wanneer u een upgrade naar AEM als Cloud Service uitvoert.

Een subtype wordt gebruikt om het type werkschemaprobleem te identificeren dat momenteel wordt ontdekt.

* `custom.asset.workflow`: Detection of a custom asset workflow model or launch.

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

* Middelenverwerking is traditioneel uitgevoerd met middelenwerkstromen die worden uitgevoerd op de AEM Auteur-instantie. Met AEM als Cloud Service, wordt de activaverwerking nu uitgevoerd door activa microservices. (Zie het [overzicht van elementmicroservices](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html) voor meer informatie.
* Workflows met standaardmiddelen worden automatisch ondersteund door mijn assetmicroservices.
* Aanpassingen aan werkstromen van bedrijfsmiddelen vereisen migratie om met AEM als Cloud Service te werken.

## Mogelijke oplossingen {#solutions}

* Als een model of een startprogramma voor een aangepaste asset-workflow wordt geïdentificeerd, is u van plan om het [Workflow-migratiehulpprogramma voor bedrijfsmiddelen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html) uit te voeren.
* Lees [Aan de slag met gebruik van elementmicroservices](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html) voor meer informatie.
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
