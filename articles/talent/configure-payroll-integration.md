---
title: Konfigurere lønintegration mellem Talent og Dayforce
description: Dette emne forklarer, hvordan du kan konfigurere integration mellem Microsoft Dynamics 365 for Talent og Ceridian Dayforce, så du kan behandle en lønkørsel.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
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
ms.openlocfilehash: 59234ef44ad22383ae5daf71d4b663c6183e6c05
ms.sourcegitcommit: d599bc1fc60a010c2753ca547219ae21456b1df9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/25/2019
ms.locfileid: "1702812"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="77ac4-103">Konfigurere lønintegrationen mellem Talent og Dayforce</span><span class="sxs-lookup"><span data-stu-id="77ac4-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="77ac4-104">Integration mellem Microsoft Dynamics 365 for Talent og Ceridian Dayforce er baseret på flere konfigurationstrin, der er beskrevet i dette emne.</span><span class="sxs-lookup"><span data-stu-id="77ac4-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="77ac4-105">Du skal konfigurere integrationen i både Talent og Dayforce, før du kan behandle en lønkørsel.</span><span class="sxs-lookup"><span data-stu-id="77ac4-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="77ac4-106">Når du bruger en tjeneste, f.eks. Dayforce, til at fuldføre lønkørsler, skal du aktivere integrationen i Talent.</span><span class="sxs-lookup"><span data-stu-id="77ac4-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="77ac4-107">Integrationen kræver bestemte data fra Talent.</span><span class="sxs-lookup"><span data-stu-id="77ac4-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="77ac4-108">Du skal derfor kontrollere, at data, der er knyttet til Dayforce, er konfigureret i Talent på en måde, der understøtter integrationen.</span><span class="sxs-lookup"><span data-stu-id="77ac4-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="77ac4-109">Integrationen bruger følgende brede kategorier af data.</span><span class="sxs-lookup"><span data-stu-id="77ac4-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="77ac4-110">Personaledata</span><span class="sxs-lookup"><span data-stu-id="77ac4-110">Human resources data</span></span>
- <span data-ttu-id="77ac4-111">Kompensationsdata</span><span class="sxs-lookup"><span data-stu-id="77ac4-111">Compensation data</span></span>
- <span data-ttu-id="77ac4-112">Lønoplysninger, f.eks. løncyklusser, betalingsperioder og lønkoder</span><span class="sxs-lookup"><span data-stu-id="77ac4-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="77ac4-113">Arbejderdata</span><span class="sxs-lookup"><span data-stu-id="77ac4-113">Worker data</span></span>

<span data-ttu-id="77ac4-114">Dette emne beskrives de trin, du skal udføre for at aktivere integrationen.</span><span class="sxs-lookup"><span data-stu-id="77ac4-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="77ac4-115">Det forklarer også typerne af data og oplysninger om konfigurationen, der kræves til integrationen.</span><span class="sxs-lookup"><span data-stu-id="77ac4-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="77ac4-116">Aktivere integrationen.</span><span class="sxs-lookup"><span data-stu-id="77ac4-116">Enable the integration</span></span>

<span data-ttu-id="77ac4-117">I Talent skal du aktivere integrationen og angive konfigurationsoplysningerne for at oprette forbindelse til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="77ac4-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="77ac4-118">Hvis den finanspostering, der er produceret, skal importeres til Microsoft Dynamics 365 for Finance and Operations, skal du også konfigurere en Microsoft Azure-lagerkonto og angive Azure-lagerets forbindelsesstreng i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="77ac4-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="77ac4-119">Følg disse trin for at aktivere integrationen i Talent.</span><span class="sxs-lookup"><span data-stu-id="77ac4-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="77ac4-120">På siden **Systemadministration** skal du vælge **Integrationskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="77ac4-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="77ac4-121">Angiv det sikre FTP-slutpunkt og den sikre FTP-mappesti.</span><span class="sxs-lookup"><span data-stu-id="77ac4-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="77ac4-122">Angiv brugernavnet og adgangskoden for den bruger, der skal have adgang til det sikre FTP-slutpunkt og den sikre mappesti.</span><span class="sxs-lookup"><span data-stu-id="77ac4-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="77ac4-123">Test forbindelsen, som krævet, og angiv indstillingen **Aktivér lønintegration** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="77ac4-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="77ac4-124">Når integrationen er aktiveret, oprettes dataeksportpakken og -filerne, og hyppigheden angives.</span><span class="sxs-lookup"><span data-stu-id="77ac4-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="77ac4-125">Du kan ændre denne frekvens efter behov.</span><span class="sxs-lookup"><span data-stu-id="77ac4-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="77ac4-126">Yderligere oplysninger om Azure-lagerkonti og Azure-lagerforbindelsesstrenge finder du i følgende Azure-emner:</span><span class="sxs-lookup"><span data-stu-id="77ac4-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="77ac4-127">Om Azure-lagerkonti</span><span class="sxs-lookup"><span data-stu-id="77ac4-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="77ac4-128">Konfigurere forbindelsesstrenge for Azure-datalager</span><span class="sxs-lookup"><span data-stu-id="77ac4-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="77ac4-129">Tekniske oplysninger ved aktivering af lønintegration</span><span class="sxs-lookup"><span data-stu-id="77ac4-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="77ac4-130">Aktivering af lønintegration har to primære effekter:</span><span class="sxs-lookup"><span data-stu-id="77ac4-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="77ac4-131">Der oprettes et dataeksport projekt ved navn "Lønintegrationseksport".</span><span class="sxs-lookup"><span data-stu-id="77ac4-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="77ac4-132">Dette projekt indeholder de objekter og felter, der kræves til lønintegration.</span><span class="sxs-lookup"><span data-stu-id="77ac4-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="77ac4-133">Hvis du vil undersøge projektet, skal du gå til **Systemadministration**, vælge feltet **Datastyring** og derefter åbne dataprojektet på listen over projekter.</span><span class="sxs-lookup"><span data-stu-id="77ac4-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="77ac4-134">Dette batchjob udfører dataeksportprojektet, krypterer den resulterende datapakke og overfører datapakkefilen til det SFTP-slutpunkt, der er konfigureret på skærmen **Integrationskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="77ac4-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="77ac4-135">Den datapakke, der overføres til SFTP-slutpunktet, krypteres ved hjælp af en nøgle, der er entydig for pakken.</span><span class="sxs-lookup"><span data-stu-id="77ac4-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="77ac4-136">Nøglen er i en Azure Key Vault, der kun kan åbnes af Ceridian.</span><span class="sxs-lookup"><span data-stu-id="77ac4-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="77ac4-137">Det er ikke muligt at dekryptere og undersøge datapakkens indhold.</span><span class="sxs-lookup"><span data-stu-id="77ac4-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="77ac4-138">Hvis du har brug for at undersøge indholdet af datapakken, skal du eksportere dataprojektet "Lønintegrationseksport" manuelt, download det og derefter åbne det.</span><span class="sxs-lookup"><span data-stu-id="77ac4-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="77ac4-139">Manuel eksport anvender ikke kryptering eller overførsel af pakken.</span><span class="sxs-lookup"><span data-stu-id="77ac4-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="77ac4-140">Konfigurere dine data</span><span class="sxs-lookup"><span data-stu-id="77ac4-140">Configure your data</span></span> 

<span data-ttu-id="77ac4-141">Hvis du vil behandle løn, skal du konfigurere personaledata i Talent.</span><span class="sxs-lookup"><span data-stu-id="77ac4-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="77ac4-142">Du skal angive virksomhedens data, f.eks. job og stillinger, sammen med frynsegoder og kompensationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="77ac4-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="77ac4-143">Disse oplysninger indeholder oplysningerne om ansættelse, løn og fradrag, der kræves for at generere løn for medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="77ac4-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="77ac4-144">Personaledata</span><span class="sxs-lookup"><span data-stu-id="77ac4-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="77ac4-145">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="77ac4-145">Benefits</span></span> 

<span data-ttu-id="77ac4-146">Personale indeholder en række værktøjer til konfiguration og vedligeholdelse af frynsegoder, fradrag og arbejderkompensationsplaner, som en organisation tilbyder eller behandler for sine ansatte.</span><span class="sxs-lookup"><span data-stu-id="77ac4-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="77ac4-147">Når du opretter frynsegoder, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="77ac4-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="77ac4-148">Frynsegodeplaner</span><span class="sxs-lookup"><span data-stu-id="77ac4-148">Benefit plans</span></span>

