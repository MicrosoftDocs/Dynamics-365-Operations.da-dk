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
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d14b0622f4fbad87ddf019307910d4d4e316888a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995284"
---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="0ef95-103">Registrere og bogføre en fremdateret check for en debitor</span><span class="sxs-lookup"><span data-stu-id="0ef95-103">Register and post a postdated check for a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0ef95-104">Du kan registrere oplysninger om en fremdateret check, du har modtaget fra en kunde.</span><span class="sxs-lookup"><span data-stu-id="0ef95-104">You can register details of a postdated check received from a customer.</span></span> <span data-ttu-id="0ef95-105">Du kan også bogføre den fremdaterede check og generere økonomiske bevægelser.</span><span class="sxs-lookup"><span data-stu-id="0ef95-105">You can also post the postdated check and generate financial transactions.</span></span>   <span data-ttu-id="0ef95-106">Fuldfør følgende opgaver, inden du registrerer og bogfører en fremdateret check, du har modtaget fra en kunde: *Opret fremdaterede checks på siden Kontant- og bankstyring* Opret en betalingsmåde for fremdaterede checks Rollen for denne procedure er Kasserer.</span><span class="sxs-lookup"><span data-stu-id="0ef95-106">Complete the following tasks before you register and post a postdated check received from a customer:   \* Set up postdated check in the Cash and bank management page \* Set up a method of payment for postdated checks   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="0ef95-107">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="0ef95-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="0ef95-108">Gå til Kreditor > Betalinger > Betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="0ef95-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="0ef95-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0ef95-109">Click New.</span></span>
3. <span data-ttu-id="0ef95-110">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0ef95-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0ef95-111">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="0ef95-111">Click Lines.</span></span>
5. <span data-ttu-id="0ef95-112">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0ef95-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="0ef95-113">I feltet Konto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="0ef95-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="0ef95-114">Angiv et tal i feltet Kredit.</span><span class="sxs-lookup"><span data-stu-id="0ef95-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="0ef95-115">Indtast det beløb, der er angivet på den fremdaterede check.</span><span class="sxs-lookup"><span data-stu-id="0ef95-115">Enter the amount specified in the postdated check.</span></span>  
8. <span data-ttu-id="0ef95-116">Klik på fanen Betaling.</span><span class="sxs-lookup"><span data-stu-id="0ef95-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="0ef95-117">Indtast en værdi i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="0ef95-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="0ef95-118">Vælg betalingsmåden for den fremdaterede check.</span><span class="sxs-lookup"><span data-stu-id="0ef95-118">Select the method of payment for the postdated check.</span></span>  
10. <span data-ttu-id="0ef95-119">Klik på fanen Fremdaterede checks.</span><span class="sxs-lookup"><span data-stu-id="0ef95-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="0ef95-120">Angiv en dato i feltet Forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="0ef95-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="0ef95-121">Angiv den dato, hvor den fremdaterede check skal indløses.</span><span class="sxs-lookup"><span data-stu-id="0ef95-121">Enter the date when the postdated check is due for payment.</span></span>  
12. <span data-ttu-id="0ef95-122">Skriv en værdi i feltet Udstedende bankfilial.</span><span class="sxs-lookup"><span data-stu-id="0ef95-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="0ef95-123">Angiv bankoplysningerne på den fremdaterede check.</span><span class="sxs-lookup"><span data-stu-id="0ef95-123">Enter the bank details of the postdated check.</span></span>  
13. <span data-ttu-id="0ef95-124">Skriv en værdi i feltet Checknummer.</span><span class="sxs-lookup"><span data-stu-id="0ef95-124">In the check number field, type a value.</span></span>
14. <span data-ttu-id="0ef95-125">Skriv en værdi i feltet Navn på udstedende bank.</span><span class="sxs-lookup"><span data-stu-id="0ef95-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="0ef95-126">Angiv bankoplysningerne på den fremdaterede check.</span><span class="sxs-lookup"><span data-stu-id="0ef95-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="0ef95-127">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="0ef95-127">Click Post.</span></span>
16. <span data-ttu-id="0ef95-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0ef95-128">Close the page.</span></span>

