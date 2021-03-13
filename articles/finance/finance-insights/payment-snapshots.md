---
title: Oversigt over snapshots (prøveversion)
description: I dette emne beskrives funktionen snapshots, hvor du kan gemme et likviditetsbudget til analyse eller sammenligning med faktiske oplysninger senere. Når du opretter et likviditetsbudget, kan du gemme det i budgettet som et "snapshot". Du kan derefter bruge disse snaphosts til at redigere de konti, der er medtaget i budgettet, eller sammenligne budgettet i snapshottet med faktiske oplysninger.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: a07749533e84cb26ce59b80e4bde12c96eaf0a3f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009337"
---
# <a name="snapshots-overview-preview"></a>Oversigt over snapshots (prøveversion)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Med Snapshots kan organisationer redigere og gemme oplysninger om deres Likviditets- og likviditetsbudgetter på et bestemt tidspunkt. Du kan sammenligne det snapshot med faktiske økonomiske værdier, undersøge variansen og bruge disse oplysninger til at forbedre likviditetsbudgetterne over tid. Mere specifikt kan snapshots bruges på følgende måder:

- Spore kasseposition og likviditetsbudgetter over tid.
- Filtrer dataene for at vise et undersæt af juridiske enheder, som snapshottet blev oprettet til.
- Rediger kontant position og likviditetsbudget, der er genereret af systemet.
- Udfør what if-analyse for at behandle optimistiske, pessimistiske og mest sandsynlige visninger af pengestrømmen.
- Sammenlign den faktiske økonomiske ydeevne med det budget, der er gemt i snapshottet.

Du kan oprette et snapshot ved at vælge **Nyt snapshot** under fanen **Likviditet** eller fanen **Likviditetsbudget** i arbejdsområdet **Likviditetsbudgetter**. Når der er oprettet et snapshot, kan indstrømningen og udstrømningerne redigeres og gemmes. Alle gemte snapshots er tilgængelige under fanen **Snapshots**. Hvis du vil åbne et snapshot, skal du vælge dets navn.

Indgående pengestrømme og udgående pengestrømme i snapshots kan altid redigeres. Når et indbetalingsbeløb eller et udgående beløb redigeres, omregnes det opdaterede beløb til de likviditetskonti, der har den oprindelige saldo. Når du er færdig med at redigere et snapshot, skal du vælge **Gem** for at gemme ændringerne.

Hvis du vil sammenligne flere snapshots, skal du vælge **Sammenlign Snapshots**. Du kan sammenligne to snapshots ad gangen. Vælg de to snapshots, der skal sammenlignes, og vælg derefter **OK**. Siden **Sammenlign snapshot** viser en sammenligning af de valgte snapshots. Diagrammet øverst på siden viser en sammenligning af indgående og udgående pengestrømme og banksaldi i de overlappende perioder mellem de to snapshots. I gitteret i den nederste sektion vises en detaljeret sammenligning af de to budgetter for hvert likviditetsbeløb. Kolonnen **Afvigelse** i gitteret viser forskellen mellem saldiene i en periode.

Hvis du vil sammenligne faktiske økonomiske resultater med et budget, der er gemt som et snapshot, skal du vælge **Sammenlign med faktiske værdier**. På siden **Sammenlign snapshot** kan du se en sammenligning af de faktiske beløb og prognosen. Diagrammet øverst på siden viser en sammenligning af indgående og udgående pengestrømme og banksaldi i de overlappende perioder mellem de to snapshots. I gitteret i den nederste sektion vises en detaljeret sammenligning af den faktiske saldo pr. periode og budgetter for hvert likviditetsbeløb. Kolonnen **Afvigelse** i gitteret viser forskellen mellem den faktiske saldo i en periode og den budgetterede saldo.

#### <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger
Forhåndsvisning (1) kan anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen (SLA) for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.
