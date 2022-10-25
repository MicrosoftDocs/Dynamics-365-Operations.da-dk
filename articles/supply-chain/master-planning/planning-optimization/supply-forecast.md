---
title: Varedisponering med forsyningsprognoser
description: Denne artikel beskriver, hvordan forsyningsprognoser tages i betragtning under varedisponering.
author: t-benebo
ms.date: 09/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-21
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: dc83d10851958ec67166cb7e40cfd84dceae6651
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690075"
---
# <a name="master-planning-with-supply-forecasts"></a>Varedisponering med forsyningsprognoser

[!include [banner](../../includes/banner.md)]

Forsyningsprognoser giver dig mulighed for at angive den forsyning, du forventer at have brug for i en fremtidig periode. Du vil typisk basere estimatet på salgshistorikken for sidste år og derefter bruge prognosen til budgetteringsformål. Du kan også konfigurere behovsplaner, så du kan overveje budgetter under planlægning.

## <a name="set-up-a-master-plan-to-consider-supply-forecasts"></a>Oprette en behovsplan, der tager forsyningsprognoser i betragtning

Du kan angive, om hver behovsplan skal overveje prognoser, når den køres. Benyt følgende fremgangsmåde for at angive prognoseindstillinger for hver enkelt plan.

1. Gå til **Varedisponering \> Opsætning \> Planer \> Behovsplaner**.
1. Vælg enten en eksisterende behovsplan i listeruden, eller vælg **Ny** i handlingsruden for at oprette en ny.
1. I oversigtspanelet **Generelt** skal du indstille følgende felter:

    - **Budgetmodel** – Vælg den model, der indeholder de udbuds- og/eller efterspørgselsprognoser, der skal tages i betragtning af behovsplanen.
    - **Medtag forsyningsprognose** – Angiv denne indstilling til *Ja* for at medtage forsyningsprognoser i behovsplanen.
    - **Medtag behovsprognose** – Angiv denne indstilling til *Ja* for at medtage behovsprognoser i behovsplanen. Selvom denne indstilling er uafhængig af indstillingen **Medtag forsyningsprognose**, gælder nogle af de andre indstillinger på siden for både forsyningsprognoser og behovsprognoser. Du kan finde flere oplysninger om planlægning, der tager højde for behovsprognoser, i [Varedisponering med behovsprognoser](demand-forecast.md).
    - **Metode, der bruges til at reducere prognosekrav** – Vælg den metode, der skal bruges til at reducere prognosekravet i varedisponering:

        - *Ingen* – Prognosekrav reduceres ikke under varedisponering.
        - *Procent - reduktionsnøgle* – Prognosekravene reduceres i henhold til de procentandele og perioder, som er defineret i reduktionsnøglen.
        - *Transaktioner - reduktionsnøgle* – Prognosekravene reduceres af de transaktioner, som finder sted i løbet af de perioder, der er defineret i reduktionsnøglen.
        - *Transaktioner - dynamisk periode* – Prognosekravene reduceres med de faktiske ordretransaktioner, der finder sted i løbet af den dynamiske periode. Den dynamiske periode dækker de aktuelle prognosedatoer og slutter ved starten af den næste prognose. Metoden *Transaktioner – dynamisk periode* hverken bruger eller kræver en reduktionsnøgle, og når den bruges, gælder følgende betingelser:

            - Hvis prognosen reduceres helt, bliver prognosekravene for den aktuelle prognose 0 (nul).
            - Hvis der ikke er noget fremtidigt budget, bliver budgetbehovet fra det sidst angivne budget reduceret.
            - Tidshorisonter medtages i beregningen af budgetreduktionen.
            - Positive dage medtages i beregningen af budgetreduktionen.
            - Hvis de faktiske ordreposteringer overstiger budgetbehovet, overføres de resterende posteringer ikke til den næste budgetperiode.

        > [!NOTE]
        > Indstillingen **Metode, der er brugt til at reducere prognosebehovet**, gælder også for behovsprognoser, hvis du har aktiveret dem for behovsplanen, og den påvirker dem på samme måde. Du kan finde flere oplysninger under [Varedisponering med behovsprognoser](demand-forecast.md).

