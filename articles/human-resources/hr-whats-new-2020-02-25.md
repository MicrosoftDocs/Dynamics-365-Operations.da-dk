---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (25. februar 2020)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 02/25/2020
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
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e5bc232bef257e757086d37d56b0f68b80114749
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555069"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a><span data-ttu-id="c276f-103">Nyheder eller ændringer i Dynamics 365 Human Resources (25. februar 2020)</span><span class="sxs-lookup"><span data-stu-id="c276f-103">What's new or changed in Dynamics 365 Human Resources (February 25, 2020)</span></span>

<span data-ttu-id="c276f-104">I denne artikel beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c276f-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="c276f-105">Ændringerne gælder for build nummer 8.1.2927.</span><span class="sxs-lookup"><span data-stu-id="c276f-105">Changes apply to build number 8.1.2927.</span></span> <span data-ttu-id="c276f-106">Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.</span><span class="sxs-lookup"><span data-stu-id="c276f-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a><span data-ttu-id="c276f-107">Aktivér navigation i Sagsstyring og datastyringsobjektenhed (DMF) (414754)</span><span class="sxs-lookup"><span data-stu-id="c276f-107">Enable Case Management navigation and data management framework (DMF) entity (414754)</span></span>

<span data-ttu-id="c276f-108">Denne eksempelfunktion aktiverer yderligere navigation til sager i Sagsstyring.</span><span class="sxs-lookup"><span data-stu-id="c276f-108">This preview feature enables additional navigation to case management cases.</span></span> <span data-ttu-id="c276f-109">Du kan aktivere denne visningsfunktion i arbejdsområdet **Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="c276f-109">You can enable this preview feature in the **Feature Management** workspace.</span></span> <span data-ttu-id="c276f-110">Disse menupunkter vises i arbejdsområdet **Overholdelse** i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c276f-110">These menu items appear in the **Compliance** workspace of Dynamics 365 Human Resources.</span></span> <span data-ttu-id="c276f-111">Med denne ændring har HR adgang til:</span><span class="sxs-lookup"><span data-stu-id="c276f-111">With this change, Human Resources can access:</span></span>

- <span data-ttu-id="c276f-112">Alle sager</span><span class="sxs-lookup"><span data-stu-id="c276f-112">All cases</span></span>
- <span data-ttu-id="c276f-113">Mine sager</span><span class="sxs-lookup"><span data-stu-id="c276f-113">My cases</span></span>
- <span data-ttu-id="c276f-114">Mine åbne sager</span><span class="sxs-lookup"><span data-stu-id="c276f-114">My open cases</span></span>
- <span data-ttu-id="c276f-115">Mine forsinkede sager</span><span class="sxs-lookup"><span data-stu-id="c276f-115">My overdue cases</span></span>
- <span data-ttu-id="c276f-116">Sager, der er tildelt mig via arbejdsgangen</span><span class="sxs-lookup"><span data-stu-id="c276f-116">Cases assigned to me through workflow</span></span>

<span data-ttu-id="c276f-117">Sammen med disse nye visninger i sager er DMF-enheden **Sagsoplysninger** også tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="c276f-117">Along with these new views into cases, the **Case detail** DMF entity is also available.</span></span>

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a><span data-ttu-id="c276f-118">Aktivér Relationsdefinitioner i det globale adressekartotek (414762)</span><span class="sxs-lookup"><span data-stu-id="c276f-118">Enable Relationship definitions in global address bBook (414762)</span></span>

