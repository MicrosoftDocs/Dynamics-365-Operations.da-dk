---
title: Nyheder eller ændringer i Dynamics 365 for Talent Core HR (august 2018)
description: Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 08/27/2018
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
ms.search.validFrom: 2018-08-27
ms.dyn365.ops.version: Talent August 2018 update
ms.openlocfilehash: 3327939137486038b9002029c7c9e8d65dfa2f64
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742603"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-august-2018"></a><span data-ttu-id="2fd07-103">Nyheder eller ændringer i Dynamics 365 for Talent Core HR (august 2018)</span><span class="sxs-lookup"><span data-stu-id="2fd07-103">What's new or changed in Dynamics 365 for Talent Core HR (August 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2fd07-104">**Build 8.1.104**</span><span class="sxs-lookup"><span data-stu-id="2fd07-104">**Build 8.1.104**</span></span>

<span data-ttu-id="2fd07-105">Dette emne beskriver funktioner, der enten er nye eller ændrede i Dynamics 365 for Talent Core HR.</span><span class="sxs-lookup"><span data-stu-id="2fd07-105">This topic describes features that are either new or changed in Dynamics 365 for Talent Core HR.</span></span>

## <a name="view-expiring-records-in-manager-self-service"></a><span data-ttu-id="2fd07-106">Se udløbende poster i Selvbetjening for leder</span><span class="sxs-lookup"><span data-stu-id="2fd07-106">View expiring records in Manager self service</span></span>

<span data-ttu-id="2fd07-107">Du kan du se udløbende poster i Selvbetjening for leder.</span><span class="sxs-lookup"><span data-stu-id="2fd07-107">You can now view expiring records in Manager self-service.</span></span> <span data-ttu-id="2fd07-108">Med nye indstillinger er det muligt at konfigurere, hvilke oplysninger ledere kan få vist.</span><span class="sxs-lookup"><span data-stu-id="2fd07-108">New options are allow you to configure what information will be available for managers to view.</span></span> <span data-ttu-id="2fd07-109">Disse omfatter:</span><span class="sxs-lookup"><span data-stu-id="2fd07-109">These include:</span></span>

-   <span data-ttu-id="2fd07-110">Certifikater</span><span class="sxs-lookup"><span data-stu-id="2fd07-110">Certificates</span></span>

-   <span data-ttu-id="2fd07-111">Identifikationsnumre</span><span class="sxs-lookup"><span data-stu-id="2fd07-111">Identification numbers</span></span>

-   <span data-ttu-id="2fd07-112">Prøvetid</span><span class="sxs-lookup"><span data-stu-id="2fd07-112">Probation periods</span></span>

-   <span data-ttu-id="2fd07-113">Screeninger</span><span class="sxs-lookup"><span data-stu-id="2fd07-113">Screenings</span></span>

-   <span data-ttu-id="2fd07-114">Test</span><span class="sxs-lookup"><span data-stu-id="2fd07-114">Tests</span></span>

<span data-ttu-id="2fd07-115">Denne funktion giver dig også mulighed for at angive det interval af dage, hvor du vil søge efter udløbende poster.</span><span class="sxs-lookup"><span data-stu-id="2fd07-115">This feature also gives you the ability to specify the range of days in which to look for expiring records.</span></span>

## <a name="configurable-transfer-actions"></a><span data-ttu-id="2fd07-116">Overførselshandlinger, der kan konfigureres</span><span class="sxs-lookup"><span data-stu-id="2fd07-116">Configurable transfer actions</span></span>

<span data-ttu-id="2fd07-117">Du kan konfigurere de indstillinger efter rolle, der skal være tilgængelige, under angivelsen af en anmodning om dataoverførsel.</span><span class="sxs-lookup"><span data-stu-id="2fd07-117">You can configure by role the options that will be available during the entry of a transfer request.</span></span> <span data-ttu-id="2fd07-118">Denne funktion giver ekstra fleksibilitet på tværs af rollerne i en organisation.</span><span class="sxs-lookup"><span data-stu-id="2fd07-118">This feature provides additional flexibility across the roles in an organization.</span></span>

<span data-ttu-id="2fd07-119">For eksempel har ledere, der anmoder om medarbejderoverførsler, ikke nødvendigvis adgang til at foreslå eller angive kompensationsbeløb eller vælge den opgaveliste, der skal knyttes til anmodningen om overførslen.</span><span class="sxs-lookup"><span data-stu-id="2fd07-119">For example, managers requesting employee transfers may not have access to suggest or enter compensation amounts or select the task lists that will be associated with the transfer request.</span></span> <span data-ttu-id="2fd07-120">I dette tilfælde kan ledere oprette og sende anmodninger om overførsel, men kan ikke angive kompensations- eller opgavelistetildelinger.</span><span class="sxs-lookup"><span data-stu-id="2fd07-120">In this case, managers can create and submit transfer requests but are not allowed to enter compensation or task list assignments.</span></span> <span data-ttu-id="2fd07-121">I denne samme konfiguration kan HR tildele de nye værdier for kompensation samt tilknytte eventuelle yderligere kontrollister, der skal fuldføres som følge af fuldførelsen af overførslen.</span><span class="sxs-lookup"><span data-stu-id="2fd07-121">In this same configuration, HR will be able to assign the new compensation values as well as assign any additional checklists to be completed as a result of the transfer completing.</span></span>

