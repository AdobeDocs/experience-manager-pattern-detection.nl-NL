---
title: OCU
description: Help-pagina Patroondetectiecode.
exl-id: cb28c727-415d-436c-ab74-cf7f1f34f7c7
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# OCU {#ocu}

VEROUDERD: Verouderd codegebruik (vervangen door OU, Verouderd gebruik)

## Achtergrond {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ocu_overview"
>title="Verouderd codegebruik"
>abstract="OCU identificeert de situatie waarin sommige knopen JCR, zoals Sling of AEM componenten of uitvoer API OSGi, op een niet compatibele manier worden veranderd of verwijderd. De klant is wellicht niet op de hoogte van deze wijziging voordat een upgrade wordt uitgevoerd. Ze kunnen worden bijgewerkt naar een niet-compatibele versie of zijn helemaal niet beschikbaar."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Opvallende wijzigingen - AEM as a Cloud Service"

`OCU` geeft de situatie aan waarin sommige JCR-knooppunten, zoals Sling- of AEM-componenten of OSGi-API-exportbewerkingen, op een niet-compatibele manier worden gewijzigd of verwijderd. De klant is wellicht niet op de hoogte van deze wijziging voordat een upgrade wordt uitgevoerd. Ze kunnen worden bijgewerkt naar een niet-compatibele versie of zijn helemaal niet beschikbaar.

Aangezien de oude versies niet standaard worden geïnstalleerd, werkt de toepassing van de klant mogelijk niet correct.

## Mogelijke gevolgen en risico&#39;s {#implications-and-risks}

* De functionaliteit die afhankelijk is van een component die afgekeurde componenten of API&#39;s gebruikt, kan worden verbroken en wordt na een upgrade mogelijk niet correct omgezet.
* Sommige functies van de klanttoepassing of bepaalde AEM werken mogelijk niet correct of zijn mogelijk niet actief na een upgrade.

## Mogelijke oplossingen {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ocu_guidance"
>title="Implementatieleiding"
>abstract="De beste praktijken moeten klantencode herzien en aanpassen om de nieuwste versie van AEM componenten of APIs te gebruiken. Neem contact op met Adobe Support voor hulp en verduidelijkingen."
>additional-url="https://javadoc.io/doc/com.adobe.aem/aem-sdk-api/latest/index.html" text="ADOBE EXPERIENCE MANAGER SDK API"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Ondersteuning voor Experience Cloud"

* Korte termijn: installatie van compatibiliteitspakket kan helpen.
* Lange termijn: pas de klantcode aan om de nieuwste versie van AEM componenten of API&#39;s te gebruiken.
* Contact opnemen met de [Ondersteuningsteam AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) voor verduidelijkingen of om de problemen te verhelpen.
