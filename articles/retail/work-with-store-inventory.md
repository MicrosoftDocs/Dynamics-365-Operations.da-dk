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
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6245d37ace9f46ecce83a0cf80a014d5de898bbc
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="manage-store-inventory"></a><span data-ttu-id="699c4-103">Administer butikslager</span><span class="sxs-lookup"><span data-stu-id="699c4-103">Manage store inventory</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="699c4-104">Denne artikel beskriver de typer af dokumenter, du kan bruge til at administrere lager.</span><span class="sxs-lookup"><span data-stu-id="699c4-104">This article describes the types of documents that you can use to manage inventory.</span></span>

<span data-ttu-id="699c4-105">Du kan bruge følgende typer dokumenter til at administrere organisationens lager.</span><span class="sxs-lookup"><span data-stu-id="699c4-105">You can use the following types of documents to manage your organization's inventory.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="699c4-106">Indkøbsordrer</span><span class="sxs-lookup"><span data-stu-id="699c4-106">Purchase orders</span></span>
<span data-ttu-id="699c4-107">Indkøbsordrer oprettes på hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="699c4-107">Purchase orders are created at the head office.</span></span> <span data-ttu-id="699c4-108">Hvis et detaillagersted er medtaget i indkøbsordrehovedet, kan ordren modtages i butikken ved hjælp af Modern POS (MPOS) eller Cloud POS i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="699c4-108">If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="699c4-109">Når antallet, der er modtaget i butikken, er angivet, kan det gemmes lokalt og ændres yderligere.</span><span class="sxs-lookup"><span data-stu-id="699c4-109">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="699c4-110">Alternativt kan antallet bindes og sendes til hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="699c4-110">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="699c4-111">På hovedkontoret vises det antal, der er modtaget i butikken, i Dynamics 365 for Retail, i feltet **Modtag nu** på indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="699c4-111">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the purchase order.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="699c4-112">Flytteordrer</span><span class="sxs-lookup"><span data-stu-id="699c4-112">Transfer orders</span></span>
<span data-ttu-id="699c4-113">En flytteordre kan angive, at en bestemt butik er en lokalitet, som varerne kan afsendes fra.</span><span class="sxs-lookup"><span data-stu-id="699c4-113">A transfer order can specify that a particular store is a location that items can be shipped from.</span></span> <span data-ttu-id="699c4-114">I dette tilfælde vises flytteordren i butikken som en plukanmodning i MPOS eller Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="699c4-114">In this case, the transfer order appears at the store as a picking request in MPOS or Cloud POS.</span></span> <span data-ttu-id="699c4-115">Når de antal, der er anmodet om, er blevet plukket, gøres de bindende og sendes til hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="699c4-115">After the quantities that are requested are picked, they are committed and sent to the head office.</span></span> <span data-ttu-id="699c4-116">På hovedkontoret vises det antal, der er plukket i butikken, i Dynamics 365 for Retail, i feltet **Afsend nu** i flytteordren.</span><span class="sxs-lookup"><span data-stu-id="699c4-116">At the head office, the quantities that were picked at the store are displayed in Dynamics 365 for Retail, in the **Ship now** field on the transfer order.</span></span> <span data-ttu-id="699c4-117">En flytteordre kan angive, at en bestemt butik er en lokalitet, som varerne kan sendes til.</span><span class="sxs-lookup"><span data-stu-id="699c4-117">A transfer order may specify that a particular store is a location that items can be shipped to.</span></span> <span data-ttu-id="699c4-118">I dette tilfælde vises flytteordren i butikken som en tilgangsanmodning i MPOS eller Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="699c4-118">In this case, the transfer order appears at the store as a receiving request in MPOS or Cloud POS.</span></span> <span data-ttu-id="699c4-119">Når antallet, der er modtaget i butikken, er angivet, kan det gemmes lokalt og ændres yderligere.</span><span class="sxs-lookup"><span data-stu-id="699c4-119">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="699c4-120">Alternativt kan antallet bindes og sendes til hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="699c4-120">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="699c4-121">På hovedkontoret vises det antal, der er modtaget i butikken, i Dynamics 365 for Retail, i feltet **Modtag nu** på flytteordren.</span><span class="sxs-lookup"><span data-stu-id="699c4-121">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the transfer order.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="699c4-122">Lagerstatus</span><span class="sxs-lookup"><span data-stu-id="699c4-122">Stock counts</span></span>
<span data-ttu-id="699c4-123">Status kan enten være planlagt eller ikke-planlagt.</span><span class="sxs-lookup"><span data-stu-id="699c4-123">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="699c4-124">Planlagte statusopgørelser startes i hovedkontoret, der angiver, hvilke varer der skal optælles.</span><span class="sxs-lookup"><span data-stu-id="699c4-124">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="699c4-125">Hovedkontoret opretter et optællingsdokument, som kan modtages i butikken, hvor antallet af den disponible beholdning angives i MPOS eller Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="699c4-125">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="699c4-126">Ikke-planlagte statusoptællinger startes i en butik, og antal i den disponible lagerbeholdning opdateres i enten i MPOS eller Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="699c4-126">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="699c4-127">I modsætning til planlagt status har ikke-planlagt status ikke en foruddefineret liste over varer.</span><span class="sxs-lookup"><span data-stu-id="699c4-127">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="699c4-128">Når en status af en af typerne er fuldført, gøres den bindende og sendes til hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="699c4-128">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="699c4-129">På hovedkontoret valideres antallet og bogføres.</span><span class="sxs-lookup"><span data-stu-id="699c4-129">At the head office, the count is validated and posted.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="699c4-130">Lagersøgning</span><span class="sxs-lookup"><span data-stu-id="699c4-130">Inventory lookup</span></span>
<span data-ttu-id="699c4-131">Det aktuelle antal disponible produkter for flere butikker og lagersteder kan ses på siden Lagersøgning.</span><span class="sxs-lookup"><span data-stu-id="699c4-131">The current product quantity on hand for multiple stores and warehouses can be viewed on the Inventory lookup page.</span></span> <span data-ttu-id="699c4-132">Udover den aktuelle disponible beholdning kan det fremtidige disponible tilsagn (DTT) vises for hver enkelt butik.</span><span class="sxs-lookup"><span data-stu-id="699c4-132">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="699c4-133">Det gør du ved at vælge den butik, du vil have vist DTT for, og derefter klikke på **Vis butikkens tilgængelighed**.</span><span class="sxs-lookup"><span data-stu-id="699c4-133">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>





