---
title: Garantier
description: Denne artikel indeholder oplysninger om garantier. I en garanti accepterer en bank at betale et bestemt pengebeløb til en person, hvis en af bankens kunder misligholder en betaling eller en forpligtelse til den pågældende person.
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankLGGuarantee
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 18291
ms.assetid: 5c0b5e37-d51d-4a01-bb37-1882173abb9f
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3dbf08679c165258a4a4027bf1cf73484d9efd3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441607"
---
# <a name="letters-of-guarantee"></a><span data-ttu-id="4022c-104">Garantier</span><span class="sxs-lookup"><span data-stu-id="4022c-104">Letters of guarantee</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4022c-105">Denne artikel indeholder oplysninger om garantier.</span><span class="sxs-lookup"><span data-stu-id="4022c-105">This article provides information about letters of guarantee.</span></span> <span data-ttu-id="4022c-106">I en garanti accepterer en bank at betale et bestemt pengebeløb til en person, hvis en af bankens kunder misligholder en betaling eller en forpligtelse til den pågældende person.</span><span class="sxs-lookup"><span data-stu-id="4022c-106">In a letter of guarantee, a bank agrees to pay a specific amount of money to a person if one of the bank's customers defaults on a payment or obligation to that person.</span></span> 

<span data-ttu-id="4022c-107">En garanti er en aftale med en bank (kautionisten) om at betale et angivet beløb til en anden person (beneficianten), hvis en banks kunde (hovedparten) misligholder en betaling eller en forpligtelse over for beneficianten.</span><span class="sxs-lookup"><span data-stu-id="4022c-107">A letter of guarantee is an agreement by a bank (the guarantor) to pay a set amount of money to some person (the beneficiary) if a bank customer (the principal) defaults on a payment or an obligation to the beneficiary.</span></span> <span data-ttu-id="4022c-108">Garantier kan ikke overdrages.</span><span class="sxs-lookup"><span data-stu-id="4022c-108">Letters of guarantee aren't transferable.</span></span> <span data-ttu-id="4022c-109">De gælder kun for den beneficiant, der er nævnt i aftalen.</span><span class="sxs-lookup"><span data-stu-id="4022c-109">They apply only to the beneficiary who is named in the agreement.</span></span> <span data-ttu-id="4022c-110">Hovedparten kan anmode om en forøgelse eller reducering af værdien af en garanti med forbehold for betingelserne i aftalen.</span><span class="sxs-lookup"><span data-stu-id="4022c-110">The principal can request an increase or decrease in the value of a letter of guarantee, subject to the terms of the agreement.</span></span> 

<span data-ttu-id="4022c-111">Hvis du vil afvikle en garanti, skal beneficianten indsende den originale garanti og informere banken før udløbsdatoen.</span><span class="sxs-lookup"><span data-stu-id="4022c-111">To liquidate a letter of guarantee, the beneficiary must submit the original letter of guarantee and inform the bank of the principal’s default before the expiration date.</span></span> <span data-ttu-id="4022c-112">Derefter betaler banken det forfaldne beløb til beneficiantens konto i overensstemmelse med betingelserne i garantien.</span><span class="sxs-lookup"><span data-stu-id="4022c-112">The bank then pays the amount that is due to the beneficiary's account, according to the terms in the letter of guarantee.</span></span> <span data-ttu-id="4022c-113">Banken hensætter en procentdel af betalingen som avance.</span><span class="sxs-lookup"><span data-stu-id="4022c-113">The bank reserves a percentage of the payment as a margin.</span></span> <span data-ttu-id="4022c-114">Procentdelen aftales og angives i aftalens betingelser.</span><span class="sxs-lookup"><span data-stu-id="4022c-114">The percentage is agreed upon and specified in the terms of the agreement.</span></span> 

<span data-ttu-id="4022c-115">Du kan oprette en kode, der sporer formålet med garantien.</span><span class="sxs-lookup"><span data-stu-id="4022c-115">You can create a code to track the purpose of a letter of guarantee.</span></span> <span data-ttu-id="4022c-116">Du kan også angive de grunde, der kan være knyttet til garantien, når brevet er annulleret.</span><span class="sxs-lookup"><span data-stu-id="4022c-116">You can also specify the reasons that can be associated with a letter of guarantee when the letter is canceled.</span></span> <span data-ttu-id="4022c-117">Du kan se formålskoder og bankårsager på siderne **Betalingsformålskoder** og **Bankårsager**.</span><span class="sxs-lookup"><span data-stu-id="4022c-117">You can view the purpose codes and bank reasons on the **Payment purpose codes** and **Bank reasons** pages.</span></span> 

<span data-ttu-id="4022c-118">Du kan bruge siden **Garanti** til at udføre disse opgaver:</span><span class="sxs-lookup"><span data-stu-id="4022c-118">You can use the **Letter of guarantee** page to complete these tasks:</span></span>

