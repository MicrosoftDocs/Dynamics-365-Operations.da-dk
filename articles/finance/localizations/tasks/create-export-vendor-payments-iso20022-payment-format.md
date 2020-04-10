---
title: Oprette og eksportere kreditorbetalinger ved hjælp af ISO20022-betalingsformat
description: Denne procedure viser, hvordan du opretter betalingslinjer i kreditorbetalingskladde og genererer en kreditorbetalingsfil ved hjælp af eksempel med ISO2022-overførsel.
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff8a2858bfa96eb1d4b0afa1e48ebd1b578a4431
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143118"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="e0c12-103">Oprette og eksportere kreditorbetalinger ved hjælp af ISO20022-betalingsformat</span><span class="sxs-lookup"><span data-stu-id="e0c12-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e0c12-104">I dette emne beskrives, hvordan du opretter betalingslinjer i kreditorbetalingskladde og genererer en kreditorbetalingsfil ved hjælp af eksempel med ISO2022-overførsel.</span><span class="sxs-lookup"><span data-stu-id="e0c12-104">This topic explains how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span>

<span data-ttu-id="e0c12-105">Det er den femte procedure af fem, der illustrerer kreditors betalingsproces ved hjælp af konfigurationer af elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="e0c12-105">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="e0c12-106">Brug DEMF-demodata til at fuldføre dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="e0c12-106">Use the DEMF demo data to complete this example.</span></span>

## <a name="example"></a><span data-ttu-id="e0c12-107">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e0c12-107">Example</span></span>

1.    <span data-ttu-id="e0c12-108">Gå til **Kreditor > Betalinger > Betalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="e0c12-108">Go to **Accounts payable > Payments > Payment journal**.</span></span>
2.    <span data-ttu-id="e0c12-109">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e0c12-109">Click **New**.</span></span>
3.    <span data-ttu-id="e0c12-110">Indtast eller vælg en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e0c12-110">In the **Name** field, enter or select a value.</span></span>
4.    <span data-ttu-id="e0c12-111">Klik på **Linjer > Betalingsforslag > Opret betalingsforslag**.</span><span class="sxs-lookup"><span data-stu-id="e0c12-111">Click **Lines > Payment proposal > Create payment proposal**.</span></span>
5.    <span data-ttu-id="e0c12-112">Udvid sektionen **Poster, der skal indgå**.</span><span class="sxs-lookup"><span data-stu-id="e0c12-112">Expand the **Records to include** section.</span></span>
6.    <span data-ttu-id="e0c12-113">Klik på **Filtrér**.</span><span class="sxs-lookup"><span data-stu-id="e0c12-113">Click **Filter**.</span></span>
7.    <span data-ttu-id="e0c12-114">Markér rækken til tabellen **Leverandører** og feltet **Kreditorkonto** på listen.</span><span class="sxs-lookup"><span data-stu-id="e0c12-114">In the list, select the row for **Vendors table** and **Vendor account field**.</span></span>
8.    <span data-ttu-id="e0c12-115">Indtast eller vælg en værdi i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="e0c12-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="e0c12-116">Du kan anvende kriterier efter eget valg for udvælgelse af kreditorposteringer, der skal betales. I dette eksempel bruges DE 001 som en kreditorkonto.</span><span class="sxs-lookup"><span data-stu-id="e0c12-116">You can apply any criteria for selecting vendor transactions to pay, for this example, use DE-001 as a vendor account.</span></span>
12.    <span data-ttu-id="e0c12-117">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0c12-117">Click **OK**.</span></span>
13.    <span data-ttu-id="e0c12-118">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0c12-118">Click **OK**.</span></span>
14.    <span data-ttu-id="e0c12-119">Klik på **Opret betalinger**.</span><span class="sxs-lookup"><span data-stu-id="e0c12-119">Click **Create payments**.</span></span>
15. <span data-ttu-id="e0c12-120">Generer en ISO20022-betalingsfil.</span><span class="sxs-lookup"><span data-stu-id="e0c12-120">Generate an ISO20022 payment file.</span></span>
    1.    <span data-ttu-id="e0c12-121">Klik på **Generer betalinger**.</span><span class="sxs-lookup"><span data-stu-id="e0c12-121">Click **Generate payments**.</span></span>
    2.    <span data-ttu-id="e0c12-122">Indtast eller vælg en værdi i feltet **Betalingsmåde**.</span><span class="sxs-lookup"><span data-stu-id="e0c12-122">In the **Method of payment** field, enter or select a value.</span></span>
    3.    <span data-ttu-id="e0c12-123">Skriv en værdi i feltet **Filnavn**.</span><span class="sxs-lookup"><span data-stu-id="e0c12-123">In the **File name** field, type a value.</span></span> <span data-ttu-id="e0c12-124">I dette eksempel bliver den oprettede fil SEPA-kompatibel på grund af indbetalingen i EUR.</span><span class="sxs-lookup"><span data-stu-id="e0c12-124">For this example, because of the EUR payment, the generated file will be SEPA compliant.</span></span> <span data-ttu-id="e0c12-125">ISO20022-pengeoverførsel samt andre formater for kreditorbetalinger kan også bruges til oprettelse af betalinger i andre valutaer.</span><span class="sxs-lookup"><span data-stu-id="e0c12-125">ISO20022 credit transfer as well as other vendor payment formats can also be used for generating payments in other currencies.</span></span>
    4.    <span data-ttu-id="e0c12-126">Indtast eller vælg en værdi i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="e0c12-126">In the **Bank account** field, enter or select a value.</span></span>

