---
title: Konfigurer udgiftsstyring
description: "I denne artikel beskrives de overvejelser og de beslutninger, du skal foretage i planlægningsprocessen, før du konfigurerer Udgiftsstyring i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4fad62c5da11e88e07f4e9d4343c4ac1a487bdd8
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="configure-expense-management"></a><span data-ttu-id="f16b8-103">Konfigurer udgiftsstyring</span><span class="sxs-lookup"><span data-stu-id="f16b8-103">Configure expense management</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f16b8-104">I denne emne beskrives de overvejelser og de beslutninger, du skal foretage i planlægningsprocessen, før du konfigurerer Udgiftsstyring i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="f16b8-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="f16b8-105">Du kan gemme oplysninger om bl.a betalingsmetoderne, rejserekvisitioner, udgiftsrapporter og politikker i området Udgiftsstyring.</span><span class="sxs-lookup"><span data-stu-id="f16b8-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="f16b8-106">Da mange af de beslutninger, du foretager, når du planlægger din konfiguration for udgiftsstyring, er baseret på organisationens hierarki og økonomiske struktur, skal du referere til planlægningsdokumenterne for de pågældende områder.</span><span class="sxs-lookup"><span data-stu-id="f16b8-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="f16b8-107">Interne udgifter</span><span class="sxs-lookup"><span data-stu-id="f16b8-107">Intercompany expenses</span></span>

<span data-ttu-id="f16b8-108">Når du aktiverer interne udgifter, giver du juridiske enheder og medarbejdere mulighed for at pådrage dig udgifter på vegne af en anden juridisk enhed og opkræve betaling fra den juridiske enhed med ansættelsen i organisationen.</span><span class="sxs-lookup"><span data-stu-id="f16b8-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="f16b8-109">En medarbejder i juridisk enhed A fuldfører f.eks. et projekt for juridisk enhed B, og projektet indebærer rejserelaterede udgifter.</span><span class="sxs-lookup"><span data-stu-id="f16b8-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="f16b8-110">Hvis interne udgifter er aktiveret, kan medarbejderen derefter indsende en udgiftsrapport, der bogfører udgiften til juridisk enhed B, og udgiften skal derefter betales af juridisk enhed A. Hvis organisationen ikke har flere juridiske enheder, behøver du ikke at aktivere interne udgifter.</span><span class="sxs-lookup"><span data-stu-id="f16b8-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="f16b8-111">**Beslutning:** Vil du aktivere interne udgifter?</span><span class="sxs-lookup"><span data-stu-id="f16b8-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="f16b8-112">Økonomistyring</span><span class="sxs-lookup"><span data-stu-id="f16b8-112">Financial management</span></span>

<span data-ttu-id="f16b8-113">Udgiftsstyring er tæt integreret med den finansielle forvaltning af organisationen.</span><span class="sxs-lookup"><span data-stu-id="f16b8-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="f16b8-114">Mange af konfigurationerne for udgiftsstyring baseres på de beslutninger, du har foretaget om virksomhedens økonomi.</span><span class="sxs-lookup"><span data-stu-id="f16b8-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="f16b8-115">I følgende afsnit beskrives de forskellige områder, der kræver planlægning og beslutninger, der er baseret på organisationens finansielle beslutninger og vejledning fra ledelsen.</span><span class="sxs-lookup"><span data-stu-id="f16b8-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="f16b8-116">Diæter</span><span class="sxs-lookup"><span data-stu-id="f16b8-116">Per diems</span></span>

<span data-ttu-id="f16b8-117">Du skal definere medarbejderen pr. diæt, som organisationen stiller til rådighed.</span><span class="sxs-lookup"><span data-stu-id="f16b8-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="f16b8-118">Da diæter normalt bruges til at dække udgifter som måltider, logi og andre omkostninger, kan du oprette regler for diætgodtgørelser, som organisationen tilbyder.</span><span class="sxs-lookup"><span data-stu-id="f16b8-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="f16b8-119">Diætsatser kan baseres på tidspunktet på året, rejselokationen eller begge.</span><span class="sxs-lookup"><span data-stu-id="f16b8-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="f16b8-120">Når du definerer en diætregel, kan du angive, at du vil tilbageholde en procentdel af en diætsats, hvis en arbejder modtager ekstra måltider eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="f16b8-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="f16b8-121">Du kan også definere diætsatsniveauer for at angive et minimum- og maksimumantal timer, en diætsats kan gælde for en arbejders rejse.</span><span class="sxs-lookup"><span data-stu-id="f16b8-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="f16b8-122">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="f16b8-122">**Decisions:**</span></span>

