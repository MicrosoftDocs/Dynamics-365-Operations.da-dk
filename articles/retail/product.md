---
title: Produktanbefalinger på POS
description: Dette emne beskriver brugen af produktanbefalinger på en POS-enhed.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c78fc1f2f1bb08d01828a8b71ad5d3c16ad31b86
ms.sourcegitcommit: 5b53bdafa5cb9a1279576bfece0452a50383b122
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2278368"
---
# <a name="product-recommendations-on-pos"></a>Produktanbefalinger på POS

[!include [banner](includes/banner.md)]

I sin kerne er produktanbefalinger et tværgående forretningsprogram, der dækker alle detailområder for at skabe avancerede, spændende og skræddersyede oplevelser med produktregistrering. Hvis du vil implementere denne funktion på POS, skal du følge trinnene under [Sådan tilføjer du anbefalinger på dine POS-enheder.](add-recommendations-control-pos-screen.md) 

Yderligere oplysninger om funktioner for produktanbefalinger finder du under [Oversigt over produktanbefalinger.](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>Scenarier

Produktanbefalinger er aktiveret for følgende POS-scenarier. De er tilgængelige i Cloud POS eller Modern POS (MPOS).

1. På siden **Produktdetaljer**:

    - • Hvis en butiksansat går ind på siden **Produktdetaljer**, når vedkommende ser på tidligere transaktioner på tværs af forskellige kanaler, foreslår anbefalingstjenesten flere varer, det er sandsynligt at købe sammen.

    [![Anbefalinger på siden Produktdetaljer](./media/proddetails.png)](./media/proddetails.png)

2. På siden **Transaktion**:

    - • Anbefalingsprogrammet foreslår varer baseret på hele listen med varer i kurven, der ofte købes sammen.

    > [!NOTE]
    > For at få vist anbefalinger på siden **Transaktion** skal forhandleren opdatere skærmlayoutet i Dynamics 365 for Retail. Kontrolelementet **Anbefalinger** skal slippes på siden **Transaktion**.

    [![Anbefalinger på siden Transaktion](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-dynamics-365-retail-to-enable-pos-recommendations"></a>Konfigurere Dynamics 365 Retail til aktivering af POS-anbefalinger

Benyt følgende fremgangsmåde for at konfigurere produktanbefalinger:

1. Kontrollér, at din tjeneste er blevet opdateret til **10.0.6-buildet.**
2. Følg instruktionerne i, hvordan du kan [aktivere produktanbefalinger](../commerce/enable-product-recommendations.md) for din virksomhed.
3. Valgfrit: For at få vist anbefalinger på skærmbilledet Transaktion, skal du gå til **Skærmlayout**, vælge dit skærmlayout, starte **skærmlayoutdesigneren** og derefter slippe kontrolelementet med **anbefalinger**, hvor der er behov for det.
4. Gå til **Detailparametre**, vælg **Maskinel indlæring** og vælg **Ja** under **Aktivér POS-anbefalinger**.
5. For at se anbefalinger på et POS skal du kører det globale konfigurationsjob **1110**. For at afspejle ændringer i POS-skærmlayoutdesigneren skal du køre kanalkonfigurationsjobbet **1070**.



## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>Foretage fejlfinding af problemer, hvor produktanbefalingerne allerede er aktiveret

- Gå til **Detailparametre** \> **Anbefalingslister** \> **Deaktiver produktanbefalinger**, og kør **Globalt konfigurationsjob \[9999\]**. 
- Hvis du har føjet **Kontrolelement til anbefalinger** til din transaktionsskærm ved hjælp af **Designer for skærmlayout**, skal du også fjerne det.
- Hvis du har flere spørgsmål, kan du se [Ofte stillede spørgsmål om anbefalinger](../commerce/faq-recommendations.md) for at få yderligere oplysninger.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilføje et kontrolelement for anbefalinger på transaktionssiden på en POS-enhed](add-recommendations-control-pos-screen.md)
[Oversigt over produktanbefalinger](../commerce/product-recommendations.md)
[Aktivere produktanbefalinger](../commerce/enable-product-recommendations.md) 
