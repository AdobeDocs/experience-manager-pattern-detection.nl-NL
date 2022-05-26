---
title: UMI
description: Help-pagina Patroondetectiecode
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
source-git-commit: b19818f3f043641328b68adfe37a9c9cb09d1143
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---

# UMI {#umi}

Probleem met verkeerde configuratie van upgrade

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Probleem met verkeerde configuratie van upgrade"
>abstract="UMI identificeert wijzigingen aan bepaalde configuraties OSGi die kwesties wanneer bevordering, met inbegrip van een ontbroken verbetering of verminderde functionaliteit zullen veroorzaken."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Opvallende wijzigingen - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="AEM as a Cloud Service - Opmerkingen bij de release"

`UMI` identificeert wijzigingen aan bepaalde configuraties OSGi die kwesties wanneer bevordering, met inbegrip van een ontbroken verbetering of verminderde functionaliteit zullen veroorzaken.

De volgende configuraties worden gecontroleerd op wijziging:
* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`
* `com.day.cq.commons.impl.ExternalizerImpl`

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* Het wijzigen of verwijderen van configuraties kan hieronder problemen veroorzaken:
   * De upgrade kan vastlopen (bijvoorbeeld `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` ontbreekt, maar aanwezig in `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`).
   * Autorisatiekwesties kunnen na upgrade optreden (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * Bepaalde functionaliteit werkt mogelijk niet zoals verwacht. Bijvoorbeeld wijzigen `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` kan ertoe leiden dat sommige JSP dossiers niet worden gecompileerd, wat uiteindelijk in verlies van functionaliteit zal resulteren.
   * De waarden van de externalizer config `com.day.cq.commons.impl.ExternalizerImpl` worden ingesteld door de omgevingsvariabelen van de cloud-manager in AEM as a Cloud Service.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Implementatieleiding"
>abstract="De beste praktijken zijn overzicht uw huidige configuraties en keren om het even welke veranderingen terug die aan vermelde configuraties worden aangebracht om om het even welke toekomstige verbeteringskwesties te vermijden. Neem contact op met Adobe Support voor hulp en uitleg"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud-ondersteuning"

* Wijzig of verwijder de vier bovenstaande configuraties niet.
   * In geval van de volgende schending:\
      &quot;Vereiste eigenschappen voor de OSGi-configuratie &#39;xyz-configuration&#39; ontbreken: &#39;[property-1,property-2...]&quot;.&quot;\
      Gelieve te bevestigen of deze schrappingen wettig of niet zijn aangezien deze configuraties OOTB zijn en nooit van de Manager van OSGi Config gewijzigd/bewaard zouden kunnen zijn.
* Als configuraties zijn gewijzigd, moeten ze worden teruggezet op de verwachte waarden. Deze waarden worden vermeld in het `UMI` berichten.
* Voor `com.day.cq.commons.impl.ExternalizerImpl`, gelieve [documentatie](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developer-tools/externalizer.html?lang=en) voor het instellen van externalizer config met gebruik van de omgevingsvariabelen van de cloud manager in AEM as a Cloud Service.
* Neem contact op met onze [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
