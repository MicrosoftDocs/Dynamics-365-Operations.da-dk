---
title: Lukke regnskabsåret
description: Denne procedure gennemgår processen for årsafslutning, som overfører saldi til et nyt regnskabsår.
author: aprilolson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6299325bb8d77cad3977ae3c20790122574b47f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235807"
---
# <a name="close-the-fiscal-year"></a><span data-ttu-id="ae07a-103">Lukke regnskabsåret</span><span class="sxs-lookup"><span data-stu-id="ae07a-103">Close the fiscal year</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ae07a-104">Denne procedure gennemgår processen for årsafslutning, som overfører saldi til et nyt regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="ae07a-104">This procedure steps through the year end close process that transfers balances to a new fiscal year.</span></span>


## <a name="validate-year-end-close-parameters"></a><span data-ttu-id="ae07a-105">Valider årsafslutningens parametre</span><span class="sxs-lookup"><span data-stu-id="ae07a-105">Validate year-end close parameters</span></span>
1. <span data-ttu-id="ae07a-106">Gå til **Navigationsrude > Moduler > Finans > Opsætning Finans > Finansparametre**.</span><span class="sxs-lookup"><span data-stu-id="ae07a-106">Go to **Navigation pane > Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="ae07a-107">Udvid sektionen **Årsafslutning**.</span><span class="sxs-lookup"><span data-stu-id="ae07a-107">Expand the **Fiscal year close** section.</span></span>
3. <span data-ttu-id="ae07a-108">Vælg 'Ja' eller 'Nej' for indstillingen **Slet årsafslutningsposter ved overførsel**.</span><span class="sxs-lookup"><span data-stu-id="ae07a-108">Select 'Yes' or 'No' for the **Delete close-of-year transactions during transfer** option.</span></span>
    
    <span data-ttu-id="ae07a-109">Denne indstilling er vigtig, hvis regnskabsåret er blevet lukket, og årsafslutningen køres igen.</span><span class="sxs-lookup"><span data-stu-id="ae07a-109">If the fiscal year has already been closed and the year-end close is being run again, this setting is important.</span></span> <span data-ttu-id="ae07a-110">Hvis indstillingen er angivet til Ja, slettes bilaget for forrige årsafslutning, og der oprettes et nyt bilag for alle kontienes primosaldi.</span><span class="sxs-lookup"><span data-stu-id="ae07a-110">If set to Yes, the voucher for the previous year-end close will be deleted, and a new voucher will be created for all accounts beginning balances.</span></span> <span data-ttu-id="ae07a-111">Hvis indstillingen er angivet til Nej, forbliver det tidligere bilag, og der oprettes kun et nyt bilag til regulering af poster, der blev bogført efter den sidste årsafslutning.</span><span class="sxs-lookup"><span data-stu-id="ae07a-111">If set to No, the previous voucher will remain and a new voucher will only be created for adjusting entries that were posted after the last year-end close.</span></span>

4. <span data-ttu-id="ae07a-112">Vælg 'Ja' eller 'Nej' for indstillingen **Opret ultimoposter ved overførsel**.</span><span class="sxs-lookup"><span data-stu-id="ae07a-112">Select 'Yes' or 'No' for the **Create closing transactions during transfer** option.</span></span>

    <span data-ttu-id="ae07a-113">Hvis værdien angives til Ja, oprettes der to posteringer.</span><span class="sxs-lookup"><span data-stu-id="ae07a-113">If set to Yes, two transactions are created.</span></span> <span data-ttu-id="ae07a-114">Der oprettes et bilag i det regnskabsår, der afsluttes, for at bringe saldiene for P&L-finanskontiene til nul, og der oprettes et andet bilag i det næste regnskabsår for startsaldiene.</span><span class="sxs-lookup"><span data-stu-id="ae07a-114">One voucher is created in the fiscal year being closed to bring the balances of the P&L ledger accounts down to zero and a second voucher is created in the next fiscal year for the beginning balances.</span></span> <span data-ttu-id="ae07a-115">Hvis værdien angives til Nej, oprettes der et enkelt bilag i det næste regnskabsår for startsaldiene.</span><span class="sxs-lookup"><span data-stu-id="ae07a-115">If set to No, a single voucher is created in the next fiscal year for the beginning balances.</span></span>  

5. <span data-ttu-id="ae07a-116">Vælg 'Ja' eller 'Nej' for indstillingen **Indstil status til permanent afsluttet for regnskabsåret**.</span><span class="sxs-lookup"><span data-stu-id="ae07a-116">Select 'Yes' or 'No' for the **Set fiscal year status to permanently closed** option.</span></span>

    <span data-ttu-id="ae07a-117">Hvis værdien er angivet til Ja, angives regnskabsårets status til Permanent lukket.</span><span class="sxs-lookup"><span data-stu-id="ae07a-117">If set to Yes, the fiscal year status will be set to Permanently closed.</span></span>  <span data-ttu-id="ae07a-118">Da et permanent lukket år ikke kan åbnes igen, er den bedste fremgangsmåde at angive denne indstilling til Nej.</span><span class="sxs-lookup"><span data-stu-id="ae07a-118">Because a permanently closed year cannot be reopened, it would be a best practice to set this option to No.</span></span>  

