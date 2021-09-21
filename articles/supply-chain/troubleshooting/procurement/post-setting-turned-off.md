---
title: Indstillingen Vil du bogføre på omkostningskontoen i finans er ikke aktiveret
description: Dette problem opstår, når en indkøbsordre faktureres, hvis indstillingen 'Bogfør på omkostningskontoen i finans' er aktiveret under fanen 'Faktura' på siden 'Kreditorparametre'
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 592444958dad4624fdc9098dc58df0a2e49e63de
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475924"
---
# <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>Indstillingen Vil du bogføre på omkostningskontoen i finans er ikke aktiveret

## <a name="symptoms"></a>Symptomer

Dette problem opstår, når en indkøbsordre faktureres, hvis indstillingen **Vil du bogføre på omkostningskontoen i finans?** er angivet til *Ja* under fanen **Faktura** på siden **Kreditorparametre**.

## <a name="reproduce-the-issue"></a>Genskabe problemet

Følgende procedurer viser en måde at genskabe problemet på.

1. Gå til **Kreditor \> Opsætning \> Kreditorparametre**.
1. Under fanen **Faktura** skal du angive **Vil du bogføre på omkostningskontoen i finans?** til *Ja*.
1. Gå til **Lagerstyring \> Konfiguration \> Bogføring \> Bogføring**.
1. Under fanen **Indkøbsordre** skal du sikre dig, at du har slettet alle linjerne i købsudgiften for produktet.
1. Gå til **Kreditor \> Indkøbsordrer \> Alle indkøbsordrer**.
1. Oprette en indkøbsordre. Vælg **1001 ACME kontorartikler** i feltet *Kreditorkonto*.
1. Tilføj en indkøbsordrelinje, der har følgende indstillinger:

    - **Varenummer:** *D0011 laserprojektor*
    - **Lokation:** *1*
    - **Lagersted:** *11*
    - **Antal:** *4*

1. Vælg **Bekræft** i gruppen **Handling** under fanen **Indkøb** i handlingsruden.
1. Gå til handlingsruden, og vælg **Produktkvittering** i gruppen **Generér** under fanen **Modtag**.
1. Angiv et vilkårligt nummer i feltet **Produktkvittering** i dialogboksen **Konterer produktkvittering**, og vælg derefter **OK**.
1. Vælg **Faktura** i gruppen **Generér** under fanen **Faktura** i handlingsruden.
1. Angiv et vilkårligt nummer som fakturanummer i feltet **Nummer**.
1. Opdater status for sammenholdelse, og bogfør.
1. Bemærk, at du nu får vist følgende fejl, når du opretter en faktura ud fra en indkøbsordre: "Kontonummer for konteringstypen Indkøbsudgifter for produkt findes ikke".

## <a name="resolution"></a>Løsning

Dette afhænger af parameterindstillingerne for fakturaer og fakturagrupper. Du kan finde flere oplysninger i følgende blogindlæg: [Regnskabsføring for indkøbstillæg og lagervariation](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).
