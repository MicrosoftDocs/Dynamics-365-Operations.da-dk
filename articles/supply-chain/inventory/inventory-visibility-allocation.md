---
title: Allokering af Inventory Visibility-slager
description: Denne artikel forklarer, hvordan du opretter og bruger lagerfordelingsfunktionen, hvilket giver dig mulighed for at sætte en dedikeret lagerbeholdning til side for at sikre, at du kan honorere de mest profitable kanaler eller kunder.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 449ca0616405ba589b92fba1ef078a4350d1e3b1
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762666"
---
# <a name="inventory-visibility-inventory-allocation"></a>Allokering af Inventory Visibility-slager

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>Forretningsbaggrund og -formål

Organisationer skal ofte forudallokere deres lagerbeholdning til deres vigtigste salgskanaler, kundegrupper, regioner og kampagnehændelser for at sikre, at den forudallokerede lagerbeholdning er sikret mod enhver anden anvendelse og kun kan forbruges via salgstransaktioner, der er relevante for fordelingen. Lagerfordeling i lagersynlighed er en komponent i salgsplanlægningsprocessen, og den udføres, før de faktiske salgsaktiviteter finder sted, og der oprettes en salgsordre.

Et firma med navnet Contoso producerer f.eks. en populær cykel. Netop fordi en ny afbrydelse af forsyningskæden har påvirket alle transitlager i denne periode, har Contoso kun begrænset lagerbeholdning og skal derfor have den optimale udnyttelse. Contoso foretager både online- og butikssalg. I hver salgskanal har firmaet et par vigtige samarbejdspartnere (markedspladser og store detailforretninger), som kræver, at der gemmes en bestemt del af cyklens lagerbeholdning til dem. Cykelfirmaet skal derfor kunne afbalancere distributionen af lagerbeholdning på tværs af kanaler og også håndtere forventningerne fra sine VIP-partnere. Den bedste måde at opnå begge mål på er at bruge lagerfordeling, så hver kanal og detailhandler kan modtage specifikke tildelte mængder, der kan sælges til forbrugerne.

Lagerfordeling har to grundlæggende forretningsformål:

- **Lagerbeskyttelse (ringorganisering)** – Organisationer vil forhåndsfordele begrænset lagerbeholdning til prioriterede kanaler, geografiske områder, VIP-kunder og datterselskaber. Funktionen til fordeling af lagersynlighed har til formål at beskytte den fordelte lagerbeholdning, så de andre tildelinger, reservationer eller anden salgsefterspørgsel ikke påvirker den tidligere fordelte lagerbeholdning.
- **Oversalgsstyring** – Funktionen til fordeling af lagersynlighed begrænser de tidligere fordelte antal, så den modtagende part (f.eks. en kanal eller kundegruppe) ikke overforbruger dem, når den faktiske salgstransaktion, der er baseret på en foreløbig reservation, træder i kraft.

## <a name="allocation-definition-in-inventory-visibility-service"></a>Fordelingsdefinition i lagersynlighedstjeneste

### <a name="allocation-virtual-pool"></a>Virtuel fordelingspulje

Selvom fordelingsfunktionen i lagersynlighed ikke tilsidesætter fysiske lagerantal, refererer den til fysisk disponibelt lagerantal for at definere det første *tilgængelige antal for tildeling* af virtuelle puljer. Lagerfordeling i lagersynlighed er en foreløbig tildeling. Det sker, før de faktiske salgstransaktioner finder sted, og afhænger ikke af salgsordrer. Du kan f.eks. fordele lagerbeholdning til dine vigtigste salgskanaler eller store detailforretninger, før nogen slutkunder besøger salgskanalen eller detailbutikken for at købe den.

### <a name="difference-between-inventory-allocation-and-soft-reservation"></a>Difference mellem lagerfordeling og forhåndsreservation

