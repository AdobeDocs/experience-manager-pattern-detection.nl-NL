---
title: LOCP
description: Help-pagina Patroondetectiecode.
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# LOCP {#locp}

/libs Overwriting Custom Packages

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Overwriting Custom Packages"
>abstract="LOCP identificeert de opsporing van een douanepakket dat inhoud aan `/libs` levert, die een anti-patroon (behalve als er ACLs) is."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Duurzame verbeteringen"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Samenvoeging van verkoopbronnen"

`LOCP` Identificeert de opsporing van een douanepakket dat inhoud aan `/libs` levert, dat een anti-patroon (behalve in het geval ACLs) is.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* De klantencode zou voor om het even welke GFP, SP, of belangrijke AEM verbetering kunnen worden geschrapt of worden vervangen.
* Soms wordt de nieuwe inhoud mogelijk niet correct geïnstalleerd.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Implementatieleiding"
>abstract="Klanten dienen hun aangepaste code en pakketten te controleren om na te gaan of inhoud aan `/libs` wordt geleverd. Indien nodig, moet u erop vertrouwen dat de inhoud in /apps wordt bedekt en compatibel is met AEM as a Cloud Service. Neem contact op met de ondersteuning van de Adobe voor hulp of verduidelijking."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Bedekkingen"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Klantpakketten moeten inhoud implementeren in `/apps` in plaats van `/libs` .
* Contacteer het [ AEM Team van de Steun ](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) als u behandelde verduidelijkingen of bekommeringen nodig hebt.
