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
ms.openlocfilehash: 0d32a5f7859f0200da823a73d94b9a6b2a9c8e7d
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019696"
---
# <a name="integrated-tax"></a><span data-ttu-id="27091-103">Integreret moms</span><span class="sxs-lookup"><span data-stu-id="27091-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="27091-104">Data vedrørende momsopsætning definerer opsætningen for både indirekte moms (moms, GST, moms) og a-skat.</span><span class="sxs-lookup"><span data-stu-id="27091-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="27091-105">Det beskriver momsberegningsreglen, momssatsen, momsregnskabet, afregning og andre begreber.</span><span class="sxs-lookup"><span data-stu-id="27091-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="27091-106">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="27091-106">Templates</span></span>

<span data-ttu-id="27091-107">Momsdata omfatter en samling af enhedstilknytninger, der arbejder sammen i forbindelse med datainteraktion, som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="27091-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="27091-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27091-108">Finance and Operations</span></span>   | <span data-ttu-id="27091-109">Andre Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="27091-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="27091-110">Momskoder</span><span class="sxs-lookup"><span data-stu-id="27091-110">Tax codes</span></span>                  | <span data-ttu-id="27091-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="27091-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="27091-112">Momsgrupper</span><span class="sxs-lookup"><span data-stu-id="27091-112">Tax groups</span></span>               | <span data-ttu-id="27091-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="27091-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="27091-114">Momsvaregrupper</span><span class="sxs-lookup"><span data-stu-id="27091-114">Tax item groups</span></span>          | <span data-ttu-id="27091-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="27091-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="27091-116">Momsfritagelser</span><span class="sxs-lookup"><span data-stu-id="27091-116">Tax Exemptions</span></span>           | <span data-ttu-id="27091-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="27091-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="27091-118">Momsmyndigheder</span><span class="sxs-lookup"><span data-stu-id="27091-118">Tax Authorities</span></span>          | <span data-ttu-id="27091-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="27091-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="27091-120">Koder for indeholdt skat</span><span class="sxs-lookup"><span data-stu-id="27091-120">Withholding tax codes</span></span>      | <span data-ttu-id="27091-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="27091-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="27091-122">Grupper for indeholdt skat</span><span class="sxs-lookup"><span data-stu-id="27091-122">Withholding tax groups</span></span>   | <span data-ttu-id="27091-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="27091-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="27091-124">Momsfinanskontogruppe</span><span class="sxs-lookup"><span data-stu-id="27091-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="27091-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="27091-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

