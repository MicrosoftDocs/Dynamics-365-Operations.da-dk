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
ms.openlocfilehash: 720b4e03549a059c8945bec9d27de9cdcaada488
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092746"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a><span data-ttu-id="3a62d-103">Nyheder eller ændringer i Dynamics 365 Human Resources (25. februar 2020)</span><span class="sxs-lookup"><span data-stu-id="3a62d-103">What's new or changed in Dynamics 365 Human Resources (February 25, 2020)</span></span>

<span data-ttu-id="3a62d-104">I denne artikel beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3a62d-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="3a62d-105">Ændringerne gælder for build nummer 8.1.2927.</span><span class="sxs-lookup"><span data-stu-id="3a62d-105">Changes apply to build number 8.1.2927.</span></span> <span data-ttu-id="3a62d-106">Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.</span><span class="sxs-lookup"><span data-stu-id="3a62d-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a><span data-ttu-id="3a62d-107">Aktivér navigation i Sagsstyring og datastyringsobjektenhed (DMF) (414754)</span><span class="sxs-lookup"><span data-stu-id="3a62d-107">Enable Case Management navigation and data management framework (DMF) entity (414754)</span></span>

<span data-ttu-id="3a62d-108">Denne eksempelfunktion aktiverer yderligere navigation til sager i Sagsstyring.</span><span class="sxs-lookup"><span data-stu-id="3a62d-108">This preview feature enables additional navigation to case management cases.</span></span> <span data-ttu-id="3a62d-109">Du kan aktivere denne visningsfunktion i arbejdsområdet **Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="3a62d-109">You can enable this preview feature in the **Feature Management** workspace.</span></span> <span data-ttu-id="3a62d-110">Disse menupunkter vises i arbejdsområdet **Overholdelse** i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3a62d-110">These menu items appear in the **Compliance** workspace of Dynamics 365 Human Resources.</span></span> <span data-ttu-id="3a62d-111">Med denne ændring har HR adgang til:</span><span class="sxs-lookup"><span data-stu-id="3a62d-111">With this change, Human Resources can access:</span></span>

- <span data-ttu-id="3a62d-112">Alle sager</span><span class="sxs-lookup"><span data-stu-id="3a62d-112">All cases</span></span>
- <span data-ttu-id="3a62d-113">Mine sager</span><span class="sxs-lookup"><span data-stu-id="3a62d-113">My cases</span></span>
- <span data-ttu-id="3a62d-114">Mine åbne sager</span><span class="sxs-lookup"><span data-stu-id="3a62d-114">My open cases</span></span>
- <span data-ttu-id="3a62d-115">Mine forsinkede sager</span><span class="sxs-lookup"><span data-stu-id="3a62d-115">My overdue cases</span></span>
- <span data-ttu-id="3a62d-116">Sager, der er tildelt mig via arbejdsgangen</span><span class="sxs-lookup"><span data-stu-id="3a62d-116">Cases assigned to me through workflow</span></span>

<span data-ttu-id="3a62d-117">Sammen med disse nye visninger i sager er DMF-enheden **Sagsoplysninger** også tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="3a62d-117">Along with these new views into cases, the **Case detail** DMF entity is also available.</span></span>

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a><span data-ttu-id="3a62d-118">Aktivér Relationsdefinitioner i det globale adressekartotek (414762)</span><span class="sxs-lookup"><span data-stu-id="3a62d-118">Enable Relationship definitions in global address bBook (414762)</span></span>