<span data-ttu-id="c276f-119">Relationer er nu aktiveret i det globale adressekartotek.</span><span class="sxs-lookup"><span data-stu-id="c276f-119">Relationships are now enabled in the global address book.</span></span> <span data-ttu-id="c276f-120">Før denne uges udgivelse viste faktafeltet **Relationer** alle systemdefinerede relationer.</span><span class="sxs-lookup"><span data-stu-id="c276f-120">Prior to this week's release, the **Relationship** fact box displayed any system-defined relationships.</span></span> <span data-ttu-id="c276f-121">Nu kan du definere disse relationer på siden med det globale adressekartotek.</span><span class="sxs-lookup"><span data-stu-id="c276f-121">Now you can define those relationships within the global address book page.</span></span>

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a><span data-ttu-id="c276f-122">En stilling kan fjernes, når der findes aktive kompensationsposter for stillingen (414568)</span><span class="sxs-lookup"><span data-stu-id="c276f-122">A position can be removed when active compensation records exist for the position (414568)</span></span>

<span data-ttu-id="c276f-123">Med denne ændring vises en advarsel, når du forsøger at slette en stilling, og en arbejder har en aktiv kompensationspost for samme stilling.</span><span class="sxs-lookup"><span data-stu-id="c276f-123">With this change, a warning appears when you attempt to delete a position and a worker has an active compensation record for that same position.</span></span> <span data-ttu-id="c276f-124">Når det sker, skal du opdatere medarbejderens faste løn-post, før stillingen fjernes.</span><span class="sxs-lookup"><span data-stu-id="c276f-124">When this happens, you must update the employee fixed compensation record before removing the position.</span></span>

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a><span data-ttu-id="c276f-125">Arbejdsprocessen for gennemgang af ydeevne tilføjer indimellem godkendelser fra personer, der ikke er en del af processen (414171)</span><span class="sxs-lookup"><span data-stu-id="c276f-125">Performance review workflow occasionally adds sign-offs from people who are not part of the process (414171)</span></span>

<span data-ttu-id="c276f-126">Denne ændring retter et problem, hvor yderligere godkendelsesdeltagere føjes til gennemsynet af ydeevnen.</span><span class="sxs-lookup"><span data-stu-id="c276f-126">This change corrects an issue where additional sign-off participants are added to the performance review.</span></span>

## <a name="worker-position-assignment-not-created-in-common-data-service-when-selected-on-the-new-worker-dialog-413479"></a><span data-ttu-id="c276f-127">Tildelingen af arbejderstilling, der ikke er oprettet i Common Data Service, da den blev valgt i dialogboksen Ny arbejder (413479)</span><span class="sxs-lookup"><span data-stu-id="c276f-127">Worker position assignment not created in Common Data Service when selected on the New Worker dialog (413479)</span></span>

<span data-ttu-id="c276f-128">Denne ændring retter en fejl, når du ansætter en ny arbejder og tildeler den nye ansættelse til en stilling via dialogboksen **Ny medarbejder**.</span><span class="sxs-lookup"><span data-stu-id="c276f-128">This change corrects an issue when hiring a new worker and assigning the new hire to a position through the **New worker** dialog.</span></span> <span data-ttu-id="c276f-129">Nu afspejles stillingstildelingen i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="c276f-129">Now the position assignment is reflected in Common Data Service.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="c276f-130">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="c276f-130">Coming soon</span></span>

### <a name="updated-common-data-service-solution"></a><span data-ttu-id="c276f-131">Opdateret Common Data Service-løsning</span><span class="sxs-lookup"><span data-stu-id="c276f-131">Updated Common Data Service solution</span></span>

