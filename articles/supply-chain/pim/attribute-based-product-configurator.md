---
title: Attributbaserede salgspriser for begrænsningsbaseret produktkonfiguration
description: Dette emne beskriver, hvordan du kan oprette salgsprismodeller med salgspriser, der er baseret på komponenter og attributter, og ikke på den fysiske stykliste og ruten.
author: sorenva
ms.date: 10/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2020-08-17
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 1538b806a60a9a9950f54c29bd19447c66ac9ec2
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359095"
---
# <a name="attribute-based-sales-prices-for-constraint-based-product-configuration"></a>Attributbaserede salgspriser for begrænsningsbaseret produktkonfiguration

Dette emne beskriver, hvordan du kan oprette salgsprismodeller med salgspriser, der er baseret på komponenter og attributter, og ikke på den fysiske stykliste og ruten. Du kan oprette flere salgsprismodeller for hver produktkonfigurationsmodel.

## <a name="set-relevant-product-information-management-parameters"></a>Angive relevante parametre for administration af produktoplysninger

Før du begynder at opbygge dine prismodeller, skal du definere en standardvaluta, der bruges, når du opbygger dine salgsprismodeller. Du kan også vælge, om du vil knytte en Microsoft Excel-fil til en prisopdeling for alle ordre- eller tilbudslinjer. Du kan bruge prisopdelingen til at dele oplysninger med kunder om, hvordan du er kommet frem til en bestemt salgspris for et konfigureret produkt.

Sådan angiver du standardvalutaen:

1. Gå til **Administration af produktoplysninger \> Konfiguration \> Parametre for administration af produktoplysninger**.
1. Åbn fanen **Begrænsningsbaserede modeller til produktkonfiguration**.
1. Åbn rullelisten **Standardvaluta**, og vælg din valuta.

    ![Angive standardvalutaen for begrænsningsbaseret produktkonfiguration.](media/prod-config-currency.png "Angive standardvalutaen for begrænsningsbaseret produktkonfiguration")

1. Hvis du vil vedhæfte en Excel-fil med en prisopdeling for alle ordre- eller tilbudslinjer, skal du angive **Vedhæft** til **Ja** i sektionen *Prismodel*.

## <a name="build-your-sales-price-models"></a><a name="build-price-model"></a>Oprette salgsprismodeller

Sådan opretter du en salgsprismodel:

1. Gå til **Administration af produktoplysninger \> Produkter \> Produktkonfigurationsmodeller**.
1. Vælg målproduktets konfigurationsmodel.
1. Åbn fanen **Model** i handlingsruden, og vælg **Prismodeller** i gruppen **Konfigurer**.
1. Siden **Prismodeller** åbnes.
1. Vælg en prismodel, eller føj en ny til gitteret.
1. Vælg **Rediger** for at åbne siden Rediger for den valgte model, som indeholder følgende funktioner:
    - I overskriften på formularen vises standardvalutaen, og du kan tilføje nye valutaer i prisopsætningen.
    - I ruden til venstre vises alle komponenter og brugerkrav for produktmodellen. Hver node i produktmodeltræet kan have ét basisprisudtryk og et valgfrit antal udtryksregler. En udtryksregel består af en betingelse og et udtryk, og hver udtryksregel omfatter en produktindstilling, der hjælper med at styre produktets pris.
    - Når du bygger dine betingelser og udtryk, har du de samme operatorer, som er tilgængelige for beregninger i en produktmodel. Udtrykseditoren understøtter også både betingelser og udtryk.
1. Vælg en node i venstre kolonne, og brug derefter de funktioner, der er beskrevet i det foregående trin, til at oprette prissætningsregler for den (se også det eksempel, der følger efter denne procedure). Gentag dette trin for hver node efter behov.

Følgende eksempel viser en basispris for et statisk antal på 899,95 EUR, som kan redigeres af en eller flere af følgende fem udtryksregler, afhængigt af den konfiguration, der er valgt af kunden:

- For hvid kabinetfinish fratrækkes 59,95 EUR.
- For hjørnebeskyttelse tillægges 35,95 EUR.
- For metalforgitter tillægges 89,95 EUR.
- For rosewood-kabinetfinish tillægges 119,95 EUR.
- Tillæg 12,95 EUR for hver enhed af højttalerhøjde.

