---
title: OU
description: Help-pagina Patroondetectiecode.
exl-id: 6ec96fab-dd6e-46af-864f-05dad387cbb6
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# OU {#ou}

Verouderd gebruik

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ou_overview"
>title="Verouderd gebruik"
>abstract="OU identificeert de situatie waarin sommige knopen JCR, zoals Sling of AEM componenten of uitvoer API OSGi, op een niet compatibele manier worden veranderd of verwijderd. De klant is wellicht niet op de hoogte van deze wijziging voordat een upgrade wordt uitgevoerd. Ze kunnen worden bijgewerkt naar een niet-compatibele versie of zijn helemaal niet beschikbaar."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Opvallende wijzigingen - AEM as a Cloud Service"

`OU` geeft de situatie aan waarin sommige JCR-knooppunten, zoals Sling- of AEM-componenten of OSGi-API-exportbewerkingen, op een niet-compatibele manier worden gewijzigd of verwijderd. De klant is wellicht niet op de hoogte van deze wijziging voordat een upgrade wordt uitgevoerd. Ze kunnen worden bijgewerkt naar een niet-compatibele versie of zijn helemaal niet beschikbaar.

Aangezien de oude versies niet standaard worden geïnstalleerd, werkt de toepassing van de klant mogelijk niet correct.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* De functionaliteit die afhankelijk is van een component die afgekeurde componenten of API&#39;s gebruikt, kan worden verbroken en wordt na een upgrade mogelijk niet correct omgezet.
* Sommige functies van de klanttoepassing of bepaalde AEM werken mogelijk niet correct of zijn mogelijk niet actief na een upgrade.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ou_guidance"
>title="Implementatieleiding"
>abstract="De beste praktijken moeten klantencode herzien en aanpassen om de nieuwste versie van AEM componenten of APIs te gebruiken. Neem contact op met de ondersteuning van de Adobe voor hulp of verduidelijking."
>additional-url="https://javadoc.io/doc/com.adobe.aem/aem-sdk-api/latest/index.html" text="ADOBE EXPERIENCE MANAGER SDK API"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Korte termijn: installatie van compatibiliteitspakket kan helpen.
* Lange termijn: pas de klantcode aan om de nieuwste versie van AEM componenten of API&#39;s te gebruiken.
* Contact opnemen met de [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om de problemen te verhelpen.
