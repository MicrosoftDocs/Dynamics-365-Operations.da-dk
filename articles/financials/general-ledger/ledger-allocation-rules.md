---
title: Finansfordelingsregler
description: Denne artikel indeholder generelle oplysninger om finansfordelingsregler. Den beskriver de forskellige komponenter i disse fordelingsregler og de fordelingsmetoder, som kan bruges til dem.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 63562cde3f2813fdcfc9df7ccbfc623aa2fbe9b1
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="ledger-allocation-rules"></a><span data-ttu-id="17fd2-104">Finansfordelingsregler</span><span class="sxs-lookup"><span data-stu-id="17fd2-104">Ledger allocation rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="17fd2-105">Denne artikel indeholder generelle oplysninger om finansfordelingsregler.</span><span class="sxs-lookup"><span data-stu-id="17fd2-105">This article provides information about ledger allocation rules.</span></span> <span data-ttu-id="17fd2-106">Den beskriver de forskellige komponenter i disse fordelingsregler og de fordelingsmetoder, som kan bruges til dem.</span><span class="sxs-lookup"><span data-stu-id="17fd2-106">It describes the various components of these allocation rules and the allocation methods that can be used for them.</span></span>

<span data-ttu-id="17fd2-107">Finansfordelingsregler bruges til automatisk at beregne og generere fordelingskladder og kontoposter for fordeling af finanssaldi eller faste beløb.</span><span class="sxs-lookup"><span data-stu-id="17fd2-107">Ledger allocation rules are used to automatically calculate and generate allocation journals and account entries for the allocation of ledger balances or fixed amounts.</span></span> <span data-ttu-id="17fd2-108">Fordelingsmetoderne kan være variable eller faste.</span><span class="sxs-lookup"><span data-stu-id="17fd2-108">Allocation methods can be variable or fixed.</span></span> <span data-ttu-id="17fd2-109">Følgende fordelingsmetoder kan bruges til finansfordelingsregler:</span><span class="sxs-lookup"><span data-stu-id="17fd2-109">The following allocation methods can be used for ledger allocation rules:</span></span>

-   <span data-ttu-id="17fd2-110">**Basis** – Denne variable metode bruges, når fordelingen afhænger af den faktiske finanssaldo baseret på filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="17fd2-110">**Basis** – This variable method is used when the allocation depends on the actual ledger balance, based on filter criteria.</span></span> <span data-ttu-id="17fd2-111">Du kan f.eks. fordele reklameomkostninger baseret på den enkelte afdelings salg i forhold til det samlede afdelingssalg.</span><span class="sxs-lookup"><span data-stu-id="17fd2-111">For example, advertising expenses can be allocated based on each department's sales in proportion to the total departmental sales.</span></span>
-   <span data-ttu-id="17fd2-112">**Fast procentdel** og **Fast vægt** – For disse metoder defineres fordelingsprocenten eller -vægten direkte for reglen.</span><span class="sxs-lookup"><span data-stu-id="17fd2-112">**Fixed percentage** and **Fixed weight** – For these methods, the allocation percentage or weight is defined directly for the rule.</span></span> <span data-ttu-id="17fd2-113">Reklameudgifter kan f.eks. fordeles, så afdeling A modtager 70 procent af reklameomkostninger, og afdeling B modtager 30 procent.</span><span class="sxs-lookup"><span data-stu-id="17fd2-113">For example, advertising expenses can be allocated so that Department A receives 70 percent of the advertising expense and Department B receives 30 percent.</span></span>
-   <span data-ttu-id="17fd2-114">**Ligeligt** – Denne metode fordeler beløbet ligeligt mellem alle de destinationer, der er defineret.</span><span class="sxs-lookup"><span data-stu-id="17fd2-114">**Equally** – This method distributes the amount equally to each defined destination.</span></span> <span data-ttu-id="17fd2-115">Hvis der f.eks. er fastsat bestemmelsessteder for afdeling A og afdeling B, kan reklameudgifter fordeles, så både afdeling A og afdeling B modtager 50 % af reklameudgiften.</span><span class="sxs-lookup"><span data-stu-id="17fd2-115">For example, if destinations are defined for Department A and Department B, advertising expenses can be allocated so that both Department A and Department B receive 50 percent of the advertising expense.</span></span>

<span data-ttu-id="17fd2-116">Hvis Bases bruges som fordelingsmetoden til en fordelingsregel, skal du også definere separate basisregler for finansfordeling.</span><span class="sxs-lookup"><span data-stu-id="17fd2-116">If Basis is used as the allocation method for an allocation rule, you must also define separate ledger allocation basis rules.</span></span> <span data-ttu-id="17fd2-117">I processen "Udfør fordelingsanmodning" kan brugerne behandle finansfordelingsreglen og få vist den resulterende fordelingskladde, før de enten bogfører eller sletter de beregnede fordelinger.</span><span class="sxs-lookup"><span data-stu-id="17fd2-117">The "Process allocation request" process lets users process the ledger allocation rule and preview the resulting allocation journal entries before they either post or delete the calculated allocations.</span></span>

