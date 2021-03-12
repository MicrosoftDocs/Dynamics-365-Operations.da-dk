---
title: Aktivere likviditetsbudget (prøveversion)
description: Dette emne forklarer, hvordan du aktiverer funktionen likviditetsbudgetforslag i Finance Insights.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 1977dac4a3ab66cca2248dc0124d3a06d6963f40
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978758"
---
# <a name="enable-cash-flow-forecasting-preview"></a>Aktivere likviditetsbudget (prøveversion)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emne forklarer, hvordan du aktiverer funktionen likviditetsbudgetforslag i Finance Insights.

> [!NOTE]
> Hvis du vil bruge kontantforudsigelser i likviditeten, skal du konfigurere funktionen til debitorbetalingsforudsigelser som beskrevet i [Aktiver debitorbetalingsforudsigelser](enable-cust-paymnt-prediction.md).

1. Brug oplysninger fra miljøsiden i Microsoft Dynamics Lifecycle Services (LCS) til at oprette forbindelse til den primære forekomst af Azure SQL for det pågældende miljø. Kør følgende Transact-SQL (T-SQL)-kommando for at aktivere funktioner til sandkassemiljøet. (Du skal muligvis aktivere adgang til din IP-adresse i LCS, før du kan oprette fjernforbindelse til applikationsobjektserveren \[AOS\] .)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > Hvis din installation af Microsoft Dynamics 365 Finance er en Service Fabric-installation, kan du springe dette trin over. Finance Insights-team burde allerede have aktiveret funktionen til dig. Hvis du ikke kan se funktionerne i arbejdsområdet **Funktionsstyring**, eller hvis der opstår problemer, når du forsøger at aktivere dem, skal du kontakte <fiap@microsoft.com>.
  
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

## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger

Forhåndsvisning (1) kan anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen (SLA) for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.
