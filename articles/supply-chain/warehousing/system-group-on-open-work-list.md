---
title: Systemgruppering på en åben opgaveliste
description: Dette emne beskriver, hvordan du filtrerer oversigten over åbne opgaver på en mobilenhed.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a4faa358fc598859bf3b226b48b57594317f37d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831092"
---
# <a name="system-grouping-on-an-open-work-list"></a>Systemgruppering på en åben opgaveliste

[!include [banner](../includes/banner.md)]

Ved hjælp af et felt til systemgruppering kan du filtrere en oversigt over åbne opgaver uden at skulle redigere menupunktet for mobilenheden.
Hvis det er relevant, fungerer systemgruppering til filtrering af en opgaveliste på et enkelt felt med opgaveoverskrift. Du kan ikke bruge systemgruppering til at filtrere online feltniveauer.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Konfigurere systemgruppering på en oversigt over åbent arbejde
Brug disse trin til at konfigurere systemgruppering på en oversigt over åbent arbejde.

-   Vælg et menupunkt på en mobilenhed, vælg **Tilstand: indirekte** og **Aktivitetskode: Vis oversigt over åbent arbejde**. Følgende valgmuligheder bliver tilgængelige. Disse indstillinger er påkrævet for systemgruppering på en oversigt over åbent arbejde. 

|        Indstilling         |                                                                                                                                                                                                                                                                         Beskrivelse                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tillad systemgruppering |                                                                                                                                                                                                                                                 Aktiverer systemgruppering for et valgt menupunkt på arbejdslisten.                                                                                                                                                                                                                                                  |
| Systemgrupperingsfelt | Kun tilgængelig, hvis <strong>Tillad systemarbejde</strong> er angivet til <strong>Ja</strong>. Markér det felt, der bestemmer, hvordan plukkearbejde grupperes for arbejdere. Hvis du f.eks. vælger feltet <strong>ShipmentId</strong>, scanner arbejderen forsendelses-id for at gruppere plukkearbejdet. Alt arbejde for forsendelsen knyttes derefter til arbejderen. Dette felt kræver, at du opretter et menupunkt, der bruger eksisterende arbejde, der er grupperet af systemet. Brug feltet <strong>Systemgrupperingslabel</strong> til at informere arbejderen, hvad der skal scannes. |
| Systemgrupperingslabel |                       Kun tilgængelig, hvis <strong>Tillad systemarbejde</strong> er angivet til <strong>Ja</strong>. Angiv oplysninger arbejderen om, hvad der skal scannes, når plukkearbejde er grupperet. Hvis du f.eks. bruger feltet <strong>ShipmentId</strong> til at gruppere plukkearbejde efter forsendelse, kan du skrive Forsendelses-id i feltet. Dette felt kræver, at du opretter et menupunkt, der bruger eksisterende arbejde, der er grupperet af systemet. Du skal også vælge det felt, der skal grupperes efter, i feltet <strong>Systemgruppering</strong>.                       |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]