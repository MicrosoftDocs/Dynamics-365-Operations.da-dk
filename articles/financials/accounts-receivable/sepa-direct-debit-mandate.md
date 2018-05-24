---
title: Oprette bemyndigelse til SEPA Direct Debit
description: "En direkte SEPA-debitering (fælles eurobetalingsområde (SEPA)) gør det muligt for en kreditor at indsamle midler fra en debitors bankkonto, forudsat at debitoren er tildelt en signeret bemyndigelse til kreditor."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 242d6d3d517ad5190b96ace36bd585a5769ae994
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-sepa-direct-debit-mandate"></a>Oprette bemyndigelse til SEPA Direct Debit

[!include [banner](../includes/banner.md)]

En direkte SEPA-debitering (fælles eurobetalingsområde (SEPA)) gør det muligt for en kreditor at indsamle midler fra en debitors bankkonto, forudsat at debitoren er tildelt en signeret bemyndigelse til kreditor. Den bemyndigelse, som debitor underskriver, giver kreditoren tilladelse til at opkræve en betaling og beder kundens bank om at betale opkrævningen. Dette emne er organiseret til at vise processen til oprettelse af SEPA-bemyndigelser til direkte debitering.

## <a name="prerequisites"></a>Forudsætninger
Følgende tabel viser de forudsætninger, der skal være på plads, før du starter.

| Kategori       | Forudsætning                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Land/område | Den primære adresse for den juridiske enhed skal være i de følgende lande: Østrig, Belgien, Tyskland, Spanien, Frankrig, Italien eller Nederlandene. |

1. Opret en nummerserie til bemyndigelser til direkte debitering. Hver bemyndigelse til direkte debitering skal have et entydigt nummer. Brug siden **Nummerserier** til at oprette en nummerserie for bemyndigelser til direkte debitering. Du skal bruge denne identifikator til at tildele nummerserien til systemet til bemyndigelser til direkte debitering på siden **Debitorparametre**.

2. Angiv debitorparametre for bemyndigelser til direkte debitering: Brug siden **Debitorparametre** til at konfigurere parametre for bemyndigelser til direkte debitering. For at angive parametrene under fanen **Direct Debit** skal du ændre standardparametrene efter behov. Under fanen **Nummerserier** skal du derefter opdatere feltet **Id for bemyndigelse til Direct Debit** med den nummerserie, du har angivet tidligere.

3. Konfigurer en betalingsmåde for bemyndigelser til direkte debitering. Du skal angive en betalingsmåde for bemyndigelser til direkte debitering. Du kan bruge denne betalingsmåde til at forespørge om fakturaer, der skal genereres direkte debetbetalinger for. Brug siden **Betalingsmetode** til at konfigurere betalingsmetoden. Hvis du vil konfigurere en betalingsmetode for bemyndigelse af direkte debitering, skal du følge følgende fremgangsmåde for en betalingsmetode:

-   I feltet **Betalingstype** skal du vælge **Elektronisk betaling**.
-   Valgfrit: Hvis du forventer, at hver af dine kunder skal have flere bemyndigelser, skal du i feltet **Periode** vælge **Faktura**. Der oprettes en separat betaling for hver faktura, og hver betaling bruger den bemyndigelse, der er angivet for fakturaen.
-   Vælg indstillingen **Kræv bemyndigelse** for at oprette betalinger ved hjælp af bemyndigelser til direkte debitering. Indstillingen **Kræv bemyndigelse** er kun tilgængelig, hvis du vælger **Elektronisk betaling** i feltet **Betalingstype**.

Yderligere ressourcer

[Oversigt over direkte debitering](sepa-direct-debit-overview.md) 

[Oprette en ny bemyndigelse til direkte debitering til en debitor](tasks/create-direct-debit-mandate-customer.md) 


