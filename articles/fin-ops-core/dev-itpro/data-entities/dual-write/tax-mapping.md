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
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 68461f375c6d5b04f224331dc192c921cf3c4d04
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979323"
---
# <a name="integrated-tax"></a><span data-ttu-id="9ae01-103">Integreret moms</span><span class="sxs-lookup"><span data-stu-id="9ae01-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="9ae01-104">Data vedrørende momsopsætning definerer opsætningen for både indirekte moms (moms, GST, moms) og a-skat.</span><span class="sxs-lookup"><span data-stu-id="9ae01-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="9ae01-105">Det beskriver momsberegningsreglen, momssatsen, momsregnskabet, afregning og andre begreber.</span><span class="sxs-lookup"><span data-stu-id="9ae01-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="9ae01-106">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="9ae01-106">Templates</span></span>

<span data-ttu-id="9ae01-107">Momsdata omfatter en samling af enhedstilknytninger, der arbejder sammen i forbindelse med datainteraktion, som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="9ae01-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="9ae01-108">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="9ae01-108">Finance and Operations apps</span></span> | <span data-ttu-id="9ae01-109">Modelstyrede apps i Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="9ae01-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="9ae01-110">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="9ae01-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="9ae01-111">Varemomsgruppe</span><span class="sxs-lookup"><span data-stu-id="9ae01-111">Item sales tax group</span></span> | <span data-ttu-id="9ae01-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="9ae01-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="9ae01-113">Momsmyndigheder</span><span class="sxs-lookup"><span data-stu-id="9ae01-113">Sales tax authorities</span></span> | <span data-ttu-id="9ae01-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="9ae01-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="9ae01-115">Enhed for momsfritagelseskode i CDS</span><span class="sxs-lookup"><span data-stu-id="9ae01-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="9ae01-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="9ae01-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="9ae01-117">Momsgrupper</span><span class="sxs-lookup"><span data-stu-id="9ae01-117">Sales tax groups</span></span> | <span data-ttu-id="9ae01-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="9ae01-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="9ae01-119">Momsfinanskonteringsgrupper V2</span><span class="sxs-lookup"><span data-stu-id="9ae01-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="9ae01-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="9ae01-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="9ae01-121">Koder for indeholdt skat</span><span class="sxs-lookup"><span data-stu-id="9ae01-121">Withholding tax codes</span></span> | <span data-ttu-id="9ae01-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="9ae01-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="9ae01-123">Grupper for indeholdt skat</span><span class="sxs-lookup"><span data-stu-id="9ae01-123">Withholding tax groups</span></span> | <span data-ttu-id="9ae01-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="9ae01-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

