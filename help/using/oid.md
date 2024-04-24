---
title: OID
description: Help-pagina Patroondetectiecode.
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# OID {#oid}

Eak-indexdefinitie

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_overview"
>title="Eak-indexdefinitie"
>abstract="OID identificeert kwesties met betrekking tot de definities van eikenindexen. Het identificeert wijzigingen die aan standaarddefinities van de eikenindex zijn aangebracht. De code identificeert ook de definities van de aangepaste eikenindex die niet compatibel zijn met AEM as a Cloud Service. Het bericht voor elke OID-bevinding identificeert de index en verstrekt aanvullende informatie."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/operations/indexing#how-to-use" text="Richtlijnen voor indexering van inhoud"

`OID`  Identificeert kwesties met betrekking tot de definities van de eikenindex. Het identificeert wijzigingen die aan standaarddefinities van de eikenindex zijn aangebracht. De code identificeert ook de definities van de aangepaste eikenindex die niet compatibel zijn met AEM as a Cloud Service. Het bericht voor elke `OID` het zoeken identificeert de index en verstrekt extra informatie.

Subtypes worden gebruikt om de verschillende soorten informatie te identificeren:

* `index.rule.violation`: Een aangepaste eikenindex is niet compatibel met AEM as a Cloud Service
* `standard.index.modification`: Een wijziging in een standaard-eikenindex.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_guidance"
>title="Implementatieleiding"
>abstract="U kunt het beste alle aangepaste indexen bekijken en de structuur aanpassen aan de richtlijnen voor het indexeren van inhoud. Met de indexconverter kunt u bestaande definities van aangepaste eik-indexen migreren naar AEM as a Cloud Service compatibele definitie van aangepaste eik-indexen"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#oak-indexes" text="Richtlijnen voor verpakking"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/index-converter#refactoring-tools" text="Indexconversie"

* Wijzigingen in de standaarddefinities van de eiken-index kunnen tijdens een AEM-upgrade verloren gaan.
* De definities van eikels zijn onveranderlijk, zouden met de code van het klantenproject moeten worden verpakt, en zouden slechts moeten worden opgesteld gebruikend de Manager van de Wolk.
* Bij alle definities van de eikenindex moeten de naamgevingsconventie en andere regels voor eiken-indexen in AEM as a Cloud Service worden gevolgd. Anders kan dit ongewenste effecten veroorzaken.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_tools"
>title="Hulpmiddelen &amp; Middelen"
>abstract="Bekijk het WKND-verouderde project om te begrijpen hoe OID-schendingen in uw project kunnen worden opgelost. Ook, het Voorbeeld van de Schending van OID van het Overzicht op GitHub om te begrijpen hoe de erfenisindexen kunnen worden omgezet gebruikend het hulpmiddel van de Convertor van de Index en compatibel gemaakt met AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid" text="WKND-verouderd project"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid" text="Voorbeeld van OID-schending - GitHub"

* Los de schendingen van de indexregel op die in het bericht worden geïdentificeerd.
* Als u nieuwe of aangepaste Eak-indexdefinities wilt gebruiken, volgt u AEM as a Cloud Service [verpakkingsrichtlijnen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure).
* Aangepaste AEM standaardindexen en nieuwe aangepaste Eak-indexdefinities moeten de [richtlijnen voor indexering van inhoud](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/operations/indexing#preparing-the-new-index-definition) voor AEM as a Cloud Service.
* Controleren [verouderd](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) projecten en begrijpen hoe [OID-overtredingen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) kan worden gecorrigeerd en verenigbaar worden gemaakt met AEM as a Cloud Service.
* Contact opnemen met de [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om de problemen te verhelpen.
* Gebruik de [Indexconversie](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/index-converter#refactoring-tools) om bestaande definities van de Index van de Eik van de Douane aan AEM as a Cloud Service compatibele Definities van de Index van de Eik te migreren.
