---
title: REP
description: Help-pagina Patroondetectiecode
exl-id: e788deba-a301-404f-8e90-51f721409e69
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# [!DNL REP] {#rep}

Replication Agent

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_overview"
>title="Replication Agent"
>abstract="REP identificeert toegelaten replicatieagenten. Deze worden gerapporteerd vanwege het potentieel voor problemen die moeten worden aangepakt wanneer wordt overgegaan tot AEM as a Cloud Service. AEM as a Cloud Service gebruikt de Verspreiding van de Inhoud van de Verkoop om inhoud van auteur aan publicatiemilieu&#39;s te verdelen. Dit wordt gedaan buiten AEM runtime gebruikend de pijpleidingsdienst van Adobe I/O. Dit wordt automatisch gevormd in het provisioned AEM as a Cloud Service milieu."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#replication-agents" text="Opvallende wijzigingen - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#no-reverse-replication-agents" text="Richtlijnen voor ontwikkeling"

`REP` identificeert toegelaten replicatieagenten. Deze worden gerapporteerd vanwege het potentieel voor problemen die moeten worden aangepakt wanneer wordt overgegaan tot AEM as a Cloud Service.

Subtypes worden gebruikt om verschillende soorten informatie te identificeren:

* `forward.replication`: Identificeer de toegelaten voorwaartse replicatieagenten.
* `reverse.replication`: Identificeer de toegelaten omgekeerde replicatieagenten.
* `standard.replication.agent.modification`: Identificeer de toegelaten standaardreplicatieagenten die worden gewijzigd.
* `custom.replication.agent.detection`: Identificeer de toegelaten agenten van de douanereplicatie.

as a Cloud Service gebruik AEM [Distributie van inhoud verkopen](https://sling.apache.org/documentation/bundles/content-distribution.html) om inhoud van auteur naar publicatieomgeving te distribueren. Dit wordt gedaan buiten AEM runtime gebruikend de pijpleidingsdienst van Adobe I/O. Dit wordt automatisch gevormd in het provisioned AEM as a Cloud Service milieu.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* De configuratie van replicatie is veranderd met AEM as a Cloud Service. Alle huidige replicatieagenten zouden moeten worden herzien om te zien welke door standaardvermogen worden vervangen, welke configuraties aan code moeten worden verplaatst, en die niet worden gesteund.
* Om het even welk gebruik van replicatieagenten in douanecode of werkschema&#39;s zou moeten worden herzien terwijl bevordering aan AEM as a Cloud Service.
* Omgekeerde replicatie wordt in eerste instantie niet ondersteund in AEM as a Cloud Service.
* Er is geen behoefte om een afzonderlijke verzender te vormen flush agent. Dit wordt automatisch gevormd in het AEM as a Cloud Service milieu.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_guidance"
>title="Implementatieleiding"
>abstract="De beste praktijken moeten, douanefunctionaliteit direct afhankelijk van replicatieagenten herzien, refactor, en optimaliseren en het compatibel maken met AEM as a Cloud Service. Neem contact op met de Adobe Support voor hulp en verduidelijking"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#replication" text="Replicatie - AEM as a Cloud Service"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Zie de AEM as a Cloud Service [Richtlijnen voor ontwikkeling](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#no-reverse-replication-agents) en opmerkingen bij de release voor [replicatiemiddelen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#replication-agents).
* Het overzicht, de refactor, en optimaliseert functionaliteit direct afhankelijk van replicatieagenten om bedrijfstaken uit te voeren.
* Zie hoe [replicatie](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#replication) wordt beïnvloed door plaatsing in AEM as a Cloud Service.
* Neem contact op met onze [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
