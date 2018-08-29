---
title: "Konfigurere lønintegration mellem Talent og Dayforce"
description: "Dette emne forklarer, hvordan du kan konfigurere integration mellem Microsoft Dynamics 365 for Talent og Ceridian Dayforce, så du kan behandle en lønkørsel."
author: jcart1106
manager: AnnBe
ms.date: 07/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: fcddf82cffb9f0ba94b83eb21809b810585ebc9e
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---

# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="67c83-103">Konfigurere lønintegration mellem Talent og Dayforce</span><span class="sxs-lookup"><span data-stu-id="67c83-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="67c83-104">Integration mellem Microsoft Dynamics 365 for Talent og Ceridian Dayforce er baseret på flere konfigurationstrin, der er beskrevet i dette emne.</span><span class="sxs-lookup"><span data-stu-id="67c83-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="67c83-105">Du skal konfigurere integrationen i både Talent og Dayforce, før du kan behandle en lønkørsel.</span><span class="sxs-lookup"><span data-stu-id="67c83-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="67c83-106">Når du bruger en tjeneste, f.eks. Dayforce, til at fuldføre lønkørsler, skal du aktivere integrationen i Talent.</span><span class="sxs-lookup"><span data-stu-id="67c83-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="67c83-107">Integrationen kræver bestemte data fra Talent.</span><span class="sxs-lookup"><span data-stu-id="67c83-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="67c83-108">Du skal derfor kontrollere, at data, der er knyttet til Dayforce, er konfigureret i Talent på en måde, der understøtter integrationen.</span><span class="sxs-lookup"><span data-stu-id="67c83-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="67c83-109">Integrationen bruger følgende brede kategorier af data.</span><span class="sxs-lookup"><span data-stu-id="67c83-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="67c83-110">Personaledata</span><span class="sxs-lookup"><span data-stu-id="67c83-110">Human resources data</span></span>
- <span data-ttu-id="67c83-111">Kompensationsdata</span><span class="sxs-lookup"><span data-stu-id="67c83-111">Compensation data</span></span>
- <span data-ttu-id="67c83-112">Lønoplysninger, f.eks. løncyklusser, betalingsperioder og lønkoder</span><span class="sxs-lookup"><span data-stu-id="67c83-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="67c83-113">Arbejderdata</span><span class="sxs-lookup"><span data-stu-id="67c83-113">Worker data</span></span>

<span data-ttu-id="67c83-114">Dette emne beskrives de trin, du skal udføre for at aktivere integrationen.</span><span class="sxs-lookup"><span data-stu-id="67c83-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="67c83-115">Det forklarer også typerne af data og oplysninger om konfigurationen, der kræves til integrationen.</span><span class="sxs-lookup"><span data-stu-id="67c83-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="67c83-116">Aktivere integrationen.</span><span class="sxs-lookup"><span data-stu-id="67c83-116">Enable the integration</span></span>

<span data-ttu-id="67c83-117">I Talent skal du aktivere integrationen og angive konfigurationsoplysningerne for at oprette forbindelse til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="67c83-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="67c83-118">Hvis den finanspostering, der er produceret, skal importeres til Microsoft Dynamics 365 for Finance and Operations, skal du også konfigurere en Microsoft Azure-lagerkonto og angive Azure-lagerets forbindelsesstreng i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="67c83-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="67c83-119">Følg disse trin for at aktivere integrationen i Talent.</span><span class="sxs-lookup"><span data-stu-id="67c83-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="67c83-120">På siden **Systemadministration** skal du vælge **Integrationskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="67c83-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="67c83-121">Angiv det sikre FTP-slutpunkt og den sikre FTP-mappesti.</span><span class="sxs-lookup"><span data-stu-id="67c83-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="67c83-122">Angiv brugernavnet og adgangskoden for den bruger, der skal have adgang til det sikre FTP-slutpunkt og den sikre mappesti.</span><span class="sxs-lookup"><span data-stu-id="67c83-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="67c83-123">Test forbindelsen, som krævet, og angiv indstillingen **Aktivér lønintegration** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="67c83-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="67c83-124">Når integrationen er aktiveret, oprettes dataeksportpakken og -filerne, og hyppigheden angives.</span><span class="sxs-lookup"><span data-stu-id="67c83-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="67c83-125">Du kan ændre denne frekvens efter behov.</span><span class="sxs-lookup"><span data-stu-id="67c83-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="67c83-126">Yderligere oplysninger om Azure-lagerkonti og Azure-lagerforbindelsesstrenge finder du i følgende Azure-emner:</span><span class="sxs-lookup"><span data-stu-id="67c83-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="67c83-127">Om Azure-lagerkonti</span><span class="sxs-lookup"><span data-stu-id="67c83-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="67c83-128">Konfigurere forbindelsesstrenge for Azure-datalager</span><span class="sxs-lookup"><span data-stu-id="67c83-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="67c83-129">Konfigurere dine data</span><span class="sxs-lookup"><span data-stu-id="67c83-129">Configure your data</span></span> 

<span data-ttu-id="67c83-130">Hvis du vil behandle løn, skal du konfigurere personaledata i Talent.</span><span class="sxs-lookup"><span data-stu-id="67c83-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="67c83-131">Du skal angive virksomhedens data, f.eks. job og stillinger, sammen med frynsegoder og kompensationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="67c83-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="67c83-132">Disse oplysninger indeholder oplysningerne om ansættelse, løn og fradrag, der kræves for at generere løn for medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="67c83-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="67c83-133">Personaledata</span><span class="sxs-lookup"><span data-stu-id="67c83-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="67c83-134">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="67c83-134">Benefits</span></span> 

<span data-ttu-id="67c83-135">Personale indeholder en række værktøjer til konfiguration og vedligeholdelse af frynsegoder, fradrag og arbejderkompensationsplaner, som en organisation tilbyder eller behandler for sine ansatte.</span><span class="sxs-lookup"><span data-stu-id="67c83-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="67c83-136">Når du opretter frynsegoder, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="67c83-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="67c83-137">Frynsegodeplaner</span><span class="sxs-lookup"><span data-stu-id="67c83-137">Benefit plans</span></span>

