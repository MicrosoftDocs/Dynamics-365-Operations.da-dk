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
# <a name="integrated-tax"></a>Integreret moms

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

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

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

