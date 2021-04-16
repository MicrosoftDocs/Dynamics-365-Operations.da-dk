---
title: Oprette posteringsprofiler for bankfaciliteter til garanti
description: Denne opgave opretter en bankfacilitet og bogføringsprofil, der er nødvendig til at behandle en garanti.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1147650944ba40d1c8054444c09db9c5ee97bde3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834614"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="8a0c2-103">Oprette posteringsprofiler for bankfaciliteter til garanti</span><span class="sxs-lookup"><span data-stu-id="8a0c2-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8a0c2-104">Denne opgave opretter en bankfacilitet og bogføringsprofil, der er nødvendig til at behandle en garanti.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="8a0c2-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="8a0c2-106">Finansparameter</span><span class="sxs-lookup"><span data-stu-id="8a0c2-106">General ledger parameter</span></span>
1. <span data-ttu-id="8a0c2-107">Gå til Kontant- og bankstyring > Opsætning > Kontant- og bankstyringsparametre</span><span class="sxs-lookup"><span data-stu-id="8a0c2-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="8a0c2-108">Udvid sektionen Bankdokument.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="8a0c2-109">Vælg garantiindstillingen Aktivér.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="8a0c2-110">Klik på rullelisten i feltet Posteringsjournal for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="8a0c2-111">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="8a0c2-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="8a0c2-113">Klik på fanen Nummerserier.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="8a0c2-114">Definer nummerseriekode for garantinummer og garantitransaktionsreferencer</span><span class="sxs-lookup"><span data-stu-id="8a0c2-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="8a0c2-115">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-115">Click Save.</span></span>
9. <span data-ttu-id="8a0c2-116">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="8a0c2-117">Oprette bankfacilitet</span><span class="sxs-lookup"><span data-stu-id="8a0c2-117">Create Bank facility</span></span>
1. <span data-ttu-id="8a0c2-118">Gå til Kontant- og bankstyring > Opsætning > Bankfaciliteter</span><span class="sxs-lookup"><span data-stu-id="8a0c2-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="8a0c2-119">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-119">Click New.</span></span>
3. <span data-ttu-id="8a0c2-120">Angiv navnet på bankfacilitetsgruppen for garantiposteringen i feltet Facilitetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="8a0c2-121">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8a0c2-122">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-122">Click Save.</span></span>
6. <span data-ttu-id="8a0c2-123">Klik på fanen Facilitetstyper.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="8a0c2-124">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-124">Click New.</span></span>
8. <span data-ttu-id="8a0c2-125">Angiv navnet på den bankfacilitetstype, der er relateret til bankfacilitetsaftalen, i feltet Facilitetstype.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="8a0c2-126">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="8a0c2-127">Klik på rullelisten i feltet Facilitetsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="8a0c2-128">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="8a0c2-129">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="8a0c2-130">Vælg en indstilling i feltet Facilitetsart.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="8a0c2-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-131">Click Save.</span></span>
15. <span data-ttu-id="8a0c2-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="8a0c2-133">Bankbogføringsprofil</span><span class="sxs-lookup"><span data-stu-id="8a0c2-133">Bank posting profile</span></span>
1. <span data-ttu-id="8a0c2-134">Gå til Kontant- og bankstyring > Opsætning > Bogføringsprofil for bankdokumenter.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="8a0c2-135">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-135">Click New.</span></span>
3. <span data-ttu-id="8a0c2-136">Klik på rullelisten i feltet Konto/gruppenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8a0c2-137">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="8a0c2-138">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8a0c2-139">Vælg hovedkontoen til udligning i feltet Afregn konto.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="8a0c2-140">Vælg kontoen til udgiftsposteringer i feltet Gebyrkonto.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="8a0c2-141">Vælg kontoen til avanceposteringen feltet Margenkonto.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="8a0c2-142">I feltet Afviklingskonto skal du vælge afviklingskontoen til garantitransaktionen.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="8a0c2-143">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-143">Click Save.</span></span>
11. <span data-ttu-id="8a0c2-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-144">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]