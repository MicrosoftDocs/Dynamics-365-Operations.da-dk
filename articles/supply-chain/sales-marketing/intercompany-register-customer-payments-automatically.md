---
title: Registrere betalinger for interne debitorfakturaer automatisk
description: Denne artikel forklarer registrering af betalinger for interne debitorfakturaer automatisk
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4e8f784cd310026f0a647a0f509999e11ab26ce5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878781"
---
# <a name="register-payments-automatically-for-intercompany-customer-invoices"></a>Registrere betalinger for interne debitorfakturaer automatisk

[!include [banner](../../includes/banner.md)]

I Microsoft Dynamics 365 Supply Chain Management oprettes en debitorpostering, når en intern debitorfaktura bogføres. Denne debitorpostering bliver ved med at være åben, indtil den udlignes, hvilket betyder, at den betales. Når den tilsvarende interne indkøbsordre opdateres i form af en faktura, oprettes der en kreditorpostering svarende til debitorposteringen. Denne kreditorpostering er også åben, indtil den udlignes. Hvis risikoen for differencer skal reduceres, kan der automatisk oprettes og bogføres en debitorbetalingskladde, når kreditorbetalingskladden bogføres.

1. Gå til **Salg og marketing \> Kunder \> Alle kunder**.
1. I handlingsruden skal du under fanen **Generelt** vælge **Intern**.
1. Hvis du vil konfigurere interne debitorbetalinger på siden **Intern handel** for salgsordrer, skal du vælge linket **Til politikker for salgsordrer**.
1. Vælg den debitorbetalingskladde, som du vil registrere interne kreditorbetalinger på, i feltet **Betalingskladde**. Du kan angive dette på siden **Debitorparametre**.
1. Hvis du vil bogføre automatisk til denne kladde, skal du markere afkrydsningsfeltet **Bogfør kladde automatisk**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
