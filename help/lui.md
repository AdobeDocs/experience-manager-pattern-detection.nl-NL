---
title: LUI
description: Help-pagina Patroondetectiecode
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
translation-type: tm+mt
source-git-commit: 76dc944f1592118920f89c513faf456b8aa443a9
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 2%

---

# LUI {#lui}

Oudere gebruikersinterface

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Oudere gebruikersinterface"
>abstract="LUI identificeert het gebruik van verouderde gebruikersinterface-elementen die niet worden aanbevolen of niet worden ondersteund in latere versies van AEM en in AEM als Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Opvallende wijzigingen - AEM als Cloud Service"

`LUI` identificeert het gebruik van vervangen gebruikersinterface-elementen die niet worden aanbevolen of niet worden ondersteund in latere versies van AEM en in AEM als Cloud Service.

Subtypes worden gebruikt om de verschillende types van gebruikersinterfaceelementen te identificeren die zouden moeten of moeten worden bevorderd:

* `legacy.dialog.classic`: Klassieke UI-dialoogvensters die zijn gebaseerd op ExtJS, moeten worden gewijzigd in Coral.
   * Dit wordt gedetecteerd wanneer de naam van het dialoogvenster &quot;dialog&quot; of &quot;design_dialog&quot; is en wanneer
de waarde van de eigenschap `jcr:primaryType` of de waarde van de eigenschap `xtype` is &quot;cq:Dialog&quot;.
* `legacy.dialog.coral2`: Coral 2 dialogs, moet worden bijgewerkt om Coral 3 te gebruiken.
   * Dit wordt gedetecteerd wanneer het dialoogvenster en de namen van onderliggende inhoudsknooppunten &#39;cq:dialog/content&#39; zijn,
&quot;cq:design_dialog/content&quot;, &quot;cq:dialog.coral2/content&quot; of &quot;cq:design_dialog.coral2/content&quot;
en de eigenschapswaarde `sling:resourceType` bevat niet
&quot;graniet/ui/componenten/koraal/stichting&quot;.
* `legacy.custom.component`: Componenten die overerven van  `foundation/components`, moeten worden bijgewerkt om Core Components te gebruiken.
   * Dit wordt gedetecteerd wanneer de waarde van de eigenschap `jcr:primaryType` &quot;cq:Component&quot; is en de eigenschap
      `sling:resourceSuperType` eigenschapswaarde bevat &quot;foundation/components&quot; of een van de
      `sling:resourceSuperType` eigenschapswaarden van de keten van supertype-componenten bevatten &quot;foundation/components&quot;.
* `legacy.static.template`: De statische Malplaatjes, zouden aan Editable Malplaatjes moeten worden bevorderd.
   * Dit wordt ontdekt wanneer de `jcr:primaryType` bezitswaarde &quot;cq:Malplaatje&quot;is.

## Mogelijke implicaties en risico&#39;s {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Implementatieleiding"
>abstract="De klassieke UI is niet meer beschikbaar in AEM als Cloud Service en de standaardinterface voor creatie is Touch-Toegelaten UI. De beste praktijken moeten alle niet gestaafde interfaces bewegen en de verbonden aanpassingen zouden aan nieuwere eigenschappen/mogelijkheden moeten worden refactored die met AEM als Cloud Service compatibel zijn. Klanten kunnen de bestaande AEM Modernization Suite gebruiken om de inspanningen te verminderen die nodig zijn om de AEM Sites-implementaties te moderniseren."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM-moderniseringstools"

* De klassieke gebruikersinterface is niet meer beschikbaar in AEM als Cloud Service. De standaardinterface voor ontwerpen is de interface met aanraakbediening.
* Het vertrouwen op verouderde douanecomponenten kan onderhoudskosten in tijd verhogen.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Hulpmiddelen &amp; Middelen"
>abstract="Met behulp van AEM Modernization Suite kunnen klanten de dialoog Classic (ExtJS) omzetten in de dialoogvensters Coral. De bedoeling is om klanten te helpen van de niet-ondersteunde of oudere functies over te stappen op het robuuste, moderne AEM. Deze hulpmiddelen zijn vervormbaar, configuratie-bewust en verlengbaar. Ook, verken vervanging van douanecomponenten met de reeks gestandaardiseerde Componenten van de Kern om de ontwikkelingstijd te versnellen en de onderhoudskosten van uw toepassingen te drukken."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/tools/component.html" text="Componentconversie"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html" text="Kernonderdelen"

* Gebruik [AEM Moderniseringsreeks](https://opensource.adobe.com/aem-modernize-tools/) om de inspanning te verminderen nodig om uw implementaties van AEM Sites te moderniseren. Deze gereedschappen zijn onder andere:
   * Klassieke (ExtJS) Dialoogvensters naar Coral Dialogs
   * Elementaire componenten omzetten naar kerncomponenten
   * Statische sjablonen en kolombesturing voor bewerkbare sjablonen en responsief raster
   * Ontwerpdialoogvensters en ontwerpdialoogvensters voor bewerkbaar sjabloonbeleid
* Bekijk de bibliotheek met aangepaste componenten van uw project en maak, indien mogelijk, een overgang naar de gestandaardiseerde [Core Components](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html) om de ontwikkelingstijd te versnellen en de onderhoudskosten van uw toepassingen te verlagen.
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
