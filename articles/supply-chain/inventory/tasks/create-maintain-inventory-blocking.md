---
title: Opret og vedligehold en lagerblokering
description: Dette emne beskriver, hvordan du kan bruge lagerblokeringen til at forhindre, at den fysiske disponible lagerbeholdning reserveres af andre udgående kildedokumenter.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956152"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="19943-103">Opret og vedligehold en lagerblokering</span><span class="sxs-lookup"><span data-stu-id="19943-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="19943-104">Dette emne beskriver, hvordan du kan bruge lagerblokeringen til at forhindre, at den fysiske disponible lagerbeholdning reserveres af andre udgående kildedokumenter.</span><span class="sxs-lookup"><span data-stu-id="19943-104">This topic describes how to use an inventory blocking to prevent physical on-hand inventory from being reserved by other outbound source documents.</span></span> <span data-ttu-id="19943-105">Før du starter procedurerne i dette emne, skal du have en vare, der er tilgængelig i den fysiske disponibke lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="19943-105">Before you start the procedures in this topic, you must have an item that physical on-hand inventory is available for.</span></span>

## <a name="block-inventory"></a><span data-ttu-id="19943-106">Bloker lager</span><span class="sxs-lookup"><span data-stu-id="19943-106">Block inventory</span></span>

<span data-ttu-id="19943-107">Hvis du vil oprette en lagerblokeringspost, så lageret blokeres, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="19943-107">To create an inventory blocking record so that inventory is blocked, follow these steps.</span></span>

1. <span data-ttu-id="19943-108">Gå til **Lagerstyring \> Periodiske opgaver \> Lagerblokering**.</span><span class="sxs-lookup"><span data-stu-id="19943-108">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="19943-109">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="19943-109">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="19943-110">I overskriften i den nye blokeringspost skal du angive feltet **Varenummer** til den vare, der skal spærres, og angive en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="19943-110">On the header of the new blocking record, set the **Item number** field to the item that you want to block, and enter a description.</span></span>
1. <span data-ttu-id="19943-111">Indtast antallet af varer til blokering i feltet **Antal** i oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="19943-111">On the **General** FastTab, in the **Quantity** field, enter the number of items to block.</span></span>
1. <span data-ttu-id="19943-112">I oversigtspanelet **Lagerdimensioner** skal du angive den lokation og det lagersted, hvor de varer, du vil blokere, er placeret i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="19943-112">On the **Inventory dimensions** FastTab, specify the site and warehouse where the items that you want to block are currently located.</span></span>
1. <span data-ttu-id="19943-113">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="19943-113">On the Action Pane, select **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="19943-114">Opdater betingelserne for lagerblokeringen</span><span class="sxs-lookup"><span data-stu-id="19943-114">Update the conditions of the inventory blocking</span></span>

<span data-ttu-id="19943-115">Benyt følgende fremgangsmåde for at opdatere en lagerblokeringspost.</span><span class="sxs-lookup"><span data-stu-id="19943-115">To update an inventory blocking record, follow these steps.</span></span>

1. <span data-ttu-id="19943-116">Gå til **Lagerstyring \> Periodiske opgaver \> Lagerblokering**.</span><span class="sxs-lookup"><span data-stu-id="19943-116">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="19943-117">Vælg den relevante blokeringspost i listeruden.</span><span class="sxs-lookup"><span data-stu-id="19943-117">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="19943-118">Rediger posten efter behov.</span><span class="sxs-lookup"><span data-stu-id="19943-118">Edit the record as required.</span></span> <span data-ttu-id="19943-119">Du kan f.eks ændre værdien for feltet **Forventet dato** for at angive, hvornår det blokerede lager forventes at blive tilgængeligt for reservation.</span><span class="sxs-lookup"><span data-stu-id="19943-119">For example, you might change the value of the **Expected date** field to indicate when the blocked inventory is expected to become available for reservation.</span></span> <span data-ttu-id="19943-120">Hvis indstillingen **Forventede tilgange** er valgt, vises datoen i den forventede transaktion.</span><span class="sxs-lookup"><span data-stu-id="19943-120">If the **Expected receipts** option is selected, the date will appear on the expected transaction.</span></span> <span data-ttu-id="19943-121">(Indstillingen **Forventede tilgange** vælges som standard, når du opretter en blokeringspost manuelt.)</span><span class="sxs-lookup"><span data-stu-id="19943-121">(The **Expected receipts** option is selected by default when you manually create a blocking record.)</span></span>
1. <span data-ttu-id="19943-122">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="19943-122">On the Action Pane, select **Save**.</span></span>

## <a name="unblock-inventory"></a><span data-ttu-id="19943-123">Blokere lager</span><span class="sxs-lookup"><span data-stu-id="19943-123">Unblock inventory</span></span>

<span data-ttu-id="19943-124">Hvis du vil fjerne en lagerblokeringspost, så lagerets blokering ophæves, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="19943-124">To remove an inventory blocking record so that inventory is unblocked, follow these steps.</span></span>

1. <span data-ttu-id="19943-125">Gå til **Lagerstyring \> Periodiske opgaver \> Lagerblokering**.</span><span class="sxs-lookup"><span data-stu-id="19943-125">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="19943-126">Vælg den relevante blokeringspost i listeruden.</span><span class="sxs-lookup"><span data-stu-id="19943-126">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="19943-127">Vælg **Slet** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="19943-127">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="19943-128">Du bliver bedt om at bekræfte handlingen.</span><span class="sxs-lookup"><span data-stu-id="19943-128">You're prompted to confirm the operation.</span></span> <span data-ttu-id="19943-129">Vælg **Ja** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="19943-129">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="19943-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="19943-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
