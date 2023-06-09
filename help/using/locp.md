---
title: LOCP
description: Help-pagina Patroondetectiecode
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# LOCP {#locp}

/libs Overwriting Custom Packages

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Overwriting Custom Packages"
>abstract="LOCP identificeert de opsporing van een douanepakket dat inhoud aan /libs levert, die een anti-patroon (behalve in het geval ACLs) is."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html" text="Duurzame verbeteringen"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html#platform" text="Samenvoegen van verkoopbronnen"

`LOCP` identificeert de opsporing van een douanepakket dat inhoud aan levert `/libs`, die een anti-patroon (behalve in het geval ACLs) is.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* De klantencode zou voor om het even welke GFP, SP of belangrijke AEM verbetering kunnen worden geschrapt of worden vervangen.
* In sommige gevallen wordt de nieuwe inhoud mogelijk niet correct geïnstalleerd.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Implementatieleiding"
>abstract="Klanten dienen hun aangepaste code en pakketten te controleren om na te gaan of inhoud wordt geleverd aan /libs en deze opnieuw te ordenen op bedekking van de inhoud onder /apps en deze compatibel te maken met AEM as a Cloud Service. Neem contact op met Adobe Support voor hulp en uitleg"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html#platform" text="Bedekkingen"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-ondersteuning"

* Klantpakketten moeten inhoud implementeren op `/apps` in plaats van `/libs`.
* Neem contact op met onze [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
