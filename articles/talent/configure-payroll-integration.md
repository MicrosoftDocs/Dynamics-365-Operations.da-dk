---
title: Konfigurere lønintegration mellem Talent og Dayforce
description: Dette emne forklarer, hvordan du kan konfigurere integration mellem Microsoft Dynamics 365 Talent og Ceridian Dayforce, så du kan behandle en lønkørsel.
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
ms.openlocfilehash: 075b2bdfa08bb190f66b6d60074e1263feedcf70
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898523"
---
# <a name="configure-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="90a09-103">Konfigurer lønintegration mellem Talent og Dayforce</span><span class="sxs-lookup"><span data-stu-id="90a09-103">Configure payroll integration between Talent and Dayforce</span></span>

<span data-ttu-id="90a09-104">Integration mellem Microsoft Dynamics 365 Talent og Ceridian Dayforce er baseret på flere konfigurationstrin, der er beskrevet i dette emne.</span><span class="sxs-lookup"><span data-stu-id="90a09-104">The integration between Microsoft Dynamics 365 Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="90a09-105">Du skal konfigurere integrationen i både Talent og Dayforce, før du kan behandle en lønkørsel.</span><span class="sxs-lookup"><span data-stu-id="90a09-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="90a09-106">Når du bruger en tjeneste, f.eks. Dayforce, til at fuldføre lønkørsler, skal du aktivere integrationen i Talent.</span><span class="sxs-lookup"><span data-stu-id="90a09-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="90a09-107">Integrationen kræver bestemte data fra Talent.</span><span class="sxs-lookup"><span data-stu-id="90a09-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="90a09-108">Du skal derfor kontrollere, at data, der er knyttet til Dayforce, er konfigureret i Talent på en måde, der understøtter integrationen.</span><span class="sxs-lookup"><span data-stu-id="90a09-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="90a09-109">Integrationen bruger følgende brede kategorier af data.</span><span class="sxs-lookup"><span data-stu-id="90a09-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="90a09-110">Personaledata</span><span class="sxs-lookup"><span data-stu-id="90a09-110">Human resources data</span></span>
- <span data-ttu-id="90a09-111">Kompensationsdata</span><span class="sxs-lookup"><span data-stu-id="90a09-111">Compensation data</span></span>
- <span data-ttu-id="90a09-112">Lønoplysninger, f.eks. løncyklusser, betalingsperioder og lønkoder</span><span class="sxs-lookup"><span data-stu-id="90a09-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="90a09-113">Arbejderdata</span><span class="sxs-lookup"><span data-stu-id="90a09-113">Worker data</span></span>

<span data-ttu-id="90a09-114">Dette emne beskrives de trin, du skal udføre for at aktivere integrationen.</span><span class="sxs-lookup"><span data-stu-id="90a09-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="90a09-115">Det forklarer også typerne af data og oplysninger om konfigurationen, der kræves til integrationen.</span><span class="sxs-lookup"><span data-stu-id="90a09-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="90a09-116">Aktivere integrationen.</span><span class="sxs-lookup"><span data-stu-id="90a09-116">Enable the integration</span></span>

<span data-ttu-id="90a09-117">I Talent skal du aktivere integrationen og angive konfigurationsoplysningerne for at oprette forbindelse til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="90a09-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="90a09-118">Hvis den finanspostering, der er oprettet, skal importeres til Microsoft Dynamics 365 Finance, skal du også konfigurere en Microsoft Azure-lagerkonto og angive Azure-lagerets forbindelsesstreng i Finance.</span><span class="sxs-lookup"><span data-stu-id="90a09-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="90a09-119">Følg disse trin for at aktivere integrationen i Talent.</span><span class="sxs-lookup"><span data-stu-id="90a09-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="90a09-120">På siden **Systemadministration** skal du vælge **Integrationskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="90a09-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="90a09-121">Angiv det sikre FTP-slutpunkt og den sikre FTP-mappesti.</span><span class="sxs-lookup"><span data-stu-id="90a09-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="90a09-122">Angiv brugernavnet og adgangskoden for den bruger, der skal have adgang til det sikre FTP-slutpunkt og den sikre mappesti.</span><span class="sxs-lookup"><span data-stu-id="90a09-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="90a09-123">Test forbindelsen, som krævet, og angiv indstillingen **Aktivér lønintegration** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="90a09-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="90a09-124">Når integrationen er aktiveret, oprettes dataeksportpakken og -filerne, og hyppigheden angives.</span><span class="sxs-lookup"><span data-stu-id="90a09-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="90a09-125">Du kan ændre denne frekvens efter behov.</span><span class="sxs-lookup"><span data-stu-id="90a09-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="90a09-126">Yderligere oplysninger om Azure-lagerkonti og Azure-lagerforbindelsesstrenge finder du i følgende Azure-emner:</span><span class="sxs-lookup"><span data-stu-id="90a09-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="90a09-127">Om Azure-lagerkonti</span><span class="sxs-lookup"><span data-stu-id="90a09-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="90a09-128">Konfigurere forbindelsesstrenge for Azure-datalager</span><span class="sxs-lookup"><span data-stu-id="90a09-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="90a09-129">Tekniske oplysninger ved aktivering af lønintegration</span><span class="sxs-lookup"><span data-stu-id="90a09-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="90a09-130">Aktivering af lønintegration har to primære effekter:</span><span class="sxs-lookup"><span data-stu-id="90a09-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="90a09-131">Der oprettes et dataeksport projekt ved navn "Lønintegrationseksport".</span><span class="sxs-lookup"><span data-stu-id="90a09-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="90a09-132">Dette projekt indeholder de objekter og felter, der kræves til lønintegration.</span><span class="sxs-lookup"><span data-stu-id="90a09-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="90a09-133">Hvis du vil undersøge projektet, skal du gå til **Systemadministration**, vælge feltet **Datastyring** og derefter åbne dataprojektet på listen over projekter.</span><span class="sxs-lookup"><span data-stu-id="90a09-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="90a09-134">Dette batchjob udfører dataeksportprojektet, krypterer den resulterende datapakke og overfører datapakkefilen til det SFTP-slutpunkt, der er konfigureret på skærmen **Integrationskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="90a09-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="90a09-135">Den datapakke, der overføres til SFTP-slutpunktet, krypteres ved hjælp af en nøgle, der er entydig for pakken.</span><span class="sxs-lookup"><span data-stu-id="90a09-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="90a09-136">Nøglen er i en Azure Key Vault, der kun kan åbnes af Ceridian.</span><span class="sxs-lookup"><span data-stu-id="90a09-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="90a09-137">Det er ikke muligt at dekryptere og undersøge datapakkens indhold.</span><span class="sxs-lookup"><span data-stu-id="90a09-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="90a09-138">Hvis du har brug for at undersøge indholdet af datapakken, skal du eksportere dataprojektet "Lønintegrationseksport" manuelt, download det og derefter åbne det.</span><span class="sxs-lookup"><span data-stu-id="90a09-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="90a09-139">Manuel eksport anvender ikke kryptering eller overførsel af pakken.</span><span class="sxs-lookup"><span data-stu-id="90a09-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="90a09-140">Konfigurere dine data</span><span class="sxs-lookup"><span data-stu-id="90a09-140">Configure your data</span></span> 

<span data-ttu-id="90a09-141">Hvis du vil behandle løn, skal du konfigurere personaledata i Talent.</span><span class="sxs-lookup"><span data-stu-id="90a09-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="90a09-142">Du skal angive virksomhedens data, f.eks. job og stillinger, sammen med frynsegoder og kompensationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="90a09-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="90a09-143">Disse oplysninger indeholder oplysningerne om ansættelse, løn og fradrag, der kræves for at generere løn for medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="90a09-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="90a09-144">Personaledata</span><span class="sxs-lookup"><span data-stu-id="90a09-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="90a09-145">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="90a09-145">Benefits</span></span> 

<span data-ttu-id="90a09-146">Personale indeholder en række værktøjer til konfiguration og vedligeholdelse af frynsegoder, fradrag og arbejderkompensationsplaner, som en organisation tilbyder eller behandler for sine ansatte.</span><span class="sxs-lookup"><span data-stu-id="90a09-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="90a09-147">Når du opretter frynsegoder, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="90a09-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="90a09-148">Frynsegodeplaner</span><span class="sxs-lookup"><span data-stu-id="90a09-148">Benefit plans</span></span>

