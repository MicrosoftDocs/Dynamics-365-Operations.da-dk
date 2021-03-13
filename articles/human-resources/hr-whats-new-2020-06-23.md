---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (25. juni 2020)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 23. juni 2020.
author: andreabichsel
manager: tfehr
ms.date: 06/25/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ad80e53c0a24d602ac446d3e0765f397dd0fc2d9
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127491"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a><span data-ttu-id="2912a-103">Nyheder eller ændringer i Dynamics 365 Human Resources (23. juni 2020)</span><span class="sxs-lookup"><span data-stu-id="2912a-103">What's new or changed in Dynamics 365 Human Resources (June 23, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2912a-104">I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2912a-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2912a-105">Ændringerne gælder for build nummer 8.1.3347.</span><span class="sxs-lookup"><span data-stu-id="2912a-105">Changes apply to build number 8.1.3347.</span></span> <span data-ttu-id="2912a-106">Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.</span><span class="sxs-lookup"><span data-stu-id="2912a-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a><span data-ttu-id="2912a-107">Når en tilmelding er udløbet for en fratrådt medarbejder, ryddes orlovstypen, saldoen og beløbet i formularen Orlovstilmelding (444867)</span><span class="sxs-lookup"><span data-stu-id="2912a-107">When an enrollment is expired for a terminated employee, the leave type, balance, and amount are all cleared in the Leave enrollment form (444867)</span></span>

<span data-ttu-id="2912a-108">Værdierne i **Orlovstype**, **Saldo** og **Beløbet** bevares nu i stedet for at blive ryddet, når dette valg foretages.</span><span class="sxs-lookup"><span data-stu-id="2912a-108">Values in the **Leave type**, **Balance**, and **Amount** are now maintained instead of cleared upon making this selection.</span></span>

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a><span data-ttu-id="2912a-109">Forkert budgetteret saldo, når den nye funktion (Orlovsperiodisering for et enkelt firma eller en enkelt plan) er aktiveret (456553)</span><span class="sxs-lookup"><span data-stu-id="2912a-109">Incorrect forecasted balance when new feature (Leave accrual for a single company or a single plan) is enabled (456553)</span></span>

<span data-ttu-id="2912a-110">Den rigtige budgetterede prognose vises nu, når orlovsperiodiseringen for et enkelt firma eller en enkelt plan er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="2912a-110">The correct forecasted balance now displays when the leave accrual for a single company or single plan has been enabled.</span></span>

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a><span data-ttu-id="2912a-111">Enheder med relationer, der resulterer i dublerede navigationsegenskaber (456486)</span><span class="sxs-lookup"><span data-stu-id="2912a-111">Entities with relations that result in duplicate navigation properties (456486)</span></span>

<span data-ttu-id="2912a-112">Denne version retter et problem med navigationsegenskaberne (relationen) for flere enheder.</span><span class="sxs-lookup"><span data-stu-id="2912a-112">This release corrects an issue with the navigation properties (relation) of multiple entities.</span></span> <span data-ttu-id="2912a-113">Dublerede relationer registreres.</span><span class="sxs-lookup"><span data-stu-id="2912a-113">Duplicate relations are detected.</span></span> <span data-ttu-id="2912a-114">Disse scenarier er alle blevet rettet.</span><span class="sxs-lookup"><span data-stu-id="2912a-114">These scenarios have all been corrected.</span></span>
 
## <a name="cross-company-comments-on-performance-review-455536"></a><span data-ttu-id="2912a-115">Kommentarer på tværs af firmaer ved performance-gennemgang (455536)</span><span class="sxs-lookup"><span data-stu-id="2912a-115">Cross-company comments on Performance review (455536)</span></span>

