---
title: Begrænse redigeringen af regnskabsfordelinger på fakturaer
description: I dette emne forklares det, hvordan du kan kræve, at de økonomiske dimensioner i en indkøbsordre svarer til dimensionerne på den tilsvarende kreditorfaktura.
author: v-kiarnd
manager: AnnBe
ms.date: 10/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.search.industry: public sector
ms.author: v-kiarnd
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 56ad3ac4a883a6b75183f559c4e1f71a5c6a4e44
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555403"
---
# <a name="restrict-editing-of-accounting-distributions-on-invoices"></a><span data-ttu-id="ca660-103">Begrænse redigeringen af regnskabsfordelinger på fakturaer</span><span class="sxs-lookup"><span data-stu-id="ca660-103">Restrict editing of accounting distributions on invoices</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ca660-104">I dette emne forklares det, hvordan du kan kræve, at de økonomiske dimensioner i en indkøbsordre svarer til dimensionerne på den tilsvarende kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="ca660-104">This topic explains how to require that the financial dimensions on a purchase order (PO) match the dimensions on the corresponding vendor invoice.</span></span> <span data-ttu-id="ca660-105">Du kan konfigurere bestemte økonomiske dimensioner, der skal være ens mellem en indkøbsordre og en faktura, der oprettes ud fra den.</span><span class="sxs-lookup"><span data-stu-id="ca660-105">You can set up specific financial dimensions that must match between a PO and an invoice that is created from it.</span></span> <span data-ttu-id="ca660-106">Du kan f.eks. kræve, at alle økonomiske dimensioner stemmer overens mellem indkøbsordrer og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="ca660-106">For example, you can require that all financial dimensions match between POs and invoices.</span></span> <span data-ttu-id="ca660-107">På fakturaer, der er tilknyttet en indkøbsordre, kan du ikke ændre finanskontiene på fakturaens detaljelinjer, så de afviger fra de konti, der er angivet på indkøbsordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="ca660-107">On invoices that are associated with a PO, you can't change the general ledger accounts on the invoice detail lines so that they differ from the accounts that were entered on the PO lines.</span></span>

## <a name="set-up-locked-financial-dimensions"></a><span data-ttu-id="ca660-108">Konfigurere låste økonomiske dimensioner</span><span class="sxs-lookup"><span data-stu-id="ca660-108">Set up locked financial dimensions</span></span>

<span data-ttu-id="ca660-109">Benyt følgende fremgangsmåde for at definere de økonomiske dimensioner, der skal være ens mellem en indkøbsordre og relaterede fakturaer.</span><span class="sxs-lookup"><span data-stu-id="ca660-109">Follow these steps to define the financial dimensions that must match between a PO and related invoices.</span></span>

1. <span data-ttu-id="ca660-110">Gå til **Kreditor \> Opsætning \> Kreditorparametre**.</span><span class="sxs-lookup"><span data-stu-id="ca660-110">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="ca660-111">På siden **Kreditorparametre** skal du vælge **Validering af indkøbsordre-/fakturasammenholdelse**.</span><span class="sxs-lookup"><span data-stu-id="ca660-111">On the **Accounts payable parameters** page, select **PO/Invoice matching validation**.</span></span>
3. <span data-ttu-id="ca660-112">Markér afkrydsningsfeltet **Påkrævet sammenholdelse** for de dimensioner, der skal være ens.</span><span class="sxs-lookup"><span data-stu-id="ca660-112">Select the **Matching required** check box for the dimensions that must match.</span></span> <span data-ttu-id="ca660-113">Alle de økonomiske dimensioner, der er konfigureret på siden **Økonomiske dimensioner**, kan vælges.</span><span class="sxs-lookup"><span data-stu-id="ca660-113">All the financial dimensions that are set up on the **Financial dimensions** page are available for selection.</span></span>
4. <span data-ttu-id="ca660-114">Vælg **Luk**.</span><span class="sxs-lookup"><span data-stu-id="ca660-114">Select **Close**.</span></span>

## <a name="work-with-locked-financial-dimensions-on-an-invoice"></a><span data-ttu-id="ca660-115">Arbejde med låste økonomiske dimensioner på en faktura</span><span class="sxs-lookup"><span data-stu-id="ca660-115">Work with locked financial dimensions on an invoice</span></span>

<span data-ttu-id="ca660-116">Når du opretter en kreditorfaktura ud fra en indkøbsordre, kan du ikke redigere de låste økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="ca660-116">When you create a vendor invoice from a PO, you can't edit the locked financial dimensions.</span></span> <span data-ttu-id="ca660-117">Hvis du forsøger at redigere en låst økonomisk dimension, modtager du en fejlmeddelelse, og hele den økonomiske dimensionsstreng går tilbage til den oprindelige streng.</span><span class="sxs-lookup"><span data-stu-id="ca660-117">If you try to edit a locked financial dimension, you receive an error message, and the whole financial dimension string reverts to the original string.</span></span>

<span data-ttu-id="ca660-118">Du kan se økonomiske dimensioner for fakturaen.</span><span class="sxs-lookup"><span data-stu-id="ca660-118">You can view financial dimensions for the invoice.</span></span>

1. <span data-ttu-id="ca660-119">Gå til **Kreditor \> Generelt \> Kreditorfakturaer \> Ventende kreditorfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="ca660-119">Go to **Accounts payable \> Common \> Vendor invoices \> Pending vendor invoices**.</span></span>
2. <span data-ttu-id="ca660-120">Åbn fakturaen.</span><span class="sxs-lookup"><span data-stu-id="ca660-120">Open the invoice.</span></span>
3. <span data-ttu-id="ca660-121">På siden **Kreditorfaktura** skal du i oversigtspanelet **Linjer** vælge **Finans \> Fordel beløb**.</span><span class="sxs-lookup"><span data-stu-id="ca660-121">On the **Vendor invoice** page, on the **Lines** FastTab, select **Financials \> Distribute amount**.</span></span>

> [!NOTE]
> <span data-ttu-id="ca660-122">Økonomiske dimensioner er ikke låst på linjer, der manuelt føjes til en faktura og ikke er baseret på indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="ca660-122">Financial dimensions aren't locked on lines that are manually added to an invoice and not based on PO.</span></span> <span data-ttu-id="ca660-123">I dette tilfælde kan du ændre de økonomiske dimensioner på fakturaen efter behov, indtil fakturaen er bogført.</span><span class="sxs-lookup"><span data-stu-id="ca660-123">In this case, you can change the financial dimensions on the invoice as you require, until the invoice is posted.</span></span>
