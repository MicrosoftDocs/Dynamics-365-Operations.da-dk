---
title: Budgetanalyserapport
description: Denne artikel beskriver budgetanalyserapporten, som anvendes til at generere en opsummeret rapport, der sammenligner budgetterede beløb med faktiske udgifter og indtægtsaktiviteter i løbet af en periode, du angiver.
author: v-kiarnd
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.search.industry: public sector
ms.author: twheeloc
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 9045f39dad09f8b8697151eafcbe65f7e6fb6d8e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879383"
---
# <a name="budget-analysis-report"></a>Budgetanalyserapport

[!include[banner](../includes/banner.md)]

Du kan bruge **Budgetanalyse**-rapporten til at generere en opsummeret rapport, der sammenligner budgetterede beløb med faktiske udgifter og indtægtsaktiviteter i løbet af en periode, du angiver. For hver konto viser rapporten de budgetterede beløb, faktiske udgifter eller indtægter, behæftelsesbeløb fra indkøbsordrer og budgetreservationsbeløb fra indkøbsrekvisitioner. Desuden viser rapporten det resterende budgetbeløb for hver konto og fond.

Rapporten kan sorteres efter fond og derefter kontonummer. I hver fond viser rapporten subtotaler baseret på den økonomiske dimensionsopsætning, du har valgt at gruppere efter. Når du bruger navigationsruden til at gennemse aktiviteten, bestemmer grupperingen, hvordan aktiviteten vises der.

Rapporten indeholder alle konti, der har en aktivitet i datointervallet for enten konti for indtægter eller udgifter. Alle konti, der er markeret som en driftskontotype, medtages ikke i rapporten. Rapporten inkluderer heller ikke nettototaler. (Nettototaler beregnes som indtægt minus udgifter).

Hvis du vil have vist flere oplysninger om en konto, skal du vælge kontonavnet eller -nummeret for at åbne siden **Budgetanalyseforespørgsel**. Du kan få vist alle de transaktioner, der bidrager til beløbet i rapporten. Hvis du vil se transaktionerne, kan du få vist linkene til nedrulningsrapporten i rapporten. Vælg et link for at åbne en nedrulningsrapport, der indeholder transaktionsoplysninger om det reviderede budget, faktiske udgifter eller indtægter, behæftelser eller budgetreservationer. Nedrulningsrapporterne kan også omfatte ventende transaktioner.

## <a name="filter-the-data-on-this-report"></a>Filtrere dataene i denne rapport

Når du opretter rapporten, vises følgende standardparametre. Du kan bruge disse parametre til at filtrere de data, der vises i rapporten. Du kan finde flere oplysninger i afsnittet "Sådan arbejder du med rapporter" i denne artikel.

