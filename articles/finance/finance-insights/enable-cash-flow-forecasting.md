---
title: Aktivere likviditetsbudget
description: Denne artikel forklarer, hvordan du aktiverer funktionen likviditetsbudgetforslag i Finance Insights.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 253e3ea9c1c44573b37503f167b4cb3860683c10
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859851"
---
# <a name="enable-cash-flow-forecasting"></a>Aktivere likviditetsbudget

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du aktiverer funktionen likviditetsbudgetforslag i Finance Insights.

> [!NOTE]
> Hvis du vil bruge kontantforudsigelser i likviditeten, skal du konfigurere funktionen til debitorbetalingsforudsigelser som beskrevet i [Aktiver debitorbetalingsforudsigelser](enable-cust-paymnt-prediction.md).
  
1. Åbn arbejdsområdet **Funktionsstyring**, og udfør følgende trin:

    1. Vælg **Søg efter opdateringer**.
    2. Søg efter **Likviditetsbudgetter** under fanen **Alle**. Hvis du ikke kan finde denne funktion, skal du søge efter **(Forhåndsversion) Likviditetsbudgetter**. 
    3. Slå funktionen til.

2. Gå til **Likviditet- og bankstyring \> Opsætning af likviditetsbudget**, og tilføj de likviditetskonti, der skal medtages i budgetterne. Konfigurer også likviditetskontoen til betalinger under fanerne **Debitor** og **Kreditor**. Sørg for at genberegne likviditetsbudgettet.

    > [!NOTE]
    > Hvis der ikke er konfigureret likviditetskonti, kan likviditeten ikke genereres.
    >
    > Du kan finde flere oplysninger om, hvordan du konfigurerer likviditetsbudgetter, i [Likviditetsbudget](../cash-bank-management/cash-flow-forecasting.md).

3. Gå til **Likviditet- og bankstyring \> Opsætning \> Finance Insights (prøveversion) \> Likviditetsbudgetter (prøveversion)**, og udfør disse trin:

    1. På fanen skal du vælge **Likviditetsbudget** og vælge **Aktiver funktion**.
    2. Vælg **Opret forudsigelsesmodel**.

> [!NOTE]
> Modeltræningen **Likviditetsbudget** kræver data med 100 eller flere transaktioner, der dækker mere end ét år. Det anbefales, at du har mindst to års data med mere end 1.000 transaktioner.

Du kan finde flere oplysninger om, hvordan du konfigurerer funktionen likviditetsbudgettering i [Likviditetsbudget](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
