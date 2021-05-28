---
title: Karantænezoner for uoverensstemmelser
description: Dette emne beskriver, hvordan du opretter og bruger karantænezoner til uoverensstemmelser.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80f4b9dfc7882af4570bf1908784b8d114396402
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021798"
---
# <a name="quarantine-zones-for-nonconformances"></a><span data-ttu-id="ffb14-103">Karantænezoner for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="ffb14-103">Quarantine zones for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffb14-104">Dette emne beskriver, hvordan du opretter og bruger karantænezoner til uoverensstemmelser.</span><span class="sxs-lookup"><span data-stu-id="ffb14-104">This topic describes how to create and use quarantine zones for nonconformances.</span></span>

<span data-ttu-id="ffb14-105">Du kan bruge siden **Karantænezoner** til at definere de zoner, der kan tildeles til uoverensstemmelser.</span><span class="sxs-lookup"><span data-stu-id="ffb14-105">You use the **Quarantine zones** page to define zones that can be assigned to nonconformances.</span></span> <span data-ttu-id="ffb14-106">Når du opretter en uoverensstemmelse, kan du angive felterne **Karantænezone** og **Karantænetype** under fanen **Generelt** på siden **Uoverensstemmelser**.</span><span class="sxs-lookup"><span data-stu-id="ffb14-106">When you create a nonconformance, you can set the **Quarantine zone** and **Quarantine type** fields on the **General** tab of the **Non conformances** page.</span></span> <span data-ttu-id="ffb14-107">Feltet **Karantænezone** angiver typisk det område eller den lokation, hvor varen er placeret.</span><span class="sxs-lookup"><span data-stu-id="ffb14-107">The **Quarantine zone** field typically indicates the area or location where the item is located.</span></span> <span data-ttu-id="ffb14-108">Feltet **Karantænetype** definerer varen som enten *Begrænset brug* eller *Ubrugelig*.</span><span class="sxs-lookup"><span data-stu-id="ffb14-108">The **Quarantine type** field defines the item as either *Restricted usage* or *Unusable*.</span></span>

<span data-ttu-id="ffb14-109">Når du udskriver en uoverensstemmelses- eller korrektionsrapport for en uoverensstemmelse, kan du få vist karantænezonen, hvor varen er placeret.</span><span class="sxs-lookup"><span data-stu-id="ffb14-109">When you print a nonconformance or corrections report for a nonconformance, you can view the quarantine zone where the item is located.</span></span>

<span data-ttu-id="ffb14-110">Du kan også udskrive et uoverensstemmelsesmærkat for en uoverensstemmelse.</span><span class="sxs-lookup"><span data-stu-id="ffb14-110">You can also print a nonconformance tag for a nonconformance.</span></span> <span data-ttu-id="ffb14-111">Denne rapport viser den tildelte karantænezone og oplysninger om brugen for at vejlede om, hvordan defekt materiale skal håndteres.</span><span class="sxs-lookup"><span data-stu-id="ffb14-111">This report shows the assigned quarantine zone and information about usage to provide guidance about how defective material should be handled.</span></span> <span data-ttu-id="ffb14-112">Karatænezonerne kan svare til lagerlokationer eller operationsressourcer.</span><span class="sxs-lookup"><span data-stu-id="ffb14-112">The quarantine zones might correspond to inventory locations or operations resources.</span></span>

## <a name="examples-of-quarantine-zones"></a><span data-ttu-id="ffb14-113">Eksempler på karantænezoner</span><span class="sxs-lookup"><span data-stu-id="ffb14-113">Examples of quarantine zones</span></span>

### <a name="example-1"></a><span data-ttu-id="ffb14-114">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="ffb14-114">Example 1</span></span>

<span data-ttu-id="ffb14-115">Du arbejder i en virksomhed, der producerer og distribuerer tv, højttalere og medieafspillere.</span><span class="sxs-lookup"><span data-stu-id="ffb14-115">You work at an electronics manufacturing company that produces and distributes televisions, speakers, and media players.</span></span> <span data-ttu-id="ffb14-116">I dette tilfælde kan du konfigurere en karantænezone, der repræsenterer hver produkttype.</span><span class="sxs-lookup"><span data-stu-id="ffb14-116">In this case, you can configure a quarantine zone to represent each type of product.</span></span>

### <a name="example-2"></a><span data-ttu-id="ffb14-117">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="ffb14-117">Example 2</span></span>

<span data-ttu-id="ffb14-118">Tre beholdere og to reoler bruges til opbevaring af varer, der ikke opfylder kravene.</span><span class="sxs-lookup"><span data-stu-id="ffb14-118">Three bins and two racks are used to store items that are nonconforming.</span></span> <span data-ttu-id="ffb14-119">I dette tilfælde kan du konfigurere fem karantænezoner, én for hver beholder og hver reol.</span><span class="sxs-lookup"><span data-stu-id="ffb14-119">In this case, you can configure five quarantine zones, one for each bin and each rack.</span></span>

## <a name="create-a-quarantine-zone"></a><span data-ttu-id="ffb14-120">Oprette en ny karantænezone</span><span class="sxs-lookup"><span data-stu-id="ffb14-120">Create a quarantine zone</span></span>

1. <span data-ttu-id="ffb14-121">Gå til **Lagerstyring \> Opsætning \> Kvalitetsstyring \> Karantænezoner**.</span><span class="sxs-lookup"><span data-stu-id="ffb14-121">Go to **Inventory management \> Setup \> Quality management \> Quarantine zones**.</span></span>
1. <span data-ttu-id="ffb14-122">Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="ffb14-122">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="ffb14-123">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="ffb14-123">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="ffb14-124">**Karantænezone** – Angiv et entydigt id eller navn til karantænezonen.</span><span class="sxs-lookup"><span data-stu-id="ffb14-124">**Quarantine zone** – Enter a unique ID or name for the quarantine zone.</span></span>
    - <span data-ttu-id="ffb14-125">**Beskrivelse** – Indtast en detaljeret beskrivelse af karantænezonen.</span><span class="sxs-lookup"><span data-stu-id="ffb14-125">**Description** – Enter a detailed description of the quarantine zone.</span></span>

1. <span data-ttu-id="ffb14-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ffb14-126">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ffb14-127">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ffb14-127">Additional resources</span></span>

- [<span data-ttu-id="ffb14-128">Oversigt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="ffb14-128">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="ffb14-129">Aktivere styring af kvalitet og uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="ffb14-129">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="ffb14-130">Arbejdere, der er ansvarlige for godkendelse af uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="ffb14-130">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="ffb14-131">Problemtyper for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="ffb14-131">Problem types for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="ffb14-132">Diagnosticeringstyper for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="ffb14-132">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="ffb14-133">Kvalitetsgebyrer for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="ffb14-133">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="ffb14-134">Operationer for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="ffb14-134">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="ffb14-135">Kvalitetsstyring for lagerstedsprocesser.</span><span class="sxs-lookup"><span data-stu-id="ffb14-135">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