- <span data-ttu-id="f16b8-123">Standarddiætregler for første og sidste dag:</span><span class="sxs-lookup"><span data-stu-id="f16b8-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="f16b8-124">Hvad er det mindste antal timer, en medarbejder kan gøre krav på for en dag og stadig få en diæt?</span><span class="sxs-lookup"><span data-stu-id="f16b8-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="f16b8-125">Er der en reduktion af det beløb, der tilbydes for måltider for den første og sidste dag?</span><span class="sxs-lookup"><span data-stu-id="f16b8-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="f16b8-126">Hvis der er en reduktion af, hvad er procentdelen for reduktionen?</span><span class="sxs-lookup"><span data-stu-id="f16b8-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="f16b8-127">Er der en reduktion af det beløb, der tilbydes for et hotel for den første og sidste dag?</span><span class="sxs-lookup"><span data-stu-id="f16b8-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="f16b8-128">Hvis der er en reduktion af, hvad er procentdelen for reduktionen?</span><span class="sxs-lookup"><span data-stu-id="f16b8-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="f16b8-129">Er der en reduktion af det beløb, der tilbydes for andre udgifter, der påløber den første og sidste dag?</span><span class="sxs-lookup"><span data-stu-id="f16b8-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="f16b8-130">Hvis der er en reduktion af, hvad er procentdelen for reduktionen?</span><span class="sxs-lookup"><span data-stu-id="f16b8-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="f16b8-131">Standarddiætregler:</span><span class="sxs-lookup"><span data-stu-id="f16b8-131">Default per diem rules:</span></span>

    - <span data-ttu-id="f16b8-132">Er der en procentvis reduktion i diætgodtgørelsen til hvert måltid, hvis for eksempel måltidet er gratis?</span><span class="sxs-lookup"><span data-stu-id="f16b8-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="f16b8-133">Hvis der er en reduktion af, hvad er procentdelen for reduktion for hvert måltid?</span><span class="sxs-lookup"><span data-stu-id="f16b8-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="f16b8-134">Beregnes nedsættelsen for måltider pr. dag, pr. rejse eller med antallet af måltider pr. dag?</span><span class="sxs-lookup"><span data-stu-id="f16b8-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="f16b8-135">Skal diætbeløb afrundes på almindelig måde eller rundes op?</span><span class="sxs-lookup"><span data-stu-id="f16b8-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="f16b8-136">Bliver diæter beregnet baseret på en 24-timers periode eller en kalenderdag?</span><span class="sxs-lookup"><span data-stu-id="f16b8-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="f16b8-137">Diætregler, der er baseret på lokalitet:</span><span class="sxs-lookup"><span data-stu-id="f16b8-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="f16b8-138">Varierer diætsatser efter lokalitet?</span><span class="sxs-lookup"><span data-stu-id="f16b8-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="f16b8-139">Hvilke lokalitet medtages?</span><span class="sxs-lookup"><span data-stu-id="f16b8-139">What locations are included?</span></span>
    - <span data-ttu-id="f16b8-140">Hvis diætsatser varierer i henhold til lokalitet, hvilken procentdel af beløbet tilbydes så for hver lokalitet for følgende typer udgifter:</span><span class="sxs-lookup"><span data-stu-id="f16b8-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="f16b8-141">Måltider</span><span class="sxs-lookup"><span data-stu-id="f16b8-141">Meals</span></span>
        - <span data-ttu-id="f16b8-142">Hotel</span><span class="sxs-lookup"><span data-stu-id="f16b8-142">Hotel</span></span>
        - <span data-ttu-id="f16b8-143">Øvrige udgifter</span><span class="sxs-lookup"><span data-stu-id="f16b8-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="f16b8-144">Administration af udgiftskladder og konti</span><span class="sxs-lookup"><span data-stu-id="f16b8-144">Expense management journals and accounts</span></span>

<span data-ttu-id="f16b8-145">Udgiftsstyring kræver, at du bruger flere kladder og konti.</span><span class="sxs-lookup"><span data-stu-id="f16b8-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="f16b8-146">For eksempel skal du beslutte, om den samme konto bruges til kontantforskud og tvister om kreditkort.</span><span class="sxs-lookup"><span data-stu-id="f16b8-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="f16b8-147">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="f16b8-147">**Decisions:**</span></span>

