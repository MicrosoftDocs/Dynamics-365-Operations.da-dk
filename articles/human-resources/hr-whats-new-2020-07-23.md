---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (23. juli 2020)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 23. juli 2020.
author: Darinkramer
manager: AnnBe
ms.date: 07/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 30662ccf7e37f7f1e131e3b18b5a770c53fea0d1
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/20/2020
ms.locfileid: "3711862"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a><span data-ttu-id="2bde6-103">Nyheder eller ændringer i Dynamics 365 Human Resources (23. juli 2020)</span><span class="sxs-lookup"><span data-stu-id="2bde6-103">What's new or changed in Dynamics 365 Human Resources (July 23, 2020)</span></span>

<span data-ttu-id="2bde6-104">I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2bde6-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2bde6-105">Ændringerne gælder for build nummer 8.1.3416.</span><span class="sxs-lookup"><span data-stu-id="2bde6-105">Changes apply to build number 8.1.3416.</span></span> <span data-ttu-id="2bde6-106">Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.</span><span class="sxs-lookup"><span data-stu-id="2bde6-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a><span data-ttu-id="2bde6-107">Sletning af økonomiske dimensioner på en stilling fungerer ikke som forventet (445476)</span><span class="sxs-lookup"><span data-stu-id="2bde6-107">Deleting Financial Dimensions on a Position doesn't work as expected (445476)</span></span>

<span data-ttu-id="2bde6-108">Hvis du fjerner dimensioner fra en stilling, fjerner du nu de samme stillinger fra Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="2bde6-108">Removing dimensions from a position now removes those same positions from Common Data Service.</span></span>

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a><span data-ttu-id="2bde6-109">Stillinger, der ikke er i hierarki, viser inaktive stillinger (397257)</span><span class="sxs-lookup"><span data-stu-id="2bde6-109">Positions not in hierarchy show inactive positions (397257)</span></span>

<span data-ttu-id="2bde6-110">Stillinger, der er inaktive (har en udløbet varighed), vises ikke længere i stillingshierarkiet som **Stillinger, der ikke er i hierarki**.</span><span class="sxs-lookup"><span data-stu-id="2bde6-110">Positions that are inactive (have an expired duration), no longer display in the position hierarchy as **Positions not in hierarchy**.</span></span> 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a><span data-ttu-id="2bde6-111">Validering, der sker mellem LeaveEnrollmentEntity og HcmWorkerEntity under import af Data Management Framework (DMF), medfører langsom dataindlæsning (442324)</span><span class="sxs-lookup"><span data-stu-id="2bde6-111">Validation occurring between LeaveEnrollmentEntity and HcmWorkerEntity on Data Management Framework (DMF) import causes slow data loads (442324)</span></span>

<span data-ttu-id="2bde6-112">Ændringer i denne frigivelse øger ydeevnen af **LeaveEnrollmentEntity**.</span><span class="sxs-lookup"><span data-stu-id="2bde6-112">Changes in this release increase the performance of **LeaveEnrollmentEntity**.</span></span>

## <a name="unable-to-personalize-in-organization-administration-447490"></a><span data-ttu-id="2bde6-113">Det er ikke muligt at tilpasse i organisationsadministration (447490)</span><span class="sxs-lookup"><span data-stu-id="2bde6-113">Unable to personalize in Organization administration (447490)</span></span>

<span data-ttu-id="2bde6-114">Med denne ændring kan du nu tilpasse linkene i **Organisationsadministration**.</span><span class="sxs-lookup"><span data-stu-id="2bde6-114">With this change, you can now personalize the links in **Organization administration**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="2bde6-115">Som eksempel</span><span class="sxs-lookup"><span data-stu-id="2bde6-115">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="2bde6-116">Obligatoriske felter</span><span class="sxs-lookup"><span data-stu-id="2bde6-116">Mandatory fields</span></span> 

