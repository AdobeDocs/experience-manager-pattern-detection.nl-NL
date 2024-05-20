---
title: URC
description: Help-pagina Patroondetectiecode.
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# URC {#urc}

Niet-ondersteunde configuratie van de uitvoermodus

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Niet-ondersteunde configuratie van de uitvoermodus"
>abstract="URC identificeert het gebruik van configuraties die op een naam van de looppaswijze gebaseerd zijn die niet in AEM as a Cloud Service wordt gesteund."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes" text="Ondersteunde uitvoermodi"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#runmodes" text="Modus Uitvoeren"

`URC`  Identificeert het gebruik van configuraties die op een naam van de looppaswijze gebaseerd zijn die niet in AEM as a Cloud Service wordt gesteund.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Implementatieleiding"
>abstract="U kunt het beste controleren of alle uitvoermodi die in uw toepassing worden gebruikt, worden ondersteund. En zorg ervoor dat ze de richtlijnen voor de resolutie van de uitvoeringsmodus volgen"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#deploying" text="Richtlijnen voor resolutie in de modus Uitvoeren"

* De reeks namen die kan worden gebruikt voor het uitvoeren van verschillende modi in AEM as a Cloud Service is beperkt.
* Configuraties die zijn gebaseerd op niet-ondersteunde namen voor de uitvoeringsmodus, hebben geen effect wanneer ze worden geïmplementeerd AEM as a Cloud Service.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Hulpmiddelen en Middelen"
>abstract="Bekijk het WKND-verouderde project om te begrijpen hoe schendingen van URC compatibel kunnen worden gemaakt met AEM Cloud Service. Ook, het Voorbeeld van de Overtreding van het Overzicht URC op GitHub om te begrijpen hoe de op wijze-gebaseerde configuraties van douane looppas OSGi kunnen worden bijgewerkt om met AEM as a Cloud Service te houden."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="WKND-verouderd project"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Voorbeeld van URC-schending - GitHub"

* Herzie het gebruik van deze configuratie zodat kunt u bepalen als het noodzakelijk is.
* Wijzig de naam van de configuratie met een van de ondersteunde configuraties [namen van uitvoermodi](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes) en volgen [Richtlijnen voor resolutie in de uitvoermodus](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#runmode-resolution).
* Controleren [verouderd](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) projecten en begrijpen hoe [OTC-overtredingen](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) kan worden gecorrigeerd en verenigbaar worden gemaakt met AEM as a Cloud Service.
* Contact opnemen met de [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om de problemen te verhelpen.
