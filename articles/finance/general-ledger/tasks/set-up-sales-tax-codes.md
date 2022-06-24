---
title: Konfigurer momskoder
description: Denne artikel beskriver, hvordan du konfigurerer koder for moms i Dynamics 365 Finance.
author: twheeloc
ms.date: 09/27/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b12133583f40cc17cb85f6dbd86697592af25caf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858462"
---
# <a name="set-up-sales-tax-codes"></a>Konfigurer momskoder

[!include [banner](../../includes/banner.md)]

Denne artikel beskriver, hvordan du konfigurerer momskoder. Momskoder oprettes til enhver indirekte moms eller afgift, som den juridiske enhed er forpligtet til at beregne, opkræve og betale til momsmyndighederne.

Denne opgave bruger demofirmaet USMF.

1. Gå til **Navigationsrude > Skat > Indirekte skatter > Moms > Momskoder**.
2. Vælg **Ny**.
3. Skrive en værdi i feltet **Momskode**.
4. Skriv en værdi i feltet **Navn**.
5. Vælg en **Afregningsperiode** ved at åbne rullelisten for at angive, hvilken momsmyndighed og i hvilke intervaller denne moms skal rapporteres og betales.
6. Vælg en **Finanskonteringsgruppe** for at angive de hovedkonti, der skal bogføres moms til finans på.
7. Udvid oversigtspanelet **Beregning**. Dette omfatter flere felter, der styrer, hvordan momsbeløb beregnes. Udfyld disse felter efter behov.  
8. I **Handlingsruden** øverst på grænsefladen skal du vælge **Momskode**.
9. Vælg **Værdier**.
10. Angiv værdien for denne momskode i kolonnen **værdi**.

    Værdien i oversigtspanelet **Beregning** i feltet **Oprindelig** bliver ganget med antallet på transaktionen, der skal beregnes momsbeløbet, hvis **beløb pr. enhed** er markeret.  Hvis momskoden ikke er en enhed baseret skat, er værdien en procentdel, der er anvendt på oprindelsen for denne momskode til beregning af sales tax-beløbet.     

11. Vælg **Gem**.
12. Luk siden.
13. Vælg **Gem**.

Fra og med Microsoft Dynamics 365 Finance version 10.0.22, hvis du bruger [Momsservice](../../localizations/global-tax-calcuation-service-overview.md), og funktionen [**Understøttelse af flere momsregistreringsnumre**](../../localizations/emea-multiple-vat-registration-numbers.md) er aktivere i arbejdsområdet **Funktionsområdet**, kan du bruge **Momstype**-feltet til at angive momskodetype. Følgende værdier er tilgængelige:

- Standardmoms
- Reduceret moms
- MOMS 0 %
- Afgifter
- Andet

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
