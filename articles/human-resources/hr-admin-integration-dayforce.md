---
title: Konfigurer integration med Dayforce
description: Integrationen mellem Microsoft Dynamics 365 Human Resources og Ceridian Dayforce er baseret på flere konfigurationstrin, der er beskrevet i dette emne. Du skal konfigurere integrationen i både Personale og Dayforce, før du kan behandle en lønkørsel.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: c66ec772ea66732e042f50081f04a6569852f211
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417729"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="9c069-104">Konfigurer integration med Dayforce</span><span class="sxs-lookup"><span data-stu-id="9c069-104">Configure integration with Dayforce</span></span>

<span data-ttu-id="9c069-105">Integrationen mellem Microsoft Dynamics 365 Human Resources og Ceridian Dayforce er baseret på flere konfigurationstrin, der er beskrevet i dette emne.</span><span class="sxs-lookup"><span data-stu-id="9c069-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="9c069-106">Du skal konfigurere integrationen i både Personale og Dayforce, før du kan behandle en lønkørsel.</span><span class="sxs-lookup"><span data-stu-id="9c069-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="9c069-107">Når du bruger en tjeneste, f.eks. Dayforce, til at fuldføre lønkørsler, skal du aktivere integrationen i Personale.</span><span class="sxs-lookup"><span data-stu-id="9c069-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="9c069-108">Integrationen kræver bestemte data fra Personale.</span><span class="sxs-lookup"><span data-stu-id="9c069-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="9c069-109">Du skal derfor kontrollere, at data, der er knyttet til Dayforce, er konfigureret i Personale på en måde, der understøtter integrationen.</span><span class="sxs-lookup"><span data-stu-id="9c069-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="9c069-110">Integrationen bruger følgende brede kategorier af data.</span><span class="sxs-lookup"><span data-stu-id="9c069-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="9c069-111">Personaledata</span><span class="sxs-lookup"><span data-stu-id="9c069-111">Human resources data</span></span>
- <span data-ttu-id="9c069-112">Kompensationsdata</span><span class="sxs-lookup"><span data-stu-id="9c069-112">Compensation data</span></span>
- <span data-ttu-id="9c069-113">Lønoplysninger, f.eks. løncyklusser, betalingsperioder og lønkoder</span><span class="sxs-lookup"><span data-stu-id="9c069-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="9c069-114">Arbejderdata</span><span class="sxs-lookup"><span data-stu-id="9c069-114">Worker data</span></span>

<span data-ttu-id="9c069-115">Denne artikel beskriver de trin, du skal udføre for at aktivere integrationen.</span><span class="sxs-lookup"><span data-stu-id="9c069-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="9c069-116">Det forklarer også typerne af data og oplysninger om konfigurationen, der kræves til integrationen.</span><span class="sxs-lookup"><span data-stu-id="9c069-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="9c069-117">Aktivere integrationen.</span><span class="sxs-lookup"><span data-stu-id="9c069-117">Enable the integration</span></span>

<span data-ttu-id="9c069-118">I Personale skal du aktivere integrationen og angive konfigurationsoplysningerne for at oprette forbindelse til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9c069-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="9c069-119">Hvis den finanspostering, der er oprettet, skal importeres til Microsoft Dynamics 365 Finance, skal du også konfigurere en Microsoft Azure-lagerkonto og angive Azure-lagerets forbindelsesstreng i Finance.</span><span class="sxs-lookup"><span data-stu-id="9c069-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="9c069-120">Følg disse trin for at aktivere integrationen i Personale.</span><span class="sxs-lookup"><span data-stu-id="9c069-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="9c069-121">På siden **Systemadministration** skal du vælge **Integrationskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="9c069-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="9c069-122">Angiv det sikre FTP-slutpunkt og den sikre FTP-mappesti.</span><span class="sxs-lookup"><span data-stu-id="9c069-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="9c069-123">Angiv brugernavnet og adgangskoden for den bruger, der skal have adgang til det sikre FTP-slutpunkt og den sikre mappesti.</span><span class="sxs-lookup"><span data-stu-id="9c069-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="9c069-124">Test forbindelsen, som krævet, og angiv indstillingen **Aktivér lønintegration** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9c069-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="9c069-125">Når integrationen er aktiveret, oprettes dataeksportpakken og -filerne, og hyppigheden angives.</span><span class="sxs-lookup"><span data-stu-id="9c069-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="9c069-126">Du kan ændre denne frekvens efter behov.</span><span class="sxs-lookup"><span data-stu-id="9c069-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="9c069-127">Yderligere oplysninger om Azure-lagerkonti og Azure-lagerforbindelsesstrenge finder du i følgende Azure-artikler:</span><span class="sxs-lookup"><span data-stu-id="9c069-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="9c069-128">Om Azure-lagerkonti</span><span class="sxs-lookup"><span data-stu-id="9c069-128">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="9c069-129">Konfigurere forbindelsesstrenge for Azure-datalager</span><span class="sxs-lookup"><span data-stu-id="9c069-129">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="9c069-130">Tekniske oplysninger ved aktivering af lønintegration</span><span class="sxs-lookup"><span data-stu-id="9c069-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="9c069-131">Aktivering af lønintegration har to primære effekter:</span><span class="sxs-lookup"><span data-stu-id="9c069-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="9c069-132">Der oprettes et dataeksport projekt ved navn "Lønintegrationseksport".</span><span class="sxs-lookup"><span data-stu-id="9c069-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="9c069-133">Dette projekt indeholder de objekter og felter, der kræves til lønintegration.</span><span class="sxs-lookup"><span data-stu-id="9c069-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="9c069-134">Hvis du vil undersøge projektet, skal du gå til **Systemadministration**, vælge feltet **Datastyring** og derefter åbne dataprojektet på listen over projekter.</span><span class="sxs-lookup"><span data-stu-id="9c069-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="9c069-135">Dette batchjob udfører dataeksportprojektet, krypterer den resulterende datapakke og overfører datapakkefilen til det SFTP-slutpunkt, der er konfigureret på skærmen **Integrationskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="9c069-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="9c069-136">Den datapakke, der overføres til SFTP-slutpunktet, krypteres ved hjælp af en nøgle, der er entydig for pakken.</span><span class="sxs-lookup"><span data-stu-id="9c069-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="9c069-137">Nøglen er i en Azure Key Vault, der kun kan åbnes af Ceridian.</span><span class="sxs-lookup"><span data-stu-id="9c069-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="9c069-138">Det er ikke muligt at dekryptere og undersøge datapakkens indhold.</span><span class="sxs-lookup"><span data-stu-id="9c069-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="9c069-139">Hvis du har brug for at undersøge indholdet af datapakken, skal du eksportere dataprojektet "Lønintegrationseksport" manuelt, download det og derefter åbne det.</span><span class="sxs-lookup"><span data-stu-id="9c069-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="9c069-140">Manuel eksport anvender ikke kryptering eller overførsel af pakken.</span><span class="sxs-lookup"><span data-stu-id="9c069-140">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="9c069-141">Konfigurere dine data</span><span class="sxs-lookup"><span data-stu-id="9c069-141">Configure your data</span></span> 

<span data-ttu-id="9c069-142">Hvis du vil behandle løn, skal du konfigurere personaledata i Personale.</span><span class="sxs-lookup"><span data-stu-id="9c069-142">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="9c069-143">Du skal angive virksomhedens data, f.eks. job og stillinger, sammen med frynsegoder og kompensationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="9c069-143">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="9c069-144">Disse oplysninger indeholder oplysningerne om ansættelse, løn og fradrag, der kræves for at generere løn for medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="9c069-144">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="9c069-145">Personaledata</span><span class="sxs-lookup"><span data-stu-id="9c069-145">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="9c069-146">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="9c069-146">Benefits</span></span> 

<span data-ttu-id="9c069-147">Personale indeholder en række værktøjer til konfiguration og vedligeholdelse af frynsegoder, fradrag og arbejderkompensationsplaner, som en organisation tilbyder eller behandler for sine ansatte.</span><span class="sxs-lookup"><span data-stu-id="9c069-147">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="9c069-148">Når du opretter frynsegoder, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9c069-148">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="9c069-149">Frynsegodeplaner</span><span class="sxs-lookup"><span data-stu-id="9c069-149">Benefit plans</span></span>

