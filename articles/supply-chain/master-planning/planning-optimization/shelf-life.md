---
title: Overordnet planlægning for produkter med begrænset hyldelevetid
description: Denne artikel beskriver, hvordan du kan konfigurere og bruge planlægningsfunktioner, der tager højde for hyldelevetid for letfordærvelige produkter.
author: t-benebo
ms.date: 08/10/2022
ms.topic: article
ms.search.form: ReqPlanSched, CustTable, EcoResProductDetailsExtended, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 68a1ba2bfe90aaf0462917c405d483fa12bf8126
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428215"
---
# <a name="master-planning-for-products-with-limited-shelf-life"></a>Overordnet planlægning for produkter med begrænset hyldelevetid

[!include [banner](../../includes/banner.md)]

Hyldelevetid er den tid, et produkt kan opbevares, indtil det ikke længere kan bruges eller sælges. For produkter med en begrænset hyldelevetid vil du sandsynligvis bruge et FEFO-lagerstedsstrategi (First-Expire, First-Out), som prioriterer forbruget og salget af varer ud fra den resterende hyldelevetid. Denne lagerstedsstrategi er relevant for fødevarer, mennesker og andre varer, der er kendetegnede ved kort opbevaringstid. Ifølge FEFO opbevares varer på lagerstedet som varer på en supermarkeds hylde: Produkter med en lang hyldelevetid placeres dyb i hylderne, så produkter, der har en kortere hyldelevetid, afsendes først.

## <a name="using-shelf-life-in-master-planning"></a>Bruge hyldelevetid i varedisponering

Dette afsnit indeholder en forklaring på, hvordan varedisponering foreslår levering af hyldelevetidsvarer.

Når du kører en behovsplan, genererer den forslag til ordreforslag (forsyning), der kan imødekomme behovet og minimere forsinkelserne. Hvis din plan omfatter varer med begrænset hyldelevetid, bliver planlægningsberegninger mere komplekse, da planen ikke kun skal minimere forsinkelserne, men også bruge eksisterende levering, før den udløber. Planen skal forsøge at bruge levering, der er tættest på udløbsdatoen, før levering udløber senere. Derfor søger behovsplanlægningen at opnå følgende mål i denne rækkefølge:

1. Minimere summen af forsinkelser.
1. Maksimér summen af FEFO-forsyning.
1. Minimere genopfyldningen af lageret.

I nogle tilfælde kan der være en konflikt mellem de første to mål, og der skal foretages et valg: Vil du udskyde en forsendelse, eller vil du bruge levering, der udløber senere i stedet for levering, der udløber før tid? For at løse denne konflikt under behovsplanlægningen prioriterer systemet minimerer forsinkelserne over brugen af leveringer, der snart udløber. Generelt opstår denne type konflikt, når der kan være forsinkelser og disponering efter periode. Det anbefales derfor, at du bruger en disponeringsperiode, der er kortere end hyldelevetiden for en vare. Andre typer disponering (f.eks. krav) er ønsker at møde denne type konflikt.

## <a name="set-up-shelf-life"></a>Konfigurere hyldelevetid

### <a name="configure-each-master-plan-to-consider-shelf-life"></a>Konfigurere hver behovsplan til at overveje hyldelevetid

Som standard tager behovsplaner ikke hyldelevetid med i betragtning. Du kan bruge følgende procedure til at aktivere beregning af hyldelevetid for hver behovsplan, der kræver dem.

1. Gå til **Varedisponering \> Opsætning \> Planer \> Behovsplaner**.
1. Vælg en behovsplan på listesiden, eller opret en ny.
1. I oversigtspanelet **Generelt** skal du angive indstillingen **Brug datoer for hyldelevetid** til *Ja*.

### <a name="configure-tracking-dimension-groups-to-track-the-batch-dimension"></a>Konfigurer sporingsdimensionsgrupper til sporing af batch-dimension

En vares hyldelevetid kan kun spores, hvis den pågældende vare spores på batchdimensionen. Det vil sige, at batchreferencen og de ønskede datoer skal registreres ved tilgang eller produktion og ved hver lagertransaktion for varen. Du kan administrere denne indstilling ved at oprette en eller flere sporingsdimensionsgrupper for at udføre den nødvendige sporing og derefter tildele de relevante varer til disse grupper efter behov.

