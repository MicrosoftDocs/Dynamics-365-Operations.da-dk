---
title: Økonomisk afstemning i detailbutikker
description: Dette emne beskriver økonomisk afstemning i detailbutikker for POS til Microsoft Dynamics 365 Commerce.
author: anpurush
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5d0520f35391f76b52fd8a333033b0d7ba4f7fe1
ms.sourcegitcommit: 1e6a7b50596eaf9d965e0155f3f2c50f7f50747e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/22/2020
ms.locfileid: "3498007"
---
# <a name="financial-reconciliation-in-retail-stores"></a><span data-ttu-id="46b5d-103">Økonomisk afstemning i detailbutikker</span><span class="sxs-lookup"><span data-stu-id="46b5d-103">Financial reconciliation in retail stores</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="46b5d-104">I Microsoft Dynamics 365 Commerce version 10.0.10 og tidligere giver den funktionalitet, som POS-klienten har i forbindelse med processer ved dagens afslutning i detailbutikker, mulighed for at lade butiksassistenter og butikschefer udføre aktiviteter i forbindelse med dagens afslutning.</span><span class="sxs-lookup"><span data-stu-id="46b5d-104">In Microsoft Dynamics 365 Commerce version 10.0.10 and earlier, the functionality that the point of sale (POS) client provides for end-of-day processes in retail stores lets store clerks and store managers perform end-of-day operations.</span></span> <span data-ttu-id="46b5d-105">De kan f.eks. lave kasseoptællinger, foretage skift lukket uden kontrol, afstemme skifteposteringer og lukke skift.</span><span class="sxs-lookup"><span data-stu-id="46b5d-105">For example, they can do tender declarations, blind-close shifts, reconcile shift transactions, and close shifts.</span></span> <span data-ttu-id="46b5d-106">Men der er ingen mulighed i POS til at færdiggøre de økonomiske oplysninger for skift, så de kan bruges til bogføring af regnskaber i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="46b5d-106">However, there is no capability in POS to finalize the financial information for shifts, so that it can be used to post the financials in Commerce headquarters.</span></span> <span data-ttu-id="46b5d-107">Butikschefer er typisk ansvarlige for at udføre denne opgave.</span><span class="sxs-lookup"><span data-stu-id="46b5d-107">Typically, store managers are responsible for completing this task.</span></span> <span data-ttu-id="46b5d-108">Før de kan godkende et skift, skal de gennemgå oplysningerne, foretage eventuelle nødvendige rettelser og færdiggøre totalerne for det pågældende skift.</span><span class="sxs-lookup"><span data-stu-id="46b5d-108">Before they can sign off on a shift, they must review the information, make any corrections that are required, and finalize the totals for that shift.</span></span> <span data-ttu-id="46b5d-109">De endelige totaler skal derefter bogføres i regnskabsmoduler i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="46b5d-109">The finalized totals should then be posted in financial modules in Commerce headquarters.</span></span>

<span data-ttu-id="46b5d-110">Derudover kan butikschefer i Commerce version 10.0.10 og tidligere kontrollere og foretage nogle reguleringer af opgørelseslinjer i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="46b5d-110">Additionally, in Commerce version 10.0.10 and earlier, store managers can review and make some adjustments to statement lines in Commerce headquarters.</span></span> <span data-ttu-id="46b5d-111">Muligheden er dog begrænset, og butikschefer har sjældent adgang til Commerce Headquarters-klienten.</span><span class="sxs-lookup"><span data-stu-id="46b5d-111">However, the capability is limited, and store managers rarely have access to the Commerce headquarters client.</span></span> <span data-ttu-id="46b5d-112">Desuden kan der kun foretages gennemsyn og regulering af en økonomisk detailopgørelse, når der oprettes opgørelser i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="46b5d-112">Moreover, financial retail statement review and adjustment can be done only when the statements are created in Commerce headquarters.</span></span> <span data-ttu-id="46b5d-113">Denne proces er dog typisk en, der kører natten over.</span><span class="sxs-lookup"><span data-stu-id="46b5d-113">However, that process is typically a nightly process.</span></span> <span data-ttu-id="46b5d-114">Butikschefer skal derfor vente på godkendelse af skift, når der oprettes økonomiske detailopgørelser i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="46b5d-114">Therefore, store managers must wait for the shift sign-off when financial retail statements are created in Commerce headquarters.</span></span>

