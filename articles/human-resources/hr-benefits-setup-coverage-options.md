---
title: Oprette disponeringsindstillinger
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
ms.openlocfilehash: 27b43d858a92beac526ac0fc40b544649ef658b0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008432"
---
# <a name="create-coverage-options"></a><span data-ttu-id="66469-102">Oprette disponeringsindstillinger</span><span class="sxs-lookup"><span data-stu-id="66469-102">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="66469-103">Disponeringsindstillinger i Microsoft Dynamics 365 Human Resources er disponeringsniveauer for en deltagers valg i en frynsegodeplan eller et frynsegodeprogram, f.eks. Kun medarbejder for en medicinsk plan eller en 2 x løn for en livsforsikringsplan.</span><span class="sxs-lookup"><span data-stu-id="66469-103">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="66469-104">Når den er defineret, kan indstillingerne for frynsegodedisponering genbruges, og du kan knytte en indstilling til en eller flere planer.</span><span class="sxs-lookup"><span data-stu-id="66469-104">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="66469-105">Når disponeringsindstillingerne er defineret, skal du knytte disponeringsindstillingerne til en type af frynsegodeplan.</span><span class="sxs-lookup"><span data-stu-id="66469-105">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="66469-106">Plantypen knyttes derefter til en frynsegodeplan eller et frynsegodeprogram.</span><span class="sxs-lookup"><span data-stu-id="66469-106">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="66469-107">Disponeringsindstillinger, der er knyttet til plantype, vil være tilgængelige for alle de planer, der oprettes med den pågældende plantype.</span><span class="sxs-lookup"><span data-stu-id="66469-107">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="66469-108">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Disponeringsindstillinger** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="66469-108">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="66469-109">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="66469-109">Select **New**.</span></span>