Benyt følgende fremgangsmåde for at oprette en sporingsdimensionsgruppe til sporing af batchdimensionen.

1. Gå til **Administration af produktoplysninger \> Konfiguration \> Dimension og variantgrupper \> Sporing af dimensionsgrupper**.
1. Udfør ét af følgende trin:

    - Vælg **Ny** i handlingsruden for at oprette en ny sporingsdimensionsgruppe. Angiv navn og beskrivelse, og vælg **Gem** i handlingsruden.
    - Vælg den eksisterende sporingsdimensionsgruppe i listeruden, som du vil konfigurere til at spore batchdimensionen.

1. Marker afkrydsningsfelterne i kolonnerne for **aktivt** og **fysisk lager** i oversigtspanelet **Sporingsdimension** i rækken **Batchnummer**.

### <a name="set-up-shelf-life-for-a-product"></a>Konfigurere hyldelevetid for et produkt

Benyt følgende fremgangsmåde for at konfigurere hyldelevetid for et produkt.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Opret eller åbn det produkt, du vil konfigurere.
1. Hvis du vil bruge indstillingerne i oversigtspanelet **Generelt**, skal du indstille feltet **Sporingsdimensionsgruppe** til en sporingsdimensionsgruppe, der er konfigureret til at spore batchdimensionen. Du kan kun angive dette felt, når du opretter et produkt første gang. Du kan ikke ændre værdien for eksisterende produkter.
1. I oversigtspanelet **Administrer lager** skal du angive følgende felter:

    - **Hyldevejledningsperiode i dage** – Angiv den periode (i dage), som en batch af dette produkt skal kontrolleres for at sikre, at det er passende til forbrug eller videresalg. Værdien i dette felt føjes til *produktionsdatoen* for en batch for at bestemme *hyldevejledningsdatoen*. Du kan konfigurere systemet til at generere kvalitetsordrer, når en batch nærmer sig hyldeforslagsdatoen.
    - **Hyldelevetidsperiode i dage** – Angiv antallet af dage, før en batch af dette produkt udløber. Denne værdi føjes til *produktionsdatoen* for at fastlægge *udløbsdatoen*. Batchen betragtes som ubrugelig efter denne dato.
    - **Sidste før-periode i dage** – Angiv den periode (i dage), hvorefter en batch af dette produkt anses for stadig at være salgbar, men ikke længere kan bevare nogle af dets oprindelige egenskaber. Denne værdi føjes til *produktionsdatoen* for at fastlægge *bedst før-dato*. Du kan køre rapporter for at identificere lager, der har passeret bedst før-dato. 

### <a name="set-a-sellable-days-rule-for-each-customer"></a>Angive en regel for salgbare dage for hver debitor

Funktionen *salgbare dage* sikrer, at produkter fra en batch, der snart udløber, ikke sendes til kunder. Den sikrer desuden, at der stadig vil være et tilstrækkeligt antal salgbare dage efter levering, når produkterne sendes til en kunde.

Hvis du vil bruge funktionen salgbare dage, skal du definere antallet af salgbare dage, der gælder for hvert produkt (eller produktgruppe) for hver debitor. Du skal udføre processen manuelt, da der ikke findes nogen dataenhed for den.

Benyt følgende fremgangsmåde for at oprette salgbare dage for hvert produkt for hver debitor.

