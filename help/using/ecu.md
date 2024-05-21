---
title: ECU
description: Help-pagina Patroondetectiecode.
exl-id: fd061001-b00e-44ae-bd31-71bd2fa733cd
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# ECU {#ecu}

VEROUDERD: gebruik van externe inhoud (vervangen door CAV, schending van inhoudsgebied)

## Achtergrond {#background}

`ECU`  Identificeert het patroon waar verschillende inhoudsgebieden worden gebruikt op een manier die de regels van de inhoudsclassificatie schendt.

Verwerking van verzendverzoeken bepaalt hoe de inhoud van een bron, de `sling:resourceType` wordt met name gebruikt om het script te bepalen dat wordt gebruikt om de inhoud te renderen. (Zie [Script zoeken](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/the-basics#locating-the-script) voor meer informatie .) Sling biedt ook technieken om bronnen te openen en samen te voegen via Bedekkingen en Overschrijvingen. Deze technieken worden beschreven als onderdeel van de [Samenvoeging van verkoopbronnen](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger) en in [Bedekkingen](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/overlays).

Om het voor klanten veiliger en gemakkelijker te maken om te begrijpen welke gebieden `/libs` zijn veilig te gebruiken en bedekken, de inhoud in `/libs` is geclassificeerd met &quot;mixin&quot;-eigenschappen:

* Openbaar
* Abstract
* Definitief
* Intern

Elke classificatie impliceert regels over hoe de inhoud gebruiker, geërft, of bedekt kan zijn. Zie [Duurzame verbeteringen](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades) voor een gedetailleerde beschrijving.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* Een AEM upgrade kan leiden tot weergaveproblemen en ander ongewenste gedrag.
* Beveiligingsupdates zijn niet effectief.

## Mogelijke oplossingen {#solutions}

* Minimaliseer het gebruik van inhoudsoverlay voor die gevallen waarin het nodig is.
* Vermijd met name het bedekken van beperkte inhoud (definitieve en interne indeling).
* Overweeg wijzigingen aan te passen die afkomstig zijn van `/libs` na AEM upgrades, Service Pack of Cumulative Fix Pack-installaties.
* Contact opnemen met de [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om de problemen te verhelpen.
