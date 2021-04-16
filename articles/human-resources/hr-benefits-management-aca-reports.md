---
title: Generere Affordable Care Act-rapporter i Frynsegodeadministration
description: I dette emner beskrives, hvordan Frynsegodeadministration hjælper dig med at spore de oplysninger, der er rapporteret på blanket 1095-B og 1095-C for Affordable Care Act (ACA) Employer Mandate.
author: andreabichsel
ms.date: 12/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a41195ea3b52a707ce9deae38f12eb90de2ff5aa
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805796"
---
# <a name="generate-aca-reports-in-benefits-management"></a><span data-ttu-id="68887-103">Generere ACA-rapporter i Frynsegodeadministration</span><span class="sxs-lookup"><span data-stu-id="68887-103">Generate ACA reports in Benefits management</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="68887-104">Frynsegodeadministration hjælper dig med at spore de oplysninger, der er rapporteret på blanket 1095-B og 1095-C for Affordable Care Act (ACA) Employer Mandate.</span><span class="sxs-lookup"><span data-stu-id="68887-104">Benefits management helps you track information that is reported on Form 1095-B and Form 1095-C for the Affordable Care Act (ACA) employer mandate.</span></span> <span data-ttu-id="68887-105">Ligesom ACA-rapporteringsfunktionen i det gamle arbejdsområde **Frynsegoder** gælder denne funktion kun for juridiske enheder i USA.</span><span class="sxs-lookup"><span data-stu-id="68887-105">Like the ACA reporting capability in the old **Benefits** workspace, this functionality applies only to legal entities in the United States.</span></span>

