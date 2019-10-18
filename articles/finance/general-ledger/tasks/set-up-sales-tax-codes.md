---
title: Konfigurere momskoder
description: Dette emne beskriver, hvordan du konfigurerer koder for moms i Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45a4a7a20b20961d707e43b35d61c10a08c74943
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185974"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="324c1-103">Konfigurere momskoder</span><span class="sxs-lookup"><span data-stu-id="324c1-103">Set up sales tax codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="324c1-104">Dette emne beskriver, hvordan du konfigurerer momskoder.</span><span class="sxs-lookup"><span data-stu-id="324c1-104">This topic explains how to set up sales tax codes.</span></span> <span data-ttu-id="324c1-105">Momskoder oprettes til enhver indirekte moms eller afgift, som den juridiske enhed er forpligtet til at beregne, opkræve og betale til momsmyndighederne.</span><span class="sxs-lookup"><span data-stu-id="324c1-105">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="324c1-106">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="324c1-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="324c1-107">Gå til **Navigationsrude > Skat > Indirekte skatter > Moms > Momskoder**.</span><span class="sxs-lookup"><span data-stu-id="324c1-107">Go to **Navigation pane > Tax > Indirect taxes > Sales tax > Sales tax codes**.</span></span>
2. <span data-ttu-id="324c1-108">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="324c1-108">Select **New**.</span></span>
3. <span data-ttu-id="324c1-109">Skrive en værdi i feltet **Momskode**.</span><span class="sxs-lookup"><span data-stu-id="324c1-109">In the **Sales tax code** field, type a value.</span></span>
4. <span data-ttu-id="324c1-110">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="324c1-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="324c1-111">Vælg en **Afregningsperiode** ved at åbne rullelisten for at angive, hvilken momsmyndighed og i hvilke intervaller denne moms skal rapporteres og betales.</span><span class="sxs-lookup"><span data-stu-id="324c1-111">Select a **Settlement period** by opening the pull-down list to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="324c1-112">Vælg en **Finanskonteringsgruppe** for at angive de hovedkonti, der skal bogføres moms til finans på.</span><span class="sxs-lookup"><span data-stu-id="324c1-112">Select a **Ledger posting group** to specify the main accounts to post sales tax to the general ledger.</span></span>
7. <span data-ttu-id="324c1-113">Udvid oversigtspanelet **Beregning**.</span><span class="sxs-lookup"><span data-stu-id="324c1-113">Expand the **Calculation** FastTab.</span></span> <span data-ttu-id="324c1-114">Dette omfatter flere felter, der styrer, hvordan momsbeløb beregnes.</span><span class="sxs-lookup"><span data-stu-id="324c1-114">This includes multiple fields that control how sales tax amounts will be calculated.</span></span> <span data-ttu-id="324c1-115">Udfyld disse felter efter behov.</span><span class="sxs-lookup"><span data-stu-id="324c1-115">Fill these fields out as needed.</span></span>  
8. <span data-ttu-id="324c1-116">I **Handlingsruden** øverst på grænsefladen skal du vælge **Momskode**.</span><span class="sxs-lookup"><span data-stu-id="324c1-116">On the **Action Pane** at the top of the interface, select **Sales tax code**.</span></span>
9. <span data-ttu-id="324c1-117">Vælg **Værdier**.</span><span class="sxs-lookup"><span data-stu-id="324c1-117">Select **Values**.</span></span>
10. <span data-ttu-id="324c1-118">Angiv værdien for denne momskode i kolonnen **værdi**.</span><span class="sxs-lookup"><span data-stu-id="324c1-118">Enter the value for this tax code in the **value** column.</span></span>
    - <span data-ttu-id="324c1-119">Hvis beløb pr. enhed er markeret, bliver værdien i oversigtspanelet **Beregning** i feltet Grundlag ganget med antallet på transaktionen, der skal beregnes momsbeløbet.</span><span class="sxs-lookup"><span data-stu-id="324c1-119">On the **Calculation** FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="324c1-120">Hvis momskoden ikke er en enhed baseret skat, er værdien en procentdel, der er anvendt på oprindelsen for denne momskode til beregning af sales tax-beløbet.</span><span class="sxs-lookup"><span data-stu-id="324c1-120">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
11. <span data-ttu-id="324c1-121">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="324c1-121">Select **Save**.</span></span>
12. <span data-ttu-id="324c1-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="324c1-122">Close the page.</span></span>
13. <span data-ttu-id="324c1-123">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="324c1-123">Select **Save**.</span></span>

