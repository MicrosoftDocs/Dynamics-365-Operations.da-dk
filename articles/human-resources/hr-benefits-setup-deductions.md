---
title: Konfigurere fradrag
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 7ee9e8f3bc0e9027e41d3aa91bd097a3f046cbb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008508"
---
# <a name="configure-deductions"></a><span data-ttu-id="c1d12-102">Konfigurere fradrag</span><span class="sxs-lookup"><span data-stu-id="c1d12-102">Configure deductions</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="c1d12-103">Du kan bruge fradrag i Microsoft Dynamics 365 Human Resources til at afgøre, hvor meget der eventuelt skal trækkes fra en medarbejders løn for hvert enkelt frynsegode.</span><span class="sxs-lookup"><span data-stu-id="c1d12-103">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="c1d12-104">Fradrag gælder for datoer, så du kan bevare en historisk oversigt over oplysninger om fradrag.</span><span class="sxs-lookup"><span data-stu-id="c1d12-104">Deductions are date effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="c1d12-105">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Fradrag** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c1d12-105">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="c1d12-106">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c1d12-106">Select **New**.</span></span>

3. <span data-ttu-id="c1d12-107">Angiv værdier for følgende felter:</span><span class="sxs-lookup"><span data-stu-id="c1d12-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="c1d12-108">Felt</span><span class="sxs-lookup"><span data-stu-id="c1d12-108">Field</span></span> | <span data-ttu-id="c1d12-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c1d12-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c1d12-110">Fradrag</span><span class="sxs-lookup"><span data-stu-id="c1d12-110">Deduction</span></span> | <span data-ttu-id="c1d12-111">Et entydigt id, der bruges til at identificere frynsegodefradraget.</span><span class="sxs-lookup"><span data-stu-id="c1d12-111">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="c1d12-112">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c1d12-112">Description</span></span> | <span data-ttu-id="c1d12-113">En beskrivelse af fradraget.</span><span class="sxs-lookup"><span data-stu-id="c1d12-113">A description for the deduction.</span></span> |
   | <span data-ttu-id="c1d12-114">Gyldig</span><span class="sxs-lookup"><span data-stu-id="c1d12-114">Effective</span></span> | <span data-ttu-id="c1d12-115">Startdatoen.</span><span class="sxs-lookup"><span data-stu-id="c1d12-115">The start date.</span></span> <span data-ttu-id="c1d12-116">Standardværdien er den aktuelle systemdato.</span><span class="sxs-lookup"><span data-stu-id="c1d12-116">The default value is the current system date.</span></span> |
   | <span data-ttu-id="c1d12-117">Udløb</span><span class="sxs-lookup"><span data-stu-id="c1d12-117">Expiration</span></span> | <span data-ttu-id="c1d12-118">Slutdatoen.</span><span class="sxs-lookup"><span data-stu-id="c1d12-118">The end date.</span></span> <span data-ttu-id="c1d12-119">Standardværdien er 31-12-2154, som angiver aldrig.</span><span class="sxs-lookup"><span data-stu-id="c1d12-119">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="c1d12-120">Overskrift</span><span class="sxs-lookup"><span data-stu-id="c1d12-120">Heading</span></span> | <span data-ttu-id="c1d12-121">Overskriftskoden fra det lønsystem, som dette fradrag vil bruge til medarbejderdelen af fradraget ved behandling af frynsegoder i forbindelse med løn.</span><span class="sxs-lookup"><span data-stu-id="c1d12-121">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="c1d12-122">Den bruges, når du bruger en tredjepartslønudbyder.</span><span class="sxs-lookup"><span data-stu-id="c1d12-122">This is used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="c1d12-123">Reference for medarbejders lønfradrag</span><span class="sxs-lookup"><span data-stu-id="c1d12-123">Employee payroll deduction reference</span></span> | <span data-ttu-id="c1d12-124">Fradragskoden fra det lønsystem, som dette fradrag bruger for medarbejderdelen af fradraget, når der behandles frynsegoder til løn.</span><span class="sxs-lookup"><span data-stu-id="c1d12-124">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="c1d12-125">Beløbsoverskrift</span><span class="sxs-lookup"><span data-stu-id="c1d12-125">Amount heading</span></span> | <span data-ttu-id="c1d12-126">Overskriftskoden fra det lønsystem, som dette fradragsbeløb vil bruge til medarbejderdelen af fradraget ved behandling af frynsegoder i forbindelse med løn.</span><span class="sxs-lookup"><span data-stu-id="c1d12-126">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="c1d12-127">Den bruges normalt, når du bruger en tredjepartslønudbyder.</span><span class="sxs-lookup"><span data-stu-id="c1d12-127">This is normally used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="c1d12-128">Kan slette</span><span class="sxs-lookup"><span data-stu-id="c1d12-128">Can delete</span></span> | <span data-ttu-id="c1d12-129">Angiver, om en eksporteret værdi fra Dynamics 365 for Finance and Operations kan forårsage, at værdien slettes i lønsystemet.</span><span class="sxs-lookup"><span data-stu-id="c1d12-129">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="c1d12-130">Parrede kolonner</span><span class="sxs-lookup"><span data-stu-id="c1d12-130">Paired columns</span></span> | <span data-ttu-id="c1d12-131">Angiver, om der skal eksporteres overskrifts- og fradragsbeløb i parrede tilstødende kolonner til lønsystemet.</span><span class="sxs-lookup"><span data-stu-id="c1d12-131">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="c1d12-132">Skift ikrafttrædelsesdato</span><span class="sxs-lookup"><span data-stu-id="c1d12-132">Change effective date</span></span> | <span data-ttu-id="c1d12-133">Den dato, hvor ændringen af frynsegodefradraget træder i kraft.</span><span class="sxs-lookup"><span data-stu-id="c1d12-133">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="c1d12-134">På denne dato vil systemet automatisk ændre frynsegodefradraget og opdatere alle de frynsegodeplaner, der er tilknyttet fradraget, hvis du kører behandling af opdatering af ændret fradrag.</span><span class="sxs-lookup"><span data-stu-id="c1d12-134">On this date the system will automatically change the benefit deduction and update all benefit plans associated with this deduction, as long as you run Deduction change update processing.</span></span> |
   | <span data-ttu-id="c1d12-135">Ændring af fradrag fuldført</span><span class="sxs-lookup"><span data-stu-id="c1d12-135">Deduction change completed</span></span> | <span data-ttu-id="c1d12-136">Afkrydsningsfeltet Ændret fradrag er fuldført markeres automatisk, når ændringen af frynsegodefradraget er fuldført af fradrag af behandlingen af opdatering af ændret fradrag.</span><span class="sxs-lookup"><span data-stu-id="c1d12-136">The Deduction change completed check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="c1d12-137">Hvis du vil spore og vedligeholde ændringer af opsætningen af frynsegodesatsen, skal du vælge **Handlinger** og derefter vælge **Vedligehold versioner**.</span><span class="sxs-lookup"><span data-stu-id="c1d12-137">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="c1d12-138">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c1d12-138">Select **Save**.</span></span> 
