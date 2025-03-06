---
title: WRF
description: Help-pagina Patroondetectiecode.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# WRF {#wrf}

## Achtergrond {#background}

WRF identificeert wij-kleinhandelsgebruik dat met AEM 6.5 LTS onverenigbaar is.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Mogelijke oplossingen {#solutions}

Zoek de mogelijke oplossingen voor de verschillende hieronder subtypes:

* `weretail.bundles.detected` - Deze bundels worden tijdens de upgrade verwijderd
* `weretail.packages.detected` - Deze pakketten worden tijdens de upgrade verwijderd
* `weretail.configs.detected` - Gebruik geen Web.Retail config-eigenschappen in uw aangepaste code
* `weretail.packages.dependency` - Verwijder de afhankelijkheid van elk aangepast pakket op We.Retail
* `weretail.paths.detected` - Deze We.Retail-paden kunnen worden verwijderd nadat u ervoor hebt gezorgd dat u geen gebruik maakt van sociale
* `weretail.resource.type.detected` - We verwijderen. Gebruik van het mediatype Handel
* `weretail.usage` - We.Retail-API&#39;s verwijderen uit uw aangepaste code.