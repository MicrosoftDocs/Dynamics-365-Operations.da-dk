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
ms.openlocfilehash: a4da37d45698290b40f6c72148f1500bef72127a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173079"
---
# <a name="integrated-tax"></a><span data-ttu-id="185e1-103">Integreret moms</span><span class="sxs-lookup"><span data-stu-id="185e1-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="185e1-104">Data vedrørende momsopsætning definerer opsætningen for både indirekte moms (moms, GST, moms) og a-skat.</span><span class="sxs-lookup"><span data-stu-id="185e1-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="185e1-105">Det beskriver momsberegningsreglen, momssatsen, momsregnskabet, afregning og andre begreber.</span><span class="sxs-lookup"><span data-stu-id="185e1-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="185e1-106">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="185e1-106">Templates</span></span>

<span data-ttu-id="185e1-107">Momsdata omfatter en samling af enhedstilknytninger, der arbejder sammen i forbindelse med datainteraktion, som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="185e1-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="185e1-108">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="185e1-108">Finance and Operations apps</span></span> | <span data-ttu-id="185e1-109">Modelstyrede apps i Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="185e1-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="185e1-110">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="185e1-110">Description</span></span> |
-------------------------|---------------------------------
<span data-ttu-id="185e1-111">Momskoder</span><span class="sxs-lookup"><span data-stu-id="185e1-111">Tax codes</span></span>                   | <span data-ttu-id="185e1-112">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="185e1-112">msdyn\_taxcodes.md</span></span> | 
<span data-ttu-id="185e1-113">Momsgrupper</span><span class="sxs-lookup"><span data-stu-id="185e1-113">Tax groups</span></span>                 | <span data-ttu-id="185e1-114">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="185e1-114">msdyn\_taxgroups.md</span></span> | 
<span data-ttu-id="185e1-115">Momsvaregrupper</span><span class="sxs-lookup"><span data-stu-id="185e1-115">Tax item groups</span></span>             | <span data-ttu-id="185e1-116">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="185e1-116">msdyn\_taxitemgroups.md</span></span> | 
<span data-ttu-id="185e1-117">Momsfritagelser</span><span class="sxs-lookup"><span data-stu-id="185e1-117">Tax Exemptions</span></span>             | <span data-ttu-id="185e1-118">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="185e1-118">msdyn\_taxexemptcodes.md</span></span> | 
<span data-ttu-id="185e1-119">Momsmyndigheder</span><span class="sxs-lookup"><span data-stu-id="185e1-119">Tax Authorities</span></span>             | <span data-ttu-id="185e1-120">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="185e1-120">msdyn\_taxauthorities.md</span></span> | 
<span data-ttu-id="185e1-121">Koder for indeholdt skat</span><span class="sxs-lookup"><span data-stu-id="185e1-121">Withholding tax codes</span></span>       | <span data-ttu-id="185e1-122">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="185e1-122">msdyn\_withholdingtaxcodes.md</span></span> | 
<span data-ttu-id="185e1-123">Grupper for indeholdt skat</span><span class="sxs-lookup"><span data-stu-id="185e1-123">Withholding tax groups</span></span>     | <span data-ttu-id="185e1-124">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="185e1-124">msdyn\_withholdingtaxgroups.md</span></span> | 
<span data-ttu-id="185e1-125">Momsfinanskontogruppe</span><span class="sxs-lookup"><span data-stu-id="185e1-125">Tax Ledger Account Group</span></span> | <span data-ttu-id="185e1-126">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="185e1-126">msdyn\_taxpostinggroups</span></span>     | 

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

