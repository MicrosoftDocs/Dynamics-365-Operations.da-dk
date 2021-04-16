---
title: Konfigurer integration med Dayforce
description: Integrationen mellem Microsoft Dynamics 365 Human Resources og Ceridian Dayforce er baseret på flere konfigurationstrin, der er beskrevet i dette emne. Du skal konfigurere integrationen i både Human Resources og Dayforce, før du kan behandle en lønkørsel.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bcb57082a49fc07a4139aa37f9507890ca7ed620
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805076"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="151f8-104">Konfigurer integration med Dayforce</span><span class="sxs-lookup"><span data-stu-id="151f8-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="151f8-105">Integrationen mellem Microsoft Dynamics 365 Human Resources og Ceridian Dayforce er baseret på flere konfigurationstrin, der er beskrevet i dette emne.</span><span class="sxs-lookup"><span data-stu-id="151f8-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="151f8-106">Du skal konfigurere integrationen i både Human Resources og Dayforce, før du kan behandle en lønkørsel.</span><span class="sxs-lookup"><span data-stu-id="151f8-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="151f8-107">Når du bruger en tjeneste, f.eks. Dayforce, til at fuldføre lønkørsler, skal du aktivere integrationen i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="151f8-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="151f8-108">Integrationen kræver bestemte data fra Human Resources.</span><span class="sxs-lookup"><span data-stu-id="151f8-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="151f8-109">Du skal derfor kontrollere, at data, der er knyttet til Dayforce, er konfigureret i Human Resources på en måde, der understøtter integrationen.</span><span class="sxs-lookup"><span data-stu-id="151f8-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="151f8-110">Integrationen bruger følgende brede kategorier af data.</span><span class="sxs-lookup"><span data-stu-id="151f8-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="151f8-111">Human Resourcesdata</span><span class="sxs-lookup"><span data-stu-id="151f8-111">Human resources data</span></span>
- <span data-ttu-id="151f8-112">Kompensationsdata</span><span class="sxs-lookup"><span data-stu-id="151f8-112">Compensation data</span></span>
- <span data-ttu-id="151f8-113">Lønoplysninger, f.eks. løncyklusser, betalingsperioder og lønkoder</span><span class="sxs-lookup"><span data-stu-id="151f8-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="151f8-114">Arbejderdata</span><span class="sxs-lookup"><span data-stu-id="151f8-114">Worker data</span></span>

<span data-ttu-id="151f8-115">Denne artikel beskriver de trin, du skal udføre for at aktivere integrationen.</span><span class="sxs-lookup"><span data-stu-id="151f8-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="151f8-116">Det forklarer også typerne af data og oplysninger om konfigurationen, der kræves til integrationen.</span><span class="sxs-lookup"><span data-stu-id="151f8-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="151f8-117">Aktivere integrationen.</span><span class="sxs-lookup"><span data-stu-id="151f8-117">Enable the integration</span></span>

<span data-ttu-id="151f8-118">I Human Resources skal du aktivere integrationen og angive konfigurationsoplysningerne for at oprette forbindelse til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="151f8-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="151f8-119">Hvis den finanspostering, der er oprettet, skal importeres til Microsoft Dynamics 365 Finance, skal du også konfigurere en Microsoft Azure-lagerkonto og angive Azure-lagerets forbindelsesstreng i Finance.</span><span class="sxs-lookup"><span data-stu-id="151f8-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="151f8-120">Følg disse trin for at aktivere integrationen i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="151f8-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="151f8-121">På siden **Systemadministration** skal du vælge **Integrationskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="151f8-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="151f8-122">Angiv det sikre FTP-slutpunkt og den sikre FTP-mappesti.</span><span class="sxs-lookup"><span data-stu-id="151f8-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="151f8-123">Angiv brugernavnet og adgangskoden for den bruger, der skal have adgang til det sikre FTP-slutpunkt og den sikre mappesti.</span><span class="sxs-lookup"><span data-stu-id="151f8-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="151f8-124">Test forbindelsen, som krævet, og angiv indstillingen **Aktivér lønintegration** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="151f8-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="151f8-125">Når integrationen er aktiveret, oprettes dataeksportpakken og -filerne, og hyppigheden angives.</span><span class="sxs-lookup"><span data-stu-id="151f8-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="151f8-126">Du kan ændre denne frekvens efter behov.</span><span class="sxs-lookup"><span data-stu-id="151f8-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="151f8-127">Yderligere oplysninger om Azure-lagerkonti og Azure-lagerforbindelsesstrenge finder du i følgende Azure-artikler:</span><span class="sxs-lookup"><span data-stu-id="151f8-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="151f8-128">Om Azure-lagerkonti</span><span class="sxs-lookup"><span data-stu-id="151f8-128">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="151f8-129">Konfigurere forbindelsesstrenge for Azure-datalager</span><span class="sxs-lookup"><span data-stu-id="151f8-129">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="151f8-130">Tekniske oplysninger ved aktivering af lønintegration</span><span class="sxs-lookup"><span data-stu-id="151f8-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="151f8-131">Aktivering af lønintegration har to primære effekter:</span><span class="sxs-lookup"><span data-stu-id="151f8-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="151f8-132">Der oprettes et dataeksport projekt ved navn "Lønintegrationseksport".</span><span class="sxs-lookup"><span data-stu-id="151f8-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="151f8-133">Dette projekt indeholder de objekter og felter, der kræves til lønintegration.</span><span class="sxs-lookup"><span data-stu-id="151f8-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="151f8-134">Hvis du vil undersøge projektet, skal du gå til **Systemadministration**, vælge feltet **Datastyring** og derefter åbne dataprojektet på listen over projekter.</span><span class="sxs-lookup"><span data-stu-id="151f8-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="151f8-135">Dette batchjob udfører dataeksportprojektet, krypterer den resulterende datapakke og overfører datapakkefilen til det SFTP-slutpunkt, der er konfigureret på skærmen **Integrationskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="151f8-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="151f8-136">Den datapakke, der overføres til SFTP-slutpunktet, krypteres ved hjælp af en nøgle, der er entydig for pakken.</span><span class="sxs-lookup"><span data-stu-id="151f8-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="151f8-137">Nøglen er i en Azure Key Vault, der kun kan åbnes af Ceridian.</span><span class="sxs-lookup"><span data-stu-id="151f8-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="151f8-138">Det er ikke muligt at dekryptere og undersøge datapakkens indhold.</span><span class="sxs-lookup"><span data-stu-id="151f8-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="151f8-139">Hvis du har brug for at undersøge indholdet af datapakken, skal du eksportere dataprojektet "Lønintegrationseksport" manuelt, download det og derefter åbne det.</span><span class="sxs-lookup"><span data-stu-id="151f8-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="151f8-140">Manuel eksport anvender ikke kryptering eller overførsel af pakken.</span><span class="sxs-lookup"><span data-stu-id="151f8-140">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="151f8-141">Konfigurere dine data</span><span class="sxs-lookup"><span data-stu-id="151f8-141">Configure your data</span></span> 

<span data-ttu-id="151f8-142">Hvis du vil behandle løn, skal du konfigurere personaledata i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="151f8-142">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="151f8-143">Du skal angive virksomhedens data, f.eks. job og stillinger, sammen med frynsegoder og kompensationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="151f8-143">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="151f8-144">Disse oplysninger indeholder oplysningerne om ansættelse, løn og fradrag, der kræves for at generere løn for medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="151f8-144">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="151f8-145">Human Resourcesdata</span><span class="sxs-lookup"><span data-stu-id="151f8-145">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="151f8-146">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="151f8-146">Benefits</span></span> 

<span data-ttu-id="151f8-147">Human Resources indeholder en række værktøjer til konfiguration og vedligeholdelse af frynsegoder, fradrag og arbejderkompensationsplaner, som en organisation tilbyder eller behandler for sine ansatte.</span><span class="sxs-lookup"><span data-stu-id="151f8-147">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="151f8-148">Når du opretter frynsegoder, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="151f8-148">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="151f8-149">Frynsegodeplaner</span><span class="sxs-lookup"><span data-stu-id="151f8-149">Benefit plans</span></span>

