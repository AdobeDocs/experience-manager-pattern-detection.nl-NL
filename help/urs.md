---
title: URS
description: Help-pagina Patroondetectiecode
translation-type: tm+mt
source-git-commit: 5a83dd8d08da974a5d775032b8dbea2593be9d15
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---


# URS {#urs}

Niet-ondersteunde gegevensopslagstructuur

## Achtergrond {#background}

`URS` identificeert gevallen van niet-ondersteunde gegevensopslagstructuur. Vanaf AEM 6.4 zijn er richtsnoeren voor de herstructurering van de inhoud van de opslagplaats opgesteld. Door hiërarchieën voor AEM productcode en klantcode duidelijk te omlijnen en conflicten tussen hen te vermijden, wordt de inhoud geherstructureerd uit `/etc` aan andere omslagen in de bewaarplaats, die de volgende regels op hoog niveau volgen:

* AEM productcode wordt altijd in `/libs` geplaatst, die niet door douanecode moet worden beschreven de code van de Douane zou in `/apps`, `/content`, en `/conf` moeten worden geplaatst.
* Het wordt ten zeerste aanbevolen dat deze richtsnoeren voor AEM als Cloud Service worden gevolgd.

Subtypes worden gebruikt om de specifieke types van bewaarplaatskwesties te identificeren die zouden moeten worden opgelost:
* `clientlibs.location`: Een clientbibliotheek die  `/etc` per pad verwijst.
* `file.location`: Een bestand onder  `/etc` dat sinds de installatie is gewijzigd.
* `node.location`: Een knooppunt onder  `/etc` dat sinds de installatie is gewijzigd.
* `workflow.location`: Een workflowmodel of startprogramma onder  `/etc/workflow`.
* `package.structure`: Een pakket dat zowel muteerbare als onveranderlijke inhoud bevat.

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

* Aangepaste code die afhankelijk is van oudere paden kan ongewenste werking en productfunctionaliteit veroorzaken.
* Pakketten met zowel muteerbare als onveranderlijke inhoud veroorzaken waarschijnlijk problemen tijdens plaatsing.

## Mogelijke oplossingen {#solutions}

* Zie [Herstructurering van opslagplaats](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html) voor richtsnoeren ter voorbereiding op AEM als Cloud Service.
* Raadpleeg ook [AEM Projectstructuur](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) voor meer informatie over veranderbare en onveranderlijke gebieden van de opslagplaats.
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
* Benut [Repository Modernizer](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html#refactoring-tools) om bestaande projectpakketten te herstructureren door inhoud en code in discrete pakketten te scheiden zodat deze compatibel zijn met de projectstructuur die voor Adobe Experience Manager als Cloud Service wordt gedefinieerd.