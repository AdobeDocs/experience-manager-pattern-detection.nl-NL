---
title: IOI
description: Help-pagina Patroondetectiecode.
exl-id: b6c9d11f-5189-4799-98c0-c2699dfe3f40
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# IOI {#ioi}

Interne Oak-import

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_overview"
>title="Interne Oak-import"
>abstract="IOI-code identificeert het gebruik door klanten van interne Oak-pakketten, waarbij deze worden geïmporteerd via OSGi. Ze worden zonder een bepaalde versie geëxporteerd. Oak-pakketten of laagactieve AEM gebruiken deze alleen."

`IOI` Identificeert het klantgebruik van interne pakketten van Oak, die hen via OSGi invoeren. Ze worden zonder een bepaalde versie geëxporteerd. Oak-pakketten of laagactieve AEM gebruiken deze alleen.
Sommige van deze gebieden worden gebruikt door `com.adobe.granite.repository` , dat een opslagplaats voor AEM tijdens het opstarten instelt. Een ander voorbeeld is de bundel van de Adobe `com.adobe.granite.maintenance.oak`, die omhult en Oak onderhoudstaken verstrekt.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* In een toekomstige AEM versie kan de interne export worden verwijderd, waardoor verbroken afhankelijkheden en inactieve bundels ontstaan die rechtstreeks afhankelijk zijn van Oak.
* API in interne export kan veranderen.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_guidance"
>title="Implementatieleiding"
>abstract="Klanten dienen hun aangepaste code te herzien om het gebruik van dergelijke API&#39;s te identificeren en deze te koppelen aan AEM as a Cloud Service. Neem contact op met de ondersteuning van de Adobe voor hulp of verduidelijking."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Gebruik de Sling Resource API (of de JCR API) in plaats van toegang op laag niveau.
* Vermijd dat dit afhankelijk is van interne pakketten die geen deel uitmaken van een openbare API of SPI.
* Contacteer het [ AEM Team van de Steun ](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om kwesties te hebben die worden gericht.
