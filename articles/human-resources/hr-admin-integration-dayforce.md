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
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d150daa92fe79cf6620ce5ddf1a01f369c64053
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051491"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="51e04-104">Konfigurer integration med Dayforce</span><span class="sxs-lookup"><span data-stu-id="51e04-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="51e04-105">Integrationen mellem Microsoft Dynamics 365 Human Resources og Ceridian Dayforce er baseret på flere konfigurationstrin, der er beskrevet i dette emne.</span><span class="sxs-lookup"><span data-stu-id="51e04-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="51e04-106">Du skal konfigurere integrationen i både Human Resources og Dayforce, før du kan behandle en lønkørsel.</span><span class="sxs-lookup"><span data-stu-id="51e04-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="51e04-107">Når du bruger en tjeneste, f.eks. Dayforce, til at fuldføre lønkørsler, skal du aktivere integrationen i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="51e04-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="51e04-108">Integrationen kræver bestemte data fra Human Resources.</span><span class="sxs-lookup"><span data-stu-id="51e04-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="51e04-109">Du skal derfor kontrollere, at data, der er knyttet til Dayforce, er konfigureret i Human Resources på en måde, der understøtter integrationen.</span><span class="sxs-lookup"><span data-stu-id="51e04-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="51e04-110">Integrationen bruger følgende brede kategorier af data.</span><span class="sxs-lookup"><span data-stu-id="51e04-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="51e04-111">Human Resourcesdata</span><span class="sxs-lookup"><span data-stu-id="51e04-111">Human resources data</span></span>
- <span data-ttu-id="51e04-112">Kompensationsdata</span><span class="sxs-lookup"><span data-stu-id="51e04-112">Compensation data</span></span>
- <span data-ttu-id="51e04-113">Lønoplysninger, f.eks. løncyklusser, betalingsperioder og lønkoder</span><span class="sxs-lookup"><span data-stu-id="51e04-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="51e04-114">Arbejderdata</span><span class="sxs-lookup"><span data-stu-id="51e04-114">Worker data</span></span>

<span data-ttu-id="51e04-115">Denne artikel beskriver de trin, du skal udføre for at aktivere integrationen.</span><span class="sxs-lookup"><span data-stu-id="51e04-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="51e04-116">Det forklarer også typerne af data og oplysninger om konfigurationen, der kræves til integrationen.</span><span class="sxs-lookup"><span data-stu-id="51e04-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="51e04-117">Aktivere integrationen.</span><span class="sxs-lookup"><span data-stu-id="51e04-117">Enable the integration</span></span>