<span data-ttu-id="46b5d-115">I Commerce version 10.0.11 og senere kan butikschefer gennemgå, justere og færdiggøre deres skift i POS-klienten.</span><span class="sxs-lookup"><span data-stu-id="46b5d-115">In Commerce version 10.0.11 and later, store managers can review, adjust, and finalize their shifts in the POS client itself.</span></span> <span data-ttu-id="46b5d-116">Disse oplysninger bruges derefter til at oprette og bogføre økonomiske detailopgørelser i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="46b5d-116">That data is then used to create and post financial retail statements in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="46b5d-117">Den funktionalitet, der er relateret til økonomisk afstemning i detailbutikker, fungerer kun, hvis sivende feedbaseret ordreoprettelse er slået til.</span><span class="sxs-lookup"><span data-stu-id="46b5d-117">The functionality that is related to financial reconciliation in retail stores works only if trickle feed–based order creation is turned on.</span></span> <span data-ttu-id="46b5d-118">Du kan få flere oplysninger under [Foretage sivende feedbaseret ordreoprettelse til transaktioner i detailbutik](trickle-feed.md).</span><span class="sxs-lookup"><span data-stu-id="46b5d-118">For more information, see [Trickle feed-based order creation for retail store transactions](trickle-feed.md).</span></span>

## <a name="set-up-financial-reconciliation"></a><span data-ttu-id="46b5d-119">Konfigurere økonomisk afstemning</span><span class="sxs-lookup"><span data-stu-id="46b5d-119">Set up financial reconciliation</span></span>

<span data-ttu-id="46b5d-120">Udfør følgende trin for at bruge funktionen til økonomisk afstemning.</span><span class="sxs-lookup"><span data-stu-id="46b5d-120">Follow these steps to use the financial reconciliation functionality.</span></span>

1. <span data-ttu-id="46b5d-121">Gå til arbejdsområdet **Funktionsstyring**, og aktivér funktionen **Detailopgørelser (sivende feed)**.</span><span class="sxs-lookup"><span data-stu-id="46b5d-121">In the **Feature management** workspace, turn on the **Retail statements - Trickle feed** feature.</span></span>
1. <span data-ttu-id="46b5d-122">I POS-funktionalitetsprofilen for den relevante butik skal du angive indstillingen **Aktivér økonomisk afstemning i butik** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="46b5d-122">In the POS functionality profile for the appropriate store, set the **Enable financial reconciliation in store** option to **Yes**.</span></span>

## <a name="more-information-about-financial-reconciliation"></a><span data-ttu-id="46b5d-123">Flere oplysninger om økonomisk afstemning</span><span class="sxs-lookup"><span data-stu-id="46b5d-123">More information about financial reconciliation</span></span>

<span data-ttu-id="46b5d-124">Når funktionen til økonomisk afstemning er slået til, synkroniseres nogle af de parametre, der er defineret i oversigtspanelet **Opgørelse/ultimo** på siden **Detailbutikker** i Commerce Headquarters, med kanaldatabasen.</span><span class="sxs-lookup"><span data-stu-id="46b5d-124">When the financial reconciliation functionality is turned on, some of the parameters that are defined on the **Statement/closing** FastTab of the **Retail stores** page in Commerce headquarters are synced to the channel database.</span></span> <span data-ttu-id="46b5d-125">Det samme sæt beregningskriterier og beløbsgrænser, der bruges til detailopgørelser, gennemtvinges.</span><span class="sxs-lookup"><span data-stu-id="46b5d-125">The same set of calculation criteria and amount thresholds that is used for retail statements is enforced.</span></span>

<span data-ttu-id="46b5d-126">Når handlingen **Luk skift** aktiveres, kontrollerer systemet, at de systemberegnede beløb og de erklærede beløb stemmer overens.</span><span class="sxs-lookup"><span data-stu-id="46b5d-126">When the **Close shift** operation is invoked, the system validates that the system-computed amounts and the declared amounts match.</span></span> <span data-ttu-id="46b5d-127">Hvis de er forskellige, og forskellen overskrider den definerede tærskelværdi, bliver brugeren spurgt, om han eller hun vil foretage de nødvendige justeringer.</span><span class="sxs-lookup"><span data-stu-id="46b5d-127">If they differ, and the difference exceeds defined thresholds, the user is prompted and can make the required adjustments.</span></span>

<span data-ttu-id="46b5d-128">Der kan foretages reguleringer for de enkelte betalingsmidler.</span><span class="sxs-lookup"><span data-stu-id="46b5d-128">Adjustments can be made for each tender.</span></span> <span data-ttu-id="46b5d-129">Når der er valgt et betalingsmiddel, kan brugeren få vist totalerne for forskellige posteringstyper og redigere totalerne for en bestemt posteringstype.</span><span class="sxs-lookup"><span data-stu-id="46b5d-129">When a tender is selected, the user can view the totals for different transaction types and edit the totals for a specific transaction type.</span></span> <span data-ttu-id="46b5d-130">Under redigering viser systemet det oprindeligt beregnede beløb og det tilsidesatte beløb for den pågældende posteringstype.</span><span class="sxs-lookup"><span data-stu-id="46b5d-130">During editing, the system shows the original computed amount and the overridden amount for that transaction type.</span></span> <span data-ttu-id="46b5d-131">Brugeren kan også angive bemærkninger som en del af redigeringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="46b5d-131">The user can also capture notes as a part of the editing process.</span></span> <span data-ttu-id="46b5d-132">Bemærkninger kan bruges til revisionsformål.</span><span class="sxs-lookup"><span data-stu-id="46b5d-132">Notes can be used for auditing purposes.</span></span>