<span data-ttu-id="2912a-116">Kommentarer på tværs af firmaer kan nu ses på performance-gennemgange med denne rettelse.</span><span class="sxs-lookup"><span data-stu-id="2912a-116">Cross-company comments are now visible on performance reviews with this fix.</span></span> <span data-ttu-id="2912a-117">Denne ændring korrigerer visningen af validators kommentarer, der er angivet i forskellige firmaer for den samme performance-gennemgang.</span><span class="sxs-lookup"><span data-stu-id="2912a-117">This change corrects the view of reviewer comments that were entered in different companies for the same performance review.</span></span>
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a><span data-ttu-id="2912a-118">Inkonsistens i visning af kompensationsstyringsdata (432562)</span><span class="sxs-lookup"><span data-stu-id="2912a-118">Inconsistency in showing compensation management data (432562)</span></span>

<span data-ttu-id="2912a-119">En ensartet visning af kompensationsdata vedligeholdes nu i lederselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="2912a-119">A consistent view of compensation data is now maintained in Manager self service.</span></span> <span data-ttu-id="2912a-120">Afhængigt af, hvordan du navigerer til en arbejders **kompensationsoplysninger**, vises kompensationsdataene nu altid for lederne.</span><span class="sxs-lookup"><span data-stu-id="2912a-120">Depending on how you navigate to a worker's **Compensation details**, compensation data now consistently displays to managers.</span></span>
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a><span data-ttu-id="2912a-121">Ikrafttrædelsesdato for fast løn angives som standard til dags dato (411994)</span><span class="sxs-lookup"><span data-stu-id="2912a-121">Fixed compensation plan's effective date defaults to today's date (411994)</span></span>

<span data-ttu-id="2912a-122">Startdatoen for kompensation er nu baseret på startdatoen for den stilling, der tildeles medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="2912a-122">The compensation start date is now based on the start date of the position being assigned to the employee.</span></span>

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a><span data-ttu-id="2912a-123">Formularen Aktivér halvdagsdefinition for orlov og fravær er deaktiveret, når formularen åbnes (452607)</span><span class="sxs-lookup"><span data-stu-id="2912a-123">Leave and absence form Enable half day definition is disabled when form opens (452607)</span></span>

<span data-ttu-id="2912a-124">Med denne ændring aktiveres **Aktivér Halvdagsdefinition**, indtil der findes nye orlovsposteringer.</span><span class="sxs-lookup"><span data-stu-id="2912a-124">With this change, the **Enable half day definition** will be enabled until new leave transactions exist.</span></span> 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a><span data-ttu-id="2912a-125">Der kan ikke udgives til HcmDiscussionEntity via Excel. Fejl i feltet TotalRatingScore (453899)</span><span class="sxs-lookup"><span data-stu-id="2912a-125">Unable to publish to HcmDiscussionEntity via Excel; TotalRatingScore field error (453899)</span></span>

<span data-ttu-id="2912a-126">Du kan nu opdatere feltet **TotalRatingScore** ved hjælp af **HCMDiscussionEntity** i Excel-projektmappedesigneren.</span><span class="sxs-lookup"><span data-stu-id="2912a-126">You can now update the **TotalRatingScore** field using **HCMDiscussionEntity** in the Excel workbook designer.</span></span>

## <a name="in-preview"></a><span data-ttu-id="2912a-127">Som eksempel</span><span class="sxs-lookup"><span data-stu-id="2912a-127">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="2912a-128">Databaselogføring</span><span class="sxs-lookup"><span data-stu-id="2912a-128">Database logging</span></span>

