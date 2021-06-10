---
title: Generere Affordable Care Act-indberetninger (ACA)
description: Affordable Care Act (ACA)-rapportering genererer blanketterne 1095-B og 1095-C som led i **Employer Mandate**-afsnittet af Affordable Care Act.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1091460ee1996b944b760f3771007bd2a26666a9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053195"
---
# <a name="generate-aca-reports"></a><span data-ttu-id="e34c6-103">Generere ACA-rapporter</span><span class="sxs-lookup"><span data-stu-id="e34c6-103">Generate ACA reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e34c6-104">Affordable Care Act (ACA)-rapportering genererer blanketterne 1095-B og 1095-C som led i **Employer Mandate**-afsnittet af Affordable Care Act.</span><span class="sxs-lookup"><span data-stu-id="e34c6-104">Affordable Care Act (ACA) reporting generates forms 1095-B and 1095-C in support of the **Employer Mandate** portion of the Affordable Care Act.</span></span>

> [!NOTE]
> <span data-ttu-id="e34c6-105">ACA-rapportering er kun aktiveret for juridiske enheder i USA.</span><span class="sxs-lookup"><span data-stu-id="e34c6-105">ACA reporting is only enabled for legal entities in the United States.</span></span>

## <a name="getting-started"></a><span data-ttu-id="e34c6-106">Kom godt i gang</span><span class="sxs-lookup"><span data-stu-id="e34c6-106">Getting started</span></span>

<span data-ttu-id="e34c6-107">Hvis du vil spore oplysninger, som skal indberettes i blanketterne 1095-B og C-1095, skal du først oprette en eller flere Affordable Care-dækningsgrupper.</span><span class="sxs-lookup"><span data-stu-id="e34c6-107">To track information for forms 1095-B and 1095-C, you must first create one or more Affordable care coverage groups.</span></span> <span data-ttu-id="e34c6-108">Affordable Care-dækningsgrupper angiver:</span><span class="sxs-lookup"><span data-stu-id="e34c6-108">Affordable Care coverage groups indicate:</span></span>

- <span data-ttu-id="e34c6-109">Tilbuddet om dækning for en medarbejder</span><span class="sxs-lookup"><span data-stu-id="e34c6-109">The offer of coverage for an employee</span></span>
- <span data-ttu-id="e34c6-110">Medarbejderens andel af det laveste månedlige løntillæg, hvis omkostningen ligger over den føderale fattigdomsgrænse</span><span class="sxs-lookup"><span data-stu-id="e34c6-110">The employee’s share of the lowest cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="e34c6-111">Safe Harbor bruges af arbejdsgiveren, hvis det er relevant</span><span class="sxs-lookup"><span data-stu-id="e34c6-111">Safe Harbor used by the employer, if applicable</span></span>

<span data-ttu-id="e34c6-112">Brug af dækningsgrupper under Affordable Care gør det muligt at administrere oplysningerne for disse felter uden at skulle ændre alle medarbejderposter, hvor betingelserne er ens.</span><span class="sxs-lookup"><span data-stu-id="e34c6-112">Affordable Care coverage groups allow you to manage the information for these fields without changing every employee record where the conditions are the same.</span></span> <span data-ttu-id="e34c6-113">Desuden kan Affordable Care-dækningsgrupper nemt tildeles til en eller flere medarbejdere ved hjælp af indstillingen **Massetildeling** på siden.</span><span class="sxs-lookup"><span data-stu-id="e34c6-113">You can easily assign Affordable Care coverage groups to one or more employees by using the **Mass assign** option on the page.</span></span>

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a><span data-ttu-id="e34c6-114">Vedligeholde flere versioner af en dækningsgruppe</span><span class="sxs-lookup"><span data-stu-id="e34c6-114">Maintaining multiple versions of a coverage group</span></span>

<span data-ttu-id="e34c6-115">Du kan vedligeholde flere versioner af en enhver dækningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e34c6-115">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="e34c6-116">Denne funktionalitet giver dig mulighed for at foretage ændringer uden at skulle oprette en ny gruppe og tildele medarbejdere til den igen.</span><span class="sxs-lookup"><span data-stu-id="e34c6-116">This functionality allows you to make changes without having to create a new group and reassign employees to it.</span></span> 

