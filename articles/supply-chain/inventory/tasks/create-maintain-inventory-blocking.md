---
title: Opret og vedligehold en lagerblokering
description: Denne fremgangsmåde viser, hvordan du ved hjælp af lagerblokeringen forhindrer, at fysisk disponibel lagerbeholdning reserveres af udgående kildedokumenter.
author: perlynne
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5fb3c7fc5dbeb6263357113d2a9348afc5b1ac9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212741"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="255a6-103">Opret og vedligehold en lagerblokering</span><span class="sxs-lookup"><span data-stu-id="255a6-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="255a6-104">Denne fremgangsmåde viser, hvordan du ved hjælp af lagerblokeringen forhindrer, at fysisk disponibel lagerbeholdning reserveres af udgående kildedokumenter.</span><span class="sxs-lookup"><span data-stu-id="255a6-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="255a6-105">Du kan køre proceduren i USMF-demodatafirmaet ved hjælp af eksempelværdierne, der vises.</span><span class="sxs-lookup"><span data-stu-id="255a6-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="255a6-106">Du skal have en vare med en tilgængelig fysisk disponibel lagerbeholdning, før du begynder denne procedure.</span><span class="sxs-lookup"><span data-stu-id="255a6-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="255a6-107">Opret en lagerblokering</span><span class="sxs-lookup"><span data-stu-id="255a6-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="255a6-108">I **navigationsruden** skal du gå til **Moduler > Lagerstyring > Periodiske opgaver > Lagerblokering**.</span><span class="sxs-lookup"><span data-stu-id="255a6-108">In the **Navigation pane**, go to **Modules > Inventory management > Periodic tasks > Inventory blocking**.</span></span>
2. <span data-ttu-id="255a6-109">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="255a6-109">Click **New**.</span></span>
3. <span data-ttu-id="255a6-110">Klik på rullelisten i feltet **Varenummer** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="255a6-110">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="255a6-111">Vælg den vare, du vil bruge, på listen.</span><span class="sxs-lookup"><span data-stu-id="255a6-111">In the list, select the item you want to choose.</span></span> <span data-ttu-id="255a6-112">Vælg et varenummer med fysisk disponibel lagerbeholdning, du vil blokere.</span><span class="sxs-lookup"><span data-stu-id="255a6-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="255a6-113">Hvis du bruger USMF, kan du vælge vare M9201.</span><span class="sxs-lookup"><span data-stu-id="255a6-113">If you're using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="255a6-114">Angiv et tal i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="255a6-114">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="255a6-115">Hvis du bruger vare M9201, skal du vælge mindre end 200.</span><span class="sxs-lookup"><span data-stu-id="255a6-115">If you're using item M9201, you need to select less than 200.</span></span>
6. <span data-ttu-id="255a6-116">Udvid oversigtspanelet **Lagerdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="255a6-116">Expand the **Inventory dimensions** fastTab.</span></span>
7. <span data-ttu-id="255a6-117">Klik på rullelisten i feltet **Lagersted** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="255a6-117">In the **Warehouse** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="255a6-118">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="255a6-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="255a6-119">Hvis du bruger vare M9201, kan du vælge lagersted 51.</span><span class="sxs-lookup"><span data-stu-id="255a6-119">If you're using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="255a6-120">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="255a6-120">Click **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="255a6-121">Opdater betingelserne for lagerblokeringen</span><span class="sxs-lookup"><span data-stu-id="255a6-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="255a6-122">Skriv et tal i feltet **Antal** i oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="255a6-122">In the **General** fastTab, in the **Quantity** field, enter a number.</span></span> <span data-ttu-id="255a6-123">Opdater feltet fast lagerantal for at afspejle mængden, der skal blokeres.</span><span class="sxs-lookup"><span data-stu-id="255a6-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="255a6-124">Indtast en dato i feltet **Forventet dato**.</span><span class="sxs-lookup"><span data-stu-id="255a6-124">In the **Expected date** field, enter a date.</span></span> <span data-ttu-id="255a6-125">Du vil måske angive, hvornår det blokerede lager forventes at blive tilgængeligt for reservation ved at tildele en forventet dato.</span><span class="sxs-lookup"><span data-stu-id="255a6-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="255a6-126">Hvis den indstillingen Forventede tilgange er markeret for lagerblokeringen, som den er som standard, når du manuelt opretter en blokering, vises denne dato på den forventede transaktion.</span><span class="sxs-lookup"><span data-stu-id="255a6-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="255a6-127">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="255a6-127">Click **Save**.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="255a6-128">Fjern lagerblokeringen</span><span class="sxs-lookup"><span data-stu-id="255a6-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="255a6-129">Klik på **Slet** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="255a6-129">On the **Action Pane**, click **Delete**.</span></span>
2. <span data-ttu-id="255a6-130">Klik på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="255a6-130">Click **Yes**.</span></span>
3. <span data-ttu-id="255a6-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="255a6-131">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]