<span data-ttu-id="2bde6-117">Du kan nu gøre felter obligatoriske ved hjælp af funktionerne til tilpasning til personale.</span><span class="sxs-lookup"><span data-stu-id="2bde6-117">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="2bde6-118">Denne funktion kræver **Gemte visninger**.</span><span class="sxs-lookup"><span data-stu-id="2bde6-118">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="2bde6-119">Human Resources-app i Teams</span><span class="sxs-lookup"><span data-stu-id="2bde6-119">Human Resources application in Teams</span></span>

<span data-ttu-id="2bde6-120">Medarbejderne kan få vist og anmode om fri fra arbejde i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2bde6-120">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="2bde6-121">De kan interagere med en bot for at oprette orlovsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="2bde6-121">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="2bde6-122">Yderligere oplysninger finder du i [Human Resources-appen i Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="2bde6-122">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="2bde6-123">DMF-enheder (Data Management Framework) til styring af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="2bde6-123">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="2bde6-124">Enheder til håndtering af frynsegoder frigives.</span><span class="sxs-lookup"><span data-stu-id="2bde6-124">Benefits management entities are releasing.</span></span> <span data-ttu-id="2bde6-125">Med DMF-enheder kan du importere og eksportere data, så du nemt kan konfigurere frynsegodestyring.</span><span class="sxs-lookup"><span data-stu-id="2bde6-125">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="2bde6-126">En skabelon til frynsegodestyring kan også bruges til at flytte data.</span><span class="sxs-lookup"><span data-stu-id="2bde6-126">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="2bde6-127">Skabelonen eksporterer og importerer dataene sekventielt for at respektere dataafhængigheder.</span><span class="sxs-lookup"><span data-stu-id="2bde6-127">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="2bde6-128">Købe og sælge orlov</span><span class="sxs-lookup"><span data-stu-id="2bde6-128">Buy and sell leave</span></span> 

<span data-ttu-id="2bde6-129">Nogle organisationer giver et frynsegode, der giver medarbejderne mulighed for at købe eller sælge deres orlov.</span><span class="sxs-lookup"><span data-stu-id="2bde6-129">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="2bde6-130">Denne proces styres ofte manuelt.</span><span class="sxs-lookup"><span data-stu-id="2bde6-130">This process is often managed manually.</span></span> <span data-ttu-id="2bde6-131">Denne funktion automatiserer administration af politikker og anmodninger for HR-afdelingen.</span><span class="sxs-lookup"><span data-stu-id="2bde6-131">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="2bde6-132">Den effektiviserer orlovsprocessen og medvirker til at eliminere fejltagelser.</span><span class="sxs-lookup"><span data-stu-id="2bde6-132">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="2bde6-133">Du kan finde flere oplysninger i:</span><span class="sxs-lookup"><span data-stu-id="2bde6-133">For more information, see:</span></span>

