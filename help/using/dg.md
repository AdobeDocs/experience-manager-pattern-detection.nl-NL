---
title: DG
description: Help-pagina Patroondetectiecode.
exl-id: 7ee3b177-bd79-41cd-abaf-ece3ae98ce03
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# DG {#dg}

Richtlijnen voor ontwikkelaars

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_overview"
>title="Richtlijnen voor ontwikkelaars"
>abstract="De code van het directoraat-generaal geeft afwijkingen aan van de geselecteerde richtsnoeren voor ontwikkeling voor AEM 6.5 en AEM as a Cloud Service. De beste praktijken kunnen het onderhoud en de prestaties van uw systeem verbeteren. Hoewel sommige van deze afwijkingen geen probleem in andere toepassingscontexten, met inbegrip van vorige versies van AEM kunnen zijn, kunnen zij problemen veroorzaken wanneer gebruikt met AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices" text="AEM ontwikkeling - Richtsnoeren en beste praktijken"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="as a Cloud Service ontwikkelingsrichtsnoeren AEM"


`DG`  Hiermee worden afwijkingen van geselecteerde ontwikkelrichtlijnen aangegeven voor [AEM 6,5](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices) en [AEM as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines). De beste praktijken kunnen het onderhoud en de prestaties van uw systeem verbeteren. Hoewel sommige van deze afwijkingen geen probleem in andere toepassingscontexten, met inbegrip van vorige versies van AEM kunnen zijn, kunnen zij problemen veroorzaken wanneer gebruikt met AEM as a Cloud Service.

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
   * Richtsnoeren voor [achtergrondtaken en langdurige taken](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#background-tasks-and-long-running-jobs) suggereert dat de code die als geplande taak wordt uitgevoerd ook moet veronderstellen dat de instantie het loopt, op elk ogenblik kan worden onderdrukt. Daarom moet de code veerkrachtig en herbruikbaar zijn.

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
>abstract="Controleer uw implementaties op het gebruik van de Planner van Commons van de Verkoop. Herstructureer hen aan het Verdelen van Banen, herstructureer hun taken van het systeemonderhoud, herzie het stromen van om het even welke binaire gegevens, en vernieuw hun code om met AEM as a Cloud Service compatibel te zijn."
>additional-url="https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing" text="Verkooptaken"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/operations/maintenance" text="Onderhoudstaken in AEM as a Cloud Service"

* `java.io.inputstream`
   * Gebruik een direct-binaire upload benadering waarin het binaire getal direct aan de datastore wordt toegevoegd.
   * Voor elementen die u gebruikt, raadpleegt u [aem-upload](https://github.com/adobe/aem-upload). Voor andere typen binaire getallen kan de aangepaste upload-logica worden gemodelleerd volgens hetzelfde patroon.

* `maintenance.task.configuration`
   * AEM as a Cloud Service bekijken [Onderhoudstaken](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/operations/maintenance) documentatie.
   * Zorg ervoor dat [Configuratie onderhoudstaken](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#maintenance-tasks-configuration-in-source-control) is in broncontrole.

* `sling.commons.scheduler`
   * Het gebruik van [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) with [Verkooptaken](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing), die ten minste eenmaal een uitvoeringsgarantie hebben.
   * Lange banen moeten worden vermeden.

* `unsupported.asset.api`
   * In plaats van de niet-ondersteunde API&#39;s van Asset Manager te gebruiken raadpleegt u [aem-upload](https://github.com/adobe/aem-upload).

* `javax.jcr.observation.EventListener`
   * In plaats van de gebeurtenislistener te gebruiken, wordt aangeraden het gebeurtenisafhandelingsmechanisme te verwijzen naar [Verkooptaken](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing) aangezien zij de garantie van verwerking biedt.

* `custom.guava.cache`
   * Indien nodig moeten er buiten AEM kooien worden gemaakt. Een externe caching-oplossing kan overwogen worden.
* Contact opnemen met de [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om de problemen te verhelpen.
