---
title: Gøre forudsigelsesmodellen bedre (prøveversion)
description: I dette emne beskrives funktioner, som du kan bruge til at forbedre ydeevnen i forudsigelsesmodeller.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/28/2020
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 2bcdea4a2a8f4386b274077cd1e95398fb6fac37
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009362"
---
# <a name="improve-the-prediction-model-preview"></a>Gøre forudsigelsesmodellen bedre (prøveversion)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

I dette emne beskrives funktioner, som du kan bruge til at forbedre ydeevnen i forudsigelsesmodeller. Du begynder at forbedre din model i arbejdsområdet **Forudsigelser om debitorbetalinger** i Microsoft Dynamics 365 Finance. Forbedringstrinene afsluttes derefter i AI Builder.

## <a name="select-historical-outcomes"></a>Vælge historiske resultater

Du skal først vælge en eller flere af de tre mulige udfald for fakturaer: **Til tiden**, **Sent** og **Meget sent**. Du skal vælge alle tre resultater. Hvis du fjerner markeringen af udfaldet, filtreres fakturaer ud af uddannelsesprocessen, og nøjagtigheden af prognosen reduceres.

[![Bekræfte udfald](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)

Hvis din organisation kun kræver to udfald, skal du ændre tærsklen **Sent** og **Meget sent** til 0 (nul) dage. På denne måde kan du effektivt skjule forudsigelsen til en binær tilstand for **Til tiden** eller **Sent**.

## <a name="select-fields"></a>Vælg felter

Når du vælger felter, der skal medtages i modellen, skal du være opmærksom på, at listen indeholder alle tilgængelige felter i den Microsoft Dataverse-tabel, der er knyttet til data i Azure Data Lake. Nogle af disse felter skal **ikke** markeres. De felter, der ikke skal vælges, falder i en af tre kategorier:

- Feltet er obligatorisk for Dataverse-tabellen, men der er ingen sikkerhedskopi af data i Data Lake.
- Feltet er et id og giver derfor ikke mening for en maskinel indlæringsfunktion.
- Feltet viser oplysninger, der ikke vil være tilgængelige i forbindelse med forudsigelse.

Følgende afsnit viser de felter, der er tilgængelige for faktura- og kundeenhederne, og viser de felter, der **ikke** skal vælges til uddannelse. Den kategori, der er angivet for hvert af disse felter, refererer til kategorierne på den foregående liste.
 
### <a name="invoice-dataverse-table"></a>Dataverse-fakturatabel

Følgende illustration viser de felter, der er tilgængelige til fakturatabellen.

[![Tilgængelige felter til fakturatabellen](./media/available-fields.png)](./media/available-fields.png)

Følgende felter skal ikke vælges til oplæring:

- **Fakturakonto** (kategori 2)
- **Er lukket** (kategori 3) – Dette felt bruges til at filtrere fakturaer for uddannelse (lukket) og forudsigelse (ikke lukket).
- **Navn** (kategori 1)
- **Kilde-id** (kategori 2)
- **Kilde-post** (kategori 2)
- **Kildetabel** (kategori 2)

### <a name="customer-dataverse-table"></a>Dataverse-kundetabel

Følgende illustration viser de felter, der er tilgængelige til kundetabellen.

[![Tilgængelige felter til kundetabellen](./media/related-entities.png)](./media/related-entities.png)

Følgende felt skal ikke vælges til oplæring:

- **Nøgle for entydig række** (kategori 2)

## <a name="filters"></a>Filtre

Filtrene understøtter i øjeblikket ikke scenariet med debitorbetalingsprognoser. Du kan derfor vælge **Spring dette trin over**, og fortsæt til oversigtssiden.

[![Fokusmodel med filtre](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)

#### <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger
Forhåndsvisning (1) kan anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen (SLA) for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.
