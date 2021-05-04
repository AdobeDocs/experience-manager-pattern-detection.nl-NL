---
title: CAV
description: Help-pagina Patroondetectiecode
exl-id: b2282da2-a028-4be7-914c-17dcd5d2902a
translation-type: tm+mt
source-git-commit: 1966a3e83ab6b2247d9f1095c8965eac399e3b6e
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# CAV {#cav}

Overtreding van inhoudsgebied

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_overview"
>title="Overtreding van inhoudsgebied"
>abstract="De CAV-code identificeert het patroon waarbij verschillende inhoudsgebieden worden gebruikt op een manier die in strijd is met de regels van de inhoudclassificatie. Deze schending zou u een overzicht over overlays, beperkte inhoud geven die veranderingen zou kunnen vereisen zodra wij als Cloud Service AEM."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html#platform" text="Samenvoegen van verkoopbronnen"

`CAV` Hiermee geeft u het patroon aan waarin verschillende inhoudsgebieden worden gebruikt op een manier die in strijd is met de regels van de inhoudclassificatie.

Het verkopen verzoekverwerking bepaalt hoe de inhoud van een middel, zijn `sling:resourceType` bezit in het bijzonder, wordt gebruikt om het manuscript te bepalen dat aan het teruggeven van de inhoud zal worden gebruikt. Zie [Script](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html#locating-the-script) zoeken voor meer informatie. Sling biedt ook technieken voor het benaderen en samenvoegen van bronnen via &quot;Bedekkingen&quot; en &quot;Overschrijvingen&quot;. Deze worden beschreven als deel van [Sling Resource Merger](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html) en in [Overlays](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html).

Om het voor klanten veiliger en gemakkelijker te maken om te begrijpen welke gebieden van `/libs` veilig zijn om te gebruiken en de inhoud in `/libs` te bedekken is geclassificeerd met &quot;mixin&quot;eigenschappen: Openbaar, Abstract, Definitief en Intern. Elke classificatie impliceert regels over hoe de inhoud gebruiker, geërft, of bedekt kan zijn. Zie [Duurzame verbeteringen](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html) voor een gedetailleerde beschrijving.

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

* Een AEM upgrade kan leiden tot weergaveproblemen en ander ongewenste gedrag.
* Beveiligingsupdates zijn niet effectief.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_guidance"
>title="Implementatieleiding"
>abstract="Patronen die met CAS zijn geïdentificeerd en waarbij een ander inhoudsgebied wordt geschonden, moeten worden herzien. Definitieve en interne gebieden voor de classificatie van inhoud moeten worden vermeden. Neem contact op met Adobe Support voor hulp en verduidelijkingen."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html" text="Duurzame verbeteringen"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-ondersteuning"

* Minimaliseer het gebruik van inhoudsoverlay voor die gevallen waarin het nodig is.
* Vermijd met name het bedekken van beperkte inhoud (definitieve en interne indeling).
* Overweeg wijzigingen die afkomstig zijn van `/libs` aan te passen na AEM upgrades, ServicePack- of CumulativeFixPack-installaties.
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
