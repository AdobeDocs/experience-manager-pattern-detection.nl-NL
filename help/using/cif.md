---
title: CIF
description: Help-pagina Patroondetectiecode.
exl-id: cf9d5f62-c9dd-4f56-982c-1b5b19c81506
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# CIF {#cif}

Commerce integration framework Classic

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce integration framework Classic"
>abstract="CIF identificeert de klassieke versie van Commerce integration framework-gebruik die niet compatibel is met AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/content-and-commerce/introduction" text=" Inhoud en Commerce"

`CIF` Hiermee wordt de klassieke versie van het Commerce integration framework-gebruik aangegeven die niet compatibel is met AEM as a Cloud Service. Het bericht voor elke `CIF` -bevinding geeft het gebruik aan en bevat aanvullende informatie.

Subtypes worden gebruikt om de verschillende soorten informatie te identificeren:

* `commerce.integration.framework.detected`: een klassieke versie van Commerce integration framework die niet compatibel is met AEM as a Cloud Service.


## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Implementatieleiding"
>abstract="U kunt het beste alle klassieke versies van Commerce integration framework-gebruik bekijken."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/content-and-commerce/changes" text="Opvallende wijzigingen in CIF"

* De klassieke versie van Commerce integration framework wordt niet meer ondersteund op AEM as a Cloud Service. Het zou de upgrade naar AEM as a Cloud Service blokkeren.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Hulpmiddelen en Middelen"
>abstract="Deze handleiding helpt u de gebieden te identificeren die u moet bijwerken voor de Experience Manager Cloud Service-migratie."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/content-and-commerce/migration" text="Migratiehandleiding voor CIF"

* Voor Experience Manager as a Cloud Service is de CIF add-on de enige ondersteunde oplossing voor commerciële integratie voor Adobe Commerce en handelsoplossingen van derden. De invoegtoepassing CIF wordt automatisch geïmplementeerd voor klanten op Experience Manager as a Cloud Service. Handmatige implementatie is niet nodig. Zie [ Begonnen het worden met AEM Commerce as a Cloud Service ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/content-and-commerce/storefront/getting-started).
* Om projecten te steunen die CIF opstellen, verstrekt Adobe {de Componenten van de Kern van 0} AEM CIF ](https://github.com/adobe/aem-core-cif-components).[
* CIF toe:voegen-op is beschikbaar voor AEM 6.5 evenals als [ portaal van de Distributie van de Software ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html). Het is compatibel en biedt dezelfde functies als de CIF-invoegtoepassing voor Experience Manager as a Cloud Service. Aanpassingen zijn niet vereist.
* Klassieke CIF met zijn afhankelijkheden is niet meer beschikbaar. Code die afhankelijk is van deze CIF-versie met com.adobe.cq.commerce.api Java™ API&#39;s moet worden aangepast aan de CIF-invoegtoepassing en de bijbehorende principes.

Zoek ook de mogelijke oplossingen voor de verschillende subtypen hieronder:

* `commerce.bundles.detected` - Deze bundels worden tijdens de upgrade verwijderd
* `commerce.packages.detected` - Deze pakketten worden tijdens de upgrade verwijderd
* `commerce.packages.dependency` - Eventuele afhankelijkheden van Commerce verwijderen uit aangepaste pakketten
* `commerce.nodes.detected` - Aangepaste code bijwerken om geen CQ Commerce-knooppunten te maken
* `commerce.configs.detected` - Gebruik geen CQ Commerce config-eigenschappen in aangepaste code
* `commerce.users.detected` - Gebruik geen CQ Commerce-servicegebruikers in aangepaste code
* `commerce.overlays.detected` - Gebruik van CQ Commerce-overlays verwijderen
* `commerce.paths.detected` - Handelspaden verwijderen nadat is gecontroleerd of deze paden niet worden gebruikt op AEM
* `commerce.resource.type.detected` - Het type handelsbron verwijderen
* `commerce.usage` - CQ Commerce API&#39;s verwijderen in uw aangepaste code.
