---
title: PCX
description: Help-pagina Patroondetectiecode
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# PCX {#pcx}

Complexiteit pagina

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_overview"
>title="Complexiteit pagina"
>abstract="PCX identificeert pagina&#39;s die een groot aantal knooppunten in hun structuur bevatten."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Opvallende wijzigingen - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="AEM as a Cloud Service - Opmerkingen bij de release"

`PCX` Hiermee geeft u pagina&#39;s aan die een groot aantal knooppunten in hun structuur bevatten.

Subtypes worden gebruikt om de verschillende soorten informatie te identificeren:

* `page.complexity.medium`: Een pagina bevat een gemiddeld hoog aantal knooppunten die de renderprestaties kunnen beïnvloeden.
* `page.complexity.high`: Een pagina bevat een zeer groot aantal knooppunten die de renderprestaties kunnen beïnvloeden.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* Een groot aantal knooppunten in een pagina kan van invloed zijn op de renderprestaties.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="Implementatieleiding"
>abstract="De beste manier is de inhoudsstructuur te controleren om de complexiteit van de pagina te verminderen, wat weer de weergaveprestaties van de pagina zou verbeteren. Neem contact op met Adobe Support voor hulp en uitleg"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-ondersteuning"

* Ga als volgt te werk om het totale aantal knooppunten op een pagina te verminderen:
   * Controleer of er geen onnodige containers zijn.
   * Test of dezelfde lay-out kan worden bereikt met minder containers.
   * Vereenvoudig de pagina-inhoud.
   * Verminder de diepte van de knoopstructuur.
   * Refactor omvat alle ervaringsfragmenten voor eenvoud.
* Neem contact op met onze [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
