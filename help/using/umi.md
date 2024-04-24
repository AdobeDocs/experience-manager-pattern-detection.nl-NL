---
title: UMI
description: Help-pagina Patroondetectiecode.
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# UMI {#umi}

Probleem met verkeerde configuratie van upgrade

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Probleem met verkeerde configuratie van upgrade"
>abstract="UMI identificeert wijzigingen aan bepaalde configuraties OSGi die kwesties wanneer bevordering, met inbegrip van een ontbroken verbetering of verminderde functionaliteit veroorzaken."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Opvallende wijzigingen - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service - Opmerkingen bij de release"

`UMI`  Identificeert wijzigingen aan bepaalde configuraties OSGi die kwesties wanneer bevordering, met inbegrip van een ontbroken verbetering of verminderde functionaliteit veroorzaken.

De volgende configuraties worden gecontroleerd op wijziging:

* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`
* `com.day.cq.commons.impl.ExternalizerImpl`
* `org.apache.sling.commons.log.LogManager.factory.config` : Geef aan of de `org.apache.sling.commons.log.file` eigenschap van de aangepaste loggers verwijst naar iets anders dan `logs/error.log` bestand.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* Het wijzigen of verwijderen van configuraties kan hieronder problemen veroorzaken:
   * De upgrade kan vastlopen (bijvoorbeeld `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` ontbreekt, maar aanwezig in `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`).
   * Autorisatiekwesties kunnen na upgrade optreden (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * Bepaalde functionaliteit werkt mogelijk niet zoals verwacht. Bijvoorbeeld wijzigen `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` kan ertoe leiden dat sommige JSP dossiers niet worden gecompileerd, wat uiteindelijk in verlies van functionaliteit resulteert.
   * De waarden van de configuratie ExternalAlizer `com.day.cq.commons.impl.ExternalizerImpl` worden ingesteld door de omgevingsvariabelen van de cloud-manager in AEM as a Cloud Service.
   * AEM als Cloud Servicen ondersteunt geen aangepaste logbestanden. Logboeken die naar logboeken met aangepaste namen worden geschreven, zijn niet toegankelijk vanuit AEM as a Cloud Service.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Implementatieleiding"
>abstract="De beste praktijken moeten uw huidige configuraties herzien en om het even welke veranderingen terugkeren die aan vermelde configuraties worden aangebracht om om het even welke toekomstige verbeteringskwesties te vermijden. Neem contact op met de ondersteuning van de Adobe voor hulp of verduidelijking."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Wijzig of verwijder de vier bovenstaande configuraties niet.
   * Als er sprake is van de volgende schending:\
     &quot;Vereiste eigenschappen voor de configuratie OSGi `xyz-configuration` ontbreken: &#39;[property-1,property-2...]&quot;.&quot;\
     Bevestig of deze schrappingen wettig of niet zijn omdat deze configuraties OSGI OTB zijn en nooit van de Manager van OSGi Config gewijzigd/zouden kunnen zijn bewaard.
* Als configuraties zijn gewijzigd, moeten ze worden teruggezet op de verwachte waarden. Deze waarden worden vermeld in het `UMI` berichten.
* Voor `com.day.cq.commons.impl.ExternalizerImpl`, zie [documentatie](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developer-tools/externalizer) voor het instellen van Externalzer config met gebruik van de omgevingsvariabelen van de cloud-manager in AEM as a Cloud Service.
* Voor `org.apache.sling.commons.log.LogManager.factory.config`, verander de configuratie OSGI om het aangepaste registreerapparaat naar te verzenden `logs/error.log` bestand. Zie [documentatie](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/logs) voor het opnieuw aanwijzen van `logs/error.log` bestand.
* Contact opnemen met de [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om de problemen te verhelpen.
