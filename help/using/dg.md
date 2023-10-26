---
title: DG
description: Help-pagina Patroondetectiecode
exl-id: 7ee3b177-bd79-41cd-abaf-ece3ae98ce03
source-git-commit: 65335d21a5035f023577c74fd073e0160a053932
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 1%

---

# DG {#dg}

Richtlijnen voor ontwikkelaars

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_overview"
>title="Richtlijnen voor ontwikkelaars"
>abstract="De code van het directoraat-generaal geeft afwijkingen aan van de geselecteerde richtsnoeren voor ontwikkeling voor AEM 6.5 en AEM as a Cloud Service. De beste praktijken kunnen het onderhoud en de prestaties van uw systeem verbeteren. Hoewel sommige van deze afwijkingen geen probleem in andere toepassingscontexten, met inbegrip van vorige versies van AEM kunnen zijn, kunnen zij problemen veroorzaken wanneer gebruikt met AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html" text="AEM ontwikkeling - Richtlijnen en beste praktijken"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html" text="Ontwikkelingsrichtlijnen voor AEM as a Cloud Service"


`DG` identificeert afwijkingen van geselecteerde ontwikkelingrichtsnoeren voor [AEM 6,5](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html) en [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html). De beste praktijken kunnen het onderhoud en de prestaties van uw systeem verbeteren. Hoewel sommige van deze afwijkingen geen probleem in andere toepassingscontexten, met inbegrip van vorige versies van AEM kunnen zijn, kunnen zij problemen veroorzaken wanneer gebruikt met AEM as a Cloud Service.

Subtypes worden gebruikt om de verschillende types van ontdekte schendingen te identificeren:

* `java.io.inputstream`: Het gebruik van `java.io.InputStream` in de toepassingscode.
* `maintenance.task.configuration`: De configuratie van een bepaalde periodieke onderhoudsactiviteit.
* `sling.commons.scheduler`: Het gebruik van de Sling Commons Scheduler-API voor een geplande taak.
* `unsupported.asset.api`: Het gebruik van niet-ondersteunde API&#39;s van Asset Manager in de toepassingscode.
* `javax.jcr.observation.EventListener`: Het gebruik van Event Listener in toepassingscode.
* `custom.guava.cache`: Het gebruik van Guava Cache in toepassingscode.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* `java.io.inputstream`
   * Streaming van binaire gegevens met `java.io.InputStream` kan geheugenbronnen gebruiken om de prestaties te beïnvloeden. Dit is vooral een probleem vanwege de beperkte hoeveelheid geheugen die beschikbaar is in containers die in AEM as a Cloud Service worden gebruikt.

* `maintenance.task.configuration`
   * Sommige onderhoudstaken die eerder expliciete configuratie vereiste worden nu automatisch gevormd en binnen as a Cloud Service AEM beheerd.
   * De configuratie van de onderhoudstaak in AEM as a Cloud Service moet in broncontrole worden bewogen.

* `sling.commons.scheduler`
   * Toepassingen die afhankelijk zijn van achtergrondtaken die [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) werkt mogelijk niet zoals verwacht, omdat uitvoering niet kan worden gegarandeerd in AEM as a Cloud Service.
   * AEM richtsnoeren voor as a Cloud Service ontwikkeling [achtergrondtaken en langdurige taken](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#background-tasks-and-long-running-jobs) suggereert dat de code die als geplande taak wordt uitgevoerd moet veronderstellen dat de instantie het loopt, op elk ogenblik kan worden onderdrukt. Daarom moet de code veerkrachtig en herbruikbaar zijn.

* `unsupported.asset.api`
   * De volgende API&#39;s van AssetManager worden gemarkeerd als niet-ondersteund op AEM as a Cloud Service.
      * createAssetForBinary
      * getAssetForBinary
      * removeAssetForBinary
      * createAsset

* `javax.jcr.observation.EventListener`
   * Toepassingen die afhankelijk zijn van de gebeurtenislistener werken mogelijk niet zoals verwacht, omdat de uitvoering niet kan worden gegarandeerd.

* `custom.guava.cache`
   * Het gebruik van de Guava-cache kan prestatieproblemen veroorzaken bij AEM.


## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_guidance"
>title="Implementatieleiding"
>abstract="Volgens AEM ontwikkelings richtlijnen &amp; beste praktijken, zouden de Klanten hun implementaties over gebruik van het Verdelen van de Planner van Commons moeten herzien en hen herstructureren aan het Verlenen van Banen, hun systeemonderhoudstaken herstructureren, het stromen van om het even welke binaire gegevens herzien en hun code om met AEM as a Cloud Service in overeenstemming te zijn te zijn."
>additional-url="https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing" text="Verkooptaken"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/maintenance.html" text="Onderhoudstaken in AEM as a Cloud Service"

* `java.io.inputstream`
   * Gebruik een direct-binaire upload benadering waarin het binaire getal direct aan de datastore wordt toegevoegd.
   * Gebruik deze optie voor gebruik van middelen [aem-upload](https://github.com/adobe/aem-upload). Voor andere typen binaire getallen kan de aangepaste upload-logica worden gemodelleerd volgens hetzelfde patroon.

* `maintenance.task.configuration`
   * AEM as a Cloud Service bekijken [Onderhoudstaken](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/maintenance.html) documentatie.
   * Zorg ervoor dat [Configuratie onderhoudstaken](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#maintenance-tasks-configuration-in-source-control) is in broncontrole.

* `sling.commons.scheduler`
   * Het gebruik van [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) with [Verkooptaken](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing), die ten minste eenmaal een uitvoeringsgarantie hebben.
   * Langlopende banen moeten zo mogelijk worden vermeden.

* `unsupported.asset.api`
   * Gebruik in plaats van de niet-ondersteunde API&#39;s van Asset Manager [aem-upload](https://github.com/adobe/aem-upload).

* `javax.jcr.observation.EventListener`
   * In plaats van de gebeurtenislistener te gebruiken, wordt aangeraden het gebeurtenisafhandelingsmechanisme te verwijzen naar [Verkooptaken](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing) aangezien zij de garantie van verwerking biedt.

* `custom.guava.cache`
   * Indien nodig moeten er buiten AEM kooien worden gemaakt. Een externe caching-oplossing kan overwogen worden.
* Neem contact op met onze [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
