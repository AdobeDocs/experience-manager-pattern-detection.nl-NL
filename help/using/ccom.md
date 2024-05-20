---
title: CCOM
description: Help-pagina Patroondetectiecode.
exl-id: 59071538-56ec-44e7-8196-56e6525bb4b9
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# CCOM {#ccom}

Aangepaste component

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_overview"
>title="Aangepaste component"
>abstract="CCOM identificeert douanecomponenten die op AEM worden geïnstalleerd. Deze informatie wordt verstrekt met het oog op de beoordeling van beste praktijken"

`CCOM` Identificeert douanecomponenten die op AEM geïnstalleerd zijn. Deze informatie wordt verstrekt met het oog op de beoordeling van beste praktijken.

Met deze code wordt een subtype gebruikt om de componentcategorie te identificeren:

* `custom.core`: Een supertype in de keten van supertypen van de component bevat `core/wcm/components/`, die aangeeft dat deze overerft van een kerncomponent.
* `custom.foundation`: Een supertype in de keten van supertypen van de component bevat &quot;`core/wcm/components/`, die aangeeft dat deze overerft van een kerncomponent.
* `custom.overlay.foundation`: Het componentpad bevat `wcm/foundation/components/` of `foundation/components/`, die aangeeft dat deze een stichtingscomponent bedekt.
* `custom`: De aangepaste component neemt een kern- of stichtingscomponent niet over of bedekt deze.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* De beste praktijken moeten het aantal douanecomponenten minimaliseren, de Componenten van de Kern gebruiken, en de Componenten van de Kern met het Systeem van de Stijl gebruiken zodat kunt u technische schuld verminderen.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_guidance"
>title="Implementatieleiding"
>abstract="De beste praktijken moeten het aantal douanecomponenten minimaliseren, kerncomponenten gebruiken, en kerncomponenten met het Systeem van de Stijl gebruiken om technische schuld te verminderen."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-core-components/using/introduction" text="Kernonderdelen"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use#page-authoring" text="Stijlsysteem"

* Meer informatie over Core Components vindt u op [Introductie van kerncomponenten](https://experienceleague.adobe.com/en/docs/experience-manager-core-components/using/introduction).
* Meer informatie over het Stijlsysteem vindt u op [Het stijlsysteem gebruiken](https://experienceleague.adobe.com/en/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use#page-authoring).
* Contact opnemen met de [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om de problemen te verhelpen.
