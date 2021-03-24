---
title: DG
description: Help-pagina Patroondetectiecode
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---


# DG {#dg}

Richtlijnen voor ontwikkelaars

## Achtergrond {#background}

`DG` geeft afwijkingen aan van bepaalde richtsnoeren voor ontwikkeling voor  [AEM 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html) en  [AEM als Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html). De beste praktijken kunnen het onderhoud en de prestaties van uw systeem verbeteren. Hoewel sommige van deze afwijkingen geen probleem in andere toepassingscontexten, met inbegrip van vorige versies van AEM kunnen zijn, kunnen zij problemen veroorzaken wanneer gebruikt met AEM als Cloud Service.

Subtypes worden gebruikt om de verschillende types van ontdekte schendingen te identificeren:

* `java.io.inputstream`: Het gebruik van code  `java.io.InputStream` in de toepassing.
* `maintenance.task.configuration`: De configuratie van een bepaalde periodieke onderhoudsactiviteit.
* `sling.commons.scheduler`: Het gebruik van de Sling Commons Scheduler-API voor een geplande taak.

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

* `java.io.inputstream`
   * Het stromen van binaire gegevens met `java.io.InputStream` kan geheugenmiddelen tot het punt van beïnvloeding van prestaties verbruiken. Dit is vooral een probleem vanwege het beperkte geheugen dat beschikbaar is in containers die in AEM als Cloud Service worden gebruikt.

* `maintenance.task.configuration`
   * Sommige onderhoudstaken die eerder expliciete configuratie vereiste worden nu automatisch gevormd en binnen AEM als Cloud Service beheerd.
   * De taakconfiguratie van het onderhoud in AEM als Cloud Service moet in broncontrole worden bewogen.

* `sling.commons.scheduler`
   * Toepassingen die afhankelijk zijn van achtergrondtaken met [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) werken mogelijk niet zoals verwacht omdat uitvoering niet kan worden gegarandeerd in AEM als Cloud Service.
   * AEM als richtlijnen voor de ontwikkeling van Cloud Servicen voor [achtergrondtaken en langdurige taken](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#background-tasks-and-long-running-jobs) suggereren dat de code die als een geplande taak wordt uitgevoerd, moet veronderstellen dat de instantie het loopt, op elk ogenblik kan worden verminderd. Daarom moet de code veerkrachtig en herbruikbaar zijn.

## Mogelijke oplossingen {#solutions}

* `java.io.inputstream`
   * Gebruik een direct-binaire upload benadering waarin het binaire getal direct aan de datastore wordt toegevoegd.
   * Gebruik [aem-upload](https://github.com/adobe/aem-upload) voor gebruik van middelen. Voor andere typen binaire getallen kan de aangepaste upload-logica worden gemodelleerd volgens hetzelfde patroon.

* `maintenance.task.configuration`
   * AEM controleren als Cloud Service [Onderhoudstaken](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/maintenance.html) documentatie.
   * Zorg ervoor dat [Configuratie van onderhoudstaak](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#maintenance-tasks-configuration-in-source-control) in broncontrole is.

* `sling.commons.scheduler`
   * Vervang het gebruik van [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) door [Sling Jobs](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing), die een minstens eenmaal uitvoeringsgarantie hebben.
   * Langlopende banen moeten zo mogelijk worden vermeden.

* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
