---
title: Ofte spurgte spørgsmål i forbindelse med ultimoaktiviteter
description: Dette emne er kompileret for at hjælpe med ultimoaktiviteter.
author: kweekley
manager: tfehr
ms.date: 01/25/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6d10f54913ca8dff56a59ea597a9bd7c3e69d4bc
ms.sourcegitcommit: bd4763cc6088e114818e80bb1c27c6521b039743
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/02/2021
ms.locfileid: "5107689"
---
# <a name="year-end-activities-faq"></a><span data-ttu-id="ad292-103">Ofte spurgte spørgsmål i forbindelse med ultimoaktiviteter</span><span class="sxs-lookup"><span data-stu-id="ad292-103">Year-end activities FAQ</span></span> 

<span data-ttu-id="ad292-104">Dette emne er kompileret for at hjælpe med ultimoaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="ad292-104">This topic has been compiled to assist with year-end closing activities.</span></span> <span data-ttu-id="ad292-105">Oplysningerne i dette emne fokuserer primært på spørgsmål, der vedrører ultimoaktiviteter ved årsopgørelsen for Finans og Kreditor.</span><span class="sxs-lookup"><span data-stu-id="ad292-105">The information in this topic primarily focuses on questions concerning year-end closing activities  for General ledger and Accounts payable.</span></span>

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a><span data-ttu-id="ad292-106">Finans: Hvordan ved jeg, at vi kører ultimoafslutning og ikke kan fortryde ultimoafslutning?</span><span class="sxs-lookup"><span data-stu-id="ad292-106">General ledger: How do I know that we're running year-end close and not undoing year-end close?</span></span>
<span data-ttu-id="ad292-107">Vi har set organisationer forsøge at køre ultimoafslutninger, men i stedet fortrød ultimoafslutningen.</span><span class="sxs-lookup"><span data-stu-id="ad292-107">We have seen organizations try to run the year-end close but instead were performing an undo of the year-end close.</span></span> <span data-ttu-id="ad292-108">Hvis ultimoafslutning lukkes meget hurtigt, eller ultimoafslutning ikke giver startsaldi, skal du validere indstillingen **Fortryd forrige lukning** i **Ultimoafslutning** (**Finans > Periodelukning > Ultimoafslutning > Kør regnskabsafslutning**).</span><span class="sxs-lookup"><span data-stu-id="ad292-108">If the year-end close is finishing really quickly or the year end close does not produce opening balances, validate the **Undo previous close** setting in **Year-end close** (**General ledger > Period close > Year end close > Run fiscal close**).</span></span> 

