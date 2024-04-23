---
title: WRK
description: Help-pagina Patroondetectiecode.
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---

# WRK {#wrk}

Workflow

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="Workflow"
>abstract="De code van het WRK identificeert een bevinding met betrekking tot een werkschemamodel of een lancerer. Deze worden gerapporteerd omdat workflowmodellen met aangepaste elementen moeten worden gemigreerd wanneer u een upgrade uitvoert naar AEM as a Cloud Service. Met AEM as a Cloud Service, wordt de activaverwerking nu uitgevoerd door activa microservices."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/asset-microservices-overview" text="Asset Microservices"

WRK identificeert het vinden met betrekking tot een werkschemamodel of een lancerer. Deze worden gerapporteerd omdat workflowmodellen met aangepaste elementen moeten worden gemigreerd wanneer u een upgrade uitvoert naar AEM as a Cloud Service.

Een subtype wordt gebruikt om het type werkschemaprobleem te identificeren dat momenteel wordt ontdekt.

* `custom.asset.workflow`: Detection of a custom asset workflow model or launch.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="Implementatieleiding"
>abstract="Workflows met standaardmiddelen worden automatisch ondersteund door mijn assetmicroservices. Daarom is het aan te raden om alle workflowmodellen voor aangepaste elementen of Lanceerprogramma te bekijken om na te gaan of deze nodig zijn nadat u naar AEM as a Cloud Service bent gegaan. Aanpassingen aan workflows voor bedrijfsmiddelen vereisen migratie om te kunnen werken met AEM as a Cloud Service met behulp van het Hulpprogramma voor migratie van bedrijfsmiddelen"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-microservices-configure-and-use" text="Aan de slag - Asset Microservices"

* Middelenverwerking is traditioneel uitgevoerd met middelenwerkstromen die worden uitgevoerd op de AEM Auteur-instantie. Met AEM as a Cloud Service, wordt de activaverwerking nu uitgevoerd door activa microservices. Zie de [Overzicht van asset microservices](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/asset-microservices-overview) voor meer informatie .
* Workflows met standaardmiddelen worden automatisch ondersteund door mijn assetmicroservices.
* Voor aanpassingen aan werkstromen met middelen is migratie vereist om met AEM as a Cloud Service te kunnen werken.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="Hulpmiddelen &amp; Middelen"
>abstract="Reviseren en plannen om het Asset Workflow Migration Tool uit te voeren zodra een aangepast workflowmodel of een startprogramma voor middelen is geïdentificeerd. Neem contact op met de ondersteuning van de Adobe voor hulp of verduidelijking."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/asset-workflow-migration-tool" text="De tool Asset Workflow Migration"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Als er een workflowmodel voor aangepaste middelen of een startprogramma is geïdentificeerd, kunt u het programma [Hulpprogramma voor migratie van workflows](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/asset-workflow-migration-tool).
* Controleer de [Aan de slag met middelenmicroservices](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-microservices-configure-and-use) voor meer informatie .
* Contact opnemen met de [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om de problemen te verhelpen.
