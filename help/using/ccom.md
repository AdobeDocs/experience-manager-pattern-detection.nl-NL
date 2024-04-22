---
title: CCOM
description: Help-pagina Patroondetectiecode.
exl-id: 59071538-56ec-44e7-8196-56e6525bb4b9
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# CCOM {#ccom}

Aangepaste component

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_overview"
>title="Aangepaste component"
>abstract="CCOM identificeert aangepaste componenten die op AEM zijn geïnstalleerd. Deze informatie wordt verstrekt met het oog op de beoordeling van beste praktijken"

`CCOM` identificeert douanecomponenten die op AEM zijn geïnstalleerd. Deze informatie wordt verstrekt met het oog op de beoordeling van beste praktijken.

Met deze code wordt een subtype gebruikt om de componentcategorie te identificeren:

* `custom.core`: Een supertype in de keten van supertypen van de component bevat &quot;core/wcm/components/&quot;, wat aangeeft dat het overerft van een kerncomponent.
* `custom.foundation`: Een supertype in de keten van supertypen van de component bevat &quot;core/wcm/components/&quot;, wat aangeeft dat het overerft van een kerncomponent.
* `custom.overlay.foundation`: Het componentpad bevat &quot;wcm/foundation/components/&quot; of &quot;foundation/components/&quot;, wat aangeeft dat het een stivingscomponent bedekt.
* `custom`: De aangepaste component neemt een kern- of stichtingscomponent niet over of bedekt deze.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* De beste praktijken moeten aantal douanecomponenten minimaliseren, hefboomwerking kerncomponenten, en kerncomponenten met het Systeem van de Stijl gebruiken om technische schuld te verminderen.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_guidance"
>title="Implementatieleiding"
>abstract="De beste praktijken moeten aantal douanecomponenten minimaliseren, hefboomwerking kerncomponenten, en kerncomponenten met het Systeem van de Stijl gebruiken om technische schuld te verminderen."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html" text="Kernonderdelen"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use.html?lang=en#page-authoring" text="Stijlsysteem"

* Meer informatie over Core Components vindt u op [Introductie van kerncomponenten](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html).
* Meer informatie over het Stijlsysteem vindt u op [Het stijlsysteem gebruiken](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use.html?lang=en#page-authoring).
* Contact opnemen met de [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om de problemen te verhelpen.
