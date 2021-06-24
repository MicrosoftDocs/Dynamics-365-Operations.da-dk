---
title: Aktivere likviditetsbudget (prøveversion)
description: Dette emne forklarer, hvordan du aktiverer funktionen likviditetsbudgetforslag i Finance Insights.
author: ShivamPandey-msft
ms.date: 06/03/2021
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
ms.openlocfilehash: ba8acb2191291e2abed5cabf234c19fe09e6c8ff
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222552"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="6ebd1-103">Aktivere likviditetsbudget (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="6ebd1-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="6ebd1-104">Dette emne forklarer, hvordan du aktiverer funktionen likviditetsbudgetforslag i Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="6ebd1-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="6ebd1-105">Hvis du vil bruge kontantforudsigelser i likviditeten, skal du konfigurere funktionen til debitorbetalingsforudsigelser som beskrevet i [Aktiver debitorbetalingsforudsigelser](enable-cust-paymnt-prediction.md).</span><span class="sxs-lookup"><span data-stu-id="6ebd1-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="6ebd1-106">Brug oplysninger fra miljøsiden i Microsoft Dynamics Lifecycle Services (LCS) til at oprette forbindelse til den primære forekomst af Azure SQL for det pågældende miljø.</span><span class="sxs-lookup"><span data-stu-id="6ebd1-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="6ebd1-107">Kør følgende Transact-SQL (T-SQL)-kommando for at aktivere funktioner til sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="6ebd1-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="6ebd1-108">(Du skal muligvis aktivere adgang til din IP-adresse i LCS, før du kan oprette fjernforbindelse til applikationsobjektserveren \[AOS\] .)</span><span class="sxs-lookup"><span data-stu-id="6ebd1-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="6ebd1-109">Spring dette trin over, hvis du bruger version 10.0.20 eller senere, eller hvis du bruger en installation af Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="6ebd1-109">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="6ebd1-110">Finance Insights-team burde allerede have aktiveret funktionen til dig.</span><span class="sxs-lookup"><span data-stu-id="6ebd1-110">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="6ebd1-111">Hvis du ikke kan se funktionen i arbejdsområdet **Funktionsstyring**, eller hvis der opstår problemer, når du forsøger at aktivere den, skal du kontakte <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="6ebd1-111">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="6ebd1-112">Åbn arbejdsområdet **Funktionsstyring**, og udfør følgende trin:</span><span class="sxs-lookup"><span data-stu-id="6ebd1-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="6ebd1-113">Vælg **Søg efter opdateringer**.</span><span class="sxs-lookup"><span data-stu-id="6ebd1-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="6ebd1-114">Slå følgende funktioner til:</span><span class="sxs-lookup"><span data-stu-id="6ebd1-114">Turn on the following features:</span></span>

        - <span data-ttu-id="6ebd1-115">Nyt gitterkontrolelement</span><span class="sxs-lookup"><span data-stu-id="6ebd1-115">New grid control</span></span>
        - <span data-ttu-id="6ebd1-116">Gruppering i gitre (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="6ebd1-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="6ebd1-117">Forudsigelser for debitorbetaling (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="6ebd1-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="6ebd1-118">Likviditetsbudgetter (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="6ebd1-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="6ebd1-119">Gå til **Likviditet- og bankstyring \> Opsætning af likviditetsbudget**, og tilføj de likviditetskonti, der skal medtages i budgetterne.</span><span class="sxs-lookup"><span data-stu-id="6ebd1-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6ebd1-120">Hvis der ikke er konfigureret likviditetskonti, kan likviditeten ikke genereres.</span><span class="sxs-lookup"><span data-stu-id="6ebd1-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="6ebd1-121">Gå til **Likviditet- og bankstyring \> Opsætning \> Finance Insights (prøveversion) \> Likviditetsbudgetter (prøveversion)**, og udfør disse trin:</span><span class="sxs-lookup"><span data-stu-id="6ebd1-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="6ebd1-122">På fanen skal du vælge **Likviditetsbudget** og vælge **Aktiver funktion**.</span><span class="sxs-lookup"><span data-stu-id="6ebd1-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="6ebd1-123">Vælg **Opret forudsigelsesmodel**.</span><span class="sxs-lookup"><span data-stu-id="6ebd1-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="6ebd1-124">Du kan finde flere oplysninger om, hvordan du konfigurerer funktionen likviditetsbudgettering i [Likviditetsbudget](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="6ebd1-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
