--- 
title: "Oprettelse af udlånsemner"
description: "Udlånsemner er poster, der hjælper dig med at holde styr på fysiske emner, som f.eks. telefoner eller computere, som virksomheden udlåner til arbejdere."
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cef1f9b2e3d202d7eea3a967fa8a6c371c6ac3a5
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-loan-items"></a><span data-ttu-id="fc5ab-103">Oprettelse af udlånsemner</span><span class="sxs-lookup"><span data-stu-id="fc5ab-103">Create loan items</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fc5ab-104">Udlånsemner er poster, der hjælper dig med at holde styr på fysiske emner, som f.eks. telefoner eller computere, som virksomheden udlåner til arbejdere.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="fc5ab-105">Alle fysiske emner skal have et tilknyttet udlånsemne.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="fc5ab-106">Alle udlånsemneposter skal beskrive, hvad der udlånes, hvem der er ansvarlig for udlånet, og det antal dage, emnet kan udlånes.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="fc5ab-107">Du kan oprette flere udlånsemner f.eks. nøgler, adgangskort og uniformer, på samme tid.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="fc5ab-108">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="fc5ab-109">Opret udlånstyper</span><span class="sxs-lookup"><span data-stu-id="fc5ab-109">Create Loan types</span></span>
1. <span data-ttu-id="fc5ab-110">Gå til Personale > Arbejdere > Udlånsemner > Udlånstyper.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="fc5ab-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-111">Click New.</span></span>
3. <span data-ttu-id="fc5ab-112">Indtast en værdi i feltet Udlånstype.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="fc5ab-113">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fc5ab-114">Angiv det antal dage, som emner, der er knyttet til denne udlånstype, kan være overskredet med.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="fc5ab-115">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-115">Click Save.</span></span>
7. <span data-ttu-id="fc5ab-116">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-116">Close the page.</span></span>
8. <span data-ttu-id="fc5ab-117">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="fc5ab-118">Opret Udlånsemner</span><span class="sxs-lookup"><span data-stu-id="fc5ab-118">Create Loan items</span></span>
1. <span data-ttu-id="fc5ab-119">Gå til Personale > Arbejdere > Udlånsemner > Udlånsemner.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="fc5ab-120">Klik på Opret udlånsemner.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-120">Click Create loan items.</span></span>
3. <span data-ttu-id="fc5ab-121">I feltet Antal. skal du angive et tal.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-121">In the Qty. field, enter a number.</span></span>
4. <span data-ttu-id="fc5ab-122">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-122">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fc5ab-123">Klik på rullelisten i feltet Udlånstype for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-123">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="fc5ab-124">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-124">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="fc5ab-125">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="fc5ab-126">Angiv antal dage, emnet kan lånes.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-126">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="fc5ab-127">Standardværdien i feltet Planlagt retur på siden Lånt udstyr beregnes som den aktuelle dato plus dette tal.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-127">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="fc5ab-128">Klik på rullelisten i feltet Ansvarlig for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-128">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="fc5ab-129">Klik på Vælg.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-129">Click Select.</span></span>
11. <span data-ttu-id="fc5ab-130">Indtast et tal i feltet Startværdi, der skal tilføjes.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-130">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="fc5ab-131">Angiv et tal i feltet Interval.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-131">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="fc5ab-132">Skriv en værdi i feltet Format.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-132">In the Format field, type a value.</span></span>
    * <span data-ttu-id="fc5ab-133">Hvis det højeste startnummer for et udlånt emne f.eks. er 10, skal du skrive to talsymboler i feltet Format.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-133">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="fc5ab-134">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-134">Click OK.</span></span>
15. <span data-ttu-id="fc5ab-135">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-135">Refresh the page.</span></span>