![Eksempel på prismodel.](media/prod-config-rules-example.png "Eksempel på prismodel")

## <a name="add-support-for-multiple-currencies"></a>Tilføje understøttelse af flere valutaer

Når der sælges et produkt, der kan konfigureres, kontrollerer systemet, om priserne er udtrykkeligt angivet i kundens valuta. Hvis det er tilfældet, bruges de eksplicitte værdier. Hvis ikke, bruger systemet de valutakurser, der er oprettet for salgsfirmaet, for at omregne standardvalutaens værdi til kundens valuta.

Sådan tilføjer du eksplicitte priser i en ekstra valuta:

1. Åbn siden Rediger for prismodellen som beskrevet i [Oprette salgsprismodeller](#build-price-model).
1. Vælg knappen **Tilføj** i overskriften på prismodellen for at åbne dialogboksen **Valutaer**, der indeholder de tilgængelige valutaer.
1. Vælg den valuta, du vil tilføje, i dialogboksen **Valutaer**, og vælg derefter **OK**.
1. Rullelisten **Aktuel valuta** indeholder nu den valuta, du lige har tilføjet, plus eventuelle andre valutaer, der tidligere er tilføjet. Vælg den nye valuta, og læg mærke til, at gitteret i sektionen **Udtryksregler** nu indeholder to udtryksfelter:
    - **Udtryk** – Viser udtrykket (eller den konstante værdi) til søgning efter prisen ved hjælp af den valuta, der aktuelt er valgt som **Aktuel valuta**.
    - **Standardudtryk** – Viser udtrykket (eller den konstante værdi) til søgning efter prisen ved hjælp af standardvalutaen (vist i feltet **Standardvaluta**).

    > [!NOTE]
    > Feltet **Betingelse** for udtryksreglerne er "ejet" af standardvalutaen, hvilket betyder, at du ikke kan ændre betingelsen for andre valutaer. Du kan heller ikke tilføje nye udtryksregler, mens en anden valuta end standardvalutaen er valgt som **Aktuel valuta**.
1. Rediger værdierne i **Udtryk**-kolonnen efter behov til den aktuelle valuta.

I eksemplet nedenfor er _EUR_ standardvalutaen, og _USD_ er blevet tilføjet som en ekstra valuta.

![Eksempel på en model med flere valutaer.](media/prod-config-rules-currency-example.png "Eksempel på en model med flere valutaer")

> [!NOTE]
> Du kan ikke tilføje udtryksregler, der er entydige for en valuta, der ikke er standard. Hvis du vil oprette udtryksregler, der kun er relevante for en anden valuta end standardvalutaen, skal du angive prisudtrykket for standardvalutaen til nul. Angiv derefter det relevante udtryk for valutaen, der ikke er standard.

## <a name="test-your-price-model"></a>Teste prismodellen

Hvis du vil teste, hvordan salgspriserne fungerer i en konfigurationssession, skal du åbne siden Rediger for prismodellen, som det er beskrevet i [Oprette salgsprismodeller](#build-price-model) og derefter vælge **Test** i handlingsruden. Dialogboksen **Test produktmodel** åbnes, hvor du kan gøre følgende:

- Brug de konfigurationsindstillinger, der tilbydes her, til at vælge produktindstillinger og derefter se, hvordan de påvirker den værdi, der vises for **Pris og afsendelsesdato**.
- Vælg **Vis prisopdeling** for at hente et Excel-dokument, der indeholder detaljerede oplysninger om, hvordan prisen blev beregnet.

![Teste prismodellen.](media/prod-config-test.png "Teste prismodellen")

Det hentede regneark viser både den absolutte værdi og bidraget som en procentdel for hvert aktive priselement. Hvis du har valgt indstillingen **Tilknyt** for prismodellen på siden **Parametre til administration af produktoplysninger**, bliver dette Excel-ark tilknyttet ordre- eller tilbudslinjen.

![Excel-regneark, der viser prisopdeling.](media/prod-config-excel-example.png "Excel-regneark, der viser prisopdeling")

## <a name="set-up-selection-criteria-for-price-models"></a>Konfigurere udvælgelseskriterier for prismodeller

Når prismodellerne er på plads, skal du oprette mindst ét udvælgelseskriterium for at kunne hente prismodellen, når du konfigurerer tilbud eller ordrer. Det gør du ved at konfigurere en eller flere forespørgsler. I en kombination med tilsvarende salgsprismodeller giver forespørgslerne stor fleksibilitet ved målretning af salgspriser for bestemte kunder, områder, perioder og andre kriterier.

Sådan konfigurerer du udvælgelseskriterier for prismodeller:

1. Gå til **Administration af produktoplysninger \> Produkter \> Produktkonfigurationsmodeller**.
1. Vælg målproduktets konfigurationsmodel.
1. Åbn fanen **Model** i handlingsruden, og vælg **Prismodelkriterier** i gruppen **Konfigurer**. Siden **Prismodelkriterier** åbnes.
1. Hvis den forespørgselsrække, du skal bruge, ikke findes endnu, skal du vælge **Ny** i handlingsruden for at føje en ny række til gitteret og foretage følgende indstillinger for den:
    - **Navn** – Angiv et navn til denne række.
    - **Beskrivelse** - Beskriv kort forespørgslen, og hvad den er til.
    - **Prismodel** – Vælg en [prismodel](#build-price-model) (fra den aktuelle konfigurationsmodel), som forespørgslen skal anvende, når den udløses.
    - **Ordretype** – Vælg den type ordre, som forespørgslen skal gælde for.
    - **Gyldig fra** – Angiv den første dag, hvor forespørgslen skal gælde.
    - **Udløber senest** – Angiv den sidste dato, hvor forespørgslen gælder.

    ![Prismodelkriterier.](media/prod-config-price-model-criteria.png "Prismodelkriterier").

1. Vælg rækken for den forespørgsel, du vil definere, og vælg derefter **Rediger** i **handlingsruden**. Dialogboksen for forespørgselsdesigneren åbnes. Den fungerer som de fleste forespørgselsdesignere i Supply Chain Management. Brug den til at definere de betingelser, som prismodellen for den række, du har valgt, skal anvendes under.

1. Gentag trin 4-5 for hver forespørgsel, du ønsker.
    > [!TIP]
    > Du kan spare tid ved at kopiere en eksisterende række, der allerede ligner en ny, som du skal tilføje. Det gør du ved at vælge en destinationsrække og derefter vælge **Dupliker** i handlingsruden.

1. Når du er færdig med at definere kriterier, skal du arrangere dem i den rigtige rækkefølge på listen **Prismodelkriterier**. Hvis du vil flytte en række, skal du markere rækken og derefter vælge **Op** eller **Ned** i handlingsruden.

    > [!IMPORTANT]
    > På konfigurationstidspunktet starter systemet søgningen øverst på listen og bruger den første forespørgsel, der svarer til dataene på tilbuddet eller ordrelinjen. Du skal derfor placere de mest specifikke forespørgsler øverst. Hvis du placerer en generel forespørgsel øverst på listen, er det den, der bruges, selvom der kan være en forespørgsel længere nede på listen, der er rettet mod den nøjagtige kunde eller kundeemnet i konfigurationen.

## <a name="set-attribute-based-sales-prices-for-the-product-model-version"></a>Angive attributbaserede salgspriser for produktmodelversionen

Det sidste trin er at angive attributbaserede salgspriser for produktmodelversionen. Sådan gør du dette:

1. Gå til **Administration af produktoplysninger \> Produkter \> Produktkonfigurationsmodeller**.
1. Vælg målproduktets konfigurationsmodel.
1. Åbn fanen **Model** i handlingsruden, og vælg **Versioner** i gruppen **Oplysninger om produktmodel**.
1. Siden **Versioner** åbnes. Sørg for, at **Prissætningsmetode** er angivet til **Attributbaseret**.
    ![Angive pissætningsmetoden til attributbaseret.](media/prod-config-versions.png "Angive pissætningsmetoden til attributbaseret")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]