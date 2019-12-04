---
title: Opret en ansættelsesprocesskabelon i Attract
description: Dette emne indeholder oplysninger om, hvordan du opretter en ansættelsesprocesskabelon i Attract.
author: andreabichsel
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: 82046d43cf7366b760c140bdb8b017337b4f41da
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832552"
---
# <a name="create-a-hiring-process-template-in-attract"></a><span data-ttu-id="4992a-103">Opret en ansættelsesprocesskabelon i Attract</span><span class="sxs-lookup"><span data-stu-id="4992a-103">Create a hiring process template in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4992a-104">En *ansættelsesprocesskabelon* indeholder alle de aktiviteter, der skal medtages som en del af ansættelsesprocessen for et job.</span><span class="sxs-lookup"><span data-stu-id="4992a-104">A *hiring process template* contains all the activities that should be included as part of the hiring process for a job.</span></span> <span data-ttu-id="4992a-105">I dette emne beskrives elementerne i en processkabelon i Microsoft Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="4992a-105">This topic describes the elements of a process template in Microsoft Dynamics 365 Talent: Attract.</span></span> <span data-ttu-id="4992a-106">Det beskrives også, hvordan du opretter en skabelon.</span><span class="sxs-lookup"><span data-stu-id="4992a-106">It also explains how to create a template.</span></span>

> [!NOTE]
> <span data-ttu-id="4992a-107">Skabelonoprettelse er en del af tilføjelsesprogrammet til omfattende ansættelser i Attract.</span><span class="sxs-lookup"><span data-stu-id="4992a-107">Template creation is part of the Comprehensive Hiring Add-on for Attract.</span></span>

## <a name="template-management"></a><span data-ttu-id="4992a-108">Skabelonstyring</span><span class="sxs-lookup"><span data-stu-id="4992a-108">Template management</span></span>

<span data-ttu-id="4992a-109">Organisationer kan bestemme, om teammedlemmer eller kun administratorer kan oprette processkabeloner i Attract.</span><span class="sxs-lookup"><span data-stu-id="4992a-109">Organizations can decide whether team members or only admins can create process templates in Attract.</span></span> <span data-ttu-id="4992a-110">Du kan konfigurere skabelonstyring ved at gå til **Administration** \> **Skabelonstyring**.</span><span class="sxs-lookup"><span data-stu-id="4992a-110">To configure template management, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="4992a-111">Hvis teammedlemmer opretter deres egne skabeloner, skal du aktivere skabelonstyring.</span><span class="sxs-lookup"><span data-stu-id="4992a-111">To let team members create their own templates, turn on template management.</span></span> <span data-ttu-id="4992a-112">Hvis du ikke aktiverer skabelonstyring, kan kun administratorer oprette skabeloner.</span><span class="sxs-lookup"><span data-stu-id="4992a-112">If you don't turn on template management, only admins can create templates.</span></span>

## <a name="default-template"></a><span data-ttu-id="4992a-113">Standardskabelon</span><span class="sxs-lookup"><span data-stu-id="4992a-113">Default template</span></span>

<span data-ttu-id="4992a-114">Kun administratorer kan indstille standardskabelonen.</span><span class="sxs-lookup"><span data-stu-id="4992a-114">Only admins can set the default template.</span></span> <span data-ttu-id="4992a-115">Standardskabelonen bruges, hvis der ikke er markeret en skabelon, når der oprettes et job.</span><span class="sxs-lookup"><span data-stu-id="4992a-115">The default template is used if a template isn't selected when a job is created.</span></span> <span data-ttu-id="4992a-116">Du kan indstille standardskabelonen ved at gå til **Administration** \> **Skabelonstyring**.</span><span class="sxs-lookup"><span data-stu-id="4992a-116">To set the default template, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="4992a-117">På kortet for den skabelon, der skal være standardskabelon, skal du vælge ellipseknappen (**...**) og derefter vælge **Angiv som standard**.</span><span class="sxs-lookup"><span data-stu-id="4992a-117">On the card for the template that should be the default template, select the ellipsis button (**...**), and then select **Set as default**.</span></span>

## <a name="create-a-process-template"></a><span data-ttu-id="4992a-118">Oprette en processkabelon</span><span class="sxs-lookup"><span data-stu-id="4992a-118">Create a process template</span></span>

