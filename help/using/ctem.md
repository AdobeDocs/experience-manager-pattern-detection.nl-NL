---
title: CTEM
description: Help-pagina Patroondetectiecode.
exl-id: cd70486c-8e21-4c31-89bf-928b80fa8772
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 2%

---

# CTEM {#ctem}

Aangepaste sjabloon

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_overview"
>title="Aangepaste sjabloon"
>abstract="CTEM identificeert douanecomponenten die op AEM zijn geïnstalleerd. Deze informatie wordt verstrekt met het oog op de beoordeling van beste praktijken"

CTEM identificeert douanesjablonen die op AEM zijn geïnstalleerd. Deze informatie wordt verstrekt met het oog op de beoordeling van beste praktijken.

Sjablonen worden aangeduid met een waarde van het primaire type van `cq:Template`. Met deze code wordt een subtype gebruikt om de sjablooncategorie aan te duiden:

* `custom.editable.template`: Het pad van de sjabloon begint niet met &quot;/apps&quot;.
* `custom.static.template`: Het pad van de sjabloon begint met &quot;/apps&quot;.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_guidance"
>title="Implementatieleiding"
>abstract="U kunt het beste alle statische sjablonen naar bewerkbare sjablonen verplaatsen. Klanten kunnen bestaande AEM moderniseringsgereedschappen gebruiken om statische sjablonen te migreren naar bewerkbare sjablonen."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/templates/templates" text="Bewerkbare sjablonen"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM-moderniseringstools"

* U kunt het beste alle statische sjablonen naar bewerkbare sjablonen verplaatsen.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_tools"
>title="Hulpmiddelen &amp; Middelen"
>abstract="Met behulp van AEM Moderniseringssuite kunnen klanten de structuur van een pagina manipuleren van een statische definitie naar een bewerkbare sjabloon. De bedoeling is om klanten te helpen van de beperkte mogelijkheden van de oudere functies over te stappen op het robuuste, moderne AEM. Deze hulpmiddelen zijn configureerbaar, configuratie-bewust, en verlengbaar. Neem contact op met de ondersteuning van de Adobe voor hulp of verduidelijking."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/structure/about.html" text="Paginastructuurconverter"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Gebruik de [AEM moderniseringsinstrumenten](https://opensource.adobe.com/aem-modernize-tools/) om statische sjablonen te migreren naar bewerkbare sjablonen.
* Meer informatie over bewerkbare sjablonen vindt u op [Sjablonen](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/templates/templates).
* Contact opnemen met de [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om de problemen te verhelpen.
