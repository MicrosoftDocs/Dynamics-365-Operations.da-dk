---
title: Oprette dimensioner og importere dimensionsmedlemmer
description: Driftsregnskab er et uafhængigt modul, der kræver masterdata fra andre moduler.
author: ShylaThompson
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3eedce9cd092f9c299a2381a28a801351f15c4cc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226383"
---
# <a name="create-dimensions-and-import-dimension-members"></a><span data-ttu-id="105dd-103">Oprette dimensioner og importere dimensionsmedlemmer</span><span class="sxs-lookup"><span data-stu-id="105dd-103">Create dimensions and import dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="105dd-104">Driftsregnskab er et uafhængigt modul, der kræver data fra andre moduler.</span><span class="sxs-lookup"><span data-stu-id="105dd-104">Cost accounting is an independent module that requires data from other modules.</span></span> <span data-ttu-id="105dd-105">Disse data er kategoriseret som følgende:</span><span class="sxs-lookup"><span data-stu-id="105dd-105">This data is categorized into the following:</span></span>

-  <span data-ttu-id="105dd-106">Omkostningselementer</span><span class="sxs-lookup"><span data-stu-id="105dd-106">Cost elements</span></span>
-  <span data-ttu-id="105dd-107">Omkostningsobjekter</span><span class="sxs-lookup"><span data-stu-id="105dd-107">Cost objects</span></span>
-  <span data-ttu-id="105dd-108">Statistiske dimensioner</span><span class="sxs-lookup"><span data-stu-id="105dd-108">Statistical dimensions</span></span>

<span data-ttu-id="105dd-109">Et **omkostningselement** svarer til et omkostningsrelevant element i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="105dd-109">A **Cost element** corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="105dd-110">Et **omkostningsobjekt** svarer til alle typer økonomiske dimensioner, f.eks. produkter, bærere og projekter, du vil vurdere, allokere omkostninger til eller måle direkte.</span><span class="sxs-lookup"><span data-stu-id="105dd-110">A **Cost object** corresponds to any type of financial dimension, such as products, cost centers, and projects that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="105dd-111">En **statistisk dimension** og dens medlemmer bruges til registrering af ikke-pengemæssige poster.</span><span class="sxs-lookup"><span data-stu-id="105dd-111">A **Statistical dimension** and its members are used to register non-monetary entries.</span></span> <span data-ttu-id="105dd-112">Statistiske dimensionsmedlemmer kan bruges som fordelingsbasis i omkostningsdistribution og omkostningsfordeling.</span><span class="sxs-lookup"><span data-stu-id="105dd-112">Statistical dimension members can be used as an allocation base in cost distribution and allocation</span></span> 

<span data-ttu-id="105dd-113">I følgende diagram illustreres de dimensioner, der bruges i forbindelse med driftsregnskab.</span><span class="sxs-lookup"><span data-stu-id="105dd-113">The following diagram illustrates the dimensions that are used in Cost accounting.</span></span>

<span data-ttu-id="105dd-114">[![Dimensioner for omkostningsregnskab](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="105dd-114">[![Cost accounting dimensions](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span></span>

<span data-ttu-id="105dd-115">Når dataene importeres til driftsregnskab, kan du bruge dem til at oprette forskellige perspektiver, der giver indsigt for ledere på alle niveauer i organisationen.</span><span class="sxs-lookup"><span data-stu-id="105dd-115">After the data is imported into Cost accounting, you can use it to build various perspectives that provide insights to managers at all levels of the organization.</span></span> <span data-ttu-id="105dd-116">Følgende emner indeholder oplysninger om oprettelse af dimensioner og import af dimensionsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="105dd-116">The following topics provide information about creating dimensions and importing dimension members.</span></span> 

-  [<span data-ttu-id="105dd-117">Dimensioner for omkostningselement</span><span class="sxs-lookup"><span data-stu-id="105dd-117">Cost element dimensions</span></span>](cost-elements.md)
-  [<span data-ttu-id="105dd-118">Oprette omkostningselementer</span><span class="sxs-lookup"><span data-stu-id="105dd-118">Create cost elements</span></span>](./tasks/create-cost-elements.md)
-  [<span data-ttu-id="105dd-119">Dimensioner for omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="105dd-119">Cost object dimensions</span></span>](cost-objects.md)
-  [<span data-ttu-id="105dd-120">Knytte dimensionsmedlemmer for omkostningselement til et fælles sæt dimensionsmedlemmer</span><span class="sxs-lookup"><span data-stu-id="105dd-120">Map cost element dimension members to a common set of dimension members</span></span>](map-cost-elements-dimension-members.md)
-  [<span data-ttu-id="105dd-121">Tilknytte en dimension for omkostningselement</span><span class="sxs-lookup"><span data-stu-id="105dd-121">Map a cost element dimension</span></span>](./tasks/map-cost-element-dimension.md)
-  [<span data-ttu-id="105dd-122">Skabeloner for statistiske dimensionsmedlemmer og providere af statistiske målinger</span><span class="sxs-lookup"><span data-stu-id="105dd-122">Statistical dimension members and statistical measure provider templates</span></span>](statistical-measure-provider-template.md)








[!INCLUDE[footer-include](../../includes/footer-banner.md)]