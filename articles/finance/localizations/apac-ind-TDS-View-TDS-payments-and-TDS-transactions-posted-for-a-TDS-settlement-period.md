---
title: Få vist bogførte TDS-betalinger og -transaktioner for en TDS-afregningsperiode
description: Denne artikel forklarer, hvordan du kan få vist de betalinger og posteringer af afgifter fratrukket ved kilden (TDS), der er bogført for en afregningsperiode.
author: kailiang
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: c441b6f26636ef1f18e3910a201d02feb4350f33
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898053"
---
# <a name="view-posted-tds-payments-and-transactions-for-a-tds-settlement-period"></a>Få vist bogførte TDS-betalinger og -transaktioner for en TDS-afregningsperiode

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du kan få vist de betalinger og posteringer af afgifter fratrukket ved kilden (TDS), der er bogført for en afregningsperiode.

1. Gå til **Moms \> Indirekte skatter \> A-skat \> Afregningsperioder for A-skat**.

    [![Siden Afregningsperioder for A-skat.](./media/apac-ind-TDS-50.png)](./media/apac-ind-TDS-50.png)

2. På siden **Afregningsperioder for A-skat** skal du vælge **A-skattebetalinger** for at åbne siden **A-skattebetalinger**, hvor du kan få vist TDS-afregninger, der er foretaget for en bestemt TDS-afregningsperiode.

    Følgende oplysninger vises under fanen **Oversigt**:

    - **Dato** – Datoen for TDS-afregning.
    - **Bilag** – Bilagsnummeret på TDS-afregningstransaktionen.
    - **Skattetype** – Den skattetype, som afregningsprocessen køres for.
    - **Tax Account Number (TAN)** – TAN-nummeret for den udlignede TDS-transaktion.
    - **Afregningsperiode** – Den afregningsperiode, som TDS-afregningsprocessen køres for.
    - **Fra-dato** – Startdatoen for afregningsperioden.
    - **Til-dato** – Slutdatoen for afregningsperioden.
    - **Version af betaling af A-skat** – Versionen af betalingen for A-skat: **Oprindelig**, **Seneste korrektioner** eller **Liste over totaler**.

5. Vælg **Bilag** for at få vist bilagsposterne for TDS-transaktionen.
6. Vælg **Posteringer med indeholdt skat** for at få vist detaljerede oplysninger om de TDS-posteringer, der blev afregnet for en bestemt periode i løbet af en afregningsperiode. Vælg **Bilag** for at få vist bilagsposterne for TDS-transaktionen. Vælg **A-skattekomponenter** for at få vist det TDS-beløb, der blev beregnet pr. TDS-afgiftskomponent for en bestemt TDS-afgiftskode.
7. Luk siden **A-skattebetalinger** for at vende tilbage til siden **Afregningsperioder for A-skat**.
8. Vælg **Posteringer med indeholdt skat** for at få vist detaljerede oplysninger om de TDS-posteringer, der blev afregnet for afregningsperioden.