<span data-ttu-id="e34c6-117">Når du har oprettet ACA-dækningsgrupper, kan du tildele medarbejderne flere grupper med indstillingen **Massetildeling**.</span><span class="sxs-lookup"><span data-stu-id="e34c6-117">After you’ve created ACA coverage groups, you can mass assign the groups to employees with the **Mass assignment** option.</span></span> <span data-ttu-id="e34c6-118">Du kan også enkeltvist angive, om ACA-oplysninger skal spores og rapporteres, og knytte en medarbejder til dækningsgruppen Affordable Care for medarbejderne.</span><span class="sxs-lookup"><span data-stu-id="e34c6-118">You can also individually indicate whether to track and report ACA information, and assign an employee to an Affordable Care coverage group.</span></span>

<span data-ttu-id="e34c6-119">Du behøver ikke spore visse ACA-dækningsoplysninger, f.eks. for deltidsansatte.</span><span class="sxs-lookup"><span data-stu-id="e34c6-119">You don't need to track some ACA coverage information, such as for part-time employees.</span></span> <span data-ttu-id="e34c6-120">I dette tilfælde skal du angive feltet **Rapportdækning** til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="e34c6-120">In this case, set the **Report coverage** field to **No**.</span></span> <span data-ttu-id="e34c6-121">Selvom du skal tildele hver enkelt medarbejder med ACA-oplysninger, der kan spores, til en Affordable Care-dækningsgruppe, kan du stadig ændre følgende indstillinger for måneder med forskellige værdier:</span><span class="sxs-lookup"><span data-stu-id="e34c6-121">Although you must assign each employee with trackable ACA information to an Affordable Care coverage group, you can still change the following options for months with different values:</span></span>

- <span data-ttu-id="e34c6-122">**Tilbud om dækning**</span><span class="sxs-lookup"><span data-stu-id="e34c6-122">**Offer of coverage**</span></span>
- <span data-ttu-id="e34c6-123">**Medarbejderens andel af omkostningen**</span><span class="sxs-lookup"><span data-stu-id="e34c6-123">**Employee share of cost**</span></span>
- <span data-ttu-id="e34c6-124">**Safe Harbor**</span><span class="sxs-lookup"><span data-stu-id="e34c6-124">**Safe Harbor**</span></span>

<span data-ttu-id="e34c6-125">Hvis du vil angive undtagelser til værdier i Affordable Care-dækningsgrupper, skal du klikke på linket **Affordable Care Coverage** på siden **Detaljer om arbejder** under afsnittet **Flere oplysninger** under fanen **Ansættelse**.</span><span class="sxs-lookup"><span data-stu-id="e34c6-125">To enter exceptions for Affordable Care coverage group values, select the **Affordable Care Coverage** link on the **Worker detail** page under the **Additional information** section on the **Employment tab**.</span></span>

## <a name="reporting-health-care-coverage"></a><span data-ttu-id="e34c6-126">Indberetning af dækning af sygeforsikring</span><span class="sxs-lookup"><span data-stu-id="e34c6-126">Reporting health care coverage</span></span>

<span data-ttu-id="e34c6-127">Udover at spore en sygeforsikringsdækning, der blev tilbudt til fuldtidsmedarbejdere, hvis arbejdsgiveren tilbyder en arbejdsgiver-sponsoreret sygesikringsordning med egendækning, som medarbejderen er tilmeldt (uanset om vedkommendes ansættelsesstatus er fuldtid eller deltid), skal yderligere oplysninger rapporteres i 1095-C.</span><span class="sxs-lookup"><span data-stu-id="e34c6-127">In addition to tracking health insurance coverage offered to full-time employees, if the employer offers employer-sponsored self-insured health coverage for which the employee is enrolled (regardless of whether their employment status is full-time or part-time), additional information needs to be reported on the 1095-C.</span></span> <span data-ttu-id="e34c6-128">Hver medarbejder (inklusive deres afhængige parter), der er omfattet af arbejdsgiver-sponsorerede frynsegodeplaner, skal medtages i indberetningen for de måneder, hvor de var dækket.</span><span class="sxs-lookup"><span data-stu-id="e34c6-128">Each employee (including dependents) covered by the employer-sponsored benefit plans needs to be included on the report for the months they were covered.</span></span> 