<span data-ttu-id="3a62d-119">Relationer er nu aktiveret i det globale adressekartotek.</span><span class="sxs-lookup"><span data-stu-id="3a62d-119">Relationships are now enabled in the global address book.</span></span> <span data-ttu-id="3a62d-120">Før denne uges udgivelse viste faktafeltet **Relationer** alle systemdefinerede relationer.</span><span class="sxs-lookup"><span data-stu-id="3a62d-120">Prior to this week's release, the **Relationship** fact box displayed any system-defined relationships.</span></span> <span data-ttu-id="3a62d-121">Nu kan du definere disse relationer på siden med det globale adressekartotek.</span><span class="sxs-lookup"><span data-stu-id="3a62d-121">Now you can define those relationships within the global address book page.</span></span>

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a><span data-ttu-id="3a62d-122">En stilling kan fjernes, når der findes aktive kompensationsposter for stillingen (414568)</span><span class="sxs-lookup"><span data-stu-id="3a62d-122">A position can be removed when active compensation records exist for the position (414568)</span></span>

<span data-ttu-id="3a62d-123">Med denne ændring vises en advarsel, når du forsøger at slette en stilling, og en arbejder har en aktiv kompensationspost for samme stilling.</span><span class="sxs-lookup"><span data-stu-id="3a62d-123">With this change, a warning appears when you attempt to delete a position and a worker has an active compensation record for that same position.</span></span> <span data-ttu-id="3a62d-124">Når det sker, skal du opdatere medarbejderens faste løn-post, før stillingen fjernes.</span><span class="sxs-lookup"><span data-stu-id="3a62d-124">When this happens, you must update the employee fixed compensation record before removing the position.</span></span>

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a><span data-ttu-id="3a62d-125">Arbejdsprocessen for gennemgang af ydeevne tilføjer indimellem godkendelser fra personer, der ikke er en del af processen (414171)</span><span class="sxs-lookup"><span data-stu-id="3a62d-125">Performance review workflow occasionally adds sign-offs from people who are not part of the process (414171)</span></span>

<span data-ttu-id="3a62d-126">Denne ændring retter et problem, hvor yderligere godkendelsesdeltagere føjes til gennemsynet af ydeevnen.</span><span class="sxs-lookup"><span data-stu-id="3a62d-126">This change corrects an issue where additional sign-off participants are added to the performance review.</span></span>

## <a name="worker-position-assignment-not-created-in-common-data-service-when-selected-on-the-new-worker-dialog-413479"></a><span data-ttu-id="3a62d-127">Tildelingen af arbejderstilling, der ikke er oprettet i Common Data Service, da den blev valgt i dialogboksen Ny arbejder (413479)</span><span class="sxs-lookup"><span data-stu-id="3a62d-127">Worker position assignment not created in Common Data Service when selected on the New Worker dialog (413479)</span></span>

<span data-ttu-id="3a62d-128">Denne ændring retter en fejl, når du ansætter en ny arbejder og tildeler den nye ansættelse til en stilling via dialogboksen **Ny medarbejder**.</span><span class="sxs-lookup"><span data-stu-id="3a62d-128">This change corrects an issue when hiring a new worker and assigning the new hire to a position through the **New worker** dialog.</span></span> <span data-ttu-id="3a62d-129">Nu afspejles stillingstildelingen i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3a62d-129">Now the position assignment is reflected in Common Data Service.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="3a62d-130">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="3a62d-130">Coming soon</span></span>

### <a name="updated-common-data-service-solution"></a><span data-ttu-id="3a62d-131">Opdateret Common Data Service-løsning</span><span class="sxs-lookup"><span data-stu-id="3a62d-131">Updated Common Data Service solution</span></span>

