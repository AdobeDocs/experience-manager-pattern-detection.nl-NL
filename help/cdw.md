---
title: CDW
description: Help-pagina Patroondetectiecode
exl-id: a9e9dae8-0aa2-4679-a3c1-418cab01cfda
source-git-commit: d12f2613493d9bf379464d9c089ad376532c4de2
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# CDW {#cdw}

Aangepaste dialoogvensterwidget

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_overview"
>title="Aangepaste dialoogvensterwidget"
>abstract="CDW identificeert de widgets van de Dialoog van de Douane die zouden moeten worden bijgewerkt om hen met AEM as a Cloud Service compatibel te zijn."

`CDW`  Aangepaste dialoogvensterwidgets identificeren de aangepaste widgets CoralUI en Klassiek. Deze moeten worden bijgewerkt om ze compatibel te maken met AEM as a Cloud Service.

Subtypes worden gebruikt om de verschillende soorten informatie te identificeren, zoals:

* `custom.coral.widget`: Identificeer de widgets van de douanedialoog die op CoralUI 2 of CoralUI 3 worden gebaseerd.
* `custom.classic.widget`: Identificeer de douane dialoog widgets die op ExtJs worden gebaseerd.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* De klassieke gebruikersinterface is niet meer beschikbaar in AEM as a Cloud Service. De standaardinterface voor ontwerpen is de interface met aanraakbediening.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_guidance"
>title="Implementatieleiding"
>abstract="Neem contact op met de klantenservice voor hulp."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-ondersteuning"

* Aangepaste Klassieke dialoogvensterwidgets moeten worden omgezet van ExtJS in [CoralUI](https://developer.adobe.com/experience-manager/reference-materials/6-5/coral-ui/coralui3/getting-started.html).
* De widgets van het dialoogvenster Aangepast koraal moeten worden geëvalueerd voor update naar CoralUI 3.
* Bereik onze [Klantenzorgteam van Experience Manager](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