| Felt | Beskrivende tekst |
|---|---|
| Økonomisk dimensionsopsætning | Vælg dimensionsgruppen for de finanskonti, der skal vises i rapporten.<p>En økonomisk dimensionsopsætning er en navngivet gruppe konti eller dimensioner, der indeholder enten kontoværdier for kontoen eller dimensionsværdier for en enkelt dimension. Et sæt kan f.eks. omfatte hovedkonti, afdelinger og bærere. Alternativt kan det indeholde kombinationer, f.eks. en bærer og en hovedkonto eller en afdeling og en bærer.  |
| Budgetmodel | Vælg den budgetmodel, der skal rapporteres budgetbeløb fra. |
| Tidsperiode for budgetcyklus | Angiv den budgetcyklus, der skal oprettes en rapport for. |
| Kontotype | Angiv, om der skal rapporteres budget- og faktiske beløb for udgiftskonti eller indtægtskonti. Som standard rapporteres udgiftskonti. Hvis du ændrer kontotypen, når du har valgt konti eller angiver en valgforespørgsel, skal du vælge en ny gruppe af konti i **Hovedkonti**-felterne og vælge **Vælg** for at angive en ny forespørgsel. |
| Gruppér hovedkonti efter kategori | Markér dette afkrydsningsfelt for at gruppere konti efter hovedkontokategori, når de er grupperet efter økonomiske dimensioner på en finanskonto. Det laveste grupperingsniveau vises, uanset hvilken økonomisk dimension du har valgt. Hovedkontokategorierne sorteres efter deres alfanumeriske koder. Alle konti, der ikke er tildelt til en hovedkontokategori, grupperes efter hinanden. Du konfigurerer hovedkontokategorier ved hjælp af siden **Hovedkontokategorier**. |
| Undertryk konti med nuller | Markér dette afkrydsningsfelt for kun at få vist konti, der har faktiske og budgetterede beløb, som ikke er nul. |
| Vis links til detailudledningsrapport | Markér dette afkrydsningsfelt for at vise links, der kan bruges til at åbne en nedrulningsrapport, der indeholder transaktionsoplysninger om det reviderede budget, faktiske udgifter eller indtægter, behæftelser eller budgetreservationer. |
| Vis ventende transaktioner i detailudledningsrapporter | Hvis afkrydsningsfeltet **Vis links til nedrulningsrapporter** er markeret, kan du markere dette afkrydsningsfelt for at medtage ventende transaktionsdetaljer i en nedrulningsrapport for revideret budget, faktiske udgifter eller indtægter, behæftelser eller budgetreservationer.<blockquote>[!NOTE] Hvis du markerer dette afkrydsningsfelt, kan de viste saldi være forskellige fra de beløb, der vises i **Budgetanalyse**-rapporten. |
| Datoer, der skal indgå | Angiv, om beløb skal rapporteres for en hel budgetcyklus eller et datointerval. Når du kører denne rapport for et tidligere år, undertrykkes år-til-dato-kolonnerne (ÅTD).<ul><li>Hvis du vælger **Budgetcyklus**, skal du vælge navnet på en budgetcyklus. Denne indstilling bruger de datoer, der er konfigureret for den valgte budgetcyklus på siden **Tidsperioder for budgetcyklus**.</li><li>Hvis du vælger **Datointerval**, skal du vælge start-og slutdatoerne for budgettet og de faktiske poster, der skal medtages i rapporten. Du kan angive forskellige intervaller for budgetbeløbene og de faktiske beløb. Hvis organisationen f.eks. lægger budget for to år, kan du rapportere budgetbeløb for et datointerval på to år, mens kun det aktuelle år for faktiske udgifter eller omsætningsbeløb medtages.<blockquote>[!NOTE] Det datointerval, du angiver, skal være i et eller flere af de regnskabsår, der er medtaget i den regnskabskalender, der blev valgt, da tidsperioden for budgetcyklussen blev konfigureret. En regnskabskalender for en budgetcyklus omfatter f.eks. regnskabsår, der har datoer fra 1. januar 2010 til 31. december 2014. I dette tilfælde kan datoen i "fra" ikke ligge før 1. januar 2010.</blockquote></li></ul> |
| Budget | Angiv datointervallet for de budgetposter, der skal medtages i rapporten. |
| Faktiske oplysninger | Angiv datointervallet for de faktiske poster, der skal medtages i rapporten. |
| Sammenlæg pr. | Vælg den dimensionsopsætning, der bruges til at vise subtotaler efter gruppe. Finanskonti, der har samme værdi for de økonomiske dimensioner, du angiver i dimensionsopsætningen, er grupperet i rapporten. Du kan oprette nye dimensionsopsætninger, som konti skal grupperes efter. |
| Sideskift ved | Vælg en økonomisk dimensionsopsætning, der indeholder de dimensioner, hvor du vil indsætte en ny rapportside, hvis dimensionsværdien ændres. Du kan kun indsætte et sideskift for dimensioner i den dimensionsopsætning, du har valgt i feltet **Gruppér efter**. Hvis du f.eks. grupperer efter Fond-Afdeling, skal du indsætte siden for Fond og Afdeling eller kun for Fond. Du kan oprette nye dimensionsopsætninger, som konti skal grupperes efter.  |
| Hovedkonti | Angiv intervallet for de hovedkontonumre, der skal vises i rapporten. Lad felterne være tomme for at køre rapporten for alle konti. |

## <a name="review-the-report"></a>Gennemse rapporten

Rapporten indeholder følgende oplysninger:

- Kontonummer
- Kontonavn
- Revideret budget (= oprindeligt budget + budgetreguleringer)
- Aktuelle faktiske oplysninger (for enten indtægter eller udgifter afhængigt af kontotypen)
- Aktuel procentdel af budget (faktiske oplysninger/revideret budget)
- ÅTD-faktiske oplysninger (kun bogførte transaktioner for indeværende år tages i betragtning).
- Behæftelser (kun bogførte transaktioner for indeværende år tages i betragtning).
- Budgetreservationer (kun bogførte transaktioner for indeværende år tages i betragtning).
- Resterende budget (= oprindeligt budget + budgetreguleringer – faktiske oplysninger – behæftelser – budgetreservationer) (kun bogførte transaktioner medtages i denne beregning).
- ÅTD-procent af resterende budget (= resterende budget ÷ revideret budget) (kun bogførte transaktioner for indeværende år medtages i denne beregning).

Rapporten indeholder også totaler for hver finansierings-, afdelings-og hovedkontokategori, hvis de er medtaget.

Nedrulningsrapporten indeholder følgende oplysninger:

- Navnet på kategorien for nedrulninger: revideret budget, faktisk udgifter eller indtægter, ÅTD-behæftelser eller ÅTD-budgetreservationer
- Navn på den juridiske enhed
- Finanskontonummer
- Dato for transaktionen
- Bilagsnummer
- Dokumentoplysninger for transaktionen
- Beskrivelse af bilagstransaktionsdatoen
- Bilagsoplysninger
- Debet-og kreditoplysninger for bilaget med faktiske oplysninger
- Positive og negative beløb for budgettet, behæftelse og budgetreservationsbilaget
- Åbne, afslutte og køre saldi for finanskontoen


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
