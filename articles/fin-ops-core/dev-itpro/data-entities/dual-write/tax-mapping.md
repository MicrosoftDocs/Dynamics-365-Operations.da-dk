---
title: Integreret moms
description: I dette emne beskrives integrationen af momsdata mellem Finance and Operations og Dataverse.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 14c22dd6602b5fbf866c8dc6b057f6c8acb1f48f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679290"
---
# <a name="integrated-tax"></a>Integreret moms

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Data vedrørende momsopsætning definerer opsætningen for både indirekte moms (moms, GST, moms) og a-skat. Det beskriver momsberegningsreglen, momssatsen, momsregnskabet, afregning og andre begreber.

## <a name="templates"></a>Skabeloner

Momsdata omfatter en samling af tabeltilknytninger, der arbejder sammen i forbindelse med datainteraktion, som vist i følgende tabel.

Finance and Operations-apps | Modelstyrede apps i Dynamics 365 | Beskrivende tekst |
-------------------------|---------------------------------|----|
Varemomsgruppe | msdyn_taxitemgroups |
Momsmyndigheder | msdyn_taxauthorities |
Enhed for momsfritagelseskode i CDS | msdyn_taxexemptcodes |
Momsgrupper | msdyn_taxgroups |
Momsfinanskonteringsgrupper V2 | msdyn_taxpostinggroups |
Koder for indeholdt skat | msdyn_withholdingtaxcodes |
Grupper for indeholdt skat | msdyn_withholdingtaxgroups | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]