1. Gå til **Salg og marketing \> Kunder \> Alle kunder**.
1. Vælg og vælg den kunde, du vil konfigurere.
1. Gå til handlingsruden, og på fanen **Sælg** i gruppen **Konfigurer** vælges **Sælg \> Salgbare dage**.
1. På siden **Salgbare dage for debitor** viser gitteret eksisterende regler for salgbare dage for hvert produkt eller en produktgruppe. Brug knapperne i handlingsruden til at tilføje eller redigere rækker i gitteret efter behov. Der findes et **filter**, som kan hjælpe dig med at finde eksisterende rækker.
1. På hver række skal du angive følgende felter:

    - **Varekode** - Vælg en af følgende værdier for at angive omfanget af de varer, der påvirkes:

        - *Tabel* – Rækken gælder for en bestemt vare.
        - *Gruppe* – Rækken gælder for en bestemt varegruppe.
        - *Alle* – Rækken anvendes til alle varer.

    - **Varerelation** - Hvis du angiver feltet **Varekode** til *Tabel*, skal du vælge en bestemt vare. Hvis du har valgt **Gruppe** i feltet *Varekode*, skal du vælge en varegruppe. Hvis du vælger **Alle** som *Varekode*, er dette felt ikke tilgængeligt.
    - **Salgbare dage** – angiv det mindste antal dage, hvor kunden skal sælge tilsvarende produkter, før batchen udløber. Værdien for salgbare dage baseres på den ønskede modtagelsesdato (eller den bekræftede modtagelsesdato, hvis den er defineret) for de tilsvarende produkter på salgsordren.
    - *(Andre produktdimensioner)* – Hvis området for en række skal begrænses yderligere, skal du angive andre dimensionsværdier (f.eks. **Størrelse** og **Farve**) efter behov. Vælg **Vis dimensioner** i handlingsruden for at vælge de ekstra dimensioner, der vises.

### <a name="set-up-all-relevant-products-so-that-they-are-fefo-date-controlled"></a>Konfigurere alle relevante produkter, så de er FEFO-datokontrollerede

Ved salgbare arbejdsdage skal hver relevant vare tilhøre en varemodelgruppe, hvor afkrydsningsfeltet **datokontrolleret FEFO** er markeret.

Benyt følgende fremgangsmåde for at oprette en varemodelgruppe, så den understøtter funktionen salgbare dage.

1. Gå til **Lagerstyring \> Opsætning \> Lagerbeholdning \> Varemodelgrupper**.
1. Vælg en eksisterende gruppe på listen, eller opret en ny ved at vælge **Ny** i handlingsruden.
1. I oversigtspanelet **Lagerpolitikker** skal du markere afkrydsningsfeltet **FEFO-datokontrolleret**.
1. Angiv de andre felter efter behov.

Benyt følgende fremgangsmåde for at få vist eller angive den varemodelgruppe, som et produkt tilhører.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Åbn det produkt, som du vil inspicere eller redigere.
1. Angiv feltet **Varemodelgruppe** i oversigtspanelet **Generelt** til en gruppe, hvor afkrydsningsfeltet, der er **datokontrolleret under FEFO**, er markeret.

## <a name="example-1-simple-fefo-10-day-period-zero-days-of-lead-time"></a>Eksempel 1: Simpel FEFO, 10-dagesperiode, nul dage i gennemløbstid

Dette eksempel viser et grundlæggende eksempel på hyldelevetid, hvor udligning mellem forsyningsordrerne og efterspørgslen udføres for at opfylde følgende systemmål:

- Minimere summen af forsinkelser.
- Maksimér summen af FEFO-forsyning.
- Minimere genopfyldningen af lageret.

Systemet har følgende indstillinger for vare- og behovsplan:

- **Disponeringskode (genopfyldningsstrategi):** Periode 
- **Disponeringsperiode:** 10 dage (lig med hyldelevetiden)
- **Hyldelevetid:** 10 dage
- **Salgbare dage:** 0 dage
- **Leveringstid:** 0 dage
- **Negative dage:** 0 dage
- **Ordreforslagstype (standardordreindstillinger for varen):** Indkøbsordre

Der findes følgende salgsordrer for varen i systemet:

- **SO1:** Antal (antal) = 2, ønsket leveringsdato = i dag + 1 dag
- **SO2:** Antal = 1, ønsket leveringsdato = i dag + 4 dage
- **SO3:** Antal = 1, ønsket leveringsdato = i dag + 5 dage

Alle disse salgsordrer opretter efterspørgsel efter varen.

Der findes følgende leveringer for varen:

