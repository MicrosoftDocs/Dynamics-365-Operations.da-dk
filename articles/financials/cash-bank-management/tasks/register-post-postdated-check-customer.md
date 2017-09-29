--- 
title: "Registrere og bogføre en fremdateret check for en debitor"
description: Du kan registrere oplysninger om en fremdateret check, du har modtaget fra en kunde.
author: kweekley
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
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1610036815349f625a67d5dd67260114d42fff97
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="79e4f-103">Registrere og bogføre en fremdateret check for en debitor</span><span class="sxs-lookup"><span data-stu-id="79e4f-103">Register and post a postdated check for a customer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="79e4f-104">Du kan registrere oplysninger om en fremdateret check, du har modtaget fra en kunde.</span><span class="sxs-lookup"><span data-stu-id="79e4f-104">You can register details of a postdated cheque received from a customer.</span></span> <span data-ttu-id="79e4f-105">Du kan også bogføre den fremdaterede check og generere økonomiske bevægelser.</span><span class="sxs-lookup"><span data-stu-id="79e4f-105">You can also post the postdated cheque and generate financial transactions.</span></span>   <span data-ttu-id="79e4f-106">Fuldfør følgende opgaver, inden du registrerer og bogfører en fremdateret check, du har modtaget fra en kunde: • Opret fremdaterede checks på siden Kontant- og bankstyring • Opret en betalingsmåde for fremdaterede checks Rollen for denne procedure er Kasserer.</span><span class="sxs-lookup"><span data-stu-id="79e4f-106">Complete the following tasks before you register and post a postdated cheque received from a customer:   • Set up postdated Cheques in the Cash and bank management page • Set up a method of payment for postdated Cheques   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="79e4f-107">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="79e4f-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="79e4f-108">Gå til Kreditor > Betalinger > Betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="79e4f-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="79e4f-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="79e4f-109">Click New.</span></span>
3. <span data-ttu-id="79e4f-110">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="79e4f-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="79e4f-111">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="79e4f-111">Click Lines.</span></span>
5. <span data-ttu-id="79e4f-112">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="79e4f-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="79e4f-113">I feltet Konto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="79e4f-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="79e4f-114">Angiv et tal i feltet Kredit.</span><span class="sxs-lookup"><span data-stu-id="79e4f-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="79e4f-115">Indtast det beløb, der er angivet på den fremdaterede check.</span><span class="sxs-lookup"><span data-stu-id="79e4f-115">Enter the amount specified in the postdated cheque.</span></span>  
8. <span data-ttu-id="79e4f-116">Klik på fanen Betaling.</span><span class="sxs-lookup"><span data-stu-id="79e4f-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="79e4f-117">Indtast en værdi i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="79e4f-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="79e4f-118">Vælg betalingsmåden for den fremdaterede check</span><span class="sxs-lookup"><span data-stu-id="79e4f-118">Select the method of payment for the postdated cheque</span></span>  
10. <span data-ttu-id="79e4f-119">Klik på fanen Fremdaterede checks.</span><span class="sxs-lookup"><span data-stu-id="79e4f-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="79e4f-120">Angiv en dato i feltet Forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="79e4f-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="79e4f-121">Angiv den dato, hvor den fremdaterede check skal indløses.</span><span class="sxs-lookup"><span data-stu-id="79e4f-121">Enter the date when the postdated cheque is due for payment.</span></span>  
12. <span data-ttu-id="79e4f-122">Skriv en værdi i feltet Udstedende bankfilial.</span><span class="sxs-lookup"><span data-stu-id="79e4f-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="79e4f-123">Angiv bankoplysningerne på den fremdaterede check.</span><span class="sxs-lookup"><span data-stu-id="79e4f-123">Enter the bank details of the postdated cheque.</span></span>  
13. <span data-ttu-id="79e4f-124">Skriv en værdi i feltet Checknummer.</span><span class="sxs-lookup"><span data-stu-id="79e4f-124">In the cheque number field, type a value.</span></span>
14. <span data-ttu-id="79e4f-125">Skriv en værdi i feltet Navn på udstedende bank.</span><span class="sxs-lookup"><span data-stu-id="79e4f-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="79e4f-126">Angiv bankoplysningerne på den fremdaterede check.</span><span class="sxs-lookup"><span data-stu-id="79e4f-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="79e4f-127">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="79e4f-127">Click Post.</span></span>
16. <span data-ttu-id="79e4f-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="79e4f-128">Close the page.</span></span>


