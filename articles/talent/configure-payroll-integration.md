---
title: Konfigurere lønintegration mellem Talent og Dayforce
description: Dette emne forklarer, hvordan du kan konfigurere integration mellem Microsoft Dynamics 365 for Talent og Ceridian Dayforce, så du kan behandle en lønkørsel.
author: andreabichsel
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9a88bf61dbb12520b555ceb7363b1c646d95386e
ms.sourcegitcommit: 204e4554e409c39fbbf7b273ad138ce2809931a8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/26/2019
ms.locfileid: "898438"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="52f18-103">Konfigurere lønintegrationen mellem Talent og Dayforce</span><span class="sxs-lookup"><span data-stu-id="52f18-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="52f18-104">Integration mellem Microsoft Dynamics 365 for Talent og Ceridian Dayforce er baseret på flere konfigurationstrin, der er beskrevet i dette emne.</span><span class="sxs-lookup"><span data-stu-id="52f18-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="52f18-105">Du skal konfigurere integrationen i både Talent og Dayforce, før du kan behandle en lønkørsel.</span><span class="sxs-lookup"><span data-stu-id="52f18-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="52f18-106">Når du bruger en tjeneste, f.eks. Dayforce, til at fuldføre lønkørsler, skal du aktivere integrationen i Talent.</span><span class="sxs-lookup"><span data-stu-id="52f18-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="52f18-107">Integrationen kræver bestemte data fra Talent.</span><span class="sxs-lookup"><span data-stu-id="52f18-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="52f18-108">Du skal derfor kontrollere, at data, der er knyttet til Dayforce, er konfigureret i Talent på en måde, der understøtter integrationen.</span><span class="sxs-lookup"><span data-stu-id="52f18-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="52f18-109">Integrationen bruger følgende brede kategorier af data.</span><span class="sxs-lookup"><span data-stu-id="52f18-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="52f18-110">Personaledata</span><span class="sxs-lookup"><span data-stu-id="52f18-110">Human resources data</span></span>
- <span data-ttu-id="52f18-111">Kompensationsdata</span><span class="sxs-lookup"><span data-stu-id="52f18-111">Compensation data</span></span>
- <span data-ttu-id="52f18-112">Lønoplysninger, f.eks. løncyklusser, betalingsperioder og lønkoder</span><span class="sxs-lookup"><span data-stu-id="52f18-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="52f18-113">Arbejderdata</span><span class="sxs-lookup"><span data-stu-id="52f18-113">Worker data</span></span>

<span data-ttu-id="52f18-114">Dette emne beskrives de trin, du skal udføre for at aktivere integrationen.</span><span class="sxs-lookup"><span data-stu-id="52f18-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="52f18-115">Det forklarer også typerne af data og oplysninger om konfigurationen, der kræves til integrationen.</span><span class="sxs-lookup"><span data-stu-id="52f18-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="52f18-116">Aktivere integrationen.</span><span class="sxs-lookup"><span data-stu-id="52f18-116">Enable the integration</span></span>

<span data-ttu-id="52f18-117">I Talent skal du aktivere integrationen og angive konfigurationsoplysningerne for at oprette forbindelse til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="52f18-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="52f18-118">Hvis den finanspostering, der er produceret, skal importeres til Microsoft Dynamics 365 for Finance and Operations, skal du også konfigurere en Microsoft Azure-lagerkonto og angive Azure-lagerets forbindelsesstreng i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="52f18-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="52f18-119">Følg disse trin for at aktivere integrationen i Talent.</span><span class="sxs-lookup"><span data-stu-id="52f18-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="52f18-120">På siden **Systemadministration** skal du vælge **Integrationskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="52f18-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="52f18-121">Angiv det sikre FTP-slutpunkt og den sikre FTP-mappesti.</span><span class="sxs-lookup"><span data-stu-id="52f18-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="52f18-122">Angiv brugernavnet og adgangskoden for den bruger, der skal have adgang til det sikre FTP-slutpunkt og den sikre mappesti.</span><span class="sxs-lookup"><span data-stu-id="52f18-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="52f18-123">Test forbindelsen, som krævet, og angiv indstillingen **Aktivér lønintegration** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="52f18-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="52f18-124">Når integrationen er aktiveret, oprettes dataeksportpakken og -filerne, og hyppigheden angives.</span><span class="sxs-lookup"><span data-stu-id="52f18-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="52f18-125">Du kan ændre denne frekvens efter behov.</span><span class="sxs-lookup"><span data-stu-id="52f18-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="52f18-126">Yderligere oplysninger om Azure-lagerkonti og Azure-lagerforbindelsesstrenge finder du i følgende Azure-emner:</span><span class="sxs-lookup"><span data-stu-id="52f18-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="52f18-127">Om Azure-lagerkonti</span><span class="sxs-lookup"><span data-stu-id="52f18-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="52f18-128">Konfigurere forbindelsesstrenge for Azure-datalager</span><span class="sxs-lookup"><span data-stu-id="52f18-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="52f18-129">Konfigurere dine data</span><span class="sxs-lookup"><span data-stu-id="52f18-129">Configure your data</span></span> 

<span data-ttu-id="52f18-130">Hvis du vil behandle løn, skal du konfigurere personaledata i Talent.</span><span class="sxs-lookup"><span data-stu-id="52f18-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="52f18-131">Du skal angive virksomhedens data, f.eks. job og stillinger, sammen med frynsegoder og kompensationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="52f18-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="52f18-132">Disse oplysninger indeholder oplysningerne om ansættelse, løn og fradrag, der kræves for at generere løn for medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="52f18-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="52f18-133">Personaledata</span><span class="sxs-lookup"><span data-stu-id="52f18-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="52f18-134">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="52f18-134">Benefits</span></span> 

<span data-ttu-id="52f18-135">Personale indeholder en række værktøjer til konfiguration og vedligeholdelse af frynsegoder, fradrag og arbejderkompensationsplaner, som en organisation tilbyder eller behandler for sine ansatte.</span><span class="sxs-lookup"><span data-stu-id="52f18-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="52f18-136">Når du opretter frynsegoder, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="52f18-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="52f18-137">Frynsegodeplaner</span><span class="sxs-lookup"><span data-stu-id="52f18-137">Benefit plans</span></span>

