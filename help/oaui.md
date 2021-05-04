---
title: OAUI
description: Help-pagina Patroondetectiecode
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# OAUI {#oaui}

OAuth-gebruikersinstantie

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="OAuth-gebruikersinstantie"
>abstract="De code OAUI identificeert het patroon waar er minstens één op OAuth betrekking hebbende gevormde gebruiker is die correcte migratie vereist. OAuth wordt gevormd voor gebruikers wanneer er een subnode is die direct onder een rep wordt genoemd:AuthorizableId knoop in de vorm van /home/user-path/user-node/oauth"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="AEM als Cloud Service - Opmerkingen bij de release"

`OAUI` identificeert het patroon waar er minstens één OAuth-gerelateerde gevormde gebruiker is die correcte migratie vereist.

OAuth wordt gevormd voor gebruikers wanneer er een subnode genoemd `oauth` direct onder een `rep:AuthorizableId` knoop in de vorm van `/home/user-path/user-node/oauth` is.

Een voorbeeld is: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`.

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

* Externe gebruikers die met OAuth zijn geconfigureerd, kunnen zich niet aanmelden bij auteur-/publicatieinstanties totdat deze opnieuw zijn geconfigureerd met de onderstaande procedure.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="Implementatieleiding"
>abstract="Externe gebruikers die met OAuth zijn geconfigureerd, kunnen zich pas aanmelden bij auteur-/publicatieinstanties als deze opnieuw zijn geconfigureerd om compatibel te zijn met AEM als Cloud Service. AEM als Cloud Service biedt IMS-verificatieondersteuning alleen voor auteur-, Admin- en Dev-gebruikers en SAML-gebaseerde integratie voor de publicatieomgevingen. Neem contact op met Adobe Support voor hulp en uitleg"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/ims-support.html" text="IMS-ondersteuning - AEM als Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/personalization/user-and-group-sync-for-publish-tier.html?lang=en#integration-with-an-idp" text="SAML-integratie - Publiceren"

* Neem contact op met uw Adobe-vertegenwoordiger om opties voor gebruikersmigratie te bespreken.
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