<span data-ttu-id="e34c6-129">Du kan angive, om hver frynsegodeplan skal indberettes, ved at markere afkrydsningsfeltet **Skal indberettes til det amerikanske skattevæsen (ACA)**.</span><span class="sxs-lookup"><span data-stu-id="e34c6-129">You can indicate whether or not each benefit plan must be reported by selecting the **ACA reportable** check box.</span></span>

<span data-ttu-id="e34c6-130">Hvis medarbejdere derudover har valgt, at en eller flere afhængige parter skal være omfattet af et frynsegode, kan du angive de datoer, hvor disse afhængige har været dækket, for hver medarbejder på siden **Vedligehold frynsegoder**.</span><span class="sxs-lookup"><span data-stu-id="e34c6-130">In addition, if employees have chosen to have any of their dependents covered under a benefit, you can indicate the dates the dependent was covered for each employee on the **Maintain benefits** page.</span></span> <span data-ttu-id="e34c6-131">Du kan angive, at den afhængige part er dækket af frynsegoden, ved at vælge knappen **Rediger** i handlingsruden i oversigtspanelet **Afhængige**.</span><span class="sxs-lookup"><span data-stu-id="e34c6-131">To indicate that the dependent is covered under the benefit, select the **Edit** button in the action pane of the **Dependents** fast tab.</span></span>

<span data-ttu-id="e34c6-132">På siden **Håndtering af dækningsdato for den afhængige** kan du angive de datoer, hvor den afhængige part er dækket af frynsegodet.</span><span class="sxs-lookup"><span data-stu-id="e34c6-132">On the **Dependent coverage date manager** page, you can indicate the dates the dependent was covered by the benefit.</span></span> <span data-ttu-id="e34c6-133">Når du angiver datoer på denne side, markeres afkrydsningsfeltet **Dækket** automatisk på siden **Vedligehold frynsegoder**.</span><span class="sxs-lookup"><span data-stu-id="e34c6-133">Entering dates on this page will automatically select the **Covered** checkbox on the **Maintain benefits** page.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="e34c6-134">Generere 1095-B- og 1095-C-blanketter</span><span class="sxs-lookup"><span data-stu-id="e34c6-134">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="e34c6-135">Du kan også generere 1095-B- og 1095-C-blanketter fra produktet og distribuere dem til hver af dine medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="e34c6-135">You can also generate 1095-B and 1095-C forms from within the product, and distribute them to each of your employees.</span></span> <span data-ttu-id="e34c6-136">Systemet kan også generere 1095-C-blanketter elektronisk og 1094-C IRS-overførselsfilerne.</span><span class="sxs-lookup"><span data-stu-id="e34c6-136">The system can also electronically generate 1095-C forms and the 1094-C IRS transmittal files.</span></span>  

<span data-ttu-id="e34c6-137">Når du opretter blanketten 1095-C, skal du angive det relevante skatteår og angive, om social security-numre skal skjules.</span><span class="sxs-lookup"><span data-stu-id="e34c6-137">When generating the 1095-C form, enter the appropriate tax year and indicate if social security numbers should be masked.</span></span> <span data-ttu-id="e34c6-138">Hvis du udskriver 1095-C-blanketter for mere end 500 medarbejdere, modtager du mere end én PDF-fil.</span><span class="sxs-lookup"><span data-stu-id="e34c6-138">If you're printing 1095-C forms for more than 500 employees, you'll receive more than one PDF file.</span></span> <span data-ttu-id="e34c6-139">Det anbefales, at du øger **Maksimal filstørrelse** i vinduet **Dokumentstyringsparametre** til 150 MB.</span><span class="sxs-lookup"><span data-stu-id="e34c6-139">It’s recommended that you increase the **Maximum file size** in the **Document management parameters** window to 150 MB.</span></span>

## <a name="viewing-information"></a><span data-ttu-id="e34c6-140">Visning af oplysninger</span><span class="sxs-lookup"><span data-stu-id="e34c6-140">Viewing information</span></span>