6. <span data-ttu-id="ae07a-119">Vælg 'Ja' eller 'Nej' for indstillingen **Bilagsnummeret skal udfyldes under årsafslutning**.</span><span class="sxs-lookup"><span data-stu-id="ae07a-119">Select 'Yes' or 'No' for the **Voucher number must be filled in during the year end close** option.</span></span>

    <span data-ttu-id="ae07a-120">Hvis værdien er angivet til Ja, skal der manuelt angives et bilagsnummer under processen for årsafslutning.</span><span class="sxs-lookup"><span data-stu-id="ae07a-120">If set to Yes, a voucher number must be manually entered during the year end close process.</span></span> <span data-ttu-id="ae07a-121">Der bruges ikke en nummerserie til at oprette dette bilagsnummer.</span><span class="sxs-lookup"><span data-stu-id="ae07a-121">A number sequence is not used to generate this voucher number.</span></span> <span data-ttu-id="ae07a-122">Det er bedste fremgangsmåde at angive den til Ja.</span><span class="sxs-lookup"><span data-stu-id="ae07a-122">It's a best practice to set this to Yes.</span></span>  

7. <span data-ttu-id="ae07a-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ae07a-123">Close the page.</span></span>
8. <span data-ttu-id="ae07a-124">Gå til **Finans > Luk periode > Årsafslutning**.</span><span class="sxs-lookup"><span data-stu-id="ae07a-124">Go to **General ledger > Period close > Year end close**.</span></span>
9. <span data-ttu-id="ae07a-125">Klik på **Ny** for at oprette en årsafslutningsskabelon.</span><span class="sxs-lookup"><span data-stu-id="ae07a-125">Click **New** to create a year-end close template.</span></span>

    <span data-ttu-id="ae07a-126">Der kan oprettes en skabelon for en gruppe af juridiske enheder, der skal køres årsafslutning for.</span><span class="sxs-lookup"><span data-stu-id="ae07a-126">A template can be created for a group of legal entities for which to run the year-end close.</span></span> <span data-ttu-id="ae07a-127">Denne skabelon kan bruges igen år efter år.</span><span class="sxs-lookup"><span data-stu-id="ae07a-127">This template can be reused year after year.</span></span>  

10. <span data-ttu-id="ae07a-128">I feltet **Gruppenavn** skal du angive et navn til årsafslutningsskabelonen.</span><span class="sxs-lookup"><span data-stu-id="ae07a-128">In the **Group name** field, enter a year-end close template name..</span></span>
11. <span data-ttu-id="ae07a-129">Vælg det regnskabsår, som skabelonen skal oprettes for, i feltet **Regnskabskalender**.</span><span class="sxs-lookup"><span data-stu-id="ae07a-129">In the **Fiscal calendar** field, select the fiscal year for which the template will be created.</span></span>

    <span data-ttu-id="ae07a-130">Det er kun juridiske enheder, der bruger samme regnskabsår, der kan grupperes sammen i skabelonen for årsafslutning.</span><span class="sxs-lookup"><span data-stu-id="ae07a-130">Only legal entities which use the same fiscal year can be grouped together in the year-end close template.</span></span> <span data-ttu-id="ae07a-131">Det skyldes, at årsafslutningen sker ved at vælge et regnskabsår, ikke en dato.</span><span class="sxs-lookup"><span data-stu-id="ae07a-131">This is because the year end close is done by selecting a fiscal year, not a date.</span></span>  

12. <span data-ttu-id="ae07a-132">Klik på **Gem** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="ae07a-132">On the **Action pane**, click **Save**.</span></span>
13. <span data-ttu-id="ae07a-133">I sektionen **Juridiske enheder** skal du klikke på **Tilføj** for at vælge de juridiske enheder for denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="ae07a-133">In the **Legal entities** section, click **Add** to select the legal entities for this template.</span></span>
    
    <span data-ttu-id="ae07a-134">Juridiske enheder kan tilføjes ved enten at vælge de juridiske enheder eller ved at vælge et organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="ae07a-134">Legal entities can be added by either selecting the legal entities or by selecting an organizational hierarchy.</span></span>  <span data-ttu-id="ae07a-135">Der kan kun tilføjes juridiske enheder, hvor det organisatoriske hierarki med den samme regnskabskalender er valgt.</span><span class="sxs-lookup"><span data-stu-id="ae07a-135">Only legal entities with the organizational hierarchy with the same fiscal calendar selected will be added.</span></span>  

