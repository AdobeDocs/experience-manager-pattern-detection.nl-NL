---
title: MI
description: Help-pagina Patroondetectiecode.
exl-id: fa47ac63-1b5d-43b3-8acd-4a71c3fa714e
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '199'
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
* `missing.maintenance.configuration`: Identificeer ontbrekende configuraties van de Taak van het Onderhoud.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* `sling.job.max.parallel`
   * De waarde -1 wordt vervangen door het aantal beschikbare processors. Als dusdanig, zou het prestatieskwesties op een AEM instantie kunnen veroorzaken.
* `missing.maintenance.configuration`
   * De ontbrekende configuraties van de Taak van het Onderhoud kunnen verlies van prestaties of instantiecorruptie veroorzaken.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_guidance"
>title="Implementatieleiding"
>abstract="Neem contact op met de klantenservice voor hulp."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* `sling.job.max.parallel`
   * Adobe raadt aan de waarde in te stellen op 0,5 om te profiteren van de helft van de beschikbare processors.
* `missing.maintenance.configuration`
   * Opruimen van de revisie: Zie [ Opruimen van de Herziening ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/deploying/revision-cleanup). Het belangrijke deel met betrekking tot de configuratie is hier: [ Opruiming van de Revisie - vorm het Lusje en Volledige samenperking ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/deploying/revision-cleanup).
   * Lucene bindt schoonmaakbeurt: Zie [ Dashboard van Verrichtingen - de Bindingen van Lucene schoonmaakbeurt ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/administering/operations/operations-dashboard#lucene-binaries-cleanup).
   * De Inzameling van het huisvuil van de Opslag van gegevens: Zie [ de Inzameling van het huisvuil van de Opslag van Gegevens ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/administering/operations/data-store-garbage-collection).
   * Wissen van het werkschema: Zie [ Regelmatig het Wissen van de Instanties van het Werkschema ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/administering/operations/workflows-administering#regular-purging-of-workflow-instances).
   * De Taak van het Onderhoud van AuditLog: Zie [ het Onderhoud van het Logboek van de Controle ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/administering/operations/operations-audit-log).
* Contacteer het [ Team van de Zorg van de Klant van de Experience Manager ](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om bedenkingen te richten.
