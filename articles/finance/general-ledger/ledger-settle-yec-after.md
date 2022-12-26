---
title: Opmærksomhed mellem finansudligning efter årsafslutning
description: Denne artikel forklarer, hvordan du bruger funktionen Opmærksomhed mellem finansudligning, når processen til lukning af finansårsafslutningen køres.
author: kweekley
ms.date: 12/02/2022
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
ms.openlocfilehash: 7efa9d652d74bd836f51b5b1c5f6bfaf8934ea40
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832161"
---
# <a name="awareness-between-ledger-settlement-feature-after-year-end-close"></a>Opmærksomhed mellem finansudligning efter årsafslutning

[!include [banner](../includes/banner.md)]

## <a name="preparing-for-the-ledger-settlement-awareness-feature-after-year-end-close"></a>Forberedelse til opmærksomhed mellem finansudligning efter årsafslutning

En større ændring ved funktionen **Opmærksomhed mellem finansudligning og årsafslutning** (funktionen **Opmærksomhed**) betyder at finansudligning ikke kan gennemføres på tværs af regnskabsår. Denne begrænsning på tværs af året er kun relevant for finansudligning, ikke for udligninger i Debitor eller Kreditor.

Før funktionen **Opmærksomhed** er aktiveret, må det regnskabsår, hvor årsslut lukningen afsluttes, ikke have nogen finansposteringer, der udlignes hen over flere regnskabsår. Helt specifikt skal alle posteringer, der er bogført i det regnskabsår, som du kører årsafslut slutter for, ikke-udlignet fra posteringer, der er bogført i et andet regnskabsår. Transaktionerne kan derefter udlignes igen i forhold til transaktioner i indeværende regnskabsår.

I denne artikel beskrives de trin, der er nødvendige for at identificere, udligne og nulstille de finansposteringer, der udlignes på tværs af regnskabsår. I det eksempel, der er angivet, er regnskabsåret 2022 lukket. Der fokuseres på at forberede udligninger for finansposteringerne længe før årsafslutningen for 2023 køres.

## <a name="example-setup"></a>Eksempel på opsætning

I følgende illustration vises de transaktioner, der blev bogført for hovedkontoen 110190. Finansposteringerne med grønt udlignes i samme regnskabsår og behøver ikke at blive ændret. Posteringerne i rødt er finansudlignet, men de har posteringsdatoer i forskellige regnskabsår. Disse posteringer skal identificeres, og finansudligregningen skal muligvis tilbageføres.

![Finansposter.](./media/afterYEC1.png)

## <a name="example"></a>Eksempel:

Følg disse trin, hvis din organisation vil bruge funktionen **Opmærksomhed**, når årsafslutningen for regnskabsåret 2022 er kørt.

> [!NOTE]
> Årsslutslutresultatet for 2022 og tidligere regnskabsår skal kun køres igen, hvis der bogføres nye posteringer i regnskabsåret 2022 eller tidligere. Når du fuldfører følgende procedure, skal der ikke bogføres nye posteringer i 2022. Derfor skal årsafslutningsprocessen ikke køres igen.
>
> Finansposteringer, der udlignes på tværs af regnskabsår, kan forblive finansudlignet, hvis de ikke udlignes mod en postering, der blev bogført i 2023 eller senere. Hvis du f.eks. har udlignet posteringer for 2019 og 2020, kan de stadig udlignes.

1. Gennemfør årsslutsluten for 2022, uden at funktionen **Opmærksomhed** er aktiveret.
2. Valgfrit: Når årsslutslutning for 2022 er fuldført, skal du aktivere funktionen **Opmærksomhed**. En årsafslutning betragtes som fuldført, når alle reguleringer bogføres, og årsslutprocessen ikke køres igen.

    > [!IMPORTANT]
    > Funktionen **Opmærksomhed** må ikke aktiveres, hvis årsafslutningen for 2022 køres igen. Fordelen ved at aktivere funktionen nu er, at du forhindrer brugere i at afregne finansposteringer, der er bogført i andre regnskabsår.

    Hvis årsafslutningen ikke er fuldført, kan du stadig udføre de næste trin uden at aktivere funktionen **Opmærksomhed**. Du aktiverer funktionen på et senere tidspunkt, som angivet.

3. På siden **Finansudligning** skal du identificere summen af alle de posteringer, der er udlignet for regnskabsårene 2022 og 2023. Bemærk, at 2021-posteringer, der udlignes mod 2022-posteringer, ikke er relevante, da 2022 allerede er lukket. Disse posteringer kan forblive udlignet.

    1. Angiv et datointerval for hele regnskabsåret 2022. Angiv f.eks. 1. januar 2022 til og med 31. december 2022, hvis du bruger et kalenderår som regnskabsår.
    2. Vælg **Udlignet** i feltet **Status**.
    3. Filtrer på én finanskonto ad gangen.

        - Du skal gentage disse trin for hver finanskonto, der foretages finansudligning for.
        - Hvis der ikke længere er konfigureret andre finanskonti til finansudligning, skal du måske midlertidigt føje dem tilbage til opsætningen af finansudligning. Udfør derefter disse trin, hvis disse finanskonti har posteringer i 2023, der er udlignet mod posteringer i 2022 eller tidligere.

    4. Vælg og hold (eller højreklikke) i kolonnen **Status**, og vælg derefter at gruppere efter denne kolonne.
    5. Vælg og hold (eller højreklikke) i kolonnen **Beløb i transaktionsvaluta**, og vælg derefter at lave en total for denne kolonne.

        - Hvis du kun har udlignet posteringer i 2022, er totalen 0 (nul).
        - Hvis du har posteringer, der er udlignet i løbet af flere regnskabsår, er totalen ikke 0 (nul).

    6. Identificer, hvilke posteringer der blev udlignet mellem 2022 og 2023, ved at filtrere på **udligningsdatoværdien**. Hvis du filtrerer på en udligningsdato fra 1. januar 2023 til og med 31. december 2023, får du i alt $700, som er summen af posteringer, der er udlignet for 2022 og 2023.

    ![Samlede 2022-finansposteringer.](./media/afterYEC2.png)

