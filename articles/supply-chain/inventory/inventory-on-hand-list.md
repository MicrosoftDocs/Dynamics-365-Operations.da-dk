---
title: Listen Disponibel lagerbeholdning
description: Dette emne beskriver, hvordan du bruger den disponible listeside til at inspicere oplysninger om disponibel lagerbeholdning. Det viser et par af de måder, som de forskellige filtrerings- og sorteringsindstillinger fungerer sammen på, og hvordan disse indstillinger undertiden kan give uventede resultater, når de kombineres.
author: sherry-zheng
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventOnhandItem, InventOnHandItemListPage, WHSOnHand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: cd90b3c8b84aa969f93015f8c953105db1636902c7dcf1d3150356284efa302b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780216"
---
# <a name="inventory-on-hand-list"></a>Listen Disponibel lagerbeholdning

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du bruger siden **Beholdningsliste** til at inspicere oplysninger om disponibel lagerbeholdning. Det viser et par af de måder, som de forskellige filtrerings- og sorteringsindstillinger fungerer sammen på, og hvordan disse indstillinger undertiden kan give uventede resultater, når de kombineres.

## <a name="query-your-on-hand-inventory"></a>Forespørgsel på dit disponible lager

Hvis du vil kontrollere tilgængeligheden af lager, skal du gå til **Lagerstyring \> Forespørgsler og rapporter \> Beholdningsliste**.

Siden **Beholdningsliste** opdateres automatisk, når der foretages transaktioner på lageret. Disse transaktioner kan være budgetterede, fysiske eller økonomiske transaktioner.

Brug følgende værktøjer til at finde frem til det sæt produkter, du søger efter:

