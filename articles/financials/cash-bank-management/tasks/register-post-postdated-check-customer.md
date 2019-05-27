---
title: Registrere og bogføre en fremdateret check for en debitor
description: Du kan registrere oplysninger om en fremdateret check, du har modtaget fra en kunde.
author: kweekley
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 131e4f364c62d03b95fb4b77f472828b9483d5e1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566081"
---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="3f650-103">Registrere og bogføre en fremdateret check for en debitor</span><span class="sxs-lookup"><span data-stu-id="3f650-103">Register and post a postdated check for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3f650-104">Du kan registrere oplysninger om en fremdateret check, du har modtaget fra en kunde.</span><span class="sxs-lookup"><span data-stu-id="3f650-104">You can register details of a postdated check received from a customer.</span></span> <span data-ttu-id="3f650-105">Du kan også bogføre den fremdaterede check og generere økonomiske bevægelser.</span><span class="sxs-lookup"><span data-stu-id="3f650-105">You can also post the postdated check and generate financial transactions.</span></span>   <span data-ttu-id="3f650-106">Fuldfør følgende opgaver, inden du registrerer og bogfører en fremdateret check, du har modtaget fra en kunde: • Opret fremdaterede checks på siden Kontant- og bankstyring • Opret en betalingsmåde for fremdaterede checks Rollen for denne procedure er Kasserer.</span><span class="sxs-lookup"><span data-stu-id="3f650-106">Complete the following tasks before you register and post a postdated check received from a customer:   • Set up postdated check in the Cash and bank management page • Set up a method of payment for postdated checks   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="3f650-107">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="3f650-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="3f650-108">Gå til Kreditor > Betalinger > Betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="3f650-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="3f650-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3f650-109">Click New.</span></span>
3. <span data-ttu-id="3f650-110">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3f650-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="3f650-111">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="3f650-111">Click Lines.</span></span>
5. <span data-ttu-id="3f650-112">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3f650-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="3f650-113">I feltet Konto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="3f650-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="3f650-114">Angiv et tal i feltet Kredit.</span><span class="sxs-lookup"><span data-stu-id="3f650-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="3f650-115">Indtast det beløb, der er angivet på den fremdaterede check.</span><span class="sxs-lookup"><span data-stu-id="3f650-115">Enter the amount specified in the postdated check.</span></span>  
8. <span data-ttu-id="3f650-116">Klik på fanen Betaling.</span><span class="sxs-lookup"><span data-stu-id="3f650-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="3f650-117">Indtast en værdi i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="3f650-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="3f650-118">Vælg betalingsmåden for den fremdaterede check.</span><span class="sxs-lookup"><span data-stu-id="3f650-118">Select the method of payment for the postdated check.</span></span>  
10. <span data-ttu-id="3f650-119">Klik på fanen Fremdaterede checks.</span><span class="sxs-lookup"><span data-stu-id="3f650-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="3f650-120">Angiv en dato i feltet Forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="3f650-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="3f650-121">Angiv den dato, hvor den fremdaterede check skal indløses.</span><span class="sxs-lookup"><span data-stu-id="3f650-121">Enter the date when the postdated check is due for payment.</span></span>  
12. <span data-ttu-id="3f650-122">Skriv en værdi i feltet Udstedende bankfilial.</span><span class="sxs-lookup"><span data-stu-id="3f650-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="3f650-123">Angiv bankoplysningerne på den fremdaterede check.</span><span class="sxs-lookup"><span data-stu-id="3f650-123">Enter the bank details of the postdated check.</span></span>  
13. <span data-ttu-id="3f650-124">Skriv en værdi i feltet Checknummer.</span><span class="sxs-lookup"><span data-stu-id="3f650-124">In the check number field, type a value.</span></span>
14. <span data-ttu-id="3f650-125">Skriv en værdi i feltet Navn på udstedende bank.</span><span class="sxs-lookup"><span data-stu-id="3f650-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="3f650-126">Angiv bankoplysningerne på den fremdaterede check.</span><span class="sxs-lookup"><span data-stu-id="3f650-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="3f650-127">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="3f650-127">Click Post.</span></span>
16. <span data-ttu-id="3f650-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3f650-128">Close the page.</span></span>

