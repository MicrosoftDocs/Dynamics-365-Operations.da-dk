---
title: Konfigurere personaleparametre
description: Dette emne forklarer, hvordan du konfigurerer virksomhedsspecifikke parametre i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cd66cb4f5ac02407250e15ae134b36f5ccd4d290
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889926"
---
# <a name="configure-human-resources-parameters"></a><span data-ttu-id="0f61f-103">Konfigurere personaleparametre</span><span class="sxs-lookup"><span data-stu-id="0f61f-103">Configure Human resources parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0f61f-104">Indstillingerne for nogle personaleparametre deles på tværs af firmaer, mens indstillingerne af andre parametre er firmaspecifikke.</span><span class="sxs-lookup"><span data-stu-id="0f61f-104">The settings of some Human resources parameters are shared across companies, while the settings of other parameters are company-specific.</span></span> <span data-ttu-id="0f61f-105">Dette emne forklarer, hvordan du konfigurerer firmaspecifikke personaleparametre.</span><span class="sxs-lookup"><span data-stu-id="0f61f-105">This topic explains how to set up company-specific Human resources parameters.</span></span>

<span data-ttu-id="0f61f-106">To sider bruges til at angive personaleparametre.</span><span class="sxs-lookup"><span data-stu-id="0f61f-106">Two pages are used to set Human resources parameters.</span></span> <span data-ttu-id="0f61f-107">For parametre, der deles på tværs af firmaer, skal du bruge siden **Delte parametre for personale**.</span><span class="sxs-lookup"><span data-stu-id="0f61f-107">For parameters that are shared across companies, you use the **Human resources shared parameters** page.</span></span> <span data-ttu-id="0f61f-108">For parametre, der er specifikke for virksomheden (med andre ord gælder indstillingerne for en enkelt virksomhed), skal du bruge siden **Human Resourcesparametre**.</span><span class="sxs-lookup"><span data-stu-id="0f61f-108">For parameters that are company-specific (in other words, the settings apply to a single company), you use the **Human resource parameters** page.</span></span>

![Gå til Personaleparametre](./media/hr-employee-self-service-human-resources-parameters.png)

<span data-ttu-id="0f61f-110">På siden **Human Resourcesparametre** er indstillingerne fordelt på seks faner:</span><span class="sxs-lookup"><span data-stu-id="0f61f-110">On the **Human resources parameters** page, the settings are divided among six tabs:</span></span>

