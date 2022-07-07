---
title: Bogføringsmetoder for udskydelse
description: Denne artikel beskriver forskellene mellem metoderne for udskudt bogføring af indtægter og udgifter ved abonnementsfakturering.
author: JodiChristiansen
ms.date: 6/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: c66ed1c38251140dd798c39797873ceb5f7121a4
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9019092"
---
# <a name="deferral-posting-methods"></a>Bogføringsmetoder for udskydelse

Denne artikel beskriver forskellene mellem metoderne for udskudt bogføring af indtægter og udgifter ved abonnementsfakturering.

På siden **Udskydelsesparameter til indtægter og udgifter** er indstillingerne til bogføringsmetoder for udskydelse **Drift** og **Balance**. Eksemplet i denne artikel hjælper med at forklare forskellene mellem de to metoder og årsagerne til, at du bruger den ene metode eller den anden.

Metoden **Balance** bruger kun to konti. Derfor er der mindre opsætning. Metoden **Drift** har to yderligere konti, **Første indregning** og **Føringsmodkonto**, til omsætning, rabatter og omkostninger afhængigt af transaktionstypen. Disse konti konfigureres på siden **Udskydelsesstandarder** (**Fakturering af abonnement \> Udskydelser af indtægter og udgifter \> Konfiguration**). Selvom eksemplet er fokuseret på udskudte indtægter, kan samme koncept anvendes til udskudte rabatter og udskudte omkostninger.

## <a name="example"></a>Eksempel

Salgsfaktura 1 har et totalbeløb af $3.000 og har udskudt indtægt. I følgende tabeller vises fordelingerne, når denne salgsfaktura bogføres.

**Balancemetode**

| Type | Konto | Debet | Kredit|
|---|---|---|---|
| Debet | Debitor | 3.000,00 | |
| Kredit | Udskudt indtægt | | 3.000,00 |

**Driftsmetode**

| Type | Konto | Debet | Kredit |
|---|---|---|---|
| Debet | Debitor | 3.000,00 | |
| Debet | Indtægtsføringsmodkonto | 3.000,00 | |
| Kredit | Udskudt indtægt | | 3.000,00 |
| Kredit | Startindtægtsføring | | 3.000,00 |

Salgsfaktura 2 har et totalbeløb af $2.000 og har ingen udskudt indtægt.

| Type | Konto | Antal |
|---|---|---|
| Debet | Debitor | 3.000,00 |
| Kredit | Indtægter | 3.000,00 |

**Balancemetodetotaler for salgsfaktura 1 og 2 i kombination**

| Konto | Debet | Kredit |
|---|---|---|
| Debitor | 5.000,00 | |
| Indtægter | | 2.000,00 |
| Udskudt indtægt | | 3.000,00 |

Når metoden **Balance** bruges, er det ikke så let at se bruttoindtægten for en periode. Noget af indtægten bogføres på kontoen **Udskudt indtægt**. Husk på, at når indtægt føres hver periode, er der flere debiteringer og krediteringer på kontoen **Udskudt indtægt**. Bruttoindtægt for en given periode blandes med input/output af indtægtsføringen.

**Driftsmetodetotaler for salgsfaktura 1 og 2 i kombination**

| Konto | Debet | Kredit |
|---|---|---|
| Debitor | 5.000,00 | |
| Indtægter | | 5.000,00 |
| Indtægtsmodkonto | 3.000,00 | |
| Udskudt indtægt | | 3.000,00 |

Al indtægt går til driftskontoen **Indtægter**. Derefter flyttes den udskudte indtægt fra driftsopgørelsen til balancen. Du kan nemt se bruttoindtægten, da alt bogføres på kontoen **Indtægter**. Noget af denne bruttoindtægt er dog udskudt. Den flyttes derfor til kontoen **Udskudt indtægt** og bogføres senere.

I metoden **Drift** kan du se på kontoen **Indtægt** og **Indtægtsmodkonto** for at se bruttoindtægt på $5.000 og nettoindtægt (netto af udskudt) på $2.000. Selvom **Drift**-metoden kan gøre det nemmere at rapportere, er der flere konti, der skal konfigureres.