- <span data-ttu-id="f16b8-148">Hvilken finanskladde skal godkendte udgiftsrapporter bogføres til?</span><span class="sxs-lookup"><span data-stu-id="f16b8-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="f16b8-149">Hvilken konto bruges der til kontantforskud?</span><span class="sxs-lookup"><span data-stu-id="f16b8-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="f16b8-150">Skal kontantforskud bogføres med det samme?</span><span class="sxs-lookup"><span data-stu-id="f16b8-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="f16b8-151">Betalingsmetoder</span><span class="sxs-lookup"><span data-stu-id="f16b8-151">Payment methods</span></span>

<span data-ttu-id="f16b8-152">Når du tillader medarbejdere at pådrage dig udgifter på vegne af din virksomhed, skal du definere de betalingsmetoder, medarbejdere har tilladelse til at bruge.</span><span class="sxs-lookup"><span data-stu-id="f16b8-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="f16b8-153">For eksempel kan du tillade medarbejdere at bruge penge eller firmaets kreditkort.</span><span class="sxs-lookup"><span data-stu-id="f16b8-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="f16b8-154">Du kan også tillade medarbejdere at bruge personlige kreditkort og derefter refundere medarbejderne.</span><span class="sxs-lookup"><span data-stu-id="f16b8-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="f16b8-155">Du skal træffe følgende beslutninger for hver betalingsmetode, du tillader.</span><span class="sxs-lookup"><span data-stu-id="f16b8-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="f16b8-156">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="f16b8-156">**Decisions:**</span></span>

- <span data-ttu-id="f16b8-157">Hvile betalingsmetoder er tilladte?</span><span class="sxs-lookup"><span data-stu-id="f16b8-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="f16b8-158">Hvem ejer udgifterne til betalingsmetoden?</span><span class="sxs-lookup"><span data-stu-id="f16b8-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="f16b8-159">Er der en modkontotype?</span><span class="sxs-lookup"><span data-stu-id="f16b8-159">Is there an offset account type?</span></span> <span data-ttu-id="f16b8-160">Hvis der findes en modkontotype, hvad er den?</span><span class="sxs-lookup"><span data-stu-id="f16b8-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="f16b8-161">Hvis der findes en modkonto, hvad er kontoen?</span><span class="sxs-lookup"><span data-stu-id="f16b8-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="f16b8-162">Hvis betalingsmetoden er et kreditkort, skal betalingsmetoden så kun bruges ved importerede transaktioner?</span><span class="sxs-lookup"><span data-stu-id="f16b8-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="f16b8-163">Udgiftskategorier og delte kategorier</span><span class="sxs-lookup"><span data-stu-id="f16b8-163">Expense categories and shared categories</span></span>

<span data-ttu-id="f16b8-164">Når medarbejderne opretter en udgiftsrapport, skal hver udgift, de registrerer, knyttes til en udgiftskategori.</span><span class="sxs-lookup"><span data-stu-id="f16b8-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="f16b8-165">Udgiftskategorier stammer fra delte kategorier, der kan deles på tværs af de juridiske enheder i organisationen.</span><span class="sxs-lookup"><span data-stu-id="f16b8-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="f16b8-166">Disse kategorier kan også deles i Projektstyring og regnskab, afhængigt af den måde organisationen er defineret på.</span><span class="sxs-lookup"><span data-stu-id="f16b8-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="f16b8-167">Baseret på definitionen af organisationen og vejledning fra implementeringsgruppen skal du afgøre, om de kategorier, der bruges i udgiftsstyring, kun skal bruges i udgiftsstyring, eller om de skal deles mellem projektstyring og regnskab og udgiftsstyring.</span><span class="sxs-lookup"><span data-stu-id="f16b8-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="f16b8-168">Bemærk, at disse kategorier kan deles mellem projekt og udgift eller projekt og produktion, men ikke mellem udgift og produktion.</span><span class="sxs-lookup"><span data-stu-id="f16b8-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="f16b8-169">Du skal træffe følgende beslutninger for hver udgiftskategori.</span><span class="sxs-lookup"><span data-stu-id="f16b8-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="f16b8-170">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="f16b8-170">**Decisions:**</span></span>

