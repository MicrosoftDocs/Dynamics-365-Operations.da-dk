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
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b72a412aaaf1c70b4414d00e99b923380f7dd86
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225291"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="3f346-103">Oprette posteringsprofiler for bankfaciliteter til garanti</span><span class="sxs-lookup"><span data-stu-id="3f346-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3f346-104">Denne opgave opretter en bankfacilitet og bogføringsprofil, der er nødvendig til at behandle en garanti.</span><span class="sxs-lookup"><span data-stu-id="3f346-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="3f346-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="3f346-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="3f346-106">Finansparameter</span><span class="sxs-lookup"><span data-stu-id="3f346-106">General ledger parameter</span></span>
1. <span data-ttu-id="3f346-107">Gå til Kontant- og bankstyring > Opsætning > Kontant- og bankstyringsparametre</span><span class="sxs-lookup"><span data-stu-id="3f346-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="3f346-108">Udvid sektionen Bankdokument.</span><span class="sxs-lookup"><span data-stu-id="3f346-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="3f346-109">Vælg garantiindstillingen Aktivér.</span><span class="sxs-lookup"><span data-stu-id="3f346-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="3f346-110">Klik på rullelisten i feltet Posteringsjournal for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="3f346-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="3f346-111">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="3f346-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="3f346-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3f346-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="3f346-113">Klik på fanen Nummerserier.</span><span class="sxs-lookup"><span data-stu-id="3f346-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="3f346-114">Definer nummerseriekode for garantinummer og garantitransaktionsreferencer</span><span class="sxs-lookup"><span data-stu-id="3f346-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="3f346-115">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3f346-115">Click Save.</span></span>
9. <span data-ttu-id="3f346-116">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3f346-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="3f346-117">Oprette bankfacilitet</span><span class="sxs-lookup"><span data-stu-id="3f346-117">Create Bank facility</span></span>
1. <span data-ttu-id="3f346-118">Gå til Kontant- og bankstyring > Opsætning > Bankfaciliteter</span><span class="sxs-lookup"><span data-stu-id="3f346-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="3f346-119">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3f346-119">Click New.</span></span>
3. <span data-ttu-id="3f346-120">Angiv navnet på bankfacilitetsgruppen for garantiposteringen i feltet Facilitetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3f346-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="3f346-121">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3f346-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3f346-122">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3f346-122">Click Save.</span></span>
6. <span data-ttu-id="3f346-123">Klik på fanen Facilitetstyper.</span><span class="sxs-lookup"><span data-stu-id="3f346-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="3f346-124">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3f346-124">Click New.</span></span>
8. <span data-ttu-id="3f346-125">Angiv navnet på den bankfacilitetstype, der er relateret til bankfacilitetsaftalen, i feltet Facilitetstype.</span><span class="sxs-lookup"><span data-stu-id="3f346-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="3f346-126">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3f346-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="3f346-127">Klik på rullelisten i feltet Facilitetsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="3f346-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="3f346-128">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="3f346-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="3f346-129">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3f346-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="3f346-130">Vælg en indstilling i feltet Facilitetsart.</span><span class="sxs-lookup"><span data-stu-id="3f346-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="3f346-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3f346-131">Click Save.</span></span>
15. <span data-ttu-id="3f346-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3f346-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="3f346-133">Bankbogføringsprofil</span><span class="sxs-lookup"><span data-stu-id="3f346-133">Bank posting profile</span></span>
1. <span data-ttu-id="3f346-134">Gå til Kontant- og bankstyring > Opsætning > Bogføringsprofil for bankdokumenter.</span><span class="sxs-lookup"><span data-stu-id="3f346-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="3f346-135">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3f346-135">Click New.</span></span>
3. <span data-ttu-id="3f346-136">Klik på rullelisten i feltet Konto/gruppenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="3f346-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="3f346-137">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="3f346-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="3f346-138">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3f346-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="3f346-139">Vælg hovedkontoen til udligning i feltet Afregn konto.</span><span class="sxs-lookup"><span data-stu-id="3f346-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="3f346-140">Vælg kontoen til udgiftsposteringer i feltet Gebyrkonto.</span><span class="sxs-lookup"><span data-stu-id="3f346-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="3f346-141">Vælg kontoen til avanceposteringen feltet Margenkonto.</span><span class="sxs-lookup"><span data-stu-id="3f346-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="3f346-142">I feltet Afviklingskonto skal du vælge afviklingskontoen til garantitransaktionen.</span><span class="sxs-lookup"><span data-stu-id="3f346-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="3f346-143">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3f346-143">Click Save.</span></span>
11. <span data-ttu-id="3f346-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3f346-144">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]