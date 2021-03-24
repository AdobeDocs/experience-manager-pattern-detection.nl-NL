---
title: URC
description: Help-pagina Patroondetectiecode
translation-type: tm+mt
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# URC {#urc}

Niet-ondersteunde configuratie van de uitvoermodus

## Achtergrond {#background}

`URC` identificeert het gebruik van configuraties die op een runmode naam gebaseerd zijn die niet in AEM als Cloud Service wordt gesteund.

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

* De reeks namen die in AEM als Cloud Service voor runmodi kan worden gebruikt, is beperkt.
* Configuraties die zijn gebaseerd op niet-ondersteunde runmodusnamen hebben geen effect wanneer ze worden geïmplementeerd als een Cloud Service.

## Mogelijke oplossingen {#solutions}

* Herzie het gebruik van deze configuratie om te bepalen als het noodzakelijk is.
* Wijzig de naam van de configuratie zodat een van de ondersteunde [runmode-namen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#custom-runmodes) wordt gebruikt en volg [runmode-resolutierichtlijnen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#runmode-resolution).
* Bekijk het [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc)-project en begrijp hoe [URC-schendingen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) kunnen worden gecorrigeerd en compatibel kunnen worden gemaakt met AEM als Cloud Service.
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
