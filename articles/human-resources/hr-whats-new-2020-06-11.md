---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (11. juni 2020)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 11. juni 2020.
author: andreabichsel
ms.date: 06/16/2020
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
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8265c0b6218f69b95f2729140aa303edeaa31443
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891931"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a><span data-ttu-id="e57b9-103">Nyheder eller ændringer i Dynamics 365 Human Resources (11. juni 2020)</span><span class="sxs-lookup"><span data-stu-id="e57b9-103">What's new or changed in Dynamics 365 Human Resources (June 11, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e57b9-104">I denne artikel beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e57b9-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="e57b9-105">Ændringerne gælder for build nummer 8.1.3316.</span><span class="sxs-lookup"><span data-stu-id="e57b9-105">Changes apply to build number 8.1.3316.</span></span> <span data-ttu-id="e57b9-106">Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.</span><span class="sxs-lookup"><span data-stu-id="e57b9-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a><span data-ttu-id="e57b9-107">Strømlinede medarbejderformularer bevirker nogle gange, at lukke (X)-knapper i underordnede formularer holder op med at fungere (442369)</span><span class="sxs-lookup"><span data-stu-id="e57b9-107">Streamlined employee form sometimes causes child form close (X) buttons to stop working (442369)</span></span>

<span data-ttu-id="e57b9-108">Når den nye formular **Arbejder** blev aktiveret, fungerede knappen Luk (**X**) indimellem ikke i underordnede formularer.</span><span class="sxs-lookup"><span data-stu-id="e57b9-108">When the new **Worker** form was enabled, the close (**X**) button occasionally didn't work on child forms.</span></span> <span data-ttu-id="e57b9-109">Dette problem var periodisk.</span><span class="sxs-lookup"><span data-stu-id="e57b9-109">This problem was intermittent.</span></span> <span data-ttu-id="e57b9-110">Du kunne lukke formen, når du var gået væk fra den og vendte tilbage til den.</span><span class="sxs-lookup"><span data-stu-id="e57b9-110">You could close the form after leaving and coming back to it.</span></span> <span data-ttu-id="e57b9-111">Du kunne f.eks. vælge et menupunkt til venstre og gå tilbage til **Arbejder**-formularen og derefter lukke den.</span><span class="sxs-lookup"><span data-stu-id="e57b9-111">For example, you could select a menu item on the left, and navigate back to the **Worker** form, and then close it.</span></span> <span data-ttu-id="e57b9-112">Denne uges frigivelse løser dette problem.</span><span class="sxs-lookup"><span data-stu-id="e57b9-112">This week's release fixes this problem.</span></span> 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a><span data-ttu-id="e57b9-113">Arbejderens personlige kontaktpersonenhed eksporterer ikke personlige kontakter med en overordnet relationstype</span><span class="sxs-lookup"><span data-stu-id="e57b9-113">The Worker personal contact person entity doesn't export personal contacts with a parent relationship type</span></span>

<span data-ttu-id="e57b9-114">Med denne frigivelse eksporterer objektet **Arbejders personlige kontaktperson** alle relationstyper.</span><span class="sxs-lookup"><span data-stu-id="e57b9-114">With this release, the **Worker personal contact person** entity exports all relationship types.</span></span>

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a><span data-ttu-id="e57b9-115">HcmPositionWorkerAssignmentV2Entity skal være en del af Ceridian-lønintegrationspakken som standard (448506)</span><span class="sxs-lookup"><span data-stu-id="e57b9-115">The HcmPositionWorkerAssignmentV2Entity should be part of the Ceridian payroll integration package by default (448506)</span></span>

<span data-ttu-id="e57b9-116">Med denne ændring er **HcmPositionWorkerAssignmentV2Entity** inkluderet i Ceridian-lønintegrationspakken.</span><span class="sxs-lookup"><span data-stu-id="e57b9-116">With this change, the **HcmPositionWorkerAssignmentV2Entity** is included in the Ceridian payroll integration package.</span></span>

## <a name="in-preview"></a><span data-ttu-id="e57b9-117">Som eksempel</span><span class="sxs-lookup"><span data-stu-id="e57b9-117">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="e57b9-118">Databaselogføring</span><span class="sxs-lookup"><span data-stu-id="e57b9-118">Database logging</span></span>

