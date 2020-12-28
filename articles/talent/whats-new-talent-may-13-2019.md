---
title: Nyheder eller ændringer i Dynamics 365 Talent (13. maj 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-05-13
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 11c9f03f4b3915d81b624115a1d97a0c7bc31709
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529726"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-13-2019"></a><span data-ttu-id="693aa-103">Nyheder eller ændringer i Dynamics 365 Talent (13. maj 2019)</span><span class="sxs-lookup"><span data-stu-id="693aa-103">What's new or changed in Dynamics 365 Talent (May 13, 2019)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="693aa-104">I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="693aa-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="coming-soon-in-attract"></a><span data-ttu-id="693aa-105">Kommer snart i Attract</span><span class="sxs-lookup"><span data-stu-id="693aa-105">Coming soon in Attract</span></span>

### <a name="job-approvals-on-home-page"></a><span data-ttu-id="693aa-106">Jobgodkendelser på Startside</span><span class="sxs-lookup"><span data-stu-id="693aa-106">Job approvals on home page</span></span>

<span data-ttu-id="693aa-107">Godkendelser vises i området **Godkendelser** på dashboardet.</span><span class="sxs-lookup"><span data-stu-id="693aa-107">Approvals appear in an **Approvals** section on the dashboard.</span></span> <span data-ttu-id="693aa-108">Godkendere kan gennemse deres godkendelser under **Tildelt til dig**, som viser job-id, titel, andre godkendere og tildelingsdato.</span><span class="sxs-lookup"><span data-stu-id="693aa-108">Approvers can review their approvals under **Assigned to you**, which displays the job ID, title, other approvers, and date assigned.</span></span> <span data-ttu-id="693aa-109">Brugere, der sender et job til godkendelse, kan gennemse deres job under **Anmodet af dig**, som viser de godkendere, der stadig har brug for at godkende det sendte job.</span><span class="sxs-lookup"><span data-stu-id="693aa-109">Users who submit a job for approval can review their jobs under **Requested by you**, which displays the approvers who still need to approve the submitted job.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="693aa-110">Ændringer i Onboard</span><span class="sxs-lookup"><span data-stu-id="693aa-110">Changes in Onboard</span></span>

<span data-ttu-id="693aa-111">Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="693aa-111">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="693aa-112">Ændringer i Core HR</span><span class="sxs-lookup"><span data-stu-id="693aa-112">Changes in Core HR</span></span>

<span data-ttu-id="693aa-113">Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2297.</span><span class="sxs-lookup"><span data-stu-id="693aa-113">Changes described in this section apply to build number 8.1.2297.</span></span> <span data-ttu-id="693aa-114">Tallene i parenteser i nogle overskrifter henviser til supportnumre i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="693aa-114">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="indicate-instance-type-when-provisioning-talent"></a><span data-ttu-id="693aa-115">Angive en forekomsttype under klargøring af Talent</span><span class="sxs-lookup"><span data-stu-id="693aa-115">Indicate instance type when provisioning Talent</span></span>

<span data-ttu-id="693aa-116">Når du klargør en ny forekomst af Talent, kan du angive, om forekomsttypen er **Produktion** eller **Sandkasse**, hvilket giver mulighed for tidlig test af nye funktioner.</span><span class="sxs-lookup"><span data-stu-id="693aa-116">When provisioning a new instance of Talent, you can indicate whether the instance type is **Production** or **Sandbox**, which allows for early testing of new features.</span></span> <span data-ttu-id="693aa-117">Alle eksisterende Talent-forekomster vil blive opdateret til **Produktion**-forekomsttypen.</span><span class="sxs-lookup"><span data-stu-id="693aa-117">All existing Talent instances will be updated to the **Production** instance type.</span></span> <span data-ttu-id="693aa-118">Hvis en af de eksisterende forekomster skal opdateres til **Sandkasse**-forekomsttypen, skal du kontakte [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) for at starte ændringsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="693aa-118">If you want one of your existing instances to be updated to the **Sandbox** instance type, please contact [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) to initiate the change request.</span></span>

### <a name="common-data-service-entity-support-for-custom-fields"></a><span data-ttu-id="693aa-119">Understøttelse i Common Data Service-enheden af brugerdefinerede felter</span><span class="sxs-lookup"><span data-stu-id="693aa-119">Common Data Service entity support for custom fields</span></span>

<span data-ttu-id="693aa-120">I denne uges udgivelse understøtter følgende Common Data Service-enheder nu brugerdefinerede felter: Ansættelse, Frynsegodeberegningsfrekvens, Frynsegodeberegningssats, Arbejdskalenderferie og Identifikationstype.</span><span class="sxs-lookup"><span data-stu-id="693aa-120">In this week's release, the following Common Data Service entities now support custom fields: Employment, Benefit calc frequency, Benefit calc rate, Work calendar holiday, and Identification type.</span></span>

### <a name="common-data-service-integration-page"></a><span data-ttu-id="693aa-121">Common Data Service-integrationsside</span><span class="sxs-lookup"><span data-stu-id="693aa-121">Common Data Service integration page</span></span>

<span data-ttu-id="693aa-122">Denne version giver dig en ny indstilling i **Systemadministration > Links > Integrationer > Common Data Service > Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="693aa-122">This release provides a new option in **System Administration > Links > Integrations > Common Data Service configuration**.</span></span> <span data-ttu-id="693aa-123">Indstillingen **Common Data Service-konfiguration** giver en administrator eller dataadministratorer en vis fleksibilitet og indsigt med Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="693aa-123">The **Common Data Service configuration** option allows an administrator or data management administrator some flexibility and insights with the Common Data Service.</span></span> <span data-ttu-id="693aa-124">Med denne indstilling kan du aktivere eller deaktivere Common Data Service-integration med en Talent-forekomst og få vist synkroniseringsdetaljerne mellem Talent-forekomsten og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="693aa-124">With this option, you can enable or disable Common Data Service integration with a Talent instance and view the sync details between the Talent instance and the Common Data Service.</span></span>

### <a name="import-performance-data-with-final-employee-rating-316710"></a><span data-ttu-id="693aa-125">Importere ydelsesdata med endelig medarbejderrangering (316710)</span><span class="sxs-lookup"><span data-stu-id="693aa-125">Import performance data with final employee rating (316710)</span></span>

<span data-ttu-id="693aa-126">I denne version kan du importere historiske medarbejderrangeringsdata.</span><span class="sxs-lookup"><span data-stu-id="693aa-126">In this release, you can import historical employee rating data.</span></span> <span data-ttu-id="693aa-127">Feltet **FinalEmployeeRatingId** har nu skrivetilladelse.</span><span class="sxs-lookup"><span data-stu-id="693aa-127">The **FinalEmployeeRatingId** field now has write permission.</span></span>

### <a name="cant-create-worker-address-in-common-data-service-and-sync-it-with-talent-317555"></a><span data-ttu-id="693aa-128">Det er ikke muligt at oprette arbejderadresse i Common Data Service og synkronisere den med Talent (317555)</span><span class="sxs-lookup"><span data-stu-id="693aa-128">Can't create Worker address in Common Data Service and sync it with Talent (317555)</span></span>

<span data-ttu-id="693aa-129">Denne ændring gør det muligt at adresse data, der er oprettet i Common Data Service, til synkronisering med Talent.</span><span class="sxs-lookup"><span data-stu-id="693aa-129">This change allows address data created in Common Data Service to sync with Talent.</span></span>

## <a name="in-preview"></a><span data-ttu-id="693aa-130">Som eksempel</span><span class="sxs-lookup"><span data-stu-id="693aa-130">In preview</span></span>

### <a name="new-page-to-validate-position-hierarchy-data"></a><span data-ttu-id="693aa-131">Ny side til validering af data i stillingshierarki</span><span class="sxs-lookup"><span data-stu-id="693aa-131">New page to validate position hierarchy data</span></span>

<span data-ttu-id="693aa-132">Personale (HR) og administratorer kan validere ledelseshierarkiet for cirkulære referencer, der utilsigtet er importeret.</span><span class="sxs-lookup"><span data-stu-id="693aa-132">Human resources (HR) and administrators can validate the managerial hierarchy for any circular references that might have been inadvertently imported.</span></span> <span data-ttu-id="693aa-133">Du kan få adgang til denne nye side fra **Virksomhedsadministration > Links > Stillinger > Validering af stillingshierarki**.</span><span class="sxs-lookup"><span data-stu-id="693aa-133">You can access this new page from **Organizational administration > Links > Positions > Position hierarchy validation**.</span></span>

### <a name="specify-reason-codes-on-leave-types"></a><span data-ttu-id="693aa-134">Angiv årsagskoder for orlovstyper</span><span class="sxs-lookup"><span data-stu-id="693aa-134">Specify reason codes on leave types</span></span>

<span data-ttu-id="693aa-135">Organisationer har muligvis brug for yderligere oplysninger om fritidsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="693aa-135">Organizations might require additional information about time-off requests.</span></span> <span data-ttu-id="693aa-136">Du kan nu angive årsagskoder for orlovstyper og lade medarbejderne vælge en årsagskode på deres fritidsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="693aa-136">You can now specify reason codes for leave types and let employees select a reason code on their time-off requests.</span></span>

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a><span data-ttu-id="693aa-137">Krav om årsagskoder for bestemte orlovstyper på fritidsanmodninger</span><span class="sxs-lookup"><span data-stu-id="693aa-137">Require reason codes for specific leave types on time-off requests</span></span>

<span data-ttu-id="693aa-138">Organisationer kræver muligvis årsagskoder for specifikke orlovstyper, når medarbejderne sender anmodninger om at få fri.</span><span class="sxs-lookup"><span data-stu-id="693aa-138">Organizations might require reason codes for specific leave types when employees submit time-off requests.</span></span> <span data-ttu-id="693aa-139">Dette krav kan være en følge af firmaets politik eller lovgivningsmæssige krav.</span><span class="sxs-lookup"><span data-stu-id="693aa-139">This requirement might exist because of company policy or regulatory requirements.</span></span> <span data-ttu-id="693aa-140">Du kan angive, hvilke orlovstyper der kræver en årsagskode, og du kan kræve, at medarbejderne angiver en årsagskode på deres fritidsanmodninger for den pågældende orlovstype.</span><span class="sxs-lookup"><span data-stu-id="693aa-140">You can specify which leave types require a reason code, and you can require that employees provide a reason code for the leave type on their time-off requests.</span></span>

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a><span data-ttu-id="693aa-141">Udarbejdelse af en transaktionsliste over orlov og fravær til Personale</span><span class="sxs-lookup"><span data-stu-id="693aa-141">Provide a leave and absence transaction list for HR</span></span>

<span data-ttu-id="693aa-142">Muligheden for at spor medarbejdernes fridage og forstå, hvordan fridagene beregnes, hjælper ikke alene Personale med at besvare medarbejdernes spørgsmål, men det er også med til at sikre, at medarbejderne tildeles den korrekte mængde fridage.</span><span class="sxs-lookup"><span data-stu-id="693aa-142">The ability to track employee time off and understand how time off is calculated not only helps HR answer employee questions, but also helps ensure accurate time-off awards for employees.</span></span> <span data-ttu-id="693aa-143">Personale har nu fået et nyt indblik i transaktionerne (tilskud, periodiseringer, reguleringer og anmodninger), så Personale-medarbejderne derved kan se de bagvedliggende årsager til fritidssaldiene.</span><span class="sxs-lookup"><span data-stu-id="693aa-143">HR now has a new view into the transactions (grants, accruals, adjustments, and requests), so that HR staff can view the reasons behind time-off balances.</span></span>
