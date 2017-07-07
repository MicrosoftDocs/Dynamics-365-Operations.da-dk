---
title: "Systemgruppering på en åben opgaveliste"
description: "Dette emne beskriver, hvordan du filtrerer oversigten over åbne opgaver på en mobilenhed."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: dbf0e49b1156c54cd37bbbe57ca564cdbc45fb2d
ms.contentlocale: da-dk
ms.lasthandoff: 06/20/2017


---

# <a name="system-grouping-on-an-open-work-list"></a>Systemgruppering på en åben opgaveliste

[!include[banner](../includes/banner.md)]

Ved hjælp af et felt til systemgruppering kan du filtrere en oversigt over åbne opgaver uden at skulle redigere menupunktet for mobilenheden.
Hvis det er relevant, fungerer systemgruppering til filtrering af en opgaveliste på et enkelt felt med opgaveoverskrift. Du kan ikke bruge systemgruppering til at filtrere online feltniveauer.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Konfigurere systemgruppering på en oversigt over åbent arbejde
Brug disse trin til at konfigurere systemgruppering på en oversigt over åbent arbejde.

-   Vælg et menupunkt på en mobilenhed, vælg **Tilstand: indirekte** og **Aktivitetskode: Vis oversigt over åbent arbejde**. Følgende valgmuligheder bliver tilgængelige. Disse indstillinger er påkrævet for systemgruppering på en oversigt over åbent arbejde. 

| Indstilling        | Betegnelse   | 
| ------------- | ------------- |
| Tillad systemgruppering   | Aktiverer systemgruppering for et valgt menupunkt på arbejdslisten.| 
| Systemgrupperingsfelt   | Kun tilgængelig, hvis **Tillad systemarbejde** er angivet til **Ja**. Markér det felt, der bestemmer, hvordan plukkearbejde grupperes for arbejdere. Hvis du f.eks. vælger feltet **ShipmentId**, scanner arbejderen forsendelses-id for at gruppere plukkearbejdet. Alt arbejde for forsendelsen knyttes derefter til arbejderen. Dette felt kræver, at du opretter et menupunkt, der bruger eksisterende arbejde, der er grupperet af systemet. Brug feltet **Systemgrupperingslabel** til at informere arbejderen, hvad der skal scannes. |
| Systemgrupperingslabel   | Kun tilgængelig, hvis **Tillad systemarbejde** er angivet til **Ja**. Angiv oplysninger arbejderen om, hvad der skal scannes, når plukkearbejde er grupperet. Hvis du f.eks. bruger feltet **ShipmentId** til at gruppere plukkearbejde efter forsendelse, kan du skrive Forsendelses-id i feltet. Dette felt kræver, at du opretter et menupunkt, der bruger eksisterende arbejde, der er grupperet af systemet. Du skal også vælge det felt, der skal grupperes efter, i feltet **Systemgruppering**.|

