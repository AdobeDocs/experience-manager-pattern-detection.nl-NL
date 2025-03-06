---
title: SPI
description: Help-pagina Patroondetectiecode.
source-git-commit: e050b9190f67fd6ccfac31490c4bf2a60d47731f
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# SPI {#spi}

## Achtergrond {#background}

SIF identificeert het gebruik van het Onderzoek en van de Bevordering die met AEM 6.5 LTS onverenigbaar is.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Mogelijke oplossingen {#solutions}

Zoek de mogelijke oplossingen voor de verschillende hieronder subtypes:

* `searchpromote.bundles.detected` - Deze bundels worden tijdens de upgrade verwijderd
* `earchpromote.packages.detected` - Deze pakketten worden tijdens de upgrade verwijderd
* `searchpromote.packages.dependency` - Verwijder alle zoekopdrachten en promoot de afhankelijkheid van uw aangepaste pakketten
* `searchpromote.usage` - Zoeken en promotie-API&#39;s verwijderen uit uw aangepaste code
* `searchpromote.users.detected` - Gebruik geen zoek- en promotiegebruikers in aangepaste code
* `searchpromote.configs.detected` - Gebruik de eigenschappen van de Configuratie van het Onderzoek en van de Bevordering niet in uw douanecode.