3. <span data-ttu-id="66469-110">Angiv værdier for følgende felter:</span><span class="sxs-lookup"><span data-stu-id="66469-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="66469-111">Felt</span><span class="sxs-lookup"><span data-stu-id="66469-111">Field</span></span> | <span data-ttu-id="66469-112">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="66469-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="66469-113">**Disponeringsindstilling**</span><span class="sxs-lookup"><span data-stu-id="66469-113">**Coverage option**</span></span> | <span data-ttu-id="66469-114">Et entydigt navn på en disponeringsindstilling.</span><span class="sxs-lookup"><span data-stu-id="66469-114">A unique coverage option name.</span></span> |
   | <span data-ttu-id="66469-115">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="66469-115">**Description**</span></span> | <span data-ttu-id="66469-116">En beskrivelse af disponeringsindstillingen.</span><span class="sxs-lookup"><span data-stu-id="66469-116">A description of the coverage option.</span></span> |
   | <span data-ttu-id="66469-117">**Dækningskode**</span><span class="sxs-lookup"><span data-stu-id="66469-117">**Coverage code**</span></span> | <span data-ttu-id="66469-118">Disponeringskoder tilknytter minimum- og maksimumbeløb for alle berettigede disponerede persontyper.</span><span class="sxs-lookup"><span data-stu-id="66469-118">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="66469-119">En disponeringskode angiver, hvem der er disponeret, eller disponeringsbeløbet, der er tilladt for en plantype.</span><span class="sxs-lookup"><span data-stu-id="66469-119">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="66469-120">Du kan udtrykke beløbet for disponering som et kronebeløb eller en procentdel.</span><span class="sxs-lookup"><span data-stu-id="66469-120">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="66469-121">F.eks.:</span><span class="sxs-lookup"><span data-stu-id="66469-121">For example:</span></span></br></br><span data-ttu-id="66469-122">- **EMP+1** – for at blive kvalificeret skal medarbejderen have valgt én afhængig (hvis der er valgt mere end én, er de ikke længere kvalificeret).</span><span class="sxs-lookup"><span data-stu-id="66469-122">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="66469-123">- **EMP+familie** – for at blive kvalificeret skal medarbejderen have valgt mindst to afhængige.</span><span class="sxs-lookup"><span data-stu-id="66469-123">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="66469-124">**Maks. antal**</span><span class="sxs-lookup"><span data-stu-id="66469-124">**Maximum number**</span></span> | <span data-ttu-id="66469-125">Maks. antal af afhængige.</span><span class="sxs-lookup"><span data-stu-id="66469-125">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="66469-126">**Status**</span><span class="sxs-lookup"><span data-stu-id="66469-126">**Status**</span></span> | <span data-ttu-id="66469-127">Statussen for disponeringsindstillingen.</span><span class="sxs-lookup"><span data-stu-id="66469-127">The status of the coverage option.</span></span> <span data-ttu-id="66469-128">Hvis status for disponeringsindstillingen er angivet til Inaktiv, kan indstillingen Disponering ikke vælges for plantyper.</span><span class="sxs-lookup"><span data-stu-id="66469-128">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="66469-129">**Procent**</span><span class="sxs-lookup"><span data-stu-id="66469-129">**Percent**</span></span> | <span data-ttu-id="66469-130">Beløb i procent.</span><span class="sxs-lookup"><span data-stu-id="66469-130">The percent amount.</span></span> <span data-ttu-id="66469-131">Dette felt er kun aktivt, hvis % x løn blev valgt i feltet Disponeringskode.</span><span class="sxs-lookup"><span data-stu-id="66469-131">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="66469-132">**Nævner**</span><span class="sxs-lookup"><span data-stu-id="66469-132">**Divisor**</span></span> | <span data-ttu-id="66469-133">Den divisor, der skal bruges i beregningen, når du vælger disponeringskode % x løn.</span><span class="sxs-lookup"><span data-stu-id="66469-133">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="66469-134">**Min. procentdel**</span><span class="sxs-lookup"><span data-stu-id="66469-134">**Percent minimum**</span></span> | <span data-ttu-id="66469-135">Den minimale procentdel, når du vælger Procentdisponeringskode.</span><span class="sxs-lookup"><span data-stu-id="66469-135">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="66469-136">**Maks. procent**</span><span class="sxs-lookup"><span data-stu-id="66469-136">**Percent maximum**</span></span> | <span data-ttu-id="66469-137">Den maksimale procentdel, når du vælger Procentdisponeringskode.</span><span class="sxs-lookup"><span data-stu-id="66469-137">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="66469-138">Under **Indstillinger for berettigelse for personlige kontakter** skal du knytte den relevante indstilling for personlig kontaktberettigelse til de enkelte disponeringsindstillinger.</span><span class="sxs-lookup"><span data-stu-id="66469-138">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="66469-139">Under **Selvbetjening** skal du angive værdier for følgende felter:</span><span class="sxs-lookup"><span data-stu-id="66469-139">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="66469-140">Felt</span><span class="sxs-lookup"><span data-stu-id="66469-140">Field</span></span> | <span data-ttu-id="66469-141">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="66469-141">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="66469-142">**Tillad medarbejderbidragsbeløb**</span><span class="sxs-lookup"><span data-stu-id="66469-142">**Allow employee contribution amount**</span></span> | <span data-ttu-id="66469-143">Angiver, om medarbejdere skal kunne redigere bidragsbeløbet via selvbetjening for frynsegoder, når de vælger frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="66469-143">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="66469-144">Hvis du markerer dette afkrydsningsfelt, beregner systemet parametre for frynsegodeplanen baseret på det bidragsbeløb, som medarbejderen indtaster i selvbetjeningstjenesten for frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="66469-144">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="66469-145">**Tillad medarbejderdækningsbeløb**</span><span class="sxs-lookup"><span data-stu-id="66469-145">**Allow employee coverage amount**</span></span> | <span data-ttu-id="66469-146">Angiver, om medarbejdere skal kunne redigere disponeringsbeløbet via selvbetjening for frynsegoder, når de vælger frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="66469-146">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="66469-147">Hvis du markerer dette afkrydsningsfelt, beregner systemet parametre for frynsegodeplanen baseret på det disponeringsbeløb, som medarbejderen indtaster i selvbetjeningstjenesten for medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="66469-147">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="66469-148">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="66469-148">Select **Save**.</span></span> 
