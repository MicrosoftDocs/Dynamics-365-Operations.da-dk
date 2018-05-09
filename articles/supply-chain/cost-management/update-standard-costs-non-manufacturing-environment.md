---
title: "Opdatere standardomkostninger i et ikke-produktionsmiljø"
description: "Denne artikel indeholder vejledning i at opdatere standardomkostninger i et ikke-produktionsmiljø."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8b12e37a82e81a32b560e212fe879dbe4b114969
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a><span data-ttu-id="4a6d3-103">Opdatere standardomkostninger i et ikke-produktionsmiljø</span><span class="sxs-lookup"><span data-stu-id="4a6d3-103">Update standard costs in a non-manufacturing environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a6d3-104">Denne artikel indeholder vejledning i at opdatere standardomkostninger i et ikke-produktionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-104">This article provides guidance for updating standard costs in a non-manufacturing environment.</span></span>

<span data-ttu-id="4a6d3-105">I følgende retningslinjer antages det, at du bruger en tilgang med to versioner til at opdatere standardomkostning.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-105">The following guidelines assume that you use a two-version approach to update standard cost.</span></span> <span data-ttu-id="4a6d3-106">I denne tilgang indeholder den ene efterkalkulationsversion de standardomkostninger, der oprindeligt blev defineret for den frosne periode, og den anden efterkalkulationsversion indeholder de trinvise opdateringer.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-106">In this approach, one costing version contains the standard costs that were originally defined for the frozen period, and the second costing version contains the incremental updates.</span></span> <span data-ttu-id="4a6d3-107">De enkelte opdateringer angives som en omkostningspost i den anden efterkalkulationsversion, og den aktiveres til sidst.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-107">Each update is entered as a cost record that is enclosed in the second costing version, and eventually it's enabled.</span></span> <span data-ttu-id="4a6d3-108">Der kan også bruges en tilgang med én version, hvor der gøres brug af det sæt standardomkostninger, der oprindeligt blev defineret.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-108">An alternative, one-version approach uses the set of standard costs that was originally defined.</span></span> <span data-ttu-id="4a6d3-109">I tilgangen med to versioner skal du definere en anden efterkalkulationsversion.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-109">The two-version approach requires that you define a second costing version.</span></span> <span data-ttu-id="4a6d3-110">Her er retningslinjerne for, hvordan denne efterkalkulationsversion skal defineres:</span><span class="sxs-lookup"><span data-stu-id="4a6d3-110">Here are the guidelines for defining this costing version:</span></span>

-   <span data-ttu-id="4a6d3-111">Tildel efterkalkulationstypen **Standardomkostninger**.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-111">Assign a costing type of **Standard costs**.</span></span>
-   <span data-ttu-id="4a6d3-112">Tildel et beskrivende id, der angiver indholdet af efterkalkulationsversionen, f.eks. **2016-OPDATERINGER**.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-112">Assign a meaningful identifier that indicates the contents of the costing version, such as **2016-UPDATES**.</span></span>
-   <span data-ttu-id="4a6d3-113">Sørg for, at indholdet omfatter omkostningsposter.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-113">Make sure that the content includes cost records.</span></span>
-   <span data-ttu-id="4a6d3-114">Tillad, at der kan angives omkostningsposter for alle steder.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-114">Allow cost records to be entered for all sites.</span></span> <span data-ttu-id="4a6d3-115">Hvis du angiver et sted, kan omkostningsposter kun angives for det pågældende sted.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-115">If you specify a site, cost records can be entered only for that site.</span></span>
-   <span data-ttu-id="4a6d3-116">Angiv **Ingen** som beredskabsprincip.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-116">Indicate a fallback principle of **None**.</span></span> <span data-ttu-id="4a6d3-117">Beredskabsprincippet anvendes kun til omkostningsberegninger for producerede varer.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-117">The fallback principle applies only to cost calculations for manufactured items.</span></span>