- <span data-ttu-id="f16b8-171">Hvad er udgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="f16b8-171">What is the expense category?</span></span> <span data-ttu-id="f16b8-172">Eksemplerne omfatter kategorier for flyvninger, hotel eller kørsel.</span><span class="sxs-lookup"><span data-stu-id="f16b8-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="f16b8-173">Kan udgiftskategorien også bruges i projektstyring og regnskab?</span><span class="sxs-lookup"><span data-stu-id="f16b8-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="f16b8-174">Hvad er udgiftstypen?</span><span class="sxs-lookup"><span data-stu-id="f16b8-174">What is the expense type?</span></span>
- <span data-ttu-id="f16b8-175">Hvad er standardbetalingsmetoden for udgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="f16b8-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="f16b8-176">Skal udgifter i udgiftskategorien specificeres?</span><span class="sxs-lookup"><span data-stu-id="f16b8-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="f16b8-177">Hvad er standardhovedkontoen for udgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="f16b8-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="f16b8-178">Hvad er standardvaremomsgruppen for udgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="f16b8-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="f16b8-179">Er yderligere betalingsmetoder tilladt for denne udgiftskategori?</span><span class="sxs-lookup"><span data-stu-id="f16b8-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="f16b8-180">Hvis flere betalingsmetoder er tilladt, hvilke er der så tale om?</span><span class="sxs-lookup"><span data-stu-id="f16b8-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="f16b8-181">Er der underkategorier i denne udgiftskategori?</span><span class="sxs-lookup"><span data-stu-id="f16b8-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="f16b8-182">Hvis der er underkategorier, skal du også foretage følgende beslutninger:</span><span class="sxs-lookup"><span data-stu-id="f16b8-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="f16b8-183">Er der nogen af de underkategorier, der er udelukket fra momsopkrævning?</span><span class="sxs-lookup"><span data-stu-id="f16b8-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="f16b8-184">Hvad er varemomsgruppen for underkategorierne?</span><span class="sxs-lookup"><span data-stu-id="f16b8-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="f16b8-185">Hvis udgiftskategorien også anvendes i projektstyring og regnskab, skal du svare på de resterende spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="f16b8-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="f16b8-186">Ellers gå videre til næste afsnit.</span><span class="sxs-lookup"><span data-stu-id="f16b8-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="f16b8-187">Hvilke omkostningskonti skal der bruges til følgende udgifter?</span><span class="sxs-lookup"><span data-stu-id="f16b8-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="f16b8-188">Kost</span><span class="sxs-lookup"><span data-stu-id="f16b8-188">Cost</span></span>
    - <span data-ttu-id="f16b8-189">Lønfordeling</span><span class="sxs-lookup"><span data-stu-id="f16b8-189">Payroll allocation</span></span>
    - <span data-ttu-id="f16b8-190">IGVF - kostværdi</span><span class="sxs-lookup"><span data-stu-id="f16b8-190">WIP-cost value</span></span>
    - <span data-ttu-id="f16b8-191">Omkostning-vare</span><span class="sxs-lookup"><span data-stu-id="f16b8-191">Cost-item</span></span>
    - <span data-ttu-id="f16b8-192">IGVF - kostværdi - vare</span><span class="sxs-lookup"><span data-stu-id="f16b8-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="f16b8-193">Periodiseret tab</span><span class="sxs-lookup"><span data-stu-id="f16b8-193">Accrued loss</span></span>
    - <span data-ttu-id="f16b8-194">IGVF - periodiseret tab</span><span class="sxs-lookup"><span data-stu-id="f16b8-194">WIP-accrued loss</span></span>

