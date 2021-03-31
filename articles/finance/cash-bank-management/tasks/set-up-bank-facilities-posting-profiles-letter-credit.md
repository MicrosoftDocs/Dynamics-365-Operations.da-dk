---
title: Oprette posteringsprofiler for bankfaciliteter til remburs
description: Denne procedure gennemgår oprettelsen af en bankfacilitet og posteringsprofil, der bruges til at behandle remburser.
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
ms.openlocfilehash: bc94100461bc82e9e7cd243f198711ab61a79b0c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225267"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a><span data-ttu-id="b7438-103">Oprette posteringsprofiler for bankfaciliteter til remburs</span><span class="sxs-lookup"><span data-stu-id="b7438-103">Set up bank facilities and posting profiles for letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b7438-104">Denne procedure gennemgår oprettelsen af en bankfacilitet og posteringsprofil, der bruges til at behandle remburser.</span><span class="sxs-lookup"><span data-stu-id="b7438-104">This procedure walks through creating a Bank facility and posting profile required to process Letters of credit.</span></span> 

<span data-ttu-id="b7438-105">Disse opgaver bruger demofirmaet 'USMF'.</span><span class="sxs-lookup"><span data-stu-id="b7438-105">This tasks uses the demo company 'USMF'.</span></span>






## <a name="general-ledger-parameter"></a><span data-ttu-id="b7438-106">Finansparameter</span><span class="sxs-lookup"><span data-stu-id="b7438-106">General ledger parameter</span></span>
1. <span data-ttu-id="b7438-107">Gå til Kontant- og bankstyring > Opsætning > Kontant- og bankstyringsparametre</span><span class="sxs-lookup"><span data-stu-id="b7438-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="b7438-108">Udvid sektionen Bankdokument.</span><span class="sxs-lookup"><span data-stu-id="b7438-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="b7438-109">Vælg indstillingen Aktivér importremburs.</span><span class="sxs-lookup"><span data-stu-id="b7438-109">Select the Enable import letter of credit option.</span></span>
4. <span data-ttu-id="b7438-110">Vælg indstillingen Aktivér eksportremburs.</span><span class="sxs-lookup"><span data-stu-id="b7438-110">Select the Enable export letter of credit option.</span></span>
5. <span data-ttu-id="b7438-111">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="b7438-111">Click Save.</span></span>
6. <span data-ttu-id="b7438-112">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b7438-112">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="b7438-113">Oprette bankfacilitet</span><span class="sxs-lookup"><span data-stu-id="b7438-113">Create Bank facility</span></span>
1. <span data-ttu-id="b7438-114">Gå til Kontant- og bankstyring > Opsætning > Bankfaciliteter</span><span class="sxs-lookup"><span data-stu-id="b7438-114">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="b7438-115">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="b7438-115">Click New.</span></span>
3. <span data-ttu-id="b7438-116">Angiv navnet på bankfacilitetsgruppen i feltet Facilitetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b7438-116">In the Facility group field, enter the bank facility group name.</span></span>
4. <span data-ttu-id="b7438-117">Angiv beskrivelsen af bankfacilitetsgruppen i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b7438-117">In the Description field, enter the bank facility group description.</span></span>
5. <span data-ttu-id="b7438-118">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="b7438-118">Click Save.</span></span>
6. <span data-ttu-id="b7438-119">Klik på fanen Facilitetstyper.</span><span class="sxs-lookup"><span data-stu-id="b7438-119">Click the Facility types tab.</span></span>
7. <span data-ttu-id="b7438-120">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="b7438-120">Click New.</span></span>
8. <span data-ttu-id="b7438-121">I feltet Facilitetstype skal du angive en entydig kode.</span><span class="sxs-lookup"><span data-stu-id="b7438-121">In the Facility type field, enter a unique code.</span></span>
9. <span data-ttu-id="b7438-122">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b7438-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="b7438-123">Klik på rullelisten i feltet Facilitetsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="b7438-123">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="b7438-124">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b7438-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="b7438-125">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b7438-125">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="b7438-126">Vælg bankfacilitetens art i feltet Facilitetsart.</span><span class="sxs-lookup"><span data-stu-id="b7438-126">In the Facility nature field, select the nature of the bank facility.</span></span>
14. <span data-ttu-id="b7438-127">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="b7438-127">Click Save.</span></span>
15. <span data-ttu-id="b7438-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b7438-128">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="b7438-129">Bankbogføringsprofil</span><span class="sxs-lookup"><span data-stu-id="b7438-129">Bank posting profile</span></span>
1. <span data-ttu-id="b7438-130">Gå til Kontant- og bankstyring > Opsætning > Bogføringsprofil for bankdokumenter.</span><span class="sxs-lookup"><span data-stu-id="b7438-130">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="b7438-131">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="b7438-131">Click New.</span></span>
3. <span data-ttu-id="b7438-132">Klik på rullelisten i feltet Konto/gruppenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="b7438-132">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b7438-133">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b7438-133">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b7438-134">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b7438-134">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b7438-135">Vælg hovedkontoen til udligning.</span><span class="sxs-lookup"><span data-stu-id="b7438-135">Select the main account for settlement.</span></span>
    * <span data-ttu-id="b7438-136">Denne konto bruges til beregning af likviditetsbudgettet.</span><span class="sxs-lookup"><span data-stu-id="b7438-136">This account is used when calculating cash flow forecast.</span></span>  
7. <span data-ttu-id="b7438-137">Vælg kontoen til udgiftsposteringer i feltet Gebyrkonto.</span><span class="sxs-lookup"><span data-stu-id="b7438-137">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="b7438-138">Vælg kontoen til avanceposteringer i feltet Margenkonto.</span><span class="sxs-lookup"><span data-stu-id="b7438-138">In the Margin account field, select the account for margin transactions.</span></span>
    * <span data-ttu-id="b7438-139">Denne konto debiteres, når startdepositummet bogføres, og krediteres, når betalingen bogføres.</span><span class="sxs-lookup"><span data-stu-id="b7438-139">This account is debited when the opening margin is posted and credited when the payment is posted.</span></span>  
9. <span data-ttu-id="b7438-140">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="b7438-140">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]