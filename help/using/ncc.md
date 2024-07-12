---
title: NCC
description: Help-pagina Patroondetectiecode.
exl-id: 4a374956-c64e-43fc-8279-ed25f6ed5cb0
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# NCC {#ncc}

Niet-compatibele wijzigingen

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_overview"
>title="Niet-compatibele wijzigingen"
>abstract="NCC stelt vast in welke situatie sommige JCR-knooppunten of -bundels op een niet-compatibele manier worden gewijzigd. Het is mogelijk dat de klant niet op de hoogte is van deze wijziging voordat een upgrade wordt uitgevoerd."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Opvallende wijzigingen - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Opmerkingen bij de release - AEM as a Cloud Service"

`NCC` Hiermee wordt aangegeven in welke situatie sommige JCR-knooppunten of -bundels niet-compatibel zijn gewijzigd. Het is mogelijk dat de klant niet op de hoogte is van deze wijziging voordat een upgrade wordt uitgevoerd.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* De functionaliteit die afhankelijk is van een component die niet-compatibele wijzigingen gebruikt, kan worden verbroken en niet correct worden omgezet.
* Sommige functies van de klanttoepassing of bepaalde AEM werken mogelijk niet correct na een upgrade.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_guidance"
>title="Implementatieleiding"
>abstract="Aangepaste code controleren is de beste manier om te controleren of alleen compatibele Sling-componenten worden bedekt of waarnaar wordt verwezen. Neem contact op met de ondersteuning van de Adobe voor hulp of verduidelijking."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/overlays#platform" text="Bedekkingen"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Bedekking of verwijzing alleen compatibele Sling-componenten.
* U kunt bronnen die afkomstig zijn van `/libs` of bundels aanpassen na een AEM upgrade.
* Contacteer het [ AEM Team van de Steun ](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om kwesties te hebben die worden gericht.
