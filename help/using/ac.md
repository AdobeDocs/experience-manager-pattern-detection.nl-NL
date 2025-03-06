---
title: Wisselen
description: Help-pagina Patroondetectiecode.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---

# Wisselen {#ac}

## Achtergrond {#background}

AC identificeert Assets bundelgebruik dat met AEM 6.5 LTS onverenigbaar is

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Mogelijke oplossingen {#solutions}

Zoek de mogelijke oplossingen voor de verschillende hieronder subtypes:

* `asset.bundles.detected` - Deze bundel wordt tijdens de upgrade verwijderd.
* `asset.usage` - Verwijder alle afhankelijkheden van de component Asset Rating en Asset Catalog uit de aangepaste code. Wijzig, indien van toepassing, de code voor het gebruik van de nieuwe API `List<Scene7ConfigSetting>` `com.day.cq.dam.scene7.api.model.Scene7ViewerConfig#getSettingsList()` .
* `asset.overlays.detected` - Bedekkingen die zijn gemaakt in Assets Rating- en Catalog-componenten moeten worden verwijderd.
* `asset.resource.type.detected` - Verwijder elk gebruik van het brontype van de Assets-ratingcomponent in uw aangepaste code.
* `asset.paths.detected` - Verplaats de inhoud van de klant die zich onder deze paden bevindt en verwijder deze paden nadat u ervoor hebt gezorgd dat deze niet in AEM worden gebruikt.