---
title: Aktivere anbefalinger af "Køb tilsvarende beskrivelse"
description: Dette emne beskriver, hvordan du aktiverer produktanbefalingerne "Køb tilsvarende beskrivelse" i Microsoft Dynamics 365 Commerce.
author: bsokolov
manager: AnnBe
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b6b397b1f21e3dfcdb4a2b7fe67ddb541d090a97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234383"
---
# <a name="enable-shop-similar-description-recommendations"></a>Aktivér anbefalinger af "Køb tilsvarende beskrivelse"

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du aktiverer produktanbefalingerne "Køb tilsvarende beskrivelse" i Microsoft Dynamics 365 Commerce.

Anbefalingsfunktionen "Køb tilsvarende beskrivelse" i Dynamics 365 Commerce bruger styrkerne i kunstig intelligens og maskinel læring (AI-ML) til at give anbefalinger til produkter, der er beskrivelser, der svarer til det, kunden leder efter. Når du gør anbefalinger af typen "Køb tilsvarende beskrivelse" tilgængelige for alle detailkanaler i Commerce, kan detailhandlerne hjælpe kunderne til nemt at finde det, de ønsker.

Anbefalingsfunktionen "Køb tilsvarende beskrivelse" bruger produktafbildninger af rangerede produktnavn og beskrivelse til at finde og anbefale visuelt tilsvarende produkter i en forhandlers produktkatalog.

Anbefalinger af typen "Køb tilsvarende beskrivelse" er tilgængelige i både POS- og e-handelsløsninger.

## <a name="example-scenarios"></a>Eksempelscenarier

Scenarierne nedenfor viser de typer af anbefalinger, som funktionen "køb tilsvarende beskrivelse" kan indeholde:

- En kunde får at se et par års kontekster, der ligner hinanden, og modtager et sæt anbefalinger for andre produkter, der har et lignende design i detailbranchen.
- En kunde bruger anbefalinger i "køb tilsvarende beskrivelse" til at finde kaffemærker, der ligner dem, de tidligere har købt af forhandleren.

## <a name="set-up-shop-similar-description-recommendations"></a>Konfigurere anbefalinger af "Køb tilsvarende beskrivelse"

Produktanbefalinger understøttes kun for Commerce-brugere, som har overført deres lager til Azure Data Lake Storage Gen2.

### <a name="prerequisites"></a>Forudsætninger

Før "køb tilsvarende beskrivelse" kan vises til kunder, skal du udføre følgende forudsætninger:

- [Aktiver produktanbefalinger](enable-product-recommendations.md) i Commerce Headquarters.
- Bekræft, at medieserveren understøtter HTTPS-kald.

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a>Aktivere funktionen med anbefalinger i "Køb tilsvarende beskrivelse"

Hvis du vil aktivere anbefalingsfunktionen "Køb tilsvarende beskrivelse" i Commerce Headquarters, skal du udføre disse trin.

1. I arbejdsområdet **Funktionsstyring** på listen over tilgængelige funktioner skal du søge efter og vælge **Køb tilsvarende beskrivelse**.
1. Vælg **Aktivér** i højre rude.

> [!NOTE]
> Når du aktiverer funktionen, begynder systemet at generere lister over produktanbefalinger. Der kan gå op til en dag, før disse lister er tilgængelige og synlige online og på POS-terminaler.
>
> Hvis du deaktiverer funktionen, påvirkes andre typer produktanbefalinger ikke. Yderligere oplysninger om produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a>Tilføje en knap med Køb tilsvarende beskrivelse til sider med produktoplysninger

Når du har aktiveret funktionen "Køb tilsvarende beskrivelse" i Commerce Headquarters, kan en indstilling i Commerce-webstedsgenerator lade detailhandlere føje knappen **Køb tilsvarende beskrivelse** til købefeltet på alle produktoplysningssider (PDP). En kunde, der vælger denne knap, føres til en dedikeret side af typen **Køb tilsvarende beskrivelse**, som returnerer visuelt tilsvarende produkter. Kunden kan bruge vælgere til at filtrere produkterne yderligere.

Hvis du vil tilføje knappen **Køb tilsvarende beskrivelse** til en PDP ved hjælp af Commerce-webstedsgenerator, skal du udføre disse trin.

1. Åbn en eksisterende side med webstedsgeneratoren, som indeholder et købefeltmodul.
1. Vælg købefeltmodulet i navigationsruden til venstre.
1. Marker afkrydsningsfeltet **Aktivér link til Køb tilsvarende beskrivelse** i højre navigationsrude.
1. Vælg **Gem**.
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den. Når siden er udgivet, vil PDP inkludere knappen **Køb tilsvarende beskrivelse**.

I følgende illustration vises afkrydsningsfeltet **Aktiver link til Køb tilsvarende beskrivelse** og knappen **Køb tilsvarende beskrivelse** i et PDP-eksempel i webstedsgeneratoren.

![I følgende illustration vises afkrydsningsfeltet Aktiver link til Køb tilsvarende beskrivelse og knappen Køb tilsvarende på en PDP i webstedsgeneratoren.](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over produktanbefalinger](product-recommendations.md)

[Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktivér produktanbefalinger](enable-product-recommendations.md)

[Aktivér anbefalinger af "Køb tilsvarende"](shop-similar-looks.md)

[Justere resultater for AI-ML-anbefalinger](modify-product-recommendation-results.md)

[Oprette overvågede anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Ofte stillede spørgsmål om produktanbefalinger](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]