---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (23. juli 2020)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 23. juli 2020.
author: andreabichsel
ms.date: 07/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 10369bd5aa67641fe840312bc3d8ebc0e91865e0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791287"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a><span data-ttu-id="cd580-103">Nyheder eller ændringer i Dynamics 365 Human Resources (23. juli 2020)</span><span class="sxs-lookup"><span data-stu-id="cd580-103">What's new or changed in Dynamics 365 Human Resources (July 23, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="cd580-104">I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cd580-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="cd580-105">Ændringerne gælder for build nummer 8.1.3416.</span><span class="sxs-lookup"><span data-stu-id="cd580-105">Changes apply to build number 8.1.3416.</span></span> <span data-ttu-id="cd580-106">Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.</span><span class="sxs-lookup"><span data-stu-id="cd580-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a><span data-ttu-id="cd580-107">Sletning af økonomiske dimensioner på en stilling fungerer ikke som forventet (445476)</span><span class="sxs-lookup"><span data-stu-id="cd580-107">Deleting Financial Dimensions on a Position doesn't work as expected (445476)</span></span>

<span data-ttu-id="cd580-108">Hvis du fjerner dimensioner fra en stilling, fjerner du nu de samme stillinger fra Dataverse.</span><span class="sxs-lookup"><span data-stu-id="cd580-108">Removing dimensions from a position now removes those same positions from Dataverse.</span></span>

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a><span data-ttu-id="cd580-109">Stillinger, der ikke er i hierarki, viser inaktive stillinger (397257)</span><span class="sxs-lookup"><span data-stu-id="cd580-109">Positions not in hierarchy show inactive positions (397257)</span></span>

<span data-ttu-id="cd580-110">Stillinger, der er inaktive (har en udløbet varighed), vises ikke længere i stillingshierarkiet som **Stillinger, der ikke er i hierarki**.</span><span class="sxs-lookup"><span data-stu-id="cd580-110">Positions that are inactive (have an expired duration), no longer display in the position hierarchy as **Positions not in hierarchy**.</span></span> 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a><span data-ttu-id="cd580-111">Validering, der sker mellem LeaveEnrollmentEntity og HcmWorkerEntity under import af Data Management Framework (DMF), medfører langsom dataindlæsning (442324)</span><span class="sxs-lookup"><span data-stu-id="cd580-111">Validation occurring between LeaveEnrollmentEntity and HcmWorkerEntity on Data Management Framework (DMF) import causes slow data loads (442324)</span></span>

<span data-ttu-id="cd580-112">Ændringer i denne frigivelse øger ydeevnen af **LeaveEnrollmentEntity**.</span><span class="sxs-lookup"><span data-stu-id="cd580-112">Changes in this release increase the performance of **LeaveEnrollmentEntity**.</span></span>

## <a name="unable-to-personalize-in-organization-administration-447490"></a><span data-ttu-id="cd580-113">Det er ikke muligt at tilpasse i organisationsadministration (447490)</span><span class="sxs-lookup"><span data-stu-id="cd580-113">Unable to personalize in Organization administration (447490)</span></span>

<span data-ttu-id="cd580-114">Med denne ændring kan du nu tilpasse linkene i **Organisationsadministration**.</span><span class="sxs-lookup"><span data-stu-id="cd580-114">With this change, you can now personalize the links in **Organization administration**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="cd580-115">Som eksempel</span><span class="sxs-lookup"><span data-stu-id="cd580-115">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="cd580-116">Obligatoriske felter</span><span class="sxs-lookup"><span data-stu-id="cd580-116">Mandatory fields</span></span> 

<span data-ttu-id="cd580-117">Du kan nu gøre felter obligatoriske ved hjælp af funktionerne til tilpasning til personale.</span><span class="sxs-lookup"><span data-stu-id="cd580-117">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="cd580-118">Denne funktion kræver **Gemte visninger**.</span><span class="sxs-lookup"><span data-stu-id="cd580-118">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="cd580-119">Human Resources-app i Teams</span><span class="sxs-lookup"><span data-stu-id="cd580-119">Human Resources application in Teams</span></span>

