---
title: MI
description: Help-pagina Patroondetectiecode
exl-id: fa47ac63-1b5d-43b3-8acd-4a71c3fa714e
source-git-commit: efb06dc7e00f91d4c080553df3153deb90b093f2
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# MI {#mi}

Probleem met verkeerde configuratie

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_overview"
>title="Probleem met verkeerde configuratie"
>abstract="MI identificeert configuratiekwesties op AEM instantie"

`MI`  Probleem met verkeerde configuratie identificeert configuratieproblemen bij AEM instantie.

Subtypes worden gebruikt om de verschillende soorten informatie te identificeren, zoals:

* `sling.job.max.parallel`: Identificeer de slingertaken waarbij de maximale parallelle configuratie is ingesteld op -1.
* `missing.maintenance.configuration`: Identificeer ontbrekende configuraties van onderhoudstaak.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* `sling.job.max.parallel`
   * De waarde -1 wordt vervangen door het aantal beschikbare processors. Dit kan prestatieproblemen veroorzaken bij AEM instantie.
* `missing.maintenance.configuration`
   * Ontbrekende configuraties van onderhoudstaken kunnen leiden tot prestatieverlies of beschadiging van instanties.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_guidance"
>title="Implementatieleiding"
>abstract="Neem contact op met de klantenservice voor hulp."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* `sling.job.max.parallel`
   * Het is raadzaam de waarde in te stellen op 0,5 om de helft van de beschikbare verwerkers te benutten.
* `missing.maintenance.configuration`
   * Opschonen van revisie: raadpleeg [Opschonen van revisie](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html). Het belangrijke deel met betrekking tot de configuratie is hier: [Revisie-opschoning - Tail en volledige compressie configureren](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html#how-to-configure-full-and-tail-compaction).
   * Lucene Binaries Cleanup: Gelieve te verwijzen naar [Operations-dashboard - opschonen van Lucene-binaire bestanden](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-dashboard.html#lucene-binaries-cleanup).
   * Verzameling opschonen van gegevensopslag: raadpleeg [Opruimverzameling gegevensopslag](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/data-store-garbage-collection.html).
   * Werkstroom leegmaken: raadpleeg [Regelmatig leegmaken van workflowinstanties](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/workflows-administering.html#regular-purging-of-workflow-instances).
   * AuditLog-onderhoudstaak: raadpleeg [Controle van logboekonderhoud](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-audit-log.html).
* Bereik uit naar onze [Klantenzorgteam van Experience Manager](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