14. <span data-ttu-id="ae07a-136">Vælg enten de juridiske enheder eller organisationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="ae07a-136">Select either the legal entities or the organizational hierarchy.</span></span>
15. <span data-ttu-id="ae07a-137">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae07a-137">Click **OK**.</span></span>
16. <span data-ttu-id="ae07a-138">Vælg 'Ja' eller 'Nej' i **Overfør balancedimensioner**.</span><span class="sxs-lookup"><span data-stu-id="ae07a-138">Select 'Yes' or 'No' in the **Transfer balance sheet dimension**.</span></span>

    <span data-ttu-id="ae07a-139">Det er den bedste praksis at angive denne indstilling til Ja for statuskonti.</span><span class="sxs-lookup"><span data-stu-id="ae07a-139">It's best practice to set this option to Yes for Balance sheet accounts.</span></span> <span data-ttu-id="ae07a-140">Derved bevares de økonomiske dimensioner for bogførte posteringer, når der oprettes primosaldi for statuskonti.</span><span class="sxs-lookup"><span data-stu-id="ae07a-140">This will maintain the financial dimensions on posted transactions when creating the beginning balances for the balance sheet accounts.</span></span> <span data-ttu-id="ae07a-141">Til driftskonti kan du vælge at bevare de økonomiske dimensioner (Luk alle), når saldiene er flyttet til Overført resultat, eller du kan vælge at få de økonomiske dimensioner erstattet med en anden dimensionsværdi (Luk et enkelt).</span><span class="sxs-lookup"><span data-stu-id="ae07a-141">For profit and loss accounts, you can select to maintain the financial dimensions (Close all) when the balances are moved to Retained earnings or you can select to have the financial dimensions replaced with a different dimension value (Close single).</span></span> <span data-ttu-id="ae07a-142">Hvis du vælger Luk et enkelt, kan du definere en bestemt dimensionsværdi for hver dimension eller vælge at lade det være tomt.</span><span class="sxs-lookup"><span data-stu-id="ae07a-142">If you choose Close single, you can define a specific dimension value for each dimension or even choose to leave it blank.</span></span>  

17. <span data-ttu-id="ae07a-143">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ae07a-143">Click **Save**.</span></span>
18. <span data-ttu-id="ae07a-144">Start årsafslutningen ved at vælge **Kør regnskabsafslutning** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="ae07a-144">Start the year-end close by choosing **Run fiscal close** on the **Action Pane**.</span></span> <span data-ttu-id="ae07a-145">Årsafslutningen køres for den valgte skabelon.</span><span class="sxs-lookup"><span data-stu-id="ae07a-145">The year-end close will be run for the selected template.</span></span>  
19. <span data-ttu-id="ae07a-146">Vælg alle eller nogle af de juridiske enheder fra den skabelon, som årsafslutningen skal køres for.</span><span class="sxs-lookup"><span data-stu-id="ae07a-146">Select all or a subset of legal entities from the template for which to run the year-end close.</span></span>

    <span data-ttu-id="ae07a-147">Når årsafslutningen køres første gang, vælger de fleste organisationer at køre årsafslutningen for alle juridiske enheder i skabelonen for at få primosaldi.</span><span class="sxs-lookup"><span data-stu-id="ae07a-147">When first running the year-end close, to get beginning balance,s most organizations may choose to run the year-end close for all legal entities within the template.</span></span> <span data-ttu-id="ae07a-148">Hvis der foretages reguleringsposteringer herefter, kan du vælge at køre årsafslutningen kun for de juridiske enheder, der har justeringer.</span><span class="sxs-lookup"><span data-stu-id="ae07a-148">If adjusting entries are made after that, you may choose to run the year-end close for only the legal entities that have adjustments.</span></span>  

20. <span data-ttu-id="ae07a-149">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae07a-149">Click **OK**.</span></span>
21. <span data-ttu-id="ae07a-150">Vælg regnskabskalender, som årsafslutningen skal køres for.</span><span class="sxs-lookup"><span data-stu-id="ae07a-150">Select the fiscal year for which to run the year-end close.</span></span>
22. <span data-ttu-id="ae07a-151">Skriv en værdi i feltet **Bilag**.</span><span class="sxs-lookup"><span data-stu-id="ae07a-151">In the **Voucher field**, type a value.</span></span> <span data-ttu-id="ae07a-152">Det er god praksis at medtage regnskabsåret i bilagsnummeret for at gøre det nemmere at finde på det årsafslutningsbilag, der oprettes.</span><span class="sxs-lookup"><span data-stu-id="ae07a-152">It's best practice to include the fiscal year in the voucher number, to make it easier to find the year-end close voucher that is created.</span></span>  
23. <span data-ttu-id="ae07a-153">Årsafslutningen køres som standarder i batch.</span><span class="sxs-lookup"><span data-stu-id="ae07a-153">The year-end close defaults to run in batch.</span></span> <span data-ttu-id="ae07a-154">Det er den bedste praksis for langvarige processer, der skal køres i batchtilstand.</span><span class="sxs-lookup"><span data-stu-id="ae07a-154">It's best practice for long-running processes to run in batch mode.</span></span> <span data-ttu-id="ae07a-155">Det er typisk en af disse processer, hvilket er grunden til, at standarden er at bruge batchtilstand.</span><span class="sxs-lookup"><span data-stu-id="ae07a-155">This is typically one of those processes, which is why the default is to use batch mode.</span></span>  
24. <span data-ttu-id="ae07a-156">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae07a-156">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]