---
title: Få vist bogførte TDS-betalinger og -transaktioner for en TDS-afregningsperiode
description: Dette emne forklarer, hvordan du kan få vist de betalinger og posteringer af afgifter fratrukket ved kilden (TDS), der er bogført for en afregningsperiode.
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: 2bada42073e46c69101e6d31f3328a2eeb95f880
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023111"
---
# <a name="view-posted-tds-payments-and-transactions-for-a-tds-settlement-period"></a><span data-ttu-id="73789-103">Få vist bogførte TDS-betalinger og -transaktioner for en TDS-afregningsperiode</span><span class="sxs-lookup"><span data-stu-id="73789-103">View posted TDS payments and transactions for a TDS settlement period</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73789-104">Dette emne forklarer, hvordan du kan få vist de betalinger og posteringer af afgifter fratrukket ved kilden (TDS), der er bogført for en afregningsperiode.</span><span class="sxs-lookup"><span data-stu-id="73789-104">This topic explains how to view the Tax Deducted at Source (TDS) payments and transactions that were posted for a settlement period.</span></span>

1. <span data-ttu-id="73789-105">Gå til **Moms \> Indirekte skatter \> A-skat \> Afregningsperioder for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="73789-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="73789-106">[![Siden Afregningsperioder for A-skat](./media/apac-ind-TDS-50.png)](./media/apac-ind-TDS-50.png)</span><span class="sxs-lookup"><span data-stu-id="73789-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-50.png)](./media/apac-ind-TDS-50.png)</span></span>

2. <span data-ttu-id="73789-107">På siden **Afregningsperioder for A-skat** skal du vælge **A-skattebetalinger** for at åbne siden **A-skattebetalinger**, hvor du kan få vist TDS-afregninger, der er foretaget for en bestemt TDS-afregningsperiode.</span><span class="sxs-lookup"><span data-stu-id="73789-107">On the **Withholding tax settlement periods** page, select **Withholding tax payments** to open the **Withholding tax payments** page, where you can view the TDS settlements that were made for a specific TDS settlement period.</span></span>

    <span data-ttu-id="73789-108">Følgende oplysninger vises under fanen **Oversigt**:</span><span class="sxs-lookup"><span data-stu-id="73789-108">The **Overview** tab shows the following information:</span></span>

    - <span data-ttu-id="73789-109">**Dato** – Datoen for TDS-afregning.</span><span class="sxs-lookup"><span data-stu-id="73789-109">**Date** – The date of TDS settlement.</span></span>
    - <span data-ttu-id="73789-110">**Bilag** – Bilagsnummeret på TDS-afregningstransaktionen.</span><span class="sxs-lookup"><span data-stu-id="73789-110">**Voucher** – The voucher number of the TDS settlement transaction.</span></span>
    - <span data-ttu-id="73789-111">**Skattetype** – Den skattetype, som afregningsprocessen køres for.</span><span class="sxs-lookup"><span data-stu-id="73789-111">**Tax type** – The tax type that the settlement process is run for.</span></span>
    - <span data-ttu-id="73789-112">**Tax Account Number (TAN)** – TAN-nummeret for den udlignede TDS-transaktion.</span><span class="sxs-lookup"><span data-stu-id="73789-112">**Tax Account Number (TAN)** – The Tax Account Number (TAN) of the settled TDS transaction.</span></span>
    - <span data-ttu-id="73789-113">**Afregningsperiode** – Den afregningsperiode, som TDS-afregningsprocessen køres for.</span><span class="sxs-lookup"><span data-stu-id="73789-113">**Settlement period** – The settlement period that the TDS settlement process is run for.</span></span>
    - <span data-ttu-id="73789-114">**Fra-dato** – Startdatoen for afregningsperioden.</span><span class="sxs-lookup"><span data-stu-id="73789-114">**From date** – The start date of the settlement period.</span></span>
    - <span data-ttu-id="73789-115">**Til-dato** – Slutdatoen for afregningsperioden.</span><span class="sxs-lookup"><span data-stu-id="73789-115">**To date** – The end date of the settlement period.</span></span>
    - <span data-ttu-id="73789-116">**Version af betaling af A-skat** – Versionen af betalingen for A-skat: **Oprindelig**, **Seneste korrektioner** eller **Liste over totaler**.</span><span class="sxs-lookup"><span data-stu-id="73789-116">**Withholding tax payment version** – The version of the withholding tax payment: **Original**, **Latest corrections**, or **Total list**.</span></span>

5. <span data-ttu-id="73789-117">Vælg **Bilag** for at få vist bilagsposterne for TDS-transaktionen.</span><span class="sxs-lookup"><span data-stu-id="73789-117">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
6. <span data-ttu-id="73789-118">Vælg **Posteringer med indeholdt skat** for at få vist detaljerede oplysninger om de TDS-posteringer, der blev afregnet for en bestemt periode i løbet af en afregningsperiode.</span><span class="sxs-lookup"><span data-stu-id="73789-118">Select **Withholding tax transactions** to view the details of the TDS transactions that were settled for a specific period during a settlement period.</span></span> <span data-ttu-id="73789-119">Vælg **Bilag** for at få vist bilagsposterne for TDS-transaktionen.</span><span class="sxs-lookup"><span data-stu-id="73789-119">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span> <span data-ttu-id="73789-120">Vælg **A-skattekomponenter** for at få vist det TDS-beløb, der blev beregnet pr. TDS-afgiftskomponent for en bestemt TDS-afgiftskode.</span><span class="sxs-lookup"><span data-stu-id="73789-120">Select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>
7. <span data-ttu-id="73789-121">Luk siden **A-skattebetalinger** for at vende tilbage til siden **Afregningsperioder for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="73789-121">Close the **Withholding tax payments** page to return to the **Withholding tax settlement periods** page.</span></span>
8. <span data-ttu-id="73789-122">Vælg **Posteringer med indeholdt skat** for at få vist detaljerede oplysninger om de TDS-posteringer, der blev afregnet for afregningsperioden.</span><span class="sxs-lookup"><span data-stu-id="73789-122">Select **Withholding tax transactions** to view the details of the TDS transactions that were settled for the settlement period.</span></span>
