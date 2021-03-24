---
title: CCOM
description: Help-pagina Patroondetectiecode
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# CCOM {#ccom}

Aangepaste component

## Achtergrond {#background}

`CCOM` identificeert douanecomponenten die op AEM zijn geïnstalleerd. Deze informatie wordt verstrekt met het oog op de beoordeling van beste praktijken.

Met deze code wordt een subtype gebruikt om de componentcategorie te identificeren:

* `custom.core`: Een supertype in de keten van supertypes van de component bevat &quot;kern/wcm/componenten/&quot;, erop wijzend dat het van een kerncomponent erft.
* `custom.foundation`: Een supertype in de keten van supertypes van de component bevat &quot;kern/wcm/componenten/&quot;, erop wijzend dat het van een kerncomponent erft.
* `custom.overlay.foundation`: Het componentpad bevat &quot;wcm/foundation/components/&quot; of &quot;foundation/components/&quot;, wat aangeeft dat het een stichtingscomponent bedekt.
* `custom`: De aangepaste component neemt een kern- of stichtingscomponent niet over of bedekt deze.

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

* De beste praktijken moeten aantal douanecomponenten minimaliseren, hefboomwerking kerncomponenten, en kerncomponenten met het Systeem van de Stijl gebruiken om technische schuld te verminderen.

## Mogelijke oplossingen {#solutions}

* Meer informatie over de Componenten van de Kern bij [Inleiding van de Componenten van de Kern](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html) vindt.
* Meer informatie over het Systeem van de Stijl bij [Gebruikend het Systeem van de Stijl](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use.html?lang=en#page-authoring).
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
