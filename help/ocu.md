---
title: OCU
description: Help-pagina Patroondetectiecode
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# OCU {#ocu}

Verouderd codegebruik

## Achtergrond {#background}

`OCU` geeft de situatie aan waarin sommige JCR-knooppunten, zoals Sling- of AEM-componenten of OSGi-API-exportbewerkingen, op een niet-compatibele manier worden gewijzigd of verwijderd. De klant is wellicht niet op de hoogte van deze wijziging voordat een upgrade wordt uitgevoerd. Ze kunnen worden bijgewerkt naar een niet-compatibele versie of zijn helemaal niet beschikbaar.

Aangezien de oude versies niet standaard worden geïnstalleerd, werkt de klantentoepassing mogelijk niet correct.

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

* De functionaliteit die afhankelijk is van een component die afgekeurde componenten of API&#39;s gebruikt, kan worden verbroken en wordt na een upgrade mogelijk niet correct omgezet.
* Sommige functies van de klanttoepassing of bepaalde AEM werken mogelijk niet correct of zijn mogelijk niet actief na een upgrade.

## Mogelijke oplossingen {#solutions}

* Korte termijn: Installatie van compatibiliteitspakket kan helpen.
* Langdurig: Pas de klantcode aan om de nieuwste versie van AEM componenten of API&#39;s te gebruiken.
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
