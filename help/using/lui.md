---
title: LUI
description: Help-pagina Patroondetectiecode
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '783'
ht-degree: 1%

---

# LUI {#lui}

Oudere gebruikersinterface

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Oudere gebruikersinterface"
>abstract="LUI identificeert het gebruik van verouderde gebruikersinterface-elementen die niet worden aanbevolen of niet worden ondersteund in latere versies van AEM en in AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Opvallende wijzigingen - AEM as a Cloud Service"

`LUI` identificeert het gebruik van vervangen gebruikersinterface-elementen die niet worden aanbevolen of niet worden ondersteund in latere versies van AEM en in AEM as a Cloud Service.

Subtypes worden gebruikt om de verschillende types van gebruikersinterfaceelementen te identificeren die zouden moeten of moeten worden bevorderd:

* `legacy.dialog.classic`: Klassieke UI-dialoogvensters die op ExtJS zijn gebaseerd, moeten worden gewijzigd in Coral.
   * Dit wordt gedetecteerd wanneer de naam van het dialoogvenster &quot;dialog&quot; of &quot;design_dialog&quot; is en wanneer de naam `jcr:primaryType` eigenschapswaarde of de `xtype` eigenschapswaarde is &quot;cq:Dialog&quot;.
* `legacy.dialog.coral2`: Dialoogvensters voor koraal 2 moeten worden bijgewerkt om koraal 3 te gebruiken.
   * Dit wordt gedetecteerd wanneer het dialoogvenster en de onderliggende inhoudsknooppuntnamen &#39;cq:dialog/content&#39;, &#39;cq:design_dialog/content&#39;, &#39;cq:dialog.coral2/content&#39; of &#39;cq:design_dialog.coral2/content&#39; en de `sling:resourceType` eigenschapswaarde bevat niet &quot;graniet/ui/components/koral/foundation&quot;.
* `legacy.custom.component`: Componenten die overerven van `foundation/components` moet worden bijgewerkt om Core Components te gebruiken.
   * Dit wordt gedetecteerd wanneer de `jcr:primaryType` eigenschapswaarde is &quot;cq:Component&quot; en de
     `sling:resourceSuperType` eigenschapswaarde bevat &quot;foundation/components&quot; of een van de
     `sling:resourceSuperType` eigenschapswaarden van de keten van supertype-componenten bevatten &quot;foundation/components&quot;.
* `legacy.static.template`: Statische sjablonen moeten worden bijgewerkt naar bewerkbare sjablonen.
   * Dit wordt gedetecteerd wanneer de `jcr:primaryType` eigenschapswaarde is &quot;cq:Template&quot;.
* `content.fragment.template`: In inhoudsfragmentsjablonen moeten fragmentmodellen worden gemaakt ter vervanging van de fragmentsjablonen.
   * U vindt sjablonen voor inhoudsfragmenten op de volgende locaties:
      * Sjablonen voor inhoudsfragmenten buiten het vak worden opgeslagen in `/libs/settings/dam/cfm/templates`
      * Ze kunnen worden overlapt in  `/apps/settings/dam/cfm/templates`  of  `/conf/.../settings/dam/cfm/templates`(... = global of &quot;huurder&quot;)
* `translation.dictionary`: I18n-woordenboek aanwezig onder /apps.
   * /apps is onveranderlijk bij runtime en translator.html zou niet meer in AEM als wolkendienst beschikbaar zijn.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Implementatieleiding"
>abstract="De klassieke interface is niet meer beschikbaar in AEM as a Cloud Service en de standaardinterface voor ontwerpen is de interface met aanraakbediening. De beste praktijken moeten alle niet gestaafde interfaces bewegen en de verbonden aanpassingen zouden aan nieuwere eigenschappen/mogelijkheden moeten worden geheroriënteerd die met AEM as a Cloud Service compatibel zijn. Klanten kunnen de bestaande AEM Modernization Suite gebruiken om de inspanningen die nodig zijn om de AEM Sites-implementaties te moderniseren, te verminderen."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM-moderniseringstools"

* De klassieke gebruikersinterface is niet meer beschikbaar in AEM as a Cloud Service. De standaardinterface voor ontwerpen is de interface met aanraakbediening.
* Het vertrouwen op verouderde douanecomponenten kan onderhoudskosten in tijd verhogen.
* De sjablonen voor inhoudsfragmenten zijn vervangen door de modellen voor inhoudsfragmenten in AEM 6.3. Door inhoudsfragmenten te migreren die zijn gebaseerd op verouderde sjablonen naar AEM as a Cloud Service, blijven deze fragmenten behouden als functioneel, maar kunnen er geen nieuwe fragmenten worden gemaakt op basis van de verouderde sjabloon. Deze fragmenten kunnen ook niet worden geleverd met AEM GraphQL, waarvoor als schema&#39;s modellen voor inhoudsfragmenten zijn vereist.
* /apps is onveranderlijk bij runtime en translator.html zou niet meer in AEM als wolkendienst beschikbaar zijn. De I18n-woordenboeken moeten dus via de CI/CD-leiding van Git komen.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Hulpmiddelen &amp; Middelen"
>abstract="Met behulp van AEM Modernization Suite kunnen klanten de dialoog Classic (ExtJS) omzetten in de dialoogvensters Coral. De bedoeling is om klanten te helpen van de niet-ondersteunde of oudere functies over te stappen op het robuuste, moderne AEM. Deze hulpmiddelen zijn configureerbaar, configuratie-bewust en verlengbaar. Ook, verken vervanging van douanecomponenten met de reeks gestandaardiseerde Componenten van de Kern om de ontwikkelingstijd te versnellen en de onderhoudskosten van uw toepassingen te drukken."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/component/about.html" text="Componentconversie"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html" text="Kernonderdelen"

* Gebruiken [AEM Moderniseringsgereedschapsset](https://opensource.adobe.com/aem-modernize-tools/) om de benodigde inspanningen voor de modernisering van uw AEM Sites-implementaties te verminderen. Deze gereedschappen zijn onder andere:
   * Klassieke (ExtJS) Dialoogvensters naar Coral Dialogs
   * Elementaire componenten omzetten naar kerncomponenten
   * Statische sjablonen en kolombesturing voor bewerkbare sjablonen en responsief raster
   * Ontwerpdialoogvensters en ontwerpdialoogvensters voor bewerkbaar sjabloonbeleid
* Bekijk de bibliotheek met aangepaste componenten van uw project en ga zo mogelijk over naar de gestandaardiseerde set [Kernonderdelen](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html) om de ontwikkelingstijd te versnellen en de onderhoudskosten van uw toepassingen te drukken.
* U wordt aangeraden inhoudsfragmentmodellen te maken met dezelfde mogelijkheden als de oudere sjablonen en deze modellen te gebruiken voor het maken van inhoudsfragmenten die verder gaan.Zie voor [Modellen van inhoudsfragmenten](https://experienceleague.adobe.com/docs/experience-manager-65/assets/content-fragments/content-fragments-models.html?lang=en) voor meer informatie .
* I18n-woordenboeken moeten afkomstig zijn van Git via de CI/CD-pijpleiding. [Documentatie](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes.html?lang=en#apps-libs-immutable)
* Neem contact op met onze [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
