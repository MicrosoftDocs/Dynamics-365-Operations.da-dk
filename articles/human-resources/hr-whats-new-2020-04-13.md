---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (13. april 2020)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 13. april 2020.
author: andreabichsel
manager: tfehr
ms.date: 04/13/2020
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
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3afc112f8a30bb187fbe37c9062afe7943e986ec
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127891"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a><span data-ttu-id="8e04a-103">Nyheder eller ændringer i Dynamics 365 Human Resources (13. april 2020)</span><span class="sxs-lookup"><span data-stu-id="8e04a-103">What's new or changed in Dynamics 365 Human Resources (April 13, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8e04a-104">I denne artikel beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8e04a-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="8e04a-105">Ændringerne gælder for build nummer 8.1.3136.</span><span class="sxs-lookup"><span data-stu-id="8e04a-105">Changes apply to build number 8.1.3136.</span></span> <span data-ttu-id="8e04a-106">Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.</span><span class="sxs-lookup"><span data-stu-id="8e04a-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="8e04a-107">Ny udgivelsestakt for produktionsudgivelser</span><span class="sxs-lookup"><span data-stu-id="8e04a-107">New production release cadence</span></span>

<span data-ttu-id="8e04a-108">Med denne uges udgivelse skifter udgivelsestakten for Human Resources fra en ugentlig opdatering til en opdatering hver anden uge.</span><span class="sxs-lookup"><span data-stu-id="8e04a-108">With this week's release, the release cadence for Human Resources shifts from a weekly update to a biweekly update.</span></span> <span data-ttu-id="8e04a-109">Hvis du vil sikre en justering med sikker implementeringspraksis og vedligeholde høje standarder for stabilitet og pålidelighed i tjenesten, vil processen med at implementere tjenesteopdateringer til alle områder nu være en fase på to uger.</span><span class="sxs-lookup"><span data-stu-id="8e04a-109">To ensure alignment with safe deployment practices, and maintain high standards of stability and reliability in the service, the process of deploying service updates to all regions is now a two-week rollout.</span></span> <span data-ttu-id="8e04a-110">Yderligere test og skærme er på plads for at sikre en vellykket implementering på hvert trin i processen.</span><span class="sxs-lookup"><span data-stu-id="8e04a-110">Additional testing and monitors are in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="8e04a-111">Du kan få flere oplysninger om frigivelsestakt i [Opdateringsproces](hr-admin-setup-update-process.md).</span><span class="sxs-lookup"><span data-stu-id="8e04a-111">For more information on the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a><span data-ttu-id="8e04a-112">Feltet Afrundingspræcision kan ikke redigeres, når der er angivet en Afrundingstype (435616)</span><span class="sxs-lookup"><span data-stu-id="8e04a-112">Rounding precision field isn't editable after specifying a Rounding type (435616)</span></span>

<span data-ttu-id="8e04a-113">Med denne ændring er feltet **Afrundingspræcision** tilgængeligt, når du har opdateret feltet **Afrundingstype**.</span><span class="sxs-lookup"><span data-stu-id="8e04a-113">With this change, the **Rounding precision** field is now available after you update the **Rounding type** field.</span></span>

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a><span data-ttu-id="8e04a-114">Kan ikke redigere orlovstilmeldingens slutdatoen, når orlovsplanen ikke har periodiseringsperioder (413628)</span><span class="sxs-lookup"><span data-stu-id="8e04a-114">Can't edit leave enrollment end date when the leave plan doesn't have accrual periods (413628)</span></span>

<span data-ttu-id="8e04a-115">Du kan nu redigere orlovstilmeldings slutdatoen, uden at fejlen "Udgangspunktet for feltet periodisering af felter skal udfyldes" vises.</span><span class="sxs-lookup"><span data-stu-id="8e04a-115">You can now edit the enrollment end date without getting the error "Field Accrual date basis must be filled in."</span></span>

## <a name="employment-entity-doesnt-sync-to-dataverse-430834"></a><span data-ttu-id="8e04a-116">Ansættelsesenhed synkroniseres ikke med Dataverse (430834)</span><span class="sxs-lookup"><span data-stu-id="8e04a-116">Employment entity doesn't sync to Dataverse (430834)</span></span>

