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

`LUI` Hiermee wordt het gebruik van vervangen gebruikersinterface-elementen aangegeven. Deze elementen worden niet aanbevolen of worden niet ondersteund in latere versies van AEM en in AEM as a Cloud Service.

Subtypes worden gebruikt om de verschillende types van gebruikersinterfaceelementen te identificeren die zouden moeten of moeten worden bevorderd:

* `legacy.dialog.classic`: op ExtJS gebaseerde dialoogvensters voor klassieke gebruikersinterface moeten worden gewijzigd in koraal.
   * Dit subtype wordt gedetecteerd wanneer de naam van het dialoogvenster `dialog` of `design_dialog` is en wanneer
de eigenschapwaarde `jcr:primaryType` of de eigenschapwaarde `xtype` is `cq:Dialog` .
* `legacy.dialog.coral2`: `Coral 2` dialoogvensters moeten worden bijgewerkt om te gebruiken `Coral 3` .
   * Dit subtype wordt gedetecteerd wanneer het dialoogvenster en de namen van onderliggende inhoudsknooppunten worden
      * `cq:dialog/content` ,
      * `cq:design_dialog/content` ,
      * `cq:dialog.coral2/content` ,
      * of `cq:design_dialog.coral2/content`
en de waarde van de eigenschap `sling:resourceType` bevat niet `granite/ui/components/coral/foundation` .
* `legacy.custom.component`: Componenten die overerven van `foundation/components` moeten worden bijgewerkt om Core Components te gebruiken.
   * Dit subtype wordt gedetecteerd wanneer de waarde van de eigenschap `jcr:primaryType` `cq:Component` en de eigenschap
     De waarde van de eigenschap `sling:resourceSuperType` bevat &quot;foundation / components&quot;. Of een van de
     `sling:resourceSuperType` eigenschapwaarden van de keten van supertype-componenten bevatten
&quot;stichting/componenten.&quot;
* `legacy.static.template`: statische sjablonen moeten worden bijgewerkt naar bewerkbare sjablonen.
   * Dit subtype wordt gedetecteerd wanneer de waarde van de eigenschap `jcr:primaryType` `cq:Template` is.
* `content.fragment.template`: Sjablonen voor inhoudsfragmenten moeten fragmentmodellen maken ter vervanging van fragmentsjablonen.
   * U vindt sjablonen voor inhoudsfragmenten op de volgende locaties:
      * Sjablonen voor inhoudsfragmenten buiten het vak worden opgeslagen in `/libs/settings/dam/cfm/templates`
      * Ze kunnen worden geplaatst in `/apps/settings/dam/cfm/templates` of `/conf/.../settings/dam/cfm/templates` (... = global of &quot;huurder&quot;)
* `translation.dictionary` : `I18n` woordenboek aanwezig onder `/apps` .
   * `/apps` is onveranderlijk bij runtime en translator.html zou niet meer in AEM als wolkendienst beschikbaar zijn.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Implementatieleiding"
>abstract="De klassieke gebruikersinterface is niet meer beschikbaar in AEM as a Cloud Service en de standaardinterface voor ontwerpen is de interface met aanraakbediening. De beste praktijken moeten alle niet gestaafde interfaces bewegen en de verbonden aanpassingen zouden aan nieuwere eigenschappen en mogelijkheden moeten worden verfrist die met AEM as a Cloud Service compatibel zijn. Klanten kunnen de bestaande AEM Modernization Suite gebruiken om de inspanningen te verminderen die nodig zijn om de AEM Sites-implementaties te moderniseren."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM-moderniseringstools"

* De klassieke gebruikersinterface is niet meer beschikbaar in AEM as a Cloud Service. De standaardinterface voor ontwerpen is de interface met aanraakbediening.
* Het vertrouwen op verouderde douanecomponenten kan onderhoudskosten in tijd verhogen.
* Sjablonen voor inhoudsfragmenten hebben de modellen voor inhoudsfragmenten in AEM 6.3 vervangen. Bij het migreren van inhoudsfragmenten die zijn gebaseerd op verouderde sjablonen naar AEM as a Cloud Service blijven deze fragmenten behouden als functioneel, maar het is niet mogelijk om fragmenten te maken op basis van de verouderde sjabloon. Het is ook niet mogelijk om deze fragmenten te leveren met behulp van AEM GraphQL, waarvoor Content Fragment-modellen als schema&#39;s zijn vereist.
* /apps is onveranderlijk bij runtime en translator.html zou niet meer in AEM als wolkendienst beschikbaar zijn. Daarom moeten `I18n` woordenboeken van Git door middel van CI/CD pijpleiding komen.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Hulpmiddelen en Middelen"
>abstract="Met behulp van AEM Modernization Suite kunnen klanten de dialoog Classic (ExtJS) omzetten in de dialoogvensters Coral. De bedoeling is om klanten te helpen van de niet-ondersteunde of oudere functies over te stappen op het robuuste, moderne AEM. Deze hulpmiddelen zijn configureerbaar, configuratie-bewust, en verlengbaar. Ook, verken vervanging van douanecomponenten met de reeks gestandaardiseerde Componenten van de Kern om de ontwikkelingstijd te versnellen en de onderhoudskosten van uw toepassingen te drukken."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/component/about.html" text="Componentconversie"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-core-components/using/introduction" text="Kernonderdelen"

* Om de inspanning te verminderen nodig om uw implementaties van AEM Sites te moderniseren, gebruik de [ AEM Reeks van Hulpmiddelen van de Modernisering ](https://opensource.adobe.com/aem-modernize-tools/). Deze gereedschappen zijn onder andere:
   * Klassieke (ExtJS) Dialoogvensters naar Coral Dialogs
   * Elementaire componenten omzetten naar kerncomponenten
   * Statische sjablonen en kolombesturing voor bewerkbare sjablonen en responsief raster
   * Ontwerpdialoogvensters en ontwerpdialoogvensters voor bewerkbaar sjabloonbeleid
* Herzie de bibliotheek van de douanecomponenten van uw project en overgang, indien mogelijk, aan de reeks gestandaardiseerde [ Componenten van de Kern ](https://experienceleague.adobe.com/en/docs/experience-manager-core-components/using/introduction) om de ontwikkelingstijd te versnellen en de onderhoudskosten van uw toepassingen te drukken.
* Maak modellen van inhoudsfragmenten met vergelijkbare mogelijkheden als oudere sjablonen en gebruik deze modellen voor het maken van inhoudsfragmenten in de toekomst. Zie [ Modellen van het Fragment van de Inhoud ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/content-fragments/content-fragments-models) voor meer details.
* `I18n` woordenboeken moeten afkomstig zijn van Git via de CI/CD-pijplijn. [ Documentatie ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#apps-libs-immutable)
* Contacteer het [ AEM Team van de Steun ](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om kwesties te hebben die worden gericht.