<span data-ttu-id="68887-106">Hvis du vil bruge denne funktion, skal du først aktivere **avanceret administration af frynsegoder**.</span><span class="sxs-lookup"><span data-stu-id="68887-106">To use this functionality, you must first turn on **Advanced Benefits Management**.</span></span> <span data-ttu-id="68887-107">Yderligere oplysninger, herunder vigtige oplysninger om styring af goder, finder du i [Aktiver eller deaktiver administration af frynsegoder](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span><span class="sxs-lookup"><span data-stu-id="68887-107">For more information, including important caveats about Benefits management, see [Enable or disable Benefits management](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="68887-108">Du kan kun bruge ACA-rapportering fra arbejdsområdet til **Frynsegodeadministration** eller det gamle arbejdsområde til **Frynsegoder**, ikke fra begge.</span><span class="sxs-lookup"><span data-stu-id="68887-108">You can use ACA reporting only from either the **Benefits management** workspace or the old **Benefits** workspace, not from both.</span></span> <span data-ttu-id="68887-109">Hvis du f.eks. har skiftet til Frynsegodeadministration, er ACA-rapportering kun tilgængelig fra arbejdsområdet **Frynsegodeadministration**, ikke fra det gamle arbejdsområde til **Frynsegoder**.</span><span class="sxs-lookup"><span data-stu-id="68887-109">For example, if you switched to Benefits management, ACA reporting is available only from the **Benefits management** workspace, not from the old **Benefits** workspace.</span></span>
>
> <span data-ttu-id="68887-110">Hvis du skifter til Frynsegodeadministration midt i et tilmeldingsår, skal du konfigurere medarbejderdata korrekt for hele året i Frynsegodeadministration.</span><span class="sxs-lookup"><span data-stu-id="68887-110">If you switch to Benefits management in the middle of an enrollment year, you must correctly configure employee data for the whole year in Benefits management.</span></span> <span data-ttu-id="68887-111">På denne måde sikrer du, at du modtager nøjagtige rapporteringsoplysninger for hele året.</span><span class="sxs-lookup"><span data-stu-id="68887-111">In this way, you ensure that you will receive accurate reporting information for the whole year.</span></span>

## <a name="getting-started"></a><span data-ttu-id="68887-112">Kom godt i gang</span><span class="sxs-lookup"><span data-stu-id="68887-112">Getting started</span></span>

<span data-ttu-id="68887-113">Hvis du vil spore oplysninger for 1095-.blanketter, skal du første oprette en eller flere Affordable Care-dækningsgrupper.</span><span class="sxs-lookup"><span data-stu-id="68887-113">To track information for 1095 forms, first create one or more Affordable Care coverage groups.</span></span> <span data-ttu-id="68887-114">Disse grupper angiver følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="68887-114">These groups indicate the following information:</span></span>

- <span data-ttu-id="68887-115">Det dækningstilbud, som er til rådighed for en medarbejder</span><span class="sxs-lookup"><span data-stu-id="68887-115">The offer of coverage that was provided to an employee</span></span>
- <span data-ttu-id="68887-116">Medarbejderens andel af det laveste månedlige løntillæg, hvis omkostningen ligger over den føderale fattigdomsgrænse</span><span class="sxs-lookup"><span data-stu-id="68887-116">The employee's share of the lowest-cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="68887-117">'Safe Harbor', der bruges af arbejdsgiveren, hvis det er relevant</span><span class="sxs-lookup"><span data-stu-id="68887-117">The safe harbor that is used by the employer, if applicable</span></span>

<span data-ttu-id="68887-118">De Affordable Care-dækningsgrupper giver dig mulighed for at administrere disse oplysninger for flere medarbejderposter, der har samme betingelser.</span><span class="sxs-lookup"><span data-stu-id="68887-118">Affordable Care coverage groups help you manage this information for multiple employee records that have the same conditions.</span></span> <span data-ttu-id="68887-119">Det er nemt at tildele grupper til en eller flere medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="68887-119">You can easily assign groups to one or more employees.</span></span>

### <a name="create-or-edit-an-affordable-care-coverage-group"></a><span data-ttu-id="68887-120">Oprette eller redigere en Affordable Care-dækningsgruppe</span><span class="sxs-lookup"><span data-stu-id="68887-120">Create or edit an Affordable Care coverage group</span></span>

1. <span data-ttu-id="68887-121">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Affordable Care-dækningsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="68887-121">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>

    ![Vælge Affordable Care-dækningsgruppe](./media/hr-benefits-management-aca-coverage-group.png)

2. <span data-ttu-id="68887-123">Vælg **Ny** for at oprette en ny Affordable Care-dækningsgruppe eller **Rediger** for at ændre en eksisterende gruppe.</span><span class="sxs-lookup"><span data-stu-id="68887-123">Select **New** to create a new Affordable Care coverage group or **Edit** to change an existing group.</span></span>

    ![Vælge Ny eller Rediger](./media/hr-benefits-management-aca-new.png)

3. <span data-ttu-id="68887-125">Angiv følgende felter.</span><span class="sxs-lookup"><span data-stu-id="68887-125">Set the following fields.</span></span>

    | <span data-ttu-id="68887-126">Felt</span><span class="sxs-lookup"><span data-stu-id="68887-126">Field</span></span> | <span data-ttu-id="68887-127">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="68887-127">Description</span></span> |
    |---|---|
    | <span data-ttu-id="68887-128">Navn</span><span class="sxs-lookup"><span data-stu-id="68887-128">Name</span></span> | <span data-ttu-id="68887-129">Angiv et navn på gruppen.</span><span class="sxs-lookup"><span data-stu-id="68887-129">Enter a name for the group.</span></span> |
    | <span data-ttu-id="68887-130">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="68887-130">Description</span></span> | <span data-ttu-id="68887-131">Angiv en beskrivelse af gruppen.</span><span class="sxs-lookup"><span data-stu-id="68887-131">Enter a description of the group.</span></span> |
    | <span data-ttu-id="68887-132">Tilbud om dækning</span><span class="sxs-lookup"><span data-stu-id="68887-132">Offer of coverage</span></span> | <span data-ttu-id="68887-133">Den dækning, der tilbydes medarbejderne, deres ægtefælle eller partner og deres afhængige.</span><span class="sxs-lookup"><span data-stu-id="68887-133">The coverage that is offered to employees, their spouse or partner, and their dependents.</span></span> |
    | <span data-ttu-id="68887-134">Medarbejderens andel af omkostningen</span><span class="sxs-lookup"><span data-stu-id="68887-134">Employee share of cost</span></span> | <span data-ttu-id="68887-135">Det beløb, medarbejderen er ansvarlig for.</span><span class="sxs-lookup"><span data-stu-id="68887-135">The amount that the employee is responsible for.</span></span> |
    | <span data-ttu-id="68887-136">Gældende afsnit i 4980H Safe Harbor</span><span class="sxs-lookup"><span data-stu-id="68887-136">Applicable section 4980H safe harbor</span></span> | <span data-ttu-id="68887-137">Safe harbor-koden for 4980H eller overførselshjælpekoden.</span><span class="sxs-lookup"><span data-stu-id="68887-137">The 4980H safe harbor or transition relief code.</span></span> |
    | <span data-ttu-id="68887-138">Planlæg startmåned</span><span class="sxs-lookup"><span data-stu-id="68887-138">Plan start month</span></span> | <span data-ttu-id="68887-139">Vælg den kalendermåned, hvor frynsegodeplanåret starter.</span><span class="sxs-lookup"><span data-stu-id="68887-139">Select the calendar month when your benefit plan year begins.</span></span> |
    | <span data-ttu-id="68887-140">Gruppen er gældende fra</span><span class="sxs-lookup"><span data-stu-id="68887-140">Group valid from</span></span> | <span data-ttu-id="68887-141">Den første dato, denne post er gyldig.</span><span class="sxs-lookup"><span data-stu-id="68887-141">The first date when this record is valid.</span></span> |
    | <span data-ttu-id="68887-142">Gruppen er gældende til</span><span class="sxs-lookup"><span data-stu-id="68887-142">Group valid through</span></span> | <span data-ttu-id="68887-143">Den sidste dato, hvor denne post er gyldig.</span><span class="sxs-lookup"><span data-stu-id="68887-143">The last date when this record is valid.</span></span> <span data-ttu-id="68887-144">Hvis der ikke er nogen udløbsdato, skal du angive **Aldrig**.</span><span class="sxs-lookup"><span data-stu-id="68887-144">If there is no expiration date, enter **Never**.</span></span> |

    ![Oprette en dækningsgruppe](./media/hr-benefits-management-aca-new-group.png)

4. <span data-ttu-id="68887-146">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="68887-146">Select **Save**.</span></span>

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a><span data-ttu-id="68887-147">Tilknytte flere medarbejdere til Affordable Care-dækningsgruppe</span><span class="sxs-lookup"><span data-stu-id="68887-147">Assign multiple employees to an Affordable Care coverage group</span></span>

1. <span data-ttu-id="68887-148">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Affordable Care-dækningsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="68887-148">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>
2. <span data-ttu-id="68887-149">Vælg den gruppe, der skal tildeles medarbejdere til.</span><span class="sxs-lookup"><span data-stu-id="68887-149">Select the group to assign employees to.</span></span>
3. <span data-ttu-id="68887-150">Vælg **Massetildeling**.</span><span class="sxs-lookup"><span data-stu-id="68887-150">Select **Mass assignment**.</span></span>

    ![Vælge Massetildeling](./media/hr-benefits-management-aca-mass-assignment.png)

4. <span data-ttu-id="68887-152">Vælg medarbejdere på listen, og vælg derefter **Tildel**.</span><span class="sxs-lookup"><span data-stu-id="68887-152">Select employees in the list, and then select **Assign**.</span></span>

    ![Tildele valgte medarbejdere til en gruppe](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a><span data-ttu-id="68887-154">Vedligeholde flere versioner af en dækningsmuligheder</span><span class="sxs-lookup"><span data-stu-id="68887-154">Maintain multiple versions of coverage options</span></span>

<span data-ttu-id="68887-155">Du kan vedligeholde flere versioner af en enhver dækningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="68887-155">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="68887-156">Når der sker ændringer i organisationen eller de frynsegoder, der tilbydes, kan du holde oplysningerne for gruppen opdateret uden at skulle oprette en ny gruppe og tildele medarbejdere til den igen.</span><span class="sxs-lookup"><span data-stu-id="68887-156">When something changes in your organization or the benefits that are offered, you can keep the group's information up to date without having to create a new group and reassign employees to it.</span></span>

<span data-ttu-id="68887-157">Når du har oprettet Affordable Care-dækningsgrupper, kan du massetildele medarbejdere til dem.</span><span class="sxs-lookup"><span data-stu-id="68887-157">After you've created Affordable Care coverage groups, you can mass-assign employees to them.</span></span> <span data-ttu-id="68887-158">Du kan også tildele medarbejdere til grupper enkeltvist og angive, om ACA-oplysninger spores og rapporteres.</span><span class="sxs-lookup"><span data-stu-id="68887-158">You can also individually assign employees to groups, and indicate whether ACA information is tracked and reported.</span></span>

<span data-ttu-id="68887-159">Hvis du ikke behøver at spore og rapportere ACA-oplysninger for en medarbejder, kan du angive indstillingen **Rapportdækning** til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="68887-159">If you don't have to track and report ACA information for an employee, you can set the **Report coverage** option to **No**.</span></span> <span data-ttu-id="68887-160">Du kan f.eks. have deltidsansatte, der ikke kræver ACA-rapportering.</span><span class="sxs-lookup"><span data-stu-id="68887-160">For example, you might have part-time employees who don't require ACA reporting.</span></span>

### <a name="override-default-values-for-an-employee"></a><span data-ttu-id="68887-161">Tilsidesætte standardværdier for en medarbejder</span><span class="sxs-lookup"><span data-stu-id="68887-161">Override default values for an employee</span></span>

<span data-ttu-id="68887-162">For medarbejdere, der er knyttet til en Affordable Care-dækningsgruppe kan du ændre følgende indstillinger for alle måneder, der kræver forskellige værdier:</span><span class="sxs-lookup"><span data-stu-id="68887-162">For employees who are assigned to an Affordable Care coverage group, you can change the following options for any months that require different values:</span></span>

- <span data-ttu-id="68887-163">Tilbud om dækning</span><span class="sxs-lookup"><span data-stu-id="68887-163">Offer of coverage</span></span>
- <span data-ttu-id="68887-164">Medarbejderens andel af omkostningen</span><span class="sxs-lookup"><span data-stu-id="68887-164">Employee share of cost</span></span>
- <span data-ttu-id="68887-165">Gældende afsnit i 4980H Safe Harbor</span><span class="sxs-lookup"><span data-stu-id="68887-165">Applicable section 4980H safe harbor</span></span>

> [!NOTE]
> <span data-ttu-id="68887-166">Ved 2020 ACA-rapporter skal du rapportere både arbejds- og privat postnumre på Blanket 1095-C.</span><span class="sxs-lookup"><span data-stu-id="68887-166">For 2020 ACA reports, you must report both work and home ZIP Codes on Form 1095-C.</span></span> <span data-ttu-id="68887-167">Værdierne angives automatisk på basis af aktuelt aktive lokationer.</span><span class="sxs-lookup"><span data-stu-id="68887-167">Values are automatically filled in, based on current active locations.</span></span> <span data-ttu-id="68887-168">Hvis en af lokationerne har været forskellig i løbet af et år, skal du tilsidesætte værdien.</span><span class="sxs-lookup"><span data-stu-id="68887-168">If either location was different during any part of the year, you must override the value.</span></span> <span data-ttu-id="68887-169">Feltet **Postnummer** (linje 17) i 1095-C-rapporten udfyldes kun på følgende måde, hvis **Tilbud om dækning**-koden indeholder **1L** - **1Q**:</span><span class="sxs-lookup"><span data-stu-id="68887-169">The **ZIP Code** field (line 17) of the 1095-C report is filled in only if the **Offer of coverage** code contains **1L** through **1Q**, as follows:</span></span>
>
> - <span data-ttu-id="68887-170">**1L, 1M eller 1N:** Det primære postnummer for bopæl</span><span class="sxs-lookup"><span data-stu-id="68887-170">**1L, 1M, or 1N:** The primary residence ZIP Code</span></span>
> - <span data-ttu-id="68887-171">**1O, 1P, 1Q:** Det primære postnummer for arbejde</span><span class="sxs-lookup"><span data-stu-id="68887-171">**1O, 1P, 1Q:** The primary work ZIP Code</span></span>

<span data-ttu-id="68887-172">Benyt følgende fremgangsmåde for at angive undtagelser for værdier for en Affordable Care-dækningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="68887-172">To enter exceptions for any values of an Affordable Care coverage group, follow these steps.</span></span>

1. <span data-ttu-id="68887-173">Vælg **Links** i arbejdsområdet **Personalestyring**, og vælg derefter **Arbejdere**.</span><span class="sxs-lookup"><span data-stu-id="68887-173">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>
2. <span data-ttu-id="68887-174">Vælg medarbejderen på listen.</span><span class="sxs-lookup"><span data-stu-id="68887-174">Select the employee in the list.</span></span>
3. <span data-ttu-id="68887-175">Under fanen **Ansættelse** i afsnittet **Flere oplysninger** skal du vælge **Affordable Care-dækning**.</span><span class="sxs-lookup"><span data-stu-id="68887-175">On the **Employment** tab, in the **More information** section, select **Affordable Care coverage**.</span></span>

    ![Ændre indstillinger for én medarbejder](./media/hr-benefits-management-aca-change-single-employee.png)

4. <span data-ttu-id="68887-177">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="68887-177">Select **Edit**.</span></span>
5. <span data-ttu-id="68887-178">For hver måned, der kræver ændringer, skal du markere afkrydsningsfeltet **Tilsidesæt standard** og derefter ændre de andre værdier efter behov.</span><span class="sxs-lookup"><span data-stu-id="68887-178">For each month that requires changes, select the **Override default** check box, and then change the other values as required.</span></span>

    ![Tilsidesætte standardværdier](./media/hr-benefits-management-aca-override-default.png)

6. <span data-ttu-id="68887-180">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="68887-180">Select **Save**.</span></span>

## <a name="report-health-care-coverage"></a><span data-ttu-id="68887-181">Indberette dækning af sygeforsikring</span><span class="sxs-lookup"><span data-stu-id="68887-181">Report health care coverage</span></span>

<span data-ttu-id="68887-182">Du skal spore alle medarbejder-sponsorerede, selv-forsikrede sundhedsforsikringer for fuldtids- og deltidsansatte.</span><span class="sxs-lookup"><span data-stu-id="68887-182">You must track any employer-sponsored, self-insured health care coverage for full-time and part-time employees.</span></span> <span data-ttu-id="68887-183">Medtag hver medarbejder sammen med deres afhængige i 1095-C-rapporten for de måneder, de var dækket.</span><span class="sxs-lookup"><span data-stu-id="68887-183">Include each employee, together with their dependents, on the 1095-C report for the months when they were covered.</span></span>

<span data-ttu-id="68887-184">Hvis du vil angive, om der skal rapporteres en frynsegodeplan, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="68887-184">To indicate whether a benefit plan must be reported, follow these steps.</span></span>

1. <span data-ttu-id="68887-185">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Frynsegodeplaner**.</span><span class="sxs-lookup"><span data-stu-id="68887-185">In the **Benefits management** workspace, select **Benefit plans**.</span></span>
2. <span data-ttu-id="68887-186">Vælg den frynsegodeplan, der skal rapporteres.</span><span class="sxs-lookup"><span data-stu-id="68887-186">Select the benefit plan to report.</span></span>
3. <span data-ttu-id="68887-187">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="68887-187">Select **Edit**.</span></span>
4. <span data-ttu-id="68887-188">Angiv indstillingen **Rapporteret i henhold til Affordable Care Act** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="68887-188">Set the **Reported under the Affordable Care Act** option to **Yes**.</span></span>

    ![Indberetning af dækning af sygeforsikring](./media/hr-benefits-management-aca-report-coverage.png)

5. <span data-ttu-id="68887-190">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="68887-190">Select **Save**.</span></span>

<span data-ttu-id="68887-191">Hvis en medarbejder vælger sundhedsforsikring for en afhængig, bestemmes den afhængiges dækningsperiode på den dato, hvor den afhængige blev tilmeldt eller fjernet.</span><span class="sxs-lookup"><span data-stu-id="68887-191">If an employee chooses health care coverage for a dependent, the dependent's coverage period is determined by the date when the dependent was enrolled or removed.</span></span> <span data-ttu-id="68887-192">Dækningsdatoer for afhængige beregnes automatisk på basis af den periode, hvor den afhængige var berettiget og aktiv i en plan i løbet af tilmeldingsåret.</span><span class="sxs-lookup"><span data-stu-id="68887-192">Coverage dates for dependents are automatically calculated based on the period when the dependent was eligible and active in a plan during the enrollment year.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="68887-193">Generere 1095-B- og 1095-C-blanketter</span><span class="sxs-lookup"><span data-stu-id="68887-193">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="68887-194">Du kan også generere ACA 1095-B- og 1095-C-blanketter og derefter distribuere dem til hver af dine medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="68887-194">You can generate ACA 1095-B and 1095-C forms, and then distribute them to each of your employees.</span></span> <span data-ttu-id="68887-195">Du kan også elektronisk generere Blanket 1095-C og de tilsvarende 1094-C-overførselsfiler, der skal sendes til Internal Revenue Service (IRS).</span><span class="sxs-lookup"><span data-stu-id="68887-195">You can also electronically generate Form 1095-C and the corresponding 1094-C transmittal files to send to the Internal Revenue Service (IRS).</span></span>

1. <span data-ttu-id="68887-196">Vælg **ACA 1095-B**- eller **ACA 1095-C**-blanketten i arbejdsområdet **Frynsegodeadministration**.</span><span class="sxs-lookup"><span data-stu-id="68887-196">In the **Benefits management** workspace, select **ACA 1095-B form** or **ACA 1095-C form**.</span></span>
2. <span data-ttu-id="68887-197">Rediger parametrene efter behov, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="68887-197">Change the parameters as required, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="68887-198">Hvis du udskriver 1095-C-blanketter for mere end 500 medarbejdere, modtager du mere end én PDF-fil.</span><span class="sxs-lookup"><span data-stu-id="68887-198">If you're printing 1095-C forms for more than 500 employees, you will receive more than one PDF file.</span></span> <span data-ttu-id="68887-199">Det anbefales, at du øger værdien i feltet **Maksimal filstørrelse i megabyte** på siden **Dokumentadministrationsparametre** til **150**.</span><span class="sxs-lookup"><span data-stu-id="68887-199">We recommend that you increase the value of the **Maximum file size in megabytes** field on the **Document management parameters** page to **150**.</span></span> <span data-ttu-id="68887-200">(Hvis du hurtigt vil åbne siden, kan du bruge søgefeltet på navigationslinjen).</span><span class="sxs-lookup"><span data-stu-id="68887-200">(To quickly open that page, you can use the search field on the navigation bar.)</span></span>
    >
    > ![Ændre den maksimale filstørrelse](./media/hr-benefits-management-aca-maximum-file-size.png)

3. <span data-ttu-id="68887-202">Hvis du vil kontrollere status for rapporterne og få dem vist, skal du bruge søgefeltet på navigationslinjen til at åbne siden **Elektroniske rapporteringsjobs**.</span><span class="sxs-lookup"><span data-stu-id="68887-202">To check the status of your reports and view them, use the search field on the navigation bar to open the **Electronic reporting jobs** page.</span></span>

    ![Søge efter siden Job til elektronisk rapportering](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. <span data-ttu-id="68887-204">Marker den rapport, du vil have vist, og vælg derefter **Vis filer**.</span><span class="sxs-lookup"><span data-stu-id="68887-204">Select the report to view, and then select **Show files**.</span></span>

    ![Vise filer](./media/hr-benefits-management-aca-show-files.png)

5. <span data-ttu-id="68887-206">Vælg **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="68887-206">Select **Open**.</span></span>

    ![Åbne en fil](./media/hr-benefits-management-aca-open-file.png)

6. <span data-ttu-id="68887-208">Åbn zip-filen, og vælg derefter rapporten på den meddelelseslinje, der vises nederst i browservinduet.</span><span class="sxs-lookup"><span data-stu-id="68887-208">From the Notification bar that appears at the bottom of the browser window, open the zip file, and then select the report.</span></span> <span data-ttu-id="68887-209">Du kan få vist eller udskrive PDF-filen.</span><span class="sxs-lookup"><span data-stu-id="68887-209">You can view or print the PDF file.</span></span>

    ![Eksempel på 1095-C-blanket](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a><span data-ttu-id="68887-211">Vise oplysninger om ACA-dækning</span><span class="sxs-lookup"><span data-stu-id="68887-211">View ACA coverage information</span></span>

<span data-ttu-id="68887-212">På siden **Arbejderens dækning under Affordable Care** vises følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="68887-212">The **Worker Affordable Care coverage** page shows the following information:</span></span>

- <span data-ttu-id="68887-213">Medarbejdere, der er tilknyttet hver dækningsgruppe</span><span class="sxs-lookup"><span data-stu-id="68887-213">Employees who are assigned to each coverage group</span></span>
- <span data-ttu-id="68887-214">Medarbejdere, der ikke behøver at blive medtaget i en rapport</span><span class="sxs-lookup"><span data-stu-id="68887-214">Employees who don't have to be included on a report</span></span>
- <span data-ttu-id="68887-215">Ikke-tildelt medarbejder</span><span class="sxs-lookup"><span data-stu-id="68887-215">Unassigned employees</span></span>

<span data-ttu-id="68887-216">Benyt følgende trin for at se disse oplysninger.</span><span class="sxs-lookup"><span data-stu-id="68887-216">To view this information, follow these steps.</span></span>

1. <span data-ttu-id="68887-217">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Arbejderens dækning under Affordable Care**.</span><span class="sxs-lookup"><span data-stu-id="68887-217">In the **Benefits management** workspace, select **Worker Affordable Care coverage**.</span></span>
2. <span data-ttu-id="68887-218">Vælg en gruppe i feltet **Gruppenavn**.</span><span class="sxs-lookup"><span data-stu-id="68887-218">In the **Group name** field, select a group.</span></span>

    ![Vise ACA-dækning](./media/hr-benefits-management-aca-view-coverage.png)

<span data-ttu-id="68887-220">Hvis nogen af standardværdier fra Affordable Care-dækningsgruppen er blevet tilsidesat, vises en stjerne ud for den værdi, der er ændret.</span><span class="sxs-lookup"><span data-stu-id="68887-220">If any default values from the Affordable Care coverage group have been overridden, an asterisk appears next to the value that was changed.</span></span> <span data-ttu-id="68887-221">Hvis værdierne for alle 12 måneder er de samme og ikke er blevet tilsidesat, vises værdien i kolonnen **Alle 12 måneder**.</span><span class="sxs-lookup"><span data-stu-id="68887-221">If the values for all 12 months are the same and haven't been overridden, the value appears in the **All 12 months** column.</span></span>

<span data-ttu-id="68887-222">Du kan få vist medarbejdere, som ikke er markeret som ACA-reportable, og som ikke behøver en Blanket 1095-C.</span><span class="sxs-lookup"><span data-stu-id="68887-222">You can view employees who are marked as not ACA-reportable, and who won't require a Form 1095-C.</span></span> <span data-ttu-id="68887-223">Vælg **Ikke ACA-rapporterbar** i feltet **Filtrer efter**.</span><span class="sxs-lookup"><span data-stu-id="68887-223">In the **Filter by** field, select **Not ACA reportable**.</span></span>

<span data-ttu-id="68887-224">Du kan få vist medarbejdere, som ikke er knyttet til en gruppe, eller som er tildelt en udløbet gruppe.</span><span class="sxs-lookup"><span data-stu-id="68887-224">You can view employees who aren't assigned to a group, or who are assigned to an expired group.</span></span> <span data-ttu-id="68887-225">Vælg **ikke-tildelt eller udløbet gruppe** i feltet **Filtrer efter**.</span><span class="sxs-lookup"><span data-stu-id="68887-225">In the **Filter by** field, select **Unassigned or expired group**.</span></span>

### <a name="export-to-excel"></a><span data-ttu-id="68887-226">Eksportér til Excel</span><span class="sxs-lookup"><span data-stu-id="68887-226">Export to Excel</span></span>

<span data-ttu-id="68887-227">Hvis du vil eksportere en af Microsoft Excel-listerne, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="68887-227">To export any of the lists to Microsoft Excel, follow these steps.</span></span>

1. <span data-ttu-id="68887-228">Vælg knappen **Åbn i Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="68887-228">Select the **Open in Microsoft Office** button.</span></span>
2. <span data-ttu-id="68887-229">Vælg **HCM Human Resources-midlertidige tabel til intern brug**.</span><span class="sxs-lookup"><span data-stu-id="68887-229">Select **HCM Human Resources temporary table for internal use**.</span></span>
3. <span data-ttu-id="68887-230">Vælg **Hent**.</span><span class="sxs-lookup"><span data-stu-id="68887-230">Select **Download**.</span></span>

### <a name="view-aca-reportable-dependents"></a><span data-ttu-id="68887-231">Vise afhængige ACA, der kan rapporteres</span><span class="sxs-lookup"><span data-stu-id="68887-231">View ACA-reportable dependents</span></span>

<span data-ttu-id="68887-232">Hvis du skal rapportere dækkede personer, fordi du giver dig selv forsikret dækning, kan du få vist alle afhængige, der er dækket af frynsegodeplaner, der er markeret som **ACA-rapporterbare**.</span><span class="sxs-lookup"><span data-stu-id="68887-232">If you must report covered individuals because you provide self-insured coverage, you can view dependents who are covered under benefit plans that are marked as **ACA reportable**.</span></span> <span data-ttu-id="68887-233">Vælg **Vis afhængig af dækning** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="68887-233">On the Action Pane, select **View Dependent coverage**.</span></span>

![Vise afhængig af dækning](./media/hr-benefits-management-aca-view-dependent-coverage.png)

<span data-ttu-id="68887-235">Der vises dækningsoplysninger for dem, der er afhængige af medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="68887-235">Coverage information for the employee's dependents is shown.</span></span>

![Dækning for afhængig part](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> <span data-ttu-id="68887-237">Siden viser kun frynsegoder, der er markeret som **ACA-rapporterbare**.</span><span class="sxs-lookup"><span data-stu-id="68887-237">The page shows only benefits plans that are marked as **ACA reportable**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]