---
title: IOI
description: Help-pagina Patroondetectiecode
exl-id: b6c9d11f-5189-4799-98c0-c2699dfe3f40
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# IOI {#ioi}

Importeren van intern eiken

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_overview"
>title="Importeren van intern eiken"
>abstract="IOI-code identificeert het gebruik door klanten van interne eiken-pakketten, die ze via OSGi importeren. Zij worden gewoonlijk zonder bepaalde versie uitgevoerd en zijn uitsluitend bestemd voor consumptie door andere eikenbundels of laagactieve AEM."

`IOI` identificeert klantengebruik van interne pakketten van eikenhout, die hen via OSGi invoeren. Zij worden gewoonlijk zonder bepaalde versie uitgevoerd en zijn uitsluitend bestemd voor consumptie door andere eikenbundels of laagactieve AEM.

Sommige hiervan worden gebruikt door `com.adobe.granite.repository`, die een opslagplaats voor AEM tijdens het opstarten instelt. Een ander voorbeeld is het `com.adobe.granite.maintenance.oak` Adobe bundel, die omhult en onderhouds taken van eikel verstrekt.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* In een toekomstige AEM versie kan de interne export worden verwijderd, waardoor verbroken afhankelijkheden en inactieve bundels ontstaan die rechtstreeks afhankelijk zijn van eiken.
* API in interne export kan veranderen.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_guidance"
>title="Implementatieleiding"
>abstract="Klanten dienen hun aangepaste code te herzien om het gebruik van dergelijke API&#39;s te identificeren en te controleren of deze compatibel zijn met AEM as a Cloud Service. Neem contact op met de Adobe Support voor hulp en verduidelijking"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Gebruik de Sling Resource API (of de JCR API) in plaats van toegang op laag niveau.
* Vermijd dat dit afhankelijk is van interne pakketten die geen deel uitmaken van een openbare API of SPI.
* Neem contact op met onze [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