- <span data-ttu-id="67c83-138">Plan (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-138">Plan (required)</span></span>
- <span data-ttu-id="67c83-139">Type (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-139">Type (required)</span></span>
- <span data-ttu-id="67c83-140">Løneffekt (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-140">Payroll impact (required)</span></span>
- <span data-ttu-id="67c83-141">Opkræv restancer</span><span class="sxs-lookup"><span data-stu-id="67c83-141">Recover arrears</span></span>
- <span data-ttu-id="67c83-142">Fradragsmetode</span><span class="sxs-lookup"><span data-stu-id="67c83-142">Deduction method</span></span>
- <span data-ttu-id="67c83-143">Prioriteret fradrag</span><span class="sxs-lookup"><span data-stu-id="67c83-143">Deduction priority</span></span>
- <span data-ttu-id="67c83-144">Grænseperiode</span><span class="sxs-lookup"><span data-stu-id="67c83-144">Limit period</span></span>
- <span data-ttu-id="67c83-145">Beløb for grænse</span><span class="sxs-lookup"><span data-stu-id="67c83-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="67c83-146">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="67c83-146">Benefits</span></span>

- <span data-ttu-id="67c83-147">Plan (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-147">Plan (required)</span></span>
- <span data-ttu-id="67c83-148">Type (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-148">Type (required)</span></span>
- <span data-ttu-id="67c83-149">Mulighed (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-149">Option (required)</span></span>
- <span data-ttu-id="67c83-150">Frynsegode-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-150">Benefit ID (required)</span></span>
- <span data-ttu-id="67c83-151">Frekvens</span><span class="sxs-lookup"><span data-stu-id="67c83-151">Frequency</span></span>
- <span data-ttu-id="67c83-152">Basis</span><span class="sxs-lookup"><span data-stu-id="67c83-152">Basis</span></span>
- <span data-ttu-id="67c83-153">Beløb eller sats</span><span class="sxs-lookup"><span data-stu-id="67c83-153">Amount or rate</span></span>
- <span data-ttu-id="67c83-154">Lønkode</span><span class="sxs-lookup"><span data-stu-id="67c83-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="67c83-155">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="67c83-155">Supported frequencies</span></span> 

- <span data-ttu-id="67c83-156">Ugentlig</span><span class="sxs-lookup"><span data-stu-id="67c83-156">Weekly</span></span>
- <span data-ttu-id="67c83-157">Pr. 14 dage</span><span class="sxs-lookup"><span data-stu-id="67c83-157">Bi-weekly</span></span>
- <span data-ttu-id="67c83-158">To gange om måneden</span><span class="sxs-lookup"><span data-stu-id="67c83-158">Semi-monthly</span></span>
- <span data-ttu-id="67c83-159">Månedlig</span><span class="sxs-lookup"><span data-stu-id="67c83-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="67c83-160">Understøttede grundlag</span><span class="sxs-lookup"><span data-stu-id="67c83-160">Supported bases</span></span> 

- <span data-ttu-id="67c83-161">Fast beløb</span><span class="sxs-lookup"><span data-stu-id="67c83-161">Fixed amount</span></span>
- <span data-ttu-id="67c83-162">Procentdel af løn</span><span class="sxs-lookup"><span data-stu-id="67c83-162">Percent of earnings</span></span>
- <span data-ttu-id="67c83-163">Produktive timer</span><span class="sxs-lookup"><span data-stu-id="67c83-163">Productive hours</span></span>

<span data-ttu-id="67c83-164">Dayforce opretter følgende fradrag, der er baseret på den løneffekt, der er defineret på frynsegodeplanen.</span><span class="sxs-lookup"><span data-stu-id="67c83-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="67c83-165">Valg i Talent</span><span class="sxs-lookup"><span data-stu-id="67c83-165">Selection in Talent</span></span>        | <span data-ttu-id="67c83-166">Resultat i Dayforce</span><span class="sxs-lookup"><span data-stu-id="67c83-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="67c83-167">None</span><span class="sxs-lookup"><span data-stu-id="67c83-167">None</span></span>                       | <span data-ttu-id="67c83-168">Der oprettes ikke noget fradrag.</span><span class="sxs-lookup"><span data-stu-id="67c83-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="67c83-169">Kun fradrag</span><span class="sxs-lookup"><span data-stu-id="67c83-169">Deduction only</span></span>             | <span data-ttu-id="67c83-170">Der oprettes et medarbejderfradrag.</span><span class="sxs-lookup"><span data-stu-id="67c83-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="67c83-171">Kun bidrag</span><span class="sxs-lookup"><span data-stu-id="67c83-171">Contribution only</span></span>          | <span data-ttu-id="67c83-172">Der oprettes et arbejdsgiverfradrag.</span><span class="sxs-lookup"><span data-stu-id="67c83-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="67c83-173">Fradrag og bidrag</span><span class="sxs-lookup"><span data-stu-id="67c83-173">Deduction and contribution</span></span> | <span data-ttu-id="67c83-174">Der oprettes medarbejder- og arbejdsgiverfradrag.</span><span class="sxs-lookup"><span data-stu-id="67c83-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="67c83-175">Du kan finde flere oplysninger om, hvordan du definerer og administrerer et frynsegodeprogram under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="67c83-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="67c83-176">Levere et frynsegodeprogram for medarbejdere</span><span class="sxs-lookup"><span data-stu-id="67c83-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="67c83-177">Oprette et nyt frynsegode</span><span class="sxs-lookup"><span data-stu-id="67c83-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="67c83-178">Definere regler og politikker for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="67c83-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="67c83-179">Tilmelde og fjerne frynsegoder fra arbejdere</span><span class="sxs-lookup"><span data-stu-id="67c83-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="67c83-180">Kompensation</span><span class="sxs-lookup"><span data-stu-id="67c83-180">Compensation</span></span> 

<span data-ttu-id="67c83-181">Kompensationsstyring bruges til at styre fordelingen af grundløn og bonusser.</span><span class="sxs-lookup"><span data-stu-id="67c83-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="67c83-182">En medarbejders faste grundløn og kvalifikationstillæg styres gennem faste lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="67c83-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="67c83-183">Betalingen af incitamentsløn som f.eks. bonusudbetalinger, præstationsbonusser, aktieoptioner og tildelte aktier samt engangsbonusser styres ved hjælp af variable lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="67c83-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="67c83-184">Dayforce anvendes kompensationsoplysninger til at beregne en medarbejders timesats eller årlige sats.</span><span class="sxs-lookup"><span data-stu-id="67c83-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="67c83-185">Konverteringer af planer for fast løn og lønsats er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="67c83-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="67c83-186">Medarbejderne skal være knyttet til en plan for fast løn.</span><span class="sxs-lookup"><span data-stu-id="67c83-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="67c83-187">Du kan finde flere oplysninger om kompensationsplaner under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="67c83-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="67c83-188">Oprette faste kompensationsordninger</span><span class="sxs-lookup"><span data-stu-id="67c83-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="67c83-189">Oprette planer for variabel kompensation</span><span class="sxs-lookup"><span data-stu-id="67c83-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="67c83-190">Udarbejde løn-/kompensationsstruktur og -planer</span><span class="sxs-lookup"><span data-stu-id="67c83-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="67c83-191">Proceskompensation</span><span class="sxs-lookup"><span data-stu-id="67c83-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="67c83-192">Definere kompensationsproces og beregne resultater</span><span class="sxs-lookup"><span data-stu-id="67c83-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="67c83-193">Melde en medarbejder til en fast lønplan</span><span class="sxs-lookup"><span data-stu-id="67c83-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="67c83-194">Melde en medarbejder til en variabel lønplan</span><span class="sxs-lookup"><span data-stu-id="67c83-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="67c83-195">Job</span><span class="sxs-lookup"><span data-stu-id="67c83-195">Jobs</span></span> 

<span data-ttu-id="67c83-196">Et job er en samling af de opgaver og ansvarsområder, der kræves af en person, der udfører et job.</span><span class="sxs-lookup"><span data-stu-id="67c83-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="67c83-197">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="67c83-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="67c83-198">Konfiguration af komponenter i et job</span><span class="sxs-lookup"><span data-stu-id="67c83-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="67c83-199">Definere nye job</span><span class="sxs-lookup"><span data-stu-id="67c83-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="67c83-200">Stillinger</span><span class="sxs-lookup"><span data-stu-id="67c83-200">Positions</span></span>

<span data-ttu-id="67c83-201">En stilling er en individuel forekomst af et job.</span><span class="sxs-lookup"><span data-stu-id="67c83-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="67c83-202">For eksempel er stillingen "Salgschef (øst)" én af de stillinger, der er tilknyttet jobbet "Salgschef".</span><span class="sxs-lookup"><span data-stu-id="67c83-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="67c83-203">En stilling findes i en afdeling.</span><span class="sxs-lookup"><span data-stu-id="67c83-203">A position exists in a department.</span></span> <span data-ttu-id="67c83-204">Der kan kun knyttes én arbejder til hver stilling.</span><span class="sxs-lookup"><span data-stu-id="67c83-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="67c83-205">Hav følgende data og konfiguration i tankerne, når du konfigurerer stillinger:</span><span class="sxs-lookup"><span data-stu-id="67c83-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="67c83-206">Stilling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-206">Position (required)</span></span>
- <span data-ttu-id="67c83-207">Beskrivelse (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-207">Description (required)</span></span>
- <span data-ttu-id="67c83-208">Job (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-208">Job (required)</span></span>
- <span data-ttu-id="67c83-209">Afdeling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-209">Department (required)</span></span>
- <span data-ttu-id="67c83-210">Stillingstype (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-210">Position type (required)</span></span>
- <span data-ttu-id="67c83-211">Fuldtidsækvivalent</span><span class="sxs-lookup"><span data-stu-id="67c83-211">Full-time equivalent</span></span>
- <span data-ttu-id="67c83-212">Normaltimer på årsbasis (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="67c83-213">Betalt af juridiske enhed (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="67c83-214">Betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-214">Pay cycle (required)</span></span>
- <span data-ttu-id="67c83-215">Økonomisk standarddimension – bærer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="67c83-216">Arbejdertildeling – arbejder, tildelingsstart, tildelingsslut, årsagskode</span><span class="sxs-lookup"><span data-stu-id="67c83-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="67c83-217">Hvis flere stillinger i den samme afdeling er knyttet til samme job, konsolideres de til en enkelt stilling i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="67c83-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="67c83-218">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="67c83-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="67c83-219">Organisere dine medarbejdere ved hjælp af afdelinger, jobs og stillinger</span><span class="sxs-lookup"><span data-stu-id="67c83-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="67c83-220">Konfigurere stillinger</span><span class="sxs-lookup"><span data-stu-id="67c83-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="67c83-221">Afdelinger</span><span class="sxs-lookup"><span data-stu-id="67c83-221">Departments</span></span>

<span data-ttu-id="67c83-222">En afdeling er en driftsenhed, der repræsenterer en kategori eller et funktionsområde i en organisation.</span><span class="sxs-lookup"><span data-stu-id="67c83-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="67c83-223">En afdeling er ansvarlig for et bestemt område i organisationen, såsom salg, regnskab eller personale.</span><span class="sxs-lookup"><span data-stu-id="67c83-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="67c83-224">Du kan bruge afdelinger til at rapportere om funktionsområder.</span><span class="sxs-lookup"><span data-stu-id="67c83-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="67c83-225">Afdelinger kan have ansvar for driftsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="67c83-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="67c83-226">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="67c83-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="67c83-227">Oprette en afdeling og knytte den til afdelingshierarkiet</span><span class="sxs-lookup"><span data-stu-id="67c83-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="67c83-228">Definere nye afdelinger</span><span class="sxs-lookup"><span data-stu-id="67c83-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="67c83-229">Betalingscyklusser og lønperioder</span><span class="sxs-lookup"><span data-stu-id="67c83-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="67c83-230">En betalingscyklus bestemmer, hvor ofte løn køres,og de specifikke dage, hvor arbejdere betales.</span><span class="sxs-lookup"><span data-stu-id="67c83-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="67c83-231">En løncyklus kan f.eks. være månedlig, og medarbejdere betales måske på den sidste dag i måneden.</span><span class="sxs-lookup"><span data-stu-id="67c83-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="67c83-232">En løncyklus kan også være ugentligt, og medarbejdere betales måske tirsdag efter slutningen af lønperioden.</span><span class="sxs-lookup"><span data-stu-id="67c83-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="67c83-233">Løncyklusser tildeles til stillinger for at styre, hvornår arbejdere i disse stillinger bliver betalt.</span><span class="sxs-lookup"><span data-stu-id="67c83-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="67c83-234">Når du opretter betalingscyklusser, kan du generere lønperioder for hver cyklus.</span><span class="sxs-lookup"><span data-stu-id="67c83-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="67c83-235">Hver lønperiode omfatter en standardbetalingsdato, der er baseret på oplysninger, du angiver.</span><span class="sxs-lookup"><span data-stu-id="67c83-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="67c83-236">Du kan dog redigere standardbetalingsdatoen i en lønperiode til at tillade undtagelser, f.eks. når betalingsdatoen falder på en helligdag.</span><span class="sxs-lookup"><span data-stu-id="67c83-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="67c83-237">Følgende oplysninger bruges i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="67c83-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="67c83-238">Betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-238">Pay cycle (required)</span></span>
- <span data-ttu-id="67c83-239">Hyppighed for betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="67c83-240">Periodens startdato (første lønperiode påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="67c83-241">Standardbetalingsdato (første lønperiode påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="67c83-242">Oplysningerne er integreret med Dayforce som løngrupper og adskilles af et land eller område for hver løncyklus.</span><span class="sxs-lookup"><span data-stu-id="67c83-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="67c83-243">Mindst én periode skal genereres før integration.</span><span class="sxs-lookup"><span data-stu-id="67c83-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="67c83-244">Dayforce genererer løngruppekalendere og betalingsdatoer, der er baseret på startdatoen for den første lønperiode og den standardbetalingsdato, der er angivet i Talent.</span><span class="sxs-lookup"><span data-stu-id="67c83-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="67c83-245">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="67c83-245">Earning codes</span></span>

<span data-ttu-id="67c83-246">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="67c83-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="67c83-247">Koderne har forskellige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="67c83-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="67c83-248">Følgende oplysninger bruges i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="67c83-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="67c83-249">Lønkode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-249">Earning Code (required)</span></span>
- <span data-ttu-id="67c83-250">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="67c83-250">Description</span></span>
- <span data-ttu-id="67c83-251">Måleenhed</span><span class="sxs-lookup"><span data-stu-id="67c83-251">Unit of measure</span></span>
- <span data-ttu-id="67c83-252">Produktiv</span><span class="sxs-lookup"><span data-stu-id="67c83-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="67c83-253">Arbejderdata</span><span class="sxs-lookup"><span data-stu-id="67c83-253">Worker data</span></span>

<span data-ttu-id="67c83-254">Posterne for de forskellige typer arbejdere, du beskæftiger, er vigtige for dine personale- og lønsystemer.</span><span class="sxs-lookup"><span data-stu-id="67c83-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="67c83-255">De oplysninger, du angiver, kan bruges til at spore arbejdere og personoplysninger.</span><span class="sxs-lookup"><span data-stu-id="67c83-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="67c83-256">Du kan vedligeholde følgende oplysninger for arbejdere:</span><span class="sxs-lookup"><span data-stu-id="67c83-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="67c83-257">**Basis** – Vedligehold grundlæggende oplysninger om en arbejder, f.eks. kontaktoplysninger, demografiske oplysninger, identifikationsoplysninger, oplysninger om familie, status for militærtjeneste, oplysninger om udstationering og personlige kontaktpersoner og kontaktpersoner i nødsituationer.</span><span class="sxs-lookup"><span data-stu-id="67c83-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="67c83-258">**Beskæftigelse** – Vedligehold oplysninger om en arbejders beskæftigelse, f.eks. firma- eller organisationstilhørsforhold, stillingstildeling, start- og slutdatoer, arbejdstilladelse, vilkår for ansættelse, pension, ferie og flytteoplysninger.</span><span class="sxs-lookup"><span data-stu-id="67c83-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="67c83-259">**Orlov og fravær** – Vedligehold oplysninger om en arbejders fravær, f.eks. arbejdskalendere, fraværstransaktioner og fraværsopsætning.</span><span class="sxs-lookup"><span data-stu-id="67c83-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="67c83-260">**Kompensation og løn** – Vedligehold oplysninger om en arbejders kompensationsplaner og lønoplysninger, f.eks. tilmelding til planer, priser, ydeevne, provision, skatteoplysninger, pensionering og skattefradrag.</span><span class="sxs-lookup"><span data-stu-id="67c83-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="67c83-261">Når du angiver arbejderoplysninger, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="67c83-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="67c83-262">Generelle oplysninger</span><span class="sxs-lookup"><span data-stu-id="67c83-262">General information</span></span>

- <span data-ttu-id="67c83-263">Personalenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-263">Personnel number (required)</span></span>
- <span data-ttu-id="67c83-264">Fornavn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-264">First name (required)</span></span>
- <span data-ttu-id="67c83-265">Efternavn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-265">Last name (required)</span></span>
- <span data-ttu-id="67c83-266">Mellemnavn</span><span class="sxs-lookup"><span data-stu-id="67c83-266">Middle name</span></span>
- <span data-ttu-id="67c83-267">Anciennitetsdato</span><span class="sxs-lookup"><span data-stu-id="67c83-267">Seniority date</span></span>
- <span data-ttu-id="67c83-268">Kendt som</span><span class="sxs-lookup"><span data-stu-id="67c83-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="67c83-269">Personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="67c83-269">Personal information</span></span>

- <span data-ttu-id="67c83-270">Ægteskabelig status (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-270">Marital status (required)</span></span>
- <span data-ttu-id="67c83-271">Fødselsdato (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-271">Birth date (required)</span></span>
- <span data-ttu-id="67c83-272">Køn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-272">Gender (required)</span></span>
- <span data-ttu-id="67c83-273">Handicappet</span><span class="sxs-lookup"><span data-stu-id="67c83-273">Person with disabilities</span></span>
- <span data-ttu-id="67c83-274">Land eller område for nationalitet (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="67c83-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="67c83-275">Adresseoplysninger</span><span class="sxs-lookup"><span data-stu-id="67c83-275">Address information</span></span>

- <span data-ttu-id="67c83-276">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-276">Primary (required)</span></span>
- <span data-ttu-id="67c83-277">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-277">Country/region (required)</span></span>
- <span data-ttu-id="67c83-278">Postnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-278">Postal code (required)</span></span>
- <span data-ttu-id="67c83-279">Gadenummer (påkrævet) (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="67c83-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="67c83-280">Bygningskomplement (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="67c83-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="67c83-281">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-281">City (required)</span></span>
- <span data-ttu-id="67c83-282">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-282">State (required)</span></span>
- <span data-ttu-id="67c83-283">Region (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="67c83-284">Kontaktoplysninger</span><span class="sxs-lookup"><span data-stu-id="67c83-284">Contact information</span></span> 

- <span data-ttu-id="67c83-285">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-285">Primary (required)</span></span>
- <span data-ttu-id="67c83-286">Kontaktpersonens nummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-286">Contact number (required)</span></span>
- <span data-ttu-id="67c83-287">Forlængelse</span><span class="sxs-lookup"><span data-stu-id="67c83-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="67c83-288">Lønoplysninger og lønkoder</span><span class="sxs-lookup"><span data-stu-id="67c83-288">Payroll information and earning codes</span></span>

<span data-ttu-id="67c83-289">Medarbejdere kan tildeles en bestemt løn med en given betalingshyppighed og have en foretrukken betalingsmetode.</span><span class="sxs-lookup"><span data-stu-id="67c83-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="67c83-290">Følgende felter bruges i Dayforce til at sikre, at disse præferencer og indstillinger bruges.</span><span class="sxs-lookup"><span data-stu-id="67c83-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="67c83-291">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="67c83-291">Earning codes</span></span>

- <span data-ttu-id="67c83-292">Stilling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-292">Position (required)</span></span>
- <span data-ttu-id="67c83-293">Lønkode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-293">Earning Code (required)</span></span>
- <span data-ttu-id="67c83-294">Frekvens (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-294">Frequency (required)</span></span>
- <span data-ttu-id="67c83-295">Beløb (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="67c83-296">Lønoplysninger</span><span class="sxs-lookup"><span data-stu-id="67c83-296">Payroll information</span></span>

- <span data-ttu-id="67c83-297">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="67c83-297">Payment Method</span></span>
- <span data-ttu-id="67c83-298">Økonomisk område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-298">Economic Region (required)</span></span>
- <span data-ttu-id="67c83-299">Id for medarbejderfrynsegoder</span><span class="sxs-lookup"><span data-stu-id="67c83-299">Employee Benefits ID</span></span>
- <span data-ttu-id="67c83-300">Nationalt id-nummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-300">National ID Number (required)</span></span>
- <span data-ttu-id="67c83-301">Tjenestenummer hos militær</span><span class="sxs-lookup"><span data-stu-id="67c83-301">Military Service Number</span></span>
- <span data-ttu-id="67c83-302">Skifte-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-302">Shift ID (required)</span></span>
- <span data-ttu-id="67c83-303">Skattenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-303">Tax Number (required)</span></span>
- <span data-ttu-id="67c83-304">Fagforenings-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-304">Union ID (required)</span></span>
- <span data-ttu-id="67c83-305">Arbejdsdags-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-305">Work Day ID (required)</span></span>
- <span data-ttu-id="67c83-306">Arbejdstilladelsesnummer</span><span class="sxs-lookup"><span data-stu-id="67c83-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="67c83-307">For betalingsmetoden understøtter Mexico **Kontant**, **Check** (firmaets fysiske check), og **Elektronisk betaling**.</span><span class="sxs-lookup"><span data-stu-id="67c83-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="67c83-308">Hvis der ikke er angivet nogen betalingsmetode, bruges **Check** som standard.</span><span class="sxs-lookup"><span data-stu-id="67c83-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="67c83-309">Detaljer om ansættelse</span><span class="sxs-lookup"><span data-stu-id="67c83-309">Employment details</span></span>

<span data-ttu-id="67c83-310">Detaljeret ansættelseshistorik bruges som vigtige oplysninger til at udlede statusser for en medarbejders ansættelse, fratrædelse og genansættelse i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="67c83-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="67c83-311">Dayforce understøtter kun én aktiv ansættelsespost ad gangen.</span><span class="sxs-lookup"><span data-stu-id="67c83-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="67c83-312">Startdato for ansættelse (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-312">Employment start date (required)</span></span>
- <span data-ttu-id="67c83-313">Slutdato for ansættelse</span><span class="sxs-lookup"><span data-stu-id="67c83-313">Employment end date</span></span>
- <span data-ttu-id="67c83-314">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="67c83-314">Start date</span></span>
- <span data-ttu-id="67c83-315">Justeret startdato</span><span class="sxs-lookup"><span data-stu-id="67c83-315">Adjusted start date</span></span>
- <span data-ttu-id="67c83-316">Fratrædelsesdato (kræves ved fratrædelse)</span><span class="sxs-lookup"><span data-stu-id="67c83-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="67c83-317">Fratrædelsesårsag (kræves ved fratrædelse)</span><span class="sxs-lookup"><span data-stu-id="67c83-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="67c83-318">Vigtige datoer for en medarbejders udledes ved hjælp af følgende oplysninger.</span><span class="sxs-lookup"><span data-stu-id="67c83-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="67c83-319">Talent</span><span class="sxs-lookup"><span data-stu-id="67c83-319">Talent</span></span>                | <span data-ttu-id="67c83-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="67c83-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67c83-321">Den seneste ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="67c83-321">Most recent hire date</span></span> | <span data-ttu-id="67c83-322">Historikpost for ansættelsesstart for aktuel ikke-afsluttet ansættelse</span><span class="sxs-lookup"><span data-stu-id="67c83-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="67c83-323">Fratrædelsesdato</span><span class="sxs-lookup"><span data-stu-id="67c83-323">Termination date</span></span>      | <span data-ttu-id="67c83-324">Historikpost for fratrædelsesdato for aktuel ikke-afsluttet ansættelse</span><span class="sxs-lookup"><span data-stu-id="67c83-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="67c83-325">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="67c83-325">Start date</span></span>            | <span data-ttu-id="67c83-326">Historikpost for justeret startdato, startdato eller startdato for ansættelse for aktuel ikke-aktiv ansættelse</span><span class="sxs-lookup"><span data-stu-id="67c83-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="67c83-327">Oprindelig ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="67c83-327">Original hire date</span></span>    | <span data-ttu-id="67c83-328">Historikpost for ansættelsesstart for tidligste ansættelse</span><span class="sxs-lookup"><span data-stu-id="67c83-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="67c83-329">Kompensation</span><span class="sxs-lookup"><span data-stu-id="67c83-329">Compensation</span></span>

<span data-ttu-id="67c83-330">En fast lønstruktur skal tilknyttes hver medarbejders primære stilling gennem hele ansættelsesperioden.</span><span class="sxs-lookup"><span data-stu-id="67c83-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="67c83-331">Denne periode starter på den dato, hvor medarbejderen blev ansat (eller ansættelsesstartdatoen) og fortsætter, indtil fratrædelsen.</span><span class="sxs-lookup"><span data-stu-id="67c83-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="67c83-332">Ikrafttrædelsesdato (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-332">Effective Date (required)</span></span>
- <span data-ttu-id="67c83-333">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="67c83-333">Expiration date</span></span>
- <span data-ttu-id="67c83-334">Lønsats (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-334">Pay Rate (required)</span></span>
- <span data-ttu-id="67c83-335">Konverteringer af lønsats (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="67c83-336">Årlig ækvivalent (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="67c83-337">Timebaseret ækvivalent (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="67c83-338">Hvis en timeansat medarbejder har flere stillinger, indlæses den faste løn for den primære stilling i Dayforce, som basissats/-løn på medarbejderniveau.</span><span class="sxs-lookup"><span data-stu-id="67c83-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="67c83-339">For ikke-primære stillinger gemmes timesatsen i den tilsvarende position i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="67c83-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="67c83-340">Hvis en funktionær har flere stillinger, afledes den kumulative timesats og årlig gage på tværs af alle aktive stillinger og bruges som basissats/-gage på medarbejderniveau.</span><span class="sxs-lookup"><span data-stu-id="67c83-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="67c83-341">Identifikationsnumre</span><span class="sxs-lookup"><span data-stu-id="67c83-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="67c83-342">Social Security-identifikator</span><span class="sxs-lookup"><span data-stu-id="67c83-342">Social Security identifier</span></span> 

<span data-ttu-id="67c83-343">Alle medarbejdere skal have én primær identifikator.</span><span class="sxs-lookup"><span data-stu-id="67c83-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="67c83-344">Identifikatoren skal være af **SSN**-identifikationstypen</span><span class="sxs-lookup"><span data-stu-id="67c83-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="67c83-345">I Dayforce afledes den automatisk som medarbejderens Social Security-identifikator, der er påkrævet ved ansættelse.</span><span class="sxs-lookup"><span data-stu-id="67c83-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="67c83-346">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-346">Primary (required)</span></span>
- <span data-ttu-id="67c83-347">Identifikationstype = "SSN"</span><span class="sxs-lookup"><span data-stu-id="67c83-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="67c83-348">Udstedt den</span><span class="sxs-lookup"><span data-stu-id="67c83-348">Issued Date</span></span>
- <span data-ttu-id="67c83-349">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="67c83-349">Expiration Date</span></span>

<span data-ttu-id="67c83-350">Medarbejdere kan angive flere identifikationsnumre af **SSN**-identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="67c83-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="67c83-351">Men det er kun den post, der er markeret som **Primær**, som er integreret i Dayforce, uanset om nummeret er aktivt eller udløbet.</span><span class="sxs-lookup"><span data-stu-id="67c83-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="67c83-352">Bankkonto og udbetalinger</span><span class="sxs-lookup"><span data-stu-id="67c83-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="67c83-353">Gyldige bankkontooplysninger skal angives for enhver medarbejder, der vælger at blive betalt via bankkontooverførsler.</span><span class="sxs-lookup"><span data-stu-id="67c83-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="67c83-354">Talent</span><span class="sxs-lookup"><span data-stu-id="67c83-354">Talent</span></span>                         | <span data-ttu-id="67c83-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="67c83-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67c83-356">Bankkontonummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="67c83-357">SWIFT-kode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-357">SWIFT code (required)</span></span>          | <span data-ttu-id="67c83-358">Feltet **Bank-id** bruges ved behandling af løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="67c83-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="67c83-359">Afdelingsnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="67c83-360">Bankkontotype (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-360">Bank account type (required)</span></span>   | <span data-ttu-id="67c83-361">Feltet **Kontotype** bruges ved behandling af løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="67c83-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="67c83-362">Understøttede værdier omfatter **Check** og **Løn**.</span><span class="sxs-lookup"><span data-stu-id="67c83-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="67c83-363">Medarbejdere, der vælger at betales via bankkontooverførsler, skal angive et link til en restbeløbskonto, der hører under en juridisk enhed, som har primær adresse i Mexico og er knyttet til en gyldig bankkonto fra en mexicansk bank.</span><span class="sxs-lookup"><span data-stu-id="67c83-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="67c83-364">Alle andre restbeløbskonti ignoreres.</span><span class="sxs-lookup"><span data-stu-id="67c83-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="67c83-365">Adresseoplysninger</span><span class="sxs-lookup"><span data-stu-id="67c83-365">Address information</span></span>

<span data-ttu-id="67c83-366">Alle medarbejdere skal have én primær placering.</span><span class="sxs-lookup"><span data-stu-id="67c83-366">Every employee must have one primary location.</span></span> <span data-ttu-id="67c83-367">I Dayforce bruges denne placering til at bestemme medarbejderens primære opholdssted til skattemæssige formål.</span><span class="sxs-lookup"><span data-stu-id="67c83-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="67c83-368">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-368">Primary (required)</span></span>
- <span data-ttu-id="67c83-369">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-369">Country/region (required)</span></span>
- <span data-ttu-id="67c83-370">Postnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="67c83-371">Gade (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-371">Street (required)</span></span>
- <span data-ttu-id="67c83-372">Gadenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-372">Street Number (required)</span></span>
- <span data-ttu-id="67c83-373">Bygningskomplement</span><span class="sxs-lookup"><span data-stu-id="67c83-373">Building Complement</span></span>
- <span data-ttu-id="67c83-374">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-374">City (required)</span></span>
- <span data-ttu-id="67c83-375">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-375">State (required)</span></span>
- <span data-ttu-id="67c83-376">Region (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="67c83-377">Konfigurere dataene for at generere løn i USA og Canada</span><span class="sxs-lookup"><span data-stu-id="67c83-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="67c83-378">Hvis du genererer løn for medarbejdere i USA og Canada, skal følgende elementer konfigureres:</span><span class="sxs-lookup"><span data-stu-id="67c83-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="67c83-379">Der kræves afdelinger til stillinger.</span><span class="sxs-lookup"><span data-stu-id="67c83-379">Departments are required on positions.</span></span>
- <span data-ttu-id="67c83-380">Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="67c83-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="67c83-381">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="67c83-381">Job types</span></span>

<span data-ttu-id="67c83-382">Jobtyper bruges til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="67c83-382">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="67c83-383">Jobtyper kræves for at behandle løn i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="67c83-383">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="67c83-384">Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="67c83-384">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="67c83-385">Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.</span><span class="sxs-lookup"><span data-stu-id="67c83-385">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="67c83-386">Der kræves følgende jobtyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="67c83-386">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="67c83-387">Jobtype</span><span class="sxs-lookup"><span data-stu-id="67c83-387">Job type</span></span>   | <span data-ttu-id="67c83-388">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="67c83-388">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="67c83-389">Pr. time</span><span class="sxs-lookup"><span data-stu-id="67c83-389">Hourly</span></span>     | <span data-ttu-id="67c83-390">Pr. time</span><span class="sxs-lookup"><span data-stu-id="67c83-390">Hourly</span></span>      |
| <span data-ttu-id="67c83-391">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="67c83-391">Salaried</span></span>   | <span data-ttu-id="67c83-392">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="67c83-392">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="67c83-393">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="67c83-393">Position types</span></span> 

<span data-ttu-id="67c83-394">Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet.</span><span class="sxs-lookup"><span data-stu-id="67c83-394">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="67c83-395">Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="67c83-395">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="67c83-396">Der kræves følgende stillingstyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="67c83-396">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="67c83-397">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="67c83-397">Position type</span></span>   | <span data-ttu-id="67c83-398">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="67c83-398">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="67c83-399">Fuld tid</span><span class="sxs-lookup"><span data-stu-id="67c83-399">Full-time</span></span>       | <span data-ttu-id="67c83-400">Fuldtidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="67c83-400">Full time employee</span></span> |
| <span data-ttu-id="67c83-401">Deltid</span><span class="sxs-lookup"><span data-stu-id="67c83-401">Part-time</span></span>       | <span data-ttu-id="67c83-402">Deltidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="67c83-402">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="67c83-403">Årsagskoder</span><span class="sxs-lookup"><span data-stu-id="67c83-403">Reason codes</span></span>

<span data-ttu-id="67c83-404">Årsagskoder indeholder oplysninger om status for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="67c83-404">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="67c83-405">Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.</span><span class="sxs-lookup"><span data-stu-id="67c83-405">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="67c83-406">Der kræves følgende årsagskoder og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="67c83-406">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="67c83-407">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="67c83-407">Reason code</span></span>    | <span data-ttu-id="67c83-408">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="67c83-408">Description</span></span>      | <span data-ttu-id="67c83-409">Anvendelige scenarier</span><span class="sxs-lookup"><span data-stu-id="67c83-409">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="67c83-410">OPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="67c83-410">RESIGNATION</span></span>    | <span data-ttu-id="67c83-411">Opsigelse</span><span class="sxs-lookup"><span data-stu-id="67c83-411">Resignation</span></span>      | <span data-ttu-id="67c83-412">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="67c83-412">Terminate worker</span></span>     |
| <span data-ttu-id="67c83-413">OPHØR</span><span class="sxs-lookup"><span data-stu-id="67c83-413">TERMINATION</span></span>    | <span data-ttu-id="67c83-414">Ophør</span><span class="sxs-lookup"><span data-stu-id="67c83-414">Termination</span></span>      | <span data-ttu-id="67c83-415">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="67c83-415">Terminate worker</span></span>     |
| <span data-ttu-id="67c83-416">PENSION</span><span class="sxs-lookup"><span data-stu-id="67c83-416">RETIREMENT</span></span>     | <span data-ttu-id="67c83-417">Pension</span><span class="sxs-lookup"><span data-stu-id="67c83-417">Retirement</span></span>       | <span data-ttu-id="67c83-418">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="67c83-418">Terminate worker</span></span>     |
| <span data-ttu-id="67c83-419">ANDET</span><span class="sxs-lookup"><span data-stu-id="67c83-419">OTHER</span></span>          | <span data-ttu-id="67c83-420">Andre årsager</span><span class="sxs-lookup"><span data-stu-id="67c83-420">Other Reasons</span></span>    | <span data-ttu-id="67c83-421">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="67c83-421">Terminate worker</span></span>     |
| <span data-ttu-id="67c83-422">DØDSFALD</span><span class="sxs-lookup"><span data-stu-id="67c83-422">DEATH</span></span>          | <span data-ttu-id="67c83-423">Dødsfald</span><span class="sxs-lookup"><span data-stu-id="67c83-423">Death</span></span>            | <span data-ttu-id="67c83-424">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="67c83-424">Terminate worker</span></span>     |
| <span data-ttu-id="67c83-425">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="67c83-425">LEAVEOFABSENCE</span></span> | <span data-ttu-id="67c83-426">Orlov</span><span class="sxs-lookup"><span data-stu-id="67c83-426">Leave of Absence</span></span> | <span data-ttu-id="67c83-427">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="67c83-427">Terminate worker</span></span>     |
| <span data-ttu-id="67c83-428">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="67c83-428">CONTRACTEND</span></span>    | <span data-ttu-id="67c83-429">Kontraktudløb</span><span class="sxs-lookup"><span data-stu-id="67c83-429">End of Contract</span></span>  | <span data-ttu-id="67c83-430">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="67c83-430">Terminate worker</span></span>     |
| <span data-ttu-id="67c83-431">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="67c83-431">SALARYCHANGE</span></span>   | <span data-ttu-id="67c83-432">Ændring af løn</span><span class="sxs-lookup"><span data-stu-id="67c83-432">Change of Salary</span></span> | <span data-ttu-id="67c83-433">Kompensation</span><span class="sxs-lookup"><span data-stu-id="67c83-433">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="67c83-434">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="67c83-434">Marital status</span></span>

<span data-ttu-id="67c83-435">Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="67c83-435">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="67c83-436">Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="67c83-436">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="67c83-437">Talent</span><span class="sxs-lookup"><span data-stu-id="67c83-437">Talent</span></span>                 | <span data-ttu-id="67c83-438">Dayforce</span><span class="sxs-lookup"><span data-stu-id="67c83-438">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="67c83-439">Gift</span><span class="sxs-lookup"><span data-stu-id="67c83-439">Married</span></span>                | <span data-ttu-id="67c83-440">Gift</span><span class="sxs-lookup"><span data-stu-id="67c83-440">Married</span></span>              |
| <span data-ttu-id="67c83-441">Enlig</span><span class="sxs-lookup"><span data-stu-id="67c83-441">Single</span></span>                 | <span data-ttu-id="67c83-442">Enlig</span><span class="sxs-lookup"><span data-stu-id="67c83-442">Single</span></span>               |
| <span data-ttu-id="67c83-443">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="67c83-443">Widowed</span></span>                | <span data-ttu-id="67c83-444">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="67c83-444">Widowed</span></span>              |
| <span data-ttu-id="67c83-445">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="67c83-445">Divorced</span></span>               | <span data-ttu-id="67c83-446">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="67c83-446">Divorced</span></span>             |
| <span data-ttu-id="67c83-447">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="67c83-447">Registered Partnership</span></span> | <span data-ttu-id="67c83-448">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="67c83-448">Domestic Partnership</span></span> |
| <span data-ttu-id="67c83-449">None</span><span class="sxs-lookup"><span data-stu-id="67c83-449">None</span></span>                   | <span data-ttu-id="67c83-450">None</span><span class="sxs-lookup"><span data-stu-id="67c83-450">None</span></span>                 |
| <span data-ttu-id="67c83-451">Samlever</span><span class="sxs-lookup"><span data-stu-id="67c83-451">Cohabiting</span></span>             | <span data-ttu-id="67c83-452">Samlever</span><span class="sxs-lookup"><span data-stu-id="67c83-452">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="67c83-453">Køn</span><span class="sxs-lookup"><span data-stu-id="67c83-453">Gender</span></span>

<span data-ttu-id="67c83-454">Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="67c83-454">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="67c83-455">Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="67c83-455">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="67c83-456">Talent</span><span class="sxs-lookup"><span data-stu-id="67c83-456">Talent</span></span>       | <span data-ttu-id="67c83-457">Dayforce</span><span class="sxs-lookup"><span data-stu-id="67c83-457">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="67c83-458">Mand</span><span class="sxs-lookup"><span data-stu-id="67c83-458">Male</span></span>         | <span data-ttu-id="67c83-459">Mand</span><span class="sxs-lookup"><span data-stu-id="67c83-459">Male</span></span>            |
| <span data-ttu-id="67c83-460">Kvinde</span><span class="sxs-lookup"><span data-stu-id="67c83-460">Female</span></span>       | <span data-ttu-id="67c83-461">Kvinde</span><span class="sxs-lookup"><span data-stu-id="67c83-461">Female</span></span>          |
| <span data-ttu-id="67c83-462">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="67c83-462">Non-specific</span></span> | <span data-ttu-id="67c83-463">*Understøttes ikke*</span><span class="sxs-lookup"><span data-stu-id="67c83-463">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="67c83-464">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="67c83-464">Earning codes</span></span>

<span data-ttu-id="67c83-465">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="67c83-465">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="67c83-466">Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="67c83-466">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="67c83-467">Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="67c83-467">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="67c83-468">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="67c83-468">Supported frequencies</span></span>

- <span data-ttu-id="67c83-469">Alt</span><span class="sxs-lookup"><span data-stu-id="67c83-469">All</span></span>
- <span data-ttu-id="67c83-470">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="67c83-470">EVERYPAY</span></span>
- <span data-ttu-id="67c83-471">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="67c83-471">EACHPAYPERIOD</span></span>
- <span data-ttu-id="67c83-472">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="67c83-472">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="67c83-473">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="67c83-473">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="67c83-474">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-474">1OFMTH</span></span>
- <span data-ttu-id="67c83-475">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-475">LASTOFMTH</span></span>
- <span data-ttu-id="67c83-476">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-476">2OFMTH</span></span>
- <span data-ttu-id="67c83-477">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-477">3OFMTH</span></span>
- <span data-ttu-id="67c83-478">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-478">4OFMTH</span></span>
- <span data-ttu-id="67c83-479">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-479">5OFMTH</span></span>
- <span data-ttu-id="67c83-480">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-480">1N2OFMTH</span></span>
- <span data-ttu-id="67c83-481">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-481">3N4OFMTH</span></span>
- <span data-ttu-id="67c83-482">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-482">1N3OFMTH</span></span>
- <span data-ttu-id="67c83-483">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-483">1N4OFMTH</span></span>
- <span data-ttu-id="67c83-484">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-484">2N3OFMTH</span></span>
- <span data-ttu-id="67c83-485">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-485">2N4OFMTH</span></span>
- <span data-ttu-id="67c83-486">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-486">1N2N3OFMTH</span></span>
- <span data-ttu-id="67c83-487">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-487">1N2N4OFMTH</span></span>
- <span data-ttu-id="67c83-488">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-488">1N3N4OFMTH</span></span>
- <span data-ttu-id="67c83-489">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-489">2N3N4OFMTH</span></span>
- <span data-ttu-id="67c83-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="67c83-491">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="67c83-491">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="67c83-492">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="67c83-492">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="67c83-493">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="67c83-493">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="67c83-494">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="67c83-494">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="67c83-495">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="67c83-495">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="67c83-496">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="67c83-496">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="67c83-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="67c83-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="67c83-498">Adresser</span><span class="sxs-lookup"><span data-stu-id="67c83-498">Addresses</span></span>

<span data-ttu-id="67c83-499">Identifikation af specifikke koder for land eller region, stat og område (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende.</span><span class="sxs-lookup"><span data-stu-id="67c83-499">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="67c83-500">Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.</span><span class="sxs-lookup"><span data-stu-id="67c83-500">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="67c83-501">Talent</span><span class="sxs-lookup"><span data-stu-id="67c83-501">Talent</span></span>          | <span data-ttu-id="67c83-502">Dayforce</span><span class="sxs-lookup"><span data-stu-id="67c83-502">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="67c83-503">Land/område</span><span class="sxs-lookup"><span data-stu-id="67c83-503">Country/Region</span></span>  | <span data-ttu-id="67c83-504">Landekode</span><span class="sxs-lookup"><span data-stu-id="67c83-504">Country Code</span></span>          |
| <span data-ttu-id="67c83-505">Postnummer</span><span class="sxs-lookup"><span data-stu-id="67c83-505">Zip/Postal Code</span></span> | <span data-ttu-id="67c83-506">Postnummer</span><span class="sxs-lookup"><span data-stu-id="67c83-506">Postal Code</span></span>           |
| <span data-ttu-id="67c83-507">Status</span><span class="sxs-lookup"><span data-stu-id="67c83-507">State</span></span>           | <span data-ttu-id="67c83-508">Statskode</span><span class="sxs-lookup"><span data-stu-id="67c83-508">State Code</span></span>            |
| <span data-ttu-id="67c83-509">Bynavn</span><span class="sxs-lookup"><span data-stu-id="67c83-509">City</span></span>            | <span data-ttu-id="67c83-510">Bynavn</span><span class="sxs-lookup"><span data-stu-id="67c83-510">City</span></span>                  |
| <span data-ttu-id="67c83-511">Region</span><span class="sxs-lookup"><span data-stu-id="67c83-511">County</span></span>          | <span data-ttu-id="67c83-512">Område (kommune)</span><span class="sxs-lookup"><span data-stu-id="67c83-512">County (Municipality)</span></span> |
| <span data-ttu-id="67c83-513">Gade</span><span class="sxs-lookup"><span data-stu-id="67c83-513">Street</span></span>          | <span data-ttu-id="67c83-514">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="67c83-514">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="67c83-515">Skatteområder</span><span class="sxs-lookup"><span data-stu-id="67c83-515">Tax regions</span></span>

<span data-ttu-id="67c83-516">Skatteområder bruges til at bestemme den relevante skat, der skal anvendes ved løngenerering.</span><span class="sxs-lookup"><span data-stu-id="67c83-516">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="67c83-517">Skatteområder er tilknyttet Dayforce som placeringsadresser.</span><span class="sxs-lookup"><span data-stu-id="67c83-517">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="67c83-518">Standardskatteområder skal knyttes til arbejderens aktive stilling.</span><span class="sxs-lookup"><span data-stu-id="67c83-518">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="67c83-519">Skatteområde (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-519">Tax region (required)</span></span>
- <span data-ttu-id="67c83-520">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-520">Country/Region (required)</span></span>
- <span data-ttu-id="67c83-521">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-521">State (required)</span></span>
- <span data-ttu-id="67c83-522">Region</span><span class="sxs-lookup"><span data-stu-id="67c83-522">County</span></span> 
- <span data-ttu-id="67c83-523">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="67c83-523">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="67c83-524">Konfigurere dataene for at generere løn i Mexico</span><span class="sxs-lookup"><span data-stu-id="67c83-524">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="67c83-525">Hvis du genererer løn for medarbejdere i Mexico skal følgende elementer konfigureres:</span><span class="sxs-lookup"><span data-stu-id="67c83-525">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="67c83-526">Der kræves afdelinger til stillinger.</span><span class="sxs-lookup"><span data-stu-id="67c83-526">Departments are required on positions.</span></span>
- <span data-ttu-id="67c83-527">Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="67c83-527">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="67c83-528">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="67c83-528">Job types</span></span>

<span data-ttu-id="67c83-529">Jobtyper bruges til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="67c83-529">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="67c83-530">Jobtyper kræves for at behandle løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="67c83-530">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="67c83-531">Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="67c83-531">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="67c83-532">Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.</span><span class="sxs-lookup"><span data-stu-id="67c83-532">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="67c83-533">Der kræves følgende jobtyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="67c83-533">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="67c83-534">Jobtype</span><span class="sxs-lookup"><span data-stu-id="67c83-534">Job type</span></span>   | <span data-ttu-id="67c83-535">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="67c83-535">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="67c83-536">Pr. time</span><span class="sxs-lookup"><span data-stu-id="67c83-536">Hourly</span></span>     | <span data-ttu-id="67c83-537">MX Pr. time</span><span class="sxs-lookup"><span data-stu-id="67c83-537">MX Hourly</span></span>   |
| <span data-ttu-id="67c83-538">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="67c83-538">Salaried</span></span>   | <span data-ttu-id="67c83-539">MX Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="67c83-539">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="67c83-540">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="67c83-540">Position types</span></span> 

<span data-ttu-id="67c83-541">Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet.</span><span class="sxs-lookup"><span data-stu-id="67c83-541">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="67c83-542">Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="67c83-542">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="67c83-543">Der kræves følgende stillingstyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="67c83-543">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="67c83-544">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="67c83-544">Position type</span></span>   | <span data-ttu-id="67c83-545">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="67c83-545">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="67c83-546">Fuld tid</span><span class="sxs-lookup"><span data-stu-id="67c83-546">Full-time</span></span>       | <span data-ttu-id="67c83-547">Fuldtidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="67c83-547">Full time employee</span></span> |
| <span data-ttu-id="67c83-548">Deltid</span><span class="sxs-lookup"><span data-stu-id="67c83-548">Part-time</span></span>       | <span data-ttu-id="67c83-549">Deltidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="67c83-549">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="67c83-550">Årsagskoder</span><span class="sxs-lookup"><span data-stu-id="67c83-550">Reason codes</span></span>

<span data-ttu-id="67c83-551">Årsagskoder indeholder oplysninger om status for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="67c83-551">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="67c83-552">Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.</span><span class="sxs-lookup"><span data-stu-id="67c83-552">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="67c83-553">Der kræves følgende årsagskoder og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="67c83-553">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="67c83-554">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="67c83-554">Reason code</span></span>            | <span data-ttu-id="67c83-555">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="67c83-555">Description</span></span>                    | <span data-ttu-id="67c83-556">Anvendelige scenarier</span><span class="sxs-lookup"><span data-stu-id="67c83-556">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="67c83-557">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="67c83-557">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="67c83-558">Afgang før første løn</span><span class="sxs-lookup"><span data-stu-id="67c83-558">Departure before first payroll</span></span> | <span data-ttu-id="67c83-559">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="67c83-559">Terminate worker</span></span>     |
| <span data-ttu-id="67c83-560">OPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="67c83-560">RESIGNATION</span></span>            | <span data-ttu-id="67c83-561">Opsigelse</span><span class="sxs-lookup"><span data-stu-id="67c83-561">Resignation</span></span>                    | <span data-ttu-id="67c83-562">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="67c83-562">Terminate worker</span></span>     |
| <span data-ttu-id="67c83-563">PENSION</span><span class="sxs-lookup"><span data-stu-id="67c83-563">PENSION</span></span>                | <span data-ttu-id="67c83-564">Pension</span><span class="sxs-lookup"><span data-stu-id="67c83-564">Pension</span></span>                        | <span data-ttu-id="67c83-565">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="67c83-565">Terminate worker</span></span>     |
| <span data-ttu-id="67c83-566">OPHØR</span><span class="sxs-lookup"><span data-stu-id="67c83-566">TERMINATION</span></span>            | <span data-ttu-id="67c83-567">Ophør</span><span class="sxs-lookup"><span data-stu-id="67c83-567">Termination</span></span>                    | <span data-ttu-id="67c83-568">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="67c83-568">Terminate worker</span></span>     |
| <span data-ttu-id="67c83-569">PENSION</span><span class="sxs-lookup"><span data-stu-id="67c83-569">RETIREMENT</span></span>             | <span data-ttu-id="67c83-570">Pension</span><span class="sxs-lookup"><span data-stu-id="67c83-570">Retirement</span></span>                     | <span data-ttu-id="67c83-571">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="67c83-571">Terminate worker</span></span>     |
| <span data-ttu-id="67c83-572">FRAVÆRENDE</span><span class="sxs-lookup"><span data-stu-id="67c83-572">ABSENTEE</span></span>               | <span data-ttu-id="67c83-573">Fraværende</span><span class="sxs-lookup"><span data-stu-id="67c83-573">Absentee</span></span>                       | <span data-ttu-id="67c83-574">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="67c83-574">Terminate worker</span></span>     |
| <span data-ttu-id="67c83-575">ANDET</span><span class="sxs-lookup"><span data-stu-id="67c83-575">OTHER</span></span>                  | <span data-ttu-id="67c83-576">Andre årsager</span><span class="sxs-lookup"><span data-stu-id="67c83-576">Other Reasons</span></span>                  | <span data-ttu-id="67c83-577">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="67c83-577">Terminate worker</span></span>     |
| <span data-ttu-id="67c83-578">LUKNING</span><span class="sxs-lookup"><span data-stu-id="67c83-578">CLOSURE</span></span>                | <span data-ttu-id="67c83-579">Virksomhedslukning</span><span class="sxs-lookup"><span data-stu-id="67c83-579">Business Closure</span></span>               | <span data-ttu-id="67c83-580">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="67c83-580">Terminate worker</span></span>     |
| <span data-ttu-id="67c83-581">DØDSFALD</span><span class="sxs-lookup"><span data-stu-id="67c83-581">DEATH</span></span>                  | <span data-ttu-id="67c83-582">Dødsfald</span><span class="sxs-lookup"><span data-stu-id="67c83-582">Death</span></span>                          | <span data-ttu-id="67c83-583">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="67c83-583">Terminate worker</span></span>     |
| <span data-ttu-id="67c83-584">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="67c83-584">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="67c83-585">Orlov</span><span class="sxs-lookup"><span data-stu-id="67c83-585">Leave of Absence</span></span>               | <span data-ttu-id="67c83-586">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="67c83-586">Terminate worker</span></span>     |
| <span data-ttu-id="67c83-587">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="67c83-587">CONTRACTEND</span></span>            | <span data-ttu-id="67c83-588">Kontraktudløb</span><span class="sxs-lookup"><span data-stu-id="67c83-588">End of Contract</span></span>                | <span data-ttu-id="67c83-589">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="67c83-589">Terminate worker</span></span>     |
| <span data-ttu-id="67c83-590">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="67c83-590">SALARYCHANGE</span></span>           | <span data-ttu-id="67c83-591">Ændring af løn</span><span class="sxs-lookup"><span data-stu-id="67c83-591">Change of Salary</span></span>               | <span data-ttu-id="67c83-592">Kompensation</span><span class="sxs-lookup"><span data-stu-id="67c83-592">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="67c83-593">Ansættelsesvilkår</span><span class="sxs-lookup"><span data-stu-id="67c83-593">Terms of employment</span></span>

<span data-ttu-id="67c83-594">Ansættelsesvilkår bruges til at oprette kategorier for ansættelsesvilkår.</span><span class="sxs-lookup"><span data-stu-id="67c83-594">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="67c83-595">Vilkårene knyttes til Dayforce som beskæftigelsesindikatorværdier.</span><span class="sxs-lookup"><span data-stu-id="67c83-595">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="67c83-596">Følgende begreber for beskæftigelse og beskrivelser er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="67c83-596">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="67c83-597">Ansættelsesvilkår</span><span class="sxs-lookup"><span data-stu-id="67c83-597">Terms of employment</span></span>   | <span data-ttu-id="67c83-598">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="67c83-598">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="67c83-599">Regulær</span><span class="sxs-lookup"><span data-stu-id="67c83-599">Regular</span></span>               | <span data-ttu-id="67c83-600">Regulær</span><span class="sxs-lookup"><span data-stu-id="67c83-600">Regular</span></span>     |
| <span data-ttu-id="67c83-601">Direkte</span><span class="sxs-lookup"><span data-stu-id="67c83-601">Direct</span></span>                | <span data-ttu-id="67c83-602">Direkte</span><span class="sxs-lookup"><span data-stu-id="67c83-602">Direct</span></span>      |
| <span data-ttu-id="67c83-603">Turnustjeneste</span><span class="sxs-lookup"><span data-stu-id="67c83-603">Internship</span></span>            | <span data-ttu-id="67c83-604">Turnustjeneste</span><span class="sxs-lookup"><span data-stu-id="67c83-604">Internship</span></span>  |
| <span data-ttu-id="67c83-605">Permanent</span><span class="sxs-lookup"><span data-stu-id="67c83-605">Permanent</span></span>             | <span data-ttu-id="67c83-606">Permanent</span><span class="sxs-lookup"><span data-stu-id="67c83-606">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="67c83-607">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="67c83-607">Marital status</span></span>

<span data-ttu-id="67c83-608">Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="67c83-608">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="67c83-609">Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="67c83-609">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="67c83-610">Talent</span><span class="sxs-lookup"><span data-stu-id="67c83-610">Talent</span></span>                 | <span data-ttu-id="67c83-611">Dayforce</span><span class="sxs-lookup"><span data-stu-id="67c83-611">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="67c83-612">Gift</span><span class="sxs-lookup"><span data-stu-id="67c83-612">Married</span></span>                | <span data-ttu-id="67c83-613">Gift</span><span class="sxs-lookup"><span data-stu-id="67c83-613">Married</span></span>                   |
| <span data-ttu-id="67c83-614">Enlig</span><span class="sxs-lookup"><span data-stu-id="67c83-614">Single</span></span>                 | <span data-ttu-id="67c83-615">Enlig</span><span class="sxs-lookup"><span data-stu-id="67c83-615">Single</span></span>                    |
| <span data-ttu-id="67c83-616">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="67c83-616">Widowed</span></span>                | <span data-ttu-id="67c83-617">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="67c83-617">Widowed</span></span>                   |
| <span data-ttu-id="67c83-618">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="67c83-618">Divorced</span></span>               | <span data-ttu-id="67c83-619">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="67c83-619">Divorced</span></span>                  |
| <span data-ttu-id="67c83-620">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="67c83-620">Registered Partnership</span></span> | <span data-ttu-id="67c83-621">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="67c83-621">Domestic Partnership</span></span>      |
| <span data-ttu-id="67c83-622">None</span><span class="sxs-lookup"><span data-stu-id="67c83-622">None</span></span>                   | <span data-ttu-id="67c83-623">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="67c83-623">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="67c83-624">Samlever</span><span class="sxs-lookup"><span data-stu-id="67c83-624">Cohabiting</span></span>             | <span data-ttu-id="67c83-625">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="67c83-625">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="67c83-626">Køn</span><span class="sxs-lookup"><span data-stu-id="67c83-626">Gender</span></span>

<span data-ttu-id="67c83-627">Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="67c83-627">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="67c83-628">Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="67c83-628">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="67c83-629">Talent</span><span class="sxs-lookup"><span data-stu-id="67c83-629">Talent</span></span>       | <span data-ttu-id="67c83-630">Dayforce</span><span class="sxs-lookup"><span data-stu-id="67c83-630">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="67c83-631">Mand</span><span class="sxs-lookup"><span data-stu-id="67c83-631">Male</span></span>         | <span data-ttu-id="67c83-632">Mand</span><span class="sxs-lookup"><span data-stu-id="67c83-632">Male</span></span>                      |
| <span data-ttu-id="67c83-633">Kvinde</span><span class="sxs-lookup"><span data-stu-id="67c83-633">Female</span></span>       | <span data-ttu-id="67c83-634">Kvinde</span><span class="sxs-lookup"><span data-stu-id="67c83-634">Female</span></span>                    |
| <span data-ttu-id="67c83-635">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="67c83-635">Non-specific</span></span> | <span data-ttu-id="67c83-636">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="67c83-636">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="67c83-637">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="67c83-637">Payment method</span></span>

<span data-ttu-id="67c83-638">Betalingsmetoder giver medarbejderen og virksomheden en måde til at beskrive, hvordan medarbejdere skal betales.</span><span class="sxs-lookup"><span data-stu-id="67c83-638">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="67c83-639">Betalingsmåder knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="67c83-639">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="67c83-640">Følgende tabel viser, hvordan betalingsmetoder knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="67c83-640">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="67c83-641">Talent</span><span class="sxs-lookup"><span data-stu-id="67c83-641">Talent</span></span>             | <span data-ttu-id="67c83-642">Dayforce</span><span class="sxs-lookup"><span data-stu-id="67c83-642">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="67c83-643">Indløsning</span><span class="sxs-lookup"><span data-stu-id="67c83-643">Cash</span></span>               | <span data-ttu-id="67c83-644">Indløsning</span><span class="sxs-lookup"><span data-stu-id="67c83-644">Cash</span></span>                      |
| <span data-ttu-id="67c83-645">Elektronisk betaling</span><span class="sxs-lookup"><span data-stu-id="67c83-645">Electronic Payment</span></span> | <span data-ttu-id="67c83-646">Ompostering</span><span class="sxs-lookup"><span data-stu-id="67c83-646">Transfer</span></span>                  |
| <span data-ttu-id="67c83-647">Check</span><span class="sxs-lookup"><span data-stu-id="67c83-647">Check</span></span>              | <span data-ttu-id="67c83-648">Check</span><span class="sxs-lookup"><span data-stu-id="67c83-648">Cheque</span></span>                    |
| <span data-ttu-id="67c83-649">Bankanvisning</span><span class="sxs-lookup"><span data-stu-id="67c83-649">Bank Draft</span></span>         | <span data-ttu-id="67c83-650">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="67c83-650">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="67c83-651">Andre</span><span class="sxs-lookup"><span data-stu-id="67c83-651">Other</span></span>              | <span data-ttu-id="67c83-652">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="67c83-652">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="67c83-653">Bankkontotype</span><span class="sxs-lookup"><span data-stu-id="67c83-653">Bank account type</span></span>

<span data-ttu-id="67c83-654">Bankkontotyper bruges til elektroniske betalinger til medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="67c83-654">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="67c83-655">Bankkontotyper knyttes til Dayforce som overførselskontooplysninger.</span><span class="sxs-lookup"><span data-stu-id="67c83-655">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="67c83-656">Bankkontotyperne oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="67c83-656">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="67c83-657">Talent</span><span class="sxs-lookup"><span data-stu-id="67c83-657">Talent</span></span>            | <span data-ttu-id="67c83-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="67c83-658">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="67c83-659">Checkkonto</span><span class="sxs-lookup"><span data-stu-id="67c83-659">Checking Account</span></span>  | <span data-ttu-id="67c83-660">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="67c83-660">CheckingAccount</span></span>           |
| <span data-ttu-id="67c83-661">Lønkonto</span><span class="sxs-lookup"><span data-stu-id="67c83-661">Payroll Account</span></span>   | <span data-ttu-id="67c83-662">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="67c83-662">PayrollAccount</span></span>            |
| <span data-ttu-id="67c83-663">Opsparingskonto</span><span class="sxs-lookup"><span data-stu-id="67c83-663">Savings Account</span></span>   | <span data-ttu-id="67c83-664">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="67c83-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="67c83-665">BankGirot-konto</span><span class="sxs-lookup"><span data-stu-id="67c83-665">BankGirot account</span></span> | <span data-ttu-id="67c83-666">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="67c83-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="67c83-667">PlusGirot-konto</span><span class="sxs-lookup"><span data-stu-id="67c83-667">PlusGirot account</span></span> | <span data-ttu-id="67c83-668">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="67c83-668">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="67c83-669">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="67c83-669">Earning codes</span></span>

<span data-ttu-id="67c83-670">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="67c83-670">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="67c83-671">Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="67c83-671">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="67c83-672">Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="67c83-672">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="67c83-673">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="67c83-673">Supported frequencies</span></span>

- <span data-ttu-id="67c83-674">Alt</span><span class="sxs-lookup"><span data-stu-id="67c83-674">All</span></span>
- <span data-ttu-id="67c83-675">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="67c83-675">EVERYPAY</span></span>
- <span data-ttu-id="67c83-676">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="67c83-676">EACHPAYPERIOD</span></span>
- <span data-ttu-id="67c83-677">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="67c83-677">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="67c83-678">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="67c83-678">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="67c83-679">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-679">1OFMTH</span></span>
- <span data-ttu-id="67c83-680">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-680">LASTOFMTH</span></span>
- <span data-ttu-id="67c83-681">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-681">2OFMTH</span></span>
- <span data-ttu-id="67c83-682">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-682">3OFMTH</span></span>
- <span data-ttu-id="67c83-683">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-683">4OFMTH</span></span>
- <span data-ttu-id="67c83-684">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-684">5OFMTH</span></span>
- <span data-ttu-id="67c83-685">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-685">1N2OFMTH</span></span>
- <span data-ttu-id="67c83-686">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-686">3N4OFMTH</span></span>
- <span data-ttu-id="67c83-687">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-687">1N3OFMTH</span></span>
- <span data-ttu-id="67c83-688">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-688">1N4OFMTH</span></span>
- <span data-ttu-id="67c83-689">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-689">2N3OFMTH</span></span>
- <span data-ttu-id="67c83-690">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-690">2N4OFMTH</span></span>
- <span data-ttu-id="67c83-691">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-691">1N2N3OFMTH</span></span>
- <span data-ttu-id="67c83-692">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-692">1N2N4OFMTH</span></span>
- <span data-ttu-id="67c83-693">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-693">1N3N4OFMTH</span></span>
- <span data-ttu-id="67c83-694">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-694">2N3N4OFMTH</span></span>
- <span data-ttu-id="67c83-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="67c83-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="67c83-696">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="67c83-696">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="67c83-697">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="67c83-697">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="67c83-698">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="67c83-698">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="67c83-699">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="67c83-699">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="67c83-700">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="67c83-700">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="67c83-701">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="67c83-701">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="67c83-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="67c83-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="67c83-703">Adresser</span><span class="sxs-lookup"><span data-stu-id="67c83-703">Addresses</span></span>

<span data-ttu-id="67c83-704">Identifikation af specifikke koder for land eller region, stat og område (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende.</span><span class="sxs-lookup"><span data-stu-id="67c83-704">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="67c83-705">Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.</span><span class="sxs-lookup"><span data-stu-id="67c83-705">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="67c83-706">Talent</span><span class="sxs-lookup"><span data-stu-id="67c83-706">Talent</span></span>              | <span data-ttu-id="67c83-707">Dayforce</span><span class="sxs-lookup"><span data-stu-id="67c83-707">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="67c83-708">Land/område</span><span class="sxs-lookup"><span data-stu-id="67c83-708">Country/Region</span></span>      | <span data-ttu-id="67c83-709">Landekode</span><span class="sxs-lookup"><span data-stu-id="67c83-709">Country Code</span></span>          |
| <span data-ttu-id="67c83-710">Postnummer</span><span class="sxs-lookup"><span data-stu-id="67c83-710">Zip/Postal Code</span></span>     | <span data-ttu-id="67c83-711">Postnummer</span><span class="sxs-lookup"><span data-stu-id="67c83-711">Postal Code</span></span>           |
| <span data-ttu-id="67c83-712">Status</span><span class="sxs-lookup"><span data-stu-id="67c83-712">State</span></span>               | <span data-ttu-id="67c83-713">Statskode</span><span class="sxs-lookup"><span data-stu-id="67c83-713">State Code</span></span>            |
| <span data-ttu-id="67c83-714">Bynavn</span><span class="sxs-lookup"><span data-stu-id="67c83-714">City</span></span>                | <span data-ttu-id="67c83-715">Bynavn</span><span class="sxs-lookup"><span data-stu-id="67c83-715">City</span></span>                  |
| <span data-ttu-id="67c83-716">Region</span><span class="sxs-lookup"><span data-stu-id="67c83-716">County</span></span>              | <span data-ttu-id="67c83-717">Område (kommune)</span><span class="sxs-lookup"><span data-stu-id="67c83-717">County (Municipality)</span></span> |
| <span data-ttu-id="67c83-718">Gade</span><span class="sxs-lookup"><span data-stu-id="67c83-718">Street</span></span>              | <span data-ttu-id="67c83-719">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="67c83-719">Address Line 1</span></span>        |
| <span data-ttu-id="67c83-720">Gadenummer</span><span class="sxs-lookup"><span data-stu-id="67c83-720">Street Number</span></span>       | <span data-ttu-id="67c83-721">Adresselinje 2</span><span class="sxs-lookup"><span data-stu-id="67c83-721">Address Line 2</span></span>        |
| <span data-ttu-id="67c83-722">Bygningskomplement</span><span class="sxs-lookup"><span data-stu-id="67c83-722">Building Complement</span></span> | <span data-ttu-id="67c83-723">Adresselinje 5</span><span class="sxs-lookup"><span data-stu-id="67c83-723">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="67c83-724">Pasnummer</span><span class="sxs-lookup"><span data-stu-id="67c83-724">Passport number</span></span>

<span data-ttu-id="67c83-725">Medarbejdere kan erklære pasoplysninger.</span><span class="sxs-lookup"><span data-stu-id="67c83-725">Employees can declare passport information.</span></span> <span data-ttu-id="67c83-726">Disse oplysninger er af identifikationstypen **Pas** og er integreret i Dayforce som en del af en medarbejders Mexico-specifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="67c83-726">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="67c83-727">Identifikationstype = "Pas"</span><span class="sxs-lookup"><span data-stu-id="67c83-727">Identification Type = "Passport"</span></span>
- <span data-ttu-id="67c83-728">Udstedt den</span><span class="sxs-lookup"><span data-stu-id="67c83-728">Issued Date</span></span>
- <span data-ttu-id="67c83-729">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="67c83-729">Expiration Date</span></span>

<span data-ttu-id="67c83-730">Medarbejdere kan angive flere identifikationsnumre af **Pas**-identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="67c83-730">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="67c83-731">Men det er kun den aktuelle aktive paspost, der integreres i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="67c83-731">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="67c83-732">Hvis alle pasposter er udløbet, integreres det pas, der senest blev udstedt, i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="67c83-732">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