[Forhåndsreservationer](inventory-visibility-reservations.md) er normalt knyttet til faktiske salgstransaktioner (salgsordrelinjer). Både allokering og forhåndsreservation kan bruges uafhængigt, men hvis du vil bruge dem sammen, skal forhåndsreservation udføres efter tildeling. Vi anbefaler, at du bruger funktionerne til tildeling og foreløbig reservation sammen, og at du først foretager lagerfordeling og derefter foreløbig reservation af de tildelte antal. Du kan finde flere oplysninger under [Forbruge som en foreløbig reservation](#consume-to-soft-reserved).

Lagerfordelingsfunktionen giver salgsplanlæggere eller key account managers mulighed for at administrere og forhåndsfordele vigtig lagerbeholdning på tværs af fordelingsgrupper (f.eks. kanaler, geografiske regioner og kundegrupper). Det understøtter også sporing, regulering og analyser i realtid af forbruget i forhold til fordelte antal for at sikre, at genopfyldning eller omfordeling kan ske til tiden. Denne mulighed for at få synlighed af fordeling, forbrug og fordelingssaldo i realtid er særlig vigtig ved hurtige salgs- eller kampagnehændelser.

## <a name="terminology"></a>Terminologi

Følgende udtryk og begreber er nyttige i diskussioner om lagerfordeling:

- **Fordelingsgruppe** – Den gruppe, der ejer fordelingen, f.eks. en salgskanal, kundegruppe eller ordretype.
- **Værdi af fordelingsgruppe** – Værdien af hver enkelt fordelingsgruppe. F.eks. kan *net* eller *butik* være værdien af salgskanaltildelingsgruppen, mens *VIP* eller *normal* kan være værdien af kundefordelingsgruppen.
- **Fordelingshierarki** – En måde at kombinere fordelingsgrupper på en hierarkisk måde. Du kan f.eks. definere *kanal* som hierarkiniveau 1, *region* som niveau 2 og *kundegruppe* som niveau 3. Under lagerfordeling skal du følge fordelingshierarkirækkefølgen, når du angiver værdien af fordelingsgruppen. Du kan f.eks. tildele 200 røde cykler til kanalen *net*, regionen *London* og kundegruppen *VIP*.
- **Tilgængelig til fordeling** – Den *virtuelle fælles pulje*, der angiver det antal, der er tilgængeligt for yderligere fordeling. Det er en beregnet måling, som du frit kan definere ved hjælp af din egen formel. Hvis du også bruger funktionen til foreløbig reservation, anbefales det, at du bruger samme formel til at beregne tilgængelig til fordeling og tilgængelig til reservering.
- **Tildelt** – En fysisk måling, der viser den tildelte kvote, der kan forbruges af fordelingsgrupperne. Den fratrækkes samtidig med, at det forbrugte antal tilføjes.
- **Forbrugt** – En fysisk måling, der angiver det antal, der er forbrugt, i forhold til det oprindeligt tildelte antal. Efterhånden som der føjes tal til denne fysiske måling, reduceres den tildelte fysiske måling automatisk.

I følgende illustration vises forretningsarbejdsgangen for lagerfordeling.

![Arbejdsproces for fordeling af lagersynlighed.](media/inventory-visibility-allocation-flow.png "Arbejdsproces for fordeling af lagersynlighed.")

I følgende illustration vises fordelingshierarkiet og tildelingsgrupperne. Den *virtuelle fælles pulje*, som vises her, er det antal, der kan tildeles.

[<img src="media/inventory-visibility-allocation-hierarchy.png" alt="Inventory Visibility allocation hierarchy." title="Allokering af lagersynlighedshierarki" width="720" />](media/inventory-visibility-allocation-hierarchy.png)

## <a name="set-up-inventory-allocation"></a>Konfigurere lagerfordeling

Lagerfordelingsfunktionen består af følgende komponenter:

- Den foruddefinerede, fordelingsrelaterede datakilde, fysiske målinger og beregnede målinger.
- Brugerdefinerbare fordelingsgrupper, der maksimalt har otte niveauer.
- Et sæt fordelings-API'er (Application Programming Interfaces):

    - allocate (fordele)
    - reallocate (omfordele)
    - unallocate (ikke-fordele)
    - consume (forbruge)
    - query (forespørgsel)

Der er tre trin til konfiguration af fordelingsfunktionen:

- Aktiver funktionen i appen Lagersynlighed ved at gå til **Konfiguration \> Funktionsstyring og indstillinger \> Allokering**.
- Konfigurer [datakilden](inventory-visibility-configuration.md#data-source-configuration) og dens [målinger](inventory-visibility-configuration.md#data-source-configuration-physical-measures).
- Konfigurer fordelingsgruppenavnet og -hierarkiet.

### <a name="predefined-data-source"></a>Forhåndsdefineret datakilde

Når du aktiverer fordelingsfunktionen og kalder API til konfigurationsopdatering, opretter lagersynlighed én foruddefineret datakilde og flere indledende målinger.

Datakildens navn er `@iv`. Den omfatter et sæt standard fysiske mål. Du kan få dem vist fra Appen Lagersynlighed ved at gå til **Konfiguration \> Datakilde**. Du bør se **Datakilde – @IV**. Udvid `@iv`-datakilden for at få vist en liste over indledende fysiske målinger:

- `@iv`

    - `@allocated`
    - `@cumulative_allocated`
    - `@consumed`
    - `@cumulative_consumed`

Vælg fanen **Beregnede måleenheder** for at få vist den første beregnede måleenhed, der kaldes `@iv.@available_to_allocate`:

- `@iv`

    - `@iv.@available_to_allocate` = `??` – `??` – `@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>Føje andre fysiske måleenheder til den beregnede måling "available-to-allocate"

Hvis du vil bruge fordeling, skal du korrekt konfigurere formalen for beregnet "available-to-allocate" måling (`@iv.@available_to_allocate`). Du har f.eks. datakilden `fno` og målingen `onordered`, datakilden `pos` og målingen `inbound`, og du vil fordele den disponible beholdning for summen af `fno.onordered` og `pos.inbound`. I dette tilfælde skal `@iv.@available_to_allocate` indeholde `pos.inbound` og `fno.onordered` i formlen. Her er et eksempel:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

> [!NOTE]
> Datakilde `@iv` er en foruddefineret datakilde, og de fysiske målinger, der er defineret i `@iv` med præfikset `@`, er foruddefinerede mål. Disse foranstaltninger er en foruddefineret konfiguration af fordelingsfunktionen, så du skal ikke ændre eller slette dem, eller du vil sandsynligvis komme til at møde uventede fejl, når du bruger fordelingsfunktionen.
>
> Du kan føje nye fysiske måleenheder til den foruddefinerede beregnede måleenhed `@iv.@available_to_allocate`, men du må ikke ændre navnet.

### <a name="manage-allocation-groups"></a>Administrere allokeringsgrupper

Der kan maksimalt angives otte fordelingsgruppenavne. Grupperne har et hierarki. Hvis du vil se og opdatere allokeringsgrupper.

1. Log på Power Apps-miljøet, og åbn **Lagersynlighed**.
1. Åbn siden **Konfiguration**, og vælg derefter **Rediger konfiguration** under fanen **Fordeling**. Der findes som standard et fordelingshierarki med fire lag: `Channel` (øverste lag), `customerGroup` (andet lag), `Region` (tredje lag) og `OrderType` (fjerde lag).
1. Du kan fjerne en eksisterende fordelingsgruppe ved at vælge **X** ud for den. Du kan også føje nye fordelingsgrupper til hierarkiet ved at angive navnet på hver ny gruppe direkte i feltet.

    > [!IMPORTANT]
    > Vær forsigtig, når du sletter eller ændrer tilknytningen af fordelingshierarkiet. Du kan finde vejledninger i [tip til brug af fordeling](#allocation-tips).

1. Når du er færdig med at konfigurere indstillingerne for fordelingsgruppe og hierarki, skal du gemme ændringerne og derefter vælge **Opdater konfiguration** i øverste højre hjørne. Værdierne for de konfigurerede fordelingsgrupper opdateres, når du opretter en fordeling ved hjælp af enten brugergrænsefladen eller API POST (/api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/allocate). Oplysninger om begge metoder finder du senere i denne artikel.

Hvis du bruger fire gruppenavne og angiver dem til \[`channel`, `customerGroup`, `region`, `orderType`\], gælder disse navne for fordelingsrelaterede anmodninger, når du kalder API til konfigurationsopdatering.

### <a name="tips-for-using-allocation"></a><a name="allocation-tips"></a>Tips til brug af allokering

- For hvert produkt skal fordelingsfunktionen bruge samme *dimensionsniveau* i henhold til det produktindekshierarkiet, som du har angivet i [konfigurationen af produktindekshierarkiet](inventory-visibility-configuration.md#index-configuration). Forestil dig f.eks., at indekshierarkiet er \[`Site`, `Location`, `Color`, `Size`\]. Hvis du tildeler et antal for ét produkt på dimensionsniveau \[`Site`, `Location`, `Color`\]næste gang du vil tildele dette produkt, skal du også tildele det på samme niveau, \[`Site`, `Location`, `Color`\] Hvis du bruger niveauet \[`Site`, `Location`, `Color`, `Size`\] eller \[`Site`, `Location`\] vil dataene være uoverensstemmende.
- **Redigere fordelingsgrupper og hierarkiet:** Hvis der allerede findes fordelingsdata i systemet, vil sletning af eksisterende fordelingsgrupper eller et skift i fordelingsgruppehierarkiet beskadige den eksisterende tilknytning mellem fordelingsgrupperne. Derfor skal du sørge for at rydde op manuelt i alle gamle data, før du opdaterer den nye konfiguration. Men da tilføjelsen af nye fordelingsgrupper til det laveste hierarki ikke påvirker eksisterende tilknytninger, behøver du ikke at rydde op i dataene.
- Fordelingen lykkes kun, hvis produktet har et positivt `available_to_allocate`-antal.
- Hvis du vil fordele produkter fra en gruppe på højt *tildelingsniveau* til en undergruppe, skal du bruge `Reallocate` API. Du har f.eks. et fordelingsgruppehierarki, \[`channel` `customerGroup`, `region`, `orderType`\], og du vil tildele et produkt fra tildelingsgruppen \[Online, VIP\] til underfordelingsgruppen \[Online, VIP, EU\], brug `Reallocate` API til at flytte antallet. Hvis du bruger `Allocate` API, vil den tildele antallet fra den virtuelle fælles pulje.
- Hvis du vil have vist den generelle tilgængelighed af produkter (den fælles pulje), skal du bruge [API-forespørgslen](inventory-visibility-api.md#query-on-hand) til anmodning om det lagerbeløb, der *kan fordeles*. Derefter kan du træffe fordelingsbeslutninger på baggrund af disse oplysninger.

## <a name="use-the-allocation-api"></a><a name="using-allocation-api"></a>Brug af fordelings-API

Aktuelt er der åbnet fem fordelings-API'er:

- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/allocate** – Denne API bruges til at oprette den indledende fordeling.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/unallocate** – Denne API bruges til at fjerne eller genoprette allokerede mængder.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/reallocate** – Denne API bruges til at flytte den tildelte mængde fra en eksisterende fordeling til andre fordelingsgrupper.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/consume** – Denne API bruges til at fjerne eller genoprette allokeret mængde.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/query** – Denne API bruges til at kontrollere eksisterende fordelingsposter mod fordelingsgrupper og hierarki.

### <a name="allocate"></a>Tildel

Kald `Allocate`-API for at tildele et produkt, der har bestemte dimensioner. Her er skemaet for anmodningsindholdet.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

Du ønsker f.eks. at fordele et antal på 10 for produkt *Cykel*, sted *1*, lokation *11*, farve *rød*, kanal *Online*, kundegruppe *VIP* og region *USA*. For at kunne foretage denne fordeling kan du foretage et kald med følgende indhold.

```json
{
    "id": "test101",
    "productId": "Bike",
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 10,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

Antallet skal altid være større end 0 (nul).

### <a name="unallocate"></a>Unallocate

Brug API'en `Unallocate` til at tilbageføre `Allocate`-operationen. Negativt antal er ikke tilladt i en `Allocate`-operation. Indholdet af `Unallocate` er identisk med indholdet af `Allocate`.

### <a name="reallocate"></a>Reallocate

Brug API'en `Reallocate` til at flytte et tildelt antal til en anden gruppekombination. Her er skemaet for anmodningsindholdet.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "sourceGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "groups": {
        "groupD": "string",
        "groupE": "string",
        "groupF": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

Du kan f.eks. flytte to cykler med dimensionerne \[sted=1, lokation=11, farve=rød\] fra fordelingsgruppe \[Online, VIP, USA\] til fordelingsgruppe \[Online, VIP, EU\] ved at kalde API'en `Reallocate` og levere følgende brødtekst.

```json
{
    "id": "test102",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "EU"
    },
    "quantity": 2,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

### <a name="consume"></a>Consume

Brug API'en `Consume` til at bogføre forbrugsantallet i forhold til fordeling. Du kan f.eks. bruge denne API til at flytte fordelt antal til nogle faktiske målinger. Her er skemaet for anmodningsindholdet.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "physicalMeasures": {
        "datasource1": {
            "measure": "string" // Addition or Subtraction
        }
    }
}
```

Der er f.eks. otte tildelte cykler, som har dimensionerne \[sted=1, lokation=11, farve=rød\] for fordelingsgruppen \[Online, VIP, USA\]. Der bruges følgende fordelingsformel:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

De otte cykler fordeles fra målingen `pos.inbound`.

Nu er tre cykler solgt, og de tages fra fordelingspuljen. For at registrere denne flytning kan du foretage et kald med følgende anmodningsindhold.

```json
{
    "id": "test103",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "pos": {
            "inbound": "Subtraction"
        }
    }
}
```

Efter dette opkald reduceres det tildelte antal for produktet med 3. Derudover vil Lagersynlighed generere en hændelse for ændring af disponibel beholdning, hvor `pos.inbound` = *-3*. Alternativt kan du beholde værdien `pos.inbound`, som den er, og blot forbruge det tildelte antal. I dette tilfælde skal du dog enten oprette endnu en fysisk måling for at beholde de forbrugte antal eller bruge den foruddefinerede måling `@iv.@consumed`.

I denne anmodning skal du bemærke, at den fysiske måling, du bruger i forbrugsanmodningen, skal bruge den modsatte modifikatortype (Addition eller Subtraktion), sammenlignet med den modifikatortype, der bruges i den beregnede måling. Så i dette forbrugsindhold har `iv.inbound` værdien `Subtraction`, ikke `Addition`.

`fno`-datakilden kan ikke bruges i forbrugsindholdet, da lagersynlighed ikke kan ændre data for `fno`-datakilden. Dataflowet er envejs, hvilket betyder, at alle ændringer af antal for datakilden `fno` skal komme fra dit Supply Chain Management-miljø.

### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a>Forbruge som en foreløbig reservation

API'en `Consume` kan også forbruge det tildelte antal som en foreløbig reservation. I dette tilfælde reducerer operationen `Consume` det tildelte antal og laver derefter en foreløbig reservation af det pågældende antal. Hvis du vil bruge denne metode, skal du også bruge funktionen [foreløbig reservation](inventory-visibility-reservations.md) til lagersynlighed.

Du har f.eks. angivet en fysisk måling til foreløbig reservation som `iv.softreserved`. Følgende formel bruges til den beregnede måling af tilgængelig til reservation:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound` – `iv.softreserved`

Hvis du vil bruge denne opsætning sammen med fordelingsfunktionen, skal du føje `@iv.@allocated` til `iv.available_to_reserve` for at oprette følgende formel:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound` – `iv.softreserved` – `@iv.@allocated`

Opdater derefter `@iv.@available_to_allocate` til den samme værdi.

Når du vil forbruge et antal på 3 og reservere dette antal direkte, kan du foretage et kald med følgende anmodningsindhold.

```json
{
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "iv": {
            "softreserved": "Addition"
        }
    }
}
```

I denne anmodning skal du bemærke, at `iv.softreserved` har værdien `Addition`, ikke `Subtraction`.

### <a name="query"></a>Query

Brug API'en `Query` til at hente fordelingsrelaterede oplysninger for nogle produkter. Du kan bruge dimensionsfiltre og fordelingsgruppefiltre til at indsnævre resultaterne. Dimensionerne skal svare præcist til den, du vil hente, f.eks. vil \[sted=1, lokation=11\] have ikke-relaterede resultater sammenlignet med \[sted=1, lokation=11, farve=rød\].

```json
{
    "productId": "string",
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "groups": {
        "additionalProp1": "string",
        "additionalProp2": "string",
        "additionalProp3": "string"
    },
}
```

Brug f.eks. \[sted=1, lokation=11, farve=rød\] og tomt gruppefelt til at hente alle fordelingsposter:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

Brug \[sted=1, lokation=11, farve=rød\] og grupperne \[kanal=Online, kundegruppe=VIP, region=USA\] til at hente fordelingsposter for denne gruppe:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

## <a name="use-the-allocation-user-interface"></a>Brug fordelingsbrugergrænsefladen

Du kan administrere fordelinger manuelt via brugergrænsefladen ved at åbne appen Lagersynlighed og gå til **Operationel synlighed \> Allokering**. Derfra kan du udføre alle de handlinger, der er beskrevet i følgende undersektioner.

### <a name="create-an-allocation"></a>Oprette en allokering

Følg disse trin for at oprette en fordeling fra **fordelingssiden** i appen Lagersynlighed.

1. Vælg **Alloker**.
1. Angiv værdier for basisfelter, dimensioner og målfordelingsgrupper. (Når du vælger den indsamlede datakilde i **Dimensionssektionen** skal først bruge rullelisten til at angive dimensionerne (f.eks. `siteId`). Angiv derefter dimensionsværdierne i de felter, der vises.)
1. Vælg **send**.

### <a name="consume-an-allocation"></a>Forbruge en fordeling

Vælg **Forbrug**, hvis du vil bruge en allokering. Du kan sikre, at du forbruger inden for den korrekte tildelingsgruppe og det korrekte hierarki, ved at angive de samme sæt organisations- og dimensionsdetaljer, som du angav, da du oprettede tildelingen.

### <a name="reallocate-an-allocation"></a>Genoprette en allokering

Vælg **Genalloker,** hvis du vil flytte eksisterende tildelt antal fra et sæt fordelingsgrupper til et andet.

### <a name="query-existing-allocations"></a>Forespørge på eksisterende tildelinger

Vælg **Forespørgsel**, og angiv derefter værdier for produkt, organisation, dimension og tildelingsgruppe for at få forespørgselsresultater for eksisterende tildelinger.