## <a name="components-of-ledger-allocation-rules"></a><span data-ttu-id="17fd2-118">Komponenter i finansfordelingsregler</span><span class="sxs-lookup"><span data-stu-id="17fd2-118">Components of ledger allocation rules</span></span>
<span data-ttu-id="17fd2-119">Hver fordelingsregel består af fire komponenter: generel, kilde, destination og modregning.</span><span class="sxs-lookup"><span data-stu-id="17fd2-119">Each allocation rule has four components: general, source, destination, and offset.</span></span> <span data-ttu-id="17fd2-120">Der kræves en ekstra komponent, finansfordelingsbasisregler, hvis Basis bruges som fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="17fd2-120">An additional component, ledger allocation bases rules, is required if Basis is used as the allocation method.</span></span> <span data-ttu-id="17fd2-121">Hver af disse komponenter udgør en central del af de informationer, der skal bruges for at behandle fordelinger.</span><span class="sxs-lookup"><span data-stu-id="17fd2-121">Each component provides a critical piece of the information that is required in order to process allocations.</span></span>

-   <span data-ttu-id="17fd2-122">**Generelt** – Denne komponent er det sted, hvor brugeren angiver muligheder, f.eks. fordelingsmetode, indstillinger for regler for intern handel, og om reglen er aktiv eller ej.</span><span class="sxs-lookup"><span data-stu-id="17fd2-122">**General** – This component is where the user specifies options such as the allocation method, intercompany rule settings, and whether the rule is active.</span></span>
-   <span data-ttu-id="17fd2-123">**Kilde** – Denne komponent er det sted, hvor brugeren angiver kildedataene til fordelingen.</span><span class="sxs-lookup"><span data-stu-id="17fd2-123">**Source** – This component is where the user specifies the source data for the allocation.</span></span> <span data-ttu-id="17fd2-124">Fordelingen kan baseres på finanssaldi (**Datakilde** = **Finans**) eller faste beløb (**Datakilde** = **Faste værdi**).</span><span class="sxs-lookup"><span data-stu-id="17fd2-124">Allocation can be based on ledger balances (**Data source** = **Ledger**) or fixed amounts (**Data source** = **Fixed value**).</span></span> <span data-ttu-id="17fd2-125">Når **Datakilde** er angivet til **Finans**, skal der være defineret filterkriterier for finansfordelingsregel (f.eks. til reklameudgifter).</span><span class="sxs-lookup"><span data-stu-id="17fd2-125">When **Data source** is set to **Ledger**, source filter criteria must be defined for the ledger allocation rule (for example, for the advertising expenses).</span></span>
-   <span data-ttu-id="17fd2-126">**Destination** – Denne komponent definerer, hvordan resultatet af fordelingsberegningen skal distribueres og gøres rede for.</span><span class="sxs-lookup"><span data-stu-id="17fd2-126">**Destination** – This component defines how the result of the allocation calculation should be distributed and accounted for.</span></span> <span data-ttu-id="17fd2-127">Der kan f.eks. være én destinationslinje for hver afdeling.</span><span class="sxs-lookup"><span data-stu-id="17fd2-127">For example, there can be one destination line for each department.</span></span>
-   <span data-ttu-id="17fd2-128">**Modregn** – Denne komponent definerer, hvordan hovedkonti og dimensioner skal bestemmes for de forskudte poster, som er afstemt på destinationsposterne.</span><span class="sxs-lookup"><span data-stu-id="17fd2-128">**Offset** – This component defines how main accounts and dimensions should be determined for the offset entries that balance the destination entries.</span></span> <span data-ttu-id="17fd2-129">Brugerdefinerede indstillinger anvendes typisk i stedet for de konti og dimensioner, der er baseret på kilden.</span><span class="sxs-lookup"><span data-stu-id="17fd2-129">User-defined options are typically used instead of accounts and dimensions that are based on the source.</span></span> <span data-ttu-id="17fd2-130">Når **Datakilde** er angivet til **Faste værdier**, kan **Kilde** ikke bruges som en indstilling.</span><span class="sxs-lookup"><span data-stu-id="17fd2-130">When **Data source** is set to **Fixed value**, **Source** can't be used as an option.</span></span>
-   <span data-ttu-id="17fd2-131">**Finansfordelingsbasisregler** – Disse regler anvender deres filterkriterier til at bestemme, hvilke finanssaldi der skal bruges til fordeling (f.eks. omsætning pr. afdeling).</span><span class="sxs-lookup"><span data-stu-id="17fd2-131">**Ledger allocation basis rules** – These rules use their own source filter criteria to determine which ledger balances should be used for allocation (for example, the revenue per department).</span></span> <span data-ttu-id="17fd2-132">De enkelte fordelingsbasisregler kan bruges til flere fordelingsregler.</span><span class="sxs-lookup"><span data-stu-id="17fd2-132">Each allocation basis rule can be used with multiple allocation rules.</span></span>