- **Lagerbeholdning:** Antal = 1, udløbsdato = dags dato + 5 dage
- **Indkøbsordre 1 (PO1):** Modtagelsesdato = i dag + 2 dage, antal = 1, udløbsdato = i dag + 4 dage

Systemet opretter en liste over leveringer, der kan dække denne efterspørgsel, og sorterer listen efter udløbsdato (ved hjælp af FEFO).

Ved behovsplanlægning oprettes den nødvendige udligning mellem udbud og efterspørgsel. Den opretter også en behovsefterspørgsel på basis af leveringslisten (ved hjælp af FEFO) og tager tilgængelighedsdatoen med i vurdering.

- SO1 kan opfyldes med det disponible antal, men det kan ikke opfyldes i INDKØBSORDRE1, da tilgængelighedsdatoen for INDKØBSORDRE1 er én dag senere end SO1 kræver. SO1 genererer derfor behovet for én vareenhed.
- SO2 kan dækkes af indkøbsordre1, da PO1 ankommer inden det ønskede tidspunkt, og udløbsdatoen stadig er gyldig. SO2-kravet er derfor fuldt dækket af PO1.
- SO3 er ikke dækket, da ressourcer ikke er tilgængelige. SO3 genererer derfor behovet for én vareenhed.

Hvis du vil dække alle de resterende behov, skal systemet oprette følgende indkøbsordreforslag:

- **PPO1:** Modtagelsesdato = i dag, antal = 2, udløbsdato = i dag + 10 dage

I følgende tabel vises en oversigt over resultatet.

| Efterspørgsel | Udligning |
|---|---|
| **SO1:** Leveringsdato = i dag + 1 dag, antal = 2 | <p>**Lagerbeholdning:** Antal = 1, udløbsdato = i dag + 5 dage</p><p>**PPO1:** Modtagelsesdato = i dag, antal = 1, udløbsdato = i dag + 10 dage</p> |
| **SO2:** Leveringsdato = i dag + 4 dage, antal = 1 | **PO1:** Modtagelsesdato = i dag, 2 dage, i antal, udløbsdato = i dag + 4 dage |
| **SO3:** Leveringsdato = i dag + 5 dage, antal = 1 | **PPO1:** Modtagelsesdato = i dag, antal = 2, udløbsdato = i dag + 10 dage |

I følgende illustration vises, hvordan tidslinjen ser ud i dette eksempel.

![Eksempel 1: Simpel FEFO, 10-dagesperiode, nul dage i gennemløbstid.](media/fefo-example-1.png "Eksempel 1: Simpel FEFO, 10-dagesperiode, nul dage i gennemløbstid")

## <a name="example-2-simple-fefo-requirement-three-days-of-lead-time"></a>Eksempel 2: Simpel FEFO, krav, tre dage i gennemløbstid

Dette eksempel viser, hvordan systemets forsøg på at minimere forsinkelser kan medføre, at der opstår overordre.

Systemet har følgende indstillinger for vare- og behovsplan:

- **Disponeringskode (genopfyldningsstrategi):** Krav
- **Hyldelevetid:** 10 dage
- **Salgbare dage:** 0 dage
- **Gennemløbstid:** Fastlagt af følgende samhandelsaftaler med leverandører:

    - **Handelsaftale 1:** Hvis antal = 1, leveringstid = 4
    - **Handelsaftale 2:** Hvis antal = 2, leveringstid = 3

- **Negative dage:** 0 dage
- **Ordreforslagstype (standardordreindstillinger for varen):** Indkøbsordre

Der findes følgende salgsordrelinjer i systemet:

- **SO1:** Antal = 2, ønsket leveringsdato = i dag + 3 dage

Denne efterspørgsel dækkes af det eksisterende udbud og en bekræftet indkøbsordre:

- **Lagerbeholdning:** Tilgængelig = i dag, antal = 1, udløbsdato = i dag + 2 dage
- **PO1:** Modtagelsesdato = i dag, 3 dage, antal = 1, udløbsdato = i dag + 4 dage

