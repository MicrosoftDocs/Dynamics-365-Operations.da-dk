---
title: Omkostningsposter
description: Denne artikel indeholder oplysninger om omkostningsposter, og hvornår de er oprettet. En omkostningspost er en post, der registrerer antallet og omkostningen for en given hændelse.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3116f9fd2d1fe6a0967b114a069f495cea6217a1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424295"
---
# <a name="cost-entries"></a>Omkostningsposter

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om omkostningsposter, og hvornår de er oprettet. En omkostningspost er en post, der registrerer antallet og omkostningen for en given hændelse.

Omkostningsposter er akkumuleringer af lagertransaktioner, der er registreret på aktive økonomiske lagerdimensioner.

## <a name="examples"></a>Eksempler
### <a name="example-1-no-cost-entries-are-created"></a>Eksempel 1: Der er ikke oprettet omkostningsposter

Der er registreret en overførselsjournalhændelse. Hændelsen overfører et eksemplar af vare A fra lokalitet A til lokalitet B. Lagerdimensionens lokalitet betragtes ikke som en del af omkostningsobjektet. Hændelsen opretter derfor to lagerposteringer og ingen omkostningsposter.

### <a name="example-2-cost-entries-are-created"></a>Eksempel 2: Der er oprettet omkostningsposter

Der er registreret en overførselsjournalhændelse. Hændelsen overfører ét eksemplar af vare A fra websted 1 til websted 2. Lagerdimensionen for lokationen betragtes som en del af omkostningsobjektet. Hændelsen opretter derfor to lagerposteringer og to omkostningsposter.

### <a name="example-3-one-cost-entry-is-created"></a>Eksempel 3: Der oprettes én omkostningspost

Hændelsens produktkvittering registreres for en indkøbsordre. Hændelsen registrerer 100 styk af vare A til en enhedsomkostning på 10,00 amerikanske dollar (USD). Da vare A bruger et serienummer til at spore formålet med lagerstyring, oprettes der et entydigt serienummer for hver vare, der modtages. Hændelsen opretter derfor 100 lagerposteringer og én omkostningspost.

## <a name="cost-entries-page"></a>Siden Omkostningsposter
På den nye side **Omkostningsposter** kan du få vist og styre registreringer af mængder og omkostninger. Siden supplerer siderne **Lagertransaktion** og **Lagerudligning**. Poster registreres i kronologisk rækkefølge for en hændelse. Derfor kan du hurtigt finde og styre de akkumulerede omkostninger for en bestemt hændelse eller alle hændelser, der er relateret til et dokument. Her er et eksempel:

-   En produktkvitteringshændelsen er registreret for vare A. Et hundrede stykker er modtaget til en enhedskostpris på USD 10,00.
-   Et par dage efter, at fakturahændelsen er registreret, stiger omkostningen til 11,00 USD. Det samlede beløb er derfor 1.100 USD. Der oprettes endnu et bilag for at tage højde for forskellen på 100 USD.
-   Et par dage senere registreres et tillæg på 15,00 USD til dækning af transportomkostningerne på indkøbsordren.

| Bilag | Dato       | Reference      | Tal | Parti-id  | Mængde | Beløb  |
|---------|------------|----------------|--------|---------|---------------|----|
| 00001   | 01-01-2015 | Indkøbsordre | 100001 | 0000101 | 100,00   | 1000.00 |
| 00002   | 20-01-2015 | Indkøbsordre | 100001 | 0000101 |          | 100,00  |
| 00003   | 31-01-2015 | Tilpasning     | 100001 | 0000101 |          | 15,00   |

Siden **Omkostningsposter** gør det muligt at filtrere efter dokument-id og dokumentdato. 

> [!NOTE]
> Omkostningsposter er kun tilgængelige for [omkostningsobjekter](cost-object.md) eller frigivne produkter.

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Omkostningsobjekter](cost-object.md)



