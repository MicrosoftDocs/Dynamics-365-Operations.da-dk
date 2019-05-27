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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3419d975c087350c01c6854dbbae07b6bb20bc03
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566021"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a><span data-ttu-id="44757-103">Oprette posteringsprofiler for bankfaciliteter til remburs</span><span class="sxs-lookup"><span data-stu-id="44757-103">Set up bank facilities and posting profiles for letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="44757-104">Denne procedure gennemgår oprettelsen af en bankfacilitet og posteringsprofil, der bruges til at behandle remburser.</span><span class="sxs-lookup"><span data-stu-id="44757-104">This procedure walks through creating a Bank facility and posting profile required to process Letters of credit.</span></span> 

<span data-ttu-id="44757-105">Disse opgaver bruger demofirmaet 'USMF'.</span><span class="sxs-lookup"><span data-stu-id="44757-105">This tasks uses the demo company 'USMF'.</span></span>






## <a name="general-ledger-parameter"></a><span data-ttu-id="44757-106">Finansparameter</span><span class="sxs-lookup"><span data-stu-id="44757-106">General ledger parameter</span></span>
1. <span data-ttu-id="44757-107">Gå til Kontant- og bankstyring > Opsætning > Kontant- og bankstyringsparametre</span><span class="sxs-lookup"><span data-stu-id="44757-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="44757-108">Udvid sektionen Bankdokument.</span><span class="sxs-lookup"><span data-stu-id="44757-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="44757-109">Vælg indstillingen Aktivér importremburs.</span><span class="sxs-lookup"><span data-stu-id="44757-109">Select the Enable import letter of credit option.</span></span>
4. <span data-ttu-id="44757-110">Vælg indstillingen Aktivér eksportremburs.</span><span class="sxs-lookup"><span data-stu-id="44757-110">Select the Enable export letter of credit option.</span></span>
5. <span data-ttu-id="44757-111">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="44757-111">Click Save.</span></span>
6. <span data-ttu-id="44757-112">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="44757-112">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="44757-113">Oprette bankfacilitet</span><span class="sxs-lookup"><span data-stu-id="44757-113">Create Bank facility</span></span>
1. <span data-ttu-id="44757-114">Gå til Kontant- og bankstyring > Opsætning > Bankfaciliteter</span><span class="sxs-lookup"><span data-stu-id="44757-114">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="44757-115">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="44757-115">Click New.</span></span>
3. <span data-ttu-id="44757-116">Angiv navnet på bankfacilitetsgruppen i feltet Facilitetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="44757-116">In the Facility group field, enter the bank facility group name.</span></span>
4. <span data-ttu-id="44757-117">Angiv beskrivelsen af bankfacilitetsgruppen i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="44757-117">In the Description field, enter the bank facility group description.</span></span>
5. <span data-ttu-id="44757-118">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="44757-118">Click Save.</span></span>
6. <span data-ttu-id="44757-119">Klik på fanen Facilitetstyper.</span><span class="sxs-lookup"><span data-stu-id="44757-119">Click the Facility types tab.</span></span>
7. <span data-ttu-id="44757-120">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="44757-120">Click New.</span></span>
8. <span data-ttu-id="44757-121">I feltet Facilitetstype skal du angive en entydig kode.</span><span class="sxs-lookup"><span data-stu-id="44757-121">In the Facility type field, enter a unique code.</span></span>
9. <span data-ttu-id="44757-122">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="44757-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="44757-123">Klik på rullelisten i feltet Facilitetsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="44757-123">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="44757-124">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="44757-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="44757-125">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="44757-125">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="44757-126">Vælg bankfacilitetens art i feltet Facilitetsart.</span><span class="sxs-lookup"><span data-stu-id="44757-126">In the Facility nature field, select the nature of the bank facility.</span></span>
14. <span data-ttu-id="44757-127">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="44757-127">Click Save.</span></span>
15. <span data-ttu-id="44757-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="44757-128">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="44757-129">Bankbogføringsprofil</span><span class="sxs-lookup"><span data-stu-id="44757-129">Bank posting profile</span></span>
1. <span data-ttu-id="44757-130">Gå til Kontant- og bankstyring > Opsætning > Bogføringsprofil for bankdokumenter.</span><span class="sxs-lookup"><span data-stu-id="44757-130">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="44757-131">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="44757-131">Click New.</span></span>
3. <span data-ttu-id="44757-132">Klik på rullelisten i feltet Konto/gruppenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="44757-132">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="44757-133">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="44757-133">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="44757-134">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="44757-134">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="44757-135">Vælg hovedkontoen til udligning.</span><span class="sxs-lookup"><span data-stu-id="44757-135">Select the main account for settlement.</span></span>
    * <span data-ttu-id="44757-136">Denne konto bruges til beregning af likviditetsbudgettet.</span><span class="sxs-lookup"><span data-stu-id="44757-136">This account is used when calculating cash flow forecast.</span></span>  
7. <span data-ttu-id="44757-137">Vælg kontoen til udgiftsposteringer i feltet Gebyrkonto.</span><span class="sxs-lookup"><span data-stu-id="44757-137">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="44757-138">Vælg kontoen til avanceposteringer i feltet Margenkonto.</span><span class="sxs-lookup"><span data-stu-id="44757-138">In the Margin account field, select the account for margin transactions.</span></span>
    * <span data-ttu-id="44757-139">Denne konto debiteres, når startdepositummet bogføres, og krediteres, når betalingen bogføres.</span><span class="sxs-lookup"><span data-stu-id="44757-139">This account is debited when the opening margin is posted and credited when the payment is posted.</span></span>  
9. <span data-ttu-id="44757-140">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="44757-140">Click Save.</span></span>