## <a name="set-reduction-options-for-coverage-groups"></a>Angive reduktionsindstillinger for disponeringsgrupper

Hvis du vil angive indstillinger, der styrer, hvordan en disponeringsgruppe skal reducere sine prognosebehov for behovsplaner, der bruger transaktionsbaseret reduktion, skal du følge disse trin.

1. Gå til **Varedisponering \> Opsætning \> Planer \> Disponeringsgrupper**.
1. Vælg enten en eksisterende dækningsgruppe i listeruden, eller vælg **Ny** i handlingsruden for at oprette en ny.
1. I feltet **Reducer prognose med** i oversigtspanelet **Andet** skal du angive, hvordan forsyningsprognosebehov skal reduceres prognoses for varer i dækningsgruppen for behovsplaner, hvor feltet **Metode, der er brugt til at reducere prognosebehovet** er angivet til *Transaktioner – reduktionsnøgle* eller *Transaktioner – dynamisk periode*. Vælg en af følgende værdier:

    - *Alle transaktioner* – Alle transaktioner skal reducere prognosen.
    - *Ordrer* – Det er kun ordrer af samme type, der skal reducere prognosen.

    Standardordreindstillingerne for en vare angiver f.eks., at den skal produceres. Der er en forsyningsprognoselinje for et antal på 50, og der er en eksisterende indkøbsordre for et antal på 20. Hvis feltet **Reducer budget med** er angivet til *Ordrer*, oprettes der et produktionsordreforslag for et antal på 50. Hvis den er angivet til *Alle transaktioner*, reduceres produktionsordreforslaget til et antal på 30.

    Denne indstilling gælder også for reduktion af behovsprognose. Du kan finde flere oplysninger under [Varedisponering med behovsprognoser](demand-forecast.md).

## <a name="enter-a-supply-forecast-for-a-product"></a>Angive en forsyningsprognose for et produkt

Benyt følgende fremgangsmåde for at angive en forsyningsprognose for et produkt.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Vælg det produkt, som du vil angive en prognose for.
1. Vælg **Plan** i handlingsruden, og vælg derefter **Forsyningsprognose**.
1. Vælg **Ny** i handlingsruden på siden **Forsyningsprognose** for at tilføje en prognose i gitteret.
1. Angiv de nødvendige oplysninger på den nye linje for at angive prognosen.

## <a name="plan-for-an-item-with-supply-forecast-lines"></a>Planlægge for en vare med forsyningsprognoselinjer

Når du kører en behovsplan, der indeholder en vare, som der findes en forsyningsprognose for, opretter systemet en indkøbsordre for de forsyningslinjer, der er angivet. Standardordreindstillingerne for varen overholdes. Hvis disse standardordreindstillinger angiver værdien **Indkøbsordre** som *Standardordretype*, og der ikke er angivet en kreditorkonto på forsyningsprognoselinjen, bruger systemet standardleverandøren for varen.

## <a name="check-whether-a-planned-order-is-a-supply-forecast-order"></a>Kontrollere, om et ordreforslag er en forsyningsprognoseordre

Benyt følgende fremgangsmåde for at finde ud af, om der er oprettet et ordreforslag som et resultat af en forsyningsprognose.

1. Gå til **Varedisponering \> Varedisponering \> Ordreforslag**.
1. Åbn det ordreforslag, som du vil inspicere.
1. Se værdien i feltet **Forsyningsprognose** i oversigtspanelet **Generelt**. Hvis ordren er oprettet for at dække en forsyningsprognose, angives dette felt til *Ja*.

## <a name="examples-of-master-planning-with-supply-forecasts"></a>Eksempler på varedisponering med forsyningsprognoser

Dette afsnit indeholder en række eksempler, der viser, hvordan forsyningsprognose påvirker varedisponering.

### <a name="example-1-supply-forecast-for-an-item"></a>Eksempel 1: forsyningsprognose for en vare

Du har en vare, hvor standardordretypen er *Indkøbsordre*, og standardleverandøren er *US-002*. Den har følgende forsyningsprognoselinje.