<span data-ttu-id="2912a-129">Databaselogning gør det muligt at bestemme, hvilke tabeller og felter der skal overvåges.</span><span class="sxs-lookup"><span data-stu-id="2912a-129">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="2912a-130">Du kan også bestemme, hvilke hændelser der skal udløse ændringssporing.</span><span class="sxs-lookup"><span data-stu-id="2912a-130">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="2912a-131">Du kan bruge logføringsfunktioner for databasen til at se disse ændringer over tid.</span><span class="sxs-lookup"><span data-stu-id="2912a-131">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="2912a-132">Du kan finde flere oplysninger under [Konfigurere og administrere databaselogning](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="2912a-132">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="2912a-133">Obligatoriske felter</span><span class="sxs-lookup"><span data-stu-id="2912a-133">Mandatory fields</span></span> 

<span data-ttu-id="2912a-134">Du kan nu gøre felter obligatoriske ved hjælp af funktionerne til tilpasning til personale.</span><span class="sxs-lookup"><span data-stu-id="2912a-134">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="2912a-135">Denne funktion kræver **Gemte visninger**.</span><span class="sxs-lookup"><span data-stu-id="2912a-135">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="2912a-136">Human Resources-app i Teams</span><span class="sxs-lookup"><span data-stu-id="2912a-136">Human Resources application in Teams</span></span>

<span data-ttu-id="2912a-137">Medarbejderne kan få vist og anmode om fri fra arbejde i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2912a-137">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="2912a-138">De kan interagere med en bot for at oprette orlovsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="2912a-138">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="2912a-139">Yderligere oplysninger finder du i [Human Resources-appen i Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="2912a-139">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="2912a-140">DMF-enheder (Data Management Framework) til styring af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="2912a-140">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="2912a-141">Enheder til håndtering af frynsegoder frigives.</span><span class="sxs-lookup"><span data-stu-id="2912a-141">Benefits management entities are releasing.</span></span> <span data-ttu-id="2912a-142">Med DMF-enheder kan du importere og eksportere data, så du nemt kan konfigurere frynsegodestyring.</span><span class="sxs-lookup"><span data-stu-id="2912a-142">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="2912a-143">En skabelon til frynsegodestyring kan også bruges til at flytte data.</span><span class="sxs-lookup"><span data-stu-id="2912a-143">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="2912a-144">Skabelonen eksporterer og importerer dataene sekventielt for at respektere dataafhængigheder.</span><span class="sxs-lookup"><span data-stu-id="2912a-144">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="2912a-145">Købe og sælge orlov</span><span class="sxs-lookup"><span data-stu-id="2912a-145">Buy and sell leave</span></span> 

<span data-ttu-id="2912a-146">Nogle organisationer giver et frynsegode, der giver medarbejderne mulighed for at købe eller sælge deres orlov.</span><span class="sxs-lookup"><span data-stu-id="2912a-146">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="2912a-147">Denne proces styres ofte manuelt.</span><span class="sxs-lookup"><span data-stu-id="2912a-147">This process is often managed manually.</span></span> <span data-ttu-id="2912a-148">Denne funktion automatiserer administration af politikker og anmodninger for HR-afdelingen.</span><span class="sxs-lookup"><span data-stu-id="2912a-148">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="2912a-149">Den effektiviserer orlovsprocessen og medvirker til at eliminere fejltagelser.</span><span class="sxs-lookup"><span data-stu-id="2912a-149">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="2912a-150">Du kan finde flere oplysninger i:</span><span class="sxs-lookup"><span data-stu-id="2912a-150">For more information, see:</span></span>

- [<span data-ttu-id="2912a-151">Administrere politikker for køb og salg af orlov</span><span class="sxs-lookup"><span data-stu-id="2912a-151">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="2912a-152">Købe og sælge orlov</span><span class="sxs-lookup"><span data-stu-id="2912a-152">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="2912a-153">Orlovsperiodisering for et enkelt firma eller en enkelt plan</span><span class="sxs-lookup"><span data-stu-id="2912a-153">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="2912a-154">Kunderne kan behandle periodiseringer for et enkelt firma eller en enkelt orlovs- fraværsplan.</span><span class="sxs-lookup"><span data-stu-id="2912a-154">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="2912a-155">Denne mulighed giver klarhed over periodiseringsprocessen for kunder med forskellige sabbatår eller politikker for orlovsperiodisering.</span><span class="sxs-lookup"><span data-stu-id="2912a-155">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="2912a-156">Du kan finde flere oplysninger under [Periodiseret orlov pr. firma eller pr. orlovsplan](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="2912a-156">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="2912a-157">Føje vedhæftede filer til anmodninger om fravær</span><span class="sxs-lookup"><span data-stu-id="2912a-157">Add attachments to time off requests</span></span>

<span data-ttu-id="2912a-158">Muligheden for at føje vedhæftede filer til anmodninger om godkendt orlov er afgørende i det aktuelle COVID-19-miljø.</span><span class="sxs-lookup"><span data-stu-id="2912a-158">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="2912a-159">Medarbejderne kan nu tilføje disse vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="2912a-159">Employees can now add these attachments.</span></span> <span data-ttu-id="2912a-160">De har også en mere indsigt i, hvordan der foretages opdateringer af anmodninger om orlov.</span><span class="sxs-lookup"><span data-stu-id="2912a-160">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="2912a-161">Du kan finde flere oplysninger under [Føje en vedhæftet fil til en eksisterende anmodning](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="2912a-161">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="2912a-162">Føje årsagskode til periodiseringssuspenderinger</span><span class="sxs-lookup"><span data-stu-id="2912a-162">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="2912a-163">Årsagskoder er føjet til periodiseringssuspenderingen.</span><span class="sxs-lookup"><span data-stu-id="2912a-163">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="2912a-164">Overføre regler</span><span class="sxs-lookup"><span data-stu-id="2912a-164">Carry forward rules</span></span> 

<span data-ttu-id="2912a-165">Du kan angive en orlovstype for overførselssaldi, hvor gennemførte reguleringer overføres.</span><span class="sxs-lookup"><span data-stu-id="2912a-165">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="2912a-166">Hvis en medarbejder f.eks. overfører 10 dage, kan du vælge en anden orlovstype for disse 10 dage.</span><span class="sxs-lookup"><span data-stu-id="2912a-166">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="2912a-167">Du kan finde flere oplysninger i [Konfigurere orlovs- og fraværstyper](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="2912a-167">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="2912a-168">Suspendere orlovsperiodisering for angivne orlovstyper</span><span class="sxs-lookup"><span data-stu-id="2912a-168">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="2912a-169">Du kan oprette en regel om suspendering af orlovsperiodiseringer for medarbejdere med orlovsanmodninger, der er angivet til ubetalt orlov.</span><span class="sxs-lookup"><span data-stu-id="2912a-169">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="2912a-170">Ubetalt orlov kan være en type, men behøver ikke at være det.</span><span class="sxs-lookup"><span data-stu-id="2912a-170">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="2912a-171">Du kan suspendere enhver orlov baseret på en anden orlovstype.</span><span class="sxs-lookup"><span data-stu-id="2912a-171">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="2912a-172">DMF-enhed er tilgængelig for periodiseringssuspenderinger</span><span class="sxs-lookup"><span data-stu-id="2912a-172">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="2912a-173">En DMF-enhed er nu tilgængelig for periodiseringssuspenderinger.</span><span class="sxs-lookup"><span data-stu-id="2912a-173">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="2912a-174">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="2912a-174">Coming soon</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="2912a-175">Konfigurere navnet på medarbejderselvbetjening</span><span class="sxs-lookup"><span data-stu-id="2912a-175">Configure the name of Employee self-service</span></span>

<span data-ttu-id="2912a-176">En ny indstilling vil være tilgængelig i **Human Resources-parametrene** for at opdatere navnet på arbejdsområdet for medarbejderselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="2912a-176">A new option will be available in **Human Resources parameters** to update the name of the Employee self service workspace to Self service.</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="2912a-177">Kontrollisteenheder inkluderet i Dataverse</span><span class="sxs-lookup"><span data-stu-id="2912a-177">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="2912a-178">Der vil snart være tilgængelige kontrollisteenheder til processer til onboarding, offboarding, overførsler og forretning i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2912a-178">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon within Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="2912a-179">Se også</span><span class="sxs-lookup"><span data-stu-id="2912a-179">See also</span></span>

[<span data-ttu-id="2912a-180">Nyheder eller ændringer i Human Resources</span><span class="sxs-lookup"><span data-stu-id="2912a-180">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="2912a-181">Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2</span><span class="sxs-lookup"><span data-stu-id="2912a-181">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="2912a-182">Opdater proces</span><span class="sxs-lookup"><span data-stu-id="2912a-182">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="2912a-183">Administrere funktioner</span><span class="sxs-lookup"><span data-stu-id="2912a-183">Manage features</span></span>](hr-admin-manage-features.md)