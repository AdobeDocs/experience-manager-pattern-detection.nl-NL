---
title: MI
description: Help-pagina Patroondetectiecode.
exl-id: fa47ac63-1b5d-43b3-8acd-4a71c3fa714e
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# MI {#mi}

Probleem met verkeerde configuratie

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_overview"
>title="Probleem met verkeerde configuratie"
>abstract="MI identificeert configuratiekwesties op AEM instantie"

`MI` (Probleem met verkeerde configuratie) Hiermee worden configuratieproblemen in AEM instantie aangegeven.

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
   * Adobe raadt aan de waarde in te stellen op 0,5 om te profiteren van de helft van de beschikbare processors.
* `missing.maintenance.configuration`
   * Revisie opschonen: Zie [Opschonen van revisie](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/deploying/revision-cleanup). Het belangrijke deel met betrekking tot de configuratie is hier: [Revisie-opschoning - Tail en volledige compressie configureren](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/deploying/revision-cleanup).
   * Opruiming Lucene Binaries: Zie [Operations-dashboard - opschonen van Lucene-binaire bestanden](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/administering/operations/operations-dashboard#lucene-binaries-cleanup).
   * Opschoonfunctie gegevensopslag, verzameling: Zie [Opruimverzameling gegevensopslag](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/administering/operations/data-store-garbage-collection).
   * Werkstroom leegmaken: Zie [Regelmatig leegmaken van workflowinstanties](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/administering/operations/workflows-administering#regular-purging-of-workflow-instances).
   * AuditLog-onderhoudstaak: Zie [Controle van logboekonderhoud](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/administering/operations/operations-audit-log).
* Contact opnemen met de [Klantenzorgteam van Experience Manager](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om problemen aan te pakken.
