---
title: Operationer for uoverensstemmelser
description: Dette emne beskriver, hvordan du opretter og bruger operationer til uoverensstemmelser.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9a6cc88b80f82d77edac0341cb6a3c0db4b42ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022198"
---
# <a name="operations-for-nonconformances"></a><span data-ttu-id="6956f-103">Operationer for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="6956f-103">Operations for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6956f-104">Dette emne beskriver, hvordan du opretter og bruger operationer til uoverensstemmelser.</span><span class="sxs-lookup"><span data-stu-id="6956f-104">This topic describes how to create and use operations for nonconformances.</span></span>

<span data-ttu-id="6956f-105">Du kan bruge siden **Operationer** til at definere klassifikationer af det arbejde, der kan udføres for en godkendt uoverensstemmelse.</span><span class="sxs-lookup"><span data-stu-id="6956f-105">You can use the **Operations** page to define classifications of the work that can be performed for an approved nonconformance.</span></span> <span data-ttu-id="6956f-106">Når du knytter en relateret operation til en uoverensstemmelse, kan du angive detaljer som f.eks. det tilknyttede materiale, de arbejdstimer og gebyrer, der kræves for at udføre operationen.</span><span class="sxs-lookup"><span data-stu-id="6956f-106">When you assign a related operation to a nonconformance, you can provide details such as the associated material, labor hours, and charges that are required to do the operation.</span></span> <span data-ttu-id="6956f-107">Systemet bruger disse oplysninger bruges til at beregne en forkalkuleret omkostning for operationen.</span><span class="sxs-lookup"><span data-stu-id="6956f-107">The system uses this information to calculate an estimated cost for the operation.</span></span> <span data-ttu-id="6956f-108">De detaljerede oplysninger og forkalkulerede omkostninger er til reference.</span><span class="sxs-lookup"><span data-stu-id="6956f-108">The detailed information and estimated costs are for reference.</span></span> <span data-ttu-id="6956f-109">De relaterede operationer for kvalitet er ikke de samme som de operationer, der kan angives for en produktionsrute.</span><span class="sxs-lookup"><span data-stu-id="6956f-109">The related operations for quality differ from the operations that can be defined for a production route.</span></span>

> [!NOTE]
> <span data-ttu-id="6956f-110">Selvom du kan spore omkostninger, tid og de varer, der bruges i en operation, der er relateret til en uoverensstemmelse, er de data, du angiver, kun vejledende.</span><span class="sxs-lookup"><span data-stu-id="6956f-110">Although you can track costs, time, and the items that are used in an operation that is related to a nonconformance, the data that you enter is only informational.</span></span> <span data-ttu-id="6956f-111">De integreres ikke automatisk med finansregnskabet, lagerregnskabet eller modulet **Tid og fremmøde**.</span><span class="sxs-lookup"><span data-stu-id="6956f-111">It isn't automatically integrated with the general ledger, inventory subledger, or the **Time and attendance** module.</span></span>

## <a name="examples-of-operations"></a><span data-ttu-id="6956f-112">Eksempler på operationer</span><span class="sxs-lookup"><span data-stu-id="6956f-112">Examples of operations</span></span>

<span data-ttu-id="6956f-113">Du arbejder i en produktionsvirksomhed.</span><span class="sxs-lookup"><span data-stu-id="6956f-113">You work for a manufacturing company.</span></span> <span data-ttu-id="6956f-114">Der blev oprettet og godkendt en uoverensstemmelse for varer, der ikke bestod en kvalitetstest.</span><span class="sxs-lookup"><span data-stu-id="6956f-114">A nonconformance was created and approved for items that failed a quality test.</span></span> <span data-ttu-id="6956f-115">Der er oprettet en rettelse, som angiver, at problemet var relateret til et beskadiget leje i en maskine.</span><span class="sxs-lookup"><span data-stu-id="6956f-115">A correction was created to indicate that the problem was related to a bad bearing on a machine.</span></span> <span data-ttu-id="6956f-116">Der kræves adskillige trin for at udskifte lejet, og ansvaret for hver operation spores.</span><span class="sxs-lookup"><span data-stu-id="6956f-116">Several steps are required to replace the bearing, and the responsibility for each operation is tracked.</span></span> <span data-ttu-id="6956f-117">Følgende trin kan f.eks. være påkrævede:</span><span class="sxs-lookup"><span data-stu-id="6956f-117">For example, the following steps might be required:</span></span>

