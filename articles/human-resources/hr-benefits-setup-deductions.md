---
title: Konfigurere fradrag
description: Du kan bruge fradrag i Microsoft Dynamics 365 Human Resources til at afgøre, hvor meget der eventuelt skal trækkes fra en medarbejders løn for hvert enkelt frynsegode.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5e645c3f098163626cb686aba347897781d7ebc0
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230056"
---
# <a name="configure-deductions"></a><span data-ttu-id="868a1-103">Konfigurere fradrag</span><span class="sxs-lookup"><span data-stu-id="868a1-103">Configure deductions</span></span>

<span data-ttu-id="868a1-104">Du kan bruge fradrag i Microsoft Dynamics 365 Human Resources til at afgøre, hvor meget der eventuelt skal trækkes fra en medarbejders løn for hvert enkelt frynsegode.</span><span class="sxs-lookup"><span data-stu-id="868a1-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="868a1-105">Fradrag gælder for datoer, så du kan bevare en historisk oversigt over oplysninger om fradrag.</span><span class="sxs-lookup"><span data-stu-id="868a1-105">Deductions are date-effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="868a1-106">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Fradrag** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="868a1-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="868a1-107">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="868a1-107">Select **New**.</span></span>

3. <span data-ttu-id="868a1-108">Angiv værdier for følgende felter:</span><span class="sxs-lookup"><span data-stu-id="868a1-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="868a1-109">Felt</span><span class="sxs-lookup"><span data-stu-id="868a1-109">Field</span></span> | <span data-ttu-id="868a1-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="868a1-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="868a1-111">**Fradrag**</span><span class="sxs-lookup"><span data-stu-id="868a1-111">**Deduction**</span></span> | <span data-ttu-id="868a1-112">Et entydigt id, der bruges til at identificere frynsegodefradraget.</span><span class="sxs-lookup"><span data-stu-id="868a1-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="868a1-113">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="868a1-113">**Description**</span></span> | <span data-ttu-id="868a1-114">En beskrivelse af fradraget.</span><span class="sxs-lookup"><span data-stu-id="868a1-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="868a1-115">**Gyldig**</span><span class="sxs-lookup"><span data-stu-id="868a1-115">**Effective**</span></span> | <span data-ttu-id="868a1-116">Startdatoen.</span><span class="sxs-lookup"><span data-stu-id="868a1-116">The start date.</span></span> <span data-ttu-id="868a1-117">Standardværdien er den aktuelle systemdato.</span><span class="sxs-lookup"><span data-stu-id="868a1-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="868a1-118">**Udløb**</span><span class="sxs-lookup"><span data-stu-id="868a1-118">**Expiration**</span></span> | <span data-ttu-id="868a1-119">Slutdatoen.</span><span class="sxs-lookup"><span data-stu-id="868a1-119">The end date.</span></span> <span data-ttu-id="868a1-120">Standardværdien er 31-12-2154, som angiver aldrig.</span><span class="sxs-lookup"><span data-stu-id="868a1-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="868a1-121">**Overskrift**</span><span class="sxs-lookup"><span data-stu-id="868a1-121">**Heading**</span></span> | <span data-ttu-id="868a1-122">Overskriftskoden fra det lønsystem, som dette fradrag vil bruge til medarbejderdelen af fradraget ved behandling af frynsegoder i forbindelse med løn.</span><span class="sxs-lookup"><span data-stu-id="868a1-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="868a1-123">Den bruges, når du bruger en tredjepartslønudbyder.</span><span class="sxs-lookup"><span data-stu-id="868a1-123">This is used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="868a1-124">**Reference for medarbejders lønfradrag**</span><span class="sxs-lookup"><span data-stu-id="868a1-124">**Employee payroll deduction reference**</span></span> | <span data-ttu-id="868a1-125">Fradragskoden fra det lønsystem, som dette fradrag bruger for medarbejderdelen af fradraget, når der behandles frynsegoder til løn.</span><span class="sxs-lookup"><span data-stu-id="868a1-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="868a1-126">**Beløbsoverskrift**</span><span class="sxs-lookup"><span data-stu-id="868a1-126">**Amount heading**</span></span> | <span data-ttu-id="868a1-127">Overskriftskoden fra det lønsystem, som dette fradragsbeløb vil bruge til medarbejderdelen af fradraget ved behandling af frynsegoder i forbindelse med løn.</span><span class="sxs-lookup"><span data-stu-id="868a1-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="868a1-128">Den bruges normalt, når du bruger en tredjepartslønudbyder.</span><span class="sxs-lookup"><span data-stu-id="868a1-128">This is normally used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="868a1-129">**Kan slette**</span><span class="sxs-lookup"><span data-stu-id="868a1-129">**Can delete**</span></span> | <span data-ttu-id="868a1-130">Angiver, om en eksporteret værdi fra Dynamics 365 for Finance and Operations kan forårsage, at værdien slettes i lønsystemet.</span><span class="sxs-lookup"><span data-stu-id="868a1-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="868a1-131">**Parrede kolonner**</span><span class="sxs-lookup"><span data-stu-id="868a1-131">**Paired columns**</span></span> | <span data-ttu-id="868a1-132">Angiver, om der skal eksporteres overskrifts- og fradragsbeløb i parrede tilstødende kolonner til lønsystemet.</span><span class="sxs-lookup"><span data-stu-id="868a1-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="868a1-133">**Skift ikrafttrædelsesdato**</span><span class="sxs-lookup"><span data-stu-id="868a1-133">**Change effective date**</span></span> | <span data-ttu-id="868a1-134">Den dato, hvor ændringen af frynsegodefradraget træder i kraft.</span><span class="sxs-lookup"><span data-stu-id="868a1-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="868a1-135">På denne dato ændrer systemet automatisk frynsegodefradraget og opdaterer alle de frynsegodeplaner, der er tilknyttet fradraget, hvis du kører behandling af **Opdatering af ændret fradrag**.</span><span class="sxs-lookup"><span data-stu-id="868a1-135">On this date, the system automatically changes the benefit deduction and updates all benefit plans associated with this deduction, as long as you run **Deduction change update** processing.</span></span> |
   | <span data-ttu-id="868a1-136">**Ændring af fradrag fuldført**</span><span class="sxs-lookup"><span data-stu-id="868a1-136">**Deduction change completed**</span></span> | <span data-ttu-id="868a1-137">Afkrydsningsfeltet **Ændret fradrag er fuldført** markeres automatisk, når ændringen af frynsegodefradraget er fuldført af fradrag af behandlingen af opdatering af ændret fradrag.</span><span class="sxs-lookup"><span data-stu-id="868a1-137">The **Deduction change completed** check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="868a1-138">Hvis du vil spore og vedligeholde ændringer af opsætningen af frynsegodesatsen, skal du vælge **Handlinger** og derefter vælge **Vedligehold versioner**.</span><span class="sxs-lookup"><span data-stu-id="868a1-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="868a1-139">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="868a1-139">Select **Save**.</span></span> 
