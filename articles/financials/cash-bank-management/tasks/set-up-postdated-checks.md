---
title: Oprette fremdaterede checks
description: I dette emne beskrives, hvordan du angiver, om du vil bogføre journalposter for fremdaterede checks, og hvilke bogføringsjournaler, der skal bruges til at fjerne poster og kreditorbetalinger.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8696aeccee651368a036ab8d90980e9ed9cea6b3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841867"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="33c7b-103">Oprette fremdaterede checks</span><span class="sxs-lookup"><span data-stu-id="33c7b-103">Set up postdated checks</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="33c7b-104">I dette emne beskrives, hvordan du angiver, om du vil bogføre journalposter for fremdaterede checks, og hvilke bogføringsjournaler, der skal bruges til at fjerne poster og kreditorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="33c7b-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="33c7b-105">Du kan også angive clearingkonti for udstedte kontrol, modtagne checks og A-skat.</span><span class="sxs-lookup"><span data-stu-id="33c7b-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="33c7b-106">Fremdaterede checks, der udstedes med det formål at foretage og modtage betalinger på en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="33c7b-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="33c7b-107">Du kan angive, om checken skal afspejles i regnskaberne før dens forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="33c7b-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="33c7b-108">Rollen for denne procedure er Kasserer.</span><span class="sxs-lookup"><span data-stu-id="33c7b-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="33c7b-109">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="33c7b-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="33c7b-110">Oprette fremdaterede checks</span><span class="sxs-lookup"><span data-stu-id="33c7b-110">Set up postdated checks</span></span>
1. <span data-ttu-id="33c7b-111">Gå til Kontant- og bankstyring > Opsætning > Kontant- og bankstyringsparametre</span><span class="sxs-lookup"><span data-stu-id="33c7b-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="33c7b-112">Klik på fanen Fremdaterede checks.</span><span class="sxs-lookup"><span data-stu-id="33c7b-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="33c7b-113">Marker eller fjern markeringen af afkrydsningsfeltet Aktivér fremdaterede checks.</span><span class="sxs-lookup"><span data-stu-id="33c7b-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="33c7b-114">Marker eller fjern markeringen i afkrydsningsfeltet Bogfør kladdeposteringer for fremdaterede checks.</span><span class="sxs-lookup"><span data-stu-id="33c7b-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="33c7b-115">Angiv de ønskede værdier i feltet Clearingkonto til udstedte checks.</span><span class="sxs-lookup"><span data-stu-id="33c7b-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="33c7b-116">Angiv de ønskede værdier i feltet Clearingkonto til modtagne checks.</span><span class="sxs-lookup"><span data-stu-id="33c7b-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="33c7b-117">Skriv en værdi i feltet Finanskladde til clearingposteringer.</span><span class="sxs-lookup"><span data-stu-id="33c7b-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="33c7b-118">Skriv en værdi i feltet Overfør fremdaterede checks til denne kreditorbetalingskladde.</span><span class="sxs-lookup"><span data-stu-id="33c7b-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="33c7b-119">Angiv de ønskede værdier i feltet Clearingkonto til A-skat.</span><span class="sxs-lookup"><span data-stu-id="33c7b-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="33c7b-120">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="33c7b-120">Click Save.</span></span>
11. <span data-ttu-id="33c7b-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="33c7b-121">Close the page.</span></span>
12. <span data-ttu-id="33c7b-122">Gå til Kreditor > Opsætning af betaling > Betalingsmåder.</span><span class="sxs-lookup"><span data-stu-id="33c7b-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="33c7b-123">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="33c7b-123">Click New.</span></span>
14. <span data-ttu-id="33c7b-124">Indtast en værdi i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="33c7b-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="33c7b-125">Vælg indstillingen Bogføring af fremdateret checkclearing for at angive, at checkbeløbet bogføres på en clearingkonto.</span><span class="sxs-lookup"><span data-stu-id="33c7b-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="33c7b-126">Vælg "Bank" i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="33c7b-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="33c7b-127">Modkontoen for betalingsmetoden bliver en bank.</span><span class="sxs-lookup"><span data-stu-id="33c7b-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="33c7b-128">I feltet Betalingskonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="33c7b-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="33c7b-129">Vælg den bankkonto, der bruges til at fratrække fakturabeløbet.</span><span class="sxs-lookup"><span data-stu-id="33c7b-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="33c7b-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="33c7b-130">Close the page.</span></span>
19. <span data-ttu-id="33c7b-131">Gå til Debitor > Opsætning af betaling > Betalingsmetoder</span><span class="sxs-lookup"><span data-stu-id="33c7b-131">Go to Accounts receivable > Payment setup > Methods of payment</span></span>
20. <span data-ttu-id="33c7b-132">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="33c7b-132">Click New.</span></span>
21. <span data-ttu-id="33c7b-133">Indtast en værdi i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="33c7b-133">In the Method of payment field, type a value.</span></span>
22. <span data-ttu-id="33c7b-134">Vælg indstillingen Bogføring af fremdateret checkclearing for at angive, at checkbeløbet bogføres på en clearingkonto.</span><span class="sxs-lookup"><span data-stu-id="33c7b-134">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
23. <span data-ttu-id="33c7b-135">Vælg "Bank" i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="33c7b-135">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="33c7b-136">Modkontoen for betalingsmetoden bliver en bank.</span><span class="sxs-lookup"><span data-stu-id="33c7b-136">The offset account of the payment method will be a bank.</span></span>  
24. <span data-ttu-id="33c7b-137">I feltet Betalingskonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="33c7b-137">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="33c7b-138">Vælg den bankkonto, der bruges til at fratrække fakturabeløbet.</span><span class="sxs-lookup"><span data-stu-id="33c7b-138">Select the bank account that is used to deduct the invoice amount.</span></span>  
25. <span data-ttu-id="33c7b-139">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="33c7b-139">Close the page.</span></span>

