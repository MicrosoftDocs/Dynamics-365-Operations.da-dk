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
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517574"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="2fabb-103">Konfigurere lønintegrationen mellem Talent og Dayforce</span><span class="sxs-lookup"><span data-stu-id="2fabb-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2fabb-104">Integration mellem Microsoft Dynamics 365 for Talent og Ceridian Dayforce er baseret på flere konfigurationstrin, der er beskrevet i dette emne.</span><span class="sxs-lookup"><span data-stu-id="2fabb-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="2fabb-105">Du skal konfigurere integrationen i både Talent og Dayforce, før du kan behandle en lønkørsel.</span><span class="sxs-lookup"><span data-stu-id="2fabb-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="2fabb-106">Når du bruger en tjeneste, f.eks. Dayforce, til at fuldføre lønkørsler, skal du aktivere integrationen i Talent.</span><span class="sxs-lookup"><span data-stu-id="2fabb-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="2fabb-107">Integrationen kræver bestemte data fra Talent.</span><span class="sxs-lookup"><span data-stu-id="2fabb-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="2fabb-108">Du skal derfor kontrollere, at data, der er knyttet til Dayforce, er konfigureret i Talent på en måde, der understøtter integrationen.</span><span class="sxs-lookup"><span data-stu-id="2fabb-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="2fabb-109">Integrationen bruger følgende brede kategorier af data.</span><span class="sxs-lookup"><span data-stu-id="2fabb-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="2fabb-110">Personaledata</span><span class="sxs-lookup"><span data-stu-id="2fabb-110">Human resources data</span></span>
- <span data-ttu-id="2fabb-111">Kompensationsdata</span><span class="sxs-lookup"><span data-stu-id="2fabb-111">Compensation data</span></span>
- <span data-ttu-id="2fabb-112">Lønoplysninger, f.eks. løncyklusser, betalingsperioder og lønkoder</span><span class="sxs-lookup"><span data-stu-id="2fabb-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="2fabb-113">Arbejderdata</span><span class="sxs-lookup"><span data-stu-id="2fabb-113">Worker data</span></span>

<span data-ttu-id="2fabb-114">Dette emne beskrives de trin, du skal udføre for at aktivere integrationen.</span><span class="sxs-lookup"><span data-stu-id="2fabb-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="2fabb-115">Det forklarer også typerne af data og oplysninger om konfigurationen, der kræves til integrationen.</span><span class="sxs-lookup"><span data-stu-id="2fabb-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="2fabb-116">Aktivere integrationen.</span><span class="sxs-lookup"><span data-stu-id="2fabb-116">Enable the integration</span></span>

<span data-ttu-id="2fabb-117">I Talent skal du aktivere integrationen og angive konfigurationsoplysningerne for at oprette forbindelse til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2fabb-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="2fabb-118">Hvis den finanspostering, der er produceret, skal importeres til Microsoft Dynamics 365 for Finance and Operations, skal du også konfigurere en Microsoft Azure-lagerkonto og angive Azure-lagerets forbindelsesstreng i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2fabb-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="2fabb-119">Følg disse trin for at aktivere integrationen i Talent.</span><span class="sxs-lookup"><span data-stu-id="2fabb-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="2fabb-120">På siden **Systemadministration** skal du vælge **Integrationskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="2fabb-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="2fabb-121">Angiv det sikre FTP-slutpunkt og den sikre FTP-mappesti.</span><span class="sxs-lookup"><span data-stu-id="2fabb-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="2fabb-122">Angiv brugernavnet og adgangskoden for den bruger, der skal have adgang til det sikre FTP-slutpunkt og den sikre mappesti.</span><span class="sxs-lookup"><span data-stu-id="2fabb-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="2fabb-123">Test forbindelsen, som krævet, og angiv indstillingen **Aktivér lønintegration** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2fabb-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="2fabb-124">Når integrationen er aktiveret, oprettes dataeksportpakken og -filerne, og hyppigheden angives.</span><span class="sxs-lookup"><span data-stu-id="2fabb-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="2fabb-125">Du kan ændre denne frekvens efter behov.</span><span class="sxs-lookup"><span data-stu-id="2fabb-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="2fabb-126">Yderligere oplysninger om Azure-lagerkonti og Azure-lagerforbindelsesstrenge finder du i følgende Azure-emner:</span><span class="sxs-lookup"><span data-stu-id="2fabb-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="2fabb-127">Om Azure-lagerkonti</span><span class="sxs-lookup"><span data-stu-id="2fabb-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="2fabb-128">Konfigurere forbindelsesstrenge for Azure-datalager</span><span class="sxs-lookup"><span data-stu-id="2fabb-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="2fabb-129">Konfigurere dine data</span><span class="sxs-lookup"><span data-stu-id="2fabb-129">Configure your data</span></span> 

<span data-ttu-id="2fabb-130">Hvis du vil behandle løn, skal du konfigurere personaledata i Talent.</span><span class="sxs-lookup"><span data-stu-id="2fabb-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="2fabb-131">Du skal angive virksomhedens data, f.eks. job og stillinger, sammen med frynsegoder og kompensationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="2fabb-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="2fabb-132">Disse oplysninger indeholder oplysningerne om ansættelse, løn og fradrag, der kræves for at generere løn for medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="2fabb-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="2fabb-133">Personaledata</span><span class="sxs-lookup"><span data-stu-id="2fabb-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="2fabb-134">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="2fabb-134">Benefits</span></span> 

<span data-ttu-id="2fabb-135">Personale indeholder en række værktøjer til konfiguration og vedligeholdelse af frynsegoder, fradrag og arbejderkompensationsplaner, som en organisation tilbyder eller behandler for sine ansatte.</span><span class="sxs-lookup"><span data-stu-id="2fabb-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="2fabb-136">Når du opretter frynsegoder, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2fabb-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="2fabb-137">Frynsegodeplaner</span><span class="sxs-lookup"><span data-stu-id="2fabb-137">Benefit plans</span></span>

