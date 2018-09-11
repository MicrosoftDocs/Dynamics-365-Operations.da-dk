--- 
title: Konfigurer momskoder
description: "Momskoder oprettes til enhver indirekte moms eller afgift, som den juridiske enhed er forpligtet til at beregne, opkræve og betale til momsmyndighederne."
author: twheeloc
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: f0e078b9c700570b775f91b34a55f2ef490f329a
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="f2551-103">Konfigurer momskoder</span><span class="sxs-lookup"><span data-stu-id="f2551-103">Set up sales tax codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2551-104">Momskoder oprettes til enhver indirekte moms eller afgift, som den juridiske enhed er forpligtet til at beregne, opkræve og betale til momsmyndighederne.</span><span class="sxs-lookup"><span data-stu-id="f2551-104">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="f2551-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="f2551-105">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="f2551-106">Gå til Moms > Indirekte skatter > Moms > Momskoder.</span><span class="sxs-lookup"><span data-stu-id="f2551-106">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="f2551-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f2551-107">Click New.</span></span>
3. <span data-ttu-id="f2551-108">Skrive en værdi i feltet Momskode.</span><span class="sxs-lookup"><span data-stu-id="f2551-108">In the Sales tax code field, type a value.</span></span>
4. <span data-ttu-id="f2551-109">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="f2551-109">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f2551-110">Vælg en afregningsperiode for at angive, hvilken momsmyndighed og i hvilke intervaller denne moms skal rapporteres og betales.</span><span class="sxs-lookup"><span data-stu-id="f2551-110">Select a Settlement period to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="f2551-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f2551-111">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f2551-112">Vælg en finanskonteringsgruppe for at angive de hovedkonti, der skal bogføres moms til Finans på.</span><span class="sxs-lookup"><span data-stu-id="f2551-112">Select a Ledger posting group to specify the main accounts to post sales tax to the general ledger.</span></span>
8. <span data-ttu-id="f2551-113">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f2551-113">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="f2551-114">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f2551-114">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="f2551-115">Udvid oversigtspanelet Beregning.</span><span class="sxs-lookup"><span data-stu-id="f2551-115">Expand the Calculation FastTab.</span></span>
    * <span data-ttu-id="f2551-116">Oversigtspanelet Beregning har flere felter, der styrer, hvordan momsbeløb beregnes.</span><span class="sxs-lookup"><span data-stu-id="f2551-116">The Calculation FastTab has multiple fields that control how sales tax amounts will be calculated.</span></span>  
11. <span data-ttu-id="f2551-117">Klik på Momskode i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f2551-117">On the Action Pane, click Sales tax code.</span></span>
12. <span data-ttu-id="f2551-118">Klik på Værdier.</span><span class="sxs-lookup"><span data-stu-id="f2551-118">Click Values.</span></span>
13. <span data-ttu-id="f2551-119">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f2551-119">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="f2551-120">Angiv værdien for denne momskode.</span><span class="sxs-lookup"><span data-stu-id="f2551-120">Enter the value for this tax code.</span></span>
    * <span data-ttu-id="f2551-121">I oversigtspanelet beregning i feltet grundlag, hvis beløb pr. enhed er markeret, skal værdien ganges med antallet på transaktionen, der skal beregnes sales tax-beløbet.</span><span class="sxs-lookup"><span data-stu-id="f2551-121">On the Calculation FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="f2551-122">Hvis momskoden ikke er en enhed baseret skat, er værdien en procentdel, der er anvendt på oprindelsen for denne momskode til beregning af sales tax-beløbet.</span><span class="sxs-lookup"><span data-stu-id="f2551-122">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
15. <span data-ttu-id="f2551-123">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="f2551-123">Click Save.</span></span>
16. <span data-ttu-id="f2551-124">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f2551-124">Close the page.</span></span>
17. <span data-ttu-id="f2551-125">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="f2551-125">Click Save.</span></span>


