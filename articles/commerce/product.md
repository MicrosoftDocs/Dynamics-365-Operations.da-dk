---
title: Tilføje produktanbefalinger på POS
description: Denne artikel beskriver brugen af produktanbefalinger på en POS-enhed.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 170e2bf18aefc79a796620818c7100ff8e6e689a
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460050"
---
# <a name="add-product-recommendations-on-pos"></a>Tilføje produktanbefalinger på POS

[!include [banner](includes/banner.md)]

I sin kerne er produktanbefalinger et tværgående forretningsprogram, der dækker alle Commerce-områder for at skabe avancerede, spændende og skræddersyede oplevelser med produktregistrering. Hvis du vil implementere denne funktion på POS, skal du følge trinnene under [Sådan tilføjer du anbefalinger på dine POS-enheder.](add-recommendations-control-pos-screen.md) 

Yderligere oplysninger om funktioner for produktanbefalinger finder du under [Oversigt over produktanbefalinger.](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>Scenarier

Produktanbefalinger er aktiveret for følgende POS-scenarier. De er tilgængelige i Cloud POS eller Modern POS (MPOS).

1. På siden **Produktdetaljer**:

    - Hvis en medarbejder går ind på siden **Produktdetaljer**, når de ser på tidligere transaktioner på tværs af forskellige kanaler, foreslår anbefalingstjenesten flere varer, det er sandsynligt at købe sammen. Afhængigt af tilføjelsesprogrammet til tjenesten kan detailforretninger vise **Shop lignende udseende** og **shop lignende beskrivelsesanbefalinger** for produkter samt personaliserede anbefalinger for brugere, der har en tidligere købshistorik.

    [![Anbefalinger på siden Produktdetaljer.](./media/proddetails.png)](./media/proddetails.png)

2. På siden **Transaktion**:

    - Anbefalingsprogrammet foreslår varer baseret på hele listen med varer i kurven, der ofte købes sammen.

    > [!NOTE]
    > For at få vist anbefalinger på siden **Transaktion** skal forhandleren opdatere skærmlayoutet i Dynamics 365 Commerce. Kontrolelementet **Anbefalinger** skal slippes på siden **Transaktion**.

    [![Anbefalinger på siden Transaktion.](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>Konfigurere Commerce til aktivering af POS-anbefalinger 

Hvis du vil oprette produktanbefalinger, skal du bekræfte, at du har fuldført klargøringsprocessen til handelsproduktanbefalinger ved at følge trinnene i [Aktivér produktanbefalinger](../commerce/enable-product-recommendations.md). Som standard vises anbefalinger både på siden **Produktdetaljer** og på siden **Kundeoplysninger**, når du har fuldført klargøringstrinnene, og dataene er færdige. 

## <a name="add-recommendations-to-the-transaction-screen"></a>Føje anbefalinger til transaktionsskærmen

1. Hvis du vil føje anbefalinger til transaktionsskærmbilledet, skal du følge trinnene i [Føj anbefalinger til transaktionsskærmbilledet](add-recommendations-control-pos-screen.md).
1. Kør kanalkonfigurationsjobbet **1070** i Commerce Headquarters for at afspejle de ændringer, der er foretaget i POS-skærmlayoutdesigneren.

> [!NOTE] 
> Hvis du vil aktivere POS-anbefalinger ved at bruge CSV-filen (RecoMock kommaseparerede værdier), skal du implementere CSV-filen på Microsoft Dynamics-anlægsaktivbiblioteket Lifecycle Services (LCS), før du konfigurerer layoutstyringen. Hvis du bruger filen RecoMock CSV, behøver du ikke aktivere anbefalinger. CSV-filen er kun tilgængelig til demonstrationsformål. Den anbefales af kunder eller løsningsarkitekter, der ønsker at bevare udseendet af anbefalede lister til demonstrationsformål uden at skulle købe en enhed til vedligeholdelse af et lager (SKU).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over produktanbefalinger](product-recommendations.md)

[Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktivér produktanbefalinger](enable-product-recommendations.md)

[Aktivere tilpassede anbefalinger](personalized-recommendations.md)

[Fravælge tilpassede anbefalinger](personalization-gdpr.md)

[Aktivere anbefalinger af "Køb tilsvarende"](shop-similar-looks.md)

[Føje anbefalinger til transaktionsskærmen](add-recommendations-control-pos-screen.md)

[Justere resultater for AI-ML-anbefalinger](modify-product-recommendation-results.md)

[Oprette overvågede anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Oprette anbefalinger med demonstrationsdata](product-recommendations-demo-data.md)

[Ofte stillede spørgsmål om produktanbefalinger](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
