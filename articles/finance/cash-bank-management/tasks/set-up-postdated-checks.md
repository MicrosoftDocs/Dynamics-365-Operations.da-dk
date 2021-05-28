---
title: Oprette fremdaterede checks
description: I dette emne beskrives, hvordan du angiver, om du vil bogføre journalposter for fremdaterede checks, og hvilke bogføringsjournaler, der skal bruges til at fjerne poster og kreditorbetalinger.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0d4afd74f9a0f9018629fa92ab6595bfa94f973
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026199"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="18adb-103">Oprette fremdaterede checks</span><span class="sxs-lookup"><span data-stu-id="18adb-103">Set up postdated checks</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="18adb-104">I dette emne beskrives, hvordan du angiver, om du vil bogføre journalposter for fremdaterede checks, og hvilke bogføringsjournaler, der skal bruges til at fjerne poster og kreditorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="18adb-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="18adb-105">Du kan også angive clearingkonti for udstedte kontrol, modtagne checks og A-skat.</span><span class="sxs-lookup"><span data-stu-id="18adb-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="18adb-106">Fremdaterede checks, der udstedes med det formål at foretage og modtage betalinger på en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="18adb-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="18adb-107">Du kan angive, om checken skal afspejles i regnskaberne før dens forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="18adb-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="18adb-108">Rollen for denne procedure er Kasserer.</span><span class="sxs-lookup"><span data-stu-id="18adb-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="18adb-109">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="18adb-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="18adb-110">Oprette fremdaterede checks</span><span class="sxs-lookup"><span data-stu-id="18adb-110">Set up postdated checks</span></span>
1. <span data-ttu-id="18adb-111">Gå til Kontant- og bankstyring > Opsætning > Kontant- og bankstyringsparametre</span><span class="sxs-lookup"><span data-stu-id="18adb-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="18adb-112">Klik på fanen Fremdaterede checks.</span><span class="sxs-lookup"><span data-stu-id="18adb-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="18adb-113">Marker eller fjern markeringen af afkrydsningsfeltet Aktivér fremdaterede checks.</span><span class="sxs-lookup"><span data-stu-id="18adb-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="18adb-114">Marker eller fjern markeringen i afkrydsningsfeltet Bogfør kladdeposteringer for fremdaterede checks.</span><span class="sxs-lookup"><span data-stu-id="18adb-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="18adb-115">Angiv de ønskede værdier i feltet Clearingkonto til udstedte checks.</span><span class="sxs-lookup"><span data-stu-id="18adb-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="18adb-116">Angiv de ønskede værdier i feltet Clearingkonto til modtagne checks.</span><span class="sxs-lookup"><span data-stu-id="18adb-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="18adb-117">Skriv en værdi i feltet Finanskladde til clearingposteringer.</span><span class="sxs-lookup"><span data-stu-id="18adb-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="18adb-118">Skriv en værdi i feltet Overfør fremdaterede checks til denne kreditorbetalingskladde.</span><span class="sxs-lookup"><span data-stu-id="18adb-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="18adb-119">Angiv de ønskede værdier i feltet Clearingkonto til A-skat.</span><span class="sxs-lookup"><span data-stu-id="18adb-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="18adb-120">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="18adb-120">Click Save.</span></span>
11. <span data-ttu-id="18adb-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="18adb-121">Close the page.</span></span>
12. <span data-ttu-id="18adb-122">Gå til Kreditor > Opsætning af betaling > Betalingsmåder.</span><span class="sxs-lookup"><span data-stu-id="18adb-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="18adb-123">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="18adb-123">Click New.</span></span>
14. <span data-ttu-id="18adb-124">Indtast en værdi i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="18adb-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="18adb-125">Vælg indstillingen Bogføring af fremdateret checkclearing for at angive, at checkbeløbet bogføres på en clearingkonto.</span><span class="sxs-lookup"><span data-stu-id="18adb-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="18adb-126">Vælg "Bank" i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="18adb-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="18adb-127">Modkontoen for betalingsmetoden bliver en bank.</span><span class="sxs-lookup"><span data-stu-id="18adb-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="18adb-128">I feltet Betalingskonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="18adb-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="18adb-129">Vælg den bankkonto, der bruges til at fratrække fakturabeløbet.</span><span class="sxs-lookup"><span data-stu-id="18adb-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="18adb-130">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="18adb-130">Click Save.</span></span>
19. <span data-ttu-id="18adb-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="18adb-131">Close the page.</span></span>
> [!NOTE]
> <span data-ttu-id="18adb-132">Hvis du vil kunne bogføre en fremdateret check på en bankkonto, når sessionsdatoen er større end eller lig med forfaldsdatoen, skal du aktivere funktionen **Forfaldsdatovalidering af bogføring af betalingskladde med fremdaterede checks på bankkontoen**.</span><span class="sxs-lookup"><span data-stu-id="18adb-132">To be able to post a postdated check to a bank account when the session date is greater than or equal to the maturity date, you must enable the feature **Maturity date validation of posting payment journal with postdated checks to bank account**.</span></span> <span data-ttu-id="18adb-133">Denne funktion giver dig mulighed for at bogføre betalingskladder for kreditorer eller debitorer med fremdaterede checks, når sessionsdatoen er større end eller lig med forfaldsdatoen.</span><span class="sxs-lookup"><span data-stu-id="18adb-133">This feature allows you to post payment journals for vendors or customers with postdated checks, when the session date is greater than or equal to the maturity date.</span></span>
> 
> <span data-ttu-id="18adb-134">Når du angiver **Betalingsmåde** (**Kreditor > Opsætning af betaling > Betalingsmåder**), skal du ikke udfylde **Mellemkonto**.</span><span class="sxs-lookup"><span data-stu-id="18adb-134">When setting the **Method of payment** (**Accounts payable > Payment setup > Methods of payment**), do not fill in **Bridging account**.</span></span> <span data-ttu-id="18adb-135">I dette tilfælde udfyldes modkontoen med den bankkonto, der er angivet i **Betalingsmåde**.</span><span class="sxs-lookup"><span data-stu-id="18adb-135">In this case, the offset account is filled in with the bank account, which is set up in the **Method of payment**.</span></span>
>  
> <span data-ttu-id="18adb-136">Når funktionen er aktiveret, og sessionsdatoen er mindre end forfaldsdatoen, vises følgende fejlmeddelelse, når du bogfører en betalingskladde "Forfaldsdato skal være mindre eller lig med sessionsdatoen, hvis modkontotypen er Bank".</span><span class="sxs-lookup"><span data-stu-id="18adb-136">When the feature is enabled and the session date is less than the maturity date, the following error message is displayed when posting a payment journal, "Maturity date must be less or equal to the session date if offset account type is Bank".</span></span> <span data-ttu-id="18adb-137">Hvis funktionen ikke er aktiveret, kan du bogføre en betalingskladde med en fremdateret check, når sessionsdatoen er mindre end forfaldsdatoen.</span><span class="sxs-lookup"><span data-stu-id="18adb-137">If the feature is not enabled, you can post a payment journal with a postdated check when the session date is less than the maturity date.</span></span>    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
