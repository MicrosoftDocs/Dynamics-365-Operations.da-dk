---
title: Arbejde med lokationsvejledninger
description: Dette emne beskriver, hvordan du kan arbejde med lokationsvejledninger. Lokationsvejledninger er brugerdefinerede regler, der hjælper med at identificere pluk og læg-lokationer for lagerbevægelser.
author: Mirzaab
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSLocDirHint, WHSLocDirTableUOM, WHSLocDirFailure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-11-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: b1b3bafb24ff6eb0c42d901fac3b6668cedf39ef
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963304"
---
# <a name="work-with-location-directives"></a>Arbejde med lokationsvejledninger

[!include [banner](../includes/banner.md)]

Lokationsvejledninger er regler, der hjælper med at identificere pluk og læg-lokationer for lagerbevægelser. I f.eks. en salgsordretransaktion bestemmer en lokationsvejledning, hvor varerne plukkes, og hvor de plukkede varer skal lægges på lager. Lokationsvejledninger består af en overskrift og tilknyttede linjer. De oprettes for bestemte *typer af arbejdsordrer*.

> [!NOTE]
> Dette emne gælder for funktioner i modulet **Lagerstedsstyring**. Det gælder ikke for funktioner i modulet [Lagerstyring](../inventory/inventory-home-page.md).

Du kan bruge lokationsvejledninger til at udføre følgende opgaver:

- Lægge indgående varer væk.
- Plukke og lægge varer på midlertidigt lager til udgående transaktioner.
- Plukke og lægge råvarer på lager til produktion.
- Genopfylde lokationer.

## <a name="prerequisites"></a>Forudsætninger

Før du kan oprette en lokationsvejledning, skal du følge disse trin for at sikre, at forudsætningerne er på plads.

