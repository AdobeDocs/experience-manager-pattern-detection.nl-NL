---
title: CIF
description: Help-pagina Patroondetectiecode
exl-id: cf9d5f62-c9dd-4f56-982c-1b5b19c81506
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# CIF {#cif}

Commerce integration framework, klassiek

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce integration framework, klassiek"
>abstract="CIF identificeert de klassieke versie van het gebruik van het Commerce integration framework die met AEM as a Cloud Service onverenigbaar zijn."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/introduction.html" text=" Inhoud en handel"

`CIF` CIF identificeert de klassieke versie van het gebruik van het Commerce integration framework die met AEM as a Cloud Service onverenigbaar zijn. Het bericht voor elke `CIF` zoeken zal het gebruik identificeren en aanvullende informatie verstrekken .

Subtypes worden gebruikt om de verschillende soorten informatie te identificeren:

* `commerce.integration.framework.detected`: Een klassieke versie van een Commerce integration framework dat niet compatibel is met AEM as a Cloud Service.


## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Implementatieleiding"
>abstract="De beste praktijken moeten alle klassieke versie van het gebruik van het Commerce integration framework herzien."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/changes.html" text="Opvallende wijzigingen in CIF"

* De klassieke versie van het Commerce integration framework wordt niet meer ondersteund op AEM as a Cloud Service. Het zou de upgrade naar AEM as a Cloud Service blokkeren.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Hulpmiddelen &amp; Middelen"
>abstract="Deze handleiding helpt u de gebieden te identificeren die u voor de migratie van de Experience Manager Cloud Service moet bijwerken."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/migration.html" text="Migratiehandleiding voor CIF"

* Voor as a Cloud Service Experience Manager is de CIF toe:voegen-on de enige gesteunde handelsintegratieoplossing voor Adobe Commerce en derdehandelsoplossingen. De CIF invoegtoepassing wordt automatisch geïmplementeerd voor klanten met as a Cloud Service Experience Manager. Handmatige implementatie is niet nodig. Zie [Aan de slag met AEM as a Cloud Service Handel](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/storefront/getting-started.html).
* Om projecten te steunen die CIF Adobe opstellen verstrekt [AEM CIF Core-componenten](https://github.com/adobe/aem-core-cif-components).
* CIF invoegtoepassing is ook beschikbaar voor AEM 6.5 via de [Software Distribution Portal](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html). Het is compatibel en biedt dezelfde functies als de CIF add-on voor as a Cloud Service Experience Manager. Er zijn geen aanpassingen nodig.
* Klassieke CIF met zijn gebiedsdelen is niet meer beschikbaar. Code die afhankelijk is van deze CIF versie met com.adobe.cq.commerce.api Java API&#39;s moet worden aangepast aan de CIF add-on en de bijbehorende principes.
