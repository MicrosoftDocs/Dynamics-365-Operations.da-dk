---
title: Nyheder eller ændringer i Dynamics 365 Talent (5. november 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
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
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6a81209c3c4a95ee51668533d40d4aecc1d58b9
ms.sourcegitcommit: a46fb06138f7f82e973dca3157d30f9b21d3a70b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/08/2019
ms.locfileid: "2778376"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a><span data-ttu-id="1f734-103">Nyheder eller ændringer i Dynamics 365 Talent (5. november 2019)</span><span class="sxs-lookup"><span data-stu-id="1f734-103">What's new or changed in Dynamics 365 Talent (November 5, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1f734-104">I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="1f734-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="1f734-105">Ændringer i Attract</span><span class="sxs-lookup"><span data-stu-id="1f734-105">Changes in Attract</span></span>

<span data-ttu-id="1f734-106">Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="1f734-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="1f734-107">Ændringer i Onboard</span><span class="sxs-lookup"><span data-stu-id="1f734-107">Changes in Onboard</span></span>

<span data-ttu-id="1f734-108">Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="1f734-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="1f734-109">Ændringer i Core HR</span><span class="sxs-lookup"><span data-stu-id="1f734-109">Changes in Core HR</span></span>

<span data-ttu-id="1f734-110">Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2598.</span><span class="sxs-lookup"><span data-stu-id="1f734-110">Changes described in this section apply to build number 8.1.2598.</span></span> <span data-ttu-id="1f734-111">Tallene i parenteser i nogle overskrifter henviser til supportnumre i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="1f734-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="copy-a-core-hr-instance"></a><span data-ttu-id="1f734-112">Kopier en Core HR-forekomst</span><span class="sxs-lookup"><span data-stu-id="1f734-112">Copy a Core HR instance</span></span>

<span data-ttu-id="1f734-113">I denne uges udgivelse kan du bruge Microsoft Dynamics Lifecycle Services (LCS) til at kopiere en Microsoft Dynamics 365 Talent: Core HR-database til et sandkasse-miljø.</span><span class="sxs-lookup"><span data-stu-id="1f734-113">In this week's release, you can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Talent: Core HR database to a sandbox environment.</span></span> <span data-ttu-id="1f734-114">Hvis du har et andet sandkasse-miljø, kan du også kopiere databasen fra det pågældende miljø til et målrettet sandkasse-miljø.</span><span class="sxs-lookup"><span data-stu-id="1f734-114">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span> <span data-ttu-id="1f734-115">Du kan finde flere oplysninger i:</span><span class="sxs-lookup"><span data-stu-id="1f734-115">For more information, see:</span></span>

- <span data-ttu-id="1f734-116">[Bredere miljøstyring](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) i Dynamics 365: 2019 Frigivelsesbølge 2-plan</span><span class="sxs-lookup"><span data-stu-id="1f734-116">[Broader environment management](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) in the Dynamics 365: 2019 release wave 2 plan</span></span>

- <span data-ttu-id="1f734-117">[Kopier en Core HR-forekomst](hr-copy-instance.md) i Talent-dokumentation</span><span class="sxs-lookup"><span data-stu-id="1f734-117">[Copy a Core HR instance](hr-copy-instance.md) in Talent documentation</span></span>

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a><span data-ttu-id="1f734-118">Common Data Service-integrationsbatchjob oprettes ikke, når Common Data Service-integration er aktiveret (388030)</span><span class="sxs-lookup"><span data-stu-id="1f734-118">Common Data Service integration batch jobs aren't created when Common Data Service integration is enabled (388030)</span></span>

<span data-ttu-id="1f734-119">Denne ændring vil oprette batchjob til Common Data Service-integration, når den er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="1f734-119">This change will create batch jobs for Common Data Service integration when it's enabled.</span></span>

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a><span data-ttu-id="1f734-120">HcmPersonImageEntity ændrer ikke størrelsen på personbilledet, når det overføres (369469)</span><span class="sxs-lookup"><span data-stu-id="1f734-120">The HcmPersonImageEntity doesn't resize the person image when uploaded (369469)</span></span>

<span data-ttu-id="1f734-121">Denne uges udgivelse ændrer, hvordan billedernes størrelse tilpasses for at opnå en bedre ydeevne, når de importeres via datastyring.</span><span class="sxs-lookup"><span data-stu-id="1f734-121">This week's release changes how images are resized for better performance when imported through data management.</span></span>

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a><span data-ttu-id="1f734-122">En stillings "Tilgængelig for tildelingsdato" kan ligge før Aktiveringsdatoen (340103)</span><span class="sxs-lookup"><span data-stu-id="1f734-122">A position's Available for assignment date can be earlier than the Activation date (340103)</span></span>

<span data-ttu-id="1f734-123">Med denne ændring vises der en advarsel, hvis du vælger en **Tilgængelig for tildelingsdato**, der ligger før stillingens **Aktiveringsdato**.</span><span class="sxs-lookup"><span data-stu-id="1f734-123">With this change, a warning will appear if you select an **Available for assignment date** that's earlier than the position's **Activation date**.</span></span>

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a><span data-ttu-id="1f734-124">Der kan ikke oprettes en ændringsanmodning om kompensation i selvbetjening for medarbejder for trinbaserede planer (376872)</span><span class="sxs-lookup"><span data-stu-id="1f734-124">Can't create a compensation change request in employee self-service for step-based plans (376872)</span></span>

<span data-ttu-id="1f734-125">Denne version retter et problem, som opstår, når der anmodes om kompensationsændringer via selvbetjningstjenesten for medarbejdere for trinbaserede planer.</span><span class="sxs-lookup"><span data-stu-id="1f734-125">This release corrects an issue when requesting compensation changes through employee self-service for step-based plans.</span></span> 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a><span data-ttu-id="1f734-126">Årsagskoden synkroniseres ikke med Common Data Service, hvis beskrivelsen er længere end 30 tegn; Core HR tillader 60 (352682)</span><span class="sxs-lookup"><span data-stu-id="1f734-126">Reason code doesn't sync to Common Data Service if the description is longer than 30 characters, Core HR allows 60 (352682)</span></span>

<span data-ttu-id="1f734-127">med denne ændring vil årsagskoder med mere end 30 tegn blive opdateret i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="1f734-127">with this change, reason codes with more than 30 characters will be updated in Common Data Service.</span></span> <span data-ttu-id="1f734-128">Ændringer, der foretages i Common Data Service, afspejles også i Talent.</span><span class="sxs-lookup"><span data-stu-id="1f734-128">Changes made in Common Data Service will also be reflected back in Talent.</span></span>

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a><span data-ttu-id="1f734-129">Adresseintegration fra Talen til Finance and Operations (351961)</span><span class="sxs-lookup"><span data-stu-id="1f734-129">Address integration from Talent to Finance and Operations (351961)</span></span>

<span data-ttu-id="1f734-130">Denne udgivelse løser et problem, hvor adresser, der opdateres i Talent, ikke blev opdateret i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1f734-130">This release fixes an issue where addresses updated in Talent weren't updating in Finance and Operations.</span></span> <span data-ttu-id="1f734-131">Ændringer i adresseblokke opdateres nu.</span><span class="sxs-lookup"><span data-stu-id="1f734-131">Changes to address blocks will now update.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="1f734-132">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="1f734-132">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="1f734-133">Udskiv performancegennemgange</span><span class="sxs-lookup"><span data-stu-id="1f734-133">Print performance reviews</span></span>

<span data-ttu-id="1f734-134">Se [Udskrive performancegennemgange](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) i Dynamics 365: 2019 frigivelsesbølge 2-plan.</span><span class="sxs-lookup"><span data-stu-id="1f734-134">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="1f734-135">Arbejdsområdet Administration af funktioner</span><span class="sxs-lookup"><span data-stu-id="1f734-135">Feature management workspace</span></span>

<span data-ttu-id="1f734-136">Funktioner tilføjes og opdateres i alle versioner.</span><span class="sxs-lookup"><span data-stu-id="1f734-136">Features are added and updated in every release.</span></span> <span data-ttu-id="1f734-137">Administrationen af funktioner indeholder et arbejdsområde, hvor du kan få vist en liste over de funktioner, der er leveret i hver version.</span><span class="sxs-lookup"><span data-stu-id="1f734-137">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="1f734-138">Nye funktioner er som standard slået fra.</span><span class="sxs-lookup"><span data-stu-id="1f734-138">By default, new features are turned off.</span></span> <span data-ttu-id="1f734-139">Du kan bruge arbejdsområdet til at aktivere dem og få vist dokumentationen til dem.</span><span class="sxs-lookup"><span data-stu-id="1f734-139">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="1f734-140">Du kan få mere at vide om de ændringer, der kommer til funktionsstyring, under [Oversigt over funktionsstyring](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="1f734-140">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
