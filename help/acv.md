---
title: ACV
description: Help-pagina Patroondetectiecode
exl-id: 1dd1af45-aa56-48da-8582-c4330cded489
source-git-commit: 301aef7e53e94eb5941691450b3f1192408f2c6b
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# ACV {#acv}

Assets Content Validator

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Assets Content Validator"
>abstract="ACV identificeert de ontbrekende verplichte knooppunten in de inhoud van elementen."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html" text="Opmerkelijke wijzigingen - Experience Manager as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="Experience Manager as a Cloud Service - Opmerkingen bij de release"

`ACV`  De Content Validator van activa identificeert de ontbrekende verplichte knopen in activa inhoud. Dit kan ertoe leiden dat bepaalde elementen van Activa op as a Cloud Service Experience Manager niet correct zijn.

Subtypes worden gebruikt om de verschillende soorten informatie te identificeren, zoals:

* `missing.jcrcontent`: Identificeer de mappen met ontbrekende verplichte knooppunten in de opslagplaats. Door eventuele ontbrekende inhoud in de opslagplaats te identificeren, kunt u eventuele defecte functies of gebruiksgevallen voorkomen.
* `missing.original.rendition`: Identificeer de activa met een ontbrekende verplichte originele vertoning in de bewaarplaats.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* Dit kan tot mislukken van bepaalde eigenschappen van Activa leiden die van geërfte eigenschappen in as a Cloud Service Experience Manager afhangen.
* AEM Assets is afhankelijk van het bestaan van de oorspronkelijke uitvoering. De verwerking van het element in de Cloud Service verloopt in een lus als de oorspronkelijke uitvoering ontbreekt.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Implementatieleiding"
>abstract="Adobe raadt aan de inhoudstructuur te controleren om te voorkomen dat werkstromen die afhankelijk zijn van overgenomen eigenschappen, worden verbroken. Neem contact op met de klantenservice voor hulp."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-ondersteuning"

* Analyseer een map als er een onderliggend knooppunt ontbreekt. Maak de knooppunten handmatig als het aantal mappen kan worden beheerd. Gebruik anders een script.
* Voor de elementen die de oorspronkelijke uitvoering missen, uploadt u de elementen opnieuw of verwijdert u deze voordat u migreert.
* Bereik onze [Klantenzorgteam van Experience Manager](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
