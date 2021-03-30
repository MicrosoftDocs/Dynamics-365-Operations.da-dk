---
title: Medtag fysisk værdi
description: Du skal bruge afkrydsningsfeltet Medtag fysisk værdi i oversigtspanelet Lagermodel på siden Varemodelgrupper til at angive, om fysisk opdaterede transaktioner medtages, når varens løbende gennemsnitlige kostpris beregnes.
author: AndersGirke
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a769f9cb5b34581b9bd20b19bcd8bcd0b1c7bff8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205422"
---
# <a name="include-physical-value"></a><span data-ttu-id="bf6ab-103">Medtag fysisk værdi</span><span class="sxs-lookup"><span data-stu-id="bf6ab-103">Include physical value</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf6ab-104">Du skal bruge afkrydsningsfeltet Medtag fysisk værdi i oversigtspanelet Lagermodel på siden Varemodelgrupper til at angive, om fysisk opdaterede transaktioner medtages, når varens løbende gennemsnitlige kostpris beregnes.</span><span class="sxs-lookup"><span data-stu-id="bf6ab-104">You use the Include physical value check box on the Inventory model FastTab of the Item model groups page to specify whether physically updated transactions are considered when the running average cost price is calculated for an item.</span></span>

<span data-ttu-id="bf6ab-105">Afkrydsningsfeltet **Medtag fysisk værdi** har følgende værdier.</span><span class="sxs-lookup"><span data-stu-id="bf6ab-105">The **Include physical value** check box has the following values.</span></span>

| <span data-ttu-id="bf6ab-106">Værdi</span><span class="sxs-lookup"><span data-stu-id="bf6ab-106">Value</span></span>    | <span data-ttu-id="bf6ab-107">Resultat</span><span class="sxs-lookup"><span data-stu-id="bf6ab-107">Result</span></span>                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf6ab-108">Markeret</span><span class="sxs-lookup"><span data-stu-id="bf6ab-108">Selected</span></span> | <span data-ttu-id="bf6ab-109">Både de fysisk opdaterede transaktioner og økonomisk opdaterede transaktioner bruges til at beregne den løbende gennemsnitskostpris.</span><span class="sxs-lookup"><span data-stu-id="bf6ab-109">Both physically updated transactions and financially updated transactions are used to calculate the running average cost price.</span></span> |
| <span data-ttu-id="bf6ab-110">Afstemt</span><span class="sxs-lookup"><span data-stu-id="bf6ab-110">Cleared</span></span>  | <span data-ttu-id="bf6ab-111">Kun de økonomisk opdaterede transaktioner bruges til at beregne den løbende gennemsnitskostpris.</span><span class="sxs-lookup"><span data-stu-id="bf6ab-111">Only financially updated transactions are used to calculate the running average cost price.</span></span>                                     |

<span data-ttu-id="bf6ab-112">Afkrydsningsfeltet har lidt forskellige effekter, afhængigt af hvilken lagermodel du bruger.</span><span class="sxs-lookup"><span data-stu-id="bf6ab-112">The check box has slightly different effects, depending on the inventory model that you use.</span></span>

-   <span data-ttu-id="bf6ab-113">Hvis du markerer afkrydsningsfeltet **Medtag fysisk værdi**, når du bruger lagermodellen FIFO (First in, first out), LIFO (Last in, first out) eller LIFO-dato, foretages der også reguleringer af fysisk opdaterede transaktioner ved lukning af lageret.</span><span class="sxs-lookup"><span data-stu-id="bf6ab-113">If you select the **Include physical value** check box when you use the FIFO (First in, first out), LIFO (Last in, first out), or LIFO date inventory model, inventory close also makes adjustments to physically updated transactions.</span></span>
-   <span data-ttu-id="bf6ab-114">Hvis du ikke markerer afkrydsningsfeltet **Medtag fysisk værdi**, når du bruger disse lagermodeller, foretages der kun udligninger af økonomisk opdaterede transaktioner ved lukning af lager.</span><span class="sxs-lookup"><span data-stu-id="bf6ab-114">If you don't select the **Include physical value** check box when you use these inventory models, inventory close makes settlements only to financially updated transactions.</span></span>
-   <span data-ttu-id="bf6ab-115">Når du bruger det vægtede gennemsnit eller lagermodellen for vægtet gennemsnitsdato, udlignes der kun økonomisk opdaterede transaktioner under lukning af lager, uanset om du markerer afkrydsningsfeltet **Medtag fysisk værdi** eller ej.</span><span class="sxs-lookup"><span data-stu-id="bf6ab-115">When you use the weighted average or weighted average date inventory model, inventory close settles only financially updated transactions, regardless of whether you select the **Include physical value** check box.</span></span>

