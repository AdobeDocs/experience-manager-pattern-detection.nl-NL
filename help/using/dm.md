---
title: DM
description: Leer hoe patroondetectiecode het gebruik van AEM Assets - Dynamic Media identificeert.
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# DM {#dm}

Dynamic Media

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="De DM-code identificeert het gebruik van AEM Assets Dynamic Media in uw huidige implementatie. De uitvoeringsmodus detecteert de Dynamic Media-modus."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices" text="AEM ontwikkeling - Richtsnoeren en beste praktijken"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="AEM as a Cloud Service-ontwikkelingsrichtsnoeren"

`DM` (Dynamic Media) Identificeert het gebruik van AEM Assets Dynamic Media. De uitvoeringsmodus detecteert de Dynamic Media-modus.

Er wordt een subtype gebruikt met deze code:

* `dynamic.media.runmode`: de gekoppelde waarde van dit subtype, indien opgegeven, is:
   * `dynamicmedia`: Dynamic Media - Hybride modus
   * `dynamicmedia_scene7`: Dynamic Media - Scene7-modus

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* `dynamic.media.runmode`
   * Er kunnen upgradeproblemen zijn met betrekking tot Dynamic Media.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_guidance"
>title="Implementatieleiding"
>abstract="AEM as a Cloud Service ondersteunt alleen de uitvoermodus dynamicmedia_scene7. Bekijk de huidige instellingen en neem contact op met het ondersteuningsteam van de Adobe voor hulp en verduidelijkingen."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media" text="Dynamic Media instellen"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"


* `dynamic.media.runmode`
   * Vind meer informatie bij [ Opstelling Dynamic Media ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media).

* Contacteer het [ AEM Team van de Steun ](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) als u behandelde verduidelijkingen of bekommeringen nodig hebt.
