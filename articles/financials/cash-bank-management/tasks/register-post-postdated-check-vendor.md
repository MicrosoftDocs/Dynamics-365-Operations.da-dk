--- 
title: "Registrere og bogføre en fremdateret check for en kreditor"
description: "Du kan registrere detaljerne omkring en fremdateret check, før du udsteder checken til en leverandør ved brug af kladdebilaget."
author: kweekley
manager: AnnBe
ms.date: 10/31/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: cd00227ed6d288a4b2041630bc7a604ac94d3c70
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="0de0d-103">Registrere og bogføre en fremdateret check for en kreditor</span><span class="sxs-lookup"><span data-stu-id="0de0d-103">Register and post a postdated check for a vendor</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0de0d-104">Du kan registrere detaljerne omkring en fremdateret check, før du udsteder checken til en leverandør ved brug af kladdebilaget.</span><span class="sxs-lookup"><span data-stu-id="0de0d-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="0de0d-105">Du kan også bogføre den fremdaterede check og generere økonomiske bevægelser.</span><span class="sxs-lookup"><span data-stu-id="0de0d-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="0de0d-106">Inden du registrerer og bogfører en fremdateret check fra en kunde, skal du udføre følgende opgave:</span><span class="sxs-lookup"><span data-stu-id="0de0d-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="0de0d-107">Konfigurer fremdaterede checks på siden Kontant- og bankstyring.</span><span class="sxs-lookup"><span data-stu-id="0de0d-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="0de0d-108">Rollen for denne opgaveguide er Kasserer.</span><span class="sxs-lookup"><span data-stu-id="0de0d-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="0de0d-109">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="0de0d-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="0de0d-110">Gå til Kreditor > Betalinger > Betalingskladde</span><span class="sxs-lookup"><span data-stu-id="0de0d-110">Go to Accounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="0de0d-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0de0d-111">Click New.</span></span>
3. <span data-ttu-id="0de0d-112">Skriv VendPay i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0de0d-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="0de0d-113">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="0de0d-113">Click Lines.</span></span>
5. <span data-ttu-id="0de0d-114">I feltet Konto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="0de0d-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="0de0d-115">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0de0d-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="0de0d-116">Angiv et tal i feltet Debet.</span><span class="sxs-lookup"><span data-stu-id="0de0d-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="0de0d-117">Klik på rullelisten i feltet Betalingsmåde for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="0de0d-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0de0d-118">Vælg betalingsmåden for den fremdaterede check</span><span class="sxs-lookup"><span data-stu-id="0de0d-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="0de0d-119">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="0de0d-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="0de0d-120">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0de0d-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="0de0d-121">Klik på fanen Fremdaterede checks.</span><span class="sxs-lookup"><span data-stu-id="0de0d-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="0de0d-122">Skriv en værdi i feltet Checknummer.</span><span class="sxs-lookup"><span data-stu-id="0de0d-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="0de0d-123">Angiv eller ret nummeret på den fremdaterede check.</span><span class="sxs-lookup"><span data-stu-id="0de0d-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="0de0d-124">Skriv en værdi i feltet Navn på udstedende bank.</span><span class="sxs-lookup"><span data-stu-id="0de0d-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="0de0d-125">Angiv bankoplysninger om den udstedende bank.</span><span class="sxs-lookup"><span data-stu-id="0de0d-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="0de0d-126">Klik på fanen Liste.</span><span class="sxs-lookup"><span data-stu-id="0de0d-126">Click the List tab.</span></span>
15. <span data-ttu-id="0de0d-127">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="0de0d-127">Click Post.</span></span>
16. <span data-ttu-id="0de0d-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0de0d-128">Close the page.</span></span>
17. <span data-ttu-id="0de0d-129">Klik på fanen Fremdaterede checks.</span><span class="sxs-lookup"><span data-stu-id="0de0d-129">Click the Postdated checks tab.</span></span>


