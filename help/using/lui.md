---
title: LUI
description: Help-pagina Patroondetectiecode.
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 1%

---

# LUI {#lui}

Oudere gebruikersinterface

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Oudere gebruikersinterface"
>abstract="LUI identificeert het gebruik van verouderde gebruikersinterface-elementen. Deze elementen worden niet aanbevolen of worden niet ondersteund in latere versies van AEM en in AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Opvallende wijzigingen - AEM as a Cloud Service"

`LUI`  Hiermee wordt het gebruik van vervangen gebruikersinterface-elementen aangegeven. Deze elementen worden niet aanbevolen of worden niet ondersteund in latere versies van AEM en in AEM as a Cloud Service.

Subtypes worden gebruikt om de verschillende types van gebruikersinterfaceelementen te identificeren die zouden moeten of moeten worden bevorderd:

* `legacy.dialog.classic`: Klassieke UI dialoogvakjes die op ExtJS worden gebaseerd moeten in Koraal worden veranderd.
   * Dit subtype wordt gedetecteerd wanneer de naam van het dialoogvenster is `dialog` of `design_dialog` en wanneer de `jcr:primaryType` eigenschapswaarde of de `xtype` eigenschapswaarde is `cq:Dialog`.
* `legacy.dialog.coral2`: `Coral 2` dialoogvensters moeten worden bijgewerkt om te kunnen worden gebruikt `Coral 3`.
   * Dit subtype wordt gedetecteerd wanneer het dialoogvenster en de namen van onderliggende inhoudsknooppunten worden
      * `cq:dialog/content`,
      * `cq:design_dialog/content`,
      * `cq:dialog.coral2/content`,
      * of `cq:design_dialog.coral2/content`
en de `sling:resourceType` eigenschapswaarde bevat niet `granite/ui/components/coral/foundation`.
* `legacy.custom.component`: Componenten die overerven van `foundation/components` moet worden bijgewerkt om Core Components te gebruiken.
   * Dit subtype wordt gedetecteerd wanneer de `jcr:primaryType` eigenschapswaarde is `cq:Component` en de
     `sling:resourceSuperType` eigenschapswaarde bevat &quot;foundation / components.&quot; Of een van de
     `sling:resourceSuperType` eigenschapswaarden van de keten van supertype-componenten bevatten &#39;foundation / components&#39;.
* `legacy.static.template`: Statische sjablonen moeten worden bijgewerkt naar bewerkbare sjablonen.
   * Dit subtype wordt gedetecteerd wanneer de `jcr:primaryType` eigenschapswaarde is `cq:Template`.
* `content.fragment.template`: Met inhoudsfragmentsjablonen moeten fragmentmodellen worden gemaakt ter vervanging van fragmentsjablonen.
   * U vindt sjablonen voor inhoudsfragmenten op de volgende locaties:
      * Sjablonen voor inhoudsfragmenten buiten het vak worden opgeslagen in `/libs/settings/dam/cfm/templates`
      * Ze kunnen worden overlapt in  `/apps/settings/dam/cfm/templates`  of  `/conf/.../settings/dam/cfm/templates`(... = global of &quot;huurder&quot;)
* `translation.dictionary`: `I18n` woordenboek dat aanwezig is onder `/apps`.
   * `/apps` is onveranderlijk bij runtime en translator.html zou niet meer in AEM als wolkendienst beschikbaar zijn.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Implementatieleiding"
>abstract="De klassieke interface is niet meer beschikbaar in AEM as a Cloud Service en de standaardinterface voor ontwerpen is de interface met aanraakbediening. De beste praktijken moeten alle niet gestaafde interfaces bewegen en de verbonden aanpassingen zouden aan nieuwere eigenschappen en mogelijkheden moeten worden verfrist die met AEM as a Cloud Service compatibel zijn. Klanten kunnen de bestaande AEM Modernization Suite gebruiken om de inspanningen te verminderen die nodig zijn om de AEM Sites-implementaties te moderniseren."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM-moderniseringstools"

* De klassieke gebruikersinterface is niet meer beschikbaar in AEM as a Cloud Service. De standaardinterface voor ontwerpen is de interface met aanraakbediening.
* Het vertrouwen op verouderde douanecomponenten kan onderhoudskosten in tijd verhogen.
* Sjablonen voor inhoudsfragmenten hebben de modellen voor inhoudsfragmenten in AEM 6.3 vervangen. Bij het migreren van inhoudsfragmenten die zijn gebaseerd op verouderde sjablonen om as a Cloud Service te AEM, blijven deze fragmenten behouden als functioneel, maar het is niet mogelijk om fragmenten te maken die zijn gebaseerd op de verouderde sjabloon. Het is ook niet mogelijk om deze fragmenten te leveren met behulp van AEM GraphQL, waarvoor Content Fragment-modellen als schema&#39;s zijn vereist.
* /apps is onveranderlijk bij runtime en translator.html zou niet meer in AEM als wolkendienst beschikbaar zijn. Daarom `I18n` woordenboeken moeten afkomstig zijn van Git via de CI/CD-pijplijn.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Hulpmiddelen en Middelen"
>abstract="Met behulp van AEM Modernization Suite kunnen klanten de dialoog Classic (ExtJS) omzetten in de dialoogvensters Coral. De bedoeling is om klanten te helpen van de niet-ondersteunde of oudere functies over te stappen op het robuuste, moderne AEM. Deze hulpmiddelen zijn configureerbaar, configuratie-bewust, en verlengbaar. Ook, verken vervanging van douanecomponenten met de reeks gestandaardiseerde Componenten van de Kern om de ontwikkelingstijd te versnellen en de onderhoudskosten van uw toepassingen te drukken."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/component/about.html" text="Componentconversie"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-core-components/using/introduction" text="Kernonderdelen"

* Als u de inspanningen die nodig zijn om uw AEM Sites-implementaties te moderniseren wilt verminderen, kunt u de opdracht [AEM Moderniseringsgereedschapsset](https://opensource.adobe.com/aem-modernize-tools/). Deze gereedschappen zijn onder andere:
   * Klassieke (ExtJS) Dialoogvensters naar Coral Dialogs
   * Elementaire componenten omzetten naar kerncomponenten
   * Statische sjablonen en kolombesturing voor bewerkbare sjablonen en responsief raster
   * Ontwerpdialoogvensters en ontwerpdialoogvensters voor bewerkbaar sjabloonbeleid
* Bekijk de bibliotheek met aangepaste componenten van uw project en ga zo mogelijk over naar de gestandaardiseerde set [Kernonderdelen](https://experienceleague.adobe.com/en/docs/experience-manager-core-components/using/introduction) om de ontwikkelingstijd te versnellen en de onderhoudskosten van uw toepassingen te drukken.
* Maak modellen van inhoudsfragmenten met vergelijkbare mogelijkheden als oudere sjablonen en gebruik deze modellen voor het maken van inhoudsfragmenten in de toekomst. Zie [Modellen van inhoudsfragmenten](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/content-fragments/content-fragments-models) voor meer informatie .
* `I18n` woordenboeken moeten afkomstig zijn van Git via de CI/CD-pijplijn. [Documentatie](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#apps-libs-immutable)
* Contact opnemen met de [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om de problemen te verhelpen.
