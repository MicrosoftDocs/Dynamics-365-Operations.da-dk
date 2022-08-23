---
title: Integreret moms
description: Denne artikel beskriver integrationen af momsdata mellem finans og drift og Dataverse.
author: josaw
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8f148b710e2294edf1e402b9b8b22cb24e60a1f2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288788"
---
# <a name="integrated-tax"></a>Integreret moms

[!include [banner](../../includes/banner.md)]



Data vedrørende momsopsætning definerer opsætningen for både indirekte moms (moms, GST, moms) og a-skat. Det beskriver momsberegningsreglen, momssatsen, momsregnskabet, afregning og andre begreber.

## <a name="templates"></a>Skabeloner

Momsdata omfatter en samling af tabeltilknytninger, der arbejder sammen i forbindelse med datainteraktion, som vist i følgende tabel.

| Programmer til finans og drift | Kundeengagementapps | Beskrivende tekst |
|-----------------------------|-----------------------------------|-------------|
[Varemomsgruppe](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Momsmyndigheder](mapping-reference.md#193) | msdyn_taxauthorities | |
[Enhed for momsfritagelseskode i CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[Momsgrupper](mapping-reference.md#195) | msdyn_taxgroups | |
[Momsfinanskonteringsgrupper V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Koder for indeholdt skat](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Grupper for indeholdt skat](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

