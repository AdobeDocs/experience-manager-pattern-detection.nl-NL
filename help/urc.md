---
title: URC
description: Help-pagina Patroondetectiecode
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# URC {#urc}

Niet-ondersteunde configuratie van de uitvoermodus

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Niet-ondersteunde configuratie van de uitvoermodus"
>abstract="URC identificeert het gebruik van configuraties die op een runmode naam gebaseerd zijn die niet in AEM as a Cloud Service wordt gesteund."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#custom-runmodes" text="Ondersteunde uitvoermodi"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#runmodes" text="Runmodi"

`URC` identificeert het gebruik van configuraties die op een runmode naam gebaseerd zijn die niet in AEM as a Cloud Service wordt gesteund.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Implementatieleiding"
>abstract="De beste praktijk is om te controleren of alle runmodi die in uw toepassing worden gebruikt, worden ondersteund en ervoor te zorgen dat deze de richtlijnen voor de resolutie van de runmode volgen"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#deploying" text="Richtlijnen voor resolutie bij uitvoering"

* De reeks namen die in AEM as a Cloud Service voor runmodi kan worden gebruikt, is beperkt.
* Configuraties die zijn gebaseerd op niet-ondersteunde runmodusnamen hebben geen effect wanneer ze worden geïmplementeerd op AEM as a Cloud Service.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Hulpmiddelen &amp; Middelen"
>abstract="Bekijk het WKND-oudere project om te begrijpen hoe schendingen van URC compatibel kunnen worden gemaakt met AEM Cloud Service. Lees ook het voorbeeld voor OSGi-configuraties van OSGi-versies op basis van aangepaste runmode op basis van Github om na te gaan of AEM as a Cloud Service is."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="WKND-verouderd project"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Voorbeeld van schending van URC - Github"

* Herzie het gebruik van deze configuratie om te bepalen als het noodzakelijk is.
* Wijzig de naam van de configuratie om een van de ondersteunde configuraties te gebruiken [runmode-namen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#custom-runmodes) en volgen [richtlijnen voor runmode resolutie](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#runmode-resolution).
* Controleren [verouderd](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) projecten en begrijpen hoe [OTC-overtredingen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) kan worden gecorrigeerd en verenigbaar worden gemaakt met AEM as a Cloud Service.
* Neem contact op met onze [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
