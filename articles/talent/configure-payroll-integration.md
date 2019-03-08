---
title: Konfigurere lønintegration mellem Talent og Dayforce
description: Dette emne forklarer, hvordan du kan konfigurere integration mellem Microsoft Dynamics 365 for Talent og Ceridian Dayforce, så du kan behandle en lønkørsel.
author: jcart1106
manager: AnnBe
ms.date: 07/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fcddf82cffb9f0ba94b83eb21809b810585ebc9e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "303709"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="a293e-103">Konfigurere lønintegrationen mellem Talent og Dayforce</span><span class="sxs-lookup"><span data-stu-id="a293e-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a293e-104">Integration mellem Microsoft Dynamics 365 for Talent og Ceridian Dayforce er baseret på flere konfigurationstrin, der er beskrevet i dette emne.</span><span class="sxs-lookup"><span data-stu-id="a293e-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="a293e-105">Du skal konfigurere integrationen i både Talent og Dayforce, før du kan behandle en lønkørsel.</span><span class="sxs-lookup"><span data-stu-id="a293e-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="a293e-106">Når du bruger en tjeneste, f.eks. Dayforce, til at fuldføre lønkørsler, skal du aktivere integrationen i Talent.</span><span class="sxs-lookup"><span data-stu-id="a293e-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="a293e-107">Integrationen kræver bestemte data fra Talent.</span><span class="sxs-lookup"><span data-stu-id="a293e-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="a293e-108">Du skal derfor kontrollere, at data, der er knyttet til Dayforce, er konfigureret i Talent på en måde, der understøtter integrationen.</span><span class="sxs-lookup"><span data-stu-id="a293e-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="a293e-109">Integrationen bruger følgende brede kategorier af data.</span><span class="sxs-lookup"><span data-stu-id="a293e-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="a293e-110">Personaledata</span><span class="sxs-lookup"><span data-stu-id="a293e-110">Human resources data</span></span>
- <span data-ttu-id="a293e-111">Kompensationsdata</span><span class="sxs-lookup"><span data-stu-id="a293e-111">Compensation data</span></span>
- <span data-ttu-id="a293e-112">Lønoplysninger, f.eks. løncyklusser, betalingsperioder og lønkoder</span><span class="sxs-lookup"><span data-stu-id="a293e-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="a293e-113">Arbejderdata</span><span class="sxs-lookup"><span data-stu-id="a293e-113">Worker data</span></span>

<span data-ttu-id="a293e-114">Dette emne beskrives de trin, du skal udføre for at aktivere integrationen.</span><span class="sxs-lookup"><span data-stu-id="a293e-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="a293e-115">Det forklarer også typerne af data og oplysninger om konfigurationen, der kræves til integrationen.</span><span class="sxs-lookup"><span data-stu-id="a293e-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="a293e-116">Aktivere integrationen.</span><span class="sxs-lookup"><span data-stu-id="a293e-116">Enable the integration</span></span>

<span data-ttu-id="a293e-117">I Talent skal du aktivere integrationen og angive konfigurationsoplysningerne for at oprette forbindelse til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="a293e-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="a293e-118">Hvis den finanspostering, der er produceret, skal importeres til Microsoft Dynamics 365 for Finance and Operations, skal du også konfigurere en Microsoft Azure-lagerkonto og angive Azure-lagerets forbindelsesstreng i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a293e-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="a293e-119">Følg disse trin for at aktivere integrationen i Talent.</span><span class="sxs-lookup"><span data-stu-id="a293e-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="a293e-120">På siden **Systemadministration** skal du vælge **Integrationskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="a293e-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="a293e-121">Angiv det sikre FTP-slutpunkt og den sikre FTP-mappesti.</span><span class="sxs-lookup"><span data-stu-id="a293e-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="a293e-122">Angiv brugernavnet og adgangskoden for den bruger, der skal have adgang til det sikre FTP-slutpunkt og den sikre mappesti.</span><span class="sxs-lookup"><span data-stu-id="a293e-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="a293e-123">Test forbindelsen, som krævet, og angiv indstillingen **Aktivér lønintegration** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a293e-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="a293e-124">Når integrationen er aktiveret, oprettes dataeksportpakken og -filerne, og hyppigheden angives.</span><span class="sxs-lookup"><span data-stu-id="a293e-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="a293e-125">Du kan ændre denne frekvens efter behov.</span><span class="sxs-lookup"><span data-stu-id="a293e-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="a293e-126">Yderligere oplysninger om Azure-lagerkonti og Azure-lagerforbindelsesstrenge finder du i følgende Azure-emner:</span><span class="sxs-lookup"><span data-stu-id="a293e-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="a293e-127">Om Azure-lagerkonti</span><span class="sxs-lookup"><span data-stu-id="a293e-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="a293e-128">Konfigurere forbindelsesstrenge for Azure-datalager</span><span class="sxs-lookup"><span data-stu-id="a293e-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="a293e-129">Konfigurere dine data</span><span class="sxs-lookup"><span data-stu-id="a293e-129">Configure your data</span></span> 

<span data-ttu-id="a293e-130">Hvis du vil behandle løn, skal du konfigurere personaledata i Talent.</span><span class="sxs-lookup"><span data-stu-id="a293e-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="a293e-131">Du skal angive virksomhedens data, f.eks. job og stillinger, sammen med frynsegoder og kompensationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="a293e-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="a293e-132">Disse oplysninger indeholder oplysningerne om ansættelse, løn og fradrag, der kræves for at generere løn for medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="a293e-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="a293e-133">Personaledata</span><span class="sxs-lookup"><span data-stu-id="a293e-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="a293e-134">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="a293e-134">Benefits</span></span> 

<span data-ttu-id="a293e-135">Personale indeholder en række værktøjer til konfiguration og vedligeholdelse af frynsegoder, fradrag og arbejderkompensationsplaner, som en organisation tilbyder eller behandler for sine ansatte.</span><span class="sxs-lookup"><span data-stu-id="a293e-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="a293e-136">Når du opretter frynsegoder, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="a293e-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="a293e-137">Frynsegodeplaner</span><span class="sxs-lookup"><span data-stu-id="a293e-137">Benefit plans</span></span>