<span data-ttu-id="51e04-118">I Human Resources skal du aktivere integrationen og angive konfigurationsoplysningerne for at oprette forbindelse til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="51e04-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="51e04-119">Hvis den finanspostering, der er oprettet, skal importeres til Microsoft Dynamics 365 Finance, skal du også konfigurere en Microsoft Azure-lagerkonto og angive Azure-lagerets forbindelsesstreng i Finance.</span><span class="sxs-lookup"><span data-stu-id="51e04-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="51e04-120">Følg disse trin for at aktivere integrationen i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="51e04-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="51e04-121">På siden **Systemadministration** skal du vælge **Integrationskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="51e04-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="51e04-122">Angiv det sikre FTP-slutpunkt og den sikre FTP-mappesti.</span><span class="sxs-lookup"><span data-stu-id="51e04-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="51e04-123">Angiv brugernavnet og adgangskoden for den bruger, der skal have adgang til det sikre FTP-slutpunkt og den sikre mappesti.</span><span class="sxs-lookup"><span data-stu-id="51e04-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="51e04-124">Test forbindelsen, som krævet, og angiv indstillingen **Aktivér lønintegration** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="51e04-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="51e04-125">Når integrationen er aktiveret, oprettes dataeksportpakken og -filerne, og hyppigheden angives.</span><span class="sxs-lookup"><span data-stu-id="51e04-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="51e04-126">Du kan ændre denne frekvens efter behov.</span><span class="sxs-lookup"><span data-stu-id="51e04-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="51e04-127">Yderligere oplysninger om Azure-lagerkonti og Azure-lagerforbindelsesstrenge finder du i følgende Azure-artikler:</span><span class="sxs-lookup"><span data-stu-id="51e04-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="51e04-128">Om Azure-lagerkonti</span><span class="sxs-lookup"><span data-stu-id="51e04-128">About Azure storage accounts</span></span>](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="51e04-129">Konfigurere forbindelsesstrenge for Azure-datalager</span><span class="sxs-lookup"><span data-stu-id="51e04-129">Configure Azure Storage connection strings</span></span>](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="51e04-130">Tekniske oplysninger ved aktivering af lønintegration</span><span class="sxs-lookup"><span data-stu-id="51e04-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="51e04-131">Aktivering af lønintegration har to primære effekter:</span><span class="sxs-lookup"><span data-stu-id="51e04-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="51e04-132">Der oprettes et dataeksport projekt ved navn "Lønintegrationseksport".</span><span class="sxs-lookup"><span data-stu-id="51e04-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="51e04-133">Dette projekt indeholder de objekter og felter, der kræves til lønintegration.</span><span class="sxs-lookup"><span data-stu-id="51e04-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="51e04-134">Hvis du vil undersøge projektet, skal du gå til **Systemadministration**, vælge feltet **Datastyring** og derefter åbne dataprojektet på listen over projekter.</span><span class="sxs-lookup"><span data-stu-id="51e04-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="51e04-135">Dette batchjob udfører dataeksportprojektet, krypterer den resulterende datapakke og overfører datapakkefilen til det SFTP-slutpunkt, der er konfigureret på skærmen **Integrationskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="51e04-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="51e04-136">Den datapakke, der overføres til SFTP-slutpunktet, krypteres ved hjælp af en nøgle, der er entydig for pakken.</span><span class="sxs-lookup"><span data-stu-id="51e04-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="51e04-137">Nøglen er i en Azure Key Vault, der kun kan åbnes af Ceridian.</span><span class="sxs-lookup"><span data-stu-id="51e04-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="51e04-138">Det er ikke muligt at dekryptere og undersøge datapakkens indhold.</span><span class="sxs-lookup"><span data-stu-id="51e04-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="51e04-139">Hvis du har brug for at undersøge indholdet af datapakken, skal du eksportere dataprojektet "Lønintegrationseksport" manuelt, download det og derefter åbne det.</span><span class="sxs-lookup"><span data-stu-id="51e04-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="51e04-140">Manuel eksport anvender ikke kryptering eller overførsel af pakken.</span><span class="sxs-lookup"><span data-stu-id="51e04-140">Manual export will not apply encryption or transfer the package.</span></span>
> <span data-ttu-id="51e04-141">I tilfælde, hvor integrationsfilerne sendes fra et Dynamics 365 Human Resources UAT- eller sandkassemiljø til et Ceridian Dayforce-testmiljø, kan du bruge følgende URL-adresse til Key Vault: https://payrollintegrationprod.vault.azure.net.</span><span class="sxs-lookup"><span data-stu-id="51e04-141">For instances where the integration files are sent from a Dynamics 365 Human Resources UAT or Sandbox environment to a Ceridian Dayforce Test environment, you can use the following key vault URL: https://payrollintegrationprod.vault.azure.net.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="51e04-142">Konfigurere dine data</span><span class="sxs-lookup"><span data-stu-id="51e04-142">Configure your data</span></span> 

<span data-ttu-id="51e04-143">Hvis du vil behandle løn, skal du konfigurere personaledata i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="51e04-143">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="51e04-144">Du skal angive virksomhedens data, f.eks. job og stillinger, sammen med frynsegoder og kompensationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="51e04-144">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="51e04-145">Disse oplysninger indeholder oplysningerne om ansættelse, løn og fradrag, der kræves for at generere løn for medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="51e04-145">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="51e04-146">Human Resourcesdata</span><span class="sxs-lookup"><span data-stu-id="51e04-146">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="51e04-147">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="51e04-147">Benefits</span></span> 

<span data-ttu-id="51e04-148">Human Resources indeholder en række værktøjer til konfiguration og vedligeholdelse af frynsegoder, fradrag og arbejderkompensationsplaner, som en organisation tilbyder eller behandler for sine ansatte.</span><span class="sxs-lookup"><span data-stu-id="51e04-148">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="51e04-149">Når du opretter frynsegoder, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="51e04-149">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="51e04-150">Frynsegodeplaner</span><span class="sxs-lookup"><span data-stu-id="51e04-150">Benefit plans</span></span>

- <span data-ttu-id="51e04-151">Plan (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-151">Plan (required)</span></span>
- <span data-ttu-id="51e04-152">Type (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-152">Type (required)</span></span>
- <span data-ttu-id="51e04-153">Løneffekt (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-153">Payroll impact (required)</span></span>
- <span data-ttu-id="51e04-154">Opkræv restancer</span><span class="sxs-lookup"><span data-stu-id="51e04-154">Recover arrears</span></span>
- <span data-ttu-id="51e04-155">Fradragsmetode</span><span class="sxs-lookup"><span data-stu-id="51e04-155">Deduction method</span></span>
- <span data-ttu-id="51e04-156">Prioriteret fradrag</span><span class="sxs-lookup"><span data-stu-id="51e04-156">Deduction priority</span></span>
- <span data-ttu-id="51e04-157">Grænseperiode</span><span class="sxs-lookup"><span data-stu-id="51e04-157">Limit period</span></span>
- <span data-ttu-id="51e04-158">Beløb for grænse</span><span class="sxs-lookup"><span data-stu-id="51e04-158">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="51e04-159">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="51e04-159">Benefits</span></span>

- <span data-ttu-id="51e04-160">Plan (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-160">Plan (required)</span></span>
- <span data-ttu-id="51e04-161">Type (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-161">Type (required)</span></span>
- <span data-ttu-id="51e04-162">Mulighed (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-162">Option (required)</span></span>
- <span data-ttu-id="51e04-163">Frynsegode-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-163">Benefit ID (required)</span></span>
- <span data-ttu-id="51e04-164">Frekvens</span><span class="sxs-lookup"><span data-stu-id="51e04-164">Frequency</span></span>
- <span data-ttu-id="51e04-165">Basis</span><span class="sxs-lookup"><span data-stu-id="51e04-165">Basis</span></span>
- <span data-ttu-id="51e04-166">Beløb eller sats</span><span class="sxs-lookup"><span data-stu-id="51e04-166">Amount or rate</span></span>
- <span data-ttu-id="51e04-167">Lønkode</span><span class="sxs-lookup"><span data-stu-id="51e04-167">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="51e04-168">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="51e04-168">Supported frequencies</span></span> 

- <span data-ttu-id="51e04-169">Ugentlig</span><span class="sxs-lookup"><span data-stu-id="51e04-169">Weekly</span></span>
- <span data-ttu-id="51e04-170">Pr. 14 dage</span><span class="sxs-lookup"><span data-stu-id="51e04-170">Bi-weekly</span></span>
- <span data-ttu-id="51e04-171">To gange om måneden</span><span class="sxs-lookup"><span data-stu-id="51e04-171">Semi-monthly</span></span>
- <span data-ttu-id="51e04-172">Månedlig</span><span class="sxs-lookup"><span data-stu-id="51e04-172">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="51e04-173">Understøttede grundlag</span><span class="sxs-lookup"><span data-stu-id="51e04-173">Supported bases</span></span> 

- <span data-ttu-id="51e04-174">Fast beløb</span><span class="sxs-lookup"><span data-stu-id="51e04-174">Fixed amount</span></span>
- <span data-ttu-id="51e04-175">Procentdel af løn</span><span class="sxs-lookup"><span data-stu-id="51e04-175">Percent of earnings</span></span>
- <span data-ttu-id="51e04-176">Produktive timer</span><span class="sxs-lookup"><span data-stu-id="51e04-176">Productive hours</span></span>

<span data-ttu-id="51e04-177">Dayforce opretter følgende fradrag, der er baseret på den løneffekt, der er defineret på frynsegodeplanen.</span><span class="sxs-lookup"><span data-stu-id="51e04-177">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="51e04-178">Valg i Human Resources</span><span class="sxs-lookup"><span data-stu-id="51e04-178">Selection in Human Resources</span></span>        | <span data-ttu-id="51e04-179">Resultat i Dayforce</span><span class="sxs-lookup"><span data-stu-id="51e04-179">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="51e04-180">Ingen</span><span class="sxs-lookup"><span data-stu-id="51e04-180">None</span></span>                       | <span data-ttu-id="51e04-181">Der oprettes ikke noget fradrag.</span><span class="sxs-lookup"><span data-stu-id="51e04-181">No deduction is created.</span></span>                      |
| <span data-ttu-id="51e04-182">Kun fradrag</span><span class="sxs-lookup"><span data-stu-id="51e04-182">Deduction only</span></span>             | <span data-ttu-id="51e04-183">Der oprettes et medarbejderfradrag.</span><span class="sxs-lookup"><span data-stu-id="51e04-183">An employee deduction is created.</span></span>             |
| <span data-ttu-id="51e04-184">Kun bidrag</span><span class="sxs-lookup"><span data-stu-id="51e04-184">Contribution only</span></span>          | <span data-ttu-id="51e04-185">Der oprettes et arbejdsgiverfradrag.</span><span class="sxs-lookup"><span data-stu-id="51e04-185">An employer deduction is created.</span></span>             |
| <span data-ttu-id="51e04-186">Fradrag og bidrag</span><span class="sxs-lookup"><span data-stu-id="51e04-186">Deduction and contribution</span></span> | <span data-ttu-id="51e04-187">Der oprettes medarbejder- og arbejdsgiverfradrag.</span><span class="sxs-lookup"><span data-stu-id="51e04-187">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="51e04-188">Du kan finde flere oplysninger om, hvordan du definerer og administrerer et frynsegodeprogram i følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="51e04-188">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="51e04-189">Levere et frynsegodeprogram for medarbejdere</span><span class="sxs-lookup"><span data-stu-id="51e04-189">Deliver an employee benefits program</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="51e04-190">Opret et nyt frynsegode</span><span class="sxs-lookup"><span data-stu-id="51e04-190">Create a new benefit</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="51e04-191">Definere regler og politikker for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="51e04-191">Define benefit eligibility rules and policies</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="51e04-192">Tilmelde og fjerne frynsegoder fra arbejdere</span><span class="sxs-lookup"><span data-stu-id="51e04-192">Enroll and remove benefits from workers</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="51e04-193">Kompensation</span><span class="sxs-lookup"><span data-stu-id="51e04-193">Compensation</span></span> 

<span data-ttu-id="51e04-194">Kompensationsstyring bruges til at styre fordelingen af grundløn og bonusser.</span><span class="sxs-lookup"><span data-stu-id="51e04-194">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="51e04-195">En medarbejders faste grundløn og kvalifikationstillæg styres gennem faste lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="51e04-195">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="51e04-196">Betalingen af incitamentsløn som f.eks. bonusudbetalinger, præstationsbonusser, aktieoptioner og tildelte aktier samt engangsbonusser styres ved hjælp af variable lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="51e04-196">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="51e04-197">Dayforce anvendes kompensationsoplysninger til at beregne en medarbejders timesats eller årlige sats.</span><span class="sxs-lookup"><span data-stu-id="51e04-197">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="51e04-198">Konverteringer af planer for fast løn og lønsats er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="51e04-198">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="51e04-199">Medarbejderne skal være knyttet til en plan for fast løn.</span><span class="sxs-lookup"><span data-stu-id="51e04-199">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="51e04-200">Du kan finde flere oplysninger om kompensationsplaner i følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="51e04-200">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="51e04-201">Oprette planer for fast løn</span><span class="sxs-lookup"><span data-stu-id="51e04-201">Create fixed compensation plans</span></span>](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="51e04-202">Oprette planer for variabel kompensation</span><span class="sxs-lookup"><span data-stu-id="51e04-202">Create variable compensation plans</span></span>](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="51e04-203">Udarbejde løn-/kompensationsstruktur og -planer</span><span class="sxs-lookup"><span data-stu-id="51e04-203">Develop salary/compensation structure and plans</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="51e04-204">Proceskompensation</span><span class="sxs-lookup"><span data-stu-id="51e04-204">Process compensation</span></span>](/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="51e04-205">Definere kompensationsproces og beregne resultater</span><span class="sxs-lookup"><span data-stu-id="51e04-205">Define compensation process and calculate results</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="51e04-206">Melde en medarbejder til en fast lønplan</span><span class="sxs-lookup"><span data-stu-id="51e04-206">Enroll an employee in a fixed compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="51e04-207">Melde en medarbejder til en variabel lønplan</span><span class="sxs-lookup"><span data-stu-id="51e04-207">Enroll an employee in a variable compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="51e04-208">Job</span><span class="sxs-lookup"><span data-stu-id="51e04-208">Jobs</span></span> 

<span data-ttu-id="51e04-209">Et job er en samling af de opgaver og ansvarsområder, der kræves af en person, der udfører et job.</span><span class="sxs-lookup"><span data-stu-id="51e04-209">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="51e04-210">Du kan finde flere oplysninger i følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="51e04-210">For more information, see the following articles:</span></span>

- [<span data-ttu-id="51e04-211">Konfiguration af komponenter i et job</span><span class="sxs-lookup"><span data-stu-id="51e04-211">Setting up the components of a job</span></span>](/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="51e04-212">Definere nye job</span><span class="sxs-lookup"><span data-stu-id="51e04-212">Define new jobs</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="51e04-213">Stillinger</span><span class="sxs-lookup"><span data-stu-id="51e04-213">Positions</span></span>

<span data-ttu-id="51e04-214">En stilling er en individuel forekomst af et job.</span><span class="sxs-lookup"><span data-stu-id="51e04-214">A position is an individual instance of a job.</span></span> <span data-ttu-id="51e04-215">For eksempel er stillingen "Salgschef (øst)" én af de stillinger, der er tilknyttet jobbet "Salgschef".</span><span class="sxs-lookup"><span data-stu-id="51e04-215">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="51e04-216">En stilling findes i en afdeling.</span><span class="sxs-lookup"><span data-stu-id="51e04-216">A position exists in a department.</span></span> <span data-ttu-id="51e04-217">Der kan kun knyttes én arbejder til hver stilling.</span><span class="sxs-lookup"><span data-stu-id="51e04-217">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="51e04-218">Hav følgende data og konfiguration i tankerne, når du konfigurerer stillinger:</span><span class="sxs-lookup"><span data-stu-id="51e04-218">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="51e04-219">Stilling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-219">Position (required)</span></span>
- <span data-ttu-id="51e04-220">Beskrivelse (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-220">Description (required)</span></span>
- <span data-ttu-id="51e04-221">Job (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-221">Job (required)</span></span>
- <span data-ttu-id="51e04-222">Afdeling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-222">Department (required)</span></span>
- <span data-ttu-id="51e04-223">Stillingstype (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-223">Position type (required)</span></span>
- <span data-ttu-id="51e04-224">Fuldtidsækvivalent</span><span class="sxs-lookup"><span data-stu-id="51e04-224">Full-time equivalent</span></span>
- <span data-ttu-id="51e04-225">Normaltimer på årsbasis (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-225">Annual regular hours (required)</span></span>
- <span data-ttu-id="51e04-226">Betalt af juridiske enhed (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-226">Paid by legal entity (required)</span></span>
- <span data-ttu-id="51e04-227">Betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-227">Pay cycle (required)</span></span>
- <span data-ttu-id="51e04-228">Økonomisk standarddimension – bærer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-228">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="51e04-229">Arbejdertildeling – arbejder, tildelingsstart, tildelingsslut, årsagskode</span><span class="sxs-lookup"><span data-stu-id="51e04-229">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="51e04-230">Hvis flere stillinger i den samme afdeling er knyttet til samme job, konsolideres de til en enkelt stilling i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="51e04-230">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="51e04-231">Du kan finde flere oplysninger i følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="51e04-231">For more information, see the following articles:</span></span>

- [<span data-ttu-id="51e04-232">Organisere dine medarbejdere ved hjælp af afdelinger, jobs og stillinger</span><span class="sxs-lookup"><span data-stu-id="51e04-232">Organize your workforce using departments, jobs, and positions</span></span>](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="51e04-233">Konfigurere stillinger</span><span class="sxs-lookup"><span data-stu-id="51e04-233">Set up positions</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="51e04-234">Afdelinger</span><span class="sxs-lookup"><span data-stu-id="51e04-234">Departments</span></span>

<span data-ttu-id="51e04-235">En afdeling er en driftsenhed, der repræsenterer en kategori eller et funktionsområde i en organisation.</span><span class="sxs-lookup"><span data-stu-id="51e04-235">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="51e04-236">En afdeling er ansvarlig for et bestemt område i organisationen, såsom salg, regnskab eller personale.</span><span class="sxs-lookup"><span data-stu-id="51e04-236">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="51e04-237">Du kan bruge afdelinger til at rapportere om funktionsområder.</span><span class="sxs-lookup"><span data-stu-id="51e04-237">You can use departments to report on functional areas.</span></span> <span data-ttu-id="51e04-238">Afdelinger kan have ansvar for driftsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="51e04-238">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="51e04-239">Du kan finde flere oplysninger i følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="51e04-239">For more information, see the following articles:</span></span>

- [<span data-ttu-id="51e04-240">Oprette en afdeling og knytte den til afdelingshierarkiet</span><span class="sxs-lookup"><span data-stu-id="51e04-240">Create a department and associate it with the department hierarchy</span></span>](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="51e04-241">Definere nye afdelinger</span><span class="sxs-lookup"><span data-stu-id="51e04-241">Define new departments</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="51e04-242">Betalingscyklusser og lønperioder</span><span class="sxs-lookup"><span data-stu-id="51e04-242">Pay cycles and pay periods</span></span>

<span data-ttu-id="51e04-243">En betalingscyklus bestemmer, hvor ofte løn køres,og de specifikke dage, hvor arbejdere betales.</span><span class="sxs-lookup"><span data-stu-id="51e04-243">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="51e04-244">En løncyklus kan f.eks. være månedlig, og medarbejdere betales måske på den sidste dag i måneden.</span><span class="sxs-lookup"><span data-stu-id="51e04-244">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="51e04-245">En løncyklus kan også være ugentligt, og medarbejdere betales måske tirsdag efter slutningen af lønperioden.</span><span class="sxs-lookup"><span data-stu-id="51e04-245">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="51e04-246">Løncyklusser tildeles til stillinger for at styre, hvornår arbejdere i disse stillinger bliver betalt.</span><span class="sxs-lookup"><span data-stu-id="51e04-246">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="51e04-247">Når du opretter betalingscyklusser, kan du generere lønperioder for hver cyklus.</span><span class="sxs-lookup"><span data-stu-id="51e04-247">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="51e04-248">Hver lønperiode omfatter en standardbetalingsdato, der er baseret på oplysninger, du angiver.</span><span class="sxs-lookup"><span data-stu-id="51e04-248">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="51e04-249">Du kan dog redigere standardbetalingsdatoen i en lønperiode til at tillade undtagelser, f.eks. når betalingsdatoen falder på en helligdag.</span><span class="sxs-lookup"><span data-stu-id="51e04-249">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="51e04-250">Følgende oplysninger bruges i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="51e04-250">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="51e04-251">Betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-251">Pay cycle (required)</span></span>
- <span data-ttu-id="51e04-252">Hyppighed for betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-252">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="51e04-253">Periodens startdato (første lønperiode påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-253">Period start date (first pay period required)</span></span>
- <span data-ttu-id="51e04-254">Standardbetalingsdato (første lønperiode påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-254">Default payment date (first pay period required)</span></span>

<span data-ttu-id="51e04-255">Oplysningerne er integreret med Dayforce som løngrupper og adskilles af et land eller område for hver løncyklus.</span><span class="sxs-lookup"><span data-stu-id="51e04-255">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="51e04-256">Mindst én periode skal genereres før integration.</span><span class="sxs-lookup"><span data-stu-id="51e04-256">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="51e04-257">Dayforce genererer løngruppekalendere og betalingsdatoer, der er baseret på startdatoen for den første lønperiode og den standardbetalingsdato, der er angivet i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="51e04-257">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="51e04-258">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="51e04-258">Earning codes</span></span>

<span data-ttu-id="51e04-259">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="51e04-259">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="51e04-260">Koderne har forskellige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="51e04-260">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="51e04-261">Følgende oplysninger bruges i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="51e04-261">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="51e04-262">Lønkode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-262">Earning Code (required)</span></span>
- <span data-ttu-id="51e04-263">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="51e04-263">Description</span></span>
- <span data-ttu-id="51e04-264">Måleenhed</span><span class="sxs-lookup"><span data-stu-id="51e04-264">Unit of measure</span></span>
- <span data-ttu-id="51e04-265">Produktiv</span><span class="sxs-lookup"><span data-stu-id="51e04-265">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="51e04-266">Arbejderdata</span><span class="sxs-lookup"><span data-stu-id="51e04-266">Worker data</span></span>

<span data-ttu-id="51e04-267">Posterne for de forskellige typer arbejdere, du beskæftiger, er vigtige for dine personale- og lønsystemer.</span><span class="sxs-lookup"><span data-stu-id="51e04-267">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="51e04-268">De oplysninger, du angiver, kan bruges til at spore arbejdere og personoplysninger.</span><span class="sxs-lookup"><span data-stu-id="51e04-268">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="51e04-269">Du kan vedligeholde følgende oplysninger for arbejdere:</span><span class="sxs-lookup"><span data-stu-id="51e04-269">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="51e04-270">**Basis** – Vedligehold grundlæggende oplysninger om en arbejder, f.eks. kontaktoplysninger, demografiske oplysninger, identifikationsoplysninger, oplysninger om familie, status for militærtjeneste, oplysninger om udstationering og personlige kontaktpersoner og kontaktpersoner i nødsituationer.</span><span class="sxs-lookup"><span data-stu-id="51e04-270">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="51e04-271">**Beskæftigelse** – Vedligehold oplysninger om en arbejders beskæftigelse, f.eks. firma- eller organisationstilhørsforhold, stillingstildeling, start- og slutdatoer, arbejdstilladelse, vilkår for ansættelse, pension, ferie og flytteoplysninger.</span><span class="sxs-lookup"><span data-stu-id="51e04-271">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="51e04-272">**Orlov og fravær** – Vedligehold oplysninger om en arbejders fravær, f.eks. arbejdskalendere, fraværstransaktioner og fraværsopsætning.</span><span class="sxs-lookup"><span data-stu-id="51e04-272">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="51e04-273">**Kompensation og løn** – Vedligehold oplysninger om en arbejders kompensationsplaner og lønoplysninger, f.eks. tilmelding til planer, priser, ydeevne, provision, skatteoplysninger, pensionering og skattefradrag.</span><span class="sxs-lookup"><span data-stu-id="51e04-273">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="51e04-274">Når du angiver arbejderoplysninger, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="51e04-274">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="51e04-275">Generelle oplysninger</span><span class="sxs-lookup"><span data-stu-id="51e04-275">General information</span></span>

- <span data-ttu-id="51e04-276">Personalenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-276">Personnel number (required)</span></span>
- <span data-ttu-id="51e04-277">Fornavn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-277">First name (required)</span></span>
- <span data-ttu-id="51e04-278">Efternavn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-278">Last name (required)</span></span>
- <span data-ttu-id="51e04-279">Mellemnavn</span><span class="sxs-lookup"><span data-stu-id="51e04-279">Middle name</span></span>
- <span data-ttu-id="51e04-280">Anciennitetsdato</span><span class="sxs-lookup"><span data-stu-id="51e04-280">Seniority date</span></span>
- <span data-ttu-id="51e04-281">Kendt som</span><span class="sxs-lookup"><span data-stu-id="51e04-281">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="51e04-282">Personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="51e04-282">Personal information</span></span>

- <span data-ttu-id="51e04-283">Ægteskabelig status (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-283">Marital status (required)</span></span>
- <span data-ttu-id="51e04-284">Fødselsdato (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-284">Birth date (required)</span></span>
- <span data-ttu-id="51e04-285">Køn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-285">Gender (required)</span></span>
- <span data-ttu-id="51e04-286">Handicappet</span><span class="sxs-lookup"><span data-stu-id="51e04-286">Person with disabilities</span></span>
- <span data-ttu-id="51e04-287">Land eller område for nationalitet (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="51e04-287">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="51e04-288">Adresseoplysninger</span><span class="sxs-lookup"><span data-stu-id="51e04-288">Address information</span></span>

- <span data-ttu-id="51e04-289">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-289">Primary (required)</span></span>
- <span data-ttu-id="51e04-290">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-290">Country/region (required)</span></span>
- <span data-ttu-id="51e04-291">Postnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-291">Postal code (required)</span></span>
- <span data-ttu-id="51e04-292">Gadenummer (påkrævet) (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="51e04-292">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="51e04-293">Bygningskomplement (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="51e04-293">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="51e04-294">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-294">City (required)</span></span>
- <span data-ttu-id="51e04-295">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-295">State (required)</span></span>
- <span data-ttu-id="51e04-296">Region (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-296">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="51e04-297">Kontaktoplysninger</span><span class="sxs-lookup"><span data-stu-id="51e04-297">Contact information</span></span> 

- <span data-ttu-id="51e04-298">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-298">Primary (required)</span></span>
- <span data-ttu-id="51e04-299">Kontaktpersonens nummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-299">Contact number (required)</span></span>
- <span data-ttu-id="51e04-300">Forlængelse</span><span class="sxs-lookup"><span data-stu-id="51e04-300">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="51e04-301">Lønoplysninger og lønkoder</span><span class="sxs-lookup"><span data-stu-id="51e04-301">Payroll information and earning codes</span></span>

<span data-ttu-id="51e04-302">Medarbejdere kan tildeles en bestemt løn med en given betalingshyppighed og have en foretrukken betalingsmetode.</span><span class="sxs-lookup"><span data-stu-id="51e04-302">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="51e04-303">Følgende felter bruges i Dayforce til at sikre, at disse præferencer og indstillinger bruges.</span><span class="sxs-lookup"><span data-stu-id="51e04-303">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="51e04-304">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="51e04-304">Earning codes</span></span>

- <span data-ttu-id="51e04-305">Stilling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-305">Position (required)</span></span>
- <span data-ttu-id="51e04-306">Lønkode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-306">Earning Code (required)</span></span>
- <span data-ttu-id="51e04-307">Frekvens (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-307">Frequency (required)</span></span>
- <span data-ttu-id="51e04-308">Beløb (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-308">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="51e04-309">Lønoplysninger</span><span class="sxs-lookup"><span data-stu-id="51e04-309">Payroll information</span></span>

- <span data-ttu-id="51e04-310">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="51e04-310">Payment Method</span></span>
- <span data-ttu-id="51e04-311">Økonomisk område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-311">Economic Region (required)</span></span>
- <span data-ttu-id="51e04-312">Id for medarbejderfrynsegoder</span><span class="sxs-lookup"><span data-stu-id="51e04-312">Employee Benefits ID</span></span>
- <span data-ttu-id="51e04-313">Nationalt id-nummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-313">National ID Number (required)</span></span>
- <span data-ttu-id="51e04-314">Tjenestenummer hos militær</span><span class="sxs-lookup"><span data-stu-id="51e04-314">Military Service Number</span></span>
- <span data-ttu-id="51e04-315">Skifte-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-315">Shift ID (required)</span></span>
- <span data-ttu-id="51e04-316">Skattenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-316">Tax Number (required)</span></span>
- <span data-ttu-id="51e04-317">Fagforenings-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-317">Union ID (required)</span></span>
- <span data-ttu-id="51e04-318">Arbejdsdags-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-318">Work Day ID (required)</span></span>
- <span data-ttu-id="51e04-319">Arbejdstilladelsesnummer</span><span class="sxs-lookup"><span data-stu-id="51e04-319">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="51e04-320">For betalingsmetoden understøtter Mexico **Kontant**, **Check** (firmaets fysiske check), og **Elektronisk betaling**.</span><span class="sxs-lookup"><span data-stu-id="51e04-320">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="51e04-321">Hvis der ikke er angivet nogen betalingsmetode, bruges **Check** som standard.</span><span class="sxs-lookup"><span data-stu-id="51e04-321">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="51e04-322">Detaljer om ansættelse</span><span class="sxs-lookup"><span data-stu-id="51e04-322">Employment details</span></span>

<span data-ttu-id="51e04-323">Detaljeret ansættelseshistorik bruges som vigtige oplysninger til at udlede statusser for en medarbejders ansættelse, fratrædelse og genansættelse i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="51e04-323">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="51e04-324">Dayforce understøtter kun én aktiv ansættelsespost ad gangen.</span><span class="sxs-lookup"><span data-stu-id="51e04-324">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="51e04-325">Startdato for ansættelse (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-325">Employment start date (required)</span></span>
- <span data-ttu-id="51e04-326">Slutdato for ansættelse</span><span class="sxs-lookup"><span data-stu-id="51e04-326">Employment end date</span></span>
- <span data-ttu-id="51e04-327">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="51e04-327">Start date</span></span>
- <span data-ttu-id="51e04-328">Justeret startdato</span><span class="sxs-lookup"><span data-stu-id="51e04-328">Adjusted start date</span></span>
- <span data-ttu-id="51e04-329">Fratrædelsesdato (kræves ved fratrædelse)</span><span class="sxs-lookup"><span data-stu-id="51e04-329">Termination date (required upon termination)</span></span>
- <span data-ttu-id="51e04-330">Fratrædelsesårsag (kræves ved fratrædelse)</span><span class="sxs-lookup"><span data-stu-id="51e04-330">Termination reason (required upon termination)</span></span>

<span data-ttu-id="51e04-331">Vigtige datoer for en medarbejders udledes ved hjælp af følgende oplysninger.</span><span class="sxs-lookup"><span data-stu-id="51e04-331">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="51e04-332">Human Resources</span><span class="sxs-lookup"><span data-stu-id="51e04-332">Human Resources</span></span>                | <span data-ttu-id="51e04-333">Dayforce</span><span class="sxs-lookup"><span data-stu-id="51e04-333">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51e04-334">Den seneste ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="51e04-334">Most recent hire date</span></span> | <span data-ttu-id="51e04-335">Historikpost for ansættelsesstart for aktuel ikke-afsluttet ansættelse</span><span class="sxs-lookup"><span data-stu-id="51e04-335">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="51e04-336">Fratrædelsesdato</span><span class="sxs-lookup"><span data-stu-id="51e04-336">Termination date</span></span>      | <span data-ttu-id="51e04-337">Historikpost for fratrædelsesdato for aktuel ikke-afsluttet ansættelse</span><span class="sxs-lookup"><span data-stu-id="51e04-337">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="51e04-338">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="51e04-338">Start date</span></span>            | <span data-ttu-id="51e04-339">Historikpost for justeret startdato, startdato eller startdato for ansættelse for aktuel ikke-aktiv ansættelse</span><span class="sxs-lookup"><span data-stu-id="51e04-339">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="51e04-340">Oprindelig ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="51e04-340">Original hire date</span></span>    | <span data-ttu-id="51e04-341">Historikpost for ansættelsesstart for tidligste ansættelse</span><span class="sxs-lookup"><span data-stu-id="51e04-341">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="51e04-342">Kompensation</span><span class="sxs-lookup"><span data-stu-id="51e04-342">Compensation</span></span>

<span data-ttu-id="51e04-343">En fast lønstruktur skal tilknyttes hver medarbejders primære stilling gennem hele ansættelsesperioden.</span><span class="sxs-lookup"><span data-stu-id="51e04-343">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="51e04-344">Denne periode starter på den dato, hvor medarbejderen blev ansat (eller ansættelsesstartdatoen) og fortsætter, indtil fratrædelsen.</span><span class="sxs-lookup"><span data-stu-id="51e04-344">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="51e04-345">Ikrafttrædelsesdato (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-345">Effective Date (required)</span></span>
- <span data-ttu-id="51e04-346">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="51e04-346">Expiration date</span></span>
- <span data-ttu-id="51e04-347">Lønsats (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-347">Pay Rate (required)</span></span>
- <span data-ttu-id="51e04-348">Konverteringer af lønsats (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-348">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="51e04-349">Årlig ækvivalent (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-349">Annual equivalent (required)</span></span>
- <span data-ttu-id="51e04-350">Timebaseret ækvivalent (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-350">Hourly equivalent (required)</span></span>

<span data-ttu-id="51e04-351">Hvis en timeansat medarbejder har flere stillinger, indlæses den faste løn for den primære stilling i Dayforce, som basissats/-løn på medarbejderniveau.</span><span class="sxs-lookup"><span data-stu-id="51e04-351">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="51e04-352">For ikke-primære stillinger gemmes timesatsen i den tilsvarende position i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="51e04-352">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="51e04-353">Hvis en funktionær har flere stillinger, afledes den kumulative timesats og årlig gage på tværs af alle aktive stillinger og bruges som basissats/-gage på medarbejderniveau.</span><span class="sxs-lookup"><span data-stu-id="51e04-353">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="51e04-354">Identifikationsnumre</span><span class="sxs-lookup"><span data-stu-id="51e04-354">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="51e04-355">Social Security-identifikator</span><span class="sxs-lookup"><span data-stu-id="51e04-355">Social Security identifier</span></span> 

<span data-ttu-id="51e04-356">Alle medarbejdere skal have én primær identifikator.</span><span class="sxs-lookup"><span data-stu-id="51e04-356">Every employee must have one primary identifier.</span></span> <span data-ttu-id="51e04-357">Identifikatoren skal være af **SSN**-identifikationstypen</span><span class="sxs-lookup"><span data-stu-id="51e04-357">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="51e04-358">I Dayforce afledes den automatisk som medarbejderens Social Security-identifikator, der er påkrævet ved ansættelse.</span><span class="sxs-lookup"><span data-stu-id="51e04-358">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="51e04-359">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-359">Primary (required)</span></span>
- <span data-ttu-id="51e04-360">Identifikationstype = "SSN"</span><span class="sxs-lookup"><span data-stu-id="51e04-360">Identification Type = "SSN"</span></span>
- <span data-ttu-id="51e04-361">Udstedt den</span><span class="sxs-lookup"><span data-stu-id="51e04-361">Issued Date</span></span>
- <span data-ttu-id="51e04-362">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="51e04-362">Expiration Date</span></span>

<span data-ttu-id="51e04-363">Medarbejdere kan angive flere identifikationsnumre af **SSN**-identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="51e04-363">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="51e04-364">Men det er kun den post, der er markeret som **Primær**, som er integreret i Dayforce, uanset om nummeret er aktivt eller udløbet.</span><span class="sxs-lookup"><span data-stu-id="51e04-364">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="51e04-365">Bankkonto og udbetalinger</span><span class="sxs-lookup"><span data-stu-id="51e04-365">Bank accounts and disbursements</span></span>

<span data-ttu-id="51e04-366">Gyldige bankkontooplysninger skal angives for enhver medarbejder, der vælger at blive betalt via bankkontooverførsler.</span><span class="sxs-lookup"><span data-stu-id="51e04-366">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="51e04-367">Human Resources</span><span class="sxs-lookup"><span data-stu-id="51e04-367">Human Resources</span></span>                         | <span data-ttu-id="51e04-368">Dayforce</span><span class="sxs-lookup"><span data-stu-id="51e04-368">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51e04-369">Bankkontonummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-369">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="51e04-370">SWIFT-kode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-370">SWIFT code (required)</span></span>          | <span data-ttu-id="51e04-371">Feltet **Bank-id** bruges ved behandling af løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="51e04-371">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="51e04-372">Afdelingsnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-372">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="51e04-373">Bankkontotype (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-373">Bank account type (required)</span></span>   | <span data-ttu-id="51e04-374">Feltet **Kontotype** bruges ved behandling af løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="51e04-374">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="51e04-375">Understøttede værdier omfatter **Check** og **Løn**.</span><span class="sxs-lookup"><span data-stu-id="51e04-375">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="51e04-376">Medarbejdere, der vælger at betales via bankkontooverførsler, skal angive et link til en restbeløbskonto, der hører under en juridisk enhed, som har primær adresse i Mexico og er knyttet til en gyldig bankkonto fra en mexicansk bank.</span><span class="sxs-lookup"><span data-stu-id="51e04-376">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="51e04-377">Alle andre restbeløbskonti ignoreres.</span><span class="sxs-lookup"><span data-stu-id="51e04-377">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="51e04-378">Adresseoplysninger</span><span class="sxs-lookup"><span data-stu-id="51e04-378">Address information</span></span>

<span data-ttu-id="51e04-379">Alle medarbejdere skal have én primær placering.</span><span class="sxs-lookup"><span data-stu-id="51e04-379">Every employee must have one primary location.</span></span> <span data-ttu-id="51e04-380">I Dayforce bruges denne placering til at bestemme medarbejderens primære opholdssted til skattemæssige formål.</span><span class="sxs-lookup"><span data-stu-id="51e04-380">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="51e04-381">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-381">Primary (required)</span></span>
- <span data-ttu-id="51e04-382">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-382">Country/region (required)</span></span>
- <span data-ttu-id="51e04-383">Postnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-383">Zip/postal code (required)</span></span>
- <span data-ttu-id="51e04-384">Gade (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-384">Street (required)</span></span>
- <span data-ttu-id="51e04-385">Gadenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-385">Street Number (required)</span></span>
- <span data-ttu-id="51e04-386">Bygningskomplement</span><span class="sxs-lookup"><span data-stu-id="51e04-386">Building Complement</span></span>
- <span data-ttu-id="51e04-387">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-387">City (required)</span></span>
- <span data-ttu-id="51e04-388">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-388">State (required)</span></span>
- <span data-ttu-id="51e04-389">Region (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-389">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="51e04-390">Konfigurere dataene for at generere løn i USA og Canada</span><span class="sxs-lookup"><span data-stu-id="51e04-390">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="51e04-391">Hvis du genererer løn for medarbejdere i USA og Canada, skal følgende elementer konfigureres:</span><span class="sxs-lookup"><span data-stu-id="51e04-391">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="51e04-392">Der kræves afdelinger til stillinger.</span><span class="sxs-lookup"><span data-stu-id="51e04-392">Departments are required on positions.</span></span>
- <span data-ttu-id="51e04-393">Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="51e04-393">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="51e04-394">Du kan konfigurere Human Resources til at kræve, at der angives en afdeling for stillinger.</span><span class="sxs-lookup"><span data-stu-id="51e04-394">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="51e04-395">For at gøre dette skal du gå til **Human Resourcests delte stillinger > Stillinger > Kræv afdelinger for stillinger**.</span><span class="sxs-lookup"><span data-stu-id="51e04-395">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="51e04-396">Det anbefales, at denne indstilling gennemtvinges i forbindelse med integrationen.</span><span class="sxs-lookup"><span data-stu-id="51e04-396">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="51e04-397">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="51e04-397">Job types</span></span>

<span data-ttu-id="51e04-398">Jobtyper bruges til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="51e04-398">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="51e04-399">Jobtyper kræves for at behandle løn i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="51e04-399">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="51e04-400">Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="51e04-400">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="51e04-401">Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.</span><span class="sxs-lookup"><span data-stu-id="51e04-401">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="51e04-402">Der kræves følgende jobtyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="51e04-402">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="51e04-403">Jobtype</span><span class="sxs-lookup"><span data-stu-id="51e04-403">Job type</span></span>   | <span data-ttu-id="51e04-404">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="51e04-404">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="51e04-405">Pr. time</span><span class="sxs-lookup"><span data-stu-id="51e04-405">Hourly</span></span>     | <span data-ttu-id="51e04-406">Pr. time</span><span class="sxs-lookup"><span data-stu-id="51e04-406">Hourly</span></span>      |
| <span data-ttu-id="51e04-407">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="51e04-407">Salaried</span></span>   | <span data-ttu-id="51e04-408">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="51e04-408">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="51e04-409">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="51e04-409">Position types</span></span> 

<span data-ttu-id="51e04-410">Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet.</span><span class="sxs-lookup"><span data-stu-id="51e04-410">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="51e04-411">Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="51e04-411">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="51e04-412">Der kræves følgende stillingstyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="51e04-412">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="51e04-413">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="51e04-413">Position type</span></span>   | <span data-ttu-id="51e04-414">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="51e04-414">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="51e04-415">Fuld tid</span><span class="sxs-lookup"><span data-stu-id="51e04-415">Full-time</span></span>       | <span data-ttu-id="51e04-416">Fuldtidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="51e04-416">Full time employee</span></span> |
| <span data-ttu-id="51e04-417">Deltid</span><span class="sxs-lookup"><span data-stu-id="51e04-417">Part-time</span></span>       | <span data-ttu-id="51e04-418">Deltidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="51e04-418">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="51e04-419">Årsagskoder</span><span class="sxs-lookup"><span data-stu-id="51e04-419">Reason codes</span></span>

<span data-ttu-id="51e04-420">Årsagskoder indeholder oplysninger om status for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="51e04-420">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="51e04-421">Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.</span><span class="sxs-lookup"><span data-stu-id="51e04-421">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="51e04-422">Der kræves følgende årsagskoder og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="51e04-422">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="51e04-423">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="51e04-423">Reason code</span></span>    | <span data-ttu-id="51e04-424">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="51e04-424">Description</span></span>      | <span data-ttu-id="51e04-425">Anvendelige scenarier</span><span class="sxs-lookup"><span data-stu-id="51e04-425">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="51e04-426">OPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="51e04-426">RESIGNATION</span></span>    | <span data-ttu-id="51e04-427">Opsigelse</span><span class="sxs-lookup"><span data-stu-id="51e04-427">Resignation</span></span>      | <span data-ttu-id="51e04-428">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="51e04-428">Terminate worker</span></span>     |
| <span data-ttu-id="51e04-429">OPHØR</span><span class="sxs-lookup"><span data-stu-id="51e04-429">TERMINATION</span></span>    | <span data-ttu-id="51e04-430">Ophør</span><span class="sxs-lookup"><span data-stu-id="51e04-430">Termination</span></span>      | <span data-ttu-id="51e04-431">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="51e04-431">Terminate worker</span></span>     |
| <span data-ttu-id="51e04-432">PENSION</span><span class="sxs-lookup"><span data-stu-id="51e04-432">RETIREMENT</span></span>     | <span data-ttu-id="51e04-433">Pension</span><span class="sxs-lookup"><span data-stu-id="51e04-433">Retirement</span></span>       | <span data-ttu-id="51e04-434">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="51e04-434">Terminate worker</span></span>     |
| <span data-ttu-id="51e04-435">ANDET</span><span class="sxs-lookup"><span data-stu-id="51e04-435">OTHER</span></span>          | <span data-ttu-id="51e04-436">Andre årsager</span><span class="sxs-lookup"><span data-stu-id="51e04-436">Other Reasons</span></span>    | <span data-ttu-id="51e04-437">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="51e04-437">Terminate worker</span></span>     |
| <span data-ttu-id="51e04-438">DØDSFALD</span><span class="sxs-lookup"><span data-stu-id="51e04-438">DEATH</span></span>          | <span data-ttu-id="51e04-439">Dødsfald</span><span class="sxs-lookup"><span data-stu-id="51e04-439">Death</span></span>            | <span data-ttu-id="51e04-440">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="51e04-440">Terminate worker</span></span>     |
| <span data-ttu-id="51e04-441">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="51e04-441">LEAVEOFABSENCE</span></span> | <span data-ttu-id="51e04-442">Orlov</span><span class="sxs-lookup"><span data-stu-id="51e04-442">Leave of Absence</span></span> | <span data-ttu-id="51e04-443">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="51e04-443">Terminate worker</span></span>     |
| <span data-ttu-id="51e04-444">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="51e04-444">CONTRACTEND</span></span>    | <span data-ttu-id="51e04-445">Kontraktudløb</span><span class="sxs-lookup"><span data-stu-id="51e04-445">End of Contract</span></span>  | <span data-ttu-id="51e04-446">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="51e04-446">Terminate worker</span></span>     |
| <span data-ttu-id="51e04-447">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="51e04-447">SALARYCHANGE</span></span>   | <span data-ttu-id="51e04-448">Ændring af løn</span><span class="sxs-lookup"><span data-stu-id="51e04-448">Change of Salary</span></span> | <span data-ttu-id="51e04-449">Kompensation</span><span class="sxs-lookup"><span data-stu-id="51e04-449">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="51e04-450">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="51e04-450">Marital status</span></span>

<span data-ttu-id="51e04-451">Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="51e04-451">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="51e04-452">Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="51e04-452">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="51e04-453">Human Resources</span><span class="sxs-lookup"><span data-stu-id="51e04-453">Human Resources</span></span>                 | <span data-ttu-id="51e04-454">Dayforce</span><span class="sxs-lookup"><span data-stu-id="51e04-454">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="51e04-455">Gift</span><span class="sxs-lookup"><span data-stu-id="51e04-455">Married</span></span>                | <span data-ttu-id="51e04-456">Gift</span><span class="sxs-lookup"><span data-stu-id="51e04-456">Married</span></span>              |
| <span data-ttu-id="51e04-457">Enlig</span><span class="sxs-lookup"><span data-stu-id="51e04-457">Single</span></span>                 | <span data-ttu-id="51e04-458">Enlig</span><span class="sxs-lookup"><span data-stu-id="51e04-458">Single</span></span>               |
| <span data-ttu-id="51e04-459">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="51e04-459">Widowed</span></span>                | <span data-ttu-id="51e04-460">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="51e04-460">Widowed</span></span>              |
| <span data-ttu-id="51e04-461">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="51e04-461">Divorced</span></span>               | <span data-ttu-id="51e04-462">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="51e04-462">Divorced</span></span>             |
| <span data-ttu-id="51e04-463">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="51e04-463">Registered Partnership</span></span> | <span data-ttu-id="51e04-464">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="51e04-464">Domestic Partnership</span></span> |
| <span data-ttu-id="51e04-465">None</span><span class="sxs-lookup"><span data-stu-id="51e04-465">None</span></span>                   | <span data-ttu-id="51e04-466">None</span><span class="sxs-lookup"><span data-stu-id="51e04-466">None</span></span>                 |
| <span data-ttu-id="51e04-467">Samlever</span><span class="sxs-lookup"><span data-stu-id="51e04-467">Cohabiting</span></span>             | <span data-ttu-id="51e04-468">Samlever</span><span class="sxs-lookup"><span data-stu-id="51e04-468">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="51e04-469">Køn</span><span class="sxs-lookup"><span data-stu-id="51e04-469">Gender</span></span>

<span data-ttu-id="51e04-470">Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="51e04-470">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="51e04-471">Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="51e04-471">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="51e04-472">Human Resources</span><span class="sxs-lookup"><span data-stu-id="51e04-472">Human Resources</span></span>       | <span data-ttu-id="51e04-473">Dayforce</span><span class="sxs-lookup"><span data-stu-id="51e04-473">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="51e04-474">Mand</span><span class="sxs-lookup"><span data-stu-id="51e04-474">Male</span></span>         | <span data-ttu-id="51e04-475">Mand</span><span class="sxs-lookup"><span data-stu-id="51e04-475">Male</span></span>            |
| <span data-ttu-id="51e04-476">Kvinde</span><span class="sxs-lookup"><span data-stu-id="51e04-476">Female</span></span>       | <span data-ttu-id="51e04-477">Kvinde</span><span class="sxs-lookup"><span data-stu-id="51e04-477">Female</span></span>          |
| <span data-ttu-id="51e04-478">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="51e04-478">Non-specific</span></span> | <span data-ttu-id="51e04-479">*Understøttes ikke*</span><span class="sxs-lookup"><span data-stu-id="51e04-479">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="51e04-480">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="51e04-480">Earning codes</span></span>

<span data-ttu-id="51e04-481">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="51e04-481">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="51e04-482">Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="51e04-482">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="51e04-483">Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="51e04-483">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="51e04-484">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="51e04-484">Supported frequencies</span></span>

- <span data-ttu-id="51e04-485">Alt</span><span class="sxs-lookup"><span data-stu-id="51e04-485">All</span></span>
- <span data-ttu-id="51e04-486">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="51e04-486">EVERYPAY</span></span>
- <span data-ttu-id="51e04-487">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="51e04-487">EACHPAYPERIOD</span></span>
- <span data-ttu-id="51e04-488">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="51e04-488">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="51e04-489">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="51e04-489">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="51e04-490">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-490">1OFMTH</span></span>
- <span data-ttu-id="51e04-491">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-491">LASTOFMTH</span></span>
- <span data-ttu-id="51e04-492">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-492">2OFMTH</span></span>
- <span data-ttu-id="51e04-493">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-493">3OFMTH</span></span>
- <span data-ttu-id="51e04-494">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-494">4OFMTH</span></span>
- <span data-ttu-id="51e04-495">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-495">5OFMTH</span></span>
- <span data-ttu-id="51e04-496">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-496">1N2OFMTH</span></span>
- <span data-ttu-id="51e04-497">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-497">3N4OFMTH</span></span>
- <span data-ttu-id="51e04-498">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-498">1N3OFMTH</span></span>
- <span data-ttu-id="51e04-499">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-499">1N4OFMTH</span></span>
- <span data-ttu-id="51e04-500">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-500">2N3OFMTH</span></span>
- <span data-ttu-id="51e04-501">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-501">2N4OFMTH</span></span>
- <span data-ttu-id="51e04-502">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-502">1N2N3OFMTH</span></span>
- <span data-ttu-id="51e04-503">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-503">1N2N4OFMTH</span></span>
- <span data-ttu-id="51e04-504">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-504">1N3N4OFMTH</span></span>
- <span data-ttu-id="51e04-505">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-505">2N3N4OFMTH</span></span>
- <span data-ttu-id="51e04-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="51e04-507">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="51e04-507">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="51e04-508">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="51e04-508">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="51e04-509">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="51e04-509">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="51e04-510">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="51e04-510">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="51e04-511">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="51e04-511">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="51e04-512">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="51e04-512">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="51e04-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="51e04-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="51e04-514">Adresser</span><span class="sxs-lookup"><span data-stu-id="51e04-514">Addresses</span></span>

<span data-ttu-id="51e04-515">Identifikation af specifikke koder for land eller område, stat og region (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende.</span><span class="sxs-lookup"><span data-stu-id="51e04-515">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="51e04-516">Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.</span><span class="sxs-lookup"><span data-stu-id="51e04-516">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="51e04-517">Human Resources</span><span class="sxs-lookup"><span data-stu-id="51e04-517">Human Resources</span></span>          | <span data-ttu-id="51e04-518">Dayforce</span><span class="sxs-lookup"><span data-stu-id="51e04-518">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="51e04-519">Land/område</span><span class="sxs-lookup"><span data-stu-id="51e04-519">Country/Region</span></span>  | <span data-ttu-id="51e04-520">Landekode</span><span class="sxs-lookup"><span data-stu-id="51e04-520">Country Code</span></span>          |
| <span data-ttu-id="51e04-521">Postnummer</span><span class="sxs-lookup"><span data-stu-id="51e04-521">Zip/Postal Code</span></span> | <span data-ttu-id="51e04-522">Postnummer</span><span class="sxs-lookup"><span data-stu-id="51e04-522">Postal Code</span></span>           |
| <span data-ttu-id="51e04-523">Status</span><span class="sxs-lookup"><span data-stu-id="51e04-523">State</span></span>           | <span data-ttu-id="51e04-524">Statskode</span><span class="sxs-lookup"><span data-stu-id="51e04-524">State Code</span></span>            |
| <span data-ttu-id="51e04-525">Bynavn</span><span class="sxs-lookup"><span data-stu-id="51e04-525">City</span></span>            | <span data-ttu-id="51e04-526">Bynavn</span><span class="sxs-lookup"><span data-stu-id="51e04-526">City</span></span>                  |
| <span data-ttu-id="51e04-527">Region</span><span class="sxs-lookup"><span data-stu-id="51e04-527">County</span></span>          | <span data-ttu-id="51e04-528">Område (kommune)</span><span class="sxs-lookup"><span data-stu-id="51e04-528">County (Municipality)</span></span> |
| <span data-ttu-id="51e04-529">Gade</span><span class="sxs-lookup"><span data-stu-id="51e04-529">Street</span></span>          | <span data-ttu-id="51e04-530">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="51e04-530">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="51e04-531">Skatteområder</span><span class="sxs-lookup"><span data-stu-id="51e04-531">Tax regions</span></span>

<span data-ttu-id="51e04-532">Skatteområder bruges til at bestemme den relevante skat, der skal anvendes ved løngenerering.</span><span class="sxs-lookup"><span data-stu-id="51e04-532">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="51e04-533">Skatteområder er tilknyttet Dayforce som placeringsadresser.</span><span class="sxs-lookup"><span data-stu-id="51e04-533">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="51e04-534">Standardskatteområder skal knyttes til arbejderens aktive stilling.</span><span class="sxs-lookup"><span data-stu-id="51e04-534">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="51e04-535">Skatteområde (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-535">Tax region (required)</span></span>
- <span data-ttu-id="51e04-536">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-536">Country/Region (required)</span></span>
- <span data-ttu-id="51e04-537">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-537">State (required)</span></span>
- <span data-ttu-id="51e04-538">Region</span><span class="sxs-lookup"><span data-stu-id="51e04-538">County</span></span> 
- <span data-ttu-id="51e04-539">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="51e04-539">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="51e04-540">Konfigurere dataene for at generere løn i Mexico</span><span class="sxs-lookup"><span data-stu-id="51e04-540">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="51e04-541">Hvis du genererer løn for medarbejdere i Mexico skal følgende elementer konfigureres:</span><span class="sxs-lookup"><span data-stu-id="51e04-541">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="51e04-542">Der kræves afdelinger til stillinger.</span><span class="sxs-lookup"><span data-stu-id="51e04-542">Departments are required on positions.</span></span>
- <span data-ttu-id="51e04-543">Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="51e04-543">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="51e04-544">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="51e04-544">Job types</span></span>

<span data-ttu-id="51e04-545">Jobtyper bruges til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="51e04-545">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="51e04-546">Jobtyper kræves for at behandle løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="51e04-546">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="51e04-547">Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="51e04-547">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="51e04-548">Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.</span><span class="sxs-lookup"><span data-stu-id="51e04-548">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="51e04-549">Der kræves følgende jobtyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="51e04-549">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="51e04-550">Jobtype</span><span class="sxs-lookup"><span data-stu-id="51e04-550">Job type</span></span>   | <span data-ttu-id="51e04-551">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="51e04-551">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="51e04-552">Pr. time</span><span class="sxs-lookup"><span data-stu-id="51e04-552">Hourly</span></span>     | <span data-ttu-id="51e04-553">MX Pr. time</span><span class="sxs-lookup"><span data-stu-id="51e04-553">MX Hourly</span></span>   |
| <span data-ttu-id="51e04-554">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="51e04-554">Salaried</span></span>   | <span data-ttu-id="51e04-555">MX Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="51e04-555">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="51e04-556">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="51e04-556">Position types</span></span> 

<span data-ttu-id="51e04-557">Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet.</span><span class="sxs-lookup"><span data-stu-id="51e04-557">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="51e04-558">Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="51e04-558">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="51e04-559">Der kræves følgende stillingstyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="51e04-559">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="51e04-560">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="51e04-560">Position type</span></span>   | <span data-ttu-id="51e04-561">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="51e04-561">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="51e04-562">Fuld tid</span><span class="sxs-lookup"><span data-stu-id="51e04-562">Full-time</span></span>       | <span data-ttu-id="51e04-563">Fuldtidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="51e04-563">Full time employee</span></span> |
| <span data-ttu-id="51e04-564">Deltid</span><span class="sxs-lookup"><span data-stu-id="51e04-564">Part-time</span></span>       | <span data-ttu-id="51e04-565">Deltidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="51e04-565">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="51e04-566">Årsagskoder</span><span class="sxs-lookup"><span data-stu-id="51e04-566">Reason codes</span></span>

<span data-ttu-id="51e04-567">Årsagskoder indeholder oplysninger om status for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="51e04-567">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="51e04-568">Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.</span><span class="sxs-lookup"><span data-stu-id="51e04-568">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="51e04-569">Der kræves følgende årsagskoder og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="51e04-569">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="51e04-570">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="51e04-570">Reason code</span></span>            | <span data-ttu-id="51e04-571">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="51e04-571">Description</span></span>                    | <span data-ttu-id="51e04-572">Anvendelige scenarier</span><span class="sxs-lookup"><span data-stu-id="51e04-572">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="51e04-573">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="51e04-573">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="51e04-574">Afgang før første løn</span><span class="sxs-lookup"><span data-stu-id="51e04-574">Departure before first payroll</span></span> | <span data-ttu-id="51e04-575">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="51e04-575">Terminate worker</span></span>     |
| <span data-ttu-id="51e04-576">OPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="51e04-576">RESIGNATION</span></span>            | <span data-ttu-id="51e04-577">Opsigelse</span><span class="sxs-lookup"><span data-stu-id="51e04-577">Resignation</span></span>                    | <span data-ttu-id="51e04-578">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="51e04-578">Terminate worker</span></span>     |
| <span data-ttu-id="51e04-579">PENSION</span><span class="sxs-lookup"><span data-stu-id="51e04-579">PENSION</span></span>                | <span data-ttu-id="51e04-580">Pension</span><span class="sxs-lookup"><span data-stu-id="51e04-580">Pension</span></span>                        | <span data-ttu-id="51e04-581">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="51e04-581">Terminate worker</span></span>     |
| <span data-ttu-id="51e04-582">OPHØR</span><span class="sxs-lookup"><span data-stu-id="51e04-582">TERMINATION</span></span>            | <span data-ttu-id="51e04-583">Ophør</span><span class="sxs-lookup"><span data-stu-id="51e04-583">Termination</span></span>                    | <span data-ttu-id="51e04-584">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="51e04-584">Terminate worker</span></span>     |
| <span data-ttu-id="51e04-585">PENSION</span><span class="sxs-lookup"><span data-stu-id="51e04-585">RETIREMENT</span></span>             | <span data-ttu-id="51e04-586">Pension</span><span class="sxs-lookup"><span data-stu-id="51e04-586">Retirement</span></span>                     | <span data-ttu-id="51e04-587">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="51e04-587">Terminate worker</span></span>     |
| <span data-ttu-id="51e04-588">FRAVÆRENDE</span><span class="sxs-lookup"><span data-stu-id="51e04-588">ABSENTEE</span></span>               | <span data-ttu-id="51e04-589">Fraværende</span><span class="sxs-lookup"><span data-stu-id="51e04-589">Absentee</span></span>                       | <span data-ttu-id="51e04-590">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="51e04-590">Terminate worker</span></span>     |
| <span data-ttu-id="51e04-591">ANDET</span><span class="sxs-lookup"><span data-stu-id="51e04-591">OTHER</span></span>                  | <span data-ttu-id="51e04-592">Andre årsager</span><span class="sxs-lookup"><span data-stu-id="51e04-592">Other Reasons</span></span>                  | <span data-ttu-id="51e04-593">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="51e04-593">Terminate worker</span></span>     |
| <span data-ttu-id="51e04-594">LUKNING</span><span class="sxs-lookup"><span data-stu-id="51e04-594">CLOSURE</span></span>                | <span data-ttu-id="51e04-595">Virksomhedslukning</span><span class="sxs-lookup"><span data-stu-id="51e04-595">Business Closure</span></span>               | <span data-ttu-id="51e04-596">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="51e04-596">Terminate worker</span></span>     |
| <span data-ttu-id="51e04-597">DØDSFALD</span><span class="sxs-lookup"><span data-stu-id="51e04-597">DEATH</span></span>                  | <span data-ttu-id="51e04-598">Dødsfald</span><span class="sxs-lookup"><span data-stu-id="51e04-598">Death</span></span>                          | <span data-ttu-id="51e04-599">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="51e04-599">Terminate worker</span></span>     |
| <span data-ttu-id="51e04-600">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="51e04-600">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="51e04-601">Orlov</span><span class="sxs-lookup"><span data-stu-id="51e04-601">Leave of Absence</span></span>               | <span data-ttu-id="51e04-602">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="51e04-602">Terminate worker</span></span>     |
| <span data-ttu-id="51e04-603">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="51e04-603">CONTRACTEND</span></span>            | <span data-ttu-id="51e04-604">Kontraktudløb</span><span class="sxs-lookup"><span data-stu-id="51e04-604">End of Contract</span></span>                | <span data-ttu-id="51e04-605">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="51e04-605">Terminate worker</span></span>     |
| <span data-ttu-id="51e04-606">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="51e04-606">SALARYCHANGE</span></span>           | <span data-ttu-id="51e04-607">Ændring af løn</span><span class="sxs-lookup"><span data-stu-id="51e04-607">Change of Salary</span></span>               | <span data-ttu-id="51e04-608">Kompensation</span><span class="sxs-lookup"><span data-stu-id="51e04-608">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="51e04-609">Ansættelsesvilkår</span><span class="sxs-lookup"><span data-stu-id="51e04-609">Terms of employment</span></span>

<span data-ttu-id="51e04-610">Ansættelsesvilkår bruges til at oprette kategorier for ansættelsesvilkår.</span><span class="sxs-lookup"><span data-stu-id="51e04-610">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="51e04-611">Vilkårene knyttes til Dayforce som beskæftigelsesindikatorværdier.</span><span class="sxs-lookup"><span data-stu-id="51e04-611">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="51e04-612">Følgende begreber for beskæftigelse og beskrivelser er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="51e04-612">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="51e04-613">Ansættelsesvilkår</span><span class="sxs-lookup"><span data-stu-id="51e04-613">Terms of employment</span></span>   | <span data-ttu-id="51e04-614">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="51e04-614">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="51e04-615">Regulær</span><span class="sxs-lookup"><span data-stu-id="51e04-615">Regular</span></span>               | <span data-ttu-id="51e04-616">Regulær</span><span class="sxs-lookup"><span data-stu-id="51e04-616">Regular</span></span>     |
| <span data-ttu-id="51e04-617">Direkte</span><span class="sxs-lookup"><span data-stu-id="51e04-617">Direct</span></span>                | <span data-ttu-id="51e04-618">Direkte</span><span class="sxs-lookup"><span data-stu-id="51e04-618">Direct</span></span>      |
| <span data-ttu-id="51e04-619">Turnustjeneste</span><span class="sxs-lookup"><span data-stu-id="51e04-619">Internship</span></span>            | <span data-ttu-id="51e04-620">Turnustjeneste</span><span class="sxs-lookup"><span data-stu-id="51e04-620">Internship</span></span>  |
| <span data-ttu-id="51e04-621">Permanent</span><span class="sxs-lookup"><span data-stu-id="51e04-621">Permanent</span></span>             | <span data-ttu-id="51e04-622">Permanent</span><span class="sxs-lookup"><span data-stu-id="51e04-622">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="51e04-623">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="51e04-623">Marital status</span></span>

<span data-ttu-id="51e04-624">Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="51e04-624">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="51e04-625">Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="51e04-625">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="51e04-626">Human Resources</span><span class="sxs-lookup"><span data-stu-id="51e04-626">Human Resources</span></span>                 | <span data-ttu-id="51e04-627">Dayforce</span><span class="sxs-lookup"><span data-stu-id="51e04-627">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="51e04-628">Gift</span><span class="sxs-lookup"><span data-stu-id="51e04-628">Married</span></span>                | <span data-ttu-id="51e04-629">Gift</span><span class="sxs-lookup"><span data-stu-id="51e04-629">Married</span></span>                   |
| <span data-ttu-id="51e04-630">Enlig</span><span class="sxs-lookup"><span data-stu-id="51e04-630">Single</span></span>                 | <span data-ttu-id="51e04-631">Enlig</span><span class="sxs-lookup"><span data-stu-id="51e04-631">Single</span></span>                    |
| <span data-ttu-id="51e04-632">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="51e04-632">Widowed</span></span>                | <span data-ttu-id="51e04-633">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="51e04-633">Widowed</span></span>                   |
| <span data-ttu-id="51e04-634">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="51e04-634">Divorced</span></span>               | <span data-ttu-id="51e04-635">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="51e04-635">Divorced</span></span>                  |
| <span data-ttu-id="51e04-636">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="51e04-636">Registered Partnership</span></span> | <span data-ttu-id="51e04-637">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="51e04-637">Domestic Partnership</span></span>      |
| <span data-ttu-id="51e04-638">None</span><span class="sxs-lookup"><span data-stu-id="51e04-638">None</span></span>                   | <span data-ttu-id="51e04-639">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="51e04-639">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="51e04-640">Samlever</span><span class="sxs-lookup"><span data-stu-id="51e04-640">Cohabiting</span></span>             | <span data-ttu-id="51e04-641">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="51e04-641">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="51e04-642">Køn</span><span class="sxs-lookup"><span data-stu-id="51e04-642">Gender</span></span>

<span data-ttu-id="51e04-643">Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="51e04-643">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="51e04-644">Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="51e04-644">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="51e04-645">Human Resources</span><span class="sxs-lookup"><span data-stu-id="51e04-645">Human Resources</span></span>       | <span data-ttu-id="51e04-646">Dayforce</span><span class="sxs-lookup"><span data-stu-id="51e04-646">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="51e04-647">Mand</span><span class="sxs-lookup"><span data-stu-id="51e04-647">Male</span></span>         | <span data-ttu-id="51e04-648">Mand</span><span class="sxs-lookup"><span data-stu-id="51e04-648">Male</span></span>                      |
| <span data-ttu-id="51e04-649">Kvinde</span><span class="sxs-lookup"><span data-stu-id="51e04-649">Female</span></span>       | <span data-ttu-id="51e04-650">Kvinde</span><span class="sxs-lookup"><span data-stu-id="51e04-650">Female</span></span>                    |
| <span data-ttu-id="51e04-651">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="51e04-651">Non-specific</span></span> | <span data-ttu-id="51e04-652">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="51e04-652">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="51e04-653">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="51e04-653">Payment method</span></span>

<span data-ttu-id="51e04-654">Betalingsmetoder giver medarbejderen og virksomheden en måde til at beskrive, hvordan medarbejdere skal betales.</span><span class="sxs-lookup"><span data-stu-id="51e04-654">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="51e04-655">Betalingsmåder knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="51e04-655">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="51e04-656">Følgende tabel viser, hvordan betalingsmetoder knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="51e04-656">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="51e04-657">Human Resources</span><span class="sxs-lookup"><span data-stu-id="51e04-657">Human Resources</span></span>             | <span data-ttu-id="51e04-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="51e04-658">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="51e04-659">Indløsning</span><span class="sxs-lookup"><span data-stu-id="51e04-659">Cash</span></span>               | <span data-ttu-id="51e04-660">Indløsning</span><span class="sxs-lookup"><span data-stu-id="51e04-660">Cash</span></span>                      |
| <span data-ttu-id="51e04-661">Elektronisk betaling</span><span class="sxs-lookup"><span data-stu-id="51e04-661">Electronic Payment</span></span> | <span data-ttu-id="51e04-662">Ompostering</span><span class="sxs-lookup"><span data-stu-id="51e04-662">Transfer</span></span>                  |
| <span data-ttu-id="51e04-663">Check</span><span class="sxs-lookup"><span data-stu-id="51e04-663">Check</span></span>              | <span data-ttu-id="51e04-664">Check</span><span class="sxs-lookup"><span data-stu-id="51e04-664">Cheque</span></span>                    |
| <span data-ttu-id="51e04-665">Bankanvisning</span><span class="sxs-lookup"><span data-stu-id="51e04-665">Bank Draft</span></span>         | <span data-ttu-id="51e04-666">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="51e04-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="51e04-667">Andre</span><span class="sxs-lookup"><span data-stu-id="51e04-667">Other</span></span>              | <span data-ttu-id="51e04-668">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="51e04-668">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="51e04-669">Bankkontotype</span><span class="sxs-lookup"><span data-stu-id="51e04-669">Bank account type</span></span>

<span data-ttu-id="51e04-670">Bankkontotyper bruges til elektroniske betalinger til medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="51e04-670">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="51e04-671">Bankkontotyper knyttes til Dayforce som overførselskontooplysninger.</span><span class="sxs-lookup"><span data-stu-id="51e04-671">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="51e04-672">Bankkontotyperne oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="51e04-672">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="51e04-673">Human Resources</span><span class="sxs-lookup"><span data-stu-id="51e04-673">Human Resources</span></span>            | <span data-ttu-id="51e04-674">Dayforce</span><span class="sxs-lookup"><span data-stu-id="51e04-674">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="51e04-675">Checkkonto</span><span class="sxs-lookup"><span data-stu-id="51e04-675">Checking Account</span></span>  | <span data-ttu-id="51e04-676">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="51e04-676">CheckingAccount</span></span>           |
| <span data-ttu-id="51e04-677">Lønkonto</span><span class="sxs-lookup"><span data-stu-id="51e04-677">Payroll Account</span></span>   | <span data-ttu-id="51e04-678">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="51e04-678">PayrollAccount</span></span>            |
| <span data-ttu-id="51e04-679">Opsparingskonto</span><span class="sxs-lookup"><span data-stu-id="51e04-679">Savings Account</span></span>   | <span data-ttu-id="51e04-680">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="51e04-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="51e04-681">BankGirot-konto</span><span class="sxs-lookup"><span data-stu-id="51e04-681">BankGirot account</span></span> | <span data-ttu-id="51e04-682">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="51e04-682">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="51e04-683">PlusGirot-konto</span><span class="sxs-lookup"><span data-stu-id="51e04-683">PlusGirot account</span></span> | <span data-ttu-id="51e04-684">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="51e04-684">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="51e04-685">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="51e04-685">Earning codes</span></span>

<span data-ttu-id="51e04-686">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="51e04-686">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="51e04-687">Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="51e04-687">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="51e04-688">Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="51e04-688">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="51e04-689">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="51e04-689">Supported frequencies</span></span>

- <span data-ttu-id="51e04-690">Alt</span><span class="sxs-lookup"><span data-stu-id="51e04-690">All</span></span>
- <span data-ttu-id="51e04-691">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="51e04-691">EVERYPAY</span></span>
- <span data-ttu-id="51e04-692">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="51e04-692">EACHPAYPERIOD</span></span>
- <span data-ttu-id="51e04-693">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="51e04-693">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="51e04-694">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="51e04-694">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="51e04-695">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-695">1OFMTH</span></span>
- <span data-ttu-id="51e04-696">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-696">LASTOFMTH</span></span>
- <span data-ttu-id="51e04-697">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-697">2OFMTH</span></span>
- <span data-ttu-id="51e04-698">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-698">3OFMTH</span></span>
- <span data-ttu-id="51e04-699">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-699">4OFMTH</span></span>
- <span data-ttu-id="51e04-700">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-700">5OFMTH</span></span>
- <span data-ttu-id="51e04-701">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-701">1N2OFMTH</span></span>
- <span data-ttu-id="51e04-702">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-702">3N4OFMTH</span></span>
- <span data-ttu-id="51e04-703">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-703">1N3OFMTH</span></span>
- <span data-ttu-id="51e04-704">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-704">1N4OFMTH</span></span>
- <span data-ttu-id="51e04-705">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-705">2N3OFMTH</span></span>
- <span data-ttu-id="51e04-706">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-706">2N4OFMTH</span></span>
- <span data-ttu-id="51e04-707">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-707">1N2N3OFMTH</span></span>
- <span data-ttu-id="51e04-708">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-708">1N2N4OFMTH</span></span>
- <span data-ttu-id="51e04-709">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-709">1N3N4OFMTH</span></span>
- <span data-ttu-id="51e04-710">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-710">2N3N4OFMTH</span></span>
- <span data-ttu-id="51e04-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="51e04-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="51e04-712">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="51e04-712">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="51e04-713">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="51e04-713">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="51e04-714">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="51e04-714">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="51e04-715">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="51e04-715">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="51e04-716">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="51e04-716">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="51e04-717">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="51e04-717">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="51e04-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="51e04-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="51e04-719">Adresser</span><span class="sxs-lookup"><span data-stu-id="51e04-719">Addresses</span></span>

<span data-ttu-id="51e04-720">Identifikation af specifikke koder for land eller område, stat og region (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende.</span><span class="sxs-lookup"><span data-stu-id="51e04-720">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="51e04-721">Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.</span><span class="sxs-lookup"><span data-stu-id="51e04-721">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="51e04-722">Human Resources</span><span class="sxs-lookup"><span data-stu-id="51e04-722">Human Resources</span></span>              | <span data-ttu-id="51e04-723">Dayforce</span><span class="sxs-lookup"><span data-stu-id="51e04-723">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="51e04-724">Land/område</span><span class="sxs-lookup"><span data-stu-id="51e04-724">Country/Region</span></span>      | <span data-ttu-id="51e04-725">Landekode</span><span class="sxs-lookup"><span data-stu-id="51e04-725">Country Code</span></span>          |
| <span data-ttu-id="51e04-726">Postnummer</span><span class="sxs-lookup"><span data-stu-id="51e04-726">Zip/Postal Code</span></span>     | <span data-ttu-id="51e04-727">Postnummer</span><span class="sxs-lookup"><span data-stu-id="51e04-727">Postal Code</span></span>           |
| <span data-ttu-id="51e04-728">Status</span><span class="sxs-lookup"><span data-stu-id="51e04-728">State</span></span>               | <span data-ttu-id="51e04-729">Statskode</span><span class="sxs-lookup"><span data-stu-id="51e04-729">State Code</span></span>            |
| <span data-ttu-id="51e04-730">Bynavn</span><span class="sxs-lookup"><span data-stu-id="51e04-730">City</span></span>                | <span data-ttu-id="51e04-731">Bynavn</span><span class="sxs-lookup"><span data-stu-id="51e04-731">City</span></span>                  |
| <span data-ttu-id="51e04-732">Region</span><span class="sxs-lookup"><span data-stu-id="51e04-732">County</span></span>              | <span data-ttu-id="51e04-733">Område (kommune)</span><span class="sxs-lookup"><span data-stu-id="51e04-733">County (Municipality)</span></span> |
| <span data-ttu-id="51e04-734">Gade</span><span class="sxs-lookup"><span data-stu-id="51e04-734">Street</span></span>              | <span data-ttu-id="51e04-735">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="51e04-735">Address Line 1</span></span>        |
| <span data-ttu-id="51e04-736">Gadenummer</span><span class="sxs-lookup"><span data-stu-id="51e04-736">Street Number</span></span>       | <span data-ttu-id="51e04-737">Adresselinje 2</span><span class="sxs-lookup"><span data-stu-id="51e04-737">Address Line 2</span></span>        |
| <span data-ttu-id="51e04-738">Bygningskomplement</span><span class="sxs-lookup"><span data-stu-id="51e04-738">Building Complement</span></span> | <span data-ttu-id="51e04-739">Adresselinje 5</span><span class="sxs-lookup"><span data-stu-id="51e04-739">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="51e04-740">Pasnummer</span><span class="sxs-lookup"><span data-stu-id="51e04-740">Passport number</span></span>

<span data-ttu-id="51e04-741">Medarbejdere kan erklære pasoplysninger.</span><span class="sxs-lookup"><span data-stu-id="51e04-741">Employees can declare passport information.</span></span> <span data-ttu-id="51e04-742">Disse oplysninger er af identifikationstypen **Pas** og er integreret i Dayforce som en del af en medarbejders Mexico-specifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="51e04-742">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="51e04-743">Identifikationstype = "Pas"</span><span class="sxs-lookup"><span data-stu-id="51e04-743">Identification Type = "Passport"</span></span>
- <span data-ttu-id="51e04-744">Udstedt den</span><span class="sxs-lookup"><span data-stu-id="51e04-744">Issued Date</span></span>
- <span data-ttu-id="51e04-745">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="51e04-745">Expiration Date</span></span>

<span data-ttu-id="51e04-746">Medarbejdere kan angive flere identifikationsnumre af **Pas**-identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="51e04-746">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="51e04-747">Men det er kun den aktuelle aktive paspost, der integreres i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="51e04-747">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="51e04-748">Hvis alle pasposter er udløbet, integreres det pas, der senest blev udstedt, i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="51e04-748">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]