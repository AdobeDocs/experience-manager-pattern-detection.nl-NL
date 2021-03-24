---
title: LUI
description: Help-pagina Patroondetectiecode
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 2%

---


# LUI {#lui}

Oudere gebruikersinterface

## Achtergrond {#background}

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

* De klassieke gebruikersinterface is niet meer beschikbaar in AEM als Cloud Service. De standaardinterface voor ontwerpen is de interface met aanraakbediening.
* Het vertrouwen op verouderde douanecomponenten kan onderhoudskosten in tijd verhogen.

## Mogelijke oplossingen {#solutions}

* Gebruik [AEM Moderniseringsreeks](https://opensource.adobe.com/aem-modernize-tools/) om de inspanning te verminderen nodig om uw implementaties van AEM Sites te moderniseren. Deze gereedschappen zijn onder andere:
   * Klassieke (ExtJS) Dialoogvensters naar Coral Dialogs
   * Elementaire componenten omzetten naar kerncomponenten
   * Statische sjablonen en kolombesturing voor bewerkbare sjablonen en responsief raster
   * Ontwerpdialoogvensters en ontwerpdialoogvensters voor bewerkbaar sjabloonbeleid
* Bekijk de bibliotheek met aangepaste componenten van uw project en maak, indien mogelijk, een overgang naar de gestandaardiseerde [Core Components](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html) om de ontwikkelingstijd te versnellen en de onderhoudskosten van uw toepassingen te verlagen.
* Neem contact op met ons [AEM ondersteuningsteam](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor meer informatie of voor meer informatie.