- I handlingsruden skal du vælge [**Dimensioner**](#dimensions) for at åbne en dialogboks, hvor du kan tilføje eller fjerne de kolonner, der vises i gitteret **Beholdning**.
- I ruden [**Filtre**](#filters-pane) skal du angive værdier for bestemte felter, så der kun vises poster, der svarer til disse værdier. Bemærk, at filtre, som du definerer her, gælder for kildetabeller, der kan samles senere i henhold til de dimensioner, du har valgt at få vist. Du kan finde oplysninger om, hvordan denne funktionsmåde kan påvirke resultaterne, under [eksemplerne](#examples) senere i dette emne.
- I ruden **Filtre** skal du vælge **Anvend** for at generere en liste med tilsvarende disponibel lagerbeholdning i gitteret **Disponibel**.
- I gitteret **Disponibel** skal du vælge en kolonneoverskrift for at sortere eller filtrere efter værdier i den pågældende kolonne. Et QuickFilter øverst i gitteret giver yderligere filtreringsmuligheder. Disse filtre gælder for resultaterne, ikke for kildetabellerne. Du kan finde oplysninger om, hvordan denne funktionsmåde kan påvirke resultaterne, under [eksemplerne](#examples) senere i dette emne.

For hver tilsvarende vare indeholder gitteret **Beholdning** følgende kolonner med lageroplysninger.

| Kolonne | Beskrivende tekst |
|---|---|
| Fysisk lager | Den fysiske mængde, der er tilgængelig på lageret. |
| Fysisk reserveret | Samlet antal, der er reserveret fysisk. |
| Fysisk disponibelt | Den tilgængelige (ikke reserverede) mængde, der er tilgængelig på det fysiske lager.<p>**Fysisk disponibelt** er et beregnet felt. Værdien er lig med den **Fysiske lager**-værdi minus den **Fysisk reserverede**-værdi.</p> |
| Fysisk disponibelt på ekstra dimensioner | Det fysisk disponible antal for alle de dimensioner, der vises i gitteret. |
| Bestilt i alt | Det samlede antal, der er medtaget i indgående ordrer, eller som har et positivt antal i forskellige lagerkladder. |
| I bestilling | Det samlede antal, der er medtaget i udgående ordrer, eller som har et negativt antal i forskellige lagerkladder. |
| Bestilt reserveret | Samlet antal, der er reserveret på bestilte tilgange. Værdien i dette felt repræsenterer det samlede antal varer i udgående transaktioner, der har status som _Bestilt reserveret_. Varer, der er reserveret som bestilt, er ikke fysisk disponible på lageret. Derfor kan de ikke plukkes og leveres direkte. |
| Disponibel til reservation | Det totale antal disponibelt lager, der kan reserveres.<p>**Bemærk:** Hvis afkrydsningsfeltet **Reservér bestilte varer** er markeret på siden **Parametre for lager og lokalitetsstyring**, omfatter værdien i dette felt forventede tilgange. Hvis afkrydsningsfeltet ikke er markeret, omfatter værdien ikke forventede tilgange.</p> |
| I alt disponibelt | Disponibelt antal i alt.<p>**I alt disponibelt** er et beregnet felt. Værdien er lig med den **Fysisk disponibelt**-værdi plus **Bestilt i alt**-værdi minus **I bestilling**-værdien.</p> |

## <a name="apply-filters-to-find-the-records-that-youre-looking-for"></a><a name="filters-pane"></a>Anvende filtre til at finde de poster, du søger efter

Du kan bruge ruden **Filtre** til at filtrere den disponible lagerbeholdning, så den kun medtager poster, hvor feltværdierne svarer til filtreringskriterierne. Hvis du vil definere et filter, skal du udføre disse trin.

1. Find det felt, du vil filtrere efter, i ruden **Filtre**.
2. Vælg en logisk operator (f.eks. *starter med*, *er lig med* eller *er større end*) i feltet under navnet på målfeltet.
3. Vælg eller indtast den værdi, du vil søge efter.

> [!IMPORTANT]
> Siden **Beholdningsliste** samles fra en detaljeret disponibel lagerbeholdningstabel, der omfatter alle tilgængelige dimensioner. Listen på denne side er dog en oversigt. Derfor kan den kombinere rækker fra kildetabellen ved at aggregere værdier i henhold til de viste dimensioner.
>
> De filtre, du definerer i ruden **Filtre**, gælder for kildetabellen, ikke den samlede liste. Denne funktionsmåde kan undertiden give uventede resultater. Du kan finde oplysninger om, hvordan denne funktionsmåde kan påvirke resultaterne, under [eksemplerne](#examples) senere i dette emne.
> 
> De [filtre, der findes i gitteret](#grid-filters), *bliver* anvendt på den samlede liste. Disse filtre omfatter både QuickFilter øverst i gitteret og filteret for hver kolonneoverskrift.

Du kan redigere det sæt filtre, der er tilgængeligt i ruden **Filtre**, ved at følge disse trin.

- Hvis du vil fjerne et filter fra ruden, skal du vælge dets **Luk**-knap (**X**).
- Hvis du vil tilføje et filter, skal du vælge **Tilføj** øverst i **Filtre**-ruden. Dialogboksen **Tilføj filterfelter**, der vises, har en liste over de tilgængelige felter. Den indeholder også oplysninger om datatypen og tabellen for hvert felt. Brug kolonneoverskrifterne til at filtrere og sortere listen efter behov, og markér derefter afkrydsningsfeltet for hvert felt, du vil føje til **Filter**-ruden. Når du er færdig, skal du vælge **Indsæt** for at anvende ændringerne.

## <a name="select-which-dimensions-to-show"></a><a name="dimensions"></a>Vælg, hvilke dimensioner der skal vises

Dimensioner fortæller dig mere om de enkelte varer på listen over disponible lagerbeholdninger og giver dig flere muligheder for at sortere og filtrere listen. De dimensioner, du vælger at få vist, har også indflydelse på, hvordan rækker samles på siden **Beholdningsliste**. Denne aggregering kan påvirke, hvordan rækker fra kildetabellerne kombineres i de resultater, du får vist. Du kan finde oplysninger om, hvordan denne funktionsmåde kan påvirke resultaterne, under [eksemplerne](#examples) senere i dette emne.

Benyt følgende fremgangsmåde for at tilpasse det udvalg af lagerdimensioner, der vises.

1. Vælg **Dimensioner** i handlingsruden.

    Dialogboksen **Dimensionsvisning** vises med hver enkelt dimension.

2. Markér afkrydsningsfeltet for hver dimension, der skal inkluderes i gitteret.
3. Hvis du ønsker, at dit valg skal bruges som standard, næste gang du åbner siden **Beholdningsliste**, skal du angive indstillingen **Gem opsætning** til **Ja**. Hvis du angiver denne indstilling til **Nej**, vil dit valg kun blive brugt i den aktuelle session. Derfor bruges det aktuelle standardvalg, næste gang du åbner siden.
4. Vælg **OK** for at anvende dine ændringer og lukke dialogboksen.

## <a name="filter-on-the-output-of-the-inventory-on-hand-list"></a><a name="grid-filters"></a>Filtrere på afgang fra lagerbeholdningslisten

I gitteret **Disponibel** kan du vælge enhver kolonneoverskrift for at sortere eller filtrere efter værdier i den pågældende kolonne. Et QuickFilter øverst i gitteret giver yderligere filtreringsmuligheder. Disse filtre gælder for resultaterne, ikke for kildetabellerne. Du kan finde oplysninger om, hvordan denne funktionsmåde kan påvirke resultaterne, under [eksemplerne](#examples) senere i dette emne.

> [!NOTE]
> Du kan ikke filtrere og sortere efter alle kolonner. De fleste af antalskolonnerne inkluderer ikke sorterings- og filtreringskontrolelementer, fordi de er beregnede felter. Kolonnen **I bestilling** er en undtagelse.

## <a name="examples"></a><a name="examples"></a>Eksempler

Systemet indeholder en detaljeret (ikkesamlet) lagertabel, der viser følgende disponible lagerbeholdning.

| Varenummer | Lokation | Lagersted | Fysisk lager | Fysisk disponibelt |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 2 | 2 | 2 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-1"></a>Scenario 1

Siden **Beholdningsliste** er konfigureret til at vise følgende endelige dimensioner:

- varenummer
- Lokation
- Lagersted

I ruden **Filtre** konfigureres følgende filtreringskriterier:

- **Varenummer** \| **er nøjagtigt** \| _IA0001_
- **Fysisk disponibelt** \| **er mindre end eller lig med** \| _1_

Her vises resultatet.

| Varenummer | Lokation | Lagersted | Fysisk lager | Fysisk disponibelt |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-2"></a>Scenario 2

Siden **Beholdningsliste** er konfigureret til at vise følgende endelige dimensioner:

- varenummer
- Lokation

I ruden **Filtre** konfigureres følgende filtreringskriterier:

- **Varenummer** \| **er nøjagtigt** \| _IA0001_
- **Fysisk disponibelt** \| **er mindre end eller lig med** \| _1_

Her vises resultatet.

| Varenummer | Lokation | Fysisk lager | Fysisk disponibelt |
|---|---|---|---|
| IA0001 | 1 | 2 | 2 |

Bemærk, at indstillingerne i ruden **Filtre** gælder for den detaljerede (ikkesamlede) lagertabel, der vises i starten af dette afsnit. Derfor finder kriteriet **Fysisk disponibelt** \| **er mindre end eller lig med** \| _1_ to rækker fra den pågældende tabel (første og tredje række, der hver især viser en **Fysisk disponibelt**-værdi af _1_). Men i dette scenarie siden **Beholdningsliste** ikke konfigureret til at vise **Lagersted-**-dimensionen. Derfor samles de to oprindelige rækker i en enkelt resultatrække, da begge rækker har identiske værdier i alle de viste dimensioner. Denne række ser ud til at overtræde filtreringskriteriet, fordi **Fysisk disponibelt**-værdien vises som _2_. Resultatet er dog korrekt, da indstillingerne i ruden **Filtre** gælder for kildetabellen og ikke i den samlede tabel, der vises på siden **Beholdningsliste**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]