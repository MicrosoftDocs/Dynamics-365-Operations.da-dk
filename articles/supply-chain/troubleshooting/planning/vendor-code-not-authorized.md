---
title: Kreditorkode er ikke godkendt for et bestemt produkt og en bestemt dato
description: Når du forsøger at autorisere et ordreforslag eller at føje en linje til en indkøbsordre, modtager du en fejlmeddelelse om, at kreditorkoden ikke er godkendt for et produkt og en dato.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294041"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a><span data-ttu-id="9a947-103">Kreditorkode er ikke godkendt for et bestemt produkt og en bestemt dato</span><span class="sxs-lookup"><span data-stu-id="9a947-103">Vendor code isn't authorized for a specific product and date</span></span>

<span data-ttu-id="9a947-104">Fejlkode: SYP4881415</span><span class="sxs-lookup"><span data-stu-id="9a947-104">Error code: SYP4881415</span></span>

## <a name="symptoms"></a><span data-ttu-id="9a947-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="9a947-105">Symptoms</span></span>

<span data-ttu-id="9a947-106">Når du forsøger at autorisere et ordreforslag eller at føje en linje til en indkøbsordre, får du vist følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="9a947-106">When you try to firm a planned order or add a line to a purchase order, you receive the following error message:</span></span>

> <span data-ttu-id="9a947-107">Kreditorkoden %1 er ikke godkendt for %2 i %3.</span><span class="sxs-lookup"><span data-stu-id="9a947-107">Vendor code %1 is not authorized for %2 on %3.</span></span>

## <a name="cause"></a><span data-ttu-id="9a947-108">Årsag</span><span class="sxs-lookup"><span data-stu-id="9a947-108">Cause</span></span>

<span data-ttu-id="9a947-109">Fejlen opstår, fordi feltet **Godkendt kontrolmetode for kreditorer** er angivet til *Kun advarsel* eller *Ikke tilladt* for det angivne produkt, og kreditoren er i øjeblikket ikke godkendt til at levere det pågældende produkt.</span><span class="sxs-lookup"><span data-stu-id="9a947-109">The error occurs because the **Approved vendor check method** field is set to *Warning only* or *Not allowed* for the specified product, and the vendor isn't currently authorized to supply that product.</span></span>

## <a name="resolution"></a><span data-ttu-id="9a947-110">Løsning</span><span class="sxs-lookup"><span data-stu-id="9a947-110">Resolution</span></span>

<span data-ttu-id="9a947-111">Du kan løse dette problem ved enten at deaktivere kreditorkontrollen for det relevante produkt eller godkende kreditoren.</span><span class="sxs-lookup"><span data-stu-id="9a947-111">To fix this issue, either disable the vendor check for the relevant product or approve the vendor.</span></span>

<span data-ttu-id="9a947-112">Benyt følgende fremgangsmåde for at deaktivere kreditorkontrollen for et produkt.</span><span class="sxs-lookup"><span data-stu-id="9a947-112">To disable the vendor check for a product, follow these steps.</span></span>

1. <span data-ttu-id="9a947-113">Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="9a947-113">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="9a947-114">Åbn det relevante produkt.</span><span class="sxs-lookup"><span data-stu-id="9a947-114">Open the relevant product.</span></span>
1. <span data-ttu-id="9a947-115">I oversigtspanelet **Indkøb** skal du angive feltet **Godkendt kontrolmetode for kreditorer** til en anden værdi end *Kun advarsel* eller *Ikke tilladt*.</span><span class="sxs-lookup"><span data-stu-id="9a947-115">On the **Purchase** FastTab, set the **Approved vendor check method** field to a value other than *Warning only* or *Not allowed*.</span></span>

<span data-ttu-id="9a947-116">Benyt følgende fremgangsmåde for at godkende en kreditor for et produkt.</span><span class="sxs-lookup"><span data-stu-id="9a947-116">To approve a vendor for a product, follow these steps.</span></span>

1. <span data-ttu-id="9a947-117">Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="9a947-117">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="9a947-118">Åbn den relevante vare.</span><span class="sxs-lookup"><span data-stu-id="9a947-118">Open the relevant item.</span></span>
1. <span data-ttu-id="9a947-119">Vælg **Opsætning** i gruppen **Godkendt kreditor** under fanen **Køb** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9a947-119">On the Action Pane, on the **Purchase** tab, in the **Approved vendor** group, select **Setup**.</span></span>
1. <span data-ttu-id="9a947-120">Føj en række til gitteret på listesiden **Godkendt kreditor**, og angiv følgende værdier for det:</span><span class="sxs-lookup"><span data-stu-id="9a947-120">On the **Approved vendor** list page, add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="9a947-121">**Kreditor** – Vælg den kreditor, du vil godkende for det aktuelle produkt.</span><span class="sxs-lookup"><span data-stu-id="9a947-121">**Vendor** – Select the vendor to approve for the current product.</span></span>
    - <span data-ttu-id="9a947-122">**Ikrafttrædelsesdato** – Vælg den første dato, som kreditoren er godkendt for.</span><span class="sxs-lookup"><span data-stu-id="9a947-122">**Effective date** – Select the first date that the vendor is approved for.</span></span>
    - <span data-ttu-id="9a947-123">**Udløbsdato** – Vælg den sidste dato, som kreditoren er godkendt for.</span><span class="sxs-lookup"><span data-stu-id="9a947-123">**Expiration date** – Select the last date that the vendor is approved for.</span></span>

<span data-ttu-id="9a947-124">Du kan finde flere oplysninger i [Godkende kreditorer til specifikke produkter](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span><span class="sxs-lookup"><span data-stu-id="9a947-124">For more information, see [Approve vendors for specific products](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span></span>
