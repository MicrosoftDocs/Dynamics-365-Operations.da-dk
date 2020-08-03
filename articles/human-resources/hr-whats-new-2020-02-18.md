---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (18. februar 2020)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 60b46f5bd8f5eeae8aedc9bf81f1e7892caa0c93
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555333"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a><span data-ttu-id="290a4-103">Nyheder eller ændringer i Dynamics 365 Human Resources (18. februar 2020)</span><span class="sxs-lookup"><span data-stu-id="290a4-103">What's new or changed in Dynamics 365 Human Resources (February 18, 2020)</span></span>

<span data-ttu-id="290a4-104">I denne artikel beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="290a4-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="290a4-105">Ændringerne gælder for build nummer 8.1.2903.</span><span class="sxs-lookup"><span data-stu-id="290a4-105">Changes apply to build number 8.1.2903.</span></span> <span data-ttu-id="290a4-106">Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.</span><span class="sxs-lookup"><span data-stu-id="290a4-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="290a4-107">Platform update 32</span><span class="sxs-lookup"><span data-stu-id="290a4-107">Platform update 32</span></span> 

<span data-ttu-id="290a4-108">Platformsopdatering 32 er nu tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="290a4-108">Platform update 32 is now available.</span></span> <span data-ttu-id="290a4-109">Du kan finde flere oplysninger under [Nyheder eller ændringer i platformsopdatering 32 til Finance and Operations (februar 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span><span class="sxs-lookup"><span data-stu-id="290a4-109">For more information, see [What's new or changed in Platform update 32 for Finance and Operations (February 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span></span>

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a><span data-ttu-id="290a4-110">Søgeværdier huskes, når der ændres visningsindstillinger i den strømlinede medarbejderformular (383833)</span><span class="sxs-lookup"><span data-stu-id="290a4-110">Search values are remembered when changing view options in streamlined employee form (383833)</span></span>

<span data-ttu-id="290a4-111">Den nye formular **Arbejder** husker nu søgeværdier, når du ændrer visningsindstillingerne og anvender ændringer.</span><span class="sxs-lookup"><span data-stu-id="290a4-111">The new **Worker** form now remembers  search values when you change the view options and apply changes.</span></span>

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a><span data-ttu-id="290a4-112">Oversigtsfelter for kompensationsstyring i visningsfunktionen omdirigeres til forkert formular (401861)</span><span class="sxs-lookup"><span data-stu-id="290a4-112">Compensation management summary tiles in preview feature redirect to wrong form (401861)</span></span>

<span data-ttu-id="290a4-113">I de faste og variable kompensationsstyringsfelter vises nu de korrekte poster i den nye **Arbejder**-formular.</span><span class="sxs-lookup"><span data-stu-id="290a4-113">Fixed and variable compensation management tiles now display the correct records in the new **Worker** form.</span></span> <span data-ttu-id="290a4-114">Gælder kun for eksempelfunktionen i den strømlinede medarbejderformular.</span><span class="sxs-lookup"><span data-stu-id="290a4-114">Applies only to the streamlined employee form preview feature.</span></span> <span data-ttu-id="290a4-115">Du kan aktivere denne visningsfunktion i **Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="290a4-115">You can enable this preview feature in **Feature management**.</span></span> <span data-ttu-id="290a4-116">Du kan finde flere oplysninger under [Administrere funktioner](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="290a4-116">For more information, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="empty-status-field-for-some-leave-request-records-in-common-data-service-414915"></a><span data-ttu-id="290a4-117">Tomt Status-felt for nogle orlovsanmodningsposter i Common Data Service (414915)</span><span class="sxs-lookup"><span data-stu-id="290a4-117">Empty Status field for some leave request records in Common Data Service (414915)</span></span>

<span data-ttu-id="290a4-118">Denne ændring løser et problem i Common Data Service, når feltet **Status** i en orlovsanmodning er indstillet til **Gennemsyn**.</span><span class="sxs-lookup"><span data-stu-id="290a4-118">This change corrects an issue in Common Data Service when the **Status** field in a leave request is set to **Review**.</span></span> <span data-ttu-id="290a4-119">Common Data Service afspejler nu statussen.</span><span class="sxs-lookup"><span data-stu-id="290a4-119">Common Data Service now reflects the status.</span></span>

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a><span data-ttu-id="290a4-120">Analyse af kompetencekløft er kun mulig for tildelt job (411390)</span><span class="sxs-lookup"><span data-stu-id="290a4-120">Skill gap analysis only possible for assigned job (411390)</span></span>

<span data-ttu-id="290a4-121">Du kan nu foretage en analyse af kompetencekløft på et job, der er defineret i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="290a4-121">You can now do a skill gap analysis on any job defined in Human Resources.</span></span>

## <a name="system-currency-doesnt-sync-from-common-data-service-to-human-resources-in-new-environments-418011"></a><span data-ttu-id="290a4-122">Systemvaluta synkroniseres ikke fra Common Data Service til Human Resources i nye miljøer (418011)</span><span class="sxs-lookup"><span data-stu-id="290a4-122">System currency doesn't sync from Common Data Service to Human Resources in new environments (418011)</span></span>

<span data-ttu-id="290a4-123">Systemvalutaen i Common Data Service kan nu synkroniseres til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="290a4-123">The system currency in Common Data Service can now sync to Human Resources.</span></span>

## <a name="in-preview"></a><span data-ttu-id="290a4-124">Som eksempel</span><span class="sxs-lookup"><span data-stu-id="290a4-124">In preview</span></span>

- [<span data-ttu-id="290a4-125">Visningsfunktioner for orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="290a4-125">Leave and absence preview features</span></span>](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [<span data-ttu-id="290a4-126">Prøveversionsfunktion til Administration af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="290a4-126">Benefits management preview features</span></span>](hr-benefits-management-overview.md)

## <a name="coming-soon"></a><span data-ttu-id="290a4-127">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="290a4-127">Coming soon</span></span>

### <a name="updated-common-data-service-solution"></a><span data-ttu-id="290a4-128">Opdateret Common Data Service-løsning</span><span class="sxs-lookup"><span data-stu-id="290a4-128">Updated Common Data Service solution</span></span>

<span data-ttu-id="290a4-129">Der vil snart være en ny Common Data Service-løsning med følgende ændringer:</span><span class="sxs-lookup"><span data-stu-id="290a4-129">A new Common Data Service solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="290a4-130">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="290a4-130">Description</span></span> | <span data-ttu-id="290a4-131">Forskydning</span><span class="sxs-lookup"><span data-stu-id="290a4-131">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="290a4-132">Ændringer i objektet **Job/Stilling**</span><span class="sxs-lookup"><span data-stu-id="290a4-132">**Job/Position** entity changes</span></span> | <span data-ttu-id="290a4-133">**Kompensationsområde** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="290a4-133">**Compensation region** added</span></span></br><span data-ttu-id="290a4-134">**Økonomiske dimensioner** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="290a4-134">**Financial dimensions** added</span></span> |
| <span data-ttu-id="290a4-135">Ændringer i objektet **Arbejder**</span><span class="sxs-lookup"><span data-stu-id="290a4-135">**Worker** entity changes</span></span> | <span data-ttu-id="290a4-136">**Navnerækkefølge** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="290a4-136">**Name sequence** added</span></span></br><span data-ttu-id="290a4-137">**Arbejder hjemmefra** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="290a4-137">**Works from home** added</span></span></br><span data-ttu-id="290a4-138">**Sprog** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="290a4-138">**Language** added</span></span></br><span data-ttu-id="290a4-139">**Anciennitetsdato** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="290a4-139">**Seniority date** added</span></span></br><span data-ttu-id="290a4-140">**Jubilæumsdato** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="290a4-140">**Anniversary date** added</span></span></br><span data-ttu-id="290a4-141">**Oprindelig ansættelsesdato** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="290a4-141">**Original hire date** added</span></span> |
| <span data-ttu-id="290a4-142">Ændringer af objektet **Ansættelse**</span><span class="sxs-lookup"><span data-stu-id="290a4-142">**Employment** entity changes</span></span> | <span data-ttu-id="290a4-143">**Økonomiske dimensioner** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="290a4-143">**Financial dimensions** added</span></span></br><span data-ttu-id="290a4-144">**Årsag til fratrædelse** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="290a4-144">**Termination reason** added</span></span></br><span data-ttu-id="290a4-145">**Fratrædelsesdato** er omdøbt fra **Overførselsdato**</span><span class="sxs-lookup"><span data-stu-id="290a4-145">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="290a4-146">**Datoer for prøvetid** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="290a4-146">**Probation date** added</span></span> |
| <span data-ttu-id="290a4-147">Ændringer i objektet **Arbejders adresse**</span><span class="sxs-lookup"><span data-stu-id="290a4-147">**Worker address** entity changes</span></span> | <span data-ttu-id="290a4-148">**Gadenavn** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="290a4-148">**Street address** added</span></span></br><span data-ttu-id="290a4-149">**Adresselinje 1**, **Adresselinje 2** og **Adresselinje 3** er markeret til udfasning</span><span class="sxs-lookup"><span data-stu-id="290a4-149">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="290a4-150">Nye konfigurationsobjekter til variabel kompensation</span><span class="sxs-lookup"><span data-stu-id="290a4-150">New variable compensation setup entities</span></span> | <span data-ttu-id="290a4-151">**Type af variabel kompensationsplan**</span><span class="sxs-lookup"><span data-stu-id="290a4-151">**Compensation variable plan type**</span></span></br><span data-ttu-id="290a4-152">**Kompensation - variabel struktur**</span><span class="sxs-lookup"><span data-stu-id="290a4-152">**Compensation variable plan**</span></span></br><span data-ttu-id="290a4-153">**Fordelingsregler**</span><span class="sxs-lookup"><span data-stu-id="290a4-153">**Vesting rules**</span></span></br><span data-ttu-id="290a4-154">**Niveau i variabel kompensationsplan**</span><span class="sxs-lookup"><span data-stu-id="290a4-154">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="290a4-155">Nyt objekt **Arbejderkalender for ansættelse**</span><span class="sxs-lookup"><span data-stu-id="290a4-155">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="290a4-156">**Arbejdskalenderobjekt** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="290a4-156">**Work calendar entity** added</span></span> |
| <span data-ttu-id="290a4-157">Nyt objekt **Lønoplysninger for stillinger**</span><span class="sxs-lookup"><span data-stu-id="290a4-157">New **Payroll position detail** entity</span></span> | <span data-ttu-id="290a4-158">**Lønoplysninger for stillinger** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="290a4-158">**Payroll position detail** added</span></span> |
| <span data-ttu-id="290a4-159">Nyt objekt **Titel**</span><span class="sxs-lookup"><span data-stu-id="290a4-159">New **Title** entity</span></span> | <span data-ttu-id="290a4-160">**Titel** er tilføjet.</span><span class="sxs-lookup"><span data-stu-id="290a4-160">**Title** added.</span></span> <span data-ttu-id="290a4-161">Den nye enhed **Titel** vil blive medtaget i synkroniseringsprocessen mellem Human Resources og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="290a4-161">The new **Title** entity will be included in the sync process between Human Resources and Common Data Service.</span></span> <span data-ttu-id="290a4-162">Der henvises ikke til den først i enhederne **Stilling** eller **Job**.</span><span class="sxs-lookup"><span data-stu-id="290a4-162">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

## <a name="see-also"></a><span data-ttu-id="290a4-163">Se også</span><span class="sxs-lookup"><span data-stu-id="290a4-163">See also</span></span>

[<span data-ttu-id="290a4-164">Nyheder eller ændringer i Human Resources</span><span class="sxs-lookup"><span data-stu-id="290a4-164">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="290a4-165">Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2</span><span class="sxs-lookup"><span data-stu-id="290a4-165">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="290a4-166">Opdater proces</span><span class="sxs-lookup"><span data-stu-id="290a4-166">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="290a4-167">Administrere funktioner</span><span class="sxs-lookup"><span data-stu-id="290a4-167">Manage features</span></span>](hr-admin-manage-features.md)