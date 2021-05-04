---
title: OID
description: Help-pagina Patroondetectiecode
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# OID {#oid}

Eak-indexdefinitie

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_overview"
>title="Eak-indexdefinitie"
>abstract="OID identificeert kwesties met betrekking tot de definities van eikenindexen. Het identificeert wijzigingen die aan standaarddefinities van de eikenindex zijn aangebracht. De code identificeert ook de definities van de aangepaste eikenindex die niet compatibel zijn met AEM als Cloud Service. Het bericht voor elke OID-bevinding zal de index identificeren en aanvullende informatie verstrekken."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html#how-to-use" text="Richtlijnen voor indexering van inhoud"

`OID` geeft kwesties aan die verband houden met definities van eikenindexen. Het identificeert wijzigingen die aan standaarddefinities van de eikenindex zijn aangebracht. De code identificeert ook de definities van de aangepaste eikenindex die niet compatibel zijn met AEM als Cloud Service. Het bericht voor elke `OID` het vinden zal de index identificeren en extra informatie verstrekken.

Subtypes worden gebruikt om de verschillende soorten informatie te identificeren:

* `custom.index.violation`: Een aangepaste eikenindex is niet compatibel met AEM als Cloud Service.
* `standard.index.modification`: Een wijziging in een standaard-eikenindex.

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_guidance"
>title="Implementatieleiding"
>abstract="U kunt het beste alle aangepaste indexen bekijken en deze opnieuw ordenen volgens de richtlijnen voor het indexeren van inhoud. Gebruik de omzetter van de Index om bestaande Definities van de Index van het Eak van de Douane te migreren om als Cloud Service compatibele Definitie van de Index van het Eikje te AEM"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#oak-indexes" text="Richtlijnen voor verpakking"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html#refactoring-tools" text="Indexconversie"

* Wijzigingen in de standaarddefinities van de eiken-index kunnen tijdens een AEM-upgrade verloren gaan.
* De definities van eikels zijn onveranderlijk, zouden met de code van het klantenproject moeten worden verpakt, en zouden slechts moeten worden opgesteld gebruikend de Manager van de Wolk.
* Alle definities van de eikenindex moeten de naamgevingsconventie en andere regels voor eiken-indexen in AEM als Cloud Service volgen. Diegenen die dat niet doen, kunnen ongewenst gedrag veroorzaken.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_tools"
>title="Hulpmiddelen &amp; Middelen"
>abstract="Bekijk het WKND-verouderde project om te begrijpen hoe OID-schendingen in uw project kunnen worden opgelost. Bekijk ook het voorbeeld OID-schending op Github om te begrijpen hoe verouderde indexen kunnen worden geconverteerd met het gereedschap Indexconverter en compatibel kunnen worden gemaakt met AEM als Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid" text="WKND-verouderd project"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid" text="Voorbeeld van OID-schending - Github"

* Los de schendingen van de indexregel op die in het bericht worden geïdentificeerd.
* Volg AEM als Cloud Service [verpakkingsrichtlijnen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) om nieuwe of aangepaste definities van de index van het eikel op te stellen.
* Aangepaste AEM standaardindexen en nieuwe definities van de indexindex van het Eak zouden [inhoud het indexeren richtlijnen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html#preparing-the-new-index-definition) voor AEM als Cloud Service moeten volgen.
* Bekijk het [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid)-project en begrijp hoe [OID-schendingen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) kunnen worden gecorrigeerd en compatibel kunnen worden gemaakt met AEM als Cloud Service.
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
* Gebruik de [Indexconverter](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html#refactoring-tools) om bestaande definities van de Index van de Eik van de Douane aan AEM als Cloud Service compatibele Definities van de Index van de Eik van de Eik te migreren.