- <span data-ttu-id="77ac4-149">Plan (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-149">Plan (required)</span></span>
- <span data-ttu-id="77ac4-150">Type (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-150">Type (required)</span></span>
- <span data-ttu-id="77ac4-151">Løneffekt (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-151">Payroll impact (required)</span></span>
- <span data-ttu-id="77ac4-152">Opkræv restancer</span><span class="sxs-lookup"><span data-stu-id="77ac4-152">Recover arrears</span></span>
- <span data-ttu-id="77ac4-153">Fradragsmetode</span><span class="sxs-lookup"><span data-stu-id="77ac4-153">Deduction method</span></span>
- <span data-ttu-id="77ac4-154">Prioriteret fradrag</span><span class="sxs-lookup"><span data-stu-id="77ac4-154">Deduction priority</span></span>
- <span data-ttu-id="77ac4-155">Grænseperiode</span><span class="sxs-lookup"><span data-stu-id="77ac4-155">Limit period</span></span>
- <span data-ttu-id="77ac4-156">Beløb for grænse</span><span class="sxs-lookup"><span data-stu-id="77ac4-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="77ac4-157">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="77ac4-157">Benefits</span></span>

- <span data-ttu-id="77ac4-158">Plan (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-158">Plan (required)</span></span>
- <span data-ttu-id="77ac4-159">Type (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-159">Type (required)</span></span>
- <span data-ttu-id="77ac4-160">Mulighed (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-160">Option (required)</span></span>
- <span data-ttu-id="77ac4-161">Frynsegode-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-161">Benefit ID (required)</span></span>
- <span data-ttu-id="77ac4-162">Frekvens</span><span class="sxs-lookup"><span data-stu-id="77ac4-162">Frequency</span></span>
- <span data-ttu-id="77ac4-163">Basis</span><span class="sxs-lookup"><span data-stu-id="77ac4-163">Basis</span></span>
- <span data-ttu-id="77ac4-164">Beløb eller sats</span><span class="sxs-lookup"><span data-stu-id="77ac4-164">Amount or rate</span></span>
- <span data-ttu-id="77ac4-165">Lønkode</span><span class="sxs-lookup"><span data-stu-id="77ac4-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="77ac4-166">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="77ac4-166">Supported frequencies</span></span> 

- <span data-ttu-id="77ac4-167">Ugentlig</span><span class="sxs-lookup"><span data-stu-id="77ac4-167">Weekly</span></span>
- <span data-ttu-id="77ac4-168">Pr. 14 dage</span><span class="sxs-lookup"><span data-stu-id="77ac4-168">Bi-weekly</span></span>
- <span data-ttu-id="77ac4-169">To gange om måneden</span><span class="sxs-lookup"><span data-stu-id="77ac4-169">Semi-monthly</span></span>
- <span data-ttu-id="77ac4-170">Månedlig</span><span class="sxs-lookup"><span data-stu-id="77ac4-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="77ac4-171">Understøttede grundlag</span><span class="sxs-lookup"><span data-stu-id="77ac4-171">Supported bases</span></span> 

- <span data-ttu-id="77ac4-172">Fast beløb</span><span class="sxs-lookup"><span data-stu-id="77ac4-172">Fixed amount</span></span>
- <span data-ttu-id="77ac4-173">Procentdel af løn</span><span class="sxs-lookup"><span data-stu-id="77ac4-173">Percent of earnings</span></span>
- <span data-ttu-id="77ac4-174">Produktive timer</span><span class="sxs-lookup"><span data-stu-id="77ac4-174">Productive hours</span></span>

<span data-ttu-id="77ac4-175">Dayforce opretter følgende fradrag, der er baseret på den løneffekt, der er defineret på frynsegodeplanen.</span><span class="sxs-lookup"><span data-stu-id="77ac4-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="77ac4-176">Valg i Talent</span><span class="sxs-lookup"><span data-stu-id="77ac4-176">Selection in Talent</span></span>        | <span data-ttu-id="77ac4-177">Resultat i Dayforce</span><span class="sxs-lookup"><span data-stu-id="77ac4-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="77ac4-178">None</span><span class="sxs-lookup"><span data-stu-id="77ac4-178">None</span></span>                       | <span data-ttu-id="77ac4-179">Der oprettes ikke noget fradrag.</span><span class="sxs-lookup"><span data-stu-id="77ac4-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="77ac4-180">Kun fradrag</span><span class="sxs-lookup"><span data-stu-id="77ac4-180">Deduction only</span></span>             | <span data-ttu-id="77ac4-181">Der oprettes et medarbejderfradrag.</span><span class="sxs-lookup"><span data-stu-id="77ac4-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="77ac4-182">Kun bidrag</span><span class="sxs-lookup"><span data-stu-id="77ac4-182">Contribution only</span></span>          | <span data-ttu-id="77ac4-183">Der oprettes et arbejdsgiverfradrag.</span><span class="sxs-lookup"><span data-stu-id="77ac4-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="77ac4-184">Fradrag og bidrag</span><span class="sxs-lookup"><span data-stu-id="77ac4-184">Deduction and contribution</span></span> | <span data-ttu-id="77ac4-185">Der oprettes medarbejder- og arbejdsgiverfradrag.</span><span class="sxs-lookup"><span data-stu-id="77ac4-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="77ac4-186">Du kan finde flere oplysninger om, hvordan du definerer og administrerer et frynsegodeprogram under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="77ac4-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="77ac4-187">Levere et frynsegodeprogram for medarbejdere</span><span class="sxs-lookup"><span data-stu-id="77ac4-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="77ac4-188">Oprette et nyt frynsegode</span><span class="sxs-lookup"><span data-stu-id="77ac4-188">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="77ac4-189">Definere regler og politikker for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="77ac4-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="77ac4-190">Tilmelde og fjerne frynsegoder fra arbejdere</span><span class="sxs-lookup"><span data-stu-id="77ac4-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="77ac4-191">Kompensation</span><span class="sxs-lookup"><span data-stu-id="77ac4-191">Compensation</span></span> 

<span data-ttu-id="77ac4-192">Kompensationsstyring bruges til at styre fordelingen af grundløn og bonusser.</span><span class="sxs-lookup"><span data-stu-id="77ac4-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="77ac4-193">En medarbejders faste grundløn og kvalifikationstillæg styres gennem faste lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="77ac4-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="77ac4-194">Betalingen af incitamentsløn som f.eks. bonusudbetalinger, præstationsbonusser, aktieoptioner og tildelte aktier samt engangsbonusser styres ved hjælp af variable lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="77ac4-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="77ac4-195">Dayforce anvendes kompensationsoplysninger til at beregne en medarbejders timesats eller årlige sats.</span><span class="sxs-lookup"><span data-stu-id="77ac4-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="77ac4-196">Konverteringer af planer for fast løn og lønsats er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="77ac4-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="77ac4-197">Medarbejderne skal være knyttet til en plan for fast løn.</span><span class="sxs-lookup"><span data-stu-id="77ac4-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="77ac4-198">Du kan finde flere oplysninger om kompensationsplaner under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="77ac4-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="77ac4-199">Oprette faste kompensationsordninger</span><span class="sxs-lookup"><span data-stu-id="77ac4-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="77ac4-200">Oprette planer for variabel kompensation</span><span class="sxs-lookup"><span data-stu-id="77ac4-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="77ac4-201">Udarbejde løn-/kompensationsstruktur og -planer</span><span class="sxs-lookup"><span data-stu-id="77ac4-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="77ac4-202">Proceskompensation</span><span class="sxs-lookup"><span data-stu-id="77ac4-202">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="77ac4-203">Definere kompensationsproces og beregne resultater</span><span class="sxs-lookup"><span data-stu-id="77ac4-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="77ac4-204">Melde en medarbejder til en fast lønplan</span><span class="sxs-lookup"><span data-stu-id="77ac4-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="77ac4-205">Melde en medarbejder til en variabel lønplan</span><span class="sxs-lookup"><span data-stu-id="77ac4-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="77ac4-206">Job</span><span class="sxs-lookup"><span data-stu-id="77ac4-206">Jobs</span></span> 

<span data-ttu-id="77ac4-207">Et job er en samling af de opgaver og ansvarsområder, der kræves af en person, der udfører et job.</span><span class="sxs-lookup"><span data-stu-id="77ac4-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="77ac4-208">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="77ac4-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="77ac4-209">Konfiguration af komponenter i et job</span><span class="sxs-lookup"><span data-stu-id="77ac4-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="77ac4-210">Definere nye job</span><span class="sxs-lookup"><span data-stu-id="77ac4-210">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="77ac4-211">Stillinger</span><span class="sxs-lookup"><span data-stu-id="77ac4-211">Positions</span></span>

<span data-ttu-id="77ac4-212">En stilling er en individuel forekomst af et job.</span><span class="sxs-lookup"><span data-stu-id="77ac4-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="77ac4-213">For eksempel er stillingen "Salgschef (øst)" én af de stillinger, der er tilknyttet jobbet "Salgschef".</span><span class="sxs-lookup"><span data-stu-id="77ac4-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="77ac4-214">En stilling findes i en afdeling.</span><span class="sxs-lookup"><span data-stu-id="77ac4-214">A position exists in a department.</span></span> <span data-ttu-id="77ac4-215">Der kan kun knyttes én arbejder til hver stilling.</span><span class="sxs-lookup"><span data-stu-id="77ac4-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="77ac4-216">Hav følgende data og konfiguration i tankerne, når du konfigurerer stillinger:</span><span class="sxs-lookup"><span data-stu-id="77ac4-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="77ac4-217">Stilling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-217">Position (required)</span></span>
- <span data-ttu-id="77ac4-218">Beskrivelse (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-218">Description (required)</span></span>
- <span data-ttu-id="77ac4-219">Job (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-219">Job (required)</span></span>
- <span data-ttu-id="77ac4-220">Afdeling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-220">Department (required)</span></span>
- <span data-ttu-id="77ac4-221">Stillingstype (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-221">Position type (required)</span></span>
- <span data-ttu-id="77ac4-222">Fuldtidsækvivalent</span><span class="sxs-lookup"><span data-stu-id="77ac4-222">Full-time equivalent</span></span>
- <span data-ttu-id="77ac4-223">Normaltimer på årsbasis (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="77ac4-224">Betalt af juridiske enhed (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="77ac4-225">Betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-225">Pay cycle (required)</span></span>
- <span data-ttu-id="77ac4-226">Økonomisk standarddimension – bærer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="77ac4-227">Arbejdertildeling – arbejder, tildelingsstart, tildelingsslut, årsagskode</span><span class="sxs-lookup"><span data-stu-id="77ac4-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="77ac4-228">Hvis flere stillinger i den samme afdeling er knyttet til samme job, konsolideres de til en enkelt stilling i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="77ac4-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="77ac4-229">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="77ac4-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="77ac4-230">Organisere dine medarbejdere ved hjælp af afdelinger, jobs og stillinger</span><span class="sxs-lookup"><span data-stu-id="77ac4-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="77ac4-231">Konfigurere stillinger</span><span class="sxs-lookup"><span data-stu-id="77ac4-231">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="77ac4-232">Afdelinger</span><span class="sxs-lookup"><span data-stu-id="77ac4-232">Departments</span></span>

<span data-ttu-id="77ac4-233">En afdeling er en driftsenhed, der repræsenterer en kategori eller et funktionsområde i en organisation.</span><span class="sxs-lookup"><span data-stu-id="77ac4-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="77ac4-234">En afdeling er ansvarlig for et bestemt område i organisationen, såsom salg, regnskab eller personale.</span><span class="sxs-lookup"><span data-stu-id="77ac4-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="77ac4-235">Du kan bruge afdelinger til at rapportere om funktionsområder.</span><span class="sxs-lookup"><span data-stu-id="77ac4-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="77ac4-236">Afdelinger kan have ansvar for driftsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="77ac4-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="77ac4-237">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="77ac4-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="77ac4-238">Oprette en afdeling og knytte den til afdelingshierarkiet</span><span class="sxs-lookup"><span data-stu-id="77ac4-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="77ac4-239">Definere nye afdelinger</span><span class="sxs-lookup"><span data-stu-id="77ac4-239">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="77ac4-240">Betalingscyklusser og lønperioder</span><span class="sxs-lookup"><span data-stu-id="77ac4-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="77ac4-241">En betalingscyklus bestemmer, hvor ofte løn køres,og de specifikke dage, hvor arbejdere betales.</span><span class="sxs-lookup"><span data-stu-id="77ac4-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="77ac4-242">En løncyklus kan f.eks. være månedlig, og medarbejdere betales måske på den sidste dag i måneden.</span><span class="sxs-lookup"><span data-stu-id="77ac4-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="77ac4-243">En løncyklus kan også være ugentligt, og medarbejdere betales måske tirsdag efter slutningen af lønperioden.</span><span class="sxs-lookup"><span data-stu-id="77ac4-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="77ac4-244">Løncyklusser tildeles til stillinger for at styre, hvornår arbejdere i disse stillinger bliver betalt.</span><span class="sxs-lookup"><span data-stu-id="77ac4-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="77ac4-245">Når du opretter betalingscyklusser, kan du generere lønperioder for hver cyklus.</span><span class="sxs-lookup"><span data-stu-id="77ac4-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="77ac4-246">Hver lønperiode omfatter en standardbetalingsdato, der er baseret på oplysninger, du angiver.</span><span class="sxs-lookup"><span data-stu-id="77ac4-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="77ac4-247">Du kan dog redigere standardbetalingsdatoen i en lønperiode til at tillade undtagelser, f.eks. når betalingsdatoen falder på en helligdag.</span><span class="sxs-lookup"><span data-stu-id="77ac4-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="77ac4-248">Følgende oplysninger bruges i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="77ac4-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="77ac4-249">Betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-249">Pay cycle (required)</span></span>
- <span data-ttu-id="77ac4-250">Hyppighed for betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="77ac4-251">Periodens startdato (første lønperiode påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="77ac4-252">Standardbetalingsdato (første lønperiode påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="77ac4-253">Oplysningerne er integreret med Dayforce som løngrupper og adskilles af et land eller område for hver løncyklus.</span><span class="sxs-lookup"><span data-stu-id="77ac4-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="77ac4-254">Mindst én periode skal genereres før integration.</span><span class="sxs-lookup"><span data-stu-id="77ac4-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="77ac4-255">Dayforce genererer løngruppekalendere og betalingsdatoer, der er baseret på startdatoen for den første lønperiode og den standardbetalingsdato, der er angivet i Talent.</span><span class="sxs-lookup"><span data-stu-id="77ac4-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="77ac4-256">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="77ac4-256">Earning codes</span></span>

<span data-ttu-id="77ac4-257">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="77ac4-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="77ac4-258">Koderne har forskellige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="77ac4-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="77ac4-259">Følgende oplysninger bruges i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="77ac4-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="77ac4-260">Lønkode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-260">Earning Code (required)</span></span>
- <span data-ttu-id="77ac4-261">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="77ac4-261">Description</span></span>
- <span data-ttu-id="77ac4-262">Måleenhed</span><span class="sxs-lookup"><span data-stu-id="77ac4-262">Unit of measure</span></span>
- <span data-ttu-id="77ac4-263">Produktiv</span><span class="sxs-lookup"><span data-stu-id="77ac4-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="77ac4-264">Arbejderdata</span><span class="sxs-lookup"><span data-stu-id="77ac4-264">Worker data</span></span>

<span data-ttu-id="77ac4-265">Posterne for de forskellige typer arbejdere, du beskæftiger, er vigtige for dine personale- og lønsystemer.</span><span class="sxs-lookup"><span data-stu-id="77ac4-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="77ac4-266">De oplysninger, du angiver, kan bruges til at spore arbejdere og personoplysninger.</span><span class="sxs-lookup"><span data-stu-id="77ac4-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="77ac4-267">Du kan vedligeholde følgende oplysninger for arbejdere:</span><span class="sxs-lookup"><span data-stu-id="77ac4-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="77ac4-268">**Basis** – Vedligehold grundlæggende oplysninger om en arbejder, f.eks. kontaktoplysninger, demografiske oplysninger, identifikationsoplysninger, oplysninger om familie, status for militærtjeneste, oplysninger om udstationering og personlige kontaktpersoner og kontaktpersoner i nødsituationer.</span><span class="sxs-lookup"><span data-stu-id="77ac4-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="77ac4-269">**Beskæftigelse** – Vedligehold oplysninger om en arbejders beskæftigelse, f.eks. firma- eller organisationstilhørsforhold, stillingstildeling, start- og slutdatoer, arbejdstilladelse, vilkår for ansættelse, pension, ferie og flytteoplysninger.</span><span class="sxs-lookup"><span data-stu-id="77ac4-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="77ac4-270">**Orlov og fravær** – Vedligehold oplysninger om en arbejders fravær, f.eks. arbejdskalendere, fraværstransaktioner og fraværsopsætning.</span><span class="sxs-lookup"><span data-stu-id="77ac4-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="77ac4-271">**Kompensation og løn** – Vedligehold oplysninger om en arbejders kompensationsplaner og lønoplysninger, f.eks. tilmelding til planer, priser, ydeevne, provision, skatteoplysninger, pensionering og skattefradrag.</span><span class="sxs-lookup"><span data-stu-id="77ac4-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="77ac4-272">Når du angiver arbejderoplysninger, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="77ac4-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="77ac4-273">Generelle oplysninger</span><span class="sxs-lookup"><span data-stu-id="77ac4-273">General information</span></span>

- <span data-ttu-id="77ac4-274">Personalenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-274">Personnel number (required)</span></span>
- <span data-ttu-id="77ac4-275">Fornavn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-275">First name (required)</span></span>
- <span data-ttu-id="77ac4-276">Efternavn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-276">Last name (required)</span></span>
- <span data-ttu-id="77ac4-277">Mellemnavn</span><span class="sxs-lookup"><span data-stu-id="77ac4-277">Middle name</span></span>
- <span data-ttu-id="77ac4-278">Anciennitetsdato</span><span class="sxs-lookup"><span data-stu-id="77ac4-278">Seniority date</span></span>
- <span data-ttu-id="77ac4-279">Kendt som</span><span class="sxs-lookup"><span data-stu-id="77ac4-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="77ac4-280">Personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="77ac4-280">Personal information</span></span>

- <span data-ttu-id="77ac4-281">Ægteskabelig status (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-281">Marital status (required)</span></span>
- <span data-ttu-id="77ac4-282">Fødselsdato (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-282">Birth date (required)</span></span>
- <span data-ttu-id="77ac4-283">Køn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-283">Gender (required)</span></span>
- <span data-ttu-id="77ac4-284">Handicappet</span><span class="sxs-lookup"><span data-stu-id="77ac4-284">Person with disabilities</span></span>
- <span data-ttu-id="77ac4-285">Land eller område for nationalitet (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="77ac4-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="77ac4-286">Adresseoplysninger</span><span class="sxs-lookup"><span data-stu-id="77ac4-286">Address information</span></span>

- <span data-ttu-id="77ac4-287">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-287">Primary (required)</span></span>
- <span data-ttu-id="77ac4-288">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-288">Country/region (required)</span></span>
- <span data-ttu-id="77ac4-289">Postnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-289">Postal code (required)</span></span>
- <span data-ttu-id="77ac4-290">Gadenummer (påkrævet) (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="77ac4-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="77ac4-291">Bygningskomplement (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="77ac4-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="77ac4-292">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-292">City (required)</span></span>
- <span data-ttu-id="77ac4-293">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-293">State (required)</span></span>
- <span data-ttu-id="77ac4-294">Region (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="77ac4-295">Kontaktoplysninger</span><span class="sxs-lookup"><span data-stu-id="77ac4-295">Contact information</span></span> 

- <span data-ttu-id="77ac4-296">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-296">Primary (required)</span></span>
- <span data-ttu-id="77ac4-297">Kontaktpersonens nummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-297">Contact number (required)</span></span>
- <span data-ttu-id="77ac4-298">Forlængelse</span><span class="sxs-lookup"><span data-stu-id="77ac4-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="77ac4-299">Lønoplysninger og lønkoder</span><span class="sxs-lookup"><span data-stu-id="77ac4-299">Payroll information and earning codes</span></span>

<span data-ttu-id="77ac4-300">Medarbejdere kan tildeles en bestemt løn med en given betalingshyppighed og have en foretrukken betalingsmetode.</span><span class="sxs-lookup"><span data-stu-id="77ac4-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="77ac4-301">Følgende felter bruges i Dayforce til at sikre, at disse præferencer og indstillinger bruges.</span><span class="sxs-lookup"><span data-stu-id="77ac4-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="77ac4-302">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="77ac4-302">Earning codes</span></span>

- <span data-ttu-id="77ac4-303">Stilling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-303">Position (required)</span></span>
- <span data-ttu-id="77ac4-304">Lønkode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-304">Earning Code (required)</span></span>
- <span data-ttu-id="77ac4-305">Frekvens (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-305">Frequency (required)</span></span>
- <span data-ttu-id="77ac4-306">Beløb (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="77ac4-307">Lønoplysninger</span><span class="sxs-lookup"><span data-stu-id="77ac4-307">Payroll information</span></span>

- <span data-ttu-id="77ac4-308">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="77ac4-308">Payment Method</span></span>
- <span data-ttu-id="77ac4-309">Økonomisk område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-309">Economic Region (required)</span></span>
- <span data-ttu-id="77ac4-310">Id for medarbejderfrynsegoder</span><span class="sxs-lookup"><span data-stu-id="77ac4-310">Employee Benefits ID</span></span>
- <span data-ttu-id="77ac4-311">Nationalt id-nummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-311">National ID Number (required)</span></span>
- <span data-ttu-id="77ac4-312">Tjenestenummer hos militær</span><span class="sxs-lookup"><span data-stu-id="77ac4-312">Military Service Number</span></span>
- <span data-ttu-id="77ac4-313">Skifte-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-313">Shift ID (required)</span></span>
- <span data-ttu-id="77ac4-314">Skattenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-314">Tax Number (required)</span></span>
- <span data-ttu-id="77ac4-315">Fagforenings-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-315">Union ID (required)</span></span>
- <span data-ttu-id="77ac4-316">Arbejdsdags-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-316">Work Day ID (required)</span></span>
- <span data-ttu-id="77ac4-317">Arbejdstilladelsesnummer</span><span class="sxs-lookup"><span data-stu-id="77ac4-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="77ac4-318">For betalingsmetoden understøtter Mexico **Kontant**, **Check** (firmaets fysiske check), og **Elektronisk betaling**.</span><span class="sxs-lookup"><span data-stu-id="77ac4-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="77ac4-319">Hvis der ikke er angivet nogen betalingsmetode, bruges **Check** som standard.</span><span class="sxs-lookup"><span data-stu-id="77ac4-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="77ac4-320">Detaljer om ansættelse</span><span class="sxs-lookup"><span data-stu-id="77ac4-320">Employment details</span></span>

<span data-ttu-id="77ac4-321">Detaljeret ansættelseshistorik bruges som vigtige oplysninger til at udlede statusser for en medarbejders ansættelse, fratrædelse og genansættelse i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="77ac4-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="77ac4-322">Dayforce understøtter kun én aktiv ansættelsespost ad gangen.</span><span class="sxs-lookup"><span data-stu-id="77ac4-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="77ac4-323">Startdato for ansættelse (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-323">Employment start date (required)</span></span>
- <span data-ttu-id="77ac4-324">Slutdato for ansættelse</span><span class="sxs-lookup"><span data-stu-id="77ac4-324">Employment end date</span></span>
- <span data-ttu-id="77ac4-325">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="77ac4-325">Start date</span></span>
- <span data-ttu-id="77ac4-326">Justeret startdato</span><span class="sxs-lookup"><span data-stu-id="77ac4-326">Adjusted start date</span></span>
- <span data-ttu-id="77ac4-327">Fratrædelsesdato (kræves ved fratrædelse)</span><span class="sxs-lookup"><span data-stu-id="77ac4-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="77ac4-328">Fratrædelsesårsag (kræves ved fratrædelse)</span><span class="sxs-lookup"><span data-stu-id="77ac4-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="77ac4-329">Vigtige datoer for en medarbejders udledes ved hjælp af følgende oplysninger.</span><span class="sxs-lookup"><span data-stu-id="77ac4-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="77ac4-330">Talent</span><span class="sxs-lookup"><span data-stu-id="77ac4-330">Talent</span></span>                | <span data-ttu-id="77ac4-331">Dayforce</span><span class="sxs-lookup"><span data-stu-id="77ac4-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77ac4-332">Den seneste ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="77ac4-332">Most recent hire date</span></span> | <span data-ttu-id="77ac4-333">Historikpost for ansættelsesstart for aktuel ikke-afsluttet ansættelse</span><span class="sxs-lookup"><span data-stu-id="77ac4-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="77ac4-334">Fratrædelsesdato</span><span class="sxs-lookup"><span data-stu-id="77ac4-334">Termination date</span></span>      | <span data-ttu-id="77ac4-335">Historikpost for fratrædelsesdato for aktuel ikke-afsluttet ansættelse</span><span class="sxs-lookup"><span data-stu-id="77ac4-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="77ac4-336">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="77ac4-336">Start date</span></span>            | <span data-ttu-id="77ac4-337">Historikpost for justeret startdato, startdato eller startdato for ansættelse for aktuel ikke-aktiv ansættelse</span><span class="sxs-lookup"><span data-stu-id="77ac4-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="77ac4-338">Oprindelig ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="77ac4-338">Original hire date</span></span>    | <span data-ttu-id="77ac4-339">Historikpost for ansættelsesstart for tidligste ansættelse</span><span class="sxs-lookup"><span data-stu-id="77ac4-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="77ac4-340">Kompensation</span><span class="sxs-lookup"><span data-stu-id="77ac4-340">Compensation</span></span>

<span data-ttu-id="77ac4-341">En fast lønstruktur skal tilknyttes hver medarbejders primære stilling gennem hele ansættelsesperioden.</span><span class="sxs-lookup"><span data-stu-id="77ac4-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="77ac4-342">Denne periode starter på den dato, hvor medarbejderen blev ansat (eller ansættelsesstartdatoen) og fortsætter, indtil fratrædelsen.</span><span class="sxs-lookup"><span data-stu-id="77ac4-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="77ac4-343">Ikrafttrædelsesdato (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-343">Effective Date (required)</span></span>
- <span data-ttu-id="77ac4-344">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="77ac4-344">Expiration date</span></span>
- <span data-ttu-id="77ac4-345">Lønsats (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-345">Pay Rate (required)</span></span>
- <span data-ttu-id="77ac4-346">Konverteringer af lønsats (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="77ac4-347">Årlig ækvivalent (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="77ac4-348">Timebaseret ækvivalent (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="77ac4-349">Hvis en timeansat medarbejder har flere stillinger, indlæses den faste løn for den primære stilling i Dayforce, som basissats/-løn på medarbejderniveau.</span><span class="sxs-lookup"><span data-stu-id="77ac4-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="77ac4-350">For ikke-primære stillinger gemmes timesatsen i den tilsvarende position i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="77ac4-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="77ac4-351">Hvis en funktionær har flere stillinger, afledes den kumulative timesats og årlig gage på tværs af alle aktive stillinger og bruges som basissats/-gage på medarbejderniveau.</span><span class="sxs-lookup"><span data-stu-id="77ac4-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="77ac4-352">Identifikationsnumre</span><span class="sxs-lookup"><span data-stu-id="77ac4-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="77ac4-353">Social Security-identifikator</span><span class="sxs-lookup"><span data-stu-id="77ac4-353">Social Security identifier</span></span> 

<span data-ttu-id="77ac4-354">Alle medarbejdere skal have én primær identifikator.</span><span class="sxs-lookup"><span data-stu-id="77ac4-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="77ac4-355">Identifikatoren skal være af **SSN**-identifikationstypen</span><span class="sxs-lookup"><span data-stu-id="77ac4-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="77ac4-356">I Dayforce afledes den automatisk som medarbejderens Social Security-identifikator, der er påkrævet ved ansættelse.</span><span class="sxs-lookup"><span data-stu-id="77ac4-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="77ac4-357">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-357">Primary (required)</span></span>
- <span data-ttu-id="77ac4-358">Identifikationstype = "SSN"</span><span class="sxs-lookup"><span data-stu-id="77ac4-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="77ac4-359">Udstedt den</span><span class="sxs-lookup"><span data-stu-id="77ac4-359">Issued Date</span></span>
- <span data-ttu-id="77ac4-360">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="77ac4-360">Expiration Date</span></span>

<span data-ttu-id="77ac4-361">Medarbejdere kan angive flere identifikationsnumre af **SSN**-identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="77ac4-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="77ac4-362">Men det er kun den post, der er markeret som **Primær**, som er integreret i Dayforce, uanset om nummeret er aktivt eller udløbet.</span><span class="sxs-lookup"><span data-stu-id="77ac4-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="77ac4-363">Bankkonto og udbetalinger</span><span class="sxs-lookup"><span data-stu-id="77ac4-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="77ac4-364">Gyldige bankkontooplysninger skal angives for enhver medarbejder, der vælger at blive betalt via bankkontooverførsler.</span><span class="sxs-lookup"><span data-stu-id="77ac4-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="77ac4-365">Talent</span><span class="sxs-lookup"><span data-stu-id="77ac4-365">Talent</span></span>                         | <span data-ttu-id="77ac4-366">Dayforce</span><span class="sxs-lookup"><span data-stu-id="77ac4-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77ac4-367">Bankkontonummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="77ac4-368">SWIFT-kode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-368">SWIFT code (required)</span></span>          | <span data-ttu-id="77ac4-369">Feltet **Bank-id** bruges ved behandling af løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="77ac4-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="77ac4-370">Afdelingsnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="77ac4-371">Bankkontotype (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-371">Bank account type (required)</span></span>   | <span data-ttu-id="77ac4-372">Feltet **Kontotype** bruges ved behandling af løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="77ac4-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="77ac4-373">Understøttede værdier omfatter **Check** og **Løn**.</span><span class="sxs-lookup"><span data-stu-id="77ac4-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="77ac4-374">Medarbejdere, der vælger at betales via bankkontooverførsler, skal angive et link til en restbeløbskonto, der hører under en juridisk enhed, som har primær adresse i Mexico og er knyttet til en gyldig bankkonto fra en mexicansk bank.</span><span class="sxs-lookup"><span data-stu-id="77ac4-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="77ac4-375">Alle andre restbeløbskonti ignoreres.</span><span class="sxs-lookup"><span data-stu-id="77ac4-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="77ac4-376">Adresseoplysninger</span><span class="sxs-lookup"><span data-stu-id="77ac4-376">Address information</span></span>

<span data-ttu-id="77ac4-377">Alle medarbejdere skal have én primær placering.</span><span class="sxs-lookup"><span data-stu-id="77ac4-377">Every employee must have one primary location.</span></span> <span data-ttu-id="77ac4-378">I Dayforce bruges denne placering til at bestemme medarbejderens primære opholdssted til skattemæssige formål.</span><span class="sxs-lookup"><span data-stu-id="77ac4-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="77ac4-379">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-379">Primary (required)</span></span>
- <span data-ttu-id="77ac4-380">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-380">Country/region (required)</span></span>
- <span data-ttu-id="77ac4-381">Postnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="77ac4-382">Gade (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-382">Street (required)</span></span>
- <span data-ttu-id="77ac4-383">Gadenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-383">Street Number (required)</span></span>
- <span data-ttu-id="77ac4-384">Bygningskomplement</span><span class="sxs-lookup"><span data-stu-id="77ac4-384">Building Complement</span></span>
- <span data-ttu-id="77ac4-385">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-385">City (required)</span></span>
- <span data-ttu-id="77ac4-386">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-386">State (required)</span></span>
- <span data-ttu-id="77ac4-387">Region (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="77ac4-388">Konfigurere dataene for at generere løn i USA og Canada</span><span class="sxs-lookup"><span data-stu-id="77ac4-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="77ac4-389">Hvis du genererer løn for medarbejdere i USA og Canada, skal følgende elementer konfigureres:</span><span class="sxs-lookup"><span data-stu-id="77ac4-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="77ac4-390">Der kræves afdelinger til stillinger.</span><span class="sxs-lookup"><span data-stu-id="77ac4-390">Departments are required on positions.</span></span>
- <span data-ttu-id="77ac4-391">Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="77ac4-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="77ac4-392">Du kan konfigurere Talent til at kræve, at der angives en afdeling for stillinger.</span><span class="sxs-lookup"><span data-stu-id="77ac4-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="77ac4-393">For at gøre dette skal du gå til **Personalets delte stillinger > Stillinger > Kræv afdelinger for stillinger**.</span><span class="sxs-lookup"><span data-stu-id="77ac4-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="77ac4-394">Det anbefales, at denne indstilling gennemtvinges i forbindelse med integrationen.</span><span class="sxs-lookup"><span data-stu-id="77ac4-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="77ac4-395">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="77ac4-395">Job types</span></span>

<span data-ttu-id="77ac4-396">Jobtyper bruges til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="77ac4-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="77ac4-397">Jobtyper kræves for at behandle løn i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="77ac4-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="77ac4-398">Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="77ac4-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="77ac4-399">Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.</span><span class="sxs-lookup"><span data-stu-id="77ac4-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="77ac4-400">Der kræves følgende jobtyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="77ac4-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="77ac4-401">Jobtype</span><span class="sxs-lookup"><span data-stu-id="77ac4-401">Job type</span></span>   | <span data-ttu-id="77ac4-402">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="77ac4-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="77ac4-403">Pr. time</span><span class="sxs-lookup"><span data-stu-id="77ac4-403">Hourly</span></span>     | <span data-ttu-id="77ac4-404">Pr. time</span><span class="sxs-lookup"><span data-stu-id="77ac4-404">Hourly</span></span>      |
| <span data-ttu-id="77ac4-405">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="77ac4-405">Salaried</span></span>   | <span data-ttu-id="77ac4-406">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="77ac4-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="77ac4-407">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="77ac4-407">Position types</span></span> 

<span data-ttu-id="77ac4-408">Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet.</span><span class="sxs-lookup"><span data-stu-id="77ac4-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="77ac4-409">Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="77ac4-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="77ac4-410">Der kræves følgende stillingstyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="77ac4-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="77ac4-411">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="77ac4-411">Position type</span></span>   | <span data-ttu-id="77ac4-412">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="77ac4-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="77ac4-413">Fuld tid</span><span class="sxs-lookup"><span data-stu-id="77ac4-413">Full-time</span></span>       | <span data-ttu-id="77ac4-414">Fuldtidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="77ac4-414">Full time employee</span></span> |
| <span data-ttu-id="77ac4-415">Deltid</span><span class="sxs-lookup"><span data-stu-id="77ac4-415">Part-time</span></span>       | <span data-ttu-id="77ac4-416">Deltidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="77ac4-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="77ac4-417">Årsagskoder</span><span class="sxs-lookup"><span data-stu-id="77ac4-417">Reason codes</span></span>

<span data-ttu-id="77ac4-418">Årsagskoder indeholder oplysninger om status for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="77ac4-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="77ac4-419">Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.</span><span class="sxs-lookup"><span data-stu-id="77ac4-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="77ac4-420">Der kræves følgende årsagskoder og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="77ac4-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="77ac4-421">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="77ac4-421">Reason code</span></span>    | <span data-ttu-id="77ac4-422">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="77ac4-422">Description</span></span>      | <span data-ttu-id="77ac4-423">Anvendelige scenarier</span><span class="sxs-lookup"><span data-stu-id="77ac4-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="77ac4-424">OPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="77ac4-424">RESIGNATION</span></span>    | <span data-ttu-id="77ac4-425">Opsigelse</span><span class="sxs-lookup"><span data-stu-id="77ac4-425">Resignation</span></span>      | <span data-ttu-id="77ac4-426">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="77ac4-426">Terminate worker</span></span>     |
| <span data-ttu-id="77ac4-427">OPHØR</span><span class="sxs-lookup"><span data-stu-id="77ac4-427">TERMINATION</span></span>    | <span data-ttu-id="77ac4-428">Ophør</span><span class="sxs-lookup"><span data-stu-id="77ac4-428">Termination</span></span>      | <span data-ttu-id="77ac4-429">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="77ac4-429">Terminate worker</span></span>     |
| <span data-ttu-id="77ac4-430">PENSION</span><span class="sxs-lookup"><span data-stu-id="77ac4-430">RETIREMENT</span></span>     | <span data-ttu-id="77ac4-431">Pension</span><span class="sxs-lookup"><span data-stu-id="77ac4-431">Retirement</span></span>       | <span data-ttu-id="77ac4-432">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="77ac4-432">Terminate worker</span></span>     |
| <span data-ttu-id="77ac4-433">ANDET</span><span class="sxs-lookup"><span data-stu-id="77ac4-433">OTHER</span></span>          | <span data-ttu-id="77ac4-434">Andre årsager</span><span class="sxs-lookup"><span data-stu-id="77ac4-434">Other Reasons</span></span>    | <span data-ttu-id="77ac4-435">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="77ac4-435">Terminate worker</span></span>     |
| <span data-ttu-id="77ac4-436">DØDSFALD</span><span class="sxs-lookup"><span data-stu-id="77ac4-436">DEATH</span></span>          | <span data-ttu-id="77ac4-437">Dødsfald</span><span class="sxs-lookup"><span data-stu-id="77ac4-437">Death</span></span>            | <span data-ttu-id="77ac4-438">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="77ac4-438">Terminate worker</span></span>     |
| <span data-ttu-id="77ac4-439">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="77ac4-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="77ac4-440">Orlov</span><span class="sxs-lookup"><span data-stu-id="77ac4-440">Leave of Absence</span></span> | <span data-ttu-id="77ac4-441">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="77ac4-441">Terminate worker</span></span>     |
| <span data-ttu-id="77ac4-442">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="77ac4-442">CONTRACTEND</span></span>    | <span data-ttu-id="77ac4-443">Kontraktudløb</span><span class="sxs-lookup"><span data-stu-id="77ac4-443">End of Contract</span></span>  | <span data-ttu-id="77ac4-444">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="77ac4-444">Terminate worker</span></span>     |
| <span data-ttu-id="77ac4-445">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="77ac4-445">SALARYCHANGE</span></span>   | <span data-ttu-id="77ac4-446">Ændring af løn</span><span class="sxs-lookup"><span data-stu-id="77ac4-446">Change of Salary</span></span> | <span data-ttu-id="77ac4-447">Kompensation</span><span class="sxs-lookup"><span data-stu-id="77ac4-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="77ac4-448">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="77ac4-448">Marital status</span></span>

<span data-ttu-id="77ac4-449">Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="77ac4-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="77ac4-450">Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="77ac4-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="77ac4-451">Talent</span><span class="sxs-lookup"><span data-stu-id="77ac4-451">Talent</span></span>                 | <span data-ttu-id="77ac4-452">Dayforce</span><span class="sxs-lookup"><span data-stu-id="77ac4-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="77ac4-453">Gift</span><span class="sxs-lookup"><span data-stu-id="77ac4-453">Married</span></span>                | <span data-ttu-id="77ac4-454">Gift</span><span class="sxs-lookup"><span data-stu-id="77ac4-454">Married</span></span>              |
| <span data-ttu-id="77ac4-455">Enlig</span><span class="sxs-lookup"><span data-stu-id="77ac4-455">Single</span></span>                 | <span data-ttu-id="77ac4-456">Enlig</span><span class="sxs-lookup"><span data-stu-id="77ac4-456">Single</span></span>               |
| <span data-ttu-id="77ac4-457">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="77ac4-457">Widowed</span></span>                | <span data-ttu-id="77ac4-458">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="77ac4-458">Widowed</span></span>              |
| <span data-ttu-id="77ac4-459">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="77ac4-459">Divorced</span></span>               | <span data-ttu-id="77ac4-460">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="77ac4-460">Divorced</span></span>             |
| <span data-ttu-id="77ac4-461">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="77ac4-461">Registered Partnership</span></span> | <span data-ttu-id="77ac4-462">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="77ac4-462">Domestic Partnership</span></span> |
| <span data-ttu-id="77ac4-463">None</span><span class="sxs-lookup"><span data-stu-id="77ac4-463">None</span></span>                   | <span data-ttu-id="77ac4-464">None</span><span class="sxs-lookup"><span data-stu-id="77ac4-464">None</span></span>                 |
| <span data-ttu-id="77ac4-465">Samlever</span><span class="sxs-lookup"><span data-stu-id="77ac4-465">Cohabiting</span></span>             | <span data-ttu-id="77ac4-466">Samlever</span><span class="sxs-lookup"><span data-stu-id="77ac4-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="77ac4-467">Køn</span><span class="sxs-lookup"><span data-stu-id="77ac4-467">Gender</span></span>

<span data-ttu-id="77ac4-468">Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="77ac4-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="77ac4-469">Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="77ac4-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="77ac4-470">Talent</span><span class="sxs-lookup"><span data-stu-id="77ac4-470">Talent</span></span>       | <span data-ttu-id="77ac4-471">Dayforce</span><span class="sxs-lookup"><span data-stu-id="77ac4-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="77ac4-472">Mand</span><span class="sxs-lookup"><span data-stu-id="77ac4-472">Male</span></span>         | <span data-ttu-id="77ac4-473">Mand</span><span class="sxs-lookup"><span data-stu-id="77ac4-473">Male</span></span>            |
| <span data-ttu-id="77ac4-474">Kvinde</span><span class="sxs-lookup"><span data-stu-id="77ac4-474">Female</span></span>       | <span data-ttu-id="77ac4-475">Kvinde</span><span class="sxs-lookup"><span data-stu-id="77ac4-475">Female</span></span>          |
| <span data-ttu-id="77ac4-476">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="77ac4-476">Non-specific</span></span> | <span data-ttu-id="77ac4-477">*Understøttes ikke*</span><span class="sxs-lookup"><span data-stu-id="77ac4-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="77ac4-478">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="77ac4-478">Earning codes</span></span>

<span data-ttu-id="77ac4-479">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="77ac4-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="77ac4-480">Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="77ac4-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="77ac4-481">Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="77ac4-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="77ac4-482">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="77ac4-482">Supported frequencies</span></span>

- <span data-ttu-id="77ac4-483">Alt</span><span class="sxs-lookup"><span data-stu-id="77ac4-483">All</span></span>
- <span data-ttu-id="77ac4-484">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="77ac4-484">EVERYPAY</span></span>
- <span data-ttu-id="77ac4-485">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="77ac4-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="77ac4-486">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="77ac4-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="77ac4-487">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="77ac4-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="77ac4-488">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-488">1OFMTH</span></span>
- <span data-ttu-id="77ac4-489">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-489">LASTOFMTH</span></span>
- <span data-ttu-id="77ac4-490">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-490">2OFMTH</span></span>
- <span data-ttu-id="77ac4-491">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-491">3OFMTH</span></span>
- <span data-ttu-id="77ac4-492">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-492">4OFMTH</span></span>
- <span data-ttu-id="77ac4-493">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-493">5OFMTH</span></span>
- <span data-ttu-id="77ac4-494">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-494">1N2OFMTH</span></span>
- <span data-ttu-id="77ac4-495">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-495">3N4OFMTH</span></span>
- <span data-ttu-id="77ac4-496">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-496">1N3OFMTH</span></span>
- <span data-ttu-id="77ac4-497">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-497">1N4OFMTH</span></span>
- <span data-ttu-id="77ac4-498">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-498">2N3OFMTH</span></span>
- <span data-ttu-id="77ac4-499">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-499">2N4OFMTH</span></span>
- <span data-ttu-id="77ac4-500">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="77ac4-501">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="77ac4-502">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="77ac4-503">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="77ac4-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="77ac4-505">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="77ac4-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="77ac4-506">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="77ac4-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="77ac4-507">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="77ac4-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="77ac4-508">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="77ac4-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="77ac4-509">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="77ac4-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="77ac4-510">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="77ac4-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="77ac4-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="77ac4-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="77ac4-512">Adresser</span><span class="sxs-lookup"><span data-stu-id="77ac4-512">Addresses</span></span>

<span data-ttu-id="77ac4-513">Identifikation af specifikke koder for land eller region, stat og område (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende.</span><span class="sxs-lookup"><span data-stu-id="77ac4-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="77ac4-514">Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.</span><span class="sxs-lookup"><span data-stu-id="77ac4-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="77ac4-515">Talent</span><span class="sxs-lookup"><span data-stu-id="77ac4-515">Talent</span></span>          | <span data-ttu-id="77ac4-516">Dayforce</span><span class="sxs-lookup"><span data-stu-id="77ac4-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="77ac4-517">Land/område</span><span class="sxs-lookup"><span data-stu-id="77ac4-517">Country/Region</span></span>  | <span data-ttu-id="77ac4-518">Landekode</span><span class="sxs-lookup"><span data-stu-id="77ac4-518">Country Code</span></span>          |
| <span data-ttu-id="77ac4-519">Postnummer</span><span class="sxs-lookup"><span data-stu-id="77ac4-519">Zip/Postal Code</span></span> | <span data-ttu-id="77ac4-520">Postnummer</span><span class="sxs-lookup"><span data-stu-id="77ac4-520">Postal Code</span></span>           |
| <span data-ttu-id="77ac4-521">Status</span><span class="sxs-lookup"><span data-stu-id="77ac4-521">State</span></span>           | <span data-ttu-id="77ac4-522">Statskode</span><span class="sxs-lookup"><span data-stu-id="77ac4-522">State Code</span></span>            |
| <span data-ttu-id="77ac4-523">Bynavn</span><span class="sxs-lookup"><span data-stu-id="77ac4-523">City</span></span>            | <span data-ttu-id="77ac4-524">Bynavn</span><span class="sxs-lookup"><span data-stu-id="77ac4-524">City</span></span>                  |
| <span data-ttu-id="77ac4-525">Region</span><span class="sxs-lookup"><span data-stu-id="77ac4-525">County</span></span>          | <span data-ttu-id="77ac4-526">Område (kommune)</span><span class="sxs-lookup"><span data-stu-id="77ac4-526">County (Municipality)</span></span> |
| <span data-ttu-id="77ac4-527">Gade</span><span class="sxs-lookup"><span data-stu-id="77ac4-527">Street</span></span>          | <span data-ttu-id="77ac4-528">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="77ac4-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="77ac4-529">Skatteområder</span><span class="sxs-lookup"><span data-stu-id="77ac4-529">Tax regions</span></span>

<span data-ttu-id="77ac4-530">Skatteområder bruges til at bestemme den relevante skat, der skal anvendes ved løngenerering.</span><span class="sxs-lookup"><span data-stu-id="77ac4-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="77ac4-531">Skatteområder er tilknyttet Dayforce som placeringsadresser.</span><span class="sxs-lookup"><span data-stu-id="77ac4-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="77ac4-532">Standardskatteområder skal knyttes til arbejderens aktive stilling.</span><span class="sxs-lookup"><span data-stu-id="77ac4-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="77ac4-533">Skatteområde (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-533">Tax region (required)</span></span>
- <span data-ttu-id="77ac4-534">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-534">Country/Region (required)</span></span>
- <span data-ttu-id="77ac4-535">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-535">State (required)</span></span>
- <span data-ttu-id="77ac4-536">Region</span><span class="sxs-lookup"><span data-stu-id="77ac4-536">County</span></span> 
- <span data-ttu-id="77ac4-537">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="77ac4-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="77ac4-538">Konfigurere dataene for at generere løn i Mexico</span><span class="sxs-lookup"><span data-stu-id="77ac4-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="77ac4-539">Hvis du genererer løn for medarbejdere i Mexico skal følgende elementer konfigureres:</span><span class="sxs-lookup"><span data-stu-id="77ac4-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="77ac4-540">Der kræves afdelinger til stillinger.</span><span class="sxs-lookup"><span data-stu-id="77ac4-540">Departments are required on positions.</span></span>
- <span data-ttu-id="77ac4-541">Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="77ac4-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="77ac4-542">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="77ac4-542">Job types</span></span>

<span data-ttu-id="77ac4-543">Jobtyper bruges til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="77ac4-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="77ac4-544">Jobtyper kræves for at behandle løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="77ac4-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="77ac4-545">Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="77ac4-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="77ac4-546">Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.</span><span class="sxs-lookup"><span data-stu-id="77ac4-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="77ac4-547">Der kræves følgende jobtyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="77ac4-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="77ac4-548">Jobtype</span><span class="sxs-lookup"><span data-stu-id="77ac4-548">Job type</span></span>   | <span data-ttu-id="77ac4-549">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="77ac4-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="77ac4-550">Pr. time</span><span class="sxs-lookup"><span data-stu-id="77ac4-550">Hourly</span></span>     | <span data-ttu-id="77ac4-551">MX Pr. time</span><span class="sxs-lookup"><span data-stu-id="77ac4-551">MX Hourly</span></span>   |
| <span data-ttu-id="77ac4-552">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="77ac4-552">Salaried</span></span>   | <span data-ttu-id="77ac4-553">MX Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="77ac4-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="77ac4-554">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="77ac4-554">Position types</span></span> 

<span data-ttu-id="77ac4-555">Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet.</span><span class="sxs-lookup"><span data-stu-id="77ac4-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="77ac4-556">Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="77ac4-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="77ac4-557">Der kræves følgende stillingstyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="77ac4-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="77ac4-558">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="77ac4-558">Position type</span></span>   | <span data-ttu-id="77ac4-559">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="77ac4-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="77ac4-560">Fuld tid</span><span class="sxs-lookup"><span data-stu-id="77ac4-560">Full-time</span></span>       | <span data-ttu-id="77ac4-561">Fuldtidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="77ac4-561">Full time employee</span></span> |
| <span data-ttu-id="77ac4-562">Deltid</span><span class="sxs-lookup"><span data-stu-id="77ac4-562">Part-time</span></span>       | <span data-ttu-id="77ac4-563">Deltidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="77ac4-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="77ac4-564">Årsagskoder</span><span class="sxs-lookup"><span data-stu-id="77ac4-564">Reason codes</span></span>

<span data-ttu-id="77ac4-565">Årsagskoder indeholder oplysninger om status for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="77ac4-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="77ac4-566">Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.</span><span class="sxs-lookup"><span data-stu-id="77ac4-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="77ac4-567">Der kræves følgende årsagskoder og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="77ac4-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="77ac4-568">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="77ac4-568">Reason code</span></span>            | <span data-ttu-id="77ac4-569">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="77ac4-569">Description</span></span>                    | <span data-ttu-id="77ac4-570">Anvendelige scenarier</span><span class="sxs-lookup"><span data-stu-id="77ac4-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="77ac4-571">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="77ac4-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="77ac4-572">Afgang før første løn</span><span class="sxs-lookup"><span data-stu-id="77ac4-572">Departure before first payroll</span></span> | <span data-ttu-id="77ac4-573">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="77ac4-573">Terminate worker</span></span>     |
| <span data-ttu-id="77ac4-574">OPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="77ac4-574">RESIGNATION</span></span>            | <span data-ttu-id="77ac4-575">Opsigelse</span><span class="sxs-lookup"><span data-stu-id="77ac4-575">Resignation</span></span>                    | <span data-ttu-id="77ac4-576">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="77ac4-576">Terminate worker</span></span>     |
| <span data-ttu-id="77ac4-577">PENSION</span><span class="sxs-lookup"><span data-stu-id="77ac4-577">PENSION</span></span>                | <span data-ttu-id="77ac4-578">Pension</span><span class="sxs-lookup"><span data-stu-id="77ac4-578">Pension</span></span>                        | <span data-ttu-id="77ac4-579">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="77ac4-579">Terminate worker</span></span>     |
| <span data-ttu-id="77ac4-580">OPHØR</span><span class="sxs-lookup"><span data-stu-id="77ac4-580">TERMINATION</span></span>            | <span data-ttu-id="77ac4-581">Ophør</span><span class="sxs-lookup"><span data-stu-id="77ac4-581">Termination</span></span>                    | <span data-ttu-id="77ac4-582">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="77ac4-582">Terminate worker</span></span>     |
| <span data-ttu-id="77ac4-583">PENSION</span><span class="sxs-lookup"><span data-stu-id="77ac4-583">RETIREMENT</span></span>             | <span data-ttu-id="77ac4-584">Pension</span><span class="sxs-lookup"><span data-stu-id="77ac4-584">Retirement</span></span>                     | <span data-ttu-id="77ac4-585">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="77ac4-585">Terminate worker</span></span>     |
| <span data-ttu-id="77ac4-586">FRAVÆRENDE</span><span class="sxs-lookup"><span data-stu-id="77ac4-586">ABSENTEE</span></span>               | <span data-ttu-id="77ac4-587">Fraværende</span><span class="sxs-lookup"><span data-stu-id="77ac4-587">Absentee</span></span>                       | <span data-ttu-id="77ac4-588">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="77ac4-588">Terminate worker</span></span>     |
| <span data-ttu-id="77ac4-589">ANDET</span><span class="sxs-lookup"><span data-stu-id="77ac4-589">OTHER</span></span>                  | <span data-ttu-id="77ac4-590">Andre årsager</span><span class="sxs-lookup"><span data-stu-id="77ac4-590">Other Reasons</span></span>                  | <span data-ttu-id="77ac4-591">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="77ac4-591">Terminate worker</span></span>     |
| <span data-ttu-id="77ac4-592">LUKNING</span><span class="sxs-lookup"><span data-stu-id="77ac4-592">CLOSURE</span></span>                | <span data-ttu-id="77ac4-593">Virksomhedslukning</span><span class="sxs-lookup"><span data-stu-id="77ac4-593">Business Closure</span></span>               | <span data-ttu-id="77ac4-594">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="77ac4-594">Terminate worker</span></span>     |
| <span data-ttu-id="77ac4-595">DØDSFALD</span><span class="sxs-lookup"><span data-stu-id="77ac4-595">DEATH</span></span>                  | <span data-ttu-id="77ac4-596">Dødsfald</span><span class="sxs-lookup"><span data-stu-id="77ac4-596">Death</span></span>                          | <span data-ttu-id="77ac4-597">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="77ac4-597">Terminate worker</span></span>     |
| <span data-ttu-id="77ac4-598">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="77ac4-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="77ac4-599">Orlov</span><span class="sxs-lookup"><span data-stu-id="77ac4-599">Leave of Absence</span></span>               | <span data-ttu-id="77ac4-600">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="77ac4-600">Terminate worker</span></span>     |
| <span data-ttu-id="77ac4-601">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="77ac4-601">CONTRACTEND</span></span>            | <span data-ttu-id="77ac4-602">Kontraktudløb</span><span class="sxs-lookup"><span data-stu-id="77ac4-602">End of Contract</span></span>                | <span data-ttu-id="77ac4-603">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="77ac4-603">Terminate worker</span></span>     |
| <span data-ttu-id="77ac4-604">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="77ac4-604">SALARYCHANGE</span></span>           | <span data-ttu-id="77ac4-605">Ændring af løn</span><span class="sxs-lookup"><span data-stu-id="77ac4-605">Change of Salary</span></span>               | <span data-ttu-id="77ac4-606">Kompensation</span><span class="sxs-lookup"><span data-stu-id="77ac4-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="77ac4-607">Ansættelsesvilkår</span><span class="sxs-lookup"><span data-stu-id="77ac4-607">Terms of employment</span></span>

<span data-ttu-id="77ac4-608">Ansættelsesvilkår bruges til at oprette kategorier for ansættelsesvilkår.</span><span class="sxs-lookup"><span data-stu-id="77ac4-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="77ac4-609">Vilkårene knyttes til Dayforce som beskæftigelsesindikatorværdier.</span><span class="sxs-lookup"><span data-stu-id="77ac4-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="77ac4-610">Følgende begreber for beskæftigelse og beskrivelser er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="77ac4-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="77ac4-611">Ansættelsesvilkår</span><span class="sxs-lookup"><span data-stu-id="77ac4-611">Terms of employment</span></span>   | <span data-ttu-id="77ac4-612">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="77ac4-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="77ac4-613">Regulær</span><span class="sxs-lookup"><span data-stu-id="77ac4-613">Regular</span></span>               | <span data-ttu-id="77ac4-614">Regulær</span><span class="sxs-lookup"><span data-stu-id="77ac4-614">Regular</span></span>     |
| <span data-ttu-id="77ac4-615">Direkte</span><span class="sxs-lookup"><span data-stu-id="77ac4-615">Direct</span></span>                | <span data-ttu-id="77ac4-616">Direkte</span><span class="sxs-lookup"><span data-stu-id="77ac4-616">Direct</span></span>      |
| <span data-ttu-id="77ac4-617">Turnustjeneste</span><span class="sxs-lookup"><span data-stu-id="77ac4-617">Internship</span></span>            | <span data-ttu-id="77ac4-618">Turnustjeneste</span><span class="sxs-lookup"><span data-stu-id="77ac4-618">Internship</span></span>  |
| <span data-ttu-id="77ac4-619">Permanent</span><span class="sxs-lookup"><span data-stu-id="77ac4-619">Permanent</span></span>             | <span data-ttu-id="77ac4-620">Permanent</span><span class="sxs-lookup"><span data-stu-id="77ac4-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="77ac4-621">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="77ac4-621">Marital status</span></span>

<span data-ttu-id="77ac4-622">Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="77ac4-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="77ac4-623">Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="77ac4-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="77ac4-624">Talent</span><span class="sxs-lookup"><span data-stu-id="77ac4-624">Talent</span></span>                 | <span data-ttu-id="77ac4-625">Dayforce</span><span class="sxs-lookup"><span data-stu-id="77ac4-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="77ac4-626">Gift</span><span class="sxs-lookup"><span data-stu-id="77ac4-626">Married</span></span>                | <span data-ttu-id="77ac4-627">Gift</span><span class="sxs-lookup"><span data-stu-id="77ac4-627">Married</span></span>                   |
| <span data-ttu-id="77ac4-628">Enlig</span><span class="sxs-lookup"><span data-stu-id="77ac4-628">Single</span></span>                 | <span data-ttu-id="77ac4-629">Enlig</span><span class="sxs-lookup"><span data-stu-id="77ac4-629">Single</span></span>                    |
| <span data-ttu-id="77ac4-630">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="77ac4-630">Widowed</span></span>                | <span data-ttu-id="77ac4-631">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="77ac4-631">Widowed</span></span>                   |
| <span data-ttu-id="77ac4-632">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="77ac4-632">Divorced</span></span>               | <span data-ttu-id="77ac4-633">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="77ac4-633">Divorced</span></span>                  |
| <span data-ttu-id="77ac4-634">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="77ac4-634">Registered Partnership</span></span> | <span data-ttu-id="77ac4-635">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="77ac4-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="77ac4-636">None</span><span class="sxs-lookup"><span data-stu-id="77ac4-636">None</span></span>                   | <span data-ttu-id="77ac4-637">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="77ac4-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="77ac4-638">Samlever</span><span class="sxs-lookup"><span data-stu-id="77ac4-638">Cohabiting</span></span>             | <span data-ttu-id="77ac4-639">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="77ac4-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="77ac4-640">Køn</span><span class="sxs-lookup"><span data-stu-id="77ac4-640">Gender</span></span>

<span data-ttu-id="77ac4-641">Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="77ac4-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="77ac4-642">Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="77ac4-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="77ac4-643">Talent</span><span class="sxs-lookup"><span data-stu-id="77ac4-643">Talent</span></span>       | <span data-ttu-id="77ac4-644">Dayforce</span><span class="sxs-lookup"><span data-stu-id="77ac4-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="77ac4-645">Mand</span><span class="sxs-lookup"><span data-stu-id="77ac4-645">Male</span></span>         | <span data-ttu-id="77ac4-646">Mand</span><span class="sxs-lookup"><span data-stu-id="77ac4-646">Male</span></span>                      |
| <span data-ttu-id="77ac4-647">Kvinde</span><span class="sxs-lookup"><span data-stu-id="77ac4-647">Female</span></span>       | <span data-ttu-id="77ac4-648">Kvinde</span><span class="sxs-lookup"><span data-stu-id="77ac4-648">Female</span></span>                    |
| <span data-ttu-id="77ac4-649">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="77ac4-649">Non-specific</span></span> | <span data-ttu-id="77ac4-650">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="77ac4-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="77ac4-651">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="77ac4-651">Payment method</span></span>

<span data-ttu-id="77ac4-652">Betalingsmetoder giver medarbejderen og virksomheden en måde til at beskrive, hvordan medarbejdere skal betales.</span><span class="sxs-lookup"><span data-stu-id="77ac4-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="77ac4-653">Betalingsmåder knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="77ac4-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="77ac4-654">Følgende tabel viser, hvordan betalingsmetoder knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="77ac4-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="77ac4-655">Talent</span><span class="sxs-lookup"><span data-stu-id="77ac4-655">Talent</span></span>             | <span data-ttu-id="77ac4-656">Dayforce</span><span class="sxs-lookup"><span data-stu-id="77ac4-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="77ac4-657">Indløsning</span><span class="sxs-lookup"><span data-stu-id="77ac4-657">Cash</span></span>               | <span data-ttu-id="77ac4-658">Indløsning</span><span class="sxs-lookup"><span data-stu-id="77ac4-658">Cash</span></span>                      |
| <span data-ttu-id="77ac4-659">Elektronisk betaling</span><span class="sxs-lookup"><span data-stu-id="77ac4-659">Electronic Payment</span></span> | <span data-ttu-id="77ac4-660">Ompostering</span><span class="sxs-lookup"><span data-stu-id="77ac4-660">Transfer</span></span>                  |
| <span data-ttu-id="77ac4-661">Check</span><span class="sxs-lookup"><span data-stu-id="77ac4-661">Check</span></span>              | <span data-ttu-id="77ac4-662">Check</span><span class="sxs-lookup"><span data-stu-id="77ac4-662">Cheque</span></span>                    |
| <span data-ttu-id="77ac4-663">Bankanvisning</span><span class="sxs-lookup"><span data-stu-id="77ac4-663">Bank Draft</span></span>         | <span data-ttu-id="77ac4-664">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="77ac4-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="77ac4-665">Andre</span><span class="sxs-lookup"><span data-stu-id="77ac4-665">Other</span></span>              | <span data-ttu-id="77ac4-666">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="77ac4-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="77ac4-667">Bankkontotype</span><span class="sxs-lookup"><span data-stu-id="77ac4-667">Bank account type</span></span>

<span data-ttu-id="77ac4-668">Bankkontotyper bruges til elektroniske betalinger til medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="77ac4-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="77ac4-669">Bankkontotyper knyttes til Dayforce som overførselskontooplysninger.</span><span class="sxs-lookup"><span data-stu-id="77ac4-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="77ac4-670">Bankkontotyperne oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="77ac4-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="77ac4-671">Talent</span><span class="sxs-lookup"><span data-stu-id="77ac4-671">Talent</span></span>            | <span data-ttu-id="77ac4-672">Dayforce</span><span class="sxs-lookup"><span data-stu-id="77ac4-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="77ac4-673">Checkkonto</span><span class="sxs-lookup"><span data-stu-id="77ac4-673">Checking Account</span></span>  | <span data-ttu-id="77ac4-674">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="77ac4-674">CheckingAccount</span></span>           |
| <span data-ttu-id="77ac4-675">Lønkonto</span><span class="sxs-lookup"><span data-stu-id="77ac4-675">Payroll Account</span></span>   | <span data-ttu-id="77ac4-676">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="77ac4-676">PayrollAccount</span></span>            |
| <span data-ttu-id="77ac4-677">Opsparingskonto</span><span class="sxs-lookup"><span data-stu-id="77ac4-677">Savings Account</span></span>   | <span data-ttu-id="77ac4-678">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="77ac4-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="77ac4-679">BankGirot-konto</span><span class="sxs-lookup"><span data-stu-id="77ac4-679">BankGirot account</span></span> | <span data-ttu-id="77ac4-680">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="77ac4-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="77ac4-681">PlusGirot-konto</span><span class="sxs-lookup"><span data-stu-id="77ac4-681">PlusGirot account</span></span> | <span data-ttu-id="77ac4-682">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="77ac4-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="77ac4-683">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="77ac4-683">Earning codes</span></span>

<span data-ttu-id="77ac4-684">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="77ac4-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="77ac4-685">Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="77ac4-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="77ac4-686">Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="77ac4-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="77ac4-687">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="77ac4-687">Supported frequencies</span></span>

- <span data-ttu-id="77ac4-688">Alt</span><span class="sxs-lookup"><span data-stu-id="77ac4-688">All</span></span>
- <span data-ttu-id="77ac4-689">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="77ac4-689">EVERYPAY</span></span>
- <span data-ttu-id="77ac4-690">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="77ac4-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="77ac4-691">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="77ac4-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="77ac4-692">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="77ac4-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="77ac4-693">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-693">1OFMTH</span></span>
- <span data-ttu-id="77ac4-694">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-694">LASTOFMTH</span></span>
- <span data-ttu-id="77ac4-695">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-695">2OFMTH</span></span>
- <span data-ttu-id="77ac4-696">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-696">3OFMTH</span></span>
- <span data-ttu-id="77ac4-697">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-697">4OFMTH</span></span>
- <span data-ttu-id="77ac4-698">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-698">5OFMTH</span></span>
- <span data-ttu-id="77ac4-699">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-699">1N2OFMTH</span></span>
- <span data-ttu-id="77ac4-700">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-700">3N4OFMTH</span></span>
- <span data-ttu-id="77ac4-701">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-701">1N3OFMTH</span></span>
- <span data-ttu-id="77ac4-702">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-702">1N4OFMTH</span></span>
- <span data-ttu-id="77ac4-703">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-703">2N3OFMTH</span></span>
- <span data-ttu-id="77ac4-704">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-704">2N4OFMTH</span></span>
- <span data-ttu-id="77ac4-705">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="77ac4-706">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="77ac4-707">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="77ac4-708">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="77ac4-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77ac4-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="77ac4-710">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="77ac4-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="77ac4-711">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="77ac4-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="77ac4-712">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="77ac4-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="77ac4-713">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="77ac4-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="77ac4-714">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="77ac4-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="77ac4-715">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="77ac4-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="77ac4-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="77ac4-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="77ac4-717">Adresser</span><span class="sxs-lookup"><span data-stu-id="77ac4-717">Addresses</span></span>

<span data-ttu-id="77ac4-718">Identifikation af specifikke koder for land eller region, stat og område (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende.</span><span class="sxs-lookup"><span data-stu-id="77ac4-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="77ac4-719">Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.</span><span class="sxs-lookup"><span data-stu-id="77ac4-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="77ac4-720">Talent</span><span class="sxs-lookup"><span data-stu-id="77ac4-720">Talent</span></span>              | <span data-ttu-id="77ac4-721">Dayforce</span><span class="sxs-lookup"><span data-stu-id="77ac4-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="77ac4-722">Land/område</span><span class="sxs-lookup"><span data-stu-id="77ac4-722">Country/Region</span></span>      | <span data-ttu-id="77ac4-723">Landekode</span><span class="sxs-lookup"><span data-stu-id="77ac4-723">Country Code</span></span>          |
| <span data-ttu-id="77ac4-724">Postnummer</span><span class="sxs-lookup"><span data-stu-id="77ac4-724">Zip/Postal Code</span></span>     | <span data-ttu-id="77ac4-725">Postnummer</span><span class="sxs-lookup"><span data-stu-id="77ac4-725">Postal Code</span></span>           |
| <span data-ttu-id="77ac4-726">Status</span><span class="sxs-lookup"><span data-stu-id="77ac4-726">State</span></span>               | <span data-ttu-id="77ac4-727">Statskode</span><span class="sxs-lookup"><span data-stu-id="77ac4-727">State Code</span></span>            |
| <span data-ttu-id="77ac4-728">Bynavn</span><span class="sxs-lookup"><span data-stu-id="77ac4-728">City</span></span>                | <span data-ttu-id="77ac4-729">Bynavn</span><span class="sxs-lookup"><span data-stu-id="77ac4-729">City</span></span>                  |
| <span data-ttu-id="77ac4-730">Region</span><span class="sxs-lookup"><span data-stu-id="77ac4-730">County</span></span>              | <span data-ttu-id="77ac4-731">Område (kommune)</span><span class="sxs-lookup"><span data-stu-id="77ac4-731">County (Municipality)</span></span> |
| <span data-ttu-id="77ac4-732">Gade</span><span class="sxs-lookup"><span data-stu-id="77ac4-732">Street</span></span>              | <span data-ttu-id="77ac4-733">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="77ac4-733">Address Line 1</span></span>        |
| <span data-ttu-id="77ac4-734">Gadenummer</span><span class="sxs-lookup"><span data-stu-id="77ac4-734">Street Number</span></span>       | <span data-ttu-id="77ac4-735">Adresselinje 2</span><span class="sxs-lookup"><span data-stu-id="77ac4-735">Address Line 2</span></span>        |
| <span data-ttu-id="77ac4-736">Bygningskomplement</span><span class="sxs-lookup"><span data-stu-id="77ac4-736">Building Complement</span></span> | <span data-ttu-id="77ac4-737">Adresselinje 5</span><span class="sxs-lookup"><span data-stu-id="77ac4-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="77ac4-738">Pasnummer</span><span class="sxs-lookup"><span data-stu-id="77ac4-738">Passport number</span></span>

<span data-ttu-id="77ac4-739">Medarbejdere kan erklære pasoplysninger.</span><span class="sxs-lookup"><span data-stu-id="77ac4-739">Employees can declare passport information.</span></span> <span data-ttu-id="77ac4-740">Disse oplysninger er af identifikationstypen **Pas** og er integreret i Dayforce som en del af en medarbejders Mexico-specifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="77ac4-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="77ac4-741">Identifikationstype = "Pas"</span><span class="sxs-lookup"><span data-stu-id="77ac4-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="77ac4-742">Udstedt den</span><span class="sxs-lookup"><span data-stu-id="77ac4-742">Issued Date</span></span>
- <span data-ttu-id="77ac4-743">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="77ac4-743">Expiration Date</span></span>

<span data-ttu-id="77ac4-744">Medarbejdere kan angive flere identifikationsnumre af **Pas**-identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="77ac4-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="77ac4-745">Men det er kun den aktuelle aktive paspost, der integreres i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="77ac4-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="77ac4-746">Hvis alle pasposter er udløbet, integreres det pas, der senest blev udstedt, i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="77ac4-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
