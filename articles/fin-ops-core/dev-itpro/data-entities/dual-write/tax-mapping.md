---
title: Integreret moms
description: Denne artikel beskriver integrationen af momsdata mellem Finans og drift og Dataverse.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8864a9567d57739aa72fa1859f5cfce6df33e8f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864537"
---
# <a name="integrated-tax"></a>Integreret moms

[!include [banner](../../includes/banner.md)]



Data vedrørende momsopsætning definerer opsætningen for både indirekte moms (moms, GST, moms) og a-skat. Det beskriver momsberegningsreglen, momssatsen, momsregnskabet, afregning og andre begreber.

## <a name="templates"></a>Skabeloner

Momsdata omfatter en samling af tabeltilknytninger, der arbejder sammen i forbindelse med datainteraktion, som vist i følgende tabel.

| Finans og drift-apps | Kundeengagementapps | Beskrivelse |
|-----------------------------|-----------------------------------|-------------|
[Varemomsgruppe](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Momsmyndigheder](mapping-reference.md#193) | msdyn_taxauthorities | |
[Enhed for momsfritagelseskode i CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[Momsgrupper](mapping-reference.md#195) | msdyn_taxgroups | |
[Momsfinanskonteringsgrupper V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Koder for indeholdt skat](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Grupper for indeholdt skat](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
