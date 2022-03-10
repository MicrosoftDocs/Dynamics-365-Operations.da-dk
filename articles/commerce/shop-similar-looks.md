---
title: Aktivrtr anbefalinger af "Køb tilsvarende"
description: Dette emne beskriver, hvordan du aktiverer produktanbefalingerne "Køb tilsvarende" i Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: e70365be8484d71ef9e0e9823b0a4406b0fd2761439780cafc30e1284bda1f20
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721994"
---
# <a name="enable-shop-similar-looks-recommendations"></a>Aktivér anbefalinger af "Køb tilsvarende"

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du aktiverer produktanbefalingerne "Køb tilsvarende" i Microsoft Dynamics 365 Commerce.

Anbefalingsfunktionen "Køb tilsvarende" i Dynamics 365 Commerce bruger styrkerne i kunstig intelligens og maskinel læring (AI-ML) til at give anbefalinger af visuelt tilsvarende produkter til kunder. Når du gør anbefalinger af typen "Køb tilsvarende" tilgængelige for alle detailkanaler i Commerce, kan detailhandlerne øge kundetilfredsheden ved at hjælpe kunderne til nemt at finde det, de ønsker.

Anbefalingsfunktionen "Køb tilsvarende" bruger produktafbildninger af rangerede produktvarianter til at finde og anbefale visuelt tilsvarende produkter i en forhandlers produktkatalog. 

Anbefalinger af typen "Køb tilsvarende" er tilgængelige i både POS- og e-handelsløsninger.

### <a name="example-scenarios"></a>Eksempelscenarier

- En kunde ser en sortstribet sweater og får en anbefaling afl en lignende sweater i rødt. Kunden vælger det anbefalede produkt i stedet for det oprindeligt viste produkt og modtager derefter anbefalinger af lignende produkter i rødt. 
- En kunde bruger anbefalinger af typen "Køb tilsvarende" til at finde frem til matchende ørenringe til en ringe, som kunden er interesseret i at købe.

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a>Aktivere anbefalinger af typen "Køb tilsvarende" i Commerce Headquarters

Produktanbefalinger understøttes kun for Commerce-brugere, som har overført deres lager til Azure Data Lake Gen2.

### <a name="prerequisites"></a>Forudsætninger

Før detailhandlere kan begynde at vise anbefalingerne "Køb tilsvarende" til kunderne, kræves to forudgående trin:

- [Aktiver produktanbefalinger](enable-product-recommendations.md) i Commerce Headquarters.
- Bekræft, at medieserveren understøtter HTTPS-kald.

For at anbefalingsfunktionen kan få adgang til produktbillederne, skal detailhandlerne oprette URL-adresser for produkterne. Hvis du vil oprette URL-adresser for produkter i Commerce Headquarters, skal du udføre disse trin.

1. Gå til **Produktbilleder**.
1. Gå til handlingsruden, og vælg **Definer medieskabeloner**.
1. Vælg **Opret URL-adresser** under **URL-adresser for medier** i egenskabsruden **Definer medieskabelon**.

> [!NOTE]
> Når du aktiverer anbefalingsfunktionen "Køb tilsvarende", starter processen for oprettelse af produktanbefalinger. Der kan gå op til en dag, før disse lister er tilgængelige og synlige online og på POS-terminaler.

Hvis du vil aktivere anbefalingsfunktionen "Køb tilsvarende" i Commerce Headquarters, skal du udføre disse trin.

1. Gå til **Funktionsstyring**.
1. På listen over tilgængelige funktioner kan du søge efter og vælge **Køb tilsvarende**.
1. I højre rude skal du vælge **Aktivér** for at aktivere tjenesten.

I følgende illustration vises funktionen **Køb tilsvarende** på siden **Funktionsstyring** i Commerce Headquarters.

![Funktionen Køb tilsvarende på siden Funktionsstyring i Commerce Headquarters.](./media/enableshopsimilarlooks.png)

Når de foregående opgaver er udført, forbedres POS-klienter automatisk med et kontekstafhængigt panel for **Køb tilsvarende produkter**. Hvis du vælger **Vis flere**, kan brugere af POS-terminalen føres til en dedikeret side af typen "Køb tilsvarende", der kan filtreres yderligere.

> [!NOTE]
> Hvis du deaktiverer funktionen "Køb tilsvarende", påvirkes ingen andre typer produktanbefalinger. Yderligere oplysninger om produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a>Tilføje en knap for Køb tilsvarende til produktdetaljesider ved hjælp af Commerce-webstedsgenerator

Når du har aktiveret funktionen "Køb tilsvarende" i Commerce Headquarters, kan en indstilling i Commerce-webstedsgenerator lade detailhandlere føje knappen **Køb tilsvarende** til købefeltet på alle produktoplysningssider (PDP). En kunde, der vælger denne knap, føres til en dedikeret side af typen "Køb tilsvarende", som returnerer visuelt tilsvarende produkter. Her kan kunden bruge vælgere til at filtrere produkterne yderligere.

Hvis du vil tilføje knappen **Køb tilsvarende** til en PDP ved hjælp af Commerce-webstedsgenerator, skal du udføre disse trin.

1. Åbn en eksisterende side med webstedsgeneratoren, som indeholder et købefeltmodul.
1. Vælg købefeltmodulet i navigationsruden til venstre.
1. Marker afkrydsningsfeltet **Aktivér link til Køb tilsvarende** i højre navigationsrude.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den. Når siden er udgivet, vil PDP medtage knappen **Køb tilsvarende**.

I følgende illustration vises afkrydsningsfeltet **Aktiver link til Køb tilsvarende** og knappen **Køb tilsvarende** i et PDP-eksempel i webstedsgeneratoren.

![I følgende illustration vises afkrydsningsfeltet Aktivér link til Køb tilsvarende og knappen Køb tilsvarende på en PDP i webstedsgeneratoren.](./media/SSLecomtooling.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over produktanbefalinger](product-recommendations.md)

[Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktivér produktanbefalinger](enable-product-recommendations.md)

[Fravælge tilpassede anbefalinger](personalization-gdpr.md)

[Tilføje produktanbefalinger på POS](product.md)

[Føje anbefalinger til transaktionsskærmen](add-recommendations-control-pos-screen.md)

[Justere resultater for AI-ML-anbefalinger](modify-product-recommendation-results.md)

[Oprette overvågede anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Oprette anbefalinger med demonstrationsdata](product-recommendations-demo-data.md)

[Ofte stillede spørgsmål om produktanbefalinger](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
