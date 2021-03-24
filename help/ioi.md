---
title: IOI
description: Help-pagina Patroondetectiecode
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---


# IOI {#ioi}

Importeren van intern eiken

## Achtergrond {#background}

`IOI` identificeert klantengebruik van interne pakketten van eikenhout, die hen via OSGi invoeren. Zij worden gewoonlijk zonder bepaalde versie uitgevoerd en zijn uitsluitend bestemd voor consumptie door andere eikenbundels of laagactieve AEM.

Sommige hiervan worden gebruikt door `com.adobe.granite.repository`, die een bewaarplaats voor AEM tijdens opstarten plaatst. Een ander voorbeeld is de bundel van `com.adobe.granite.maintenance.oak` Adobe, die omhult en onderhouds taken Oak verstrekt.

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

* In een toekomstige AEM versie kan de interne export worden verwijderd, waardoor verbroken afhankelijkheden en inactieve bundels ontstaan die rechtstreeks afhankelijk zijn van eiken.
* API in interne export kan veranderen.

## Mogelijke oplossingen {#solutions}

* Gebruik de Sling Resource API (of de JCR API) in plaats van toegang op laag niveau.
* Vermijd dat dit afhankelijk is van interne pakketten die geen deel uitmaken van een openbare API of SPI.
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.