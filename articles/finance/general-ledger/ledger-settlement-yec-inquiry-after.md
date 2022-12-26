---
title: Forståelse mellem funktionen for finansudligning efter årsafslutning ved hjælp af forespørgselssiden
description: Denne artikel forklarer, hvordan du bruger funktionen Opmærksomhed mellem finansudligning med den nye forespørgselsside, efter årsafslutning for Finans er kørt.
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
ms.openlocfilehash: 921d2a17409ae10cd9c22eeca11557ba1248b9bc
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853119"
---
# <a name="awareness-between-ledger-settlement-feature-after-year-end-close-using-the-inquiry-page"></a>Forståelse mellem funktionen for finansudligning efter årsafslutning ved hjælp af forespørgselssiden

En primær ændring ved funktionen **Opmærksomhed mellem finansudligning og årsafslutning** (funktionen **Opmærksomhed**) betyder at finansudligning ikke kan gennemføres på tværs af regnskabsår. Denne begrænsning på tværs af året er kun relevant for finansudligning, ikke for udligninger i Debitor eller Kreditor.

Før funktionen **Opmærksomhed** er aktiveret, må det regnskabsår, hvor årsslut lukningen afsluttes, ikke have nogen finansposteringer, der udlignes hen over flere regnskabsår. Helt specifikt skal alle posteringer, der er bogført i det regnskabsår, som du kører årsafslut slutter for, ikke-udlignet fra posteringer, der er bogført i et andet regnskabsår. Transaktionerne kan derefter udlignes igen i forhold til transaktioner i indeværende regnskabsår.

Denne artikel beskriver de trin, der er nødvendige for at identificere, udligne og nulstille de finansposteringer, der udlignes på tværs af året. I det eksempel, der er angivet, er regnskabsåret 2022 lukket. Der fokuseres på at forberede udligninger for finansposteringerne længe før årsafslutningen for 2023 køres.

Pr. Microsoft Dynamics 365 Finance release 10.0.29 kan du identificere, fjerne udligning og udligne finansposteringer igen ved at bruge en ny forespørgselsside, der er tilgængelig. Hvis du ikke aktuelt er i Microsoft Dynamics 365 Finance-version 10.0.29 eller senere, kan du finde trinene til at identificere, annullere og nulstille finanstransaktionerne i følgende artikler:

- [Opmærksomhed mellem finansudligningsfunktionen før årsafslutning](ledger-settle-yec.md)
- [Opmærksomhed mellem finansudligning efter årsafslutning](ledger-settle-yec-after.md)

Yderligere oplysninger om det nye forespørgselsvindue finder du i [forespørgsel om finansudligning](ledger-settlement-inquiry.md). 

## <a name="example-setup"></a>Eksempel på opsætning

I følgende illustration vises de transaktioner, der blev bogført for hovedkontoen 110200. Posteringerne med grønt blev udlignet i samme regnskabsår og behøver ikke at blive ændret. Posteringerne i rødt er finansudlignet, men de har posteringsdatoer i forskellige regnskabsår. Disse posteringer skal identificeres, og finansudligregningen skal muligvis tilbageføres.

![Bogførte finansposteringer.](./media/excel.png)

## <a name="example"></a>Eksempel:

Følg disse trin, hvis din organisation vil bruge funktionen **Opmærksomhed**, når årsafslutningen for regnskabsåret 2022 er kørt.

> [!NOTE]
> Årsslutslutresultatet for 2022 og tidligere regnskabsår skal kun køres igen, hvis der bogføres nye posteringer i regnskabsåret 2022 eller tidligere. Når du fuldfører følgende procedure, skal der ikke bogføres nye posteringer i 2022. Derfor skal årsafslutningsprocessen ikke køres igen.
>
> Finansposteringer, der udlignes på tværs af regnskabsår, kan forblive finansudlignet, hvis de ikke udlignes mod en postering, der blev bogført i 2022 eller senere. Hvis du f.eks. har udlignet posteringer i 2019 og 2020, kan de stadig udlignes.

1. Gennemfør årsslutsluten for 2022, uden at funktionen **Opmærksomhed** er aktiveret.
2. Identificer alle de posteringer, der er bogført i andre regnskabsår, men udlignet mod posteringer, der blev bogført i 2023 (det næste regnskabsår, der skal lukkes).

    > [!NOTE]
    > 2021-posteringer, der udlignes mod 2022-posteringer, ikke er relevante, da 2022 allerede er lukket. Disse posteringer kan forblive udlignet.

    1. Vælg **Gennemse udligninger** på siden **Finansudligninger**.
    2. Vælg regnskabsåret 2023, det næste finansår, du vil køre årsafslutningen for.
    3. Vælg en værdi i feltet **Økonomisk dimensionsopsætning** for at få vist de økonomiske dimensioner, du vil have vist for finanskontoen. Hovedkontoen vises altid, selvom den dimensionssæt, der er valgt, ikke indeholder en hovedkonto.
    4. Vælg **Vis transaktioner**.

    Forespørgselssiden viser alle transaktioner fra andre regnskabsår, der er udlignet mod transaktioner, der blev bogført i 2023.

    ![Udligninger på tværs af 2023.](./media/2023-cross-settlement.png)

