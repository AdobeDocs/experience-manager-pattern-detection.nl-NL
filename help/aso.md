---
title: ASO
description: Help-pagina Patroondetectiecode
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
source-git-commit: 3e05ecb2c78b0ebf97d334cf592347b54255c75f
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%

---

# ASO {#aso}

Systeemoverzicht AEM

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="Systeemoverzicht AEM"
>abstract="ASO-code identificeert algemene informatie over de AEM. Elke vondst verstrekt één waarde van een bepaald type van systeeminformatie die in uw migratieplanning en refactoring inspanning kan helpen."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="AEM as a Cloud Service - Opmerkingen bij de release"

`ASO` identificeert algemene informatie over de AEM instantie. Elke bevinding biedt één waarde voor een bepaald type systeeminformatie.

Subtypes worden gebruikt om verschillende soorten informatie te identificeren:

* `aem.version`: De AEM versie.
* `aem.product`: Detectie van het gebruik van een AEM product (handel, Forms, enz.).
* `node.count`: Het aantal knooppunten van een bepaald type (pagina, element, enz.) en het totaal aan knooppunten.
* `node.store`: Het implementatietype van de knoopopslag (SegmentNodeStore, DocumentNodeStore) en zijn grootte.
* `data.store`: Het implementatietype voor gegevensopslag (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task`: Een onderhoudstaak.
* `slow.query`: Een langzame query.
* `group.membership`: Het aantal gebruikers en subgroepen (alleen directe/gedeclareerde leden) in een groep.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* De AEM versie, knooptellingen, groepslidmaatschap en knoopopslag en de implementatietypen van de gegevensopslag worden verstrekt voor informatiedoeleinden.
* De aangepaste toepassing kan afhankelijk zijn van producten of functies die niet beschikbaar zijn in AEM as a Cloud Service.
* Een upgrade met niet-ondersteunde functies kan resulteren in een mislukte upgrade en een niet-functionele toepassing.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Implementatieleiding"
>abstract="Informatie die via ASO-code wordt weergegeven, biedt algemene informatie voor uw AEM omgeving, zoals versie, productinvoegtoepassingen, systeeminformatie. Deze informatie moet worden gecontroleerd voor niet-ondersteunde producten of functies in AEM as a Cloud Service. Neem contact op met Adobe Support voor hulp en verduidelijkingen."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-ondersteuning"

* AEM upgrades met niet-ondersteunde producten of functies worden niet aanbevolen en worden mogelijk niet ondersteund.
* Controleer de [releaseopmerkingen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html) voor meer informatie over de meest recente wijzigingen in AEM as a Cloud Service.
* Neem contact op met onze [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
