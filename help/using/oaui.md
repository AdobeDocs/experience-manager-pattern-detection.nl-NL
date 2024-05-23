---
title: OAUI
description: Help-pagina Patroondetectiecode.
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
source-git-commit: b77a168fc8c075e8e41149a38df4d83fd2504a14
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---

# OAUI {#oaui}

OAuth Users Instance

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="OAuth Users Instance"
>abstract="De code OAUI identificeert het patroon waar er minstens één op OAuth betrekking hebbende gevormde gebruiker is die correcte migratie vereist. OAuth wordt gevormd voor gebruikers wanneer er een subnode genoemd OAuth direct onder een rep:AuthorizableId knoop in de vorm van /home/user-path/user-node/oauth is"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service - Opmerkingen bij de release"

`OAUI`  Identificeert het patroon waar er minstens één OAuth-Verwante gevormde gebruiker is die correcte migratie vereist.

OAuth wordt gevormd voor gebruikers wanneer er een subnode genoemd is `oauth` rechtstreeks onder een `rep:AuthorizableId` knooppunt in de vorm van `/home/user-path/user-node/oauth`.

Een voorbeeld is: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* Externe gebruikers die zijn geconfigureerd met OAuth kunnen zich niet aanmelden bij auteur-/publicatieinstanties totdat deze opnieuw zijn geconfigureerd met de onderstaande procedure.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="Implementatieleiding"
>abstract="Externe gebruikers die zijn geconfigureerd met OAuth kunnen zich niet aanmelden bij auteur-/publicatieinstanties totdat deze opnieuw zijn geconfigureerd om compatibel te zijn met AEM as a Cloud Service. AEM as a Cloud Service biedt IMS-verificatieondersteuning alleen voor auteur-, Admin- en Dev-gebruikers en SAML-gebaseerde integratie voor de publicatieomgevingen. Neem contact op met de ondersteuning van de Adobe voor hulp of verduidelijking."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/security/ims-support" text="IMS-ondersteuning - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/personalization/user-and-group-sync-for-publish-tier#integration-with-an-idp" text="SAML-integratie - Publiceren"

* Neem contact op met uw Adobe als u opties voor gebruikersmigratie moet bespreken.
* Contact opnemen met de [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om de problemen te verhelpen.
