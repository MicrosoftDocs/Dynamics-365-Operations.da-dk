---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (08. juli 2020)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 8. juli 2020.
author: andreabichsel
manager: tfehr
ms.date: 07/08/2020
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
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9715f332088b7b5340f4252af5f789d226d90ff2
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463592"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a><span data-ttu-id="b8ee2-103">Nyheder eller ændringer i Dynamics 365 Human Resources (8. juli 2020)</span><span class="sxs-lookup"><span data-stu-id="b8ee2-103">What's new or changed in Dynamics 365 Human Resources (July 8, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b8ee2-104">I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b8ee2-105">Ændringerne gælder for build nummer 8.1.3382.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-105">Changes apply to build number 8.1.3382.</span></span> <span data-ttu-id="b8ee2-106">Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="database-logging"></a><span data-ttu-id="b8ee2-107">Databaselogføring</span><span class="sxs-lookup"><span data-stu-id="b8ee2-107">Database logging</span></span>

<span data-ttu-id="b8ee2-108">Databaselogning gør det muligt at bestemme, hvilke tabeller og felter der skal overvåges.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-108">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="b8ee2-109">Du kan også bestemme, hvilke hændelser der skal udløse ændringssporing.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-109">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="b8ee2-110">Du kan bruge logføringsfunktioner for databasen til at se disse ændringer over tid.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-110">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="b8ee2-111">Du kan finde flere oplysninger under [Konfigurere og administrere databaselogning](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="b8ee2-111">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="b8ee2-112">Konfigurere navnet på medarbejderselvbetjening</span><span class="sxs-lookup"><span data-stu-id="b8ee2-112">Configure the name of Employee self service</span></span>

<span data-ttu-id="b8ee2-113">I **Parametre for Human Resources** kan du nu ændre navnet på arbejdsområdet **Medarbejderselvbetjening** til **Selvbetjening**.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-113">In **Human Resources parameters**, you can now change the name of the **Employee self service** workspace to **Self service**.</span></span> <span data-ttu-id="b8ee2-114">Yderligere oplysninger finder du i [Skifte arbejdsområdenavn for medarbejderselvbetjening](hr-employee-self-service-workspace-name.md).</span><span class="sxs-lookup"><span data-stu-id="b8ee2-114">For more information, see [Change Employee self service workspace name](hr-employee-self-service-workspace-name.md)</span></span>

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a><span data-ttu-id="b8ee2-115">Adgang til styring af åben tilmelding til frynsegoder uden for periode</span><span class="sxs-lookup"><span data-stu-id="b8ee2-115">Benefits management open enrollment access outside of period</span></span>

<span data-ttu-id="b8ee2-116">Denne frigivelse løser en fejl, hvor medarbejdere kan få adgang til åben tilmelding til frynsegoder uden for tilmeldingsperioden eller uden en livshændelse.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-116">This release fixes a bug where employees could access benefits open enrollment outside of the enrollment period or without a life event.</span></span> <span data-ttu-id="b8ee2-117">Derfor skal du justere de åbne tilmeldingsdatoer til i dag (eller tidligere) for at gøre den tilgængelig, hvis du har brug for at demonstrere den åbne tilmelding i Medarbejderselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-117">As a result, if you need to demo open enrollment in Employee self service, you must adjust the open enrollment dates to today (or earlier) to make it accessible.</span></span> <span data-ttu-id="b8ee2-118">Du kan ændre denne indstilling under **Frynsegodeadministration > Regler og indstillingsperioder**.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-118">You can change this setting under **Benefits management > Rules and options periods**.</span></span>

## <a name="email-employee-enrollment-confirmation"></a><span data-ttu-id="b8ee2-119">Bekræftelse af tilmelding på e-mail til medarbejdere</span><span class="sxs-lookup"><span data-stu-id="b8ee2-119">Email employee enrollment confirmation</span></span>

<span data-ttu-id="b8ee2-120">Du kan nu sende mails til medarbejdere, når de har fuldført valget af frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-120">You can now send emails to employees after they complete their benefits selection.</span></span> <span data-ttu-id="b8ee2-121">Du kan enten sende en standardmeddelelse eller bruge en e-mailskabelon fra organisationen.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-121">You can either send a default message or use an organization email template.</span></span> <span data-ttu-id="b8ee2-122">Disse indstillinger er under **Parametre for Human Resources > Frynsegodeadministration**.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-122">These settings are under **Human resource parameters > Benefits management**.</span></span>

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a><span data-ttu-id="b8ee2-123">Annulleret orlov vises stadig i forestående fritid i arbejdsområdet Personer (441358)</span><span class="sxs-lookup"><span data-stu-id="b8ee2-123">Canceled leave still appears in upcoming time off on People workspace (441358)</span></span>

