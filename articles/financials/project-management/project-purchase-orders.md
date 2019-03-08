---
title: Indkøbsordrer til et projekt
description: I denne artikel beskrives de forskellige metoder, du kan bruge til at oprette indkøbsordrer for et projekt. Den metode, du bruger, afhænger af formålet med indkøbsordren, og hvornår de købte varer forbruges og debiteres et projekt.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 767a1805e7a2609c5c28bed891b42f7c8c3aaffc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "348681"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="04fc8-104">Indkøbsordrer til et projekt</span><span class="sxs-lookup"><span data-stu-id="04fc8-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04fc8-105">I denne artikel beskrives de forskellige metoder, du kan bruge til at oprette indkøbsordrer for et projekt.</span><span class="sxs-lookup"><span data-stu-id="04fc8-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="04fc8-106">Den metode, du bruger, afhænger af formålet med indkøbsordren, og hvornår de købte varer forbruges og debiteres et projekt.</span><span class="sxs-lookup"><span data-stu-id="04fc8-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

<span data-ttu-id="04fc8-107">Du kan i Microsoft Dynamics 365 for Finance and Operations bruge flere metoder til at oprette indkøbsordrer for et projekt.</span><span class="sxs-lookup"><span data-stu-id="04fc8-107">In Microsoft Dynamics 365 for Finance and Operations, you can use multiple methods to create purchase orders for a project.</span></span> <span data-ttu-id="04fc8-108">Den metode, du bruger, afhænger af formålet med indkøbsordren, hvornår de købte varer forbruges og hvornår de købte varer debiteres et projekt.</span><span class="sxs-lookup"><span data-stu-id="04fc8-108">The method that you use depends on the purpose of the purchase order, when the purchased items are consumed, and when the purchased items are charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="04fc8-109">Metoder til oprettelse af en indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="04fc8-109">Methods for creating a purchase order</span></span>

<span data-ttu-id="04fc8-110">Du kan bruge en af forskellige metoder til at oprette en indkøbsordre i Projektstyring og regnskab.</span><span class="sxs-lookup"><span data-stu-id="04fc8-110">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="04fc8-111">Formålet med indkøbsordren angiver, hvornår indkøbsordren bruges, og angiver derfor, hvornår varerne faktureres på et projekt.</span><span class="sxs-lookup"><span data-stu-id="04fc8-111">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="04fc8-112">Metode</span><span class="sxs-lookup"><span data-stu-id="04fc8-112">Method</span></span></th>
<th><span data-ttu-id="04fc8-113">Formål</span><span class="sxs-lookup"><span data-stu-id="04fc8-113">Purpose</span></span></th>
<th><span data-ttu-id="04fc8-114">Vareforbrug</span><span class="sxs-lookup"><span data-stu-id="04fc8-114">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="04fc8-115">Oprette en indkøbsordre direkte fra et projekt.</span><span class="sxs-lookup"><span data-stu-id="04fc8-115">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="04fc8-116">Brug denne metode til at købe varer fra en ekstern leverandør til forbrug på et projekt.</span><span class="sxs-lookup"><span data-stu-id="04fc8-116">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="04fc8-117">Du kan oprette indkøbsordren på to måder:</span><span class="sxs-lookup"><span data-stu-id="04fc8-117">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="04fc8-118">Fra selve projektet.</span><span class="sxs-lookup"><span data-stu-id="04fc8-118">From the project itself.</span></span> <span data-ttu-id="04fc8-119">I dette tilfælde er projektet allerede defineret for indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="04fc8-119">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="04fc8-120">Ved at gå til projektindkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="04fc8-120">By navigating to the project purchase order.</span></span> <span data-ttu-id="04fc8-121">Du skal både vælge den leverandør og det projekt, som indkøbsordren skal oprettes for.</span><span class="sxs-lookup"><span data-stu-id="04fc8-121">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="04fc8-122">Varer er forbrugt, når kreditorfakturaen opdateres.</span><span class="sxs-lookup"><span data-stu-id="04fc8-122">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04fc8-123">Opret en indkøbsordre fra en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="04fc8-123">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="04fc8-124">Du kan bruge denne metode til at købe varer, når du opretter en salgsordre fra et projekt.</span><span class="sxs-lookup"><span data-stu-id="04fc8-124">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="04fc8-125">Varerne er brugt, når salgsordren faktureres til kunden.</span><span class="sxs-lookup"><span data-stu-id="04fc8-125">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04fc8-126">Opret en indkøbsordre ud fra et varebehov.</span><span class="sxs-lookup"><span data-stu-id="04fc8-126">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="04fc8-127">Du kan bruge denne metode til at købe varer, når du opretter et varebehov fra et projekt.</span><span class="sxs-lookup"><span data-stu-id="04fc8-127">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="04fc8-128">Varerne bruges, når følgesedlen for varebehovet opdateres.</span><span class="sxs-lookup"><span data-stu-id="04fc8-128">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="04fc8-129">Når du opdaterer kreditorfakturaen eller følgesedlen, bliver du bedt om at opdatere følgesedlen for varebehovet.</span><span class="sxs-lookup"><span data-stu-id="04fc8-129">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="04fc8-130">Yderligere oplysninger finder du i [Modtage varer på indkøbsordre ud fra varebehov](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="04fc8-130">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

