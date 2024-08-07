---
title: ASO
description: Help-pagina Patroondetectiecode.
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# ASO {#aso}

Systeemoverzicht AEM

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="Systeemoverzicht AEM"
>abstract="ASO-code identificeert algemene informatie over de AEM. Elke vondst verstrekt één waarde van een bepaald type van systeeminformatie die in uw migratieplanning en refactoring inspanning kan helpen."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service - Opmerkingen bij de release"

`ASO` Hiermee wordt algemene informatie over de AEM opgegeven. Elke bevinding biedt één waarde voor een bepaald type systeeminformatie.

Subtypes worden gebruikt om verschillende soorten informatie te identificeren:

* `aem.version`: De AEM versie.
* `aem.product`: detectie van het gebruik van een AEM product (Commerce, Forms, enzovoort).
* `node.count`: Het aantal knooppunten van een bepaald type (Pagina, Element, enzovoort) en het totaal aan knooppunten.
* `node.store`: Het implementatietype van de nodenopslag (SegmentNodeStore, DocumentNodeStore) en zijn grootte.
* `data.store`: Het implementatietype voor de gegevensopslag (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task`: Een onderhoudstaak.
* `slow.query`: een langzame query.
* `group.membership`: Het aantal gebruikers en subgroepen (alleen directe leden/gedeclareerde leden) in een groep.
* `cqtag.count`: Het aantal gecodeerde CQ-elementen.
* `smarttag.count`: Het aantal slimme gelabelde elementen.
* `ccom.version`: De versie van het pakket Core Component.
* `instance.type`: Het AEM instantietype (auteur|publish).
* `unprocessed.asset.count`: Het aantal onverwerkte elementen.
* `vanity.url.count`: Het aantal vanity URL&#39;s.
* `index.size`: Totale migreerbare indexgrootte van Luceen.
* `workflow.count`: Het aantal workflows van de auteur in de staat van uitvoering en schaal.
* `jvm.arguments`: De JVM-argumenten die aan de opdrachtregel worden toegevoegd bij het starten van de AEM.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* De AEM versie, knooppuntaantallen, groepslidmaatschap, knoopopslag, de types van implementatie van de gegevensopslag, CQ Telling van de Markering, Slimme Telling van de Markering, de versie van de Component van de Kern, AEM instantietype, en Onverwerkte activa worden verstrekt voor informatiedoeleinden.
* Het hogere aantal vanity URL&#39;s (>1000) kan laden op de Dispatcher en de Publish-servers met dure query&#39;s.
* De aangepaste toepassing kan afhankelijk zijn van producten of functies die niet beschikbaar zijn in AEM as a Cloud Service.
* Een upgrade met niet-ondersteunde functies kan resulteren in een mislukte upgrade en een niet-functionele toepassing.
* Een hoog aantal workflows van auteurs in een actieve of verouderde status kan de prestaties nadelig beïnvloeden.
* De langzame vragen kunnen de prestaties van het systeem degraderen.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Implementatieleiding"
>abstract="De informatie die door middel van code van ASO wordt blootgesteld verstrekt algemene informatie voor uw AEM milieu met inbegrip van versie, product toe:voegen-ons, en systeeminformatie. Bekijk deze voor niet-ondersteunde producten of functies in AEM as a Cloud Service. Neem contact op met de ondersteuning van de Adobe voor hulp of verduidelijking."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* AEM upgrades met niet-ondersteunde producten of functies worden niet aanbevolen en worden mogelijk niet ondersteund.
* De onverwerkte elementen moeten worden verwerkt en de eigenschap `dam:assetState` op het knooppunt `jcr:content` van het element moet worden ingesteld op &quot;processing&quot;. Of u moet deze elementen verwijderen uit de migratieset voordat u naar AEMaaCS gaat.
* URL&#39;s met Vanity kunnen worden vervangen door Apache Rewrites.
* Zie [ documentatie ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/bestpractices/troubleshooting-slow-queries) voor het oplossen van problemen langzame vragen.
* Zie de [ versienota&#39;s ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current) als u meer over de recentste veranderingen in AEM as a Cloud Service wilt leren.
* Contacteer het [ AEM Team van de Steun ](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om kwesties te hebben die worden gericht.
