---
title: Opdatere overførselsbudgettet efter reduktioner i indkøbsordrer og fakturaer
description: Denne artikel beskriver, hvordan du kan styre, hvad der sker med overførselsbudgettet, når indkøbsordrer annulleres eller reduceres, og når fakturaer reduceres.
author: TaylorVH
ms.date: 02/11/2022
ms.topic: article
ms.search.form: LedgerFund
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-savanh
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2022-02-01
ms.openlocfilehash: 7f0ef0ffdf697609e811f754b4378b1f7a81c494
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897952"
---
# <a name="update-the-carry-forward-budget-after-reductions-in-purchase-orders-and-invoices"></a>Opdatere overførselsbudgettet efter reduktioner i indkøbsordrer og fakturaer

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Denne artikel beskriver, hvordan du kan styre, hvad der sker med overførselsbudgettet, når indkøbsordrer annulleres eller reduceres, og når fakturaer reduceres.

Du kan finde oplysninger om, hvordan indkøbsordrer behandles ved årsafslutning, i [Behandle indkøbsordrer ved årsafslutning](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end).

## <a name="turn-carry-forward-budget-reductions-for-invoice-variances-on-or-off"></a>Slå reduktioner i overførselsbudgettet for fakturaafvigelser til og fra

Systemet kan altid opdatere overførselsbudgettet, når en indkøbsordre annulleres eller reduceres. Hvis du vil opdatere overførselsbudgettet, når en faktura reduceres, skal du dog aktivere funktionen *Reducer overført budget, når en faktura mod en indkøbsordre reduceres med en afvigelse*. Administratorer kan aktivere eller deaktivere denne funktion ved at søge efter den i arbejdsområdet **[Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)**.

## <a name="purchase-order-reductions-and-cancellations"></a>Reduktioner og annulleringer af indkøbsordrer

Uanset om funktionen *Reducer overført budget, når en faktura mod en indkøbsordre reduceres med en afvigelse* er aktiveret, opdateres det overførte budget, når en kvalificerende indkøbsordre annulleres eller reduceres. Du kan indstille hver finansieringskilde til reagere på en af følgende måder:

- Bevar det overførte budget, som det blev oprettet.
- Juster automatisk det overførte budget for at fjerne det annullerede eller reducerede beløb.

Kun indkøbsordrelinjer med fordelinger, der omfatter en finansieringskilde, er tilgængelige til automatisk budgetregulering. Den automatiske budgetregulering finder sted, når indkøbsordren er færdig, eller en reduktion i en indkøbsordre bekræftes.

## <a name="invoice-reductions"></a>Fakturareduktioner

Når funktionen *Reducer overført budget, når en faktura mod en indkøbsordre reduceres med en afvigelse* er aktiveret, kan du angive, om hver finansieringskilde skal reducere det overførte budget, når en faktura reduceres, i tillæg til når en indkøbsordre annulleres eller reduceres. Fakturaen skal være for en indkøbsordre, der har et overført budget. Reduktioner omfatter prisafvigelser, gebyrafvigelser og momsafvigelser. Når en overført indkøbsordre reduceres under fakturering, oprettes der en afvigelse. Når fakturaen bogføres, reduceres behæftelsen af indkøbsordren med beløbet i afvigelsen. Funktionen opretter også den automatiske budgetregulering for beløbet i afvigelsen.

Når funktionen *Reducer overført budget, når en faktura mod en indkøbsordre reduceres med en afvigelse* er slået til, reduceres det overførte budget ikke i dette scenarie. Derfor vil det resterende overførte budget for beløbet i afvigelsen blive efterladt.

## <a name="configure-the-carry-forward-budget-options-for-each-fund"></a>Konfigurere indstillingerne for det overførte budget for hver finansieringskilde

Benyt følgende fremgangsmåde for hver finansieringskilde i finans, der skal kunne reducere det overførte budget, når en indkøbsordre eller faktura reduceres.

1. Gå til **Finans \> Kontoplan \> Finansieringskilder \> Finansieringskilder**.
1. Vælg den finansieringskilde, du vil konfigurere.
1. Under **Proces for indkøbsordrers årsafslutning** skal du kontrollere, at indstillingen **Tilsidesæt valgte ultimoindstilling** er angivet til *Ja*.
1. Under **Status for overført budget** skal du angive feltet **Genindfør budgettet, når en overført indkøbsordre annulleres eller reduceres** efter behov. Indstillingerne har lidt forskellige virkninger, afhængigt af om *Reducer overført budget, når en faktura mod en indkøbsordre reduceres med en afvigelse* er aktiveret i systemet.

    - Når funktionen er deaktiveret, reagerer systemet kun på annullerede eller reducerede indkøbsordrer. Indstillingerne fungerer på følgende måde:

        - *Nej* – Systemet opretter en budgetregisterpost for den resterende saldo i indkøbsordrer, der er blevet annulleret eller reduceret.
        - *Ja* – Systemet tillader, at indkøbsordrer annulleres eller reduceres, men der oprettes ikke en budgetregisterpost. Det overførte budget er stadig tilgængeligt for forbrug i andre dokumenter.

    - Når funktionen er aktiveret, reagerer systemet både på fakturaafvigelser og annullerede eller reducerede indkøbsordrer. Indstillingerne fungerer på følgende måde:

        - *Nej* – I forbindelse med fakturaafvigelser opretter systemet en budgetregisterpost på indkøbsordren for afvigelsesreduktionsbeløbet. For annullerede eller reducerede indkøbsordrer har denne indstilling samme effekt, som når funktionen deaktiveres.
        - *Ja* – I forbindelse med fakturaafvigelser tillader systemet fakturareduktionen, men opretter ikke en budgetregisterpost. Det overførte budget er stadig tilgængeligt for forbrug i andre dokumenter. For annullerede eller reducerede indkøbsordrer har denne indstilling samme effekt, som når funktionen deaktiveres.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Behandle indkøbsordrer ved årsafslutning](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end)
- [Vedligehold generelle budgetreservationer](general-budget-reservation-tasks.md)
- [Midler i den offentlige sektor](funds-public-sector.md)
- [Konfigurere en finansieringskilde i den offentlige sektor](tasks/set-up-fund-public-sector.md)