<span data-ttu-id="4992a-119">Administratorer, rekrutteringsmedarbejdere og ansættelsesansvarlige kan oprette processkabelon.</span><span class="sxs-lookup"><span data-stu-id="4992a-119">Admins, recruiters, and hiring managers can create process templates.</span></span> <span data-ttu-id="4992a-120">En processkabelon består af *stadier* og *aktiviteter*.</span><span class="sxs-lookup"><span data-stu-id="4992a-120">A process template consists of *stages* and *activities*.</span></span> <span data-ttu-id="4992a-121">Stadier grupperer en eller flere aktiviteter sammen.</span><span class="sxs-lookup"><span data-stu-id="4992a-121">Stages group together one or more activities.</span></span> <span data-ttu-id="4992a-122">Hver processkabelon har som standard jobkandidat-, ansøgnings- og tilbudsaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="4992a-122">By default, every process template has Prospect, Application, and Offer activities.</span></span> <span data-ttu-id="4992a-123">De stadier, der indeholder disse aktiviteter kan omdøbes.</span><span class="sxs-lookup"><span data-stu-id="4992a-123">The stages that contain these activities can be renamed.</span></span> <span data-ttu-id="4992a-124">Du kan tilføje flere stadier ved at vælge **+ Nyt stadie**.</span><span class="sxs-lookup"><span data-stu-id="4992a-124">You can add more stages by selecting **+ New Stage**.</span></span> <span data-ttu-id="4992a-125">Du kan føje aktiviteter til et stadie ved enten at trække dem til det relevante stadie eller ved at dobbeltklikke på dem på aktivitetslisten.</span><span class="sxs-lookup"><span data-stu-id="4992a-125">You can add activities to a stage either by dragging them to the appropriate stage or by double-clicking them in the activity list.</span></span>

> [!NOTE]
> <span data-ttu-id="4992a-126">Stadienavne er synlige for kandidater på siden **Ansøgningsstatus**.</span><span class="sxs-lookup"><span data-stu-id="4992a-126">Stage names are visible to candidates on the **Application status** page.</span></span> <span data-ttu-id="4992a-127">Du bør overveje dette, når du vælger navne til stadier.</span><span class="sxs-lookup"><span data-stu-id="4992a-127">You should consider this fact when you choose names for stages.</span></span>

<span data-ttu-id="4992a-128">Du kan få mere at vide om aktiviteter i [Aktiviteter i ansættelsesprocesser](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="4992a-128">To learn more about activities, see [Activities in hiring processes](./activities-attract.md).</span></span>

<span data-ttu-id="4992a-129">Følg disse trin for at oprette en ansættelsesprocesskabelon.</span><span class="sxs-lookup"><span data-stu-id="4992a-129">Follow these steps to create a hiring process template.</span></span>

1. <span data-ttu-id="4992a-130">Gå til **Skabeloner**.</span><span class="sxs-lookup"><span data-stu-id="4992a-130">Go to **Templates**.</span></span>
2. <span data-ttu-id="4992a-131">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="4992a-131">Select **New**.</span></span>
3. <span data-ttu-id="4992a-132">I feltet **Skabelonnavn** skal du angive et navn til skabelonen og derefter vælge **Opret**.</span><span class="sxs-lookup"><span data-stu-id="4992a-132">In the **Template name** field, enter a name for the template, and then select **Create**.</span></span>
4. <span data-ttu-id="4992a-133">På listen **Vælg godkendelsesprocessen** skal du vælge **Standard** for at kræve godkendelse af et job.</span><span class="sxs-lookup"><span data-stu-id="4992a-133">In the **Choose the approval process** list, select **Default** to require approval for a job.</span></span>
5. <span data-ttu-id="4992a-134">Vælg at aktivere eller deaktivere jobkandidater.</span><span class="sxs-lookup"><span data-stu-id="4992a-134">Select to enable or disable prospects.</span></span>
6. <span data-ttu-id="4992a-135">Valgfrit: Tilføj eller fjern stadier.</span><span class="sxs-lookup"><span data-stu-id="4992a-135">Optional: Add or remove stages.</span></span>

    - <span data-ttu-id="4992a-136">For at tilføje et stadie skal du vælge **+ Nyt stadie**.</span><span class="sxs-lookup"><span data-stu-id="4992a-136">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="4992a-137">Hvis du vil fjerne et stadie, skal du placere markøren over stadiet og derefter vælge den papirkurvsknap, der vises.</span><span class="sxs-lookup"><span data-stu-id="4992a-137">To remove a stage, hover the pointer over the stage, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="4992a-138">Stadierne Jobkandidat, Ansøgning og Tilbud kan ikke fjernes, men de kan omdøbes.</span><span class="sxs-lookup"><span data-stu-id="4992a-138">Prospect, Application, and Offer stages can't be removed, but they can be renamed.</span></span>

7. <span data-ttu-id="4992a-139">Valgfrit: Tilføj eller fjern aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="4992a-139">Optional: Add or remove activities.</span></span>

    - <span data-ttu-id="4992a-140">Hvis du vil tilføje en aktivitet, skal du trække den fra listen til højre til det relevante stadie.</span><span class="sxs-lookup"><span data-stu-id="4992a-140">To add an activity, drag it from the activity list on the right to the appropriate stage.</span></span> <span data-ttu-id="4992a-141">Du kan også dobbeltklikke på aktiviteten og derefter vælge det stadie, den skal føjes til.</span><span class="sxs-lookup"><span data-stu-id="4992a-141">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="4992a-142">Hvis du vil fjerne en aktivitet, skal du udvide den og derefter vælge papirkurvsknappen i overskriften til aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="4992a-142">To remove an activity, expand it, and then select the trash can button on the activity header.</span></span>

8. <span data-ttu-id="4992a-143">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="4992a-143">Select **Save**.</span></span>