3. Vælg og hold (eller højreklik på) gitterhovedet, og vælg derefter **Eksporter alle rækker**. Disse rækker er alle de posteringer, der skal være ikke-modposteret fra posteringerne i 2022, før årsafslutningen for næste år (2023) kan køres. Du vil have en registrering af disse transaktioner.

    Når alle de detaljerede posteringer fra 2022 er eksporteret til Excel, er du klar til at fjerne posteringerne ved hjælp af forespørgselssiden.

4. Vælg alle poster i gitteret, og vælg derefter **Ikke-markerede poster**. Alle de valgte transaktioner i gitteret er ikke udlignet.

    Der vises to advarselsmeddelelser for at sikre, at posteringsoplysningerne eksporteres til Excel, før posteringerne ikke er udlignet. Hvis du ved et uheld fjernede finansposteringer, før du sender oplysningerne til Excel, kan du ikke tilbageføre de uafsluttende finansposteringer.

    ![Fjern udligning på tværs af året.](./media/revert-settlement.png)

5. Brug Excel-dataene til at finde det samlede antal posteringer i 2022, som blev udlignet mod posteringer i 2023. I dette eksempel er der posteringer i 2023 og $700.
6. Bogfør en reguleringskladde for at opdele startsaldoen for 2022 i to beløb: den del, der er udlignet mod regnskabsåret 2022-posteringen, og den del, der endnu ikke er udlignet i 2023.

    - **Del af den startsaldo, der er udlignet i forhold til forrige år:** Det første beløb på $700 er baseret på de totaler, der blev fundet udlignet for 2021 og 2022.
    - **Den del af startsaldoen, der ikke blev udlignet i forhold til forrige år:** Det andet beløb er forskellen mellem startsaldoen og det udlignede beløb på $700. Resterende beløb er $1.700 – $700 = $1.000.

    På denne måde kan du udligne 2023-posteringerne mod den $700, der oprindeligt blev udlignet mod 2022-posteringen. Dette trin er påkrævet, da finansudlignet ikke tillader delvis udligning.

    1. Gå til finanskladden, og bogfør reguleringen. Din organisation skal beslutte, hvilken posteringsdato der skal bruges, baseret på de perioder, der er åbne i 2023.
    2. Du skal muligvis midlertidigt deaktivere parameteren **Tillad ikke manuel indtastning** på **hovedkontosiden**. Denne justering bogføres ikke, hvis hovedkontoen ikke tillader manuel indtastning.

    ![Bogføre en reguleringskladde.](./media/no-manual4.png)

7. Du kan nu nulstille de ikke-sætte posteringer. Vend tilbage til **finansudligningsiden**, og begræns datointervallet til 1. januar til 31. december 2023. Brug derefter de detaljerede posteringer, du eksporterede til Excel, til at finde de specifikke posteringer, der skal nulstilles. Følgende illustration viser disse posteringer, der ikke er udlignet.

    ![Ikke-udlignede transaktioner for 2023.](./media/2023-unsettled5.png)

    - Startsaldoen på $1.700 kan udlignes mod reguleringen på -$1.700.
    - De detaljerede posteringer, der ikke blev udlignet for -$700 kan udlignes mod reguleringen for $700,00.

8. Aktiver funktionen **Opmærksomhed**. Du er nu klar til at køre årsafslutningen.

    - Før du kører årsafslutning for 2023, skal du overveje at vælge indstillingen **Behold detaljer** for alle statuskonti i opsætningen af finansudligning. Yderligere oplysningerne finde i [Opmærksomhed mellem finansudligning og årsafslutning](awareness-between-ledger-settlement-year-end-close.md).
    - Når du starter årsslutningen for 2023, og der stadig findes posteringer, der udlignes hen over regnskabsår, giver processen til årsslutningen dig straks besked. Denne situation kan forekomme, hvis brugere udlignede posteringer over flere regnskabsår, før funktionen **Opmærksomhed** blev aktiveret.
    - Hvis posteringerne for 2022 og 2023 stadig udlignes, skal du deaktivere funktionen **Opmærksomhed** igen og gentage de forrige trin for at udligne posteringerne. Denne tilgang er påkrævet, fordi 2022 er lukket, og posteringer ikke kan ikke bogføres i et lukket regnskabsår.

Når årsslutresultatet for 2022 er gennemført korrekt, kan du lade funktionen **Opmærksomhed** være aktiveret fra nu af.
