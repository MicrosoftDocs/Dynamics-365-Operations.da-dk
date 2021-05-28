---
title: Angive parametre for kildeskat
description: Dette emne beskriver, hvordan du angiver parametre for at aktivere funktionen til kildeskat (TDS – Tax Deducted at Source) for angivne transaktioner. Det er et nødvendigt trin for at kunne bruge funktionen til kildeskat.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023116"
---
# <a name="set-the-tds-parameters"></a>Angive parametre for kildeskat

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du angiver parametre for at aktivere funktionen til kildeskat (TDS – Tax Deducted at Source) for angivne transaktioner. Det er et nødvendigt trin for at kunne bruge funktionen til kildeskat.

1. Gå til **Finans \> Opsætning Finans \> Finansparametre**.
2. Under fanen **Direkte skatter** i sektionen **Kildeskat** skal du angive indstillingen **Aktivér kildeskat** til **Ja** for at aktivere funktionen til kildeskat samt de sider og felter, der hører under den.
3. Angiv indstillingen **Faktura** til **Ja** for at aktivere de felter, der bruges til at beregne og fratrække kildeskat på fakturaniveau.
4. Angiv indstillingen **Betaling** til **Ja** for at aktivere de felter, der bruges til at beregne og fratrække kildeskat på betalingsniveau.

    [![Fanen Direkte skatter](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)

5. Under fanen **Nummerserier** skal du finde den serie, hvor feltet **Reference** er angivet til **Betaling af A-skat**. I feltet **Nummerseriekode** for serien skal du vælge nummerseriekoden. Nummerseriekoden bruges til at generere bilagsnumre til den periodiske skatteudligningsproces.

    > [!NOTE]
    > Du kan køre den periodiske skatteudligningsproces ved at gå til **Skat \> Angivelser \> A-skat \> Betaling af A-skat**.

    [![Fanen Nummerserier](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)

6. Luk siden.
