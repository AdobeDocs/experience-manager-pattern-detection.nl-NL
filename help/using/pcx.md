---
title: PCX
description: Help-pagina Patroondetectiecode.
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
source-git-commit: b77a168fc8c075e8e41149a38df4d83fd2504a14
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

`PCX` Identificeert pagina&#39;s die veel knooppunten in hun structuur bevatten.

Subtypes worden gebruikt om de verschillende soorten informatie te identificeren:

* `page.complexity.medium`: Een pagina bevat een gemiddeld hoog aantal knooppunten dat de renderprestaties kan beïnvloeden.
* `page.complexity.high`: Een pagina bevat een groot aantal knooppunten die de renderprestaties kunnen beïnvloeden.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* Veel knooppunten in een pagina kunnen van invloed zijn op de renderprestaties.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="Implementatieleiding"
>abstract="U kunt de inhoudsstructuur het beste controleren om de complexiteit van pagina&#39;s te verminderen. Op zijn beurt kan dit de weergaveprestaties van pagina&#39;s verbeteren. Neem contact op met de ondersteuning van de Adobe voor hulp of verduidelijking."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Verminder het totale aantal knooppunten in een pagina door de volgende actie uit te voeren:
   * Controleer of er geen onnodige containers zijn.
   * Test of dezelfde indeling met minder containers kan worden bereikt.
   * Vereenvoudig de pagina-inhoud.
   * Verminder de diepte van de nodestructuur.
   * Refactor omvat alle ervaringsfragmenten voor eenvoud.
* Contacteer het [ AEM Team van de Steun ](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om kwesties te hebben die worden gericht.