- <span data-ttu-id="a293e-138">Plan (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-138">Plan (required)</span></span>
- <span data-ttu-id="a293e-139">Type (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-139">Type (required)</span></span>
- <span data-ttu-id="a293e-140">Løneffekt (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-140">Payroll impact (required)</span></span>
- <span data-ttu-id="a293e-141">Opkræv restancer</span><span class="sxs-lookup"><span data-stu-id="a293e-141">Recover arrears</span></span>
- <span data-ttu-id="a293e-142">Fradragsmetode</span><span class="sxs-lookup"><span data-stu-id="a293e-142">Deduction method</span></span>
- <span data-ttu-id="a293e-143">Prioriteret fradrag</span><span class="sxs-lookup"><span data-stu-id="a293e-143">Deduction priority</span></span>
- <span data-ttu-id="a293e-144">Grænseperiode</span><span class="sxs-lookup"><span data-stu-id="a293e-144">Limit period</span></span>
- <span data-ttu-id="a293e-145">Beløb for grænse</span><span class="sxs-lookup"><span data-stu-id="a293e-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="a293e-146">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="a293e-146">Benefits</span></span>

- <span data-ttu-id="a293e-147">Plan (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-147">Plan (required)</span></span>
- <span data-ttu-id="a293e-148">Type (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-148">Type (required)</span></span>
- <span data-ttu-id="a293e-149">Mulighed (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-149">Option (required)</span></span>
- <span data-ttu-id="a293e-150">Frynsegode-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-150">Benefit ID (required)</span></span>
- <span data-ttu-id="a293e-151">Frekvens</span><span class="sxs-lookup"><span data-stu-id="a293e-151">Frequency</span></span>
- <span data-ttu-id="a293e-152">Basis</span><span class="sxs-lookup"><span data-stu-id="a293e-152">Basis</span></span>
- <span data-ttu-id="a293e-153">Beløb eller sats</span><span class="sxs-lookup"><span data-stu-id="a293e-153">Amount or rate</span></span>
- <span data-ttu-id="a293e-154">Lønkode</span><span class="sxs-lookup"><span data-stu-id="a293e-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="a293e-155">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="a293e-155">Supported frequencies</span></span> 

- <span data-ttu-id="a293e-156">Ugentlig</span><span class="sxs-lookup"><span data-stu-id="a293e-156">Weekly</span></span>
- <span data-ttu-id="a293e-157">Pr. 14 dage</span><span class="sxs-lookup"><span data-stu-id="a293e-157">Bi-weekly</span></span>
- <span data-ttu-id="a293e-158">To gange om måneden</span><span class="sxs-lookup"><span data-stu-id="a293e-158">Semi-monthly</span></span>
- <span data-ttu-id="a293e-159">Månedlig</span><span class="sxs-lookup"><span data-stu-id="a293e-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="a293e-160">Understøttede grundlag</span><span class="sxs-lookup"><span data-stu-id="a293e-160">Supported bases</span></span> 

- <span data-ttu-id="a293e-161">Fast beløb</span><span class="sxs-lookup"><span data-stu-id="a293e-161">Fixed amount</span></span>
- <span data-ttu-id="a293e-162">Procentdel af løn</span><span class="sxs-lookup"><span data-stu-id="a293e-162">Percent of earnings</span></span>
- <span data-ttu-id="a293e-163">Produktive timer</span><span class="sxs-lookup"><span data-stu-id="a293e-163">Productive hours</span></span>

<span data-ttu-id="a293e-164">Dayforce opretter følgende fradrag, der er baseret på den løneffekt, der er defineret på frynsegodeplanen.</span><span class="sxs-lookup"><span data-stu-id="a293e-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="a293e-165">Valg i Talent</span><span class="sxs-lookup"><span data-stu-id="a293e-165">Selection in Talent</span></span>        | <span data-ttu-id="a293e-166">Resultat i Dayforce</span><span class="sxs-lookup"><span data-stu-id="a293e-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="a293e-167">None</span><span class="sxs-lookup"><span data-stu-id="a293e-167">None</span></span>                       | <span data-ttu-id="a293e-168">Der oprettes ikke noget fradrag.</span><span class="sxs-lookup"><span data-stu-id="a293e-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="a293e-169">Kun fradrag</span><span class="sxs-lookup"><span data-stu-id="a293e-169">Deduction only</span></span>             | <span data-ttu-id="a293e-170">Der oprettes et medarbejderfradrag.</span><span class="sxs-lookup"><span data-stu-id="a293e-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="a293e-171">Kun bidrag</span><span class="sxs-lookup"><span data-stu-id="a293e-171">Contribution only</span></span>          | <span data-ttu-id="a293e-172">Der oprettes et arbejdsgiverfradrag.</span><span class="sxs-lookup"><span data-stu-id="a293e-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="a293e-173">Fradrag og bidrag</span><span class="sxs-lookup"><span data-stu-id="a293e-173">Deduction and contribution</span></span> | <span data-ttu-id="a293e-174">Der oprettes medarbejder- og arbejdsgiverfradrag.</span><span class="sxs-lookup"><span data-stu-id="a293e-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="a293e-175">Du kan finde flere oplysninger om, hvordan du definerer og administrerer et frynsegodeprogram under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="a293e-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="a293e-176">Levere et frynsegodeprogram for medarbejdere</span><span class="sxs-lookup"><span data-stu-id="a293e-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="a293e-177">Oprette et nyt frynsegode</span><span class="sxs-lookup"><span data-stu-id="a293e-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="a293e-178">Definere regler og politikker for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="a293e-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="a293e-179">Tilmelde og fjerne frynsegoder fra arbejdere</span><span class="sxs-lookup"><span data-stu-id="a293e-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="a293e-180">Kompensation</span><span class="sxs-lookup"><span data-stu-id="a293e-180">Compensation</span></span> 

<span data-ttu-id="a293e-181">Kompensationsstyring bruges til at styre fordelingen af grundløn og bonusser.</span><span class="sxs-lookup"><span data-stu-id="a293e-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="a293e-182">En medarbejders faste grundløn og kvalifikationstillæg styres gennem faste lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="a293e-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="a293e-183">Betalingen af incitamentsløn som f.eks. bonusudbetalinger, præstationsbonusser, aktieoptioner og tildelte aktier samt engangsbonusser styres ved hjælp af variable lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="a293e-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="a293e-184">Dayforce anvendes kompensationsoplysninger til at beregne en medarbejders timesats eller årlige sats.</span><span class="sxs-lookup"><span data-stu-id="a293e-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="a293e-185">Konverteringer af planer for fast løn og lønsats er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="a293e-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="a293e-186">Medarbejderne skal være knyttet til en plan for fast løn.</span><span class="sxs-lookup"><span data-stu-id="a293e-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="a293e-187">Du kan finde flere oplysninger om kompensationsplaner under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="a293e-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="a293e-188">Oprette faste kompensationsordninger</span><span class="sxs-lookup"><span data-stu-id="a293e-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="a293e-189">Oprette planer for variabel kompensation</span><span class="sxs-lookup"><span data-stu-id="a293e-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="a293e-190">Udarbejde løn-/kompensationsstruktur og -planer</span><span class="sxs-lookup"><span data-stu-id="a293e-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="a293e-191">Proceskompensation</span><span class="sxs-lookup"><span data-stu-id="a293e-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="a293e-192">Definere kompensationsproces og beregne resultater</span><span class="sxs-lookup"><span data-stu-id="a293e-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="a293e-193">Melde en medarbejder til en fast lønplan</span><span class="sxs-lookup"><span data-stu-id="a293e-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="a293e-194">Melde en medarbejder til en variabel lønplan</span><span class="sxs-lookup"><span data-stu-id="a293e-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="a293e-195">Job</span><span class="sxs-lookup"><span data-stu-id="a293e-195">Jobs</span></span> 

<span data-ttu-id="a293e-196">Et job er en samling af de opgaver og ansvarsområder, der kræves af en person, der udfører et job.</span><span class="sxs-lookup"><span data-stu-id="a293e-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="a293e-197">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="a293e-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="a293e-198">Konfiguration af komponenter i et job</span><span class="sxs-lookup"><span data-stu-id="a293e-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="a293e-199">Definere nye job</span><span class="sxs-lookup"><span data-stu-id="a293e-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="a293e-200">Stillinger</span><span class="sxs-lookup"><span data-stu-id="a293e-200">Positions</span></span>

<span data-ttu-id="a293e-201">En stilling er en individuel forekomst af et job.</span><span class="sxs-lookup"><span data-stu-id="a293e-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="a293e-202">For eksempel er stillingen "Salgschef (øst)" én af de stillinger, der er tilknyttet jobbet "Salgschef".</span><span class="sxs-lookup"><span data-stu-id="a293e-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="a293e-203">En stilling findes i en afdeling.</span><span class="sxs-lookup"><span data-stu-id="a293e-203">A position exists in a department.</span></span> <span data-ttu-id="a293e-204">Der kan kun knyttes én arbejder til hver stilling.</span><span class="sxs-lookup"><span data-stu-id="a293e-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="a293e-205">Hav følgende data og konfiguration i tankerne, når du konfigurerer stillinger:</span><span class="sxs-lookup"><span data-stu-id="a293e-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="a293e-206">Stilling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-206">Position (required)</span></span>
- <span data-ttu-id="a293e-207">Beskrivelse (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-207">Description (required)</span></span>
- <span data-ttu-id="a293e-208">Job (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-208">Job (required)</span></span>
- <span data-ttu-id="a293e-209">Afdeling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-209">Department (required)</span></span>
- <span data-ttu-id="a293e-210">Stillingstype (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-210">Position type (required)</span></span>
- <span data-ttu-id="a293e-211">Fuldtidsækvivalent</span><span class="sxs-lookup"><span data-stu-id="a293e-211">Full-time equivalent</span></span>
- <span data-ttu-id="a293e-212">Normaltimer på årsbasis (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="a293e-213">Betalt af juridiske enhed (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="a293e-214">Betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-214">Pay cycle (required)</span></span>
- <span data-ttu-id="a293e-215">Økonomisk standarddimension – bærer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="a293e-216">Arbejdertildeling – arbejder, tildelingsstart, tildelingsslut, årsagskode</span><span class="sxs-lookup"><span data-stu-id="a293e-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="a293e-217">Hvis flere stillinger i den samme afdeling er knyttet til samme job, konsolideres de til en enkelt stilling i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="a293e-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="a293e-218">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="a293e-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="a293e-219">Organisere dine medarbejdere ved hjælp af afdelinger, jobs og stillinger</span><span class="sxs-lookup"><span data-stu-id="a293e-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="a293e-220">Konfigurere stillinger</span><span class="sxs-lookup"><span data-stu-id="a293e-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="a293e-221">Afdelinger</span><span class="sxs-lookup"><span data-stu-id="a293e-221">Departments</span></span>

<span data-ttu-id="a293e-222">En afdeling er en driftsenhed, der repræsenterer en kategori eller et funktionsområde i en organisation.</span><span class="sxs-lookup"><span data-stu-id="a293e-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="a293e-223">En afdeling er ansvarlig for et bestemt område i organisationen, såsom salg, regnskab eller personale.</span><span class="sxs-lookup"><span data-stu-id="a293e-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="a293e-224">Du kan bruge afdelinger til at rapportere om funktionsområder.</span><span class="sxs-lookup"><span data-stu-id="a293e-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="a293e-225">Afdelinger kan have ansvar for driftsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="a293e-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="a293e-226">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="a293e-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="a293e-227">Oprette en afdeling og knytte den til afdelingshierarkiet</span><span class="sxs-lookup"><span data-stu-id="a293e-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="a293e-228">Definere nye afdelinger</span><span class="sxs-lookup"><span data-stu-id="a293e-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="a293e-229">Betalingscyklusser og lønperioder</span><span class="sxs-lookup"><span data-stu-id="a293e-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="a293e-230">En betalingscyklus bestemmer, hvor ofte løn køres,og de specifikke dage, hvor arbejdere betales.</span><span class="sxs-lookup"><span data-stu-id="a293e-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="a293e-231">En løncyklus kan f.eks. være månedlig, og medarbejdere betales måske på den sidste dag i måneden.</span><span class="sxs-lookup"><span data-stu-id="a293e-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="a293e-232">En løncyklus kan også være ugentligt, og medarbejdere betales måske tirsdag efter slutningen af lønperioden.</span><span class="sxs-lookup"><span data-stu-id="a293e-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="a293e-233">Løncyklusser tildeles til stillinger for at styre, hvornår arbejdere i disse stillinger bliver betalt.</span><span class="sxs-lookup"><span data-stu-id="a293e-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="a293e-234">Når du opretter betalingscyklusser, kan du generere lønperioder for hver cyklus.</span><span class="sxs-lookup"><span data-stu-id="a293e-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="a293e-235">Hver lønperiode omfatter en standardbetalingsdato, der er baseret på oplysninger, du angiver.</span><span class="sxs-lookup"><span data-stu-id="a293e-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="a293e-236">Du kan dog redigere standardbetalingsdatoen i en lønperiode til at tillade undtagelser, f.eks. når betalingsdatoen falder på en helligdag.</span><span class="sxs-lookup"><span data-stu-id="a293e-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="a293e-237">Følgende oplysninger bruges i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="a293e-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="a293e-238">Betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-238">Pay cycle (required)</span></span>
- <span data-ttu-id="a293e-239">Hyppighed for betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="a293e-240">Periodens startdato (første lønperiode påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="a293e-241">Standardbetalingsdato (første lønperiode påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="a293e-242">Oplysningerne er integreret med Dayforce som løngrupper og adskilles af et land eller område for hver løncyklus.</span><span class="sxs-lookup"><span data-stu-id="a293e-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="a293e-243">Mindst én periode skal genereres før integration.</span><span class="sxs-lookup"><span data-stu-id="a293e-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="a293e-244">Dayforce genererer løngruppekalendere og betalingsdatoer, der er baseret på startdatoen for den første lønperiode og den standardbetalingsdato, der er angivet i Talent.</span><span class="sxs-lookup"><span data-stu-id="a293e-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="a293e-245">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="a293e-245">Earning codes</span></span>

<span data-ttu-id="a293e-246">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="a293e-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="a293e-247">Koderne har forskellige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="a293e-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="a293e-248">Følgende oplysninger bruges i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="a293e-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="a293e-249">Lønkode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-249">Earning Code (required)</span></span>
- <span data-ttu-id="a293e-250">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="a293e-250">Description</span></span>
- <span data-ttu-id="a293e-251">Måleenhed</span><span class="sxs-lookup"><span data-stu-id="a293e-251">Unit of measure</span></span>
- <span data-ttu-id="a293e-252">Produktiv</span><span class="sxs-lookup"><span data-stu-id="a293e-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="a293e-253">Arbejderdata</span><span class="sxs-lookup"><span data-stu-id="a293e-253">Worker data</span></span>

<span data-ttu-id="a293e-254">Posterne for de forskellige typer arbejdere, du beskæftiger, er vigtige for dine personale- og lønsystemer.</span><span class="sxs-lookup"><span data-stu-id="a293e-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="a293e-255">De oplysninger, du angiver, kan bruges til at spore arbejdere og personoplysninger.</span><span class="sxs-lookup"><span data-stu-id="a293e-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="a293e-256">Du kan vedligeholde følgende oplysninger for arbejdere:</span><span class="sxs-lookup"><span data-stu-id="a293e-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="a293e-257">**Basis** – Vedligehold grundlæggende oplysninger om en arbejder, f.eks. kontaktoplysninger, demografiske oplysninger, identifikationsoplysninger, oplysninger om familie, status for militærtjeneste, oplysninger om udstationering og personlige kontaktpersoner og kontaktpersoner i nødsituationer.</span><span class="sxs-lookup"><span data-stu-id="a293e-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="a293e-258">**Beskæftigelse** – Vedligehold oplysninger om en arbejders beskæftigelse, f.eks. firma- eller organisationstilhørsforhold, stillingstildeling, start- og slutdatoer, arbejdstilladelse, vilkår for ansættelse, pension, ferie og flytteoplysninger.</span><span class="sxs-lookup"><span data-stu-id="a293e-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="a293e-259">**Orlov og fravær** – Vedligehold oplysninger om en arbejders fravær, f.eks. arbejdskalendere, fraværstransaktioner og fraværsopsætning.</span><span class="sxs-lookup"><span data-stu-id="a293e-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="a293e-260">**Kompensation og løn** – Vedligehold oplysninger om en arbejders kompensationsplaner og lønoplysninger, f.eks. tilmelding til planer, priser, ydeevne, provision, skatteoplysninger, pensionering og skattefradrag.</span><span class="sxs-lookup"><span data-stu-id="a293e-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="a293e-261">Når du angiver arbejderoplysninger, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="a293e-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="a293e-262">Generelle oplysninger</span><span class="sxs-lookup"><span data-stu-id="a293e-262">General information</span></span>

- <span data-ttu-id="a293e-263">Personalenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-263">Personnel number (required)</span></span>
- <span data-ttu-id="a293e-264">Fornavn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-264">First name (required)</span></span>
- <span data-ttu-id="a293e-265">Efternavn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-265">Last name (required)</span></span>
- <span data-ttu-id="a293e-266">Mellemnavn</span><span class="sxs-lookup"><span data-stu-id="a293e-266">Middle name</span></span>
- <span data-ttu-id="a293e-267">Anciennitetsdato</span><span class="sxs-lookup"><span data-stu-id="a293e-267">Seniority date</span></span>
- <span data-ttu-id="a293e-268">Kendt som</span><span class="sxs-lookup"><span data-stu-id="a293e-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="a293e-269">Personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="a293e-269">Personal information</span></span>

- <span data-ttu-id="a293e-270">Ægteskabelig status (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-270">Marital status (required)</span></span>
- <span data-ttu-id="a293e-271">Fødselsdato (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-271">Birth date (required)</span></span>
- <span data-ttu-id="a293e-272">Køn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-272">Gender (required)</span></span>
- <span data-ttu-id="a293e-273">Handicappet</span><span class="sxs-lookup"><span data-stu-id="a293e-273">Person with disabilities</span></span>
- <span data-ttu-id="a293e-274">Land eller område for nationalitet (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="a293e-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="a293e-275">Adresseoplysninger</span><span class="sxs-lookup"><span data-stu-id="a293e-275">Address information</span></span>

- <span data-ttu-id="a293e-276">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-276">Primary (required)</span></span>
- <span data-ttu-id="a293e-277">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-277">Country/region (required)</span></span>
- <span data-ttu-id="a293e-278">Postnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-278">Postal code (required)</span></span>
- <span data-ttu-id="a293e-279">Gadenummer (påkrævet) (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="a293e-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="a293e-280">Bygningskomplement (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="a293e-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="a293e-281">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-281">City (required)</span></span>
- <span data-ttu-id="a293e-282">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-282">State (required)</span></span>
- <span data-ttu-id="a293e-283">Region (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="a293e-284">Kontaktoplysninger</span><span class="sxs-lookup"><span data-stu-id="a293e-284">Contact information</span></span> 

- <span data-ttu-id="a293e-285">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-285">Primary (required)</span></span>
- <span data-ttu-id="a293e-286">Kontaktpersonens nummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-286">Contact number (required)</span></span>
- <span data-ttu-id="a293e-287">Forlængelse</span><span class="sxs-lookup"><span data-stu-id="a293e-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="a293e-288">Lønoplysninger og lønkoder</span><span class="sxs-lookup"><span data-stu-id="a293e-288">Payroll information and earning codes</span></span>

<span data-ttu-id="a293e-289">Medarbejdere kan tildeles en bestemt løn med en given betalingshyppighed og have en foretrukken betalingsmetode.</span><span class="sxs-lookup"><span data-stu-id="a293e-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="a293e-290">Følgende felter bruges i Dayforce til at sikre, at disse præferencer og indstillinger bruges.</span><span class="sxs-lookup"><span data-stu-id="a293e-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="a293e-291">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="a293e-291">Earning codes</span></span>

- <span data-ttu-id="a293e-292">Stilling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-292">Position (required)</span></span>
- <span data-ttu-id="a293e-293">Lønkode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-293">Earning Code (required)</span></span>
- <span data-ttu-id="a293e-294">Frekvens (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-294">Frequency (required)</span></span>
- <span data-ttu-id="a293e-295">Beløb (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="a293e-296">Lønoplysninger</span><span class="sxs-lookup"><span data-stu-id="a293e-296">Payroll information</span></span>

- <span data-ttu-id="a293e-297">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="a293e-297">Payment Method</span></span>
- <span data-ttu-id="a293e-298">Økonomisk område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-298">Economic Region (required)</span></span>
- <span data-ttu-id="a293e-299">Id for medarbejderfrynsegoder</span><span class="sxs-lookup"><span data-stu-id="a293e-299">Employee Benefits ID</span></span>
- <span data-ttu-id="a293e-300">Nationalt id-nummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-300">National ID Number (required)</span></span>
- <span data-ttu-id="a293e-301">Tjenestenummer hos militær</span><span class="sxs-lookup"><span data-stu-id="a293e-301">Military Service Number</span></span>
- <span data-ttu-id="a293e-302">Skifte-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-302">Shift ID (required)</span></span>
- <span data-ttu-id="a293e-303">Skattenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-303">Tax Number (required)</span></span>
- <span data-ttu-id="a293e-304">Fagforenings-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-304">Union ID (required)</span></span>
- <span data-ttu-id="a293e-305">Arbejdsdags-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-305">Work Day ID (required)</span></span>
- <span data-ttu-id="a293e-306">Arbejdstilladelsesnummer</span><span class="sxs-lookup"><span data-stu-id="a293e-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="a293e-307">For betalingsmetoden understøtter Mexico **Kontant**, **Check** (firmaets fysiske check), og **Elektronisk betaling**.</span><span class="sxs-lookup"><span data-stu-id="a293e-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="a293e-308">Hvis der ikke er angivet nogen betalingsmetode, bruges **Check** som standard.</span><span class="sxs-lookup"><span data-stu-id="a293e-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="a293e-309">Detaljer om ansættelse</span><span class="sxs-lookup"><span data-stu-id="a293e-309">Employment details</span></span>

<span data-ttu-id="a293e-310">Detaljeret ansættelseshistorik bruges som vigtige oplysninger til at udlede statusser for en medarbejders ansættelse, fratrædelse og genansættelse i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="a293e-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="a293e-311">Dayforce understøtter kun én aktiv ansættelsespost ad gangen.</span><span class="sxs-lookup"><span data-stu-id="a293e-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="a293e-312">Startdato for ansættelse (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-312">Employment start date (required)</span></span>
- <span data-ttu-id="a293e-313">Slutdato for ansættelse</span><span class="sxs-lookup"><span data-stu-id="a293e-313">Employment end date</span></span>
- <span data-ttu-id="a293e-314">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="a293e-314">Start date</span></span>
- <span data-ttu-id="a293e-315">Justeret startdato</span><span class="sxs-lookup"><span data-stu-id="a293e-315">Adjusted start date</span></span>
- <span data-ttu-id="a293e-316">Fratrædelsesdato (kræves ved fratrædelse)</span><span class="sxs-lookup"><span data-stu-id="a293e-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="a293e-317">Fratrædelsesårsag (kræves ved fratrædelse)</span><span class="sxs-lookup"><span data-stu-id="a293e-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="a293e-318">Vigtige datoer for en medarbejders udledes ved hjælp af følgende oplysninger.</span><span class="sxs-lookup"><span data-stu-id="a293e-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="a293e-319">Talent</span><span class="sxs-lookup"><span data-stu-id="a293e-319">Talent</span></span>                | <span data-ttu-id="a293e-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="a293e-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a293e-321">Den seneste ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="a293e-321">Most recent hire date</span></span> | <span data-ttu-id="a293e-322">Historikpost for ansættelsesstart for aktuel ikke-afsluttet ansættelse</span><span class="sxs-lookup"><span data-stu-id="a293e-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="a293e-323">Fratrædelsesdato</span><span class="sxs-lookup"><span data-stu-id="a293e-323">Termination date</span></span>      | <span data-ttu-id="a293e-324">Historikpost for fratrædelsesdato for aktuel ikke-afsluttet ansættelse</span><span class="sxs-lookup"><span data-stu-id="a293e-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="a293e-325">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="a293e-325">Start date</span></span>            | <span data-ttu-id="a293e-326">Historikpost for justeret startdato, startdato eller startdato for ansættelse for aktuel ikke-aktiv ansættelse</span><span class="sxs-lookup"><span data-stu-id="a293e-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="a293e-327">Oprindelig ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="a293e-327">Original hire date</span></span>    | <span data-ttu-id="a293e-328">Historikpost for ansættelsesstart for tidligste ansættelse</span><span class="sxs-lookup"><span data-stu-id="a293e-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="a293e-329">Kompensation</span><span class="sxs-lookup"><span data-stu-id="a293e-329">Compensation</span></span>

<span data-ttu-id="a293e-330">En fast lønstruktur skal tilknyttes hver medarbejders primære stilling gennem hele ansættelsesperioden.</span><span class="sxs-lookup"><span data-stu-id="a293e-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="a293e-331">Denne periode starter på den dato, hvor medarbejderen blev ansat (eller ansættelsesstartdatoen) og fortsætter, indtil fratrædelsen.</span><span class="sxs-lookup"><span data-stu-id="a293e-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="a293e-332">Ikrafttrædelsesdato (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-332">Effective Date (required)</span></span>
- <span data-ttu-id="a293e-333">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="a293e-333">Expiration date</span></span>
- <span data-ttu-id="a293e-334">Lønsats (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-334">Pay Rate (required)</span></span>
- <span data-ttu-id="a293e-335">Konverteringer af lønsats (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="a293e-336">Årlig ækvivalent (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="a293e-337">Timebaseret ækvivalent (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="a293e-338">Hvis en timeansat medarbejder har flere stillinger, indlæses den faste løn for den primære stilling i Dayforce, som basissats/-løn på medarbejderniveau.</span><span class="sxs-lookup"><span data-stu-id="a293e-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="a293e-339">For ikke-primære stillinger gemmes timesatsen i den tilsvarende position i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="a293e-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="a293e-340">Hvis en funktionær har flere stillinger, afledes den kumulative timesats og årlig gage på tværs af alle aktive stillinger og bruges som basissats/-gage på medarbejderniveau.</span><span class="sxs-lookup"><span data-stu-id="a293e-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="a293e-341">Identifikationsnumre</span><span class="sxs-lookup"><span data-stu-id="a293e-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="a293e-342">Social Security-identifikator</span><span class="sxs-lookup"><span data-stu-id="a293e-342">Social Security identifier</span></span> 

<span data-ttu-id="a293e-343">Alle medarbejdere skal have én primær identifikator.</span><span class="sxs-lookup"><span data-stu-id="a293e-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="a293e-344">Identifikatoren skal være af **SSN**-identifikationstypen</span><span class="sxs-lookup"><span data-stu-id="a293e-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="a293e-345">I Dayforce afledes den automatisk som medarbejderens Social Security-identifikator, der er påkrævet ved ansættelse.</span><span class="sxs-lookup"><span data-stu-id="a293e-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="a293e-346">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-346">Primary (required)</span></span>
- <span data-ttu-id="a293e-347">Identifikationstype = "SSN"</span><span class="sxs-lookup"><span data-stu-id="a293e-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="a293e-348">Udstedt den</span><span class="sxs-lookup"><span data-stu-id="a293e-348">Issued Date</span></span>
- <span data-ttu-id="a293e-349">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="a293e-349">Expiration Date</span></span>

<span data-ttu-id="a293e-350">Medarbejdere kan angive flere identifikationsnumre af **SSN**-identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="a293e-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="a293e-351">Men det er kun den post, der er markeret som **Primær**, som er integreret i Dayforce, uanset om nummeret er aktivt eller udløbet.</span><span class="sxs-lookup"><span data-stu-id="a293e-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="a293e-352">Bankkonto og udbetalinger</span><span class="sxs-lookup"><span data-stu-id="a293e-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="a293e-353">Gyldige bankkontooplysninger skal angives for enhver medarbejder, der vælger at blive betalt via bankkontooverførsler.</span><span class="sxs-lookup"><span data-stu-id="a293e-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="a293e-354">Talent</span><span class="sxs-lookup"><span data-stu-id="a293e-354">Talent</span></span>                         | <span data-ttu-id="a293e-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="a293e-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a293e-356">Bankkontonummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="a293e-357">SWIFT-kode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-357">SWIFT code (required)</span></span>          | <span data-ttu-id="a293e-358">Feltet **Bank-id** bruges ved behandling af løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="a293e-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="a293e-359">Afdelingsnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="a293e-360">Bankkontotype (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-360">Bank account type (required)</span></span>   | <span data-ttu-id="a293e-361">Feltet **Kontotype** bruges ved behandling af løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="a293e-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="a293e-362">Understøttede værdier omfatter **Check** og **Løn**.</span><span class="sxs-lookup"><span data-stu-id="a293e-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="a293e-363">Medarbejdere, der vælger at betales via bankkontooverførsler, skal angive et link til en restbeløbskonto, der hører under en juridisk enhed, som har primær adresse i Mexico og er knyttet til en gyldig bankkonto fra en mexicansk bank.</span><span class="sxs-lookup"><span data-stu-id="a293e-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="a293e-364">Alle andre restbeløbskonti ignoreres.</span><span class="sxs-lookup"><span data-stu-id="a293e-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="a293e-365">Adresseoplysninger</span><span class="sxs-lookup"><span data-stu-id="a293e-365">Address information</span></span>

<span data-ttu-id="a293e-366">Alle medarbejdere skal have én primær placering.</span><span class="sxs-lookup"><span data-stu-id="a293e-366">Every employee must have one primary location.</span></span> <span data-ttu-id="a293e-367">I Dayforce bruges denne placering til at bestemme medarbejderens primære opholdssted til skattemæssige formål.</span><span class="sxs-lookup"><span data-stu-id="a293e-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="a293e-368">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-368">Primary (required)</span></span>
- <span data-ttu-id="a293e-369">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-369">Country/region (required)</span></span>
- <span data-ttu-id="a293e-370">Postnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="a293e-371">Gade (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-371">Street (required)</span></span>
- <span data-ttu-id="a293e-372">Gadenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-372">Street Number (required)</span></span>
- <span data-ttu-id="a293e-373">Bygningskomplement</span><span class="sxs-lookup"><span data-stu-id="a293e-373">Building Complement</span></span>
- <span data-ttu-id="a293e-374">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-374">City (required)</span></span>
- <span data-ttu-id="a293e-375">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-375">State (required)</span></span>
- <span data-ttu-id="a293e-376">Region (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="a293e-377">Konfigurere dataene for at generere løn i USA og Canada</span><span class="sxs-lookup"><span data-stu-id="a293e-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="a293e-378">Hvis du genererer løn for medarbejdere i USA og Canada, skal følgende elementer konfigureres:</span><span class="sxs-lookup"><span data-stu-id="a293e-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="a293e-379">Der kræves afdelinger til stillinger.</span><span class="sxs-lookup"><span data-stu-id="a293e-379">Departments are required on positions.</span></span>
- <span data-ttu-id="a293e-380">Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="a293e-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="a293e-381">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="a293e-381">Job types</span></span>

<span data-ttu-id="a293e-382">Jobtyper bruges til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="a293e-382">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="a293e-383">Jobtyper kræves for at behandle løn i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="a293e-383">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="a293e-384">Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="a293e-384">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="a293e-385">Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.</span><span class="sxs-lookup"><span data-stu-id="a293e-385">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="a293e-386">Der kræves følgende jobtyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="a293e-386">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="a293e-387">Jobtype</span><span class="sxs-lookup"><span data-stu-id="a293e-387">Job type</span></span>   | <span data-ttu-id="a293e-388">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="a293e-388">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="a293e-389">Pr. time</span><span class="sxs-lookup"><span data-stu-id="a293e-389">Hourly</span></span>     | <span data-ttu-id="a293e-390">Pr. time</span><span class="sxs-lookup"><span data-stu-id="a293e-390">Hourly</span></span>      |
| <span data-ttu-id="a293e-391">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="a293e-391">Salaried</span></span>   | <span data-ttu-id="a293e-392">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="a293e-392">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="a293e-393">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="a293e-393">Position types</span></span> 

<span data-ttu-id="a293e-394">Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet.</span><span class="sxs-lookup"><span data-stu-id="a293e-394">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="a293e-395">Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="a293e-395">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="a293e-396">Der kræves følgende stillingstyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="a293e-396">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="a293e-397">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="a293e-397">Position type</span></span>   | <span data-ttu-id="a293e-398">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="a293e-398">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="a293e-399">Fuld tid</span><span class="sxs-lookup"><span data-stu-id="a293e-399">Full-time</span></span>       | <span data-ttu-id="a293e-400">Fuldtidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="a293e-400">Full time employee</span></span> |
| <span data-ttu-id="a293e-401">Deltid</span><span class="sxs-lookup"><span data-stu-id="a293e-401">Part-time</span></span>       | <span data-ttu-id="a293e-402">Deltidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="a293e-402">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="a293e-403">Årsagskoder</span><span class="sxs-lookup"><span data-stu-id="a293e-403">Reason codes</span></span>

<span data-ttu-id="a293e-404">Årsagskoder indeholder oplysninger om status for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="a293e-404">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="a293e-405">Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.</span><span class="sxs-lookup"><span data-stu-id="a293e-405">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="a293e-406">Der kræves følgende årsagskoder og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="a293e-406">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="a293e-407">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="a293e-407">Reason code</span></span>    | <span data-ttu-id="a293e-408">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="a293e-408">Description</span></span>      | <span data-ttu-id="a293e-409">Anvendelige scenarier</span><span class="sxs-lookup"><span data-stu-id="a293e-409">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="a293e-410">OPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="a293e-410">RESIGNATION</span></span>    | <span data-ttu-id="a293e-411">Opsigelse</span><span class="sxs-lookup"><span data-stu-id="a293e-411">Resignation</span></span>      | <span data-ttu-id="a293e-412">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="a293e-412">Terminate worker</span></span>     |
| <span data-ttu-id="a293e-413">OPHØR</span><span class="sxs-lookup"><span data-stu-id="a293e-413">TERMINATION</span></span>    | <span data-ttu-id="a293e-414">Ophør</span><span class="sxs-lookup"><span data-stu-id="a293e-414">Termination</span></span>      | <span data-ttu-id="a293e-415">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="a293e-415">Terminate worker</span></span>     |
| <span data-ttu-id="a293e-416">PENSION</span><span class="sxs-lookup"><span data-stu-id="a293e-416">RETIREMENT</span></span>     | <span data-ttu-id="a293e-417">Pension</span><span class="sxs-lookup"><span data-stu-id="a293e-417">Retirement</span></span>       | <span data-ttu-id="a293e-418">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="a293e-418">Terminate worker</span></span>     |
| <span data-ttu-id="a293e-419">ANDET</span><span class="sxs-lookup"><span data-stu-id="a293e-419">OTHER</span></span>          | <span data-ttu-id="a293e-420">Andre årsager</span><span class="sxs-lookup"><span data-stu-id="a293e-420">Other Reasons</span></span>    | <span data-ttu-id="a293e-421">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="a293e-421">Terminate worker</span></span>     |
| <span data-ttu-id="a293e-422">DØDSFALD</span><span class="sxs-lookup"><span data-stu-id="a293e-422">DEATH</span></span>          | <span data-ttu-id="a293e-423">Dødsfald</span><span class="sxs-lookup"><span data-stu-id="a293e-423">Death</span></span>            | <span data-ttu-id="a293e-424">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="a293e-424">Terminate worker</span></span>     |
| <span data-ttu-id="a293e-425">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="a293e-425">LEAVEOFABSENCE</span></span> | <span data-ttu-id="a293e-426">Orlov</span><span class="sxs-lookup"><span data-stu-id="a293e-426">Leave of Absence</span></span> | <span data-ttu-id="a293e-427">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="a293e-427">Terminate worker</span></span>     |
| <span data-ttu-id="a293e-428">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="a293e-428">CONTRACTEND</span></span>    | <span data-ttu-id="a293e-429">Kontraktudløb</span><span class="sxs-lookup"><span data-stu-id="a293e-429">End of Contract</span></span>  | <span data-ttu-id="a293e-430">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="a293e-430">Terminate worker</span></span>     |
| <span data-ttu-id="a293e-431">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="a293e-431">SALARYCHANGE</span></span>   | <span data-ttu-id="a293e-432">Ændring af løn</span><span class="sxs-lookup"><span data-stu-id="a293e-432">Change of Salary</span></span> | <span data-ttu-id="a293e-433">Kompensation</span><span class="sxs-lookup"><span data-stu-id="a293e-433">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="a293e-434">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="a293e-434">Marital status</span></span>

<span data-ttu-id="a293e-435">Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="a293e-435">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="a293e-436">Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="a293e-436">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="a293e-437">Talent</span><span class="sxs-lookup"><span data-stu-id="a293e-437">Talent</span></span>                 | <span data-ttu-id="a293e-438">Dayforce</span><span class="sxs-lookup"><span data-stu-id="a293e-438">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="a293e-439">Gift</span><span class="sxs-lookup"><span data-stu-id="a293e-439">Married</span></span>                | <span data-ttu-id="a293e-440">Gift</span><span class="sxs-lookup"><span data-stu-id="a293e-440">Married</span></span>              |
| <span data-ttu-id="a293e-441">Enlig</span><span class="sxs-lookup"><span data-stu-id="a293e-441">Single</span></span>                 | <span data-ttu-id="a293e-442">Enlig</span><span class="sxs-lookup"><span data-stu-id="a293e-442">Single</span></span>               |
| <span data-ttu-id="a293e-443">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="a293e-443">Widowed</span></span>                | <span data-ttu-id="a293e-444">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="a293e-444">Widowed</span></span>              |
| <span data-ttu-id="a293e-445">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="a293e-445">Divorced</span></span>               | <span data-ttu-id="a293e-446">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="a293e-446">Divorced</span></span>             |
| <span data-ttu-id="a293e-447">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="a293e-447">Registered Partnership</span></span> | <span data-ttu-id="a293e-448">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="a293e-448">Domestic Partnership</span></span> |
| <span data-ttu-id="a293e-449">None</span><span class="sxs-lookup"><span data-stu-id="a293e-449">None</span></span>                   | <span data-ttu-id="a293e-450">None</span><span class="sxs-lookup"><span data-stu-id="a293e-450">None</span></span>                 |
| <span data-ttu-id="a293e-451">Samlever</span><span class="sxs-lookup"><span data-stu-id="a293e-451">Cohabiting</span></span>             | <span data-ttu-id="a293e-452">Samlever</span><span class="sxs-lookup"><span data-stu-id="a293e-452">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="a293e-453">Køn</span><span class="sxs-lookup"><span data-stu-id="a293e-453">Gender</span></span>

<span data-ttu-id="a293e-454">Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="a293e-454">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="a293e-455">Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="a293e-455">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="a293e-456">Talent</span><span class="sxs-lookup"><span data-stu-id="a293e-456">Talent</span></span>       | <span data-ttu-id="a293e-457">Dayforce</span><span class="sxs-lookup"><span data-stu-id="a293e-457">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="a293e-458">Mand</span><span class="sxs-lookup"><span data-stu-id="a293e-458">Male</span></span>         | <span data-ttu-id="a293e-459">Mand</span><span class="sxs-lookup"><span data-stu-id="a293e-459">Male</span></span>            |
| <span data-ttu-id="a293e-460">Kvinde</span><span class="sxs-lookup"><span data-stu-id="a293e-460">Female</span></span>       | <span data-ttu-id="a293e-461">Kvinde</span><span class="sxs-lookup"><span data-stu-id="a293e-461">Female</span></span>          |
| <span data-ttu-id="a293e-462">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="a293e-462">Non-specific</span></span> | <span data-ttu-id="a293e-463">*Understøttes ikke*</span><span class="sxs-lookup"><span data-stu-id="a293e-463">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="a293e-464">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="a293e-464">Earning codes</span></span>

<span data-ttu-id="a293e-465">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="a293e-465">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="a293e-466">Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="a293e-466">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="a293e-467">Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="a293e-467">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="a293e-468">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="a293e-468">Supported frequencies</span></span>

- <span data-ttu-id="a293e-469">Alt</span><span class="sxs-lookup"><span data-stu-id="a293e-469">All</span></span>
- <span data-ttu-id="a293e-470">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="a293e-470">EVERYPAY</span></span>
- <span data-ttu-id="a293e-471">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="a293e-471">EACHPAYPERIOD</span></span>
- <span data-ttu-id="a293e-472">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="a293e-472">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="a293e-473">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="a293e-473">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="a293e-474">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-474">1OFMTH</span></span>
- <span data-ttu-id="a293e-475">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-475">LASTOFMTH</span></span>
- <span data-ttu-id="a293e-476">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-476">2OFMTH</span></span>
- <span data-ttu-id="a293e-477">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-477">3OFMTH</span></span>
- <span data-ttu-id="a293e-478">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-478">4OFMTH</span></span>
- <span data-ttu-id="a293e-479">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-479">5OFMTH</span></span>
- <span data-ttu-id="a293e-480">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-480">1N2OFMTH</span></span>
- <span data-ttu-id="a293e-481">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-481">3N4OFMTH</span></span>
- <span data-ttu-id="a293e-482">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-482">1N3OFMTH</span></span>
- <span data-ttu-id="a293e-483">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-483">1N4OFMTH</span></span>
- <span data-ttu-id="a293e-484">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-484">2N3OFMTH</span></span>
- <span data-ttu-id="a293e-485">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-485">2N4OFMTH</span></span>
- <span data-ttu-id="a293e-486">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-486">1N2N3OFMTH</span></span>
- <span data-ttu-id="a293e-487">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-487">1N2N4OFMTH</span></span>
- <span data-ttu-id="a293e-488">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-488">1N3N4OFMTH</span></span>
- <span data-ttu-id="a293e-489">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-489">2N3N4OFMTH</span></span>
- <span data-ttu-id="a293e-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="a293e-491">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="a293e-491">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="a293e-492">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="a293e-492">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="a293e-493">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="a293e-493">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="a293e-494">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="a293e-494">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="a293e-495">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="a293e-495">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="a293e-496">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="a293e-496">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="a293e-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="a293e-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="a293e-498">Adresser</span><span class="sxs-lookup"><span data-stu-id="a293e-498">Addresses</span></span>

<span data-ttu-id="a293e-499">Identifikation af specifikke koder for land eller region, stat og område (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende.</span><span class="sxs-lookup"><span data-stu-id="a293e-499">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="a293e-500">Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.</span><span class="sxs-lookup"><span data-stu-id="a293e-500">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="a293e-501">Talent</span><span class="sxs-lookup"><span data-stu-id="a293e-501">Talent</span></span>          | <span data-ttu-id="a293e-502">Dayforce</span><span class="sxs-lookup"><span data-stu-id="a293e-502">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="a293e-503">Land/område</span><span class="sxs-lookup"><span data-stu-id="a293e-503">Country/Region</span></span>  | <span data-ttu-id="a293e-504">Landekode</span><span class="sxs-lookup"><span data-stu-id="a293e-504">Country Code</span></span>          |
| <span data-ttu-id="a293e-505">Postnummer</span><span class="sxs-lookup"><span data-stu-id="a293e-505">Zip/Postal Code</span></span> | <span data-ttu-id="a293e-506">Postnummer</span><span class="sxs-lookup"><span data-stu-id="a293e-506">Postal Code</span></span>           |
| <span data-ttu-id="a293e-507">Status</span><span class="sxs-lookup"><span data-stu-id="a293e-507">State</span></span>           | <span data-ttu-id="a293e-508">Statskode</span><span class="sxs-lookup"><span data-stu-id="a293e-508">State Code</span></span>            |
| <span data-ttu-id="a293e-509">Bynavn</span><span class="sxs-lookup"><span data-stu-id="a293e-509">City</span></span>            | <span data-ttu-id="a293e-510">Bynavn</span><span class="sxs-lookup"><span data-stu-id="a293e-510">City</span></span>                  |
| <span data-ttu-id="a293e-511">Region</span><span class="sxs-lookup"><span data-stu-id="a293e-511">County</span></span>          | <span data-ttu-id="a293e-512">Område (kommune)</span><span class="sxs-lookup"><span data-stu-id="a293e-512">County (Municipality)</span></span> |
| <span data-ttu-id="a293e-513">Gade</span><span class="sxs-lookup"><span data-stu-id="a293e-513">Street</span></span>          | <span data-ttu-id="a293e-514">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="a293e-514">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="a293e-515">Skatteområder</span><span class="sxs-lookup"><span data-stu-id="a293e-515">Tax regions</span></span>

<span data-ttu-id="a293e-516">Skatteområder bruges til at bestemme den relevante skat, der skal anvendes ved løngenerering.</span><span class="sxs-lookup"><span data-stu-id="a293e-516">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="a293e-517">Skatteområder er tilknyttet Dayforce som placeringsadresser.</span><span class="sxs-lookup"><span data-stu-id="a293e-517">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="a293e-518">Standardskatteområder skal knyttes til arbejderens aktive stilling.</span><span class="sxs-lookup"><span data-stu-id="a293e-518">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="a293e-519">Skatteområde (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-519">Tax region (required)</span></span>
- <span data-ttu-id="a293e-520">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-520">Country/Region (required)</span></span>
- <span data-ttu-id="a293e-521">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-521">State (required)</span></span>
- <span data-ttu-id="a293e-522">Region</span><span class="sxs-lookup"><span data-stu-id="a293e-522">County</span></span> 
- <span data-ttu-id="a293e-523">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="a293e-523">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="a293e-524">Konfigurere dataene for at generere løn i Mexico</span><span class="sxs-lookup"><span data-stu-id="a293e-524">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="a293e-525">Hvis du genererer løn for medarbejdere i Mexico skal følgende elementer konfigureres:</span><span class="sxs-lookup"><span data-stu-id="a293e-525">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="a293e-526">Der kræves afdelinger til stillinger.</span><span class="sxs-lookup"><span data-stu-id="a293e-526">Departments are required on positions.</span></span>
- <span data-ttu-id="a293e-527">Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="a293e-527">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="a293e-528">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="a293e-528">Job types</span></span>

<span data-ttu-id="a293e-529">Jobtyper bruges til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="a293e-529">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="a293e-530">Jobtyper kræves for at behandle løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="a293e-530">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="a293e-531">Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="a293e-531">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="a293e-532">Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.</span><span class="sxs-lookup"><span data-stu-id="a293e-532">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="a293e-533">Der kræves følgende jobtyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="a293e-533">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="a293e-534">Jobtype</span><span class="sxs-lookup"><span data-stu-id="a293e-534">Job type</span></span>   | <span data-ttu-id="a293e-535">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="a293e-535">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="a293e-536">Pr. time</span><span class="sxs-lookup"><span data-stu-id="a293e-536">Hourly</span></span>     | <span data-ttu-id="a293e-537">MX Pr. time</span><span class="sxs-lookup"><span data-stu-id="a293e-537">MX Hourly</span></span>   |
| <span data-ttu-id="a293e-538">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="a293e-538">Salaried</span></span>   | <span data-ttu-id="a293e-539">MX Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="a293e-539">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="a293e-540">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="a293e-540">Position types</span></span> 

<span data-ttu-id="a293e-541">Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet.</span><span class="sxs-lookup"><span data-stu-id="a293e-541">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="a293e-542">Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="a293e-542">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="a293e-543">Der kræves følgende stillingstyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="a293e-543">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="a293e-544">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="a293e-544">Position type</span></span>   | <span data-ttu-id="a293e-545">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="a293e-545">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="a293e-546">Fuld tid</span><span class="sxs-lookup"><span data-stu-id="a293e-546">Full-time</span></span>       | <span data-ttu-id="a293e-547">Fuldtidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="a293e-547">Full time employee</span></span> |
| <span data-ttu-id="a293e-548">Deltid</span><span class="sxs-lookup"><span data-stu-id="a293e-548">Part-time</span></span>       | <span data-ttu-id="a293e-549">Deltidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="a293e-549">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="a293e-550">Årsagskoder</span><span class="sxs-lookup"><span data-stu-id="a293e-550">Reason codes</span></span>

<span data-ttu-id="a293e-551">Årsagskoder indeholder oplysninger om status for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="a293e-551">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="a293e-552">Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.</span><span class="sxs-lookup"><span data-stu-id="a293e-552">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="a293e-553">Der kræves følgende årsagskoder og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="a293e-553">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="a293e-554">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="a293e-554">Reason code</span></span>            | <span data-ttu-id="a293e-555">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="a293e-555">Description</span></span>                    | <span data-ttu-id="a293e-556">Anvendelige scenarier</span><span class="sxs-lookup"><span data-stu-id="a293e-556">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="a293e-557">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="a293e-557">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="a293e-558">Afgang før første løn</span><span class="sxs-lookup"><span data-stu-id="a293e-558">Departure before first payroll</span></span> | <span data-ttu-id="a293e-559">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="a293e-559">Terminate worker</span></span>     |
| <span data-ttu-id="a293e-560">OPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="a293e-560">RESIGNATION</span></span>            | <span data-ttu-id="a293e-561">Opsigelse</span><span class="sxs-lookup"><span data-stu-id="a293e-561">Resignation</span></span>                    | <span data-ttu-id="a293e-562">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="a293e-562">Terminate worker</span></span>     |
| <span data-ttu-id="a293e-563">PENSION</span><span class="sxs-lookup"><span data-stu-id="a293e-563">PENSION</span></span>                | <span data-ttu-id="a293e-564">Pension</span><span class="sxs-lookup"><span data-stu-id="a293e-564">Pension</span></span>                        | <span data-ttu-id="a293e-565">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="a293e-565">Terminate worker</span></span>     |
| <span data-ttu-id="a293e-566">OPHØR</span><span class="sxs-lookup"><span data-stu-id="a293e-566">TERMINATION</span></span>            | <span data-ttu-id="a293e-567">Ophør</span><span class="sxs-lookup"><span data-stu-id="a293e-567">Termination</span></span>                    | <span data-ttu-id="a293e-568">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="a293e-568">Terminate worker</span></span>     |
| <span data-ttu-id="a293e-569">PENSION</span><span class="sxs-lookup"><span data-stu-id="a293e-569">RETIREMENT</span></span>             | <span data-ttu-id="a293e-570">Pension</span><span class="sxs-lookup"><span data-stu-id="a293e-570">Retirement</span></span>                     | <span data-ttu-id="a293e-571">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="a293e-571">Terminate worker</span></span>     |
| <span data-ttu-id="a293e-572">FRAVÆRENDE</span><span class="sxs-lookup"><span data-stu-id="a293e-572">ABSENTEE</span></span>               | <span data-ttu-id="a293e-573">Fraværende</span><span class="sxs-lookup"><span data-stu-id="a293e-573">Absentee</span></span>                       | <span data-ttu-id="a293e-574">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="a293e-574">Terminate worker</span></span>     |
| <span data-ttu-id="a293e-575">ANDET</span><span class="sxs-lookup"><span data-stu-id="a293e-575">OTHER</span></span>                  | <span data-ttu-id="a293e-576">Andre årsager</span><span class="sxs-lookup"><span data-stu-id="a293e-576">Other Reasons</span></span>                  | <span data-ttu-id="a293e-577">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="a293e-577">Terminate worker</span></span>     |
| <span data-ttu-id="a293e-578">LUKNING</span><span class="sxs-lookup"><span data-stu-id="a293e-578">CLOSURE</span></span>                | <span data-ttu-id="a293e-579">Virksomhedslukning</span><span class="sxs-lookup"><span data-stu-id="a293e-579">Business Closure</span></span>               | <span data-ttu-id="a293e-580">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="a293e-580">Terminate worker</span></span>     |
| <span data-ttu-id="a293e-581">DØDSFALD</span><span class="sxs-lookup"><span data-stu-id="a293e-581">DEATH</span></span>                  | <span data-ttu-id="a293e-582">Dødsfald</span><span class="sxs-lookup"><span data-stu-id="a293e-582">Death</span></span>                          | <span data-ttu-id="a293e-583">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="a293e-583">Terminate worker</span></span>     |
| <span data-ttu-id="a293e-584">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="a293e-584">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="a293e-585">Orlov</span><span class="sxs-lookup"><span data-stu-id="a293e-585">Leave of Absence</span></span>               | <span data-ttu-id="a293e-586">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="a293e-586">Terminate worker</span></span>     |
| <span data-ttu-id="a293e-587">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="a293e-587">CONTRACTEND</span></span>            | <span data-ttu-id="a293e-588">Kontraktudløb</span><span class="sxs-lookup"><span data-stu-id="a293e-588">End of Contract</span></span>                | <span data-ttu-id="a293e-589">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="a293e-589">Terminate worker</span></span>     |
| <span data-ttu-id="a293e-590">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="a293e-590">SALARYCHANGE</span></span>           | <span data-ttu-id="a293e-591">Ændring af løn</span><span class="sxs-lookup"><span data-stu-id="a293e-591">Change of Salary</span></span>               | <span data-ttu-id="a293e-592">Kompensation</span><span class="sxs-lookup"><span data-stu-id="a293e-592">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="a293e-593">Ansættelsesvilkår</span><span class="sxs-lookup"><span data-stu-id="a293e-593">Terms of employment</span></span>

<span data-ttu-id="a293e-594">Ansættelsesvilkår bruges til at oprette kategorier for ansættelsesvilkår.</span><span class="sxs-lookup"><span data-stu-id="a293e-594">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="a293e-595">Vilkårene knyttes til Dayforce som beskæftigelsesindikatorværdier.</span><span class="sxs-lookup"><span data-stu-id="a293e-595">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="a293e-596">Følgende begreber for beskæftigelse og beskrivelser er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="a293e-596">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="a293e-597">Ansættelsesvilkår</span><span class="sxs-lookup"><span data-stu-id="a293e-597">Terms of employment</span></span>   | <span data-ttu-id="a293e-598">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="a293e-598">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="a293e-599">Regulær</span><span class="sxs-lookup"><span data-stu-id="a293e-599">Regular</span></span>               | <span data-ttu-id="a293e-600">Regulær</span><span class="sxs-lookup"><span data-stu-id="a293e-600">Regular</span></span>     |
| <span data-ttu-id="a293e-601">Direkte</span><span class="sxs-lookup"><span data-stu-id="a293e-601">Direct</span></span>                | <span data-ttu-id="a293e-602">Direkte</span><span class="sxs-lookup"><span data-stu-id="a293e-602">Direct</span></span>      |
| <span data-ttu-id="a293e-603">Turnustjeneste</span><span class="sxs-lookup"><span data-stu-id="a293e-603">Internship</span></span>            | <span data-ttu-id="a293e-604">Turnustjeneste</span><span class="sxs-lookup"><span data-stu-id="a293e-604">Internship</span></span>  |
| <span data-ttu-id="a293e-605">Permanent</span><span class="sxs-lookup"><span data-stu-id="a293e-605">Permanent</span></span>             | <span data-ttu-id="a293e-606">Permanent</span><span class="sxs-lookup"><span data-stu-id="a293e-606">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="a293e-607">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="a293e-607">Marital status</span></span>

<span data-ttu-id="a293e-608">Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="a293e-608">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="a293e-609">Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="a293e-609">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="a293e-610">Talent</span><span class="sxs-lookup"><span data-stu-id="a293e-610">Talent</span></span>                 | <span data-ttu-id="a293e-611">Dayforce</span><span class="sxs-lookup"><span data-stu-id="a293e-611">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="a293e-612">Gift</span><span class="sxs-lookup"><span data-stu-id="a293e-612">Married</span></span>                | <span data-ttu-id="a293e-613">Gift</span><span class="sxs-lookup"><span data-stu-id="a293e-613">Married</span></span>                   |
| <span data-ttu-id="a293e-614">Enlig</span><span class="sxs-lookup"><span data-stu-id="a293e-614">Single</span></span>                 | <span data-ttu-id="a293e-615">Enlig</span><span class="sxs-lookup"><span data-stu-id="a293e-615">Single</span></span>                    |
| <span data-ttu-id="a293e-616">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="a293e-616">Widowed</span></span>                | <span data-ttu-id="a293e-617">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="a293e-617">Widowed</span></span>                   |
| <span data-ttu-id="a293e-618">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="a293e-618">Divorced</span></span>               | <span data-ttu-id="a293e-619">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="a293e-619">Divorced</span></span>                  |
| <span data-ttu-id="a293e-620">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="a293e-620">Registered Partnership</span></span> | <span data-ttu-id="a293e-621">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="a293e-621">Domestic Partnership</span></span>      |
| <span data-ttu-id="a293e-622">None</span><span class="sxs-lookup"><span data-stu-id="a293e-622">None</span></span>                   | <span data-ttu-id="a293e-623">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="a293e-623">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="a293e-624">Samlever</span><span class="sxs-lookup"><span data-stu-id="a293e-624">Cohabiting</span></span>             | <span data-ttu-id="a293e-625">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="a293e-625">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="a293e-626">Køn</span><span class="sxs-lookup"><span data-stu-id="a293e-626">Gender</span></span>

<span data-ttu-id="a293e-627">Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="a293e-627">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="a293e-628">Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="a293e-628">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="a293e-629">Talent</span><span class="sxs-lookup"><span data-stu-id="a293e-629">Talent</span></span>       | <span data-ttu-id="a293e-630">Dayforce</span><span class="sxs-lookup"><span data-stu-id="a293e-630">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="a293e-631">Mand</span><span class="sxs-lookup"><span data-stu-id="a293e-631">Male</span></span>         | <span data-ttu-id="a293e-632">Mand</span><span class="sxs-lookup"><span data-stu-id="a293e-632">Male</span></span>                      |
| <span data-ttu-id="a293e-633">Kvinde</span><span class="sxs-lookup"><span data-stu-id="a293e-633">Female</span></span>       | <span data-ttu-id="a293e-634">Kvinde</span><span class="sxs-lookup"><span data-stu-id="a293e-634">Female</span></span>                    |
| <span data-ttu-id="a293e-635">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="a293e-635">Non-specific</span></span> | <span data-ttu-id="a293e-636">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="a293e-636">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="a293e-637">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="a293e-637">Payment method</span></span>

<span data-ttu-id="a293e-638">Betalingsmetoder giver medarbejderen og virksomheden en måde til at beskrive, hvordan medarbejdere skal betales.</span><span class="sxs-lookup"><span data-stu-id="a293e-638">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="a293e-639">Betalingsmåder knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="a293e-639">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="a293e-640">Følgende tabel viser, hvordan betalingsmetoder knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="a293e-640">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="a293e-641">Talent</span><span class="sxs-lookup"><span data-stu-id="a293e-641">Talent</span></span>             | <span data-ttu-id="a293e-642">Dayforce</span><span class="sxs-lookup"><span data-stu-id="a293e-642">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="a293e-643">Indløsning</span><span class="sxs-lookup"><span data-stu-id="a293e-643">Cash</span></span>               | <span data-ttu-id="a293e-644">Indløsning</span><span class="sxs-lookup"><span data-stu-id="a293e-644">Cash</span></span>                      |
| <span data-ttu-id="a293e-645">Elektronisk betaling</span><span class="sxs-lookup"><span data-stu-id="a293e-645">Electronic Payment</span></span> | <span data-ttu-id="a293e-646">Ompostering</span><span class="sxs-lookup"><span data-stu-id="a293e-646">Transfer</span></span>                  |
| <span data-ttu-id="a293e-647">Check</span><span class="sxs-lookup"><span data-stu-id="a293e-647">Check</span></span>              | <span data-ttu-id="a293e-648">Check</span><span class="sxs-lookup"><span data-stu-id="a293e-648">Cheque</span></span>                    |
| <span data-ttu-id="a293e-649">Bankanvisning</span><span class="sxs-lookup"><span data-stu-id="a293e-649">Bank Draft</span></span>         | <span data-ttu-id="a293e-650">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="a293e-650">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="a293e-651">Andre</span><span class="sxs-lookup"><span data-stu-id="a293e-651">Other</span></span>              | <span data-ttu-id="a293e-652">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="a293e-652">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="a293e-653">Bankkontotype</span><span class="sxs-lookup"><span data-stu-id="a293e-653">Bank account type</span></span>

<span data-ttu-id="a293e-654">Bankkontotyper bruges til elektroniske betalinger til medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="a293e-654">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="a293e-655">Bankkontotyper knyttes til Dayforce som overførselskontooplysninger.</span><span class="sxs-lookup"><span data-stu-id="a293e-655">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="a293e-656">Bankkontotyperne oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="a293e-656">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="a293e-657">Talent</span><span class="sxs-lookup"><span data-stu-id="a293e-657">Talent</span></span>            | <span data-ttu-id="a293e-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="a293e-658">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="a293e-659">Checkkonto</span><span class="sxs-lookup"><span data-stu-id="a293e-659">Checking Account</span></span>  | <span data-ttu-id="a293e-660">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="a293e-660">CheckingAccount</span></span>           |
| <span data-ttu-id="a293e-661">Lønkonto</span><span class="sxs-lookup"><span data-stu-id="a293e-661">Payroll Account</span></span>   | <span data-ttu-id="a293e-662">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="a293e-662">PayrollAccount</span></span>            |
| <span data-ttu-id="a293e-663">Opsparingskonto</span><span class="sxs-lookup"><span data-stu-id="a293e-663">Savings Account</span></span>   | <span data-ttu-id="a293e-664">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="a293e-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="a293e-665">BankGirot-konto</span><span class="sxs-lookup"><span data-stu-id="a293e-665">BankGirot account</span></span> | <span data-ttu-id="a293e-666">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="a293e-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="a293e-667">PlusGirot-konto</span><span class="sxs-lookup"><span data-stu-id="a293e-667">PlusGirot account</span></span> | <span data-ttu-id="a293e-668">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="a293e-668">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="a293e-669">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="a293e-669">Earning codes</span></span>

<span data-ttu-id="a293e-670">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="a293e-670">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="a293e-671">Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="a293e-671">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="a293e-672">Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="a293e-672">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="a293e-673">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="a293e-673">Supported frequencies</span></span>

- <span data-ttu-id="a293e-674">Alt</span><span class="sxs-lookup"><span data-stu-id="a293e-674">All</span></span>
- <span data-ttu-id="a293e-675">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="a293e-675">EVERYPAY</span></span>
- <span data-ttu-id="a293e-676">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="a293e-676">EACHPAYPERIOD</span></span>
- <span data-ttu-id="a293e-677">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="a293e-677">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="a293e-678">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="a293e-678">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="a293e-679">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-679">1OFMTH</span></span>
- <span data-ttu-id="a293e-680">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-680">LASTOFMTH</span></span>
- <span data-ttu-id="a293e-681">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-681">2OFMTH</span></span>
- <span data-ttu-id="a293e-682">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-682">3OFMTH</span></span>
- <span data-ttu-id="a293e-683">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-683">4OFMTH</span></span>
- <span data-ttu-id="a293e-684">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-684">5OFMTH</span></span>
- <span data-ttu-id="a293e-685">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-685">1N2OFMTH</span></span>
- <span data-ttu-id="a293e-686">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-686">3N4OFMTH</span></span>
- <span data-ttu-id="a293e-687">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-687">1N3OFMTH</span></span>
- <span data-ttu-id="a293e-688">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-688">1N4OFMTH</span></span>
- <span data-ttu-id="a293e-689">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-689">2N3OFMTH</span></span>
- <span data-ttu-id="a293e-690">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-690">2N4OFMTH</span></span>
- <span data-ttu-id="a293e-691">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-691">1N2N3OFMTH</span></span>
- <span data-ttu-id="a293e-692">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-692">1N2N4OFMTH</span></span>
- <span data-ttu-id="a293e-693">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-693">1N3N4OFMTH</span></span>
- <span data-ttu-id="a293e-694">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-694">2N3N4OFMTH</span></span>
- <span data-ttu-id="a293e-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="a293e-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="a293e-696">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="a293e-696">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="a293e-697">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="a293e-697">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="a293e-698">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="a293e-698">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="a293e-699">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="a293e-699">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="a293e-700">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="a293e-700">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="a293e-701">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="a293e-701">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="a293e-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="a293e-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="a293e-703">Adresser</span><span class="sxs-lookup"><span data-stu-id="a293e-703">Addresses</span></span>

<span data-ttu-id="a293e-704">Identifikation af specifikke koder for land eller region, stat og område (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende.</span><span class="sxs-lookup"><span data-stu-id="a293e-704">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="a293e-705">Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.</span><span class="sxs-lookup"><span data-stu-id="a293e-705">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="a293e-706">Talent</span><span class="sxs-lookup"><span data-stu-id="a293e-706">Talent</span></span>              | <span data-ttu-id="a293e-707">Dayforce</span><span class="sxs-lookup"><span data-stu-id="a293e-707">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="a293e-708">Land/område</span><span class="sxs-lookup"><span data-stu-id="a293e-708">Country/Region</span></span>      | <span data-ttu-id="a293e-709">Landekode</span><span class="sxs-lookup"><span data-stu-id="a293e-709">Country Code</span></span>          |
| <span data-ttu-id="a293e-710">Postnummer</span><span class="sxs-lookup"><span data-stu-id="a293e-710">Zip/Postal Code</span></span>     | <span data-ttu-id="a293e-711">Postnummer</span><span class="sxs-lookup"><span data-stu-id="a293e-711">Postal Code</span></span>           |
| <span data-ttu-id="a293e-712">Status</span><span class="sxs-lookup"><span data-stu-id="a293e-712">State</span></span>               | <span data-ttu-id="a293e-713">Statskode</span><span class="sxs-lookup"><span data-stu-id="a293e-713">State Code</span></span>            |
| <span data-ttu-id="a293e-714">Bynavn</span><span class="sxs-lookup"><span data-stu-id="a293e-714">City</span></span>                | <span data-ttu-id="a293e-715">Bynavn</span><span class="sxs-lookup"><span data-stu-id="a293e-715">City</span></span>                  |
| <span data-ttu-id="a293e-716">Region</span><span class="sxs-lookup"><span data-stu-id="a293e-716">County</span></span>              | <span data-ttu-id="a293e-717">Område (kommune)</span><span class="sxs-lookup"><span data-stu-id="a293e-717">County (Municipality)</span></span> |
| <span data-ttu-id="a293e-718">Gade</span><span class="sxs-lookup"><span data-stu-id="a293e-718">Street</span></span>              | <span data-ttu-id="a293e-719">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="a293e-719">Address Line 1</span></span>        |
| <span data-ttu-id="a293e-720">Gadenummer</span><span class="sxs-lookup"><span data-stu-id="a293e-720">Street Number</span></span>       | <span data-ttu-id="a293e-721">Adresselinje 2</span><span class="sxs-lookup"><span data-stu-id="a293e-721">Address Line 2</span></span>        |
| <span data-ttu-id="a293e-722">Bygningskomplement</span><span class="sxs-lookup"><span data-stu-id="a293e-722">Building Complement</span></span> | <span data-ttu-id="a293e-723">Adresselinje 5</span><span class="sxs-lookup"><span data-stu-id="a293e-723">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="a293e-724">Pasnummer</span><span class="sxs-lookup"><span data-stu-id="a293e-724">Passport number</span></span>

<span data-ttu-id="a293e-725">Medarbejdere kan erklære pasoplysninger.</span><span class="sxs-lookup"><span data-stu-id="a293e-725">Employees can declare passport information.</span></span> <span data-ttu-id="a293e-726">Disse oplysninger er af identifikationstypen **Pas** og er integreret i Dayforce som en del af en medarbejders Mexico-specifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="a293e-726">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="a293e-727">Identifikationstype = "Pas"</span><span class="sxs-lookup"><span data-stu-id="a293e-727">Identification Type = "Passport"</span></span>
- <span data-ttu-id="a293e-728">Udstedt den</span><span class="sxs-lookup"><span data-stu-id="a293e-728">Issued Date</span></span>
- <span data-ttu-id="a293e-729">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="a293e-729">Expiration Date</span></span>

<span data-ttu-id="a293e-730">Medarbejdere kan angive flere identifikationsnumre af **Pas**-identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="a293e-730">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="a293e-731">Men det er kun den aktuelle aktive paspost, der integreres i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="a293e-731">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="a293e-732">Hvis alle pasposter er udløbet, integreres det pas, der senest blev udstedt, i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="a293e-732">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
