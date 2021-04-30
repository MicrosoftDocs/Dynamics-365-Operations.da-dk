---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (16. september 2020)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 16. september 2020.
author: jcart1106
ms.date: 09/16/2020
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
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6b07bfb27bbe5e546dac9d72666b3225cc202670
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890693"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a><span data-ttu-id="0b003-103">Nyheder eller ændringer i Dynamics 365 Human Resources (16. september 2020)</span><span class="sxs-lookup"><span data-stu-id="0b003-103">What's new or changed in Dynamics 365 Human Resources (September 16, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0b003-104">I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0b003-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="0b003-105">Ændringerne gælder for build nummer 8.1.3557.</span><span class="sxs-lookup"><span data-stu-id="0b003-105">Changes apply to build number 8.1.3557.</span></span> <span data-ttu-id="0b003-106">Tallene i parenteser ved siden af visse funktioner henviser til Lifecycle Services (LCS)-supportnumre til reference.</span><span class="sxs-lookup"><span data-stu-id="0b003-106">The numbers in parentheses next to some features refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="included-in-this-release"></a><span data-ttu-id="0b003-107">Inkluderet i denne version</span><span class="sxs-lookup"><span data-stu-id="0b003-107">Included in this release</span></span>

-  [<span data-ttu-id="0b003-108">Gemte visninger – generel tilgængelighed</span><span class="sxs-lookup"><span data-stu-id="0b003-108">Saved views - general availability</span></span>](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br><span data-ttu-id="0b003-109">- Du kan finde flere oplysninger i [Gemte visninger](../fin-ops-core/fin-ops/get-started/saved-views.md).</span><span class="sxs-lookup"><span data-stu-id="0b003-109">- For more information, see [Saved views](../fin-ops-core/fin-ops/get-started/saved-views.md).</span></span> 

- <span data-ttu-id="0b003-110">I formularen **Stillingshandlinger** findes et opdateret dimensionsgitter og en ny dialog (469495).</span><span class="sxs-lookup"><span data-stu-id="0b003-110">The **Position actions** form has an updated dimensions grid and new dialogue (469495).</span></span>

- <span data-ttu-id="0b003-111">Hvis du angiver **Begrænset adgang til arbejderoplysninger** til Ja i **Avanceret adgang** i **Delte Human Resources-parametre**, viser formen Frynsegoder nu kun de relevante arbejdere (393384).</span><span class="sxs-lookup"><span data-stu-id="0b003-111">If you set **Restrict access to worker information** to yes in **Advanced access** in **Human Resources Shared parameters**, benefits forms now show only the appropriate workers (393384).</span></span>

- <span data-ttu-id="0b003-112">Indstillinger for ny kalenderoprettelse i **WorkCalendar**-enheden (477055):</span><span class="sxs-lookup"><span data-stu-id="0b003-112">New calendar generation options in the **WorkCalendar** entity (477055):</span></span><br><span data-ttu-id="0b003-113">- Standardsluttidspunkt</span><span class="sxs-lookup"><span data-stu-id="0b003-113">- Default ending time</span></span><br><span data-ttu-id="0b003-114">- Standardstarttidspunkt</span><span class="sxs-lookup"><span data-stu-id="0b003-114">-    Default starting time</span></span><br><span data-ttu-id="0b003-115">- Fredag er arbejdsdag</span><span class="sxs-lookup"><span data-stu-id="0b003-115">-  Is Friday working day</span></span><br><span data-ttu-id="0b003-116">- Mandag er arbejdsdag</span><span class="sxs-lookup"><span data-stu-id="0b003-116">-  Is Monday working day</span></span><br><span data-ttu-id="0b003-117">- Lørdag er arbejdsdag</span><span class="sxs-lookup"><span data-stu-id="0b003-117">-  Is Saturday working day</span></span><br><span data-ttu-id="0b003-118">- Søndag er arbejdsdag</span><span class="sxs-lookup"><span data-stu-id="0b003-118">- Is Sunday working day</span></span><br><span data-ttu-id="0b003-119">- Torsdag er arbejdsdag</span><span class="sxs-lookup"><span data-stu-id="0b003-119">- Is Thursday working day</span></span><br><span data-ttu-id="0b003-120">- Tirsdag er arbejdsdag</span><span class="sxs-lookup"><span data-stu-id="0b003-120">- Is Tuesday working day</span></span><br><span data-ttu-id="0b003-121">- Onsdag er arbejdsdag</span><span class="sxs-lookup"><span data-stu-id="0b003-121">- Is Wednesday working day</span></span><br><span data-ttu-id="0b003-122">- Arbejdskalenderfridags-id</span><span class="sxs-lookup"><span data-stu-id="0b003-122">- Work calendar holiday ID</span></span>

- <span data-ttu-id="0b003-123">**LeaveBankTransactionV1**-enheden indeholder nu årsagskoden (477823).</span><span class="sxs-lookup"><span data-stu-id="0b003-123">The **LeaveBankTransactionV1** entity now includes the reason code (477823).</span></span>

- <span data-ttu-id="0b003-124">Du kan nu gemme opgaveregistreringer (492923).</span><span class="sxs-lookup"><span data-stu-id="0b003-124">You can now save task recordings (492923).</span></span>

- <span data-ttu-id="0b003-125">Data publiceres nu korrekt fra **HCMWorkerContactEntity** (427620).</span><span class="sxs-lookup"><span data-stu-id="0b003-125">Data is now published successfully from **HCMWorkerContactEntity** (427620).</span></span>

- <span data-ttu-id="0b003-126">Oversigtsfanen **Kompensation** vises nu for arbejdertypen kontrahent i formularen **Arbejderhandlinger** (482494).</span><span class="sxs-lookup"><span data-stu-id="0b003-126">The **Compensation** fast tab now displays for the contractor worker type in the **Worker actions** form (482494).</span></span>

- <span data-ttu-id="0b003-127">Felterne **Niveau** og **Plan** er nu obligatoriske, hvis der angives **Fast kompensation**.</span><span class="sxs-lookup"><span data-stu-id="0b003-127">The **Level** and **Plan** fields are now mandatory if you set **Fixed compensation**.</span></span> <span data-ttu-id="0b003-128">Der vises en fejlmeddelelse, hvis du ikke udfylder disse felter (482497).</span><span class="sxs-lookup"><span data-stu-id="0b003-128">An error message displays if you leave these fields blank (482497).</span></span>

- <span data-ttu-id="0b003-129">Feltet **Plantype** i **Frynsegoder** er nu en rulleliste (488768).</span><span class="sxs-lookup"><span data-stu-id="0b003-129">The **Plan type** field in **Benefits** is now a dropdown list (488768).</span></span>

- <span data-ttu-id="0b003-130">Systemadministratorer modtager nu en besked, hvis et brugerdefineret felt slettes fra Human Resources (481408).</span><span class="sxs-lookup"><span data-stu-id="0b003-130">System administrators now receive a notification if a custom field is deleted from Human Resources (481408).</span></span>

- <span data-ttu-id="0b003-131">Under processen til opsigelse af medarbejder fungerer Human Resources som forventet og ændrer ikke den valgte virksomhed efter at være blevet låst (479877).</span><span class="sxs-lookup"><span data-stu-id="0b003-131">During the terminate employee process, Human Resources behaves as expected and doesn't change the selected company after appearing to lock (479877).</span></span> 

- <span data-ttu-id="0b003-132">Ledere kan ikke længere tilføje en talkolonne ved hjælp af brugertilpasning (485317).</span><span class="sxs-lookup"><span data-stu-id="0b003-132">Managers can no longer add a number column through personalization (485317).</span></span>

- <span data-ttu-id="0b003-133">Ledere kan ikke længere fjerne dataområdefilteret fra de identifikationsnumre, der udløber (485321).</span><span class="sxs-lookup"><span data-stu-id="0b003-133">Managers can no longer remove the data range filter from identification numbers expiring (485321).</span></span>

- <span data-ttu-id="0b003-134">Når feltet **Rapporterer til** er tomt, vises der stadig stillingsdetaljer, når markøren hviler på stillingen (433328).</span><span class="sxs-lookup"><span data-stu-id="0b003-134">When the **Reports to** field is empty, position details still display when hovering over the position (433328).</span></span>

- <span data-ttu-id="0b003-135">Medarbejdere kan nu se oplysninger om frynsegodeplanen i Medarbejderselvbetjening (481676).</span><span class="sxs-lookup"><span data-stu-id="0b003-135">Employees can now view benefit plan information in Employee self service (481676).</span></span>

- <span data-ttu-id="0b003-136">Medarbejdere kan nu se alle tilmeldte kurser (429048).</span><span class="sxs-lookup"><span data-stu-id="0b003-136">Employees can now see all registered courses (429048).</span></span>

- <span data-ttu-id="0b003-137">Du kan nu begrænse visningsindstillingerne for siden **Professionelle certifikater**.</span><span class="sxs-lookup"><span data-stu-id="0b003-137">You can now restrict viewing options for the **Professional certificates** page.</span></span> <span data-ttu-id="0b003-138">Du kan begrænse visningsindstillinger til den aktuelle juridiske enhed efter arbejderstatus og arbejdertype (451501).</span><span class="sxs-lookup"><span data-stu-id="0b003-138">You can restrict viewing options to the current legal entity, by worker status, and by worker type (451501).</span></span> 


## <a name="in-preview"></a><span data-ttu-id="0b003-139">Som prøveversion</span><span class="sxs-lookup"><span data-stu-id="0b003-139">In Preview</span></span>

### <a name="human-resources-app-in-teams"></a><span data-ttu-id="0b003-140">Human Resources-app i Teams</span><span class="sxs-lookup"><span data-stu-id="0b003-140">Human Resources app in Teams</span></span>

<span data-ttu-id="0b003-141">Medarbejderne kan få vist og anmode om fri fra arbejde i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="0b003-141">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="0b003-142">De kan interagere med en bot for at oprette orlovsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="0b003-142">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="0b003-143">Du kan finde flere oplysninger i:</span><span class="sxs-lookup"><span data-stu-id="0b003-143">For more information, see:</span></span>

- <span data-ttu-id="0b003-144">[Løsning til medarbejderes orlov og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020-frigivelsesplan bølge 1</span><span class="sxs-lookup"><span data-stu-id="0b003-144">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="0b003-145">[Appen Human Resources i Teams](./hr-admin-teams-leave-app.md) i dokumentation til Human Resources</span><span class="sxs-lookup"><span data-stu-id="0b003-145">[Human Resources app in Teams](./hr-admin-teams-leave-app.md) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="0b003-146">Human Resources-app i Teams-prøveversionsfunktioner</span><span class="sxs-lookup"><span data-stu-id="0b003-146">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="0b003-147">**Beskeder**: Afsendere og godkendere af anmodninger om fritid får besked i appen Human Resources i Teams.</span><span class="sxs-lookup"><span data-stu-id="0b003-147">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="0b003-148">Godkendere kan godkende eller afvise anmodninger om fravær.</span><span class="sxs-lookup"><span data-stu-id="0b003-148">Approvers can approve or deny time-off requests.</span></span> <span data-ttu-id="0b003-149">Afsendere får besked, hvis anmodningen godkendes eller afvises.</span><span class="sxs-lookup"><span data-stu-id="0b003-149">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="0b003-150">Du kan finde flere oplysninger i:</span><span class="sxs-lookup"><span data-stu-id="0b003-150">For more information, see:</span></span>
   - <span data-ttu-id="0b003-151">[Løsning til medarbejderes orlov og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020-frigivelsesplan bølge 2</span><span class="sxs-lookup"><span data-stu-id="0b003-151">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="0b003-152">[Aktivere beskeder for appen Human Resources i Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) i dokumentation til Human Resources</span><span class="sxs-lookup"><span data-stu-id="0b003-152">[Enable notifications for the Human Resources app in Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="0b003-153">[Slå Teams-beskeder til eller fra for de enkelte brugere](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) i dokumentationen til Human Resources</span><span class="sxs-lookup"><span data-stu-id="0b003-153">[Turn Teams notifications on or off for individual users](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="0b003-154">[Teams-beskeder](./hr-teams-leave-app.md#respond-to-teams-notifications) i dokumentationen til Human Resources</span><span class="sxs-lookup"><span data-stu-id="0b003-154">[Teams notifications](./hr-teams-leave-app.md#respond-to-teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="0b003-155">[Se dit teams orlovskalender](./hr-teams-leave-app.md#view-your-teams-leave-calendar) i dokumentationen til Human Resources</span><span class="sxs-lookup"><span data-stu-id="0b003-155">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="0b003-156">**Fraværskalender for leder**: Ledere kan se godkendte og afventende fravær for deres direkte underordnede i en kalendervisning.</span><span class="sxs-lookup"><span data-stu-id="0b003-156">**Manager time-off calendar**: Managers can see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="0b003-157">Denne visning giver en nem forståelse af, hvornår teammedlemmer ikke er på arbejde.</span><span class="sxs-lookup"><span data-stu-id="0b003-157">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="0b003-158">Du kan finde flere oplysninger i:</span><span class="sxs-lookup"><span data-stu-id="0b003-158">For more information, see:</span></span>
   - <span data-ttu-id="0b003-159">[Løsning til medarbejderes orlov og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020-frigivelsesplan bølge 2</span><span class="sxs-lookup"><span data-stu-id="0b003-159">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="0b003-160">[Se dit teams orlovskalender](./hr-teams-leave-app.md#view-your-teams-leave-calendar) i dokumentationen til Human Resources</span><span class="sxs-lookup"><span data-stu-id="0b003-160">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="0b003-161">Konfigurationsindstilling til placering af listen Workflowopgaver, der er tildelt til mig (477004)</span><span class="sxs-lookup"><span data-stu-id="0b003-161">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="0b003-162">En ny indstilling er nu tilgængelig til at placere listen **Workflowopgaver, der er tildelt til mig**, i kolonnen til højre på dashboardet.</span><span class="sxs-lookup"><span data-stu-id="0b003-162">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="0b003-163">Med denne ændring vises alle arbejdsopgaver og opgavelister i samme område.</span><span class="sxs-lookup"><span data-stu-id="0b003-163">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="0b003-164">Aktivér denne funktion ved at aktivere **Prøveversion – forbedringer af arbejdsgangsoplevelsen** i Funktionsstyring.</span><span class="sxs-lookup"><span data-stu-id="0b003-164">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="0b003-165">Du kan få flere oplysninger om aktivering af prøveversionsfunktioner under [Administrere funktioner](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="0b003-165">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="0b003-166">Denne funktion fremhæver også de arbejdsprocesindstillinger, der vises i formularen til personalehandlinger.</span><span class="sxs-lookup"><span data-stu-id="0b003-166">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="0b003-167">Der vises også indstillinger for arbejdsgangen over fanen til hurtig handling med nem adgang til.</span><span class="sxs-lookup"><span data-stu-id="0b003-167">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="0b003-168">Du kan finde flere oplysninger i:</span><span class="sxs-lookup"><span data-stu-id="0b003-168">For more information, see:</span></span> 

- <span data-ttu-id="0b003-169">[Forbedringer af arbejdsprocesser for organisation og personalestyring](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) i Dynamics 365: 2020-frigivelsesplan bølge 2</span><span class="sxs-lookup"><span data-stu-id="0b003-169">[Organization and personnel management workflow experience enhancements](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![Workflowopgaver, der er tildelt til mig](./media/hr-workflow-work-items-assigned-to-me.png)

![Hurtig adgang til arbejdsgangselementer](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a><span data-ttu-id="0b003-172">Kalender for orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="0b003-172">Leave and absence calendar</span></span>

<span data-ttu-id="0b003-173">Denne frigivelse indeholder yderligere kalenderindstillinger for orlovs- og fraværskalendere.</span><span class="sxs-lookup"><span data-stu-id="0b003-173">This release includes additional calendar options for leave and absence calendars.</span></span> <span data-ttu-id="0b003-174">Du kan finde flere oplysninger i [Vise team- og firmakalendere](./hr-employee-self-service-calendar.md).</span><span class="sxs-lookup"><span data-stu-id="0b003-174">For more information, see [View team and company calendars](./hr-employee-self-service-calendar.md).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="0b003-175">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="0b003-175">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="0b003-176">Kontrollisteenheder inkluderet i Dataverse</span><span class="sxs-lookup"><span data-stu-id="0b003-176">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="0b003-177">Der vil snart være tilgængelige kontrollisteenheder til processer til onboarding, offboarding, overførsler og forretning i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="0b003-177">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="0b003-178">Årsagskoder for administration af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="0b003-178">Benefits management reason codes</span></span>

<span data-ttu-id="0b003-179">Årsagskoder for administration af frynsegoder vil snart blive kombineret med eksisterende årsagskoder i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0b003-179">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="0b003-180">Hvis du har oprettet årsagskoder i Frynsegodeadministration på mere end 15 tegn, skal du ændre navnet på årsagskoden i formen **Årsagskoder** for Frynsegodeadministration til højst 15 tegn.</span><span class="sxs-lookup"><span data-stu-id="0b003-180">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="0b003-181">Når du har opdateret navnet, vises årsagskoden under den eksisterende formular til årsagskode i Personalestyring.</span><span class="sxs-lookup"><span data-stu-id="0b003-181">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="0b003-182">Denne ændring vil være tilgængelig i fremtiden og vil ikke påvirke den eksisterende funktion.</span><span class="sxs-lookup"><span data-stu-id="0b003-182">This change will be available in the future and won't affect existing functionality.</span></span>

## <a name="see-also"></a><span data-ttu-id="0b003-183">Se også</span><span class="sxs-lookup"><span data-stu-id="0b003-183">See also</span></span>

[<span data-ttu-id="0b003-184">Nyheder eller ændringer i Human Resources</span><span class="sxs-lookup"><span data-stu-id="0b003-184">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="0b003-185">Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2</span><span class="sxs-lookup"><span data-stu-id="0b003-185">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="0b003-186">Opdater proces</span><span class="sxs-lookup"><span data-stu-id="0b003-186">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="0b003-187">Administrere funktioner</span><span class="sxs-lookup"><span data-stu-id="0b003-187">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
