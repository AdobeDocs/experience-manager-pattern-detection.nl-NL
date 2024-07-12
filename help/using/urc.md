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
>abstract="URC identificeert het gebruik van configuraties die gebaseerd zijn op de naam van een uitvoeringsmodus die niet in AEM as a Cloud Service wordt ondersteund."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes" text="Ondersteunde uitvoermodi"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#runmodes" text="Modus Uitvoeren"

`URC` Hiermee wordt het gebruik aangegeven van configuraties die zijn gebaseerd op de naam van een uitvoeringsmodus die niet wordt ondersteund in AEM as a Cloud Service.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Implementatieleiding"
>abstract="U kunt het beste controleren of alle uitvoermodi die in uw toepassing worden gebruikt, worden ondersteund. En zorg ervoor dat ze de richtlijnen voor de resolutie van de uitvoeringsmodus volgen"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#deploying" text="Richtlijnen voor resolutie in de modus Uitvoeren"

* De reeks namen die kan worden gebruikt voor het uitvoeren van verschillende modi in AEM as a Cloud Service is beperkt.
* Configuraties die zijn gebaseerd op niet-ondersteunde namen voor de uitvoeringsmodus, hebben geen effect wanneer ze worden geïmplementeerd op AEM as a Cloud Service.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Hulpmiddelen en Middelen"
>abstract="Bekijk het WKND-verouderde project om te begrijpen hoe schendingen van URC compatibel kunnen worden gemaakt met AEM Cloud Service. Ook, het Voorbeeld van de Overtreding van het Overzicht URC op GitHub om te begrijpen hoe de douane looppas op wijze-gebaseerde configuraties OSGi kunnen worden bijgewerkt om met AEM as a Cloud Service te voldoen."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="WKND-verouderd project"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Voorbeeld van URC-schending - GitHub"

* Herzie het gebruik van deze configuratie zodat kunt u bepalen als het noodzakelijk is.
* Verander de configuratie gebruikend één van de gesteunde [ namen van de looppaswijze ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes) en volg [ de richtlijnen van de looppas wijzeresolutie ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#runmode-resolution).
* Het overzicht [ wknd-erfenis ](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) project en begrijpt hoe [ schendingen URC ](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) kan worden verbeterd en compatibel gemaakt met AEM as a Cloud Service.
* Contacteer het [ AEM Team van de Steun ](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om kwesties te hebben die worden gericht.