SO1 kan ikke opfyldes med den lagerbeholdning, da lagerudløbsdatoen ligger før afsendelsesdatoen. PO1 kan dække SO1-kravet med et antal på kun 1. SO1 genererer derfor behovet for én vareenhed. For at dække dette krav opretter systemet et indkøbsordreforslag (PPO1).

Systemet har to samhandelsaftaler (en for antal = 1, gennemløbstid = 4 dage, og en for antal = 2, gennemløbstid = 3 dage). Systemet forsøger derfor at minimere forsinkelserne ved at oprette et indkøbsordreforslag (PPO1), der opfylder den anden samhandelsaftale. Resultatet er en overlevering (antal = 2, udløbsdato = i dag + 10 dage).

I følgende tabel vises en oversigt over resultatet.

| Efterspørgsel | Udligning |
|---|---|
| **SO1:** Leveringsdato = i dag + 3 dage, antal = 2 | <p>**PO1:** Modtagelsesdato = i dag, 3 dage, antal = 1, udløbsdato = i dag + 4 dage</p><p>**PPO1:** Modtagelsesdato = i dag, 3 dage, antal = 1, udløbsdato = i dag + 10 dage</p> |

I følgende illustration vises, hvordan tidslinjen ser ud i dette eksempel.

![Eksempel 2: Simpel FEFO, krav, tre dage i gennemløbstid.](media/fefo-example-2.png "Eksempel 2: Simpel FEFO, krav, tre dage i gennemløbstid")

## <a name="example-3-simple-fefo-requirement-three-days-of-lead-time-five-sellable-days"></a>Eksempel 3: Simpel FEFO, krav, tre dage i gennemløbstid, fem salgbare dage

Dette eksempel viser, hvordan hyldelevetid fungerer, når der tilføjes salgbare dage for en vare.

Systemet har følgende indstillinger for vare- og behovsplan:

- **Disponeringskode (genopfyldningsstrategi):** Krav
- **Hyldelevetid:** 10 dage
- **Salgbare dage:** 5 dage
- **Leveringstid:** 5 dage
- **Negative dage:** 0 dage
- **Ordreforslagstype (standardordreindstillinger for varen):** Indkøbsordre

Der findes følgende salgsordrer i systemet:

- **SO1:** Antal = 2, ønsket leveringsdato = i dag + 2 dage
- **SO2:** Antal = 1, ønsket leveringsdato = i dag + 3 dage
- **SO3:** Antal = 1, ønsket leveringsdato = i dag + 5 dage

Denne efterspørgsel kan være dækket af det eksisterende udbud og en bekræftet indkøbsordre:

- **Lagerbeholdning:** Tilgængelig = i dag, antal = 1, udløbsdato = i dag + 6 dage
- **PO1:** Modtagelsesdato = i dag, 2 dage, antal = 3, udløbsdato = i dag + 10 dage

Systemet opretter en liste over udligningslande ud fra FEFO-liste og tilgængelighedsdatoer. SO1 kan derfor ikke opfyldes af den lagerbeholdning, da lageret udløber inden afslutningen af de salgbare dage, som kunden har brug for (ønsket modtagelsesdato + 5 dage). PO1 kan dække SO1-kravet med to enheder og SO2-kravet med én enhed. Derfor er det kun SO3, der stadig har afset behovet for én vareenhed. For at dække dette krav opretter systemet følgende planlagte indkøbsordre:

- **PP01:** Modtagelsesdato = i dag, 5 dage, antal = 1, udløbsdato = i dag + 10 dage

I følgende tabel vises en oversigt over resultatet.

| Efterspørgsel | Udligning |
|---|---|
| **SO1:** Leveringsdato = i dag + 2 dage, antal = 2 | **PO1:** Modtagelsesdato = i dag, 2 dage, antal = 2, udløbsdato = i dag + 10 dage |
| **SO2:** Leveringsdato = i dag + 3 dage, antal = 1 | **PO1:** Modtagelsesdato = i dag, 2 dage, antal = 1, udløbsdato = i dag + 10 dage |
| **SO3:** Leveringsdato = i dag + 5 dage, antal = 1 | **PPO1:** Modtagelsesdato = i dag, 5 dage, antal = 1, udløbsdato = i dag + 10 dage |

