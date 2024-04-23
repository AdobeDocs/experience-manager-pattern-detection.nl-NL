---
title: PCX
description: Help-pagina Patroondetectiecode.
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# PCX {#pcx}

Complexiteit pagina

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_overview"
>title="Complexiteit pagina"
>abstract="PCX identificeert pagina&#39;s die een groot aantal knooppunten in hun structuur bevatten."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Opvallende wijzigingen - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service - Opmerkingen bij de release"

PCX identificeert pagina&#39;s die vele knopen in hun structuur bevatten.

Subtypes worden gebruikt om de verschillende soorten informatie te identificeren:

* `page.complexity.medium`: Een pagina bevat een matig hoog aantal knooppunten dat de renderprestaties kan beïnvloeden.
* `page.complexity.high`: Een pagina bevat een groot aantal knooppunten die de renderprestaties kunnen beïnvloeden.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* Veel knooppunten in een pagina kunnen van invloed zijn op de renderprestaties.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="Implementatieleiding"
>abstract="De beste manier is de inhoudsstructuur te controleren om de complexiteit van pagina&#39;s te verminderen, wat op zijn beurt de weergaveprestaties van pagina&#39;s zou verbeteren. Neem contact op met de ondersteuning van de Adobe voor hulp of verduidelijking."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Verminder het totale aantal knooppunten in een pagina door de volgende actie uit te voeren:
   * Controleer of er geen onnodige containers zijn.
   * Test of dezelfde indeling met minder containers kan worden bereikt.
   * Vereenvoudig de pagina-inhoud.
   * Verminder de diepte van de nodestructuur.
   * Refactor omvat alle ervaringsfragmenten voor eenvoud.
* Contact opnemen met de [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om de problemen te verhelpen.
