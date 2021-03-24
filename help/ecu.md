---
title: ECU
description: Help-pagina Patroondetectiecode
translation-type: tm+mt
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---


# ECU {#ecu}

VEROUDERD: Gebruik van externe inhoud (vervangen door CAV, schending van inhoudsgebied)

## Achtergrond {#background}

`ECU` Hiermee geeft u het patroon aan waarin verschillende inhoudsgebieden worden gebruikt op een manier die in strijd is met de regels van de inhoudclassificatie.

Het verkopen verzoekverwerking bepaalt hoe de inhoud van een middel, zijn `sling:resourceType` bezit in het bijzonder, wordt gebruikt om het manuscript te bepalen dat aan het teruggeven van de inhoud zal worden gebruikt. (Zie [Het script zoeken](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html#locating-the-script) voor meer informatie.) Sling biedt ook technieken voor het benaderen en samenvoegen van bronnen via &quot;Bedekkingen&quot; en &quot;Overschrijvingen&quot;. Deze worden beschreven als deel van [Sling Resource Merger](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html) en in [Overlays](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html).

Om het voor klanten veiliger en gemakkelijker te maken om te begrijpen welke gebieden van `/libs` veilig zijn om te gebruiken en de inhoud in `/libs` te bedekken is geclassificeerd met &quot;mixin&quot;eigenschappen: Openbaar, Abstract, Definitief en Intern. Elke classificatie impliceert regels over hoe de inhoud gebruiker, geërft, of bedekt kan zijn. Zie [Duurzame verbeteringen](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html) voor een gedetailleerde beschrijving.

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

* Een AEM upgrade kan leiden tot weergaveproblemen en ander ongewenste gedrag.
* Beveiligingsupdates zijn niet effectief.

## Mogelijke oplossingen {#solutions}

* Minimaliseer het gebruik van inhoudsoverlay voor die gevallen waarin het nodig is.
* Vermijd met name het bedekken van beperkte inhoud (definitieve en interne indeling).
* Overweeg wijzigingen die afkomstig zijn van `/libs` aan te passen na AEM upgrades, ServicePack- of CumulativeFixPack-installaties.
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
