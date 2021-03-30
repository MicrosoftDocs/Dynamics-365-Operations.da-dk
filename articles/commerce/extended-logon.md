---
title: Konfigurere udvidede logonfunktioner for MPOS og Cloud POS
description: Dette emne dækker dine muligheder for at konfigurere udvidet logon til Cloud POS og Retail Modern POS (MPOS).
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ecb6f56f26133e7c46805500914e906b74e64df8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209095"
---
# <a name="set-up-extended-logon-functionality-for-mpos-and-cloud-pos"></a><span data-ttu-id="a78df-103">Konfigurere udvidet logonfunktionalitet for MPOS og Cloud POS</span><span class="sxs-lookup"><span data-stu-id="a78df-103">Set up extended logon functionality for MPOS and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a78df-104">Dette emne dækker dine muligheder for at konfigurere udvidet logon til Cloud POS og Retail Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="a78df-104">This topic covers your options for setting up extended logon for Cloud POS and Retail Modern POS (MPOS).</span></span>

## <a name="setting-up-extended-logon"></a><span data-ttu-id="a78df-105">Konfigurere udvidet logon</span><span class="sxs-lookup"><span data-stu-id="a78df-105">Setting up extended logon</span></span>

<span data-ttu-id="a78df-106">Du kan finde opsætningen af stregkodemasker på **Retail og Commerce** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profilers** &gt; **Funktionalitetsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="a78df-106">You can find the setup for bar code masks at **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Functionality profiles**.</span></span> <span data-ttu-id="a78df-107">Oversigtspanelet **Funktioner** indeholder følgende indstillinger, der er relateret til udvidet logon.</span><span class="sxs-lookup"><span data-stu-id="a78df-107">The **Functions** FastTab includes the following options that are related to extended logon.</span></span>

### <a name="staff-bar-code-logon"></a><span data-ttu-id="a78df-108">Logon med medarbejderstregkode</span><span class="sxs-lookup"><span data-stu-id="a78df-108">Staff bar code logon</span></span>

<span data-ttu-id="a78df-109">Når indstillingen **Logon med medarbejderstregkode** er aktiveret, kan medarbejdere, der har fået tildelt udvidet logon til deres POS-legitimationsoplysninger, logge på ved hjælp af en stregkode.</span><span class="sxs-lookup"><span data-stu-id="a78df-109">When the **Staff bar code logon** option is enabled, workers who have an extended logon assigned to their point of sale (POS) credentials can log on by using a bar code.</span></span>

### <a name="staff-bar-code-logon-requires-password"></a><span data-ttu-id="a78df-110">Medarbejderlogon med stregkode kræver adgangskode</span><span class="sxs-lookup"><span data-stu-id="a78df-110">Staff bar code logon requires password</span></span>

<span data-ttu-id="a78df-111">Når indstillingen **Medarbejderlogon med stregkode kræver adgangskode** er aktiveret, vælger logon med medarbejderstregkode kun den medarbejder, der er tildelt til det udvidede logon, der vises.</span><span class="sxs-lookup"><span data-stu-id="a78df-111">When the **Staff bar code logon requires password** option is enabled, the staff bar code logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="a78df-112">Medarbejdere skal stadig angive deres adgangskode, når denne indstilling er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="a78df-112">Workers must still enter their password when this option is enabled.</span></span>

### <a name="staff-card-logon"></a><span data-ttu-id="a78df-113">Logon med medarbejderkort</span><span class="sxs-lookup"><span data-stu-id="a78df-113">Staff card logon</span></span>

<span data-ttu-id="a78df-114">Når indstillingen **Logon med medarbejderkort** er aktiveret, kan medarbejdere, der har fået tildelt udvidet logon til deres POS-legitimationsoplysninger, logge på ved hjælp af en magnetstribe.</span><span class="sxs-lookup"><span data-stu-id="a78df-114">When the **Staff card logon** option is enabled, workers who have an extended logon assigned to their POS credentials can log on by using a magnetic stripe.</span></span>

### <a name="staff-card-logon-requires-password"></a><span data-ttu-id="a78df-115">Logon med medarbejderkort kræver adgangskode</span><span class="sxs-lookup"><span data-stu-id="a78df-115">Staff card logon requires password</span></span>

<span data-ttu-id="a78df-116">Når indstillingen **Logon med medarbejderkort kræver adgangskode** er aktiveret, vælges ved logon med medarbejderkort kun den medarbejder, der er tildelt til det udvidede logon, der vises.</span><span class="sxs-lookup"><span data-stu-id="a78df-116">When the **Staff card logon requires password** option is enabled, the staff card logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="a78df-117">Medarbejdere skal stadig angive deres adgangskode, når denne indstilling er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="a78df-117">Workers must still enter their password when this option is enabled.</span></span>

