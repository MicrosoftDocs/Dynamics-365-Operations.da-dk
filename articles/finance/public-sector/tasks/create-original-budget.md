---
title: Oprette et oprindeligt budget og derefter tilbageføre foreløbige budgetposter i den offentlige sektor
description: Dette emne indeholder oplysninger om, hvordan du opretter og tilbagefører en oprindelig budgetpost ved hjælp af budgetmodel- og dimensionsværdier med foreløbige budgetbeløb.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 134e2ca851d72965198026107817c66a808ac705
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987948"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a><span data-ttu-id="4933f-103">Oprette et oprindeligt budget og derefter tilbageføre foreløbige budgetposter i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="4933f-103">Create an original budget and then reverse preliminary budget entries in the public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4933f-104">Når du opretter en oprindelig budgetpost og bruger budgetmodellen og dimensionsværdierne, der indeholder foreløbige budgetbeløb, kan de foreløbige budgetbeløb tilbageføres.</span><span class="sxs-lookup"><span data-stu-id="4933f-104">When you create an original budget entry and use the budget model and dimension values that contain preliminary budget amounts, the preliminary budget amounts can be reversed.</span></span> <span data-ttu-id="4933f-105">Denne procedure er oprettet med PSUS-demodatafirmaet i den offentlige sektor partition.</span><span class="sxs-lookup"><span data-stu-id="4933f-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="4933f-106">Gå til Budgettering > Budgetregisterposter.</span><span class="sxs-lookup"><span data-stu-id="4933f-106">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="4933f-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="4933f-107">Click New.</span></span>
3. <span data-ttu-id="4933f-108">Klik på rullelisten i feltet Budgetmodel for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="4933f-108">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4933f-109">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="4933f-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="4933f-110">Klik på rullelisten i feltet Budgetkode for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="4933f-110">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="4933f-111">På listen skal du klikke på Oprindeligt budget.</span><span class="sxs-lookup"><span data-stu-id="4933f-111">In the list, click Original budget.</span></span>
7. <span data-ttu-id="4933f-112">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="4933f-112">Click Save.</span></span>
8. <span data-ttu-id="4933f-113">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="4933f-113">Click Add line.</span></span>
9. <span data-ttu-id="4933f-114">Valgfrit: Angiv en ny dato, hvis du vil ændre datoen i forhold til den i overskriften.</span><span class="sxs-lookup"><span data-stu-id="4933f-114">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="4933f-115">Datoen bestemmer den regnskabsperiode, som budgettet registreres for.</span><span class="sxs-lookup"><span data-stu-id="4933f-115">This date determines the fiscal period that the budget will be recorded to.</span></span>
10. <span data-ttu-id="4933f-116">Klik på rullelisten i feltet Kontostruktur for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="4933f-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="4933f-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="4933f-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="4933f-118">I feltet Dimensionsværdier skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="4933f-118">In the Dimension values field, specify the desired values.</span></span>
13. <span data-ttu-id="4933f-119">Angiv et tal i feltet Beløb.</span><span class="sxs-lookup"><span data-stu-id="4933f-119">In the Amount field, enter a number.</span></span>
14. <span data-ttu-id="4933f-120">Klik på rullelisten i feltet Valuta for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="4933f-120">In the Currency field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="4933f-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="4933f-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="4933f-122">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="4933f-122">Click Save.</span></span>
17. <span data-ttu-id="4933f-123">Klik på Opdater budgetsaldi.</span><span class="sxs-lookup"><span data-stu-id="4933f-123">Click Update budget balances.</span></span>
    * <span data-ttu-id="4933f-124">Valgfrit: Du kan vælge indstillingen Tilbagefør foreløbigt budget.</span><span class="sxs-lookup"><span data-stu-id="4933f-124">Optional: You can select the Reverse preliminary budget option.</span></span> <span data-ttu-id="4933f-125">Bemærk, at du kan tilbageføre alle foreløbige budgetposter eller kun de foreløbige budgetposter, der har den budgetkode, du angiver.</span><span class="sxs-lookup"><span data-stu-id="4933f-125">Note that you can reverse all preliminary budget entries, or only the preliminary budget entries that have the budget code that you specify.</span></span>  
    * <span data-ttu-id="4933f-126">For at angive valgfrie indstillinger skal du klikke på ikonet til oplåsning øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="4933f-126">To make optional selections, click the Unlock icon at the top of the page.</span></span>  
18. <span data-ttu-id="4933f-127">Klik på Opdater.</span><span class="sxs-lookup"><span data-stu-id="4933f-127">Click Update.</span></span>