| Model    | Dato     | Leverandørkonto | Leverandørgruppe | Antal | Enhed | Sted | Lagersted |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 |                |              | 35       | styk   | 1    | 11        |

Når du kører varedisponering, oprettes der et indkøbsordreforslag for *35 styk* fra leverandøren *US-002*.

### <a name="example-2-several-supply-forecast-lines-with-and-without-a-vendor"></a>Eksempel 2: flere forsyningsprognoselinjer med og uden en leverandør

Du har en vare, hvor standardordretypen er *Indkøbsordre*, og standardleverandøren er *US-002*. Den har følgende forsyningsprognoselinjer.

| Model    | Dato     | Leverandørkonto | Leverandørgruppe | Antal | Enhed | Sted | Lagersted |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 |                |              | 35       | styk   | 1    | 11        |
| CurrentF | 10/10/22 | US-101         |              | 25       | styk   | 1    | 11        |

I dette tilfælde behandler systemet den linje, der ikke angiver en leverandør, som en generisk prognose, og det antages, at den linje, der angiver en leverandør, skal trækkes fra den generiske prognose. Varedisponering opretter derfor følgende indkøbsordreforslag for varen:

- Et indkøbsordreforslag på *25 styk* fra leverandør *US-101* (leverandøren og det antal, der er angivet på prognoselinjen, bruges).
- Et indkøbsordreforslag for et antal på *10 styk* fra leverandør *US-002* (da der ikke er angivet en leverandør på den anden prognoselinje, bruges standardleverandøren, og antallet i denne prognoselinje reduceres med antallet på den leverandørspecifikke prognoselinje).

### <a name="example-3-plans-that-use-the-transactions---dynamic-period-reduction-method-in-a-single-forecast-period"></a>Eksempel 3: Planer, der bruger metoden Posteringer - dynamisk periode som reduktion i en enkelt prognoseperiode

For behovsplaner , der bruger *Posteringer - dynamisk periode* som metode til prognosereduktion, vil varedisponering reducere prognoseantal, hvis der er eksisterende transaktioner, der svarer til disse forsyningskarakteristika.

Du kan f.eks. have en vare, hvor standardordretypen er *Indkøbsordre*. Den har følgende forsyningsprognoselinje.

| Model    | Dato     | Leverandørkonto | Leverandørgruppe | Antal | Enhed | Sted | Lagersted |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 | US-101         |              | 25       | styk   | 1    | 11        |

Da der kun er én forsyningsprognoselinje, er der kun én prognoseperiode.

Når du kører en behovsplan, der er konfigureret til at bruge *Posteringer – dynamisk periode* som reduktionsmetode, kan et af følgende resultater forekomme:

- Hvis der findes en indkøbsordre for leverandør *US-101* og antallet *10 styk*, og feltet **Forsyningsprognose** er angivet til *Ja*, opretter varedisponering et nyt indkøbsordreforslag for det resterende antal på *10 styk*. Prognoselinjen reduceres, da leverandøren matcher den eksisterende indkøbsordre.
- Hvis der findes en indkøbsordre for leverandør *US-102*, sted *1*, lagersted *11* og antallet *10 styk*, og feltet **Forsyningsprognose** er angivet til *Ja*, opretter varedisponering et nyt indkøbsordreforslag for det fulde antal på *25 styk*. Prognoselinjen kan ikke reduceres, da den har en anden leverandør end den eksisterende indkøbsordre.

> [!NOTE]
> Denne situation kan forekomme for indkøbsordreforslag, fordi der er knyttet en leverandør til dem. I forbindelse med flytteordrer og produktionsordrer reduceres forsyningsprognosebeløbene dog altid af eksisterende ordrer, da der ikke er angivet nogen leverandør for disse ordretyper.

### <a name="example-4-plans-that-use-the-transactions---dynamic-period-reduction-method-over-several-forecast-periods"></a>Eksempel 4: Planer, der bruger metoden Posteringer - dynamisk periode som reduktion i flere prognoseperioder

Du kan have en vare, hvor standardordretypen er *Indkøbsordre*. Den har følgende forsyningsprognoselinjer.