<span data-ttu-id="e57b9-119">Du kan bruge funktionen til databaselogning til at bestemme, hvilke tabeller og felter der skal overvåges.</span><span class="sxs-lookup"><span data-stu-id="e57b9-119">The database logging feature allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="e57b9-120">Du kan også bestemme, hvilke hændelser der skal udløse ændringssporing.</span><span class="sxs-lookup"><span data-stu-id="e57b9-120">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="e57b9-121">Du kan bruge logføringsfunktioner for databasen til at se disse ændringer over tid.</span><span class="sxs-lookup"><span data-stu-id="e57b9-121">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="e57b9-122">Du kan finde flere oplysninger under [Konfigurere og administrere databaselogning](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="e57b9-122">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="e57b9-123">Human Resources-app i Teams</span><span class="sxs-lookup"><span data-stu-id="e57b9-123">Human Resources application in Teams</span></span>

<span data-ttu-id="e57b9-124">Medarbejderne kan få vist og anmode om fri fra arbejde i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="e57b9-124">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="e57b9-125">De kan interagere med en bot for at oprette orlovsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="e57b9-125">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="e57b9-126">Yderligere oplysninger finder du i [Human Resources-appen i Teams](./hr-admin-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="e57b9-126">For more information, see [Human Resources app in Teams](./hr-admin-teams-leave-app.md).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="e57b9-127">DMF-enheder (Data Management Framework) til styring af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="e57b9-127">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="e57b9-128">Enheder til håndtering af frynsegoder frigives.</span><span class="sxs-lookup"><span data-stu-id="e57b9-128">Benefits management entities are releasing.</span></span> <span data-ttu-id="e57b9-129">Med DMF-enheder kan du importere og eksportere data, så du nemt kan konfigurere frynsegodestyring.</span><span class="sxs-lookup"><span data-stu-id="e57b9-129">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="e57b9-130">En skabelon til frynsegodestyring kan også bruges til at flytte data.</span><span class="sxs-lookup"><span data-stu-id="e57b9-130">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="e57b9-131">Skabelonen eksporterer og importerer dataene sekventielt for at respektere dataafhængigheder.</span><span class="sxs-lookup"><span data-stu-id="e57b9-131">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="e57b9-132">Købe og sælge orlov</span><span class="sxs-lookup"><span data-stu-id="e57b9-132">Buy and sell leave</span></span> 

<span data-ttu-id="e57b9-133">Nogle organisationer giver et frynsegode, der giver medarbejderne mulighed for at købe eller sælge deres orlov.</span><span class="sxs-lookup"><span data-stu-id="e57b9-133">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="e57b9-134">Denne proces styres ofte manuelt.</span><span class="sxs-lookup"><span data-stu-id="e57b9-134">This process is often managed manually.</span></span> <span data-ttu-id="e57b9-135">Denne funktion automatiserer administration af politikker og anmodninger for HR-afdelingen.</span><span class="sxs-lookup"><span data-stu-id="e57b9-135">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="e57b9-136">Den effektiviserer orlovsprocessen og medvirker til at eliminere fejltagelser.</span><span class="sxs-lookup"><span data-stu-id="e57b9-136">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="e57b9-137">Du kan finde flere oplysninger i:</span><span class="sxs-lookup"><span data-stu-id="e57b9-137">For more information, see:</span></span>

- [<span data-ttu-id="e57b9-138">Administrere politikker for køb og salg af orlov</span><span class="sxs-lookup"><span data-stu-id="e57b9-138">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="e57b9-139">Købe og sælge orlov</span><span class="sxs-lookup"><span data-stu-id="e57b9-139">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="e57b9-140">Orlovsperiodisering for et enkelt firma eller en enkelt plan</span><span class="sxs-lookup"><span data-stu-id="e57b9-140">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="e57b9-141">Kunderne kan behandle periodiseringer for et enkelt firma eller en enkelt orlovs- fraværsplan.</span><span class="sxs-lookup"><span data-stu-id="e57b9-141">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="e57b9-142">Denne mulighed giver klarhed over periodiseringsprocessen for kunder med forskellige sabbatår eller politikker for orlovsperiodisering.</span><span class="sxs-lookup"><span data-stu-id="e57b9-142">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="e57b9-143">Du kan finde flere oplysninger under [Periodiseret orlov pr. firma eller pr. orlovsplan](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="e57b9-143">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="e57b9-144">Føje vedhæftede filer til anmodninger om fravær</span><span class="sxs-lookup"><span data-stu-id="e57b9-144">Add attachments to time off requests</span></span>

<span data-ttu-id="e57b9-145">Muligheden for at føje vedhæftede filer til anmodninger om godkendt orlov er afgørende i det aktuelle COVID-19-miljø.</span><span class="sxs-lookup"><span data-stu-id="e57b9-145">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="e57b9-146">Medarbejderne kan nu tilføje disse vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="e57b9-146">Employees can now add these attachments.</span></span> <span data-ttu-id="e57b9-147">De har også en mere indsigt i, hvordan der foretages opdateringer af anmodninger om orlov.</span><span class="sxs-lookup"><span data-stu-id="e57b9-147">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="e57b9-148">Du kan finde flere oplysninger under [Føje en vedhæftet fil til en eksisterende anmodning](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="e57b9-148">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="e57b9-149">Føje årsagskode til periodiseringssuspenderinger</span><span class="sxs-lookup"><span data-stu-id="e57b9-149">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="e57b9-150">Årsagskoder er føjet til periodiseringssuspenderingen.</span><span class="sxs-lookup"><span data-stu-id="e57b9-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="e57b9-151">Overføre regler</span><span class="sxs-lookup"><span data-stu-id="e57b9-151">Carry forward rules</span></span> 

<span data-ttu-id="e57b9-152">Du kan angive en orlovstype for overførselssaldi, hvor gennemførte reguleringer overføres.</span><span class="sxs-lookup"><span data-stu-id="e57b9-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="e57b9-153">Hvis en medarbejder f.eks. overfører 10 dage, kan du vælge en anden orlovstype for disse 10 dage.</span><span class="sxs-lookup"><span data-stu-id="e57b9-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="e57b9-154">Du kan finde flere oplysninger i [Konfigurere orlovs- og fraværstyper](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="e57b9-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="e57b9-155">Suspendere orlovsperiodisering for angivne orlovstyper</span><span class="sxs-lookup"><span data-stu-id="e57b9-155">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="e57b9-156">Du kan oprette en regel om suspendering af orlovsperiodiseringer for medarbejdere med orlovsanmodninger, der er angivet til ubetalt orlov.</span><span class="sxs-lookup"><span data-stu-id="e57b9-156">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="e57b9-157">Ubetalt orlov kan være en type, men behøver ikke at være det.</span><span class="sxs-lookup"><span data-stu-id="e57b9-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="e57b9-158">Du kan suspendere enhver orlov baseret på en anden orlovstype.</span><span class="sxs-lookup"><span data-stu-id="e57b9-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="e57b9-159">DMF-enhed er tilgængelig for periodiseringssuspenderinger</span><span class="sxs-lookup"><span data-stu-id="e57b9-159">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="e57b9-160">En DMF-enhed er nu tilgængelig for periodiseringssuspenderinger.</span><span class="sxs-lookup"><span data-stu-id="e57b9-160">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="e57b9-161">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="e57b9-161">Coming soon</span></span>

## <a name="new-platform-capabilities"></a><span data-ttu-id="e57b9-162">Nye platformsmuligheder</span><span class="sxs-lookup"><span data-stu-id="e57b9-162">New platform capabilities</span></span> 

<span data-ttu-id="e57b9-163">Du kan gøre felter obligatoriske ved hjælp af tilpasning.</span><span class="sxs-lookup"><span data-stu-id="e57b9-163">You'll be able to make fields mandatory by using personalization.</span></span> <span data-ttu-id="e57b9-164">Denne funktion kræver, at du aktiverer **Gemte visninger**.</span><span class="sxs-lookup"><span data-stu-id="e57b9-164">This feature will require you to enable **Saved views**.</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="e57b9-165">Konfigurere navnet på medarbejderselvbetjening</span><span class="sxs-lookup"><span data-stu-id="e57b9-165">Configure the name of Employee self-service</span></span>

<span data-ttu-id="e57b9-166">En ny indstilling vil være tilgængelig i Human Resources-parametrene for at opdatere navnet på arbejdsområdet for medarbejderselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="e57b9-166">A new option will be available in Human Resources parameters to update the name of the Employee self service workspace to Self service.</span></span> 

## <a name="see-also"></a><span data-ttu-id="e57b9-167">Se også</span><span class="sxs-lookup"><span data-stu-id="e57b9-167">See also</span></span>

[<span data-ttu-id="e57b9-168">Nyheder eller ændringer i Human Resources</span><span class="sxs-lookup"><span data-stu-id="e57b9-168">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="e57b9-169">Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2</span><span class="sxs-lookup"><span data-stu-id="e57b9-169">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="e57b9-170">Opdater proces</span><span class="sxs-lookup"><span data-stu-id="e57b9-170">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="e57b9-171">Administrere funktioner</span><span class="sxs-lookup"><span data-stu-id="e57b9-171">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]