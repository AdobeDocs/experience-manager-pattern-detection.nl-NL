---
title: REP
description: Help-pagina Patroondetectiecode
translation-type: tm+mt
source-git-commit: 7d05067fc624571e6fe520e2a1addd5dff8acbd8
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---


# [!DNL REP] {#rep}

Replication Agent

## Achtergrond {#background}

`REP` identificeert toegelaten replicatieagenten. Deze worden gerapporteerd vanwege het potentieel voor problemen die moeten worden aangepakt bij de upgrade naar AEM als Cloud Service.

AEM als Cloud Service gebruikt [Sling Content Distribution](https://sling.apache.org/documentation/bundles/content-distribution.html) om inhoud van auteur naar publicatieomgevingen te distribueren. Dit wordt gedaan buiten AEM runtime gebruikend de pijpleidingsdienst van Adobe I/O. Dit wordt automatisch gevormd in provisioned AEM als milieu van de Cloud Service.

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

* De configuratie van replicatie is veranderd met AEM als Cloud Service. Alle huidige replicatieagenten zouden moeten worden herzien om te zien welke door standaardvermogen worden vervangen, welke configuraties aan code moeten worden verplaatst, en die niet worden gesteund.
* Om het even welk gebruik van replicatieagenten in douanecode of werkschema&#39;s zou moeten worden herzien terwijl bevordering aan AEM als Cloud Service.
* Omgekeerde replicatie wordt aanvankelijk niet ondersteund in AEM als Cloud Service.
* Er is geen behoefte om een afzonderlijke verzender te vormen flush agent. Dit wordt automatisch gevormd in de AEM als milieu van de Cloud Service.

## Mogelijke oplossingen {#solutions}

* Zie de AEM als Cloud Service [Ontwikkelingsrichtlijnen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#no-reverse-replication-agents) en versienota&#39;s voor [replicatiemiddelen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#replication-agents).
* Het overzicht, de refactor, en optimaliseert functionaliteit direct afhankelijk van replicatieagenten om bedrijfstaken uit te voeren.
* Zie hoe [replicatie](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#replication) door plaatsing in AEM als Cloud Service wordt beïnvloed.
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