- <span data-ttu-id="f16b8-195">Hvilke indtægtskonti skal der bruges til følgende?</span><span class="sxs-lookup"><span data-stu-id="f16b8-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="f16b8-196">Faktureret omsætning</span><span class="sxs-lookup"><span data-stu-id="f16b8-196">Invoiced revenue</span></span>
    - <span data-ttu-id="f16b8-197">Periodiseret omsætning – Salgsværdi</span><span class="sxs-lookup"><span data-stu-id="f16b8-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="f16b8-198">IGVF - salgsværdi</span><span class="sxs-lookup"><span data-stu-id="f16b8-198">WIP-sales value</span></span>
    - <span data-ttu-id="f16b8-199">Periodiseret omsætning – produktion</span><span class="sxs-lookup"><span data-stu-id="f16b8-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="f16b8-200">IGVA – produktion</span><span class="sxs-lookup"><span data-stu-id="f16b8-200">WIP-production</span></span>
    - <span data-ttu-id="f16b8-201">Periodiseret omsætning – profit</span><span class="sxs-lookup"><span data-stu-id="f16b8-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="f16b8-202">IGVA - profit</span><span class="sxs-lookup"><span data-stu-id="f16b8-202">WIP-profit</span></span>
    - <span data-ttu-id="f16b8-203">Periodiseret omsætning – abonnement</span><span class="sxs-lookup"><span data-stu-id="f16b8-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="f16b8-204">IGVF - Abonnement</span><span class="sxs-lookup"><span data-stu-id="f16b8-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="f16b8-205">Afgifter</span><span class="sxs-lookup"><span data-stu-id="f16b8-205">Taxes</span></span>

<span data-ttu-id="f16b8-206">For udgiftsrelateret moms skal du bestemme, hvad der er inkluderet eller aktiveret i udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="f16b8-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="f16b8-207">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="f16b8-207">**Decisions:**</span></span>

- <span data-ttu-id="f16b8-208">Indgår der moms i udgiftsbeløbet?</span><span class="sxs-lookup"><span data-stu-id="f16b8-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="f16b8-209">Skal momsopkrævning være aktiveret på udgifter?</span><span class="sxs-lookup"><span data-stu-id="f16b8-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="f16b8-210">Når du havde planlagt finans, kan du ikke aktivere momsopkrævning på udgifter, hvis du har besluttet at anvende amerikanske regler for moms og importmoms.</span><span class="sxs-lookup"><span data-stu-id="f16b8-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="f16b8-211">(For at anvende regler for amerikansk moms og importmoms, skal du angive indstillingen **Anvend reglerne for moms** til **Ja**).</span><span class="sxs-lookup"><span data-stu-id="f16b8-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="f16b8-212">Politikker</span><span class="sxs-lookup"><span data-stu-id="f16b8-212">Policies</span></span>

<span data-ttu-id="f16b8-213">Når du oprettet udgiftsrapportpolitikker, kan din virksomhed spare tid og penge, når medarbejderne pådrager virksomheden udgifter på dens vegne.</span><span class="sxs-lookup"><span data-stu-id="f16b8-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="f16b8-214">Politikker sikrer, at medarbejderne holder sig inden for budgettet, angiver alle nødvendige oplysninger og kun bruger penge, når der er behov for det.</span><span class="sxs-lookup"><span data-stu-id="f16b8-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="f16b8-215">Du skal træffe følgende beslutninger for hver udgiftsrapportpolitik og hver udgiftsrapportgodkendelsespolitik, du opretter.</span><span class="sxs-lookup"><span data-stu-id="f16b8-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="f16b8-216">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="f16b8-216">**Decisions:**</span></span>

- <span data-ttu-id="f16b8-217">Hvad er navnet på politikken?</span><span class="sxs-lookup"><span data-stu-id="f16b8-217">What is the name of the policy?</span></span>
- <span data-ttu-id="f16b8-218">Hvad er udgiftspolitikken til?</span><span class="sxs-lookup"><span data-stu-id="f16b8-218">What is the expense policy for?</span></span>
- <span data-ttu-id="f16b8-219">Hvis du tidligere har besluttet at aktivere interne udgifter, for hvilke virksomheder i organisationen skal denne politik anvendes?</span><span class="sxs-lookup"><span data-stu-id="f16b8-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="f16b8-220">Hvornår vil politikken være gældende?</span><span class="sxs-lookup"><span data-stu-id="f16b8-220">When does the policy become effective?</span></span>
- <span data-ttu-id="f16b8-221">Hvornår udløber politikken?</span><span class="sxs-lookup"><span data-stu-id="f16b8-221">When does the policy expire?</span></span>
- <span data-ttu-id="f16b8-222">Hvad er politikreglen?</span><span class="sxs-lookup"><span data-stu-id="f16b8-222">What is the policy rule?</span></span>
- <span data-ttu-id="f16b8-223">Hvad er resultatet af politikreglen?</span><span class="sxs-lookup"><span data-stu-id="f16b8-223">What is the outcome of the policy rule?</span></span>

