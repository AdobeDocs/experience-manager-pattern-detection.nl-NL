---
title: CAV
description: Help-pagina Patroondetectiecode.
exl-id: b2282da2-a028-4be7-914c-17dcd5d2902a
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---

# CAV {#cav}

Overtreding van inhoudsgebied

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_overview"
>title="Overtreding van inhoudsgebied"
>abstract="De CAV-code identificeert het patroon waarbij verschillende inhoudsgebieden worden gebruikt op een manier die in strijd is met de regels van de inhoudsclassificatie. Deze schending geeft u een overzicht van overlays, beperkte inhoud die mogelijk moet worden gewijzigd nadat deze is verplaatst naar AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Samenvoeging van verkoopbronnen"

`CAV` Identificeert het patroon waar verschillende inhoudsgebieden worden gebruikt op een manier die de regels van de inhoudsclassificatie schendt.

Verwerking van verzendverzoeken bepaalt hoe de inhoud van een bron, de `sling:resourceType` wordt met name gebruikt om het script te bepalen dat wordt gebruikt om de inhoud te renderen. Zie [Script zoeken](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/the-basics#locating-the-script) voor meer informatie . Sling biedt ook technieken voor het benaderen en samenvoegen van bronnen via &quot;Bedekkingen&quot; en &quot;Overschrijvingen&quot;. Deze worden beschreven als deel van [Samenvoeging van verkoopbronnen](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger) en in [Bedekkingen](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/overlays).

Om het voor klanten veiliger en gemakkelijker te maken om te begrijpen welke gebieden `/libs` zijn veilig te gebruiken en de inhoud te bedekken in `/libs` is geclassificeerd met &quot;mixin&quot;-eigenschappen: Public, Abstract, Final en Internal. Elke classificatie impliceert regels over hoe de inhoud gebruiker, geërft, of bedekt kan zijn. Zie [Duurzame verbeteringen](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades) voor een gedetailleerde beschrijving.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* Een AEM upgrade kan leiden tot weergaveproblemen en ander ongewenste gedrag.
* Beveiligingsupdates zijn niet effectief.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_guidance"
>title="Implementatieleiding"
>abstract="Patronen die met CAS zijn geïdentificeerd en waarbij verschillende inbreuken op inhoudsgebieden bestaan, moeten worden herzien. Definitieve en interne inhoudsclassificatiegebieden moeten worden vermeden. Neem contact op met de ondersteuning van de Adobe voor hulp of verduidelijking."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Duurzame verbeteringen"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Minimaliseer het gebruik van inhoudsoverlay voor die gevallen waarin het nodig is.
* Vermijd met name het bedekken van beperkte inhoud (definitieve en interne indeling).
* Overweeg wijzigingen aan te passen die afkomstig zijn van `/libs` na AEM upgrades, Service Pack of Cumulative Fix Pack-installaties.
* Contact opnemen met de [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om de problemen te verhelpen.