<span data-ttu-id="b8ee2-124">Annulleret orlov vises ikke længere som kommende fritid på orlovskortene i arbejdsområdet **Personer**.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-124">Canceled leave no longer displays as upcoming time off on the leave cards in the **People** workspace.</span></span>

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a><span data-ttu-id="b8ee2-125">Kan ikke bruge egenskaben for afdelingsenhed i PositionV2-enhed (456486)</span><span class="sxs-lookup"><span data-stu-id="b8ee2-125">Unable to use the department entity property in the PositionV2 entity (456486)</span></span>

<span data-ttu-id="b8ee2-126">Du kan nu tilføje en afdeling uden at oprette en dubleret relation.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-126">You can now add a department without creating a duplicate relation.</span></span>

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a><span data-ttu-id="b8ee2-127">PayrollWorkerEnrolledBenefitDetailEntity må kun bruge beregnet felt til pensionsordninger (459779)</span><span class="sxs-lookup"><span data-stu-id="b8ee2-127">PayrollWorkerEnrolledBenefitDetailEntity should only use calculated field for retirement plans (459779)</span></span>

<span data-ttu-id="b8ee2-128">Når du eksporterer enheden **LønArbejderTilmeldtFrynsegodeDetaljeEnhed**, bestemmer eksporten, om det skal bruge et beregnet felt, der er baseret på en satstabel, eller ved hjælp af feltet **BidragBeløbVal** i den understøttende tabel.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-128">When exporting the **PayrollWorkerEnrolledBenefitDetailEntity** entity, the export determines whether it should use a calculated field based on a rate table or use the **ContributionAmountCur** field on the backing table.</span></span> <span data-ttu-id="b8ee2-129">Den logik, der bruges af dataenheden, bruger satstabellen i situationer, hvor programmet normalt ikke gør.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-129">The logic used by the data entity uses the rate table in situations where the application normally doesn't.</span></span> <span data-ttu-id="b8ee2-130">Denne logik medfører, at enhedseksporten returnerer en nulværdi til denne kolonne, da der ikke findes nogen beregningssatstabel, og produktet ikke giver kunden mulighed for at angive en.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-130">This logic causes the entity exports to return a zero value for this column, because there's no calculation rate table and the product doesn't allow the customer to specify one.</span></span>
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a><span data-ttu-id="b8ee2-131">Forvirrende oversættelser på tjekkisk i Personalestyring og Medarbejderselvbetjening (400276)</span><span class="sxs-lookup"><span data-stu-id="b8ee2-131">Confusing translations in Czech language in Personnel management and Employee self service (400276)</span></span>

<span data-ttu-id="b8ee2-132">Denne udgivelse retter de oversættelser for **Firmaadressekartotek**, **Næste registrerede kursus**, **Job** og **Stilling**.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-132">This release corrects the translations for **Company directory**, **Next registered course**, **Job**, and **Position**.</span></span>
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a><span data-ttu-id="b8ee2-133">Systemfelterne Oprettet og Redigeret er ikke aktiveret i tabellen ArbejdkalenderAnsættelse (460171)</span><span class="sxs-lookup"><span data-stu-id="b8ee2-133">The WorkCalendarEmployment table doesn't have the created and modified system fields enabled (460171)</span></span>

<span data-ttu-id="b8ee2-134">Systemfelter Oprettet og Ændret er nu aktiveret i tabellen **ArbejdkalenderAnsættelse** i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-134">Created and modified system fields are now enabled on the **WorkCalendarEmployment** table in Human Resources.</span></span>
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a><span data-ttu-id="b8ee2-135">Null-referenceundtagelse for ansættelse, og tilføj oplysninger om fremtidig medarbejder (455475)</span><span class="sxs-lookup"><span data-stu-id="b8ee2-135">Null reference exception for Hire and add details for future employee (455475)</span></span>

<span data-ttu-id="b8ee2-136">Denne version retter en fejl (null-reference) i strømlinet medarbejderpost, når du ansætter en medarbejder med mulighed for at **ansætte og tilføje oplysninger**.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-136">This release corrects an error (null reference) in streamlined employee entry when you hire an employee using the option to **Hire and add details**.</span></span>

