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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f696f5aa809692a0cc2c4ff559945a301480d7e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "321656"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="90e8e-103">Oprette posteringsprofiler for bankfaciliteter til garanti</span><span class="sxs-lookup"><span data-stu-id="90e8e-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="90e8e-104">Denne opgave opretter en bankfacilitet og bogføringsprofil, der er nødvendig til at behandle en garanti.</span><span class="sxs-lookup"><span data-stu-id="90e8e-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="90e8e-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="90e8e-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="90e8e-106">Finansparameter</span><span class="sxs-lookup"><span data-stu-id="90e8e-106">General ledger parameter</span></span>
1. <span data-ttu-id="90e8e-107">Gå til Kontant- og bankstyring > Opsætning > Kontant- og bankstyringsparametre</span><span class="sxs-lookup"><span data-stu-id="90e8e-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="90e8e-108">Udvid sektionen Bankdokument.</span><span class="sxs-lookup"><span data-stu-id="90e8e-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="90e8e-109">Vælg garantiindstillingen Aktivér.</span><span class="sxs-lookup"><span data-stu-id="90e8e-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="90e8e-110">Klik på rullelisten i feltet Posteringsjournal for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="90e8e-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="90e8e-111">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="90e8e-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="90e8e-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="90e8e-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="90e8e-113">Klik på fanen Nummerserier.</span><span class="sxs-lookup"><span data-stu-id="90e8e-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="90e8e-114">Definer nummerseriekode for garantinummer og garantitransaktionsreferencer</span><span class="sxs-lookup"><span data-stu-id="90e8e-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="90e8e-115">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="90e8e-115">Click Save.</span></span>
9. <span data-ttu-id="90e8e-116">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="90e8e-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="90e8e-117">Oprette bankfacilitet</span><span class="sxs-lookup"><span data-stu-id="90e8e-117">Create Bank facility</span></span>
1. <span data-ttu-id="90e8e-118">Gå til Kontant- og bankstyring > Opsætning > Bankfaciliteter</span><span class="sxs-lookup"><span data-stu-id="90e8e-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="90e8e-119">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="90e8e-119">Click New.</span></span>
3. <span data-ttu-id="90e8e-120">Angiv navnet på bankfacilitetsgruppen for garantiposteringen i feltet Facilitetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="90e8e-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="90e8e-121">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="90e8e-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="90e8e-122">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="90e8e-122">Click Save.</span></span>
6. <span data-ttu-id="90e8e-123">Klik på fanen Facilitetstyper.</span><span class="sxs-lookup"><span data-stu-id="90e8e-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="90e8e-124">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="90e8e-124">Click New.</span></span>
8. <span data-ttu-id="90e8e-125">Angiv navnet på den bankfacilitetstype, der er relateret til bankfacilitetsaftalen, i feltet Facilitetstype.</span><span class="sxs-lookup"><span data-stu-id="90e8e-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="90e8e-126">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="90e8e-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="90e8e-127">Klik på rullelisten i feltet Facilitetsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="90e8e-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="90e8e-128">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="90e8e-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="90e8e-129">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="90e8e-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="90e8e-130">Vælg en indstilling i feltet Facilitetsart.</span><span class="sxs-lookup"><span data-stu-id="90e8e-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="90e8e-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="90e8e-131">Click Save.</span></span>
15. <span data-ttu-id="90e8e-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="90e8e-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="90e8e-133">Bankbogføringsprofil</span><span class="sxs-lookup"><span data-stu-id="90e8e-133">Bank posting profile</span></span>
1. <span data-ttu-id="90e8e-134">Gå til Kontant- og bankstyring > Opsætning > Bogføringsprofil for bankdokumenter.</span><span class="sxs-lookup"><span data-stu-id="90e8e-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="90e8e-135">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="90e8e-135">Click New.</span></span>
3. <span data-ttu-id="90e8e-136">Klik på rullelisten i feltet Konto/gruppenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="90e8e-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="90e8e-137">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="90e8e-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="90e8e-138">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="90e8e-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="90e8e-139">Vælg hovedkontoen til udligning i feltet Afregn konto.</span><span class="sxs-lookup"><span data-stu-id="90e8e-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="90e8e-140">Vælg kontoen til udgiftsposteringer i feltet Gebyrkonto.</span><span class="sxs-lookup"><span data-stu-id="90e8e-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="90e8e-141">Vælg kontoen til avanceposteringen feltet Margenkonto.</span><span class="sxs-lookup"><span data-stu-id="90e8e-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="90e8e-142">I feltet Afviklingskonto skal du vælge afviklingskontoen til garantitransaktionen.</span><span class="sxs-lookup"><span data-stu-id="90e8e-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="90e8e-143">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="90e8e-143">Click Save.</span></span>
11. <span data-ttu-id="90e8e-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="90e8e-144">Close the page.</span></span>