| Model    | Dato     | Leverandørkonto | Leverandørgruppe | Antal | Enhed | Sted | Lagersted |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 | US-101         |              | 25       | styk   | 1    | 11        |
| CurrentF | 15/10/22 | US-101         |              | 25       | styk   | 1    | 11        |

I dette eksempel er der to prognoselinjer, som hver har en særskilt dato. Datoerne fastsætter derfor grænserne for prognoseperioderne. Den første periode er fra 10. oktober til og med 14. oktober 2022 (10/10/22 – 14/10/22). Den anden er fra 15. oktober 2022 (15/10/22) og frem.

Der findes en eksisterende indkøbsordre for leverandør *US-101*, et antal på *10 styk* og datoen *12/10/22* (12. oktober 2022). Når du kører en behovsplan, der er konfigureret til at bruge *Posteringer – dynamisk periode* som reduktionsmetode, oprettes følgende ordrer:

- Et ordreforslag på *15 styk* og datoen *10/10/22* (antallet reduceres med den eksisterende indkøbsordre, der er dateret i samme prognoseperiode).
- Et ordreforslag på *25 styk* og datoen *15/10/22* (antallet er prognosens fulde antal).

### <a name="example-5-plans-that-use-no-reduction"></a>Eksempel 5: Planer uden reduktion

Når du kører en plan, hvor prognosereduktionsmetoden er *Ingen*, opretter varedisponering altid planlagt forsyning for alle forsyningsprognoselinjer. Når den planlagte forsyning er godkendt, reduceres de fremtidige ordreforslag. Indkøbsordrer reducerer dog ikke forsyningsprognoselinjerne.

Du kan f.eks. have en vare, hvor standardordretypen er *Indkøbsordre*. Den har følgende forsyningsprognoselinje.

| Model    | Dato     | Leverandørkonto | Leverandørgruppe | Antal | Enhed | Sted | Lagersted |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 | US-101         |              | 25       | styk   | 1    | 11        |

Der findes en eksisterende indkøbsordre for leverandør *US-101*, sted *1*, lagersted *11* et antal på *25 styk* og datoen *10/10/22*. 

Når du kører en behovsplan, der er konfigureret til at bruge *Ingen* som reduktionsmetode, opretter den et indkøbsordreforslag for leverandør *US-101*, sted *1*, lagersted *11*, et antal på *25 styk* og datoen *10/10/22*. Med andre ord reduceres den eksisterende indkøbsordre ikke, fordi prognosereduktionsmetoden er *Ingen*.

Du skal nu redigere det indkøbsordreforslag, der blev oprettet efter den seneste planlægningskørsel, og du skal ændre antallet til *15 styk*. Godkend derefter indkøbsordren. Næste gang du kører behovsplanen, opretter den et indkøbsordreforslag for leverandør *US-101*, sted *1*, lagersted *11*, et antal på *10 styk* og datoen *10/10/22*. Denne gang reduceres antallet, så det afspejler antallet i den eksisterende godkendte ordre fra den forrige planlægningskørsel.

## <a name="differences-between-planning-optimization-and-the-built-in-planning-engine"></a>Forskelle mellem Planlægningsoptimering og det indbyggede planlægningsprogram

Forsyningsprognoser fungerer lidt anderledes alt efter den brugte varedisponering (Planlægningsoptimering eller det indbyggede program). I dette afsnit beskrives forskellene.

### <a name="vendor-groups"></a>Kreditorgrupper

Når du tilføjer en prognoselinje, kan du angive en kreditor og en kreditorgruppe. I det indbyggede planlægningsprogram grupperes de oprettede ordreforslag efter kombinationen af værdierne for kreditor- og kreditorgruppe. I Planlægningsoptimering grupperes ordreforslag efter kreditor.

Følgende tabel indeholder nogle eksempler på forsyningsprognoselinjer for en vare.

| Model    | Dato     | Leverandørkonto | Leverandørgruppe | Antal | Enhed | Sted | Lagersted |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 |                | VendorGroupA | 5        | styk   | 1    | 11        |
| CurrentF | 10/10/22 |                | VendorGroupA | 6        | styk   | 1    | 11        |
| CurrentF | 10/10/22 |                |              | 7        | styk   | 1    | 11        |

