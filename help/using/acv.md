---
title: ACV
description: Help-pagina Patroondetectiecode
exl-id: 1dd1af45-aa56-48da-8582-c4330cded489
source-git-commit: 1558502da1a63663ba239157bc1296e0a64e9616
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# ACV {#acv}

Assets Content Validator

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Assets Content Validator"
>abstract="ACV identificeert de ontbrekende verplichte knooppunten in de inhoud van elementen."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html" text="Opmerkelijke wijzigingen - Experience Manager as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="Experience Manager as a Cloud Service - Opmerkingen bij de release"

`ACV`  In de Content Validator van de elementen worden de ontbrekende verplichte knooppunten en overtredingen in de inhoud van de elementen geïdentificeerd. Dit kan ertoe leiden dat bepaalde elementen van Activa op as a Cloud Service Experience Manager niet correct zijn.

Subtypes worden gebruikt om de verschillende soorten informatie te identificeren, zoals:

* `missing.jcrcontent`: Identificeer de mappen met ontbrekende verplichte knooppunten in de opslagplaats. Door eventuele ontbrekende inhoud in de opslagplaats te identificeren, kunt u eventuele defecte functies of gebruiksgevallen voorkomen.
* `missing.original.rendition`: Identificeer de activa met een ontbrekende verplichte oorspronkelijke vertoning in de bewaarplaats. Voor voorvertoningspagina&#39;s van PDF in het veld Opmerking hoeft geen subassets te worden gegenereerd in AEMaaCS. Voor PDF-elementen wordt dus de rapportage van subactiva die de oorspronkelijke uitvoering missen, onderdrukt.
* `metadata.descendants.violation`: Identificeer de elementen met meer dan 100 afstammingen onder het metagegevensknooppunt van het element in de gegevensopslagruimte.
* `conflict.node`: Identificeer de aanwezigheid van conflictknooppunten in de opslagplaats onder /content/dam/ path.
* `psb.file.large`: Identificeer grote PSB-bestanden (dc:format: application/vnd.3gpp.pic-bw-small) met een grootte groter dan 2 gigabytes.
* `invalid.asset.name`: Identificeer elementen met ongeldige tekens[* / : [\] | # % { } ? &amp;] in de naam.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* Dit kan tot mislukken van bepaalde eigenschappen van Activa leiden die van geërfte eigenschappen in as a Cloud Service Experience Manager afhangen.
* AEM Assets is afhankelijk van het bestaan van de oorspronkelijke uitvoering. De verwerking van het element in de Cloud Service verloopt in een lus als de oorspronkelijke uitvoering ontbreekt. Het genereren van submiddelen wordt niet ondersteund in AEMaaCS.
* Een hoog aantal afstammingen onder het knooppunt metadata kan het laden van mappen die bestaan uit elementen die dit overtreden, vertragen.
* Aanwezigheid van conflictknooppunten kan leiden tot inname bij AEM as a Cloud Service.
* Experience Manager verwerkt mogelijk geen PSB-bestanden met zeer hoge resolutie. Klanten die ImageMagick gebruiken voor het verwerken van grote bestanden kunnen worden geconfronteerd met een negatieve invloed op de prestaties als benchmarking van de Experience Manager-server niet is uitgevoerd.
* Ongeldige tekens in de naam van het element kunnen leiden tot fouten tijdens het migreren naar AEM as a Cloud Service.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Implementatieleiding"
>abstract="Adobe raadt aan de inhoudsstructuur te controleren om te voorkomen dat werkstromen die afhankelijk zijn van overgenomen eigenschappen, worden verbroken. Neem contact op met de klantenservice voor hulp."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Analyseer een map als er een onderliggend knooppunt ontbreekt. Maak de knooppunten handmatig als het aantal mappen kan worden beheerd. Gebruik anders een script.
* Voor de elementen die de oorspronkelijke uitvoering missen, uploadt u de elementen opnieuw of verwijdert u deze voordat u migreert.
* Geen actie vereist voor ontbrekende subassets van oorspronkelijke uitvoering.
* In het geval van conflictknooppunten moeten ze worden opgelost of moeten ze mogelijk worden verwijderd voordat ze naar AEM as a Cloud Service worden gemigreerd.
* Neem contact op met de klantenondersteuning van de Adobe als u van plan bent om veel grote PSD- of PSB-bestanden te verwerken. Experience Manager verwerkt PSB-bestanden met zeer hoge resolutie die groter zijn dan 30000 x 23000 pixels mogelijk niet. Zie [documentatie](https://experienceleague.adobe.com/docs/experience-manager-65/assets/extending/best-practices-for-imagemagick.html).
* Bereik uit naar onze [Klantenzorgteam van Experience Manager](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) om verduidelijkingen te krijgen of om problemen aan te pakken.
