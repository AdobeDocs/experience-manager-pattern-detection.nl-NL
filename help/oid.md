---
title: OID
description: Help-pagina Patroondetectiecode
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
source-git-commit: 71fd8c278f5fa2c44e489316be36d7d0376fe695
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
>abstract="OID identificeert kwesties met betrekking tot de definities van eikenindexen. Het identificeert wijzigingen die aan standaarddefinities van de eikenindex zijn aangebracht. De code identificeert ook de definities van de aangepaste eikenindex die niet compatibel zijn met AEM as a Cloud Service. Het bericht voor elke OID-bevinding zal de index identificeren en aanvullende informatie verstrekken."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html#how-to-use" text="Richtlijnen voor indexering van inhoud"

`OID` geeft kwesties aan die verband houden met definities van eikenindexen. Het identificeert wijzigingen die aan standaarddefinities van de eikenindex zijn aangebracht. De code identificeert ook de definities van de aangepaste eikenindex die niet compatibel zijn met AEM as a Cloud Service. Het bericht voor elke `OID` zoeken zal de index identificeren en aanvullende informatie verstrekken .

Subtypes worden gebruikt om de verschillende soorten informatie te identificeren:

* `index.rule.violation`: Een aangepaste eikenindex is niet compatibel met AEM as a Cloud Service.
* `standard.index.modification`: Een wijziging in een standaard-eikenindex.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_guidance"
>title="Implementatieleiding"
>abstract="U kunt het beste alle aangepaste indexen bekijken en deze opnieuw ordenen volgens de richtlijnen voor het indexeren van inhoud. Gebruik de Indexconverter om bestaande definities van aangepaste eik-indexen te migreren naar AEM as a Cloud Service compatibele definitie van aangepaste eik-indexen"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#oak-indexes" text="Richtlijnen voor verpakking"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html#refactoring-tools" text="Indexconversie"

* Wijzigingen in de standaarddefinities van de eiken-index kunnen tijdens een AEM-upgrade verloren gaan.
* De definities van eikels zijn onveranderlijk, zouden met de code van het klantenproject moeten worden verpakt, en zouden slechts moeten worden opgesteld gebruikend de Manager van de Wolk.
* Alle definities van de eikenindex moeten de naamgevingsconventie en andere regels voor eiken-indexen in AEM als Cloud Service volgen. Diegenen die dat niet doen, kunnen ongewenst gedrag veroorzaken.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_tools"
>title="Hulpmiddelen &amp; Middelen"
>abstract="Bekijk het WKND-verouderde project om te begrijpen hoe OID-schendingen in uw project kunnen worden opgelost. Bekijk ook het voorbeeld OID-schending op Github om te begrijpen hoe verouderde indexen kunnen worden geconverteerd met het gereedschap Indexconverter en compatibel kunnen worden gemaakt met AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid" text="WKND-verouderd project"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid" text="Voorbeeld van OID-schending - Github"

* Los de schendingen van de indexregel op die in het bericht worden geïdentificeerd.
* AEM as a Cloud Service volgen [verpakkingsrichtlijnen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) om nieuwe of aangepaste Eak-indexdefinities te implementeren.
* Aangepaste AEM standaardindexen en nieuwe aangepaste Eak-indexdefinities moeten de [richtlijnen voor indexering van inhoud](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html#preparing-the-new-index-definition) voor AEM als Cloud Service.
* Controleren [verouderd](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) projecten en begrijpen hoe [OID-overtredingen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) kan worden gecorrigeerd en verenigbaar worden gemaakt met AEM as a Cloud Service.
* Neem contact op met onze [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
* De [Indexconversie](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html#refactoring-tools) om bestaande definities van de Index van de Eik van de Douane aan AEM as a Cloud Service compatibele Definities van de Index van de Eik te migreren.
