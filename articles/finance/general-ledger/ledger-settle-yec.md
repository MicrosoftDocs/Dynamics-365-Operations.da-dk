---
title: Opmærksomhed mellem finansudligningsfunktionen før årsafslutning
description: Denne artikel forklarer, hvordan du bruger funktionen Opmærksomhed mellem finansudligning, før finansprocessen til årsafslutning er kørt.
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
ms.openlocfilehash: c79b6f50296560e1534be0621bb2aa8eaa2c1dc8
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832156"
---
# <a name="awareness-between-ledger-settlement-feature-before-year-end-close"></a>Opmærksomhed mellem finansudligningsfunktionen før årsafslutning

[!include [banner](../includes/banner.md)]

## <a name="preparing-for-the-ledger-settlement-awareness-feature-before-year-end-close"></a>Forberedelse til opmærksomhed mellem finansudligning før årsafslutning

En større ændring ved funktionen **Opmærksomhed mellem finansudligning og årsafslutning** (funktionen **Opmærksomhed**) betyder at finansudligning ikke kan gennemføres på tværs af regnskabsår. Denne begrænsning på tværs af året er kun relevant for finansudligning, ikke for udligninger i Debitor eller Kreditor.

Før funktionen **Opmærksomhed** er aktiveret, må det regnskabsår, hvor årsslut lukningen afsluttes, ikke have nogen finansposteringer, der udlignes hen over flere regnskabsår. Helt specifikt skal alle posteringer, der er bogført i det regnskabsår, som du kører årsafslut slutter for, ikke-udlignet fra posteringer, der er bogført i et andet regnskabsår. Transaktionerne kan derefter udlignes igen i forhold til transaktioner i indeværende regnskabsår.

Denne artikel beskriver de trin, der er nødvendige for at identificere, udligne og nulstille de finansposteringer, der udlignes på tværs af regnskabsår. I det eksempel, der er angivet, er regnskabsåret 2021 lukket, og du gør dig klar til at køre årsslutslutkørslen for regnskabsåret 2022.

## <a name="example-setup"></a>Eksempel på opsætning

I følgende illustration vises de transaktioner, der blev bogført for hovedkontoen 110190. Finansposteringerne med grønt udlignes i samme regnskabsår og behøver ikke at blive ændret. Posteringerne i rødt er finansudlignet, men de har posteringsdatoer i forskellige regnskabsår. Disse posteringer skal identificeres, og finansudligregningen skal muligvis tilbageføres.

![Finansposter.](./media/YEC1.png)

## <a name="example"></a>Eksempel:

Følg disse trin, hvis din organisation vil bruge funktionen **Opmærksomhed**, før årsafslutningen for regnskabsåret 2022 er kørt.

> [!NOTE]
> Årsslutslutresultatet for 2021 og tidligere regnskabsår skal kun køres igen, hvis der bogføres nye posteringer i regnskabsåret 2021 eller tidligere. Når du fuldfører følgende procedure, skal der ikke bogføres nye posteringer i 2021. Derfor skal årsafslutningsprocessen ikke køres igen.
>
> Finansposteringer, der udlignes på tværs af regnskabsår, kan forblive finansudlignet, hvis de ikke udlignes mod en postering, der blev bogført i 2022 eller senere. Hvis du f.eks. har udlignet posteringer for 2019 og 2020, kan de stadig udlignes.

1. Valgfrit: Aktiver midlertidigt funktionen **Opmærksomhed**.

    - Hvis du vælger at aktivere funktionen, skal du deaktivere den i senere trin, som angivet. Fordelen ved at aktivere funktionen nu er, at du forhindrer brugere midlertidigt i at afregne finansposteringer, der er bogført i andre regnskabsår.
    - Hvis du vælger ikke at aktivere funktionen, anbefales det, at du beder dit team om ikke at udligne posteringer på tværs af regnskabsår. Hvis der foretages udligning på tværs af året, efter at følgende trin er udført, skal du gentage trinnene for at identificere og fjerne udligningen af finansposteringerne.

