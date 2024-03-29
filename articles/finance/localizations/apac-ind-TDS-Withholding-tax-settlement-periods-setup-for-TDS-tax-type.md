---
title: Konfigurere A-skat-afregningsperioder for TDS-skattetypen
description: Denne artikel indeholder en forklaring på, hvordan du kan konfigurere afregningsperioder for afgifter fratrukket ved kilden (TDS).
author: kailiang
ms.date: 02/12/2021
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
ms.openlocfilehash: 855bda71f0967c53166cf0a7f5e7e465146f34a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846549"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a>Konfigurere A-skat-afregningsperioder for TDS-skattetypen

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en forklaring på, hvordan du kan konfigurere afregningsperioder for afgifter fratrukket ved kilden (TDS).

1. Gå til **Moms \> Indirekte skatter \> A-skat \> Afregningsperioder for A-skat**.

    [![Siden Afregningsperioder for A-skat.](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)

2. Vælg **TDS** i feltet **Skattetype** for at konfigurere afregningsperioder for TDS-skattetypen.
3. Vælg **Ny** for at oprette en ny linje.
4. I feltet **Afregningsperiode** skal du angive et navn for TDS-afregningsperioden.
5. Indtast en beskrivelse i feltet **Beskrivelse**.
6. Vælg den TDS-myndighed, som du definerer TDS-afregningsperioden for, i feltet **A-skattemyndighed**.
7. Vælg typen af periodeinterval for TDS-afregningsperioden i feltet **Periodeinterval** i oversigtspanelet **Generelt**.
8. Angiv antallet af enheder for periodeintervaltypen i feltet **Antal enheder**.
9. Vælg startdatoen for TDS-afregningsperioden i feltet **Fra dato** i oversigtspanelet **Perioder**. Vælg slutdatoen i feltet **Til-dato**.
10. Hvis du vil oprette en efterfølgende TDS-afregningsperiode for en eksisterende periode baseret på periodeintervallet og periodeenhederne, skal du vælge **Ny periode**.
11. Hvis du vil have vist detaljerede oplysninger om den periodiske TDS-afregning, der køres for en bestemt afregningsperiode, skal du vælge **A-skattebetalinger** for at åbne siden **Betaling af A-skat**.

    > [!NOTE]
    > Du kan køre den periodiske TDS-udligningsproces ved at gå til **Finans \> Periodisk \> A-skat \> Betaling af A-skat**.

    [![Siden Betaling af A-skat.](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)

12. Luk siden.
