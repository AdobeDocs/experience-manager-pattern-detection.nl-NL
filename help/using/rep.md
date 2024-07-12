---
title: REP
description: Help-pagina Patroondetectiecode.
exl-id: e788deba-a301-404f-8e90-51f721409e69
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# [!DNL REP] {#rep}

Replication Agent

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_overview"
>title="Replication Agent"
>abstract="REP identificeert toegelaten replicatieagenten. Deze agentia worden gerapporteerd vanwege de mogelijkheid van problemen die moeten worden aangepakt bij de upgrade naar AEM as a Cloud Service. AEM as a Cloud Service gebruikt Sling Content Distribution om inhoud van auteur naar publicatieomgeving te distribueren. Deze distributie wordt gedaan buiten AEM runtime gebruikend de pijpleidingsdienst van Adobe I/O Runtime op Adobe Developer. Deze workflow wordt automatisch geconfigureerd in de AEM as a Cloud Service-omgeving waarvoor de provisioned is."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#replication-agents" text="Opvallende wijzigingen - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#no-reverse-replication-agents" text="Richtlijnen voor ontwikkeling"

`REP` Identificeert ingeschakelde replicatieagents. Deze agentia worden gerapporteerd vanwege de mogelijkheid van problemen die moeten worden aangepakt bij de upgrade naar AEM as a Cloud Service.

Subtypes worden gebruikt om verschillende soorten informatie te identificeren:

* `forward.replication`: Identificeer de ingeschakelde forward replication agents.
* `reverse.replication`: Identificeer de ingeschakelde reverse-replicatieagents.
* `standard.replication.agent.modification`: Identificeer de ingeschakelde standaard replicatiemiddelen die worden gewijzigd.
* `custom.replication.agent.detection`: identificeer de ingeschakelde aangepaste replicatieagents.

AEM as a Cloud Service gebruikt [ het Verdelen van de Distributie van de Inhoud ](https://sling.apache.org/documentation/bundles/content-distribution.html) om inhoud van auteur te verspreiden om milieu&#39;s te publiceren. Deze distributie wordt gedaan buiten AEM runtime gebruikend de pijpleidingsdienst van Adobe I/O Runtime op Adobe Developer. Deze workflow wordt automatisch geconfigureerd in de AEM as a Cloud Service-omgeving waarvoor de provisioned is.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* De configuratie van replicatie is gewijzigd met AEM as a Cloud Service. Alle huidige replicatieagenten zouden moeten worden herzien. De revisie helpt u om te zien:
   * die welke standaardcapaciteit kan vervangen;
   * welke configuraties naar code moeten worden verplaatst;
   * en die niet worden ondersteund.
* Elk gebruik van replicatiemiddelen in aangepaste code of workflows moet worden gecontroleerd tijdens de upgrade naar AEM as a Cloud Service.
* Omgekeerde replicatie wordt in eerste instantie niet ondersteund in AEM as a Cloud Service.
* Het is niet nodig een aparte Dispatcher flush-agent te configureren. In plaats daarvan wordt deze automatisch geconfigureerd in de AEM as a Cloud Service-omgeving.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_guidance"
>title="Implementatieleiding"
>abstract="De beste praktijken moeten, douanefunctionaliteit direct afhankelijk van replicatieagenten herzien, refactor, en optimaliseren en het compatibel maken met AEM as a Cloud Service. Neem contact op met de ondersteuning van de Adobe voor hulp of verduidelijking."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#replication" text="Replicatie - AEM as a Cloud Service"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Zie de Richtlijnen van de Ontwikkeling van AEM as a Cloud Service [ ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#no-reverse-replication-agents) en versie nota&#39;s voor [ replicatieagenten ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#replication-agents).
* Het overzicht, de refactor, en optimaliseert functionaliteit direct afhankelijk van replicatieagenten om bedrijfstaken uit te voeren.
* Zie hoe [ replicatie ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#replication) door plaatsing in AEM as a Cloud Service wordt beïnvloed.
* Contacteer het [ AEM Team van de Steun ](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om kwesties te hebben die worden gericht.
