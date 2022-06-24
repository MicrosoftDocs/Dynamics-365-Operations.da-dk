---
title: Konti til automatisk posteringer
description: Denne artikel forklarer, hvordan konti til automatiske posteringer bruges til bogføring via Microsoft Dynamics 365, og indeholder eksempler på nøglekonti til automatiske posteringer.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74e72840fea1f5d89c908b00e2cf572bce6befbe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880753"
---
# <a name="accounts-for-automatic-transactions"></a>Konti til automatisk posteringer

Siden **Konti til automatiske posteringer** (**Finans &gt; Opsætning af posteringer &gt; Konti til automatiske transaktioner**) bruges til at definere den standardhovedkonto, der bruges til hver bogføringstype i systemet. Selvom de fleste bogføringstyper kan konfigureres på en modulspecifik eller funktionsspecifik side, kan nogle bogføringstyper kun konfigureres på siden **Konti til automatiske posteringer**.

Du kan f.eks. angive den hovedkonto, der bruges til posteringstypen **Debitorsaldo**, i feltet **Oversigt** på siden **Debitorposteringsprofil** og bruge en anden hovedkonto til hver debitorprofil. På den måde har du mere detaljeret styring med posteringerne. Du kan derimod kun angive fejlkontoen på siden **Konti til automatiske posteringer**.

Når du åbner siden **Konti til automatiske posteringer** i en ny juridisk enhed, er kontolisten tom. Du kan tilføje de mest almindelige bogføringstyper, der skal konfigureres på siden, ved at vælge knappen **Opret standardtyper**. Derefter kan du for hver række vælge hovedkontoen i feltet **Hovedkonto**. Hvis du lader feltet **Hovedkonto** være tomt for en bogføringstype, og du ikke har konfigureret en hovedkonto på en modulspecifik eller funktionsspecifik side, modtager du en fejlmeddelelse, når du bogfører en postering, der bruger bogføringstypen. Meddelelsen vil typisk være "Kontoen til \[bogføringstype\] findes ikke".

## <a name="default-posting-types"></a>Standardbogføringstyper

I tabellen nedenfor vises eksempler på de standardbogføringstyper, der oprettes, når du vælger **Opret standardtyper** på siden **Konti til automatiske posteringer**. Den viser eksempler på hovedkonti og beskrivelser. Kolonnen "Debet/Kredit?" angiver, om posteringen typisk bogfører et debet- eller kreditbeløb. I nogle tilfælde kan en postering enten bogføre et debet- eller et kreditbeløb. I kolonnen "Clearingkonto" angives, om bogføringstypen er en clearingkonto. Hvis bogføringstypen er en clearingkonto, bliver det beløb, der bogføres på kontoen, automatisk tilbageført, når en senere transaktion bogføres.

| Bogføringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | Beskrivelse |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Øredifference i rapporteringsvaluta | 618160 | Diverse udgifter | Udgift | Begge | Nej | Denne bogføringstype bruges, hvis der indtræffer en øredifference, når et posteringsbeløb i en fremmed valuta omregnes til rapporteringsvalutaen. |
| Øredifference i regnskabsvaluta | 618160 | Diverse udgifter | Udgift | Begge | Nej | Denne bogføringstype bruges, hvis der indtræffer en øredifference, når et posteringsbeløb i en fremmed valuta omregnes til regnskabsvalutaen. |
| Fejlkonto | 999999 | Fejlkonto | Udgift | Begge | Nej | Denne bogføringstype bruges, når der opstår fejl i systemet. Kontoen skal valideres hver periode, og eventuelle fejl skal løses. |
| Årets resultat | 300160 | Overført overskud | Egenkapital | Begge | Nej | Denne bogføringstype bruges, når årsafslutningsprocessen køres for at flytte kontosaldoen for **Drift**-typen til den hovedkonto, der er valgt til årets resultat. |
| Debitor, kasserabat | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Nej | Den bogføringstype, der er defineret på siden **Konti til automatiske posteringer**, bruges ikke. Der kræves en hovedkonto, når kasserabatter konfigureres i Debitor.|
| Kreditor kasserabat | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Nej | Den bogføringstype, der er defineret på siden **Konti til automatiske posteringer**, bruges ikke. Der kræves en hovedkonto, når kasserabatter konfigureres i Kreditor. |

## <a name="additional-posting-types"></a>Yderligere bogføringstyper

I tabellen nedenfor vises eksempler på yderligere bogføringstyper, der skal konfigureres, hvis du planlægger at bruge de relaterede funktioner. Der findes ingen konfiguration af posteringsprofil i et andet modul for disse bogføringstyper. Kolonnen "Debet/Kredit?" angiver, om posteringen typisk bogfører et debet- eller kreditbeløb. I nogle tilfælde kan en postering enten bogføre et debet- eller et kreditbeløb. I kolonnen "Clearingkonto" angives, om bogføringstypen er en clearingkonto. Hvis bogføringstypen er en clearingkonto, bliver det beløb, der bogføres på kontoen, automatisk tilbageført, når en senere transaktion bogføres.

| Bogføringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | Beskrivelse |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Statuskonto for konsolideringsdifference | 801200 | Gevinst og tab - Værdiregulering | Udgift | Begge | Nej | Denne bogføringstype bruges, når du udfører en konsolidering, der omfatter en værdiregulering af valuta, og øredifferencer opstår under værdireguleringen. |
| Driftskonto for konsolideringsdifferencer | 801200 | Gevinst og tab - Værdiregulering | Udgift | Begge | Nej | Denne bogføringstype bruges, når du udfører en konsolidering, der omfatter en værdiregulering af valuta, og øredifferencer opstår under værdireguleringen. |
| Internt mellem enheder – debet | 133500 | Internt mellem enheder – debitor | Aktiv | Debet | Nej | Denne bogføringstype bruges, når du vælger en udligningsdimension på **Finans**-siden, og dimensionen ikke balancerer i en postering, der bogføres. |
| Internt mellem enheder - kredit | 233500 | Internt mellem enheder – kreditor | Passiv | Kredit | Nej | Denne bogføringstype bruges, når du vælger en udligningsdimension på **Finans**-siden, og dimensionen ikke balancerer i en postering, der bogføres. |