- <span data-ttu-id="52f18-138">Plan (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-138">Plan (required)</span></span>
- <span data-ttu-id="52f18-139">Type (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-139">Type (required)</span></span>
- <span data-ttu-id="52f18-140">Løneffekt (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-140">Payroll impact (required)</span></span>
- <span data-ttu-id="52f18-141">Opkræv restancer</span><span class="sxs-lookup"><span data-stu-id="52f18-141">Recover arrears</span></span>
- <span data-ttu-id="52f18-142">Fradragsmetode</span><span class="sxs-lookup"><span data-stu-id="52f18-142">Deduction method</span></span>
- <span data-ttu-id="52f18-143">Prioriteret fradrag</span><span class="sxs-lookup"><span data-stu-id="52f18-143">Deduction priority</span></span>
- <span data-ttu-id="52f18-144">Grænseperiode</span><span class="sxs-lookup"><span data-stu-id="52f18-144">Limit period</span></span>
- <span data-ttu-id="52f18-145">Beløb for grænse</span><span class="sxs-lookup"><span data-stu-id="52f18-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="52f18-146">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="52f18-146">Benefits</span></span>

- <span data-ttu-id="52f18-147">Plan (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-147">Plan (required)</span></span>
- <span data-ttu-id="52f18-148">Type (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-148">Type (required)</span></span>
- <span data-ttu-id="52f18-149">Mulighed (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-149">Option (required)</span></span>
- <span data-ttu-id="52f18-150">Frynsegode-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-150">Benefit ID (required)</span></span>
- <span data-ttu-id="52f18-151">Frekvens</span><span class="sxs-lookup"><span data-stu-id="52f18-151">Frequency</span></span>
- <span data-ttu-id="52f18-152">Basis</span><span class="sxs-lookup"><span data-stu-id="52f18-152">Basis</span></span>
- <span data-ttu-id="52f18-153">Beløb eller sats</span><span class="sxs-lookup"><span data-stu-id="52f18-153">Amount or rate</span></span>
- <span data-ttu-id="52f18-154">Lønkode</span><span class="sxs-lookup"><span data-stu-id="52f18-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="52f18-155">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="52f18-155">Supported frequencies</span></span> 

- <span data-ttu-id="52f18-156">Ugentlig</span><span class="sxs-lookup"><span data-stu-id="52f18-156">Weekly</span></span>
- <span data-ttu-id="52f18-157">Pr. 14 dage</span><span class="sxs-lookup"><span data-stu-id="52f18-157">Bi-weekly</span></span>
- <span data-ttu-id="52f18-158">To gange om måneden</span><span class="sxs-lookup"><span data-stu-id="52f18-158">Semi-monthly</span></span>
- <span data-ttu-id="52f18-159">Månedlig</span><span class="sxs-lookup"><span data-stu-id="52f18-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="52f18-160">Understøttede grundlag</span><span class="sxs-lookup"><span data-stu-id="52f18-160">Supported bases</span></span> 

- <span data-ttu-id="52f18-161">Fast beløb</span><span class="sxs-lookup"><span data-stu-id="52f18-161">Fixed amount</span></span>
- <span data-ttu-id="52f18-162">Procentdel af løn</span><span class="sxs-lookup"><span data-stu-id="52f18-162">Percent of earnings</span></span>
- <span data-ttu-id="52f18-163">Produktive timer</span><span class="sxs-lookup"><span data-stu-id="52f18-163">Productive hours</span></span>

<span data-ttu-id="52f18-164">Dayforce opretter følgende fradrag, der er baseret på den løneffekt, der er defineret på frynsegodeplanen.</span><span class="sxs-lookup"><span data-stu-id="52f18-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="52f18-165">Valg i Talent</span><span class="sxs-lookup"><span data-stu-id="52f18-165">Selection in Talent</span></span>        | <span data-ttu-id="52f18-166">Resultat i Dayforce</span><span class="sxs-lookup"><span data-stu-id="52f18-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="52f18-167">None</span><span class="sxs-lookup"><span data-stu-id="52f18-167">None</span></span>                       | <span data-ttu-id="52f18-168">Der oprettes ikke noget fradrag.</span><span class="sxs-lookup"><span data-stu-id="52f18-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="52f18-169">Kun fradrag</span><span class="sxs-lookup"><span data-stu-id="52f18-169">Deduction only</span></span>             | <span data-ttu-id="52f18-170">Der oprettes et medarbejderfradrag.</span><span class="sxs-lookup"><span data-stu-id="52f18-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="52f18-171">Kun bidrag</span><span class="sxs-lookup"><span data-stu-id="52f18-171">Contribution only</span></span>          | <span data-ttu-id="52f18-172">Der oprettes et arbejdsgiverfradrag.</span><span class="sxs-lookup"><span data-stu-id="52f18-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="52f18-173">Fradrag og bidrag</span><span class="sxs-lookup"><span data-stu-id="52f18-173">Deduction and contribution</span></span> | <span data-ttu-id="52f18-174">Der oprettes medarbejder- og arbejdsgiverfradrag.</span><span class="sxs-lookup"><span data-stu-id="52f18-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="52f18-175">Du kan finde flere oplysninger om, hvordan du definerer og administrerer et frynsegodeprogram under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="52f18-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="52f18-176">Levere et frynsegodeprogram for medarbejdere</span><span class="sxs-lookup"><span data-stu-id="52f18-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="52f18-177">Oprette et nyt frynsegode</span><span class="sxs-lookup"><span data-stu-id="52f18-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="52f18-178">Definere regler og politikker for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="52f18-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="52f18-179">Tilmelde og fjerne frynsegoder fra arbejdere</span><span class="sxs-lookup"><span data-stu-id="52f18-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="52f18-180">Kompensation</span><span class="sxs-lookup"><span data-stu-id="52f18-180">Compensation</span></span> 

<span data-ttu-id="52f18-181">Kompensationsstyring bruges til at styre fordelingen af grundløn og bonusser.</span><span class="sxs-lookup"><span data-stu-id="52f18-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="52f18-182">En medarbejders faste grundløn og kvalifikationstillæg styres gennem faste lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="52f18-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="52f18-183">Betalingen af incitamentsløn som f.eks. bonusudbetalinger, præstationsbonusser, aktieoptioner og tildelte aktier samt engangsbonusser styres ved hjælp af variable lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="52f18-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="52f18-184">Dayforce anvendes kompensationsoplysninger til at beregne en medarbejders timesats eller årlige sats.</span><span class="sxs-lookup"><span data-stu-id="52f18-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="52f18-185">Konverteringer af planer for fast løn og lønsats er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="52f18-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="52f18-186">Medarbejderne skal være knyttet til en plan for fast løn.</span><span class="sxs-lookup"><span data-stu-id="52f18-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="52f18-187">Du kan finde flere oplysninger om kompensationsplaner under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="52f18-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="52f18-188">Oprette faste kompensationsordninger</span><span class="sxs-lookup"><span data-stu-id="52f18-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="52f18-189">Oprette planer for variabel kompensation</span><span class="sxs-lookup"><span data-stu-id="52f18-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="52f18-190">Udarbejde løn-/kompensationsstruktur og -planer</span><span class="sxs-lookup"><span data-stu-id="52f18-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="52f18-191">Proceskompensation</span><span class="sxs-lookup"><span data-stu-id="52f18-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="52f18-192">Definere kompensationsproces og beregne resultater</span><span class="sxs-lookup"><span data-stu-id="52f18-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="52f18-193">Melde en medarbejder til en fast lønplan</span><span class="sxs-lookup"><span data-stu-id="52f18-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="52f18-194">Melde en medarbejder til en variabel lønplan</span><span class="sxs-lookup"><span data-stu-id="52f18-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="52f18-195">Job</span><span class="sxs-lookup"><span data-stu-id="52f18-195">Jobs</span></span> 

<span data-ttu-id="52f18-196">Et job er en samling af de opgaver og ansvarsområder, der kræves af en person, der udfører et job.</span><span class="sxs-lookup"><span data-stu-id="52f18-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="52f18-197">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="52f18-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="52f18-198">Konfiguration af komponenter i et job</span><span class="sxs-lookup"><span data-stu-id="52f18-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="52f18-199">Definere nye job</span><span class="sxs-lookup"><span data-stu-id="52f18-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="52f18-200">Stillinger</span><span class="sxs-lookup"><span data-stu-id="52f18-200">Positions</span></span>

<span data-ttu-id="52f18-201">En stilling er en individuel forekomst af et job.</span><span class="sxs-lookup"><span data-stu-id="52f18-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="52f18-202">For eksempel er stillingen "Salgschef (øst)" én af de stillinger, der er tilknyttet jobbet "Salgschef".</span><span class="sxs-lookup"><span data-stu-id="52f18-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="52f18-203">En stilling findes i en afdeling.</span><span class="sxs-lookup"><span data-stu-id="52f18-203">A position exists in a department.</span></span> <span data-ttu-id="52f18-204">Der kan kun knyttes én arbejder til hver stilling.</span><span class="sxs-lookup"><span data-stu-id="52f18-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="52f18-205">Hav følgende data og konfiguration i tankerne, når du konfigurerer stillinger:</span><span class="sxs-lookup"><span data-stu-id="52f18-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="52f18-206">Stilling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-206">Position (required)</span></span>
- <span data-ttu-id="52f18-207">Beskrivelse (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-207">Description (required)</span></span>
- <span data-ttu-id="52f18-208">Job (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-208">Job (required)</span></span>
- <span data-ttu-id="52f18-209">Afdeling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-209">Department (required)</span></span>
- <span data-ttu-id="52f18-210">Stillingstype (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-210">Position type (required)</span></span>
- <span data-ttu-id="52f18-211">Fuldtidsækvivalent</span><span class="sxs-lookup"><span data-stu-id="52f18-211">Full-time equivalent</span></span>
- <span data-ttu-id="52f18-212">Normaltimer på årsbasis (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="52f18-213">Betalt af juridiske enhed (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="52f18-214">Betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-214">Pay cycle (required)</span></span>
- <span data-ttu-id="52f18-215">Økonomisk standarddimension – bærer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="52f18-216">Arbejdertildeling – arbejder, tildelingsstart, tildelingsslut, årsagskode</span><span class="sxs-lookup"><span data-stu-id="52f18-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="52f18-217">Hvis flere stillinger i den samme afdeling er knyttet til samme job, konsolideres de til en enkelt stilling i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="52f18-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="52f18-218">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="52f18-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="52f18-219">Organisere dine medarbejdere ved hjælp af afdelinger, jobs og stillinger</span><span class="sxs-lookup"><span data-stu-id="52f18-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="52f18-220">Konfigurere stillinger</span><span class="sxs-lookup"><span data-stu-id="52f18-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="52f18-221">Afdelinger</span><span class="sxs-lookup"><span data-stu-id="52f18-221">Departments</span></span>

<span data-ttu-id="52f18-222">En afdeling er en driftsenhed, der repræsenterer en kategori eller et funktionsområde i en organisation.</span><span class="sxs-lookup"><span data-stu-id="52f18-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="52f18-223">En afdeling er ansvarlig for et bestemt område i organisationen, såsom salg, regnskab eller personale.</span><span class="sxs-lookup"><span data-stu-id="52f18-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="52f18-224">Du kan bruge afdelinger til at rapportere om funktionsområder.</span><span class="sxs-lookup"><span data-stu-id="52f18-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="52f18-225">Afdelinger kan have ansvar for driftsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="52f18-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="52f18-226">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="52f18-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="52f18-227">Oprette en afdeling og knytte den til afdelingshierarkiet</span><span class="sxs-lookup"><span data-stu-id="52f18-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="52f18-228">Definere nye afdelinger</span><span class="sxs-lookup"><span data-stu-id="52f18-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="52f18-229">Betalingscyklusser og lønperioder</span><span class="sxs-lookup"><span data-stu-id="52f18-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="52f18-230">En betalingscyklus bestemmer, hvor ofte løn køres,og de specifikke dage, hvor arbejdere betales.</span><span class="sxs-lookup"><span data-stu-id="52f18-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="52f18-231">En løncyklus kan f.eks. være månedlig, og medarbejdere betales måske på den sidste dag i måneden.</span><span class="sxs-lookup"><span data-stu-id="52f18-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="52f18-232">En løncyklus kan også være ugentligt, og medarbejdere betales måske tirsdag efter slutningen af lønperioden.</span><span class="sxs-lookup"><span data-stu-id="52f18-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="52f18-233">Løncyklusser tildeles til stillinger for at styre, hvornår arbejdere i disse stillinger bliver betalt.</span><span class="sxs-lookup"><span data-stu-id="52f18-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="52f18-234">Når du opretter betalingscyklusser, kan du generere lønperioder for hver cyklus.</span><span class="sxs-lookup"><span data-stu-id="52f18-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="52f18-235">Hver lønperiode omfatter en standardbetalingsdato, der er baseret på oplysninger, du angiver.</span><span class="sxs-lookup"><span data-stu-id="52f18-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="52f18-236">Du kan dog redigere standardbetalingsdatoen i en lønperiode til at tillade undtagelser, f.eks. når betalingsdatoen falder på en helligdag.</span><span class="sxs-lookup"><span data-stu-id="52f18-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="52f18-237">Følgende oplysninger bruges i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="52f18-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="52f18-238">Betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-238">Pay cycle (required)</span></span>
- <span data-ttu-id="52f18-239">Hyppighed for betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="52f18-240">Periodens startdato (første lønperiode påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="52f18-241">Standardbetalingsdato (første lønperiode påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="52f18-242">Oplysningerne er integreret med Dayforce som løngrupper og adskilles af et land eller område for hver løncyklus.</span><span class="sxs-lookup"><span data-stu-id="52f18-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="52f18-243">Mindst én periode skal genereres før integration.</span><span class="sxs-lookup"><span data-stu-id="52f18-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="52f18-244">Dayforce genererer løngruppekalendere og betalingsdatoer, der er baseret på startdatoen for den første lønperiode og den standardbetalingsdato, der er angivet i Talent.</span><span class="sxs-lookup"><span data-stu-id="52f18-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="52f18-245">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="52f18-245">Earning codes</span></span>

<span data-ttu-id="52f18-246">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="52f18-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="52f18-247">Koderne har forskellige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="52f18-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="52f18-248">Følgende oplysninger bruges i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="52f18-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="52f18-249">Lønkode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-249">Earning Code (required)</span></span>
- <span data-ttu-id="52f18-250">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="52f18-250">Description</span></span>
- <span data-ttu-id="52f18-251">Måleenhed</span><span class="sxs-lookup"><span data-stu-id="52f18-251">Unit of measure</span></span>
- <span data-ttu-id="52f18-252">Produktiv</span><span class="sxs-lookup"><span data-stu-id="52f18-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="52f18-253">Arbejderdata</span><span class="sxs-lookup"><span data-stu-id="52f18-253">Worker data</span></span>

<span data-ttu-id="52f18-254">Posterne for de forskellige typer arbejdere, du beskæftiger, er vigtige for dine personale- og lønsystemer.</span><span class="sxs-lookup"><span data-stu-id="52f18-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="52f18-255">De oplysninger, du angiver, kan bruges til at spore arbejdere og personoplysninger.</span><span class="sxs-lookup"><span data-stu-id="52f18-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="52f18-256">Du kan vedligeholde følgende oplysninger for arbejdere:</span><span class="sxs-lookup"><span data-stu-id="52f18-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="52f18-257">**Basis** – Vedligehold grundlæggende oplysninger om en arbejder, f.eks. kontaktoplysninger, demografiske oplysninger, identifikationsoplysninger, oplysninger om familie, status for militærtjeneste, oplysninger om udstationering og personlige kontaktpersoner og kontaktpersoner i nødsituationer.</span><span class="sxs-lookup"><span data-stu-id="52f18-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="52f18-258">**Beskæftigelse** – Vedligehold oplysninger om en arbejders beskæftigelse, f.eks. firma- eller organisationstilhørsforhold, stillingstildeling, start- og slutdatoer, arbejdstilladelse, vilkår for ansættelse, pension, ferie og flytteoplysninger.</span><span class="sxs-lookup"><span data-stu-id="52f18-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="52f18-259">**Orlov og fravær** – Vedligehold oplysninger om en arbejders fravær, f.eks. arbejdskalendere, fraværstransaktioner og fraværsopsætning.</span><span class="sxs-lookup"><span data-stu-id="52f18-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="52f18-260">**Kompensation og løn** – Vedligehold oplysninger om en arbejders kompensationsplaner og lønoplysninger, f.eks. tilmelding til planer, priser, ydeevne, provision, skatteoplysninger, pensionering og skattefradrag.</span><span class="sxs-lookup"><span data-stu-id="52f18-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="52f18-261">Når du angiver arbejderoplysninger, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="52f18-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="52f18-262">Generelle oplysninger</span><span class="sxs-lookup"><span data-stu-id="52f18-262">General information</span></span>

- <span data-ttu-id="52f18-263">Personalenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-263">Personnel number (required)</span></span>
- <span data-ttu-id="52f18-264">Fornavn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-264">First name (required)</span></span>
- <span data-ttu-id="52f18-265">Efternavn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-265">Last name (required)</span></span>
- <span data-ttu-id="52f18-266">Mellemnavn</span><span class="sxs-lookup"><span data-stu-id="52f18-266">Middle name</span></span>
- <span data-ttu-id="52f18-267">Anciennitetsdato</span><span class="sxs-lookup"><span data-stu-id="52f18-267">Seniority date</span></span>
- <span data-ttu-id="52f18-268">Kendt som</span><span class="sxs-lookup"><span data-stu-id="52f18-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="52f18-269">Personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="52f18-269">Personal information</span></span>

- <span data-ttu-id="52f18-270">Ægteskabelig status (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-270">Marital status (required)</span></span>
- <span data-ttu-id="52f18-271">Fødselsdato (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-271">Birth date (required)</span></span>
- <span data-ttu-id="52f18-272">Køn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-272">Gender (required)</span></span>
- <span data-ttu-id="52f18-273">Handicappet</span><span class="sxs-lookup"><span data-stu-id="52f18-273">Person with disabilities</span></span>
- <span data-ttu-id="52f18-274">Land eller område for nationalitet (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="52f18-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="52f18-275">Adresseoplysninger</span><span class="sxs-lookup"><span data-stu-id="52f18-275">Address information</span></span>

- <span data-ttu-id="52f18-276">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-276">Primary (required)</span></span>
- <span data-ttu-id="52f18-277">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-277">Country/region (required)</span></span>
- <span data-ttu-id="52f18-278">Postnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-278">Postal code (required)</span></span>
- <span data-ttu-id="52f18-279">Gadenummer (påkrævet) (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="52f18-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="52f18-280">Bygningskomplement (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="52f18-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="52f18-281">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-281">City (required)</span></span>
- <span data-ttu-id="52f18-282">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-282">State (required)</span></span>
- <span data-ttu-id="52f18-283">Region (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="52f18-284">Kontaktoplysninger</span><span class="sxs-lookup"><span data-stu-id="52f18-284">Contact information</span></span> 

- <span data-ttu-id="52f18-285">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-285">Primary (required)</span></span>
- <span data-ttu-id="52f18-286">Kontaktpersonens nummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-286">Contact number (required)</span></span>
- <span data-ttu-id="52f18-287">Forlængelse</span><span class="sxs-lookup"><span data-stu-id="52f18-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="52f18-288">Lønoplysninger og lønkoder</span><span class="sxs-lookup"><span data-stu-id="52f18-288">Payroll information and earning codes</span></span>

<span data-ttu-id="52f18-289">Medarbejdere kan tildeles en bestemt løn med en given betalingshyppighed og have en foretrukken betalingsmetode.</span><span class="sxs-lookup"><span data-stu-id="52f18-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="52f18-290">Følgende felter bruges i Dayforce til at sikre, at disse præferencer og indstillinger bruges.</span><span class="sxs-lookup"><span data-stu-id="52f18-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="52f18-291">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="52f18-291">Earning codes</span></span>

- <span data-ttu-id="52f18-292">Stilling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-292">Position (required)</span></span>
- <span data-ttu-id="52f18-293">Lønkode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-293">Earning Code (required)</span></span>
- <span data-ttu-id="52f18-294">Frekvens (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-294">Frequency (required)</span></span>
- <span data-ttu-id="52f18-295">Beløb (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="52f18-296">Lønoplysninger</span><span class="sxs-lookup"><span data-stu-id="52f18-296">Payroll information</span></span>

- <span data-ttu-id="52f18-297">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="52f18-297">Payment Method</span></span>
- <span data-ttu-id="52f18-298">Økonomisk område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-298">Economic Region (required)</span></span>
- <span data-ttu-id="52f18-299">Id for medarbejderfrynsegoder</span><span class="sxs-lookup"><span data-stu-id="52f18-299">Employee Benefits ID</span></span>
- <span data-ttu-id="52f18-300">Nationalt id-nummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-300">National ID Number (required)</span></span>
- <span data-ttu-id="52f18-301">Tjenestenummer hos militær</span><span class="sxs-lookup"><span data-stu-id="52f18-301">Military Service Number</span></span>
- <span data-ttu-id="52f18-302">Skifte-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-302">Shift ID (required)</span></span>
- <span data-ttu-id="52f18-303">Skattenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-303">Tax Number (required)</span></span>
- <span data-ttu-id="52f18-304">Fagforenings-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-304">Union ID (required)</span></span>
- <span data-ttu-id="52f18-305">Arbejdsdags-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-305">Work Day ID (required)</span></span>
- <span data-ttu-id="52f18-306">Arbejdstilladelsesnummer</span><span class="sxs-lookup"><span data-stu-id="52f18-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="52f18-307">For betalingsmetoden understøtter Mexico **Kontant**, **Check** (firmaets fysiske check), og **Elektronisk betaling**.</span><span class="sxs-lookup"><span data-stu-id="52f18-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="52f18-308">Hvis der ikke er angivet nogen betalingsmetode, bruges **Check** som standard.</span><span class="sxs-lookup"><span data-stu-id="52f18-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="52f18-309">Detaljer om ansættelse</span><span class="sxs-lookup"><span data-stu-id="52f18-309">Employment details</span></span>

<span data-ttu-id="52f18-310">Detaljeret ansættelseshistorik bruges som vigtige oplysninger til at udlede statusser for en medarbejders ansættelse, fratrædelse og genansættelse i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="52f18-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="52f18-311">Dayforce understøtter kun én aktiv ansættelsespost ad gangen.</span><span class="sxs-lookup"><span data-stu-id="52f18-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="52f18-312">Startdato for ansættelse (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-312">Employment start date (required)</span></span>
- <span data-ttu-id="52f18-313">Slutdato for ansættelse</span><span class="sxs-lookup"><span data-stu-id="52f18-313">Employment end date</span></span>
- <span data-ttu-id="52f18-314">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="52f18-314">Start date</span></span>
- <span data-ttu-id="52f18-315">Justeret startdato</span><span class="sxs-lookup"><span data-stu-id="52f18-315">Adjusted start date</span></span>
- <span data-ttu-id="52f18-316">Fratrædelsesdato (kræves ved fratrædelse)</span><span class="sxs-lookup"><span data-stu-id="52f18-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="52f18-317">Fratrædelsesårsag (kræves ved fratrædelse)</span><span class="sxs-lookup"><span data-stu-id="52f18-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="52f18-318">Vigtige datoer for en medarbejders udledes ved hjælp af følgende oplysninger.</span><span class="sxs-lookup"><span data-stu-id="52f18-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="52f18-319">Talent</span><span class="sxs-lookup"><span data-stu-id="52f18-319">Talent</span></span>                | <span data-ttu-id="52f18-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="52f18-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52f18-321">Den seneste ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="52f18-321">Most recent hire date</span></span> | <span data-ttu-id="52f18-322">Historikpost for ansættelsesstart for aktuel ikke-afsluttet ansættelse</span><span class="sxs-lookup"><span data-stu-id="52f18-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="52f18-323">Fratrædelsesdato</span><span class="sxs-lookup"><span data-stu-id="52f18-323">Termination date</span></span>      | <span data-ttu-id="52f18-324">Historikpost for fratrædelsesdato for aktuel ikke-afsluttet ansættelse</span><span class="sxs-lookup"><span data-stu-id="52f18-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="52f18-325">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="52f18-325">Start date</span></span>            | <span data-ttu-id="52f18-326">Historikpost for justeret startdato, startdato eller startdato for ansættelse for aktuel ikke-aktiv ansættelse</span><span class="sxs-lookup"><span data-stu-id="52f18-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="52f18-327">Oprindelig ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="52f18-327">Original hire date</span></span>    | <span data-ttu-id="52f18-328">Historikpost for ansættelsesstart for tidligste ansættelse</span><span class="sxs-lookup"><span data-stu-id="52f18-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="52f18-329">Kompensation</span><span class="sxs-lookup"><span data-stu-id="52f18-329">Compensation</span></span>

<span data-ttu-id="52f18-330">En fast lønstruktur skal tilknyttes hver medarbejders primære stilling gennem hele ansættelsesperioden.</span><span class="sxs-lookup"><span data-stu-id="52f18-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="52f18-331">Denne periode starter på den dato, hvor medarbejderen blev ansat (eller ansættelsesstartdatoen) og fortsætter, indtil fratrædelsen.</span><span class="sxs-lookup"><span data-stu-id="52f18-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="52f18-332">Ikrafttrædelsesdato (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-332">Effective Date (required)</span></span>
- <span data-ttu-id="52f18-333">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="52f18-333">Expiration date</span></span>
- <span data-ttu-id="52f18-334">Lønsats (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-334">Pay Rate (required)</span></span>
- <span data-ttu-id="52f18-335">Konverteringer af lønsats (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="52f18-336">Årlig ækvivalent (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="52f18-337">Timebaseret ækvivalent (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="52f18-338">Hvis en timeansat medarbejder har flere stillinger, indlæses den faste løn for den primære stilling i Dayforce, som basissats/-løn på medarbejderniveau.</span><span class="sxs-lookup"><span data-stu-id="52f18-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="52f18-339">For ikke-primære stillinger gemmes timesatsen i den tilsvarende position i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="52f18-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="52f18-340">Hvis en funktionær har flere stillinger, afledes den kumulative timesats og årlig gage på tværs af alle aktive stillinger og bruges som basissats/-gage på medarbejderniveau.</span><span class="sxs-lookup"><span data-stu-id="52f18-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="52f18-341">Identifikationsnumre</span><span class="sxs-lookup"><span data-stu-id="52f18-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="52f18-342">Social Security-identifikator</span><span class="sxs-lookup"><span data-stu-id="52f18-342">Social Security identifier</span></span> 

<span data-ttu-id="52f18-343">Alle medarbejdere skal have én primær identifikator.</span><span class="sxs-lookup"><span data-stu-id="52f18-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="52f18-344">Identifikatoren skal være af **SSN**-identifikationstypen</span><span class="sxs-lookup"><span data-stu-id="52f18-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="52f18-345">I Dayforce afledes den automatisk som medarbejderens Social Security-identifikator, der er påkrævet ved ansættelse.</span><span class="sxs-lookup"><span data-stu-id="52f18-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="52f18-346">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-346">Primary (required)</span></span>
- <span data-ttu-id="52f18-347">Identifikationstype = "SSN"</span><span class="sxs-lookup"><span data-stu-id="52f18-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="52f18-348">Udstedt den</span><span class="sxs-lookup"><span data-stu-id="52f18-348">Issued Date</span></span>
- <span data-ttu-id="52f18-349">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="52f18-349">Expiration Date</span></span>

<span data-ttu-id="52f18-350">Medarbejdere kan angive flere identifikationsnumre af **SSN**-identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="52f18-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="52f18-351">Men det er kun den post, der er markeret som **Primær**, som er integreret i Dayforce, uanset om nummeret er aktivt eller udløbet.</span><span class="sxs-lookup"><span data-stu-id="52f18-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="52f18-352">Bankkonto og udbetalinger</span><span class="sxs-lookup"><span data-stu-id="52f18-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="52f18-353">Gyldige bankkontooplysninger skal angives for enhver medarbejder, der vælger at blive betalt via bankkontooverførsler.</span><span class="sxs-lookup"><span data-stu-id="52f18-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="52f18-354">Talent</span><span class="sxs-lookup"><span data-stu-id="52f18-354">Talent</span></span>                         | <span data-ttu-id="52f18-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="52f18-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52f18-356">Bankkontonummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="52f18-357">SWIFT-kode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-357">SWIFT code (required)</span></span>          | <span data-ttu-id="52f18-358">Feltet **Bank-id** bruges ved behandling af løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="52f18-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="52f18-359">Afdelingsnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="52f18-360">Bankkontotype (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-360">Bank account type (required)</span></span>   | <span data-ttu-id="52f18-361">Feltet **Kontotype** bruges ved behandling af løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="52f18-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="52f18-362">Understøttede værdier omfatter **Check** og **Løn**.</span><span class="sxs-lookup"><span data-stu-id="52f18-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="52f18-363">Medarbejdere, der vælger at betales via bankkontooverførsler, skal angive et link til en restbeløbskonto, der hører under en juridisk enhed, som har primær adresse i Mexico og er knyttet til en gyldig bankkonto fra en mexicansk bank.</span><span class="sxs-lookup"><span data-stu-id="52f18-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="52f18-364">Alle andre restbeløbskonti ignoreres.</span><span class="sxs-lookup"><span data-stu-id="52f18-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="52f18-365">Adresseoplysninger</span><span class="sxs-lookup"><span data-stu-id="52f18-365">Address information</span></span>

<span data-ttu-id="52f18-366">Alle medarbejdere skal have én primær placering.</span><span class="sxs-lookup"><span data-stu-id="52f18-366">Every employee must have one primary location.</span></span> <span data-ttu-id="52f18-367">I Dayforce bruges denne placering til at bestemme medarbejderens primære opholdssted til skattemæssige formål.</span><span class="sxs-lookup"><span data-stu-id="52f18-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="52f18-368">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-368">Primary (required)</span></span>
- <span data-ttu-id="52f18-369">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-369">Country/region (required)</span></span>
- <span data-ttu-id="52f18-370">Postnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="52f18-371">Gade (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-371">Street (required)</span></span>
- <span data-ttu-id="52f18-372">Gadenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-372">Street Number (required)</span></span>
- <span data-ttu-id="52f18-373">Bygningskomplement</span><span class="sxs-lookup"><span data-stu-id="52f18-373">Building Complement</span></span>
- <span data-ttu-id="52f18-374">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-374">City (required)</span></span>
- <span data-ttu-id="52f18-375">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-375">State (required)</span></span>
- <span data-ttu-id="52f18-376">Region (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="52f18-377">Konfigurere dataene for at generere løn i USA og Canada</span><span class="sxs-lookup"><span data-stu-id="52f18-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="52f18-378">Hvis du genererer løn for medarbejdere i USA og Canada, skal følgende elementer konfigureres:</span><span class="sxs-lookup"><span data-stu-id="52f18-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="52f18-379">Der kræves afdelinger til stillinger.</span><span class="sxs-lookup"><span data-stu-id="52f18-379">Departments are required on positions.</span></span>
- <span data-ttu-id="52f18-380">Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="52f18-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="52f18-381">Du kan konfigurere Talent til at kræve, at der angives en afdeling for stillinger.</span><span class="sxs-lookup"><span data-stu-id="52f18-381">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="52f18-382">For at gøre dette skal du gå til **Personalets delte stillinger > Stillinger > Kræv afdelinger for stillinger**.</span><span class="sxs-lookup"><span data-stu-id="52f18-382">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="52f18-383">Det anbefales, at denne indstilling gennemtvinges i forbindelse med integrationen.</span><span class="sxs-lookup"><span data-stu-id="52f18-383">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="52f18-384">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="52f18-384">Job types</span></span>

<span data-ttu-id="52f18-385">Jobtyper bruges til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="52f18-385">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="52f18-386">Jobtyper kræves for at behandle løn i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="52f18-386">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="52f18-387">Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="52f18-387">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="52f18-388">Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.</span><span class="sxs-lookup"><span data-stu-id="52f18-388">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="52f18-389">Der kræves følgende jobtyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="52f18-389">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="52f18-390">Jobtype</span><span class="sxs-lookup"><span data-stu-id="52f18-390">Job type</span></span>   | <span data-ttu-id="52f18-391">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="52f18-391">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="52f18-392">Pr. time</span><span class="sxs-lookup"><span data-stu-id="52f18-392">Hourly</span></span>     | <span data-ttu-id="52f18-393">Pr. time</span><span class="sxs-lookup"><span data-stu-id="52f18-393">Hourly</span></span>      |
| <span data-ttu-id="52f18-394">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="52f18-394">Salaried</span></span>   | <span data-ttu-id="52f18-395">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="52f18-395">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="52f18-396">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="52f18-396">Position types</span></span> 

<span data-ttu-id="52f18-397">Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet.</span><span class="sxs-lookup"><span data-stu-id="52f18-397">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="52f18-398">Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="52f18-398">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="52f18-399">Der kræves følgende stillingstyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="52f18-399">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="52f18-400">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="52f18-400">Position type</span></span>   | <span data-ttu-id="52f18-401">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="52f18-401">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="52f18-402">Fuld tid</span><span class="sxs-lookup"><span data-stu-id="52f18-402">Full-time</span></span>       | <span data-ttu-id="52f18-403">Fuldtidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="52f18-403">Full time employee</span></span> |
| <span data-ttu-id="52f18-404">Deltid</span><span class="sxs-lookup"><span data-stu-id="52f18-404">Part-time</span></span>       | <span data-ttu-id="52f18-405">Deltidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="52f18-405">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="52f18-406">Årsagskoder</span><span class="sxs-lookup"><span data-stu-id="52f18-406">Reason codes</span></span>

<span data-ttu-id="52f18-407">Årsagskoder indeholder oplysninger om status for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="52f18-407">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="52f18-408">Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.</span><span class="sxs-lookup"><span data-stu-id="52f18-408">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="52f18-409">Der kræves følgende årsagskoder og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="52f18-409">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="52f18-410">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="52f18-410">Reason code</span></span>    | <span data-ttu-id="52f18-411">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="52f18-411">Description</span></span>      | <span data-ttu-id="52f18-412">Anvendelige scenarier</span><span class="sxs-lookup"><span data-stu-id="52f18-412">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="52f18-413">OPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="52f18-413">RESIGNATION</span></span>    | <span data-ttu-id="52f18-414">Opsigelse</span><span class="sxs-lookup"><span data-stu-id="52f18-414">Resignation</span></span>      | <span data-ttu-id="52f18-415">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="52f18-415">Terminate worker</span></span>     |
| <span data-ttu-id="52f18-416">OPHØR</span><span class="sxs-lookup"><span data-stu-id="52f18-416">TERMINATION</span></span>    | <span data-ttu-id="52f18-417">Ophør</span><span class="sxs-lookup"><span data-stu-id="52f18-417">Termination</span></span>      | <span data-ttu-id="52f18-418">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="52f18-418">Terminate worker</span></span>     |
| <span data-ttu-id="52f18-419">PENSION</span><span class="sxs-lookup"><span data-stu-id="52f18-419">RETIREMENT</span></span>     | <span data-ttu-id="52f18-420">Pension</span><span class="sxs-lookup"><span data-stu-id="52f18-420">Retirement</span></span>       | <span data-ttu-id="52f18-421">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="52f18-421">Terminate worker</span></span>     |
| <span data-ttu-id="52f18-422">ANDET</span><span class="sxs-lookup"><span data-stu-id="52f18-422">OTHER</span></span>          | <span data-ttu-id="52f18-423">Andre årsager</span><span class="sxs-lookup"><span data-stu-id="52f18-423">Other Reasons</span></span>    | <span data-ttu-id="52f18-424">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="52f18-424">Terminate worker</span></span>     |
| <span data-ttu-id="52f18-425">DØDSFALD</span><span class="sxs-lookup"><span data-stu-id="52f18-425">DEATH</span></span>          | <span data-ttu-id="52f18-426">Dødsfald</span><span class="sxs-lookup"><span data-stu-id="52f18-426">Death</span></span>            | <span data-ttu-id="52f18-427">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="52f18-427">Terminate worker</span></span>     |
| <span data-ttu-id="52f18-428">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="52f18-428">LEAVEOFABSENCE</span></span> | <span data-ttu-id="52f18-429">Orlov</span><span class="sxs-lookup"><span data-stu-id="52f18-429">Leave of Absence</span></span> | <span data-ttu-id="52f18-430">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="52f18-430">Terminate worker</span></span>     |
| <span data-ttu-id="52f18-431">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="52f18-431">CONTRACTEND</span></span>    | <span data-ttu-id="52f18-432">Kontraktudløb</span><span class="sxs-lookup"><span data-stu-id="52f18-432">End of Contract</span></span>  | <span data-ttu-id="52f18-433">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="52f18-433">Terminate worker</span></span>     |
| <span data-ttu-id="52f18-434">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="52f18-434">SALARYCHANGE</span></span>   | <span data-ttu-id="52f18-435">Ændring af løn</span><span class="sxs-lookup"><span data-stu-id="52f18-435">Change of Salary</span></span> | <span data-ttu-id="52f18-436">Kompensation</span><span class="sxs-lookup"><span data-stu-id="52f18-436">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="52f18-437">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="52f18-437">Marital status</span></span>

<span data-ttu-id="52f18-438">Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="52f18-438">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="52f18-439">Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="52f18-439">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="52f18-440">Talent</span><span class="sxs-lookup"><span data-stu-id="52f18-440">Talent</span></span>                 | <span data-ttu-id="52f18-441">Dayforce</span><span class="sxs-lookup"><span data-stu-id="52f18-441">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="52f18-442">Gift</span><span class="sxs-lookup"><span data-stu-id="52f18-442">Married</span></span>                | <span data-ttu-id="52f18-443">Gift</span><span class="sxs-lookup"><span data-stu-id="52f18-443">Married</span></span>              |
| <span data-ttu-id="52f18-444">Enlig</span><span class="sxs-lookup"><span data-stu-id="52f18-444">Single</span></span>                 | <span data-ttu-id="52f18-445">Enlig</span><span class="sxs-lookup"><span data-stu-id="52f18-445">Single</span></span>               |
| <span data-ttu-id="52f18-446">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="52f18-446">Widowed</span></span>                | <span data-ttu-id="52f18-447">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="52f18-447">Widowed</span></span>              |
| <span data-ttu-id="52f18-448">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="52f18-448">Divorced</span></span>               | <span data-ttu-id="52f18-449">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="52f18-449">Divorced</span></span>             |
| <span data-ttu-id="52f18-450">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="52f18-450">Registered Partnership</span></span> | <span data-ttu-id="52f18-451">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="52f18-451">Domestic Partnership</span></span> |
| <span data-ttu-id="52f18-452">None</span><span class="sxs-lookup"><span data-stu-id="52f18-452">None</span></span>                   | <span data-ttu-id="52f18-453">None</span><span class="sxs-lookup"><span data-stu-id="52f18-453">None</span></span>                 |
| <span data-ttu-id="52f18-454">Samlever</span><span class="sxs-lookup"><span data-stu-id="52f18-454">Cohabiting</span></span>             | <span data-ttu-id="52f18-455">Samlever</span><span class="sxs-lookup"><span data-stu-id="52f18-455">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="52f18-456">Køn</span><span class="sxs-lookup"><span data-stu-id="52f18-456">Gender</span></span>

<span data-ttu-id="52f18-457">Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="52f18-457">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="52f18-458">Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="52f18-458">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="52f18-459">Talent</span><span class="sxs-lookup"><span data-stu-id="52f18-459">Talent</span></span>       | <span data-ttu-id="52f18-460">Dayforce</span><span class="sxs-lookup"><span data-stu-id="52f18-460">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="52f18-461">Mand</span><span class="sxs-lookup"><span data-stu-id="52f18-461">Male</span></span>         | <span data-ttu-id="52f18-462">Mand</span><span class="sxs-lookup"><span data-stu-id="52f18-462">Male</span></span>            |
| <span data-ttu-id="52f18-463">Kvinde</span><span class="sxs-lookup"><span data-stu-id="52f18-463">Female</span></span>       | <span data-ttu-id="52f18-464">Kvinde</span><span class="sxs-lookup"><span data-stu-id="52f18-464">Female</span></span>          |
| <span data-ttu-id="52f18-465">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="52f18-465">Non-specific</span></span> | <span data-ttu-id="52f18-466">*Understøttes ikke*</span><span class="sxs-lookup"><span data-stu-id="52f18-466">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="52f18-467">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="52f18-467">Earning codes</span></span>

<span data-ttu-id="52f18-468">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="52f18-468">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="52f18-469">Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="52f18-469">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="52f18-470">Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="52f18-470">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="52f18-471">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="52f18-471">Supported frequencies</span></span>

- <span data-ttu-id="52f18-472">Alt</span><span class="sxs-lookup"><span data-stu-id="52f18-472">All</span></span>
- <span data-ttu-id="52f18-473">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="52f18-473">EVERYPAY</span></span>
- <span data-ttu-id="52f18-474">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="52f18-474">EACHPAYPERIOD</span></span>
- <span data-ttu-id="52f18-475">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="52f18-475">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="52f18-476">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="52f18-476">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="52f18-477">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-477">1OFMTH</span></span>
- <span data-ttu-id="52f18-478">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-478">LASTOFMTH</span></span>
- <span data-ttu-id="52f18-479">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-479">2OFMTH</span></span>
- <span data-ttu-id="52f18-480">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-480">3OFMTH</span></span>
- <span data-ttu-id="52f18-481">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-481">4OFMTH</span></span>
- <span data-ttu-id="52f18-482">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-482">5OFMTH</span></span>
- <span data-ttu-id="52f18-483">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-483">1N2OFMTH</span></span>
- <span data-ttu-id="52f18-484">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-484">3N4OFMTH</span></span>
- <span data-ttu-id="52f18-485">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-485">1N3OFMTH</span></span>
- <span data-ttu-id="52f18-486">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-486">1N4OFMTH</span></span>
- <span data-ttu-id="52f18-487">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-487">2N3OFMTH</span></span>
- <span data-ttu-id="52f18-488">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-488">2N4OFMTH</span></span>
- <span data-ttu-id="52f18-489">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-489">1N2N3OFMTH</span></span>
- <span data-ttu-id="52f18-490">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-490">1N2N4OFMTH</span></span>
- <span data-ttu-id="52f18-491">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-491">1N3N4OFMTH</span></span>
- <span data-ttu-id="52f18-492">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-492">2N3N4OFMTH</span></span>
- <span data-ttu-id="52f18-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="52f18-494">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="52f18-494">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="52f18-495">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="52f18-495">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="52f18-496">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="52f18-496">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="52f18-497">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="52f18-497">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="52f18-498">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="52f18-498">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="52f18-499">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="52f18-499">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="52f18-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="52f18-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="52f18-501">Adresser</span><span class="sxs-lookup"><span data-stu-id="52f18-501">Addresses</span></span>

<span data-ttu-id="52f18-502">Identifikation af specifikke koder for land eller region, stat og område (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende.</span><span class="sxs-lookup"><span data-stu-id="52f18-502">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="52f18-503">Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.</span><span class="sxs-lookup"><span data-stu-id="52f18-503">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="52f18-504">Talent</span><span class="sxs-lookup"><span data-stu-id="52f18-504">Talent</span></span>          | <span data-ttu-id="52f18-505">Dayforce</span><span class="sxs-lookup"><span data-stu-id="52f18-505">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="52f18-506">Land/område</span><span class="sxs-lookup"><span data-stu-id="52f18-506">Country/Region</span></span>  | <span data-ttu-id="52f18-507">Landekode</span><span class="sxs-lookup"><span data-stu-id="52f18-507">Country Code</span></span>          |
| <span data-ttu-id="52f18-508">Postnummer</span><span class="sxs-lookup"><span data-stu-id="52f18-508">Zip/Postal Code</span></span> | <span data-ttu-id="52f18-509">Postnummer</span><span class="sxs-lookup"><span data-stu-id="52f18-509">Postal Code</span></span>           |
| <span data-ttu-id="52f18-510">Status</span><span class="sxs-lookup"><span data-stu-id="52f18-510">State</span></span>           | <span data-ttu-id="52f18-511">Statskode</span><span class="sxs-lookup"><span data-stu-id="52f18-511">State Code</span></span>            |
| <span data-ttu-id="52f18-512">Bynavn</span><span class="sxs-lookup"><span data-stu-id="52f18-512">City</span></span>            | <span data-ttu-id="52f18-513">Bynavn</span><span class="sxs-lookup"><span data-stu-id="52f18-513">City</span></span>                  |
| <span data-ttu-id="52f18-514">Region</span><span class="sxs-lookup"><span data-stu-id="52f18-514">County</span></span>          | <span data-ttu-id="52f18-515">Område (kommune)</span><span class="sxs-lookup"><span data-stu-id="52f18-515">County (Municipality)</span></span> |
| <span data-ttu-id="52f18-516">Gade</span><span class="sxs-lookup"><span data-stu-id="52f18-516">Street</span></span>          | <span data-ttu-id="52f18-517">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="52f18-517">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="52f18-518">Skatteområder</span><span class="sxs-lookup"><span data-stu-id="52f18-518">Tax regions</span></span>

<span data-ttu-id="52f18-519">Skatteområder bruges til at bestemme den relevante skat, der skal anvendes ved løngenerering.</span><span class="sxs-lookup"><span data-stu-id="52f18-519">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="52f18-520">Skatteområder er tilknyttet Dayforce som placeringsadresser.</span><span class="sxs-lookup"><span data-stu-id="52f18-520">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="52f18-521">Standardskatteområder skal knyttes til arbejderens aktive stilling.</span><span class="sxs-lookup"><span data-stu-id="52f18-521">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="52f18-522">Skatteområde (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-522">Tax region (required)</span></span>
- <span data-ttu-id="52f18-523">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-523">Country/Region (required)</span></span>
- <span data-ttu-id="52f18-524">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-524">State (required)</span></span>
- <span data-ttu-id="52f18-525">Region</span><span class="sxs-lookup"><span data-stu-id="52f18-525">County</span></span> 
- <span data-ttu-id="52f18-526">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="52f18-526">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="52f18-527">Konfigurere dataene for at generere løn i Mexico</span><span class="sxs-lookup"><span data-stu-id="52f18-527">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="52f18-528">Hvis du genererer løn for medarbejdere i Mexico skal følgende elementer konfigureres:</span><span class="sxs-lookup"><span data-stu-id="52f18-528">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="52f18-529">Der kræves afdelinger til stillinger.</span><span class="sxs-lookup"><span data-stu-id="52f18-529">Departments are required on positions.</span></span>
- <span data-ttu-id="52f18-530">Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="52f18-530">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="52f18-531">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="52f18-531">Job types</span></span>

<span data-ttu-id="52f18-532">Jobtyper bruges til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="52f18-532">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="52f18-533">Jobtyper kræves for at behandle løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="52f18-533">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="52f18-534">Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="52f18-534">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="52f18-535">Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.</span><span class="sxs-lookup"><span data-stu-id="52f18-535">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="52f18-536">Der kræves følgende jobtyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="52f18-536">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="52f18-537">Jobtype</span><span class="sxs-lookup"><span data-stu-id="52f18-537">Job type</span></span>   | <span data-ttu-id="52f18-538">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="52f18-538">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="52f18-539">Pr. time</span><span class="sxs-lookup"><span data-stu-id="52f18-539">Hourly</span></span>     | <span data-ttu-id="52f18-540">MX Pr. time</span><span class="sxs-lookup"><span data-stu-id="52f18-540">MX Hourly</span></span>   |
| <span data-ttu-id="52f18-541">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="52f18-541">Salaried</span></span>   | <span data-ttu-id="52f18-542">MX Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="52f18-542">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="52f18-543">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="52f18-543">Position types</span></span> 

<span data-ttu-id="52f18-544">Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet.</span><span class="sxs-lookup"><span data-stu-id="52f18-544">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="52f18-545">Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="52f18-545">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="52f18-546">Der kræves følgende stillingstyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="52f18-546">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="52f18-547">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="52f18-547">Position type</span></span>   | <span data-ttu-id="52f18-548">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="52f18-548">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="52f18-549">Fuld tid</span><span class="sxs-lookup"><span data-stu-id="52f18-549">Full-time</span></span>       | <span data-ttu-id="52f18-550">Fuldtidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="52f18-550">Full time employee</span></span> |
| <span data-ttu-id="52f18-551">Deltid</span><span class="sxs-lookup"><span data-stu-id="52f18-551">Part-time</span></span>       | <span data-ttu-id="52f18-552">Deltidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="52f18-552">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="52f18-553">Årsagskoder</span><span class="sxs-lookup"><span data-stu-id="52f18-553">Reason codes</span></span>

<span data-ttu-id="52f18-554">Årsagskoder indeholder oplysninger om status for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="52f18-554">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="52f18-555">Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.</span><span class="sxs-lookup"><span data-stu-id="52f18-555">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="52f18-556">Der kræves følgende årsagskoder og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="52f18-556">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="52f18-557">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="52f18-557">Reason code</span></span>            | <span data-ttu-id="52f18-558">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="52f18-558">Description</span></span>                    | <span data-ttu-id="52f18-559">Anvendelige scenarier</span><span class="sxs-lookup"><span data-stu-id="52f18-559">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="52f18-560">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="52f18-560">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="52f18-561">Afgang før første løn</span><span class="sxs-lookup"><span data-stu-id="52f18-561">Departure before first payroll</span></span> | <span data-ttu-id="52f18-562">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="52f18-562">Terminate worker</span></span>     |
| <span data-ttu-id="52f18-563">OPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="52f18-563">RESIGNATION</span></span>            | <span data-ttu-id="52f18-564">Opsigelse</span><span class="sxs-lookup"><span data-stu-id="52f18-564">Resignation</span></span>                    | <span data-ttu-id="52f18-565">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="52f18-565">Terminate worker</span></span>     |
| <span data-ttu-id="52f18-566">PENSION</span><span class="sxs-lookup"><span data-stu-id="52f18-566">PENSION</span></span>                | <span data-ttu-id="52f18-567">Pension</span><span class="sxs-lookup"><span data-stu-id="52f18-567">Pension</span></span>                        | <span data-ttu-id="52f18-568">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="52f18-568">Terminate worker</span></span>     |
| <span data-ttu-id="52f18-569">OPHØR</span><span class="sxs-lookup"><span data-stu-id="52f18-569">TERMINATION</span></span>            | <span data-ttu-id="52f18-570">Ophør</span><span class="sxs-lookup"><span data-stu-id="52f18-570">Termination</span></span>                    | <span data-ttu-id="52f18-571">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="52f18-571">Terminate worker</span></span>     |
| <span data-ttu-id="52f18-572">PENSION</span><span class="sxs-lookup"><span data-stu-id="52f18-572">RETIREMENT</span></span>             | <span data-ttu-id="52f18-573">Pension</span><span class="sxs-lookup"><span data-stu-id="52f18-573">Retirement</span></span>                     | <span data-ttu-id="52f18-574">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="52f18-574">Terminate worker</span></span>     |
| <span data-ttu-id="52f18-575">FRAVÆRENDE</span><span class="sxs-lookup"><span data-stu-id="52f18-575">ABSENTEE</span></span>               | <span data-ttu-id="52f18-576">Fraværende</span><span class="sxs-lookup"><span data-stu-id="52f18-576">Absentee</span></span>                       | <span data-ttu-id="52f18-577">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="52f18-577">Terminate worker</span></span>     |
| <span data-ttu-id="52f18-578">ANDET</span><span class="sxs-lookup"><span data-stu-id="52f18-578">OTHER</span></span>                  | <span data-ttu-id="52f18-579">Andre årsager</span><span class="sxs-lookup"><span data-stu-id="52f18-579">Other Reasons</span></span>                  | <span data-ttu-id="52f18-580">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="52f18-580">Terminate worker</span></span>     |
| <span data-ttu-id="52f18-581">LUKNING</span><span class="sxs-lookup"><span data-stu-id="52f18-581">CLOSURE</span></span>                | <span data-ttu-id="52f18-582">Virksomhedslukning</span><span class="sxs-lookup"><span data-stu-id="52f18-582">Business Closure</span></span>               | <span data-ttu-id="52f18-583">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="52f18-583">Terminate worker</span></span>     |
| <span data-ttu-id="52f18-584">DØDSFALD</span><span class="sxs-lookup"><span data-stu-id="52f18-584">DEATH</span></span>                  | <span data-ttu-id="52f18-585">Dødsfald</span><span class="sxs-lookup"><span data-stu-id="52f18-585">Death</span></span>                          | <span data-ttu-id="52f18-586">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="52f18-586">Terminate worker</span></span>     |
| <span data-ttu-id="52f18-587">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="52f18-587">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="52f18-588">Orlov</span><span class="sxs-lookup"><span data-stu-id="52f18-588">Leave of Absence</span></span>               | <span data-ttu-id="52f18-589">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="52f18-589">Terminate worker</span></span>     |
| <span data-ttu-id="52f18-590">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="52f18-590">CONTRACTEND</span></span>            | <span data-ttu-id="52f18-591">Kontraktudløb</span><span class="sxs-lookup"><span data-stu-id="52f18-591">End of Contract</span></span>                | <span data-ttu-id="52f18-592">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="52f18-592">Terminate worker</span></span>     |
| <span data-ttu-id="52f18-593">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="52f18-593">SALARYCHANGE</span></span>           | <span data-ttu-id="52f18-594">Ændring af løn</span><span class="sxs-lookup"><span data-stu-id="52f18-594">Change of Salary</span></span>               | <span data-ttu-id="52f18-595">Kompensation</span><span class="sxs-lookup"><span data-stu-id="52f18-595">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="52f18-596">Ansættelsesvilkår</span><span class="sxs-lookup"><span data-stu-id="52f18-596">Terms of employment</span></span>

<span data-ttu-id="52f18-597">Ansættelsesvilkår bruges til at oprette kategorier for ansættelsesvilkår.</span><span class="sxs-lookup"><span data-stu-id="52f18-597">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="52f18-598">Vilkårene knyttes til Dayforce som beskæftigelsesindikatorværdier.</span><span class="sxs-lookup"><span data-stu-id="52f18-598">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="52f18-599">Følgende begreber for beskæftigelse og beskrivelser er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="52f18-599">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="52f18-600">Ansættelsesvilkår</span><span class="sxs-lookup"><span data-stu-id="52f18-600">Terms of employment</span></span>   | <span data-ttu-id="52f18-601">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="52f18-601">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="52f18-602">Regulær</span><span class="sxs-lookup"><span data-stu-id="52f18-602">Regular</span></span>               | <span data-ttu-id="52f18-603">Regulær</span><span class="sxs-lookup"><span data-stu-id="52f18-603">Regular</span></span>     |
| <span data-ttu-id="52f18-604">Direkte</span><span class="sxs-lookup"><span data-stu-id="52f18-604">Direct</span></span>                | <span data-ttu-id="52f18-605">Direkte</span><span class="sxs-lookup"><span data-stu-id="52f18-605">Direct</span></span>      |
| <span data-ttu-id="52f18-606">Turnustjeneste</span><span class="sxs-lookup"><span data-stu-id="52f18-606">Internship</span></span>            | <span data-ttu-id="52f18-607">Turnustjeneste</span><span class="sxs-lookup"><span data-stu-id="52f18-607">Internship</span></span>  |
| <span data-ttu-id="52f18-608">Permanent</span><span class="sxs-lookup"><span data-stu-id="52f18-608">Permanent</span></span>             | <span data-ttu-id="52f18-609">Permanent</span><span class="sxs-lookup"><span data-stu-id="52f18-609">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="52f18-610">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="52f18-610">Marital status</span></span>

<span data-ttu-id="52f18-611">Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="52f18-611">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="52f18-612">Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="52f18-612">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="52f18-613">Talent</span><span class="sxs-lookup"><span data-stu-id="52f18-613">Talent</span></span>                 | <span data-ttu-id="52f18-614">Dayforce</span><span class="sxs-lookup"><span data-stu-id="52f18-614">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="52f18-615">Gift</span><span class="sxs-lookup"><span data-stu-id="52f18-615">Married</span></span>                | <span data-ttu-id="52f18-616">Gift</span><span class="sxs-lookup"><span data-stu-id="52f18-616">Married</span></span>                   |
| <span data-ttu-id="52f18-617">Enlig</span><span class="sxs-lookup"><span data-stu-id="52f18-617">Single</span></span>                 | <span data-ttu-id="52f18-618">Enlig</span><span class="sxs-lookup"><span data-stu-id="52f18-618">Single</span></span>                    |
| <span data-ttu-id="52f18-619">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="52f18-619">Widowed</span></span>                | <span data-ttu-id="52f18-620">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="52f18-620">Widowed</span></span>                   |
| <span data-ttu-id="52f18-621">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="52f18-621">Divorced</span></span>               | <span data-ttu-id="52f18-622">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="52f18-622">Divorced</span></span>                  |
| <span data-ttu-id="52f18-623">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="52f18-623">Registered Partnership</span></span> | <span data-ttu-id="52f18-624">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="52f18-624">Domestic Partnership</span></span>      |
| <span data-ttu-id="52f18-625">None</span><span class="sxs-lookup"><span data-stu-id="52f18-625">None</span></span>                   | <span data-ttu-id="52f18-626">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="52f18-626">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="52f18-627">Samlever</span><span class="sxs-lookup"><span data-stu-id="52f18-627">Cohabiting</span></span>             | <span data-ttu-id="52f18-628">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="52f18-628">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="52f18-629">Køn</span><span class="sxs-lookup"><span data-stu-id="52f18-629">Gender</span></span>

<span data-ttu-id="52f18-630">Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="52f18-630">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="52f18-631">Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="52f18-631">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="52f18-632">Talent</span><span class="sxs-lookup"><span data-stu-id="52f18-632">Talent</span></span>       | <span data-ttu-id="52f18-633">Dayforce</span><span class="sxs-lookup"><span data-stu-id="52f18-633">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="52f18-634">Mand</span><span class="sxs-lookup"><span data-stu-id="52f18-634">Male</span></span>         | <span data-ttu-id="52f18-635">Mand</span><span class="sxs-lookup"><span data-stu-id="52f18-635">Male</span></span>                      |
| <span data-ttu-id="52f18-636">Kvinde</span><span class="sxs-lookup"><span data-stu-id="52f18-636">Female</span></span>       | <span data-ttu-id="52f18-637">Kvinde</span><span class="sxs-lookup"><span data-stu-id="52f18-637">Female</span></span>                    |
| <span data-ttu-id="52f18-638">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="52f18-638">Non-specific</span></span> | <span data-ttu-id="52f18-639">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="52f18-639">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="52f18-640">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="52f18-640">Payment method</span></span>

<span data-ttu-id="52f18-641">Betalingsmetoder giver medarbejderen og virksomheden en måde til at beskrive, hvordan medarbejdere skal betales.</span><span class="sxs-lookup"><span data-stu-id="52f18-641">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="52f18-642">Betalingsmåder knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="52f18-642">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="52f18-643">Følgende tabel viser, hvordan betalingsmetoder knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="52f18-643">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="52f18-644">Talent</span><span class="sxs-lookup"><span data-stu-id="52f18-644">Talent</span></span>             | <span data-ttu-id="52f18-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="52f18-645">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="52f18-646">Indløsning</span><span class="sxs-lookup"><span data-stu-id="52f18-646">Cash</span></span>               | <span data-ttu-id="52f18-647">Indløsning</span><span class="sxs-lookup"><span data-stu-id="52f18-647">Cash</span></span>                      |
| <span data-ttu-id="52f18-648">Elektronisk betaling</span><span class="sxs-lookup"><span data-stu-id="52f18-648">Electronic Payment</span></span> | <span data-ttu-id="52f18-649">Ompostering</span><span class="sxs-lookup"><span data-stu-id="52f18-649">Transfer</span></span>                  |
| <span data-ttu-id="52f18-650">Check</span><span class="sxs-lookup"><span data-stu-id="52f18-650">Check</span></span>              | <span data-ttu-id="52f18-651">Check</span><span class="sxs-lookup"><span data-stu-id="52f18-651">Cheque</span></span>                    |
| <span data-ttu-id="52f18-652">Bankanvisning</span><span class="sxs-lookup"><span data-stu-id="52f18-652">Bank Draft</span></span>         | <span data-ttu-id="52f18-653">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="52f18-653">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="52f18-654">Andre</span><span class="sxs-lookup"><span data-stu-id="52f18-654">Other</span></span>              | <span data-ttu-id="52f18-655">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="52f18-655">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="52f18-656">Bankkontotype</span><span class="sxs-lookup"><span data-stu-id="52f18-656">Bank account type</span></span>

<span data-ttu-id="52f18-657">Bankkontotyper bruges til elektroniske betalinger til medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="52f18-657">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="52f18-658">Bankkontotyper knyttes til Dayforce som overførselskontooplysninger.</span><span class="sxs-lookup"><span data-stu-id="52f18-658">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="52f18-659">Bankkontotyperne oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="52f18-659">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="52f18-660">Talent</span><span class="sxs-lookup"><span data-stu-id="52f18-660">Talent</span></span>            | <span data-ttu-id="52f18-661">Dayforce</span><span class="sxs-lookup"><span data-stu-id="52f18-661">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="52f18-662">Checkkonto</span><span class="sxs-lookup"><span data-stu-id="52f18-662">Checking Account</span></span>  | <span data-ttu-id="52f18-663">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="52f18-663">CheckingAccount</span></span>           |
| <span data-ttu-id="52f18-664">Lønkonto</span><span class="sxs-lookup"><span data-stu-id="52f18-664">Payroll Account</span></span>   | <span data-ttu-id="52f18-665">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="52f18-665">PayrollAccount</span></span>            |
| <span data-ttu-id="52f18-666">Opsparingskonto</span><span class="sxs-lookup"><span data-stu-id="52f18-666">Savings Account</span></span>   | <span data-ttu-id="52f18-667">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="52f18-667">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="52f18-668">BankGirot-konto</span><span class="sxs-lookup"><span data-stu-id="52f18-668">BankGirot account</span></span> | <span data-ttu-id="52f18-669">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="52f18-669">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="52f18-670">PlusGirot-konto</span><span class="sxs-lookup"><span data-stu-id="52f18-670">PlusGirot account</span></span> | <span data-ttu-id="52f18-671">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="52f18-671">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="52f18-672">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="52f18-672">Earning codes</span></span>

<span data-ttu-id="52f18-673">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="52f18-673">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="52f18-674">Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="52f18-674">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="52f18-675">Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="52f18-675">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="52f18-676">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="52f18-676">Supported frequencies</span></span>

- <span data-ttu-id="52f18-677">Alt</span><span class="sxs-lookup"><span data-stu-id="52f18-677">All</span></span>
- <span data-ttu-id="52f18-678">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="52f18-678">EVERYPAY</span></span>
- <span data-ttu-id="52f18-679">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="52f18-679">EACHPAYPERIOD</span></span>
- <span data-ttu-id="52f18-680">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="52f18-680">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="52f18-681">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="52f18-681">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="52f18-682">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-682">1OFMTH</span></span>
- <span data-ttu-id="52f18-683">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-683">LASTOFMTH</span></span>
- <span data-ttu-id="52f18-684">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-684">2OFMTH</span></span>
- <span data-ttu-id="52f18-685">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-685">3OFMTH</span></span>
- <span data-ttu-id="52f18-686">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-686">4OFMTH</span></span>
- <span data-ttu-id="52f18-687">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-687">5OFMTH</span></span>
- <span data-ttu-id="52f18-688">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-688">1N2OFMTH</span></span>
- <span data-ttu-id="52f18-689">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-689">3N4OFMTH</span></span>
- <span data-ttu-id="52f18-690">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-690">1N3OFMTH</span></span>
- <span data-ttu-id="52f18-691">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-691">1N4OFMTH</span></span>
- <span data-ttu-id="52f18-692">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-692">2N3OFMTH</span></span>
- <span data-ttu-id="52f18-693">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-693">2N4OFMTH</span></span>
- <span data-ttu-id="52f18-694">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-694">1N2N3OFMTH</span></span>
- <span data-ttu-id="52f18-695">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-695">1N2N4OFMTH</span></span>
- <span data-ttu-id="52f18-696">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-696">1N3N4OFMTH</span></span>
- <span data-ttu-id="52f18-697">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-697">2N3N4OFMTH</span></span>
- <span data-ttu-id="52f18-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="52f18-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="52f18-699">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="52f18-699">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="52f18-700">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="52f18-700">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="52f18-701">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="52f18-701">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="52f18-702">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="52f18-702">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="52f18-703">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="52f18-703">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="52f18-704">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="52f18-704">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="52f18-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="52f18-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="52f18-706">Adresser</span><span class="sxs-lookup"><span data-stu-id="52f18-706">Addresses</span></span>

<span data-ttu-id="52f18-707">Identifikation af specifikke koder for land eller region, stat og område (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende.</span><span class="sxs-lookup"><span data-stu-id="52f18-707">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="52f18-708">Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.</span><span class="sxs-lookup"><span data-stu-id="52f18-708">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="52f18-709">Talent</span><span class="sxs-lookup"><span data-stu-id="52f18-709">Talent</span></span>              | <span data-ttu-id="52f18-710">Dayforce</span><span class="sxs-lookup"><span data-stu-id="52f18-710">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="52f18-711">Land/område</span><span class="sxs-lookup"><span data-stu-id="52f18-711">Country/Region</span></span>      | <span data-ttu-id="52f18-712">Landekode</span><span class="sxs-lookup"><span data-stu-id="52f18-712">Country Code</span></span>          |
| <span data-ttu-id="52f18-713">Postnummer</span><span class="sxs-lookup"><span data-stu-id="52f18-713">Zip/Postal Code</span></span>     | <span data-ttu-id="52f18-714">Postnummer</span><span class="sxs-lookup"><span data-stu-id="52f18-714">Postal Code</span></span>           |
| <span data-ttu-id="52f18-715">Status</span><span class="sxs-lookup"><span data-stu-id="52f18-715">State</span></span>               | <span data-ttu-id="52f18-716">Statskode</span><span class="sxs-lookup"><span data-stu-id="52f18-716">State Code</span></span>            |
| <span data-ttu-id="52f18-717">Bynavn</span><span class="sxs-lookup"><span data-stu-id="52f18-717">City</span></span>                | <span data-ttu-id="52f18-718">Bynavn</span><span class="sxs-lookup"><span data-stu-id="52f18-718">City</span></span>                  |
| <span data-ttu-id="52f18-719">Region</span><span class="sxs-lookup"><span data-stu-id="52f18-719">County</span></span>              | <span data-ttu-id="52f18-720">Område (kommune)</span><span class="sxs-lookup"><span data-stu-id="52f18-720">County (Municipality)</span></span> |
| <span data-ttu-id="52f18-721">Gade</span><span class="sxs-lookup"><span data-stu-id="52f18-721">Street</span></span>              | <span data-ttu-id="52f18-722">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="52f18-722">Address Line 1</span></span>        |
| <span data-ttu-id="52f18-723">Gadenummer</span><span class="sxs-lookup"><span data-stu-id="52f18-723">Street Number</span></span>       | <span data-ttu-id="52f18-724">Adresselinje 2</span><span class="sxs-lookup"><span data-stu-id="52f18-724">Address Line 2</span></span>        |
| <span data-ttu-id="52f18-725">Bygningskomplement</span><span class="sxs-lookup"><span data-stu-id="52f18-725">Building Complement</span></span> | <span data-ttu-id="52f18-726">Adresselinje 5</span><span class="sxs-lookup"><span data-stu-id="52f18-726">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="52f18-727">Pasnummer</span><span class="sxs-lookup"><span data-stu-id="52f18-727">Passport number</span></span>

<span data-ttu-id="52f18-728">Medarbejdere kan erklære pasoplysninger.</span><span class="sxs-lookup"><span data-stu-id="52f18-728">Employees can declare passport information.</span></span> <span data-ttu-id="52f18-729">Disse oplysninger er af identifikationstypen **Pas** og er integreret i Dayforce som en del af en medarbejders Mexico-specifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="52f18-729">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="52f18-730">Identifikationstype = "Pas"</span><span class="sxs-lookup"><span data-stu-id="52f18-730">Identification Type = "Passport"</span></span>
- <span data-ttu-id="52f18-731">Udstedt den</span><span class="sxs-lookup"><span data-stu-id="52f18-731">Issued Date</span></span>
- <span data-ttu-id="52f18-732">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="52f18-732">Expiration Date</span></span>

<span data-ttu-id="52f18-733">Medarbejdere kan angive flere identifikationsnumre af **Pas**-identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="52f18-733">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="52f18-734">Men det er kun den aktuelle aktive paspost, der integreres i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="52f18-734">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="52f18-735">Hvis alle pasposter er udløbet, integreres det pas, der senest blev udstedt, i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="52f18-735">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
