---
title: Konfigurere momskoder
description: Dette emne beskriver, hvordan du konfigurerer koder for moms i Dynamics 365 Finance.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f5ce2c8d9a117871191dd1c2d32d822bcc72d76fabaec146d9b8c27fc85dc058
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719192"
---
# <a name="set-up-sales-tax-codes"></a>Konfigurere momskoder

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan du konfigurerer momskoder. Momskoder oprettes til enhver indirekte moms eller afgift, som den juridiske enhed er forpligtet til at beregne, opkræve og betale til momsmyndighederne.

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
    - Hvis beløb pr. enhed er markeret, bliver værdien i oversigtspanelet **Beregning** i feltet Grundlag ganget med antallet på transaktionen, der skal beregnes momsbeløbet.  Hvis momskoden ikke er en enhed baseret skat, er værdien en procentdel, der er anvendt på oprindelsen for denne momskode til beregning af sales tax-beløbet.     
11. Vælg **Gem**.
12. Luk siden.
13. Vælg **Gem**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]