<span data-ttu-id="c276f-132">Der vil snart være en ny Common Data Service-løsning med følgende ændringer:</span><span class="sxs-lookup"><span data-stu-id="c276f-132">A new Common Data Service solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="c276f-133">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c276f-133">Description</span></span> | <span data-ttu-id="c276f-134">Forskydning</span><span class="sxs-lookup"><span data-stu-id="c276f-134">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="c276f-135">Ændringer i objektet **Job/Stilling**</span><span class="sxs-lookup"><span data-stu-id="c276f-135">**Job/Position** entity changes</span></span> | <span data-ttu-id="c276f-136">**Kompensationsområde** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="c276f-136">**Compensation region** added</span></span></br><span data-ttu-id="c276f-137">**Økonomiske dimensioner** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="c276f-137">**Financial dimensions** added</span></span> |
| <span data-ttu-id="c276f-138">Ændringer i objektet **Arbejder**</span><span class="sxs-lookup"><span data-stu-id="c276f-138">**Worker** entity changes</span></span> | <span data-ttu-id="c276f-139">**Navnerækkefølge** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="c276f-139">**Name sequence** added</span></span></br><span data-ttu-id="c276f-140">**Arbejder hjemmefra** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="c276f-140">**Works from home** added</span></span></br><span data-ttu-id="c276f-141">**Sprog** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="c276f-141">**Language** added</span></span></br><span data-ttu-id="c276f-142">**Anciennitetsdato** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="c276f-142">**Seniority date** added</span></span></br><span data-ttu-id="c276f-143">**Jubilæumsdato** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="c276f-143">**Anniversary date** added</span></span></br><span data-ttu-id="c276f-144">**Oprindelig ansættelsesdato** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="c276f-144">**Original hire date** added</span></span> |
| <span data-ttu-id="c276f-145">Ændringer af objektet **Ansættelse**</span><span class="sxs-lookup"><span data-stu-id="c276f-145">**Employment** entity changes</span></span> | <span data-ttu-id="c276f-146">**Økonomiske dimensioner** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="c276f-146">**Financial dimensions** added</span></span></br><span data-ttu-id="c276f-147">**Årsag til fratrædelse** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="c276f-147">**Termination reason** added</span></span></br><span data-ttu-id="c276f-148">**Fratrædelsesdato** er omdøbt fra **Overførselsdato**</span><span class="sxs-lookup"><span data-stu-id="c276f-148">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="c276f-149">**Datoer for prøvetid** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="c276f-149">**Probation date** added</span></span> |
| <span data-ttu-id="c276f-150">Ændringer i objektet **Arbejders adresse**</span><span class="sxs-lookup"><span data-stu-id="c276f-150">**Worker address** entity changes</span></span> | <span data-ttu-id="c276f-151">**Gadenavn** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="c276f-151">**Street address** added</span></span></br><span data-ttu-id="c276f-152">**Adresselinje 1**, **Adresselinje 2** og **Adresselinje 3** er markeret til udfasning</span><span class="sxs-lookup"><span data-stu-id="c276f-152">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="c276f-153">Nye konfigurationsobjekter til variabel kompensation</span><span class="sxs-lookup"><span data-stu-id="c276f-153">New variable compensation setup entities</span></span> | <span data-ttu-id="c276f-154">**Type af variabel kompensationsplan**</span><span class="sxs-lookup"><span data-stu-id="c276f-154">**Compensation variable plan type**</span></span></br><span data-ttu-id="c276f-155">**Kompensation - variabel struktur**</span><span class="sxs-lookup"><span data-stu-id="c276f-155">**Compensation variable plan**</span></span></br><span data-ttu-id="c276f-156">**Fordelingsregler**</span><span class="sxs-lookup"><span data-stu-id="c276f-156">**Vesting rules**</span></span></br><span data-ttu-id="c276f-157">**Niveau i variabel kompensationsplan**</span><span class="sxs-lookup"><span data-stu-id="c276f-157">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="c276f-158">Nyt objekt **Arbejderkalender for ansættelse**</span><span class="sxs-lookup"><span data-stu-id="c276f-158">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="c276f-159">**Arbejdskalenderobjekt** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="c276f-159">**Work calendar entity** added</span></span> |
| <span data-ttu-id="c276f-160">Nyt objekt **Lønoplysninger for stillinger**</span><span class="sxs-lookup"><span data-stu-id="c276f-160">New **Payroll position detail** entity</span></span> | <span data-ttu-id="c276f-161">**Lønoplysninger for stillinger** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="c276f-161">**Payroll position detail** added</span></span> |
| <span data-ttu-id="c276f-162">Nyt objekt **Titel**</span><span class="sxs-lookup"><span data-stu-id="c276f-162">New **Title** entity</span></span> | <span data-ttu-id="c276f-163">**Titel** er tilføjet.</span><span class="sxs-lookup"><span data-stu-id="c276f-163">**Title** added.</span></span> <span data-ttu-id="c276f-164">Den nye enhed **Titel** vil blive medtaget i synkroniseringsprocessen mellem Human Resources og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="c276f-164">The new **Title** entity will be included in the sync process between Human Resources and Common Data Service.</span></span> <span data-ttu-id="c276f-165">Der henvises ikke til den først i enhederne **Stilling** eller **Job**.</span><span class="sxs-lookup"><span data-stu-id="c276f-165">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

