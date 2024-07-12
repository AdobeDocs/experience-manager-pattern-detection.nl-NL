---
title: URS
description: Help-pagina Patroondetectiecode.
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: b77a168fc8c075e8e41149a38df4d83fd2504a14
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# URS {#urs}

Niet-ondersteunde gegevensopslagstructuur

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Niet-ondersteunde gegevensopslagstructuur"
>abstract="URS identificeert gevallen van URS (Unsupported Repository Structure) en knooppuntkenmerken. Op deze manier wordt informatie weergegeven om conflicten te voorkomen tussen AEM productcode en klantcode, waarbij inhoud buiten `/etc` wordt geherstructureerd naar andere mappen in de opslagplaats en meer."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring" text="Repositoregeling"

## Achtergrond {#background}

`URS` Identificeert gevallen van URL&#39;s (niet-ondersteunde Repository Structure) en knooppuntkenmerken. Vanaf AEM 6.4 zijn er richtsnoeren voor de herstructurering van de inhoud van de opslagplaats opgesteld. Door hiërarchieën voor AEM productcode duidelijk te omlijnen, en klantencode te vermijden, en conflicten tussen hen allen te vermijden, wordt de inhoud geherstructureerd uit `/etc` aan andere omslagen in de bewaarplaats. Hierbij worden de volgende regels op hoog niveau in acht genomen:

* AEM productcode wordt altijd in `/libs` geplaatst dat aangepaste code niet mag worden overschreven.
* Aangepaste code moet worden geplaatst in `/apps` , `/content` en `/conf` .
* Het wordt ten zeerste aanbevolen deze richtsnoeren voor AEM as a Cloud Service te volgen.

Subtypes worden gebruikt om de specifieke types van bewaarplaatskwesties te identificeren die zouden moeten worden opgelost:

* `clientlibs.location`: een clientbibliotheek die `/etc` per pad verwijst.
* `file.location`: Een bestand onder `/etc` dat sinds de installatie is gewijzigd.
* `node.location`: een knooppunt onder `/etc` dat sinds de installatie is gewijzigd.
* `workflow.location`: een workflowmodel of een startprogramma onder `/etc/workflow` .
* `package.structure`: Een pakket dat zowel muteerbare als onveranderlijke inhoud bevat.
* `node.size`: Een knooppunt met niet-ondersteunde grootte.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* Aangepaste code op basis van oudere paden kan ongewenste werking en functionaliteit van het product veroorzaken.
* Pakketten met zowel muteerbare als onveranderlijke inhoud kunnen problemen veroorzaken tijdens plaatsing.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Implementatieleiding"
>abstract="U kunt het beste uw codeproject bekijken. Zorg ervoor dat de code voldoet aan de AEM projectstructuurrichtlijnen en vermijd dat code vertrouwt op oudere of niet-ondersteunde opslagpaden die ongewenste gedragingen in AEM as a Cloud Service kunnen veroorzaken. Neem contact op met de ondersteuning van de Adobe voor hulp of verduidelijking."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure" text="Richtlijnen voor de projectstructuur AEM"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Zie [ Herstructurering van de Bewaarplaats ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring) voor begeleiding om voor AEM as a Cloud Service voor te bereiden.
* Zie ook [ AEM de Structuur van het Project ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) als u meer over veranderlijke en onveranderlijke gebieden van de bewaarplaats wilt leren.
* Contacteer het [ AEM Team van de Steun ](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om kwesties te hebben die worden gericht.
* Gebruik de [ Modernizer van de Bewaarplaats ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/repo-modernizer#refactoring-tools) om bestaande projectpakketten te herstructureren door inhoud en code in discrete pakketten te scheiden om met de projectstructuur compatibel te zijn die voor Adobe Experience Manager as a Cloud Service wordt bepaald.