<span data-ttu-id="46b5d-133">Brugerne kan ignorere valideringsprompterne og -meddelelserne og fortsætte med at lukke skiftet.</span><span class="sxs-lookup"><span data-stu-id="46b5d-133">Users can ignore the validation prompts and messages, and can proceed to close the shift.</span></span> <span data-ttu-id="46b5d-134">Men hvis en bruger ignorerer valideringsprompterne, opstår de samme problemer og skal rettes, når skiftet posterer regnskaber i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="46b5d-134">However, if a user ignores the validation prompts, the same issues will arise and will have to be fixed when the shift posts financial statements in Commerce headquarters.</span></span>

<span data-ttu-id="46b5d-135">Handlingen **Luk skift** i POS validerer også, at alle transaktioner i offlinedatabasen synkroniseres med kanaldatabasen.</span><span class="sxs-lookup"><span data-stu-id="46b5d-135">The **Close shift** operation in POS also validates that all transactions in the offline database are synced to the channel database.</span></span> <span data-ttu-id="46b5d-136">Hvis der ikke synkroniseres nogen posteringer, modtager brugeren en advarsel, da denne situation kan medføre, at systembeløbene ikke beregnes korrekt.</span><span class="sxs-lookup"><span data-stu-id="46b5d-136">If any transactions aren't synced, the user receives a warning message, because this situation can cause the system amounts to be incorrectly computed.</span></span> <span data-ttu-id="46b5d-137">I denne situation kan brugeren afslutte handlingen **Luk skift** og prøve at synkronisere offlineposteringer med kanaldatabasen.</span><span class="sxs-lookup"><span data-stu-id="46b5d-137">In this situation, the user can end the **Close shift** operation and try to sync the offline transactions to the channel database.</span></span> <span data-ttu-id="46b5d-138">Alternativt kan brugeren manuelt justere de systemberegnede beløb til kontoen for de posteringer, der ikke synkroniseres, så det korrekte sæt af økonomiske tal afsluttes og bogføres.</span><span class="sxs-lookup"><span data-stu-id="46b5d-138">Alternatively, the user can manually adjust the system-computed amounts to account for the transactions that aren't synced, so that the correct set of financial numbers is finalized and posted.</span></span> 

<span data-ttu-id="46b5d-139">Når sivende feedbaseret bogføring bruges, så bogføringen af posteringer adskilles fra bogføringen af regnskabet, kan du vælge at justere de systemberegnede beløb for manglende offlineposteringer.</span><span class="sxs-lookup"><span data-stu-id="46b5d-139">When trickle feed statement posting is used, so that the posting of transactions is separated from the posting of financials, you can choose to adjust the system-computed amounts for missing offline transactions.</span></span> <span data-ttu-id="46b5d-140">På denne måde sikrer du, at regnskaberne altid er bogført og posteret korrekt, uanset om der mangler posteringer.</span><span class="sxs-lookup"><span data-stu-id="46b5d-140">In this way, you ensure that financials are always accounted and posted correctly, regardless of missing transactions.</span></span> <span data-ttu-id="46b5d-141">Offlinetransaktioner kan synkroniseres med kanaldatabasen og Commerce Headquarters og derefter bogføres senere separat fra de økonomiske posteringer.</span><span class="sxs-lookup"><span data-stu-id="46b5d-141">Offline transactions can be synced to the channel database and Commerce headquarters, and then posted later, separately from the financial postings.</span></span>

<span data-ttu-id="46b5d-142">Oplysninger om økonomisk afstemning for et skift synkroniseres til Commerce Headquarters ved hjælp af P-job.</span><span class="sxs-lookup"><span data-stu-id="46b5d-142">Details of the financial reconciliation for a shift are synced to Commerce headquarters by using the P-job.</span></span>

<span data-ttu-id="46b5d-143">Økonomiske detailopgørelser i Commerce Headquarters beregner ikke totaler for at få vist detaljerne på opgørelseslinjerne.</span><span class="sxs-lookup"><span data-stu-id="46b5d-143">Financial retail statements in Commerce headquarters don't compute totals to show the details on the statement lines.</span></span> <span data-ttu-id="46b5d-144">I stedet bruges de endelige beløb i POS-klienten til at oprette og bogføre økonomiske detailopgørelser.</span><span class="sxs-lookup"><span data-stu-id="46b5d-144">Instead, the finalized amounts in the POS client are used to create and post financial retail statements.</span></span>