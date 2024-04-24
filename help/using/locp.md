---
title: LOCP
description: Help-pagina Patroondetectiecode.
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# LOCP {#locp}

/libs Overwriting Custom Packages

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Overwriting Custom Packages"
>abstract="LOCP identificeert de opsporing van een douanepakket dat inhoud aan /libs levert, die een anti-patroon (behalve in het geval ACLs) is."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Duurzame verbeteringen"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Samenvoeging van verkoopbronnen"

`LOCP`  Identificeert de opsporing van een douanepakket dat inhoud aan levert `/libs`, die een anti-patroon (behalve in het geval ACLs) is.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* De klantencode zou voor om het even welke GFP, SP, of belangrijke AEM verbetering kunnen worden geschrapt of worden vervangen.
* Soms wordt de nieuwe inhoud mogelijk niet correct geïnstalleerd.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Implementatieleiding"
>abstract="Klanten dienen hun aangepaste code en pakketten te controleren om na te gaan of inhoud wordt geleverd aan /libs en deze opnieuw te ordenen op bedekking van de inhoud onder /apps en deze compatibel te maken met AEM as a Cloud Service. Neem contact op met de ondersteuning van de Adobe voor hulp of verduidelijking."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Bedekkingen"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Klantpakketten moeten inhoud implementeren op `/apps` in plaats van `/libs`.
* Contact opnemen met de [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) indien u verduidelijking of bezorgdheid nodig hebt.