<span data-ttu-id="ad292-109">[![Kør ultimoafslutning i forhold til fortryd ultimoafslutning](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)</span><span class="sxs-lookup"><span data-stu-id="ad292-109">[![Running year-end close versus undoing year-end close](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)</span></span>

<span data-ttu-id="ad292-110">Hvis **Fortryd forrige afslutning** er angivet til **Ja**, tilbageføres den forrige ultimoafslutning.</span><span class="sxs-lookup"><span data-stu-id="ad292-110">If the **Undo previous close** selection is set to **Yes**, the previous year-end close is being reversed.</span></span> <span data-ttu-id="ad292-111">Når du kører en fortrydelse, slettes alle ultimosaldoposter og startsaldoposter, som om ultimoafslutningen aldrig var blevet kørt.</span><span class="sxs-lookup"><span data-stu-id="ad292-111">When running an undo, all closing balance and opening balance entries will be deleted, as if the year-end close had never been run.</span></span> <span data-ttu-id="ad292-112">Bilagene slettes.</span><span class="sxs-lookup"><span data-stu-id="ad292-112">The vouchers are deleted.</span></span> <span data-ttu-id="ad292-113">Årsafslutningen køres ikke automatisk igen.</span><span class="sxs-lookup"><span data-stu-id="ad292-113">The year-end close will not run again automatically.</span></span> <span data-ttu-id="ad292-114">Du skal starte processen igen, og denne gang skal du ændre **Fortryd forrige lukning** til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="ad292-114">You must start the process again, this time changing **Undo previous close** to **No**.</span></span> 

> [!NOTE]
> <span data-ttu-id="ad292-115">Ultimosaldoposten oprettes efter eget valg i det år, der afsluttes.</span><span class="sxs-lookup"><span data-stu-id="ad292-115">The closing balance entry is optionally created in the year being closed.</span></span> <span data-ttu-id="ad292-116">Dette sker kun, hvis parameteren Finans **Opret ultimoposteringer ved overførsel** er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ad292-116">This only occurs if the General ledger parameter **Create closing transactions during transfer** is set to **Yes**.</span></span> <span data-ttu-id="ad292-117">Startsaldoposten oprettes altid, da dette er startsaldoen for det næste år.</span><span class="sxs-lookup"><span data-stu-id="ad292-117">The opening balance entry is always created, because this is the beginning balance for the next year.</span></span>  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a><span data-ttu-id="ad292-118">Finans: Hvad er forskellen mellem Fortryd og Slet Finansparameteren for årsslutning?</span><span class="sxs-lookup"><span data-stu-id="ad292-118">General ledger: What is the difference between Undo and Delete GL parameter for year-end close?</span></span>
<span data-ttu-id="ad292-119">Der kan være forvirring over forskellen mellem parameteren **Fortryd forrige lukning**, der findes i dialogboksen til **Årsafslutning**, og posteringerne for parameteren **Slette årsafslutningsposter ved overførsel** i Finans (**Finans > Periodens afslutning > Årsslutslutning > Kør regnskabsafslutning**).</span><span class="sxs-lookup"><span data-stu-id="ad292-119">Confusion might exist over the difference between the **Undo previous close** parameter, which is in the **Year-end close** dialog box, and the **Delete close-of-year transactions during transfer** parameter in General ledger (**General ledger > Period close > Year-end close > Run fiscal close**).</span></span>  

<span data-ttu-id="ad292-120">[![Forskellen mellem Fortryd og Slet Finansparameteren for årsslutning](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)</span><span class="sxs-lookup"><span data-stu-id="ad292-120">[![Difference between Undo and Delete GL parameter for year-end close](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)</span></span>

<span data-ttu-id="ad292-121">Vælg **Fortryd forrige afslutning** i rullemenuen, når du kører årsafslutningen for at slette alle ultimosaldo- og startsaldoposter, som om årsafslutningen aldrig var blevet kørt.</span><span class="sxs-lookup"><span data-stu-id="ad292-121">Select **Undo previous close** in the drop-down dialog menu when running the year-end close process to delete all closing balance and opening balance entries, as if the year-end close had never been run.</span></span> <span data-ttu-id="ad292-122">Bilagene slettes.</span><span class="sxs-lookup"><span data-stu-id="ad292-122">The vouchers will be deleted.</span></span> <span data-ttu-id="ad292-123">Årsafslutningen køres ikke automatisk igen.</span><span class="sxs-lookup"><span data-stu-id="ad292-123">The year-end close will not run again automatically.</span></span> <span data-ttu-id="ad292-124">Hvis du vil køre årsafslutningen, skal du starte denne proces igen, og denne gang skal du ændre **Fortryd forrige afslutning** til **Nej** (**Finans > Opsætning af Finans > Finansparametre**).</span><span class="sxs-lookup"><span data-stu-id="ad292-124">To run the year-end close, you must initiate this process again, this time changing **Undo previous close** to **No** (**General ledger > Ledger setup > General ledger parameters**).</span></span> 

<span data-ttu-id="ad292-125">[![Konfiguration af Finansparametre](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)</span><span class="sxs-lookup"><span data-stu-id="ad292-125">[![General ledger parameter setting](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)</span></span>

<span data-ttu-id="ad292-126">Parameteret **Slette årsafslutningsposter ved overførsel** i Finans bruges kun, når der køres (ikke fortrydes) årsslutslutning årsafslutning (**Fortryd forrige afslutning** er angivet til **Nej**).</span><span class="sxs-lookup"><span data-stu-id="ad292-126">The **Delete close-of-year transactions during transfer** parameter in General ledger is used only when running (not undoing) the year-end close (the **Undo previous close** selection is set to **No**).</span></span> <span data-ttu-id="ad292-127">Hvis den parameter er angivet til **Ja**, slettes alle ultimosaldoposter og startsaldoposter, og årsafslutningen køres igen.</span><span class="sxs-lookup"><span data-stu-id="ad292-127">If that parameter is set to **Yes**, all closing balance and opening balance entries will be deleted and the year-end close will run again.</span></span> <span data-ttu-id="ad292-128">Denne proces bruges, når organisationen ønsker, at alle posteringer, herunder reguleringer siden sidste årsafslutning, skal bogføres i en enkelt regnskabspost for ultimosaldo- og startsaldoposter.</span><span class="sxs-lookup"><span data-stu-id="ad292-128">This process is used when the organization wants all transactions, including adjustments since the last year-end close, to be posted in a single accounting entry for the closing balance and opening balance entries.</span></span> 

<span data-ttu-id="ad292-129">Hvis denne indstilling er angivet til **Nej**, bevares alle ultimosaldo- og startsaldoposter.</span><span class="sxs-lookup"><span data-stu-id="ad292-129">If this option is set to **No**, all closing balance and opening balance entries remain.</span></span> <span data-ttu-id="ad292-130">De slettes ikke.</span><span class="sxs-lookup"><span data-stu-id="ad292-130">They are not deleted.</span></span> <span data-ttu-id="ad292-131">Der oprettes i stedet en ny ultimosaldo- og startsaldopost for de delta- eller nye posteringer, der er bogført siden sidste årsafslutning af regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="ad292-131">Instead, a new closing balance and opening balance entry will be created for only the delta or new transactions posted since the last year-end close for that fiscal year.</span></span>  

> [!NOTE]
> <span data-ttu-id="ad292-132">Ultimosaldoposten oprettes i det år, der afsluttes.</span><span class="sxs-lookup"><span data-stu-id="ad292-132">The closing balance entry is created in the year being closed.</span></span> <span data-ttu-id="ad292-133">Dette sker kun, hvis parameteren Finans **Opret ultimoposteringer ved overførsel** er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ad292-133">This only occurs if the **Create closing transactions during transfer** parameter in General ledger is set to **Yes**.</span></span> <span data-ttu-id="ad292-134">Startsaldoposten oprettes altid, da dette er startsaldoen for det næste år.</span><span class="sxs-lookup"><span data-stu-id="ad292-134">The opening balance entry is always created, because this is the beginning balance for the next year.</span></span> 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a><span data-ttu-id="ad292-135">Finans: Hvad kan ændres for at øge ydeevnen for årsafslutningsbehandling?</span><span class="sxs-lookup"><span data-stu-id="ad292-135">General ledger: What can be changed to enhance performance of year-end processing?</span></span> 
<span data-ttu-id="ad292-136">Du kan foretage en række ændringer for at forbedre ydeevnen i forbindelse med årsafslutningen.</span><span class="sxs-lookup"><span data-stu-id="ad292-136">You can make a number of changes to improve performance of the year-end close.</span></span> <span data-ttu-id="ad292-137">Det anbefales, at du evaluerer disse foreslåede ændringer for at finde ud af, om ændringen er relevant for organisationen.</span><span class="sxs-lookup"><span data-stu-id="ad292-137">We recommend that you evaluate these suggested changes to consider whether the change is appropriate for your organization.</span></span>  

### <a name="dimension-sets"></a><span data-ttu-id="ad292-138">Dimensionsopsætninger</span><span class="sxs-lookup"><span data-stu-id="ad292-138">Dimension sets</span></span>
<span data-ttu-id="ad292-139">Når du kører årsafslutning, oprettes de enkelte saldi igen, hvilket har direkte indflydelse på ydeevnen.</span><span class="sxs-lookup"><span data-stu-id="ad292-139">When running the year end close, each dimension set balance is rebuilt, having a direct impact on the performance.</span></span> <span data-ttu-id="ad292-140">Visse organisationer opretter dimensionsopsætninger unødvendigt, fordi de er brugt på et tidspunkt eller måske skal bruges på et tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="ad292-140">Some organizations create dimension sets unnecessarily because they were used at one point or might be used at some point.</span></span>  <span data-ttu-id="ad292-141">Disse unødvendige dimensionsopsætninger opbygges stadig, når årsslutningen lukkes, hvilket øger den tid, der bruges til processen.</span><span class="sxs-lookup"><span data-stu-id="ad292-141">These unnecessary dimension sets are still rebuilt during the year end close, which adds time to the process.</span></span> <span data-ttu-id="ad292-142">Brug tid på at evaluere dimensionsopsætninger og slette eventuelle unødvendige dimensionsopsætninger.</span><span class="sxs-lookup"><span data-stu-id="ad292-142">Take time to evaluate your dimension sets and delete any unnecessary dimension sets.</span></span>

<span data-ttu-id="ad292-143">De unødvendige dimensionsopsætninger har også indflydelse på batchjobbet **BudgetDimensionFocusInitializeBalance** (**Finans > Kontoplan > Dimensioner > Økonomiske dimensionsopsætninger**).</span><span class="sxs-lookup"><span data-stu-id="ad292-143">The unnecessary dimension sets also impact the batch job **BudgetDimensionFocusInitializeBalance** (**General ledger > Chart of accounts > Dimensions > Financial dimension sets**).</span></span>

<span data-ttu-id="ad292-144">[![Økonomiske dimensionsopsætninger](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)</span><span class="sxs-lookup"><span data-stu-id="ad292-144">[![Financial dimension sets](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)</span></span>

### <a name="year-end-close-template-configuration"></a><span data-ttu-id="ad292-145">Konfiguration af skabelon til årsafslutning</span><span class="sxs-lookup"><span data-stu-id="ad292-145">Year-end close template configuration</span></span>
<span data-ttu-id="ad292-146">I skabelonen til årsafslutning kan organisationer vælge det økonomiske dimensionsniveau, der skal vedligeholdes ved overførsel af driftssaldi til overført overskud.</span><span class="sxs-lookup"><span data-stu-id="ad292-146">The year-end close template lets organizations select the financial dimension level to maintain when transferring profit and loss balances to retained earnings.</span></span> <span data-ttu-id="ad292-147">Indstillingerne giver en organisation mulighed for at vedligeholde de detaljerede økonomiske dimensioner (**Luk alle**) ved flytning af saldi til overført resultat eller vælger at opsummere beløbene til en enkelt dimensionsværdi (**Luk enkelt**).</span><span class="sxs-lookup"><span data-stu-id="ad292-147">The settings allow an organization to maintain the detailed financial dimensions (**Close all**) when moving the balances to retained earnings or choose to summarize the amounts to a single dimension value (**Close single**).</span></span> <span data-ttu-id="ad292-148">Dette kan defineres for hver økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="ad292-148">This can be defined for each financial dimension.</span></span> <span data-ttu-id="ad292-149">Yderligere oplysninger om disse indstillinger finder du i emnet [Årsafslutning](year-end-close.md).</span><span class="sxs-lookup"><span data-stu-id="ad292-149">For more information on these settings, see the [Year-end close](year-end-close.md) topic.</span></span>

<span data-ttu-id="ad292-150">Det anbefales, at du evaluerer organisationens krav og, hvis det er muligt, lukker så mange dimensioner som muligt ved hjælp af indstillingen **Luk enkelt** for at forbedre ydeevnen.</span><span class="sxs-lookup"><span data-stu-id="ad292-150">We recommend that you evaluate your organization's requirements and if possible, close as many dimensions as possible using the **Close single** year-end option to improve performance.</span></span> <span data-ttu-id="ad292-151">Ved at lukke til en enkelt dimensionsværdi (som også kan være en tom værdi), beregner systemet færre detaljer ved bestemmelse af saldi for poster på konti til overført overskud.</span><span class="sxs-lookup"><span data-stu-id="ad292-151">By closing to a single dimension value (which can also be a blank value), the system calculates less detail when determining the balances for retained earnings account entries.</span></span>

### <a name="10013-update-or-later"></a><span data-ttu-id="ad292-152">10.0.13 opdatering eller senere</span><span class="sxs-lookup"><span data-stu-id="ad292-152">10.0.13 update or later</span></span>
<span data-ttu-id="ad292-153">Hvis du har opdateret til version 10.0.13 eller senere, siden sidste gang organisationen kørte en årsafslutning, kan årsafslutningen tage længere tid pga. [HashV2-funktionsimplementering](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/verify-hash-function-changes-after-update-to-dynamics-365-finance-2020-release-wave-2)2.</span><span class="sxs-lookup"><span data-stu-id="ad292-153">If you've updated to version 10.0.13 or later since the last time your organization ran a year-end close, the year-end close process could take longer due to the [HashV2 feature implementation](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/verify-hash-function-changes-after-update-to-dynamics-365-finance-2020-release-wave-2).</span></span> <span data-ttu-id="ad292-154">(Betegnelsen *hash* refererer til et felt, der er beregnet ud fra andre strengfelter.</span><span class="sxs-lookup"><span data-stu-id="ad292-154">(The term *hash* refers to a field that is calculated from other string fields.</span></span> <span data-ttu-id="ad292-155">API'en til beregning af værdien for Hash GUID-værdien er opdateret for at øge sikkerheden. For hurtigere at kunne afslutte ultimoaktiviteter anbefales det, at saldi for dimensionsopsætninger gendannes, før ultimoafslutningen køres.</span><span class="sxs-lookup"><span data-stu-id="ad292-155">The API to calculate the hash GUID value was updated to enhance security.) To speed up the year-end closing process, we recommend rebuilding the balances of the dimension sets before running the year-end close.</span></span> <span data-ttu-id="ad292-156">Hvis du allerede har udført en gendannelse af saldi for dimensionsopsætninger efter at have foretaget opdateringen 10.0.13, er det ikke nødvendigt at køre gendanne processen.</span><span class="sxs-lookup"><span data-stu-id="ad292-156">If you've already performed a rebuild of the dimension set balances after taking the 10.0.13 update, it's not necessary to run the rebuild process again.</span></span>
 
## <a name="general-ledger--what-does-the-period-close--year-end-close-do"></a><span data-ttu-id="ad292-157">Finans – Hvad betyder Periodelukning – Årsafslutning?</span><span class="sxs-lookup"><span data-stu-id="ad292-157">General ledger – What does the Period close – Year-end close do?</span></span>
 
<span data-ttu-id="ad292-158">[![Periodelukning, årsafslutning](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)</span><span class="sxs-lookup"><span data-stu-id="ad292-158">[![Period close, year-end close](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)</span></span>

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets-new-feature"></a><span data-ttu-id="ad292-159">Forbedringer af ydeevne til gendannelse af økonomiske dimensionsopsætninger (ny funktion)</span><span class="sxs-lookup"><span data-stu-id="ad292-159">Performance improvements for rebuilding financial dimension sets (new feature)</span></span>
<span data-ttu-id="ad292-160">En ny funktion, der er tilføjet i version 10.0.16, forbedrer ydeevnen årsafslutnings- og konsolideringsprocesserne.</span><span class="sxs-lookup"><span data-stu-id="ad292-160">A new feature added in version 10.0.16 improves the performance of the year-end close and consolidation processes.</span></span> <span data-ttu-id="ad292-161">Funktionen er navngivet, Forbedringer af ydeevne til gendannelse af økonomiske dimensionsopsætninger.</span><span class="sxs-lookup"><span data-stu-id="ad292-161">The feature is named, Performance improvements for rebuilding financial dimension sets.</span></span> <span data-ttu-id="ad292-162">Med denne funktion ændres den måde, dimensionsopsætninger opbygges på, så de kun opbygges i en relevant tidsramme.</span><span class="sxs-lookup"><span data-stu-id="ad292-162">This feature changes the way dimension sets are rebuilt so that they are rebuilt only for a relevant time frame.</span></span> <span data-ttu-id="ad292-163">I tidligere versioner blev dimensionssæt genopført for alle datoer.</span><span class="sxs-lookup"><span data-stu-id="ad292-163">In the previous versions, dimension sets were rebuilt for all dates.</span></span> <span data-ttu-id="ad292-164">Hvis du f.eks. lukker år 2020, gendanner systemet kun saldi for posteringer i regnskabsåret 2020.</span><span class="sxs-lookup"><span data-stu-id="ad292-164">For example, if you're closing the year 2020, the system will only rebuild the balances for transactions within the fiscal year 2020.</span></span> <span data-ttu-id="ad292-165">Hvis du kører konsolidering for et datointerval fra 1. november 2020 til 30. november 2020, gendanner systemet kun saldi for dette datointerval.</span><span class="sxs-lookup"><span data-stu-id="ad292-165">If you're running consolidation for a date range of November 1, 2020 to November 30, 2020, the system will only rebuild the balances for that date range.</span></span>

<span data-ttu-id="ad292-166">Da denne funktion opfattes som en ændring, der giver beskadigelse, skal du aktivere den ved hjælp af arbejdsområdet **Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="ad292-166">Because this feature is considered a breaking change, you'll need to enable it using the **Feature management** workspace.</span></span>
 
<span data-ttu-id="ad292-167">[![Årsafslutning](./media/faq-2020-yr-end-06.png)](./media/faq-2020-yr-end-06.png)</span><span class="sxs-lookup"><span data-stu-id="ad292-167">[![Year-end close](./media/faq-2020-yr-end-06.png)](./media/faq-2020-yr-end-06.png)</span></span>

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2020"></a><span data-ttu-id="ad292-168">Kreditor: Hvilke ændringer er der foretaget for at understøtte 1099-årsafslutningsrapportering for 2020?</span><span class="sxs-lookup"><span data-stu-id="ad292-168">Accounts payable: What changes have been made to support 1099 year-end reporting for 2020?</span></span>

<span data-ttu-id="ad292-169">Der er tilføjet to nye lovpligtige funktioner for ændringer i 1099-årsafslutning i 2020.</span><span class="sxs-lookup"><span data-stu-id="ad292-169">Two new regulatory features have been added for 1099 year-end changes in 2020.</span></span> <span data-ttu-id="ad292-170">Den første funktion, **Anvend ændringer på 1099-NEC og 1099-MISC-formularer til 2020**, blev udgivet midt i året som en obligatorisk funktion.</span><span class="sxs-lookup"><span data-stu-id="ad292-170">The first feature, **Apply changes to 1099-NEC and 1099-MISC forms for 2020**, was released mid-year as a mandatory feature.</span></span> <span data-ttu-id="ad292-171">Formålet med dette er at sikre, at der kan spores 1099-transaktionsdata for året 2020 til den nye 1099-NEC-formular.</span><span class="sxs-lookup"><span data-stu-id="ad292-171">Its purpose is to ensure that 1099 transactional data for the year 2020 can be tracked for the new 1099-NEC form.</span></span> <span data-ttu-id="ad292-172">Denne funktion har tilføjet de 1099-felter, der skal bruges for at understøtte de nye 1099-NEC og opdaterede 1099-MISC-felter.</span><span class="sxs-lookup"><span data-stu-id="ad292-172">This feature added the 1099 fields that are needed to support the new 1099-NEC and updated the 1099-MISC fields.</span></span> <span data-ttu-id="ad292-173">Denne opdatering har også opgraderet kreditorpostdataene til 1099-feltoplysningerne.</span><span class="sxs-lookup"><span data-stu-id="ad292-173">This update also upgraded vendor record data for the 1099 box information.</span></span> 

<span data-ttu-id="ad292-174">Den anden lovpligtige funktion, **1099-erklæringer, der er opdateret til 2020-skattelovgivningen**, indeholder følgende ændringer.</span><span class="sxs-lookup"><span data-stu-id="ad292-174">The second regulatory feature, **1099 statements updated for 2020 tax law**, contains the following changes.</span></span>

- <span data-ttu-id="ad292-175">1099-OID - IRS har konverteret formularen til fortløbende brug.</span><span class="sxs-lookup"><span data-stu-id="ad292-175">1099-OID - The IRS has converted the form to continuous use.</span></span>
   - <span data-ttu-id="ad292-176">Rapporteringsårets nummer 3 og 4 skal udfyldes, når de udskrives.</span><span class="sxs-lookup"><span data-stu-id="ad292-176">The reporting year’s 3rd and 4th digit must be filled in when printed.</span></span> <span data-ttu-id="ad292-177">Brug udskriftsindstillingerne i **Rapporteringsår**-feltets 3. og 4. cifre fra 4. cifre fra **Udskriftsindstillinger for Moms 1099**.</span><span class="sxs-lookup"><span data-stu-id="ad292-177">Use the **Reporting year** field’s 3rd and 4th digits from **Tax 1099 print options**.</span></span> 

- <span data-ttu-id="ad292-178">1099-NEC – En ny formular til 2020.</span><span class="sxs-lookup"><span data-stu-id="ad292-178">1099-NEC – A new form for 2020.</span></span> <span data-ttu-id="ad292-179">Denne registrerer kompensation for ingen ansatte.</span><span class="sxs-lookup"><span data-stu-id="ad292-179">This records nonemployee compensation.</span></span> 

-   <span data-ttu-id="ad292-180">1099-MISC – På grund af oprettelsen af formular 1099-NEC har IRS revideret formular 1099-MISC og omarrangeret feltnumre til rapportering af bestemte indtægter.</span><span class="sxs-lookup"><span data-stu-id="ad292-180">1099-MISC – Due to the creation of Form 1099-NEC, the IRS has revised Form 1099-MISC and rearranged box numbers for reporting certain income.</span></span>
<span data-ttu-id="ad292-181">Ændringer i rapportering af indtægter og formularens feltnumre vises nedenfor.</span><span class="sxs-lookup"><span data-stu-id="ad292-181">Changes in the reporting of income and the form’s box numbers are listed below.</span></span>
   - <span data-ttu-id="ad292-182">Betaleren har foretaget direkte salg for $5.000 eller mere (afkrydsningsfelt) i felt 7.</span><span class="sxs-lookup"><span data-stu-id="ad292-182">Payer made direct sales of $5,000 or more (check box) in box 7.</span></span>
   - <span data-ttu-id="ad292-183">Forsikringspræmien indberettes i felt 9.</span><span class="sxs-lookup"><span data-stu-id="ad292-183">Crop insurance proceeds are reported in box 9.</span></span>
   - <span data-ttu-id="ad292-184">Bruttofortjeneste til jurist rapporteres i felt 10.</span><span class="sxs-lookup"><span data-stu-id="ad292-184">Gross proceeds to an attorney are reported in box 10.</span></span>
   - <span data-ttu-id="ad292-185">Sektion 409A udskydelser rapporteres i felt 12.</span><span class="sxs-lookup"><span data-stu-id="ad292-185">Section 409A deferrals are reported in box 12.</span></span>
   - <span data-ttu-id="ad292-186">Ikke-kvalificeret udskudt kompensationsindtægt rapporteres i felt 14.</span><span class="sxs-lookup"><span data-stu-id="ad292-186">Nonqualified deferred compensation income is reported in box 14.</span></span>
   - <span data-ttu-id="ad292-187">Felterne 15, 16 og 17 indberetter tilbageholdt statsskat, stats-id og indtægtsbeløb i staten.</span><span class="sxs-lookup"><span data-stu-id="ad292-187">Boxes 15, 16, and 17 report state taxes withheld, state identification number, and amount of income earned in the state, respectively.</span></span>

- <span data-ttu-id="ad292-188">Ingen ændringer af 1099-DIV eller 1099-INT i 2020.</span><span class="sxs-lookup"><span data-stu-id="ad292-188">No changes to 1099-DIV or 1099-INT in 2020.</span></span>

- <span data-ttu-id="ad292-189">Elektronisk indsendelse – Formatet er ændret for at tage højde for den nye NEC-formular, og MISC-feltet ændres som beskrevet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="ad292-189">Electronic filing – The format has changed to accommodate the new NEC form, and the MISC box changes described above.</span></span> <span data-ttu-id="ad292-190">Se [IRS-publikation 1220](https://www.irs.gov/pub/irs-pdf/p1220.pdf), hvis du vil have specifikke oplysninger om elektronisk indsendelse.</span><span class="sxs-lookup"><span data-stu-id="ad292-190">For specific information on electronic filing requirements, see [IRS Publication 1220](https://www.irs.gov/pub/irs-pdf/p1220.pdf).</span></span>

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a><span data-ttu-id="ad292-191">Kreditor: 1099 – Hvordan ændrer jeg 1099-feltet og -værdier for en kreditor, der ikke sporer 1099-oplysninger i løbet af hele året?</span><span class="sxs-lookup"><span data-stu-id="ad292-191">Accounts payable: 1099 – How do I change the 1099 box and values for a vendor that wasn’t tracking 1099 information throughout the year?</span></span>
<span data-ttu-id="ad292-192">Brug funktionen Opdater 1099 (**Kreditor > Kreditorer>Alle kreditorer > Vælg en kreditor > fanen Kreditor på båndet > Opdater 1099**) for at gennemgå tidligere betalte fakturaposteringer for at tildele 1099-dataene igen i henhold til indstillingerne under fanen **Moms 1099** på siden **Kreditor**.</span><span class="sxs-lookup"><span data-stu-id="ad292-192">Use the Update 1099 functionality (**Accounts payable > Vendors>All vendors > Select a vendor > Vendor tab in ribbon > Update 1099**) to go through previously paid invoice transactions to reassign the 1099 data appropriately according to the settings on the **Tax 1099** tab on the **Vendor** page.</span></span>

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a><span data-ttu-id="ad292-193">Kan jeg køre 1099-opdateringen for alle mine kreditorer på én gang?</span><span class="sxs-lookup"><span data-stu-id="ad292-193">Can I run the Update 1099 for all my vendors at once?</span></span>
<span data-ttu-id="ad292-194">Nr.</span><span class="sxs-lookup"><span data-stu-id="ad292-194">No.</span></span> <span data-ttu-id="ad292-195">Opdateringsrutinen 1099 udføres i forhold til en enkelt leverandør ad gangen.</span><span class="sxs-lookup"><span data-stu-id="ad292-195">The Update 1099 routine is performed against a single vendor at a time.</span></span> <span data-ttu-id="ad292-196">Hvis organisationen har brug for dette krav, skal du stemme for ideen med titlen [BatchProces for opdatering af kreditors 1099-data](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).</span><span class="sxs-lookup"><span data-stu-id="ad292-196">If this requirement is needed by your organization, please vote for the Idea titled [Batch Process for Update of Vendor's 1099 Data](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).</span></span>

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-vs-update-all-in-the-update-1099-utility"></a><span data-ttu-id="ad292-197">Kreditor: 1099 – "Genberegn eksisterende 1099-beløb" vs. "Opdater alle" i Opdatering 1099-værktøjet.</span><span class="sxs-lookup"><span data-stu-id="ad292-197">Accounts payable: 1099 – “Recalculate existing 1099 amounts” vs. “Update all” in the Update 1099 utility.</span></span>
<span data-ttu-id="ad292-198">**Genberegn eksisterende 1099-beløb**-afkrydsningsfeltet nulstiller 1099-beløbet til det samlede betalte beløb, når det bruges sammen med afkrydsningsfeltet **Opdater alle**.</span><span class="sxs-lookup"><span data-stu-id="ad292-198">The **Recalculate existing 1099 amounts** check box will reset the 1099 amount to the total paid values, when used in conjunction with the **Update all** check box.</span></span> 

<span data-ttu-id="ad292-199">[![Moms 1099-transaktioner: Før opdateringsrutinen køres](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)</span><span class="sxs-lookup"><span data-stu-id="ad292-199">[![Tax 1099 transactions: Before running the update routine](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)</span></span>

<span data-ttu-id="ad292-200">Afkrydsningsfeltet **Genberegn eksisterende 1099-beløb** træder først i kraft, når der er 1099-delværdier på fakturaen, eller hvis det er ændret i formularen Moms 1099.</span><span class="sxs-lookup"><span data-stu-id="ad292-200">The **Recalculate existing 1099 amounts** check box only comes into play when there are partial 1099 values on the invoice or if it was modified on the Tax 1099 form.</span></span> <span data-ttu-id="ad292-201">Antag f.eks., at en faktura har værditilvæksten i $1000,00, men brugeren skriver manuelt et 1099-beløb på $500,00.</span><span class="sxs-lookup"><span data-stu-id="ad292-201">For example, assume you have an invoice valued at $1000.00, but the user manually types in a 1099 amount on the invoice of $500.00.</span></span>

<span data-ttu-id="ad292-202">[![Moms 1099-transaktioner: Afmærkning af både Opdater alle og Genberegn eksisterende 1099-beløb](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)</span><span class="sxs-lookup"><span data-stu-id="ad292-202">[![Tax 1099 transactions: Marking both Update all and Recalculate existing 1099 amounts](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)</span></span>

<span data-ttu-id="ad292-203">Når denne betaling er betalt, er de $500.00 det 1099-beløb, der er betalt.</span><span class="sxs-lookup"><span data-stu-id="ad292-203">When this is paid, $500.00 will be the 1099 amount paid.</span></span> <span data-ttu-id="ad292-204">Hvis du udfører efterberegningsrutinen, vil systemet ændre 1099-beløbet til $1000,00, hvilket er den samlede betaling.</span><span class="sxs-lookup"><span data-stu-id="ad292-204">If you perform the recalculation routine, the system will change the 1099 amount to be $1000.00, which is the total that was paid.</span></span>

<span data-ttu-id="ad292-205">[![Moms 1099-transaktioner: Efter kørsel af 1099-rutinen](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)</span><span class="sxs-lookup"><span data-stu-id="ad292-205">[![Tax 1099 transactions: After running the 1099 routine](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)</span></span>

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a><span data-ttu-id="ad292-206">Kreditor: 1099 – Opret 1099-posteringer manuelt</span><span class="sxs-lookup"><span data-stu-id="ad292-206">Accounts payable: 1099 – Manually create 1099 transactions</span></span>
<span data-ttu-id="ad292-207">Det kan være nødvendigt for en organisation at oprette 1099-transaktioner manuelt, der ikke har tilknyttet en faktura.</span><span class="sxs-lookup"><span data-stu-id="ad292-207">An organization might need to manually create 1099 transactions that aren't associated with an invoice.</span></span> <span data-ttu-id="ad292-208">Du kan tilføje manuelle 1099-posteringer til **Kreditor > Periodiske opgaver > Moms 1099 > Kreditorudligning for 1099**.</span><span class="sxs-lookup"><span data-stu-id="ad292-208">You can add manual 1099 transactions by going to **Accounts payable > Periodic tasks > Tax 1099 > Vendor settlement for 1099s**.</span></span> <span data-ttu-id="ad292-209">Vælg knappen **Manuelle 1099-transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="ad292-209">Select the **Manual 1099 transactions** button.</span></span> 

<span data-ttu-id="ad292-210">Manuelt oprettede 1099-posteringer opdateres ikke med processen **Opdater alle** eller processen til **Genberegn eksisterende 1099-beløb** i **Opdateringsværktøj til 1099**.</span><span class="sxs-lookup"><span data-stu-id="ad292-210">Manually created 1099 transactions are not updated with the **Update all** process or the **Recalculate existing 1099 amounts** process in the **Update 1099** utility.</span></span>

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a><span data-ttu-id="ad292-211">Kreditor: 1099 – Understøtter Dynamics 365 Finance 1096-formularen?</span><span class="sxs-lookup"><span data-stu-id="ad292-211">Accounts payable: 1099 – Does Dynamics 365 Finance support the 1096 form?</span></span> 

<span data-ttu-id="ad292-212">Dynamics 365 Finance udskriver ikke 1096 Annual Summary and Transmittal of US Information Returns-formlaren.</span><span class="sxs-lookup"><span data-stu-id="ad292-212">Dynamics 365 Finance doesn’t print the 1096 Annual Summary and Transmittal of US Information Returns form.</span></span>

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a><span data-ttu-id="ad292-213">Kreditor: 1099 – Findes der nye funktioner, der understøtter 1099-rapportering for den offentlige sektor?</span><span class="sxs-lookup"><span data-stu-id="ad292-213">Accounts payable: 1099 – Are there any new features that support 1099 reporting for Public sector?</span></span> 
<span data-ttu-id="ad292-214">Der er tilføjet en ny funktion til den offentlige sektor, **Opdater 1099-oplysninger efter hovedkonto**, som du kan aktivere i arbejdsområdet til **Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="ad292-214">A new Public sector feature, **Update 1099 information by main account**, has been added, which you can enable in the **Feature management** workspace.</span></span> <span data-ttu-id="ad292-215">Med denne funktion kan du tilknytte 1099-værdierne for en kreditor til hovedkontoen i regnskabsfordelingen og ikke standardkontoen i kreditorposten.</span><span class="sxs-lookup"><span data-stu-id="ad292-215">This feature lets you associate the 1099 values for a vendor by the main account in the accounting distribution, rather than the default account on the vendor record.</span></span>

<span data-ttu-id="ad292-216">Du kan finde flere oplysninger i [Konfigurere kreditorer til 1099-rapportering](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).</span><span class="sxs-lookup"><span data-stu-id="ad292-216">For more information, see [Set up vendors for 1099 reporting](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).</span></span>