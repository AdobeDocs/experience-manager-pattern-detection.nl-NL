---
title: DG
description: Help-pagina Patroondetectiecode.
exl-id: 7ee3b177-bd79-41cd-abaf-ece3ae98ce03
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '596'
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
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="AEM as a Cloud Service-ontwikkelingsrichtsnoeren"


`DG` identificeert afwijkingen van geselecteerde ontwikkelingsrichtlijnen voor [ AEM 6.5 ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices) en [ AEM as a Cloud Service ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines). De beste praktijken kunnen het onderhoud en de prestaties van uw systeem verbeteren. Hoewel sommige van deze afwijkingen geen probleem in andere toepassingscontexten, met inbegrip van vorige versies van AEM kunnen zijn, kunnen zij problemen veroorzaken wanneer gebruikt met AEM as a Cloud Service.

Subtypes worden gebruikt om de verschillende types van ontdekte schendingen te identificeren:

* `java.io.inputstream`: het gebruik van `java.io.InputStream` in toepassingscode.
* `maintenance.task.configuration`: De configuratie van een bepaalde periodieke onderhoudsactiviteit.
* `sling.commons.scheduler`: Het gebruik van de Sling Commons Scheduler-API voor een geplande taak.
* `unsupported.asset.api`: Het gebruik van niet-ondersteunde API&#39;s van Asset Manager in de toepassingscode.
* `javax.jcr.observation.EventListener`: Het gebruik van Event Listener in toepassingscode.
* `custom.guava.cache`: Het gebruik van de cache van Guava in de toepassingscode.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* `java.io.inputstream`
   * Streaming van binaire gegevens met `java.io.InputStream` kan geheugenbronnen gebruiken om de prestaties te beïnvloeden. Dit probleem is te wijten aan het beperkte geheugen dat beschikbaar is in containers die in AEM as a Cloud Service worden gebruikt.

* `maintenance.task.configuration`
   * Sommige onderhoudstaken die voorheen expliciet moesten worden geconfigureerd, worden nu automatisch geconfigureerd en beheerd in AEM as a Cloud Service.
   * De configuratie van de onderhoudstaak in AEM as a Cloud Service moet in broncontrole worden bewogen.

* `sling.commons.scheduler`
   * De toepassingen afhankelijk van achtergrondtaken die [ gebruiken Sling Commons Planner ](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) zouden niet kunnen werken zoals verwacht omdat de uitvoering niet in AEM as a Cloud Service kan worden gewaarborgd.
   * De richtlijnen voor [ achtergrondtaken en de langlopende banen ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#background-tasks-and-long-running-jobs) suggereren dat de code als geplande taak moet ook veronderstellen dat de instantie het loopt, op elk ogenblik kan worden verminderd. Daarom moet de code veerkrachtig en herbruikbaar zijn.

* `unsupported.asset.api`
   * De volgende API&#39;s van AssetManager worden op AEM as a Cloud Service gemarkeerd als niet-ondersteund.
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
>abstract="Controleer uw implementaties op het gebruik van de Planner van Commons van de Verkoop. Herstructureer hen aan het Verdelen van Banen, herstructureer hun taken van het systeemonderhoud, herzie het stromen van om het even welke binaire gegevens, en vernieuw hun code om met AEM as a Cloud Service in overeenstemming te zijn."
>additional-url="https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing" text="Verkooptaken"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/operations/maintenance" text="Onderhoudstaken in AEM as a Cloud Service"

* `java.io.inputstream`
   * Gebruik een direct-binaire upload benadering waarin het binaire getal direct aan de datastore wordt toegevoegd.
   * Voor activa gebruiken gevallen, zie [ a-upload ](https://github.com/adobe/aem-upload). Voor andere typen binaire getallen kan de aangepaste upload-logica worden gemodelleerd volgens hetzelfde patroon.

* `maintenance.task.configuration`
   * De documentatie van de Taak van het Onderhoud van AEM as a Cloud Service van het overzicht [ ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/operations/maintenance).
   * Zorg ervoor dat [ Configuratie van de Taak van het Onderhoud ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#maintenance-tasks-configuration-in-source-control) in broncontrole is.

* `sling.commons.scheduler`
   * Vervang het gebruik van [ het Schuiven Planner van Commons ](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) met [ het Schuiven Banen ](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing), die een minstens eenmaal uitvoeringsgarantie hebben.
   * Lange banen moeten worden vermeden.

* `unsupported.asset.api`
   * In plaats van het gebruiken van niet gestaafde APIs van de Manager van Activa, zie [ aem-upload ](https://github.com/adobe/aem-upload).

* `javax.jcr.observation.EventListener`
   * In plaats van het gebruiken van de Listener van de Gebeurtenis, wordt het geadviseerd om het gebeurtenis behandelend mechanisme aan [ het Schuiven van Banen ](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing) te refactoreren aangezien het de garantie van verwerking verstrekt.

* `custom.guava.cache`
   * Indien nodig moeten er buiten AEM kooien worden gemaakt. Een externe caching-oplossing kan overwogen worden.
* Contacteer het [ AEM Team van de Steun ](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om kwesties te hebben die worden gericht.
