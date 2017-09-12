--- 
title: "Opsætte momsmyndigheder"
description: "Momsmyndighederne er enheder, som opkrævet moms skal være indrapporteret og betalt til."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f75ee28343161026a73dd889b345d65ecc345884
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-sales-tax-authorities"></a><span data-ttu-id="da3b9-103">Opsætte momsmyndigheder</span><span class="sxs-lookup"><span data-stu-id="da3b9-103">Set up sales tax authorities</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da3b9-104">Momsmyndighederne er enheder, som opkrævet moms skal være indrapporteret og betalt til.</span><span class="sxs-lookup"><span data-stu-id="da3b9-104">Sales tax authorities are entities to which collected sales tax needs to be reported and paid.</span></span> <span data-ttu-id="da3b9-105">Du kan betale moms til myndigheden direkte eller via en kreditorkonto, som du opretter til momsmyndigheden.</span><span class="sxs-lookup"><span data-stu-id="da3b9-105">You can pay sales taxes to the authority directly or through a vendor account that you create for the sales tax authority.</span></span> <span data-ttu-id="da3b9-106">Hvis du gør dette, kan firmaet bruge de almindelige betalingsmetoder, så alle beløb betales til momsmyndigheden til tiden.</span><span class="sxs-lookup"><span data-stu-id="da3b9-106">If you do this, the company can use its usual payment routines to pay the sales tax authority on time.</span></span> <span data-ttu-id="da3b9-107">Hvis du ikke opretter momsmyndigheden som kreditor, skal en eller anden sørge for, at beløbet betales manuelt til momsmyndigheden på forfaldsdatoen.</span><span class="sxs-lookup"><span data-stu-id="da3b9-107">If you do not set up the tax authority as a vendor, someone must prepare a manual payment to the tax authority on the appropriate due date.</span></span> <span data-ttu-id="da3b9-108">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="da3b9-108">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="da3b9-109">Gå til Moms > Indirekte skatter > Moms > Momsmyndigheder.</span><span class="sxs-lookup"><span data-stu-id="da3b9-109">Go to Tax > Indirect taxes > Sales tax > Sales tax authorities.</span></span>
2. <span data-ttu-id="da3b9-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="da3b9-110">Click New.</span></span>
3. <span data-ttu-id="da3b9-111">Skriv en værdi i feltet Momsmyndighed.</span><span class="sxs-lookup"><span data-stu-id="da3b9-111">In the Authority field, type a value.</span></span>
4. <span data-ttu-id="da3b9-112">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="da3b9-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="da3b9-113">Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="da3b9-113">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="da3b9-114">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="da3b9-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="da3b9-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="da3b9-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="da3b9-116">Vælg rapportlayoutet for dit land/område, hvis der er et tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="da3b9-116">Select the report layout for your country/region, if one is available.</span></span> <span data-ttu-id="da3b9-117">Hvis de viste rapportlayout ikke svarer til kravene fra momsmyndigheden, kan du bruge standardlayoutet.</span><span class="sxs-lookup"><span data-stu-id="da3b9-117">If the report layouts do not correspond to the requirements of the sales tax authority, use default layout.</span></span>
9. <span data-ttu-id="da3b9-118">Angiv værdier i formen Afrunding og felterne Afrunding for at angive, hvordan det samlede afgiftsbeløb til betaling skal afrundes.</span><span class="sxs-lookup"><span data-stu-id="da3b9-118">Enter values in the Rounding form and the Round-off fields to specify how the tax total amount to be paid should be rounded.</span></span> <span data-ttu-id="da3b9-119">Enhver afrundingsdifference bogføres til Konti til automatiske posteringer, der er oprettet i Finans.</span><span class="sxs-lookup"><span data-stu-id="da3b9-119">Any rounding differences will be posted to Accounts for automatic transactions set up in General ledger.</span></span>
10. <span data-ttu-id="da3b9-120">Angiv et tal i feltet Afrunding.</span><span class="sxs-lookup"><span data-stu-id="da3b9-120">In the Round-off field, enter a number.</span></span>
11. <span data-ttu-id="da3b9-121">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="da3b9-121">Click Save.</span></span>