1. Kontrollér, at den påkrævede licensnøgle er aktiveret. Gå til **Systemadministration \> Konfiguration \> Licenskonfiguration**, udvid licensnøglen **Handel**, og vælg derefter konfigurationsnøglen **Lagersteds- og transportstyring**. Bemærk, at der kræves administratoradgang til dette trin.
1. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lagersteder**.
1. Opret et lagersted.
1. På oversigtspanelet **Lagersted** skal du for indstillingen **Brug lagerstedsstyringsprocesser** vælge *Ja*.
1. Opret lokationer, lokationstyper, lokationsprofiler og lokationsformater. Yderligere oplysninger finder du i afsnittet [Konfigurere lokationer i et WMS-aktiveret lagersted](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).
1. Opret steder, zoner og zonegrupper. Yderligere oplysninger finder du i [Konfigurere lagersted](https://docs.microsoft.com/dynamics365/commerce/channels-setup-warehouse) og [Konfigurere lokationer i et WMS-aktiveret lagersted](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).

## <a name="work-order-types-for-location-directives"></a>Arbejdsordretyper for lokationsvejledninger

Mange af de felter, der kan angives for lokationsvejledninger, er fælles for alle typer af arbejdsordrer. Andre felter er dog specifikke for bestemte arbejdsordretyper.

![Arbejdsordretyper for lokationsvejledninger](media/Location_Directives_Work_Order_Types.png "Arbejdsordretyper for lokationsvejledninger")

> [!NOTE]
> To typer arbejdsordrer, *Annulleret arbejde* og *Cyklusoptælling*, bruges kun af systemet. Lokationsvejledninger kan ikke oprettes for disse arbejdsordretyper.

I tabellerne i følgende underafsnit vises de fælles og arbejderordretypespecifikke felter, der er tilgængelige, når du konfigurerer en lokationsvejledning.

### <a name="fields-that-are-common-to-all-work-order-types"></a>Felter, der er fælles for alle typer arbejdsordrer

Følgende tabel indeholder de felter, der er fælles for alle arbejdsordretyper.

| Oversigtspanel | Felt |
|---|---|
| Lokationsvejledninger | Arbejdstype |
| Lokationsvejledninger | Lokation |
| Lokationsvejledninger | Lagersted |
| Lokationsvejledninger | Vejledningskode |
| Lokationsvejledninger | Flere SKU'er |
| Linjer | Løbenummer |
| Linjer | Fra antal |
| Linjer | Antal til |
| Linjer | Enhed |
| Linjer | Angiv lokalitet for antal |
| Linjer | Begræns efter enhed |
| Linjer | Rund op til enhed |
| Linjer | Find emballagemængde |
| Linjer | Tillad opdeling |
| Handlinger i lokationsvejledning | Løbenummer |
| Handlinger i lokationsvejledning | Navn |
| Handlinger i lokationsvejledning | Anvendelse af fast lokation |
| Handlinger i lokationsvejledning | Tillad negativ lagerbeholdning |
| Handlinger i lokationsvejledning | Batchaktiveret |
| Handlinger i lokationsvejledning | Strategi |

### <a name="fields-that-are-specific-to-work-order-types"></a><a name="fields-specific-types"></a>Felter, der er specifikke for arbejdsordretyper

Følgende tabel indeholder de felter, der er specifikke for bestemte arbejdsordretyper.

| Oversigtspanel | Felt | Arbejdsordretype |
|---|---|---|
| Lokationsvejledninger | Find via | Indkøbsordrer |
| Lokationsvejledninger | Gældende dispositionskode | Indkøbsordrer |
| Lokationsvejledninger | Dispositionskode | Indkøbsordrer |
| Lokationsvejledninger | Gældende dispositionskode | Færdige varer, læg på lager |
| Lokationsvejledninger | Dispositionskode | Færdige varer, læg på lager |
| Lokationsvejledninger | Gældende dispositionskode | Returordrer |
| Lokationsvejledninger | Dispositionskode | Returordrer |
| Lokationsvejledninger | Gældende dispositionskode | Kanban-læg på lager |
| Lokationsvejledninger | Gældende dispositionskode | Kanban-pluk |
| Linjer | Skabelon for øjeblikkelig genopfyldning. | Salgsordre |
| Linjer | Skabelon for øjeblikkelig genopfyldning. | Råvarepluk |
| Linjer | Skabelon for øjeblikkelig genopfyldning. | Flytteafgang |
| Linjer | Skabelon for øjeblikkelig genopfyldning. | Kanban-pluk |

## <a name="open-the-location-directives-page"></a>Åbne siden Lokationsvejledninger

Hvis du vil åbne siden **Lokationsvejledninger**, skal du gå til **Lokationsstyring \> Konfiguration \> Lokationsvejledninger**.

Derfra kan du se, oprette og redigere lokationsvejledninger ved hjælp af kommandoerne i handlingsruden. Se de resterende afsnit i dette emne for at få oplysninger om, hvordan du bruger alle de felter, der er tilgængelige på siden.

## <a name="action-pane"></a>Handlingsrude

Handlingsruden på siden **Lokationsvejledninger** indeholder knapper, du kan bruge til at oprette, redigere og slette vejledninger (**Rediger**, **Ny** og **Slet**). Den indeholder også følgende knapper, du kan bruge til at justere den rækkefølge, som lokationsvejledningen behandles i, og konfigurere en forespørgsel, der definerer kriterierne for anvendelse af lokationsvejledningen:

- **Flyt op** – Flyt den valgte lokationsvejledning op i rækkefølgen. Du kan f.eks. flytte den fra sekvensnummer 4 til sekvensnummer 3.
- **Flyt ned** – Flyt den valgte lokationsvejledning ned i rækkefølgen. Du kan f.eks. flytte den fra sekvensnummer 4 til sekvensnummer 5.
- **Rediger forespørgsel** – Åbn en dialogboks, hvor du kan definere de betingelser, som den valgte lokationsvejledning skal behandles under. Det kan f.eks. være, at du ønsker, at den kun gælder for et bestemt lagersted.

## <a name="location-directives-header"></a>Overskrift til lokalitetsvejledninger

Overskriften til lokationsvejledningen indeholder følgende felter for sekvensnummeret og sigende navn til lokationsvejledningen:

- **Sekvensnummer** – Dette felt angiver den rækkefølge, som systemet prøver at anvende hver lokationsvejledning i for den valgte arbejdsordretype. Der anvendes lave numre først. Du kan ændre rækkefølgen ved hjælp af knapperne **Flyt op** og **Flyt ned** i handlingsruden.
- **Navn** – Angiv et sigende navn for lokationsvejledningen. Dette navn skal hjælpe med at identificere det generelle formål med lokationsvejledningen. Du kan f.eks. angive *Salgsordrepluk på lagersted 24*.

## <a name="location-directives-fasttab"></a>Oversigtspanelet Lokationsvejledninger

Felterne i oversigtspanelet **Lokationsvejledninger** er specifikke for den arbejdsordretype, der er valgt i feltet **Arbejdsordretype** i listeruden.

- **Arbejdstype** – Vælg den arbejdstype, der skal udføres. De tilgængelige værdier afhænger af den type lagertransaktion, som du har valgt i feltet **Arbejdsordretype**. Vælg en af følgende værdier:

    - **Læg på lager** – Lokationsvejledningen vil forsøge at finde den mest ideelle lokation til at placere eller finde lager, som tilføres systemet via modtagelse, produktion eller lagerreguleringer. Den kan også bruges til at definere Læg på stadie-lokationen eller en endelig lagerport som afsendelseslokation.
    - **Pluk** – Lokationsvejledningen vil forsøge at finde de bedste lokationer til fysisk reservation af lager (dvs. oprette arbejde). Plukket kan fuldføres (og plukarbejdslinjen kan lukkes), selvom arbejdet ikke er fuldført. Brugeren kan fuldføre fysiske pluk. I systemet er denne handling et pluktrin. Brugeren kan derefter annullere fra mobilenheden og fuldføre arbejdet senere. Arbejdshovedet lukkes imidlertid først, når det endelige læg på lager er fuldført.

    > [!IMPORTANT]
    > De andre værdier i feltet **Arbejdstype** er ikke relevante for lokationsvejledninger. De vises kun, fordi feltet ikke er filtreret til at stemme overens med den valgte arbejdsordretype.

- **Sted** – Det er et obligatorisk felt, fordi lokationsvejledningen skal bestemme det sted og lagersted, den gælder for.
- **Lagersted** – Det er et obligatorisk felt, fordi lokationsvejledningen skal bestemme det sted og lagersted, den gælder for.
- **Vejledningskode** – Vælg den vejledningskode, der skal knyttes til en arbejds- eller genopfyldningsskabelon. På siden **Vejledningskode** kan du oprette nye koder, som kan bruges til at oprette forbindelse mellem arbejdsskabeloner eller genopfyldningsskabeloner og lokationsvejledninger. Vejledningskoder kan også bruges til at oprette forbindelse mellem enhver arbejdsskabelonlinje og en lokationsvejledning (f.eks. lagerporten eller den midlertidige lagerlokation).

    > [!TIP]
    > Hvis der er angivet en vejledningskode, søger systemet ikke i lokationsvejledninger efter sekvensnummer, når der skal genereres arbejde. Det vil i stedet søge efter vejledningskode. På denne måde kan du være mere præcis om den lokationsskabelon, der bruges til et bestemt trin i en arbejdsskabelon , f.eks. trinnet for midlertidig lagring af materialer.

- **Flere SKU'er** – Angiv denne indstilling til *Ja* for at bruge flere lagerenheder (SKU'er) på en lokation. F.eks. skal flere SKU'er aktiveres for placeringen af lagerporten. Hvis du aktiverer flere SKU'er, vil læg på lager-lokationen blive angivet i arbejde som forventet. Men læg på lager-lokationen kan dog kun håndtere en læg-flere-varer-på-lager (hvis arbejde indeholder forskellige SKU'er, der skal plukkes og placeres). Den kan ikke håndtere en enkelt SKU-læg-på-lager. Hvis du angiver denne indstilling til *Nej*, angives lokationen kun, hvis dit læg-på-lager kun har én slags SKU.

    > [!IMPORTANT]
    > Hvis du vil kunne udføre SKU'er med både læg-flere-varer-på-lager læg-enkelt-vare-på-lager, skal du angive to linjer med samme struktur og opsætning, men du skal angive indstillingen **Flere SKU'er** til *Ja* for én linje og *Nej* for den anden. I forbindelse med læg på lager skal du derfor have to lokationsvejledninger, der er identiske, selvom du ikke skal skelne mellem enkelte og flere SKU'er på en arbejds-id. Hvis du ofte ikke konfigurerer begge disse lokationsvejledninger, kommer der uventede forretningsproceslokationer fra den anvendte lokationsvejledning. Du skal bruge en lignende opsætning til lokationsvejledninger, der har **Arbejdstypen** *Pluk*, hvis du skal behandle ordrer, der omfatter flere SKU'er.

    Brug indstillingen **Flere SKU'er** for arbejdslinjer, der håndterer mere end ét varenummer. (Varenummeret vil være tomt i arbejdsdetaljerne, og det vil blive vist som **Flere** på behandlingssiderne i lagerstedsappen).

    I et typisk eksempel scenario er der konfigureret en arbejdsskabelon, så den har mere end ét pluk/læg på lager-par. I dette tilfælde kan du søge efter en bestemt lokationen for midlertidig lagring til brug af linjer med **Arbejdstype** *Læg på lager*.

    > [!NOTE]
    > Hvis indstillingen **Flere SKU'er** er angivet til *Ja*, kan du ikke vælge **Rediger forespørgsel** i handlingsruden, fordi forespørgslen ikke kan evaluere på vareniveau, når der er flere varer. Hvis du vil sikre, at den ønskede lokationsvejledning er valgt, skal du bruge feltet **Vejledningskode** til at styre valget af den lokationsvejledning, der er knyttet til de læg på lager-linjer, hvor denne vejledningskode er tildelt i arbejdsskabelonen.

    Medmindre du altid arbejder med handlinger til en enkelt vare eller en blandet vare, er det vigtigt, at du definerer to lokationsvejledninger for *Læg på lager*-arbejdstypen: Den ene, hvor indstillingen **Flere SKU'er** er angivet til *Ja*, og en anden, hvor den er angivet til *Nej*.

- **Gældende dispositionskode** – Angiv, om lokationsvejledningens dispositionskode skal svare til den dispositionskode, der er anvendt ved modtagelse af varen, eller om lokationsvejledningen kan vælges på basis af en hvilken som helst dispositionskode. Hvis du vælger *Nøjagtigt match* og feltet **Dispositionskode** er tomt, er det kun tomme dispositionskoder, der tages i betragtning til lokalitetsvejledningen.

    > [!NOTE]
    > Dette felt er kun tilgængeligt for bestemte arbejdsordretyper, hvor genopfyldning er tilladt. Du kan finde en komplet liste i afsnittet [Felter, der er specifikke for arbejdsordretyper](#fields-specific-types) tidligere i dette emne.

- **Find efter** – Angiv, om læg på lager-antallet skal være hele antallet på id'er, eller om det skal være vare pr. vare. Brug dette felt som en hjælp til at sikre, at alt indholdet på et id lægges på én lokation, og at systemet ikke foreslår, at du opdeler indholdet på flere lokationer for **ASN** (id-modtagelse), **Blandet id**-modtagelse og **Klynge**-modtagelsesprocesser. (Processen til modtagelse af **Klynge** kræver, at funktionen for *læg på lager-klynge* er aktiveret). Funktionsmåden for lokationsvejledningsforespørgslen, linjerne og lokationsvejledningens handlinger varierer afhængigt af den værdi, du vælger. Oversigtspanelet **Linjer** bruges kun, når feltet **Find efter** er angivet til *Vare*.

    > [!NOTE]
    > Dette felt er kun tilgængeligt for bestemte arbejdsordretyper, hvor genopfyldning er tilladt. Du kan finde en komplet liste i afsnittet [Felter, der er specifikke for arbejdsordretyper](#fields-specific-types).

- **Dispositionskode** – Dette felt bruges til lokationsvejledninger, der har arbejdsordretypen *Indkøbsordrer*, *Færdige varer, læg på lager* eller *Returordrer* og arbejdstypen *Læg på lager*. Brug den til at vejlede flowet, så det bruger en bestemt lokationsvejledning, afhængigt af den dispositionskode, som en arbejder har valgt i lagerstedsappen. Du kan f.eks. sende returvarer til et inspektionssted, før de returneres til lageret. En dispositionskode kan knyttes til en lagerstatus. På denne måde kan den bruges til at ændre lagerstatussen som en del af en modtagelsesproces. Du har f.eks. dispositionskoden *Karantæne*, der angiver lagerstatussen til *Karantæne*. Du kan derefter have en separat lokationsvejledning, der flytter den pågældende lagerbeholdning til en karantænelokation.

    > [!NOTE]
    > Dette felt er kun tilgængeligt for bestemte arbejdsordretyper, hvor genopfyldning er tilladt. Du kan finde en komplet liste i afsnittet [Felter, der er specifikke for arbejdsordretyper](#fields-specific-types).

## <a name="lines-fasttab"></a>Oversigtspanelet Linjer

Brug oversigtspanelet **Linjer** til at fastlægge betingelser for anvendelse af de relaterede handlinger, der er angivet i oversigtspanelet **Handlinger for lokationsvejledninger**. Du kan angive et minimumantal og et maksimumantal, som handlingerne skal gælde for, på hver linje. Du kan også angive, at handlinger skal bruges til en bestemt lagerenhed.

- **Sekvensnummer** – Angiv den rækkefølge, som hver linje i lokationsvejledningen behandles i for den valgte arbejdstype. Du kan ændre rækkefølgen ved hjælp af knapperne **Flyt op** og **Flyt ned** på værktøjslinjen.
- **Fra antal** – Angiv starten af det antalsinterval, som linjen gælder for. Angiv antallet i den måleenhed, der er valgt i feltet **Enhed**.
- **Til antal** – Angiv slutningen af det antalsinterval, som linjen gælder for. Angiv antallet i den måleenhed, der er valgt i feltet **Enhed**.
- **Enhed** – Vælg måleenheden for varerne. Du kan angive et minimumantal og et maksimumantal, som vejledningen skal gælde for, og du kan angive, at vejledningen skal gælde for en bestemt lagerenhed. Feltet **Enhed** bruges *kun* til evaluering af antal. Systemet bruger antallet i den enhed, der er angivet på linjen, for at afgøre, om en lokationvejledningslinjen gælder. Hver gang det når en lokationsvejledningslinje, forsøger systemet at konvertere efterspørgselsenheden til den enhed, der er angivet på linjen. Hvis konverteringen af måleenheden ikke findes, vil systemet gå videre til næste linje.
- **Find antal** – Dette felt bruges kun under forsøg på at anbringe eller finde varer på lagerstedet. (Derfor gælder det kun, når feltet **Arbejdstype** er angivet til *Læg på lager*). Vælg en af følgende værdier for at angive det antal, der skal bruges til at evaluere, om et antal er inden for intervallet **Fra antal** og **Til antal**:

    - **Id-antal** – Brug antallet på det id, der modtages.
    - **Enhedsopdelt antal** – Brug det antal, der bruges i transaktionen. Du modtager f.eks. et antal på 1.000 på et lagersted og fordeler det på ti id'er, der hver har et antal på 100. I dette tilfælde kan du bruge et antal på 1.000 varer i stedet for id-antallet på 100.
    - **Restantal** – Brug det antal, der stadig skal modtages, på den indkøbsordrelinje, der behandles.
    - **Forventet antal** – Brug det samlede antal på indkøbsordrelinjen, uanset hvad der allerede er modtaget.

- **Begræns pr. enhed** – Dette afkrydsningsfelt giver dig mulighed for at gøre lokalitetsvejledningslinjen specifik for en måleenhed eller flere måleenheder. Markér det for at begrænse de måleenheder, der betragtes som gyldige udvælgelseskriterier for lokationsvejledningslinjerne. Denne funktionalitet fungerer kun i forbindelse med lokalitetsvejledninger, hvor feltet **Arbejdstype** er angivet til *Pluk*.

    Når du f.eks. reserverer antal, vil du kun reservere paller fra et bestemt sæt lokationer. I dette tilfælde vil linjerne begrænse rækkefølgen til paller på en sådan måde, at der ikke vælges et antal, der er mindre end en palle, til lokationsvejledningen.

    Bemærk, at afkrydsningsfeltet **Begræns efter enhed** ikke bestemmer, hvilken eller hvilke enheder der anvendes på arbejdslinjer. Enhedsbegrænsningen gælder kun for de enheder, der er tilgængelige via enhedsseriegruppen. Eksempelvis en vare, der er tilknyttet en enhedsseriegruppe, der omfatter både enheden *paller* og *stk.* Der er defineret en måleenhed, hvor 1 palle = 100 stk., og lokationsvejledningen kun bruger funktionen **Begræns pr . enhed** til paller. Desuden er der defineret en arbejdsskabelon, som begrænser oprettelsen af arbejdshoveder til 50 stk. I dette tilfælde oprettes der arbejdslinjer på 50 stk. Benyt følgende fremgangsmåde for at angive måleenheden for begrænsning:

    1. Vælg **Begræns efter enhed** på værktøjslinjen i oversigtspanelet **Linjer**. (Denne knap bliver først tilgængelig, når du har markeret afkrydsningsfeltet **Begræns efter enhed** på linjen og derefter har valgt **Gem**).
    1. Vælg den måleenhed, du vil begrænse efter pluk- og læg på lager-processerne, i feltet **Enhed** på siden **Begræns efter enheder**.

- **Rund op til enhed** – Dette felt bruges sammen med afkrydsningsfeltet **Begræns efter enhed**. Hvis f.eks. **Begræns efter enhed** og **Rund op til enhed** er valgt i lokationsvejledningslinjen, bliver det arbejde, der er genereret ud fra vejledningen til pluk af råvarer, afrundet til et multiplum af en håndteringsenheder, der er angivet på siden **Begræns efter enhed**.

    > [!NOTE]
    > Denne **Rund op til enhed**-opsætning fungerer kun for arbejdsordretypen *Råvarepluk* og kun for lokationsvejledninger, hvor feltet **Arbejdstype** er angivet til *Pluk*.

- **Find pakkeantal** – Hvis du angiver et pakkeantal på en salgsordre, en flytteordre eller en produktionsordre, kan dette afkrydsningsfelt begrænse systemet, så det kun kan vælge lokationer, der mindst har denne pakkemængde.

    > [!NOTE]
    > Dette fungerer kun med lokationsvejledninger af typen *Pluk*.

- **Tillad opdeling** – Angiver, om en lokationsvejledning må opdele det antal, der modtages eller reserveres på tværs af flere lokationer på lagerstedet, eller om hele antallet skal være placeret på eller reserveret fra en enkelt lokation for at kunne oprette arbejde.
- **Skabelon for øjeblikkelig genopfyldning** – Brug dette felt til at oprette en forbindelse til en genopfyldningsskabelon, så opfyldningen startes, så snart varerne ikke er fordelt. Hvis du lader dette felt være tomt, starter varegenopfyldningen ikke, før alle linjer i lokationsvejledningen er blevet behandlet.

    > [!NOTE]
    > Dette felt er kun tilgængeligt for bestemte arbejdsordretyper, hvor genopfyldning er tilladt. Du kan finde en komplet liste i afsnittet [Felter, der er specifikke for arbejdsordretyper](#fields-specific-types).

## <a name="location-directive-actions-fasttab"></a>Oversigtspanelet Handlinger for lokationsvejledninger

Du kan definere flere handlinger i lokationsvejledning for hver linje. Igen, et løbenummer bruges til at bestemme den rækkefølge, handlingerne vurderes i. På dette niveau kan du oprette en forespørgsel for at definere, hvordan du finder den bedste lokation på lagerstedet. Du kan også bruge foruddefinerede værdier af **Strategi** for at finde en optimal placering.

- **Sekvensnummer** – Dette felt viser den rækkefølge, som handlingerne behandles i for den valgte arbejdstype. Du kan ændre rækkefølgen ved hjælp af knapperne **Flyt op** og **Flyt ned** på værktøjslinjen.
- **Navn** – Angiv navnet på lokationsvejledningens handling. Vær specifik, så den handling, der udføres, tydeligt fremgår af navnet.
- **Anvendelse af fast lokation** – Angiv, hvilke lokaliteter lokationsvejledningen skal overveje. Vælg en af følgende værdier:

    - **Faste og ikke-faste lokationer** – Lokationsvejledningen tager alle lokationer i betragtning.
    - **Kun faste lokationer for produktet** – Lokationsvejledningen tager kun faste lokationer for produkter i betragtning.
    - **Kun faste lokationer for produktvarianten** – Lokationsvejledningen tager kun faste lokationer for produktvarianter i betragtning.

- **Tillad negativ lagerbeholdning** – Markér dette afkrydsningsfelt for at tillade negativt lager på den angivne lagerlokation i lokationsvejledninger.
- **Batchaktiveret** – Markér dette afkrydsningsfelt for at bruge batchstrategier til de varer, der er batchaktiverede. Det er vigtigt, at du markerer dette afkrydsningsfelt for processer, der bruger lokationsvejledninger til at finde lokationer, hvor der skal plukkes batchnummersporede varer fra. På denne måde medtages søgning efter lokationer, der indeholder batchnummersporede varer. Hvis dette afkrydsningsfelt er markeret, og feltet **Strategi** er angivet til *Ingen*, går systemet videre til den næste handlingslinje.
- **Strategi** – For at gøre det nemmere og hurtigere at definere de handlinger, der er tilknyttet hver enkelt linje i en lokationsvejledning, skal du vælge en af de foruddefinerede strategier:

    - **Ingen** – Der anvendes ingen strategi.
    - **Match emballagemængde** – Denne strategi kontrollerer, om en pluklokation har den angivne emballagemængde. Denne strategi er kun gyldig, når feltet **Arbejdstype** er angivet til *Pluk*.
    - **Konsolider** – Denne strategi konsoliderer varer på en bestemt lokation, når tilsvarende varer allerede er tilgængelige. Denne strategi er kun gyldig, når feltet **Arbejdstype** er angivet til *Læg på lager*. En typisk opsætning af læg på lager forsøger at konsolidere på den første handlingslinje og derefter at lægge på lager uden konsolidering på den anden linje. Konsolidering af varer gør senere pluk mere effektive.
    - **FEFO-batchreservation** – Denne strategi bruger FEFO-batchreservationer (First Expiry, First Out). Brug den, når lageret lokaliseres ved hjælp af en batchudløbsdato og tildeles til batchreservation. Du kan kun bruge denne strategi til batchaktiverede varer. Den er kun gyldig, når feltet **Arbejdstype** er angivet til *Pluk*.
    - **Rund op til fuld LP og FEFO-batch** – Denne strategi kombinerer elementerne i strategierne *FEFO-batchreservationen* og *Rund op til fuld LP*. Den er kun gyldig for batchaktiverede varer og lokationsvejledninger, hvor arbejdstypen er *Pluk*. Linjen skal være batchaktiveret, hvis du vil bruge *FEFO-batchreservation*-strategien, og *Rund op til fuld LP*-strategien kan kun bruges til genopfyldning. Hvis denne strategi konfigureres sammen med en lokationslagergrænse, kan den valgte læg på lager-arbejdslokation være overbelastet, og lagergrænser skal ignoreres.
    - **Rund op til en fuld LP** – Denne strategi runder op til lagerantallet, så det svarer til antallet af id-numre, som er tildelt de varer, der skal plukkes. Du kan kun bruge denne strategi til genopfyldning for lokationsvejledninger af typen *Pluk*. Hvis denne strategi konfigureres sammen med en lokationslagergrænse, kan den valgte læg på lager-arbejdslokation være overbelastet, og lagergrænser skal ignoreres.
    - **Nummerpladestyret** – Brug denne strategi, når du frigiver ordren til lagerstedet for at oprette pluk og læg-arbejdet. Du kan gøre dette for flere nummerplader. Denne strategi vil forsøge at reservere og oprette plukarbejde på de lokationer, hvor de anmodede nummerplader er knyttet til flytteordrelinjerne. Men hvis disse handlinger ikke kan fuldføres, men du stadig vil oprette plukarbejde, skal du gå tilbage til en anden strategi for handlinger i lokationsvejledningen. Afhængigt af dine krav til forretningsprocesser kan du også søge efter en lagerbeholdning i et andet område af lagerstedet.
    - **Tom lokation uden indgående arbejde** – Brug denne strategi til at finde tomme lokationer. En lokation anses som tom, hvis den ikke har noget fysisk lager og intet forventet indgående arbejde. Du kan kun bruge denne strategi til lokationsvejledninger med arbejdstypen *Pluk*.
    - **Lokation med aldersfordelt FIFO** – Brug strategien FIFO (First In, First Out) til at sende både batchsporede varer og varer, der ikke er batchsporede, baseret på den dato, hvor lagerbeholdningen ankom på lagerstedet. Denne facilitet kan især være nyttig for ikke-batchsporet lager, hvor en udløbsdato ikke er tilgængelig til brug ved sortering. FIFO-strategien finder den lokation, der indeholder den ældste aldersfordelte dato, og fordeler så plukningen baseret på den pågældende aldersfordelte dato.
    - **Lokation med aldersfordelt LIFO** – Brug strategien LIFO (Last In, First Out) til at sende både batchsporede varer og varer, der ikke er batchsporede, baseret på den dato, hvor lagerbeholdningen ankom på lagerstedet. Denne facilitet kan især være nyttig for ikke-batchsporet lager, hvor en udløbsdato ikke er tilgængelig til brug ved sortering. LIFO-strategien finder den lokation, der indeholder den nyeste aldersfordelte dato, og fordeler så plukningen baseret på den pågældende aldersfordelte dato.

## <a name="example-using-location-directives"></a>Eksempel: Brug af lokationsvejledninger

I dette eksempel ser vi på en indkøbsordreproces, hvor lokationsvejledningen skal finde ledig kapacitet inden for et lagersted for lagervarer, der netop er registreret i modtagelsesområdet. Du skal først prøve at finde ledig kapacitet på lagerstedet ved at konsolidere med eksisterende disponibel lagerbeholdning. Hvis konsolideringen ikke er muligt, skal du finde en tom lokation.

I dette scenarie skal du definere to handlinger i lokationsvejledningen. Den første handling i rækken skal bruge strategien *Konsolider*, og den anden skal bruge strategien *Tom lokation uden indgående arbejde*. Medmindre du definerer en tredje handling for at håndtere et overløbsscenarie, er der to mulige udfald, når der ikke er mere kapacitet på lagerstedet. Arbejde kan oprettes, selvom ingen lokationer er defineret, eller processen til oprettelse af arbejde kan mislykkes. Resultatet bestemmes af opsætningen på siden **Fejl i lokationsvejledning**, hvor du kan beslutte, om du vil vælge indstillingen **Stop arbejdet ved fejl i lokationsvejledning** for hver arbejdsordretype.

## <a name="next-step"></a>Næste trin

Når du opretter lokationsvejledninger, kan du knytte hver vejledningskode til en arbejdsskabelonkode med henblik på arbejdsoprettelse. Få flere oplysninger under [Styre lagerarbejde ved hjælp af arbejdsskabeloner og lokationsvejledninger](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/control-warehouse-location-directives).

## <a name="additional-resources"></a>Yderligere ressourcer

- Video: [Detaljeret konfiguration af lokationsstyring](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Hjælp-emne: [Styre lagerarbejde ved at bruge arbejdsskabeloner og lokationsvejledninger](control-warehouse-location-directives.md)
