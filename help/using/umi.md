---
title: UMI
description: Help-pagina Patroondetectiecode.
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '352'
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

`UMI` identificeert wijzigingen in bepaalde configuraties OSGi die kwesties wanneer bevordering, met inbegrip van een ontbroken verbetering of verminderde functionaliteit veroorzaken.

De volgende configuraties worden gecontroleerd op wijziging:

* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`
* `com.day.cq.commons.impl.ExternalizerImpl`
* `org.apache.sling.commons.log.LogManager.factory.config` : Bepaal of de eigenschap `org.apache.sling.commons.log.file` van de aangepaste loggers naar een ander bestand dan `logs/error.log` verwijst.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* Het wijzigen of verwijderen van configuraties kan de volgende problemen veroorzaken:
   * De upgrade kan vastlopen (`org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` ontbreekt bijvoorbeeld, maar komt voor in `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids` ).
   * De kwesties van de vergunning kunnen na verbetering (`org.apache.sling.engine.impl.auth.SlingAuthenticator`) komen.
   * Bepaalde functionaliteit werkt mogelijk niet zoals verwacht. Als u bijvoorbeeld `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` wijzigt, kunnen sommige JSP-bestanden niet worden gecompileerd, wat uiteindelijk leidt tot verlies van functionaliteit.
   * De waarden van de Externalzer config `com.day.cq.commons.impl.ExternalizerImpl` worden ingesteld met omgevingsvariabelen van de cloud Manager in AEM as a Cloud Service.
   * AEM als Cloud Servicen ondersteunt geen aangepaste logbestanden. Logbestanden die naar logbestanden met aangepaste namen worden geschreven, zijn niet toegankelijk vanuit AEM as a Cloud Service.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Implementatieleiding"
>abstract="De beste praktijken moeten uw huidige configuraties herzien en om het even welke veranderingen terugkeren die aan vermelde configuraties worden aangebracht om om het even welke toekomstige verbeteringskwesties te vermijden. Neem contact op met de ondersteuning van de Adobe voor hulp of verduidelijking."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Wijzig of verwijder de vier bovenstaande configuraties niet.
   * Als er sprake is van de volgende schending:\
     &quot;Vereiste eigenschappen voor de configuratie OSGi `xyz-configuration` ontbreken: &quot;[ bezit-1, bezit-2... ]&quot;.\
     Bevestig of deze schrappingen wettig of niet zijn omdat deze configuraties OSGI OTB zijn en nooit van de Manager van OSGi Config gewijzigd/zouden kunnen zijn bewaard.
* Als configuraties zijn gewijzigd, moeten ze worden teruggezet op de verwachte waarden. Deze waarden worden aangegeven in de `UMI` -berichten.
* Voor `com.day.cq.commons.impl.ExternalizerImpl`, zie [ documentatie ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developer-tools/externalizer) voor het plaatsen van uiterlijk config gebruikend de milieuvariabelen van de wolkenmanager in AEM as a Cloud Service.
* Wijzig voor `org.apache.sling.commons.log.LogManager.factory.config` de configuratie van OSGI zodanig dat het aangepaste logger naar het `logs/error.log` -bestand wordt verzonden. Zie [ documentatie ](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/logs) voor het opnieuw richten aan het `logs/error.log` dossier.
* Contacteer het [ AEM Team van de Steun ](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om kwesties te hebben die worden gericht.
