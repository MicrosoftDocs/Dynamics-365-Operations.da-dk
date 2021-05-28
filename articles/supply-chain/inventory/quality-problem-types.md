---
title: Problemtyper for uoverensstemmelser
description: Dette emne beskriver, hvordan du opretter og bruger problemtyper til uoverensstemmelser.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 742edec8570610efe41a2c627efd1df586e0733e
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022150"
---
# <a name="problem-types-for-nonconformances"></a><span data-ttu-id="b1ab5-103">Problemtyper for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="b1ab5-103">Problem types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1ab5-104">Dette emne beskriver, hvordan du opretter og bruger problemtyper til uoverensstemmelser.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-104">This topic describes how to create and use problem types for nonconformances.</span></span>

<span data-ttu-id="b1ab5-105">Du kan bruge siden **Problemtyper** til at definere en klassifikation af de kvalitetsproblemer, der kan opstå for de forskellige uoverensstemmelsestyper.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-105">You use the **Problem types** page to define a classification of the quality problems that might occur for the various nonconformance types.</span></span> <span data-ttu-id="b1ab5-106">For hver problemtype, du opretter, skal du angive de typer uoverensstemmelser, som problemtypen kan bruges til.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-106">For each problem type that you create, you must specify the types of nonconformances that the problem type can be used with.</span></span> <span data-ttu-id="b1ab5-107">Du kan oprette følgende typer af uoverensstemmelser:</span><span class="sxs-lookup"><span data-stu-id="b1ab5-107">You can set up the following nonconformance types:</span></span>

- <span data-ttu-id="b1ab5-108">**Interne** – Uoverensstemmelser af denne type er relateret til den disponible lagerbeholdning (f.eks. kvalitetsordrer eller karantæneordrer).</span><span class="sxs-lookup"><span data-stu-id="b1ab5-108">**Internal** – Nonconformances of this type are related to on-hand inventory (for example, quality orders or quarantine orders).</span></span>
- <span data-ttu-id="b1ab5-109">**Debitor** – Uoverensstemmelser af denne type er relateret til salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-109">**Customer** – Nonconformances of this type are related to sales orders.</span></span>
- <span data-ttu-id="b1ab5-110">**Kreditor** – Uoverensstemmelser af denne type er relateret til indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-110">**Vendor** – Nonconformances of this type are related to purchase orders.</span></span>
- <span data-ttu-id="b1ab5-111">**Serviceanmodning** – Uoverensstemmelser af denne type er relateret til serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-111">**Service request** – Nonconformances of this type are related to service orders.</span></span>
- <span data-ttu-id="b1ab5-112">**Produktion** – Uoverensstemmelser af denne type er relateret til batchordrer eller produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-112">**Production** – Nonconformances of this type are related to batch orders or production orders.</span></span>
- <span data-ttu-id="b1ab5-113">**Produktion af samprodukter** – Uoverensstemmelser af denne type er relateret til batchordrer for samprodukter.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-113">**Co-product production** – Nonconformances of this type are related to batch orders for co-products.</span></span>

<span data-ttu-id="b1ab5-114">Når du opretter en ny problemtype, skal du vælge **Uoverensstemmelsestyper** i handlingsruden for at oprette en liste over en eller flere uoverensstemmelsestyper, der er godkendt for problemtypen.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-114">When you create a new problem type, select **Non conformance types** on the Action Pane to create a list of one or more nonconformance types that are authorized for the problem type.</span></span> <span data-ttu-id="b1ab5-115">En problemtype, der er relateret til en defektkode kunne f.eks. gælde for alle uoverensstemmelsestyper.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-115">For example, a problem type that is related to a defect code might apply to all nonconformance types.</span></span> <span data-ttu-id="b1ab5-116">Men en problemtype, der er relateret til kundeklager, gælder måske kun for uoverensstemmelsestyperne **Debitor** og **Serviceanmodning**.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-116">However, a problem type that is related to customer complaints might apply only to the **Customer** and **Service request** nonconformance types.</span></span>

## <a name="examples-of-problem-types"></a><span data-ttu-id="b1ab5-117">Eksempler på problemtyper</span><span class="sxs-lookup"><span data-stu-id="b1ab5-117">Examples of problem types</span></span>