I følgende illustration vises, hvordan tidslinjen ser ud i dette eksempel.

![Eksempel 3: Simpel FEFO, krav, tre dage i gennemløbstid, fem salgbare dage.](media/fefo-example-3.png "Eksempel 3: Simpel FEFO, krav, tre dage i gennemløbstid, fem salgbare dage")

## <a name="example-4-simple-fefo-period-lead-time-depends-on-the-quantity"></a>Eksempel 4: Simpel FEFO, periode, gennemløbstid afhænger af antallet

Dette eksempel viser, hvordan systemets forsøg på at minimere forsinkelser kan medføre, at der opstår overordre.

Systemet har følgende indstillinger for vare- og behovsplan:

- **Disponeringskode (genopfyldningsstrategi):** Periode
- **Disponeringsperiode:** 10 dage (lig med hyldelevetiden)
- **Hyldelevetid:** 10 dage
- **Salgbare dage:** 0 dage
- **Gennemløbstid:** Fastlagt af følgende samhandelsaftaler med leverandører:

    - **Handelsaftale 1:** Hvis antal = 1, leveringstid = 5
    - **Handelsaftale 2:** Hvis antal = 2, leveringstid = 0

- **Negative dage:** 0 dage
- **Ordreforslagstype (standardordreindstillinger for varen):** Indkøbsordre

Der findes følgende salgsordrer i systemet:

- **SO1:** Antal = 1, ønsket leveringsdato = i dag
- **SO2:** Antal = 1, ønsket leveringsdato = i dag + 6 dage

Denne efterspørgsel kan dækkes delvist af eksisterende levering fra følgende bekræftede indkøbsordrer:

- **PO1:** Modtagelsesdato = i dag, 1 dage, antal = 1, udløbsdato = i dag + 2 dage
- **PO2:** Modtagelsesdato = i dag, 3 dage, antal = 1, udløbsdato = i dag + 7 dage

Systemet har to samhandelsaftaler (en for antal = 1, gennemløbstid = 5 dage, og en for antal = 2, gennemløbstid = 0 dage). Systemet forsøger derfor at minimere forsinkelse ved at oprette følgende indkøbsordreforslag, der opfylder den anden samhandelsaftale:

- **PP01:** Modtagelsesdato = i dag, antal = 2, udløbsdato = i dag + 10 dage

SO1 dækkes af én enhed fra PPO1. SO2 dækkes af INDKØBSORDRE2, da PO2 udløber før PPO1.

I følgende tabel vises en oversigt over resultatet.

| Efterspørgsel | Udligning |
|---|---|
| **SO1:** Leveringsdato = i dag, antal = 1 | **PPO1:** Modtagelsesdato = i dag, antal = 1, udløbsdato = i dag + 10 dage |
| **SO2:** Leveringsdato = i dag + 6 dage, antal = 1 | **PO2:** Modtagelsesdato = i dag, 3 dage, antal = 1, udløbsdato = i dag + 7 dage |

> [!NOTE]
> INDKØBSORDRE1 bruges ikke, da den ankommer for sent til S01 og udløber før S02 leveres. PPO1 har overordret pr. enhed for at gøre leveringstiden 0 (nul), pr. samhandelsaftale 2.

I følgende illustration vises, hvordan tidslinjen ser ud i dette eksempel.

![Eksempel 4: Simpel FEFO, periode, gennemløbstid afhænger af antallet.](media/fefo-example-4.png "Eksempel 4: Simpel FEFO, periode, gennemløbstid afhænger af antallet")

## <a name="example-5-simple-fefo-requirement-10-negative-days"></a>Eksempel 5: Simpel FEFO, behov, 10 negative dage

Dette eksempel viser, hvordan hyldelevetid fungerer, når der tilføjes et stort antal negative dage for en vare. Negative dage er det antal dage, du er villig til at vente, før du bestiller en ny genopfyldning, når du har negativ lagerbeholdning. Systemet opretter ikke levering, medmindre antallet af negative dage overskrides.

Systemet har følgende indstillinger for vare- og behovsplan:

