---
title: DG
description: Help-pagina Patroondetectiecode
exl-id: 7ee3b177-bd79-41cd-abaf-ece3ae98ce03
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 1%

---

# DG {#dg}

Richtlijnen voor ontwikkelaars

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_overview"
>title="Richtlijnen voor ontwikkelaars"
>abstract="De code van het directoraat-generaal geeft afwijkingen aan van de geselecteerde richtsnoeren voor ontwikkeling voor AEM 6.5 en AEM als Cloud Service. De beste praktijken kunnen het onderhoud en de prestaties van uw systeem verbeteren. Hoewel sommige van deze afwijkingen geen probleem in andere toepassingscontexten, met inbegrip van vorige versies van AEM kunnen zijn, kunnen zij problemen veroorzaken wanneer gebruikt met AEM als Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html" text="AEM ontwikkeling - Richtlijnen en beste praktijken"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html" text="Ontwikkelingsrichtlijnen voor AEM as a Cloud Service"


`DG` geeft afwijkingen van de geselecteerde richtsnoeren voor ontwikkeling voor  [AEM 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html) en  [AEM als Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html) aan. De beste praktijken kunnen het onderhoud en de prestaties van uw systeem verbeteren. Hoewel sommige van deze afwijkingen geen probleem in andere toepassingscontexten, met inbegrip van vorige versies van AEM kunnen zijn, kunnen zij problemen veroorzaken wanneer gebruikt met AEM als Cloud Service.

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

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_guidance"
>title="Implementatieleiding"
>abstract="Volgens AEM ontwikkelings richtlijnen &amp; beste praktijken, zouden de Klanten hun implementaties over gebruik van het Verdelen van de Planner van Commons moeten herzien en hen herstructureren aan het Verlenen van Banen, hun systeemonderhoudstaken herstructureren, het stromen van om het even welke binaire gegevens herzien en hun code om met AEM als Cloud Service in overeenstemming te zijn te zijn."
>additional-url="https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing" text="Verkooptaken"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/maintenance.html" text="Onderhoudstaken in AEM als Cloud Service"

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
