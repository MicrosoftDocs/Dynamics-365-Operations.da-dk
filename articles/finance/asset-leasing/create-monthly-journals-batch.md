---
title: Oprette månedlige kladdeposter i en batch
description: Dette emne forklarer, hvordan du opretter kladdeposteringer i en batch for at øge effektiviteten, når de månedlige leasingudgifter registreres.
author: moaamer
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: cd282ab04312a3ed1821160146b86db902906f3b
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714055"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a>Oprette månedlige kladdeposter i en batch

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Dette emne forklarer, hvordan du opretter kladdeposteringer i en batch for at øge effektiviteten, når de månedlige leasingudgifter registreres. Batchafvikling kan bruges til at oprette kladdeposter fra flere tidsplaner. Disse kladdeposteringer kan omfatte leasingbetalinger, passiv afskrivning, brugsretaktiv (ROU) afskrivning af aktiver og udgifter til udført omkostning. Du kan også bruge batchbehandling til at udføre den første anerkendelse af flere leasingaftaler samtidigt eller til at oprette overgangsjusteringer for flere leasingaftaler på samme tid.

Hvis du vil oprette et batchjob eller behandle betalingsfakturaer, afskrivninger eller renter for flere leasingaftaler skal du gå til **Aktivleasing \> Periodisk \> Oprettelse af batchkladde**. I den dialogboks, der vises, kan du vælge den plan, som kladdeposterne skal oprettes ud fra. Du kan også angive, om batchprocessen skal køres for bestemte enheder, leasinggrupper eller leasingkartoteker.

> [!NOTE]
> Efterfølgende posteringer, f. eks. planer for amortisering af passiver, betalinger, afskrivning og udgifter, bogføres først, når den første godkendelse af de tilsvarende leasingaftaler er bogført.
>
> Kladdeposterne oprettes, men de bogføres ikke, før du vælger kommandoen **Kør**.

Hvis du vil bogføre den oprindelige genkendelseskladde på en anden dato end for leasingens ikrafttrædelsesdato, skal du vælge **Tildeling af bogføringsdato for oprindelig godkendelse**. Feltet **Dato** vises, så du kan angive den korrekte bogføringsdato.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
