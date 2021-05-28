---
title: Oversigt over indisk kildeskat (TDS – Tax Deducted at Source)
description: Dette emne indeholder detaljerede oplysninger om indisk kildeskat (TDS – Tax Deducted at Source) . Skattedokumentationen dækker denne funktion.
author: kailiang
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 28ee843036e11bd37b97a065ce53d2eb860c79d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023131"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a><span data-ttu-id="a2b54-104">Oversigt over indisk kildeskat (TDS – Tax Deducted at Source)</span><span class="sxs-lookup"><span data-stu-id="a2b54-104">Indian Tax Deducted at Source (TDS) overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2b54-105">Dette emne indeholder detaljerede oplysninger om indisk kildeskat (TDS – Tax Deducted at Source) .</span><span class="sxs-lookup"><span data-stu-id="a2b54-105">This topic provides detailed information about Indian Tax Deducted at Source (TDS).</span></span>

<span data-ttu-id="a2b54-106">Skattedokumentationen dækker denne funktion.</span><span class="sxs-lookup"><span data-stu-id="a2b54-106">The TDS documentation covers the functionality of this capability.</span></span> <span data-ttu-id="a2b54-107">Den forklarer også, hvordan du foretager den grundlæggende opsætning af kildeskat, beregner kildeskat for transaktioner, fuldfører skatteudligningsprocessen, registrerer skattecertifikatnumre og genererer skatteforespørgsler, skatteopgørelser og skattecertifikater.</span><span class="sxs-lookup"><span data-stu-id="a2b54-107">It also explains how to do the basic setup for TDS, calculate TDS on transactions, complete the TDS settlement process, record TDS certificate numbers, and generate TDS inquiries, TDS statements, and TDS certificates.</span></span> <span data-ttu-id="a2b54-108">Dokumentet dækker følgende emner:</span><span class="sxs-lookup"><span data-stu-id="a2b54-108">The documentation includes the following topics:</span></span>

