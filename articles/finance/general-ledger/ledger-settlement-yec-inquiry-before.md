---
title: Forståelse mellem funktionen for finansudligning før årsafslutning ved hjælp af forespørgselssiden
description: Denne artikel forklarer, hvordan du bruger funktionen Opmærksomhed mellem finansudligning med den nye forespørgselsside, før årsafslutning for Finans er kørt.
author: kweekley
ms.date: 12/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: b138d2d5e88ff7f2ca2240cf256a4938f55a5606
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853139"
---
# <a name="awareness-between-ledger-settlement-feature-before-year-end-close-using-the-inquiry-page"></a>Forståelse mellem funktionen for finansudligning før årsafslutning ved hjælp af forespørgselssiden

En primær ændring ved funktionen **Opmærksomhed mellem finansudligning og årsafslutning** (funktionen **Opmærksomhed**) betyder at finansudligning ikke kan gennemføres på tværs af regnskabsår. Denne begrænsning på tværs af året er kun relevant for finansudligning, ikke for udligninger i Debitor eller Kreditor.

Før funktionen **Opmærksomhed** er aktiveret, må det regnskabsår, hvor årsslut lukningen afsluttes, ikke have nogen finansposteringer, der udlignes hen over flere regnskabsår. Helt specifikt skal alle posteringer, der er bogført i det regnskabsår, som du kører årsafslut slutter for, ikke-udlignet fra posteringer, der er bogført i et andet regnskabsår. Transaktionerne kan derefter udlignes igen i forhold til transaktioner i indeværende regnskabsår.

Denne artikel beskriver de trin, der er nødvendige for at identificere, udligne og nulstille de finansposteringer, der udlignes på tværs af regnskabsår. I det eksempel, der er angivet, er regnskabsåret 2021 lukket, og du gør dig klar til at køre årsslutslutkørslen for regnskabsåret 2022.

Pr. Microsoft Dynamics 365 Finance release 10.0.29 kan du identificere, fjerne udligning og udligne finansposteringer igen ved at bruge en ny forespørgselsside, der er tilgængelig. Hvis du ikke aktuelt er i finansversionen 10.0.29 eller senere, kan du finde trinene til at identificere, annullere og nulstille finanstransaktionerne i følgende artikler:

- [Opmærksomhed mellem finansudligningsfunktionen før årsafslutning](ledger-settle-yec.md)
- [Opmærksomhed mellem finansudligning efter årsafslutning](ledger-settle-yec-after.md)

Yderligere oplysninger om det nye forespørgselsvindue finder du i [forespørgsel om finansudligning](ledger-settlement-inquiry.md). 

## <a name="example-setup"></a>Eksempel på opsætning

I følgende illustration vises de transaktioner, der blev bogført for hovedkontoen 110200. Posteringerne med grønt blev udlignet i samme regnskabsår og behøver ikke at blive ændret. Posteringerne i rødt er finansudlignet, men de har posteringsdatoer i forskellige regnskabsår. Disse posteringer skal identificeres, og finansudligregningen skal muligvis tilbageføres.

![Bogførte finansposteringer.](./media/ledgersettlement.png)

## <a name="example"></a>Eksempel:

Følg disse trin, hvis din organisation vil bruge funktionen **Opmærksomhed**, før du kører årsafslutningen for regnskabsåret 2022 er kørt.

> [!NOTE]
> Årsslutslutresultatet for 2021 og tidligere regnskabsår skal kun køres igen, hvis der bogføres nye posteringer i regnskabsåret 2021 eller tidligere. Når du fuldfører følgende procedure, skal der ikke bogføres nye posteringer i 2021. Derfor skal årsafslutningsprocessen ikke køres igen.
>
> Finansposteringer, der udlignes på tværs af regnskabsår, kan forblive finansudlignet, hvis de ikke udlignes mod en postering, der blev bogført i 2022 (året, der afsluttes) eller senere. Hvis du f.eks. har udlignet posteringer i 2019 og 2020, kan de stadig udlignes.