<span data-ttu-id="8e04a-117">Denne ændring retter et problem, hvor ansættelsesdataene ikke blev synkroniseret til Dataverse, efter at der er tilføjet økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="8e04a-117">This change corrects an issue where the employment data wasn't syncing to Dataverse after adding financial dimensions.</span></span> 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a><span data-ttu-id="8e04a-118">Fjern multiovervågning for enheden Arbejdskalenderens tidsinterval (431775)</span><span class="sxs-lookup"><span data-stu-id="8e04a-118">Remove multi-parenting for Work Calendar Time Interval entity (431775)</span></span>

<span data-ttu-id="8e04a-119">Denne ændring fjerner multiovervågning for enheden **Arbejdskalenderens tidsinterval**.</span><span class="sxs-lookup"><span data-stu-id="8e04a-119">This change removes multi-parenting for the **Work Calendar Time Interval** entity.</span></span>

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a><span data-ttu-id="8e04a-120">Filteret med CAST-funktionen fungerer ikke på OData-kaldets enhed Arbejdertildeling til stilling (431699)</span><span class="sxs-lookup"><span data-stu-id="8e04a-120">Filter with CAST function doesn't work on OData call Position Worker Assignment entity (431699)</span></span>

<span data-ttu-id="8e04a-121">Denne opdatering indeholder en ændring, der giver mulighed for at filtrere med CAST-funktionen i OData for enheden **Arbejdertildeling til stilling** .</span><span class="sxs-lookup"><span data-stu-id="8e04a-121">This update includes a change to allow  filter with CAST function within OData for the **Position Worker Assignment** entity.</span></span>

## <a name="in-preview"></a><span data-ttu-id="8e04a-122">Som prøveversion</span><span class="sxs-lookup"><span data-stu-id="8e04a-122">In Preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="8e04a-123">Forlad suspension</span><span class="sxs-lookup"><span data-stu-id="8e04a-123">Leave suspension</span></span>

