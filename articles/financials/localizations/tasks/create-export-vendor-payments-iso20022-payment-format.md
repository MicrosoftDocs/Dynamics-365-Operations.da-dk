--- 
title: "Oprette og eksportere kreditorbetalinger ved hjælp af ISO20022-betalingsformat"
description: "Denne procedure viser, hvordan du opretter betalingslinjer i kreditorbetalingskladde og genererer en kreditorbetalingsfil ved hjælp af eksempel med ISO2022-overførsel."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5787edc4a041e4b571c7ab6f056f4bd0a17cf2d7
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="0e16c-103">Oprette og eksportere kreditorbetalinger ved hjælp af ISO20022-betalingsformat</span><span class="sxs-lookup"><span data-stu-id="0e16c-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e16c-104">Denne procedure viser, hvordan du opretter betalingslinjer i kreditorbetalingskladde og genererer en kreditorbetalingsfil ved hjælp af eksempel med ISO2022-overførsel.</span><span class="sxs-lookup"><span data-stu-id="0e16c-104">This procedure shows how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span> 

<span data-ttu-id="0e16c-105">Det demodatafirma, der bruges til at oprette denne procedure, er DEMF.</span><span class="sxs-lookup"><span data-stu-id="0e16c-105">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="0e16c-106">Det er den femte procedure af fem, der illustrerer kreditors betalingsproces ved hjælp af konfigurationer af elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="0e16c-106">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="0e16c-107">Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="0e16c-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-payment-lines"></a><span data-ttu-id="0e16c-108">Opret betalingslinjer</span><span class="sxs-lookup"><span data-stu-id="0e16c-108">Create payment lines</span></span>
1. <span data-ttu-id="0e16c-109">Gå til Kreditor > Betalinger > Betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="0e16c-109">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="0e16c-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0e16c-110">Click New.</span></span>
3. <span data-ttu-id="0e16c-111">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0e16c-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="0e16c-112">Indtast eller vælg en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e16c-112">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="0e16c-113">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="0e16c-113">Click Lines.</span></span>
6. <span data-ttu-id="0e16c-114">Klik på Betalingsforslag.</span><span class="sxs-lookup"><span data-stu-id="0e16c-114">Click Payment proposal.</span></span>
7. <span data-ttu-id="0e16c-115">Klik på Opret betalingsforslag.</span><span class="sxs-lookup"><span data-stu-id="0e16c-115">Click Create payment proposal.</span></span>
8. <span data-ttu-id="0e16c-116">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="0e16c-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="0e16c-117">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="0e16c-117">Click Filter.</span></span>
10. <span data-ttu-id="0e16c-118">Markér rækken til tabellen Leverandører og feltet Kreditorkonto på listen.</span><span class="sxs-lookup"><span data-stu-id="0e16c-118">In the list, select the row for Vendors table and Vendor account field.</span></span>
11. <span data-ttu-id="0e16c-119">Indtast eller vælg en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="0e16c-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="0e16c-120">Du kan anvende kriterier efter eget valg for udvælgelse af kreditorposteringer, der skal betales. I dette eksempel bruges DE 001 som en kreditorkonto.</span><span class="sxs-lookup"><span data-stu-id="0e16c-120">You can apply any criteria for selecting vendor transactions to pay, for this example use DE-001 as a vendor account.</span></span>  
12. <span data-ttu-id="0e16c-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e16c-121">Click OK.</span></span>
13. <span data-ttu-id="0e16c-122">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e16c-122">Click OK.</span></span>
14. <span data-ttu-id="0e16c-123">Klik på Opret betalinger.</span><span class="sxs-lookup"><span data-stu-id="0e16c-123">Click Create payments.</span></span>

## <a name="generate-an-iso20022-payment-file"></a><span data-ttu-id="0e16c-124">Generer en ISO20022-betalingsfil</span><span class="sxs-lookup"><span data-stu-id="0e16c-124">Generate an ISO20022 payment file</span></span>


