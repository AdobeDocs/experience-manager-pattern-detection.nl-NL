---
title: ASO
description: Help-pagina Patroondetectiecode
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---


# ASO {#aso}

Systeemoverzicht AEM

## Achtergrond {#background}

`ASO` identificeert algemene informatie over de AEM instantie. Elke bevinding biedt één waarde voor een bepaald type systeeminformatie.

Subtypes worden gebruikt om verschillende soorten informatie te identificeren:

* `aem.version`: De AEM versie.
* `aem.product`: Detectie van het gebruik van een AEM product (handel, Forms, enz.).
* `node.count`: Het aantal knooppunten van een bepaald type (Pagina, Element, enz.).
* `node.store`: Het implementatietype van de knoopopslag (SegmentNodeStore, DocumentNodeStore).
* `data.store`: Het implementatietype voor gegevensopslag (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task`: Een onderhoudstaak.
* `slow.query`: Een langzame query.

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

* De AEM versie, knooptellingen, en de de implementatietypen van de archiefopslag en van de gegevensopslag worden verstrekt voor informatiedoeleinden.
* De aangepaste toepassing kan afhankelijk zijn van producten of functies die niet in AEM als Cloud Service beschikbaar zijn.
* Een upgrade met niet-ondersteunde functies kan resulteren in een mislukte upgrade en een niet-functionele toepassing.

## Mogelijke oplossingen {#solutions}

* AEM upgrades met niet-ondersteunde producten of functies worden niet aanbevolen en worden mogelijk niet ondersteund.
* Bekijk de [releaseopmerkingen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html) voor meer informatie over de laatste wijzigingen in AEM als Cloud Service.
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