- <span data-ttu-id="2fabb-138">Plan (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-138">Plan (required)</span></span>
- <span data-ttu-id="2fabb-139">Type (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-139">Type (required)</span></span>
- <span data-ttu-id="2fabb-140">Løneffekt (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-140">Payroll impact (required)</span></span>
- <span data-ttu-id="2fabb-141">Opkræv restancer</span><span class="sxs-lookup"><span data-stu-id="2fabb-141">Recover arrears</span></span>
- <span data-ttu-id="2fabb-142">Fradragsmetode</span><span class="sxs-lookup"><span data-stu-id="2fabb-142">Deduction method</span></span>
- <span data-ttu-id="2fabb-143">Prioriteret fradrag</span><span class="sxs-lookup"><span data-stu-id="2fabb-143">Deduction priority</span></span>
- <span data-ttu-id="2fabb-144">Grænseperiode</span><span class="sxs-lookup"><span data-stu-id="2fabb-144">Limit period</span></span>
- <span data-ttu-id="2fabb-145">Beløb for grænse</span><span class="sxs-lookup"><span data-stu-id="2fabb-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="2fabb-146">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="2fabb-146">Benefits</span></span>

- <span data-ttu-id="2fabb-147">Plan (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-147">Plan (required)</span></span>
- <span data-ttu-id="2fabb-148">Type (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-148">Type (required)</span></span>
- <span data-ttu-id="2fabb-149">Mulighed (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-149">Option (required)</span></span>
- <span data-ttu-id="2fabb-150">Frynsegode-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-150">Benefit ID (required)</span></span>
- <span data-ttu-id="2fabb-151">Frekvens</span><span class="sxs-lookup"><span data-stu-id="2fabb-151">Frequency</span></span>
- <span data-ttu-id="2fabb-152">Basis</span><span class="sxs-lookup"><span data-stu-id="2fabb-152">Basis</span></span>
- <span data-ttu-id="2fabb-153">Beløb eller sats</span><span class="sxs-lookup"><span data-stu-id="2fabb-153">Amount or rate</span></span>
- <span data-ttu-id="2fabb-154">Lønkode</span><span class="sxs-lookup"><span data-stu-id="2fabb-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="2fabb-155">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="2fabb-155">Supported frequencies</span></span> 

- <span data-ttu-id="2fabb-156">Ugentlig</span><span class="sxs-lookup"><span data-stu-id="2fabb-156">Weekly</span></span>
- <span data-ttu-id="2fabb-157">Pr. 14 dage</span><span class="sxs-lookup"><span data-stu-id="2fabb-157">Bi-weekly</span></span>
- <span data-ttu-id="2fabb-158">To gange om måneden</span><span class="sxs-lookup"><span data-stu-id="2fabb-158">Semi-monthly</span></span>
- <span data-ttu-id="2fabb-159">Månedlig</span><span class="sxs-lookup"><span data-stu-id="2fabb-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="2fabb-160">Understøttede grundlag</span><span class="sxs-lookup"><span data-stu-id="2fabb-160">Supported bases</span></span> 

- <span data-ttu-id="2fabb-161">Fast beløb</span><span class="sxs-lookup"><span data-stu-id="2fabb-161">Fixed amount</span></span>
- <span data-ttu-id="2fabb-162">Procentdel af løn</span><span class="sxs-lookup"><span data-stu-id="2fabb-162">Percent of earnings</span></span>
- <span data-ttu-id="2fabb-163">Produktive timer</span><span class="sxs-lookup"><span data-stu-id="2fabb-163">Productive hours</span></span>

<span data-ttu-id="2fabb-164">Dayforce opretter følgende fradrag, der er baseret på den løneffekt, der er defineret på frynsegodeplanen.</span><span class="sxs-lookup"><span data-stu-id="2fabb-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="2fabb-165">Valg i Talent</span><span class="sxs-lookup"><span data-stu-id="2fabb-165">Selection in Talent</span></span>        | <span data-ttu-id="2fabb-166">Resultat i Dayforce</span><span class="sxs-lookup"><span data-stu-id="2fabb-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="2fabb-167">None</span><span class="sxs-lookup"><span data-stu-id="2fabb-167">None</span></span>                       | <span data-ttu-id="2fabb-168">Der oprettes ikke noget fradrag.</span><span class="sxs-lookup"><span data-stu-id="2fabb-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="2fabb-169">Kun fradrag</span><span class="sxs-lookup"><span data-stu-id="2fabb-169">Deduction only</span></span>             | <span data-ttu-id="2fabb-170">Der oprettes et medarbejderfradrag.</span><span class="sxs-lookup"><span data-stu-id="2fabb-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="2fabb-171">Kun bidrag</span><span class="sxs-lookup"><span data-stu-id="2fabb-171">Contribution only</span></span>          | <span data-ttu-id="2fabb-172">Der oprettes et arbejdsgiverfradrag.</span><span class="sxs-lookup"><span data-stu-id="2fabb-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="2fabb-173">Fradrag og bidrag</span><span class="sxs-lookup"><span data-stu-id="2fabb-173">Deduction and contribution</span></span> | <span data-ttu-id="2fabb-174">Der oprettes medarbejder- og arbejdsgiverfradrag.</span><span class="sxs-lookup"><span data-stu-id="2fabb-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="2fabb-175">Du kan finde flere oplysninger om, hvordan du definerer og administrerer et frynsegodeprogram under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="2fabb-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="2fabb-176">Levere et frynsegodeprogram for medarbejdere</span><span class="sxs-lookup"><span data-stu-id="2fabb-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="2fabb-177">Oprette et nyt frynsegode</span><span class="sxs-lookup"><span data-stu-id="2fabb-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="2fabb-178">Definere regler og politikker for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="2fabb-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="2fabb-179">Tilmelde og fjerne frynsegoder fra arbejdere</span><span class="sxs-lookup"><span data-stu-id="2fabb-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="2fabb-180">Kompensation</span><span class="sxs-lookup"><span data-stu-id="2fabb-180">Compensation</span></span> 

<span data-ttu-id="2fabb-181">Kompensationsstyring bruges til at styre fordelingen af grundløn og bonusser.</span><span class="sxs-lookup"><span data-stu-id="2fabb-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="2fabb-182">En medarbejders faste grundløn og kvalifikationstillæg styres gennem faste lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="2fabb-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="2fabb-183">Betalingen af incitamentsløn som f.eks. bonusudbetalinger, præstationsbonusser, aktieoptioner og tildelte aktier samt engangsbonusser styres ved hjælp af variable lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="2fabb-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="2fabb-184">Dayforce anvendes kompensationsoplysninger til at beregne en medarbejders timesats eller årlige sats.</span><span class="sxs-lookup"><span data-stu-id="2fabb-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="2fabb-185">Konverteringer af planer for fast løn og lønsats er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="2fabb-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="2fabb-186">Medarbejderne skal være knyttet til en plan for fast løn.</span><span class="sxs-lookup"><span data-stu-id="2fabb-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="2fabb-187">Du kan finde flere oplysninger om kompensationsplaner under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="2fabb-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="2fabb-188">Oprette faste kompensationsordninger</span><span class="sxs-lookup"><span data-stu-id="2fabb-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="2fabb-189">Oprette planer for variabel kompensation</span><span class="sxs-lookup"><span data-stu-id="2fabb-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="2fabb-190">Udarbejde løn-/kompensationsstruktur og -planer</span><span class="sxs-lookup"><span data-stu-id="2fabb-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="2fabb-191">Proceskompensation</span><span class="sxs-lookup"><span data-stu-id="2fabb-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="2fabb-192">Definere kompensationsproces og beregne resultater</span><span class="sxs-lookup"><span data-stu-id="2fabb-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="2fabb-193">Melde en medarbejder til en fast lønplan</span><span class="sxs-lookup"><span data-stu-id="2fabb-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="2fabb-194">Melde en medarbejder til en variabel lønplan</span><span class="sxs-lookup"><span data-stu-id="2fabb-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="2fabb-195">Job</span><span class="sxs-lookup"><span data-stu-id="2fabb-195">Jobs</span></span> 

<span data-ttu-id="2fabb-196">Et job er en samling af de opgaver og ansvarsområder, der kræves af en person, der udfører et job.</span><span class="sxs-lookup"><span data-stu-id="2fabb-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="2fabb-197">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="2fabb-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="2fabb-198">Konfiguration af komponenter i et job</span><span class="sxs-lookup"><span data-stu-id="2fabb-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="2fabb-199">Definere nye job</span><span class="sxs-lookup"><span data-stu-id="2fabb-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="2fabb-200">Stillinger</span><span class="sxs-lookup"><span data-stu-id="2fabb-200">Positions</span></span>

<span data-ttu-id="2fabb-201">En stilling er en individuel forekomst af et job.</span><span class="sxs-lookup"><span data-stu-id="2fabb-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="2fabb-202">For eksempel er stillingen "Salgschef (øst)" én af de stillinger, der er tilknyttet jobbet "Salgschef".</span><span class="sxs-lookup"><span data-stu-id="2fabb-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="2fabb-203">En stilling findes i en afdeling.</span><span class="sxs-lookup"><span data-stu-id="2fabb-203">A position exists in a department.</span></span> <span data-ttu-id="2fabb-204">Der kan kun knyttes én arbejder til hver stilling.</span><span class="sxs-lookup"><span data-stu-id="2fabb-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="2fabb-205">Hav følgende data og konfiguration i tankerne, når du konfigurerer stillinger:</span><span class="sxs-lookup"><span data-stu-id="2fabb-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="2fabb-206">Stilling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-206">Position (required)</span></span>
- <span data-ttu-id="2fabb-207">Beskrivelse (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-207">Description (required)</span></span>
- <span data-ttu-id="2fabb-208">Job (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-208">Job (required)</span></span>
- <span data-ttu-id="2fabb-209">Afdeling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-209">Department (required)</span></span>
- <span data-ttu-id="2fabb-210">Stillingstype (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-210">Position type (required)</span></span>
- <span data-ttu-id="2fabb-211">Fuldtidsækvivalent</span><span class="sxs-lookup"><span data-stu-id="2fabb-211">Full-time equivalent</span></span>
- <span data-ttu-id="2fabb-212">Normaltimer på årsbasis (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="2fabb-213">Betalt af juridiske enhed (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="2fabb-214">Betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-214">Pay cycle (required)</span></span>
- <span data-ttu-id="2fabb-215">Økonomisk standarddimension – bærer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="2fabb-216">Arbejdertildeling – arbejder, tildelingsstart, tildelingsslut, årsagskode</span><span class="sxs-lookup"><span data-stu-id="2fabb-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="2fabb-217">Hvis flere stillinger i den samme afdeling er knyttet til samme job, konsolideres de til en enkelt stilling i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2fabb-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="2fabb-218">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="2fabb-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="2fabb-219">Organisere dine medarbejdere ved hjælp af afdelinger, jobs og stillinger</span><span class="sxs-lookup"><span data-stu-id="2fabb-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="2fabb-220">Konfigurere stillinger</span><span class="sxs-lookup"><span data-stu-id="2fabb-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="2fabb-221">Afdelinger</span><span class="sxs-lookup"><span data-stu-id="2fabb-221">Departments</span></span>

<span data-ttu-id="2fabb-222">En afdeling er en driftsenhed, der repræsenterer en kategori eller et funktionsområde i en organisation.</span><span class="sxs-lookup"><span data-stu-id="2fabb-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="2fabb-223">En afdeling er ansvarlig for et bestemt område i organisationen, såsom salg, regnskab eller personale.</span><span class="sxs-lookup"><span data-stu-id="2fabb-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="2fabb-224">Du kan bruge afdelinger til at rapportere om funktionsområder.</span><span class="sxs-lookup"><span data-stu-id="2fabb-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="2fabb-225">Afdelinger kan have ansvar for driftsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="2fabb-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="2fabb-226">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="2fabb-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="2fabb-227">Oprette en afdeling og knytte den til afdelingshierarkiet</span><span class="sxs-lookup"><span data-stu-id="2fabb-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="2fabb-228">Definere nye afdelinger</span><span class="sxs-lookup"><span data-stu-id="2fabb-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="2fabb-229">Betalingscyklusser og lønperioder</span><span class="sxs-lookup"><span data-stu-id="2fabb-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="2fabb-230">En betalingscyklus bestemmer, hvor ofte løn køres,og de specifikke dage, hvor arbejdere betales.</span><span class="sxs-lookup"><span data-stu-id="2fabb-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="2fabb-231">En løncyklus kan f.eks. være månedlig, og medarbejdere betales måske på den sidste dag i måneden.</span><span class="sxs-lookup"><span data-stu-id="2fabb-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="2fabb-232">En løncyklus kan også være ugentligt, og medarbejdere betales måske tirsdag efter slutningen af lønperioden.</span><span class="sxs-lookup"><span data-stu-id="2fabb-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="2fabb-233">Løncyklusser tildeles til stillinger for at styre, hvornår arbejdere i disse stillinger bliver betalt.</span><span class="sxs-lookup"><span data-stu-id="2fabb-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="2fabb-234">Når du opretter betalingscyklusser, kan du generere lønperioder for hver cyklus.</span><span class="sxs-lookup"><span data-stu-id="2fabb-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="2fabb-235">Hver lønperiode omfatter en standardbetalingsdato, der er baseret på oplysninger, du angiver.</span><span class="sxs-lookup"><span data-stu-id="2fabb-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="2fabb-236">Du kan dog redigere standardbetalingsdatoen i en lønperiode til at tillade undtagelser, f.eks. når betalingsdatoen falder på en helligdag.</span><span class="sxs-lookup"><span data-stu-id="2fabb-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="2fabb-237">Følgende oplysninger bruges i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="2fabb-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="2fabb-238">Betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-238">Pay cycle (required)</span></span>
- <span data-ttu-id="2fabb-239">Hyppighed for betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="2fabb-240">Periodens startdato (første lønperiode påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="2fabb-241">Standardbetalingsdato (første lønperiode påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="2fabb-242">Oplysningerne er integreret med Dayforce som løngrupper og adskilles af et land eller område for hver løncyklus.</span><span class="sxs-lookup"><span data-stu-id="2fabb-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="2fabb-243">Mindst én periode skal genereres før integration.</span><span class="sxs-lookup"><span data-stu-id="2fabb-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="2fabb-244">Dayforce genererer løngruppekalendere og betalingsdatoer, der er baseret på startdatoen for den første lønperiode og den standardbetalingsdato, der er angivet i Talent.</span><span class="sxs-lookup"><span data-stu-id="2fabb-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="2fabb-245">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="2fabb-245">Earning codes</span></span>

<span data-ttu-id="2fabb-246">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="2fabb-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="2fabb-247">Koderne har forskellige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="2fabb-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="2fabb-248">Følgende oplysninger bruges i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="2fabb-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="2fabb-249">Lønkode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-249">Earning Code (required)</span></span>
- <span data-ttu-id="2fabb-250">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="2fabb-250">Description</span></span>
- <span data-ttu-id="2fabb-251">Måleenhed</span><span class="sxs-lookup"><span data-stu-id="2fabb-251">Unit of measure</span></span>
- <span data-ttu-id="2fabb-252">Produktiv</span><span class="sxs-lookup"><span data-stu-id="2fabb-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="2fabb-253">Arbejderdata</span><span class="sxs-lookup"><span data-stu-id="2fabb-253">Worker data</span></span>

<span data-ttu-id="2fabb-254">Posterne for de forskellige typer arbejdere, du beskæftiger, er vigtige for dine personale- og lønsystemer.</span><span class="sxs-lookup"><span data-stu-id="2fabb-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="2fabb-255">De oplysninger, du angiver, kan bruges til at spore arbejdere og personoplysninger.</span><span class="sxs-lookup"><span data-stu-id="2fabb-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="2fabb-256">Du kan vedligeholde følgende oplysninger for arbejdere:</span><span class="sxs-lookup"><span data-stu-id="2fabb-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="2fabb-257">**Basis** – Vedligehold grundlæggende oplysninger om en arbejder, f.eks. kontaktoplysninger, demografiske oplysninger, identifikationsoplysninger, oplysninger om familie, status for militærtjeneste, oplysninger om udstationering og personlige kontaktpersoner og kontaktpersoner i nødsituationer.</span><span class="sxs-lookup"><span data-stu-id="2fabb-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="2fabb-258">**Beskæftigelse** – Vedligehold oplysninger om en arbejders beskæftigelse, f.eks. firma- eller organisationstilhørsforhold, stillingstildeling, start- og slutdatoer, arbejdstilladelse, vilkår for ansættelse, pension, ferie og flytteoplysninger.</span><span class="sxs-lookup"><span data-stu-id="2fabb-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="2fabb-259">**Orlov og fravær** – Vedligehold oplysninger om en arbejders fravær, f.eks. arbejdskalendere, fraværstransaktioner og fraværsopsætning.</span><span class="sxs-lookup"><span data-stu-id="2fabb-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="2fabb-260">**Kompensation og løn** – Vedligehold oplysninger om en arbejders kompensationsplaner og lønoplysninger, f.eks. tilmelding til planer, priser, ydeevne, provision, skatteoplysninger, pensionering og skattefradrag.</span><span class="sxs-lookup"><span data-stu-id="2fabb-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="2fabb-261">Når du angiver arbejderoplysninger, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2fabb-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="2fabb-262">Generelle oplysninger</span><span class="sxs-lookup"><span data-stu-id="2fabb-262">General information</span></span>

- <span data-ttu-id="2fabb-263">Personalenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-263">Personnel number (required)</span></span>
- <span data-ttu-id="2fabb-264">Fornavn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-264">First name (required)</span></span>
- <span data-ttu-id="2fabb-265">Efternavn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-265">Last name (required)</span></span>
- <span data-ttu-id="2fabb-266">Mellemnavn</span><span class="sxs-lookup"><span data-stu-id="2fabb-266">Middle name</span></span>
- <span data-ttu-id="2fabb-267">Anciennitetsdato</span><span class="sxs-lookup"><span data-stu-id="2fabb-267">Seniority date</span></span>
- <span data-ttu-id="2fabb-268">Kendt som</span><span class="sxs-lookup"><span data-stu-id="2fabb-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="2fabb-269">Personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="2fabb-269">Personal information</span></span>

- <span data-ttu-id="2fabb-270">Ægteskabelig status (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-270">Marital status (required)</span></span>
- <span data-ttu-id="2fabb-271">Fødselsdato (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-271">Birth date (required)</span></span>
- <span data-ttu-id="2fabb-272">Køn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-272">Gender (required)</span></span>
- <span data-ttu-id="2fabb-273">Handicappet</span><span class="sxs-lookup"><span data-stu-id="2fabb-273">Person with disabilities</span></span>
- <span data-ttu-id="2fabb-274">Land eller område for nationalitet (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="2fabb-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="2fabb-275">Adresseoplysninger</span><span class="sxs-lookup"><span data-stu-id="2fabb-275">Address information</span></span>

- <span data-ttu-id="2fabb-276">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-276">Primary (required)</span></span>
- <span data-ttu-id="2fabb-277">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-277">Country/region (required)</span></span>
- <span data-ttu-id="2fabb-278">Postnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-278">Postal code (required)</span></span>
- <span data-ttu-id="2fabb-279">Gadenummer (påkrævet) (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="2fabb-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="2fabb-280">Bygningskomplement (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="2fabb-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="2fabb-281">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-281">City (required)</span></span>
- <span data-ttu-id="2fabb-282">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-282">State (required)</span></span>
- <span data-ttu-id="2fabb-283">Region (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="2fabb-284">Kontaktoplysninger</span><span class="sxs-lookup"><span data-stu-id="2fabb-284">Contact information</span></span> 

- <span data-ttu-id="2fabb-285">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-285">Primary (required)</span></span>
- <span data-ttu-id="2fabb-286">Kontaktpersonens nummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-286">Contact number (required)</span></span>
- <span data-ttu-id="2fabb-287">Forlængelse</span><span class="sxs-lookup"><span data-stu-id="2fabb-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="2fabb-288">Lønoplysninger og lønkoder</span><span class="sxs-lookup"><span data-stu-id="2fabb-288">Payroll information and earning codes</span></span>

<span data-ttu-id="2fabb-289">Medarbejdere kan tildeles en bestemt løn med en given betalingshyppighed og have en foretrukken betalingsmetode.</span><span class="sxs-lookup"><span data-stu-id="2fabb-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="2fabb-290">Følgende felter bruges i Dayforce til at sikre, at disse præferencer og indstillinger bruges.</span><span class="sxs-lookup"><span data-stu-id="2fabb-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="2fabb-291">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="2fabb-291">Earning codes</span></span>

- <span data-ttu-id="2fabb-292">Stilling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-292">Position (required)</span></span>
- <span data-ttu-id="2fabb-293">Lønkode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-293">Earning Code (required)</span></span>
- <span data-ttu-id="2fabb-294">Frekvens (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-294">Frequency (required)</span></span>
- <span data-ttu-id="2fabb-295">Beløb (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="2fabb-296">Lønoplysninger</span><span class="sxs-lookup"><span data-stu-id="2fabb-296">Payroll information</span></span>

- <span data-ttu-id="2fabb-297">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="2fabb-297">Payment Method</span></span>
- <span data-ttu-id="2fabb-298">Økonomisk område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-298">Economic Region (required)</span></span>
- <span data-ttu-id="2fabb-299">Id for medarbejderfrynsegoder</span><span class="sxs-lookup"><span data-stu-id="2fabb-299">Employee Benefits ID</span></span>
- <span data-ttu-id="2fabb-300">Nationalt id-nummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-300">National ID Number (required)</span></span>
- <span data-ttu-id="2fabb-301">Tjenestenummer hos militær</span><span class="sxs-lookup"><span data-stu-id="2fabb-301">Military Service Number</span></span>
- <span data-ttu-id="2fabb-302">Skifte-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-302">Shift ID (required)</span></span>
- <span data-ttu-id="2fabb-303">Skattenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-303">Tax Number (required)</span></span>
- <span data-ttu-id="2fabb-304">Fagforenings-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-304">Union ID (required)</span></span>
- <span data-ttu-id="2fabb-305">Arbejdsdags-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-305">Work Day ID (required)</span></span>
- <span data-ttu-id="2fabb-306">Arbejdstilladelsesnummer</span><span class="sxs-lookup"><span data-stu-id="2fabb-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="2fabb-307">For betalingsmetoden understøtter Mexico **Kontant**, **Check** (firmaets fysiske check), og **Elektronisk betaling**.</span><span class="sxs-lookup"><span data-stu-id="2fabb-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="2fabb-308">Hvis der ikke er angivet nogen betalingsmetode, bruges **Check** som standard.</span><span class="sxs-lookup"><span data-stu-id="2fabb-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="2fabb-309">Detaljer om ansættelse</span><span class="sxs-lookup"><span data-stu-id="2fabb-309">Employment details</span></span>

<span data-ttu-id="2fabb-310">Detaljeret ansættelseshistorik bruges som vigtige oplysninger til at udlede statusser for en medarbejders ansættelse, fratrædelse og genansættelse i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2fabb-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="2fabb-311">Dayforce understøtter kun én aktiv ansættelsespost ad gangen.</span><span class="sxs-lookup"><span data-stu-id="2fabb-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="2fabb-312">Startdato for ansættelse (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-312">Employment start date (required)</span></span>
- <span data-ttu-id="2fabb-313">Slutdato for ansættelse</span><span class="sxs-lookup"><span data-stu-id="2fabb-313">Employment end date</span></span>
- <span data-ttu-id="2fabb-314">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="2fabb-314">Start date</span></span>
- <span data-ttu-id="2fabb-315">Justeret startdato</span><span class="sxs-lookup"><span data-stu-id="2fabb-315">Adjusted start date</span></span>
- <span data-ttu-id="2fabb-316">Fratrædelsesdato (kræves ved fratrædelse)</span><span class="sxs-lookup"><span data-stu-id="2fabb-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="2fabb-317">Fratrædelsesårsag (kræves ved fratrædelse)</span><span class="sxs-lookup"><span data-stu-id="2fabb-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="2fabb-318">Vigtige datoer for en medarbejders udledes ved hjælp af følgende oplysninger.</span><span class="sxs-lookup"><span data-stu-id="2fabb-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="2fabb-319">Talent</span><span class="sxs-lookup"><span data-stu-id="2fabb-319">Talent</span></span>                | <span data-ttu-id="2fabb-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2fabb-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fabb-321">Den seneste ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="2fabb-321">Most recent hire date</span></span> | <span data-ttu-id="2fabb-322">Historikpost for ansættelsesstart for aktuel ikke-afsluttet ansættelse</span><span class="sxs-lookup"><span data-stu-id="2fabb-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="2fabb-323">Fratrædelsesdato</span><span class="sxs-lookup"><span data-stu-id="2fabb-323">Termination date</span></span>      | <span data-ttu-id="2fabb-324">Historikpost for fratrædelsesdato for aktuel ikke-afsluttet ansættelse</span><span class="sxs-lookup"><span data-stu-id="2fabb-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="2fabb-325">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="2fabb-325">Start date</span></span>            | <span data-ttu-id="2fabb-326">Historikpost for justeret startdato, startdato eller startdato for ansættelse for aktuel ikke-aktiv ansættelse</span><span class="sxs-lookup"><span data-stu-id="2fabb-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="2fabb-327">Oprindelig ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="2fabb-327">Original hire date</span></span>    | <span data-ttu-id="2fabb-328">Historikpost for ansættelsesstart for tidligste ansættelse</span><span class="sxs-lookup"><span data-stu-id="2fabb-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="2fabb-329">Kompensation</span><span class="sxs-lookup"><span data-stu-id="2fabb-329">Compensation</span></span>

<span data-ttu-id="2fabb-330">En fast lønstruktur skal tilknyttes hver medarbejders primære stilling gennem hele ansættelsesperioden.</span><span class="sxs-lookup"><span data-stu-id="2fabb-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="2fabb-331">Denne periode starter på den dato, hvor medarbejderen blev ansat (eller ansættelsesstartdatoen) og fortsætter, indtil fratrædelsen.</span><span class="sxs-lookup"><span data-stu-id="2fabb-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="2fabb-332">Ikrafttrædelsesdato (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-332">Effective Date (required)</span></span>
- <span data-ttu-id="2fabb-333">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="2fabb-333">Expiration date</span></span>
- <span data-ttu-id="2fabb-334">Lønsats (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-334">Pay Rate (required)</span></span>
- <span data-ttu-id="2fabb-335">Konverteringer af lønsats (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="2fabb-336">Årlig ækvivalent (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="2fabb-337">Timebaseret ækvivalent (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="2fabb-338">Hvis en timeansat medarbejder har flere stillinger, indlæses den faste løn for den primære stilling i Dayforce, som basissats/-løn på medarbejderniveau.</span><span class="sxs-lookup"><span data-stu-id="2fabb-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="2fabb-339">For ikke-primære stillinger gemmes timesatsen i den tilsvarende position i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2fabb-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="2fabb-340">Hvis en funktionær har flere stillinger, afledes den kumulative timesats og årlig gage på tværs af alle aktive stillinger og bruges som basissats/-gage på medarbejderniveau.</span><span class="sxs-lookup"><span data-stu-id="2fabb-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="2fabb-341">Identifikationsnumre</span><span class="sxs-lookup"><span data-stu-id="2fabb-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="2fabb-342">Social Security-identifikator</span><span class="sxs-lookup"><span data-stu-id="2fabb-342">Social Security identifier</span></span> 

<span data-ttu-id="2fabb-343">Alle medarbejdere skal have én primær identifikator.</span><span class="sxs-lookup"><span data-stu-id="2fabb-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="2fabb-344">Identifikatoren skal være af **SSN**-identifikationstypen</span><span class="sxs-lookup"><span data-stu-id="2fabb-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="2fabb-345">I Dayforce afledes den automatisk som medarbejderens Social Security-identifikator, der er påkrævet ved ansættelse.</span><span class="sxs-lookup"><span data-stu-id="2fabb-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="2fabb-346">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-346">Primary (required)</span></span>
- <span data-ttu-id="2fabb-347">Identifikationstype = "SSN"</span><span class="sxs-lookup"><span data-stu-id="2fabb-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="2fabb-348">Udstedt den</span><span class="sxs-lookup"><span data-stu-id="2fabb-348">Issued Date</span></span>
- <span data-ttu-id="2fabb-349">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="2fabb-349">Expiration Date</span></span>

<span data-ttu-id="2fabb-350">Medarbejdere kan angive flere identifikationsnumre af **SSN**-identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="2fabb-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="2fabb-351">Men det er kun den post, der er markeret som **Primær**, som er integreret i Dayforce, uanset om nummeret er aktivt eller udløbet.</span><span class="sxs-lookup"><span data-stu-id="2fabb-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="2fabb-352">Bankkonto og udbetalinger</span><span class="sxs-lookup"><span data-stu-id="2fabb-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="2fabb-353">Gyldige bankkontooplysninger skal angives for enhver medarbejder, der vælger at blive betalt via bankkontooverførsler.</span><span class="sxs-lookup"><span data-stu-id="2fabb-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="2fabb-354">Talent</span><span class="sxs-lookup"><span data-stu-id="2fabb-354">Talent</span></span>                         | <span data-ttu-id="2fabb-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2fabb-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fabb-356">Bankkontonummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="2fabb-357">SWIFT-kode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-357">SWIFT code (required)</span></span>          | <span data-ttu-id="2fabb-358">Feltet **Bank-id** bruges ved behandling af løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="2fabb-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="2fabb-359">Afdelingsnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="2fabb-360">Bankkontotype (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-360">Bank account type (required)</span></span>   | <span data-ttu-id="2fabb-361">Feltet **Kontotype** bruges ved behandling af løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="2fabb-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="2fabb-362">Understøttede værdier omfatter **Check** og **Løn**.</span><span class="sxs-lookup"><span data-stu-id="2fabb-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="2fabb-363">Medarbejdere, der vælger at betales via bankkontooverførsler, skal angive et link til en restbeløbskonto, der hører under en juridisk enhed, som har primær adresse i Mexico og er knyttet til en gyldig bankkonto fra en mexicansk bank.</span><span class="sxs-lookup"><span data-stu-id="2fabb-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="2fabb-364">Alle andre restbeløbskonti ignoreres.</span><span class="sxs-lookup"><span data-stu-id="2fabb-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="2fabb-365">Adresseoplysninger</span><span class="sxs-lookup"><span data-stu-id="2fabb-365">Address information</span></span>

<span data-ttu-id="2fabb-366">Alle medarbejdere skal have én primær placering.</span><span class="sxs-lookup"><span data-stu-id="2fabb-366">Every employee must have one primary location.</span></span> <span data-ttu-id="2fabb-367">I Dayforce bruges denne placering til at bestemme medarbejderens primære opholdssted til skattemæssige formål.</span><span class="sxs-lookup"><span data-stu-id="2fabb-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="2fabb-368">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-368">Primary (required)</span></span>
- <span data-ttu-id="2fabb-369">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-369">Country/region (required)</span></span>
- <span data-ttu-id="2fabb-370">Postnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="2fabb-371">Gade (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-371">Street (required)</span></span>
- <span data-ttu-id="2fabb-372">Gadenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-372">Street Number (required)</span></span>
- <span data-ttu-id="2fabb-373">Bygningskomplement</span><span class="sxs-lookup"><span data-stu-id="2fabb-373">Building Complement</span></span>
- <span data-ttu-id="2fabb-374">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-374">City (required)</span></span>
- <span data-ttu-id="2fabb-375">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-375">State (required)</span></span>
- <span data-ttu-id="2fabb-376">Region (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="2fabb-377">Konfigurere dataene for at generere løn i USA og Canada</span><span class="sxs-lookup"><span data-stu-id="2fabb-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="2fabb-378">Hvis du genererer løn for medarbejdere i USA og Canada, skal følgende elementer konfigureres:</span><span class="sxs-lookup"><span data-stu-id="2fabb-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="2fabb-379">Der kræves afdelinger til stillinger.</span><span class="sxs-lookup"><span data-stu-id="2fabb-379">Departments are required on positions.</span></span>
- <span data-ttu-id="2fabb-380">Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="2fabb-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="2fabb-381">Du kan konfigurere Talent til at kræve, at der angives en afdeling for stillinger.</span><span class="sxs-lookup"><span data-stu-id="2fabb-381">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="2fabb-382">For at gøre dette skal du gå til **Personalets delte stillinger > Stillinger > Kræv afdelinger for stillinger**.</span><span class="sxs-lookup"><span data-stu-id="2fabb-382">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="2fabb-383">Det anbefales, at denne indstilling gennemtvinges i forbindelse med integrationen.</span><span class="sxs-lookup"><span data-stu-id="2fabb-383">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="2fabb-384">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="2fabb-384">Job types</span></span>

<span data-ttu-id="2fabb-385">Jobtyper bruges til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="2fabb-385">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="2fabb-386">Jobtyper kræves for at behandle løn i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="2fabb-386">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="2fabb-387">Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="2fabb-387">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="2fabb-388">Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.</span><span class="sxs-lookup"><span data-stu-id="2fabb-388">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="2fabb-389">Der kræves følgende jobtyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="2fabb-389">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="2fabb-390">Jobtype</span><span class="sxs-lookup"><span data-stu-id="2fabb-390">Job type</span></span>   | <span data-ttu-id="2fabb-391">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="2fabb-391">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="2fabb-392">Pr. time</span><span class="sxs-lookup"><span data-stu-id="2fabb-392">Hourly</span></span>     | <span data-ttu-id="2fabb-393">Pr. time</span><span class="sxs-lookup"><span data-stu-id="2fabb-393">Hourly</span></span>      |
| <span data-ttu-id="2fabb-394">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="2fabb-394">Salaried</span></span>   | <span data-ttu-id="2fabb-395">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="2fabb-395">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="2fabb-396">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="2fabb-396">Position types</span></span> 

<span data-ttu-id="2fabb-397">Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet.</span><span class="sxs-lookup"><span data-stu-id="2fabb-397">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="2fabb-398">Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="2fabb-398">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="2fabb-399">Der kræves følgende stillingstyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="2fabb-399">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="2fabb-400">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="2fabb-400">Position type</span></span>   | <span data-ttu-id="2fabb-401">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="2fabb-401">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="2fabb-402">Fuld tid</span><span class="sxs-lookup"><span data-stu-id="2fabb-402">Full-time</span></span>       | <span data-ttu-id="2fabb-403">Fuldtidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="2fabb-403">Full time employee</span></span> |
| <span data-ttu-id="2fabb-404">Deltid</span><span class="sxs-lookup"><span data-stu-id="2fabb-404">Part-time</span></span>       | <span data-ttu-id="2fabb-405">Deltidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="2fabb-405">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="2fabb-406">Årsagskoder</span><span class="sxs-lookup"><span data-stu-id="2fabb-406">Reason codes</span></span>

<span data-ttu-id="2fabb-407">Årsagskoder indeholder oplysninger om status for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="2fabb-407">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="2fabb-408">Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.</span><span class="sxs-lookup"><span data-stu-id="2fabb-408">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="2fabb-409">Der kræves følgende årsagskoder og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="2fabb-409">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="2fabb-410">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="2fabb-410">Reason code</span></span>    | <span data-ttu-id="2fabb-411">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="2fabb-411">Description</span></span>      | <span data-ttu-id="2fabb-412">Anvendelige scenarier</span><span class="sxs-lookup"><span data-stu-id="2fabb-412">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="2fabb-413">OPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="2fabb-413">RESIGNATION</span></span>    | <span data-ttu-id="2fabb-414">Opsigelse</span><span class="sxs-lookup"><span data-stu-id="2fabb-414">Resignation</span></span>      | <span data-ttu-id="2fabb-415">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="2fabb-415">Terminate worker</span></span>     |
| <span data-ttu-id="2fabb-416">OPHØR</span><span class="sxs-lookup"><span data-stu-id="2fabb-416">TERMINATION</span></span>    | <span data-ttu-id="2fabb-417">Ophør</span><span class="sxs-lookup"><span data-stu-id="2fabb-417">Termination</span></span>      | <span data-ttu-id="2fabb-418">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="2fabb-418">Terminate worker</span></span>     |
| <span data-ttu-id="2fabb-419">PENSION</span><span class="sxs-lookup"><span data-stu-id="2fabb-419">RETIREMENT</span></span>     | <span data-ttu-id="2fabb-420">Pension</span><span class="sxs-lookup"><span data-stu-id="2fabb-420">Retirement</span></span>       | <span data-ttu-id="2fabb-421">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="2fabb-421">Terminate worker</span></span>     |
| <span data-ttu-id="2fabb-422">ANDET</span><span class="sxs-lookup"><span data-stu-id="2fabb-422">OTHER</span></span>          | <span data-ttu-id="2fabb-423">Andre årsager</span><span class="sxs-lookup"><span data-stu-id="2fabb-423">Other Reasons</span></span>    | <span data-ttu-id="2fabb-424">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="2fabb-424">Terminate worker</span></span>     |
| <span data-ttu-id="2fabb-425">DØDSFALD</span><span class="sxs-lookup"><span data-stu-id="2fabb-425">DEATH</span></span>          | <span data-ttu-id="2fabb-426">Dødsfald</span><span class="sxs-lookup"><span data-stu-id="2fabb-426">Death</span></span>            | <span data-ttu-id="2fabb-427">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="2fabb-427">Terminate worker</span></span>     |
| <span data-ttu-id="2fabb-428">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="2fabb-428">LEAVEOFABSENCE</span></span> | <span data-ttu-id="2fabb-429">Orlov</span><span class="sxs-lookup"><span data-stu-id="2fabb-429">Leave of Absence</span></span> | <span data-ttu-id="2fabb-430">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="2fabb-430">Terminate worker</span></span>     |
| <span data-ttu-id="2fabb-431">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="2fabb-431">CONTRACTEND</span></span>    | <span data-ttu-id="2fabb-432">Kontraktudløb</span><span class="sxs-lookup"><span data-stu-id="2fabb-432">End of Contract</span></span>  | <span data-ttu-id="2fabb-433">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="2fabb-433">Terminate worker</span></span>     |
| <span data-ttu-id="2fabb-434">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="2fabb-434">SALARYCHANGE</span></span>   | <span data-ttu-id="2fabb-435">Ændring af løn</span><span class="sxs-lookup"><span data-stu-id="2fabb-435">Change of Salary</span></span> | <span data-ttu-id="2fabb-436">Kompensation</span><span class="sxs-lookup"><span data-stu-id="2fabb-436">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="2fabb-437">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="2fabb-437">Marital status</span></span>

<span data-ttu-id="2fabb-438">Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="2fabb-438">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="2fabb-439">Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2fabb-439">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="2fabb-440">Talent</span><span class="sxs-lookup"><span data-stu-id="2fabb-440">Talent</span></span>                 | <span data-ttu-id="2fabb-441">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2fabb-441">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="2fabb-442">Gift</span><span class="sxs-lookup"><span data-stu-id="2fabb-442">Married</span></span>                | <span data-ttu-id="2fabb-443">Gift</span><span class="sxs-lookup"><span data-stu-id="2fabb-443">Married</span></span>              |
| <span data-ttu-id="2fabb-444">Enlig</span><span class="sxs-lookup"><span data-stu-id="2fabb-444">Single</span></span>                 | <span data-ttu-id="2fabb-445">Enlig</span><span class="sxs-lookup"><span data-stu-id="2fabb-445">Single</span></span>               |
| <span data-ttu-id="2fabb-446">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="2fabb-446">Widowed</span></span>                | <span data-ttu-id="2fabb-447">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="2fabb-447">Widowed</span></span>              |
| <span data-ttu-id="2fabb-448">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="2fabb-448">Divorced</span></span>               | <span data-ttu-id="2fabb-449">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="2fabb-449">Divorced</span></span>             |
| <span data-ttu-id="2fabb-450">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="2fabb-450">Registered Partnership</span></span> | <span data-ttu-id="2fabb-451">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="2fabb-451">Domestic Partnership</span></span> |
| <span data-ttu-id="2fabb-452">None</span><span class="sxs-lookup"><span data-stu-id="2fabb-452">None</span></span>                   | <span data-ttu-id="2fabb-453">None</span><span class="sxs-lookup"><span data-stu-id="2fabb-453">None</span></span>                 |
| <span data-ttu-id="2fabb-454">Samlever</span><span class="sxs-lookup"><span data-stu-id="2fabb-454">Cohabiting</span></span>             | <span data-ttu-id="2fabb-455">Samlever</span><span class="sxs-lookup"><span data-stu-id="2fabb-455">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="2fabb-456">Køn</span><span class="sxs-lookup"><span data-stu-id="2fabb-456">Gender</span></span>

<span data-ttu-id="2fabb-457">Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="2fabb-457">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="2fabb-458">Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2fabb-458">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="2fabb-459">Talent</span><span class="sxs-lookup"><span data-stu-id="2fabb-459">Talent</span></span>       | <span data-ttu-id="2fabb-460">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2fabb-460">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="2fabb-461">Mand</span><span class="sxs-lookup"><span data-stu-id="2fabb-461">Male</span></span>         | <span data-ttu-id="2fabb-462">Mand</span><span class="sxs-lookup"><span data-stu-id="2fabb-462">Male</span></span>            |
| <span data-ttu-id="2fabb-463">Kvinde</span><span class="sxs-lookup"><span data-stu-id="2fabb-463">Female</span></span>       | <span data-ttu-id="2fabb-464">Kvinde</span><span class="sxs-lookup"><span data-stu-id="2fabb-464">Female</span></span>          |
| <span data-ttu-id="2fabb-465">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="2fabb-465">Non-specific</span></span> | <span data-ttu-id="2fabb-466">*Understøttes ikke*</span><span class="sxs-lookup"><span data-stu-id="2fabb-466">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="2fabb-467">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="2fabb-467">Earning codes</span></span>

<span data-ttu-id="2fabb-468">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="2fabb-468">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="2fabb-469">Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="2fabb-469">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="2fabb-470">Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="2fabb-470">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="2fabb-471">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="2fabb-471">Supported frequencies</span></span>

- <span data-ttu-id="2fabb-472">Alt</span><span class="sxs-lookup"><span data-stu-id="2fabb-472">All</span></span>
- <span data-ttu-id="2fabb-473">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="2fabb-473">EVERYPAY</span></span>
- <span data-ttu-id="2fabb-474">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="2fabb-474">EACHPAYPERIOD</span></span>
- <span data-ttu-id="2fabb-475">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="2fabb-475">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="2fabb-476">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="2fabb-476">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="2fabb-477">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-477">1OFMTH</span></span>
- <span data-ttu-id="2fabb-478">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-478">LASTOFMTH</span></span>
- <span data-ttu-id="2fabb-479">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-479">2OFMTH</span></span>
- <span data-ttu-id="2fabb-480">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-480">3OFMTH</span></span>
- <span data-ttu-id="2fabb-481">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-481">4OFMTH</span></span>
- <span data-ttu-id="2fabb-482">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-482">5OFMTH</span></span>
- <span data-ttu-id="2fabb-483">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-483">1N2OFMTH</span></span>
- <span data-ttu-id="2fabb-484">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-484">3N4OFMTH</span></span>
- <span data-ttu-id="2fabb-485">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-485">1N3OFMTH</span></span>
- <span data-ttu-id="2fabb-486">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-486">1N4OFMTH</span></span>
- <span data-ttu-id="2fabb-487">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-487">2N3OFMTH</span></span>
- <span data-ttu-id="2fabb-488">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-488">2N4OFMTH</span></span>
- <span data-ttu-id="2fabb-489">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-489">1N2N3OFMTH</span></span>
- <span data-ttu-id="2fabb-490">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-490">1N2N4OFMTH</span></span>
- <span data-ttu-id="2fabb-491">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-491">1N3N4OFMTH</span></span>
- <span data-ttu-id="2fabb-492">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-492">2N3N4OFMTH</span></span>
- <span data-ttu-id="2fabb-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="2fabb-494">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="2fabb-494">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="2fabb-495">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="2fabb-495">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="2fabb-496">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="2fabb-496">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="2fabb-497">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="2fabb-497">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="2fabb-498">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="2fabb-498">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="2fabb-499">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="2fabb-499">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="2fabb-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="2fabb-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="2fabb-501">Adresser</span><span class="sxs-lookup"><span data-stu-id="2fabb-501">Addresses</span></span>

<span data-ttu-id="2fabb-502">Identifikation af specifikke koder for land eller region, stat og område (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende.</span><span class="sxs-lookup"><span data-stu-id="2fabb-502">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="2fabb-503">Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.</span><span class="sxs-lookup"><span data-stu-id="2fabb-503">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="2fabb-504">Talent</span><span class="sxs-lookup"><span data-stu-id="2fabb-504">Talent</span></span>          | <span data-ttu-id="2fabb-505">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2fabb-505">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="2fabb-506">Land/område</span><span class="sxs-lookup"><span data-stu-id="2fabb-506">Country/Region</span></span>  | <span data-ttu-id="2fabb-507">Landekode</span><span class="sxs-lookup"><span data-stu-id="2fabb-507">Country Code</span></span>          |
| <span data-ttu-id="2fabb-508">Postnummer</span><span class="sxs-lookup"><span data-stu-id="2fabb-508">Zip/Postal Code</span></span> | <span data-ttu-id="2fabb-509">Postnummer</span><span class="sxs-lookup"><span data-stu-id="2fabb-509">Postal Code</span></span>           |
| <span data-ttu-id="2fabb-510">Status</span><span class="sxs-lookup"><span data-stu-id="2fabb-510">State</span></span>           | <span data-ttu-id="2fabb-511">Statskode</span><span class="sxs-lookup"><span data-stu-id="2fabb-511">State Code</span></span>            |
| <span data-ttu-id="2fabb-512">Bynavn</span><span class="sxs-lookup"><span data-stu-id="2fabb-512">City</span></span>            | <span data-ttu-id="2fabb-513">Bynavn</span><span class="sxs-lookup"><span data-stu-id="2fabb-513">City</span></span>                  |
| <span data-ttu-id="2fabb-514">Region</span><span class="sxs-lookup"><span data-stu-id="2fabb-514">County</span></span>          | <span data-ttu-id="2fabb-515">Område (kommune)</span><span class="sxs-lookup"><span data-stu-id="2fabb-515">County (Municipality)</span></span> |
| <span data-ttu-id="2fabb-516">Gade</span><span class="sxs-lookup"><span data-stu-id="2fabb-516">Street</span></span>          | <span data-ttu-id="2fabb-517">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="2fabb-517">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="2fabb-518">Skatteområder</span><span class="sxs-lookup"><span data-stu-id="2fabb-518">Tax regions</span></span>

<span data-ttu-id="2fabb-519">Skatteområder bruges til at bestemme den relevante skat, der skal anvendes ved løngenerering.</span><span class="sxs-lookup"><span data-stu-id="2fabb-519">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="2fabb-520">Skatteområder er tilknyttet Dayforce som placeringsadresser.</span><span class="sxs-lookup"><span data-stu-id="2fabb-520">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="2fabb-521">Standardskatteområder skal knyttes til arbejderens aktive stilling.</span><span class="sxs-lookup"><span data-stu-id="2fabb-521">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="2fabb-522">Skatteområde (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-522">Tax region (required)</span></span>
- <span data-ttu-id="2fabb-523">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-523">Country/Region (required)</span></span>
- <span data-ttu-id="2fabb-524">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-524">State (required)</span></span>
- <span data-ttu-id="2fabb-525">Region</span><span class="sxs-lookup"><span data-stu-id="2fabb-525">County</span></span> 
- <span data-ttu-id="2fabb-526">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="2fabb-526">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="2fabb-527">Konfigurere dataene for at generere løn i Mexico</span><span class="sxs-lookup"><span data-stu-id="2fabb-527">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="2fabb-528">Hvis du genererer løn for medarbejdere i Mexico skal følgende elementer konfigureres:</span><span class="sxs-lookup"><span data-stu-id="2fabb-528">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="2fabb-529">Der kræves afdelinger til stillinger.</span><span class="sxs-lookup"><span data-stu-id="2fabb-529">Departments are required on positions.</span></span>
- <span data-ttu-id="2fabb-530">Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="2fabb-530">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="2fabb-531">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="2fabb-531">Job types</span></span>

<span data-ttu-id="2fabb-532">Jobtyper bruges til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="2fabb-532">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="2fabb-533">Jobtyper kræves for at behandle løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="2fabb-533">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="2fabb-534">Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="2fabb-534">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="2fabb-535">Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.</span><span class="sxs-lookup"><span data-stu-id="2fabb-535">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="2fabb-536">Der kræves følgende jobtyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="2fabb-536">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="2fabb-537">Jobtype</span><span class="sxs-lookup"><span data-stu-id="2fabb-537">Job type</span></span>   | <span data-ttu-id="2fabb-538">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="2fabb-538">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="2fabb-539">Pr. time</span><span class="sxs-lookup"><span data-stu-id="2fabb-539">Hourly</span></span>     | <span data-ttu-id="2fabb-540">MX Pr. time</span><span class="sxs-lookup"><span data-stu-id="2fabb-540">MX Hourly</span></span>   |
| <span data-ttu-id="2fabb-541">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="2fabb-541">Salaried</span></span>   | <span data-ttu-id="2fabb-542">MX Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="2fabb-542">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="2fabb-543">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="2fabb-543">Position types</span></span> 

<span data-ttu-id="2fabb-544">Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet.</span><span class="sxs-lookup"><span data-stu-id="2fabb-544">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="2fabb-545">Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="2fabb-545">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="2fabb-546">Der kræves følgende stillingstyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="2fabb-546">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="2fabb-547">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="2fabb-547">Position type</span></span>   | <span data-ttu-id="2fabb-548">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="2fabb-548">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="2fabb-549">Fuld tid</span><span class="sxs-lookup"><span data-stu-id="2fabb-549">Full-time</span></span>       | <span data-ttu-id="2fabb-550">Fuldtidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="2fabb-550">Full time employee</span></span> |
| <span data-ttu-id="2fabb-551">Deltid</span><span class="sxs-lookup"><span data-stu-id="2fabb-551">Part-time</span></span>       | <span data-ttu-id="2fabb-552">Deltidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="2fabb-552">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="2fabb-553">Årsagskoder</span><span class="sxs-lookup"><span data-stu-id="2fabb-553">Reason codes</span></span>

<span data-ttu-id="2fabb-554">Årsagskoder indeholder oplysninger om status for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="2fabb-554">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="2fabb-555">Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.</span><span class="sxs-lookup"><span data-stu-id="2fabb-555">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="2fabb-556">Der kræves følgende årsagskoder og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="2fabb-556">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="2fabb-557">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="2fabb-557">Reason code</span></span>            | <span data-ttu-id="2fabb-558">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="2fabb-558">Description</span></span>                    | <span data-ttu-id="2fabb-559">Anvendelige scenarier</span><span class="sxs-lookup"><span data-stu-id="2fabb-559">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="2fabb-560">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="2fabb-560">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="2fabb-561">Afgang før første løn</span><span class="sxs-lookup"><span data-stu-id="2fabb-561">Departure before first payroll</span></span> | <span data-ttu-id="2fabb-562">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="2fabb-562">Terminate worker</span></span>     |
| <span data-ttu-id="2fabb-563">OPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="2fabb-563">RESIGNATION</span></span>            | <span data-ttu-id="2fabb-564">Opsigelse</span><span class="sxs-lookup"><span data-stu-id="2fabb-564">Resignation</span></span>                    | <span data-ttu-id="2fabb-565">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="2fabb-565">Terminate worker</span></span>     |
| <span data-ttu-id="2fabb-566">PENSION</span><span class="sxs-lookup"><span data-stu-id="2fabb-566">PENSION</span></span>                | <span data-ttu-id="2fabb-567">Pension</span><span class="sxs-lookup"><span data-stu-id="2fabb-567">Pension</span></span>                        | <span data-ttu-id="2fabb-568">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="2fabb-568">Terminate worker</span></span>     |
| <span data-ttu-id="2fabb-569">OPHØR</span><span class="sxs-lookup"><span data-stu-id="2fabb-569">TERMINATION</span></span>            | <span data-ttu-id="2fabb-570">Ophør</span><span class="sxs-lookup"><span data-stu-id="2fabb-570">Termination</span></span>                    | <span data-ttu-id="2fabb-571">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="2fabb-571">Terminate worker</span></span>     |
| <span data-ttu-id="2fabb-572">PENSION</span><span class="sxs-lookup"><span data-stu-id="2fabb-572">RETIREMENT</span></span>             | <span data-ttu-id="2fabb-573">Pension</span><span class="sxs-lookup"><span data-stu-id="2fabb-573">Retirement</span></span>                     | <span data-ttu-id="2fabb-574">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="2fabb-574">Terminate worker</span></span>     |
| <span data-ttu-id="2fabb-575">FRAVÆRENDE</span><span class="sxs-lookup"><span data-stu-id="2fabb-575">ABSENTEE</span></span>               | <span data-ttu-id="2fabb-576">Fraværende</span><span class="sxs-lookup"><span data-stu-id="2fabb-576">Absentee</span></span>                       | <span data-ttu-id="2fabb-577">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="2fabb-577">Terminate worker</span></span>     |
| <span data-ttu-id="2fabb-578">ANDET</span><span class="sxs-lookup"><span data-stu-id="2fabb-578">OTHER</span></span>                  | <span data-ttu-id="2fabb-579">Andre årsager</span><span class="sxs-lookup"><span data-stu-id="2fabb-579">Other Reasons</span></span>                  | <span data-ttu-id="2fabb-580">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="2fabb-580">Terminate worker</span></span>     |
| <span data-ttu-id="2fabb-581">LUKNING</span><span class="sxs-lookup"><span data-stu-id="2fabb-581">CLOSURE</span></span>                | <span data-ttu-id="2fabb-582">Virksomhedslukning</span><span class="sxs-lookup"><span data-stu-id="2fabb-582">Business Closure</span></span>               | <span data-ttu-id="2fabb-583">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="2fabb-583">Terminate worker</span></span>     |
| <span data-ttu-id="2fabb-584">DØDSFALD</span><span class="sxs-lookup"><span data-stu-id="2fabb-584">DEATH</span></span>                  | <span data-ttu-id="2fabb-585">Dødsfald</span><span class="sxs-lookup"><span data-stu-id="2fabb-585">Death</span></span>                          | <span data-ttu-id="2fabb-586">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="2fabb-586">Terminate worker</span></span>     |
| <span data-ttu-id="2fabb-587">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="2fabb-587">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="2fabb-588">Orlov</span><span class="sxs-lookup"><span data-stu-id="2fabb-588">Leave of Absence</span></span>               | <span data-ttu-id="2fabb-589">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="2fabb-589">Terminate worker</span></span>     |
| <span data-ttu-id="2fabb-590">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="2fabb-590">CONTRACTEND</span></span>            | <span data-ttu-id="2fabb-591">Kontraktudløb</span><span class="sxs-lookup"><span data-stu-id="2fabb-591">End of Contract</span></span>                | <span data-ttu-id="2fabb-592">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="2fabb-592">Terminate worker</span></span>     |
| <span data-ttu-id="2fabb-593">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="2fabb-593">SALARYCHANGE</span></span>           | <span data-ttu-id="2fabb-594">Ændring af løn</span><span class="sxs-lookup"><span data-stu-id="2fabb-594">Change of Salary</span></span>               | <span data-ttu-id="2fabb-595">Kompensation</span><span class="sxs-lookup"><span data-stu-id="2fabb-595">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="2fabb-596">Ansættelsesvilkår</span><span class="sxs-lookup"><span data-stu-id="2fabb-596">Terms of employment</span></span>

<span data-ttu-id="2fabb-597">Ansættelsesvilkår bruges til at oprette kategorier for ansættelsesvilkår.</span><span class="sxs-lookup"><span data-stu-id="2fabb-597">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="2fabb-598">Vilkårene knyttes til Dayforce som beskæftigelsesindikatorværdier.</span><span class="sxs-lookup"><span data-stu-id="2fabb-598">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="2fabb-599">Følgende begreber for beskæftigelse og beskrivelser er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="2fabb-599">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="2fabb-600">Ansættelsesvilkår</span><span class="sxs-lookup"><span data-stu-id="2fabb-600">Terms of employment</span></span>   | <span data-ttu-id="2fabb-601">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="2fabb-601">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="2fabb-602">Regulær</span><span class="sxs-lookup"><span data-stu-id="2fabb-602">Regular</span></span>               | <span data-ttu-id="2fabb-603">Regulær</span><span class="sxs-lookup"><span data-stu-id="2fabb-603">Regular</span></span>     |
| <span data-ttu-id="2fabb-604">Direkte</span><span class="sxs-lookup"><span data-stu-id="2fabb-604">Direct</span></span>                | <span data-ttu-id="2fabb-605">Direkte</span><span class="sxs-lookup"><span data-stu-id="2fabb-605">Direct</span></span>      |
| <span data-ttu-id="2fabb-606">Turnustjeneste</span><span class="sxs-lookup"><span data-stu-id="2fabb-606">Internship</span></span>            | <span data-ttu-id="2fabb-607">Turnustjeneste</span><span class="sxs-lookup"><span data-stu-id="2fabb-607">Internship</span></span>  |
| <span data-ttu-id="2fabb-608">Permanent</span><span class="sxs-lookup"><span data-stu-id="2fabb-608">Permanent</span></span>             | <span data-ttu-id="2fabb-609">Permanent</span><span class="sxs-lookup"><span data-stu-id="2fabb-609">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="2fabb-610">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="2fabb-610">Marital status</span></span>

<span data-ttu-id="2fabb-611">Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="2fabb-611">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="2fabb-612">Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2fabb-612">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="2fabb-613">Talent</span><span class="sxs-lookup"><span data-stu-id="2fabb-613">Talent</span></span>                 | <span data-ttu-id="2fabb-614">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2fabb-614">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="2fabb-615">Gift</span><span class="sxs-lookup"><span data-stu-id="2fabb-615">Married</span></span>                | <span data-ttu-id="2fabb-616">Gift</span><span class="sxs-lookup"><span data-stu-id="2fabb-616">Married</span></span>                   |
| <span data-ttu-id="2fabb-617">Enlig</span><span class="sxs-lookup"><span data-stu-id="2fabb-617">Single</span></span>                 | <span data-ttu-id="2fabb-618">Enlig</span><span class="sxs-lookup"><span data-stu-id="2fabb-618">Single</span></span>                    |
| <span data-ttu-id="2fabb-619">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="2fabb-619">Widowed</span></span>                | <span data-ttu-id="2fabb-620">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="2fabb-620">Widowed</span></span>                   |
| <span data-ttu-id="2fabb-621">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="2fabb-621">Divorced</span></span>               | <span data-ttu-id="2fabb-622">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="2fabb-622">Divorced</span></span>                  |
| <span data-ttu-id="2fabb-623">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="2fabb-623">Registered Partnership</span></span> | <span data-ttu-id="2fabb-624">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="2fabb-624">Domestic Partnership</span></span>      |
| <span data-ttu-id="2fabb-625">None</span><span class="sxs-lookup"><span data-stu-id="2fabb-625">None</span></span>                   | <span data-ttu-id="2fabb-626">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="2fabb-626">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="2fabb-627">Samlever</span><span class="sxs-lookup"><span data-stu-id="2fabb-627">Cohabiting</span></span>             | <span data-ttu-id="2fabb-628">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="2fabb-628">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="2fabb-629">Køn</span><span class="sxs-lookup"><span data-stu-id="2fabb-629">Gender</span></span>

<span data-ttu-id="2fabb-630">Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="2fabb-630">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="2fabb-631">Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2fabb-631">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="2fabb-632">Talent</span><span class="sxs-lookup"><span data-stu-id="2fabb-632">Talent</span></span>       | <span data-ttu-id="2fabb-633">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2fabb-633">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="2fabb-634">Mand</span><span class="sxs-lookup"><span data-stu-id="2fabb-634">Male</span></span>         | <span data-ttu-id="2fabb-635">Mand</span><span class="sxs-lookup"><span data-stu-id="2fabb-635">Male</span></span>                      |
| <span data-ttu-id="2fabb-636">Kvinde</span><span class="sxs-lookup"><span data-stu-id="2fabb-636">Female</span></span>       | <span data-ttu-id="2fabb-637">Kvinde</span><span class="sxs-lookup"><span data-stu-id="2fabb-637">Female</span></span>                    |
| <span data-ttu-id="2fabb-638">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="2fabb-638">Non-specific</span></span> | <span data-ttu-id="2fabb-639">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="2fabb-639">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="2fabb-640">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="2fabb-640">Payment method</span></span>

<span data-ttu-id="2fabb-641">Betalingsmetoder giver medarbejderen og virksomheden en måde til at beskrive, hvordan medarbejdere skal betales.</span><span class="sxs-lookup"><span data-stu-id="2fabb-641">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="2fabb-642">Betalingsmåder knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="2fabb-642">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="2fabb-643">Følgende tabel viser, hvordan betalingsmetoder knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2fabb-643">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="2fabb-644">Talent</span><span class="sxs-lookup"><span data-stu-id="2fabb-644">Talent</span></span>             | <span data-ttu-id="2fabb-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2fabb-645">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="2fabb-646">Indløsning</span><span class="sxs-lookup"><span data-stu-id="2fabb-646">Cash</span></span>               | <span data-ttu-id="2fabb-647">Indløsning</span><span class="sxs-lookup"><span data-stu-id="2fabb-647">Cash</span></span>                      |
| <span data-ttu-id="2fabb-648">Elektronisk betaling</span><span class="sxs-lookup"><span data-stu-id="2fabb-648">Electronic Payment</span></span> | <span data-ttu-id="2fabb-649">Ompostering</span><span class="sxs-lookup"><span data-stu-id="2fabb-649">Transfer</span></span>                  |
| <span data-ttu-id="2fabb-650">Check</span><span class="sxs-lookup"><span data-stu-id="2fabb-650">Check</span></span>              | <span data-ttu-id="2fabb-651">Check</span><span class="sxs-lookup"><span data-stu-id="2fabb-651">Cheque</span></span>                    |
| <span data-ttu-id="2fabb-652">Bankanvisning</span><span class="sxs-lookup"><span data-stu-id="2fabb-652">Bank Draft</span></span>         | <span data-ttu-id="2fabb-653">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="2fabb-653">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="2fabb-654">Andre</span><span class="sxs-lookup"><span data-stu-id="2fabb-654">Other</span></span>              | <span data-ttu-id="2fabb-655">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="2fabb-655">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="2fabb-656">Bankkontotype</span><span class="sxs-lookup"><span data-stu-id="2fabb-656">Bank account type</span></span>

<span data-ttu-id="2fabb-657">Bankkontotyper bruges til elektroniske betalinger til medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="2fabb-657">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="2fabb-658">Bankkontotyper knyttes til Dayforce som overførselskontooplysninger.</span><span class="sxs-lookup"><span data-stu-id="2fabb-658">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="2fabb-659">Bankkontotyperne oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="2fabb-659">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="2fabb-660">Talent</span><span class="sxs-lookup"><span data-stu-id="2fabb-660">Talent</span></span>            | <span data-ttu-id="2fabb-661">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2fabb-661">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="2fabb-662">Checkkonto</span><span class="sxs-lookup"><span data-stu-id="2fabb-662">Checking Account</span></span>  | <span data-ttu-id="2fabb-663">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="2fabb-663">CheckingAccount</span></span>           |
| <span data-ttu-id="2fabb-664">Lønkonto</span><span class="sxs-lookup"><span data-stu-id="2fabb-664">Payroll Account</span></span>   | <span data-ttu-id="2fabb-665">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="2fabb-665">PayrollAccount</span></span>            |
| <span data-ttu-id="2fabb-666">Opsparingskonto</span><span class="sxs-lookup"><span data-stu-id="2fabb-666">Savings Account</span></span>   | <span data-ttu-id="2fabb-667">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="2fabb-667">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="2fabb-668">BankGirot-konto</span><span class="sxs-lookup"><span data-stu-id="2fabb-668">BankGirot account</span></span> | <span data-ttu-id="2fabb-669">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="2fabb-669">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="2fabb-670">PlusGirot-konto</span><span class="sxs-lookup"><span data-stu-id="2fabb-670">PlusGirot account</span></span> | <span data-ttu-id="2fabb-671">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="2fabb-671">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="2fabb-672">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="2fabb-672">Earning codes</span></span>

<span data-ttu-id="2fabb-673">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="2fabb-673">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="2fabb-674">Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="2fabb-674">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="2fabb-675">Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="2fabb-675">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="2fabb-676">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="2fabb-676">Supported frequencies</span></span>

- <span data-ttu-id="2fabb-677">Alt</span><span class="sxs-lookup"><span data-stu-id="2fabb-677">All</span></span>
- <span data-ttu-id="2fabb-678">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="2fabb-678">EVERYPAY</span></span>
- <span data-ttu-id="2fabb-679">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="2fabb-679">EACHPAYPERIOD</span></span>
- <span data-ttu-id="2fabb-680">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="2fabb-680">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="2fabb-681">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="2fabb-681">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="2fabb-682">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-682">1OFMTH</span></span>
- <span data-ttu-id="2fabb-683">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-683">LASTOFMTH</span></span>
- <span data-ttu-id="2fabb-684">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-684">2OFMTH</span></span>
- <span data-ttu-id="2fabb-685">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-685">3OFMTH</span></span>
- <span data-ttu-id="2fabb-686">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-686">4OFMTH</span></span>
- <span data-ttu-id="2fabb-687">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-687">5OFMTH</span></span>
- <span data-ttu-id="2fabb-688">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-688">1N2OFMTH</span></span>
- <span data-ttu-id="2fabb-689">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-689">3N4OFMTH</span></span>
- <span data-ttu-id="2fabb-690">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-690">1N3OFMTH</span></span>
- <span data-ttu-id="2fabb-691">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-691">1N4OFMTH</span></span>
- <span data-ttu-id="2fabb-692">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-692">2N3OFMTH</span></span>
- <span data-ttu-id="2fabb-693">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-693">2N4OFMTH</span></span>
- <span data-ttu-id="2fabb-694">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-694">1N2N3OFMTH</span></span>
- <span data-ttu-id="2fabb-695">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-695">1N2N4OFMTH</span></span>
- <span data-ttu-id="2fabb-696">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-696">1N3N4OFMTH</span></span>
- <span data-ttu-id="2fabb-697">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-697">2N3N4OFMTH</span></span>
- <span data-ttu-id="2fabb-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2fabb-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="2fabb-699">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="2fabb-699">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="2fabb-700">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="2fabb-700">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="2fabb-701">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="2fabb-701">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="2fabb-702">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="2fabb-702">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="2fabb-703">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="2fabb-703">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="2fabb-704">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="2fabb-704">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="2fabb-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="2fabb-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="2fabb-706">Adresser</span><span class="sxs-lookup"><span data-stu-id="2fabb-706">Addresses</span></span>

<span data-ttu-id="2fabb-707">Identifikation af specifikke koder for land eller region, stat og område (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende.</span><span class="sxs-lookup"><span data-stu-id="2fabb-707">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="2fabb-708">Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.</span><span class="sxs-lookup"><span data-stu-id="2fabb-708">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="2fabb-709">Talent</span><span class="sxs-lookup"><span data-stu-id="2fabb-709">Talent</span></span>              | <span data-ttu-id="2fabb-710">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2fabb-710">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="2fabb-711">Land/område</span><span class="sxs-lookup"><span data-stu-id="2fabb-711">Country/Region</span></span>      | <span data-ttu-id="2fabb-712">Landekode</span><span class="sxs-lookup"><span data-stu-id="2fabb-712">Country Code</span></span>          |
| <span data-ttu-id="2fabb-713">Postnummer</span><span class="sxs-lookup"><span data-stu-id="2fabb-713">Zip/Postal Code</span></span>     | <span data-ttu-id="2fabb-714">Postnummer</span><span class="sxs-lookup"><span data-stu-id="2fabb-714">Postal Code</span></span>           |
| <span data-ttu-id="2fabb-715">Status</span><span class="sxs-lookup"><span data-stu-id="2fabb-715">State</span></span>               | <span data-ttu-id="2fabb-716">Statskode</span><span class="sxs-lookup"><span data-stu-id="2fabb-716">State Code</span></span>            |
| <span data-ttu-id="2fabb-717">Bynavn</span><span class="sxs-lookup"><span data-stu-id="2fabb-717">City</span></span>                | <span data-ttu-id="2fabb-718">Bynavn</span><span class="sxs-lookup"><span data-stu-id="2fabb-718">City</span></span>                  |
| <span data-ttu-id="2fabb-719">Region</span><span class="sxs-lookup"><span data-stu-id="2fabb-719">County</span></span>              | <span data-ttu-id="2fabb-720">Område (kommune)</span><span class="sxs-lookup"><span data-stu-id="2fabb-720">County (Municipality)</span></span> |
| <span data-ttu-id="2fabb-721">Gade</span><span class="sxs-lookup"><span data-stu-id="2fabb-721">Street</span></span>              | <span data-ttu-id="2fabb-722">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="2fabb-722">Address Line 1</span></span>        |
| <span data-ttu-id="2fabb-723">Gadenummer</span><span class="sxs-lookup"><span data-stu-id="2fabb-723">Street Number</span></span>       | <span data-ttu-id="2fabb-724">Adresselinje 2</span><span class="sxs-lookup"><span data-stu-id="2fabb-724">Address Line 2</span></span>        |
| <span data-ttu-id="2fabb-725">Bygningskomplement</span><span class="sxs-lookup"><span data-stu-id="2fabb-725">Building Complement</span></span> | <span data-ttu-id="2fabb-726">Adresselinje 5</span><span class="sxs-lookup"><span data-stu-id="2fabb-726">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="2fabb-727">Pasnummer</span><span class="sxs-lookup"><span data-stu-id="2fabb-727">Passport number</span></span>

<span data-ttu-id="2fabb-728">Medarbejdere kan erklære pasoplysninger.</span><span class="sxs-lookup"><span data-stu-id="2fabb-728">Employees can declare passport information.</span></span> <span data-ttu-id="2fabb-729">Disse oplysninger er af identifikationstypen **Pas** og er integreret i Dayforce som en del af en medarbejders Mexico-specifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="2fabb-729">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="2fabb-730">Identifikationstype = "Pas"</span><span class="sxs-lookup"><span data-stu-id="2fabb-730">Identification Type = "Passport"</span></span>
- <span data-ttu-id="2fabb-731">Udstedt den</span><span class="sxs-lookup"><span data-stu-id="2fabb-731">Issued Date</span></span>
- <span data-ttu-id="2fabb-732">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="2fabb-732">Expiration Date</span></span>

<span data-ttu-id="2fabb-733">Medarbejdere kan angive flere identifikationsnumre af **Pas**-identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="2fabb-733">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="2fabb-734">Men det er kun den aktuelle aktive paspost, der integreres i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2fabb-734">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="2fabb-735">Hvis alle pasposter er udløbet, integreres det pas, der senest blev udstedt, i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2fabb-735">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