4. Gentag trin 3 for regnskabsåret 2023. Totalen skal stemme overens med $700 fra 2022, fordi der ikke blev udlignet 2023-posteringer mod 2024-posteringer.

    ![Samlede 2023-finansposteringer.](./media/afterYEC3.png)

5. Hvis du har aktiveret funktionen **Opmærksomhed** i trin 2, skal du deaktivere den, før du går videre til trin 6. I de næste trin skal du tilbageføre den finansudligning, der går over regnskabsår. Hvis funktionen **Opmærksomhed** er aktiveret, kan finansudligningen ikke tilbageføres for regnskabsåret 2022. Du skal derfor deaktivere funktionen, før du kan bruge fortsætte.
6. Når funktionen **Opmærksomhed** er deaktiveret, skal du bruge de samme filtre på **finansudligningssiden** til at tilbageføre finansudligningen af de detaljerede posteringer.

    1. Vend tilbage til **finansudligningssiden**, og filtrer på posteringsdatoer for 2023. Find derefter de detaljerede posteringer, der udgør $700 totalen. Filtrering af disse oplysninger er muligvis ikke let. Du skal muligvis sende dataene for at Microsoft Excel kan evaluere dem.
    2. Når du har listen over posteringer, skal du vælge finansposteringerne på **finansudligningssiden** og vælge **Marker markeret**. Du behøver ikke at se begge de finansposteringer, der blev udlignet. Hvis du markerer enten debet- eller kreditbeløbet, tilbageføres alt med samme **udlignings-id-værdi**, selvom værdien for det **markerede beløb** ikke er **0** (nul).
    3. Vælg **Tilbageføre markerede posteringer** for at annullere posteringerne.

    ![Tilbagefør posteringer.](./media/afterYEC4.png)

7. Bogfør en reguleringskladde for at opdele startsaldoen for 2023 i to beløb: den del, der er udlignet mod regnskabsåret 2022-posteringen, og den del, der endnu ikke er udlignet i 2023.

    - **Del af den startsaldo, der er udlignet i forhold til forrige år:** Det første beløb på $700 er baseret på de totaler, der blev fundet udlignet for 2022 og 2023.
    - **Den del af startsaldoen, der ikke blev udlignet i forhold til forrige år:** Det andet beløb er forskellen mellem startsaldoen og det første beløb på $525. Resterende beløb er $1700 – $700 = $1000.

    På denne måde kan du udligne 2023-posteringerne mod den $700, der oprindeligt blev udlignet mod 2022-posteringen. Dette trin er påkrævet, da finansudlignet ikke tillader delvis udligning.

    1. Gå til finanskladden, og bogfør reguleringen. Din organisation skal beslutte, hvilken posteringsdato der skal bruges, baseret på de perioder, der er åbne i 2023.
    2. Du skal muligvis midlertidigt deaktivere parameteren **Tillad ikke manuel indtastning** på **hovedkontosiden**. Denne justering bogføres ikke, hvis hovedkontoen ikke tillader manuel indtastning.

    ![Reguleringer kan ikke bogføres.](./media/afterYEC5.png)

8. Du kan nu nulstille de ikke-sætte posteringer. Vend tilbage til **finansudligningsiden**, og begræns datointervallet til 1. januar 2022 til 31. december 2022. Følgende illustration viser disse posteringer, der ikke er udlignet.

    ![Ikke-udlignede transaktioner.](./media/afterYEC6.png)

    - Startsaldoen på $1.700 kan udlignes mod reguleringen på -$1.700.
    - De detaljerede posteringer, der ikke blev udlignet for -$700 kan udlignes mod reguleringen for $700,00.

9. Aktiver funktionen **Opmærksomhed** igen.
10. Hvis funktionen **Opmærksomhed** er aktiveret, kan finansudligningen ikke tilbageføres på tværs af regnskabsår. Du skal muligvis opdele den resterende saldo på posteringer $1.000 mindre beløb, før du kan udligne mod nye posteringer i 2023. Nogle kunder vælger at bogføre denne detaljer i trin 8, hvor transaktionen yderligere $1.000 til at repræsentere de ikke-afsatte posteringer fra 2022. Denne indfaldsvinkel viser egentlig, hvad funktionen **Opmærksomhed** kun gør i løbet af det indeværende år. Næste år vil det automatisk blive udført ved hjælp af indstillingen **Behold detaljer** i opsætningen af finansudligninger.
