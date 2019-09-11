---
title: Konfigurere momsgrupper og varemomsgrupper
description: Denne opgaveregistrering fører dig gennem konfigurationen af moms- og varemomsgrupper.
author: twheeloc
manager: AnnBe
ms.date: 07-01-2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12bbeaa4e0e2f6ee4874cf72863624a871ba87ea
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916039"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="ab750-103">Konfigurere momsgrupper og varemomsgrupper</span><span class="sxs-lookup"><span data-stu-id="ab750-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ab750-104">Denne opgaveregistrering fører dig gennem konfigurationen af moms- og varemomsgrupper.</span><span class="sxs-lookup"><span data-stu-id="ab750-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="ab750-105">Momsgrupper er grupper med momskoder, der er tilknyttet debitorer og kreditorer.</span><span class="sxs-lookup"><span data-stu-id="ab750-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="ab750-106">De er også tilknyttet finanskonti for posteringer, der ikke er bogført for en bestemt kreditor eller debitor.</span><span class="sxs-lookup"><span data-stu-id="ab750-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="ab750-107">Varemomsgrupper er grupper af momskoder, der er knyttet til ressourcer som produkter.</span><span class="sxs-lookup"><span data-stu-id="ab750-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="ab750-108">Den momssats, der gælder for en bestemt postering, fastlægges af momskoden, som findes i momsgruppen og i varemomsgruppen for posteringen.</span><span class="sxs-lookup"><span data-stu-id="ab750-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="ab750-109">Der kan kun beregnes moms, hvis der er valgt en momsgruppe og en varemomsgruppe for hver postering, hvor der skal beregnes eller registreres moms.</span><span class="sxs-lookup"><span data-stu-id="ab750-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="ab750-110">Gå til **Navigationsrude > Moduler > Skat > Indirekte skatter > Moms > Momsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="ab750-110">Go to **Navigation pane > Modules > Tax > Indirect taxes > Sales tax > Sales tax groups**.</span></span>
2. <span data-ttu-id="ab750-111">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ab750-111">Click **New**.</span></span>
3. <span data-ttu-id="ab750-112">Skriv en værdi i feltet **Momsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="ab750-112">In the **Sales tax group** field, type a value.</span></span>
4. <span data-ttu-id="ab750-113">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="ab750-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="ab750-114">Slå udvidelsen af sektionen **Opsætning** til/fra.</span><span class="sxs-lookup"><span data-stu-id="ab750-114">Toggle the expansion of the **Setup** section.</span></span>
6. <span data-ttu-id="ab750-115">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="ab750-115">Click **Add**.</span></span>
7. <span data-ttu-id="ab750-116">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ab750-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="ab750-117">Klik på rullelisten i feltet **Momskode** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ab750-117">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="ab750-118">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ab750-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="ab750-119">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ab750-119">Click **Save**.</span></span>
11. <span data-ttu-id="ab750-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ab750-120">Close the page.</span></span>
12. <span data-ttu-id="ab750-121">Gå til **Moms > Indirekte skatter > Moms > Momsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="ab750-121">Go to **Tax > Indirect taxes > Sales tax > Item sales tax groups**.</span></span>
13. <span data-ttu-id="ab750-122">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ab750-122">Click **New**.</span></span>
14. <span data-ttu-id="ab750-123">Skriv en værdi i feltet **Varemomsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="ab750-123">In the **Item sales tax group** field, type a value.</span></span>
15. <span data-ttu-id="ab750-124">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="ab750-124">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="ab750-125">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="ab750-125">Click **Add**.</span></span>
17. <span data-ttu-id="ab750-126">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ab750-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="ab750-127">Klik på rullelisten i feltet **Momskode** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ab750-127">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="ab750-128">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ab750-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="ab750-129">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ab750-129">Click **Save**.</span></span>

