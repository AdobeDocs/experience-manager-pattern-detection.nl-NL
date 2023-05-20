---
title: NCC
description: Help-pagina Patroondetectiecode
exl-id: 4a374956-c64e-43fc-8279-ed25f6ed5cb0
source-git-commit: 8b8d902dc5b5a8534475d256c199dc235bb35464
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# NCC {#ncc}

Niet-compatibele wijzigingen

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_overview"
>title="Niet-compatibele wijzigingen"
>abstract="NCC identificeert de situatie waarin sommige JCR-knooppunten of -bundels op een niet-compatibele manier worden gewijzigd. De klant is wellicht niet op de hoogte van deze wijziging voordat een upgrade wordt uitgevoerd."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Opvallende wijzigingen - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="Opmerkingen bij de release - AEM as a Cloud Service"

`NCC` geeft de situatie aan waarin sommige JCR-knooppunten of -bundels op een niet-compatibele manier worden gewijzigd. De klant is wellicht niet op de hoogte van deze wijziging voordat een upgrade wordt uitgevoerd.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* De functionaliteit die afhankelijk is van een component die niet-compatibele wijzigingen gebruikt, kan worden verbroken en niet correct worden omgezet.
* Sommige functies van de klanttoepassing of bepaalde AEM werken mogelijk niet correct na een upgrade.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_guidance"
>title="Implementatieleiding"
>abstract="Aangepaste code controleren is de beste manier om alleen compatibele Sling-componenten te controleren of ernaar te verwijzen. Neem contact op met Adobe Support voor hulp en uitleg"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html#platform" text="Bedekkingen"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-ondersteuning"

* Bedekking of verwijzing alleen compatibele Sling-componenten.
* Overweeg de middelen die afkomstig zijn van `/libs` of bundels na een AEM upgrade.
* Neem contact op met onze [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
