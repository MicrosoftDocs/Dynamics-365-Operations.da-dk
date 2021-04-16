---
title: Oprette en plan for et sted
description: Produktionsplanlæggeren beregner materiale- og kapacitetskravene for produktionen af en bestemt vare.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf3016e289248acafc3bc6b79d853fd9de8c5417
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841641"
---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="94ccf-103">Oprette en plan for et sted</span><span class="sxs-lookup"><span data-stu-id="94ccf-103">Create a plan for a site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="94ccf-104">Produktionsplanlæggeren beregner materiale- og kapacitetskravene for produktionen af en bestemt vare.</span><span class="sxs-lookup"><span data-stu-id="94ccf-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="94ccf-105">Når forsyningsforslagene er oprettet, finder han ordrer på den lokation, som han planlægger og autoriserer ordrerne for, begyndende med dem, der haster.</span><span class="sxs-lookup"><span data-stu-id="94ccf-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="94ccf-106">De mest hastende ordrer er dem, der skal autoriseres på den aktuelle dato.</span><span class="sxs-lookup"><span data-stu-id="94ccf-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="94ccf-107">Brug demodatafirmaet USMF til at udføre disse opgaver.</span><span class="sxs-lookup"><span data-stu-id="94ccf-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="94ccf-108">Oprette en materiale- og kapacitetsplan for en vare</span><span class="sxs-lookup"><span data-stu-id="94ccf-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="94ccf-109">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="94ccf-109">Click Master planning.</span></span>
    * <span data-ttu-id="94ccf-110">Skal du gå til standarddashboardet.</span><span class="sxs-lookup"><span data-stu-id="94ccf-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="94ccf-111">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="94ccf-111">Click Run.</span></span>
3. <span data-ttu-id="94ccf-112">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="94ccf-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="94ccf-113">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="94ccf-113">Click Filter.</span></span>
5. <span data-ttu-id="94ccf-114">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="94ccf-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="94ccf-115">Skriv en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="94ccf-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="94ccf-116">Eksempel: D0001</span><span class="sxs-lookup"><span data-stu-id="94ccf-116">Example: D0001</span></span>  
7. <span data-ttu-id="94ccf-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="94ccf-117">Click OK.</span></span>
8. <span data-ttu-id="94ccf-118">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="94ccf-118">Click OK.</span></span>
    * <span data-ttu-id="94ccf-119">Det kan tage nogle minutter.</span><span class="sxs-lookup"><span data-stu-id="94ccf-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="94ccf-120">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="94ccf-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="94ccf-121">Identificere de planlagte ordrer på varen, som haster</span><span class="sxs-lookup"><span data-stu-id="94ccf-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="94ccf-122">Åbn kolonnefilteret Varenummer.</span><span class="sxs-lookup"><span data-stu-id="94ccf-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="94ccf-123">Anvend et filter til feltet "Varenummer" med værdien "D0001" ved hjælp af filteroperatøren "begynder med".</span><span class="sxs-lookup"><span data-stu-id="94ccf-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="94ccf-124">Åbn kolonnefilteret Bestillingsdato.</span><span class="sxs-lookup"><span data-stu-id="94ccf-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="94ccf-125">Du kan anvende et filter på feltet "Bestillingsdato" med en værdi for dags dato ved hjælp af filteroperatoren "er præcis".</span><span class="sxs-lookup"><span data-stu-id="94ccf-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="94ccf-126">Autorisere alle hasteordrer på varen</span><span class="sxs-lookup"><span data-stu-id="94ccf-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="94ccf-127">Markér eller fjern markeringen af alle rækker på listen.</span><span class="sxs-lookup"><span data-stu-id="94ccf-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="94ccf-128">Klik på Autoriser.</span><span class="sxs-lookup"><span data-stu-id="94ccf-128">Click Firm.</span></span>
3. <span data-ttu-id="94ccf-129">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="94ccf-129">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]