---
title: DOPI
description: Help-pagina Patroondetectiecode
translation-type: tm+mt
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# DOPI {#dopi}

Index van verouderde geordende eigenschappen

## Achtergrond {#background}

`DOPI` identificeert het gebruik van de geordende definities van de bezitsindex (`primaryType=oak:QueryIndexDefinition` AND  `type="ordered"`), die sinds 6.1 zijn verouderd en in 6.2 zijn verwijderd.

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

* Sommige query&#39;s reageren mogelijk niet.
* De functionaliteit van de klant werkt mogelijk onjuist.
* Traversale waarschuwingen of zelfs fouten en significante prestatiesboetes aangezien de afgekeurde indexen geen effect hebben.

## Mogelijke oplossingen {#solutions}

* Wijzig de indexdefinitie om een ondersteunde indexdefinitie te worden of vervang de index door een ondersteunde indexdefinitie. (Zie [Eak-query&#39;s en indexering](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html)).
* Bekijk het [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi)-project en begrijp hoe [DOPI-schendingen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) kunnen worden gecorrigeerd en compatibel kunnen worden gemaakt met AEM als Cloud Service.
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
