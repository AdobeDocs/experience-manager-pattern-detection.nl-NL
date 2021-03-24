---
title: UMI
description: Help-pagina Patroondetectiecode
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# UMI {#umi}

Probleem met verkeerde configuratie van upgrade

## Achtergrond {#background}

`UMI` identificeert wijzigingen aan bepaalde configuraties OSGi die kwesties wanneer bevordering, met inbegrip van een ontbroken verbetering of verminderde functionaliteit zullen veroorzaken.

De volgende configuraties worden gecontroleerd op wijziging:
* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

* Het wijzigen of verwijderen van configuraties kan hieronder problemen veroorzaken:
   * De upgrade kan vastlopen (`org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` ontbreekt bijvoorbeeld, maar is aanwezig in `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`).
   * De kwesties van de vergunning kunnen na verbetering (`org.apache.sling.engine.impl.auth.SlingAuthenticator`) komen.
   * Bepaalde functionaliteit werkt mogelijk niet zoals verwacht. Als u bijvoorbeeld `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` wijzigt, kunnen sommige JSP-bestanden niet worden gecompileerd, wat uiteindelijk zal leiden tot verlies van functionaliteit.

## Mogelijke oplossingen {#solutions}

* Wijzig of verwijder de vier bovenstaande configuraties niet.
* Als configuraties zijn gewijzigd, moeten ze worden teruggezet op de verwachte waarden. Deze waarden worden vermeld in de `UMI` berichten.
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
