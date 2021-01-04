---
title: Oprette posteringsprofiler for bankfaciliteter til garanti
description: Denne opgave opretter en bankfacilitet og bogføringsprofil, der er nødvendig til at behandle en garanti.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff5402b11cd2ccdfde2881268d9cd936947cd77e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441626"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="918f3-103">Oprette posteringsprofiler for bankfaciliteter til garanti</span><span class="sxs-lookup"><span data-stu-id="918f3-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="918f3-104">Denne opgave opretter en bankfacilitet og bogføringsprofil, der er nødvendig til at behandle en garanti.</span><span class="sxs-lookup"><span data-stu-id="918f3-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="918f3-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="918f3-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="918f3-106">Finansparameter</span><span class="sxs-lookup"><span data-stu-id="918f3-106">General ledger parameter</span></span>
1. <span data-ttu-id="918f3-107">Gå til Kontant- og bankstyring > Opsætning > Kontant- og bankstyringsparametre</span><span class="sxs-lookup"><span data-stu-id="918f3-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="918f3-108">Udvid sektionen Bankdokument.</span><span class="sxs-lookup"><span data-stu-id="918f3-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="918f3-109">Vælg garantiindstillingen Aktivér.</span><span class="sxs-lookup"><span data-stu-id="918f3-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="918f3-110">Klik på rullelisten i feltet Posteringsjournal for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="918f3-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="918f3-111">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="918f3-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="918f3-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="918f3-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="918f3-113">Klik på fanen Nummerserier.</span><span class="sxs-lookup"><span data-stu-id="918f3-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="918f3-114">Definer nummerseriekode for garantinummer og garantitransaktionsreferencer</span><span class="sxs-lookup"><span data-stu-id="918f3-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="918f3-115">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="918f3-115">Click Save.</span></span>
9. <span data-ttu-id="918f3-116">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="918f3-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="918f3-117">Oprette bankfacilitet</span><span class="sxs-lookup"><span data-stu-id="918f3-117">Create Bank facility</span></span>
1. <span data-ttu-id="918f3-118">Gå til Kontant- og bankstyring > Opsætning > Bankfaciliteter</span><span class="sxs-lookup"><span data-stu-id="918f3-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="918f3-119">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="918f3-119">Click New.</span></span>
3. <span data-ttu-id="918f3-120">Angiv navnet på bankfacilitetsgruppen for garantiposteringen i feltet Facilitetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="918f3-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="918f3-121">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="918f3-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="918f3-122">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="918f3-122">Click Save.</span></span>
6. <span data-ttu-id="918f3-123">Klik på fanen Facilitetstyper.</span><span class="sxs-lookup"><span data-stu-id="918f3-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="918f3-124">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="918f3-124">Click New.</span></span>
8. <span data-ttu-id="918f3-125">Angiv navnet på den bankfacilitetstype, der er relateret til bankfacilitetsaftalen, i feltet Facilitetstype.</span><span class="sxs-lookup"><span data-stu-id="918f3-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="918f3-126">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="918f3-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="918f3-127">Klik på rullelisten i feltet Facilitetsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="918f3-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="918f3-128">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="918f3-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="918f3-129">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="918f3-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="918f3-130">Vælg en indstilling i feltet Facilitetsart.</span><span class="sxs-lookup"><span data-stu-id="918f3-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="918f3-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="918f3-131">Click Save.</span></span>
15. <span data-ttu-id="918f3-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="918f3-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="918f3-133">Bankbogføringsprofil</span><span class="sxs-lookup"><span data-stu-id="918f3-133">Bank posting profile</span></span>
1. <span data-ttu-id="918f3-134">Gå til Kontant- og bankstyring > Opsætning > Bogføringsprofil for bankdokumenter.</span><span class="sxs-lookup"><span data-stu-id="918f3-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="918f3-135">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="918f3-135">Click New.</span></span>
3. <span data-ttu-id="918f3-136">Klik på rullelisten i feltet Konto/gruppenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="918f3-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="918f3-137">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="918f3-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="918f3-138">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="918f3-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="918f3-139">Vælg hovedkontoen til udligning i feltet Afregn konto.</span><span class="sxs-lookup"><span data-stu-id="918f3-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="918f3-140">Vælg kontoen til udgiftsposteringer i feltet Gebyrkonto.</span><span class="sxs-lookup"><span data-stu-id="918f3-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="918f3-141">Vælg kontoen til avanceposteringen feltet Margenkonto.</span><span class="sxs-lookup"><span data-stu-id="918f3-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="918f3-142">I feltet Afviklingskonto skal du vælge afviklingskontoen til garantitransaktionen.</span><span class="sxs-lookup"><span data-stu-id="918f3-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="918f3-143">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="918f3-143">Click Save.</span></span>
11. <span data-ttu-id="918f3-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="918f3-144">Close the page.</span></span>

