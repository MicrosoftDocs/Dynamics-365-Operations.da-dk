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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4b18ebe1388998b45e5ef38318b0ade9153f7c8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "342609"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="4faf7-103">Oprette fremdaterede checks</span><span class="sxs-lookup"><span data-stu-id="4faf7-103">Set up postdated checks</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4faf7-104">I dette emne beskrives, hvordan du angiver, om du vil bogføre journalposter for fremdaterede checks, og hvilke bogføringsjournaler, der skal bruges til at fjerne poster og kreditorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="4faf7-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="4faf7-105">Du kan også angive clearingkonti for udstedte kontrol, modtagne checks og A-skat.</span><span class="sxs-lookup"><span data-stu-id="4faf7-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="4faf7-106">Fremdaterede checks, der udstedes med det formål at foretage og modtage betalinger på en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="4faf7-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="4faf7-107">Du kan angive, om checken skal afspejles i regnskaberne før dens forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="4faf7-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="4faf7-108">Rollen for denne procedure er Kasserer.</span><span class="sxs-lookup"><span data-stu-id="4faf7-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="4faf7-109">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="4faf7-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="4faf7-110">Oprette fremdaterede checks</span><span class="sxs-lookup"><span data-stu-id="4faf7-110">Set up postdated checks</span></span>
1. <span data-ttu-id="4faf7-111">Gå til Kontant- og bankstyring > Opsætning > Kontant- og bankstyringsparametre</span><span class="sxs-lookup"><span data-stu-id="4faf7-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="4faf7-112">Klik på fanen Fremdaterede checks.</span><span class="sxs-lookup"><span data-stu-id="4faf7-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="4faf7-113">Marker eller fjern markeringen af afkrydsningsfeltet Aktivér fremdaterede checks.</span><span class="sxs-lookup"><span data-stu-id="4faf7-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="4faf7-114">Marker eller fjern markeringen i afkrydsningsfeltet Bogfør kladdeposteringer for fremdaterede checks.</span><span class="sxs-lookup"><span data-stu-id="4faf7-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="4faf7-115">Angiv de ønskede værdier i feltet Clearingkonto til udstedte checks.</span><span class="sxs-lookup"><span data-stu-id="4faf7-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="4faf7-116">Angiv de ønskede værdier i feltet Clearingkonto til modtagne checks.</span><span class="sxs-lookup"><span data-stu-id="4faf7-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="4faf7-117">Skriv en værdi i feltet Finanskladde til clearingposteringer.</span><span class="sxs-lookup"><span data-stu-id="4faf7-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="4faf7-118">Skriv en værdi i feltet Overfør fremdaterede checks til denne kreditorbetalingskladde.</span><span class="sxs-lookup"><span data-stu-id="4faf7-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="4faf7-119">Angiv de ønskede værdier i feltet Clearingkonto til A-skat.</span><span class="sxs-lookup"><span data-stu-id="4faf7-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="4faf7-120">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="4faf7-120">Click Save.</span></span>
11. <span data-ttu-id="4faf7-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4faf7-121">Close the page.</span></span>
12. <span data-ttu-id="4faf7-122">Gå til Kreditor > Opsætning af betaling > Betalingsmåder.</span><span class="sxs-lookup"><span data-stu-id="4faf7-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="4faf7-123">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="4faf7-123">Click New.</span></span>
14. <span data-ttu-id="4faf7-124">Indtast en værdi i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="4faf7-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="4faf7-125">Vælg indstillingen Bogføring af fremdateret checkclearing for at angive, at checkbeløbet bogføres på en clearingkonto.</span><span class="sxs-lookup"><span data-stu-id="4faf7-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="4faf7-126">Vælg "Bank" i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="4faf7-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="4faf7-127">Modkontoen for betalingsmetoden bliver en bank.</span><span class="sxs-lookup"><span data-stu-id="4faf7-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="4faf7-128">I feltet Betalingskonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="4faf7-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="4faf7-129">Vælg den bankkonto, der bruges til at fratrække fakturabeløbet.</span><span class="sxs-lookup"><span data-stu-id="4faf7-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="4faf7-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4faf7-130">Close the page.</span></span>
19. <span data-ttu-id="4faf7-131">Gå til Debitor > Opsætning af betaling > Betalingsmetoder</span><span class="sxs-lookup"><span data-stu-id="4faf7-131">Go to Accounts receivable > Payment setup > Methods of payment</span></span>
20. <span data-ttu-id="4faf7-132">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="4faf7-132">Click New.</span></span>
21. <span data-ttu-id="4faf7-133">Indtast en værdi i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="4faf7-133">In the Method of payment field, type a value.</span></span>
22. <span data-ttu-id="4faf7-134">Vælg indstillingen Bogføring af fremdateret checkclearing for at angive, at checkbeløbet bogføres på en clearingkonto.</span><span class="sxs-lookup"><span data-stu-id="4faf7-134">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
23. <span data-ttu-id="4faf7-135">Vælg "Bank" i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="4faf7-135">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="4faf7-136">Modkontoen for betalingsmetoden bliver en bank.</span><span class="sxs-lookup"><span data-stu-id="4faf7-136">The offset account of the payment method will be a bank.</span></span>  
24. <span data-ttu-id="4faf7-137">I feltet Betalingskonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="4faf7-137">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="4faf7-138">Vælg den bankkonto, der bruges til at fratrække fakturabeløbet.</span><span class="sxs-lookup"><span data-stu-id="4faf7-138">Select the bank account that is used to deduct the invoice amount.</span></span>  
25. <span data-ttu-id="4faf7-139">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4faf7-139">Close the page.</span></span>

