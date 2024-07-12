---
title: WRK
description: Help-pagina Patroondetectiecode.
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 1%

---

# WRK {#wrk}

Workflow

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="Workflow"
>abstract="De code van het WRK identificeert een bevinding met betrekking tot een werkschemamodel of een lancerer. Deze identificaties worden gerapporteerd omdat workflowmodellen voor aangepaste middelen moeten worden gemigreerd wanneer u een upgrade naar AEM as a Cloud Service uitvoert. Met AEM as a Cloud Service voert asset microservices de verwerking van bedrijfsmiddelen uit."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/asset-microservices-overview" text="Asset Microservices"

`WRK` Hiermee wordt een bevinding geïdentificeerd die gerelateerd is aan een workflowmodel of startprogramma. Deze identificaties worden gerapporteerd omdat workflowmodellen voor aangepaste middelen moeten worden gemigreerd wanneer u een upgrade naar AEM as a Cloud Service uitvoert.

Een subtype wordt gebruikt om het type werkschemaprobleem te identificeren dat momenteel wordt ontdekt.

* `custom.asset.workflow`: detectie van een workflowmodel voor aangepaste elementen of een opstartprogramma.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="Implementatieleiding"
>abstract="Workflows met standaardmiddelen worden automatisch ondersteund door mijn assetmicroservices. Daarom is het aan te raden alle workflowmodellen voor aangepaste elementen of Launcher te controleren. Bij het bekijken kunt u zien of ze nodig zijn na de overgang naar AEM as a Cloud Service. Aanpassingen aan workflows voor bedrijfsmiddelen vereisen migratie om met AEM as a Cloud Service te kunnen werken met behulp van het Asset Workflow Migration Tool"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-microservices-configure-and-use" text="Aan de slag - Asset Microservices"

* Middelenverwerking is traditioneel uitgevoerd met middelenwerkstromen die worden uitgevoerd op de AEM Auteur-instantie. Met AEM as a Cloud Service voert asset microservices de verwerking van bedrijfsmiddelen uit. Zie het [ overzicht van activa microservices ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/asset-microservices-overview) voor meer informatie.
* Workflows met standaardmiddelen worden automatisch ondersteund door mijn assetmicroservices.
* Voor aanpassingen aan workflows met middelen is migratie vereist om met AEM as a Cloud Service te kunnen werken.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="Hulpmiddelen en Middelen"
>abstract="Reviseer en plant het programma voor het uitvoeren van Workflow-migratieprogramma voor bedrijfsmiddelen zodra een model of startprogramma voor een aangepaste workflow voor bedrijfsmiddelen is geïdentificeerd. Neem contact op met de ondersteuning van de Adobe voor hulp of verduidelijking."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/asset-workflow-migration-tool" text="De tool Asset Workflow Migration"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Als een model of de lancering van het douaneactiva werkschemamodel wordt geïdentificeerd, van plan om het [ Hulpmiddel van de Migratie van het Werkschema van Activa in werking te stellen ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/asset-workflow-migration-tool).
* Herzie [ Begonnen het worden van activa microservices ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-microservices-configure-and-use) voor meer informatie.
* Contacteer het [ AEM Team van de Steun ](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om kwesties te hebben die worden gericht.