2. På siden **Finansudligning** skal du identificere summen af alle de posteringer, der er udlignet for regnskabsårene 2021 og 2022.

    1. Angiv et datointerval for hele regnskabsåret 2021. Angiv f.eks. 1. januar 2021 til og med 31. december 2021, hvis du bruger et kalenderår som regnskabsår.

        Hvis funktionen **Opmærksomhed** er aktiveret, modtager du en advarsel om, at transaktioner ikke kan udlignes eller ikke udlignes for et afsluttet regnskabsår. Advarslen er ikke relevant, fordi der ikke forekommer nogen udligning eller uafslutning i dette trin.

    2. Vælg **Udlignet** i feltet **Status**.
    3. Filtrer på én finanskonto ad gangen.

        - Du skal gentage disse trin for hver finanskonto, der foretages finansudligning for.
        - Hvis der ikke længere er konfigureret andre finanskonti til finansudligning, skal du måske midlertidigt føje dem tilbage til opsætningen af finansudligning. Udfør derefter disse trin, hvis disse finanskonti har posteringer i 2022, der er udlignet mod posteringer i et andet regnskabsår.

    4. Vælg og hold (eller højreklikke) i kolonnen **Status**, og vælg derefter at gruppere efter denne kolonne.
    5. Vælg og hold (eller højreklikke) i kolonnen **Beløb i transaktionsvaluta**, og vælg derefter at lave en total for denne kolonne.

        - Hvis du kun har udlignet posteringer i 2021, er totalen 0 (nul).
        - Hvis du har posteringer, der er udlignet i løbet af flere regnskabsår, er totalen ikke 0 (nul).

        I følgende illustration er der en saldo for $525,00. Denne saldo er summen af de posteringer, der blev udlignet mod posteringer i et andet regnskabsår. Totalen kan inkludere posteringer, der blev udlignet mellem 2021 og 2022, og posteringer, der blev udlignet mellem 2022 og 2023.

        ![Finansposter 2021-2022.](./media/YEC2.png)

    6. Identificer, hvilke posteringer der blev udlignet mellem 2020 og 2021, ved yderligere at filtrere på **udligningsdatoværdien**. Angiv datointervalfilteret 1. januar 2021 til og med 31. december 2021. Der vises ingen posteringer, da der ikke er udlignet 2020-posteringer for posteringer, der blev bogført i 2021.
    7. Identificer, hvilke posteringer der blev udlignet mellem 2021 og 2022, ved at ændre datofiltret på **udligningsdatoværdien**. Angiv datointervalfilteret 1. januar 2022 til og med 31. december 2022. Posteringerne vises igen, og totalen vises $525,00, fordi alle posteringer er udlignet mellem 2021 og 2022.

3. På siden **Finansudligning** skal du identificere summen af alle de posteringer, der er udlignet for regnskabsårene 2021 og 2022.

    1. Angiv et datointerval for hele regnskabsåret 2022. Angiv f.eks. 1. januar 2022 til og med 31. december 2022, hvis du bruger et kalenderår som regnskabsår.
    2. Vælg **Udlignet** i feltet **Status**.
    3. Filtrer på én finanskonto ad gangen.
    4. Vælg og hold (eller højreklikke) i kolonnen **Status**, og vælg derefter at gruppere efter denne kolonne.
    5. Vælg og hold (eller højreklikke) i kolonnen **Beløb i transaktionsvaluta**, og vælg derefter at lave en total for denne kolonne.

        ![De samlede finanstransaktionsbeløb.](./media/YEC3.png)

    6. Tilføj et ekstra filter på værdien for **udligningsdatoen**. Angiv datointervalfilteret 1. januar 2022 til og med 31. december 2022. Den samme total for $525,00 vises. Dette resultat validerer, at det samlede beløb af posteringer, der udlignes for 2021 og 2022, $525,00.

        ![Finansposteringer for udligningsdatoer i 2022 og 2023.](./media/YEC4.png)

    7. Skift det ekstra filter på værdien for **udligningsdatoen**. Angiv datointervalfilteret 1. januar 2023 til og med 31. december 2023. Der vises en ny værdi på $700. Denne total er det samlede beløb af posteringer, der blev udlignet for 2022 og 2023.
 