## <a name="changes-made-in-the-dataverse-worker-entity-dont-reflect-in-human-resources-455652"></a><span data-ttu-id="b8ee2-137">Ændringer, der foretages i Dataverse-arbejderenheden, afspejles ikke i Human Resources (455652)</span><span class="sxs-lookup"><span data-stu-id="b8ee2-137">Changes made in the Dataverse Worker entity don't reflect in Human Resources (455652)</span></span>

<span data-ttu-id="b8ee2-138">Ændringer, der foretages af følgende felter i enheden **Arbejder** i Dataverse, vises nu i Human Resources:</span><span class="sxs-lookup"><span data-stu-id="b8ee2-138">Changes made to the following fields in the **Worker** entity in Dataverse will now show up in Human Resources:</span></span>

- <span data-ttu-id="b8ee2-139">**Arbejder hjemmefra**</span><span class="sxs-lookup"><span data-stu-id="b8ee2-139">**Works from home**</span></span>
- <span data-ttu-id="b8ee2-140">**Anciennitetsdato**</span><span class="sxs-lookup"><span data-stu-id="b8ee2-140">**Seniority date**</span></span>
- <span data-ttu-id="b8ee2-141">**Jubilæumsdato**</span><span class="sxs-lookup"><span data-stu-id="b8ee2-141">**Anniversary date**</span></span>
- <span data-ttu-id="b8ee2-142">**Oprindelig ansættelsesdato**</span><span class="sxs-lookup"><span data-stu-id="b8ee2-142">**Original hire date**</span></span>

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a><span data-ttu-id="b8ee2-143">Korrekt kompensationsniveau er ikke standard baseret på det job, der er tildelt stillingen (394136)</span><span class="sxs-lookup"><span data-stu-id="b8ee2-143">Correct compensation level doesn't default based on the job assigned to the position (394136)</span></span>

<span data-ttu-id="b8ee2-144">Med denne ændring anvender det korrekte kompensationsniveau standardindstillingen baseret på **Gældende dato**-poster for **Detaljer for stilling** og **Startdato** for **Tildeling af kompensationsordning**.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-144">With this change, the correct compensation level defaults based on the **Date effective** records for the **Position details** and the **Start date** of the **Compensation plan assignment**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="b8ee2-145">Som eksempel</span><span class="sxs-lookup"><span data-stu-id="b8ee2-145">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="b8ee2-146">Obligatoriske felter</span><span class="sxs-lookup"><span data-stu-id="b8ee2-146">Mandatory fields</span></span> 

<span data-ttu-id="b8ee2-147">Du kan nu gøre felter obligatoriske ved hjælp af funktionerne til tilpasning til personale.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-147">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="b8ee2-148">Denne funktion kræver **Gemte visninger**.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-148">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="b8ee2-149">Human Resources-app i Teams</span><span class="sxs-lookup"><span data-stu-id="b8ee2-149">Human Resources application in Teams</span></span>