- [<span data-ttu-id="2bde6-134">Administrere politikker for køb og salg af orlov</span><span class="sxs-lookup"><span data-stu-id="2bde6-134">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="2bde6-135">Købe og sælge orlov</span><span class="sxs-lookup"><span data-stu-id="2bde6-135">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="2bde6-136">Orlovsperiodisering for et enkelt firma eller en enkelt plan</span><span class="sxs-lookup"><span data-stu-id="2bde6-136">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="2bde6-137">Kunderne kan behandle periodiseringer for et enkelt firma eller en enkelt orlovs- fraværsplan.</span><span class="sxs-lookup"><span data-stu-id="2bde6-137">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="2bde6-138">Denne mulighed giver klarhed over periodiseringsprocessen for kunder med forskellige sabbatår eller politikker for orlovsperiodisering.</span><span class="sxs-lookup"><span data-stu-id="2bde6-138">This ability provides clarity for the accrual process for customers with different leave years or leaves accrual policies.</span></span> <span data-ttu-id="2bde6-139">Du kan finde flere oplysninger under [Periodiseret orlov pr. firma eller pr. orlovsplan](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="2bde6-139">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="2bde6-140">Føje vedhæftede filer til anmodninger om fravær</span><span class="sxs-lookup"><span data-stu-id="2bde6-140">Add attachments to time-off requests</span></span>

<span data-ttu-id="2bde6-141">Muligheden for at føje vedhæftede filer til anmodninger om godkendt orlov er afgørende i det aktuelle COVID-19-miljø.</span><span class="sxs-lookup"><span data-stu-id="2bde6-141">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="2bde6-142">Medarbejderne kan nu tilføje disse vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="2bde6-142">Employees can now add these attachments.</span></span> <span data-ttu-id="2bde6-143">De har også en mere indsigt i, hvordan der foretages opdateringer af anmodninger om orlov.</span><span class="sxs-lookup"><span data-stu-id="2bde6-143">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="2bde6-144">Du kan finde flere oplysninger under [Føje en vedhæftet fil til en eksisterende anmodning](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="2bde6-144">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="2bde6-145">Føje årsagskode til periodiseringssuspenderinger</span><span class="sxs-lookup"><span data-stu-id="2bde6-145">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="2bde6-146">Årsagskoder er føjet til periodiseringssuspenderingen.</span><span class="sxs-lookup"><span data-stu-id="2bde6-146">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="2bde6-147">Overføre regler</span><span class="sxs-lookup"><span data-stu-id="2bde6-147">Carry forward rules</span></span> 

<span data-ttu-id="2bde6-148">Du kan angive en orlovstype for overførselssaldi, hvor gennemførte reguleringer overføres.</span><span class="sxs-lookup"><span data-stu-id="2bde6-148">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="2bde6-149">Hvis en medarbejder f.eks. overfører 10 dage, kan du vælge en anden orlovstype for disse 10 dage.</span><span class="sxs-lookup"><span data-stu-id="2bde6-149">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="2bde6-150">Du kan finde flere oplysninger i [Konfigurere orlovs- og fraværstyper](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="2bde6-150">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="2bde6-151">Suspendere orlovsperiodisering for angivne orlovstyper</span><span class="sxs-lookup"><span data-stu-id="2bde6-151">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="2bde6-152">Du kan oprette en regel om suspendering af orlovsperiodiseringer for medarbejdere med orlovsanmodninger, der er angivet til ubetalt orlov.</span><span class="sxs-lookup"><span data-stu-id="2bde6-152">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="2bde6-153">Ubetalt orlov kan være en type, men behøver ikke at være det.</span><span class="sxs-lookup"><span data-stu-id="2bde6-153">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="2bde6-154">Du kan suspendere enhver orlov baseret på en anden orlovstype.</span><span class="sxs-lookup"><span data-stu-id="2bde6-154">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="2bde6-155">DMF-enhed er tilgængelig for periodiseringssuspenderinger</span><span class="sxs-lookup"><span data-stu-id="2bde6-155">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="2bde6-156">En DMF-enhed er nu tilgængelig for periodiseringssuspenderinger.</span><span class="sxs-lookup"><span data-stu-id="2bde6-156">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="2bde6-157">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="2bde6-157">Coming soon</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="2bde6-158">Kontrollisteenheder inkluderet i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="2bde6-158">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="2bde6-159">Der vil snart være tilgængelige kontrollisteenheder til processer til onboarding, offboarding, overførsler og forretning i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="2bde6-159">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Common Data Service.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="2bde6-160">Platformsændringer</span><span class="sxs-lookup"><span data-stu-id="2bde6-160">Platform changes</span></span>

<span data-ttu-id="2bde6-161">Platform update 10.0.12 (36)</span><span class="sxs-lookup"><span data-stu-id="2bde6-161">Platform update 10.0.12 (36)</span></span>

## <a name="see-also"></a><span data-ttu-id="2bde6-162">Se også</span><span class="sxs-lookup"><span data-stu-id="2bde6-162">See also</span></span>

[<span data-ttu-id="2bde6-163">Nyheder eller ændringer i Human Resources</span><span class="sxs-lookup"><span data-stu-id="2bde6-163">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="2bde6-164">Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2</span><span class="sxs-lookup"><span data-stu-id="2bde6-164">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="2bde6-165">Opdater proces</span><span class="sxs-lookup"><span data-stu-id="2bde6-165">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="2bde6-166">Administrere funktioner</span><span class="sxs-lookup"><span data-stu-id="2bde6-166">Manage features</span></span>](hr-admin-manage-features.md)