- **Disponeringskode (genopfyldningsstrategi):** Krav
- **Leveringstid:** 0 dage
- **Negative dage:** 10 dage
- **Ordreforslagstype (standardordreindstillinger for varen):** Indkøbsordre

Der findes følgende salgsordrelinjer i systemet:

- **SO1:** Antal = 1, ønsket leveringsdato = i dag

Denne efterspørgsel kan dækkes af eksisterende levering fra følgende bekræftet indkøbsordre:

- **PO1:** Modtagelsesdato = i dag, 3 dage, antal = 1, udløbsdato = i dag + 5 dage

Da systemet er konfigureret til at tillade 10 negative dage, dækker det behovet i SO1 ved hjælp af PO1, selvom resultatet bliver en forsinkelse på tre dage, fordi SO1 opretter negativt lager, indtil PO1 ankommer. Der oprettes ikke et indkøbsordreforslag, selvom leveringstiden er 0 (nul), og oprettelsen af et indkøbsordreforslag reducerer forsinkelserne.

I følgende tabel vises en oversigt over resultatet.

| Efterspørgsel | Udligning |
|---|---|
| **SO1:** Leveringsdato = i dag, antal = 1 | **PO1:** Modtagelsesdato = i dag, 3 dage, antal = 1, udløbsdato = i dag + 5 dage |

I følgende illustration vises, hvordan tidslinjen ser ud i dette eksempel.

![Eksempel 5: Simpel FEFO, behov, 10 negative dage.](media/fefo-example-5.png "Eksempel 5: Simpel FEFO, behov, 10 negative dage")

## <a name="example-6-simple-fefo-requirement-five-negative-days"></a>Eksempel 6: Simpel FEFO, behov, fem negative dage

Dette eksempel viser, hvordan hyldelevetid fungerer, når antallet af negative dage for en vare er mindre end varens hyldelevetid.

Systemet har følgende indstillinger for vare- og behovsplan:

- **Disponeringskode (genopfyldningsstrategi):** Krav
- **Salgbare dage:** 0 dage
- **Leveringstid:** 0 dage
- **Negative dage:** 5 dage
- **Ordreforslagstype (standardordreindstillinger for varen):** Indkøbsordre

Der findes følgende salgsordrelinjer i systemet:

- **SO1:** Antal = 2, ønsket leveringsdato = i dag

Denne efterspørgsel kan dækkes af eksisterende levering fra følgende bekræftet indkøbsordrer:

- **PO1:** Modtagelsesdato = i dag, antal = 1, udløbsdato = i dag + 1 dag
- **PO2:** Modtagelsesdato = i dag, 2 dage, antal = 1, udløbsdato = i dag + 3 dage

Systemet skal dog overholde den begrænsning, som afsendte varer ikke kan være udløbet på tidspunktet for afsendelse. Derfor kan PO2 og PO1 ikke begge bruges til SO1, da PO1 udløber, før PO2 ankommer. Systemet opretter følgende planlagte indkøbsordre for at afslutte med at dække dette krav for SO1:

- **PPO1:** Modtagelsesdato = i dag, antal = 1, udløbsdato = i dag + 10 dage

Systemet kan udnytte de fem negative dage og bruge PO2 og PPO1 til at dække SO1. Denne tilgang vil dog medføre, at leveringen forsinkes, indtil PO2 ankommer, og PO1 udløber i mellemtiden. Systemet dækker derfor SO1 ved hjælp af PPO1 og PO1.

I følgende tabel vises en oversigt over resultatet.

| Efterspørgsel | Udligning |
|---|---|
| **SO1:** Leveringsdato = i dag, antal = 2 | <p>**PO1:** Modtagelsesdato = i dag, antal = 1, udløbsdato = i dag + 1 dag</p><p>**PPO1:** Modtagelsesdato = i dag, antal = 1, udløbsdato = i dag + 10 dage</p> |

I følgende illustration vises, hvordan tidslinjen ser ud i dette eksempel.

![Eksempel 6: Simpel FEFO, behov, fem negative dage.](media/fefo-example-6.png "Eksempel 6: Simpel FEFO, behov, fem negative dage")