<span data-ttu-id="2fd07-122">De nye konfigurationsindstillinger er som standard indstillet til ikke at ændre egenskaberne før denne opdatering.</span><span class="sxs-lookup"><span data-stu-id="2fd07-122">By default, the new configuration options are set to not change the capabilities prior to this update.</span></span>

## <a name="leave-and-absence"></a><span data-ttu-id="2fd07-123">Orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="2fd07-123">Leave and absence</span></span>

<span data-ttu-id="2fd07-124">Der findes nu flere datofelter i Orlov og fravær.</span><span class="sxs-lookup"><span data-stu-id="2fd07-124">There are now additional Date fields available in Leave and Absence.</span></span>

<span data-ttu-id="2fd07-125">Med denne funktion kan du indstille grundlaget for periodiseringsperioder på planniveau til at bruge bestemte medarbejderdatoer.</span><span class="sxs-lookup"><span data-stu-id="2fd07-125">With this feature you can set the accrual period basis at the plan level to use specific employee dates.</span></span> <span data-ttu-id="2fd07-126">Dette giver mulighed for at bruge andre datoer end planstartdatoen under orlovsperiodiseringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="2fd07-126">This allows for dates other than the plan start date to be used during the leave accrual process.</span></span> <span data-ttu-id="2fd07-127">Indstillinger for bestemte datoer for medarbejdere omfatter følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="2fd07-127">Options for employee specific dates include the following values:</span></span>

-   <span data-ttu-id="2fd07-128">Brugerdefineret (tilgængelig før denne opdatering)</span><span class="sxs-lookup"><span data-stu-id="2fd07-128">Custom (available prior to this update)</span></span>

-   <span data-ttu-id="2fd07-129">Jubilæumsdato</span><span class="sxs-lookup"><span data-stu-id="2fd07-129">Anniversary date</span></span>

-   <span data-ttu-id="2fd07-130">Oprindelig ansættelsesdato</span><span class="sxs-lookup"><span data-stu-id="2fd07-130">Original hire date</span></span>

-   <span data-ttu-id="2fd07-131">Anciennitetsdato</span><span class="sxs-lookup"><span data-stu-id="2fd07-131">Seniority date</span></span>

-   <span data-ttu-id="2fd07-132">Justeret startdato for medarbejder</span><span class="sxs-lookup"><span data-stu-id="2fd07-132">Worker’s adjusted start date</span></span>

-   <span data-ttu-id="2fd07-133">Startdato for medarbejder</span><span class="sxs-lookup"><span data-stu-id="2fd07-133">Worker’s start date</span></span>

<span data-ttu-id="2fd07-134">Når indstillingen er konfigureret til at bruge en af de specifikke datoer for medarbejderen, bruge registreringsprocessen den angivne dato til at beregne periodiseringsperioder.</span><span class="sxs-lookup"><span data-stu-id="2fd07-134">When configured to use one of the employee specific dates, the enrollment process will use the specified date to calculate the accrual periods.</span></span> <span data-ttu-id="2fd07-135">Grundlaget for periodiseringsperioder vises også på medarbejderens plantilmelding og kan hjælpe dig med at forstå, hvad der bruges i forbindelse med periodiseringen.</span><span class="sxs-lookup"><span data-stu-id="2fd07-135">The accrual period basis is also displayed on the employee’s plan enrollment to help you understand what’s being used during the accrual process.</span></span>

## <a name="microsoft-word-integration"></a><span data-ttu-id="2fd07-136">Microsoft Word-integration</span><span class="sxs-lookup"><span data-stu-id="2fd07-136">Microsoft Word integration</span></span>

<span data-ttu-id="2fd07-137">I hele Core HR er dokumentskabeloner blevet aktiveret.</span><span class="sxs-lookup"><span data-stu-id="2fd07-137">Document templates have been enabled throughout Core HR.</span></span> <span data-ttu-id="2fd07-138">Med denne funktion kan du oprette breve og rapporter, der er baseret på Word-skabeloner, som du opretter.</span><span class="sxs-lookup"><span data-stu-id="2fd07-138">This feature allows you to create letters and reports based on Word templates that you create.</span></span>

<span data-ttu-id="2fd07-139">Du kan finde flere oplysninger om denne funktion i [Selvstudium til Office-integration](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json).</span><span class="sxs-lookup"><span data-stu-id="2fd07-139">Additional information about this feature is available in the [Office integration tutorial](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json).</span></span>


## <a name="other-fixes"></a><span data-ttu-id="2fd07-140">Andre rettelser</span><span class="sxs-lookup"><span data-stu-id="2fd07-140">Other fixes</span></span>

<span data-ttu-id="2fd07-141">Denne version indeholder også en række fejlrettelser, tilføjelse af nye objekter, rettelser af eksisterende objekter og ændringer af oversatte etiketter.</span><span class="sxs-lookup"><span data-stu-id="2fd07-141">This release also includes a number of bug fixes, the addition of new entities, fixes to existing entities, and localized label changes.</span></span>
