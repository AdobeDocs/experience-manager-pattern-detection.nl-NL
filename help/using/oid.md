---
title: OID
description: Help-pagina Patroondetectiecode.
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# OID {#oid}

Oak Index Definition

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_overview"
>title="Oak Index Definition"
>abstract="OID identificeert kwesties met betrekking tot de indexdefinities van Oak. Het identificeert wijzigingen die zijn aangebracht aan de standaardindexdefinities van Oak. Ook worden aangepaste Oak-indexdefinities geïdentificeerd die niet compatibel zijn met AEM as a Cloud Service. Het bericht voor elke OID-bevinding identificeert de index en verstrekt aanvullende informatie."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/operations/indexing#how-to-use" text="Richtlijnen voor indexering van inhoud"

`OID` Hiermee worden problemen geïdentificeerd die te maken hebben met Oak-indexdefinities. Het identificeert wijzigingen die zijn aangebracht aan de standaardindexdefinities van Oak. Ook worden aangepaste Oak-indexdefinities geïdentificeerd die niet compatibel zijn met AEM as a Cloud Service. Het bericht voor elke `OID` -bevinding identificeert de index en verstrekt aanvullende informatie.

Subtypes worden gebruikt om de verschillende soorten informatie te identificeren:

* `index.rule.violation`: Een aangepaste Oak-index die niet compatibel is met AEM as a Cloud Service
* `standard.index.modification`: een wijziging in een standaard Oak-index.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_guidance"
>title="Implementatieleiding"
>abstract="U kunt het beste alle aangepaste indexen bekijken en de structuur aanpassen aan de richtlijnen voor het indexeren van inhoud. Met de indexconverter kunt u bestaande aangepaste Oak-indexdefinities migreren naar aangepaste Oak-indexdefinitie die compatibel is met AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#oak-indexes" text="Richtlijnen voor verpakking"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/index-converter#refactoring-tools" text="Indexconversie"

* Wijzigingen in standaard Oak-indexdefinities kunnen tijdens een AEM-upgrade verloren gaan.
* De definities van Oak zijn onveranderlijk, zouden met de code van het klantenproject moeten worden verpakt, en zouden slechts moeten worden opgesteld gebruikend Cloud Manager.
* Alle Oak-indexdefinities moeten de naamgevingsconventie en andere regels voor Oak-indexen in AEM as a Cloud Service volgen. Anders kan dit ongewenste effecten veroorzaken.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_tools"
>title="Hulpmiddelen en Middelen"
>abstract="Bekijk het WKND-verouderde project om te begrijpen hoe OID-schendingen in uw project kunnen worden opgelost. Lees ook het voorbeeld van OID-schending op GitHub. Zo kunt u begrijpen hoe verouderde indexen kunnen worden geconverteerd met het gereedschap Index converteren en compatibel worden gemaakt met AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid" text="WKND-verouderd project"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid" text="Voorbeeld van OID-schending - GitHub"

* Los de schendingen van de indexregel op die in het bericht worden geïdentificeerd.
* Om nieuwe of de indexdefinities van douaneOak op te stellen, volg AEM as a Cloud Service [ verpakkingsrichtlijnen ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure).
* De aangepaste AEM standaardindexen en de nieuwe de indexdefinities van douaneOak zouden de [ inhoud het indexeren richtlijnen ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/operations/indexing#preparing-the-new-index-definition) voor AEM as a Cloud Service moeten volgen.
* Het overzicht [ wknd-erfenis ](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) project en begrijpt hoe [ de schendingen van OID ](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) kunnen worden verbeterd en compatibel gemaakt met AEM as a Cloud Service.
* Contacteer het [ AEM Team van de Steun ](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om kwesties te hebben die worden gericht.
* Gebruik de [ Omzetter van de Index ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/index-converter#refactoring-tools) om bestaande de indexdefinities van Oak van de Douane aan AEM as a Cloud Service compatibele de indexdefinities van Oak van de Douane te migreren.