- [<span data-ttu-id="a2b54-109">Grundlæggende opsætning for kildeskat</span><span class="sxs-lookup"><span data-stu-id="a2b54-109">Basic setup for TDS</span></span>](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [<span data-ttu-id="a2b54-110">Funktioner i formeldesigneren og for grænseværdi, som bruges til skatteberegning</span><span class="sxs-lookup"><span data-stu-id="a2b54-110">Formula designer and threshold limit functionality used for TDS calculation</span></span>](apac-ind-TDS-Formula-designer.md)
- [<span data-ttu-id="a2b54-111">Beregning af kildeskat for fakturaer, betalinger, egenveksler og interne transaktioner</span><span class="sxs-lookup"><span data-stu-id="a2b54-111">Calculation of TDS on invoices, payments, promissory notes, and intercompany transactions</span></span>](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [<span data-ttu-id="a2b54-112">Periodisk skatteudligningsproces og udligning af skattebeløb til kreditorer hos skattemyndigheder</span><span class="sxs-lookup"><span data-stu-id="a2b54-112">Periodic TDS settlement process and settlement of TDS amounts to TDS authority vendors</span></span>](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [<span data-ttu-id="a2b54-113">Registrere og opdatere skattecertifikatnumre og -datoer</span><span class="sxs-lookup"><span data-stu-id="a2b54-113">Recording and updating TDS certificate numbers and dates</span></span>](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a><span data-ttu-id="a2b54-114">Introduktion til kildeskat</span><span class="sxs-lookup"><span data-stu-id="a2b54-114">Introduction to TDS</span></span>

<span data-ttu-id="a2b54-115">I henhold til Skatteloven 1961 fratrækkes indkomstskatten ved kilden af modtageren af tjenesten på tidspunktet for forudbetaling eller bogføring af kreditten, alt efter hvad der indtræffer først.</span><span class="sxs-lookup"><span data-stu-id="a2b54-115">Per the Income tax Act, 1961, income tax is deducted at the source by the receiver of the service at the time of advance payment or accounting of credit, whichever occurs first.</span></span> <span data-ttu-id="a2b54-116">Den person, der foretager betalingen, skal trække skattebeløbet fra og kun betale nettosaldoen til udbyderen af tjenesten.</span><span class="sxs-lookup"><span data-stu-id="a2b54-116">The person who makes the payment must deduct the tax amount and pay only the net balance to the provider of the service.</span></span> <span data-ttu-id="a2b54-117">Kildeskat beregnes af tjenester, som myndighederne har specificeret, og skatten fratrækkes ud fra de satser, som myndighederne har specificeret for en periode.</span><span class="sxs-lookup"><span data-stu-id="a2b54-117">TDS is applied on services that the government specifies, and the tax is deducted by using the rates that the government specifies for a period.</span></span> <span data-ttu-id="a2b54-118">Fradragssatsen er baseret på status for den enhed, der modtager betalingen eller leverer tjenesten.</span><span class="sxs-lookup"><span data-stu-id="a2b54-118">The rate of deduction is based on the status of the entity that receives the payment or provides the service.</span></span> <span data-ttu-id="a2b54-119">Statusserne inkluderer **Individuelt**, **Indisk uopdelt familie** (**HUF**), **Virksomhed**, **Firma**, **Tilknytning af personer** (**AOP**), **Gruppe af enkeltpersoner** (**BOI**) og **Lokal myndighed**.</span><span class="sxs-lookup"><span data-stu-id="a2b54-119">Statuses include **Individual**, **Hindu Undivided Family** (**HUF**), **Company**, **Firm**, **Association of Persons** (**AOP**), **Body of Individuals** (**BOI**), and **Local authority**.</span></span>

<span data-ttu-id="a2b54-120">I følgende afsnit vises de tjenester, som kildeskat gælder for som angivet af den indiske regering.</span><span class="sxs-lookup"><span data-stu-id="a2b54-120">The following sections list the services that TDS is applied on, as specified by the Government of India.</span></span>

<span data-ttu-id="a2b54-121">**Hjemmehørende**</span><span class="sxs-lookup"><span data-stu-id="a2b54-121">**Residents**</span></span>

- <span data-ttu-id="a2b54-122">Lønindtægter (under afsnit 192)</span><span class="sxs-lookup"><span data-stu-id="a2b54-122">Income from salaries (Under section 192)</span></span>
- <span data-ttu-id="a2b54-123">Renteindtægter på værdipapirer (under afsnit 193)</span><span class="sxs-lookup"><span data-stu-id="a2b54-123">Income from interest on securities (Under section 193)</span></span>
- <span data-ttu-id="a2b54-124">Indtægter fra udbytte (under afsnit 194)</span><span class="sxs-lookup"><span data-stu-id="a2b54-124">Income from dividend (Under section 194)</span></span>
- <span data-ttu-id="a2b54-125">Renteindtægter (under afsnit 194A)</span><span class="sxs-lookup"><span data-stu-id="a2b54-125">Income from interest (Under section 194A)</span></span>
- <span data-ttu-id="a2b54-126">Indtægter fra lotterier eller konkurrencer (under afsnit 194B)</span><span class="sxs-lookup"><span data-stu-id="a2b54-126">Income from lotteries or puzzles (Under section 194B)</span></span>
- <span data-ttu-id="a2b54-127">Gevinster fra hestevæddeløb (under afsnit 194BB)</span><span class="sxs-lookup"><span data-stu-id="a2b54-127">Winning from horse races etc. (Under section 194BB)</span></span>
- <span data-ttu-id="a2b54-128">Kontrahenter og underleverandører (under afsnit 194C)</span><span class="sxs-lookup"><span data-stu-id="a2b54-128">Contractors and sub-contractors (Under section 194C)</span></span>
- <span data-ttu-id="a2b54-129">Forsikringserstatning (under afsnit 194D)</span><span class="sxs-lookup"><span data-stu-id="a2b54-129">Insurance commission (Under section 194D)</span></span>
- <span data-ttu-id="a2b54-130">Indtægter fra indbetalinger til national opsparingsordning (under afsnit 194EE)</span><span class="sxs-lookup"><span data-stu-id="a2b54-130">Income from deposit under national saving scheme (Under section 194EE)</span></span>
- <span data-ttu-id="a2b54-131">Indtægter fra fælles fond eller UTI (under afsnit 194F)</span><span class="sxs-lookup"><span data-stu-id="a2b54-131">Income from mutual fund or UTI (Under section 194F)</span></span>
- <span data-ttu-id="a2b54-132">Provision, vederlag, præmie osv ved salg eller handel (under afsnit 194G)</span><span class="sxs-lookup"><span data-stu-id="a2b54-132">Commission, Remuneration, Prize etc., on sale or lottery (Under section 194G)</span></span>
- <span data-ttu-id="a2b54-133">Betaling af provision eller kurtage (under afsnit 194H)</span><span class="sxs-lookup"><span data-stu-id="a2b54-133">Payment of Commission or brokerage (Under section 194H)</span></span>
- <span data-ttu-id="a2b54-134">Leje (under afsnit 194I)</span><span class="sxs-lookup"><span data-stu-id="a2b54-134">Rent (Under section 194I)</span></span>
- <span data-ttu-id="a2b54-135">Professionel tjeneste (under afsnit 194J)</span><span class="sxs-lookup"><span data-stu-id="a2b54-135">Professional service (Under section 194J)</span></span>
- <span data-ttu-id="a2b54-136">Indtægter fra enheder (under afsnit 194K)</span><span class="sxs-lookup"><span data-stu-id="a2b54-136">Income from Units (Under section 194K)</span></span>
- <span data-ttu-id="a2b54-137">Betaling af kompensation ved anskaffelse af bestemte former for immateriel ejendom (under afsnit 194LA)</span><span class="sxs-lookup"><span data-stu-id="a2b54-137">Payment of compensation on acquisition of certain immovable property (Under section 194LA)</span></span>

<span data-ttu-id="a2b54-138">**Ikke-hjemmehørende**</span><span class="sxs-lookup"><span data-stu-id="a2b54-138">**Non-residents**</span></span>

- <span data-ttu-id="a2b54-139">Betalinger til ikke-hjemmehørende sportsmænd eller dennes sportsorganisation (under afsnit 194E)</span><span class="sxs-lookup"><span data-stu-id="a2b54-139">Payments to Non-resident sportsmen or sports association (Under section 194E)</span></span>
- <span data-ttu-id="a2b54-140">Øvrige beløb (under afsnit 195)</span><span class="sxs-lookup"><span data-stu-id="a2b54-140">Other sums (Under section 195)</span></span>
- <span data-ttu-id="a2b54-141">Indtægter i forbindelse med enheder for ikke-hjemmehørende (under afsnit 196A)</span><span class="sxs-lookup"><span data-stu-id="a2b54-141">Income in respect of units of non-residents (Under section 196A)</span></span>

    - <span data-ttu-id="a2b54-142">Indtægter fra obligationer og aktier i udenlandsk valuta for indisk virksomhed (under afsnit 196C)</span><span class="sxs-lookup"><span data-stu-id="a2b54-142">Income from foreign currency bonds or shares of Indian Company (Under section 196C)</span></span>
    - <span data-ttu-id="a2b54-143">Indtægter fra værdipapirer for udenlandske investorer (under afsnit 196D)</span><span class="sxs-lookup"><span data-stu-id="a2b54-143">Incomes of foreign institutional investors from securities (Under section 196D)</span></span>
    - <span data-ttu-id="a2b54-144">Løn og alle andre positive indtægter under enhver type indtægt (afsnit 192)</span><span class="sxs-lookup"><span data-stu-id="a2b54-144">Salary and all other positive incomes under any head on income (Section 192)</span></span>
    - <span data-ttu-id="a2b54-145">Rente på værdipapirer (afsnit 193)</span><span class="sxs-lookup"><span data-stu-id="a2b54-145">Interest on securities (Section 193)</span></span>
    - <span data-ttu-id="a2b54-146">Anden rente end rente på værdipapirer (afsnit 194A)</span><span class="sxs-lookup"><span data-stu-id="a2b54-146">Interest other than interest on securities (Section 194A)</span></span>
    - <span data-ttu-id="a2b54-147">Betalinger til kontrahenter og underleverandører (afsnit 194C)</span><span class="sxs-lookup"><span data-stu-id="a2b54-147">Payments to contractors and sub-contractors (Section 194C)</span></span>
    - <span data-ttu-id="a2b54-148">Gevinster fra lotteri eller krydsord (afsnit 194B)</span><span class="sxs-lookup"><span data-stu-id="a2b54-148">Winnings from Lottery or crossword puzzles (Section 194B)</span></span>
    - <span data-ttu-id="a2b54-149">Gevinster fra hestevæddeløb (afsnit 194BB)</span><span class="sxs-lookup"><span data-stu-id="a2b54-149">Winnings from horse races (Section 194BB)</span></span>
    - <span data-ttu-id="a2b54-150">Forsikringsudbetaling, der dækker alle betalinger til anskaffelse af forsikring (afsnit 194D)</span><span class="sxs-lookup"><span data-stu-id="a2b54-150">Insurance Commission covering all payments for procuring Insurance business (Section 194D)</span></span>
    - <span data-ttu-id="a2b54-151">Enhver rente, der ikke er rente på værdipapirer, der tilfalder ikke-hjemmehørende, som ikke er en virksomhed eller en udenlandsk virksomhed (afsnit 195)</span><span class="sxs-lookup"><span data-stu-id="a2b54-151">Any interest other than interest on securities payable to non-residents not being a company or to a foreign company (Section 195)</span></span>
    - <span data-ttu-id="a2b54-152">Betaling til ikke-hjemmehørende sportsmand, herunder atletik- eller sportsforeninger eller -institutioner.</span><span class="sxs-lookup"><span data-stu-id="a2b54-152">Payment to non-resident sportsman including athlete or sports association or institution.</span></span> <span data-ttu-id="a2b54-153">I tilfælde af en ikke-hjemmehørende sportsmand, betalinger for annoncer samt artikler om spil/sport i indien i aviser, magasiner osv.</span><span class="sxs-lookup"><span data-stu-id="a2b54-153">In case of non-resident sportsman, payments in respect of advertisements as well as articles on any game/sports in India in newspapers, magazines, and so.</span></span> <span data-ttu-id="a2b54-154">er inkluderet (afsnit 194E)</span><span class="sxs-lookup"><span data-stu-id="a2b54-154">is included (Section 194E)</span></span>
    - <span data-ttu-id="a2b54-155">Betaling i forbindelse med indbetalinger under NSS \[National Savings Scheme\] (afsnit 194EE)</span><span class="sxs-lookup"><span data-stu-id="a2b54-155">Payment in respect of deposits under NSS \[National Savings Scheme\] (Section 194EE)</span></span>
    - <span data-ttu-id="a2b54-156">Betaling på grund af tilbagekøb af enheder af fælles fond eller UTI (Section 194F)</span><span class="sxs-lookup"><span data-stu-id="a2b54-156">Payment on account of repurchase of Units by Mutual Fund or UTI (Section 194F)</span></span>
    - <span data-ttu-id="a2b54-157">Betaling for provision eller kurtage (afsnit 194H)</span><span class="sxs-lookup"><span data-stu-id="a2b54-157">Payment for Commission or brokerage (Section 194H)</span></span>
    - <span data-ttu-id="a2b54-158">Betaling af leje (afsnit 194I)</span><span class="sxs-lookup"><span data-stu-id="a2b54-158">Payment of rent (Section 194I)</span></span>
    - <span data-ttu-id="a2b54-159">Betaling af gebyrer for professionelle eller tekniske tjenester (afsnit 194J)</span><span class="sxs-lookup"><span data-stu-id="a2b54-159">Payment of fees for professional or technical services (Section 194J)</span></span>
    - <span data-ttu-id="a2b54-160">Provision til lagerførere, distributører, indkøbere og sælgere af lotteribilletter, herunder vederlag eller præmie for sådanne kuponer (afsnit 194G)</span><span class="sxs-lookup"><span data-stu-id="a2b54-160">Commission to Stockiest, distributors, buyers and sellers of Lottery tickets including remuneration or prize on such tickets (Section 194G)</span></span>
    - <span data-ttu-id="a2b54-161">Indtægt fra enheder, der er købt i fremmed valuta eller langsigtet kapitalgevinst som følge af overførsel af sådanne enheder, der er købt i fremmed valuta (afsnit 196B)</span><span class="sxs-lookup"><span data-stu-id="a2b54-161">Income from Units purchased in foreign currency or long-term capital gain arising from the transfer of such Units purchased in foreign currency (Section 196B)</span></span>
    - <span data-ttu-id="a2b54-162">Betaling af indtægt til ikke-hjemmehørende i forbindelse med renter eller udbytte på obligationer og aktier (afsnit 196C)</span><span class="sxs-lookup"><span data-stu-id="a2b54-162">Payment of any income to non-residents in respect of interest or dividend on bonds and shares (Section 196C)</span></span>

<span data-ttu-id="a2b54-163">Kildeskatten beregnes på indkøb, salg, salgsreturneringer, kreditnotaer, anskaffelse af anlægsaktiver, forudbetalinger, forudbetalinger, egenveksler, arbejde og interne transaktioner.</span><span class="sxs-lookup"><span data-stu-id="a2b54-163">TDS is calculated on purchases, sales, sales returns, credit notes, fixed asset acquisitions, prepayments, advance payments, promissory notes, works tax, and intercompany transactions.</span></span>

> [!NOTE]
> <span data-ttu-id="a2b54-164">I det aktuelle indiske skattescenarie beregner kildeskat ikke for salgstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="a2b54-164">In the current Indian tax scenario, TDS isn't calculated on sales transactions.</span></span> <span data-ttu-id="a2b54-165">Systemet inkluderer mulighed for at beregne skatterefusion for salgstransaktioner, især for interne transaktioner.</span><span class="sxs-lookup"><span data-stu-id="a2b54-165">However, the system includes a provision to calculate TDS recoverable on sales transactions, especially for intercompany transactions.</span></span>

<span data-ttu-id="a2b54-166">Beregningen af kildeskat tager altid højde for den grænseværdi og tærskel for fritagelse, der er defineret for skattekomponenten.</span><span class="sxs-lookup"><span data-stu-id="a2b54-166">The calculation of TDS always considers the threshold and the exception threshold that are defined for the TDS component.</span></span>

<span data-ttu-id="a2b54-167">Den periodiske skatteudligningsproces skal køres, og skattebetalingerne skal udlignes med skattemyndighedskreditorer.</span><span class="sxs-lookup"><span data-stu-id="a2b54-167">The periodic TDS settlement process must be run, and the TDS payments must be settled to TDS authority vendors.</span></span>

<span data-ttu-id="a2b54-168">Certifikatnumrene og -datoerne for skattecertifikater, der modtages fra kreditorer eller debitorer, kan registreres og opdateres.</span><span class="sxs-lookup"><span data-stu-id="a2b54-168">The certificate numbers and dates for TDS certificates that are received from vendors or customers can be recorded and updated.</span></span> <span data-ttu-id="a2b54-169">Desuden kan kvartalsopgørelser for Formular 26Q og Formular 27Q samt Formular 16A-certifikatet for kildeskat genereres i Finans.</span><span class="sxs-lookup"><span data-stu-id="a2b54-169">Additionally, Form 26Q and Form 27Q quarterly statements, and the Form 16A certificate for TDS, can be generated in Finance.</span></span>

## <a name="setting-up-and-working-with-tds"></a><span data-ttu-id="a2b54-170">Opsætte og arbejde med kildeskat</span><span class="sxs-lookup"><span data-stu-id="a2b54-170">Setting up and working with TDS</span></span>

<span data-ttu-id="a2b54-171">Her er en oversigt over processen for opsætning af og arbejde med kildeskat:</span><span class="sxs-lookup"><span data-stu-id="a2b54-171">Here is an overview of the process for setting up and working with TDS:</span></span>

1. <span data-ttu-id="a2b54-172">**Opsætning af kildeskat:**</span><span class="sxs-lookup"><span data-stu-id="a2b54-172">**TDS setup:**</span></span>

    - <span data-ttu-id="a2b54-173">Opsætning af parametre:</span><span class="sxs-lookup"><span data-stu-id="a2b54-173">Parameter setup:</span></span>

        - <span data-ttu-id="a2b54-174">I Finansparametre skal du aktivere de parametre, der er relateret til kildeskat.</span><span class="sxs-lookup"><span data-stu-id="a2b54-174">In General ledger parameters, activate parameters that are related to TDS.</span></span>
        - <span data-ttu-id="a2b54-175">Angiv nummerserien for betalinger af A-skat i Finansparametre.</span><span class="sxs-lookup"><span data-stu-id="a2b54-175">In General ledger parameters, set up the number sequence for withholding tax payments.</span></span>
        - <span data-ttu-id="a2b54-176">Angiv parametre i Kreditor og Debitor.</span><span class="sxs-lookup"><span data-stu-id="a2b54-176">Set up parameters in Accounts payable and Accounts receivable.</span></span>

    - <span data-ttu-id="a2b54-177">Grundlæggende opsætning:</span><span class="sxs-lookup"><span data-stu-id="a2b54-177">Basic setup:</span></span>

        - <span data-ttu-id="a2b54-178">Angiv skatteregistreringsnumre for en virksomhed, debitorer og kreditorer.</span><span class="sxs-lookup"><span data-stu-id="a2b54-178">Set up TDS registration numbers for a company, customers, and vendors.</span></span>
        - <span data-ttu-id="a2b54-179">Konfigurer skattekomponentgrupper.</span><span class="sxs-lookup"><span data-stu-id="a2b54-179">Set up TDS component groups.</span></span>
        - <span data-ttu-id="a2b54-180">Konfigurer skattekomponenter, knyt skattekomponentgrupper til dem, og definer grænseværdien og tærsklen for fritagelse for dem.</span><span class="sxs-lookup"><span data-stu-id="a2b54-180">Set up TDS components, attach TDS component groups to them, and define the threshold and exception threshold for them.</span></span>
        - <span data-ttu-id="a2b54-181">Angiv skattemyndigheder.</span><span class="sxs-lookup"><span data-stu-id="a2b54-181">Set up TDS authorities.</span></span>
        - <span data-ttu-id="a2b54-182">Angiv skatteudligningsperioder.</span><span class="sxs-lookup"><span data-stu-id="a2b54-182">Set up TDS settlement periods.</span></span>
        - <span data-ttu-id="a2b54-183">Angiv kildeskattekoder, og knyt skattekomponenter til dem.</span><span class="sxs-lookup"><span data-stu-id="a2b54-183">Set up TDS tax codes, and attach TDS components to them.</span></span>
        - <span data-ttu-id="a2b54-184">Angiv kildeskattegrupper, og knyt kildeskattekoder til dem.</span><span class="sxs-lookup"><span data-stu-id="a2b54-184">Set up TDS tax groups, and attach TDS tax codes to them.</span></span>
        - <span data-ttu-id="a2b54-185">I formeldesigneren skal du definere en formel for at beregne kildeskat for en kildeskattegruppe.</span><span class="sxs-lookup"><span data-stu-id="a2b54-185">In the formula designer, define a formula to calculate TDS for a TDS group.</span></span>
        - <span data-ttu-id="a2b54-186">Registrer certifikatnumre for skattekoncession.</span><span class="sxs-lookup"><span data-stu-id="a2b54-186">Record TDS concession certificate numbers.</span></span>

    - <span data-ttu-id="a2b54-187">Opsætning af finanskonti og virksomheder:</span><span class="sxs-lookup"><span data-stu-id="a2b54-187">Ledger accounts and company setup:</span></span>

        - <span data-ttu-id="a2b54-188">Konfigurere finanskonti for kildeskat i forhold til kreditorer og debitorer.</span><span class="sxs-lookup"><span data-stu-id="a2b54-188">Set up TDS payable and receivable ledger accounts.</span></span>
        - <span data-ttu-id="a2b54-189">Angiv et kontonummer for skattefradrag og -opkrævning (ITRA) og en fradragskategori for virksomheden.</span><span class="sxs-lookup"><span data-stu-id="a2b54-189">Set up a Tax Deduction and Collection Account Number (TAN) and a deductor type category for the company.</span></span>

    - <span data-ttu-id="a2b54-190">Anden opsætning:</span><span class="sxs-lookup"><span data-stu-id="a2b54-190">Other setup:</span></span>

        - <span data-ttu-id="a2b54-191">Konfigurer en betalingsplan, der omfatter skattefordeling.</span><span class="sxs-lookup"><span data-stu-id="a2b54-191">Set up a payment schedule that includes TDS allocation.</span></span>
        - <span data-ttu-id="a2b54-192">Angiv en betalingsgebyrtype for betalinger til skattemyndighed.</span><span class="sxs-lookup"><span data-stu-id="a2b54-192">Set up a payment fee type for payments to the TDS authority.</span></span>
        - <span data-ttu-id="a2b54-193">Konfigurer oplysninger om kildeskattegrupper, permanente kontonumre (PAN – Permanent Account Number) og skattekontonumre for kreditorer og debitorer.</span><span class="sxs-lookup"><span data-stu-id="a2b54-193">Set up information about TDS groups, permanent account numbers (PANs), and TANs for vendors and customers.</span></span>

2. <span data-ttu-id="a2b54-194">**Beregning af kildeskat i transaktioner:**</span><span class="sxs-lookup"><span data-stu-id="a2b54-194">**Calculation of TDS in transactions:**</span></span>

    - <span data-ttu-id="a2b54-195">Fakturaer og betalinger</span><span class="sxs-lookup"><span data-stu-id="a2b54-195">Invoices and payments</span></span>
    - <span data-ttu-id="a2b54-196">Egenveksler</span><span class="sxs-lookup"><span data-stu-id="a2b54-196">Promissory notes</span></span>
    - <span data-ttu-id="a2b54-197">Forudbetalinger</span><span class="sxs-lookup"><span data-stu-id="a2b54-197">Advance payments</span></span>
    - <span data-ttu-id="a2b54-198">Forudbetalinger</span><span class="sxs-lookup"><span data-stu-id="a2b54-198">Prepayments</span></span>

3. <span data-ttu-id="a2b54-199">**Skatteudligning:**</span><span class="sxs-lookup"><span data-stu-id="a2b54-199">**TDS settlement:**</span></span>

    - <span data-ttu-id="a2b54-200">Periodisk skatteudligningsproces</span><span class="sxs-lookup"><span data-stu-id="a2b54-200">Periodic TDS settlement process</span></span>
    - <span data-ttu-id="a2b54-201">Udligning af skattebetalinger til skattemyndighedskreditorer og generering af skatteopgørelse</span><span class="sxs-lookup"><span data-stu-id="a2b54-201">Settlement of TDS payments to TDS authority vendors and generation of TDS challan</span></span>

4. <span data-ttu-id="a2b54-202">**Skatteforespørgsler, -opgørelser og -certifikat:**</span><span class="sxs-lookup"><span data-stu-id="a2b54-202">**TDS inquiries, statements, and certificate:**</span></span>

    - <span data-ttu-id="a2b54-203">Registrer og opdater skattecertifikatnumre og -datoer.</span><span class="sxs-lookup"><span data-stu-id="a2b54-203">Record and update TDS certificate numbers and dates.</span></span>
    - <span data-ttu-id="a2b54-204">Generer en skatteforespørgsel og en bogført skatteforespørgsel.</span><span class="sxs-lookup"><span data-stu-id="a2b54-204">Generate a TDS inquiry and a posted TDS inquiry.</span></span>
    - <span data-ttu-id="a2b54-205">Generer Formular 27A, Formular 26Q og Formular 27Q for kildeskat og elektroniske kvartalsopgørelser af kildeskat.</span><span class="sxs-lookup"><span data-stu-id="a2b54-205">Generate Form 27A, Form 26Q, and Form 27Q TDS and e-TDS quarterly statements.</span></span>
    - <span data-ttu-id="a2b54-206">Generer et skattecerfikat for Formular 16A.</span><span class="sxs-lookup"><span data-stu-id="a2b54-206">Generate a Form 16A TDS certificate.</span></span>