<span data-ttu-id="4a6d3-118">Hvis du vil rette, justere eller opdatere standardomkostningerne for nye varer, skal du udføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-118">To correct, adjust, or update standard costs for new items, follow these steps.</span></span>

1.  <span data-ttu-id="4a6d3-119">Brug siden **Opsætning** **af efterkalkulationsversion** for at gøre det muligt at indtaste omkostningsdataene i den anden efterkalkulationsversion.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-119">Use the **Costing version** **setup** page to enable cost data to be entered into the second costing version.</span></span> <span data-ttu-id="4a6d3-120">Du kan vælge at forhindre aktivering af ventende omkostninger, så aktiveringen bliver tilladt, når de ventende omkostninger er fuldstændigt og korrekt defineret.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-120">Optionally, prevent the activation of pending costs, so that activation will be allowed after pending costs have been completely and accurately defined.</span></span> <span data-ttu-id="4a6d3-121">Du kan også vælge at indsætte en dato i feltet **Fra dato**.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-121">You can also optionally enter a date in the **From date** field.</span></span> <span data-ttu-id="4a6d3-122">Som en generel retningslinje kan du bruge datoen for, hvornår du regner med at aktivere de trinvise opdateringer.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-122">As a general guideline, use the date when you intend to enable the incremental updates.</span></span> <span data-ttu-id="4a6d3-123">Du kan også lade feltet **Fra dato** være tomt for efterkalkulationsversionen og derefter angive en dato i feltet **Fra dato** for de enkelte omkostningsposter.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-123">Alternatively, leave the **From date** field blank for the costing version, and then enter a date in the **From date** field for each cost record.</span></span>
2.  <span data-ttu-id="4a6d3-124">Brug siden **Varepris** til at angive opdateringer som vareomkostningsposter i den anden efterkalkulationsversion.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-124">Use the **Item price** page to enter updates as item cost records that are enclosed in the second costing version.</span></span>
3.  <span data-ttu-id="4a6d3-125">Brug rapporten **Varepriser** til at kontrollere, at vareomkostningsposterne i den anden efterkalkulationsversion er fuldstændige og nøjagtige.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-125">Use the **Item prices** report to verify the completeness and accuracy of the item cost records that are enclosed in the second costing version.</span></span>
4.  <span data-ttu-id="4a6d3-126">Brug siden **Vedligeholdelse af efterkalkulationsversion** til at skifte blokeringsflag for at tillade aktivering af ventende omkostningsposter i den anden efterkalkulationsversion.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-126">Use the **Costing version maintenance** page to change the blocking flag to allow activation of the pending cost records that are enclosed in the second costing version.</span></span>
5.  <span data-ttu-id="4a6d3-127">Brug siden **Aktivér priser** (som du kan åbne fra siden **Vedligeholdelse af efterkalkulationsversion**) til at aktivere alle ventende vareomkostningsposter, der er omfattet af den anden efterkalkulationsversion.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-127">Use the **Activate prices** page (which you open from the **Costing version maintenance** page) to activate all pending item cost records that are enclosed in the second costing version.</span></span> <span data-ttu-id="4a6d3-128">Du kan også aktivere de ventende omkostningsposter for individuelle varer ved at klikke på knappen **Aktivér afventende pris(er)** på siden **Varepris**.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-128">You can also activate the pending cost records for individual items by clicking the **Activate pending price** button on the **Item price** page.</span></span>
6.  <span data-ttu-id="4a6d3-129">Du kan undgå yderligere vedligeholdelse af data ved at bruge siden **Opsætning af efterkalkulationsversion** til at skifte blokeringsflag i den anden efterkalkulationsversion.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-129">To prevent additional data maintenance, use the **Costing version setup** page to change the blocking flags that are enclosed in the second costing version.</span></span> <span data-ttu-id="4a6d3-130">Blokeringspolitikkerne vil forhindre, at der angives nye ventende omkostninger eller aktiveres ventende omkostninger.</span><span class="sxs-lookup"><span data-stu-id="4a6d3-130">The blocking policies will prevent the entry of new pending costs and the activation of pending costs.</span></span>