<span data-ttu-id="b8ee2-150">Medarbejderne kan få vist og anmode om fri fra arbejde i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-150">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="b8ee2-151">De kan interagere med en bot for at oprette orlovsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-151">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="b8ee2-152">Yderligere oplysninger finder du i [Human Resources-appen i Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="b8ee2-152">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="b8ee2-153">DMF-enheder (Data Management Framework) til styring af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="b8ee2-153">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="b8ee2-154">Enheder til håndtering af frynsegoder frigives.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-154">Benefits management entities are releasing.</span></span> <span data-ttu-id="b8ee2-155">Med DMF-enheder kan du importere og eksportere data, så du nemt kan konfigurere frynsegodestyring.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-155">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="b8ee2-156">En skabelon til frynsegodestyring kan også bruges til at flytte data.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-156">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="b8ee2-157">Skabelonen eksporterer og importerer dataene sekventielt for at respektere dataafhængigheder.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-157">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="b8ee2-158">Købe og sælge orlov</span><span class="sxs-lookup"><span data-stu-id="b8ee2-158">Buy and sell leave</span></span> 

<span data-ttu-id="b8ee2-159">Nogle organisationer giver et frynsegode, der giver medarbejderne mulighed for at købe eller sælge deres orlov.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-159">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="b8ee2-160">Denne proces styres ofte manuelt.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-160">This process is often managed manually.</span></span> <span data-ttu-id="b8ee2-161">Denne funktion automatiserer administration af politikker og anmodninger for HR-afdelingen.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-161">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="b8ee2-162">Den effektiviserer orlovsprocessen og medvirker til at eliminere fejltagelser.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-162">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="b8ee2-163">Du kan finde flere oplysninger i:</span><span class="sxs-lookup"><span data-stu-id="b8ee2-163">For more information, see:</span></span>

- [<span data-ttu-id="b8ee2-164">Administrere politikker for køb og salg af orlov</span><span class="sxs-lookup"><span data-stu-id="b8ee2-164">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="b8ee2-165">Købe og sælge orlov</span><span class="sxs-lookup"><span data-stu-id="b8ee2-165">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="b8ee2-166">Orlovsperiodisering for et enkelt firma eller en enkelt plan</span><span class="sxs-lookup"><span data-stu-id="b8ee2-166">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="b8ee2-167">Kunderne kan behandle periodiseringer for et enkelt firma eller en enkelt orlovs- fraværsplan.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-167">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="b8ee2-168">Denne mulighed giver klarhed over periodiseringsprocessen for kunder med forskellige sabbatår eller politikker for orlovsperiodisering.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-168">This ability provides clarity for the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="b8ee2-169">Du kan finde flere oplysninger under [Periodiseret orlov pr. firma eller pr. orlovsplan](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="b8ee2-169">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="b8ee2-170">Føje vedhæftede filer til anmodninger om fravær</span><span class="sxs-lookup"><span data-stu-id="b8ee2-170">Add attachments to time-off requests</span></span>

<span data-ttu-id="b8ee2-171">Muligheden for at føje vedhæftede filer til anmodninger om godkendt orlov er afgørende i det aktuelle COVID-19-miljø.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-171">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="b8ee2-172">Medarbejderne kan nu tilføje disse vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-172">Employees can now add these attachments.</span></span> <span data-ttu-id="b8ee2-173">De har også en mere indsigt i, hvordan der foretages opdateringer af anmodninger om orlov.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-173">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="b8ee2-174">Du kan finde flere oplysninger under [Føje en vedhæftet fil til en eksisterende anmodning](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="b8ee2-174">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="b8ee2-175">Føje årsagskode til periodiseringssuspenderinger</span><span class="sxs-lookup"><span data-stu-id="b8ee2-175">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="b8ee2-176">Årsagskoder er føjet til periodiseringssuspenderingen.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-176">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="b8ee2-177">Overføre regler</span><span class="sxs-lookup"><span data-stu-id="b8ee2-177">Carry forward rules</span></span> 

<span data-ttu-id="b8ee2-178">Du kan angive en orlovstype for overførselssaldi, hvor gennemførte reguleringer overføres.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-178">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="b8ee2-179">Hvis en medarbejder f.eks. overfører 10 dage, kan du vælge en anden orlovstype for disse 10 dage.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-179">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="b8ee2-180">Du kan finde flere oplysninger i [Konfigurere orlovs- og fraværstyper](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="b8ee2-180">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="b8ee2-181">Suspendere orlovsperiodisering for angivne orlovstyper</span><span class="sxs-lookup"><span data-stu-id="b8ee2-181">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="b8ee2-182">Du kan oprette en regel om suspendering af orlovsperiodiseringer for medarbejdere med orlovsanmodninger, der er angivet til ubetalt orlov.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-182">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="b8ee2-183">Ubetalt orlov kan være en type, men behøver ikke at være det.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-183">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="b8ee2-184">Du kan suspendere enhver orlov baseret på en anden orlovstype.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-184">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="b8ee2-185">DMF-enhed er tilgængelig for periodiseringssuspenderinger</span><span class="sxs-lookup"><span data-stu-id="b8ee2-185">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="b8ee2-186">En DMF-enhed er nu tilgængelig for periodiseringssuspenderinger.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-186">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="b8ee2-187">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="b8ee2-187">Coming soon</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="b8ee2-188">Kontrollisteenheder inkluderet i Dataverse</span><span class="sxs-lookup"><span data-stu-id="b8ee2-188">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="b8ee2-189">Der vil snart være tilgængelige kontrollisteenheder til processer til onboarding, offboarding, overførsler og forretning i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b8ee2-189">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8ee2-190">Se også</span><span class="sxs-lookup"><span data-stu-id="b8ee2-190">See also</span></span>

[<span data-ttu-id="b8ee2-191">Nyheder eller ændringer i Human Resources</span><span class="sxs-lookup"><span data-stu-id="b8ee2-191">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="b8ee2-192">Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2</span><span class="sxs-lookup"><span data-stu-id="b8ee2-192">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="b8ee2-193">Opdater proces</span><span class="sxs-lookup"><span data-stu-id="b8ee2-193">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="b8ee2-194">Administrere funktioner</span><span class="sxs-lookup"><span data-stu-id="b8ee2-194">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]