<span data-ttu-id="c276f-166">I løbet af de næste par uger vil disse enhedsændringer være tilgængelige i alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="c276f-166">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="c276f-167">Sådan installeres den nyeste Common Data Service-løsning til HR manuelt:</span><span class="sxs-lookup"><span data-stu-id="c276f-167">To manually install the latest Common Data Service solution for Human Resources:</span></span>

1.  <span data-ttu-id="c276f-168">Gå til [Power Platform Administration](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="c276f-168">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="c276f-169">Vælg **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="c276f-169">Select **Environments**.</span></span>

3.  <span data-ttu-id="c276f-170">Find det miljø, du vil opgradere.</span><span class="sxs-lookup"><span data-stu-id="c276f-170">Find the environment you want to upgrade.</span></span> <span data-ttu-id="c276f-171">Det skal svare til **Miljønavn** i sektionen **Common Data Service-oplysninger** i formularen **Om** i HR.</span><span class="sxs-lookup"><span data-stu-id="c276f-171">This should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="c276f-172">Vælg miljøet for at få vist miljødetaljerne.</span><span class="sxs-lookup"><span data-stu-id="c276f-172">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="c276f-173">Vælg **Administrer løsninger** på handlingslinjen i toppen.</span><span class="sxs-lookup"><span data-stu-id="c276f-173">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="c276f-174">Der åbnes et nyt browservindue, hvor du kan navigere til **Dynamics 365 Administration** i konteksten af dit miljø.</span><span class="sxs-lookup"><span data-stu-id="c276f-174">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="c276f-175">Vælg **Dynamics 365 Human Resources Anchor** i listen **Løsning**.</span><span class="sxs-lookup"><span data-stu-id="c276f-175">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="c276f-176">Vælg **Opgrader** for at anvende den seneste løsning.</span><span class="sxs-lookup"><span data-stu-id="c276f-176">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="in-preview"></a><span data-ttu-id="c276f-177">Som eksempel</span><span class="sxs-lookup"><span data-stu-id="c276f-177">In preview</span></span>

<span data-ttu-id="c276f-178">Følgende prøvefunktioner blev tilgængelige d. 3. februar 2020:</span><span class="sxs-lookup"><span data-stu-id="c276f-178">The following preview features became available on February 3, 2020:</span></span>

- <span data-ttu-id="c276f-179">**Visningsfunktioner for orlov og fravær** - Du kan finde flere oplysninger under [Visningsfunktioner for orlov og fravær](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span><span class="sxs-lookup"><span data-stu-id="c276f-179">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="c276f-180">**Prøveversionsfunktion: Administration af frynsegoder** – Der er flere oplysninger, herunder kendte problemer, under [Oversigt over Administration af frynsegoder](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c276f-180">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c276f-181">Se også</span><span class="sxs-lookup"><span data-stu-id="c276f-181">See also</span></span>

[<span data-ttu-id="c276f-182">Nyheder eller ændringer i Human Resources</span><span class="sxs-lookup"><span data-stu-id="c276f-182">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="c276f-183">Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2</span><span class="sxs-lookup"><span data-stu-id="c276f-183">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="c276f-184">Opdater proces</span><span class="sxs-lookup"><span data-stu-id="c276f-184">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="c276f-185">Administrere funktioner</span><span class="sxs-lookup"><span data-stu-id="c276f-185">Manage features</span></span>](hr-admin-manage-features.md)