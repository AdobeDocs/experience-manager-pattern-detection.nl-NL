---
title: OAUI
description: Help-pagina Patroondetectiecode
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# OAUI {#oaui}

OAuth-gebruikersinstantie

## Achtergrond {#background}

`OAUI` identificeert het patroon waar er minstens één OAuth-gerelateerde gevormde gebruiker is die correcte migratie vereist.

OAuth wordt gevormd voor gebruikers wanneer er een subnode genoemd `oauth` direct onder een `rep:AuthorizableId` knoop in de vorm van `/home/user-path/user-node/oauth` is.

Een voorbeeld is: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`.

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

* Externe gebruikers die met OAuth zijn geconfigureerd, kunnen zich niet aanmelden bij auteur-/publicatieinstanties totdat deze opnieuw zijn geconfigureerd met de onderstaande procedure.

## Mogelijke oplossingen {#solutions}

* Neem contact op met uw Adobe-vertegenwoordiger om opties voor gebruikersmigratie te bespreken.
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
