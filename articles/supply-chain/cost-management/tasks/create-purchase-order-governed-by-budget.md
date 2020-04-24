---
title: Oprette en indkøbsordre, der er underlagt budgettet
description: Brug denne procedure, når du vil oprette en indkøbsordre, der skal kontrolleres for disponibelt budget.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa16955e0ea407555c7b52b0af37c5891be9bdbb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214278"
---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="d379f-103">Oprette en indkøbsordre, der er underlagt budgettet</span><span class="sxs-lookup"><span data-stu-id="d379f-103">Create a purchase order governed by budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d379f-104">Brug denne procedure, når du vil oprette en indkøbsordre, der skal kontrolleres for disponibelt budget.</span><span class="sxs-lookup"><span data-stu-id="d379f-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="d379f-105">Denne registrering bruger USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="d379f-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="d379f-106">Gennemse konfigurationen for budgetstyring</span><span class="sxs-lookup"><span data-stu-id="d379f-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="d379f-107">Gå til Budgettering > Opsætning > Budgetstyring > Konfiguration af budgetstyring.</span><span class="sxs-lookup"><span data-stu-id="d379f-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="d379f-108">Klik på fanen Tilgængelige budgetmidler.</span><span class="sxs-lookup"><span data-stu-id="d379f-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="d379f-109">Klik på fanen Dokumenter og journaler.</span><span class="sxs-lookup"><span data-stu-id="d379f-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="d379f-110">Klik på fanen Definer budgetstyringsregler.</span><span class="sxs-lookup"><span data-stu-id="d379f-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="d379f-111">Klik på fanen Definer budgetgrupper.</span><span class="sxs-lookup"><span data-stu-id="d379f-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="d379f-112">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d379f-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="d379f-113">Oprette indkøbsordrehovedet</span><span class="sxs-lookup"><span data-stu-id="d379f-113">Create the purchase order header</span></span>
1. <span data-ttu-id="d379f-114">Gå til Indkøb og forsyning > Indkøbsordrer > Alle indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="d379f-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="d379f-115">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d379f-115">Click New.</span></span>
3. <span data-ttu-id="d379f-116">Indtast eller vælg en værdi i feltet Kreditorkonto.</span><span class="sxs-lookup"><span data-stu-id="d379f-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="d379f-117">Udvid afsnittet Generelt.</span><span class="sxs-lookup"><span data-stu-id="d379f-117">Expand the General section.</span></span>
5. <span data-ttu-id="d379f-118">Konfigurer datoen '01-01-2016' i feltet Regnskabsdato.</span><span class="sxs-lookup"><span data-stu-id="d379f-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="d379f-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d379f-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="d379f-120">Tilføje en indkøbsordrelinje</span><span class="sxs-lookup"><span data-stu-id="d379f-120">Add a purchase order line</span></span>
1. <span data-ttu-id="d379f-121">Indtast eller vælg en værdi i feltet Indkøbskategori.</span><span class="sxs-lookup"><span data-stu-id="d379f-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="d379f-122">Indstil Antal til '2'.</span><span class="sxs-lookup"><span data-stu-id="d379f-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="d379f-123">Indtast eller vælg en værdi i feltet Enhed.</span><span class="sxs-lookup"><span data-stu-id="d379f-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="d379f-124">Angiv Enhedspris til "10000".</span><span class="sxs-lookup"><span data-stu-id="d379f-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="d379f-125">Klik på Finans.</span><span class="sxs-lookup"><span data-stu-id="d379f-125">Click Financials.</span></span>
6. <span data-ttu-id="d379f-126">Klik på Fordel beløb.</span><span class="sxs-lookup"><span data-stu-id="d379f-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="d379f-127">I feltet Finanskonto skal du angive værdien '601300-001-023--'.</span><span class="sxs-lookup"><span data-stu-id="d379f-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="d379f-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d379f-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="d379f-129">Udfør budgetkontrol</span><span class="sxs-lookup"><span data-stu-id="d379f-129">Perform budget checking</span></span>
1. <span data-ttu-id="d379f-130">Klik på Finans.</span><span class="sxs-lookup"><span data-stu-id="d379f-130">Click Financials.</span></span>
2. <span data-ttu-id="d379f-131">Klik på Udfør budgetkontrol.</span><span class="sxs-lookup"><span data-stu-id="d379f-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="d379f-132">Klik på Finans.</span><span class="sxs-lookup"><span data-stu-id="d379f-132">Click Financials.</span></span>
4. <span data-ttu-id="d379f-133">Klik på Fejl eller advarsler i forbindelse med budgetkontrol.</span><span class="sxs-lookup"><span data-stu-id="d379f-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="d379f-134">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="d379f-134">Click Close.</span></span>

