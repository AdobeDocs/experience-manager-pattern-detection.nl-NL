---
title: URS
description: Help-pagina Patroondetectiecode
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: 9d92254d2f5e84f833ed6926a0ae69b334730d21
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---

# URS {#urs}

Niet-ondersteunde gegevensopslagstructuur

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Niet-ondersteunde gegevensopslagstructuur"
>abstract="URS identificeert gevallen van niet-ondersteunde repository structuur en knooppuntkenmerken. Deze oppervlakken bevatten informatie om conflicten te voorkomen tussen AEM productcode en klantcode, inhoud die vanuit /etc wordt geherstructureerd naar andere mappen in de opslagplaats en meer."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html" text="Repositoregeling"

## Achtergrond {#background}

`URS` identificeert gevallen van niet-ondersteunde repository structuur en knooppuntkenmerken. Vanaf AEM 6.4 zijn er richtsnoeren voor de herstructurering van de inhoud van de opslagplaats opgesteld. Door hiërarchieën voor AEM productcode en klantcode duidelijk te omlijnen en conflicten tussen hen te vermijden, wordt de inhoud geherstructureerd uit `/etc` aan andere omslagen in de bewaarplaats, die de volgende regels op hoog niveau volgen:

* AEM productcode wordt altijd in `/libs` geplaatst, die niet door douanecode moet worden beschreven.
* Aangepaste code moet worden geplaatst in `/apps`, `/content` en `/conf`.
* AEM als Cloud Service biedt geen ondersteuning voor lange knooppuntnamen (>150 bytes).
* Het wordt ten zeerste aanbevolen dat deze richtsnoeren voor AEM als Cloud Service worden gevolgd.

Subtypes worden gebruikt om de specifieke types van bewaarplaatskwesties te identificeren die zouden moeten worden opgelost:
* `clientlibs.location`: Een clientbibliotheek die  `/etc` per pad verwijst.
* `file.location`: Een bestand onder  `/etc` dat sinds de installatie is gewijzigd.
* `node.location`: Een knooppunt onder  `/etc` dat sinds de installatie is gewijzigd.
* `workflow.location`: Een workflowmodel of startprogramma onder  `/etc/workflow`.
* `package.structure`: Een pakket dat zowel muteerbare als onveranderlijke inhoud bevat.
* `node.name.length`: Een knooppuntnaam met niet-ondersteunde lengte.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* Aangepaste code die afhankelijk is van oudere paden kan ongewenste werking en productfunctionaliteit veroorzaken.
* Pakketten met zowel muteerbare als onveranderlijke inhoud veroorzaken waarschijnlijk problemen tijdens plaatsing.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Implementatieleiding"
>abstract="De beste praktijken zijn overzicht uw codeproject en zorgen ervoor het zich aan de AEM projectstructuurrichtlijnen houdt en vermijden code die op oudere/niet gestaafde opbergwegen baseert die ongewenste gedrag in AEM als Cloud Service kan veroorzaken. Neem contact op met Adobe Support voor hulp en uitleg"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html" text="Richtlijnen voor projectstructuur AEM"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-ondersteuning"

* Zie [Herstructurering van opslagplaats](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html) voor richtsnoeren ter voorbereiding op AEM als Cloud Service.
* Raadpleeg ook [AEM Projectstructuur](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) voor meer informatie over veranderbare en onveranderlijke gebieden van de opslagplaats.
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
* Benut [Repository Modernizer](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html#refactoring-tools) om bestaande projectpakketten te herstructureren door inhoud en code in discrete pakketten te scheiden zodat deze compatibel zijn met de projectstructuur die voor Adobe Experience Manager als Cloud Service wordt gedefinieerd.
