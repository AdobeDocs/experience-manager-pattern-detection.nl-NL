---
title: SIF
description: Help-pagina Patroondetectiecode.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# SIF {#sif}

## Achtergrond {#background}

SIF identificeert sociaal gebruik dat met AEM 6.5 LTS onverenigbaar is.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Mogelijke oplossingen {#solutions}

Zoek de mogelijke oplossingen voor de verschillende hieronder subtypes:

* `social.bundles.detected` - Deze bundels worden tijdens de upgrade verwijderd
* `social.packages.detected` - Deze pakketten worden tijdens de upgrade verwijderd
* `social.packages.dependency` - Verwijder de pakketafhankelijkheid van een sociaal netwerk uit aangepaste pakketten
* `social.nodes.detected` - Aangepaste code bijwerken om geen sociale knooppunten te maken
* `social.configs.detected` - Gebruik geen eigenschappen van de sociale configuratie in aangepaste code
* `social.users.detected` - Gebruik geen sociale gebruikers in aangepaste code
* `social.overlays.detected` - Gebruik van sociale overlays verwijderen
* `social.paths.detected` - Verwijder sociale paden nadat u hebt gecontroleerd of deze paden niet in AEM worden gebruikt
* `social.resource.type.detected` - Gebruik van sociale bronnen verwijderen
* `social.usage` - Verwijder sociale API&#39;s uit aangepaste code.