1. **Undlad** at aktivere funktionen **Opmærksomhed** igen.
2. Vælg **Gennemse udligninger** på siden **Finansudligninger**.
3. Identificer alle de posteringer, der er bogført i andre regnskabsår, men udlignet mod posteringer, der blev bogført i 2022.

    1. Vælg regnskabsåret 2022, skal du køre årsafslutningen for.
    2. Vælg en værdi i feltet **Økonomisk dimensionsopsætning** for at få vist de økonomiske dimensioner, du vil have vist for finanskontoen. Hovedkontoen vises altid, selvom den dimensionssæt, der er valgt, ikke indeholder en hovedkonto.
    3. Vælg **Vis transaktioner**.

    På forespørgselssiden vises alle posteringer for alle finanskonti (også selvom de ikke længere er i opsætningen af finansudligning) fra alle andre regnskabsår, der er udlignet mod posteringer, der blev bogført i 2022. Der vises tre forskellige finanskonti.

    ![Udligninger på tværs af 2022.](./media/review-cross-year.png)

3. Vælg og hold (eller højreklik på) gitterhovedet, og vælg derefter **Eksporter alle rækker**. Disse rækker er alle de posteringer, der skal være ikke-modposteret fra posteringerne i 2022, før årsafslutningen kan køres. Du skal bruge den detaljerede posteringsliste, så du kan nulstille posteringerne korrekt senere.
4. Bemærk ar regnskabsåret, hvor transaktionerne blev for posteret. I dette eksempel er der posteringer i 2021 og 2023.
5. På forespørgselssiden kan du ændre regnskabsåret til 2021, det første regnskabsår, der indeholder posteringer, som blev udlignet mod 2022-posteringer.
6. Filtrer på kolonnen **Posteringsdato**, så kun posteringer, der blev bogført i 2022, medtages. Disse posteringer er detaljerede posteringer fra 2022, der blev udlignet mod posteringer i 2021.
7. Vælg og hold (eller højreklik på) gitterhovedet, og vælg derefter **Eksporter alle rækker**.

    > [!IMPORTANT]
    > I følgende fremgangsmåde vil disse posteringer blive fjernet og derefter nulstillet i forhold til posteringer i 2022. Det er vigtigt, at du vedligeholder denne detaljer i Excel.

    ![Udligninger på tværs af 2021.](./media/review-cross-year.png)

8. På forespørgselssiden kan du ændre regnskabsåret til 2023, det næste regnskabsår, der indeholder posteringer, som blev udlignet mod 2022-posteringer. 
9. Filtrer på kolonnen **Posteringsdato**, så kun posteringer, der blev bogført i 2022, medtages. Disse posteringer er detaljerede posteringer fra 2023, der blev udlignet mod posteringer i 2022. 
10. Vælg og hold (eller højreklik på) gitterhovedet, og vælg derefter **Eksporter alle rækker**.

    > [!IMPORTANT]
    > I følgende fremgangsmåde vil disse posteringer blive fjernet og derefter nulstillet i forhold til posteringer i 2022. Det er vigtigt, at du vedligeholder denne detaljer i Excel.

    ![Udligninger på tværs af 2023.](./media/filter-transactions.png)

11. Gentag de forrige trin for hvert regnskabsår, der indeholder posteringer, der er udlignet mod posteringer i 2022. Eksportér altid de detaljerede posteringer til Excel.

    Når alle de detaljerede posteringer fra 2021 og 2023 er eksporteret til Excel, er du klar til at fjerne posteringerne ved hjælp af den nye forespørgselsside.

12. Ret finansåret til 2022.
13. Vælg alle poster i gitteret, og vælg derefter **Ikke-markerede poster**. Alle de valgte transaktioner i gitteret er ikke udlignet.

    Der vises to advarselsmeddelelser for at sikre, at posteringsoplysningerne eksporteres til Excel, før posteringerne ikke er udlignet. Hvis du ved et uheld fjernede finansposteringer, før du sender oplysningerne til Excel, kan du ikke tilbageføre de uafsluttende finansposteringer.

    ![Fjerne udligning af posteringer på tværs af udligninger.](./media/revert-unsettle.png)