<span data-ttu-id="8e04a-124">Du kan afbryde orlov og fravær i Human Resources for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="8e04a-124">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="8e04a-125">Når du suspendere orlov, stoppes orloven for de valgte orlovstyper.</span><span class="sxs-lookup"><span data-stu-id="8e04a-125">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="8e04a-126">Hvis suspensionen finder sted, når en periodisering er blevet behandlet, opretter suspensionen en forholdsmæssig justering til medarbejderens orlov.</span><span class="sxs-lookup"><span data-stu-id="8e04a-126">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="8e04a-127">Du kan finde flere oplysninger i [Suspender orlov](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="8e04a-127">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="8e04a-128">Overføre regler</span><span class="sxs-lookup"><span data-stu-id="8e04a-128">Carry forward rules</span></span>

<span data-ttu-id="8e04a-129">Du kan angive en orlovstype for overførselssaldi, hvor gennemførte reguleringer overføres.</span><span class="sxs-lookup"><span data-stu-id="8e04a-129">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="8e04a-130">Hvis en medarbejder f.eks. overfører 10 dage, kan du vælge en anden orlovstype for disse 10 dage.</span><span class="sxs-lookup"><span data-stu-id="8e04a-130">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="8e04a-131">Du kan finde flere oplysninger i [Konfigurere orlovs- og fraværstyper](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="8e04a-131">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="8e04a-132">Kendte problemer</span><span class="sxs-lookup"><span data-stu-id="8e04a-132">Known issues</span></span>

## <a name="employment-details-entity"></a><span data-ttu-id="8e04a-133">Enhed med ansættelsesdetaljer</span><span class="sxs-lookup"><span data-stu-id="8e04a-133">Employment Details entity</span></span>

<span data-ttu-id="8e04a-134">Enheden **Ansættelsesdetaljer** er blevet opdateret med følgende felter:</span><span class="sxs-lookup"><span data-stu-id="8e04a-134">The **Employment Detail** entity has been updated with the following fields:</span></span>

- <span data-ttu-id="8e04a-135">**Betalingsfrekvens**</span><span class="sxs-lookup"><span data-stu-id="8e04a-135">**PayFrequency**</span></span>
- <span data-ttu-id="8e04a-136">**Ansættelseskategori-id**</span><span class="sxs-lookup"><span data-stu-id="8e04a-136">**Employment Category ID**</span></span>
- <span data-ttu-id="8e04a-137">**Medarbejdertype**</span><span class="sxs-lookup"><span data-stu-id="8e04a-137">**Employment Type**</span></span>
- <span data-ttu-id="8e04a-138">**Ansættelsestype-id**</span><span class="sxs-lookup"><span data-stu-id="8e04a-138">**EmploymentType ID**</span></span>
- <span data-ttu-id="8e04a-139">**Status for frynsegodeansættelse**</span><span class="sxs-lookup"><span data-stu-id="8e04a-139">**Benefit Employment Status**</span></span>

<span data-ttu-id="8e04a-140">Opsætningsdataene for disse felter afhænger af, at administration af frynsegoder er aktiveret i arbejdsområdet **Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="8e04a-140">The setup data for these fields rely on benefits management being enabled in the **Feature management** workspace.</span></span> <span data-ttu-id="8e04a-141">Du må ikke udfylde eller opdatere disse felter i enheden **Ansættelsesoplysninger**, da det vil resultere i fejl under importen.</span><span class="sxs-lookup"><span data-stu-id="8e04a-141">Don't populate or update these fields in the **Employment Detail** entity, because it will result in errors during import.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="8e04a-142">Prøveversionen af SharePoint fungerer ikke i visse miljøer</span><span class="sxs-lookup"><span data-stu-id="8e04a-142">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="8e04a-143">Hvis visning af dokumenter, der er gemt i SharePoint, ikke fungerer, kan du prøve følgende procedure:</span><span class="sxs-lookup"><span data-stu-id="8e04a-143">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="8e04a-144">Kontroller, at administratorbrugerkontoen har en mail tilknyttet brugerposten.</span><span class="sxs-lookup"><span data-stu-id="8e04a-144">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="8e04a-145">Du kan få vist disse oplysninger på siden **Bruger**.</span><span class="sxs-lookup"><span data-stu-id="8e04a-145">You can view this information in the **User** page.</span></span> <span data-ttu-id="8e04a-146">Hvis e-mail ikke er konfigureret, skal du tilføje e-mailadressen og udbyderen med OData Excel-tilføjelsesprogrammet.</span><span class="sxs-lookup"><span data-stu-id="8e04a-146">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="8e04a-147">E-mailadressen findes som standard ikke i Excel-designet.</span><span class="sxs-lookup"><span data-stu-id="8e04a-147">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="8e04a-148">Du skal redigere Excel-designet, tilføje alle felter, anvende og opdatere.</span><span class="sxs-lookup"><span data-stu-id="8e04a-148">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="8e04a-149">Når du har fuldført disse trin, kan du opdatere administratorkontoen.</span><span class="sxs-lookup"><span data-stu-id="8e04a-149">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="8e04a-150">Når administratorkontoen har en tilknyttet mailkonto, skal du logge på Human Resources med administrator-legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="8e04a-150">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="8e04a-151">Åbn en vedhæftet fil i SharePoint for at starte dokumentvisningen.</span><span class="sxs-lookup"><span data-stu-id="8e04a-151">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="8e04a-152">Log på med en anden brugerkonto, der har adgang til vedhæftede filer, og kontroller, at eksempelvisningen fungerer som forventet.</span><span class="sxs-lookup"><span data-stu-id="8e04a-152">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e04a-153">Se også</span><span class="sxs-lookup"><span data-stu-id="8e04a-153">See also</span></span>

[<span data-ttu-id="8e04a-154">Nyheder eller ændringer i Human Resources</span><span class="sxs-lookup"><span data-stu-id="8e04a-154">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="8e04a-155">Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2</span><span class="sxs-lookup"><span data-stu-id="8e04a-155">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="8e04a-156">Opdater proces</span><span class="sxs-lookup"><span data-stu-id="8e04a-156">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="8e04a-157">Administrere funktioner</span><span class="sxs-lookup"><span data-stu-id="8e04a-157">Manage features</span></span>](hr-admin-manage-features.md)