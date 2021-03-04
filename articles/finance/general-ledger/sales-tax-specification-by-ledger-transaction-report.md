---
title: Momsspecifikation pr. finanstransaktionsrapport
description: Dette emne forklarer, hvordan du kan bruge rapporten Momsspecifikation pr. finanstransaktion til at se og udskrive oplysninger om finanstransaktioner, der er beregnet moms for.
author: ericwang
manager: Ann Beebe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 438a640124e778b839c660f5e161efa22c319af0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441411"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a>Momsspecifikation pr. finanstransaktionsrapport
[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du kan bruge rapporten **Momsspecifikation pr. finanstransaktion** til at se og udskrive oplysninger om finanstransaktioner, der er beregnet moms for.

## <a name="tax-accounts-vs-non-tax-accounts"></a>Momskonti versus ikke-momskonti

Rapporten **Momsspecifikation efter finanstransaktion** viser momstransaktioner for både momskonti og ikke-momskonti. Disse konti kategoriseres på følgende måde:

- **Momskonto** – En konto betragtes som en momskonto, når der bogføres en momstransaktion, og hovedkontoen på **Moms**-kladdelinjen er en momskonto, f.eks. en konto for udgående moms eller en indgående momskonto.
- **Ikke-momskonto** – En konto betragtes som en ikke-momskonto, når der bogføres en momstransaktion, og hovedkontoen på den oprindelige transaktion er en ikke-momskonto, f.eks. en indtægtskonto eller en udgiftskonto.

For momskonti viser kolonnerne **Original**, **Indgående moms** og **Udgående moms** i rapporten **0** (nul). I forbindelse med ikke-momskonti viser disse kolonner beløb.

## <a name="filtering-the-data-on-the-report"></a>Filtrering af dataene i rapporten

Når du opretter rapporten, er følgende standardfelter tilgængelige. Du kan bruge disse felter til at filtrere de data, der vises i rapporten.

| Felt                      | Beskrivelse |
|----------------------------|-------------|
| Dato                       | Brug felterne i sektionerne **Fra** og **Til** til at definere et datointerval for momstransaktionerne. |
| Hovedkonto               | Brug felterne i sektionerne **Fra** og **Til** til at definere et interval af hovedkonti. |
| Momskode             | Brug felterne i sektionerne **Fra** og **Til** til at definere et interval af momskoder. |
| Gruppering                   | Vælg, om rapporten skal grupperes efter finanskonto eller momskode. |
| Subtotal efter momskode | Angiv denne indstilling til **Ja** for at få vist subtotaler efter momskode. |
| Kun totaler                | Angiv denne indstilling til **Ja** for kun at få vist totaler. |
| Kun hovedkonti         | Angiv denne indstilling til **Ja** for kun at medtage hovedkonti i rapporten. |

## <a name="showing-only-non-tax-accounts-on-the-report"></a>Visning af ikke-momskonti i rapporten

Hvis du kun vil have vist ikke-momskonti i rapporten, skal du konfigurere en filterbetingelse, f.eks. en stjerne (\*), som vist i følgende illustration.

![Rapport, der viser ikke-momskonti](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]