<span data-ttu-id="cd580-120">Medarbejderne kan få vist og anmode om fri fra arbejde i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="cd580-120">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="cd580-121">De kan interagere med en bot for at oprette orlovsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="cd580-121">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="cd580-122">Yderligere oplysninger finder du i [Human Resources-appen i Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="cd580-122">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="cd580-123">DMF-enheder (Data Management Framework) til styring af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="cd580-123">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="cd580-124">Enheder til håndtering af frynsegoder frigives.</span><span class="sxs-lookup"><span data-stu-id="cd580-124">Benefits management entities are releasing.</span></span> <span data-ttu-id="cd580-125">Med DMF-enheder kan du importere og eksportere data, så du nemt kan konfigurere frynsegodestyring.</span><span class="sxs-lookup"><span data-stu-id="cd580-125">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="cd580-126">En skabelon til frynsegodestyring kan også bruges til at flytte data.</span><span class="sxs-lookup"><span data-stu-id="cd580-126">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="cd580-127">Skabelonen eksporterer og importerer dataene sekventielt for at respektere dataafhængigheder.</span><span class="sxs-lookup"><span data-stu-id="cd580-127">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="cd580-128">Købe og sælge orlov</span><span class="sxs-lookup"><span data-stu-id="cd580-128">Buy and sell leave</span></span> 

<span data-ttu-id="cd580-129">Nogle organisationer giver et frynsegode, der giver medarbejderne mulighed for at købe eller sælge deres orlov.</span><span class="sxs-lookup"><span data-stu-id="cd580-129">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="cd580-130">Denne proces styres ofte manuelt.</span><span class="sxs-lookup"><span data-stu-id="cd580-130">This process is often managed manually.</span></span> <span data-ttu-id="cd580-131">Denne funktion automatiserer administration af politikker og anmodninger for HR-afdelingen.</span><span class="sxs-lookup"><span data-stu-id="cd580-131">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="cd580-132">Den effektiviserer orlovsprocessen og medvirker til at eliminere fejltagelser.</span><span class="sxs-lookup"><span data-stu-id="cd580-132">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="cd580-133">Du kan finde flere oplysninger i:</span><span class="sxs-lookup"><span data-stu-id="cd580-133">For more information, see:</span></span>

- [<span data-ttu-id="cd580-134">Administrere politikker for køb og salg af orlov</span><span class="sxs-lookup"><span data-stu-id="cd580-134">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="cd580-135">Købe og sælge orlov</span><span class="sxs-lookup"><span data-stu-id="cd580-135">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="cd580-136">Orlovsperiodisering for et enkelt firma eller en enkelt plan</span><span class="sxs-lookup"><span data-stu-id="cd580-136">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="cd580-137">Kunderne kan behandle periodiseringer for et enkelt firma eller en enkelt orlovs- fraværsplan.</span><span class="sxs-lookup"><span data-stu-id="cd580-137">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="cd580-138">Denne mulighed giver klarhed over periodiseringsprocessen for kunder med forskellige sabbatår eller politikker for orlovsperiodisering.</span><span class="sxs-lookup"><span data-stu-id="cd580-138">This ability provides clarity for the accrual process for customers with different leave years or leaves accrual policies.</span></span> <span data-ttu-id="cd580-139">Du kan finde flere oplysninger under [Periodiseret orlov pr. firma eller pr. orlovsplan](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="cd580-139">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="cd580-140">Føje vedhæftede filer til anmodninger om fravær</span><span class="sxs-lookup"><span data-stu-id="cd580-140">Add attachments to time-off requests</span></span>

<span data-ttu-id="cd580-141">Muligheden for at føje vedhæftede filer til anmodninger om godkendt orlov er afgørende i det aktuelle COVID-19-miljø.</span><span class="sxs-lookup"><span data-stu-id="cd580-141">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="cd580-142">Medarbejderne kan nu tilføje disse vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="cd580-142">Employees can now add these attachments.</span></span> <span data-ttu-id="cd580-143">De har også en mere indsigt i, hvordan der foretages opdateringer af anmodninger om orlov.</span><span class="sxs-lookup"><span data-stu-id="cd580-143">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="cd580-144">Du kan finde flere oplysninger under [Føje en vedhæftet fil til en eksisterende anmodning](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="cd580-144">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="cd580-145">Føje årsagskode til periodiseringssuspenderinger</span><span class="sxs-lookup"><span data-stu-id="cd580-145">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="cd580-146">Årsagskoder er føjet til periodiseringssuspenderingen.</span><span class="sxs-lookup"><span data-stu-id="cd580-146">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="cd580-147">Overføre regler</span><span class="sxs-lookup"><span data-stu-id="cd580-147">Carry forward rules</span></span> 

<span data-ttu-id="cd580-148">Du kan angive en orlovstype for overførselssaldi, hvor gennemførte reguleringer overføres.</span><span class="sxs-lookup"><span data-stu-id="cd580-148">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="cd580-149">Hvis en medarbejder f.eks. overfører 10 dage, kan du vælge en anden orlovstype for disse 10 dage.</span><span class="sxs-lookup"><span data-stu-id="cd580-149">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="cd580-150">Du kan finde flere oplysninger i [Konfigurere orlovs- og fraværstyper](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="cd580-150">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="cd580-151">Suspendere orlovsperiodisering for angivne orlovstyper</span><span class="sxs-lookup"><span data-stu-id="cd580-151">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="cd580-152">Du kan oprette en regel om suspendering af orlovsperiodiseringer for medarbejdere med orlovsanmodninger, der er angivet til ubetalt orlov.</span><span class="sxs-lookup"><span data-stu-id="cd580-152">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="cd580-153">Ubetalt orlov kan være en type, men behøver ikke at være det.</span><span class="sxs-lookup"><span data-stu-id="cd580-153">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="cd580-154">Du kan suspendere enhver orlov baseret på en anden orlovstype.</span><span class="sxs-lookup"><span data-stu-id="cd580-154">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="cd580-155">DMF-enhed er tilgængelig for periodiseringssuspenderinger</span><span class="sxs-lookup"><span data-stu-id="cd580-155">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="cd580-156">En DMF-enhed er nu tilgængelig for periodiseringssuspenderinger.</span><span class="sxs-lookup"><span data-stu-id="cd580-156">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="cd580-157">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="cd580-157">Coming soon</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="cd580-158">Kontrollisteenheder inkluderet i Dataverse</span><span class="sxs-lookup"><span data-stu-id="cd580-158">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="cd580-159">Der vil snart være tilgængelige kontrollisteenheder til processer til onboarding, offboarding, overførsler og forretning i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="cd580-159">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="cd580-160">Platformsændringer</span><span class="sxs-lookup"><span data-stu-id="cd580-160">Platform changes</span></span>

<span data-ttu-id="cd580-161">Platform update 10.0.12 (36)</span><span class="sxs-lookup"><span data-stu-id="cd580-161">Platform update 10.0.12 (36)</span></span>

## <a name="see-also"></a><span data-ttu-id="cd580-162">Se også</span><span class="sxs-lookup"><span data-stu-id="cd580-162">See also</span></span>

[<span data-ttu-id="cd580-163">Nyheder eller ændringer i Human Resources</span><span class="sxs-lookup"><span data-stu-id="cd580-163">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="cd580-164">Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2</span><span class="sxs-lookup"><span data-stu-id="cd580-164">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="cd580-165">Opdater proces</span><span class="sxs-lookup"><span data-stu-id="cd580-165">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="cd580-166">Administrere funktioner</span><span class="sxs-lookup"><span data-stu-id="cd580-166">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]