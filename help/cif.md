---
title: CIF
description: Help-pagina Patroondetectiecode
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
source-git-commit: 84aea5b24e51ce5672826bad4ec126074bf24a09
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# CIF {#cif}

Commerce Integration Framework Classic

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework Classic"
>abstract="CIF identificeert de klassieke versie van het gebruik van het Kader van de Integratie van de Handel dat met AEM als Cloud Service onverenigbaar is."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/introduction.html" text=" Inhoud en handel"

`CIF` CIF identificeert de klassieke versie van het gebruik van het Kader van de Integratie van de Handel dat met AEM als Cloud Service onverenigbaar is. Het bericht voor elke `CIF` het vinden zal het gebruik identificeren en extra informatie verstrekken.

Subtypes worden gebruikt om de verschillende soorten informatie te identificeren:

* `commerce.integration.framework.detected`: Een klassieke versie van Commerce Integration Framework is onverenigbaar met AEM als Cloud Service.


## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Implementatieleiding"
>abstract="De beste praktijken moeten alle klassieke versie van het gebruik van het Kader van de Integratie van de Handel herzien."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/changes.html" text="Opvallende wijzigingen in CIF"

* De klassieke versie van Commerce Integration Framework wordt niet meer ondersteund op AEM als Cloud Service. Het zou de verbetering aan AEM als Cloud Service blokkeren.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Hulpmiddelen &amp; Middelen"
>abstract="Deze handleiding helpt u de gebieden te identificeren die u voor de migratie van de Experience Manager Cloud Service moet bijwerken."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/migration.html" text="Migratiehandleiding voor CIF"

* Voor Experience Manager als Cloud Service is de toe:voegen-on CIF de enige gesteunde handelsintegratieoplossing voor de Handel van de Adobe en derdehandel oplossingen. De toe:voegen-op CIF wordt automatisch opgesteld voor klanten op Experience Manager als Cloud Service, geen handplaatsing wordt vereist. Zie [Aan de slag met AEM Handel als Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/storefront/getting-started.html).
* Om projecten te steunen die CIF Adobe gebruiken verstrekt [AEM de Componenten van de Kern van CIF](https://github.com/adobe/aem-core-cif-components).
* De toe:voegen-on CIF is beschikbaar voor AEM 6.5 evenals via [het portaal van de Distributie van de Software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html). Het is compatibel en biedt dezelfde functies als de CIF-invoegtoepassing voor Experience Manager als een Cloud Service. Er zijn geen aanpassingen nodig.
* Klassieke CIF met zijn gebiedsdelen is niet meer beschikbaar. Code die afhankelijk is van deze CIF-versie met com.adobe.cq.commerce.api Java API&#39;s moet worden aangepast aan de CIF-invoegtoepassing en de bijbehorende beginselen.