<span data-ttu-id="3a62d-132">Der vil snart være en ny Common Data Service-løsning med følgende ændringer:</span><span class="sxs-lookup"><span data-stu-id="3a62d-132">A new Common Data Service solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="3a62d-133">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="3a62d-133">Description</span></span> | <span data-ttu-id="3a62d-134">Forskydning</span><span class="sxs-lookup"><span data-stu-id="3a62d-134">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="3a62d-135">Ændringer i objektet **Job/Stilling**</span><span class="sxs-lookup"><span data-stu-id="3a62d-135">**Job/Position** entity changes</span></span> | <span data-ttu-id="3a62d-136">**Kompensationsområde** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="3a62d-136">**Compensation region** added</span></span></br><span data-ttu-id="3a62d-137">**Økonomiske dimensioner** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="3a62d-137">**Financial dimensions** added</span></span> |
| <span data-ttu-id="3a62d-138">Ændringer i objektet **Arbejder**</span><span class="sxs-lookup"><span data-stu-id="3a62d-138">**Worker** entity changes</span></span> | <span data-ttu-id="3a62d-139">**Navnerækkefølge** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="3a62d-139">**Name sequence** added</span></span></br><span data-ttu-id="3a62d-140">**Arbejder hjemmefra** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="3a62d-140">**Works from home** added</span></span></br><span data-ttu-id="3a62d-141">**Sprog** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="3a62d-141">**Language** added</span></span></br><span data-ttu-id="3a62d-142">**Anciennitetsdato** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="3a62d-142">**Seniority date** added</span></span></br><span data-ttu-id="3a62d-143">**Jubilæumsdato** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="3a62d-143">**Anniversary date** added</span></span></br><span data-ttu-id="3a62d-144">**Oprindelig ansættelsesdato** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="3a62d-144">**Original hire date** added</span></span> |
| <span data-ttu-id="3a62d-145">Ændringer af objektet **Ansættelse**</span><span class="sxs-lookup"><span data-stu-id="3a62d-145">**Employment** entity changes</span></span> | <span data-ttu-id="3a62d-146">**Økonomiske dimensioner** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="3a62d-146">**Financial dimensions** added</span></span></br><span data-ttu-id="3a62d-147">**Årsag til fratrædelse** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="3a62d-147">**Termination reason** added</span></span></br><span data-ttu-id="3a62d-148">**Fratrædelsesdato** er omdøbt fra **Overførselsdato**</span><span class="sxs-lookup"><span data-stu-id="3a62d-148">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="3a62d-149">**Datoer for prøvetid** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="3a62d-149">**Probation date** added</span></span> |
| <span data-ttu-id="3a62d-150">Ændringer i objektet **Arbejders adresse**</span><span class="sxs-lookup"><span data-stu-id="3a62d-150">**Worker address** entity changes</span></span> | <span data-ttu-id="3a62d-151">**Gadenavn** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="3a62d-151">**Street address** added</span></span></br><span data-ttu-id="3a62d-152">**Adresselinje 1**, **Adresselinje 2** og **Adresselinje 3** er markeret til udfasning</span><span class="sxs-lookup"><span data-stu-id="3a62d-152">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="3a62d-153">Nye konfigurationsobjekter til variabel kompensation</span><span class="sxs-lookup"><span data-stu-id="3a62d-153">New variable compensation setup entities</span></span> | <span data-ttu-id="3a62d-154">**Type af variabel kompensationsplan**</span><span class="sxs-lookup"><span data-stu-id="3a62d-154">**Compensation variable plan type**</span></span></br><span data-ttu-id="3a62d-155">**Kompensation - variabel struktur**</span><span class="sxs-lookup"><span data-stu-id="3a62d-155">**Compensation variable plan**</span></span></br><span data-ttu-id="3a62d-156">**Fordelingsregler**</span><span class="sxs-lookup"><span data-stu-id="3a62d-156">**Vesting rules**</span></span></br><span data-ttu-id="3a62d-157">**Niveau i variabel kompensationsplan**</span><span class="sxs-lookup"><span data-stu-id="3a62d-157">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="3a62d-158">Nyt objekt **Arbejderkalender for ansættelse**</span><span class="sxs-lookup"><span data-stu-id="3a62d-158">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="3a62d-159">**Arbejdskalenderobjekt** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="3a62d-159">**Work calendar entity** added</span></span> |
| <span data-ttu-id="3a62d-160">Nyt objekt **Lønoplysninger for stillinger**</span><span class="sxs-lookup"><span data-stu-id="3a62d-160">New **Payroll position detail** entity</span></span> | <span data-ttu-id="3a62d-161">**Lønoplysninger for stillinger** er tilføjet</span><span class="sxs-lookup"><span data-stu-id="3a62d-161">**Payroll position detail** added</span></span> |
| <span data-ttu-id="3a62d-162">Nyt objekt **Titel**</span><span class="sxs-lookup"><span data-stu-id="3a62d-162">New **Title** entity</span></span> | <span data-ttu-id="3a62d-163">**Titel** er tilføjet.</span><span class="sxs-lookup"><span data-stu-id="3a62d-163">**Title** added.</span></span> <span data-ttu-id="3a62d-164">Den nye enhed **Titel** vil blive medtaget i synkroniseringsprocessen mellem Human Resources og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3a62d-164">The new **Title** entity will be included in the sync process between Human Resources and Common Data Service.</span></span> <span data-ttu-id="3a62d-165">Der henvises ikke til den først i enhederne **Stilling** eller **Job**.</span><span class="sxs-lookup"><span data-stu-id="3a62d-165">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