-   <span data-ttu-id="4022c-119">Opret korrekte finansposter, og fjern manuelle indtastninger.</span><span class="sxs-lookup"><span data-stu-id="4022c-119">Create correct ledger entries, and eliminate manual entry.</span></span>
-   <span data-ttu-id="4022c-120">Registrer alle monetære og ikke-monetære transaktioner, og spor saldi i garantier.</span><span class="sxs-lookup"><span data-stu-id="4022c-120">Record all monetary and nonmonetary transactions, and track balances of letters of guarantee.</span></span>
-   <span data-ttu-id="4022c-121">Registrer og spor status og udløb for garantier.</span><span class="sxs-lookup"><span data-stu-id="4022c-121">Record and track the status and expiration of letters of guarantee.</span></span>
-   <span data-ttu-id="4022c-122">Opret en rapport, der viser de banker, som ligger inde med garantier.</span><span class="sxs-lookup"><span data-stu-id="4022c-122">Generate a report that lists the banks that are holding letters of guarantee.</span></span>

<span data-ttu-id="4022c-123">Nedenstående tabel indeholder beskrivelser af de handlinger, du kan for en garanti.</span><span class="sxs-lookup"><span data-stu-id="4022c-123">The following table describes the actions that you can perform on a letter of guarantee.</span></span>

| <span data-ttu-id="4022c-124">Handling</span><span class="sxs-lookup"><span data-stu-id="4022c-124">Action</span></span>              | <span data-ttu-id="4022c-125">Formål</span><span class="sxs-lookup"><span data-stu-id="4022c-125">Purpose</span></span>                                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4022c-126">Send til bank</span><span class="sxs-lookup"><span data-stu-id="4022c-126">Submit to bank</span></span>      | <span data-ttu-id="4022c-127">Send garantianmodningen til banken.</span><span class="sxs-lookup"><span data-stu-id="4022c-127">Submit the letter of guarantee request to the bank.</span></span>                                                                       |
| <span data-ttu-id="4022c-128">Modtag fra bank</span><span class="sxs-lookup"><span data-stu-id="4022c-128">Receive from bank</span></span>   | <span data-ttu-id="4022c-129">Når banken accepterer den sendte anmodning, skal du have garantien udleveret fra banken.</span><span class="sxs-lookup"><span data-stu-id="4022c-129">After the bank agrees to the submitted request, collect the letter of guarantee from the bank.</span></span>                            |
| <span data-ttu-id="4022c-130">Giv til beneficianten</span><span class="sxs-lookup"><span data-stu-id="4022c-130">Give to beneficiary</span></span> | <span data-ttu-id="4022c-131">Når du modtager anmodningen fra banken, skal du levere garantien til beneficianten.</span><span class="sxs-lookup"><span data-stu-id="4022c-131">After you receive the letter of guarantee from the bank, provide the letter of guarantee to the beneficiary.</span></span>              |
| <span data-ttu-id="4022c-132">øg værdien</span><span class="sxs-lookup"><span data-stu-id="4022c-132">Increase value</span></span>      | <span data-ttu-id="4022c-133">Hvis beneficianten og hovedparten er enige om det, kan den pengemæssige værdi øges.</span><span class="sxs-lookup"><span data-stu-id="4022c-133">If the beneficiary and the principal agree, increase the monetary value.</span></span>                                                  |
| <span data-ttu-id="4022c-134">Reducer værdien</span><span class="sxs-lookup"><span data-stu-id="4022c-134">Decrease value</span></span>      | <span data-ttu-id="4022c-135">Hvis beneficianten og hovedparten er enige om det, kan den pengemæssige værdi reduceres.</span><span class="sxs-lookup"><span data-stu-id="4022c-135">If the beneficiary and the principal agree, decrease the monetary value.</span></span>                                                  |
| <span data-ttu-id="4022c-136">Forlæng</span><span class="sxs-lookup"><span data-stu-id="4022c-136">Extend</span></span>              | <span data-ttu-id="4022c-137">Når du leverer garantien til beneficianten, kan du forlænge gyldighedsperioden, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="4022c-137">After you provide the letter of guarantee to the beneficiary, extend the period of validity, if an extension is required.</span></span> |
| <span data-ttu-id="4022c-138">Annullér</span><span class="sxs-lookup"><span data-stu-id="4022c-138">Cancel</span></span>              | <span data-ttu-id="4022c-139">Når det formål, der var grundlag for anmodningen om garantien, ikke længere gælder, annulleres aftalen.</span><span class="sxs-lookup"><span data-stu-id="4022c-139">When the purpose that the letter of guarantee was requested for no longer applies, cancel the agreement.</span></span>                  |
| <span data-ttu-id="4022c-140">Udfør afvikling</span><span class="sxs-lookup"><span data-stu-id="4022c-140">Liquidate</span></span>           | <span data-ttu-id="4022c-141">Når beneficianten overdrager garantien til banken, udbetales garantien.</span><span class="sxs-lookup"><span data-stu-id="4022c-141">When the beneficiary presents the letter of guarantee to the bank, cash out the letter of guarantee.</span></span>                      |


<span data-ttu-id="4022c-142">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="4022c-142">For more information, see the following topics:</span></span>

[<span data-ttu-id="4022c-143">Garantipostering</span><span class="sxs-lookup"><span data-stu-id="4022c-143">Letter of guarantee transaction</span></span>](tasks/letter-guarantee-transaction.md)

[<span data-ttu-id="4022c-144">Oprette posteringsprofiler for bankfaciliteter til garanti</span><span class="sxs-lookup"><span data-stu-id="4022c-144">Set up bank facilities and posting profiles for letters of guarantee</span></span>](tasks/set-up-bank-facilities-posting-profiles.md)


