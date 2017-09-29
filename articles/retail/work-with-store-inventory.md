---
title: Administer butikslager
description: Denne artikel beskriver de typer af dokumenter, du kan bruge til at administrere lager.
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1fd37bcd7155c61492f5f4990685203ea97bca36
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---

# <a name="manage-store-inventory"></a><span data-ttu-id="0073f-103">Administer butikslager</span><span class="sxs-lookup"><span data-stu-id="0073f-103">Manage store inventory</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="0073f-104">Denne artikel beskriver de typer af dokumenter, du kan bruge til at administrere lager.</span><span class="sxs-lookup"><span data-stu-id="0073f-104">This article describes the types of documents that you can use to manage inventory.</span></span>

<span data-ttu-id="0073f-105">Du kan bruge følgende typer dokumenter til at administrere organisationens lager.</span><span class="sxs-lookup"><span data-stu-id="0073f-105">You can use the following types of documents to manage your organization's inventory.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="0073f-106">Indkøbsordrer</span><span class="sxs-lookup"><span data-stu-id="0073f-106">Purchase orders</span></span>
<span data-ttu-id="0073f-107">Indkøbsordrer oprettes på hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="0073f-107">Purchase orders are created at the head office.</span></span> <span data-ttu-id="0073f-108">Hvis et detaillagersted er medtaget i indkøbsordrehovedet, kan ordren modtages i butikken ved hjælp af Modern POS (MPOS) eller Cloud POS i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="0073f-108">If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="0073f-109">Når antallet, der er modtaget i butikken, er angivet, kan det gemmes lokalt og ændres yderligere.</span><span class="sxs-lookup"><span data-stu-id="0073f-109">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="0073f-110">Alternativt kan antallet bindes og sendes til hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="0073f-110">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="0073f-111">På hovedkontoret vises det antal, der er modtaget i butikken, i Dynamics 365 for Retail, i feltet **Modtag nu** på indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="0073f-111">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the purchase order.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="0073f-112">Flytteordrer</span><span class="sxs-lookup"><span data-stu-id="0073f-112">Transfer orders</span></span>
<span data-ttu-id="0073f-113">En flytteordre kan angive, at en bestemt butik er en lokalitet, som varerne kan afsendes fra.</span><span class="sxs-lookup"><span data-stu-id="0073f-113">A transfer order can specify that a particular store is a location that items can be shipped from.</span></span> <span data-ttu-id="0073f-114">I dette tilfælde vises flytteordren i butikken som en plukanmodning i MPOS eller Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="0073f-114">In this case, the transfer order appears at the store as a picking request in MPOS or Cloud POS.</span></span> <span data-ttu-id="0073f-115">Når de antal, der er anmodet om, er blevet plukket, gøres de bindende og sendes til hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="0073f-115">After the quantities that are requested are picked, they are committed and sent to the head office.</span></span> <span data-ttu-id="0073f-116">På hovedkontoret vises det antal, der er plukket i butikken, i Dynamics 365 for Retail, i feltet **Afsend nu** i flytteordren.</span><span class="sxs-lookup"><span data-stu-id="0073f-116">At the head office, the quantities that were picked at the store are displayed in Dynamics 365 for Retail, in the **Ship now** field on the transfer order.</span></span> <span data-ttu-id="0073f-117">En flytteordre kan angive, at en bestemt butik er en lokalitet, som varerne kan sendes til.</span><span class="sxs-lookup"><span data-stu-id="0073f-117">A transfer order may specify that a particular store is a location that items can be shipped to.</span></span> <span data-ttu-id="0073f-118">I dette tilfælde vises flytteordren i butikken som en tilgangsanmodning i MPOS eller Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="0073f-118">In this case, the transfer order appears at the store as a receiving request in MPOS or Cloud POS.</span></span> <span data-ttu-id="0073f-119">Når antallet, der er modtaget i butikken, er angivet, kan det gemmes lokalt og ændres yderligere.</span><span class="sxs-lookup"><span data-stu-id="0073f-119">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="0073f-120">Alternativt kan antallet bindes og sendes til hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="0073f-120">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="0073f-121">På hovedkontoret vises det antal, der er modtaget i butikken, i Dynamics 365 for Retail, i feltet **Modtag nu** på flytteordren.</span><span class="sxs-lookup"><span data-stu-id="0073f-121">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the transfer order.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="0073f-122">Lagerstatus</span><span class="sxs-lookup"><span data-stu-id="0073f-122">Stock counts</span></span>
<span data-ttu-id="0073f-123">Status kan enten være planlagt eller ikke-planlagt.</span><span class="sxs-lookup"><span data-stu-id="0073f-123">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="0073f-124">Planlagte statusopgørelser startes i hovedkontoret, der angiver, hvilke varer der skal optælles.</span><span class="sxs-lookup"><span data-stu-id="0073f-124">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="0073f-125">Hovedkontoret opretter et optællingsdokument, som kan modtages i butikken, hvor antallet af den disponible beholdning angives i MPOS eller Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="0073f-125">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="0073f-126">Ikke-planlagte statusoptællinger startes i en butik, og antal i den disponible lagerbeholdning opdateres i enten i MPOS eller Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="0073f-126">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="0073f-127">I modsætning til planlagt status har ikke-planlagt status ikke en foruddefineret liste over varer.</span><span class="sxs-lookup"><span data-stu-id="0073f-127">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="0073f-128">Når en status af en af typerne er fuldført, gøres den bindende og sendes til hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="0073f-128">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="0073f-129">På hovedkontoret valideres antallet og bogføres.</span><span class="sxs-lookup"><span data-stu-id="0073f-129">At the head office, the count is validated and posted.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="0073f-130">Lagersøgning</span><span class="sxs-lookup"><span data-stu-id="0073f-130">Inventory lookup</span></span>
<span data-ttu-id="0073f-131">Det aktuelle antal disponible produkter for flere butikker og lagersteder kan ses på siden Lagersøgning.</span><span class="sxs-lookup"><span data-stu-id="0073f-131">The current product quantity on hand for multiple stores and warehouses can be viewed on the Inventory lookup page.</span></span> <span data-ttu-id="0073f-132">Udover den aktuelle disponible beholdning kan det fremtidige disponible tilsagn (DTT) vises for hver enkelt butik.</span><span class="sxs-lookup"><span data-stu-id="0073f-132">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="0073f-133">Det gør du ved at vælge den butik, du vil have vist DTT for, og derefter klikke på **Vis butikkens tilgængelighed**.</span><span class="sxs-lookup"><span data-stu-id="0073f-133">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>





