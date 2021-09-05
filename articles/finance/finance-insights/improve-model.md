---
title: Forbedre forudsigelsesmodellen
description: I dette emne beskrives funktioner, som du kan bruge til at forbedre ydeevnen i forudsigelsesmodeller.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: de753eda43cb358dfa9edc76f102d4b268291b4e
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386432"
---
# <a name="improve-the-prediction-model"></a>Forbedre forudsigelsesmodellen

[!include [banner](../includes/banner.md)]

I dette emne beskrives funktioner, som du kan bruge til at forbedre ydeevnen i forudsigelsesmodeller. Du begynder at forbedre din model i arbejdsområdet **Forudsigelser om debitorbetalinger** i Microsoft Dynamics 365 Finance. Forbedringstrinene afsluttes derefter i AI Builder.

## <a name="select-historical-outcomes"></a>Vælge historiske resultater

Du skal først vælge en eller flere af de tre mulige udfald for fakturaer: **Til tiden**, **Sent** og **Meget sent**. Du skal vælge alle tre resultater. Hvis du fjerner markeringen af udfaldet, filtreres fakturaer ud af uddannelsesprocessen, og nøjagtigheden af prognosen reduceres.

[![Bekræfte udfald.](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)

Hvis din organisation kun kræver to udfald, skal du ændre tærsklen **Sent** og **Meget sent** til 0 (nul) dage. På denne måde kan du effektivt skjule forudsigelsen til en binær tilstand for **Til tiden** eller **Sent**.

## <a name="select-fields"></a>Vælg felter

Når du vælger felter, der skal medtages i modellen, skal du være opmærksom på, at listen indeholder alle tilgængelige felter i den Microsoft Dataverse-tabel, der er knyttet til data i Azure Data Lake. Nogle af disse felter skal **ikke** markeres. De felter, der ikke skal vælges, falder i en af tre kategorier:

- Feltet er obligatorisk for Dataverse-tabellen, men der er ingen sikkerhedskopi af data i Data Lake.
- Feltet er et id og giver derfor ikke mening for en maskinel indlæringsfunktion.
- Feltet viser oplysninger, der ikke vil være tilgængelige i forbindelse med forudsigelse.

Følgende afsnit viser de felter, der er tilgængelige for faktura- og kundeenhederne, og viser de felter, der **ikke** skal vælges til uddannelse. Den kategori, der er angivet for hvert af disse felter, refererer til kategorierne på den foregående liste.
 
### <a name="invoice-dataverse-table"></a>Dataverse-fakturatabel

Følgende illustration viser de felter, der er tilgængelige til fakturatabellen.

[![Tilgængelige felter til fakturatabellen.](./media/available-fields.png)](./media/available-fields.png)

Følgende felter skal ikke vælges til oplæring:

- **Fakturakonto** (kategori 2)
- **Er lukket** (kategori 3) – Dette felt bruges til at filtrere fakturaer for uddannelse (lukket) og forudsigelse (ikke lukket).
- **Navn** (kategori 1)
- **Kilde-id** (kategori 2)
- **Kilde-post** (kategori 2)
- **Kildetabel** (kategori 2)

### <a name="customer-dataverse-table"></a>Dataverse-kundetabel

Følgende illustration viser de felter, der er tilgængelige til kundetabellen.

[![Tilgængelige felter til kundetabellen.](./media/related-entities.png)](./media/related-entities.png)

Følgende felt skal ikke vælges til oplæring:

- **Nøgle for entydig række** (kategori 2)

## <a name="filters"></a>Filtre

Du kan filtrere de fakturaer, der bruges til kurser, ved at angive filtreringskriterier for felter på fakturaen eller i kundetabellerne. Du kan for eksempel angive en grænseværdi, så den kun medtager fakturaer, hvor totalen er lig med eller overstiger et bestemt beløb. Du kan også udelukke fakturaer, der er knyttet til kunder i en bestemt kundegruppe.

Du kan finde flere oplysninger om filtrering af dataene under [Oprette en forudsigelsesmodel](https://docs.microsoft.com/ai-builder/prediction-create-model#filter-your-data).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
