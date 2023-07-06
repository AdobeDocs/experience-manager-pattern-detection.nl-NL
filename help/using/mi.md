---
title: MI
description: Help-pagina Patroondetectiecode
source-git-commit: aa05ebcb54c6945a903c76add4f31e3279cd05b5
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

* `sling.job.max.parallel`: Identificeer de slingerbanen waar maximum parallelle configuratie aan -1 wordt geplaatst.
* `missing.maintenance.configuration`: Ontbrekende configuraties van onderhoudstaken identificeren.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* `sling.job.max.parallel`
   * De waarde -1 wordt vervangen door het aantal beschikbare processors. Dit kan prestatieproblemen veroorzaken bij AEM instantie.
* `missing.maintenance.configuration`
   * Ontbrekende configuraties van onderhoudstaken kunnen prestatieverlies of beschadiging van instanties veroorzaken.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_guidance"
>title="Implementatieleiding"
>abstract="Neem contact op met de klantenservice voor hulp."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-ondersteuning"

* `sling.job.max.parallel`
   * Het is raadzaam de waarde in te stellen op 0,5 om de helft van de beschikbare verwerkers te benutten.
* `missing.maintenance.configuration`
   * Revisie opschonen: Zie [Opschonen van revisie](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html). Het belangrijke deel betreffende de configuratie is hier: [Revisie-opschoning - Tail en volledige compressie configureren](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html#how-to-configure-full-and-tail-compaction).
   * Opruiming Lucene Binaries: Zie [Operations-dashboard - opschonen van Lucene-binaire bestanden](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-dashboard.html#lucene-binaries-cleanup).
   * Verzameling opschonen van gegevensopslag: Zie [Opruimverzameling gegevensopslag](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/data-store-garbage-collection.html).
   * Werkstroom leegmaken: Zie [Regelmatig leegmaken van workflowinstanties](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/workflows-administering.html#regular-purging-of-workflow-instances).
   * AuditLog-onderhoudstaak: Zie [Controle van logboekonderhoud](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-audit-log.html).
* Bereik onze [Klantenzorgteam van Experience Manager](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.