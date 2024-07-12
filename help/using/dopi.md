---
title: DOPI
description: Help-pagina Patroondetectiecode.
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---

# DOPI {#dopi}

Index van verouderde geordende eigenschappen

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="Index van verouderde geordende eigenschappen"
>abstract="DOPI-code identificeert het gebruik van geordende definities in de eigenschappenindex ( `primaryType=oak:QueryIndexDefinition` AND `type="ordered"` ). De definitie is vervangen in AEM 6.1 en geschrapt in AEM 6.2."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing#the-ordered-index" text="Geordende index - Vervangen"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/operations/indexing" text="Indexeren - AEM as a Cloud Service"

`DOPI` Hiermee wordt het gebruik van geordende definities in de eigenschappenindex aangegeven ( `primaryType=oak:QueryIndexDefinition` AND `type="ordered"` ). De definities zijn vervangen in AEM 6.1 en geschrapt in AEM 6.2.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="Implementatieleiding"
>abstract="De beste praktijken moeten alle verouderde geordende indexen herzien en hen verplaatsen naar gesteunde vorm van indexen van Lucene om significante prestatieskwesties of niet-functionele klantenvereisten te vermijden."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/practices/best-practices-for-queries-and-indexing" text="Beste praktijken - Vragen en Indexeren"

* Sommige query&#39;s reageren mogelijk niet.
* De functionaliteit van de klant werkt mogelijk onjuist.
* Traversale waarschuwingen of zelfs fouten en significante prestatiesboetes aangezien de afgekeurde indexen geen effect hebben.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="Hulpmiddelen en Middelen"
>abstract="Het WKND-erfenisproject van het overzicht om te begrijpen hoe de schendingen van DOPI met AEM Cloud Service compatibel kunnen worden gemaakt. Lees ook het voorbeeld van DOPI-schending op GitHub. Het kan u helpen begrijpen hoe de erfenis geordende indexen in op Lucene gebaseerde indexen kunnen worden omgezet die in AEM as a Cloud Service worden gesteund."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="WKND-verouderd project"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="Voorbeeld van DOPI-schending - GitHub"

* Bewerk de indexdefinitie zodat deze een ondersteunde indexdefinitie wordt (of de index vervangt). (Zie [ Vragen van Oak en het Indexeren ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing)).
* Het overzicht [ wknd-erfenis ](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) project en begrijpt hoe [ de schendingen van het DOPI ](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) kunnen worden verbeterd en compatibel gemaakt met AEM as a Cloud Service.
* Contacteer het [ AEM Team van de Steun ](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om kwesties te hebben die worden gericht.