<span data-ttu-id="bf6ab-116">**Eksempel 1** Du har markeret afkrydsningsfeltet **Medtag fysisk værdi** og modtager følgende indkøbsordrer:</span><span class="sxs-lookup"><span data-stu-id="bf6ab-116">**Example 1** You've selected the **Include physical value** check box and receive the following purchase orders:</span></span>

-   <span data-ttu-id="bf6ab-117">En indkøbsordre for et antal af 2 og en kostpris på kr. 10,00, der er følgeseddelopdateret.</span><span class="sxs-lookup"><span data-stu-id="bf6ab-117">A purchase order for a quantity of 2 and a cost price of USD 10.00 that has been packing slip–updated.</span></span>
-   <span data-ttu-id="bf6ab-118">En indkøbsordre for et antal af 3 og en kostpris på kr. 12,00, der er fakturaopdateret.</span><span class="sxs-lookup"><span data-stu-id="bf6ab-118">A purchase order for a quantity of 3 and a cost price of USD 12.00 that has been invoice-updated.</span></span>

<span data-ttu-id="bf6ab-119">I dette tilfælde er den løbende gennemsnitlige kostpris kr. 11,20 = (2x10+3x12)/(2+3), da både de fysisk og økonomisk opdaterede transaktioner bruges til at beregne kostprisen.</span><span class="sxs-lookup"><span data-stu-id="bf6ab-119">In this case, the running average cost price will be USD 11.20 = (2x10+3x12)/(2+3), because both physically updated transactions and financially updated transactions are used to calculate the cost price.</span></span> 

<span data-ttu-id="bf6ab-120">**Eksempel 2** Du har ikke markeret afkrydsningsfeltet **Medtag fysisk værdi**, og kostprisen i vareopsætningen er kr. 10,00.</span><span class="sxs-lookup"><span data-stu-id="bf6ab-120">**Example 2** You haven't selected the **Include physical value** check box, and the cost price on the item setup is USD 10.00.</span></span> 

-   <span data-ttu-id="bf6ab-121">Du modtager en indkøbsordre på et antal på 20 og en kostpris på kr. 12,00, der er følgeseddelopdateret.</span><span class="sxs-lookup"><span data-stu-id="bf6ab-121">You receive a purchase order for a quantity of 20 and a cost price of USD 12.00 that has been packing slip–updated.</span></span>

<span data-ttu-id="bf6ab-122">Når en salgsordre bogføres, bogføres kostbeløbet på kr. 10,00, da den løbende gennemsnitlige kostpris ikke inkluderer fysisk bogførte transaktioner.</span><span class="sxs-lookup"><span data-stu-id="bf6ab-122">When a sales order is posted, the posted cost amount is USD 10.00, because the running average cost price won't include physically posted transactions.</span></span> 

> [!NOTE]
> <span data-ttu-id="bf6ab-123">Til sammenligning: Hvis du markerer afkrydsningsfeltet **Medtag fysisk værdi** for denne vare, når en salgsordre bogføres, er det bogførte kostbeløb kr. 12,00.</span><span class="sxs-lookup"><span data-stu-id="bf6ab-123">For comparison, if you select the **Include physical value** check box for this item, when a sales order is posted, the posted cost amount will be USD 12.00.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]