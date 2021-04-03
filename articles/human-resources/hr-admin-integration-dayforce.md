---
title: Konfigurer integration med Dayforce
description: Integrationen mellem Microsoft Dynamics 365 Human Resources og Ceridian Dayforce er baseret på flere konfigurationstrin, der er beskrevet i dette emne. Du skal konfigurere integrationen i både Human Resources og Dayforce, før du kan behandle en lønkørsel.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 2d5f65672960716bee3f58c98ccce249fdbf8697
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467139"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="0a67b-104">Konfigurer integration med Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a67b-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0a67b-105">Integrationen mellem Microsoft Dynamics 365 Human Resources og Ceridian Dayforce er baseret på flere konfigurationstrin, der er beskrevet i dette emne.</span><span class="sxs-lookup"><span data-stu-id="0a67b-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="0a67b-106">Du skal konfigurere integrationen i både Human Resources og Dayforce, før du kan behandle en lønkørsel.</span><span class="sxs-lookup"><span data-stu-id="0a67b-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="0a67b-107">Når du bruger en tjeneste, f.eks. Dayforce, til at fuldføre lønkørsler, skal du aktivere integrationen i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0a67b-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="0a67b-108">Integrationen kræver bestemte data fra Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0a67b-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="0a67b-109">Du skal derfor kontrollere, at data, der er knyttet til Dayforce, er konfigureret i Human Resources på en måde, der understøtter integrationen.</span><span class="sxs-lookup"><span data-stu-id="0a67b-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="0a67b-110">Integrationen bruger følgende brede kategorier af data.</span><span class="sxs-lookup"><span data-stu-id="0a67b-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="0a67b-111">Human Resourcesdata</span><span class="sxs-lookup"><span data-stu-id="0a67b-111">Human resources data</span></span>
- <span data-ttu-id="0a67b-112">Kompensationsdata</span><span class="sxs-lookup"><span data-stu-id="0a67b-112">Compensation data</span></span>
- <span data-ttu-id="0a67b-113">Lønoplysninger, f.eks. løncyklusser, betalingsperioder og lønkoder</span><span class="sxs-lookup"><span data-stu-id="0a67b-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="0a67b-114">Arbejderdata</span><span class="sxs-lookup"><span data-stu-id="0a67b-114">Worker data</span></span>

<span data-ttu-id="0a67b-115">Denne artikel beskriver de trin, du skal udføre for at aktivere integrationen.</span><span class="sxs-lookup"><span data-stu-id="0a67b-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="0a67b-116">Det forklarer også typerne af data og oplysninger om konfigurationen, der kræves til integrationen.</span><span class="sxs-lookup"><span data-stu-id="0a67b-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="0a67b-117">Aktivere integrationen.</span><span class="sxs-lookup"><span data-stu-id="0a67b-117">Enable the integration</span></span>

<span data-ttu-id="0a67b-118">I Human Resources skal du aktivere integrationen og angive konfigurationsoplysningerne for at oprette forbindelse til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a67b-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="0a67b-119">Hvis den finanspostering, der er oprettet, skal importeres til Microsoft Dynamics 365 Finance, skal du også konfigurere en Microsoft Azure-lagerkonto og angive Azure-lagerets forbindelsesstreng i Finance.</span><span class="sxs-lookup"><span data-stu-id="0a67b-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="0a67b-120">Følg disse trin for at aktivere integrationen i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0a67b-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="0a67b-121">På siden **Systemadministration** skal du vælge **Integrationskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="0a67b-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="0a67b-122">Angiv det sikre FTP-slutpunkt og den sikre FTP-mappesti.</span><span class="sxs-lookup"><span data-stu-id="0a67b-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="0a67b-123">Angiv brugernavnet og adgangskoden for den bruger, der skal have adgang til det sikre FTP-slutpunkt og den sikre mappesti.</span><span class="sxs-lookup"><span data-stu-id="0a67b-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="0a67b-124">Test forbindelsen, som krævet, og angiv indstillingen **Aktivér lønintegration** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0a67b-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="0a67b-125">Når integrationen er aktiveret, oprettes dataeksportpakken og -filerne, og hyppigheden angives.</span><span class="sxs-lookup"><span data-stu-id="0a67b-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="0a67b-126">Du kan ændre denne frekvens efter behov.</span><span class="sxs-lookup"><span data-stu-id="0a67b-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="0a67b-127">Yderligere oplysninger om Azure-lagerkonti og Azure-lagerforbindelsesstrenge finder du i følgende Azure-artikler:</span><span class="sxs-lookup"><span data-stu-id="0a67b-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="0a67b-128">Om Azure-lagerkonti</span><span class="sxs-lookup"><span data-stu-id="0a67b-128">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="0a67b-129">Konfigurere forbindelsesstrenge for Azure-datalager</span><span class="sxs-lookup"><span data-stu-id="0a67b-129">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="0a67b-130">Tekniske oplysninger ved aktivering af lønintegration</span><span class="sxs-lookup"><span data-stu-id="0a67b-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="0a67b-131">Aktivering af lønintegration har to primære effekter:</span><span class="sxs-lookup"><span data-stu-id="0a67b-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="0a67b-132">Der oprettes et dataeksport projekt ved navn "Lønintegrationseksport".</span><span class="sxs-lookup"><span data-stu-id="0a67b-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="0a67b-133">Dette projekt indeholder de objekter og felter, der kræves til lønintegration.</span><span class="sxs-lookup"><span data-stu-id="0a67b-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="0a67b-134">Hvis du vil undersøge projektet, skal du gå til **Systemadministration**, vælge feltet **Datastyring** og derefter åbne dataprojektet på listen over projekter.</span><span class="sxs-lookup"><span data-stu-id="0a67b-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="0a67b-135">Dette batchjob udfører dataeksportprojektet, krypterer den resulterende datapakke og overfører datapakkefilen til det SFTP-slutpunkt, der er konfigureret på skærmen **Integrationskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="0a67b-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="0a67b-136">Den datapakke, der overføres til SFTP-slutpunktet, krypteres ved hjælp af en nøgle, der er entydig for pakken.</span><span class="sxs-lookup"><span data-stu-id="0a67b-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="0a67b-137">Nøglen er i en Azure Key Vault, der kun kan åbnes af Ceridian.</span><span class="sxs-lookup"><span data-stu-id="0a67b-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="0a67b-138">Det er ikke muligt at dekryptere og undersøge datapakkens indhold.</span><span class="sxs-lookup"><span data-stu-id="0a67b-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="0a67b-139">Hvis du har brug for at undersøge indholdet af datapakken, skal du eksportere dataprojektet "Lønintegrationseksport" manuelt, download det og derefter åbne det.</span><span class="sxs-lookup"><span data-stu-id="0a67b-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="0a67b-140">Manuel eksport anvender ikke kryptering eller overførsel af pakken.</span><span class="sxs-lookup"><span data-stu-id="0a67b-140">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="0a67b-141">Konfigurere dine data</span><span class="sxs-lookup"><span data-stu-id="0a67b-141">Configure your data</span></span> 

<span data-ttu-id="0a67b-142">Hvis du vil behandle løn, skal du konfigurere personaledata i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0a67b-142">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="0a67b-143">Du skal angive virksomhedens data, f.eks. job og stillinger, sammen med frynsegoder og kompensationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="0a67b-143">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="0a67b-144">Disse oplysninger indeholder oplysningerne om ansættelse, løn og fradrag, der kræves for at generere løn for medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="0a67b-144">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="0a67b-145">Human Resourcesdata</span><span class="sxs-lookup"><span data-stu-id="0a67b-145">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="0a67b-146">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="0a67b-146">Benefits</span></span> 

<span data-ttu-id="0a67b-147">Human Resources indeholder en række værktøjer til konfiguration og vedligeholdelse af frynsegoder, fradrag og arbejderkompensationsplaner, som en organisation tilbyder eller behandler for sine ansatte.</span><span class="sxs-lookup"><span data-stu-id="0a67b-147">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="0a67b-148">Når du opretter frynsegoder, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a67b-148">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="0a67b-149">Frynsegodeplaner</span><span class="sxs-lookup"><span data-stu-id="0a67b-149">Benefit plans</span></span>

