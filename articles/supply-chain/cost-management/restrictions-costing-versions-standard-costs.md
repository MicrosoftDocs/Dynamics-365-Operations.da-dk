---
title: "Begrænsninger for en efterkalkulationsversioner for standardkostpriser"
description: "I dette emne beskrives de begrænsninger, der gælder for en efterkalkulationsversion for standardkostpriser."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e14d5d11e987d2dbc841f86c39fc7e94864144d3
ms.openlocfilehash: 658575492597eed91509561f4710f07e271c53c8
ms.contentlocale: da-dk
ms.lasthandoff: 01/17/2018

---


#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="a7efb-103">Begrænsninger for en efterkalkulationsversioner for standardkostpriser</span><span class="sxs-lookup"><span data-stu-id="a7efb-103">Restrictions on costing versions for standard costs</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a7efb-104">I dette emne beskrives de begrænsninger, der gælder for en efterkalkulationsversion for standardkostpriser.</span><span class="sxs-lookup"><span data-stu-id="a7efb-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="a7efb-105">Følgende begrænsninger hjælper med til at sikre, at standardefterkalkulationsprincipperne overholdes:</span><span class="sxs-lookup"><span data-stu-id="a7efb-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="a7efb-106">Gebyrer skal inkluderes i varens omkostninger.</span><span class="sxs-lookup"><span data-stu-id="a7efb-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="a7efb-107">Gebyrerne for en produceret vare afspejler de amortiserede konstante omkostninger på styklisten og ruteoplysninger.</span><span class="sxs-lookup"><span data-stu-id="a7efb-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="a7efb-108">Derfor skal gebyrerne inkluderes i enhedsomkostningen.</span><span class="sxs-lookup"><span data-stu-id="a7efb-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="a7efb-109">Gebyrerne for en købt vare medtages også i varens enhedsomkostning.</span><span class="sxs-lookup"><span data-stu-id="a7efb-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="a7efb-110">Beregningen af standardkostpriser for produceret varer skal baseres på kostprisposter i en efterkalkulationsversion for standardkostpriser.</span><span class="sxs-lookup"><span data-stu-id="a7efb-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="a7efb-111">Der kan kun bruges alternative kostprisdata i en efterkalkulationsversion for planlagte omkostninger, f.eks. indkøbsprisaftaler for købte varer.</span><span class="sxs-lookup"><span data-stu-id="a7efb-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="a7efb-112">Alternative kostprisdata defineres af styklisteberegningsgruppen.</span><span class="sxs-lookup"><span data-stu-id="a7efb-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="a7efb-113">Styklisteberegninger skal udføres med udfoldning på enkeltniveau.</span><span class="sxs-lookup"><span data-stu-id="a7efb-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="a7efb-114">Oplysninger om varens kostpris for standardkostpriser kan kopieres til andre efterkalkulationsversioner, som indeholder standardkostpriser eller planlagte omkostninger.</span><span class="sxs-lookup"><span data-stu-id="a7efb-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="a7efb-115">Oplysninger om varekostpriser for planlagte omkostninger kan dog ikke kopieres til en efterkalkulationsversion, der indeholder standardkostpriser, da den begrænsning, der vises tidligere i dette emne, ikke ville kunne anvendes på planlagte omkostninger.</span><span class="sxs-lookup"><span data-stu-id="a7efb-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

<a name="related-topics"></a><span data-ttu-id="a7efb-116">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="a7efb-116">Related topics</span></span>
--------

[<span data-ttu-id="a7efb-117">Efterkalkulationsversioner</span><span class="sxs-lookup"><span data-stu-id="a7efb-117">Costing versions</span></span>](costing-versions.md)

[<span data-ttu-id="a7efb-118">Opdatere standardomkostninger i et ikke-produktionsmiljø</span><span class="sxs-lookup"><span data-stu-id="a7efb-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="a7efb-119">Forberede at vedligeholde standardomkostninger for producerede varer</span><span class="sxs-lookup"><span data-stu-id="a7efb-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)


