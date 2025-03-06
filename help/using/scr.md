---
title: SCR
description: Help-pagina Patroondetectiecode.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---

# SCR {#scr}

## Achtergrond {#background}

SIF identificeert AEM Screens-gebruik dat niet compatibel is met AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Mogelijke oplossingen {#solutions}

Zoek de mogelijke oplossingen voor de verschillende hieronder subtypes:

* `screens.bundles.detected` - Deze bundels worden tijdens de upgrade verwijderd.
* `screens.packages.detected` - Deze pakketten worden tijdens de upgrade verwijderd.
* `screens.packages.dependency` - Verwijder alle afhankelijkheden van Screens uit uw aangepaste pakketten.
* `screens.configs.detected` - Zorg ervoor dat u geen Screens config-eigenschappen gebruikt in uw aangepaste code.
* `screens.users.detected` - zorg ervoor u geen de dienstgebruikers van Screens in douanecode gebruikt.
* `screens.paths.detected` - Verwijder Screens-paden nadat u hebt gecontroleerd of ze niet in AEM worden gebruikt.
* `screens.resource.type.detected` - Verwijder het gebruik van het Screens-brontype.
* `screens.usage` - Verwijder Screens API&#39;s uit uw aangepaste code.