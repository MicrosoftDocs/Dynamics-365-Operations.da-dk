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
# <a name="integrated-tax"></a>Integreret moms

[!include [banner](../includes/banner.md)]

Data vedrørende momsopsætning definerer opsætningen for både indirekte moms (moms, GST, moms) og a-skat. Det beskriver momsberegningsreglen, momssatsen, momsregnskabet, afregning og andre begreber.

## <a name="templates"></a>Skabeloner

Momsdata omfatter en samling af enhedstilknytninger, der arbejder sammen i forbindelse med datainteraktion, som vist i følgende tabel.

Finance and Operations   | Andre Dynamics 365-apps
-------------------------|---------------------------------
Momskoder                  | msdyn\_taxcodes.md
Momsgrupper               | msdyn\_taxgroups.md
Momsvaregrupper          | msdyn\_taxitemgroups.md
Momsfritagelser           | msdyn\_taxexemptcodes.md
Momsmyndigheder          | msdyn\_taxauthorities.md
Koder for indeholdt skat      | msdyn\_withholdingtaxcodes.md
Grupper for indeholdt skat   | msdyn\_withholdingtaxgroups.md
Momsfinanskontogruppe | msdyn\_taxpostinggroups  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

