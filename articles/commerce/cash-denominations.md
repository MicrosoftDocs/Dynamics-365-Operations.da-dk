---
title: Konfigurere kontantbeløbsangivelser for POS
description: Kontantbeløbsangivelser for sedler og mønter kan defineres i administrationen til brug for kasserere, salgsassistenter og bestyrere i butikken fra POS.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 5dbef67728e86259ee48b51c48921f6e44a61015
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793051"
---
# <a name="configure-cash-denominations-for-the-point-of-sale-pos"></a>Konfigurere kontantbeløbsangivelser for POS

[!include [banner](includes/banner.md)]

Kontantbeløbsangivelser for sedler og mønter kan defineres i administrationen til brug for kasserere, salgsassistenter og bestyrere i butikken fra POS. Disse værdienheder kan bruges som hjælp til optælling af kontanter for kasseoptællinger eller for hurtigt at gennemføre et salg.

## <a name="define-denominations"></a>Angive værdienheder

Værdienhederne angives pr. butik på siden **Konfigurer** \> indstillingen **Kontantopgørelse** fra butiksegenskaben.

![Indstillingen Kontantopgørelse](./media/image1-denomination.png)

Sådan defineres en værdienhed:

1. Klik på **Ny**.
1. Angiv typen (mønter eller seddel).
1. Angiv beløbet (værdi).

![Siden Kontantbeløbsangivelser](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a>Konfigurere funktionalitetsprofilen

Ved betaling med kontanter i POS, kan brugeren bruge seddelværdienheder til hurtigt at angive det beløb, der er betalt af kunden. I funktionalitetsprofilen kan du konfigurere de to indstillinger for visning af værdienheden i POS.

- **Større end eller lig med forfaldent beløb** – Som standard viser POS kun de seddelværdienheder, der er større end det skyldige beløb, hvilket giver mulighed for optælling med et enkelt tryk. Hvis det skyldige beløb f.eks. er $7,50, viser POS følgende værdienheder: $10, $20, $50 og $100. Ved tryk på et af disse beløb optælles salget automatisk for det pågældende beløb. $1 og $5 sedler vises ikke, da disse beløb er mindre end det skyldige beløb.
- **Alle værdienheder** – Vælg denne indstilling for altid at få vist alle seddelværdienheder i POS, uanset det skyldige beløb. Det betyder, at brugeren kan anvende en kombination af sedler til at nå det skyldige beløb. F.eks. hvis det skyldige beløb er $25,00, kan brugeren vælge $20 og $5 til at afslutte salget.


[!INCLUDE[footer-include](../includes/footer-banner.md)]