<span data-ttu-id="e34c6-141">Du kan bruge siden **Arbejderens dækning under Affordable Care** til at se, hvilke medarbejdere der er tildelt til hver dækningsgruppe, hvilke medarbejderne der ikke skal medtages i en rapport, og hvilke medarbejdere der ikke er tildelt.</span><span class="sxs-lookup"><span data-stu-id="e34c6-141">You can use the **Worker Affordable Care coverage** page to see which employees have been assigned to each coverage group, which employees don’t need to be included on a report, and which employees are unassigned.</span></span>

<span data-ttu-id="e34c6-142">Hvis nogen af standardværdier fra Affordable Care-dækningsgruppen er blevet tilsidesat, vises en stjerne ud for den værdi, der er ændret.</span><span class="sxs-lookup"><span data-stu-id="e34c6-142">If any of the default values from the Affordable Care coverage group have been overridden, an asterisk will appear next to the value that was changed.</span></span> <span data-ttu-id="e34c6-143">Hvis værdierne for alle 12 måneder er de samme og ikke er blevet tilsidesat, udskrives værdien i kolonnen **Alle 12 måneder**.</span><span class="sxs-lookup"><span data-stu-id="e34c6-143">If the values for all 12 months are the same and haven’t been overridden, the value will print in the **All 12 months** column.</span></span>

<span data-ttu-id="e34c6-144">Du kan også bruge forespørgselsvinduet til at forstå, hvilke medarbejdere der er markeret som ikke ACA-rapporterbare.</span><span class="sxs-lookup"><span data-stu-id="e34c6-144">You can also use the inquiry window to understand which employees have been flagged as not ACA reportable.</span></span> <span data-ttu-id="e34c6-145">Du behøver ikke at spore, om de har fået dækning, og derfor behøver du ikke udstede et 1095-C til dem ved udgangen af året.</span><span class="sxs-lookup"><span data-stu-id="e34c6-145">You don’t need to track whether coverage was offered to them and won't need to issue a 1095-C to them at the end of the year.</span></span> <span data-ttu-id="e34c6-146">Vælg **Ikke ACA-rapporterbar** i feltet **Filtrer efter** for at generere en liste over alle medarbejdere, der ikke vil modtage 1095-C.</span><span class="sxs-lookup"><span data-stu-id="e34c6-146">Select **Not ACA reportable** in the **Filter by** field to generate a list of all employees who won't receive a 1095-C.</span></span>

<span data-ttu-id="e34c6-147">Derudover kan du se medarbejdere, der ikke er omfattet af ACA-indberetningspligten, kan du også få vist alle medarbejdere, der ikke er tildelt (feltet **Indberet ACA-dækning** er tomt), eller som er tildelt til en Affordable Care-dækningsgruppe, der er udløbet for det år, der er valgt i feltet **År**.</span><span class="sxs-lookup"><span data-stu-id="e34c6-147">In addition, you can view any employees who are unassigned (the **ACA Report coverage** field is empty) or who have been assigned to an Affordable Care coverage group that is expired for the year selected in the **Year** field.</span></span>

<span data-ttu-id="e34c6-148">Du kan eksportere lister over medarbejdere, som er genereret ved hjælp af filtreringsindstillingerne, til Excel.</span><span class="sxs-lookup"><span data-stu-id="e34c6-148">You can export lists of employees that were generated using any of the filtering options to Excel.</span></span>

<span data-ttu-id="e34c6-149">Hvis du har brug for at rapportere dækkede personer, fordi du giver dig selv forsikret dækning, kan du få vist alle afhængige, der er dækket af frynsegodeplaner, der er markeret som **ACA-rapporterbare**.</span><span class="sxs-lookup"><span data-stu-id="e34c6-149">If you need to report covered individuals because you provide self-insured coverage, you can view any dependents covered under benefit plans marked as **ACA reportable**.</span></span> <span data-ttu-id="e34c6-150">Vælg **Vis afhængig dækning** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e34c6-150">Select **View Dependent coverage** on the action pane.</span></span>

> [!NOTE]
> <span data-ttu-id="e34c6-151">Kun frynsegodeplaner, der markeret som **ACA-rapporterbare**, vises i forespørgselsvinduet.</span><span class="sxs-lookup"><span data-stu-id="e34c6-151">Only benefit plans marked as **ACA reportable** display in the inquiry window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]