<span data-ttu-id="b1ab5-118">Her er nogle eksempler på scenarier for problemtyper, der kan bruges til de forskellige uoverensstemmelsestyper:</span><span class="sxs-lookup"><span data-stu-id="b1ab5-118">Here are some examples of scenarios for problem types that can be used with the different nonconformance types:</span></span>

- <span data-ttu-id="b1ab5-119">**Kunde:** En kunde har indsendt en klage, en kunde har returneret en vare, eller kvalitetsspecifikationer er ikke opfyldt.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-119">**Customer:** A customer filed a complaint, a customer made a return, or quality specifications weren't met.</span></span>
- <span data-ttu-id="b1ab5-120">**Leverandør:** Produktet er beskadiget, kvalitetsspecifikationer er ikke opfyldt, eller det forkerte produkt er modtaget.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-120">**Vendor:** The product was damaged, quality specifications weren't met, or the wrong product was received.</span></span>
- <span data-ttu-id="b1ab5-121">**Serviceanmodning:** Kvalitetsspecifikationer er ikke opfyldt, en kunde har indsendt en klage, eller der kræves vedligeholdelse af maskiner.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-121">**Service request:** Quality specifications weren't met, a customer filed a complaint, or machine maintenance is required.</span></span>
- <span data-ttu-id="b1ab5-122">**Produktion:** Kvalitetsspecifikationer er ikke opfyldt, der kræves vedligeholdelse af maskiner, eller produktet er beskadiget.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-122">**Production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>
- <span data-ttu-id="b1ab5-123">**Produktion af samprodukter:** Kvalitetsspecifikationer er ikke opfyldt, der kræves vedligeholdelse af maskiner, eller produktet er beskadiget.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-123">**Co-product production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a><span data-ttu-id="b1ab5-124">Oprette en problemtype og tildele den til uoverensstemmelsestyper</span><span class="sxs-lookup"><span data-stu-id="b1ab5-124">Create a problem type and assign it to nonconformance types</span></span>

1. <span data-ttu-id="b1ab5-125">Gå til **Lagerstyring \> Opsætning \> Kvalitetsstyring \> Problemtyper**.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-125">Go to **Inventory management \> Setup \> Quality management \> Problem types**.</span></span>
1. <span data-ttu-id="b1ab5-126">Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-126">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b1ab5-127">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="b1ab5-127">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="b1ab5-128">**Problemtype** – Angiv et entydigt id eller navn til problemtypen.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-128">**Problem type** – Enter a unique ID or name for the problem type.</span></span>
    - <span data-ttu-id="b1ab5-129">**Beskrivelse** – Indtast en detaljeret beskrivelse af problemtypen.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-129">**Description** – Enter a detailed description of the problem type.</span></span>

1. <span data-ttu-id="b1ab5-130">Mens den nye række stadig er markeret, skal du vælge **Uoverensstemmelsestyper** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-130">While the new row is still selected, select **Non conformance types** on the Action Pane.</span></span>
1. <span data-ttu-id="b1ab5-131">Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-131">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b1ab5-132">Derefter skal du for den nye række indstille feltet **Uoverensstemmelsestype** til den uoverensstemmelsestype, som du vil tillade for problemtypen.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-132">Then, for the new row, set the **Non conformance type** field to the nonconformance type that you want to allow for the problem type.</span></span>
1. <span data-ttu-id="b1ab5-133">Gentag det forrige trin for hver ekstra uoverensstemmelsestype, du vil autorisere for problemtypen.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-133">Repeat the previous step for each additional nonconformance type that you want to authorize for the problem type.</span></span>
1. <span data-ttu-id="b1ab5-134">Luk siderne.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-134">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1ab5-135">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b1ab5-135">Additional resources</span></span>

- [<span data-ttu-id="b1ab5-136">Oversigt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="b1ab5-136">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="b1ab5-137">Aktivere styring af kvalitet og uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="b1ab5-137">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="b1ab5-138">Arbejdere, der er ansvarlige for godkendelse af uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="b1ab5-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="b1ab5-139">Karantænezoner for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="b1ab5-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="b1ab5-140">Diagnosticeringstyper for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="b1ab5-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="b1ab5-141">Kvalitetsgebyrer for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="b1ab5-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="b1ab5-142">Operationer for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="b1ab5-142">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="b1ab5-143">Kvalitetsstyring for lagerstedsprocesser.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
