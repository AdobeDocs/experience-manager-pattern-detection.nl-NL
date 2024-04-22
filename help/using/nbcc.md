---
title: NBCC
description: Help-pagina Patroondetectiecode.
exl-id: fa6bdd3c-4deb-41ec-878d-4ea5dc1ddf60
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---

# NBCC {#nbcc}

VEROUDERD: Niet-achterwaartse compatibele wijzigingen (vervangen door NCC, niet-compatibele wijzigingen)

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_overview"
>title="Niet-achterwaartse compatibele wijzigingen"
>abstract="NBCC geeft aan in welke situatie sommige JCR-knooppunten of -bundels op een niet-compatibele manier worden gewijzigd. De klant is wellicht niet op de hoogte van deze wijziging voordat een upgrade wordt uitgevoerd."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Opvallende wijzigingen - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="Opmerkingen bij de release - AEM as a Cloud Service"

`NBCC` geeft de situatie aan waarin sommige JCR-knooppunten of -bundels op een niet-compatibele manier worden gewijzigd. De klant is wellicht niet op de hoogte van deze wijziging voordat een upgrade wordt uitgevoerd.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* De functionaliteit die afhankelijk is van een component die niet-achterwaartse compatibele wijzigingen gebruikt, kan worden verbroken en niet correct worden omgezet.
* Sommige functies van de klanttoepassing of bepaalde AEM werken mogelijk niet correct na een upgrade.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_guidance"
>title="Implementatieleiding"
>abstract="Aangepaste code controleren is de beste manier om te controleren of alleen achterwaartse compatibele Sling-componenten worden bedekt of waarnaar wordt verwezen. Neem contact op met de Adobe Support voor hulp en verduidelijking"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html#platform" text="Bedekkingen"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Bedekking of verwijzing alleen naar achterwaartse compatibele Sling-componenten.
* Overweeg de middelen die afkomstig zijn van `/libs` of bundels na een AEM upgrade.
* Contact opnemen met de [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om de problemen te verhelpen.