- <span data-ttu-id="0f61f-111">**Generel**</span><span class="sxs-lookup"><span data-stu-id="0f61f-111">**General**</span></span>
- <span data-ttu-id="0f61f-112">**Rekruttering** (denne fane er ikke inkluderet i Dynamics 365 Human Resources)</span><span class="sxs-lookup"><span data-stu-id="0f61f-112">**Recruitment** (this tab isn't included in Dynamics 365 Human Resources)</span></span>
- <span data-ttu-id="0f61f-113">**Kompensation**</span><span class="sxs-lookup"><span data-stu-id="0f61f-113">**Compensation**</span></span>
- <span data-ttu-id="0f61f-114">**Nummerserier**</span><span class="sxs-lookup"><span data-stu-id="0f61f-114">**Number sequences**</span></span>
- <span data-ttu-id="0f61f-115">**FMLA**</span><span class="sxs-lookup"><span data-stu-id="0f61f-115">**FMLA**</span></span>
- <span data-ttu-id="0f61f-116">**Medarbejderselvbetjening**</span><span class="sxs-lookup"><span data-stu-id="0f61f-116">**Employee self service**</span></span>
- <span data-ttu-id="0f61f-117">**Selvbetjening for leder**</span><span class="sxs-lookup"><span data-stu-id="0f61f-117">**Manager self service**</span></span>
- <span data-ttu-id="0f61f-118">**Frynsegodeadministration**</span><span class="sxs-lookup"><span data-stu-id="0f61f-118">**Benefits management**</span></span>
- <span data-ttu-id="0f61f-119">**Orlov og fravær**</span><span class="sxs-lookup"><span data-stu-id="0f61f-119">**Leave and absence**</span></span>
- <span data-ttu-id="0f61f-120">**Betalingsmetoder**</span><span class="sxs-lookup"><span data-stu-id="0f61f-120">**Payment methods**</span></span>

<span data-ttu-id="0f61f-121">Hver fane indeholder oplysninger, der vedrører en enkelt virksomhed.</span><span class="sxs-lookup"><span data-stu-id="0f61f-121">Each tab contains information that pertains to a single company.</span></span>

## <a name="general"></a><span data-ttu-id="0f61f-122">Generel</span><span class="sxs-lookup"><span data-stu-id="0f61f-122">General</span></span>

<span data-ttu-id="0f61f-123">Indstillingerne på fanen **Generelt** definerer visningen af oplysninger om fravær, skader og sygdom og nye ansættelser.</span><span class="sxs-lookup"><span data-stu-id="0f61f-123">The settings on the **General** tab define the appearance of information about absence, injury and illness, and new hires.</span></span> <span data-ttu-id="0f61f-124">Indstillingerne på denne fane kan også definere nogle standardposter, der vises, mens du arbejder.</span><span class="sxs-lookup"><span data-stu-id="0f61f-124">The settings on this tab also define some default entries that appear as you work.</span></span> <span data-ttu-id="0f61f-125">Denne fane giver dig mulighed for at:</span><span class="sxs-lookup"><span data-stu-id="0f61f-125">Specifically, this tab lets you:</span></span>

- <span data-ttu-id="0f61f-126">Vælge den farve, der skal anvendes på åbne fraværsposter</span><span class="sxs-lookup"><span data-stu-id="0f61f-126">Select a color to apply to open absence transactions</span></span>
- <span data-ttu-id="0f61f-127">Angive det typografiark, der skal bruges til rapporter</span><span class="sxs-lookup"><span data-stu-id="0f61f-127">Specify the style sheet to use for reports</span></span>
- <span data-ttu-id="0f61f-128">Aktivere integration mellem kurser og fraværsregistrering</span><span class="sxs-lookup"><span data-stu-id="0f61f-128">Enable the integration between training courses and absence registration</span></span>
- <span data-ttu-id="0f61f-129">Vælg den fraværskode, der bruges til at styre denne integration.</span><span class="sxs-lookup"><span data-stu-id="0f61f-129">Select the absence code that is used to control this integration.</span></span>
- <span data-ttu-id="0f61f-130">Angiv, hvor længe hændelser med skades- og sygdomstilfælde skal opbevares.</span><span class="sxs-lookup"><span data-stu-id="0f61f-130">Indicate how long to keep injury and illness case incidents.</span></span>
- <span data-ttu-id="0f61f-131">Angiv det standard-id, der vises, når der ansættes en ny arbejder.</span><span class="sxs-lookup"><span data-stu-id="0f61f-131">Specify the default identification number shown when a new worker is hired.</span></span>

![Fanen Generelt](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a><span data-ttu-id="0f61f-133">Rekruttering</span><span class="sxs-lookup"><span data-stu-id="0f61f-133">Recruitment</span></span>

<span data-ttu-id="0f61f-134">Indstillingerne under fanen **Rekruttering** definerer de dokumenttyper, der bruges til korrespondance, som automatisk sendes til ansøgere.</span><span class="sxs-lookup"><span data-stu-id="0f61f-134">The settings on the **Recruitment** tab define the document types used for correspondence automatically sent to applicants.</span></span> <span data-ttu-id="0f61f-135">Du kan også angive det rekrutteringsprojekt, der bruges til uopfordrede ansøgninger.</span><span class="sxs-lookup"><span data-stu-id="0f61f-135">You can also indicate the recruitment project used for unsolicited applications.</span></span>

<span data-ttu-id="0f61f-136">Den periode, der er defineret for det aldersfordelte rekrutteringsprojekt bestemmer rekrutteringsprojekter, der er medtaget i feltet **Aldersfordelte projekter** i arbejdsområdet **Rekrutteringsstyring**.</span><span class="sxs-lookup"><span data-stu-id="0f61f-136">The period defined for recruitment project aging determines the recruitment projects included on the **Aging projects** tile in the **Recruitment management** workspace.</span></span> <span data-ttu-id="0f61f-137">Den periode, der er defineret for advarsel om deadline for ansøgning bruges til at få vist rekrutteringsprojekter, der nærmer sig deres ansøgningsfrist i feltet den **Deadline for ansøgning nærmer sig** i arbejdsområdet **Rekruttering**.</span><span class="sxs-lookup"><span data-stu-id="0f61f-137">The period defined for the application deadline warning is used to display recruitment projects that are approaching their application deadline on the **Application deadline approaching** tile in the **Recruitment** workspace.</span></span>

<span data-ttu-id="0f61f-138">Du kan finde flere oplysninger om rekruttering under [Rekruttere jobkandidater](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="0f61f-138">For more information about recruiting, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="compensation"></a><span data-ttu-id="0f61f-139">Kompensation</span><span class="sxs-lookup"><span data-stu-id="0f61f-139">Compensation</span></span>

<span data-ttu-id="0f61f-140">I Dynamics 365 Finance definerer indstillingerne under fanen **Kompensation**, om brugere skal bekræfte, at de vil gemme oplysninger om en fast eller variabel lønstruktur.</span><span class="sxs-lookup"><span data-stu-id="0f61f-140">In Dynamics 365 Finance, the settings on the **Compensation** tab define whether users must confirm that they want to save information for a fixed or variable compensation plan.</span></span> <span data-ttu-id="0f61f-141">Hvis du vælger **Aktivér validering ved lagring**, får brugerne vist en meddelelse, når de lukker en kompensationsrelateret side, hvor de bliver spurgt, om de vil gemme posten.</span><span class="sxs-lookup"><span data-stu-id="0f61f-141">If you select **Enable save validation**, when users close a compensation-related page, they receive a message that asks whether they want to save the record.</span></span> <span data-ttu-id="0f61f-142">Nogle sider i Kompensationsstyring giver ikke brugerne mulighed for at slette information.</span><span class="sxs-lookup"><span data-stu-id="0f61f-142">Some pages in Compensation management don't let users delete information.</span></span> <span data-ttu-id="0f61f-143">Når brugeren får besked på at bekræfte, om oplysningerne skal gemmes, kan det hjælpe med at begrænse mængden af oplysninger, der gemmes, men ikke senere kan slettes.</span><span class="sxs-lookup"><span data-stu-id="0f61f-143">By prompting users to verify that they want to save information, you might be able to limit the amount of information that is saved but can't be deleted later.</span></span> <span data-ttu-id="0f61f-144">Hvis du rydder **Aktivér validering ved lagring**, gemmes poster med det samme, eventuelt før brugeren er klar.</span><span class="sxs-lookup"><span data-stu-id="0f61f-144">If you clear **Enable save validation**, records save immediately, possibly before the user is ready.</span></span> <span data-ttu-id="0f61f-145">Hvis du bruger Performancestyring, giver fanen **Kompensation** dig også mulighed for at vælge en rangeringsmodel, der skal bruges i stedet for den model, der er tildelt til kompensationsstrukturerne, når performance vurderes.</span><span class="sxs-lookup"><span data-stu-id="0f61f-145">If you're using Performance management, the **Compensation** tab also lets you select a rating model to use instead of the model assigned to compensation plans when rating performance.</span></span>

<span data-ttu-id="0f61f-146">I Human Resources kan du bruge fanen **Kompensation** til at vælge at begrænse adgangen til kompensationsplaner og angive en standardvaluta.</span><span class="sxs-lookup"><span data-stu-id="0f61f-146">In Human Resources, you can use the **Compensation** tab to choose to restrict access to compensation plans and to set a default currency.</span></span>

<span data-ttu-id="0f61f-147">Du kan finde flere oplysninger om kompensation under [Oversigt over lønstrukturer](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0f61f-147">For more information about compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Fanen Kompensation](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a><span data-ttu-id="0f61f-149">Nummerserier</span><span class="sxs-lookup"><span data-stu-id="0f61f-149">Number sequences</span></span>

<span data-ttu-id="0f61f-150">Indstillingerne under fanen **Nummerserie** bestemmer, hvilke nummerserier der bruges til automatisk at tildele elementer id'er i Human Resources, f.eks.:</span><span class="sxs-lookup"><span data-stu-id="0f61f-150">The settings on the **Number sequence** tab determine the sequences used to automatically assign IDs to items in Human Resources, such as:</span></span>

- <span data-ttu-id="0f61f-151">Anvendelser</span><span class="sxs-lookup"><span data-stu-id="0f61f-151">Applications</span></span>
- <span data-ttu-id="0f61f-152">Fraværsregistreringer</span><span class="sxs-lookup"><span data-stu-id="0f61f-152">Absence registrations</span></span>
- <span data-ttu-id="0f61f-153">Resultater af kompensationsproces</span><span class="sxs-lookup"><span data-stu-id="0f61f-153">Compensation process results</span></span>
- <span data-ttu-id="0f61f-154">Sagsnumre</span><span class="sxs-lookup"><span data-stu-id="0f61f-154">Case numbers</span></span>
- <span data-ttu-id="0f61f-155">Kurser</span><span class="sxs-lookup"><span data-stu-id="0f61f-155">Courses</span></span>
- <span data-ttu-id="0f61f-156">Kursusagendaer</span><span class="sxs-lookup"><span data-stu-id="0f61f-156">Course agendas</span></span>

<span data-ttu-id="0f61f-157">Hvis du vil vedligeholde nummerseriereferencer og -koder skal du bruge listesiden **Nummerserier** (vælg **Organisationsadministration > Nummerserier > Nummerserier**).</span><span class="sxs-lookup"><span data-stu-id="0f61f-157">To maintain number sequence references and codes, use the **Number sequences** list page (select **Organization administration > Number sequences > Number sequences**).</span></span>

<span data-ttu-id="0f61f-158">Du kan finde flere oplysninger under [Oversigt over nummerserier](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="0f61f-158">For more information, see [Number sequences overview](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

> [!NOTE]
> <span data-ttu-id="0f61f-159">Antallet af timer, der er arbejdet, må ikke overstige 1.250, og længden af beskæftigelsen må ikke overstige 12 måneder.</span><span class="sxs-lookup"><span data-stu-id="0f61f-159">The number of hours that are worked can't exceed 1,250, and the length of employment can't exceed 12 months.</span></span> <span data-ttu-id="0f61f-160">Disse maksimale værdier er i overensstemmelse med gældende lovgivning i USA.</span><span class="sxs-lookup"><span data-stu-id="0f61f-160">These maximum values are in accordance with federal law in the United States.</span></span>

![Fanen Nummerserier](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a><span data-ttu-id="0f61f-162">FMLA</span><span class="sxs-lookup"><span data-stu-id="0f61f-162">FMLA</span></span>

<span data-ttu-id="0f61f-163">Du kan angive FMLA-berettigelseskrav og FMLA-berettigelsestimer under fanen FMLA.</span><span class="sxs-lookup"><span data-stu-id="0f61f-163">On the FMLA tab, you set FMLA eligibility requirements and FMLA entitlement hours.</span></span> <span data-ttu-id="0f61f-164">Du kan finde flere oplysninger i [Konfigurere orlovs- og fraværsparametre](hr-leave-and-absence-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0f61f-164">For more information, see [Configure leave and absence parameters](hr-leave-and-absence-parameters.md).</span></span>

![Fanen FMLA](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a><span data-ttu-id="0f61f-166">Medarbejderselvbetjening</span><span class="sxs-lookup"><span data-stu-id="0f61f-166">Employee self service</span></span>

<span data-ttu-id="0f61f-167">Indstillingerne under fanen **Medarbejderselvbetjening** har indflydelse på, hvordan medarbejderens selvbetjening vises for medarbejderne.</span><span class="sxs-lookup"><span data-stu-id="0f61f-167">The settings on the **Employee self service** tab affect how Employee self service appears to employees.</span></span> <span data-ttu-id="0f61f-168">Under denne fane kan du:</span><span class="sxs-lookup"><span data-stu-id="0f61f-168">On this tab, you can:</span></span>

- <span data-ttu-id="0f61f-169">Angive et navn i arbejdsområdet Medarbejderselvbetjening</span><span class="sxs-lookup"><span data-stu-id="0f61f-169">Enter a name for the Employee self service workspace</span></span>
- <span data-ttu-id="0f61f-170">Vælge, hvilke oplysninger en leder kan angive for medarbejdere</span><span class="sxs-lookup"><span data-stu-id="0f61f-170">Select which information a manager can enter for employees</span></span>
- <span data-ttu-id="0f61f-171">Tilføje nyttige links for medarbejdere</span><span class="sxs-lookup"><span data-stu-id="0f61f-171">Add useful links for employees</span></span>
- <span data-ttu-id="0f61f-172">Begrænse medarbejdere i at tilføje eller redigere forretningskontaktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="0f61f-172">Restrict employees from adding or editing business contact details.</span></span> <span data-ttu-id="0f61f-173">Du kan finde flere oplysninger i [Begrænse redigering af personlige oplysninger](hr-employee-self-service-restrict-editing.md).</span><span class="sxs-lookup"><span data-stu-id="0f61f-173">For more information, see [Restrict editing of personal information](hr-employee-self-service-restrict-editing.md).</span></span>

<span data-ttu-id="0f61f-174">Du kan finde flere oplysninger om opsætning af medarbejderselvbetjening i [Oversigt over medarbejder- og lederselvbetjening](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0f61f-174">For more information about setting up Employee self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Fanen Medarbejderselvbetjening](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a><span data-ttu-id="0f61f-176">Selvbetjening for leder</span><span class="sxs-lookup"><span data-stu-id="0f61f-176">Manager self service</span></span>

<span data-ttu-id="0f61f-177">Indstillingerne under fanen **Selvbetjening for leder** har indflydelse på, hvad lederne kan se i Selvbetjening for leder.</span><span class="sxs-lookup"><span data-stu-id="0f61f-177">The settings on the **Manager self service** tab affect what managers see in Manager self service.</span></span> <span data-ttu-id="0f61f-178">Under denne fane kan du konfigurere følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0f61f-178">On this tab, you can configure the following options:</span></span>

- <span data-ttu-id="0f61f-179">Intervallet for udløb af poster</span><span class="sxs-lookup"><span data-stu-id="0f61f-179">The range for expiring records</span></span>
- <span data-ttu-id="0f61f-180">Informationschefer kan se udløb af poster</span><span class="sxs-lookup"><span data-stu-id="0f61f-180">Information managers can view in expiring records</span></span>
- <span data-ttu-id="0f61f-181">Om ledere kan se ledige stillinger til udvidede underordnede</span><span class="sxs-lookup"><span data-stu-id="0f61f-181">Whether managers can view open positions for extended reports</span></span>
- <span data-ttu-id="0f61f-182">Visninger af fratrædende arbejdere</span><span class="sxs-lookup"><span data-stu-id="0f61f-182">Views of exiting workers</span></span>
- <span data-ttu-id="0f61f-183">Nyttige links for ledere</span><span class="sxs-lookup"><span data-stu-id="0f61f-183">Useful links for managers</span></span>

<span data-ttu-id="0f61f-184">Du kan finde flere oplysninger om opsætning af lederselvbetjening i [Oversigt over medarbejder- og lederselvbetjening](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0f61f-184">For more information about setting up Manager self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Fanen Selvbetjening for leder](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a><span data-ttu-id="0f61f-186">Frynsegodeadministration</span><span class="sxs-lookup"><span data-stu-id="0f61f-186">Benefits management</span></span>

<span data-ttu-id="0f61f-187">Under fanen Frynsegodeadministration kan du konfigurere mailindstillinger for Frynsegodeadministration.</span><span class="sxs-lookup"><span data-stu-id="0f61f-187">On the Benefits management tab, you can configure email options for Benefits management.</span></span> <span data-ttu-id="0f61f-188">Du kan finde flere oplysninger om konfiguration og brug af Frynsegodeadministration i [Oversigt over Administration af frynsegoder](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0f61f-188">For information about setting up and using Benefits management, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

![Fanen Frynsegodeadministration](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a><span data-ttu-id="0f61f-190">Orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="0f61f-190">Leave and absence</span></span>

<span data-ttu-id="0f61f-191">Du kan finde flere oplysninger om opsætning og brug af orlov og fravær under [Oversigt over orlov og fravær](hr-leave-and-absence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0f61f-191">For information about setting up and using Leave and absence, see [Leave and absence overview](hr-leave-and-absence-overview.md).</span></span>

## <a name="payment-methods"></a><span data-ttu-id="0f61f-192">Betalingsmetoder</span><span class="sxs-lookup"><span data-stu-id="0f61f-192">Payment methods</span></span>

<span data-ttu-id="0f61f-193">Under fanen **Betalingsmetoder** kan du vælge de betalingsmetoder, der understøttes af din organisation.</span><span class="sxs-lookup"><span data-stu-id="0f61f-193">On the **Payment methods** tab, you can select the payment methods supported by your organization.</span></span> <span data-ttu-id="0f61f-194">Du kan finde flere oplysninger om konfiguration af kompensation under [Oversigt over lønstrukturer](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0f61f-194">For more information about configuring compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Fanen Betalingsmetoder](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]