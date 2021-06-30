---
title: ACV
description: Help-pagina Patroondetectiecode
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a5
source-git-commit: 57e33b97aba253bad62cf95dcca9ef6885d263e6
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# ACV {#acv}

Assets Content Validator

## Achtergrond {#background}

>[!INFO]
>id=&quot;aemcloud_bpa_acv_overview&quot;
>title=&quot;Assets Content Validator&quot;
>abstract=&quot;ACV identificeert de ontbrekende verplichte knopen in activa inhoud.&quot;
>additional-url=&quot;https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html&quot; text=&quot;Notable Changes - Experience Manager as a Cloud Service&quot;
>additional-url=&quot;https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html&quot; text=&quot;Experience Manager als Cloud Service - Release Notes&quot;

`ACV`  De Content Validator van activa identificeert de ontbrekende verplichte knopen in activa inhoud. Dit kan ertoe leiden dat bepaalde elementen van Activa bij Experience Manager als Cloud Service niet correct zijn.

Subtypes worden gebruikt om de verschillende soorten informatie te identificeren, zoals:

* `assets.sanity.missing.jcrcontent`: Identificeer de mappen met ontbrekende verplichte knooppunten in de opslagplaats. Door eventuele ontbrekende inhoud in de opslagplaats te identificeren, kunt u eventuele defecte functies of gebruiksgevallen voorkomen.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

Dit kan ertoe leiden dat bepaalde functies van Elementen die afhankelijk zijn van overerfde eigenschappen in Experience Manager als Cloud Service, mislukken.

## Mogelijke oplossingen {#solutions}

>[!INFO]
>id=&quot;aemcloud_bpa_acv_guidance&quot;
>title=&quot;Implementatieleiding&quot;
>abstract=&quot;Adobe adviseert om inhoudsstructuur te herzien om gebroken werkschema&#39;s te verhinderen die van geërfte eigenschappen afhangen. Neem contact op met de klantenservice voor hulp.&quot;
>additional-url=&quot;https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html&quot; text=&quot;Experience Cloud Support&quot;

* Analyseer een map als er een onderliggend knooppunt ontbreekt. Maak de knooppunten handmatig als het aantal mappen kan worden beheerd. Gebruik anders een script.
* Bereik uit aan ons [team van de Zorg van de Klant van de Experience Manager](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om ongerustheid te richten.