4. Gentag trin 3 for regnskabsåret 2023. Totalen skal stemme overens med $700 fra 2022, fordi der ikke blev udlignet 2023-posteringer mod 2024-posteringer.
5. Hvis du har aktiveret funktionen **Opmærksomhed** i trin 1, skal du deaktivere den, før du går videre til trin 6. I de næste trin skal du tilbageføre den finansudligning, der går over regnskabsår. Hvis funktionen **Opmærksomhed** er aktiveret, kan finansudligningen ikke tilbageføres for regnskabsåret 2021. Du skal derfor deaktivere funktionen, før du kan bruge fortsætte.
6. Når funktionen **Opmærksomhed** er deaktiveret, skal du bruge de samme filtre på **finansudligningssiden** til at tilbageføre finansudligningen af de detaljerede posteringer.

    1. Vend tilbage til **finansudligningssiden**, og filtrer på posteringsdatoer for 2021. Tilføj et ekstra filter på værdien for **udligningsdatoen**. Angiv datointervalfilteret fra 1. januar 2022 til og med 31. december 2022. Find derefter de detaljerede posteringer, der udgør $525 totalen. Filtrering af disse oplysninger er muligvis ikke let. Du skal muligvis sende dataene for at Microsoft Excel kan evaluere dem.
    2. Når du har listen over posteringer, skal du vælge finansposteringerne på **finansudligningssiden** og vælge **Marker markeret**. Du behøver ikke at se begge de finansposteringer, der blev udlignet. Hvis du markerer enten debet- eller kreditbeløbet, tilbageføres alt med samme **Udlignings-id**-værdi, selvom værdien for det **markerede beløb** ikke er **0** (nul).
    3. Vælg **Tilbageføre markerede posteringer** for at annullere posteringerne.

    ![Tilbagefør markerede posteringer.](./media/YEC5.png)

7. Gentag trin 6 for at tilbageføre udligningen af de posteringer, der blev udlignet for 2022 og 2023.

    ![Tilbagefør finansposteringer.](./media/YEC6.png)

8. Bogfør en reguleringskladde for at opdele startsaldoen for 2022 i to beløb: den del, der er udlignet mod regnskabsåret 2021-posteringen, og den del, der endnu ikke er udlignet i 2022.

    - **Del af den startsaldo, der er udlignet i forhold til forrige år:** Det første beløb på $525 er baseret på de totaler, der blev fundet udlignet for 2021 og 2022.
    - **Den del af startsaldoen, der ikke blev udlignet i forhold til forrige år:** Det andet beløb er forskellen mellem startsaldoen og det udlignede beløb på $525. Resterende beløb er $1025 – $525 = $500.

    På denne måde kan du udligne 2022-posteringerne mod den $525, der oprindeligt blev udlignet mod 2021-posteringen. Dette trin er påkrævet, da finansudlignet ikke tillader delvis udligning.

    1. Gå til finanskladden, og bogfør reguleringen. Din organisation skal beslutte, hvilken posteringsdato der skal bruges, baseret på de perioder, der er åbne. Disse posteringer kan være udlignet ved hjælp af en udligningsdato fra januar eller februar 2022, men reguleringen skal måske bogføres i december, hvis dette er den eneste åbne periode.
    2. Du skal muligvis midlertidigt deaktivere parameteren **Tillad ikke manuel indtastning** på **hovedkontosiden**. Denne justering bogføres ikke, hvis hovedkontoen ikke tillader manuel indtastning.

    ![Reguleringer kan ikke bogføres.](./media/YEC7.png)

9. Du kan nu nulstille de ikke-sætte posteringer. Vend tilbage til **finansudligningsiden**, og begræns datointervallet til 1. januar 2022 til 31. december 2022. Følgende illustration viser disse posteringer, der ikke er udlignet.

    ![Ikke-udlignede transaktioner.](./media/YEC8.png)

    - Startsaldoen på $1.025 kan udlignes mod reguleringen på -$1.025.
    - De detaljerede posteringer, der ikke blev udlignet for -$400, -$50 og -$75 kan udlignes mod reguleringen for $525,00.

    ![Detaljerede posteringer.](./media/YEC9.png)

10. Aktiver funktionen **Opmærksomhed**. Du er nu klar til at køre årsafslutningen.

    - Før du kører årsafslutning, skal du overveje at vælge indstillingen **Behold detaljer** i opsætningen af finansudligning for alle statuskonti. Yderligere oplysninger om fordelene ved at gennemføre dette trin finder du i dokumentet Opmærksomhed.
    - Når du starter årsslutningen for 2022, og der stadig findes posteringer, der udlignes hen over regnskabsår, giver processen til årsslutningen dig straks besked.
    - Hvis posteringerne for 2021 og 2022 stadig udlignes, skal du deaktivere funktionen **Opmærksomhed** igen og gentage de forrige trin for at udligne posteringerne. Denne tilgang er påkrævet, fordi 2021 er lukket, og posteringer ikke kan ikke bogføres i et lukket regnskabsår.
    - Hvis 2022- og 2023-transaktionerne stadig udlignes, behøver du **ikke** deaktivere funktionen **Opmærksomhed**. Da hverken 2022 eller 2023 er lukket, kan du bruge de foregående trin til at fjerne posteringerne.

Når årsslutresultatet for 2022 er gennemført korrekt, kan du lade funktionen **Opmærksomhed** være aktiveret fra nu af.
