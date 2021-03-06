---
title: Tilføje produktanbefalinger på POS
description: Dette emne beskriver brugen af produktanbefalinger på en POS-enhed.
author: bebeale
ms.date: 05/26/2020
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
ms.openlocfilehash: a1a25e3d5bc1cc5c1c7509186451fdfef50dd6cf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792333"
---
# <a name="add-product-recommendations-on-pos"></a>Tilføje produktanbefalinger på POS

[!include [banner](includes/banner.md)]

I sin kerne er produktanbefalinger et tværgående forretningsprogram, der dækker alle Commerce-områder for at skabe avancerede, spændende og skræddersyede oplevelser med produktregistrering. Hvis du vil implementere denne funktion på POS, skal du følge trinnene under [Sådan tilføjer du anbefalinger på dine POS-enheder.](add-recommendations-control-pos-screen.md) 

Yderligere oplysninger om funktioner for produktanbefalinger finder du under [Oversigt over produktanbefalinger.](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>Scenarier

Produktanbefalinger er aktiveret for følgende POS-scenarier. De er tilgængelige i Cloud POS eller Modern POS (MPOS).

1. På siden **Produktdetaljer**:

    - Hvis en medarbejder går ind på siden **Produktdetaljer**, når vedkommende ser på tidligere transaktioner på tværs af forskellige kanaler, foreslår anbefalingstjenesten flere varer, det er sandsynligt at købe sammen.

    [![Anbefalinger på siden Produktdetaljer](./media/proddetails.png)](./media/proddetails.png)

2. På siden **Transaktion**:

    - Anbefalingsprogrammet foreslår varer baseret på hele listen med varer i kurven, der ofte købes sammen.

    > [!NOTE]
    > For at få vist anbefalinger på siden **Transaktion** skal forhandleren opdatere skærmlayoutet i Dynamics 365 Commerce. Kontrolelementet **Anbefalinger** skal slippes på siden **Transaktion**.

    [![Anbefalinger på siden Transaktion](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>Konfigurere Commerce til aktivering af POS-anbefalinger

Benyt følgende fremgangsmåde for at konfigurere produktanbefalinger:

1. Kontrollér, at din tjeneste er blevet opdateret til **10.0.6-buildet.**
2. Følg instruktionerne i, hvordan du kan [aktivere produktanbefalinger](../commerce/enable-product-recommendations.md) for din virksomhed.
3. Valgfrit: For at få vist anbefalinger på skærmbilledet Transaktion, skal du gå til **Skærmlayout**, vælge dit skærmlayout, starte **skærmlayoutdesigneren** og derefter slippe kontrolelementet med **anbefalinger**, hvor der er behov for det.
4. Gå til **Commerce-parametre**, vælg **Maskinel indlæring**, og vælg **Ja** under **Aktivér POS-anbefalinger**.
5. For at se anbefalinger på et POS skal du kører det globale konfigurationsjob **1110**. For at afspejle ændringer i POS-skærmlayoutdesigneren skal du køre kanalkonfigurationsjobbet **1070**.

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>Foretage fejlfinding af problemer, hvor produktanbefalingerne allerede er aktiveret

- Gå til **Commerce-parametre** \> **Anbefalingslister** \> **Deaktiver produktanbefalinger**, og kør **Globalt konfigurationsjob \[9999\]**. 
- Hvis du har føjet **Kontrolelement til anbefalinger** til din transaktionsskærm ved hjælp af **Designer for skærmlayout**, skal du også fjerne det.
- Hvis du har flere spørgsmål, kan du se [Ofte stillede spørgsmål om produktanbefalinger](../commerce/faq-recommendations.md) for at få yderligere oplysninger.

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