<span data-ttu-id="3a62d-166">I løbet af de næste par uger vil disse enhedsændringer være tilgængelige i alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="3a62d-166">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="3a62d-167">Sådan installeres den nyeste Common Data Service-løsning til HR manuelt:</span><span class="sxs-lookup"><span data-stu-id="3a62d-167">To manually install the latest Common Data Service solution for Human Resources:</span></span>

1.  <span data-ttu-id="3a62d-168">Gå til [Power Platform Administration](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="3a62d-168">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="3a62d-169">Vælg **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="3a62d-169">Select **Environments**.</span></span>

3.  <span data-ttu-id="3a62d-170">Find det miljø, du vil opgradere.</span><span class="sxs-lookup"><span data-stu-id="3a62d-170">Find the environment you want to upgrade.</span></span> <span data-ttu-id="3a62d-171">Det skal svare til **Miljønavn** i sektionen **Common Data Service-oplysninger** i formularen **Om** i HR.</span><span class="sxs-lookup"><span data-stu-id="3a62d-171">This should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="3a62d-172">Vælg miljøet for at få vist miljødetaljerne.</span><span class="sxs-lookup"><span data-stu-id="3a62d-172">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="3a62d-173">Vælg **Administrer løsninger** på handlingslinjen i toppen.</span><span class="sxs-lookup"><span data-stu-id="3a62d-173">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="3a62d-174">Der åbnes et nyt browservindue, hvor du kan navigere til **Dynamics 365 Administration** i konteksten af dit miljø.</span><span class="sxs-lookup"><span data-stu-id="3a62d-174">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="3a62d-175">Vælg **Dynamics 365 Human Resources Anchor** i listen **Løsning**.</span><span class="sxs-lookup"><span data-stu-id="3a62d-175">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="3a62d-176">Vælg **Opgrader** for at anvende den seneste løsning.</span><span class="sxs-lookup"><span data-stu-id="3a62d-176">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="in-preview"></a><span data-ttu-id="3a62d-177">Som eksempel</span><span class="sxs-lookup"><span data-stu-id="3a62d-177">In preview</span></span>

<span data-ttu-id="3a62d-178">Følgende prøvefunktioner blev tilgængelige d. 3. februar 2020:</span><span class="sxs-lookup"><span data-stu-id="3a62d-178">The following preview features became available on February 3, 2020:</span></span>

- <span data-ttu-id="3a62d-179">**Visningsfunktioner for orlov og fravær** - Du kan finde flere oplysninger under [Visningsfunktioner for orlov og fravær](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span><span class="sxs-lookup"><span data-stu-id="3a62d-179">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="3a62d-180">**Prøveversionsfunktion: Administration af frynsegoder** – Der er flere oplysninger, herunder kendte problemer, under [Oversigt over Administration af frynsegoder](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3a62d-180">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>
