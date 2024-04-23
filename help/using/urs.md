---
title: URS
description: Help-pagina Patroondetectiecode.
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---

# URS {#urs}

Niet-ondersteunde gegevensopslagstructuur

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Niet-ondersteunde gegevensopslagstructuur"
>abstract="URS identificeert gevallen van niet-ondersteunde gegevensopslagstructuur en knooppuntkenmerken. Deze oppervlakken bevatten informatie om conflicten te voorkomen tussen AEM productcode en klantcode, inhoud die vanuit /etc wordt geherstructureerd naar andere mappen in de opslagplaats en meer."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring" text="Repositoregeling"

## Achtergrond {#background}

URS identificeert gevallen van niet-ondersteunde gegevensopslagstructuur en knooppuntkenmerken. Vanaf AEM 6.4 zijn er richtsnoeren voor de herstructurering van de inhoud van de opslagplaats opgesteld. Door hiërarchieën voor AEM productcode en klantencode duidelijk af te bakenen en conflicten tussen hen te vermijden, wordt de inhoud geherstructureerd uit `/etc` naar andere mappen in de opslagplaats, met inachtneming van de volgende regels op hoog niveau:

* AEM productcode wordt altijd in geplaatst `/libs`, die niet door aangepaste code mag worden overschreven.
* Aangepaste code moet in `/apps`, `/content`, en `/conf`.
* Het wordt ten zeerste aanbevolen deze richtsnoeren te volgen voor AEM as a Cloud Service.

Subtypes worden gebruikt om de specifieke types van bewaarplaatskwesties te identificeren die zouden moeten worden opgelost:

* `clientlibs.location`: Een clientbibliotheek die verwijst naar `/etc` per pad.
* `file.location`: Een bestand onder `/etc` die sinds de installatie is gewijzigd.
* `node.location`: Een knooppunt onder `/etc` die sinds de installatie is gewijzigd.
* `workflow.location`: Een workflowmodel of een startprogramma onder `/etc/workflow`.
* `package.structure`: Een pakket dat zowel muteerbare als onveranderlijke inhoud bevat.
* `node.size`: Een knooppunt met niet-ondersteunde grootte.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* Aangepaste code op basis van oudere paden kan ongewenste werking en functionaliteit van het product veroorzaken.
* Pakketten met zowel muteerbare als onveranderlijke inhoud kunnen problemen veroorzaken tijdens plaatsing.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Implementatieleiding"
>abstract="U kunt het beste uw codeproject bekijken. Zorg ervoor dat de code voldoet aan de AEM projectstructuurrichtlijnen en vermijd dat code vertrouwt op oudere/niet-ondersteunde opslagpaden die ongewenste werking in AEM as a Cloud Service kunnen veroorzaken. Neem contact op met de ondersteuning van de Adobe voor hulp of verduidelijking."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure" text="Richtlijnen voor de projectstructuur AEM"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Zie [Repositoregeling](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring) richtsnoeren ter voorbereiding op AEM as a Cloud Service.
* Zie ook [AEM projectstructuur](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) als u meer wilt weten over veranderbare en onveranderlijke gebieden van de gegevensopslagplaats.
* Contact opnemen met de [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om de problemen te verhelpen.
* Gebruik de [Repository Modernizer](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/repo-modernizer#refactoring-tools) bestaande projectpakketten te herstructureren door inhoud en code te scheiden in afzonderlijke pakketten, zodat deze verenigbaar zijn met de voor Adobe Experience Manager as a Cloud Service gedefinieerde projectstructuur.
