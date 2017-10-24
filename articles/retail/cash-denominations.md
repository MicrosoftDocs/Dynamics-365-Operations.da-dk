---
title: "Konfigurere kontantbeløbsangivelser for POS"
description: "Kontantbeløbsangivelser for sedler og mønter kan defineres i administrationen til brug for kasserere, salgsassistenter og bestyrere i butikken fra POS."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 45e70765c43b93e9d8abab5fbb9de1d67a739a74
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="configure-cash-denominations-for-pos"></a><span data-ttu-id="ec948-103">Konfigurere kontantbeløbsangivelser for POS</span><span class="sxs-lookup"><span data-stu-id="ec948-103">Configure cash denominations for POS</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="ec948-104">Kontantbeløbsangivelser for sedler og mønter kan defineres i administrationen til brug for kasserere, salgsassistenter og bestyrere i butikken fra POS.</span><span class="sxs-lookup"><span data-stu-id="ec948-104">Cash denominations for notes and coins can be defined in the back office to be used by cashiers, sales associates, and managers at the store from within the POS.</span></span> <span data-ttu-id="ec948-105">Disse værdienheder kan bruges som hjælp til optælling af kontanter for kasseoptællinger eller for hurtigt at gennemføre et salg.</span><span class="sxs-lookup"><span data-stu-id="ec948-105">These denominations can be used to aid in counting cash for end of day tender declarations or for quickly tendering a sale.</span></span>

## <a name="define-denominations"></a><span data-ttu-id="ec948-106">Angive værdienheder</span><span class="sxs-lookup"><span data-stu-id="ec948-106">Define denominations</span></span>
<span data-ttu-id="ec948-107">Værdienhederne angives pr. butik på siden **Konfigurer** > **Indstillingen Kontantopgørelse fra butiksegenskaben**.</span><span class="sxs-lookup"><span data-stu-id="ec948-107">The denominations are set up per store on the **Set up** > **Cash declaration option from the store property** page.</span></span> 

![kontantbeløbsangivelser](./media/image1-denomination.png)

<span data-ttu-id="ec948-109">Sådan defineres en værdienhed:</span><span class="sxs-lookup"><span data-stu-id="ec948-109">To define a denomination:</span></span>
1. <span data-ttu-id="ec948-110">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ec948-110">Click **New**.</span></span>
1. <span data-ttu-id="ec948-111">Angiv typen (mønter eller seddel).</span><span class="sxs-lookup"><span data-stu-id="ec948-111">Specify the type (coin or note).</span></span>
1. <span data-ttu-id="ec948-112">Angiv beløbet (værdi).</span><span class="sxs-lookup"><span data-stu-id="ec948-112">Specify the amount (value).</span></span>

![kontantbeløbsangivelser](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a><span data-ttu-id="ec948-114">Konfigurere funktionalitetsprofilen</span><span class="sxs-lookup"><span data-stu-id="ec948-114">Configure the functionality profile</span></span>
<span data-ttu-id="ec948-115">Ved betaling med kontanter i POS, kan brugeren bruge seddelværdienheder til hurtigt at angive det beløb, der er betalt af kunden.</span><span class="sxs-lookup"><span data-stu-id="ec948-115">When paying by cash in POS, the user can use the note denominations to quickly enter the amount paid by the customer.</span></span> <span data-ttu-id="ec948-116">I funktionalitetsprofilen kan du konfigurere de to indstillinger for visning af værdienheden i POS.</span><span class="sxs-lookup"><span data-stu-id="ec948-116">In the functionality profile, you can configure the two options for showing the denomination in POS.</span></span>

<span data-ttu-id="ec948-117">**Større end eller lig med forfaldent beløb**: Som standard viser POS kun de seddelværdienheder, der er større end det skyldige beløb, hvilket giver mulighed for optælling med et enkelt tryk.</span><span class="sxs-lookup"><span data-stu-id="ec948-117">**Greater or equal to amount due**: By default, POS will only show the note denominations that are greater than the amount due, which allows for one-touch tendering.</span></span> <span data-ttu-id="ec948-118">Hvis det skyldige beløb f.eks. er $7,50, viser POS følgende værdienheder: $10, $20, $50 og $100.</span><span class="sxs-lookup"><span data-stu-id="ec948-118">For example, if the amount due is $7.50, POS would show the following denominations: $10, $20, $50, and $100.</span></span> <span data-ttu-id="ec948-119">Ved tryk på et af disse beløb optælles salget automatisk for det pågældende beløb.</span><span class="sxs-lookup"><span data-stu-id="ec948-119">Touching any of these amounts will automatically tender the sale for that amount.</span></span> <span data-ttu-id="ec948-120">$1 og $5 sedler vises ikke, da disse beløb er mindre end det skyldige beløb.</span><span class="sxs-lookup"><span data-stu-id="ec948-120">The $1 and $5 notes are not shown since these amounts are less than the amount due.</span></span>

<span data-ttu-id="ec948-121">**Alle værdienheder**: Vælg denne indstilling for altid at få vist alle seddelværdienheder i POS, uanset det skyldige beløb.</span><span class="sxs-lookup"><span data-stu-id="ec948-121">**All denominations**: Select this option to always show all note denominations in POS, regardless of the amount due.</span></span> <span data-ttu-id="ec948-122">Det betyder, at brugeren kan anvende en kombination af sedler til at nå det skyldige beløb.</span><span class="sxs-lookup"><span data-stu-id="ec948-122">This means that the user can use a combination of notes to reach the amount due.</span></span> <span data-ttu-id="ec948-123">F.eks. hvis det skyldige beløb er $25,00, kan brugeren vælge $20 og $5 til at afslutte salget.</span><span class="sxs-lookup"><span data-stu-id="ec948-123">For example, if the amount due is $25.00, the user can choose $20 and $5 to complete the sale.</span></span>

