---
title: DM
description: Help-pagina Patroondetectiecode
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# DM {#dm}

Dynamic Media

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="De DM-code identificeert het gebruik van AEM Assets Dynamic Media in uw huidige implementatie. De Dynamic Media-modus wordt gedetecteerd door de uitvoeringsmodus."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html" text="AEM ontwikkeling - Richtlijnen en beste praktijken"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html" text="as a Cloud Service ontwikkelingsrichtsnoeren AEM"

`DM` identificeert het gebruik van AEM Assets Dynamic Media. De Dynamic Media-modus wordt gedetecteerd door de uitvoeringsmodus.

Er wordt een subtype gebruikt met deze code:

* `dynamic.media.runmode`: De gekoppelde waarde van dit subtype, indien opgegeven, is:
   * `dynamicmedia`: Dynamic Media - Hybride modus
   * `dynamicmedia_scene7`: Dynamic Media - modus Scene 7

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* `dynamic.media.runmode`
   * Er kunnen upgradeproblemen zijn met betrekking tot Dynamic Media.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_guidance"
>title="Implementatieleiding"
>abstract="AEM as a Cloud Service steunt slechts dynamicmedia_scene7 runmode. Controleer de huidige instellingen en neem contact op met het ondersteuningsteam voor Adoben voor hulp en uitleg."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html" text="Dynamic Media instellen"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"


* `dynamic.media.runmode`
   * Meer informatie vindt u op [Dynamic Media instellen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html).

* Neem contact op met onze [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
