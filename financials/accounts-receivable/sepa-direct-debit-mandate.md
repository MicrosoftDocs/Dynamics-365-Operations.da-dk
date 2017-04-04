---
title: Konfigurere SEPA-bemyndigelse til direkte debitering.
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: bb835f8dad16938b56365c7b06d4a0228f9aba66
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-sepa-direct-debit-mandate"></a>Konfigurere SEPA-bemyndigelse til direkte debitering.



En direkte SEPA-debitering (fælles eurobetalingsområde (SEPA)) gør det muligt for en kreditor at indsamle midler fra en debitors bankkonto, forudsat at debitoren er tildelt en signeret bemyndigelse til kreditor. Den bemyndigelse, som debitor underskriver, giver kreditoren tilladelse til at opkræve en betaling og beder kundens bank om at betale opkrævningen. Dette emne er organiseret til at vise processen til oprettelse af SEPA direkte debitering mandater.

## <a name="prerequisites"></a>Forudsætninger
Følgende tabel viser de forudsætninger, der skal være på plads, før du starter.

| Kategori       | Forudsætning                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Land/område | Den primære adresse for den juridiske enhed skal være i de følgende lande: Østrig, Belgien, Tyskland, Spanien, Frankrig, Italien eller Nederlandene. |

1. Oprette en nummerserie til direkte debitering mandater hvert direkte debitering mandat skal have et entydigt nummer. Brug siden **Nummerserier** til at oprette en nummerserie for bemyndigelser til direkte debitering. Du skal bruge denne identifikator til at tildele nummerserien til systemet til bemyndigelser til direkte debitering på siden **Debitorparametre**.

2. Angive debitorparametre for direkte debitering mandater brugen af **Accounts receivable parameters** side til at konfigurere parametre for direkte debitering mandater. Til at angive parametrene, på den **direkte debitering** fanen, ændre standardparametrene, som du har brug for. Derefter på den **nummerserier** fanen, opdatere den **direkte debet mandat ID** med den nummerserie, du har angivet tidligere.

3. Oprette en betalingsmåde for direkte debitering sikrer, at du skal konfigurere en betalingsmåde for direkte debitering mandater. Du kan bruge denne betalingsmåde til at forespørge om fakturaer, der skal genereres direkte debetbetalinger for. Brug siden **Betalingsmetode** til at konfigurere betalingsmetoden. Hvis du vil konfigurere en betalingsmetode for bemyndigelse af direkte debitering, skal du følge følgende fremgangsmåde for en betalingsmetode:

-   I feltet **Betalingstype** skal du vælge **Elektronisk betaling**.
-   Valgfrit: Hvis du forventer, at alle dine kunder skal have flere bemyndiger, i den **periode** vælge **faktura**. Der oprettes en separat betaling for hver faktura, og hver betaling vil bruge det mandat, der er angivet på fakturaen.
-   Vælg indstillingen **Kræv bemyndigelse** for at oprette betalinger ved hjælp af bemyndigelser til direkte debitering. Indstillingen **Kræv bemyndigelse** er kun tilgængelig, hvis du vælger **Elektronisk betaling** i feltet **Betalingstype**.

Se også [direkte debitering oversigt](sepa-direct-debit-overview.md) 

