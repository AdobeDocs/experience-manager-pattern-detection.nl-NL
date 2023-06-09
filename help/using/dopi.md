---
title: DOPI
description: Help-pagina Patroondetectiecode
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# DOPI {#dopi}

Index van verouderde geordende eigenschappen

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="Index van verouderde geordende eigenschappen"
>abstract="De code DOPI identificeert het gebruik van geordende eigenschappen indexdefinities (primaryType=eak:QueryIndexDefinition AND type= &quot;ordered&quot;), die sinds 6.1 zijn afgekeurd en in 6.2 zijn verwijderd."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html?lang=en#the-ordered-index" text="Geordende index - Vervangen"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html" text="Indexeren - AEM as a Cloud Service"

`DOPI` identificeert het gebruik van geordende eigenschappen indexdefinities (`primaryType=oak:QueryIndexDefinition` EN `type="ordered"`), die sinds 6.1 zijn afgekeurd en in punt 6.2 zijn geschrapt.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="Implementatieleiding"
>abstract="De beste praktijken moeten alle verouderde geordende indexen herzien en hen verplaatsen naar gesteunde vorm van lucene indexen om significante prestatieskwesties of niet-functionele klantenvereisten te vermijden."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/practices/best-practices-for-queries-and-indexing.html" text="Beste praktijken - Vragen en Indexeren"

* Sommige query&#39;s reageren mogelijk niet.
* De functionaliteit van de klant werkt mogelijk onjuist.
* Traversale waarschuwingen of zelfs fouten en significante prestatiesboetes aangezien de afgekeurde indexen geen effect hebben.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="Hulpmiddelen &amp; Middelen"
>abstract="Het WKND-erfenisproject van het overzicht om te begrijpen hoe de schendingen van DOPI met AEM Cloud Service compatibel kunnen worden gemaakt. Raadpleeg ook het voorbeeld DOPI-schending op Github om te begrijpen hoe indexen met oudere volgordes kunnen worden omgezet in indexen op basis van Lucene die worden ondersteund in AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="WKND-verouderd project"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="Voorbeeld van schending DOPI - Github"

* Wijzig de indexdefinitie om een ondersteunde indexdefinitie te worden of vervang de index door een ondersteunde indexdefinitie. (Zie [Oak-query&#39;s en indexering](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html)).
* Controleren [verouderd](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) projecten en begrijpen hoe [DOPI-overtredingen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) kan worden gecorrigeerd en verenigbaar worden gemaakt met AEM as a Cloud Service.
* Neem contact op met onze [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
