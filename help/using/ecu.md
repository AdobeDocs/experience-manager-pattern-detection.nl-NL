---
title: ECU
description: Help-pagina Patroondetectiecode
exl-id: fd061001-b00e-44ae-bd31-71bd2fa733cd
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# ECU {#ecu}

VEROUDERD: Gebruik van externe inhoud (vervangen door CAV, schending van inhoudsgebied)

## Achtergrond {#background}

`ECU` Hiermee geeft u het patroon aan waarin verschillende inhoudsgebieden worden gebruikt op een manier die in strijd is met de regels van de inhoudclassificatie.

Verwerking van verzendverzoeken bepaalt hoe de inhoud van een bron, de `sling:resourceType` Deze eigenschap wordt met name gebruikt om het script te bepalen dat wordt gebruikt voor het renderen van de inhoud. (Zie [Script zoeken](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html#locating-the-script) voor meer informatie .) Sling biedt ook technieken voor het benaderen en samenvoegen van bronnen via &quot;Bedekkingen&quot; en &quot;Overschrijvingen&quot;. Deze worden beschreven als deel van [Samenvoegen van verkoopbronnen](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html) en in [Bedekkingen](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html).

Om het voor klanten veiliger en gemakkelijker te maken te begrijpen welke gebieden `/libs` zijn veilig te gebruiken en de inhoud te bedekken in `/libs` is geclassificeerd met &quot;mixin&quot;-eigenschappen: Openbaar, Abstract, Definitief en Intern. Elke classificatie impliceert regels over hoe de inhoud gebruiker, geërft, of bedekt kan zijn. Zie [Duurzame verbeteringen](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html) voor een gedetailleerde beschrijving.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* Een AEM upgrade kan leiden tot weergaveproblemen en ander ongewenste gedrag.
* Beveiligingsupdates zijn niet effectief.

## Mogelijke oplossingen {#solutions}

* Minimaliseer het gebruik van inhoudsoverlay voor die gevallen waarin het nodig is.
* Vermijd met name het bedekken van beperkte inhoud (definitieve en interne indeling).
* Overweeg wijzigingen aan te passen die afkomstig zijn van `/libs` na AEM upgrades, ServicePack- of CumulativeFixPack-installaties.
* Neem contact op met onze [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