## <a name="assigning-an-extended-logon"></a><span data-ttu-id="a78df-118">Tildele et udvidet logon</span><span class="sxs-lookup"><span data-stu-id="a78df-118">Assigning an extended logon</span></span>

<span data-ttu-id="a78df-119">Som standard er det kun chefer, der kan tildele udvidet logon til medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="a78df-119">By default, only managers can assign extended logon to workers.</span></span> <span data-ttu-id="a78df-120">Hvis du vil tildele udvidet logon, skal du gå til **Udvidet logon** i POS.</span><span class="sxs-lookup"><span data-stu-id="a78df-120">To assign extended logon, go to **Extended log on** in POS.</span></span> <span data-ttu-id="a78df-121">Søg derefter efter en medarbejder ved at angive hans eller hendes operatør-id i søgefeltet.</span><span class="sxs-lookup"><span data-stu-id="a78df-121">Then search for a worker by entering his or her operator ID in the search field.</span></span> <span data-ttu-id="a78df-122">Vælg medarbejderen, og klik derefter på **Tildel**.</span><span class="sxs-lookup"><span data-stu-id="a78df-122">Select the worker, and then click **Assign**.</span></span> <span data-ttu-id="a78df-123">På næste side skal det udvidede logon stryges eller scannes for at tildele medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="a78df-123">On the next page, swipe or scan the extended logon to assign to the worker.</span></span> <span data-ttu-id="a78df-124">Hvis strygningen eller scanning indlæses, bliver knappen **OK** tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="a78df-124">If the swipe or scan is successfully read, the **OK** button becomes available.</span></span> <span data-ttu-id="a78df-125">Klik på **OK** for at gemme det udvidede logon for den medarbejder.</span><span class="sxs-lookup"><span data-stu-id="a78df-125">Click **OK** to save the extended logon for that worker.</span></span>

## <a name="deleting-an-extended-logon"></a><span data-ttu-id="a78df-126">Slette et udvidet logon</span><span class="sxs-lookup"><span data-stu-id="a78df-126">Deleting an extended logon</span></span>

<span data-ttu-id="a78df-127">Hvis du vil slette det udvidede logon, der er tildelt til en medarbejder, søger du efter medarbejderen ved hjælp af handlingen **Udvidet logon**.</span><span class="sxs-lookup"><span data-stu-id="a78df-127">To delete the extended logon that is assigned to a worker, search for the worker by using the **Extended log on** operation.</span></span> <span data-ttu-id="a78df-128">Vælg medarbejderen, og klik derefter på **Fjern tildeling**.</span><span class="sxs-lookup"><span data-stu-id="a78df-128">Select the worker, and then click **Unassign**.</span></span> <span data-ttu-id="a78df-129">Alle udvidede logonoplysninger, som er knyttet til medarbejderen, er fjernet.</span><span class="sxs-lookup"><span data-stu-id="a78df-129">All extended logon credentials that are associated with that worker are removed.</span></span>

## <a name="extending-extended-logon"></a><span data-ttu-id="a78df-130">Udvide udvidet logon</span><span class="sxs-lookup"><span data-stu-id="a78df-130">Extending extended logon</span></span>

<span data-ttu-id="a78df-131">Logontjenesten kan udvides til at understøtte yderligere enheder med udvidet logon, f.eks. håndfladescannere.</span><span class="sxs-lookup"><span data-stu-id="a78df-131">The logon service can be extended to support additional extended logon devices, such as palm scanners.</span></span> <span data-ttu-id="a78df-132">Yderligere oplysninger finder du i dokumentationen om POS-udvidelsesmuligheder.</span><span class="sxs-lookup"><span data-stu-id="a78df-132">For more information, see the POS extensibility documentation.</span></span>

## <a name="using-extended-logon"></a><span data-ttu-id="a78df-133">Brug af udvidet logon</span><span class="sxs-lookup"><span data-stu-id="a78df-133">Using extended logon</span></span>

<span data-ttu-id="a78df-134">Når Udvidet logon er konfigureret, og en medarbejder har fået tildelt en stregkode eller magnetstribe, skal medarbejderen har blot stryge eller scanne sit kort, mens POS-logonsiden vises.</span><span class="sxs-lookup"><span data-stu-id="a78df-134">When extended logon is configured, and a worker has been assigned a bar code or magnetic stripe, the worker just has to swipe or scan his or her card while the POS logon page is displayed.</span></span> <span data-ttu-id="a78df-135">Hvis der også kræves en adgangskode, før logon kan fortsætte, kan medarbejderen indtaste sin adgangskode.</span><span class="sxs-lookup"><span data-stu-id="a78df-135">If a password is also required before logon can proceed, the worker is prompted to enter his or her password.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]