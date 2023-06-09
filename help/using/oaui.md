---
title: OAUI
description: Help-pagina Patroondetectiecode
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
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
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="AEM as a Cloud Service - Opmerkingen bij de release"

`OAUI` identificeert het patroon waar er minstens één OAuth-gerelateerde gevormde gebruiker is die correcte migratie vereist.

OAuth wordt gevormd voor gebruikers wanneer er een subnode genoemd is `oauth` rechtstreeks onder een `rep:AuthorizableId` knooppunt in de vorm van `/home/user-path/user-node/oauth`.

Een voorbeeld is: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* Externe gebruikers die met OAuth zijn geconfigureerd, kunnen zich niet aanmelden bij auteur-/publicatieinstanties totdat deze opnieuw zijn geconfigureerd met de onderstaande procedure.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="Implementatieleiding"
>abstract="Externe gebruikers die zijn geconfigureerd met OAuth kunnen zich pas aanmelden bij auteur-/publicatieinstanties als deze opnieuw zijn geconfigureerd om compatibel te zijn met AEM as a Cloud Service. AEM as a Cloud Service biedt IMS-verificatieondersteuning alleen voor auteurs-, Admin- en Dev-gebruikers en SAML-gebaseerde integratie voor de publicatieomgevingen. Neem contact op met Adobe Support voor hulp en uitleg"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/ims-support.html" text="IMS-ondersteuning - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/personalization/user-and-group-sync-for-publish-tier.html?lang=en#integration-with-an-idp" text="SAML-integratie - Publiceren"

* Neem contact op met uw Adobe-vertegenwoordiger om opties voor gebruikersmigratie te bespreken.
* Neem contact op met onze [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