- <span data-ttu-id="0a67b-150">Plan (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-150">Plan (required)</span></span>
- <span data-ttu-id="0a67b-151">Type (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-151">Type (required)</span></span>
- <span data-ttu-id="0a67b-152">Løneffekt (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-152">Payroll impact (required)</span></span>
- <span data-ttu-id="0a67b-153">Opkræv restancer</span><span class="sxs-lookup"><span data-stu-id="0a67b-153">Recover arrears</span></span>
- <span data-ttu-id="0a67b-154">Fradragsmetode</span><span class="sxs-lookup"><span data-stu-id="0a67b-154">Deduction method</span></span>
- <span data-ttu-id="0a67b-155">Prioriteret fradrag</span><span class="sxs-lookup"><span data-stu-id="0a67b-155">Deduction priority</span></span>
- <span data-ttu-id="0a67b-156">Grænseperiode</span><span class="sxs-lookup"><span data-stu-id="0a67b-156">Limit period</span></span>
- <span data-ttu-id="0a67b-157">Beløb for grænse</span><span class="sxs-lookup"><span data-stu-id="0a67b-157">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="0a67b-158">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="0a67b-158">Benefits</span></span>

- <span data-ttu-id="0a67b-159">Plan (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-159">Plan (required)</span></span>
- <span data-ttu-id="0a67b-160">Type (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-160">Type (required)</span></span>
- <span data-ttu-id="0a67b-161">Mulighed (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-161">Option (required)</span></span>
- <span data-ttu-id="0a67b-162">Frynsegode-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-162">Benefit ID (required)</span></span>
- <span data-ttu-id="0a67b-163">Frekvens</span><span class="sxs-lookup"><span data-stu-id="0a67b-163">Frequency</span></span>
- <span data-ttu-id="0a67b-164">Basis</span><span class="sxs-lookup"><span data-stu-id="0a67b-164">Basis</span></span>
- <span data-ttu-id="0a67b-165">Beløb eller sats</span><span class="sxs-lookup"><span data-stu-id="0a67b-165">Amount or rate</span></span>
- <span data-ttu-id="0a67b-166">Lønkode</span><span class="sxs-lookup"><span data-stu-id="0a67b-166">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="0a67b-167">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="0a67b-167">Supported frequencies</span></span> 

- <span data-ttu-id="0a67b-168">Ugentlig</span><span class="sxs-lookup"><span data-stu-id="0a67b-168">Weekly</span></span>
- <span data-ttu-id="0a67b-169">Pr. 14 dage</span><span class="sxs-lookup"><span data-stu-id="0a67b-169">Bi-weekly</span></span>
- <span data-ttu-id="0a67b-170">To gange om måneden</span><span class="sxs-lookup"><span data-stu-id="0a67b-170">Semi-monthly</span></span>
- <span data-ttu-id="0a67b-171">Månedlig</span><span class="sxs-lookup"><span data-stu-id="0a67b-171">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="0a67b-172">Understøttede grundlag</span><span class="sxs-lookup"><span data-stu-id="0a67b-172">Supported bases</span></span> 

- <span data-ttu-id="0a67b-173">Fast beløb</span><span class="sxs-lookup"><span data-stu-id="0a67b-173">Fixed amount</span></span>
- <span data-ttu-id="0a67b-174">Procentdel af løn</span><span class="sxs-lookup"><span data-stu-id="0a67b-174">Percent of earnings</span></span>
- <span data-ttu-id="0a67b-175">Produktive timer</span><span class="sxs-lookup"><span data-stu-id="0a67b-175">Productive hours</span></span>

<span data-ttu-id="0a67b-176">Dayforce opretter følgende fradrag, der er baseret på den løneffekt, der er defineret på frynsegodeplanen.</span><span class="sxs-lookup"><span data-stu-id="0a67b-176">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="0a67b-177">Valg i Human Resources</span><span class="sxs-lookup"><span data-stu-id="0a67b-177">Selection in Human Resources</span></span>        | <span data-ttu-id="0a67b-178">Resultat i Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a67b-178">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="0a67b-179">Ingen</span><span class="sxs-lookup"><span data-stu-id="0a67b-179">None</span></span>                       | <span data-ttu-id="0a67b-180">Der oprettes ikke noget fradrag.</span><span class="sxs-lookup"><span data-stu-id="0a67b-180">No deduction is created.</span></span>                      |
| <span data-ttu-id="0a67b-181">Kun fradrag</span><span class="sxs-lookup"><span data-stu-id="0a67b-181">Deduction only</span></span>             | <span data-ttu-id="0a67b-182">Der oprettes et medarbejderfradrag.</span><span class="sxs-lookup"><span data-stu-id="0a67b-182">An employee deduction is created.</span></span>             |
| <span data-ttu-id="0a67b-183">Kun bidrag</span><span class="sxs-lookup"><span data-stu-id="0a67b-183">Contribution only</span></span>          | <span data-ttu-id="0a67b-184">Der oprettes et arbejdsgiverfradrag.</span><span class="sxs-lookup"><span data-stu-id="0a67b-184">An employer deduction is created.</span></span>             |
| <span data-ttu-id="0a67b-185">Fradrag og bidrag</span><span class="sxs-lookup"><span data-stu-id="0a67b-185">Deduction and contribution</span></span> | <span data-ttu-id="0a67b-186">Der oprettes medarbejder- og arbejdsgiverfradrag.</span><span class="sxs-lookup"><span data-stu-id="0a67b-186">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="0a67b-187">Du kan finde flere oplysninger om, hvordan du definerer og administrerer et frynsegodeprogram i følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="0a67b-187">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="0a67b-188">Levere et frynsegodeprogram for medarbejdere</span><span class="sxs-lookup"><span data-stu-id="0a67b-188">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="0a67b-189">Opret et nyt frynsegode</span><span class="sxs-lookup"><span data-stu-id="0a67b-189">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="0a67b-190">Definere regler og politikker for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="0a67b-190">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="0a67b-191">Tilmelde og fjerne frynsegoder fra arbejdere</span><span class="sxs-lookup"><span data-stu-id="0a67b-191">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="0a67b-192">Kompensation</span><span class="sxs-lookup"><span data-stu-id="0a67b-192">Compensation</span></span> 

<span data-ttu-id="0a67b-193">Kompensationsstyring bruges til at styre fordelingen af grundløn og bonusser.</span><span class="sxs-lookup"><span data-stu-id="0a67b-193">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="0a67b-194">En medarbejders faste grundløn og kvalifikationstillæg styres gennem faste lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="0a67b-194">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="0a67b-195">Betalingen af incitamentsløn som f.eks. bonusudbetalinger, præstationsbonusser, aktieoptioner og tildelte aktier samt engangsbonusser styres ved hjælp af variable lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="0a67b-195">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="0a67b-196">Dayforce anvendes kompensationsoplysninger til at beregne en medarbejders timesats eller årlige sats.</span><span class="sxs-lookup"><span data-stu-id="0a67b-196">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="0a67b-197">Konverteringer af planer for fast løn og lønsats er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="0a67b-197">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="0a67b-198">Medarbejderne skal være knyttet til en plan for fast løn.</span><span class="sxs-lookup"><span data-stu-id="0a67b-198">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="0a67b-199">Du kan finde flere oplysninger om kompensationsplaner i følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="0a67b-199">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="0a67b-200">Oprette planer for fast løn</span><span class="sxs-lookup"><span data-stu-id="0a67b-200">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="0a67b-201">Oprette planer for variabel kompensation</span><span class="sxs-lookup"><span data-stu-id="0a67b-201">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="0a67b-202">Udarbejde løn-/kompensationsstruktur og -planer</span><span class="sxs-lookup"><span data-stu-id="0a67b-202">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="0a67b-203">Proceskompensation</span><span class="sxs-lookup"><span data-stu-id="0a67b-203">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="0a67b-204">Definere kompensationsproces og beregne resultater</span><span class="sxs-lookup"><span data-stu-id="0a67b-204">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="0a67b-205">Melde en medarbejder til en fast lønplan</span><span class="sxs-lookup"><span data-stu-id="0a67b-205">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="0a67b-206">Melde en medarbejder til en variabel lønplan</span><span class="sxs-lookup"><span data-stu-id="0a67b-206">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="0a67b-207">Job</span><span class="sxs-lookup"><span data-stu-id="0a67b-207">Jobs</span></span> 

<span data-ttu-id="0a67b-208">Et job er en samling af de opgaver og ansvarsområder, der kræves af en person, der udfører et job.</span><span class="sxs-lookup"><span data-stu-id="0a67b-208">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="0a67b-209">Du kan finde flere oplysninger i følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="0a67b-209">For more information, see the following articles:</span></span>

- [<span data-ttu-id="0a67b-210">Konfiguration af komponenter i et job</span><span class="sxs-lookup"><span data-stu-id="0a67b-210">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="0a67b-211">Definere nye job</span><span class="sxs-lookup"><span data-stu-id="0a67b-211">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="0a67b-212">Stillinger</span><span class="sxs-lookup"><span data-stu-id="0a67b-212">Positions</span></span>

<span data-ttu-id="0a67b-213">En stilling er en individuel forekomst af et job.</span><span class="sxs-lookup"><span data-stu-id="0a67b-213">A position is an individual instance of a job.</span></span> <span data-ttu-id="0a67b-214">For eksempel er stillingen "Salgschef (øst)" én af de stillinger, der er tilknyttet jobbet "Salgschef".</span><span class="sxs-lookup"><span data-stu-id="0a67b-214">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="0a67b-215">En stilling findes i en afdeling.</span><span class="sxs-lookup"><span data-stu-id="0a67b-215">A position exists in a department.</span></span> <span data-ttu-id="0a67b-216">Der kan kun knyttes én arbejder til hver stilling.</span><span class="sxs-lookup"><span data-stu-id="0a67b-216">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="0a67b-217">Hav følgende data og konfiguration i tankerne, når du konfigurerer stillinger:</span><span class="sxs-lookup"><span data-stu-id="0a67b-217">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="0a67b-218">Stilling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-218">Position (required)</span></span>
- <span data-ttu-id="0a67b-219">Beskrivelse (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-219">Description (required)</span></span>
- <span data-ttu-id="0a67b-220">Job (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-220">Job (required)</span></span>
- <span data-ttu-id="0a67b-221">Afdeling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-221">Department (required)</span></span>
- <span data-ttu-id="0a67b-222">Stillingstype (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-222">Position type (required)</span></span>
- <span data-ttu-id="0a67b-223">Fuldtidsækvivalent</span><span class="sxs-lookup"><span data-stu-id="0a67b-223">Full-time equivalent</span></span>
- <span data-ttu-id="0a67b-224">Normaltimer på årsbasis (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-224">Annual regular hours (required)</span></span>
- <span data-ttu-id="0a67b-225">Betalt af juridiske enhed (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-225">Paid by legal entity (required)</span></span>
- <span data-ttu-id="0a67b-226">Betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-226">Pay cycle (required)</span></span>
- <span data-ttu-id="0a67b-227">Økonomisk standarddimension – bærer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-227">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="0a67b-228">Arbejdertildeling – arbejder, tildelingsstart, tildelingsslut, årsagskode</span><span class="sxs-lookup"><span data-stu-id="0a67b-228">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="0a67b-229">Hvis flere stillinger i den samme afdeling er knyttet til samme job, konsolideres de til en enkelt stilling i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a67b-229">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="0a67b-230">Du kan finde flere oplysninger i følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="0a67b-230">For more information, see the following articles:</span></span>

- [<span data-ttu-id="0a67b-231">Organisere dine medarbejdere ved hjælp af afdelinger, jobs og stillinger</span><span class="sxs-lookup"><span data-stu-id="0a67b-231">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="0a67b-232">Konfigurere stillinger</span><span class="sxs-lookup"><span data-stu-id="0a67b-232">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="0a67b-233">Afdelinger</span><span class="sxs-lookup"><span data-stu-id="0a67b-233">Departments</span></span>

<span data-ttu-id="0a67b-234">En afdeling er en driftsenhed, der repræsenterer en kategori eller et funktionsområde i en organisation.</span><span class="sxs-lookup"><span data-stu-id="0a67b-234">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="0a67b-235">En afdeling er ansvarlig for et bestemt område i organisationen, såsom salg, regnskab eller personale.</span><span class="sxs-lookup"><span data-stu-id="0a67b-235">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="0a67b-236">Du kan bruge afdelinger til at rapportere om funktionsområder.</span><span class="sxs-lookup"><span data-stu-id="0a67b-236">You can use departments to report on functional areas.</span></span> <span data-ttu-id="0a67b-237">Afdelinger kan have ansvar for driftsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="0a67b-237">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="0a67b-238">Du kan finde flere oplysninger i følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="0a67b-238">For more information, see the following articles:</span></span>

- [<span data-ttu-id="0a67b-239">Oprette en afdeling og knytte den til afdelingshierarkiet</span><span class="sxs-lookup"><span data-stu-id="0a67b-239">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="0a67b-240">Definere nye afdelinger</span><span class="sxs-lookup"><span data-stu-id="0a67b-240">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="0a67b-241">Betalingscyklusser og lønperioder</span><span class="sxs-lookup"><span data-stu-id="0a67b-241">Pay cycles and pay periods</span></span>

<span data-ttu-id="0a67b-242">En betalingscyklus bestemmer, hvor ofte løn køres,og de specifikke dage, hvor arbejdere betales.</span><span class="sxs-lookup"><span data-stu-id="0a67b-242">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="0a67b-243">En løncyklus kan f.eks. være månedlig, og medarbejdere betales måske på den sidste dag i måneden.</span><span class="sxs-lookup"><span data-stu-id="0a67b-243">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="0a67b-244">En løncyklus kan også være ugentligt, og medarbejdere betales måske tirsdag efter slutningen af lønperioden.</span><span class="sxs-lookup"><span data-stu-id="0a67b-244">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="0a67b-245">Løncyklusser tildeles til stillinger for at styre, hvornår arbejdere i disse stillinger bliver betalt.</span><span class="sxs-lookup"><span data-stu-id="0a67b-245">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="0a67b-246">Når du opretter betalingscyklusser, kan du generere lønperioder for hver cyklus.</span><span class="sxs-lookup"><span data-stu-id="0a67b-246">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="0a67b-247">Hver lønperiode omfatter en standardbetalingsdato, der er baseret på oplysninger, du angiver.</span><span class="sxs-lookup"><span data-stu-id="0a67b-247">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="0a67b-248">Du kan dog redigere standardbetalingsdatoen i en lønperiode til at tillade undtagelser, f.eks. når betalingsdatoen falder på en helligdag.</span><span class="sxs-lookup"><span data-stu-id="0a67b-248">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="0a67b-249">Følgende oplysninger bruges i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="0a67b-249">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="0a67b-250">Betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-250">Pay cycle (required)</span></span>
- <span data-ttu-id="0a67b-251">Hyppighed for betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-251">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="0a67b-252">Periodens startdato (første lønperiode påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-252">Period start date (first pay period required)</span></span>
- <span data-ttu-id="0a67b-253">Standardbetalingsdato (første lønperiode påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-253">Default payment date (first pay period required)</span></span>

<span data-ttu-id="0a67b-254">Oplysningerne er integreret med Dayforce som løngrupper og adskilles af et land eller område for hver løncyklus.</span><span class="sxs-lookup"><span data-stu-id="0a67b-254">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="0a67b-255">Mindst én periode skal genereres før integration.</span><span class="sxs-lookup"><span data-stu-id="0a67b-255">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="0a67b-256">Dayforce genererer løngruppekalendere og betalingsdatoer, der er baseret på startdatoen for den første lønperiode og den standardbetalingsdato, der er angivet i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0a67b-256">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="0a67b-257">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="0a67b-257">Earning codes</span></span>

<span data-ttu-id="0a67b-258">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="0a67b-258">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="0a67b-259">Koderne har forskellige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="0a67b-259">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="0a67b-260">Følgende oplysninger bruges i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="0a67b-260">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="0a67b-261">Lønkode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-261">Earning Code (required)</span></span>
- <span data-ttu-id="0a67b-262">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0a67b-262">Description</span></span>
- <span data-ttu-id="0a67b-263">Måleenhed</span><span class="sxs-lookup"><span data-stu-id="0a67b-263">Unit of measure</span></span>
- <span data-ttu-id="0a67b-264">Produktiv</span><span class="sxs-lookup"><span data-stu-id="0a67b-264">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="0a67b-265">Arbejderdata</span><span class="sxs-lookup"><span data-stu-id="0a67b-265">Worker data</span></span>

<span data-ttu-id="0a67b-266">Posterne for de forskellige typer arbejdere, du beskæftiger, er vigtige for dine personale- og lønsystemer.</span><span class="sxs-lookup"><span data-stu-id="0a67b-266">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="0a67b-267">De oplysninger, du angiver, kan bruges til at spore arbejdere og personoplysninger.</span><span class="sxs-lookup"><span data-stu-id="0a67b-267">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="0a67b-268">Du kan vedligeholde følgende oplysninger for arbejdere:</span><span class="sxs-lookup"><span data-stu-id="0a67b-268">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="0a67b-269">**Basis** – Vedligehold grundlæggende oplysninger om en arbejder, f.eks. kontaktoplysninger, demografiske oplysninger, identifikationsoplysninger, oplysninger om familie, status for militærtjeneste, oplysninger om udstationering og personlige kontaktpersoner og kontaktpersoner i nødsituationer.</span><span class="sxs-lookup"><span data-stu-id="0a67b-269">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="0a67b-270">**Beskæftigelse** – Vedligehold oplysninger om en arbejders beskæftigelse, f.eks. firma- eller organisationstilhørsforhold, stillingstildeling, start- og slutdatoer, arbejdstilladelse, vilkår for ansættelse, pension, ferie og flytteoplysninger.</span><span class="sxs-lookup"><span data-stu-id="0a67b-270">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="0a67b-271">**Orlov og fravær** – Vedligehold oplysninger om en arbejders fravær, f.eks. arbejdskalendere, fraværstransaktioner og fraværsopsætning.</span><span class="sxs-lookup"><span data-stu-id="0a67b-271">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="0a67b-272">**Kompensation og løn** – Vedligehold oplysninger om en arbejders kompensationsplaner og lønoplysninger, f.eks. tilmelding til planer, priser, ydeevne, provision, skatteoplysninger, pensionering og skattefradrag.</span><span class="sxs-lookup"><span data-stu-id="0a67b-272">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="0a67b-273">Når du angiver arbejderoplysninger, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a67b-273">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="0a67b-274">Generelle oplysninger</span><span class="sxs-lookup"><span data-stu-id="0a67b-274">General information</span></span>

- <span data-ttu-id="0a67b-275">Personalenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-275">Personnel number (required)</span></span>
- <span data-ttu-id="0a67b-276">Fornavn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-276">First name (required)</span></span>
- <span data-ttu-id="0a67b-277">Efternavn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-277">Last name (required)</span></span>
- <span data-ttu-id="0a67b-278">Mellemnavn</span><span class="sxs-lookup"><span data-stu-id="0a67b-278">Middle name</span></span>
- <span data-ttu-id="0a67b-279">Anciennitetsdato</span><span class="sxs-lookup"><span data-stu-id="0a67b-279">Seniority date</span></span>
- <span data-ttu-id="0a67b-280">Kendt som</span><span class="sxs-lookup"><span data-stu-id="0a67b-280">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="0a67b-281">Personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="0a67b-281">Personal information</span></span>

- <span data-ttu-id="0a67b-282">Ægteskabelig status (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-282">Marital status (required)</span></span>
- <span data-ttu-id="0a67b-283">Fødselsdato (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-283">Birth date (required)</span></span>
- <span data-ttu-id="0a67b-284">Køn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-284">Gender (required)</span></span>
- <span data-ttu-id="0a67b-285">Handicappet</span><span class="sxs-lookup"><span data-stu-id="0a67b-285">Person with disabilities</span></span>
- <span data-ttu-id="0a67b-286">Land eller område for nationalitet (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="0a67b-286">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="0a67b-287">Adresseoplysninger</span><span class="sxs-lookup"><span data-stu-id="0a67b-287">Address information</span></span>

- <span data-ttu-id="0a67b-288">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-288">Primary (required)</span></span>
- <span data-ttu-id="0a67b-289">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-289">Country/region (required)</span></span>
- <span data-ttu-id="0a67b-290">Postnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-290">Postal code (required)</span></span>
- <span data-ttu-id="0a67b-291">Gadenummer (påkrævet) (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="0a67b-291">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="0a67b-292">Bygningskomplement (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="0a67b-292">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="0a67b-293">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-293">City (required)</span></span>
- <span data-ttu-id="0a67b-294">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-294">State (required)</span></span>
- <span data-ttu-id="0a67b-295">Region (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-295">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="0a67b-296">Kontaktoplysninger</span><span class="sxs-lookup"><span data-stu-id="0a67b-296">Contact information</span></span> 

- <span data-ttu-id="0a67b-297">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-297">Primary (required)</span></span>
- <span data-ttu-id="0a67b-298">Kontaktpersonens nummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-298">Contact number (required)</span></span>
- <span data-ttu-id="0a67b-299">Forlængelse</span><span class="sxs-lookup"><span data-stu-id="0a67b-299">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="0a67b-300">Lønoplysninger og lønkoder</span><span class="sxs-lookup"><span data-stu-id="0a67b-300">Payroll information and earning codes</span></span>

<span data-ttu-id="0a67b-301">Medarbejdere kan tildeles en bestemt løn med en given betalingshyppighed og have en foretrukken betalingsmetode.</span><span class="sxs-lookup"><span data-stu-id="0a67b-301">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="0a67b-302">Følgende felter bruges i Dayforce til at sikre, at disse præferencer og indstillinger bruges.</span><span class="sxs-lookup"><span data-stu-id="0a67b-302">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="0a67b-303">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="0a67b-303">Earning codes</span></span>

- <span data-ttu-id="0a67b-304">Stilling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-304">Position (required)</span></span>
- <span data-ttu-id="0a67b-305">Lønkode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-305">Earning Code (required)</span></span>
- <span data-ttu-id="0a67b-306">Frekvens (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-306">Frequency (required)</span></span>
- <span data-ttu-id="0a67b-307">Beløb (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-307">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="0a67b-308">Lønoplysninger</span><span class="sxs-lookup"><span data-stu-id="0a67b-308">Payroll information</span></span>

- <span data-ttu-id="0a67b-309">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="0a67b-309">Payment Method</span></span>
- <span data-ttu-id="0a67b-310">Økonomisk område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-310">Economic Region (required)</span></span>
- <span data-ttu-id="0a67b-311">Id for medarbejderfrynsegoder</span><span class="sxs-lookup"><span data-stu-id="0a67b-311">Employee Benefits ID</span></span>
- <span data-ttu-id="0a67b-312">Nationalt id-nummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-312">National ID Number (required)</span></span>
- <span data-ttu-id="0a67b-313">Tjenestenummer hos militær</span><span class="sxs-lookup"><span data-stu-id="0a67b-313">Military Service Number</span></span>
- <span data-ttu-id="0a67b-314">Skifte-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-314">Shift ID (required)</span></span>
- <span data-ttu-id="0a67b-315">Skattenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-315">Tax Number (required)</span></span>
- <span data-ttu-id="0a67b-316">Fagforenings-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-316">Union ID (required)</span></span>
- <span data-ttu-id="0a67b-317">Arbejdsdags-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-317">Work Day ID (required)</span></span>
- <span data-ttu-id="0a67b-318">Arbejdstilladelsesnummer</span><span class="sxs-lookup"><span data-stu-id="0a67b-318">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="0a67b-319">For betalingsmetoden understøtter Mexico **Kontant**, **Check** (firmaets fysiske check), og **Elektronisk betaling**.</span><span class="sxs-lookup"><span data-stu-id="0a67b-319">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="0a67b-320">Hvis der ikke er angivet nogen betalingsmetode, bruges **Check** som standard.</span><span class="sxs-lookup"><span data-stu-id="0a67b-320">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="0a67b-321">Detaljer om ansættelse</span><span class="sxs-lookup"><span data-stu-id="0a67b-321">Employment details</span></span>

<span data-ttu-id="0a67b-322">Detaljeret ansættelseshistorik bruges som vigtige oplysninger til at udlede statusser for en medarbejders ansættelse, fratrædelse og genansættelse i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a67b-322">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="0a67b-323">Dayforce understøtter kun én aktiv ansættelsespost ad gangen.</span><span class="sxs-lookup"><span data-stu-id="0a67b-323">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="0a67b-324">Startdato for ansættelse (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-324">Employment start date (required)</span></span>
- <span data-ttu-id="0a67b-325">Slutdato for ansættelse</span><span class="sxs-lookup"><span data-stu-id="0a67b-325">Employment end date</span></span>
- <span data-ttu-id="0a67b-326">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="0a67b-326">Start date</span></span>
- <span data-ttu-id="0a67b-327">Justeret startdato</span><span class="sxs-lookup"><span data-stu-id="0a67b-327">Adjusted start date</span></span>
- <span data-ttu-id="0a67b-328">Fratrædelsesdato (kræves ved fratrædelse)</span><span class="sxs-lookup"><span data-stu-id="0a67b-328">Termination date (required upon termination)</span></span>
- <span data-ttu-id="0a67b-329">Fratrædelsesårsag (kræves ved fratrædelse)</span><span class="sxs-lookup"><span data-stu-id="0a67b-329">Termination reason (required upon termination)</span></span>

<span data-ttu-id="0a67b-330">Vigtige datoer for en medarbejders udledes ved hjælp af følgende oplysninger.</span><span class="sxs-lookup"><span data-stu-id="0a67b-330">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="0a67b-331">Human Resources</span><span class="sxs-lookup"><span data-stu-id="0a67b-331">Human Resources</span></span>                | <span data-ttu-id="0a67b-332">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a67b-332">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a67b-333">Den seneste ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="0a67b-333">Most recent hire date</span></span> | <span data-ttu-id="0a67b-334">Historikpost for ansættelsesstart for aktuel ikke-afsluttet ansættelse</span><span class="sxs-lookup"><span data-stu-id="0a67b-334">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="0a67b-335">Fratrædelsesdato</span><span class="sxs-lookup"><span data-stu-id="0a67b-335">Termination date</span></span>      | <span data-ttu-id="0a67b-336">Historikpost for fratrædelsesdato for aktuel ikke-afsluttet ansættelse</span><span class="sxs-lookup"><span data-stu-id="0a67b-336">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="0a67b-337">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="0a67b-337">Start date</span></span>            | <span data-ttu-id="0a67b-338">Historikpost for justeret startdato, startdato eller startdato for ansættelse for aktuel ikke-aktiv ansættelse</span><span class="sxs-lookup"><span data-stu-id="0a67b-338">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="0a67b-339">Oprindelig ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="0a67b-339">Original hire date</span></span>    | <span data-ttu-id="0a67b-340">Historikpost for ansættelsesstart for tidligste ansættelse</span><span class="sxs-lookup"><span data-stu-id="0a67b-340">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="0a67b-341">Kompensation</span><span class="sxs-lookup"><span data-stu-id="0a67b-341">Compensation</span></span>

<span data-ttu-id="0a67b-342">En fast lønstruktur skal tilknyttes hver medarbejders primære stilling gennem hele ansættelsesperioden.</span><span class="sxs-lookup"><span data-stu-id="0a67b-342">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="0a67b-343">Denne periode starter på den dato, hvor medarbejderen blev ansat (eller ansættelsesstartdatoen) og fortsætter, indtil fratrædelsen.</span><span class="sxs-lookup"><span data-stu-id="0a67b-343">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="0a67b-344">Ikrafttrædelsesdato (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-344">Effective Date (required)</span></span>
- <span data-ttu-id="0a67b-345">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="0a67b-345">Expiration date</span></span>
- <span data-ttu-id="0a67b-346">Lønsats (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-346">Pay Rate (required)</span></span>
- <span data-ttu-id="0a67b-347">Konverteringer af lønsats (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-347">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="0a67b-348">Årlig ækvivalent (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-348">Annual equivalent (required)</span></span>
- <span data-ttu-id="0a67b-349">Timebaseret ækvivalent (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-349">Hourly equivalent (required)</span></span>

<span data-ttu-id="0a67b-350">Hvis en timeansat medarbejder har flere stillinger, indlæses den faste løn for den primære stilling i Dayforce, som basissats/-løn på medarbejderniveau.</span><span class="sxs-lookup"><span data-stu-id="0a67b-350">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="0a67b-351">For ikke-primære stillinger gemmes timesatsen i den tilsvarende position i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a67b-351">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="0a67b-352">Hvis en funktionær har flere stillinger, afledes den kumulative timesats og årlig gage på tværs af alle aktive stillinger og bruges som basissats/-gage på medarbejderniveau.</span><span class="sxs-lookup"><span data-stu-id="0a67b-352">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="0a67b-353">Identifikationsnumre</span><span class="sxs-lookup"><span data-stu-id="0a67b-353">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="0a67b-354">Social Security-identifikator</span><span class="sxs-lookup"><span data-stu-id="0a67b-354">Social Security identifier</span></span> 

<span data-ttu-id="0a67b-355">Alle medarbejdere skal have én primær identifikator.</span><span class="sxs-lookup"><span data-stu-id="0a67b-355">Every employee must have one primary identifier.</span></span> <span data-ttu-id="0a67b-356">Identifikatoren skal være af **SSN**-identifikationstypen</span><span class="sxs-lookup"><span data-stu-id="0a67b-356">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="0a67b-357">I Dayforce afledes den automatisk som medarbejderens Social Security-identifikator, der er påkrævet ved ansættelse.</span><span class="sxs-lookup"><span data-stu-id="0a67b-357">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="0a67b-358">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-358">Primary (required)</span></span>
- <span data-ttu-id="0a67b-359">Identifikationstype = "SSN"</span><span class="sxs-lookup"><span data-stu-id="0a67b-359">Identification Type = "SSN"</span></span>
- <span data-ttu-id="0a67b-360">Udstedt den</span><span class="sxs-lookup"><span data-stu-id="0a67b-360">Issued Date</span></span>
- <span data-ttu-id="0a67b-361">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="0a67b-361">Expiration Date</span></span>

<span data-ttu-id="0a67b-362">Medarbejdere kan angive flere identifikationsnumre af **SSN**-identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="0a67b-362">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="0a67b-363">Men det er kun den post, der er markeret som **Primær**, som er integreret i Dayforce, uanset om nummeret er aktivt eller udløbet.</span><span class="sxs-lookup"><span data-stu-id="0a67b-363">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="0a67b-364">Bankkonto og udbetalinger</span><span class="sxs-lookup"><span data-stu-id="0a67b-364">Bank accounts and disbursements</span></span>

<span data-ttu-id="0a67b-365">Gyldige bankkontooplysninger skal angives for enhver medarbejder, der vælger at blive betalt via bankkontooverførsler.</span><span class="sxs-lookup"><span data-stu-id="0a67b-365">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="0a67b-366">Human Resources</span><span class="sxs-lookup"><span data-stu-id="0a67b-366">Human Resources</span></span>                         | <span data-ttu-id="0a67b-367">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a67b-367">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a67b-368">Bankkontonummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-368">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="0a67b-369">SWIFT-kode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-369">SWIFT code (required)</span></span>          | <span data-ttu-id="0a67b-370">Feltet **Bank-id** bruges ved behandling af løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="0a67b-370">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="0a67b-371">Afdelingsnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-371">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="0a67b-372">Bankkontotype (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-372">Bank account type (required)</span></span>   | <span data-ttu-id="0a67b-373">Feltet **Kontotype** bruges ved behandling af løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="0a67b-373">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="0a67b-374">Understøttede værdier omfatter **Check** og **Løn**.</span><span class="sxs-lookup"><span data-stu-id="0a67b-374">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="0a67b-375">Medarbejdere, der vælger at betales via bankkontooverførsler, skal angive et link til en restbeløbskonto, der hører under en juridisk enhed, som har primær adresse i Mexico og er knyttet til en gyldig bankkonto fra en mexicansk bank.</span><span class="sxs-lookup"><span data-stu-id="0a67b-375">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="0a67b-376">Alle andre restbeløbskonti ignoreres.</span><span class="sxs-lookup"><span data-stu-id="0a67b-376">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="0a67b-377">Adresseoplysninger</span><span class="sxs-lookup"><span data-stu-id="0a67b-377">Address information</span></span>

<span data-ttu-id="0a67b-378">Alle medarbejdere skal have én primær placering.</span><span class="sxs-lookup"><span data-stu-id="0a67b-378">Every employee must have one primary location.</span></span> <span data-ttu-id="0a67b-379">I Dayforce bruges denne placering til at bestemme medarbejderens primære opholdssted til skattemæssige formål.</span><span class="sxs-lookup"><span data-stu-id="0a67b-379">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="0a67b-380">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-380">Primary (required)</span></span>
- <span data-ttu-id="0a67b-381">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-381">Country/region (required)</span></span>
- <span data-ttu-id="0a67b-382">Postnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-382">Zip/postal code (required)</span></span>
- <span data-ttu-id="0a67b-383">Gade (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-383">Street (required)</span></span>
- <span data-ttu-id="0a67b-384">Gadenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-384">Street Number (required)</span></span>
- <span data-ttu-id="0a67b-385">Bygningskomplement</span><span class="sxs-lookup"><span data-stu-id="0a67b-385">Building Complement</span></span>
- <span data-ttu-id="0a67b-386">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-386">City (required)</span></span>
- <span data-ttu-id="0a67b-387">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-387">State (required)</span></span>
- <span data-ttu-id="0a67b-388">Region (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-388">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="0a67b-389">Konfigurere dataene for at generere løn i USA og Canada</span><span class="sxs-lookup"><span data-stu-id="0a67b-389">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="0a67b-390">Hvis du genererer løn for medarbejdere i USA og Canada, skal følgende elementer konfigureres:</span><span class="sxs-lookup"><span data-stu-id="0a67b-390">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="0a67b-391">Der kræves afdelinger til stillinger.</span><span class="sxs-lookup"><span data-stu-id="0a67b-391">Departments are required on positions.</span></span>
- <span data-ttu-id="0a67b-392">Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="0a67b-392">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="0a67b-393">Du kan konfigurere Human Resources til at kræve, at der angives en afdeling for stillinger.</span><span class="sxs-lookup"><span data-stu-id="0a67b-393">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="0a67b-394">For at gøre dette skal du gå til **Human Resourcests delte stillinger > Stillinger > Kræv afdelinger for stillinger**.</span><span class="sxs-lookup"><span data-stu-id="0a67b-394">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="0a67b-395">Det anbefales, at denne indstilling gennemtvinges i forbindelse med integrationen.</span><span class="sxs-lookup"><span data-stu-id="0a67b-395">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="0a67b-396">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="0a67b-396">Job types</span></span>

<span data-ttu-id="0a67b-397">Jobtyper bruges til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="0a67b-397">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="0a67b-398">Jobtyper kræves for at behandle løn i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="0a67b-398">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="0a67b-399">Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="0a67b-399">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="0a67b-400">Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.</span><span class="sxs-lookup"><span data-stu-id="0a67b-400">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="0a67b-401">Der kræves følgende jobtyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="0a67b-401">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="0a67b-402">Jobtype</span><span class="sxs-lookup"><span data-stu-id="0a67b-402">Job type</span></span>   | <span data-ttu-id="0a67b-403">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0a67b-403">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="0a67b-404">Pr. time</span><span class="sxs-lookup"><span data-stu-id="0a67b-404">Hourly</span></span>     | <span data-ttu-id="0a67b-405">Pr. time</span><span class="sxs-lookup"><span data-stu-id="0a67b-405">Hourly</span></span>      |
| <span data-ttu-id="0a67b-406">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="0a67b-406">Salaried</span></span>   | <span data-ttu-id="0a67b-407">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="0a67b-407">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="0a67b-408">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="0a67b-408">Position types</span></span> 

<span data-ttu-id="0a67b-409">Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet.</span><span class="sxs-lookup"><span data-stu-id="0a67b-409">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="0a67b-410">Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="0a67b-410">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="0a67b-411">Der kræves følgende stillingstyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="0a67b-411">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="0a67b-412">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="0a67b-412">Position type</span></span>   | <span data-ttu-id="0a67b-413">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0a67b-413">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="0a67b-414">Fuld tid</span><span class="sxs-lookup"><span data-stu-id="0a67b-414">Full-time</span></span>       | <span data-ttu-id="0a67b-415">Fuldtidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="0a67b-415">Full time employee</span></span> |
| <span data-ttu-id="0a67b-416">Deltid</span><span class="sxs-lookup"><span data-stu-id="0a67b-416">Part-time</span></span>       | <span data-ttu-id="0a67b-417">Deltidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="0a67b-417">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="0a67b-418">Årsagskoder</span><span class="sxs-lookup"><span data-stu-id="0a67b-418">Reason codes</span></span>

<span data-ttu-id="0a67b-419">Årsagskoder indeholder oplysninger om status for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="0a67b-419">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="0a67b-420">Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.</span><span class="sxs-lookup"><span data-stu-id="0a67b-420">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="0a67b-421">Der kræves følgende årsagskoder og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="0a67b-421">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="0a67b-422">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="0a67b-422">Reason code</span></span>    | <span data-ttu-id="0a67b-423">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0a67b-423">Description</span></span>      | <span data-ttu-id="0a67b-424">Anvendelige scenarier</span><span class="sxs-lookup"><span data-stu-id="0a67b-424">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="0a67b-425">OPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="0a67b-425">RESIGNATION</span></span>    | <span data-ttu-id="0a67b-426">Opsigelse</span><span class="sxs-lookup"><span data-stu-id="0a67b-426">Resignation</span></span>      | <span data-ttu-id="0a67b-427">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="0a67b-427">Terminate worker</span></span>     |
| <span data-ttu-id="0a67b-428">OPHØR</span><span class="sxs-lookup"><span data-stu-id="0a67b-428">TERMINATION</span></span>    | <span data-ttu-id="0a67b-429">Ophør</span><span class="sxs-lookup"><span data-stu-id="0a67b-429">Termination</span></span>      | <span data-ttu-id="0a67b-430">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="0a67b-430">Terminate worker</span></span>     |
| <span data-ttu-id="0a67b-431">PENSION</span><span class="sxs-lookup"><span data-stu-id="0a67b-431">RETIREMENT</span></span>     | <span data-ttu-id="0a67b-432">Pension</span><span class="sxs-lookup"><span data-stu-id="0a67b-432">Retirement</span></span>       | <span data-ttu-id="0a67b-433">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="0a67b-433">Terminate worker</span></span>     |
| <span data-ttu-id="0a67b-434">ANDET</span><span class="sxs-lookup"><span data-stu-id="0a67b-434">OTHER</span></span>          | <span data-ttu-id="0a67b-435">Andre årsager</span><span class="sxs-lookup"><span data-stu-id="0a67b-435">Other Reasons</span></span>    | <span data-ttu-id="0a67b-436">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="0a67b-436">Terminate worker</span></span>     |
| <span data-ttu-id="0a67b-437">DØDSFALD</span><span class="sxs-lookup"><span data-stu-id="0a67b-437">DEATH</span></span>          | <span data-ttu-id="0a67b-438">Dødsfald</span><span class="sxs-lookup"><span data-stu-id="0a67b-438">Death</span></span>            | <span data-ttu-id="0a67b-439">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="0a67b-439">Terminate worker</span></span>     |
| <span data-ttu-id="0a67b-440">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="0a67b-440">LEAVEOFABSENCE</span></span> | <span data-ttu-id="0a67b-441">Orlov</span><span class="sxs-lookup"><span data-stu-id="0a67b-441">Leave of Absence</span></span> | <span data-ttu-id="0a67b-442">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="0a67b-442">Terminate worker</span></span>     |
| <span data-ttu-id="0a67b-443">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="0a67b-443">CONTRACTEND</span></span>    | <span data-ttu-id="0a67b-444">Kontraktudløb</span><span class="sxs-lookup"><span data-stu-id="0a67b-444">End of Contract</span></span>  | <span data-ttu-id="0a67b-445">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="0a67b-445">Terminate worker</span></span>     |
| <span data-ttu-id="0a67b-446">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="0a67b-446">SALARYCHANGE</span></span>   | <span data-ttu-id="0a67b-447">Ændring af løn</span><span class="sxs-lookup"><span data-stu-id="0a67b-447">Change of Salary</span></span> | <span data-ttu-id="0a67b-448">Kompensation</span><span class="sxs-lookup"><span data-stu-id="0a67b-448">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="0a67b-449">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="0a67b-449">Marital status</span></span>

<span data-ttu-id="0a67b-450">Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="0a67b-450">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="0a67b-451">Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a67b-451">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="0a67b-452">Human Resources</span><span class="sxs-lookup"><span data-stu-id="0a67b-452">Human Resources</span></span>                 | <span data-ttu-id="0a67b-453">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a67b-453">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="0a67b-454">Gift</span><span class="sxs-lookup"><span data-stu-id="0a67b-454">Married</span></span>                | <span data-ttu-id="0a67b-455">Gift</span><span class="sxs-lookup"><span data-stu-id="0a67b-455">Married</span></span>              |
| <span data-ttu-id="0a67b-456">Enlig</span><span class="sxs-lookup"><span data-stu-id="0a67b-456">Single</span></span>                 | <span data-ttu-id="0a67b-457">Enlig</span><span class="sxs-lookup"><span data-stu-id="0a67b-457">Single</span></span>               |
| <span data-ttu-id="0a67b-458">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="0a67b-458">Widowed</span></span>                | <span data-ttu-id="0a67b-459">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="0a67b-459">Widowed</span></span>              |
| <span data-ttu-id="0a67b-460">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="0a67b-460">Divorced</span></span>               | <span data-ttu-id="0a67b-461">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="0a67b-461">Divorced</span></span>             |
| <span data-ttu-id="0a67b-462">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="0a67b-462">Registered Partnership</span></span> | <span data-ttu-id="0a67b-463">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="0a67b-463">Domestic Partnership</span></span> |
| <span data-ttu-id="0a67b-464">None</span><span class="sxs-lookup"><span data-stu-id="0a67b-464">None</span></span>                   | <span data-ttu-id="0a67b-465">None</span><span class="sxs-lookup"><span data-stu-id="0a67b-465">None</span></span>                 |
| <span data-ttu-id="0a67b-466">Samlever</span><span class="sxs-lookup"><span data-stu-id="0a67b-466">Cohabiting</span></span>             | <span data-ttu-id="0a67b-467">Samlever</span><span class="sxs-lookup"><span data-stu-id="0a67b-467">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="0a67b-468">Køn</span><span class="sxs-lookup"><span data-stu-id="0a67b-468">Gender</span></span>

<span data-ttu-id="0a67b-469">Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="0a67b-469">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="0a67b-470">Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a67b-470">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="0a67b-471">Human Resources</span><span class="sxs-lookup"><span data-stu-id="0a67b-471">Human Resources</span></span>       | <span data-ttu-id="0a67b-472">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a67b-472">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="0a67b-473">Mand</span><span class="sxs-lookup"><span data-stu-id="0a67b-473">Male</span></span>         | <span data-ttu-id="0a67b-474">Mand</span><span class="sxs-lookup"><span data-stu-id="0a67b-474">Male</span></span>            |
| <span data-ttu-id="0a67b-475">Kvinde</span><span class="sxs-lookup"><span data-stu-id="0a67b-475">Female</span></span>       | <span data-ttu-id="0a67b-476">Kvinde</span><span class="sxs-lookup"><span data-stu-id="0a67b-476">Female</span></span>          |
| <span data-ttu-id="0a67b-477">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="0a67b-477">Non-specific</span></span> | <span data-ttu-id="0a67b-478">*Understøttes ikke*</span><span class="sxs-lookup"><span data-stu-id="0a67b-478">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="0a67b-479">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="0a67b-479">Earning codes</span></span>

<span data-ttu-id="0a67b-480">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="0a67b-480">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="0a67b-481">Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="0a67b-481">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="0a67b-482">Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="0a67b-482">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="0a67b-483">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="0a67b-483">Supported frequencies</span></span>

- <span data-ttu-id="0a67b-484">Alt</span><span class="sxs-lookup"><span data-stu-id="0a67b-484">All</span></span>
- <span data-ttu-id="0a67b-485">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="0a67b-485">EVERYPAY</span></span>
- <span data-ttu-id="0a67b-486">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="0a67b-486">EACHPAYPERIOD</span></span>
- <span data-ttu-id="0a67b-487">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="0a67b-487">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="0a67b-488">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="0a67b-488">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="0a67b-489">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-489">1OFMTH</span></span>
- <span data-ttu-id="0a67b-490">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-490">LASTOFMTH</span></span>
- <span data-ttu-id="0a67b-491">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-491">2OFMTH</span></span>
- <span data-ttu-id="0a67b-492">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-492">3OFMTH</span></span>
- <span data-ttu-id="0a67b-493">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-493">4OFMTH</span></span>
- <span data-ttu-id="0a67b-494">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-494">5OFMTH</span></span>
- <span data-ttu-id="0a67b-495">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-495">1N2OFMTH</span></span>
- <span data-ttu-id="0a67b-496">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-496">3N4OFMTH</span></span>
- <span data-ttu-id="0a67b-497">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-497">1N3OFMTH</span></span>
- <span data-ttu-id="0a67b-498">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-498">1N4OFMTH</span></span>
- <span data-ttu-id="0a67b-499">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-499">2N3OFMTH</span></span>
- <span data-ttu-id="0a67b-500">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-500">2N4OFMTH</span></span>
- <span data-ttu-id="0a67b-501">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-501">1N2N3OFMTH</span></span>
- <span data-ttu-id="0a67b-502">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-502">1N2N4OFMTH</span></span>
- <span data-ttu-id="0a67b-503">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-503">1N3N4OFMTH</span></span>
- <span data-ttu-id="0a67b-504">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-504">2N3N4OFMTH</span></span>
- <span data-ttu-id="0a67b-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="0a67b-506">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="0a67b-506">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="0a67b-507">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="0a67b-507">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="0a67b-508">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="0a67b-508">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="0a67b-509">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="0a67b-509">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="0a67b-510">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="0a67b-510">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="0a67b-511">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="0a67b-511">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="0a67b-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="0a67b-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="0a67b-513">Adresser</span><span class="sxs-lookup"><span data-stu-id="0a67b-513">Addresses</span></span>

<span data-ttu-id="0a67b-514">Identifikation af specifikke koder for land eller område, stat og region (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende.</span><span class="sxs-lookup"><span data-stu-id="0a67b-514">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="0a67b-515">Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.</span><span class="sxs-lookup"><span data-stu-id="0a67b-515">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="0a67b-516">Human Resources</span><span class="sxs-lookup"><span data-stu-id="0a67b-516">Human Resources</span></span>          | <span data-ttu-id="0a67b-517">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a67b-517">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="0a67b-518">Land/område</span><span class="sxs-lookup"><span data-stu-id="0a67b-518">Country/Region</span></span>  | <span data-ttu-id="0a67b-519">Landekode</span><span class="sxs-lookup"><span data-stu-id="0a67b-519">Country Code</span></span>          |
| <span data-ttu-id="0a67b-520">Postnummer</span><span class="sxs-lookup"><span data-stu-id="0a67b-520">Zip/Postal Code</span></span> | <span data-ttu-id="0a67b-521">Postnummer</span><span class="sxs-lookup"><span data-stu-id="0a67b-521">Postal Code</span></span>           |
| <span data-ttu-id="0a67b-522">Status</span><span class="sxs-lookup"><span data-stu-id="0a67b-522">State</span></span>           | <span data-ttu-id="0a67b-523">Statskode</span><span class="sxs-lookup"><span data-stu-id="0a67b-523">State Code</span></span>            |
| <span data-ttu-id="0a67b-524">Bynavn</span><span class="sxs-lookup"><span data-stu-id="0a67b-524">City</span></span>            | <span data-ttu-id="0a67b-525">Bynavn</span><span class="sxs-lookup"><span data-stu-id="0a67b-525">City</span></span>                  |
| <span data-ttu-id="0a67b-526">Region</span><span class="sxs-lookup"><span data-stu-id="0a67b-526">County</span></span>          | <span data-ttu-id="0a67b-527">Område (kommune)</span><span class="sxs-lookup"><span data-stu-id="0a67b-527">County (Municipality)</span></span> |
| <span data-ttu-id="0a67b-528">Gade</span><span class="sxs-lookup"><span data-stu-id="0a67b-528">Street</span></span>          | <span data-ttu-id="0a67b-529">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="0a67b-529">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="0a67b-530">Skatteområder</span><span class="sxs-lookup"><span data-stu-id="0a67b-530">Tax regions</span></span>

<span data-ttu-id="0a67b-531">Skatteområder bruges til at bestemme den relevante skat, der skal anvendes ved løngenerering.</span><span class="sxs-lookup"><span data-stu-id="0a67b-531">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="0a67b-532">Skatteområder er tilknyttet Dayforce som placeringsadresser.</span><span class="sxs-lookup"><span data-stu-id="0a67b-532">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="0a67b-533">Standardskatteområder skal knyttes til arbejderens aktive stilling.</span><span class="sxs-lookup"><span data-stu-id="0a67b-533">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="0a67b-534">Skatteområde (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-534">Tax region (required)</span></span>
- <span data-ttu-id="0a67b-535">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-535">Country/Region (required)</span></span>
- <span data-ttu-id="0a67b-536">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-536">State (required)</span></span>
- <span data-ttu-id="0a67b-537">Region</span><span class="sxs-lookup"><span data-stu-id="0a67b-537">County</span></span> 
- <span data-ttu-id="0a67b-538">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0a67b-538">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="0a67b-539">Konfigurere dataene for at generere løn i Mexico</span><span class="sxs-lookup"><span data-stu-id="0a67b-539">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="0a67b-540">Hvis du genererer løn for medarbejdere i Mexico skal følgende elementer konfigureres:</span><span class="sxs-lookup"><span data-stu-id="0a67b-540">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="0a67b-541">Der kræves afdelinger til stillinger.</span><span class="sxs-lookup"><span data-stu-id="0a67b-541">Departments are required on positions.</span></span>
- <span data-ttu-id="0a67b-542">Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="0a67b-542">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="0a67b-543">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="0a67b-543">Job types</span></span>

<span data-ttu-id="0a67b-544">Jobtyper bruges til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="0a67b-544">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="0a67b-545">Jobtyper kræves for at behandle løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="0a67b-545">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="0a67b-546">Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="0a67b-546">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="0a67b-547">Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.</span><span class="sxs-lookup"><span data-stu-id="0a67b-547">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="0a67b-548">Der kræves følgende jobtyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="0a67b-548">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="0a67b-549">Jobtype</span><span class="sxs-lookup"><span data-stu-id="0a67b-549">Job type</span></span>   | <span data-ttu-id="0a67b-550">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0a67b-550">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="0a67b-551">Pr. time</span><span class="sxs-lookup"><span data-stu-id="0a67b-551">Hourly</span></span>     | <span data-ttu-id="0a67b-552">MX Pr. time</span><span class="sxs-lookup"><span data-stu-id="0a67b-552">MX Hourly</span></span>   |
| <span data-ttu-id="0a67b-553">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="0a67b-553">Salaried</span></span>   | <span data-ttu-id="0a67b-554">MX Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="0a67b-554">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="0a67b-555">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="0a67b-555">Position types</span></span> 

<span data-ttu-id="0a67b-556">Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet.</span><span class="sxs-lookup"><span data-stu-id="0a67b-556">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="0a67b-557">Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="0a67b-557">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="0a67b-558">Der kræves følgende stillingstyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="0a67b-558">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="0a67b-559">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="0a67b-559">Position type</span></span>   | <span data-ttu-id="0a67b-560">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0a67b-560">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="0a67b-561">Fuld tid</span><span class="sxs-lookup"><span data-stu-id="0a67b-561">Full-time</span></span>       | <span data-ttu-id="0a67b-562">Fuldtidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="0a67b-562">Full time employee</span></span> |
| <span data-ttu-id="0a67b-563">Deltid</span><span class="sxs-lookup"><span data-stu-id="0a67b-563">Part-time</span></span>       | <span data-ttu-id="0a67b-564">Deltidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="0a67b-564">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="0a67b-565">Årsagskoder</span><span class="sxs-lookup"><span data-stu-id="0a67b-565">Reason codes</span></span>

<span data-ttu-id="0a67b-566">Årsagskoder indeholder oplysninger om status for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="0a67b-566">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="0a67b-567">Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.</span><span class="sxs-lookup"><span data-stu-id="0a67b-567">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="0a67b-568">Der kræves følgende årsagskoder og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="0a67b-568">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="0a67b-569">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="0a67b-569">Reason code</span></span>            | <span data-ttu-id="0a67b-570">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0a67b-570">Description</span></span>                    | <span data-ttu-id="0a67b-571">Anvendelige scenarier</span><span class="sxs-lookup"><span data-stu-id="0a67b-571">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="0a67b-572">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="0a67b-572">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="0a67b-573">Afgang før første løn</span><span class="sxs-lookup"><span data-stu-id="0a67b-573">Departure before first payroll</span></span> | <span data-ttu-id="0a67b-574">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="0a67b-574">Terminate worker</span></span>     |
| <span data-ttu-id="0a67b-575">OPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="0a67b-575">RESIGNATION</span></span>            | <span data-ttu-id="0a67b-576">Opsigelse</span><span class="sxs-lookup"><span data-stu-id="0a67b-576">Resignation</span></span>                    | <span data-ttu-id="0a67b-577">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="0a67b-577">Terminate worker</span></span>     |
| <span data-ttu-id="0a67b-578">PENSION</span><span class="sxs-lookup"><span data-stu-id="0a67b-578">PENSION</span></span>                | <span data-ttu-id="0a67b-579">Pension</span><span class="sxs-lookup"><span data-stu-id="0a67b-579">Pension</span></span>                        | <span data-ttu-id="0a67b-580">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="0a67b-580">Terminate worker</span></span>     |
| <span data-ttu-id="0a67b-581">OPHØR</span><span class="sxs-lookup"><span data-stu-id="0a67b-581">TERMINATION</span></span>            | <span data-ttu-id="0a67b-582">Ophør</span><span class="sxs-lookup"><span data-stu-id="0a67b-582">Termination</span></span>                    | <span data-ttu-id="0a67b-583">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="0a67b-583">Terminate worker</span></span>     |
| <span data-ttu-id="0a67b-584">PENSION</span><span class="sxs-lookup"><span data-stu-id="0a67b-584">RETIREMENT</span></span>             | <span data-ttu-id="0a67b-585">Pension</span><span class="sxs-lookup"><span data-stu-id="0a67b-585">Retirement</span></span>                     | <span data-ttu-id="0a67b-586">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="0a67b-586">Terminate worker</span></span>     |
| <span data-ttu-id="0a67b-587">FRAVÆRENDE</span><span class="sxs-lookup"><span data-stu-id="0a67b-587">ABSENTEE</span></span>               | <span data-ttu-id="0a67b-588">Fraværende</span><span class="sxs-lookup"><span data-stu-id="0a67b-588">Absentee</span></span>                       | <span data-ttu-id="0a67b-589">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="0a67b-589">Terminate worker</span></span>     |
| <span data-ttu-id="0a67b-590">ANDET</span><span class="sxs-lookup"><span data-stu-id="0a67b-590">OTHER</span></span>                  | <span data-ttu-id="0a67b-591">Andre årsager</span><span class="sxs-lookup"><span data-stu-id="0a67b-591">Other Reasons</span></span>                  | <span data-ttu-id="0a67b-592">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="0a67b-592">Terminate worker</span></span>     |
| <span data-ttu-id="0a67b-593">LUKNING</span><span class="sxs-lookup"><span data-stu-id="0a67b-593">CLOSURE</span></span>                | <span data-ttu-id="0a67b-594">Virksomhedslukning</span><span class="sxs-lookup"><span data-stu-id="0a67b-594">Business Closure</span></span>               | <span data-ttu-id="0a67b-595">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="0a67b-595">Terminate worker</span></span>     |
| <span data-ttu-id="0a67b-596">DØDSFALD</span><span class="sxs-lookup"><span data-stu-id="0a67b-596">DEATH</span></span>                  | <span data-ttu-id="0a67b-597">Dødsfald</span><span class="sxs-lookup"><span data-stu-id="0a67b-597">Death</span></span>                          | <span data-ttu-id="0a67b-598">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="0a67b-598">Terminate worker</span></span>     |
| <span data-ttu-id="0a67b-599">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="0a67b-599">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="0a67b-600">Orlov</span><span class="sxs-lookup"><span data-stu-id="0a67b-600">Leave of Absence</span></span>               | <span data-ttu-id="0a67b-601">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="0a67b-601">Terminate worker</span></span>     |
| <span data-ttu-id="0a67b-602">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="0a67b-602">CONTRACTEND</span></span>            | <span data-ttu-id="0a67b-603">Kontraktudløb</span><span class="sxs-lookup"><span data-stu-id="0a67b-603">End of Contract</span></span>                | <span data-ttu-id="0a67b-604">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="0a67b-604">Terminate worker</span></span>     |
| <span data-ttu-id="0a67b-605">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="0a67b-605">SALARYCHANGE</span></span>           | <span data-ttu-id="0a67b-606">Ændring af løn</span><span class="sxs-lookup"><span data-stu-id="0a67b-606">Change of Salary</span></span>               | <span data-ttu-id="0a67b-607">Kompensation</span><span class="sxs-lookup"><span data-stu-id="0a67b-607">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="0a67b-608">Ansættelsesvilkår</span><span class="sxs-lookup"><span data-stu-id="0a67b-608">Terms of employment</span></span>

<span data-ttu-id="0a67b-609">Ansættelsesvilkår bruges til at oprette kategorier for ansættelsesvilkår.</span><span class="sxs-lookup"><span data-stu-id="0a67b-609">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="0a67b-610">Vilkårene knyttes til Dayforce som beskæftigelsesindikatorværdier.</span><span class="sxs-lookup"><span data-stu-id="0a67b-610">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="0a67b-611">Følgende begreber for beskæftigelse og beskrivelser er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="0a67b-611">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="0a67b-612">Ansættelsesvilkår</span><span class="sxs-lookup"><span data-stu-id="0a67b-612">Terms of employment</span></span>   | <span data-ttu-id="0a67b-613">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0a67b-613">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="0a67b-614">Regulær</span><span class="sxs-lookup"><span data-stu-id="0a67b-614">Regular</span></span>               | <span data-ttu-id="0a67b-615">Regulær</span><span class="sxs-lookup"><span data-stu-id="0a67b-615">Regular</span></span>     |
| <span data-ttu-id="0a67b-616">Direkte</span><span class="sxs-lookup"><span data-stu-id="0a67b-616">Direct</span></span>                | <span data-ttu-id="0a67b-617">Direkte</span><span class="sxs-lookup"><span data-stu-id="0a67b-617">Direct</span></span>      |
| <span data-ttu-id="0a67b-618">Turnustjeneste</span><span class="sxs-lookup"><span data-stu-id="0a67b-618">Internship</span></span>            | <span data-ttu-id="0a67b-619">Turnustjeneste</span><span class="sxs-lookup"><span data-stu-id="0a67b-619">Internship</span></span>  |
| <span data-ttu-id="0a67b-620">Permanent</span><span class="sxs-lookup"><span data-stu-id="0a67b-620">Permanent</span></span>             | <span data-ttu-id="0a67b-621">Permanent</span><span class="sxs-lookup"><span data-stu-id="0a67b-621">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="0a67b-622">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="0a67b-622">Marital status</span></span>

<span data-ttu-id="0a67b-623">Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="0a67b-623">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="0a67b-624">Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a67b-624">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="0a67b-625">Human Resources</span><span class="sxs-lookup"><span data-stu-id="0a67b-625">Human Resources</span></span>                 | <span data-ttu-id="0a67b-626">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a67b-626">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="0a67b-627">Gift</span><span class="sxs-lookup"><span data-stu-id="0a67b-627">Married</span></span>                | <span data-ttu-id="0a67b-628">Gift</span><span class="sxs-lookup"><span data-stu-id="0a67b-628">Married</span></span>                   |
| <span data-ttu-id="0a67b-629">Enlig</span><span class="sxs-lookup"><span data-stu-id="0a67b-629">Single</span></span>                 | <span data-ttu-id="0a67b-630">Enlig</span><span class="sxs-lookup"><span data-stu-id="0a67b-630">Single</span></span>                    |
| <span data-ttu-id="0a67b-631">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="0a67b-631">Widowed</span></span>                | <span data-ttu-id="0a67b-632">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="0a67b-632">Widowed</span></span>                   |
| <span data-ttu-id="0a67b-633">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="0a67b-633">Divorced</span></span>               | <span data-ttu-id="0a67b-634">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="0a67b-634">Divorced</span></span>                  |
| <span data-ttu-id="0a67b-635">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="0a67b-635">Registered Partnership</span></span> | <span data-ttu-id="0a67b-636">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="0a67b-636">Domestic Partnership</span></span>      |
| <span data-ttu-id="0a67b-637">None</span><span class="sxs-lookup"><span data-stu-id="0a67b-637">None</span></span>                   | <span data-ttu-id="0a67b-638">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="0a67b-638">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="0a67b-639">Samlever</span><span class="sxs-lookup"><span data-stu-id="0a67b-639">Cohabiting</span></span>             | <span data-ttu-id="0a67b-640">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="0a67b-640">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="0a67b-641">Køn</span><span class="sxs-lookup"><span data-stu-id="0a67b-641">Gender</span></span>

<span data-ttu-id="0a67b-642">Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="0a67b-642">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="0a67b-643">Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a67b-643">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="0a67b-644">Human Resources</span><span class="sxs-lookup"><span data-stu-id="0a67b-644">Human Resources</span></span>       | <span data-ttu-id="0a67b-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a67b-645">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="0a67b-646">Mand</span><span class="sxs-lookup"><span data-stu-id="0a67b-646">Male</span></span>         | <span data-ttu-id="0a67b-647">Mand</span><span class="sxs-lookup"><span data-stu-id="0a67b-647">Male</span></span>                      |
| <span data-ttu-id="0a67b-648">Kvinde</span><span class="sxs-lookup"><span data-stu-id="0a67b-648">Female</span></span>       | <span data-ttu-id="0a67b-649">Kvinde</span><span class="sxs-lookup"><span data-stu-id="0a67b-649">Female</span></span>                    |
| <span data-ttu-id="0a67b-650">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="0a67b-650">Non-specific</span></span> | <span data-ttu-id="0a67b-651">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="0a67b-651">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="0a67b-652">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="0a67b-652">Payment method</span></span>

<span data-ttu-id="0a67b-653">Betalingsmetoder giver medarbejderen og virksomheden en måde til at beskrive, hvordan medarbejdere skal betales.</span><span class="sxs-lookup"><span data-stu-id="0a67b-653">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="0a67b-654">Betalingsmåder knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="0a67b-654">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="0a67b-655">Følgende tabel viser, hvordan betalingsmetoder knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a67b-655">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="0a67b-656">Human Resources</span><span class="sxs-lookup"><span data-stu-id="0a67b-656">Human Resources</span></span>             | <span data-ttu-id="0a67b-657">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a67b-657">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="0a67b-658">Indløsning</span><span class="sxs-lookup"><span data-stu-id="0a67b-658">Cash</span></span>               | <span data-ttu-id="0a67b-659">Indløsning</span><span class="sxs-lookup"><span data-stu-id="0a67b-659">Cash</span></span>                      |
| <span data-ttu-id="0a67b-660">Elektronisk betaling</span><span class="sxs-lookup"><span data-stu-id="0a67b-660">Electronic Payment</span></span> | <span data-ttu-id="0a67b-661">Ompostering</span><span class="sxs-lookup"><span data-stu-id="0a67b-661">Transfer</span></span>                  |
| <span data-ttu-id="0a67b-662">Check</span><span class="sxs-lookup"><span data-stu-id="0a67b-662">Check</span></span>              | <span data-ttu-id="0a67b-663">Check</span><span class="sxs-lookup"><span data-stu-id="0a67b-663">Cheque</span></span>                    |
| <span data-ttu-id="0a67b-664">Bankanvisning</span><span class="sxs-lookup"><span data-stu-id="0a67b-664">Bank Draft</span></span>         | <span data-ttu-id="0a67b-665">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="0a67b-665">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="0a67b-666">Andre</span><span class="sxs-lookup"><span data-stu-id="0a67b-666">Other</span></span>              | <span data-ttu-id="0a67b-667">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="0a67b-667">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="0a67b-668">Bankkontotype</span><span class="sxs-lookup"><span data-stu-id="0a67b-668">Bank account type</span></span>

<span data-ttu-id="0a67b-669">Bankkontotyper bruges til elektroniske betalinger til medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="0a67b-669">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="0a67b-670">Bankkontotyper knyttes til Dayforce som overførselskontooplysninger.</span><span class="sxs-lookup"><span data-stu-id="0a67b-670">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="0a67b-671">Bankkontotyperne oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="0a67b-671">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="0a67b-672">Human Resources</span><span class="sxs-lookup"><span data-stu-id="0a67b-672">Human Resources</span></span>            | <span data-ttu-id="0a67b-673">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a67b-673">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="0a67b-674">Checkkonto</span><span class="sxs-lookup"><span data-stu-id="0a67b-674">Checking Account</span></span>  | <span data-ttu-id="0a67b-675">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="0a67b-675">CheckingAccount</span></span>           |
| <span data-ttu-id="0a67b-676">Lønkonto</span><span class="sxs-lookup"><span data-stu-id="0a67b-676">Payroll Account</span></span>   | <span data-ttu-id="0a67b-677">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="0a67b-677">PayrollAccount</span></span>            |
| <span data-ttu-id="0a67b-678">Opsparingskonto</span><span class="sxs-lookup"><span data-stu-id="0a67b-678">Savings Account</span></span>   | <span data-ttu-id="0a67b-679">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="0a67b-679">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="0a67b-680">BankGirot-konto</span><span class="sxs-lookup"><span data-stu-id="0a67b-680">BankGirot account</span></span> | <span data-ttu-id="0a67b-681">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="0a67b-681">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="0a67b-682">PlusGirot-konto</span><span class="sxs-lookup"><span data-stu-id="0a67b-682">PlusGirot account</span></span> | <span data-ttu-id="0a67b-683">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="0a67b-683">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="0a67b-684">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="0a67b-684">Earning codes</span></span>

<span data-ttu-id="0a67b-685">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="0a67b-685">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="0a67b-686">Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="0a67b-686">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="0a67b-687">Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="0a67b-687">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="0a67b-688">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="0a67b-688">Supported frequencies</span></span>

- <span data-ttu-id="0a67b-689">Alt</span><span class="sxs-lookup"><span data-stu-id="0a67b-689">All</span></span>
- <span data-ttu-id="0a67b-690">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="0a67b-690">EVERYPAY</span></span>
- <span data-ttu-id="0a67b-691">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="0a67b-691">EACHPAYPERIOD</span></span>
- <span data-ttu-id="0a67b-692">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="0a67b-692">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="0a67b-693">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="0a67b-693">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="0a67b-694">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-694">1OFMTH</span></span>
- <span data-ttu-id="0a67b-695">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-695">LASTOFMTH</span></span>
- <span data-ttu-id="0a67b-696">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-696">2OFMTH</span></span>
- <span data-ttu-id="0a67b-697">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-697">3OFMTH</span></span>
- <span data-ttu-id="0a67b-698">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-698">4OFMTH</span></span>
- <span data-ttu-id="0a67b-699">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-699">5OFMTH</span></span>
- <span data-ttu-id="0a67b-700">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-700">1N2OFMTH</span></span>
- <span data-ttu-id="0a67b-701">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-701">3N4OFMTH</span></span>
- <span data-ttu-id="0a67b-702">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-702">1N3OFMTH</span></span>
- <span data-ttu-id="0a67b-703">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-703">1N4OFMTH</span></span>
- <span data-ttu-id="0a67b-704">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-704">2N3OFMTH</span></span>
- <span data-ttu-id="0a67b-705">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-705">2N4OFMTH</span></span>
- <span data-ttu-id="0a67b-706">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-706">1N2N3OFMTH</span></span>
- <span data-ttu-id="0a67b-707">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-707">1N2N4OFMTH</span></span>
- <span data-ttu-id="0a67b-708">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-708">1N3N4OFMTH</span></span>
- <span data-ttu-id="0a67b-709">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-709">2N3N4OFMTH</span></span>
- <span data-ttu-id="0a67b-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0a67b-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="0a67b-711">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="0a67b-711">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="0a67b-712">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="0a67b-712">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="0a67b-713">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="0a67b-713">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="0a67b-714">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="0a67b-714">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="0a67b-715">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="0a67b-715">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="0a67b-716">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="0a67b-716">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="0a67b-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="0a67b-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="0a67b-718">Adresser</span><span class="sxs-lookup"><span data-stu-id="0a67b-718">Addresses</span></span>

<span data-ttu-id="0a67b-719">Identifikation af specifikke koder for land eller område, stat og region (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende.</span><span class="sxs-lookup"><span data-stu-id="0a67b-719">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="0a67b-720">Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.</span><span class="sxs-lookup"><span data-stu-id="0a67b-720">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="0a67b-721">Human Resources</span><span class="sxs-lookup"><span data-stu-id="0a67b-721">Human Resources</span></span>              | <span data-ttu-id="0a67b-722">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0a67b-722">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="0a67b-723">Land/område</span><span class="sxs-lookup"><span data-stu-id="0a67b-723">Country/Region</span></span>      | <span data-ttu-id="0a67b-724">Landekode</span><span class="sxs-lookup"><span data-stu-id="0a67b-724">Country Code</span></span>          |
| <span data-ttu-id="0a67b-725">Postnummer</span><span class="sxs-lookup"><span data-stu-id="0a67b-725">Zip/Postal Code</span></span>     | <span data-ttu-id="0a67b-726">Postnummer</span><span class="sxs-lookup"><span data-stu-id="0a67b-726">Postal Code</span></span>           |
| <span data-ttu-id="0a67b-727">Status</span><span class="sxs-lookup"><span data-stu-id="0a67b-727">State</span></span>               | <span data-ttu-id="0a67b-728">Statskode</span><span class="sxs-lookup"><span data-stu-id="0a67b-728">State Code</span></span>            |
| <span data-ttu-id="0a67b-729">Bynavn</span><span class="sxs-lookup"><span data-stu-id="0a67b-729">City</span></span>                | <span data-ttu-id="0a67b-730">Bynavn</span><span class="sxs-lookup"><span data-stu-id="0a67b-730">City</span></span>                  |
| <span data-ttu-id="0a67b-731">Region</span><span class="sxs-lookup"><span data-stu-id="0a67b-731">County</span></span>              | <span data-ttu-id="0a67b-732">Område (kommune)</span><span class="sxs-lookup"><span data-stu-id="0a67b-732">County (Municipality)</span></span> |
| <span data-ttu-id="0a67b-733">Gade</span><span class="sxs-lookup"><span data-stu-id="0a67b-733">Street</span></span>              | <span data-ttu-id="0a67b-734">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="0a67b-734">Address Line 1</span></span>        |
| <span data-ttu-id="0a67b-735">Gadenummer</span><span class="sxs-lookup"><span data-stu-id="0a67b-735">Street Number</span></span>       | <span data-ttu-id="0a67b-736">Adresselinje 2</span><span class="sxs-lookup"><span data-stu-id="0a67b-736">Address Line 2</span></span>        |
| <span data-ttu-id="0a67b-737">Bygningskomplement</span><span class="sxs-lookup"><span data-stu-id="0a67b-737">Building Complement</span></span> | <span data-ttu-id="0a67b-738">Adresselinje 5</span><span class="sxs-lookup"><span data-stu-id="0a67b-738">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="0a67b-739">Pasnummer</span><span class="sxs-lookup"><span data-stu-id="0a67b-739">Passport number</span></span>

<span data-ttu-id="0a67b-740">Medarbejdere kan erklære pasoplysninger.</span><span class="sxs-lookup"><span data-stu-id="0a67b-740">Employees can declare passport information.</span></span> <span data-ttu-id="0a67b-741">Disse oplysninger er af identifikationstypen **Pas** og er integreret i Dayforce som en del af en medarbejders Mexico-specifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="0a67b-741">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="0a67b-742">Identifikationstype = "Pas"</span><span class="sxs-lookup"><span data-stu-id="0a67b-742">Identification Type = "Passport"</span></span>
- <span data-ttu-id="0a67b-743">Udstedt den</span><span class="sxs-lookup"><span data-stu-id="0a67b-743">Issued Date</span></span>
- <span data-ttu-id="0a67b-744">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="0a67b-744">Expiration Date</span></span>

<span data-ttu-id="0a67b-745">Medarbejdere kan angive flere identifikationsnumre af **Pas**-identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="0a67b-745">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="0a67b-746">Men det er kun den aktuelle aktive paspost, der integreres i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a67b-746">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="0a67b-747">Hvis alle pasposter er udløbet, integreres det pas, der senest blev udstedt, i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="0a67b-747">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]