- <span data-ttu-id="151f8-150">Plan (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-150">Plan (required)</span></span>
- <span data-ttu-id="151f8-151">Type (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-151">Type (required)</span></span>
- <span data-ttu-id="151f8-152">Løneffekt (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-152">Payroll impact (required)</span></span>
- <span data-ttu-id="151f8-153">Opkræv restancer</span><span class="sxs-lookup"><span data-stu-id="151f8-153">Recover arrears</span></span>
- <span data-ttu-id="151f8-154">Fradragsmetode</span><span class="sxs-lookup"><span data-stu-id="151f8-154">Deduction method</span></span>
- <span data-ttu-id="151f8-155">Prioriteret fradrag</span><span class="sxs-lookup"><span data-stu-id="151f8-155">Deduction priority</span></span>
- <span data-ttu-id="151f8-156">Grænseperiode</span><span class="sxs-lookup"><span data-stu-id="151f8-156">Limit period</span></span>
- <span data-ttu-id="151f8-157">Beløb for grænse</span><span class="sxs-lookup"><span data-stu-id="151f8-157">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="151f8-158">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="151f8-158">Benefits</span></span>

- <span data-ttu-id="151f8-159">Plan (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-159">Plan (required)</span></span>
- <span data-ttu-id="151f8-160">Type (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-160">Type (required)</span></span>
- <span data-ttu-id="151f8-161">Mulighed (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-161">Option (required)</span></span>
- <span data-ttu-id="151f8-162">Frynsegode-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-162">Benefit ID (required)</span></span>
- <span data-ttu-id="151f8-163">Frekvens</span><span class="sxs-lookup"><span data-stu-id="151f8-163">Frequency</span></span>
- <span data-ttu-id="151f8-164">Basis</span><span class="sxs-lookup"><span data-stu-id="151f8-164">Basis</span></span>
- <span data-ttu-id="151f8-165">Beløb eller sats</span><span class="sxs-lookup"><span data-stu-id="151f8-165">Amount or rate</span></span>
- <span data-ttu-id="151f8-166">Lønkode</span><span class="sxs-lookup"><span data-stu-id="151f8-166">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="151f8-167">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="151f8-167">Supported frequencies</span></span> 

- <span data-ttu-id="151f8-168">Ugentlig</span><span class="sxs-lookup"><span data-stu-id="151f8-168">Weekly</span></span>
- <span data-ttu-id="151f8-169">Pr. 14 dage</span><span class="sxs-lookup"><span data-stu-id="151f8-169">Bi-weekly</span></span>
- <span data-ttu-id="151f8-170">To gange om måneden</span><span class="sxs-lookup"><span data-stu-id="151f8-170">Semi-monthly</span></span>
- <span data-ttu-id="151f8-171">Månedlig</span><span class="sxs-lookup"><span data-stu-id="151f8-171">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="151f8-172">Understøttede grundlag</span><span class="sxs-lookup"><span data-stu-id="151f8-172">Supported bases</span></span> 

- <span data-ttu-id="151f8-173">Fast beløb</span><span class="sxs-lookup"><span data-stu-id="151f8-173">Fixed amount</span></span>
- <span data-ttu-id="151f8-174">Procentdel af løn</span><span class="sxs-lookup"><span data-stu-id="151f8-174">Percent of earnings</span></span>
- <span data-ttu-id="151f8-175">Produktive timer</span><span class="sxs-lookup"><span data-stu-id="151f8-175">Productive hours</span></span>

<span data-ttu-id="151f8-176">Dayforce opretter følgende fradrag, der er baseret på den løneffekt, der er defineret på frynsegodeplanen.</span><span class="sxs-lookup"><span data-stu-id="151f8-176">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="151f8-177">Valg i Human Resources</span><span class="sxs-lookup"><span data-stu-id="151f8-177">Selection in Human Resources</span></span>        | <span data-ttu-id="151f8-178">Resultat i Dayforce</span><span class="sxs-lookup"><span data-stu-id="151f8-178">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="151f8-179">Ingen</span><span class="sxs-lookup"><span data-stu-id="151f8-179">None</span></span>                       | <span data-ttu-id="151f8-180">Der oprettes ikke noget fradrag.</span><span class="sxs-lookup"><span data-stu-id="151f8-180">No deduction is created.</span></span>                      |
| <span data-ttu-id="151f8-181">Kun fradrag</span><span class="sxs-lookup"><span data-stu-id="151f8-181">Deduction only</span></span>             | <span data-ttu-id="151f8-182">Der oprettes et medarbejderfradrag.</span><span class="sxs-lookup"><span data-stu-id="151f8-182">An employee deduction is created.</span></span>             |
| <span data-ttu-id="151f8-183">Kun bidrag</span><span class="sxs-lookup"><span data-stu-id="151f8-183">Contribution only</span></span>          | <span data-ttu-id="151f8-184">Der oprettes et arbejdsgiverfradrag.</span><span class="sxs-lookup"><span data-stu-id="151f8-184">An employer deduction is created.</span></span>             |
| <span data-ttu-id="151f8-185">Fradrag og bidrag</span><span class="sxs-lookup"><span data-stu-id="151f8-185">Deduction and contribution</span></span> | <span data-ttu-id="151f8-186">Der oprettes medarbejder- og arbejdsgiverfradrag.</span><span class="sxs-lookup"><span data-stu-id="151f8-186">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="151f8-187">Du kan finde flere oplysninger om, hvordan du definerer og administrerer et frynsegodeprogram i følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="151f8-187">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="151f8-188">Levere et frynsegodeprogram for medarbejdere</span><span class="sxs-lookup"><span data-stu-id="151f8-188">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="151f8-189">Opret et nyt frynsegode</span><span class="sxs-lookup"><span data-stu-id="151f8-189">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="151f8-190">Definere regler og politikker for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="151f8-190">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="151f8-191">Tilmelde og fjerne frynsegoder fra arbejdere</span><span class="sxs-lookup"><span data-stu-id="151f8-191">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="151f8-192">Kompensation</span><span class="sxs-lookup"><span data-stu-id="151f8-192">Compensation</span></span> 

<span data-ttu-id="151f8-193">Kompensationsstyring bruges til at styre fordelingen af grundløn og bonusser.</span><span class="sxs-lookup"><span data-stu-id="151f8-193">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="151f8-194">En medarbejders faste grundløn og kvalifikationstillæg styres gennem faste lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="151f8-194">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="151f8-195">Betalingen af incitamentsløn som f.eks. bonusudbetalinger, præstationsbonusser, aktieoptioner og tildelte aktier samt engangsbonusser styres ved hjælp af variable lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="151f8-195">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="151f8-196">Dayforce anvendes kompensationsoplysninger til at beregne en medarbejders timesats eller årlige sats.</span><span class="sxs-lookup"><span data-stu-id="151f8-196">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="151f8-197">Konverteringer af planer for fast løn og lønsats er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="151f8-197">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="151f8-198">Medarbejderne skal være knyttet til en plan for fast løn.</span><span class="sxs-lookup"><span data-stu-id="151f8-198">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="151f8-199">Du kan finde flere oplysninger om kompensationsplaner i følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="151f8-199">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="151f8-200">Oprette planer for fast løn</span><span class="sxs-lookup"><span data-stu-id="151f8-200">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="151f8-201">Oprette planer for variabel kompensation</span><span class="sxs-lookup"><span data-stu-id="151f8-201">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="151f8-202">Udarbejde løn-/kompensationsstruktur og -planer</span><span class="sxs-lookup"><span data-stu-id="151f8-202">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="151f8-203">Proceskompensation</span><span class="sxs-lookup"><span data-stu-id="151f8-203">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="151f8-204">Definere kompensationsproces og beregne resultater</span><span class="sxs-lookup"><span data-stu-id="151f8-204">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="151f8-205">Melde en medarbejder til en fast lønplan</span><span class="sxs-lookup"><span data-stu-id="151f8-205">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="151f8-206">Melde en medarbejder til en variabel lønplan</span><span class="sxs-lookup"><span data-stu-id="151f8-206">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="151f8-207">Job</span><span class="sxs-lookup"><span data-stu-id="151f8-207">Jobs</span></span> 

<span data-ttu-id="151f8-208">Et job er en samling af de opgaver og ansvarsområder, der kræves af en person, der udfører et job.</span><span class="sxs-lookup"><span data-stu-id="151f8-208">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="151f8-209">Du kan finde flere oplysninger i følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="151f8-209">For more information, see the following articles:</span></span>

- [<span data-ttu-id="151f8-210">Konfiguration af komponenter i et job</span><span class="sxs-lookup"><span data-stu-id="151f8-210">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="151f8-211">Definere nye job</span><span class="sxs-lookup"><span data-stu-id="151f8-211">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="151f8-212">Stillinger</span><span class="sxs-lookup"><span data-stu-id="151f8-212">Positions</span></span>

<span data-ttu-id="151f8-213">En stilling er en individuel forekomst af et job.</span><span class="sxs-lookup"><span data-stu-id="151f8-213">A position is an individual instance of a job.</span></span> <span data-ttu-id="151f8-214">For eksempel er stillingen "Salgschef (øst)" én af de stillinger, der er tilknyttet jobbet "Salgschef".</span><span class="sxs-lookup"><span data-stu-id="151f8-214">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="151f8-215">En stilling findes i en afdeling.</span><span class="sxs-lookup"><span data-stu-id="151f8-215">A position exists in a department.</span></span> <span data-ttu-id="151f8-216">Der kan kun knyttes én arbejder til hver stilling.</span><span class="sxs-lookup"><span data-stu-id="151f8-216">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="151f8-217">Hav følgende data og konfiguration i tankerne, når du konfigurerer stillinger:</span><span class="sxs-lookup"><span data-stu-id="151f8-217">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="151f8-218">Stilling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-218">Position (required)</span></span>
- <span data-ttu-id="151f8-219">Beskrivelse (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-219">Description (required)</span></span>
- <span data-ttu-id="151f8-220">Job (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-220">Job (required)</span></span>
- <span data-ttu-id="151f8-221">Afdeling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-221">Department (required)</span></span>
- <span data-ttu-id="151f8-222">Stillingstype (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-222">Position type (required)</span></span>
- <span data-ttu-id="151f8-223">Fuldtidsækvivalent</span><span class="sxs-lookup"><span data-stu-id="151f8-223">Full-time equivalent</span></span>
- <span data-ttu-id="151f8-224">Normaltimer på årsbasis (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-224">Annual regular hours (required)</span></span>
- <span data-ttu-id="151f8-225">Betalt af juridiske enhed (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-225">Paid by legal entity (required)</span></span>
- <span data-ttu-id="151f8-226">Betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-226">Pay cycle (required)</span></span>
- <span data-ttu-id="151f8-227">Økonomisk standarddimension – bærer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-227">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="151f8-228">Arbejdertildeling – arbejder, tildelingsstart, tildelingsslut, årsagskode</span><span class="sxs-lookup"><span data-stu-id="151f8-228">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="151f8-229">Hvis flere stillinger i den samme afdeling er knyttet til samme job, konsolideres de til en enkelt stilling i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="151f8-229">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="151f8-230">Du kan finde flere oplysninger i følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="151f8-230">For more information, see the following articles:</span></span>

- [<span data-ttu-id="151f8-231">Organisere dine medarbejdere ved hjælp af afdelinger, jobs og stillinger</span><span class="sxs-lookup"><span data-stu-id="151f8-231">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="151f8-232">Konfigurere stillinger</span><span class="sxs-lookup"><span data-stu-id="151f8-232">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="151f8-233">Afdelinger</span><span class="sxs-lookup"><span data-stu-id="151f8-233">Departments</span></span>

<span data-ttu-id="151f8-234">En afdeling er en driftsenhed, der repræsenterer en kategori eller et funktionsområde i en organisation.</span><span class="sxs-lookup"><span data-stu-id="151f8-234">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="151f8-235">En afdeling er ansvarlig for et bestemt område i organisationen, såsom salg, regnskab eller personale.</span><span class="sxs-lookup"><span data-stu-id="151f8-235">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="151f8-236">Du kan bruge afdelinger til at rapportere om funktionsområder.</span><span class="sxs-lookup"><span data-stu-id="151f8-236">You can use departments to report on functional areas.</span></span> <span data-ttu-id="151f8-237">Afdelinger kan have ansvar for driftsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="151f8-237">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="151f8-238">Du kan finde flere oplysninger i følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="151f8-238">For more information, see the following articles:</span></span>

- [<span data-ttu-id="151f8-239">Oprette en afdeling og knytte den til afdelingshierarkiet</span><span class="sxs-lookup"><span data-stu-id="151f8-239">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="151f8-240">Definere nye afdelinger</span><span class="sxs-lookup"><span data-stu-id="151f8-240">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="151f8-241">Betalingscyklusser og lønperioder</span><span class="sxs-lookup"><span data-stu-id="151f8-241">Pay cycles and pay periods</span></span>

<span data-ttu-id="151f8-242">En betalingscyklus bestemmer, hvor ofte løn køres,og de specifikke dage, hvor arbejdere betales.</span><span class="sxs-lookup"><span data-stu-id="151f8-242">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="151f8-243">En løncyklus kan f.eks. være månedlig, og medarbejdere betales måske på den sidste dag i måneden.</span><span class="sxs-lookup"><span data-stu-id="151f8-243">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="151f8-244">En løncyklus kan også være ugentligt, og medarbejdere betales måske tirsdag efter slutningen af lønperioden.</span><span class="sxs-lookup"><span data-stu-id="151f8-244">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="151f8-245">Løncyklusser tildeles til stillinger for at styre, hvornår arbejdere i disse stillinger bliver betalt.</span><span class="sxs-lookup"><span data-stu-id="151f8-245">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="151f8-246">Når du opretter betalingscyklusser, kan du generere lønperioder for hver cyklus.</span><span class="sxs-lookup"><span data-stu-id="151f8-246">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="151f8-247">Hver lønperiode omfatter en standardbetalingsdato, der er baseret på oplysninger, du angiver.</span><span class="sxs-lookup"><span data-stu-id="151f8-247">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="151f8-248">Du kan dog redigere standardbetalingsdatoen i en lønperiode til at tillade undtagelser, f.eks. når betalingsdatoen falder på en helligdag.</span><span class="sxs-lookup"><span data-stu-id="151f8-248">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="151f8-249">Følgende oplysninger bruges i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="151f8-249">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="151f8-250">Betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-250">Pay cycle (required)</span></span>
- <span data-ttu-id="151f8-251">Hyppighed for betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-251">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="151f8-252">Periodens startdato (første lønperiode påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-252">Period start date (first pay period required)</span></span>
- <span data-ttu-id="151f8-253">Standardbetalingsdato (første lønperiode påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-253">Default payment date (first pay period required)</span></span>

<span data-ttu-id="151f8-254">Oplysningerne er integreret med Dayforce som løngrupper og adskilles af et land eller område for hver løncyklus.</span><span class="sxs-lookup"><span data-stu-id="151f8-254">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="151f8-255">Mindst én periode skal genereres før integration.</span><span class="sxs-lookup"><span data-stu-id="151f8-255">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="151f8-256">Dayforce genererer løngruppekalendere og betalingsdatoer, der er baseret på startdatoen for den første lønperiode og den standardbetalingsdato, der er angivet i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="151f8-256">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="151f8-257">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="151f8-257">Earning codes</span></span>

<span data-ttu-id="151f8-258">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="151f8-258">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="151f8-259">Koderne har forskellige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="151f8-259">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="151f8-260">Følgende oplysninger bruges i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="151f8-260">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="151f8-261">Lønkode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-261">Earning Code (required)</span></span>
- <span data-ttu-id="151f8-262">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="151f8-262">Description</span></span>
- <span data-ttu-id="151f8-263">Måleenhed</span><span class="sxs-lookup"><span data-stu-id="151f8-263">Unit of measure</span></span>
- <span data-ttu-id="151f8-264">Produktiv</span><span class="sxs-lookup"><span data-stu-id="151f8-264">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="151f8-265">Arbejderdata</span><span class="sxs-lookup"><span data-stu-id="151f8-265">Worker data</span></span>

<span data-ttu-id="151f8-266">Posterne for de forskellige typer arbejdere, du beskæftiger, er vigtige for dine personale- og lønsystemer.</span><span class="sxs-lookup"><span data-stu-id="151f8-266">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="151f8-267">De oplysninger, du angiver, kan bruges til at spore arbejdere og personoplysninger.</span><span class="sxs-lookup"><span data-stu-id="151f8-267">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="151f8-268">Du kan vedligeholde følgende oplysninger for arbejdere:</span><span class="sxs-lookup"><span data-stu-id="151f8-268">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="151f8-269">**Basis** – Vedligehold grundlæggende oplysninger om en arbejder, f.eks. kontaktoplysninger, demografiske oplysninger, identifikationsoplysninger, oplysninger om familie, status for militærtjeneste, oplysninger om udstationering og personlige kontaktpersoner og kontaktpersoner i nødsituationer.</span><span class="sxs-lookup"><span data-stu-id="151f8-269">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="151f8-270">**Beskæftigelse** – Vedligehold oplysninger om en arbejders beskæftigelse, f.eks. firma- eller organisationstilhørsforhold, stillingstildeling, start- og slutdatoer, arbejdstilladelse, vilkår for ansættelse, pension, ferie og flytteoplysninger.</span><span class="sxs-lookup"><span data-stu-id="151f8-270">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="151f8-271">**Orlov og fravær** – Vedligehold oplysninger om en arbejders fravær, f.eks. arbejdskalendere, fraværstransaktioner og fraværsopsætning.</span><span class="sxs-lookup"><span data-stu-id="151f8-271">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="151f8-272">**Kompensation og løn** – Vedligehold oplysninger om en arbejders kompensationsplaner og lønoplysninger, f.eks. tilmelding til planer, priser, ydeevne, provision, skatteoplysninger, pensionering og skattefradrag.</span><span class="sxs-lookup"><span data-stu-id="151f8-272">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="151f8-273">Når du angiver arbejderoplysninger, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="151f8-273">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="151f8-274">Generelle oplysninger</span><span class="sxs-lookup"><span data-stu-id="151f8-274">General information</span></span>

- <span data-ttu-id="151f8-275">Personalenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-275">Personnel number (required)</span></span>
- <span data-ttu-id="151f8-276">Fornavn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-276">First name (required)</span></span>
- <span data-ttu-id="151f8-277">Efternavn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-277">Last name (required)</span></span>
- <span data-ttu-id="151f8-278">Mellemnavn</span><span class="sxs-lookup"><span data-stu-id="151f8-278">Middle name</span></span>
- <span data-ttu-id="151f8-279">Anciennitetsdato</span><span class="sxs-lookup"><span data-stu-id="151f8-279">Seniority date</span></span>
- <span data-ttu-id="151f8-280">Kendt som</span><span class="sxs-lookup"><span data-stu-id="151f8-280">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="151f8-281">Personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="151f8-281">Personal information</span></span>

- <span data-ttu-id="151f8-282">Ægteskabelig status (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-282">Marital status (required)</span></span>
- <span data-ttu-id="151f8-283">Fødselsdato (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-283">Birth date (required)</span></span>
- <span data-ttu-id="151f8-284">Køn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-284">Gender (required)</span></span>
- <span data-ttu-id="151f8-285">Handicappet</span><span class="sxs-lookup"><span data-stu-id="151f8-285">Person with disabilities</span></span>
- <span data-ttu-id="151f8-286">Land eller område for nationalitet (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="151f8-286">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="151f8-287">Adresseoplysninger</span><span class="sxs-lookup"><span data-stu-id="151f8-287">Address information</span></span>

- <span data-ttu-id="151f8-288">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-288">Primary (required)</span></span>
- <span data-ttu-id="151f8-289">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-289">Country/region (required)</span></span>
- <span data-ttu-id="151f8-290">Postnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-290">Postal code (required)</span></span>
- <span data-ttu-id="151f8-291">Gadenummer (påkrævet) (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="151f8-291">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="151f8-292">Bygningskomplement (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="151f8-292">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="151f8-293">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-293">City (required)</span></span>
- <span data-ttu-id="151f8-294">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-294">State (required)</span></span>
- <span data-ttu-id="151f8-295">Region (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-295">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="151f8-296">Kontaktoplysninger</span><span class="sxs-lookup"><span data-stu-id="151f8-296">Contact information</span></span> 

- <span data-ttu-id="151f8-297">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-297">Primary (required)</span></span>
- <span data-ttu-id="151f8-298">Kontaktpersonens nummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-298">Contact number (required)</span></span>
- <span data-ttu-id="151f8-299">Forlængelse</span><span class="sxs-lookup"><span data-stu-id="151f8-299">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="151f8-300">Lønoplysninger og lønkoder</span><span class="sxs-lookup"><span data-stu-id="151f8-300">Payroll information and earning codes</span></span>

<span data-ttu-id="151f8-301">Medarbejdere kan tildeles en bestemt løn med en given betalingshyppighed og have en foretrukken betalingsmetode.</span><span class="sxs-lookup"><span data-stu-id="151f8-301">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="151f8-302">Følgende felter bruges i Dayforce til at sikre, at disse præferencer og indstillinger bruges.</span><span class="sxs-lookup"><span data-stu-id="151f8-302">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="151f8-303">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="151f8-303">Earning codes</span></span>

- <span data-ttu-id="151f8-304">Stilling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-304">Position (required)</span></span>
- <span data-ttu-id="151f8-305">Lønkode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-305">Earning Code (required)</span></span>
- <span data-ttu-id="151f8-306">Frekvens (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-306">Frequency (required)</span></span>
- <span data-ttu-id="151f8-307">Beløb (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-307">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="151f8-308">Lønoplysninger</span><span class="sxs-lookup"><span data-stu-id="151f8-308">Payroll information</span></span>

- <span data-ttu-id="151f8-309">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="151f8-309">Payment Method</span></span>
- <span data-ttu-id="151f8-310">Økonomisk område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-310">Economic Region (required)</span></span>
- <span data-ttu-id="151f8-311">Id for medarbejderfrynsegoder</span><span class="sxs-lookup"><span data-stu-id="151f8-311">Employee Benefits ID</span></span>
- <span data-ttu-id="151f8-312">Nationalt id-nummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-312">National ID Number (required)</span></span>
- <span data-ttu-id="151f8-313">Tjenestenummer hos militær</span><span class="sxs-lookup"><span data-stu-id="151f8-313">Military Service Number</span></span>
- <span data-ttu-id="151f8-314">Skifte-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-314">Shift ID (required)</span></span>
- <span data-ttu-id="151f8-315">Skattenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-315">Tax Number (required)</span></span>
- <span data-ttu-id="151f8-316">Fagforenings-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-316">Union ID (required)</span></span>
- <span data-ttu-id="151f8-317">Arbejdsdags-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-317">Work Day ID (required)</span></span>
- <span data-ttu-id="151f8-318">Arbejdstilladelsesnummer</span><span class="sxs-lookup"><span data-stu-id="151f8-318">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="151f8-319">For betalingsmetoden understøtter Mexico **Kontant**, **Check** (firmaets fysiske check), og **Elektronisk betaling**.</span><span class="sxs-lookup"><span data-stu-id="151f8-319">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="151f8-320">Hvis der ikke er angivet nogen betalingsmetode, bruges **Check** som standard.</span><span class="sxs-lookup"><span data-stu-id="151f8-320">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="151f8-321">Detaljer om ansættelse</span><span class="sxs-lookup"><span data-stu-id="151f8-321">Employment details</span></span>

<span data-ttu-id="151f8-322">Detaljeret ansættelseshistorik bruges som vigtige oplysninger til at udlede statusser for en medarbejders ansættelse, fratrædelse og genansættelse i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="151f8-322">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="151f8-323">Dayforce understøtter kun én aktiv ansættelsespost ad gangen.</span><span class="sxs-lookup"><span data-stu-id="151f8-323">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="151f8-324">Startdato for ansættelse (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-324">Employment start date (required)</span></span>
- <span data-ttu-id="151f8-325">Slutdato for ansættelse</span><span class="sxs-lookup"><span data-stu-id="151f8-325">Employment end date</span></span>
- <span data-ttu-id="151f8-326">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="151f8-326">Start date</span></span>
- <span data-ttu-id="151f8-327">Justeret startdato</span><span class="sxs-lookup"><span data-stu-id="151f8-327">Adjusted start date</span></span>
- <span data-ttu-id="151f8-328">Fratrædelsesdato (kræves ved fratrædelse)</span><span class="sxs-lookup"><span data-stu-id="151f8-328">Termination date (required upon termination)</span></span>
- <span data-ttu-id="151f8-329">Fratrædelsesårsag (kræves ved fratrædelse)</span><span class="sxs-lookup"><span data-stu-id="151f8-329">Termination reason (required upon termination)</span></span>

<span data-ttu-id="151f8-330">Vigtige datoer for en medarbejders udledes ved hjælp af følgende oplysninger.</span><span class="sxs-lookup"><span data-stu-id="151f8-330">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="151f8-331">Human Resources</span><span class="sxs-lookup"><span data-stu-id="151f8-331">Human Resources</span></span>                | <span data-ttu-id="151f8-332">Dayforce</span><span class="sxs-lookup"><span data-stu-id="151f8-332">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="151f8-333">Den seneste ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="151f8-333">Most recent hire date</span></span> | <span data-ttu-id="151f8-334">Historikpost for ansættelsesstart for aktuel ikke-afsluttet ansættelse</span><span class="sxs-lookup"><span data-stu-id="151f8-334">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="151f8-335">Fratrædelsesdato</span><span class="sxs-lookup"><span data-stu-id="151f8-335">Termination date</span></span>      | <span data-ttu-id="151f8-336">Historikpost for fratrædelsesdato for aktuel ikke-afsluttet ansættelse</span><span class="sxs-lookup"><span data-stu-id="151f8-336">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="151f8-337">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="151f8-337">Start date</span></span>            | <span data-ttu-id="151f8-338">Historikpost for justeret startdato, startdato eller startdato for ansættelse for aktuel ikke-aktiv ansættelse</span><span class="sxs-lookup"><span data-stu-id="151f8-338">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="151f8-339">Oprindelig ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="151f8-339">Original hire date</span></span>    | <span data-ttu-id="151f8-340">Historikpost for ansættelsesstart for tidligste ansættelse</span><span class="sxs-lookup"><span data-stu-id="151f8-340">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="151f8-341">Kompensation</span><span class="sxs-lookup"><span data-stu-id="151f8-341">Compensation</span></span>

<span data-ttu-id="151f8-342">En fast lønstruktur skal tilknyttes hver medarbejders primære stilling gennem hele ansættelsesperioden.</span><span class="sxs-lookup"><span data-stu-id="151f8-342">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="151f8-343">Denne periode starter på den dato, hvor medarbejderen blev ansat (eller ansættelsesstartdatoen) og fortsætter, indtil fratrædelsen.</span><span class="sxs-lookup"><span data-stu-id="151f8-343">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="151f8-344">Ikrafttrædelsesdato (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-344">Effective Date (required)</span></span>
- <span data-ttu-id="151f8-345">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="151f8-345">Expiration date</span></span>
- <span data-ttu-id="151f8-346">Lønsats (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-346">Pay Rate (required)</span></span>
- <span data-ttu-id="151f8-347">Konverteringer af lønsats (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-347">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="151f8-348">Årlig ækvivalent (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-348">Annual equivalent (required)</span></span>
- <span data-ttu-id="151f8-349">Timebaseret ækvivalent (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-349">Hourly equivalent (required)</span></span>

<span data-ttu-id="151f8-350">Hvis en timeansat medarbejder har flere stillinger, indlæses den faste løn for den primære stilling i Dayforce, som basissats/-løn på medarbejderniveau.</span><span class="sxs-lookup"><span data-stu-id="151f8-350">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="151f8-351">For ikke-primære stillinger gemmes timesatsen i den tilsvarende position i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="151f8-351">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="151f8-352">Hvis en funktionær har flere stillinger, afledes den kumulative timesats og årlig gage på tværs af alle aktive stillinger og bruges som basissats/-gage på medarbejderniveau.</span><span class="sxs-lookup"><span data-stu-id="151f8-352">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="151f8-353">Identifikationsnumre</span><span class="sxs-lookup"><span data-stu-id="151f8-353">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="151f8-354">Social Security-identifikator</span><span class="sxs-lookup"><span data-stu-id="151f8-354">Social Security identifier</span></span> 

<span data-ttu-id="151f8-355">Alle medarbejdere skal have én primær identifikator.</span><span class="sxs-lookup"><span data-stu-id="151f8-355">Every employee must have one primary identifier.</span></span> <span data-ttu-id="151f8-356">Identifikatoren skal være af **SSN**-identifikationstypen</span><span class="sxs-lookup"><span data-stu-id="151f8-356">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="151f8-357">I Dayforce afledes den automatisk som medarbejderens Social Security-identifikator, der er påkrævet ved ansættelse.</span><span class="sxs-lookup"><span data-stu-id="151f8-357">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="151f8-358">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-358">Primary (required)</span></span>
- <span data-ttu-id="151f8-359">Identifikationstype = "SSN"</span><span class="sxs-lookup"><span data-stu-id="151f8-359">Identification Type = "SSN"</span></span>
- <span data-ttu-id="151f8-360">Udstedt den</span><span class="sxs-lookup"><span data-stu-id="151f8-360">Issued Date</span></span>
- <span data-ttu-id="151f8-361">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="151f8-361">Expiration Date</span></span>

<span data-ttu-id="151f8-362">Medarbejdere kan angive flere identifikationsnumre af **SSN**-identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="151f8-362">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="151f8-363">Men det er kun den post, der er markeret som **Primær**, som er integreret i Dayforce, uanset om nummeret er aktivt eller udløbet.</span><span class="sxs-lookup"><span data-stu-id="151f8-363">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="151f8-364">Bankkonto og udbetalinger</span><span class="sxs-lookup"><span data-stu-id="151f8-364">Bank accounts and disbursements</span></span>

<span data-ttu-id="151f8-365">Gyldige bankkontooplysninger skal angives for enhver medarbejder, der vælger at blive betalt via bankkontooverførsler.</span><span class="sxs-lookup"><span data-stu-id="151f8-365">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="151f8-366">Human Resources</span><span class="sxs-lookup"><span data-stu-id="151f8-366">Human Resources</span></span>                         | <span data-ttu-id="151f8-367">Dayforce</span><span class="sxs-lookup"><span data-stu-id="151f8-367">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="151f8-368">Bankkontonummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-368">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="151f8-369">SWIFT-kode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-369">SWIFT code (required)</span></span>          | <span data-ttu-id="151f8-370">Feltet **Bank-id** bruges ved behandling af løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="151f8-370">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="151f8-371">Afdelingsnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-371">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="151f8-372">Bankkontotype (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-372">Bank account type (required)</span></span>   | <span data-ttu-id="151f8-373">Feltet **Kontotype** bruges ved behandling af løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="151f8-373">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="151f8-374">Understøttede værdier omfatter **Check** og **Løn**.</span><span class="sxs-lookup"><span data-stu-id="151f8-374">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="151f8-375">Medarbejdere, der vælger at betales via bankkontooverførsler, skal angive et link til en restbeløbskonto, der hører under en juridisk enhed, som har primær adresse i Mexico og er knyttet til en gyldig bankkonto fra en mexicansk bank.</span><span class="sxs-lookup"><span data-stu-id="151f8-375">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="151f8-376">Alle andre restbeløbskonti ignoreres.</span><span class="sxs-lookup"><span data-stu-id="151f8-376">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="151f8-377">Adresseoplysninger</span><span class="sxs-lookup"><span data-stu-id="151f8-377">Address information</span></span>

<span data-ttu-id="151f8-378">Alle medarbejdere skal have én primær placering.</span><span class="sxs-lookup"><span data-stu-id="151f8-378">Every employee must have one primary location.</span></span> <span data-ttu-id="151f8-379">I Dayforce bruges denne placering til at bestemme medarbejderens primære opholdssted til skattemæssige formål.</span><span class="sxs-lookup"><span data-stu-id="151f8-379">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="151f8-380">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-380">Primary (required)</span></span>
- <span data-ttu-id="151f8-381">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-381">Country/region (required)</span></span>
- <span data-ttu-id="151f8-382">Postnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-382">Zip/postal code (required)</span></span>
- <span data-ttu-id="151f8-383">Gade (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-383">Street (required)</span></span>
- <span data-ttu-id="151f8-384">Gadenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-384">Street Number (required)</span></span>
- <span data-ttu-id="151f8-385">Bygningskomplement</span><span class="sxs-lookup"><span data-stu-id="151f8-385">Building Complement</span></span>
- <span data-ttu-id="151f8-386">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-386">City (required)</span></span>
- <span data-ttu-id="151f8-387">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-387">State (required)</span></span>
- <span data-ttu-id="151f8-388">Region (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-388">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="151f8-389">Konfigurere dataene for at generere løn i USA og Canada</span><span class="sxs-lookup"><span data-stu-id="151f8-389">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="151f8-390">Hvis du genererer løn for medarbejdere i USA og Canada, skal følgende elementer konfigureres:</span><span class="sxs-lookup"><span data-stu-id="151f8-390">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="151f8-391">Der kræves afdelinger til stillinger.</span><span class="sxs-lookup"><span data-stu-id="151f8-391">Departments are required on positions.</span></span>
- <span data-ttu-id="151f8-392">Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="151f8-392">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="151f8-393">Du kan konfigurere Human Resources til at kræve, at der angives en afdeling for stillinger.</span><span class="sxs-lookup"><span data-stu-id="151f8-393">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="151f8-394">For at gøre dette skal du gå til **Human Resourcests delte stillinger > Stillinger > Kræv afdelinger for stillinger**.</span><span class="sxs-lookup"><span data-stu-id="151f8-394">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="151f8-395">Det anbefales, at denne indstilling gennemtvinges i forbindelse med integrationen.</span><span class="sxs-lookup"><span data-stu-id="151f8-395">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="151f8-396">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="151f8-396">Job types</span></span>

<span data-ttu-id="151f8-397">Jobtyper bruges til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="151f8-397">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="151f8-398">Jobtyper kræves for at behandle løn i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="151f8-398">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="151f8-399">Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="151f8-399">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="151f8-400">Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.</span><span class="sxs-lookup"><span data-stu-id="151f8-400">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="151f8-401">Der kræves følgende jobtyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="151f8-401">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="151f8-402">Jobtype</span><span class="sxs-lookup"><span data-stu-id="151f8-402">Job type</span></span>   | <span data-ttu-id="151f8-403">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="151f8-403">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="151f8-404">Pr. time</span><span class="sxs-lookup"><span data-stu-id="151f8-404">Hourly</span></span>     | <span data-ttu-id="151f8-405">Pr. time</span><span class="sxs-lookup"><span data-stu-id="151f8-405">Hourly</span></span>      |
| <span data-ttu-id="151f8-406">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="151f8-406">Salaried</span></span>   | <span data-ttu-id="151f8-407">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="151f8-407">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="151f8-408">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="151f8-408">Position types</span></span> 

<span data-ttu-id="151f8-409">Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet.</span><span class="sxs-lookup"><span data-stu-id="151f8-409">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="151f8-410">Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="151f8-410">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="151f8-411">Der kræves følgende stillingstyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="151f8-411">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="151f8-412">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="151f8-412">Position type</span></span>   | <span data-ttu-id="151f8-413">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="151f8-413">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="151f8-414">Fuld tid</span><span class="sxs-lookup"><span data-stu-id="151f8-414">Full-time</span></span>       | <span data-ttu-id="151f8-415">Fuldtidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="151f8-415">Full time employee</span></span> |
| <span data-ttu-id="151f8-416">Deltid</span><span class="sxs-lookup"><span data-stu-id="151f8-416">Part-time</span></span>       | <span data-ttu-id="151f8-417">Deltidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="151f8-417">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="151f8-418">Årsagskoder</span><span class="sxs-lookup"><span data-stu-id="151f8-418">Reason codes</span></span>

<span data-ttu-id="151f8-419">Årsagskoder indeholder oplysninger om status for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="151f8-419">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="151f8-420">Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.</span><span class="sxs-lookup"><span data-stu-id="151f8-420">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="151f8-421">Der kræves følgende årsagskoder og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="151f8-421">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="151f8-422">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="151f8-422">Reason code</span></span>    | <span data-ttu-id="151f8-423">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="151f8-423">Description</span></span>      | <span data-ttu-id="151f8-424">Anvendelige scenarier</span><span class="sxs-lookup"><span data-stu-id="151f8-424">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="151f8-425">OPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="151f8-425">RESIGNATION</span></span>    | <span data-ttu-id="151f8-426">Opsigelse</span><span class="sxs-lookup"><span data-stu-id="151f8-426">Resignation</span></span>      | <span data-ttu-id="151f8-427">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="151f8-427">Terminate worker</span></span>     |
| <span data-ttu-id="151f8-428">OPHØR</span><span class="sxs-lookup"><span data-stu-id="151f8-428">TERMINATION</span></span>    | <span data-ttu-id="151f8-429">Ophør</span><span class="sxs-lookup"><span data-stu-id="151f8-429">Termination</span></span>      | <span data-ttu-id="151f8-430">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="151f8-430">Terminate worker</span></span>     |
| <span data-ttu-id="151f8-431">PENSION</span><span class="sxs-lookup"><span data-stu-id="151f8-431">RETIREMENT</span></span>     | <span data-ttu-id="151f8-432">Pension</span><span class="sxs-lookup"><span data-stu-id="151f8-432">Retirement</span></span>       | <span data-ttu-id="151f8-433">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="151f8-433">Terminate worker</span></span>     |
| <span data-ttu-id="151f8-434">ANDET</span><span class="sxs-lookup"><span data-stu-id="151f8-434">OTHER</span></span>          | <span data-ttu-id="151f8-435">Andre årsager</span><span class="sxs-lookup"><span data-stu-id="151f8-435">Other Reasons</span></span>    | <span data-ttu-id="151f8-436">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="151f8-436">Terminate worker</span></span>     |
| <span data-ttu-id="151f8-437">DØDSFALD</span><span class="sxs-lookup"><span data-stu-id="151f8-437">DEATH</span></span>          | <span data-ttu-id="151f8-438">Dødsfald</span><span class="sxs-lookup"><span data-stu-id="151f8-438">Death</span></span>            | <span data-ttu-id="151f8-439">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="151f8-439">Terminate worker</span></span>     |
| <span data-ttu-id="151f8-440">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="151f8-440">LEAVEOFABSENCE</span></span> | <span data-ttu-id="151f8-441">Orlov</span><span class="sxs-lookup"><span data-stu-id="151f8-441">Leave of Absence</span></span> | <span data-ttu-id="151f8-442">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="151f8-442">Terminate worker</span></span>     |
| <span data-ttu-id="151f8-443">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="151f8-443">CONTRACTEND</span></span>    | <span data-ttu-id="151f8-444">Kontraktudløb</span><span class="sxs-lookup"><span data-stu-id="151f8-444">End of Contract</span></span>  | <span data-ttu-id="151f8-445">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="151f8-445">Terminate worker</span></span>     |
| <span data-ttu-id="151f8-446">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="151f8-446">SALARYCHANGE</span></span>   | <span data-ttu-id="151f8-447">Ændring af løn</span><span class="sxs-lookup"><span data-stu-id="151f8-447">Change of Salary</span></span> | <span data-ttu-id="151f8-448">Kompensation</span><span class="sxs-lookup"><span data-stu-id="151f8-448">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="151f8-449">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="151f8-449">Marital status</span></span>

<span data-ttu-id="151f8-450">Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="151f8-450">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="151f8-451">Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="151f8-451">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="151f8-452">Human Resources</span><span class="sxs-lookup"><span data-stu-id="151f8-452">Human Resources</span></span>                 | <span data-ttu-id="151f8-453">Dayforce</span><span class="sxs-lookup"><span data-stu-id="151f8-453">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="151f8-454">Gift</span><span class="sxs-lookup"><span data-stu-id="151f8-454">Married</span></span>                | <span data-ttu-id="151f8-455">Gift</span><span class="sxs-lookup"><span data-stu-id="151f8-455">Married</span></span>              |
| <span data-ttu-id="151f8-456">Enlig</span><span class="sxs-lookup"><span data-stu-id="151f8-456">Single</span></span>                 | <span data-ttu-id="151f8-457">Enlig</span><span class="sxs-lookup"><span data-stu-id="151f8-457">Single</span></span>               |
| <span data-ttu-id="151f8-458">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="151f8-458">Widowed</span></span>                | <span data-ttu-id="151f8-459">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="151f8-459">Widowed</span></span>              |
| <span data-ttu-id="151f8-460">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="151f8-460">Divorced</span></span>               | <span data-ttu-id="151f8-461">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="151f8-461">Divorced</span></span>             |
| <span data-ttu-id="151f8-462">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="151f8-462">Registered Partnership</span></span> | <span data-ttu-id="151f8-463">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="151f8-463">Domestic Partnership</span></span> |
| <span data-ttu-id="151f8-464">None</span><span class="sxs-lookup"><span data-stu-id="151f8-464">None</span></span>                   | <span data-ttu-id="151f8-465">None</span><span class="sxs-lookup"><span data-stu-id="151f8-465">None</span></span>                 |
| <span data-ttu-id="151f8-466">Samlever</span><span class="sxs-lookup"><span data-stu-id="151f8-466">Cohabiting</span></span>             | <span data-ttu-id="151f8-467">Samlever</span><span class="sxs-lookup"><span data-stu-id="151f8-467">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="151f8-468">Køn</span><span class="sxs-lookup"><span data-stu-id="151f8-468">Gender</span></span>

<span data-ttu-id="151f8-469">Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="151f8-469">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="151f8-470">Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="151f8-470">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="151f8-471">Human Resources</span><span class="sxs-lookup"><span data-stu-id="151f8-471">Human Resources</span></span>       | <span data-ttu-id="151f8-472">Dayforce</span><span class="sxs-lookup"><span data-stu-id="151f8-472">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="151f8-473">Mand</span><span class="sxs-lookup"><span data-stu-id="151f8-473">Male</span></span>         | <span data-ttu-id="151f8-474">Mand</span><span class="sxs-lookup"><span data-stu-id="151f8-474">Male</span></span>            |
| <span data-ttu-id="151f8-475">Kvinde</span><span class="sxs-lookup"><span data-stu-id="151f8-475">Female</span></span>       | <span data-ttu-id="151f8-476">Kvinde</span><span class="sxs-lookup"><span data-stu-id="151f8-476">Female</span></span>          |
| <span data-ttu-id="151f8-477">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="151f8-477">Non-specific</span></span> | <span data-ttu-id="151f8-478">*Understøttes ikke*</span><span class="sxs-lookup"><span data-stu-id="151f8-478">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="151f8-479">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="151f8-479">Earning codes</span></span>

<span data-ttu-id="151f8-480">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="151f8-480">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="151f8-481">Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="151f8-481">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="151f8-482">Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="151f8-482">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="151f8-483">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="151f8-483">Supported frequencies</span></span>

- <span data-ttu-id="151f8-484">Alt</span><span class="sxs-lookup"><span data-stu-id="151f8-484">All</span></span>
- <span data-ttu-id="151f8-485">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="151f8-485">EVERYPAY</span></span>
- <span data-ttu-id="151f8-486">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="151f8-486">EACHPAYPERIOD</span></span>
- <span data-ttu-id="151f8-487">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="151f8-487">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="151f8-488">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="151f8-488">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="151f8-489">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-489">1OFMTH</span></span>
- <span data-ttu-id="151f8-490">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-490">LASTOFMTH</span></span>
- <span data-ttu-id="151f8-491">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-491">2OFMTH</span></span>
- <span data-ttu-id="151f8-492">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-492">3OFMTH</span></span>
- <span data-ttu-id="151f8-493">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-493">4OFMTH</span></span>
- <span data-ttu-id="151f8-494">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-494">5OFMTH</span></span>
- <span data-ttu-id="151f8-495">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-495">1N2OFMTH</span></span>
- <span data-ttu-id="151f8-496">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-496">3N4OFMTH</span></span>
- <span data-ttu-id="151f8-497">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-497">1N3OFMTH</span></span>
- <span data-ttu-id="151f8-498">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-498">1N4OFMTH</span></span>
- <span data-ttu-id="151f8-499">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-499">2N3OFMTH</span></span>
- <span data-ttu-id="151f8-500">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-500">2N4OFMTH</span></span>
- <span data-ttu-id="151f8-501">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-501">1N2N3OFMTH</span></span>
- <span data-ttu-id="151f8-502">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-502">1N2N4OFMTH</span></span>
- <span data-ttu-id="151f8-503">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-503">1N3N4OFMTH</span></span>
- <span data-ttu-id="151f8-504">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-504">2N3N4OFMTH</span></span>
- <span data-ttu-id="151f8-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="151f8-506">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="151f8-506">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="151f8-507">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="151f8-507">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="151f8-508">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="151f8-508">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="151f8-509">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="151f8-509">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="151f8-510">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="151f8-510">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="151f8-511">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="151f8-511">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="151f8-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="151f8-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="151f8-513">Adresser</span><span class="sxs-lookup"><span data-stu-id="151f8-513">Addresses</span></span>

<span data-ttu-id="151f8-514">Identifikation af specifikke koder for land eller område, stat og region (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende.</span><span class="sxs-lookup"><span data-stu-id="151f8-514">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="151f8-515">Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.</span><span class="sxs-lookup"><span data-stu-id="151f8-515">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="151f8-516">Human Resources</span><span class="sxs-lookup"><span data-stu-id="151f8-516">Human Resources</span></span>          | <span data-ttu-id="151f8-517">Dayforce</span><span class="sxs-lookup"><span data-stu-id="151f8-517">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="151f8-518">Land/område</span><span class="sxs-lookup"><span data-stu-id="151f8-518">Country/Region</span></span>  | <span data-ttu-id="151f8-519">Landekode</span><span class="sxs-lookup"><span data-stu-id="151f8-519">Country Code</span></span>          |
| <span data-ttu-id="151f8-520">Postnummer</span><span class="sxs-lookup"><span data-stu-id="151f8-520">Zip/Postal Code</span></span> | <span data-ttu-id="151f8-521">Postnummer</span><span class="sxs-lookup"><span data-stu-id="151f8-521">Postal Code</span></span>           |
| <span data-ttu-id="151f8-522">Status</span><span class="sxs-lookup"><span data-stu-id="151f8-522">State</span></span>           | <span data-ttu-id="151f8-523">Statskode</span><span class="sxs-lookup"><span data-stu-id="151f8-523">State Code</span></span>            |
| <span data-ttu-id="151f8-524">Bynavn</span><span class="sxs-lookup"><span data-stu-id="151f8-524">City</span></span>            | <span data-ttu-id="151f8-525">Bynavn</span><span class="sxs-lookup"><span data-stu-id="151f8-525">City</span></span>                  |
| <span data-ttu-id="151f8-526">Region</span><span class="sxs-lookup"><span data-stu-id="151f8-526">County</span></span>          | <span data-ttu-id="151f8-527">Område (kommune)</span><span class="sxs-lookup"><span data-stu-id="151f8-527">County (Municipality)</span></span> |
| <span data-ttu-id="151f8-528">Gade</span><span class="sxs-lookup"><span data-stu-id="151f8-528">Street</span></span>          | <span data-ttu-id="151f8-529">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="151f8-529">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="151f8-530">Skatteområder</span><span class="sxs-lookup"><span data-stu-id="151f8-530">Tax regions</span></span>

<span data-ttu-id="151f8-531">Skatteområder bruges til at bestemme den relevante skat, der skal anvendes ved løngenerering.</span><span class="sxs-lookup"><span data-stu-id="151f8-531">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="151f8-532">Skatteområder er tilknyttet Dayforce som placeringsadresser.</span><span class="sxs-lookup"><span data-stu-id="151f8-532">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="151f8-533">Standardskatteområder skal knyttes til arbejderens aktive stilling.</span><span class="sxs-lookup"><span data-stu-id="151f8-533">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="151f8-534">Skatteområde (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-534">Tax region (required)</span></span>
- <span data-ttu-id="151f8-535">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-535">Country/Region (required)</span></span>
- <span data-ttu-id="151f8-536">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-536">State (required)</span></span>
- <span data-ttu-id="151f8-537">Region</span><span class="sxs-lookup"><span data-stu-id="151f8-537">County</span></span> 
- <span data-ttu-id="151f8-538">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="151f8-538">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="151f8-539">Konfigurere dataene for at generere løn i Mexico</span><span class="sxs-lookup"><span data-stu-id="151f8-539">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="151f8-540">Hvis du genererer løn for medarbejdere i Mexico skal følgende elementer konfigureres:</span><span class="sxs-lookup"><span data-stu-id="151f8-540">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="151f8-541">Der kræves afdelinger til stillinger.</span><span class="sxs-lookup"><span data-stu-id="151f8-541">Departments are required on positions.</span></span>
- <span data-ttu-id="151f8-542">Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="151f8-542">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="151f8-543">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="151f8-543">Job types</span></span>

<span data-ttu-id="151f8-544">Jobtyper bruges til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="151f8-544">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="151f8-545">Jobtyper kræves for at behandle løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="151f8-545">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="151f8-546">Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="151f8-546">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="151f8-547">Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.</span><span class="sxs-lookup"><span data-stu-id="151f8-547">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="151f8-548">Der kræves følgende jobtyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="151f8-548">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="151f8-549">Jobtype</span><span class="sxs-lookup"><span data-stu-id="151f8-549">Job type</span></span>   | <span data-ttu-id="151f8-550">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="151f8-550">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="151f8-551">Pr. time</span><span class="sxs-lookup"><span data-stu-id="151f8-551">Hourly</span></span>     | <span data-ttu-id="151f8-552">MX Pr. time</span><span class="sxs-lookup"><span data-stu-id="151f8-552">MX Hourly</span></span>   |
| <span data-ttu-id="151f8-553">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="151f8-553">Salaried</span></span>   | <span data-ttu-id="151f8-554">MX Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="151f8-554">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="151f8-555">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="151f8-555">Position types</span></span> 

<span data-ttu-id="151f8-556">Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet.</span><span class="sxs-lookup"><span data-stu-id="151f8-556">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="151f8-557">Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="151f8-557">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="151f8-558">Der kræves følgende stillingstyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="151f8-558">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="151f8-559">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="151f8-559">Position type</span></span>   | <span data-ttu-id="151f8-560">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="151f8-560">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="151f8-561">Fuld tid</span><span class="sxs-lookup"><span data-stu-id="151f8-561">Full-time</span></span>       | <span data-ttu-id="151f8-562">Fuldtidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="151f8-562">Full time employee</span></span> |
| <span data-ttu-id="151f8-563">Deltid</span><span class="sxs-lookup"><span data-stu-id="151f8-563">Part-time</span></span>       | <span data-ttu-id="151f8-564">Deltidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="151f8-564">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="151f8-565">Årsagskoder</span><span class="sxs-lookup"><span data-stu-id="151f8-565">Reason codes</span></span>

<span data-ttu-id="151f8-566">Årsagskoder indeholder oplysninger om status for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="151f8-566">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="151f8-567">Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.</span><span class="sxs-lookup"><span data-stu-id="151f8-567">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="151f8-568">Der kræves følgende årsagskoder og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="151f8-568">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="151f8-569">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="151f8-569">Reason code</span></span>            | <span data-ttu-id="151f8-570">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="151f8-570">Description</span></span>                    | <span data-ttu-id="151f8-571">Anvendelige scenarier</span><span class="sxs-lookup"><span data-stu-id="151f8-571">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="151f8-572">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="151f8-572">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="151f8-573">Afgang før første løn</span><span class="sxs-lookup"><span data-stu-id="151f8-573">Departure before first payroll</span></span> | <span data-ttu-id="151f8-574">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="151f8-574">Terminate worker</span></span>     |
| <span data-ttu-id="151f8-575">OPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="151f8-575">RESIGNATION</span></span>            | <span data-ttu-id="151f8-576">Opsigelse</span><span class="sxs-lookup"><span data-stu-id="151f8-576">Resignation</span></span>                    | <span data-ttu-id="151f8-577">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="151f8-577">Terminate worker</span></span>     |
| <span data-ttu-id="151f8-578">PENSION</span><span class="sxs-lookup"><span data-stu-id="151f8-578">PENSION</span></span>                | <span data-ttu-id="151f8-579">Pension</span><span class="sxs-lookup"><span data-stu-id="151f8-579">Pension</span></span>                        | <span data-ttu-id="151f8-580">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="151f8-580">Terminate worker</span></span>     |
| <span data-ttu-id="151f8-581">OPHØR</span><span class="sxs-lookup"><span data-stu-id="151f8-581">TERMINATION</span></span>            | <span data-ttu-id="151f8-582">Ophør</span><span class="sxs-lookup"><span data-stu-id="151f8-582">Termination</span></span>                    | <span data-ttu-id="151f8-583">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="151f8-583">Terminate worker</span></span>     |
| <span data-ttu-id="151f8-584">PENSION</span><span class="sxs-lookup"><span data-stu-id="151f8-584">RETIREMENT</span></span>             | <span data-ttu-id="151f8-585">Pension</span><span class="sxs-lookup"><span data-stu-id="151f8-585">Retirement</span></span>                     | <span data-ttu-id="151f8-586">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="151f8-586">Terminate worker</span></span>     |
| <span data-ttu-id="151f8-587">FRAVÆRENDE</span><span class="sxs-lookup"><span data-stu-id="151f8-587">ABSENTEE</span></span>               | <span data-ttu-id="151f8-588">Fraværende</span><span class="sxs-lookup"><span data-stu-id="151f8-588">Absentee</span></span>                       | <span data-ttu-id="151f8-589">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="151f8-589">Terminate worker</span></span>     |
| <span data-ttu-id="151f8-590">ANDET</span><span class="sxs-lookup"><span data-stu-id="151f8-590">OTHER</span></span>                  | <span data-ttu-id="151f8-591">Andre årsager</span><span class="sxs-lookup"><span data-stu-id="151f8-591">Other Reasons</span></span>                  | <span data-ttu-id="151f8-592">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="151f8-592">Terminate worker</span></span>     |
| <span data-ttu-id="151f8-593">LUKNING</span><span class="sxs-lookup"><span data-stu-id="151f8-593">CLOSURE</span></span>                | <span data-ttu-id="151f8-594">Virksomhedslukning</span><span class="sxs-lookup"><span data-stu-id="151f8-594">Business Closure</span></span>               | <span data-ttu-id="151f8-595">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="151f8-595">Terminate worker</span></span>     |
| <span data-ttu-id="151f8-596">DØDSFALD</span><span class="sxs-lookup"><span data-stu-id="151f8-596">DEATH</span></span>                  | <span data-ttu-id="151f8-597">Dødsfald</span><span class="sxs-lookup"><span data-stu-id="151f8-597">Death</span></span>                          | <span data-ttu-id="151f8-598">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="151f8-598">Terminate worker</span></span>     |
| <span data-ttu-id="151f8-599">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="151f8-599">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="151f8-600">Orlov</span><span class="sxs-lookup"><span data-stu-id="151f8-600">Leave of Absence</span></span>               | <span data-ttu-id="151f8-601">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="151f8-601">Terminate worker</span></span>     |
| <span data-ttu-id="151f8-602">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="151f8-602">CONTRACTEND</span></span>            | <span data-ttu-id="151f8-603">Kontraktudløb</span><span class="sxs-lookup"><span data-stu-id="151f8-603">End of Contract</span></span>                | <span data-ttu-id="151f8-604">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="151f8-604">Terminate worker</span></span>     |
| <span data-ttu-id="151f8-605">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="151f8-605">SALARYCHANGE</span></span>           | <span data-ttu-id="151f8-606">Ændring af løn</span><span class="sxs-lookup"><span data-stu-id="151f8-606">Change of Salary</span></span>               | <span data-ttu-id="151f8-607">Kompensation</span><span class="sxs-lookup"><span data-stu-id="151f8-607">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="151f8-608">Ansættelsesvilkår</span><span class="sxs-lookup"><span data-stu-id="151f8-608">Terms of employment</span></span>

<span data-ttu-id="151f8-609">Ansættelsesvilkår bruges til at oprette kategorier for ansættelsesvilkår.</span><span class="sxs-lookup"><span data-stu-id="151f8-609">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="151f8-610">Vilkårene knyttes til Dayforce som beskæftigelsesindikatorværdier.</span><span class="sxs-lookup"><span data-stu-id="151f8-610">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="151f8-611">Følgende begreber for beskæftigelse og beskrivelser er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="151f8-611">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="151f8-612">Ansættelsesvilkår</span><span class="sxs-lookup"><span data-stu-id="151f8-612">Terms of employment</span></span>   | <span data-ttu-id="151f8-613">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="151f8-613">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="151f8-614">Regulær</span><span class="sxs-lookup"><span data-stu-id="151f8-614">Regular</span></span>               | <span data-ttu-id="151f8-615">Regulær</span><span class="sxs-lookup"><span data-stu-id="151f8-615">Regular</span></span>     |
| <span data-ttu-id="151f8-616">Direkte</span><span class="sxs-lookup"><span data-stu-id="151f8-616">Direct</span></span>                | <span data-ttu-id="151f8-617">Direkte</span><span class="sxs-lookup"><span data-stu-id="151f8-617">Direct</span></span>      |
| <span data-ttu-id="151f8-618">Turnustjeneste</span><span class="sxs-lookup"><span data-stu-id="151f8-618">Internship</span></span>            | <span data-ttu-id="151f8-619">Turnustjeneste</span><span class="sxs-lookup"><span data-stu-id="151f8-619">Internship</span></span>  |
| <span data-ttu-id="151f8-620">Permanent</span><span class="sxs-lookup"><span data-stu-id="151f8-620">Permanent</span></span>             | <span data-ttu-id="151f8-621">Permanent</span><span class="sxs-lookup"><span data-stu-id="151f8-621">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="151f8-622">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="151f8-622">Marital status</span></span>

<span data-ttu-id="151f8-623">Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="151f8-623">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="151f8-624">Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="151f8-624">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="151f8-625">Human Resources</span><span class="sxs-lookup"><span data-stu-id="151f8-625">Human Resources</span></span>                 | <span data-ttu-id="151f8-626">Dayforce</span><span class="sxs-lookup"><span data-stu-id="151f8-626">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="151f8-627">Gift</span><span class="sxs-lookup"><span data-stu-id="151f8-627">Married</span></span>                | <span data-ttu-id="151f8-628">Gift</span><span class="sxs-lookup"><span data-stu-id="151f8-628">Married</span></span>                   |
| <span data-ttu-id="151f8-629">Enlig</span><span class="sxs-lookup"><span data-stu-id="151f8-629">Single</span></span>                 | <span data-ttu-id="151f8-630">Enlig</span><span class="sxs-lookup"><span data-stu-id="151f8-630">Single</span></span>                    |
| <span data-ttu-id="151f8-631">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="151f8-631">Widowed</span></span>                | <span data-ttu-id="151f8-632">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="151f8-632">Widowed</span></span>                   |
| <span data-ttu-id="151f8-633">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="151f8-633">Divorced</span></span>               | <span data-ttu-id="151f8-634">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="151f8-634">Divorced</span></span>                  |
| <span data-ttu-id="151f8-635">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="151f8-635">Registered Partnership</span></span> | <span data-ttu-id="151f8-636">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="151f8-636">Domestic Partnership</span></span>      |
| <span data-ttu-id="151f8-637">None</span><span class="sxs-lookup"><span data-stu-id="151f8-637">None</span></span>                   | <span data-ttu-id="151f8-638">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="151f8-638">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="151f8-639">Samlever</span><span class="sxs-lookup"><span data-stu-id="151f8-639">Cohabiting</span></span>             | <span data-ttu-id="151f8-640">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="151f8-640">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="151f8-641">Køn</span><span class="sxs-lookup"><span data-stu-id="151f8-641">Gender</span></span>

<span data-ttu-id="151f8-642">Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="151f8-642">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="151f8-643">Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="151f8-643">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="151f8-644">Human Resources</span><span class="sxs-lookup"><span data-stu-id="151f8-644">Human Resources</span></span>       | <span data-ttu-id="151f8-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="151f8-645">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="151f8-646">Mand</span><span class="sxs-lookup"><span data-stu-id="151f8-646">Male</span></span>         | <span data-ttu-id="151f8-647">Mand</span><span class="sxs-lookup"><span data-stu-id="151f8-647">Male</span></span>                      |
| <span data-ttu-id="151f8-648">Kvinde</span><span class="sxs-lookup"><span data-stu-id="151f8-648">Female</span></span>       | <span data-ttu-id="151f8-649">Kvinde</span><span class="sxs-lookup"><span data-stu-id="151f8-649">Female</span></span>                    |
| <span data-ttu-id="151f8-650">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="151f8-650">Non-specific</span></span> | <span data-ttu-id="151f8-651">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="151f8-651">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="151f8-652">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="151f8-652">Payment method</span></span>

<span data-ttu-id="151f8-653">Betalingsmetoder giver medarbejderen og virksomheden en måde til at beskrive, hvordan medarbejdere skal betales.</span><span class="sxs-lookup"><span data-stu-id="151f8-653">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="151f8-654">Betalingsmåder knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="151f8-654">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="151f8-655">Følgende tabel viser, hvordan betalingsmetoder knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="151f8-655">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="151f8-656">Human Resources</span><span class="sxs-lookup"><span data-stu-id="151f8-656">Human Resources</span></span>             | <span data-ttu-id="151f8-657">Dayforce</span><span class="sxs-lookup"><span data-stu-id="151f8-657">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="151f8-658">Indløsning</span><span class="sxs-lookup"><span data-stu-id="151f8-658">Cash</span></span>               | <span data-ttu-id="151f8-659">Indløsning</span><span class="sxs-lookup"><span data-stu-id="151f8-659">Cash</span></span>                      |
| <span data-ttu-id="151f8-660">Elektronisk betaling</span><span class="sxs-lookup"><span data-stu-id="151f8-660">Electronic Payment</span></span> | <span data-ttu-id="151f8-661">Ompostering</span><span class="sxs-lookup"><span data-stu-id="151f8-661">Transfer</span></span>                  |
| <span data-ttu-id="151f8-662">Check</span><span class="sxs-lookup"><span data-stu-id="151f8-662">Check</span></span>              | <span data-ttu-id="151f8-663">Check</span><span class="sxs-lookup"><span data-stu-id="151f8-663">Cheque</span></span>                    |
| <span data-ttu-id="151f8-664">Bankanvisning</span><span class="sxs-lookup"><span data-stu-id="151f8-664">Bank Draft</span></span>         | <span data-ttu-id="151f8-665">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="151f8-665">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="151f8-666">Andre</span><span class="sxs-lookup"><span data-stu-id="151f8-666">Other</span></span>              | <span data-ttu-id="151f8-667">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="151f8-667">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="151f8-668">Bankkontotype</span><span class="sxs-lookup"><span data-stu-id="151f8-668">Bank account type</span></span>

<span data-ttu-id="151f8-669">Bankkontotyper bruges til elektroniske betalinger til medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="151f8-669">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="151f8-670">Bankkontotyper knyttes til Dayforce som overførselskontooplysninger.</span><span class="sxs-lookup"><span data-stu-id="151f8-670">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="151f8-671">Bankkontotyperne oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="151f8-671">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="151f8-672">Human Resources</span><span class="sxs-lookup"><span data-stu-id="151f8-672">Human Resources</span></span>            | <span data-ttu-id="151f8-673">Dayforce</span><span class="sxs-lookup"><span data-stu-id="151f8-673">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="151f8-674">Checkkonto</span><span class="sxs-lookup"><span data-stu-id="151f8-674">Checking Account</span></span>  | <span data-ttu-id="151f8-675">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="151f8-675">CheckingAccount</span></span>           |
| <span data-ttu-id="151f8-676">Lønkonto</span><span class="sxs-lookup"><span data-stu-id="151f8-676">Payroll Account</span></span>   | <span data-ttu-id="151f8-677">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="151f8-677">PayrollAccount</span></span>            |
| <span data-ttu-id="151f8-678">Opsparingskonto</span><span class="sxs-lookup"><span data-stu-id="151f8-678">Savings Account</span></span>   | <span data-ttu-id="151f8-679">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="151f8-679">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="151f8-680">BankGirot-konto</span><span class="sxs-lookup"><span data-stu-id="151f8-680">BankGirot account</span></span> | <span data-ttu-id="151f8-681">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="151f8-681">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="151f8-682">PlusGirot-konto</span><span class="sxs-lookup"><span data-stu-id="151f8-682">PlusGirot account</span></span> | <span data-ttu-id="151f8-683">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="151f8-683">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="151f8-684">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="151f8-684">Earning codes</span></span>

<span data-ttu-id="151f8-685">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="151f8-685">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="151f8-686">Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="151f8-686">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="151f8-687">Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="151f8-687">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="151f8-688">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="151f8-688">Supported frequencies</span></span>

- <span data-ttu-id="151f8-689">Alt</span><span class="sxs-lookup"><span data-stu-id="151f8-689">All</span></span>
- <span data-ttu-id="151f8-690">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="151f8-690">EVERYPAY</span></span>
- <span data-ttu-id="151f8-691">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="151f8-691">EACHPAYPERIOD</span></span>
- <span data-ttu-id="151f8-692">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="151f8-692">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="151f8-693">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="151f8-693">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="151f8-694">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-694">1OFMTH</span></span>
- <span data-ttu-id="151f8-695">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-695">LASTOFMTH</span></span>
- <span data-ttu-id="151f8-696">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-696">2OFMTH</span></span>
- <span data-ttu-id="151f8-697">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-697">3OFMTH</span></span>
- <span data-ttu-id="151f8-698">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-698">4OFMTH</span></span>
- <span data-ttu-id="151f8-699">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-699">5OFMTH</span></span>
- <span data-ttu-id="151f8-700">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-700">1N2OFMTH</span></span>
- <span data-ttu-id="151f8-701">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-701">3N4OFMTH</span></span>
- <span data-ttu-id="151f8-702">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-702">1N3OFMTH</span></span>
- <span data-ttu-id="151f8-703">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-703">1N4OFMTH</span></span>
- <span data-ttu-id="151f8-704">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-704">2N3OFMTH</span></span>
- <span data-ttu-id="151f8-705">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-705">2N4OFMTH</span></span>
- <span data-ttu-id="151f8-706">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-706">1N2N3OFMTH</span></span>
- <span data-ttu-id="151f8-707">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-707">1N2N4OFMTH</span></span>
- <span data-ttu-id="151f8-708">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-708">1N3N4OFMTH</span></span>
- <span data-ttu-id="151f8-709">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-709">2N3N4OFMTH</span></span>
- <span data-ttu-id="151f8-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="151f8-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="151f8-711">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="151f8-711">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="151f8-712">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="151f8-712">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="151f8-713">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="151f8-713">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="151f8-714">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="151f8-714">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="151f8-715">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="151f8-715">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="151f8-716">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="151f8-716">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="151f8-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="151f8-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="151f8-718">Adresser</span><span class="sxs-lookup"><span data-stu-id="151f8-718">Addresses</span></span>

<span data-ttu-id="151f8-719">Identifikation af specifikke koder for land eller område, stat og region (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende.</span><span class="sxs-lookup"><span data-stu-id="151f8-719">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="151f8-720">Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.</span><span class="sxs-lookup"><span data-stu-id="151f8-720">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="151f8-721">Human Resources</span><span class="sxs-lookup"><span data-stu-id="151f8-721">Human Resources</span></span>              | <span data-ttu-id="151f8-722">Dayforce</span><span class="sxs-lookup"><span data-stu-id="151f8-722">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="151f8-723">Land/område</span><span class="sxs-lookup"><span data-stu-id="151f8-723">Country/Region</span></span>      | <span data-ttu-id="151f8-724">Landekode</span><span class="sxs-lookup"><span data-stu-id="151f8-724">Country Code</span></span>          |
| <span data-ttu-id="151f8-725">Postnummer</span><span class="sxs-lookup"><span data-stu-id="151f8-725">Zip/Postal Code</span></span>     | <span data-ttu-id="151f8-726">Postnummer</span><span class="sxs-lookup"><span data-stu-id="151f8-726">Postal Code</span></span>           |
| <span data-ttu-id="151f8-727">Status</span><span class="sxs-lookup"><span data-stu-id="151f8-727">State</span></span>               | <span data-ttu-id="151f8-728">Statskode</span><span class="sxs-lookup"><span data-stu-id="151f8-728">State Code</span></span>            |
| <span data-ttu-id="151f8-729">Bynavn</span><span class="sxs-lookup"><span data-stu-id="151f8-729">City</span></span>                | <span data-ttu-id="151f8-730">Bynavn</span><span class="sxs-lookup"><span data-stu-id="151f8-730">City</span></span>                  |
| <span data-ttu-id="151f8-731">Region</span><span class="sxs-lookup"><span data-stu-id="151f8-731">County</span></span>              | <span data-ttu-id="151f8-732">Område (kommune)</span><span class="sxs-lookup"><span data-stu-id="151f8-732">County (Municipality)</span></span> |
| <span data-ttu-id="151f8-733">Gade</span><span class="sxs-lookup"><span data-stu-id="151f8-733">Street</span></span>              | <span data-ttu-id="151f8-734">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="151f8-734">Address Line 1</span></span>        |
| <span data-ttu-id="151f8-735">Gadenummer</span><span class="sxs-lookup"><span data-stu-id="151f8-735">Street Number</span></span>       | <span data-ttu-id="151f8-736">Adresselinje 2</span><span class="sxs-lookup"><span data-stu-id="151f8-736">Address Line 2</span></span>        |
| <span data-ttu-id="151f8-737">Bygningskomplement</span><span class="sxs-lookup"><span data-stu-id="151f8-737">Building Complement</span></span> | <span data-ttu-id="151f8-738">Adresselinje 5</span><span class="sxs-lookup"><span data-stu-id="151f8-738">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="151f8-739">Pasnummer</span><span class="sxs-lookup"><span data-stu-id="151f8-739">Passport number</span></span>

<span data-ttu-id="151f8-740">Medarbejdere kan erklære pasoplysninger.</span><span class="sxs-lookup"><span data-stu-id="151f8-740">Employees can declare passport information.</span></span> <span data-ttu-id="151f8-741">Disse oplysninger er af identifikationstypen **Pas** og er integreret i Dayforce som en del af en medarbejders Mexico-specifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="151f8-741">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="151f8-742">Identifikationstype = "Pas"</span><span class="sxs-lookup"><span data-stu-id="151f8-742">Identification Type = "Passport"</span></span>
- <span data-ttu-id="151f8-743">Udstedt den</span><span class="sxs-lookup"><span data-stu-id="151f8-743">Issued Date</span></span>
- <span data-ttu-id="151f8-744">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="151f8-744">Expiration Date</span></span>

<span data-ttu-id="151f8-745">Medarbejdere kan angive flere identifikationsnumre af **Pas**-identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="151f8-745">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="151f8-746">Men det er kun den aktuelle aktive paspost, der integreres i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="151f8-746">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="151f8-747">Hvis alle pasposter er udløbet, integreres det pas, der senest blev udstedt, i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="151f8-747">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]