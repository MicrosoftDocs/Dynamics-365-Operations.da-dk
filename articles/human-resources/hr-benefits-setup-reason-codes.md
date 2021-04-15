---
title: Definer årsagskoder
description: Dynamics 365 Human Resources bruger årsagskoder til at forklare, hvorfor en medarbejders frynsegoder ændres.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ee74cb8b11c9b72940448077ee485ade4c0b7a39
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801041"
---
# <a name="set-up-reason-codes"></a><span data-ttu-id="ad1e1-103">Definer årsagskoder</span><span class="sxs-lookup"><span data-stu-id="ad1e1-103">Set up reason codes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ad1e1-104">Dynamics 365 Human Resources bruger årsagskoder til at forklare, hvorfor en medarbejders frynsegoder ændres.</span><span class="sxs-lookup"><span data-stu-id="ad1e1-104">Dynamics 365 Human Resources uses reason codes to explain why an employee’s benefits are changing.</span></span>

> [!NOTE]
> <span data-ttu-id="ad1e1-105">Pr. januar 2021 overføres årsagskoder til arbejdsområdet **Personalestyring** i stedet for arbejdsområdet **Frynsegodeadministration**.</span><span class="sxs-lookup"><span data-stu-id="ad1e1-105">As of January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="ad1e1-106">Der er flere oplysninger i [Manuel overførsel af årsagskoder til Personalestyring](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span><span class="sxs-lookup"><span data-stu-id="ad1e1-106">For more information, see [Manually migrate reason codes to Personnel management](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span></span>

## <a name="create-reason-codes"></a><span data-ttu-id="ad1e1-107">Oprette årsagskoder</span><span class="sxs-lookup"><span data-stu-id="ad1e1-107">Create reason codes</span></span>

1. <span data-ttu-id="ad1e1-108">I arbejdsområdet **Personalestyring** (eller arbejdsområdet **Frynsegodeadministration**, hvis dine årsagskoder endnu ikke er overflyttet), skal du vælge **Links** og derefter vælge **Årsagskoder**.</span><span class="sxs-lookup"><span data-stu-id="ad1e1-108">In the **Personnel management** workspace (or **Benefits management** workspace if your reason codes haven't yet migrated), select **Links**, and then select **Reason codes**.</span></span>

2. <span data-ttu-id="ad1e1-109">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ad1e1-109">Select **New**.</span></span>

3. <span data-ttu-id="ad1e1-110">Angiv værdier for følgende felter:</span><span class="sxs-lookup"><span data-stu-id="ad1e1-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="ad1e1-111">Felt</span><span class="sxs-lookup"><span data-stu-id="ad1e1-111">Field</span></span> | <span data-ttu-id="ad1e1-112">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ad1e1-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ad1e1-113">**Årsagskode**</span><span class="sxs-lookup"><span data-stu-id="ad1e1-113">**Reason code**</span></span> | <span data-ttu-id="ad1e1-114">Et entydigt navn, der identificerer årsagen til, at en medarbejder vil ændre tilmeldingen til en frynsegodeplan.</span><span class="sxs-lookup"><span data-stu-id="ad1e1-114">A unique name to identify the reason an employee would change a benefit plan enrollment.</span></span> |
   | <span data-ttu-id="ad1e1-115">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="ad1e1-115">**Description**</span></span> | <span data-ttu-id="ad1e1-116">En beskrivelse af årsagskoden.</span><span class="sxs-lookup"><span data-stu-id="ad1e1-116">A description of the reason code.</span></span> |

4. <span data-ttu-id="ad1e1-117">Indstil **Frynsegodeadministration** under **Anvendelige scenarier** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ad1e1-117">Under **Applicable scenarios**, set **Benefits management** to **Yes**.</span></span> <span data-ttu-id="ad1e1-118">(Kan ikke anvendes, hvis årsagskoderne endnu ikke er overflyttet til arbejdsområdet **Personalestyring**.)</span><span class="sxs-lookup"><span data-stu-id="ad1e1-118">(Not applicable if your reason codes haven't yet migrated to the **Personnel management** workspace.)</span></span>

5. <span data-ttu-id="ad1e1-119">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ad1e1-119">Select **Save**.</span></span>

## <a name="manually-migrate-reason-codes-to-personnel-management"></a><span data-ttu-id="ad1e1-120">Manuelt overføre årsagskoder til Personalestyring</span><span class="sxs-lookup"><span data-stu-id="ad1e1-120">Manually migrate reason codes to Personnel management</span></span>

<span data-ttu-id="ad1e1-121">I januar 2021 overføres årsagskoder til arbejdsområdet **Personalestyring** i stedet for arbejdsområdet **Frynsegodeadministration**.</span><span class="sxs-lookup"><span data-stu-id="ad1e1-121">In January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="ad1e1-122">De fleste årsagskodedata overføres automatisk i dit miljø.</span><span class="sxs-lookup"><span data-stu-id="ad1e1-122">Most reason code data will automatically migrate in your environment.</span></span> <span data-ttu-id="ad1e1-123">Nogle årsagskodedata kan ikke overføres.</span><span class="sxs-lookup"><span data-stu-id="ad1e1-123">Some reason code data might not migrate.</span></span> <span data-ttu-id="ad1e1-124">Årsagskoder har f.eks. nu et maksimum på 15 tegn, så enhver årsagskode, der er længere end 15 tegn, overføres ikke automatisk.</span><span class="sxs-lookup"><span data-stu-id="ad1e1-124">For example, reason codes now have a 15-character maximum, so any reason codes longer than 15 characters won't migrate automatically.</span></span>

<span data-ttu-id="ad1e1-125">Du får vist et banner på siden **Links** i arbejdsområdet til **Frynsegodeadministration**, der oplyser dig om overflytningen, og om årsagskoder ikke er blevet overflyttet.</span><span class="sxs-lookup"><span data-stu-id="ad1e1-125">You'll see a banner on the **Links** page of the **Benefits management** workspace informing you about the migration and whether any reason codes didn't migrate.</span></span>

1. <span data-ttu-id="ad1e1-126">Vælg **Årsagskoder** for oplysninger om overførselsstatus.</span><span class="sxs-lookup"><span data-stu-id="ad1e1-126">Select **Reason codes** for details about migration status.</span></span>

   <span data-ttu-id="ad1e1-127">[![Årsagskoder](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span><span class="sxs-lookup"><span data-stu-id="ad1e1-127">[![Reason codes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span></span>

2. <span data-ttu-id="ad1e1-128">Vælg en årsagskode, der ikke kunne overføres.</span><span class="sxs-lookup"><span data-stu-id="ad1e1-128">Select a reason code that failed to migrate.</span></span>

   <span data-ttu-id="ad1e1-129">[![Status for overførsel af årsagskode](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span><span class="sxs-lookup"><span data-stu-id="ad1e1-129">[![Reason code migration status](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span></span>

3. <span data-ttu-id="ad1e1-130">Vælg **Overfør årsagskode**.</span><span class="sxs-lookup"><span data-stu-id="ad1e1-130">Select **Migrate reason code**.</span></span>

   <span data-ttu-id="ad1e1-131">[![Overfør årsagskode](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span><span class="sxs-lookup"><span data-stu-id="ad1e1-131">[![Migrate reason code](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span></span>

4. <span data-ttu-id="ad1e1-132">I ruden **Overflytning af frynsegodeadministration** har du to muligheder for tilknytning til en årsagskode for personalestyring:</span><span class="sxs-lookup"><span data-stu-id="ad1e1-132">In the **Benefit reason code migration** pane, you have two options for mapping to a Personnel management reason code:</span></span>

   - <span data-ttu-id="ad1e1-133">Hvis du vil bruge en eksisterende årsagskode i Personalestyring, skal du vælge en fra rullelisten **Brug eksisterende årsagskode**.</span><span class="sxs-lookup"><span data-stu-id="ad1e1-133">To use an existing reason code in Personnel management, choose one from the **Use existing reason code** dropdown.</span></span>
     > [!NOTE]
     > <span data-ttu-id="ad1e1-134">Du kan kun bruge en eksisterende årsagskode i Personalestyring, hvis en anden årsagskode for goder ikke allerede er overflyttet til den.</span><span class="sxs-lookup"><span data-stu-id="ad1e1-134">You can only use an existing reason code in Personnel management if another Benefits management reason code hasn't already migrated to it.</span></span>
   - <span data-ttu-id="ad1e1-135">Hvis du vil oprette en ny årsagskode i Personalestyring, skal du angive en ny i **Ny årsagskode** og derefter angive en beskrivelse i **Ny beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="ad1e1-135">To create a new reason code in Personnel management, enter a new one in **New reason code**, and then enter a description in **New description**.</span></span>

   <span data-ttu-id="ad1e1-136">[![Tilknytte en årsagskode for personalestyring](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span><span class="sxs-lookup"><span data-stu-id="ad1e1-136">[![Map to a Personnel management reason code](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span></span>

<span data-ttu-id="ad1e1-137">Når årsagskoder er overført til Personalestyring, angives indstillingen for brug af dem i Styring af goder automatisk til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ad1e1-137">After reason codes migrate to Personnel management, the option for using them in Benefits management is automatically set to **Yes**.</span></span>

<span data-ttu-id="ad1e1-138">[![Bruge årsagskoder i administration af frynsegoder](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span><span class="sxs-lookup"><span data-stu-id="ad1e1-138">[![Use reason code in Benefits management](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]