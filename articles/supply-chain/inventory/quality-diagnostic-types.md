---
title: Diagnosticeringstyper for uoverensstemmelser
description: Dette emne beskriver, hvordan du bruger og opretter diagnosticeringstyper, der kan bruges sammen med uoverensstemmelser.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19fcd57e28efabd6ca32c444ab961b876bde424d
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956588"
---
# <a name="diagnostic-types-for-nonconformances"></a><span data-ttu-id="67fdc-103">Diagnosticeringstyper for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="67fdc-103">Diagnostic types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67fdc-104">Dette emne beskriver, hvordan du bruger og opretter diagnosticeringstyper, der kan bruges sammen med uoverensstemmelser.</span><span class="sxs-lookup"><span data-stu-id="67fdc-104">This topic describes how to use and create diagnostic types that can be used with nonconformances.</span></span>

<span data-ttu-id="67fdc-105">Du kan bruge siden **Diagnosticeringstyper** til definere en klassifikation af diagnosticeringshandlinger.</span><span class="sxs-lookup"><span data-stu-id="67fdc-105">You use the **Diagnostic types** page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="67fdc-106">Når du derefter opretter en rettelse til en uoverensstemmelse, skal du vælge en diagnosticering.</span><span class="sxs-lookup"><span data-stu-id="67fdc-106">Then, when you create a correction for a nonconformance, you select a diagnostic.</span></span> <span data-ttu-id="67fdc-107">En rettelse angiver, hvilken type diagnosticeringshandling der skal udføres for en godkendt uoverensstemmelse, og hvem der skal udføre den pågældende handling.</span><span class="sxs-lookup"><span data-stu-id="67fdc-107">A correction specifies what type of diagnostic action should be taken for an approved nonconformance, and who should take that action.</span></span> <span data-ttu-id="67fdc-108">Den angiver også den ønskede slutdato og den planlagte slutdato.</span><span class="sxs-lookup"><span data-stu-id="67fdc-108">It also specifies the requested completion date and the planned completion date.</span></span>

## <a name="examples-of-diagnostic-types"></a><span data-ttu-id="67fdc-109">Eksempler på diagnosticeringstyper</span><span class="sxs-lookup"><span data-stu-id="67fdc-109">Examples of diagnostic types</span></span>

<span data-ttu-id="67fdc-110">Du arbejder for en produktionsvirksomhed, og flere varer har ikke bestået kvalitetstesten.</span><span class="sxs-lookup"><span data-stu-id="67fdc-110">You work for a manufacturing company, and several items have failed quality tests.</span></span> <span data-ttu-id="67fdc-111">Disse varer flyttes ind i et karantæneområde og markeres som uoverensstemmende produkter.</span><span class="sxs-lookup"><span data-stu-id="67fdc-111">Those items are moved into a quarantine area and marked as nonconforming products.</span></span> <span data-ttu-id="67fdc-112">Der oprettes en uoverensstemmelsespost i Microsoft Dynamics 365 Supply Chain Management for at spore detaljerne gennem problemløsningen.</span><span class="sxs-lookup"><span data-stu-id="67fdc-112">A nonconformance record is created in Microsoft Dynamics 365 Supply Chain Management to track the details through issue resolution.</span></span>

<span data-ttu-id="67fdc-113">I dette tilfælde opstår der kvalitetsproblemer, fordi lejerne i den maskine, der pakker varerne, er gået i stykker og bliver overophedede.</span><span class="sxs-lookup"><span data-stu-id="67fdc-113">In this case, the quality issues are occurring because bearings in the machine that packages the items have gone bad and are overheating.</span></span> <span data-ttu-id="67fdc-114">Håndteringen af dette problem er at udskifte delene i maskinen.</span><span class="sxs-lookup"><span data-stu-id="67fdc-114">The correction for this problem is to replace the parts in the machine.</span></span>

<span data-ttu-id="67fdc-115">Når du konfigurerer diagnosticeringstyperne, kan du oprette flere poster, som hver repræsenterer en problemtype, som maskinen kan blive ramt af.</span><span class="sxs-lookup"><span data-stu-id="67fdc-115">When you configure the diagnostic types, you can create multiple records, each of which represents a different type of problem that the machine might have.</span></span> <span data-ttu-id="67fdc-116">Du kan også oprette en generel diagnosticeringstype, som repræsenterer maskinreparation.</span><span class="sxs-lookup"><span data-stu-id="67fdc-116">Alternatively, you can create one generic diagnostic type that represents machine repair.</span></span>

## <a name="create-a-diagnostic-type"></a><span data-ttu-id="67fdc-117">Oprette en diagnosticeringstype</span><span class="sxs-lookup"><span data-stu-id="67fdc-117">Create a diagnostic type</span></span>

1. <span data-ttu-id="67fdc-118">Gå til **Lagerstyring \> Opsætning \> Kvalitetsstyring \> Diagnosticeringstyper**.</span><span class="sxs-lookup"><span data-stu-id="67fdc-118">Go to **Inventory management \> Setup \> Quality management \> Diagnostic types**.</span></span>
1. <span data-ttu-id="67fdc-119">Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="67fdc-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="67fdc-120">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="67fdc-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="67fdc-121">**Diagnosticering** – Angiv et entydigt id eller navn til diagnosticeringstypen.</span><span class="sxs-lookup"><span data-stu-id="67fdc-121">**Diagnostic** – Enter a unique ID or name for the diagnostic type.</span></span>
    - <span data-ttu-id="67fdc-122">**Beskrivelse** – Indtast en detaljeret beskrivelse af diagnosticeringstypen.</span><span class="sxs-lookup"><span data-stu-id="67fdc-122">**Description** – Enter a detailed description of the diagnostic type.</span></span>

1. <span data-ttu-id="67fdc-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="67fdc-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67fdc-124">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="67fdc-124">Additional resources</span></span>

- [<span data-ttu-id="67fdc-125">Oversigt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="67fdc-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="67fdc-126">Aktivere styring af kvalitet og uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="67fdc-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="67fdc-127">Arbejdere, der er ansvarlige for godkendelse af uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="67fdc-127">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="67fdc-128">Karantænezoner for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="67fdc-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="67fdc-129">Problemtyper for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="67fdc-129">Problem types for nonconformances</span></span>](quality-problem-types.md)
- [<span data-ttu-id="67fdc-130">Kvalitetsgebyrer for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="67fdc-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="67fdc-131">Operationer for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="67fdc-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="67fdc-132">Kvalitetsstyring for lagerstedsprocesser.</span><span class="sxs-lookup"><span data-stu-id="67fdc-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