- <span data-ttu-id="90a09-149">Plan (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-149">Plan (required)</span></span>
- <span data-ttu-id="90a09-150">Type (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-150">Type (required)</span></span>
- <span data-ttu-id="90a09-151">Løneffekt (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-151">Payroll impact (required)</span></span>
- <span data-ttu-id="90a09-152">Opkræv restancer</span><span class="sxs-lookup"><span data-stu-id="90a09-152">Recover arrears</span></span>
- <span data-ttu-id="90a09-153">Fradragsmetode</span><span class="sxs-lookup"><span data-stu-id="90a09-153">Deduction method</span></span>
- <span data-ttu-id="90a09-154">Prioriteret fradrag</span><span class="sxs-lookup"><span data-stu-id="90a09-154">Deduction priority</span></span>
- <span data-ttu-id="90a09-155">Grænseperiode</span><span class="sxs-lookup"><span data-stu-id="90a09-155">Limit period</span></span>
- <span data-ttu-id="90a09-156">Beløb for grænse</span><span class="sxs-lookup"><span data-stu-id="90a09-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="90a09-157">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="90a09-157">Benefits</span></span>

- <span data-ttu-id="90a09-158">Plan (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-158">Plan (required)</span></span>
- <span data-ttu-id="90a09-159">Type (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-159">Type (required)</span></span>
- <span data-ttu-id="90a09-160">Mulighed (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-160">Option (required)</span></span>
- <span data-ttu-id="90a09-161">Frynsegode-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-161">Benefit ID (required)</span></span>
- <span data-ttu-id="90a09-162">Frekvens</span><span class="sxs-lookup"><span data-stu-id="90a09-162">Frequency</span></span>
- <span data-ttu-id="90a09-163">Basis</span><span class="sxs-lookup"><span data-stu-id="90a09-163">Basis</span></span>
- <span data-ttu-id="90a09-164">Beløb eller sats</span><span class="sxs-lookup"><span data-stu-id="90a09-164">Amount or rate</span></span>
- <span data-ttu-id="90a09-165">Lønkode</span><span class="sxs-lookup"><span data-stu-id="90a09-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="90a09-166">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="90a09-166">Supported frequencies</span></span> 

- <span data-ttu-id="90a09-167">Ugentlig</span><span class="sxs-lookup"><span data-stu-id="90a09-167">Weekly</span></span>
- <span data-ttu-id="90a09-168">Pr. 14 dage</span><span class="sxs-lookup"><span data-stu-id="90a09-168">Bi-weekly</span></span>
- <span data-ttu-id="90a09-169">To gange om måneden</span><span class="sxs-lookup"><span data-stu-id="90a09-169">Semi-monthly</span></span>
- <span data-ttu-id="90a09-170">Månedlig</span><span class="sxs-lookup"><span data-stu-id="90a09-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="90a09-171">Understøttede grundlag</span><span class="sxs-lookup"><span data-stu-id="90a09-171">Supported bases</span></span> 

- <span data-ttu-id="90a09-172">Fast beløb</span><span class="sxs-lookup"><span data-stu-id="90a09-172">Fixed amount</span></span>
- <span data-ttu-id="90a09-173">Procentdel af løn</span><span class="sxs-lookup"><span data-stu-id="90a09-173">Percent of earnings</span></span>
- <span data-ttu-id="90a09-174">Produktive timer</span><span class="sxs-lookup"><span data-stu-id="90a09-174">Productive hours</span></span>

<span data-ttu-id="90a09-175">Dayforce opretter følgende fradrag, der er baseret på den løneffekt, der er defineret på frynsegodeplanen.</span><span class="sxs-lookup"><span data-stu-id="90a09-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="90a09-176">Valg i Talent</span><span class="sxs-lookup"><span data-stu-id="90a09-176">Selection in Talent</span></span>        | <span data-ttu-id="90a09-177">Resultat i Dayforce</span><span class="sxs-lookup"><span data-stu-id="90a09-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="90a09-178">None</span><span class="sxs-lookup"><span data-stu-id="90a09-178">None</span></span>                       | <span data-ttu-id="90a09-179">Der oprettes ikke noget fradrag.</span><span class="sxs-lookup"><span data-stu-id="90a09-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="90a09-180">Kun fradrag</span><span class="sxs-lookup"><span data-stu-id="90a09-180">Deduction only</span></span>             | <span data-ttu-id="90a09-181">Der oprettes et medarbejderfradrag.</span><span class="sxs-lookup"><span data-stu-id="90a09-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="90a09-182">Kun bidrag</span><span class="sxs-lookup"><span data-stu-id="90a09-182">Contribution only</span></span>          | <span data-ttu-id="90a09-183">Der oprettes et arbejdsgiverfradrag.</span><span class="sxs-lookup"><span data-stu-id="90a09-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="90a09-184">Fradrag og bidrag</span><span class="sxs-lookup"><span data-stu-id="90a09-184">Deduction and contribution</span></span> | <span data-ttu-id="90a09-185">Der oprettes medarbejder- og arbejdsgiverfradrag.</span><span class="sxs-lookup"><span data-stu-id="90a09-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="90a09-186">Du kan finde flere oplysninger om, hvordan du definerer og administrerer et frynsegodeprogram under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="90a09-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="90a09-187">Levere et frynsegodeprogram for medarbejdere</span><span class="sxs-lookup"><span data-stu-id="90a09-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="90a09-188">Oprette et nyt frynsegode</span><span class="sxs-lookup"><span data-stu-id="90a09-188">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="90a09-189">Definere regler og politikker for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="90a09-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="90a09-190">Tilmelde og fjerne frynsegoder fra arbejdere</span><span class="sxs-lookup"><span data-stu-id="90a09-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="90a09-191">Kompensation</span><span class="sxs-lookup"><span data-stu-id="90a09-191">Compensation</span></span> 

<span data-ttu-id="90a09-192">Kompensationsstyring bruges til at styre fordelingen af grundløn og bonusser.</span><span class="sxs-lookup"><span data-stu-id="90a09-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="90a09-193">En medarbejders faste grundløn og kvalifikationstillæg styres gennem faste lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="90a09-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="90a09-194">Betalingen af incitamentsløn som f.eks. bonusudbetalinger, præstationsbonusser, aktieoptioner og tildelte aktier samt engangsbonusser styres ved hjælp af variable lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="90a09-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="90a09-195">Dayforce anvendes kompensationsoplysninger til at beregne en medarbejders timesats eller årlige sats.</span><span class="sxs-lookup"><span data-stu-id="90a09-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="90a09-196">Konverteringer af planer for fast løn og lønsats er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="90a09-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="90a09-197">Medarbejderne skal være knyttet til en plan for fast løn.</span><span class="sxs-lookup"><span data-stu-id="90a09-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="90a09-198">Du kan finde flere oplysninger om kompensationsplaner under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="90a09-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="90a09-199">Oprette faste kompensationsordninger</span><span class="sxs-lookup"><span data-stu-id="90a09-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="90a09-200">Oprette planer for variabel kompensation</span><span class="sxs-lookup"><span data-stu-id="90a09-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="90a09-201">Udarbejde løn-/kompensationsstruktur og -planer</span><span class="sxs-lookup"><span data-stu-id="90a09-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="90a09-202">Proceskompensation</span><span class="sxs-lookup"><span data-stu-id="90a09-202">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="90a09-203">Definere kompensationsproces og beregne resultater</span><span class="sxs-lookup"><span data-stu-id="90a09-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="90a09-204">Melde en medarbejder til en fast lønplan</span><span class="sxs-lookup"><span data-stu-id="90a09-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="90a09-205">Melde en medarbejder til en variabel lønplan</span><span class="sxs-lookup"><span data-stu-id="90a09-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="90a09-206">Job</span><span class="sxs-lookup"><span data-stu-id="90a09-206">Jobs</span></span> 

<span data-ttu-id="90a09-207">Et job er en samling af de opgaver og ansvarsområder, der kræves af en person, der udfører et job.</span><span class="sxs-lookup"><span data-stu-id="90a09-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="90a09-208">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="90a09-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="90a09-209">Konfiguration af komponenter i et job</span><span class="sxs-lookup"><span data-stu-id="90a09-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="90a09-210">Definere nye job</span><span class="sxs-lookup"><span data-stu-id="90a09-210">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="90a09-211">Stillinger</span><span class="sxs-lookup"><span data-stu-id="90a09-211">Positions</span></span>

<span data-ttu-id="90a09-212">En stilling er en individuel forekomst af et job.</span><span class="sxs-lookup"><span data-stu-id="90a09-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="90a09-213">For eksempel er stillingen "Salgschef (øst)" én af de stillinger, der er tilknyttet jobbet "Salgschef".</span><span class="sxs-lookup"><span data-stu-id="90a09-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="90a09-214">En stilling findes i en afdeling.</span><span class="sxs-lookup"><span data-stu-id="90a09-214">A position exists in a department.</span></span> <span data-ttu-id="90a09-215">Der kan kun knyttes én arbejder til hver stilling.</span><span class="sxs-lookup"><span data-stu-id="90a09-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="90a09-216">Hav følgende data og konfiguration i tankerne, når du konfigurerer stillinger:</span><span class="sxs-lookup"><span data-stu-id="90a09-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="90a09-217">Stilling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-217">Position (required)</span></span>
- <span data-ttu-id="90a09-218">Beskrivelse (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-218">Description (required)</span></span>
- <span data-ttu-id="90a09-219">Job (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-219">Job (required)</span></span>
- <span data-ttu-id="90a09-220">Afdeling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-220">Department (required)</span></span>
- <span data-ttu-id="90a09-221">Stillingstype (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-221">Position type (required)</span></span>
- <span data-ttu-id="90a09-222">Fuldtidsækvivalent</span><span class="sxs-lookup"><span data-stu-id="90a09-222">Full-time equivalent</span></span>
- <span data-ttu-id="90a09-223">Normaltimer på årsbasis (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="90a09-224">Betalt af juridiske enhed (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="90a09-225">Betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-225">Pay cycle (required)</span></span>
- <span data-ttu-id="90a09-226">Økonomisk standarddimension – bærer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="90a09-227">Arbejdertildeling – arbejder, tildelingsstart, tildelingsslut, årsagskode</span><span class="sxs-lookup"><span data-stu-id="90a09-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="90a09-228">Hvis flere stillinger i den samme afdeling er knyttet til samme job, konsolideres de til en enkelt stilling i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="90a09-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="90a09-229">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="90a09-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="90a09-230">Organisere dine medarbejdere ved hjælp af afdelinger, jobs og stillinger</span><span class="sxs-lookup"><span data-stu-id="90a09-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="90a09-231">Konfigurere stillinger</span><span class="sxs-lookup"><span data-stu-id="90a09-231">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="90a09-232">Afdelinger</span><span class="sxs-lookup"><span data-stu-id="90a09-232">Departments</span></span>

<span data-ttu-id="90a09-233">En afdeling er en driftsenhed, der repræsenterer en kategori eller et funktionsområde i en organisation.</span><span class="sxs-lookup"><span data-stu-id="90a09-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="90a09-234">En afdeling er ansvarlig for et bestemt område i organisationen, såsom salg, regnskab eller personale.</span><span class="sxs-lookup"><span data-stu-id="90a09-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="90a09-235">Du kan bruge afdelinger til at rapportere om funktionsområder.</span><span class="sxs-lookup"><span data-stu-id="90a09-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="90a09-236">Afdelinger kan have ansvar for driftsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="90a09-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="90a09-237">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="90a09-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="90a09-238">Oprette en afdeling og knytte den til afdelingshierarkiet</span><span class="sxs-lookup"><span data-stu-id="90a09-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="90a09-239">Definere nye afdelinger</span><span class="sxs-lookup"><span data-stu-id="90a09-239">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="90a09-240">Betalingscyklusser og lønperioder</span><span class="sxs-lookup"><span data-stu-id="90a09-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="90a09-241">En betalingscyklus bestemmer, hvor ofte løn køres,og de specifikke dage, hvor arbejdere betales.</span><span class="sxs-lookup"><span data-stu-id="90a09-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="90a09-242">En løncyklus kan f.eks. være månedlig, og medarbejdere betales måske på den sidste dag i måneden.</span><span class="sxs-lookup"><span data-stu-id="90a09-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="90a09-243">En løncyklus kan også være ugentligt, og medarbejdere betales måske tirsdag efter slutningen af lønperioden.</span><span class="sxs-lookup"><span data-stu-id="90a09-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="90a09-244">Løncyklusser tildeles til stillinger for at styre, hvornår arbejdere i disse stillinger bliver betalt.</span><span class="sxs-lookup"><span data-stu-id="90a09-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="90a09-245">Når du opretter betalingscyklusser, kan du generere lønperioder for hver cyklus.</span><span class="sxs-lookup"><span data-stu-id="90a09-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="90a09-246">Hver lønperiode omfatter en standardbetalingsdato, der er baseret på oplysninger, du angiver.</span><span class="sxs-lookup"><span data-stu-id="90a09-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="90a09-247">Du kan dog redigere standardbetalingsdatoen i en lønperiode til at tillade undtagelser, f.eks. når betalingsdatoen falder på en helligdag.</span><span class="sxs-lookup"><span data-stu-id="90a09-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="90a09-248">Følgende oplysninger bruges i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="90a09-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="90a09-249">Betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-249">Pay cycle (required)</span></span>
- <span data-ttu-id="90a09-250">Hyppighed for betalingscyklus (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="90a09-251">Periodens startdato (første lønperiode påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="90a09-252">Standardbetalingsdato (første lønperiode påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="90a09-253">Oplysningerne er integreret med Dayforce som løngrupper og adskilles af et land eller område for hver løncyklus.</span><span class="sxs-lookup"><span data-stu-id="90a09-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="90a09-254">Mindst én periode skal genereres før integration.</span><span class="sxs-lookup"><span data-stu-id="90a09-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="90a09-255">Dayforce genererer løngruppekalendere og betalingsdatoer, der er baseret på startdatoen for den første lønperiode og den standardbetalingsdato, der er angivet i Talent.</span><span class="sxs-lookup"><span data-stu-id="90a09-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="90a09-256">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="90a09-256">Earning codes</span></span>

<span data-ttu-id="90a09-257">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="90a09-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="90a09-258">Koderne har forskellige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="90a09-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="90a09-259">Følgende oplysninger bruges i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="90a09-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="90a09-260">Lønkode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-260">Earning Code (required)</span></span>
- <span data-ttu-id="90a09-261">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="90a09-261">Description</span></span>
- <span data-ttu-id="90a09-262">Måleenhed</span><span class="sxs-lookup"><span data-stu-id="90a09-262">Unit of measure</span></span>
- <span data-ttu-id="90a09-263">Produktiv</span><span class="sxs-lookup"><span data-stu-id="90a09-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="90a09-264">Arbejderdata</span><span class="sxs-lookup"><span data-stu-id="90a09-264">Worker data</span></span>

<span data-ttu-id="90a09-265">Posterne for de forskellige typer arbejdere, du beskæftiger, er vigtige for dine personale- og lønsystemer.</span><span class="sxs-lookup"><span data-stu-id="90a09-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="90a09-266">De oplysninger, du angiver, kan bruges til at spore arbejdere og personoplysninger.</span><span class="sxs-lookup"><span data-stu-id="90a09-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="90a09-267">Du kan vedligeholde følgende oplysninger for arbejdere:</span><span class="sxs-lookup"><span data-stu-id="90a09-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="90a09-268">**Basis** – Vedligehold grundlæggende oplysninger om en arbejder, f.eks. kontaktoplysninger, demografiske oplysninger, identifikationsoplysninger, oplysninger om familie, status for militærtjeneste, oplysninger om udstationering og personlige kontaktpersoner og kontaktpersoner i nødsituationer.</span><span class="sxs-lookup"><span data-stu-id="90a09-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="90a09-269">**Beskæftigelse** – Vedligehold oplysninger om en arbejders beskæftigelse, f.eks. firma- eller organisationstilhørsforhold, stillingstildeling, start- og slutdatoer, arbejdstilladelse, vilkår for ansættelse, pension, ferie og flytteoplysninger.</span><span class="sxs-lookup"><span data-stu-id="90a09-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="90a09-270">**Orlov og fravær** – Vedligehold oplysninger om en arbejders fravær, f.eks. arbejdskalendere, fraværstransaktioner og fraværsopsætning.</span><span class="sxs-lookup"><span data-stu-id="90a09-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="90a09-271">**Kompensation og løn** – Vedligehold oplysninger om en arbejders kompensationsplaner og lønoplysninger, f.eks. tilmelding til planer, priser, ydeevne, provision, skatteoplysninger, pensionering og skattefradrag.</span><span class="sxs-lookup"><span data-stu-id="90a09-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="90a09-272">Når du angiver arbejderoplysninger, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="90a09-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="90a09-273">Generelle oplysninger</span><span class="sxs-lookup"><span data-stu-id="90a09-273">General information</span></span>

- <span data-ttu-id="90a09-274">Personalenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-274">Personnel number (required)</span></span>
- <span data-ttu-id="90a09-275">Fornavn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-275">First name (required)</span></span>
- <span data-ttu-id="90a09-276">Efternavn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-276">Last name (required)</span></span>
- <span data-ttu-id="90a09-277">Mellemnavn</span><span class="sxs-lookup"><span data-stu-id="90a09-277">Middle name</span></span>
- <span data-ttu-id="90a09-278">Anciennitetsdato</span><span class="sxs-lookup"><span data-stu-id="90a09-278">Seniority date</span></span>
- <span data-ttu-id="90a09-279">Kendt som</span><span class="sxs-lookup"><span data-stu-id="90a09-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="90a09-280">Personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="90a09-280">Personal information</span></span>

- <span data-ttu-id="90a09-281">Ægteskabelig status (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-281">Marital status (required)</span></span>
- <span data-ttu-id="90a09-282">Fødselsdato (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-282">Birth date (required)</span></span>
- <span data-ttu-id="90a09-283">Køn (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-283">Gender (required)</span></span>
- <span data-ttu-id="90a09-284">Handicappet</span><span class="sxs-lookup"><span data-stu-id="90a09-284">Person with disabilities</span></span>
- <span data-ttu-id="90a09-285">Land eller område for nationalitet (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="90a09-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="90a09-286">Adresseoplysninger</span><span class="sxs-lookup"><span data-stu-id="90a09-286">Address information</span></span>

- <span data-ttu-id="90a09-287">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-287">Primary (required)</span></span>
- <span data-ttu-id="90a09-288">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-288">Country/region (required)</span></span>
- <span data-ttu-id="90a09-289">Postnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-289">Postal code (required)</span></span>
- <span data-ttu-id="90a09-290">Gadenummer (påkrævet) (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="90a09-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="90a09-291">Bygningskomplement (kun for Mexico)</span><span class="sxs-lookup"><span data-stu-id="90a09-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="90a09-292">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-292">City (required)</span></span>
- <span data-ttu-id="90a09-293">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-293">State (required)</span></span>
- <span data-ttu-id="90a09-294">Region (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="90a09-295">Kontaktoplysninger</span><span class="sxs-lookup"><span data-stu-id="90a09-295">Contact information</span></span> 

- <span data-ttu-id="90a09-296">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-296">Primary (required)</span></span>
- <span data-ttu-id="90a09-297">Kontaktpersonens nummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-297">Contact number (required)</span></span>
- <span data-ttu-id="90a09-298">Forlængelse</span><span class="sxs-lookup"><span data-stu-id="90a09-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="90a09-299">Lønoplysninger og lønkoder</span><span class="sxs-lookup"><span data-stu-id="90a09-299">Payroll information and earning codes</span></span>

<span data-ttu-id="90a09-300">Medarbejdere kan tildeles en bestemt løn med en given betalingshyppighed og have en foretrukken betalingsmetode.</span><span class="sxs-lookup"><span data-stu-id="90a09-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="90a09-301">Følgende felter bruges i Dayforce til at sikre, at disse præferencer og indstillinger bruges.</span><span class="sxs-lookup"><span data-stu-id="90a09-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="90a09-302">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="90a09-302">Earning codes</span></span>

- <span data-ttu-id="90a09-303">Stilling (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-303">Position (required)</span></span>
- <span data-ttu-id="90a09-304">Lønkode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-304">Earning Code (required)</span></span>
- <span data-ttu-id="90a09-305">Frekvens (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-305">Frequency (required)</span></span>
- <span data-ttu-id="90a09-306">Beløb (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="90a09-307">Lønoplysninger</span><span class="sxs-lookup"><span data-stu-id="90a09-307">Payroll information</span></span>

- <span data-ttu-id="90a09-308">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="90a09-308">Payment Method</span></span>
- <span data-ttu-id="90a09-309">Økonomisk område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-309">Economic Region (required)</span></span>
- <span data-ttu-id="90a09-310">Id for medarbejderfrynsegoder</span><span class="sxs-lookup"><span data-stu-id="90a09-310">Employee Benefits ID</span></span>
- <span data-ttu-id="90a09-311">Nationalt id-nummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-311">National ID Number (required)</span></span>
- <span data-ttu-id="90a09-312">Tjenestenummer hos militær</span><span class="sxs-lookup"><span data-stu-id="90a09-312">Military Service Number</span></span>
- <span data-ttu-id="90a09-313">Skifte-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-313">Shift ID (required)</span></span>
- <span data-ttu-id="90a09-314">Skattenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-314">Tax Number (required)</span></span>
- <span data-ttu-id="90a09-315">Fagforenings-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-315">Union ID (required)</span></span>
- <span data-ttu-id="90a09-316">Arbejdsdags-id (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-316">Work Day ID (required)</span></span>
- <span data-ttu-id="90a09-317">Arbejdstilladelsesnummer</span><span class="sxs-lookup"><span data-stu-id="90a09-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="90a09-318">For betalingsmetoden understøtter Mexico **Kontant**, **Check** (firmaets fysiske check), og **Elektronisk betaling**.</span><span class="sxs-lookup"><span data-stu-id="90a09-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="90a09-319">Hvis der ikke er angivet nogen betalingsmetode, bruges **Check** som standard.</span><span class="sxs-lookup"><span data-stu-id="90a09-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="90a09-320">Detaljer om ansættelse</span><span class="sxs-lookup"><span data-stu-id="90a09-320">Employment details</span></span>

<span data-ttu-id="90a09-321">Detaljeret ansættelseshistorik bruges som vigtige oplysninger til at udlede statusser for en medarbejders ansættelse, fratrædelse og genansættelse i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="90a09-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="90a09-322">Dayforce understøtter kun én aktiv ansættelsespost ad gangen.</span><span class="sxs-lookup"><span data-stu-id="90a09-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="90a09-323">Startdato for ansættelse (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-323">Employment start date (required)</span></span>
- <span data-ttu-id="90a09-324">Slutdato for ansættelse</span><span class="sxs-lookup"><span data-stu-id="90a09-324">Employment end date</span></span>
- <span data-ttu-id="90a09-325">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="90a09-325">Start date</span></span>
- <span data-ttu-id="90a09-326">Justeret startdato</span><span class="sxs-lookup"><span data-stu-id="90a09-326">Adjusted start date</span></span>
- <span data-ttu-id="90a09-327">Fratrædelsesdato (kræves ved fratrædelse)</span><span class="sxs-lookup"><span data-stu-id="90a09-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="90a09-328">Fratrædelsesårsag (kræves ved fratrædelse)</span><span class="sxs-lookup"><span data-stu-id="90a09-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="90a09-329">Vigtige datoer for en medarbejders udledes ved hjælp af følgende oplysninger.</span><span class="sxs-lookup"><span data-stu-id="90a09-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="90a09-330">Talent</span><span class="sxs-lookup"><span data-stu-id="90a09-330">Talent</span></span>                | <span data-ttu-id="90a09-331">Dayforce</span><span class="sxs-lookup"><span data-stu-id="90a09-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90a09-332">Den seneste ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="90a09-332">Most recent hire date</span></span> | <span data-ttu-id="90a09-333">Historikpost for ansættelsesstart for aktuel ikke-afsluttet ansættelse</span><span class="sxs-lookup"><span data-stu-id="90a09-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="90a09-334">Fratrædelsesdato</span><span class="sxs-lookup"><span data-stu-id="90a09-334">Termination date</span></span>      | <span data-ttu-id="90a09-335">Historikpost for fratrædelsesdato for aktuel ikke-afsluttet ansættelse</span><span class="sxs-lookup"><span data-stu-id="90a09-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="90a09-336">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="90a09-336">Start date</span></span>            | <span data-ttu-id="90a09-337">Historikpost for justeret startdato, startdato eller startdato for ansættelse for aktuel ikke-aktiv ansættelse</span><span class="sxs-lookup"><span data-stu-id="90a09-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="90a09-338">Oprindelig ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="90a09-338">Original hire date</span></span>    | <span data-ttu-id="90a09-339">Historikpost for ansættelsesstart for tidligste ansættelse</span><span class="sxs-lookup"><span data-stu-id="90a09-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="90a09-340">Kompensation</span><span class="sxs-lookup"><span data-stu-id="90a09-340">Compensation</span></span>

<span data-ttu-id="90a09-341">En fast lønstruktur skal tilknyttes hver medarbejders primære stilling gennem hele ansættelsesperioden.</span><span class="sxs-lookup"><span data-stu-id="90a09-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="90a09-342">Denne periode starter på den dato, hvor medarbejderen blev ansat (eller ansættelsesstartdatoen) og fortsætter, indtil fratrædelsen.</span><span class="sxs-lookup"><span data-stu-id="90a09-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="90a09-343">Ikrafttrædelsesdato (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-343">Effective Date (required)</span></span>
- <span data-ttu-id="90a09-344">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="90a09-344">Expiration date</span></span>
- <span data-ttu-id="90a09-345">Lønsats (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-345">Pay Rate (required)</span></span>
- <span data-ttu-id="90a09-346">Konverteringer af lønsats (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="90a09-347">Årlig ækvivalent (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="90a09-348">Timebaseret ækvivalent (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="90a09-349">Hvis en timeansat medarbejder har flere stillinger, indlæses den faste løn for den primære stilling i Dayforce, som basissats/-løn på medarbejderniveau.</span><span class="sxs-lookup"><span data-stu-id="90a09-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="90a09-350">For ikke-primære stillinger gemmes timesatsen i den tilsvarende position i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="90a09-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="90a09-351">Hvis en funktionær har flere stillinger, afledes den kumulative timesats og årlig gage på tværs af alle aktive stillinger og bruges som basissats/-gage på medarbejderniveau.</span><span class="sxs-lookup"><span data-stu-id="90a09-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="90a09-352">Identifikationsnumre</span><span class="sxs-lookup"><span data-stu-id="90a09-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="90a09-353">Social Security-identifikator</span><span class="sxs-lookup"><span data-stu-id="90a09-353">Social Security identifier</span></span> 

<span data-ttu-id="90a09-354">Alle medarbejdere skal have én primær identifikator.</span><span class="sxs-lookup"><span data-stu-id="90a09-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="90a09-355">Identifikatoren skal være af **SSN**-identifikationstypen</span><span class="sxs-lookup"><span data-stu-id="90a09-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="90a09-356">I Dayforce afledes den automatisk som medarbejderens Social Security-identifikator, der er påkrævet ved ansættelse.</span><span class="sxs-lookup"><span data-stu-id="90a09-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="90a09-357">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-357">Primary (required)</span></span>
- <span data-ttu-id="90a09-358">Identifikationstype = "SSN"</span><span class="sxs-lookup"><span data-stu-id="90a09-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="90a09-359">Udstedt den</span><span class="sxs-lookup"><span data-stu-id="90a09-359">Issued Date</span></span>
- <span data-ttu-id="90a09-360">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="90a09-360">Expiration Date</span></span>

<span data-ttu-id="90a09-361">Medarbejdere kan angive flere identifikationsnumre af **SSN**-identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="90a09-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="90a09-362">Men det er kun den post, der er markeret som **Primær**, som er integreret i Dayforce, uanset om nummeret er aktivt eller udløbet.</span><span class="sxs-lookup"><span data-stu-id="90a09-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="90a09-363">Bankkonto og udbetalinger</span><span class="sxs-lookup"><span data-stu-id="90a09-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="90a09-364">Gyldige bankkontooplysninger skal angives for enhver medarbejder, der vælger at blive betalt via bankkontooverførsler.</span><span class="sxs-lookup"><span data-stu-id="90a09-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="90a09-365">Talent</span><span class="sxs-lookup"><span data-stu-id="90a09-365">Talent</span></span>                         | <span data-ttu-id="90a09-366">Dayforce</span><span class="sxs-lookup"><span data-stu-id="90a09-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90a09-367">Bankkontonummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="90a09-368">SWIFT-kode (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-368">SWIFT code (required)</span></span>          | <span data-ttu-id="90a09-369">Feltet **Bank-id** bruges ved behandling af løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="90a09-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="90a09-370">Afdelingsnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="90a09-371">Bankkontotype (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-371">Bank account type (required)</span></span>   | <span data-ttu-id="90a09-372">Feltet **Kontotype** bruges ved behandling af løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="90a09-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="90a09-373">Understøttede værdier omfatter **Check** og **Løn**.</span><span class="sxs-lookup"><span data-stu-id="90a09-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="90a09-374">Medarbejdere, der vælger at betales via bankkontooverførsler, skal angive et link til en restbeløbskonto, der hører under en juridisk enhed, som har primær adresse i Mexico og er knyttet til en gyldig bankkonto fra en mexicansk bank.</span><span class="sxs-lookup"><span data-stu-id="90a09-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="90a09-375">Alle andre restbeløbskonti ignoreres.</span><span class="sxs-lookup"><span data-stu-id="90a09-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="90a09-376">Adresseoplysninger</span><span class="sxs-lookup"><span data-stu-id="90a09-376">Address information</span></span>

<span data-ttu-id="90a09-377">Alle medarbejdere skal have én primær placering.</span><span class="sxs-lookup"><span data-stu-id="90a09-377">Every employee must have one primary location.</span></span> <span data-ttu-id="90a09-378">I Dayforce bruges denne placering til at bestemme medarbejderens primære opholdssted til skattemæssige formål.</span><span class="sxs-lookup"><span data-stu-id="90a09-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="90a09-379">Primær (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-379">Primary (required)</span></span>
- <span data-ttu-id="90a09-380">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-380">Country/region (required)</span></span>
- <span data-ttu-id="90a09-381">Postnummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="90a09-382">Gade (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-382">Street (required)</span></span>
- <span data-ttu-id="90a09-383">Gadenummer (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-383">Street Number (required)</span></span>
- <span data-ttu-id="90a09-384">Bygningskomplement</span><span class="sxs-lookup"><span data-stu-id="90a09-384">Building Complement</span></span>
- <span data-ttu-id="90a09-385">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-385">City (required)</span></span>
- <span data-ttu-id="90a09-386">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-386">State (required)</span></span>
- <span data-ttu-id="90a09-387">Region (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="90a09-388">Konfigurere dataene for at generere løn i USA og Canada</span><span class="sxs-lookup"><span data-stu-id="90a09-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="90a09-389">Hvis du genererer løn for medarbejdere i USA og Canada, skal følgende elementer konfigureres:</span><span class="sxs-lookup"><span data-stu-id="90a09-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="90a09-390">Der kræves afdelinger til stillinger.</span><span class="sxs-lookup"><span data-stu-id="90a09-390">Departments are required on positions.</span></span>
- <span data-ttu-id="90a09-391">Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="90a09-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="90a09-392">Du kan konfigurere Talent til at kræve, at der angives en afdeling for stillinger.</span><span class="sxs-lookup"><span data-stu-id="90a09-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="90a09-393">For at gøre dette skal du gå til **Personalets delte stillinger > Stillinger > Kræv afdelinger for stillinger**.</span><span class="sxs-lookup"><span data-stu-id="90a09-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="90a09-394">Det anbefales, at denne indstilling gennemtvinges i forbindelse med integrationen.</span><span class="sxs-lookup"><span data-stu-id="90a09-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="90a09-395">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="90a09-395">Job types</span></span>

<span data-ttu-id="90a09-396">Jobtyper bruges til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="90a09-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="90a09-397">Jobtyper kræves for at behandle løn i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="90a09-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="90a09-398">Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="90a09-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="90a09-399">Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.</span><span class="sxs-lookup"><span data-stu-id="90a09-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="90a09-400">Der kræves følgende jobtyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="90a09-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="90a09-401">Jobtype</span><span class="sxs-lookup"><span data-stu-id="90a09-401">Job type</span></span>   | <span data-ttu-id="90a09-402">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="90a09-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="90a09-403">Pr. time</span><span class="sxs-lookup"><span data-stu-id="90a09-403">Hourly</span></span>     | <span data-ttu-id="90a09-404">Pr. time</span><span class="sxs-lookup"><span data-stu-id="90a09-404">Hourly</span></span>      |
| <span data-ttu-id="90a09-405">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="90a09-405">Salaried</span></span>   | <span data-ttu-id="90a09-406">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="90a09-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="90a09-407">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="90a09-407">Position types</span></span> 

<span data-ttu-id="90a09-408">Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet.</span><span class="sxs-lookup"><span data-stu-id="90a09-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="90a09-409">Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="90a09-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="90a09-410">Der kræves følgende stillingstyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="90a09-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="90a09-411">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="90a09-411">Position type</span></span>   | <span data-ttu-id="90a09-412">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="90a09-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="90a09-413">Fuld tid</span><span class="sxs-lookup"><span data-stu-id="90a09-413">Full-time</span></span>       | <span data-ttu-id="90a09-414">Fuldtidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="90a09-414">Full time employee</span></span> |
| <span data-ttu-id="90a09-415">Deltid</span><span class="sxs-lookup"><span data-stu-id="90a09-415">Part-time</span></span>       | <span data-ttu-id="90a09-416">Deltidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="90a09-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="90a09-417">Årsagskoder</span><span class="sxs-lookup"><span data-stu-id="90a09-417">Reason codes</span></span>

<span data-ttu-id="90a09-418">Årsagskoder indeholder oplysninger om status for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="90a09-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="90a09-419">Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.</span><span class="sxs-lookup"><span data-stu-id="90a09-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="90a09-420">Der kræves følgende årsagskoder og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="90a09-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="90a09-421">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="90a09-421">Reason code</span></span>    | <span data-ttu-id="90a09-422">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="90a09-422">Description</span></span>      | <span data-ttu-id="90a09-423">Anvendelige scenarier</span><span class="sxs-lookup"><span data-stu-id="90a09-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="90a09-424">OPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="90a09-424">RESIGNATION</span></span>    | <span data-ttu-id="90a09-425">Opsigelse</span><span class="sxs-lookup"><span data-stu-id="90a09-425">Resignation</span></span>      | <span data-ttu-id="90a09-426">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="90a09-426">Terminate worker</span></span>     |
| <span data-ttu-id="90a09-427">OPHØR</span><span class="sxs-lookup"><span data-stu-id="90a09-427">TERMINATION</span></span>    | <span data-ttu-id="90a09-428">Ophør</span><span class="sxs-lookup"><span data-stu-id="90a09-428">Termination</span></span>      | <span data-ttu-id="90a09-429">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="90a09-429">Terminate worker</span></span>     |
| <span data-ttu-id="90a09-430">PENSION</span><span class="sxs-lookup"><span data-stu-id="90a09-430">RETIREMENT</span></span>     | <span data-ttu-id="90a09-431">Pension</span><span class="sxs-lookup"><span data-stu-id="90a09-431">Retirement</span></span>       | <span data-ttu-id="90a09-432">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="90a09-432">Terminate worker</span></span>     |
| <span data-ttu-id="90a09-433">ANDET</span><span class="sxs-lookup"><span data-stu-id="90a09-433">OTHER</span></span>          | <span data-ttu-id="90a09-434">Andre årsager</span><span class="sxs-lookup"><span data-stu-id="90a09-434">Other Reasons</span></span>    | <span data-ttu-id="90a09-435">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="90a09-435">Terminate worker</span></span>     |
| <span data-ttu-id="90a09-436">DØDSFALD</span><span class="sxs-lookup"><span data-stu-id="90a09-436">DEATH</span></span>          | <span data-ttu-id="90a09-437">Dødsfald</span><span class="sxs-lookup"><span data-stu-id="90a09-437">Death</span></span>            | <span data-ttu-id="90a09-438">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="90a09-438">Terminate worker</span></span>     |
| <span data-ttu-id="90a09-439">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="90a09-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="90a09-440">Orlov</span><span class="sxs-lookup"><span data-stu-id="90a09-440">Leave of Absence</span></span> | <span data-ttu-id="90a09-441">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="90a09-441">Terminate worker</span></span>     |
| <span data-ttu-id="90a09-442">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="90a09-442">CONTRACTEND</span></span>    | <span data-ttu-id="90a09-443">Kontraktudløb</span><span class="sxs-lookup"><span data-stu-id="90a09-443">End of Contract</span></span>  | <span data-ttu-id="90a09-444">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="90a09-444">Terminate worker</span></span>     |
| <span data-ttu-id="90a09-445">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="90a09-445">SALARYCHANGE</span></span>   | <span data-ttu-id="90a09-446">Ændring af løn</span><span class="sxs-lookup"><span data-stu-id="90a09-446">Change of Salary</span></span> | <span data-ttu-id="90a09-447">Kompensation</span><span class="sxs-lookup"><span data-stu-id="90a09-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="90a09-448">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="90a09-448">Marital status</span></span>

<span data-ttu-id="90a09-449">Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="90a09-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="90a09-450">Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="90a09-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="90a09-451">Talent</span><span class="sxs-lookup"><span data-stu-id="90a09-451">Talent</span></span>                 | <span data-ttu-id="90a09-452">Dayforce</span><span class="sxs-lookup"><span data-stu-id="90a09-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="90a09-453">Gift</span><span class="sxs-lookup"><span data-stu-id="90a09-453">Married</span></span>                | <span data-ttu-id="90a09-454">Gift</span><span class="sxs-lookup"><span data-stu-id="90a09-454">Married</span></span>              |
| <span data-ttu-id="90a09-455">Enlig</span><span class="sxs-lookup"><span data-stu-id="90a09-455">Single</span></span>                 | <span data-ttu-id="90a09-456">Enlig</span><span class="sxs-lookup"><span data-stu-id="90a09-456">Single</span></span>               |
| <span data-ttu-id="90a09-457">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="90a09-457">Widowed</span></span>                | <span data-ttu-id="90a09-458">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="90a09-458">Widowed</span></span>              |
| <span data-ttu-id="90a09-459">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="90a09-459">Divorced</span></span>               | <span data-ttu-id="90a09-460">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="90a09-460">Divorced</span></span>             |
| <span data-ttu-id="90a09-461">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="90a09-461">Registered Partnership</span></span> | <span data-ttu-id="90a09-462">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="90a09-462">Domestic Partnership</span></span> |
| <span data-ttu-id="90a09-463">None</span><span class="sxs-lookup"><span data-stu-id="90a09-463">None</span></span>                   | <span data-ttu-id="90a09-464">None</span><span class="sxs-lookup"><span data-stu-id="90a09-464">None</span></span>                 |
| <span data-ttu-id="90a09-465">Samlever</span><span class="sxs-lookup"><span data-stu-id="90a09-465">Cohabiting</span></span>             | <span data-ttu-id="90a09-466">Samlever</span><span class="sxs-lookup"><span data-stu-id="90a09-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="90a09-467">Køn</span><span class="sxs-lookup"><span data-stu-id="90a09-467">Gender</span></span>

<span data-ttu-id="90a09-468">Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="90a09-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="90a09-469">Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="90a09-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="90a09-470">Talent</span><span class="sxs-lookup"><span data-stu-id="90a09-470">Talent</span></span>       | <span data-ttu-id="90a09-471">Dayforce</span><span class="sxs-lookup"><span data-stu-id="90a09-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="90a09-472">Mand</span><span class="sxs-lookup"><span data-stu-id="90a09-472">Male</span></span>         | <span data-ttu-id="90a09-473">Mand</span><span class="sxs-lookup"><span data-stu-id="90a09-473">Male</span></span>            |
| <span data-ttu-id="90a09-474">Kvinde</span><span class="sxs-lookup"><span data-stu-id="90a09-474">Female</span></span>       | <span data-ttu-id="90a09-475">Kvinde</span><span class="sxs-lookup"><span data-stu-id="90a09-475">Female</span></span>          |
| <span data-ttu-id="90a09-476">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="90a09-476">Non-specific</span></span> | <span data-ttu-id="90a09-477">*Understøttes ikke*</span><span class="sxs-lookup"><span data-stu-id="90a09-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="90a09-478">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="90a09-478">Earning codes</span></span>

<span data-ttu-id="90a09-479">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="90a09-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="90a09-480">Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="90a09-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="90a09-481">Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="90a09-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="90a09-482">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="90a09-482">Supported frequencies</span></span>

- <span data-ttu-id="90a09-483">Alt</span><span class="sxs-lookup"><span data-stu-id="90a09-483">All</span></span>
- <span data-ttu-id="90a09-484">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="90a09-484">EVERYPAY</span></span>
- <span data-ttu-id="90a09-485">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="90a09-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="90a09-486">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="90a09-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="90a09-487">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="90a09-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="90a09-488">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-488">1OFMTH</span></span>
- <span data-ttu-id="90a09-489">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-489">LASTOFMTH</span></span>
- <span data-ttu-id="90a09-490">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-490">2OFMTH</span></span>
- <span data-ttu-id="90a09-491">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-491">3OFMTH</span></span>
- <span data-ttu-id="90a09-492">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-492">4OFMTH</span></span>
- <span data-ttu-id="90a09-493">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-493">5OFMTH</span></span>
- <span data-ttu-id="90a09-494">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-494">1N2OFMTH</span></span>
- <span data-ttu-id="90a09-495">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-495">3N4OFMTH</span></span>
- <span data-ttu-id="90a09-496">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-496">1N3OFMTH</span></span>
- <span data-ttu-id="90a09-497">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-497">1N4OFMTH</span></span>
- <span data-ttu-id="90a09-498">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-498">2N3OFMTH</span></span>
- <span data-ttu-id="90a09-499">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-499">2N4OFMTH</span></span>
- <span data-ttu-id="90a09-500">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="90a09-501">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="90a09-502">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="90a09-503">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="90a09-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="90a09-505">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="90a09-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="90a09-506">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="90a09-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="90a09-507">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="90a09-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="90a09-508">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="90a09-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="90a09-509">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="90a09-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="90a09-510">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="90a09-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="90a09-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="90a09-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="90a09-512">Adresser</span><span class="sxs-lookup"><span data-stu-id="90a09-512">Addresses</span></span>

<span data-ttu-id="90a09-513">Identifikation af specifikke koder for land eller region, stat og område (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende.</span><span class="sxs-lookup"><span data-stu-id="90a09-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="90a09-514">Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.</span><span class="sxs-lookup"><span data-stu-id="90a09-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="90a09-515">Talent</span><span class="sxs-lookup"><span data-stu-id="90a09-515">Talent</span></span>          | <span data-ttu-id="90a09-516">Dayforce</span><span class="sxs-lookup"><span data-stu-id="90a09-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="90a09-517">Land/område</span><span class="sxs-lookup"><span data-stu-id="90a09-517">Country/Region</span></span>  | <span data-ttu-id="90a09-518">Landekode</span><span class="sxs-lookup"><span data-stu-id="90a09-518">Country Code</span></span>          |
| <span data-ttu-id="90a09-519">Postnummer</span><span class="sxs-lookup"><span data-stu-id="90a09-519">Zip/Postal Code</span></span> | <span data-ttu-id="90a09-520">Postnummer</span><span class="sxs-lookup"><span data-stu-id="90a09-520">Postal Code</span></span>           |
| <span data-ttu-id="90a09-521">Status</span><span class="sxs-lookup"><span data-stu-id="90a09-521">State</span></span>           | <span data-ttu-id="90a09-522">Statskode</span><span class="sxs-lookup"><span data-stu-id="90a09-522">State Code</span></span>            |
| <span data-ttu-id="90a09-523">Bynavn</span><span class="sxs-lookup"><span data-stu-id="90a09-523">City</span></span>            | <span data-ttu-id="90a09-524">Bynavn</span><span class="sxs-lookup"><span data-stu-id="90a09-524">City</span></span>                  |
| <span data-ttu-id="90a09-525">Region</span><span class="sxs-lookup"><span data-stu-id="90a09-525">County</span></span>          | <span data-ttu-id="90a09-526">Område (kommune)</span><span class="sxs-lookup"><span data-stu-id="90a09-526">County (Municipality)</span></span> |
| <span data-ttu-id="90a09-527">Gade</span><span class="sxs-lookup"><span data-stu-id="90a09-527">Street</span></span>          | <span data-ttu-id="90a09-528">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="90a09-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="90a09-529">Skatteområder</span><span class="sxs-lookup"><span data-stu-id="90a09-529">Tax regions</span></span>

<span data-ttu-id="90a09-530">Skatteområder bruges til at bestemme den relevante skat, der skal anvendes ved løngenerering.</span><span class="sxs-lookup"><span data-stu-id="90a09-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="90a09-531">Skatteområder er tilknyttet Dayforce som placeringsadresser.</span><span class="sxs-lookup"><span data-stu-id="90a09-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="90a09-532">Standardskatteområder skal knyttes til arbejderens aktive stilling.</span><span class="sxs-lookup"><span data-stu-id="90a09-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="90a09-533">Skatteområde (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-533">Tax region (required)</span></span>
- <span data-ttu-id="90a09-534">Land/område (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-534">Country/Region (required)</span></span>
- <span data-ttu-id="90a09-535">Stat (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-535">State (required)</span></span>
- <span data-ttu-id="90a09-536">Region</span><span class="sxs-lookup"><span data-stu-id="90a09-536">County</span></span> 
- <span data-ttu-id="90a09-537">By (påkrævet)</span><span class="sxs-lookup"><span data-stu-id="90a09-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="90a09-538">Konfigurere dataene for at generere løn i Mexico</span><span class="sxs-lookup"><span data-stu-id="90a09-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="90a09-539">Hvis du genererer løn for medarbejdere i Mexico skal følgende elementer konfigureres:</span><span class="sxs-lookup"><span data-stu-id="90a09-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="90a09-540">Der kræves afdelinger til stillinger.</span><span class="sxs-lookup"><span data-stu-id="90a09-540">Departments are required on positions.</span></span>
- <span data-ttu-id="90a09-541">Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="90a09-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="90a09-542">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="90a09-542">Job types</span></span>

<span data-ttu-id="90a09-543">Jobtyper bruges til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="90a09-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="90a09-544">Jobtyper kræves for at behandle løn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="90a09-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="90a09-545">Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="90a09-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="90a09-546">Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.</span><span class="sxs-lookup"><span data-stu-id="90a09-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="90a09-547">Der kræves følgende jobtyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="90a09-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="90a09-548">Jobtype</span><span class="sxs-lookup"><span data-stu-id="90a09-548">Job type</span></span>   | <span data-ttu-id="90a09-549">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="90a09-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="90a09-550">Pr. time</span><span class="sxs-lookup"><span data-stu-id="90a09-550">Hourly</span></span>     | <span data-ttu-id="90a09-551">MX Pr. time</span><span class="sxs-lookup"><span data-stu-id="90a09-551">MX Hourly</span></span>   |
| <span data-ttu-id="90a09-552">Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="90a09-552">Salaried</span></span>   | <span data-ttu-id="90a09-553">MX Funktionærløn</span><span class="sxs-lookup"><span data-stu-id="90a09-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="90a09-554">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="90a09-554">Position types</span></span> 

<span data-ttu-id="90a09-555">Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet.</span><span class="sxs-lookup"><span data-stu-id="90a09-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="90a09-556">Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="90a09-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="90a09-557">Der kræves følgende stillingstyper og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="90a09-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="90a09-558">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="90a09-558">Position type</span></span>   | <span data-ttu-id="90a09-559">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="90a09-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="90a09-560">Fuld tid</span><span class="sxs-lookup"><span data-stu-id="90a09-560">Full-time</span></span>       | <span data-ttu-id="90a09-561">Fuldtidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="90a09-561">Full time employee</span></span> |
| <span data-ttu-id="90a09-562">Deltid</span><span class="sxs-lookup"><span data-stu-id="90a09-562">Part-time</span></span>       | <span data-ttu-id="90a09-563">Deltidsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="90a09-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="90a09-564">Årsagskoder</span><span class="sxs-lookup"><span data-stu-id="90a09-564">Reason codes</span></span>

<span data-ttu-id="90a09-565">Årsagskoder indeholder oplysninger om status for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="90a09-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="90a09-566">Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.</span><span class="sxs-lookup"><span data-stu-id="90a09-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="90a09-567">Der kræves følgende årsagskoder og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="90a09-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="90a09-568">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="90a09-568">Reason code</span></span>            | <span data-ttu-id="90a09-569">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="90a09-569">Description</span></span>                    | <span data-ttu-id="90a09-570">Anvendelige scenarier</span><span class="sxs-lookup"><span data-stu-id="90a09-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="90a09-571">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="90a09-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="90a09-572">Afgang før første løn</span><span class="sxs-lookup"><span data-stu-id="90a09-572">Departure before first payroll</span></span> | <span data-ttu-id="90a09-573">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="90a09-573">Terminate worker</span></span>     |
| <span data-ttu-id="90a09-574">OPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="90a09-574">RESIGNATION</span></span>            | <span data-ttu-id="90a09-575">Opsigelse</span><span class="sxs-lookup"><span data-stu-id="90a09-575">Resignation</span></span>                    | <span data-ttu-id="90a09-576">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="90a09-576">Terminate worker</span></span>     |
| <span data-ttu-id="90a09-577">PENSION</span><span class="sxs-lookup"><span data-stu-id="90a09-577">PENSION</span></span>                | <span data-ttu-id="90a09-578">Pension</span><span class="sxs-lookup"><span data-stu-id="90a09-578">Pension</span></span>                        | <span data-ttu-id="90a09-579">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="90a09-579">Terminate worker</span></span>     |
| <span data-ttu-id="90a09-580">OPHØR</span><span class="sxs-lookup"><span data-stu-id="90a09-580">TERMINATION</span></span>            | <span data-ttu-id="90a09-581">Ophør</span><span class="sxs-lookup"><span data-stu-id="90a09-581">Termination</span></span>                    | <span data-ttu-id="90a09-582">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="90a09-582">Terminate worker</span></span>     |
| <span data-ttu-id="90a09-583">PENSION</span><span class="sxs-lookup"><span data-stu-id="90a09-583">RETIREMENT</span></span>             | <span data-ttu-id="90a09-584">Pension</span><span class="sxs-lookup"><span data-stu-id="90a09-584">Retirement</span></span>                     | <span data-ttu-id="90a09-585">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="90a09-585">Terminate worker</span></span>     |
| <span data-ttu-id="90a09-586">FRAVÆRENDE</span><span class="sxs-lookup"><span data-stu-id="90a09-586">ABSENTEE</span></span>               | <span data-ttu-id="90a09-587">Fraværende</span><span class="sxs-lookup"><span data-stu-id="90a09-587">Absentee</span></span>                       | <span data-ttu-id="90a09-588">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="90a09-588">Terminate worker</span></span>     |
| <span data-ttu-id="90a09-589">ANDET</span><span class="sxs-lookup"><span data-stu-id="90a09-589">OTHER</span></span>                  | <span data-ttu-id="90a09-590">Andre årsager</span><span class="sxs-lookup"><span data-stu-id="90a09-590">Other Reasons</span></span>                  | <span data-ttu-id="90a09-591">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="90a09-591">Terminate worker</span></span>     |
| <span data-ttu-id="90a09-592">LUKNING</span><span class="sxs-lookup"><span data-stu-id="90a09-592">CLOSURE</span></span>                | <span data-ttu-id="90a09-593">Virksomhedslukning</span><span class="sxs-lookup"><span data-stu-id="90a09-593">Business Closure</span></span>               | <span data-ttu-id="90a09-594">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="90a09-594">Terminate worker</span></span>     |
| <span data-ttu-id="90a09-595">DØDSFALD</span><span class="sxs-lookup"><span data-stu-id="90a09-595">DEATH</span></span>                  | <span data-ttu-id="90a09-596">Dødsfald</span><span class="sxs-lookup"><span data-stu-id="90a09-596">Death</span></span>                          | <span data-ttu-id="90a09-597">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="90a09-597">Terminate worker</span></span>     |
| <span data-ttu-id="90a09-598">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="90a09-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="90a09-599">Orlov</span><span class="sxs-lookup"><span data-stu-id="90a09-599">Leave of Absence</span></span>               | <span data-ttu-id="90a09-600">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="90a09-600">Terminate worker</span></span>     |
| <span data-ttu-id="90a09-601">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="90a09-601">CONTRACTEND</span></span>            | <span data-ttu-id="90a09-602">Kontraktudløb</span><span class="sxs-lookup"><span data-stu-id="90a09-602">End of Contract</span></span>                | <span data-ttu-id="90a09-603">Lad arbejder fratræde</span><span class="sxs-lookup"><span data-stu-id="90a09-603">Terminate worker</span></span>     |
| <span data-ttu-id="90a09-604">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="90a09-604">SALARYCHANGE</span></span>           | <span data-ttu-id="90a09-605">Ændring af løn</span><span class="sxs-lookup"><span data-stu-id="90a09-605">Change of Salary</span></span>               | <span data-ttu-id="90a09-606">Kompensation</span><span class="sxs-lookup"><span data-stu-id="90a09-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="90a09-607">Ansættelsesvilkår</span><span class="sxs-lookup"><span data-stu-id="90a09-607">Terms of employment</span></span>

<span data-ttu-id="90a09-608">Ansættelsesvilkår bruges til at oprette kategorier for ansættelsesvilkår.</span><span class="sxs-lookup"><span data-stu-id="90a09-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="90a09-609">Vilkårene knyttes til Dayforce som beskæftigelsesindikatorværdier.</span><span class="sxs-lookup"><span data-stu-id="90a09-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="90a09-610">Følgende begreber for beskæftigelse og beskrivelser er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="90a09-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="90a09-611">Ansættelsesvilkår</span><span class="sxs-lookup"><span data-stu-id="90a09-611">Terms of employment</span></span>   | <span data-ttu-id="90a09-612">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="90a09-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="90a09-613">Regulær</span><span class="sxs-lookup"><span data-stu-id="90a09-613">Regular</span></span>               | <span data-ttu-id="90a09-614">Regulær</span><span class="sxs-lookup"><span data-stu-id="90a09-614">Regular</span></span>     |
| <span data-ttu-id="90a09-615">Direkte</span><span class="sxs-lookup"><span data-stu-id="90a09-615">Direct</span></span>                | <span data-ttu-id="90a09-616">Direkte</span><span class="sxs-lookup"><span data-stu-id="90a09-616">Direct</span></span>      |
| <span data-ttu-id="90a09-617">Turnustjeneste</span><span class="sxs-lookup"><span data-stu-id="90a09-617">Internship</span></span>            | <span data-ttu-id="90a09-618">Turnustjeneste</span><span class="sxs-lookup"><span data-stu-id="90a09-618">Internship</span></span>  |
| <span data-ttu-id="90a09-619">Permanent</span><span class="sxs-lookup"><span data-stu-id="90a09-619">Permanent</span></span>             | <span data-ttu-id="90a09-620">Permanent</span><span class="sxs-lookup"><span data-stu-id="90a09-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="90a09-621">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="90a09-621">Marital status</span></span>

<span data-ttu-id="90a09-622">Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="90a09-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="90a09-623">Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="90a09-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="90a09-624">Talent</span><span class="sxs-lookup"><span data-stu-id="90a09-624">Talent</span></span>                 | <span data-ttu-id="90a09-625">Dayforce</span><span class="sxs-lookup"><span data-stu-id="90a09-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="90a09-626">Gift</span><span class="sxs-lookup"><span data-stu-id="90a09-626">Married</span></span>                | <span data-ttu-id="90a09-627">Gift</span><span class="sxs-lookup"><span data-stu-id="90a09-627">Married</span></span>                   |
| <span data-ttu-id="90a09-628">Enlig</span><span class="sxs-lookup"><span data-stu-id="90a09-628">Single</span></span>                 | <span data-ttu-id="90a09-629">Enlig</span><span class="sxs-lookup"><span data-stu-id="90a09-629">Single</span></span>                    |
| <span data-ttu-id="90a09-630">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="90a09-630">Widowed</span></span>                | <span data-ttu-id="90a09-631">Enke/enkemand</span><span class="sxs-lookup"><span data-stu-id="90a09-631">Widowed</span></span>                   |
| <span data-ttu-id="90a09-632">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="90a09-632">Divorced</span></span>               | <span data-ttu-id="90a09-633">Fraskilt</span><span class="sxs-lookup"><span data-stu-id="90a09-633">Divorced</span></span>                  |
| <span data-ttu-id="90a09-634">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="90a09-634">Registered Partnership</span></span> | <span data-ttu-id="90a09-635">Registreret partnerskab</span><span class="sxs-lookup"><span data-stu-id="90a09-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="90a09-636">None</span><span class="sxs-lookup"><span data-stu-id="90a09-636">None</span></span>                   | <span data-ttu-id="90a09-637">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="90a09-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="90a09-638">Samlever</span><span class="sxs-lookup"><span data-stu-id="90a09-638">Cohabiting</span></span>             | <span data-ttu-id="90a09-639">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="90a09-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="90a09-640">Køn</span><span class="sxs-lookup"><span data-stu-id="90a09-640">Gender</span></span>

<span data-ttu-id="90a09-641">Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="90a09-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="90a09-642">Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="90a09-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="90a09-643">Talent</span><span class="sxs-lookup"><span data-stu-id="90a09-643">Talent</span></span>       | <span data-ttu-id="90a09-644">Dayforce</span><span class="sxs-lookup"><span data-stu-id="90a09-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="90a09-645">Mand</span><span class="sxs-lookup"><span data-stu-id="90a09-645">Male</span></span>         | <span data-ttu-id="90a09-646">Mand</span><span class="sxs-lookup"><span data-stu-id="90a09-646">Male</span></span>                      |
| <span data-ttu-id="90a09-647">Kvinde</span><span class="sxs-lookup"><span data-stu-id="90a09-647">Female</span></span>       | <span data-ttu-id="90a09-648">Kvinde</span><span class="sxs-lookup"><span data-stu-id="90a09-648">Female</span></span>                    |
| <span data-ttu-id="90a09-649">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="90a09-649">Non-specific</span></span> | <span data-ttu-id="90a09-650">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="90a09-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="90a09-651">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="90a09-651">Payment method</span></span>

<span data-ttu-id="90a09-652">Betalingsmetoder giver medarbejderen og virksomheden en måde til at beskrive, hvordan medarbejdere skal betales.</span><span class="sxs-lookup"><span data-stu-id="90a09-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="90a09-653">Betalingsmåder knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="90a09-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="90a09-654">Følgende tabel viser, hvordan betalingsmetoder knyttes til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="90a09-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="90a09-655">Talent</span><span class="sxs-lookup"><span data-stu-id="90a09-655">Talent</span></span>             | <span data-ttu-id="90a09-656">Dayforce</span><span class="sxs-lookup"><span data-stu-id="90a09-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="90a09-657">Indløsning</span><span class="sxs-lookup"><span data-stu-id="90a09-657">Cash</span></span>               | <span data-ttu-id="90a09-658">Indløsning</span><span class="sxs-lookup"><span data-stu-id="90a09-658">Cash</span></span>                      |
| <span data-ttu-id="90a09-659">Elektronisk betaling</span><span class="sxs-lookup"><span data-stu-id="90a09-659">Electronic Payment</span></span> | <span data-ttu-id="90a09-660">Ompostering</span><span class="sxs-lookup"><span data-stu-id="90a09-660">Transfer</span></span>                  |
| <span data-ttu-id="90a09-661">Check</span><span class="sxs-lookup"><span data-stu-id="90a09-661">Check</span></span>              | <span data-ttu-id="90a09-662">Check</span><span class="sxs-lookup"><span data-stu-id="90a09-662">Cheque</span></span>                    |
| <span data-ttu-id="90a09-663">Bankanvisning</span><span class="sxs-lookup"><span data-stu-id="90a09-663">Bank Draft</span></span>         | <span data-ttu-id="90a09-664">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="90a09-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="90a09-665">Andre</span><span class="sxs-lookup"><span data-stu-id="90a09-665">Other</span></span>              | <span data-ttu-id="90a09-666">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="90a09-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="90a09-667">Bankkontotype</span><span class="sxs-lookup"><span data-stu-id="90a09-667">Bank account type</span></span>

<span data-ttu-id="90a09-668">Bankkontotyper bruges til elektroniske betalinger til medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="90a09-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="90a09-669">Bankkontotyper knyttes til Dayforce som overførselskontooplysninger.</span><span class="sxs-lookup"><span data-stu-id="90a09-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="90a09-670">Bankkontotyperne oversættes efter behov til de accepterede værdier ved integration.</span><span class="sxs-lookup"><span data-stu-id="90a09-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="90a09-671">Talent</span><span class="sxs-lookup"><span data-stu-id="90a09-671">Talent</span></span>            | <span data-ttu-id="90a09-672">Dayforce</span><span class="sxs-lookup"><span data-stu-id="90a09-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="90a09-673">Checkkonto</span><span class="sxs-lookup"><span data-stu-id="90a09-673">Checking Account</span></span>  | <span data-ttu-id="90a09-674">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="90a09-674">CheckingAccount</span></span>           |
| <span data-ttu-id="90a09-675">Lønkonto</span><span class="sxs-lookup"><span data-stu-id="90a09-675">Payroll Account</span></span>   | <span data-ttu-id="90a09-676">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="90a09-676">PayrollAccount</span></span>            |
| <span data-ttu-id="90a09-677">Opsparingskonto</span><span class="sxs-lookup"><span data-stu-id="90a09-677">Savings Account</span></span>   | <span data-ttu-id="90a09-678">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="90a09-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="90a09-679">BankGirot-konto</span><span class="sxs-lookup"><span data-stu-id="90a09-679">BankGirot account</span></span> | <span data-ttu-id="90a09-680">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="90a09-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="90a09-681">PlusGirot-konto</span><span class="sxs-lookup"><span data-stu-id="90a09-681">PlusGirot account</span></span> | <span data-ttu-id="90a09-682">*Understøttes ikke af Mexico*</span><span class="sxs-lookup"><span data-stu-id="90a09-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="90a09-683">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="90a09-683">Earning codes</span></span>

<span data-ttu-id="90a09-684">Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager.</span><span class="sxs-lookup"><span data-stu-id="90a09-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="90a09-685">Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.</span><span class="sxs-lookup"><span data-stu-id="90a09-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="90a09-686">Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="90a09-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="90a09-687">Understøttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="90a09-687">Supported frequencies</span></span>

- <span data-ttu-id="90a09-688">Alt</span><span class="sxs-lookup"><span data-stu-id="90a09-688">All</span></span>
- <span data-ttu-id="90a09-689">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="90a09-689">EVERYPAY</span></span>
- <span data-ttu-id="90a09-690">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="90a09-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="90a09-691">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="90a09-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="90a09-692">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="90a09-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="90a09-693">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-693">1OFMTH</span></span>
- <span data-ttu-id="90a09-694">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-694">LASTOFMTH</span></span>
- <span data-ttu-id="90a09-695">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-695">2OFMTH</span></span>
- <span data-ttu-id="90a09-696">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-696">3OFMTH</span></span>
- <span data-ttu-id="90a09-697">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-697">4OFMTH</span></span>
- <span data-ttu-id="90a09-698">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-698">5OFMTH</span></span>
- <span data-ttu-id="90a09-699">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-699">1N2OFMTH</span></span>
- <span data-ttu-id="90a09-700">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-700">3N4OFMTH</span></span>
- <span data-ttu-id="90a09-701">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-701">1N3OFMTH</span></span>
- <span data-ttu-id="90a09-702">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-702">1N4OFMTH</span></span>
- <span data-ttu-id="90a09-703">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-703">2N3OFMTH</span></span>
- <span data-ttu-id="90a09-704">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-704">2N4OFMTH</span></span>
- <span data-ttu-id="90a09-705">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="90a09-706">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="90a09-707">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="90a09-708">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="90a09-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="90a09-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="90a09-710">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="90a09-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="90a09-711">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="90a09-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="90a09-712">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="90a09-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="90a09-713">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="90a09-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="90a09-714">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="90a09-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="90a09-715">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="90a09-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="90a09-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="90a09-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="90a09-717">Adresser</span><span class="sxs-lookup"><span data-stu-id="90a09-717">Addresses</span></span>

<span data-ttu-id="90a09-718">Identifikation af specifikke koder for land eller region, stat og område (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende.</span><span class="sxs-lookup"><span data-stu-id="90a09-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="90a09-719">Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.</span><span class="sxs-lookup"><span data-stu-id="90a09-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="90a09-720">Talent</span><span class="sxs-lookup"><span data-stu-id="90a09-720">Talent</span></span>              | <span data-ttu-id="90a09-721">Dayforce</span><span class="sxs-lookup"><span data-stu-id="90a09-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="90a09-722">Land/område</span><span class="sxs-lookup"><span data-stu-id="90a09-722">Country/Region</span></span>      | <span data-ttu-id="90a09-723">Landekode</span><span class="sxs-lookup"><span data-stu-id="90a09-723">Country Code</span></span>          |
| <span data-ttu-id="90a09-724">Postnummer</span><span class="sxs-lookup"><span data-stu-id="90a09-724">Zip/Postal Code</span></span>     | <span data-ttu-id="90a09-725">Postnummer</span><span class="sxs-lookup"><span data-stu-id="90a09-725">Postal Code</span></span>           |
| <span data-ttu-id="90a09-726">Status</span><span class="sxs-lookup"><span data-stu-id="90a09-726">State</span></span>               | <span data-ttu-id="90a09-727">Statskode</span><span class="sxs-lookup"><span data-stu-id="90a09-727">State Code</span></span>            |
| <span data-ttu-id="90a09-728">Bynavn</span><span class="sxs-lookup"><span data-stu-id="90a09-728">City</span></span>                | <span data-ttu-id="90a09-729">Bynavn</span><span class="sxs-lookup"><span data-stu-id="90a09-729">City</span></span>                  |
| <span data-ttu-id="90a09-730">Region</span><span class="sxs-lookup"><span data-stu-id="90a09-730">County</span></span>              | <span data-ttu-id="90a09-731">Område (kommune)</span><span class="sxs-lookup"><span data-stu-id="90a09-731">County (Municipality)</span></span> |
| <span data-ttu-id="90a09-732">Gade</span><span class="sxs-lookup"><span data-stu-id="90a09-732">Street</span></span>              | <span data-ttu-id="90a09-733">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="90a09-733">Address Line 1</span></span>        |
| <span data-ttu-id="90a09-734">Gadenummer</span><span class="sxs-lookup"><span data-stu-id="90a09-734">Street Number</span></span>       | <span data-ttu-id="90a09-735">Adresselinje 2</span><span class="sxs-lookup"><span data-stu-id="90a09-735">Address Line 2</span></span>        |
| <span data-ttu-id="90a09-736">Bygningskomplement</span><span class="sxs-lookup"><span data-stu-id="90a09-736">Building Complement</span></span> | <span data-ttu-id="90a09-737">Adresselinje 5</span><span class="sxs-lookup"><span data-stu-id="90a09-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="90a09-738">Pasnummer</span><span class="sxs-lookup"><span data-stu-id="90a09-738">Passport number</span></span>

<span data-ttu-id="90a09-739">Medarbejdere kan erklære pasoplysninger.</span><span class="sxs-lookup"><span data-stu-id="90a09-739">Employees can declare passport information.</span></span> <span data-ttu-id="90a09-740">Disse oplysninger er af identifikationstypen **Pas** og er integreret i Dayforce som en del af en medarbejders Mexico-specifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="90a09-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="90a09-741">Identifikationstype = "Pas"</span><span class="sxs-lookup"><span data-stu-id="90a09-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="90a09-742">Udstedt den</span><span class="sxs-lookup"><span data-stu-id="90a09-742">Issued Date</span></span>
- <span data-ttu-id="90a09-743">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="90a09-743">Expiration Date</span></span>

<span data-ttu-id="90a09-744">Medarbejdere kan angive flere identifikationsnumre af **Pas**-identifikationstypen.</span><span class="sxs-lookup"><span data-stu-id="90a09-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="90a09-745">Men det er kun den aktuelle aktive paspost, der integreres i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="90a09-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="90a09-746">Hvis alle pasposter er udløbet, integreres det pas, der senest blev udstedt, i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="90a09-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