Leverandør *VendorA* er standardleverandøren for leverandørgruppen *VendorGroupA*. Det er også standardleverandøren af varen.

Det indbyggede planlægningsprogram opretter følgende ordrer:

- Et indkøbsordreforslag for leverandør *VendorA*, leverandørgruppe *VendorGroupA* og et antal på *11*
- Et indkøbsordreforslag for leverandør *VendorA* og et antal på *7*

Planlægningsoptimering opretter kun én ordre:

- Et indkøbsordreforslag for leverandør *VendorA*, leverandørgruppe *VendorGroupA* og et antal på *18*

### <a name="reduction-of-general-forecasts-by-more-specific-forecasts"></a>Reduktion af generelle prognoser med mere specifikke prognoser

I det indbyggede program til varedisponering vil resultatet være uforudsigeligt, hvis nogle prognoser har en leverandør, mens andre ikke har.

I Planlægningsoptimering reduceres generelle prognoser altid med mere specifikke prognoser, som det fremgår af følgende eksempel.

Følgende tabel indeholder nogle eksempler på forsyningsprognoselinjer for en vare.

| Dato       | Antal | Kreditor   | Leverandørgruppe  |
|------------|----------|----------|---------------|
| 11/02/2022 | 5,00     | Vendor-A | VendorGroup-A |
| 11/02/2022 | 6,00     | Vendor-A | VendorGroup-A |
| 11/02/2022 | 15,00    |          |               |

Den generelle prognose (for 15 styk) reduceres med de mere specifikke prognoser (for 5 + 6 = 11 styk). Resten tildeles standardleverandøren. I følgende tabel vises ordreforslagene.

| Dato       | Antal | Kreditor   | Leverandørgruppe  |
|------------|----------|----------|---------------|
| 11/02/2022 | 11,00    | Vendor-A | VendorGroup-A |
| 11/02/2022 | 4,00     | Vendor-A | VendorGroup-A |

### <a name="respect-for-default-order-settings-when-planned-orders-are-generated"></a>Overholdelse af standardordreindstillinger, når der genereres ordreforslag

Hver vare kan have standardordreindstillinger som f.eks. et minimumsantal på indkøbsordren. I det indbyggede planlægningsprogram ignoreres disse indstillinger, og prognoser ændres derfor til ordreforslag, der har samme antal. Planlægningsoptimering overholder disse indstillinger, når der genereres ordreforslag ud fra forsyningsprognoser. 

### <a name="aggregation-of-planned-orders-as-a-result-of-reduction-by-approved-orders"></a>Aggregering af ordreforslag som følge af reduktion med godkendte ordrer

Det indbyggede varedisponeringsprogram antager, at kun én ordre reducerer den eksisterende forsyningsprognose. Hvis flere ordrer matcher en forsyningsprognoselinje, er det derfor kun den første ordre, der reducerer den. I Planlægningsoptimering reduceres den af alle ordrer, der matcher forsyningsprognoselinjen.

### <a name="reduction-of-forecasts-by-matching-vendors-only"></a>Reduktion af prognoser ved kun at matche leverandører

Når det indbyggede varedisponeringsprogram reducerer en prognose med eksisterende frigivne indkøbsordrer, sikrer det ikke, at leverandøren på indkøbsordren matcher leverandøren fra prognosen. Planlægningsoptimering reducerer kun prognoser med indkøbsordrer, der har en tilsvarende værdi i leverandørfeltet.

Ved flytteordrer og produktionsordrer ignoreres leverandørfeltet altid, da det ikke er relevant for disse ordretyper.

### <a name="reduction-of-forecasts-by-transfer-orders"></a>Reduktion af prognoser efter flytteordrer

Hvis standardordretypen for en vare er *Flytning*, kan prognoser kun reduceres af eksisterende planlagte flytteordrer. Men det er kun frigivne ordrer, der reducerer forsyningsprognosen for produktionsordrer og indkøbsordrer.

Det indbyggede planlægningsprogram reducerer for alle flytteordretilstande, hvorimod Planlægningsoptimering kun reducerer prognoser med flytteordrer i tilstanden *Frigivet*.
