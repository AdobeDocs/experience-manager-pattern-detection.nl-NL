---
title: UMI
description: Help-pagina Patroondetectiecode
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
translation-type: tm+mt
source-git-commit: 76dc944f1592118920f89c513faf456b8aa443a9
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# UMI {#umi}

Probleem met verkeerde configuratie van upgrade

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Probleem met verkeerde configuratie van upgrade"
>abstract="UMI identificeert wijzigingen aan bepaalde configuraties OSGi die kwesties wanneer bevordering, met inbegrip van een ontbroken verbetering of verminderde functionaliteit zullen veroorzaken."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Opvallende wijzigingen - AEM als Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="AEM als Cloud Service - Opmerkingen bij de release"

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

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Implementatieleiding"
>abstract="De beste praktijken zijn overzicht uw huidige configuraties en keren om het even welke veranderingen terug die aan vermelde configuraties worden aangebracht om om het even welke toekomstige verbeteringskwesties te vermijden. Neem contact op met Adobe Support voor hulp en uitleg"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-ondersteuning"

* Wijzig of verwijder de vier bovenstaande configuraties niet.
* Als configuraties zijn gewijzigd, moeten ze worden teruggezet op de verwachte waarden. Deze waarden worden vermeld in de `UMI` berichten.
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
