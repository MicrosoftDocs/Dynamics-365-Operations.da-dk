---
title: Konfigurere kontantbeløbsangivelser for POS
description: Kontantbeløbsangivelser for sedler og mønter kan defineres i administrationen til brug for kasserere, salgsassistenter og bestyrere i butikken fra POS.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a34ae8084c0ad55221f4ab93eb8c6481fa8c4771
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411048"
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