14. Brug Excel-dataene til at finde det samlede antal posteringer i 2021 og 2023, som blev udlignet mod posteringer i 2022. I dette eksempel er posteringerne for 2021 i $525 og posteringerne for 2023 i alt $700.
15. Bogfør en reguleringskladde for at opdele startsaldoen for 2022 i to beløb: den del, der er udlignet mod regnskabsåret 2021-posteringen, og den del, der endnu ikke er udlignet i 2022.

    - **Del af den startsaldo, der er udlignet i forhold til forrige år:** Det første beløb på $525 er baseret på de totaler, der blev fundet udlignet for 2021 og 2022.
    - **Den del af startsaldoen, der ikke blev udlignet i forhold til forrige år:** Det andet beløb er forskellen mellem startsaldoen og det udlignede beløb på $525. Resterende beløb er $1.025 – $525 = $500.

    På denne måde kan du udligne 2022-posteringerne mod den $525, der oprindeligt blev udlignet mod 2021-posteringen. Dette trin er påkrævet, da finansudlignet ikke tillader delvis udligning.

    1. Gå til finanskladden, og bogfør reguleringen. Din organisation skal beslutte, hvilken posteringsdato der skal bruges, baseret på de perioder, der er åbne. Disse posteringer kan være udlignet ved hjælp af en udligningsdato fra januar eller februar 2022, men reguleringen skal måske bogføres i december, hvis dette er den eneste åbne periode.
    2. Du skal muligvis midlertidigt deaktivere parameteren **Tillad ikke manuel indtastning** for 110200 på **hovedkontosiden**. Denne justering bogføres ikke, hvis hovedkontoen ikke tillader manuel indtastning.

    ![Bogføre en reguleringskladde.](./media/not-post.png)

16. Du kan nu nulstille de ikke-sætte posteringer. Vend tilbage til siden **Finansudligninger**, angiv et datointerval fra 1. januar til og med 31. december 2022, og filtrer på hovedkonto 110200. Brug derefter de detaljerede posteringer, du eksporterede til Excel, til at finde de specifikke posteringer, der skal nulstilles. Følgende illustration viser disse posteringer, der ikke er udlignet.

    ![Ikke-udlignede transaktioner.](./media/updated-unsettled.png)

    - Startsaldoen på $1.025 kan udlignes mod reguleringen på -$1.025.
    - De detaljerede posteringer, der ikke blev udlignet for -$400, -$50 og -$75 kan udlignes mod reguleringen for $25.

17. Aktiver funktionen **Opmærksomhed**. Du er nu klar til at køre årsafslutningen.

    - Før du kører årsafslutning, skal du overveje at vælge indstillingen **Behold detaljer** for alle statuskonti i opsætningen af finansudligning. Yderligere oplysningerne finde i [Opmærksomhed mellem finansudligning og årsafslutning](awareness-between-ledger-settlement-year-end-close.md).
    - Når du starter årsslutningen for 2022, og der stadig findes posteringer, der udlignes hen over regnskabsår, giver processen til årsslutningen dig straks besked. Denne situation kan forekomme, hvis brugere udlignede posteringer på tværs af regnskabsår, efter at du har fuldført de foregående trin.
    - Hvis posteringerne for 2021 og 2022 stadig udlignes, skal du deaktivere funktionen **Opmærksomhed** igen og gentage de forrige trin for at udligne posteringerne. Denne tilgang er påkrævet, fordi 2021 er lukket, og posteringer ikke kan ikke bogføres i et lukket regnskabsår.
    - Hvis 2022- og 2023-transaktionerne stadig udlignes, behøver du ikke deaktivere funktionen **Opmærksomhed**. Da hverken 2022 eller 2023 er lukket, kan du bruge de foregående trin til at fjerne posteringerne.

18. Du kan udligne posteringen $700 2023 mod de detaljerede posteringer, der blev hentet som startsaldi i 2023. Denne postering udlignes ikke mod den oprindelige postering i 2022.

Når årsslutresultatet for 2022 er gennemført korrekt, kan du lade funktionen **Opmærksomhed** være aktiveret fra nu af.