1. <span data-ttu-id="6956f-118">Produktionslinjen standses, og oprydningsrutinen udføres.</span><span class="sxs-lookup"><span data-stu-id="6956f-118">The production line is stopped, and the clean-out routine is performed.</span></span>
1. <span data-ttu-id="6956f-119">Reparatører udskifter lejet.</span><span class="sxs-lookup"><span data-stu-id="6956f-119">Maintenance personnel replace the bearing.</span></span>
1. <span data-ttu-id="6956f-120">Kvalitetssikringsmedarbejdere inspicerer maskinen, før den er tændes igen.</span><span class="sxs-lookup"><span data-stu-id="6956f-120">Quality assurance personnel inspect the machine before it's turned back on.</span></span>

<span data-ttu-id="6956f-121">I dette eksempel kan du oprette følgende operationer, der repræsenterer det arbejde, der skal udføres:</span><span class="sxs-lookup"><span data-stu-id="6956f-121">For this example, the following operations can be created to represent the work that must be done:</span></span>

- <span data-ttu-id="6956f-122">Stands produktionslinjen.</span><span class="sxs-lookup"><span data-stu-id="6956f-122">Stop the production line.</span></span>
- <span data-ttu-id="6956f-123">Ryd produktionslinjen.</span><span class="sxs-lookup"><span data-stu-id="6956f-123">Clean out the production line.</span></span>
- <span data-ttu-id="6956f-124">Udfør reparationer på maskinen.</span><span class="sxs-lookup"><span data-stu-id="6956f-124">Perform machine maintenance.</span></span>
- <span data-ttu-id="6956f-125">Inspicer maskinen.</span><span class="sxs-lookup"><span data-stu-id="6956f-125">Inspect the machine.</span></span>

## <a name="create-an-operation"></a><span data-ttu-id="6956f-126">Oprette en operation</span><span class="sxs-lookup"><span data-stu-id="6956f-126">Create an operation</span></span>

1. <span data-ttu-id="6956f-127">Gå til **Lagerstyring \> Opsætning \> Kvalitetsstyring \> Operationer**.</span><span class="sxs-lookup"><span data-stu-id="6956f-127">Go to **Inventory management \> Setup \> Quality management \> Operations**.</span></span>
1. <span data-ttu-id="6956f-128">Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="6956f-128">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="6956f-129">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="6956f-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="6956f-130">**Operation** – Angiv et entydigt id eller navn til operationen.</span><span class="sxs-lookup"><span data-stu-id="6956f-130">**Operation** – Enter a unique ID or name for the operation.</span></span>
    - <span data-ttu-id="6956f-131">**Beskrivelse** – Indtast en detaljeret beskrivelse af operationen.</span><span class="sxs-lookup"><span data-stu-id="6956f-131">**Description** – Enter a detailed description of the operation.</span></span>
    - <span data-ttu-id="6956f-132">**Type** – Hvis operationen kun kan bruges til uoverensstemmelser, der er relateret til en bestemt ordretype, skal du vælge ordretypen (*Indkøbsordre* eller *Salgsordre*).</span><span class="sxs-lookup"><span data-stu-id="6956f-132">**Type** – If the operation can be used only with nonconformances that are related to a specific type of order, select the order type (*Purchase order* or *Sales order*).</span></span>

1. <span data-ttu-id="6956f-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6956f-133">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6956f-134">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="6956f-134">Additional resources</span></span>

- [<span data-ttu-id="6956f-135">Oversigt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="6956f-135">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="6956f-136">Aktivere styring af kvalitet og uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="6956f-136">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="6956f-137">Oprette og behandle uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="6956f-137">Create and process nonconformances</span></span>](tasks/create-process-non-conformance.md)
- [<span data-ttu-id="6956f-138">Arbejdere, der er ansvarlige for godkendelse af uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="6956f-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="6956f-139">Karantænezoner for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="6956f-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="6956f-140">Diagnosticeringstyper for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="6956f-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="6956f-141">Kvalitetsgebyrer for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="6956f-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="6956f-142">Problemtyper for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="6956f-142">Problem types for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="6956f-143">Kvalitetsstyring for lagerstedsprocesser.</span><span class="sxs-lookup"><span data-stu-id="6956f-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
