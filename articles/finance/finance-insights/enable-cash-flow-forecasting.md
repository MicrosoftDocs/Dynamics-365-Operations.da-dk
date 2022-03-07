---
title: Aktivere likviditetsbudget (prøveversion)
description: Dette emne forklarer, hvordan du aktiverer funktionen likviditetsbudgetforslag i Finance Insights.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: b5a4e1c3401c945df936258f0c97d2d406019438eb14a01d901f7777c8f0b7d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768909"
---
# <a name="enable-cash-flow-forecasting-preview"></a>Aktivere likviditetsbudget (prøveversion)

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du aktiverer funktionen likviditetsbudgetforslag i Finance Insights.

> [!NOTE]
> Hvis du vil bruge kontantforudsigelser i likviditeten, skal du konfigurere funktionen til debitorbetalingsforudsigelser som beskrevet i [Aktiver debitorbetalingsforudsigelser](enable-cust-paymnt-prediction.md).

1. Brug oplysninger fra miljøsiden i Microsoft Dynamics Lifecycle Services (LCS) til at oprette forbindelse til den primære forekomst af Azure SQL for det pågældende miljø. Kør følgende Transact-SQL (T-SQL)-kommando for at aktivere funktioner til sandkassemiljøet. (Du skal muligvis aktivere adgang til din IP-adresse i LCS, før du kan oprette fjernforbindelse til applikationsobjektserveren \[AOS\] .)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > Spring dette trin over, hvis du bruger version 10.0.20 eller senere, eller hvis du bruger en installation af Service Fabric. Finance Insights-team burde allerede have aktiveret funktionen til dig. Hvis du ikke kan se funktionen i arbejdsområdet **Funktionsstyring**, eller hvis der opstår problemer, når du forsøger at aktivere den, skal du kontakte <fiap@microsoft.com>.
  
2. Åbn arbejdsområdet **Funktionsstyring**, og udfør følgende trin:

    1. Vælg **Søg efter opdateringer**.
    2. Slå følgende funktioner til:

        - Nyt gitterkontrolelement
        - Gruppering i gitre (prøveversion) 
        - Forudsigelser for debitorbetaling (prøveversion)
        - Likviditetsbudgetter (prøveversion)

3. Gå til **Likviditet- og bankstyring \> Opsætning af likviditetsbudget**, og tilføj de likviditetskonti, der skal medtages i budgetterne.

    > [!NOTE]
    > Hvis der ikke er konfigureret likviditetskonti, kan likviditeten ikke genereres.

4. Gå til **Likviditet- og bankstyring \> Opsætning \> Finance Insights (prøveversion) \> Likviditetsbudgetter (prøveversion)**, og udfør disse trin:

    1. På fanen skal du vælge **Likviditetsbudget** og vælge **Aktiver funktion**.
    2. Vælg **Opret forudsigelsesmodel**.

Du kan finde flere oplysninger om, hvordan du konfigurerer funktionen likviditetsbudgettering i [Likviditetsbudget](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
