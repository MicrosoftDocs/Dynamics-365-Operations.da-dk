---
title: Integreret moms
description: I dette emne beskrives integrationen af momsdata mellem Finance and Operations og Common Data Service.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 86e74086a5a74c7af5f2572d1a653a1658d729c0
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853853"
---
# <a name="integrated-tax"></a><span data-ttu-id="fb841-103">Integreret moms</span><span class="sxs-lookup"><span data-stu-id="fb841-103">Integrated tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb841-104">Data vedrørende momsopsætning definerer opsætningen for både indirekte moms (moms, GST, moms) og a-skat.</span><span class="sxs-lookup"><span data-stu-id="fb841-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="fb841-105">Det beskriver momsberegningsreglen, momssatsen, momsregnskabet, afregning og andre begreber.</span><span class="sxs-lookup"><span data-stu-id="fb841-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="fb841-106">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="fb841-106">Templates</span></span>

<span data-ttu-id="fb841-107">Momsdata omfatter en samling af enhedstilknytninger, der arbejder sammen i forbindelse med datainteraktion, som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="fb841-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="fb841-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fb841-108">Finance and Operations</span></span>   | <span data-ttu-id="fb841-109">Andre Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="fb841-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="fb841-110">Momskoder</span><span class="sxs-lookup"><span data-stu-id="fb841-110">Tax codes</span></span>                  | <span data-ttu-id="fb841-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="fb841-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="fb841-112">Momsgrupper</span><span class="sxs-lookup"><span data-stu-id="fb841-112">Tax groups</span></span>               | <span data-ttu-id="fb841-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="fb841-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="fb841-114">Momsvaregrupper</span><span class="sxs-lookup"><span data-stu-id="fb841-114">Tax item groups</span></span>          | <span data-ttu-id="fb841-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="fb841-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="fb841-116">Momsfritagelser</span><span class="sxs-lookup"><span data-stu-id="fb841-116">Tax Exemptions</span></span>           | <span data-ttu-id="fb841-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="fb841-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="fb841-118">Momsmyndigheder</span><span class="sxs-lookup"><span data-stu-id="fb841-118">Tax Authorities</span></span>          | <span data-ttu-id="fb841-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="fb841-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="fb841-120">Koder for indeholdt skat</span><span class="sxs-lookup"><span data-stu-id="fb841-120">Withholding tax codes</span></span>      | <span data-ttu-id="fb841-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="fb841-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="fb841-122">Grupper for indeholdt skat</span><span class="sxs-lookup"><span data-stu-id="fb841-122">Withholding tax groups</span></span>   | <span data-ttu-id="fb841-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="fb841-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="fb841-124">Momsfinanskontogruppe</span><span class="sxs-lookup"><span data-stu-id="fb841-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="fb841-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="fb841-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