- <span data-ttu-id="9c069-150">Plan (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-150">Plan (required)</span></span>
- <span data-ttu-id="9c069-151">Type (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-151">Type (required)</span></span>
- <span data-ttu-id="9c069-152">Løneffekt (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-152">Payroll impact (required)</span></span>
- <span data-ttu-id="9c069-153">Opkræv restancer</span><span class="sxs-lookup"><span data-stu-id="9c069-153">Recover arrears</span></span>
- <span data-ttu-id="9c069-154">Fradragsmetode</span><span class="sxs-lookup"><span data-stu-id="9c069-154">Deduction method</span></span>
- <span data-ttu-id="9c069-155">Prioriteret fradrag</span><span class="sxs-lookup"><span data-stu-id="9c069-155">Deduction priority</span></span>
- <span data-ttu-id="9c069-156">Grænseperiode</span><span class="sxs-lookup"><span data-stu-id="9c069-156">Limit period</span></span>
- <span data-ttu-id="9c069-157">Beløb for grænse</span><span class="sxs-lookup"><span data-stu-id="9c069-157">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="9c069-158">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="9c069-158">Benefits</span></span>

- <span data-ttu-id="9c069-159">Plan (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-159">Plan (required)</span></span>
- <span data-ttu-id="9c069-160">Type (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-160">Type (required)</span></span>
- <span data-ttu-id="9c069-161">Mulighed (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-161">Option (required)</span></span>
- <span data-ttu-id="9c069-162">Frynsegode-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-162">Benefit ID (required)</span></span>
- <span data-ttu-id="9c069-163">Frekvens</span><span class="sxs-lookup"><span data-stu-id="9c069-163">Frequency</span></span>
- <span data-ttu-id="9c069-164">Basis</span><span class="sxs-lookup"><span data-stu-id="9c069-164">Basis</span></span>
- <span data-ttu-id="9c069-165">Beløb eller sats</span><span class="sxs-lookup"><span data-stu-id="9c069-165">Amount or rate</span></span>
- <span data-ttu-id="9c069-166">Lønkode</span><span class="sxs-lookup"><span data-stu-id="9c069-166">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="9c069-167">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="9c069-167">Supported frequencies</span></span> 

- <span data-ttu-id="9c069-168">Ugentlig</span><span class="sxs-lookup"><span data-stu-id="9c069-168">Weekly</span></span>
- <span data-ttu-id="9c069-169">Pr. 14 dage</span><span class="sxs-lookup"><span data-stu-id="9c069-169">Bi-weekly</span></span>
- <span data-ttu-id="9c069-170">To gange om måneden</span><span class="sxs-lookup"><span data-stu-id="9c069-170">Semi-monthly</span></span>
- <span data-ttu-id="9c069-171">Månedlig</span><span class="sxs-lookup"><span data-stu-id="9c069-171">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="9c069-172">Understøttede grundlag</span><span class="sxs-lookup"><span data-stu-id="9c069-172">Supported bases</span></span> 

- <span data-ttu-id="9c069-173">Fast beløb</span><span class="sxs-lookup"><span data-stu-id="9c069-173">Fixed amount</span></span>
- <span data-ttu-id="9c069-174">Procentdel af løn</span><span class="sxs-lookup"><span data-stu-id="9c069-174">Percent of earnings</span></span>
- <span data-ttu-id="9c069-175">Produktive timer</span><span class="sxs-lookup"><span data-stu-id="9c069-175">Productive hours</span></span>

<span data-ttu-id="9c069-176">Dayforce opretter følgende fradrag, der er baseret på den løneffekt, der er defineret på frynsegodeplanen.</span><span class="sxs-lookup"><span data-stu-id="9c069-176">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="9c069-177">Valg i Personale</span><span class="sxs-lookup"><span data-stu-id="9c069-177">Selection in Human Resources</span></span>        | <span data-ttu-id="9c069-178">Resultat i Dayforce</span><span class="sxs-lookup"><span data-stu-id="9c069-178">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="9c069-179">Ingen</span><span class="sxs-lookup"><span data-stu-id="9c069-179">None</span></span>                       | <span data-ttu-id="9c069-180">Der oprettes ikke noget fradrag.</span><span class="sxs-lookup"><span data-stu-id="9c069-180">No deduction is created.</span></span>                      |
| <span data-ttu-id="9c069-181">Kun fradrag</span><span class="sxs-lookup"><span data-stu-id="9c069-181">Deduction only</span></span>             | <span data-ttu-id="9c069-182">Der oprettes et medarbejderfradrag.</span><span class="sxs-lookup"><span data-stu-id="9c069-182">An employee deduction is created.</span></span>             |
| <span data-ttu-id="9c069-183">Kun bidrag</span><span class="sxs-lookup"><span data-stu-id="9c069-183">Contribution only</span></span>          | <span data-ttu-id="9c069-184">Der oprettes et arbejdsgiverfradrag.</span><span class="sxs-lookup"><span data-stu-id="9c069-184">An employer deduction is created.</span></span>             |
| <span data-ttu-id="9c069-185">Fradrag og bidrag</span><span class="sxs-lookup"><span data-stu-id="9c069-185">Deduction and contribution</span></span> | <span data-ttu-id="9c069-186">Der oprettes medarbejder- og arbejdsgiverfradrag.</span><span class="sxs-lookup"><span data-stu-id="9c069-186">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="9c069-187">Du kan finde flere oplysninger om, hvordan du definerer og administrerer et frynsegodeprogram i følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="9c069-187">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="9c069-188">Levere et frynsegodeprogram for medarbejdere</span><span class="sxs-lookup"><span data-stu-id="9c069-188">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="9c069-189">Opret et nyt frynsegode</span><span class="sxs-lookup"><span data-stu-id="9c069-189">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="9c069-190">Definere regler og politikker for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="9c069-190">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="9c069-191">Tilmelde og fjerne frynsegoder fra arbejdere</span><span class="sxs-lookup"><span data-stu-id="9c069-191">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="9c069-192">Kompensation</span><span class="sxs-lookup"><span data-stu-id="9c069-192">Compensation</span></span> 

<span data-ttu-id="9c069-193">Kompensationsstyring bruges til at styre fordelingen af grundløn og bonusser.</span><span class="sxs-lookup"><span data-stu-id="9c069-193">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="9c069-194">En medarbejders faste grundløn og kvalifikationstillæg styres gennem faste lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="9c069-194">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="9c069-195">Betalingen af incitamentsløn som f.eks. bonusudbetalinger, præstationsbonusser, aktieoptioner og tildelte aktier samt engangsbonusser styres ved hjælp af variable lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="9c069-195">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="9c069-196">Dayforce anvendes kompensationsoplysninger til at beregne en medarbejders timesats eller årlige sats.</span><span class="sxs-lookup"><span data-stu-id="9c069-196">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="9c069-197">Konverteringer af planer for fast løn og lønsats er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="9c069-197">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="9c069-198">Medarbejderne skal være knyttet til en plan for fast løn.</span><span class="sxs-lookup"><span data-stu-id="9c069-198">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="9c069-199">Du kan finde flere oplysninger om kompensationsplaner i følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="9c069-199">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="9c069-200">Oprette planer for fast løn</span><span class="sxs-lookup"><span data-stu-id="9c069-200">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="9c069-201">Oprette planer for variabel kompensation</span><span class="sxs-lookup"><span data-stu-id="9c069-201">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="9c069-202">Udarbejde løn-/kompensationsstruktur og -planer</span><span class="sxs-lookup"><span data-stu-id="9c069-202">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="9c069-203">Proceskompensation</span><span class="sxs-lookup"><span data-stu-id="9c069-203">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="9c069-204">Definere kompensationsproces og beregne resultater</span><span class="sxs-lookup"><span data-stu-id="9c069-204">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="9c069-205">Melde en medarbejder til en fast lønplan</span><span class="sxs-lookup"><span data-stu-id="9c069-205">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="9c069-206">Melde en medarbejder til en variabel lønplan</span><span class="sxs-lookup"><span data-stu-id="9c069-206">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="9c069-207">Job</span><span class="sxs-lookup"><span data-stu-id="9c069-207">Jobs</span></span> 

<span data-ttu-id="9c069-208">Et job er en samling af de opgaver og ansvarsområder, der kræves af en person, der udfører et job.</span><span class="sxs-lookup"><span data-stu-id="9c069-208">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="9c069-209">Du kan finde flere oplysninger i følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="9c069-209">For more information, see the following articles:</span></span>

- [<span data-ttu-id="9c069-210">Konfiguration af komponenter i et job</span><span class="sxs-lookup"><span data-stu-id="9c069-210">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="9c069-211">Definere nye job</span><span class="sxs-lookup"><span data-stu-id="9c069-211">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="9c069-212">Stillinger</span><span class="sxs-lookup"><span data-stu-id="9c069-212">Positions</span></span>

<span data-ttu-id="9c069-213">En stilling er en individuel forekomst af et job.</span><span class="sxs-lookup"><span data-stu-id="9c069-213">A position is an individual instance of a job.</span></span> <span data-ttu-id="9c069-214">For eksempel er stillingen "Salgschef (øst)" én af de stillinger, der er tilknyttet jobbet "Salgschef".</span><span class="sxs-lookup"><span data-stu-id="9c069-214">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="9c069-215">En stilling findes i en afdeling.</span><span class="sxs-lookup"><span data-stu-id="9c069-215">A position exists in a department.</span></span> <span data-ttu-id="9c069-216">Der kan kun knyttes én arbejder til hver stilling.</span><span class="sxs-lookup"><span data-stu-id="9c069-216">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="9c069-217">Hav følgende data og konfiguration i tankerne, når du konfigurerer stillinger:</span><span class="sxs-lookup"><span data-stu-id="9c069-217">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="9c069-218">Stilling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-218">Position (required)</span></span>
- <span data-ttu-id="9c069-219">Beskrivelse (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-219">Description (required)</span></span>
- <span data-ttu-id="9c069-220">Job (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-220">Job (required)</span></span>
- <span data-ttu-id="9c069-221">Afdeling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-221">Department (required)</span></span>
- <span data-ttu-id="9c069-222">Stillingstype (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-222">Position type (required)</span></span>
- <span data-ttu-id="9c069-223">Fuldtidsækvivalent</span><span class="sxs-lookup"><span data-stu-id="9c069-223">Full-time equivalent</span></span>
- <span data-ttu-id="9c069-224">Normaltimer på årsbasis (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-224">Annual regular hours (required)</span></span>
- <span data-ttu-id="9c069-225">Betalt af juridiske enhed (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-225">Paid by legal entity (required)</span></span>
- <span data-ttu-id="9c069-226">Betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-226">Pay cycle (required)</span></span>
- <span data-ttu-id="9c069-227">Økonomisk standarddimension – bærer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-227">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="9c069-228">Arbejdertildeling – arbejder, tildelingsstart, tildelingsslut, årsagskode</span><span class="sxs-lookup"><span data-stu-id="9c069-228">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="9c069-229">Hvis flere stillinger i den samme afdeling er knyttet til samme job, konsolideres de til en enkelt stilling i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9c069-229">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="9c069-230">Du kan finde flere oplysninger i følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="9c069-230">For more information, see the following articles:</span></span>

- [<span data-ttu-id="9c069-231">Organisere dine medarbejdere ved hjælp af afdelinger, jobs og stillinger</span><span class="sxs-lookup"><span data-stu-id="9c069-231">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="9c069-232">Konfigurere stillinger</span><span class="sxs-lookup"><span data-stu-id="9c069-232">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="9c069-233">Afdelinger</span><span class="sxs-lookup"><span data-stu-id="9c069-233">Departments</span></span>

<span data-ttu-id="9c069-234">En afdeling er en driftsenhed, der repræsenterer en kategori eller et funktionsområde i en organisation.</span><span class="sxs-lookup"><span data-stu-id="9c069-234">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="9c069-235">En afdeling er ansvarlig for et bestemt område i organisationen, såsom salg, regnskab eller personale.</span><span class="sxs-lookup"><span data-stu-id="9c069-235">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="9c069-236">Du kan bruge afdelinger til at rapportere om funktionsområder.</span><span class="sxs-lookup"><span data-stu-id="9c069-236">You can use departments to report on functional areas.</span></span> <span data-ttu-id="9c069-237">Afdelinger kan have ansvar for driftsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="9c069-237">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="9c069-238">Du kan finde flere oplysninger i følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="9c069-238">For more information, see the following articles:</span></span>

- [<span data-ttu-id="9c069-239">Oprette en afdeling og knytte den til afdelingshierarkiet</span><span class="sxs-lookup"><span data-stu-id="9c069-239">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="9c069-240">Definere nye afdelinger</span><span class="sxs-lookup"><span data-stu-id="9c069-240">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="9c069-241">Betalingscyklusser og lønperioder</span><span class="sxs-lookup"><span data-stu-id="9c069-241">Pay cycles and pay periods</span></span>

<span data-ttu-id="9c069-242">En betalingscyklus bestemmer, hvor ofte løn køres,og de specifikke dage, hvor arbejdere betales.</span><span class="sxs-lookup"><span data-stu-id="9c069-242">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="9c069-243">En løncyklus kan f.eks. være månedlig, og medarbejdere betales måske på den sidste dag i måneden.</span><span class="sxs-lookup"><span data-stu-id="9c069-243">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="9c069-244">En løncyklus kan også være ugentligt, og medarbejdere betales måske tirsdag efter slutningen af lønperioden.</span><span class="sxs-lookup"><span data-stu-id="9c069-244">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="9c069-245">Løncyklusser tildeles til stillinger for at styre, hvornår arbejdere i disse stillinger bliver betalt.</span><span class="sxs-lookup"><span data-stu-id="9c069-245">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="9c069-246">Når du opretter betalingscyklusser, kan du generere lønperioder for hver cyklus.</span><span class="sxs-lookup"><span data-stu-id="9c069-246">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="9c069-247">Hver lønperiode omfatter en standardbetalingsdato, der er baseret på oplysninger, du angiver.</span><span class="sxs-lookup"><span data-stu-id="9c069-247">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="9c069-248">Du kan dog redigere standardbetalingsdatoen i en lønperiode til at tillade undtagelser, f.eks. når betalingsdatoen falder på en helligdag.</span><span class="sxs-lookup"><span data-stu-id="9c069-248">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="9c069-249">Følgende oplysninger bruges i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="9c069-249">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="9c069-250">Betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-250">Pay cycle (required)</span></span>
- <span data-ttu-id="9c069-251">Hyppighed for betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-251">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="9c069-252">Periodens startdato (første lønperiode påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-252">Period start date (first pay period required)</span></span>
- <span data-ttu-id="9c069-253">Standardbetalingsdato (første lønperiode påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-253">Default payment date (first pay period required)</span></span>

<span data-ttu-id="9c069-254">Oplysningerne er integreret med Dayforce som løngrupper og adskilles af et land eller område for hver løncyklus.</span><span class="sxs-lookup"><span data-stu-id="9c069-254">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="9c069-255">Mindst én periode skal genereres før integration.</span><span class="sxs-lookup"><span data-stu-id="9c069-255">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="9c069-256">Dayforce genererer løngruppekalendere og betalingsdatoer, der er baseret på startdatoen for den første lønperiode og den standardbetalingsdato, der er angivet i Personale.</span><span class="sxs-lookup"><span data-stu-id="9c069-256">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="9c069-257">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="9c069-257">Earning codes</span></span>

<span data-ttu-id="9c069-258">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="9c069-258">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="9c069-259">Koderne har forskellige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="9c069-259">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="9c069-260">Følgende oplysninger bruges i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="9c069-260">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="9c069-261">Lønkode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-261">Earning Code (required)</span></span>
- <span data-ttu-id="9c069-262">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="9c069-262">Description</span></span>
- <span data-ttu-id="9c069-263">Måleenhed</span><span class="sxs-lookup"><span data-stu-id="9c069-263">Unit of measure</span></span>
- <span data-ttu-id="9c069-264">Produktiv</span><span class="sxs-lookup"><span data-stu-id="9c069-264">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="9c069-265">Arbejderdata</span><span class="sxs-lookup"><span data-stu-id="9c069-265">Worker data</span></span>

<span data-ttu-id="9c069-266">Posterne for de forskellige typer arbejdere, du beskæftiger, er vigtige for dine personale- og lønsystemer.</span><span class="sxs-lookup"><span data-stu-id="9c069-266">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="9c069-267">De oplysninger, du angiver, kan bruges til at spore arbejdere og personoplysninger.</span><span class="sxs-lookup"><span data-stu-id="9c069-267">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="9c069-268">Du kan vedligeholde følgende oplysninger for arbejdere:</span><span class="sxs-lookup"><span data-stu-id="9c069-268">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="9c069-269">**Basis** – Vedligehold grundlæggende oplysninger om en arbejder, f.eks. kontaktoplysninger, demografiske oplysninger, identifikationsoplysninger, oplysninger om familie, status for militærtjeneste, oplysninger om udstationering og personlige kontaktpersoner og kontaktpersoner i nødsituationer.</span><span class="sxs-lookup"><span data-stu-id="9c069-269">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="9c069-270">**Beskæftigelse** – Vedligehold oplysninger om en arbejders beskæftigelse, f.eks. firma- eller organisationstilhørsforhold, stillingstildeling, start- og slutdatoer, arbejdstilladelse, vilkår for ansættelse, pension, ferie og flytteoplysninger.</span><span class="sxs-lookup"><span data-stu-id="9c069-270">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="9c069-271">**Orlov og fravær** – Vedligehold oplysninger om en arbejders fravær, f.eks. arbejdskalendere, fraværstransaktioner og fraværsopsætning.</span><span class="sxs-lookup"><span data-stu-id="9c069-271">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="9c069-272">**Kompensation og løn** – Vedligehold oplysninger om en arbejders kompensationsplaner og lønoplysninger, f.eks. tilmelding til planer, priser, ydeevne, provision, skatteoplysninger, pensionering og skattefradrag.</span><span class="sxs-lookup"><span data-stu-id="9c069-272">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="9c069-273">Når du angiver arbejderoplysninger, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9c069-273">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="9c069-274">Generelle oplysninger</span><span class="sxs-lookup"><span data-stu-id="9c069-274">General information</span></span>

- <span data-ttu-id="9c069-275">Personalenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-275">Personnel number (required)</span></span>
- <span data-ttu-id="9c069-276">Fornavn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-276">First name (required)</span></span>
- <span data-ttu-id="9c069-277">Efternavn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-277">Last name (required)</span></span>
- <span data-ttu-id="9c069-278">Mellemnavn</span><span class="sxs-lookup"><span data-stu-id="9c069-278">Middle name</span></span>
- <span data-ttu-id="9c069-279">Anciennitetsdato</span><span class="sxs-lookup"><span data-stu-id="9c069-279">Seniority date</span></span>
- <span data-ttu-id="9c069-280">Kendt som</span><span class="sxs-lookup"><span data-stu-id="9c069-280">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="9c069-281">Personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="9c069-281">Personal information</span></span>

- <span data-ttu-id="9c069-282">Ægteskabelig status (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-282">Marital status (required)</span></span>
- <span data-ttu-id="9c069-283">Fødselsdato (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-283">Birth date (required)</span></span>
- <span data-ttu-id="9c069-284">Køn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-284">Gender (required)</span></span>
- <span data-ttu-id="9c069-285">Handicappet</span><span class="sxs-lookup"><span data-stu-id="9c069-285">Person with disabilities</span></span>
- <span data-ttu-id="9c069-286">Land eller område for nationalitet (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="9c069-286">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="9c069-287">Adresseoplysninger</span><span class="sxs-lookup"><span data-stu-id="9c069-287">Address information</span></span>

- <span data-ttu-id="9c069-288">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-288">Primary (required)</span></span>
- <span data-ttu-id="9c069-289">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-289">Country/region (required)</span></span>
- <span data-ttu-id="9c069-290">Postnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-290">Postal code (required)</span></span>
- <span data-ttu-id="9c069-291">Gadenummer (påkrævet) (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="9c069-291">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="9c069-292">Bygningskomplement (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="9c069-292">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="9c069-293">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-293">City (required)</span></span>
- <span data-ttu-id="9c069-294">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-294">State (required)</span></span>
- <span data-ttu-id="9c069-295">Region (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-295">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="9c069-296">Kontaktoplysninger</span><span class="sxs-lookup"><span data-stu-id="9c069-296">Contact information</span></span> 

- <span data-ttu-id="9c069-297">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-297">Primary (required)</span></span>
- <span data-ttu-id="9c069-298">Kontaktpersonens nummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-298">Contact number (required)</span></span>
- <span data-ttu-id="9c069-299">Forlængelse</span><span class="sxs-lookup"><span data-stu-id="9c069-299">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="9c069-300">Lønoplysninger og lønkoder</span><span class="sxs-lookup"><span data-stu-id="9c069-300">Payroll information and earning codes</span></span>

<span data-ttu-id="9c069-301">Medarbejdere kan tildeles en bestemt løn med en given betalingshyppighed og have en foretrukken betalingsmetode.</span><span class="sxs-lookup"><span data-stu-id="9c069-301">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="9c069-302">Følgende felter bruges i Dayforce til at sikre, at disse præferencer og indstillinger bruges.</span><span class="sxs-lookup"><span data-stu-id="9c069-302">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="9c069-303">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="9c069-303">Earning codes</span></span>

- <span data-ttu-id="9c069-304">Stilling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-304">Position (required)</span></span>
- <span data-ttu-id="9c069-305">Lønkode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-305">Earning Code (required)</span></span>
- <span data-ttu-id="9c069-306">Frekvens (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-306">Frequency (required)</span></span>
- <span data-ttu-id="9c069-307">Beløb (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-307">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="9c069-308">Lønoplysninger</span><span class="sxs-lookup"><span data-stu-id="9c069-308">Payroll information</span></span>

- <span data-ttu-id="9c069-309">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="9c069-309">Payment Method</span></span>
- <span data-ttu-id="9c069-310">Økonomisk område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-310">Economic Region (required)</span></span>
- <span data-ttu-id="9c069-311">Id for medarbejderfrynsegoder</span><span class="sxs-lookup"><span data-stu-id="9c069-311">Employee Benefits ID</span></span>
- <span data-ttu-id="9c069-312">Nationalt id-nummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-312">National ID Number (required)</span></span>
- <span data-ttu-id="9c069-313">Tjenestenummer hos militær</span><span class="sxs-lookup"><span data-stu-id="9c069-313">Military Service Number</span></span>
- <span data-ttu-id="9c069-314">Skifte-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-314">Shift ID (required)</span></span>
- <span data-ttu-id="9c069-315">Skattenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-315">Tax Number (required)</span></span>
- <span data-ttu-id="9c069-316">Fagforenings-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-316">Union ID (required)</span></span>
- <span data-ttu-id="9c069-317">Arbejdsdags-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-317">Work Day ID (required)</span></span>
- <span data-ttu-id="9c069-318">Arbejdstilladelsesnummer</span><span class="sxs-lookup"><span data-stu-id="9c069-318">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="9c069-319">For betalingsmetoden understøtter Mexico **Kontant**, **Check** (firmaets fysiske check), og **Elektronisk betaling**.</span><span class="sxs-lookup"><span data-stu-id="9c069-319">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="9c069-320">Hvis der ikke er angivet nogen betalingsmetode, bruges **Check** som standard.</span><span class="sxs-lookup"><span data-stu-id="9c069-320">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="9c069-321">Detaljer om ansættelse</span><span class="sxs-lookup"><span data-stu-id="9c069-321">Employment details</span></span>

<span data-ttu-id="9c069-322">Detaljeret ansættelseshistorik bruges som vigtige oplysninger til at udlede statusser for en medarbejders ansættelse, fratrædelse og genansættelse i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9c069-322">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="9c069-323">Dayforce understøtter kun én aktiv ansættelsespost ad gangen.</span><span class="sxs-lookup"><span data-stu-id="9c069-323">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="9c069-324">Startdato for ansættelse (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-324">Employment start date (required)</span></span>
- <span data-ttu-id="9c069-325">Slutdato for ansættelse</span><span class="sxs-lookup"><span data-stu-id="9c069-325">Employment end date</span></span>
- <span data-ttu-id="9c069-326">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="9c069-326">Start date</span></span>
- <span data-ttu-id="9c069-327">Justeret startdato</span><span class="sxs-lookup"><span data-stu-id="9c069-327">Adjusted start date</span></span>
- <span data-ttu-id="9c069-328">Fratrædelsesdato (kræves ved fratrædelse)</span><span class="sxs-lookup"><span data-stu-id="9c069-328">Termination date (required upon termination)</span></span>
- <span data-ttu-id="9c069-329">Fratrædelsesårsag (kræves ved fratrædelse)</span><span class="sxs-lookup"><span data-stu-id="9c069-329">Termination reason (required upon termination)</span></span>

<span data-ttu-id="9c069-330">Vigtige datoer for en medarbejders udledes ved hjælp af følgende oplysninger.</span><span class="sxs-lookup"><span data-stu-id="9c069-330">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="9c069-331">Personale</span><span class="sxs-lookup"><span data-stu-id="9c069-331">Human Resources</span></span>                | <span data-ttu-id="9c069-332">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9c069-332">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c069-333">Den seneste ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="9c069-333">Most recent hire date</span></span> | <span data-ttu-id="9c069-334">Historikpost for ansættelsesstart for aktuel ikke-afsluttet ansættelse</span><span class="sxs-lookup"><span data-stu-id="9c069-334">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="9c069-335">Fratrædelsesdato</span><span class="sxs-lookup"><span data-stu-id="9c069-335">Termination date</span></span>      | <span data-ttu-id="9c069-336">Historikpost for fratrædelsesdato for aktuel ikke-afsluttet ansættelse</span><span class="sxs-lookup"><span data-stu-id="9c069-336">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="9c069-337">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="9c069-337">Start date</span></span>            | <span data-ttu-id="9c069-338">Historikpost for justeret startdato, startdato eller startdato for ansættelse for aktuel ikke-aktiv ansættelse</span><span class="sxs-lookup"><span data-stu-id="9c069-338">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="9c069-339">Oprindelig ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="9c069-339">Original hire date</span></span>    | <span data-ttu-id="9c069-340">Historikpost for ansættelsesstart for tidligste ansættelse</span><span class="sxs-lookup"><span data-stu-id="9c069-340">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="9c069-341">Kompensation</span><span class="sxs-lookup"><span data-stu-id="9c069-341">Compensation</span></span>

<span data-ttu-id="9c069-342">En fast lønstruktur skal tilknyttes hver medarbejders primære stilling gennem hele ansættelsesperioden.</span><span class="sxs-lookup"><span data-stu-id="9c069-342">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="9c069-343">Denne periode starter på den dato, hvor medarbejderen blev ansat (eller ansættelsesstartdatoen) og fortsætter, indtil fratrædelsen.</span><span class="sxs-lookup"><span data-stu-id="9c069-343">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="9c069-344">Ikrafttrædelsesdato (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-344">Effective Date (required)</span></span>
- <span data-ttu-id="9c069-345">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="9c069-345">Expiration date</span></span>
- <span data-ttu-id="9c069-346">Lønsats (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-346">Pay Rate (required)</span></span>
- <span data-ttu-id="9c069-347">Konverteringer af lønsats (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-347">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="9c069-348">Årlig ækvivalent (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-348">Annual equivalent (required)</span></span>
- <span data-ttu-id="9c069-349">Timebaseret ækvivalent (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-349">Hourly equivalent (required)</span></span>

<span data-ttu-id="9c069-350">Hvis en timeansat medarbejder har flere stillinger, indlæses den faste løn for den primære stilling i Dayforce, som basissats/-løn på medarbejderniveau.</span><span class="sxs-lookup"><span data-stu-id="9c069-350">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="9c069-351">For ikke-primære stillinger gemmes timesatsen i den tilsvarende position i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9c069-351">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="9c069-352">Hvis en funktionær har flere stillinger, afledes den kumulative timesats og årlig gage på tværs af alle aktive stillinger og bruges som basissats/-gage på medarbejderniveau.</span><span class="sxs-lookup"><span data-stu-id="9c069-352">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="9c069-353">Identifikationsnumre</span><span class="sxs-lookup"><span data-stu-id="9c069-353">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="9c069-354">Social Security-identifikator</span><span class="sxs-lookup"><span data-stu-id="9c069-354">Social Security identifier</span></span> 

<span data-ttu-id="9c069-355">Alle medarbejdere skal have én primær identifikator.</span><span class="sxs-lookup"><span data-stu-id="9c069-355">Every employee must have one primary identifier.</span></span> <span data-ttu-id="9c069-356">Identifikatoren skal være af **SSN**-identifikationstypen</span><span class="sxs-lookup"><span data-stu-id="9c069-356">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="9c069-357">I Dayforce afledes den automatisk som medarbejderens Social Security-identifikator, der er påkrævet ved ansættelse.</span><span class="sxs-lookup"><span data-stu-id="9c069-357">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="9c069-358">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-358">Primary (required)</span></span>
- <span data-ttu-id="9c069-359">Identifikationstype = "SSN"</span><span class="sxs-lookup"><span data-stu-id="9c069-359">Identification Type = "SSN"</span></span>
- <span data-ttu-id="9c069-360">Udstedt den</span><span class="sxs-lookup"><span data-stu-id="9c069-360">Issued Date</span></span>
- <span data-ttu-id="9c069-361">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="9c069-361">Expiration Date</span></span>

<span data-ttu-id="9c069-362">Medarbejdere kan angive flere identifikationsnumre af **SSN**-identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="9c069-362">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="9c069-363">Men det er kun den post, der er markeret som **Primær**, som er integreret i Dayforce, uanset om nummeret er aktivt eller udløbet.</span><span class="sxs-lookup"><span data-stu-id="9c069-363">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="9c069-364">Bankkonto og udbetalinger</span><span class="sxs-lookup"><span data-stu-id="9c069-364">Bank accounts and disbursements</span></span>

<span data-ttu-id="9c069-365">Gyldige bankkontooplysninger skal angives for enhver medarbejder, der vælger at blive betalt via bankkontooverførsler.</span><span class="sxs-lookup"><span data-stu-id="9c069-365">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="9c069-366">Personale</span><span class="sxs-lookup"><span data-stu-id="9c069-366">Human Resources</span></span>                         | <span data-ttu-id="9c069-367">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9c069-367">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c069-368">Bankkontonummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-368">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="9c069-369">SWIFT-kode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-369">SWIFT code (required)</span></span>          | <span data-ttu-id="9c069-370">Feltet **Bank-id** bruges ved behandling af løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="9c069-370">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="9c069-371">Afdelingsnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-371">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="9c069-372">Bankkontotype (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-372">Bank account type (required)</span></span>   | <span data-ttu-id="9c069-373">Feltet **Kontotype** bruges ved behandling af løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="9c069-373">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="9c069-374">Understøttede værdier omfatter **Check** og **Løn**.</span><span class="sxs-lookup"><span data-stu-id="9c069-374">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="9c069-375">Medarbejdere, der vælger at betales via bankkontooverførsler, skal angive et link til en restbeløbskonto, der hører under en juridisk enhed, som har primær adresse i Mexico og er knyttet til en gyldig bankkonto fra en mexicansk bank.</span><span class="sxs-lookup"><span data-stu-id="9c069-375">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="9c069-376">Alle andre restbeløbskonti ignoreres.</span><span class="sxs-lookup"><span data-stu-id="9c069-376">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="9c069-377">Adresseoplysninger</span><span class="sxs-lookup"><span data-stu-id="9c069-377">Address information</span></span>

<span data-ttu-id="9c069-378">Alle medarbejdere skal have én primær placering.</span><span class="sxs-lookup"><span data-stu-id="9c069-378">Every employee must have one primary location.</span></span> <span data-ttu-id="9c069-379">I Dayforce bruges denne placering til at bestemme medarbejderens primære opholdssted til skattemæssige formål.</span><span class="sxs-lookup"><span data-stu-id="9c069-379">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="9c069-380">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-380">Primary (required)</span></span>
- <span data-ttu-id="9c069-381">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-381">Country/region (required)</span></span>
- <span data-ttu-id="9c069-382">Postnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-382">Zip/postal code (required)</span></span>
- <span data-ttu-id="9c069-383">Gade (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-383">Street (required)</span></span>
- <span data-ttu-id="9c069-384">Gadenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-384">Street Number (required)</span></span>
- <span data-ttu-id="9c069-385">Bygningskomplement</span><span class="sxs-lookup"><span data-stu-id="9c069-385">Building Complement</span></span>
- <span data-ttu-id="9c069-386">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-386">City (required)</span></span>
- <span data-ttu-id="9c069-387">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-387">State (required)</span></span>
- <span data-ttu-id="9c069-388">Region (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-388">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="9c069-389">Konfigurere dataene for at generere løn i USA og Canada</span><span class="sxs-lookup"><span data-stu-id="9c069-389">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="9c069-390">Hvis du genererer løn for medarbejdere i USA og Canada, skal følgende elementer konfigureres:</span><span class="sxs-lookup"><span data-stu-id="9c069-390">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="9c069-391">Der kræves afdelinger til stillinger.</span><span class="sxs-lookup"><span data-stu-id="9c069-391">Departments are required on positions.</span></span>
- <span data-ttu-id="9c069-392">Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="9c069-392">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="9c069-393">Du kan konfigurere Personale til at kræve, at der angives en afdeling for stillinger.</span><span class="sxs-lookup"><span data-stu-id="9c069-393">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="9c069-394">For at gøre dette skal du gå til **Personalets delte stillinger > Stillinger > Kræv afdelinger for stillinger**.</span><span class="sxs-lookup"><span data-stu-id="9c069-394">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="9c069-395">Det anbefales, at denne indstilling gennemtvinges i forbindelse med integrationen.</span><span class="sxs-lookup"><span data-stu-id="9c069-395">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="9c069-396">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="9c069-396">Job types</span></span>

<span data-ttu-id="9c069-397">Jobtyper bruges til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="9c069-397">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="9c069-398">Jobtyper kræves for at behandle løn i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="9c069-398">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="9c069-399">Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="9c069-399">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="9c069-400">Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.</span><span class="sxs-lookup"><span data-stu-id="9c069-400">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="9c069-401">Der kræves følgende jobtyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="9c069-401">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="9c069-402">Jobtype</span><span class="sxs-lookup"><span data-stu-id="9c069-402">Job type</span></span>   | <span data-ttu-id="9c069-403">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="9c069-403">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="9c069-404">Pr. time</span><span class="sxs-lookup"><span data-stu-id="9c069-404">Hourly</span></span>     | <span data-ttu-id="9c069-405">Pr. time</span><span class="sxs-lookup"><span data-stu-id="9c069-405">Hourly</span></span>      |
| <span data-ttu-id="9c069-406">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="9c069-406">Salaried</span></span>   | <span data-ttu-id="9c069-407">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="9c069-407">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="9c069-408">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="9c069-408">Position types</span></span> 

<span data-ttu-id="9c069-409">Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet.</span><span class="sxs-lookup"><span data-stu-id="9c069-409">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="9c069-410">Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="9c069-410">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="9c069-411">Der kræves følgende stillingstyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="9c069-411">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="9c069-412">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="9c069-412">Position type</span></span>   | <span data-ttu-id="9c069-413">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="9c069-413">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="9c069-414">Fuld tid</span><span class="sxs-lookup"><span data-stu-id="9c069-414">Full-time</span></span>       | <span data-ttu-id="9c069-415">Fuldtidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="9c069-415">Full time employee</span></span> |
| <span data-ttu-id="9c069-416">Deltid</span><span class="sxs-lookup"><span data-stu-id="9c069-416">Part-time</span></span>       | <span data-ttu-id="9c069-417">Deltidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="9c069-417">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="9c069-418">Årsagskoder</span><span class="sxs-lookup"><span data-stu-id="9c069-418">Reason codes</span></span>

<span data-ttu-id="9c069-419">Årsagskoder indeholder oplysninger om status for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="9c069-419">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="9c069-420">Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.</span><span class="sxs-lookup"><span data-stu-id="9c069-420">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="9c069-421">Der kræves følgende årsagskoder og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="9c069-421">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="9c069-422">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="9c069-422">Reason code</span></span>    | <span data-ttu-id="9c069-423">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="9c069-423">Description</span></span>      | <span data-ttu-id="9c069-424">Anvendelige scenarier</span><span class="sxs-lookup"><span data-stu-id="9c069-424">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="9c069-425">OPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="9c069-425">RESIGNATION</span></span>    | <span data-ttu-id="9c069-426">Opsigelse</span><span class="sxs-lookup"><span data-stu-id="9c069-426">Resignation</span></span>      | <span data-ttu-id="9c069-427">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="9c069-427">Terminate worker</span></span>     |
| <span data-ttu-id="9c069-428">OPHØR</span><span class="sxs-lookup"><span data-stu-id="9c069-428">TERMINATION</span></span>    | <span data-ttu-id="9c069-429">Ophør</span><span class="sxs-lookup"><span data-stu-id="9c069-429">Termination</span></span>      | <span data-ttu-id="9c069-430">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="9c069-430">Terminate worker</span></span>     |
| <span data-ttu-id="9c069-431">PENSION</span><span class="sxs-lookup"><span data-stu-id="9c069-431">RETIREMENT</span></span>     | <span data-ttu-id="9c069-432">Pension</span><span class="sxs-lookup"><span data-stu-id="9c069-432">Retirement</span></span>       | <span data-ttu-id="9c069-433">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="9c069-433">Terminate worker</span></span>     |
| <span data-ttu-id="9c069-434">ANDET</span><span class="sxs-lookup"><span data-stu-id="9c069-434">OTHER</span></span>          | <span data-ttu-id="9c069-435">Andre årsager</span><span class="sxs-lookup"><span data-stu-id="9c069-435">Other Reasons</span></span>    | <span data-ttu-id="9c069-436">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="9c069-436">Terminate worker</span></span>     |
| <span data-ttu-id="9c069-437">DØDSFALD</span><span class="sxs-lookup"><span data-stu-id="9c069-437">DEATH</span></span>          | <span data-ttu-id="9c069-438">Dødsfald</span><span class="sxs-lookup"><span data-stu-id="9c069-438">Death</span></span>            | <span data-ttu-id="9c069-439">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="9c069-439">Terminate worker</span></span>     |
| <span data-ttu-id="9c069-440">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="9c069-440">LEAVEOFABSENCE</span></span> | <span data-ttu-id="9c069-441">Orlov</span><span class="sxs-lookup"><span data-stu-id="9c069-441">Leave of Absence</span></span> | <span data-ttu-id="9c069-442">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="9c069-442">Terminate worker</span></span>     |
| <span data-ttu-id="9c069-443">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="9c069-443">CONTRACTEND</span></span>    | <span data-ttu-id="9c069-444">Kontraktudløb</span><span class="sxs-lookup"><span data-stu-id="9c069-444">End of Contract</span></span>  | <span data-ttu-id="9c069-445">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="9c069-445">Terminate worker</span></span>     |
| <span data-ttu-id="9c069-446">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="9c069-446">SALARYCHANGE</span></span>   | <span data-ttu-id="9c069-447">Ændring af løn</span><span class="sxs-lookup"><span data-stu-id="9c069-447">Change of Salary</span></span> | <span data-ttu-id="9c069-448">Kompensation</span><span class="sxs-lookup"><span data-stu-id="9c069-448">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="9c069-449">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="9c069-449">Marital status</span></span>

<span data-ttu-id="9c069-450">Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="9c069-450">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="9c069-451">Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9c069-451">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="9c069-452">Personale</span><span class="sxs-lookup"><span data-stu-id="9c069-452">Human Resources</span></span>                 | <span data-ttu-id="9c069-453">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9c069-453">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="9c069-454">Gift</span><span class="sxs-lookup"><span data-stu-id="9c069-454">Married</span></span>                | <span data-ttu-id="9c069-455">Gift</span><span class="sxs-lookup"><span data-stu-id="9c069-455">Married</span></span>              |
| <span data-ttu-id="9c069-456">Enlig</span><span class="sxs-lookup"><span data-stu-id="9c069-456">Single</span></span>                 | <span data-ttu-id="9c069-457">Enlig</span><span class="sxs-lookup"><span data-stu-id="9c069-457">Single</span></span>               |
| <span data-ttu-id="9c069-458">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="9c069-458">Widowed</span></span>                | <span data-ttu-id="9c069-459">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="9c069-459">Widowed</span></span>              |
| <span data-ttu-id="9c069-460">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="9c069-460">Divorced</span></span>               | <span data-ttu-id="9c069-461">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="9c069-461">Divorced</span></span>             |
| <span data-ttu-id="9c069-462">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="9c069-462">Registered Partnership</span></span> | <span data-ttu-id="9c069-463">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="9c069-463">Domestic Partnership</span></span> |
| <span data-ttu-id="9c069-464">None</span><span class="sxs-lookup"><span data-stu-id="9c069-464">None</span></span>                   | <span data-ttu-id="9c069-465">None</span><span class="sxs-lookup"><span data-stu-id="9c069-465">None</span></span>                 |
| <span data-ttu-id="9c069-466">Samlever</span><span class="sxs-lookup"><span data-stu-id="9c069-466">Cohabiting</span></span>             | <span data-ttu-id="9c069-467">Samlever</span><span class="sxs-lookup"><span data-stu-id="9c069-467">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="9c069-468">Køn</span><span class="sxs-lookup"><span data-stu-id="9c069-468">Gender</span></span>

<span data-ttu-id="9c069-469">Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="9c069-469">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="9c069-470">Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9c069-470">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="9c069-471">Personale</span><span class="sxs-lookup"><span data-stu-id="9c069-471">Human Resources</span></span>       | <span data-ttu-id="9c069-472">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9c069-472">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="9c069-473">Mand</span><span class="sxs-lookup"><span data-stu-id="9c069-473">Male</span></span>         | <span data-ttu-id="9c069-474">Mand</span><span class="sxs-lookup"><span data-stu-id="9c069-474">Male</span></span>            |
| <span data-ttu-id="9c069-475">Kvinde</span><span class="sxs-lookup"><span data-stu-id="9c069-475">Female</span></span>       | <span data-ttu-id="9c069-476">Kvinde</span><span class="sxs-lookup"><span data-stu-id="9c069-476">Female</span></span>          |
| <span data-ttu-id="9c069-477">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="9c069-477">Non-specific</span></span> | <span data-ttu-id="9c069-478">*Understøttes ikke*</span><span class="sxs-lookup"><span data-stu-id="9c069-478">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="9c069-479">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="9c069-479">Earning codes</span></span>

<span data-ttu-id="9c069-480">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="9c069-480">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="9c069-481">Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="9c069-481">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="9c069-482">Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="9c069-482">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="9c069-483">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="9c069-483">Supported frequencies</span></span>

- <span data-ttu-id="9c069-484">Alt</span><span class="sxs-lookup"><span data-stu-id="9c069-484">All</span></span>
- <span data-ttu-id="9c069-485">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="9c069-485">EVERYPAY</span></span>
- <span data-ttu-id="9c069-486">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="9c069-486">EACHPAYPERIOD</span></span>
- <span data-ttu-id="9c069-487">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="9c069-487">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="9c069-488">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="9c069-488">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="9c069-489">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-489">1OFMTH</span></span>
- <span data-ttu-id="9c069-490">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-490">LASTOFMTH</span></span>
- <span data-ttu-id="9c069-491">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-491">2OFMTH</span></span>
- <span data-ttu-id="9c069-492">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-492">3OFMTH</span></span>
- <span data-ttu-id="9c069-493">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-493">4OFMTH</span></span>
- <span data-ttu-id="9c069-494">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-494">5OFMTH</span></span>
- <span data-ttu-id="9c069-495">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-495">1N2OFMTH</span></span>
- <span data-ttu-id="9c069-496">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-496">3N4OFMTH</span></span>
- <span data-ttu-id="9c069-497">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-497">1N3OFMTH</span></span>
- <span data-ttu-id="9c069-498">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-498">1N4OFMTH</span></span>
- <span data-ttu-id="9c069-499">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-499">2N3OFMTH</span></span>
- <span data-ttu-id="9c069-500">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-500">2N4OFMTH</span></span>
- <span data-ttu-id="9c069-501">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-501">1N2N3OFMTH</span></span>
- <span data-ttu-id="9c069-502">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-502">1N2N4OFMTH</span></span>
- <span data-ttu-id="9c069-503">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-503">1N3N4OFMTH</span></span>
- <span data-ttu-id="9c069-504">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-504">2N3N4OFMTH</span></span>
- <span data-ttu-id="9c069-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="9c069-506">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="9c069-506">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="9c069-507">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="9c069-507">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="9c069-508">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="9c069-508">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="9c069-509">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="9c069-509">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="9c069-510">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="9c069-510">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="9c069-511">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="9c069-511">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="9c069-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="9c069-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="9c069-513">Adresser</span><span class="sxs-lookup"><span data-stu-id="9c069-513">Addresses</span></span>

<span data-ttu-id="9c069-514">Identifikation af specifikke koder for land eller område, stat og region (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende.</span><span class="sxs-lookup"><span data-stu-id="9c069-514">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="9c069-515">Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.</span><span class="sxs-lookup"><span data-stu-id="9c069-515">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="9c069-516">Personale</span><span class="sxs-lookup"><span data-stu-id="9c069-516">Human Resources</span></span>          | <span data-ttu-id="9c069-517">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9c069-517">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="9c069-518">Land/område</span><span class="sxs-lookup"><span data-stu-id="9c069-518">Country/Region</span></span>  | <span data-ttu-id="9c069-519">Landekode</span><span class="sxs-lookup"><span data-stu-id="9c069-519">Country Code</span></span>          |
| <span data-ttu-id="9c069-520">Postnummer</span><span class="sxs-lookup"><span data-stu-id="9c069-520">Zip/Postal Code</span></span> | <span data-ttu-id="9c069-521">Postnummer</span><span class="sxs-lookup"><span data-stu-id="9c069-521">Postal Code</span></span>           |
| <span data-ttu-id="9c069-522">Status</span><span class="sxs-lookup"><span data-stu-id="9c069-522">State</span></span>           | <span data-ttu-id="9c069-523">Statskode</span><span class="sxs-lookup"><span data-stu-id="9c069-523">State Code</span></span>            |
| <span data-ttu-id="9c069-524">Bynavn</span><span class="sxs-lookup"><span data-stu-id="9c069-524">City</span></span>            | <span data-ttu-id="9c069-525">Bynavn</span><span class="sxs-lookup"><span data-stu-id="9c069-525">City</span></span>                  |
| <span data-ttu-id="9c069-526">Region</span><span class="sxs-lookup"><span data-stu-id="9c069-526">County</span></span>          | <span data-ttu-id="9c069-527">Område (kommune)</span><span class="sxs-lookup"><span data-stu-id="9c069-527">County (Municipality)</span></span> |
| <span data-ttu-id="9c069-528">Gade</span><span class="sxs-lookup"><span data-stu-id="9c069-528">Street</span></span>          | <span data-ttu-id="9c069-529">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="9c069-529">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="9c069-530">Skatteområder</span><span class="sxs-lookup"><span data-stu-id="9c069-530">Tax regions</span></span>

<span data-ttu-id="9c069-531">Skatteområder bruges til at bestemme den relevante skat, der skal anvendes ved løngenerering.</span><span class="sxs-lookup"><span data-stu-id="9c069-531">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="9c069-532">Skatteområder er tilknyttet Dayforce som placeringsadresser.</span><span class="sxs-lookup"><span data-stu-id="9c069-532">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="9c069-533">Standardskatteområder skal knyttes til arbejderens aktive stilling.</span><span class="sxs-lookup"><span data-stu-id="9c069-533">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="9c069-534">Skatteområde (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-534">Tax region (required)</span></span>
- <span data-ttu-id="9c069-535">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-535">Country/Region (required)</span></span>
- <span data-ttu-id="9c069-536">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-536">State (required)</span></span>
- <span data-ttu-id="9c069-537">Region</span><span class="sxs-lookup"><span data-stu-id="9c069-537">County</span></span> 
- <span data-ttu-id="9c069-538">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="9c069-538">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="9c069-539">Konfigurere dataene for at generere løn i Mexico</span><span class="sxs-lookup"><span data-stu-id="9c069-539">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="9c069-540">Hvis du genererer løn for medarbejdere i Mexico skal følgende elementer konfigureres:</span><span class="sxs-lookup"><span data-stu-id="9c069-540">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="9c069-541">Der kræves afdelinger til stillinger.</span><span class="sxs-lookup"><span data-stu-id="9c069-541">Departments are required on positions.</span></span>
- <span data-ttu-id="9c069-542">Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="9c069-542">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="9c069-543">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="9c069-543">Job types</span></span>

<span data-ttu-id="9c069-544">Jobtyper bruges til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="9c069-544">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="9c069-545">Jobtyper kræves for at behandle løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="9c069-545">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="9c069-546">Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="9c069-546">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="9c069-547">Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.</span><span class="sxs-lookup"><span data-stu-id="9c069-547">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="9c069-548">Der kræves følgende jobtyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="9c069-548">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="9c069-549">Jobtype</span><span class="sxs-lookup"><span data-stu-id="9c069-549">Job type</span></span>   | <span data-ttu-id="9c069-550">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="9c069-550">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="9c069-551">Pr. time</span><span class="sxs-lookup"><span data-stu-id="9c069-551">Hourly</span></span>     | <span data-ttu-id="9c069-552">MX Pr. time</span><span class="sxs-lookup"><span data-stu-id="9c069-552">MX Hourly</span></span>   |
| <span data-ttu-id="9c069-553">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="9c069-553">Salaried</span></span>   | <span data-ttu-id="9c069-554">MX Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="9c069-554">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="9c069-555">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="9c069-555">Position types</span></span> 

<span data-ttu-id="9c069-556">Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet.</span><span class="sxs-lookup"><span data-stu-id="9c069-556">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="9c069-557">Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="9c069-557">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="9c069-558">Der kræves følgende stillingstyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="9c069-558">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="9c069-559">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="9c069-559">Position type</span></span>   | <span data-ttu-id="9c069-560">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="9c069-560">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="9c069-561">Fuld tid</span><span class="sxs-lookup"><span data-stu-id="9c069-561">Full-time</span></span>       | <span data-ttu-id="9c069-562">Fuldtidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="9c069-562">Full time employee</span></span> |
| <span data-ttu-id="9c069-563">Deltid</span><span class="sxs-lookup"><span data-stu-id="9c069-563">Part-time</span></span>       | <span data-ttu-id="9c069-564">Deltidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="9c069-564">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="9c069-565">Årsagskoder</span><span class="sxs-lookup"><span data-stu-id="9c069-565">Reason codes</span></span>

<span data-ttu-id="9c069-566">Årsagskoder indeholder oplysninger om status for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="9c069-566">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="9c069-567">Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.</span><span class="sxs-lookup"><span data-stu-id="9c069-567">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="9c069-568">Der kræves følgende årsagskoder og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="9c069-568">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="9c069-569">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="9c069-569">Reason code</span></span>            | <span data-ttu-id="9c069-570">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="9c069-570">Description</span></span>                    | <span data-ttu-id="9c069-571">Anvendelige scenarier</span><span class="sxs-lookup"><span data-stu-id="9c069-571">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="9c069-572">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="9c069-572">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="9c069-573">Afgang før første løn</span><span class="sxs-lookup"><span data-stu-id="9c069-573">Departure before first payroll</span></span> | <span data-ttu-id="9c069-574">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="9c069-574">Terminate worker</span></span>     |
| <span data-ttu-id="9c069-575">OPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="9c069-575">RESIGNATION</span></span>            | <span data-ttu-id="9c069-576">Opsigelse</span><span class="sxs-lookup"><span data-stu-id="9c069-576">Resignation</span></span>                    | <span data-ttu-id="9c069-577">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="9c069-577">Terminate worker</span></span>     |
| <span data-ttu-id="9c069-578">PENSION</span><span class="sxs-lookup"><span data-stu-id="9c069-578">PENSION</span></span>                | <span data-ttu-id="9c069-579">Pension</span><span class="sxs-lookup"><span data-stu-id="9c069-579">Pension</span></span>                        | <span data-ttu-id="9c069-580">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="9c069-580">Terminate worker</span></span>     |
| <span data-ttu-id="9c069-581">OPHØR</span><span class="sxs-lookup"><span data-stu-id="9c069-581">TERMINATION</span></span>            | <span data-ttu-id="9c069-582">Ophør</span><span class="sxs-lookup"><span data-stu-id="9c069-582">Termination</span></span>                    | <span data-ttu-id="9c069-583">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="9c069-583">Terminate worker</span></span>     |
| <span data-ttu-id="9c069-584">PENSION</span><span class="sxs-lookup"><span data-stu-id="9c069-584">RETIREMENT</span></span>             | <span data-ttu-id="9c069-585">Pension</span><span class="sxs-lookup"><span data-stu-id="9c069-585">Retirement</span></span>                     | <span data-ttu-id="9c069-586">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="9c069-586">Terminate worker</span></span>     |
| <span data-ttu-id="9c069-587">FRAVÆRENDE</span><span class="sxs-lookup"><span data-stu-id="9c069-587">ABSENTEE</span></span>               | <span data-ttu-id="9c069-588">Fraværende</span><span class="sxs-lookup"><span data-stu-id="9c069-588">Absentee</span></span>                       | <span data-ttu-id="9c069-589">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="9c069-589">Terminate worker</span></span>     |
| <span data-ttu-id="9c069-590">ANDET</span><span class="sxs-lookup"><span data-stu-id="9c069-590">OTHER</span></span>                  | <span data-ttu-id="9c069-591">Andre årsager</span><span class="sxs-lookup"><span data-stu-id="9c069-591">Other Reasons</span></span>                  | <span data-ttu-id="9c069-592">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="9c069-592">Terminate worker</span></span>     |
| <span data-ttu-id="9c069-593">LUKNING</span><span class="sxs-lookup"><span data-stu-id="9c069-593">CLOSURE</span></span>                | <span data-ttu-id="9c069-594">Virksomhedslukning</span><span class="sxs-lookup"><span data-stu-id="9c069-594">Business Closure</span></span>               | <span data-ttu-id="9c069-595">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="9c069-595">Terminate worker</span></span>     |
| <span data-ttu-id="9c069-596">DØDSFALD</span><span class="sxs-lookup"><span data-stu-id="9c069-596">DEATH</span></span>                  | <span data-ttu-id="9c069-597">Dødsfald</span><span class="sxs-lookup"><span data-stu-id="9c069-597">Death</span></span>                          | <span data-ttu-id="9c069-598">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="9c069-598">Terminate worker</span></span>     |
| <span data-ttu-id="9c069-599">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="9c069-599">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="9c069-600">Orlov</span><span class="sxs-lookup"><span data-stu-id="9c069-600">Leave of Absence</span></span>               | <span data-ttu-id="9c069-601">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="9c069-601">Terminate worker</span></span>     |
| <span data-ttu-id="9c069-602">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="9c069-602">CONTRACTEND</span></span>            | <span data-ttu-id="9c069-603">Kontraktudløb</span><span class="sxs-lookup"><span data-stu-id="9c069-603">End of Contract</span></span>                | <span data-ttu-id="9c069-604">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="9c069-604">Terminate worker</span></span>     |
| <span data-ttu-id="9c069-605">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="9c069-605">SALARYCHANGE</span></span>           | <span data-ttu-id="9c069-606">Ændring af løn</span><span class="sxs-lookup"><span data-stu-id="9c069-606">Change of Salary</span></span>               | <span data-ttu-id="9c069-607">Kompensation</span><span class="sxs-lookup"><span data-stu-id="9c069-607">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="9c069-608">Ansættelsesvilkår</span><span class="sxs-lookup"><span data-stu-id="9c069-608">Terms of employment</span></span>

<span data-ttu-id="9c069-609">Ansættelsesvilkår bruges til at oprette kategorier for ansættelsesvilkår.</span><span class="sxs-lookup"><span data-stu-id="9c069-609">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="9c069-610">Vilkårene knyttes til Dayforce som beskæftigelsesindikatorværdier.</span><span class="sxs-lookup"><span data-stu-id="9c069-610">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="9c069-611">Følgende begreber for beskæftigelse og beskrivelser er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="9c069-611">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="9c069-612">Ansættelsesvilkår</span><span class="sxs-lookup"><span data-stu-id="9c069-612">Terms of employment</span></span>   | <span data-ttu-id="9c069-613">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="9c069-613">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="9c069-614">Regulær</span><span class="sxs-lookup"><span data-stu-id="9c069-614">Regular</span></span>               | <span data-ttu-id="9c069-615">Regulær</span><span class="sxs-lookup"><span data-stu-id="9c069-615">Regular</span></span>     |
| <span data-ttu-id="9c069-616">Direkte</span><span class="sxs-lookup"><span data-stu-id="9c069-616">Direct</span></span>                | <span data-ttu-id="9c069-617">Direkte</span><span class="sxs-lookup"><span data-stu-id="9c069-617">Direct</span></span>      |
| <span data-ttu-id="9c069-618">Turnustjeneste</span><span class="sxs-lookup"><span data-stu-id="9c069-618">Internship</span></span>            | <span data-ttu-id="9c069-619">Turnustjeneste</span><span class="sxs-lookup"><span data-stu-id="9c069-619">Internship</span></span>  |
| <span data-ttu-id="9c069-620">Permanent</span><span class="sxs-lookup"><span data-stu-id="9c069-620">Permanent</span></span>             | <span data-ttu-id="9c069-621">Permanent</span><span class="sxs-lookup"><span data-stu-id="9c069-621">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="9c069-622">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="9c069-622">Marital status</span></span>

<span data-ttu-id="9c069-623">Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="9c069-623">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="9c069-624">Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9c069-624">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="9c069-625">Personale</span><span class="sxs-lookup"><span data-stu-id="9c069-625">Human Resources</span></span>                 | <span data-ttu-id="9c069-626">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9c069-626">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="9c069-627">Gift</span><span class="sxs-lookup"><span data-stu-id="9c069-627">Married</span></span>                | <span data-ttu-id="9c069-628">Gift</span><span class="sxs-lookup"><span data-stu-id="9c069-628">Married</span></span>                   |
| <span data-ttu-id="9c069-629">Enlig</span><span class="sxs-lookup"><span data-stu-id="9c069-629">Single</span></span>                 | <span data-ttu-id="9c069-630">Enlig</span><span class="sxs-lookup"><span data-stu-id="9c069-630">Single</span></span>                    |
| <span data-ttu-id="9c069-631">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="9c069-631">Widowed</span></span>                | <span data-ttu-id="9c069-632">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="9c069-632">Widowed</span></span>                   |
| <span data-ttu-id="9c069-633">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="9c069-633">Divorced</span></span>               | <span data-ttu-id="9c069-634">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="9c069-634">Divorced</span></span>                  |
| <span data-ttu-id="9c069-635">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="9c069-635">Registered Partnership</span></span> | <span data-ttu-id="9c069-636">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="9c069-636">Domestic Partnership</span></span>      |
| <span data-ttu-id="9c069-637">None</span><span class="sxs-lookup"><span data-stu-id="9c069-637">None</span></span>                   | <span data-ttu-id="9c069-638">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="9c069-638">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="9c069-639">Samlever</span><span class="sxs-lookup"><span data-stu-id="9c069-639">Cohabiting</span></span>             | <span data-ttu-id="9c069-640">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="9c069-640">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="9c069-641">Køn</span><span class="sxs-lookup"><span data-stu-id="9c069-641">Gender</span></span>

<span data-ttu-id="9c069-642">Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="9c069-642">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="9c069-643">Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9c069-643">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="9c069-644">Personale</span><span class="sxs-lookup"><span data-stu-id="9c069-644">Human Resources</span></span>       | <span data-ttu-id="9c069-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9c069-645">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="9c069-646">Mand</span><span class="sxs-lookup"><span data-stu-id="9c069-646">Male</span></span>         | <span data-ttu-id="9c069-647">Mand</span><span class="sxs-lookup"><span data-stu-id="9c069-647">Male</span></span>                      |
| <span data-ttu-id="9c069-648">Kvinde</span><span class="sxs-lookup"><span data-stu-id="9c069-648">Female</span></span>       | <span data-ttu-id="9c069-649">Kvinde</span><span class="sxs-lookup"><span data-stu-id="9c069-649">Female</span></span>                    |
| <span data-ttu-id="9c069-650">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="9c069-650">Non-specific</span></span> | <span data-ttu-id="9c069-651">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="9c069-651">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="9c069-652">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="9c069-652">Payment method</span></span>

<span data-ttu-id="9c069-653">Betalingsmetoder giver medarbejderen og virksomheden en måde til at beskrive, hvordan medarbejdere skal betales.</span><span class="sxs-lookup"><span data-stu-id="9c069-653">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="9c069-654">Betalingsmåder knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="9c069-654">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="9c069-655">Følgende tabel viser, hvordan betalingsmetoder knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9c069-655">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="9c069-656">Personale</span><span class="sxs-lookup"><span data-stu-id="9c069-656">Human Resources</span></span>             | <span data-ttu-id="9c069-657">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9c069-657">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="9c069-658">Indløsning</span><span class="sxs-lookup"><span data-stu-id="9c069-658">Cash</span></span>               | <span data-ttu-id="9c069-659">Indløsning</span><span class="sxs-lookup"><span data-stu-id="9c069-659">Cash</span></span>                      |
| <span data-ttu-id="9c069-660">Elektronisk betaling</span><span class="sxs-lookup"><span data-stu-id="9c069-660">Electronic Payment</span></span> | <span data-ttu-id="9c069-661">Ompostering</span><span class="sxs-lookup"><span data-stu-id="9c069-661">Transfer</span></span>                  |
| <span data-ttu-id="9c069-662">Check</span><span class="sxs-lookup"><span data-stu-id="9c069-662">Check</span></span>              | <span data-ttu-id="9c069-663">Check</span><span class="sxs-lookup"><span data-stu-id="9c069-663">Cheque</span></span>                    |
| <span data-ttu-id="9c069-664">Bankanvisning</span><span class="sxs-lookup"><span data-stu-id="9c069-664">Bank Draft</span></span>         | <span data-ttu-id="9c069-665">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="9c069-665">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="9c069-666">Andre</span><span class="sxs-lookup"><span data-stu-id="9c069-666">Other</span></span>              | <span data-ttu-id="9c069-667">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="9c069-667">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="9c069-668">Bankkontotype</span><span class="sxs-lookup"><span data-stu-id="9c069-668">Bank account type</span></span>

<span data-ttu-id="9c069-669">Bankkontotyper bruges til elektroniske betalinger til medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="9c069-669">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="9c069-670">Bankkontotyper knyttes til Dayforce som overførselskontooplysninger.</span><span class="sxs-lookup"><span data-stu-id="9c069-670">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="9c069-671">Bankkontotyperne oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="9c069-671">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="9c069-672">Personale</span><span class="sxs-lookup"><span data-stu-id="9c069-672">Human Resources</span></span>            | <span data-ttu-id="9c069-673">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9c069-673">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="9c069-674">Checkkonto</span><span class="sxs-lookup"><span data-stu-id="9c069-674">Checking Account</span></span>  | <span data-ttu-id="9c069-675">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="9c069-675">CheckingAccount</span></span>           |
| <span data-ttu-id="9c069-676">Lønkonto</span><span class="sxs-lookup"><span data-stu-id="9c069-676">Payroll Account</span></span>   | <span data-ttu-id="9c069-677">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="9c069-677">PayrollAccount</span></span>            |
| <span data-ttu-id="9c069-678">Opsparingskonto</span><span class="sxs-lookup"><span data-stu-id="9c069-678">Savings Account</span></span>   | <span data-ttu-id="9c069-679">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="9c069-679">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="9c069-680">BankGirot-konto</span><span class="sxs-lookup"><span data-stu-id="9c069-680">BankGirot account</span></span> | <span data-ttu-id="9c069-681">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="9c069-681">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="9c069-682">PlusGirot-konto</span><span class="sxs-lookup"><span data-stu-id="9c069-682">PlusGirot account</span></span> | <span data-ttu-id="9c069-683">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="9c069-683">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="9c069-684">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="9c069-684">Earning codes</span></span>

<span data-ttu-id="9c069-685">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="9c069-685">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="9c069-686">Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="9c069-686">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="9c069-687">Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="9c069-687">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="9c069-688">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="9c069-688">Supported frequencies</span></span>

- <span data-ttu-id="9c069-689">Alt</span><span class="sxs-lookup"><span data-stu-id="9c069-689">All</span></span>
- <span data-ttu-id="9c069-690">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="9c069-690">EVERYPAY</span></span>
- <span data-ttu-id="9c069-691">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="9c069-691">EACHPAYPERIOD</span></span>
- <span data-ttu-id="9c069-692">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="9c069-692">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="9c069-693">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="9c069-693">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="9c069-694">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-694">1OFMTH</span></span>
- <span data-ttu-id="9c069-695">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-695">LASTOFMTH</span></span>
- <span data-ttu-id="9c069-696">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-696">2OFMTH</span></span>
- <span data-ttu-id="9c069-697">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-697">3OFMTH</span></span>
- <span data-ttu-id="9c069-698">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-698">4OFMTH</span></span>
- <span data-ttu-id="9c069-699">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-699">5OFMTH</span></span>
- <span data-ttu-id="9c069-700">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-700">1N2OFMTH</span></span>
- <span data-ttu-id="9c069-701">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-701">3N4OFMTH</span></span>
- <span data-ttu-id="9c069-702">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-702">1N3OFMTH</span></span>
- <span data-ttu-id="9c069-703">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-703">1N4OFMTH</span></span>
- <span data-ttu-id="9c069-704">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-704">2N3OFMTH</span></span>
- <span data-ttu-id="9c069-705">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-705">2N4OFMTH</span></span>
- <span data-ttu-id="9c069-706">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-706">1N2N3OFMTH</span></span>
- <span data-ttu-id="9c069-707">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-707">1N2N4OFMTH</span></span>
- <span data-ttu-id="9c069-708">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-708">1N3N4OFMTH</span></span>
- <span data-ttu-id="9c069-709">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-709">2N3N4OFMTH</span></span>
- <span data-ttu-id="9c069-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9c069-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="9c069-711">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="9c069-711">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="9c069-712">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="9c069-712">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="9c069-713">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="9c069-713">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="9c069-714">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="9c069-714">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="9c069-715">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="9c069-715">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="9c069-716">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="9c069-716">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="9c069-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="9c069-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="9c069-718">Adresser</span><span class="sxs-lookup"><span data-stu-id="9c069-718">Addresses</span></span>

<span data-ttu-id="9c069-719">Identifikation af specifikke koder for land eller område, stat og region (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende.</span><span class="sxs-lookup"><span data-stu-id="9c069-719">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="9c069-720">Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.</span><span class="sxs-lookup"><span data-stu-id="9c069-720">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="9c069-721">Personale</span><span class="sxs-lookup"><span data-stu-id="9c069-721">Human Resources</span></span>              | <span data-ttu-id="9c069-722">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9c069-722">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="9c069-723">Land/område</span><span class="sxs-lookup"><span data-stu-id="9c069-723">Country/Region</span></span>      | <span data-ttu-id="9c069-724">Landekode</span><span class="sxs-lookup"><span data-stu-id="9c069-724">Country Code</span></span>          |
| <span data-ttu-id="9c069-725">Postnummer</span><span class="sxs-lookup"><span data-stu-id="9c069-725">Zip/Postal Code</span></span>     | <span data-ttu-id="9c069-726">Postnummer</span><span class="sxs-lookup"><span data-stu-id="9c069-726">Postal Code</span></span>           |
| <span data-ttu-id="9c069-727">Status</span><span class="sxs-lookup"><span data-stu-id="9c069-727">State</span></span>               | <span data-ttu-id="9c069-728">Statskode</span><span class="sxs-lookup"><span data-stu-id="9c069-728">State Code</span></span>            |
| <span data-ttu-id="9c069-729">Bynavn</span><span class="sxs-lookup"><span data-stu-id="9c069-729">City</span></span>                | <span data-ttu-id="9c069-730">Bynavn</span><span class="sxs-lookup"><span data-stu-id="9c069-730">City</span></span>                  |
| <span data-ttu-id="9c069-731">Region</span><span class="sxs-lookup"><span data-stu-id="9c069-731">County</span></span>              | <span data-ttu-id="9c069-732">Område (kommune)</span><span class="sxs-lookup"><span data-stu-id="9c069-732">County (Municipality)</span></span> |
| <span data-ttu-id="9c069-733">Gade</span><span class="sxs-lookup"><span data-stu-id="9c069-733">Street</span></span>              | <span data-ttu-id="9c069-734">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="9c069-734">Address Line 1</span></span>        |
| <span data-ttu-id="9c069-735">Gadenummer</span><span class="sxs-lookup"><span data-stu-id="9c069-735">Street Number</span></span>       | <span data-ttu-id="9c069-736">Adresselinje 2</span><span class="sxs-lookup"><span data-stu-id="9c069-736">Address Line 2</span></span>        |
| <span data-ttu-id="9c069-737">Bygningskomplement</span><span class="sxs-lookup"><span data-stu-id="9c069-737">Building Complement</span></span> | <span data-ttu-id="9c069-738">Adresselinje 5</span><span class="sxs-lookup"><span data-stu-id="9c069-738">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="9c069-739">Pasnummer</span><span class="sxs-lookup"><span data-stu-id="9c069-739">Passport number</span></span>

<span data-ttu-id="9c069-740">Medarbejdere kan erklære pasoplysninger.</span><span class="sxs-lookup"><span data-stu-id="9c069-740">Employees can declare passport information.</span></span> <span data-ttu-id="9c069-741">Disse oplysninger er af identifikationstypen **Pas** og er integreret i Dayforce som en del af en medarbejders Mexico-specifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="9c069-741">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="9c069-742">Identifikationstype = "Pas"</span><span class="sxs-lookup"><span data-stu-id="9c069-742">Identification Type = "Passport"</span></span>
- <span data-ttu-id="9c069-743">Udstedt den</span><span class="sxs-lookup"><span data-stu-id="9c069-743">Issued Date</span></span>
- <span data-ttu-id="9c069-744">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="9c069-744">Expiration Date</span></span>

<span data-ttu-id="9c069-745">Medarbejdere kan angive flere identifikationsnumre af **Pas**-identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="9c069-745">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="9c069-746">Men det er kun den aktuelle aktive paspost, der integreres i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9c069-746">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="9c069-747">Hvis alle pasposter er udløbet, integreres det pas, der senest blev udstedt, i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9c069-747">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

