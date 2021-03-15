---
title: Konfigurere politikker for forsendelseskonsolidering
description: Dette emne forklarer, hvordan du konfigurerer standard- og brugerdefinerede politikker for forsendelseskonsolidering.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, TMSMode, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 0d6ab6c034a5c341432f661cf1e729dfd3e5c239
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996379"
---
# <a name="configure-shipment-consolidation-policies"></a>Konfigurere politikker for forsendelseskonsolidering

[!include [banner](../includes/banner.md)]

Processen til forsendelseskonsolidering, der bruger politikker for forsendelseskonsolidering, giver mulighed for automatiseret forsendelseskonsolidering og manuel frigivelse til lageret. Når du har aktiveret denne funktion, skal du konfigurere de indledende politikker. Hvis der ikke er konfigureret nogen politikker, vil hver salgslinje generere en separat forsendelse, der indeholder en enkelt lastlinje.

De scenarier, der vises i dette emne, viser, hvordan du konfigurerer standard- og brugerdefinerede politikker for forsendelseskonsolidering.

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a>Slå funktionen Politikker for forsendelseskonsolidering til

> [!IMPORTANT]
> I det [første scenarie](#scenario-1), der beskrives i dette emne, skal du først konfigurere et lagersted, så det bruger den tidligere funktion til forsendelseskonsolidering. Derefter gør du politikker for forsendelseskonsolidering tilgængelige. På denne måde kan du opleve, hvordan opgraderingsscenariet fungerer. Hvis du planlægger at bruge et demonstrationsdatamiljø til at gå gennem det første scenarie, skal du ikke aktivere funktionen, før du udfører scenariet.

Før du kan bruge funktionen *Politikker for forsendelseskonsolidering*, skal du slå den til i systemet. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Konsolider forsendelses*

## <a name="make-demo-data-available"></a>Gøre demodata tilgængelige

Hvert scenariet i dette emne indeholder referencer til værdier og poster, der er inkluderet i de standarddemodata, der er angivet for Microsoft Dynamics 365 Supply Chain Management. Hvis du vil bruge de værdier, der er angivet her, når du udfører øvelserne, skal du arbejde i et miljø, hvor demodataene er installeret, og angive den juridiske enhed til **USMF**, før du går i gang.

## <a name="scenario-1-configure-default-shipment-consolidation-policies"></a><a name="scenario-1"></a>Scenarie 1: Konfigurer standardpolitikker for forsendelseskonsolidering

Der er to situationer, hvor du skal konfigurere minimumantallet af standardpolitikker, når du har aktiveret funktionen *Politikker for forsendelseskonsolidering*:

- Du er ved at opgradere et miljø, der allerede indeholder data.
- Du er ved at installere et helt nyt miljø.

### <a name="upgrade-an-environment-where-warehouses-are-already-configured-for-cross-order-consolidation"></a>Opgradere et miljø, hvor der allerede er konfigureret lagersteder til konsolidering på tværs af ordrer

Når du starter denne procedure, skal *Politikker for forsendelseskonsolidering* være slået fra, hvis du vil simulere et miljø, hvor den grundlæggende funktion til konsolidering på tværs af flere ordrer allerede er brugt. Derefter bruger du funktionsstyring til at aktivere funktionen, så du kan lære, hvordan du opretter politikker for forsendelseskonsolidering efter opgraderingen.

Benyt følgende fremgangsmåde for at oprette standardpolitikker for forsendelseskonsolidering i et miljø, hvor der allerede er konfigureret lagersteder til konsolidering på tværs af ordrer.

1. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lagersteder**.
1. Find og Åbn den ønskede lagerstedspost på listen (f.eks. lagersted *24* i **USMF**-demodataene).
1. Vælg **Rediger** i handlingsruden.
1. Gå til oversigtspanelet **Lagersted**, og angiv indstillingen **Konsolider forsendelse ved frigivelse til lagersted** til *Ja*.
1. Gentag trin 2 til 4 for alle andre lagersteder, hvor der kræves konsolidering.
1. Luk siden.
1. Brug [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at slå funktionen *Politikker for forsendelseskonsolidering* til. I arbejdsområdet **Funktionsstyring** hedder funktionen *Konsolider afsendelse*.
1. Gå til **Lagerstyringssted \> Opsætning \> Frigiv til lagersted \> Politikker for forsendelseskonsolidering**. Du skal muligvis opdatere browseren for at få vist det nye menupunkt **Politikker for forsendelseskonsolidering**, når du har aktiveret funktionen.
1. Gå til handlingsruden, og vælg **Opret standardopsætning** for at oprette følgende politikker:

    - En **Krydsordre**-politik for politiktypen *Salgsordrer* (hvis du har mindst ét lagersted, der er konfigureret til at bruge den tidligere konsolideringsfunktion)
    - En **Standard**-politik for politiktypen *Salgsordrer*
    - En **Standard**-politik for politiktypen *Flytteafgang*
    - En **Krydsordre**-politik for politiktypen *Flytteafgang* (hvis du har mindst ét lagersted, der er konfigureret til at bruge den tidligere konsolideringsfunktion)

    > [!NOTE]
    > - Begge **Krydsordre**-politikker tager højde for det samme sæt af felter som den tidligere logik, bortset fra feltet for ordrenummeret. (Dette felt bruges til at konsolidere linjer i forsendelser, baseret på faktorer som f.eks. lagersted, leveringsmåde for transporten og adresse).
    > - Begge **Standard**-politikker tager højde for det samme sæt af felter som den tidligere logik, herunder feltet for ordrenummeret. (Dette felt bruges til at konsolidere linjer i forsendelser, baseret på faktorer som f.eks. ordrenummer, leveringsmåde for transporten og adresse).

1. Vælg **Krydsordre**-politik for politiktypen *Salgsordrer*, og vælg derefter **Rediger forespørgsel** i handlingsruden.
1. Bemærk, at lagersteder, hvor indstillingen **Konsolider forsendelse ved frigivelse til lagersted** er angivet til *Ja*, vises i dialogboksen for forespørgselseditor. Derfor medtages de i forespørgslen.

### <a name="create-default-policies-for-a-new-environment"></a>Oprette standardpolitikker til et nyt miljø

Udfør følgende trin for at oprette standardpolitikker for forsendelseskonsolidering i et helt nyt miljø.

1. Brug [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at slå funktionen *Politikker for forsendelseskonsolidering* til, hvis du ikke allerede har gjort det. I arbejdsområdet **Funktionsstyring** hedder funktionen *Konsolider afsendelse*.
1. Gå til **Lagerstyringssted \> Opsætning \> Frigiv til lagersted \> Politikker for forsendelseskonsolidering**.
1. Gå til handlingsruden, og vælg **Opret standardopsætning** for at oprette følgende politikker:

    - En **Standard**-politik for politiktypen *Salgsordrer*
    - En **Standard**-politik for politiktypen *Flytteafgang*

    > [!NOTE]
    > Begge **Standard**-politikker tager højde for det samme sæt af felter som den tidligere logik, herunder feltet for ordrenummeret. (Dette felt bruges til at konsolidere linjer i forsendelser, baseret på faktorer som f.eks. ordrenummer, leveringsmåde for transporten og adresse).

## <a name="scenario-2-configure-custom-shipment-consolidation-policies"></a>Scenarie 2: Konfigurer brugerdefinerede politikker for forsendelseskonsolidering

I dette scenarie vises, hvordan du opretter brugerdefinerede politikker for forsendelseskonsolidering. Brugerdefinerede politikker kan understøtte komplekse virksomhedskrav, når forsendelseskonsolidering afhænger af flere betingelser. For hver eksempelpolitik, du ser senere i dette scenarie, er der inkluderet en kort beskrivelse af virksomhedseksemplet. Disse eksempelpolitikker skal oprettes i en rækkefælge, der sikrer en pyramidelignende evaluering af forespørgslerne. (Med andre ord skal de politikker, der har de fleste betingelser, evalueres med den højeste prioritet).

### <a name="turn-on-the-feature-and-prepare-master-data-for-this-scenario"></a>Aktivere funktionen og forberede stamdata til dette scenarie

Før du kan gennemgå øvelserne i dette scenarie, skal du aktivere funktionen og forberede de stamdata, der skal bruges til filtrering, som beskrevet i det følgende underafsnit. (Disse forudsætninger gælder også for de scenarier, der er angivet i [Eksemplerscenarier på, hvordan du bruger politikker til forsendelseskonsolidering](#example-scenarios).)

#### <a name="turn-on-the-feature-and-create-the-default-policies"></a>Aktivere funktionen, og opret standardpolitikkerne

Du kan bruge funktionsstyringen til at aktivere funktionen, hvis du ikke allerede har slået den til, og oprette de standardkonsolideringspolitikker, der er beskrevet i [scenarie 1](#scenario-1).

#### <a name="create-two-new-product-filter-codes"></a>Oprette to nye produktfilterkoder

1. Gå til **Lagerstedsstyring \> Opsætning \> Produktfiltre \> Produktfiltre**, og tilføj to produktfiltre:

    - Produktfilter 1:

        - **Filterkode:** *Brændbar*
        - **Filtertitel:** *Kode 4*

    - Produktfilter 2:

        - **Filterkode:** *Eksplosiv*
        - **Filtertitel:** *Kode 4*

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Åbn det produkt, der har varenummeret *M9200*. (Det produkt, du vælger, skal være aktiveret for de avancerede \[WMS-\]-lagerstedsprocesser, og dette produkt er allerede aktiveret for WMS-processer i **USMF**-demodataene.)
1. Gå til oversigtspanelet **Lagersted**, og indstil feltet **Kode 4** til *Brændbar*.
1. Luk siden.
1. Åbn det produkt, der har varenummeret *M9201*. (Dette produkt er også forhåndsaktiveret for WMS-processer i **USMF**-demodataene).
1. Gå til oversigtspanelet **Lagersted**, og indstil feltet **Kode 4** til *Eksplosiv*.
1. Luk siden.

#### <a name="create-a-new-transportation-mode-of-delivery"></a>Oprette en ny leveringsmåde for transport

1. Gå til **Transportstyring \> Opsætning \> Fragtmænd \> Tilstand**.
1. Opret en transporttilstand, der skal bruges i konsolideringsforespørgsler, og navngiv den *Airways*.
1. Gå til **Transportstyring \> Opsætning \> Fragtmænd \> Fragtmænd**.
1. Opret en fragtmand, der har følgende indstillinger:

    - **Fragtmand:** *Airways*
    - **Navn:** *Airways*
    - **Tilstand:** *Airways*

1. Gå til oversigtspanelet **Tjenester** for den nye fragtmand, og tilføj en række, der har følgende indstillinger:

    - **Fragttjeneste:** *Air*
    - **Transportmetode:** *Air*

1. Vælg **Gem** i handlingsruden.

    > [!NOTE]
    > Når du gemmer den nye fragtmand, angives feltet **Leveringsmåde** for den nye række i gitteret **Tjenester** automatisk til *Airwa-Air*. Når du bruger leveringsmåden *Airwa-Air* til en salgsordre, bruges transporttilstanden *Airways* til de relaterede forsendelser.

#### <a name="create-an-order-pool"></a>Oprette en ordrepulje

1. Gå til **Salg og marketing \> Opsætning \> Salgsordrer \> Ordrepuljer**.
1. Opret en ordrepulje, der skal bruges til konsolideringsforespørgslen. Denne ordrepulje skal have følgende indstillinger:

    - **Pulje:** Angiv et heltal, der ikke allerede bruges af en anden pulje.
    - **Navn:** *ShipCons*

1. Gå til **Salg og marketing \> Kunder \> Alle kunder**.
1. Åbn debitoren med kontonummer *US-003*.
1. Gå til oversigtspanelet **Salgsordrestandarder**, og angiv feltet **Salgsordrepulje** til den ordrepulje, du lige har oprettet.
1. Luk siden, og gentag derefter trin 4 og 5 for debitoren, der har kontonummer *US-004*.

### <a name="create-example-policy-1"></a>Oprette eksempelpolitik 1

I dette eksempel skal du oprette en *Debitor + tilstand*-politik, der kan bruges til følgende forretningseksempel:

- Politikken vil forespørge efter en bestemt debitorkonto (*US-001*) og en bestemt leveringsmåde (*Airwa-Air*).
- Konsolidering med åbne forsendelser er deaktiveret.
- Konsolideringen foretages pr. ordre-id. (Det vil sige, at der vil være separate forsendelser pr. ordre, lagersted osv.)

Benyt følgende fremgangsmåde for at oprette politikken til forsendelseskonsolidering for dette forretningseksempel.

1. Gå til **Lagerstyringssted \> Opsætning \> Frigiv til lagersted \> Politikker for forsendelseskonsolidering**.
1. Angiv feltet **Politiktype** til *Salgsordrer*.
1. Gå til handlingsruden, og vælg **Ny** for at oprette en politik, der har følgende indstillinger:

    - **Politiknavn:** *CustomerMode*
    - **PolitikBeskrivelse:** *Debitorkonto og leveringsmåde*

1. Lad indstillingen **Konsolider med åbne forsendelser** være angivet til *Nej*.
1. Vælg **Gem** i handlingsruden.
1. Gå til oversigtspanelet **Konsolideringsfelter** på listen **Resterende felter**, vælg række, hvor feltet **Feltnavn** er indstillet til *Leveringsmåde*.
1. Vælg knappen **Tilføj** ![Højre pil](media/forward-button.png) for at flytte feltet til listen **Valgte felter**.
1. Vælg **Rediger forespørgsel** i handlingsruden.
1. Gå til dialogboksen for forespørgselseditor på fanen **Område**, og find den række, hvor feltet **Felt** er indstillet til *Debitorkonto* i gitteret, indstil feltet **Kriterier** for den pågældende række til *US-001*.
1. Vælg **Tilføj** for at føje en række, der har følgende indstillinger, til gitteret:

    - **Tabel:** *Ordrelinjer*
    - **Afledt tabel:** *Ordrelinjer*
    - **Felt:** *Leveringsmåde*
    - **Kriterier:** *Airwa-Air*

1. Vælg **OK** for at lukke dialogboksen.

> [!NOTE]
> I dette forretningseksempel konsolideres ordrelinjer for debitor *US-001*, der bruger leveringsmåden *Airwa-Air*, ikke på tværs af ordrer. Denne politik er beregnet til først at blive brugt i en sekvens i tilfælde, hvor forsendelser for alle andre leveringsmåder er konsolideret for denne debitor.

### <a name="create-example-policy-2"></a>Oprette eksempelpolitik 2

I dette eksempel skal du oprette en *Farlige varer*-politik, der kan bruges til følgende forretningseksempel:

- Politikken vil forespørge efter en bestemt filterkode (*farlig*) og en bestemt leveringsmåde (*Airwa-Air*).
- Konsolidering med åbne forsendelser er aktiveret.
- Konsolideringen foretages på tværs af ordrer. (Med andre ord vil der være separate forsendelser pr. konto, lagersted osv., men kun i den varegruppe, der er angivet i forespørgslen).

Benyt følgende fremgangsmåde for at oprette politikken til forsendelseskonsolidering for dette forretningseksempel.

1. Gå til **Lagerstyringssted \> Opsætning \> Frigiv til lagersted \> Politikker for forsendelseskonsolidering**.
1. Angiv feltet **Politiktype** til *Salgsordrer*.
1. Gå til handlingsruden, og vælg **Ny** for at oprette en politik, der har følgende indstillinger:

    - **Politiknavn:** *Varetype*
    - **Politikbeskrivelse:** *Konsolider samme varetype på tværs af ordrer*

1. Angiv indstillingen **Konsolider med åbne forsendelser** til *Ja*.
1. Vælg **Gem** i handlingsruden.
1. Gå til oversigtspanelet **Konsolideringsfelter** på listen **Resterende felter**, vælg række, hvor feltet **Feltnavn** er indstillet til *Leveringsmåde*.
1. Vælg knappen **Tilføj** ![Højre pil](media/forward-button.png) for at flytte feltet til listen **Valgte felter**.
1. Vælg **Rediger forespørgsel** i handlingsruden.
1. I dialogboksen for forespørgselseditor skal du gå til fanen **Joins** og udvide og vælge **Tabeller \> Lastdetaljer** i træet.
1. Vælg **Tilføj tabeljoin**.
1. Find og markér den række, hvor feltet **Relation** er angivet til *Lagerstedsvarenummer (varenummer)*, i relationsgitteret, der vises og vælg derefter **Vælg**. 
1. Gå til fanen **Område**, og vælg **Tilføj** for at tilføje en række, der har følgende indstillinger, til gitteret:

    - **Tabel:** *Lagerstedsvarenummer*
    - **Afledt tabel:** *Lagerstedsvarenummer*
    - **Felt:** *Kode 4*
    - **Kriterier:** *Brændbar*

1. Vælg **OK** for at lukke dialogboksen.

> [!NOTE]
> I dette forretningseksempel bliver alle ordrelinjer, hvor varer har en bestemt filterkode (dvs. den filterkode, hvor feltet **Kode 4** er indstillet til *Brændbar*) konsolideret med andre varer af samme type på tværs af ordrer. Hvis der er en åben forsendelse for samme konto, lagersted og gruppe af varer, knyttes de nye linjer til den.

### <a name="create-example-policy-3"></a>Oprette eksempelpolitik 3

I dette eksempel skal du oprette en *Debitorkrav*-politik, der kan bruges til følgende forretningseksempel:

- Politikken vil forespørge om en bestemt debitorkonto.
- Konsolidering med åbne forsendelser er aktiveret.
- Konsolidering sker på tværs af ordrer, men er baseret på debitorrekvisitioner. (Med andre ord samles flere ordrer i forsendelser baseret på samme debitorrekvisitionsnummer og lagersted).

Benyt følgende fremgangsmåde for at oprette politikken til forsendelseskonsolidering for dette forretningseksempel.

1. Gå til **Lagerstyringssted \> Opsætning \> Frigiv til lagersted \> Politikker for forsendelseskonsolidering**.
1. Angiv feltet **Politiktype** til *Salgsordrer*.
1. Gå til handlingsruden, og vælg **Ny** for at oprette en politik, der har følgende indstillinger:

    - **Politiknavn:** *CustomerOrderNo*
    - **Politikbeskrivelse:** *Konsolider linjer baseret på debitorindkøbsordre*

1. Angiv indstillingen **Konsolider med åbne forsendelser** til *Ja*.
1. Vælg **Gem** i handlingsruden.
1. Gå til oversigtspanelet **Konsolideringsfelter** på listen **Resterende felter**, vælg række, hvor feltet **Feltnavn** er indstillet til *Debitorrekvisition*.
1. Vælg knappen **Tilføj** ![Højre pil](media/forward-button.png) for at flytte feltet til listen **Valgte felter**.
1. På listen **Resterende felter** skal du vælge den række, hvor feltet **Feltnavn** er indstillet til *Leveringsmåde*.
1. Vælg knappen **Tilføj** ![Højre pil](media/forward-button.png) for at flytte feltet til listen **Valgte felter**.
1. Vælg **Rediger forespørgsel** i handlingsruden.
1. Gå til dialogboksen for forespørgselseditor på fanen **Område**, og find den række, hvor feltet **Felt** er indstillet til *Debitorkonto*, indstil feltet **Kriterier** for den pågældende række til *US-001*.
1. Vælg **OK** for at lukke dialogboksen.

> [!NOTE]
> I dette forretningseksempel vil alle ordrelinjer, hvor salgsordrer har samme debitorrekvisitionsnummer, blive konsolideret til én forsendelse, uanset salgsordrenummeret. (Debitorrekvisitionsnummeret bruges som debitorens indkøbsordre \[PO\]-nummer.) Hvis der er en åben forsendelse for samme konto, lagersted og debitorrekvisition, føjes de nye linjer til den. Denne politik kan bruges, hvis debitoren sender yderligere ordrelinjer, der har samme indkøbsordrenummer, flere gange i løbet af en dag, og ønsker, at alle linjerne skal grupperes i én forsendelse. (Det vil sige, at der findes én fragtseddel og én følgeseddel).

### <a name="create-example-policy-4"></a>Oprette eksempelpolitik 4

I dette eksempel skal du oprette en *Debitor tillader konsolidering*-politik, der kan bruges til følgende forretningseksempel:

- Politikken vil forespørge efter en bestemt ordrepulje for at identificere debitorer, der accepterer konsoliderede forsendelser.
- Konsolidering med åbne forsendelser er deaktiveret.
- Konsolidering sker på tværs af ordrer ved hjælp af de felter, der er valgt som i standard-krydsordre-pdsolitikken (for at replikere det tidligere afkrydsningsfelt **Konsolider forsendelse ved frigivelse til lagersted**).

- Du kan tilsidesætte reglen på en salgsordre ved at vælge en anden ordrepulje.

Benyt følgende fremgangsmåde for at oprette politikken til forsendelseskonsolidering for dette forretningseksempel.

1. Gå til **Lagerstyringssted \> Opsætning \> Frigiv til lagersted \> Politikker for forsendelseskonsolidering**.
1. Angiv feltet **Politiktype** til *Salgsordrer*.
1. Gå til handlingsruden, og vælg **Ny** for at oprette en politik, der har følgende indstillinger:

    - **Politiknavn:** *Ordrepulje*
    - **Politikbeskrivelse:** *Konsolider på tværs af ordrer baseret på ordrepulje*

1. Lad indstillingen **Konsolider med åbne forsendelser** være angivet til *Nej*.
1. Vælg **Gem** i handlingsruden.
1. Gå til oversigtspanelet **Konsolideringsfelter** på listen **Resterende felter**, vælg række, hvor feltet **Feltnavn** er indstillet til *Leveringsmåde*.
1. Vælg knappen **Tilføj** ![Højre pil](media/forward-button.png) for at flytte feltet til listen **Valgte felter**.
1. Vælg **Rediger forespørgsel** i handlingsruden.
1. Gå til dialogboksen for forespørgselseditor, og vælg **Tilføj** på fanen **Område** for at tilføje en række, der har følgende indstillinger, til gitteret:

    - **Tabel:** *Salgsordrer*
    - **Afledt tabel:** *Salgsordrer*
    - **Felt:** *Pulje*
    - **Kriterier:** *ShipCons*

1. Vælg **OK** for at lukke dialogboksen.

> [!NOTE]
> I dette forretningseksempel vil alle ordrelinjer, hvor salgsordrer tilhører samme ordrepulje, blive konsolideret til én forsendelse på tværs af salgsordrer for samme konto, lagersted og leveringsmåde for transport. I stedet for ordrepuljen kan du bruge et hvilket som helst andet felt til at skelne en gruppe debitorer og bruge salgsordrehovedet som standard. Du kan bruge denne fremgangsmåde, hvis debitoren – og ikke lagerstedet – har behov for konsolidering. (I den tidligere konsolideringslogik var lagerstedet drivkraften bag konsolidering).

### <a name="create-example-policy-5"></a>Oprette eksempelpolitik 5

I dette eksempel skal du oprette en *Lagersted tillader konsolidering*-politik, der kan bruges til følgende forretningseksempel:

- Politikken vil forespørge efter en bestemt ordrepulje for at identificere lagersteder, der kan konsolidere forsendelser.
- Konsolidering med åbne forsendelser er deaktiveret.
- Konsolidering sker på tværs af ordrer ved hjælp af de felter, der er valgt som i standard-krydsordre-pdsolitikken (for at replikere det tidligere afkrydsningsfelt **Konsolider forsendelse ved frigivelse til lagersted**).

Dette forretningseksempel kan typisk håndteres ved hjælp af de standardpolitikker, du har oprettet i [scenarie 1](#scenario-1). Du kan dog også oprette ensartede politikker manuelt ved at følge disse trin.

1. Gå til **Lagerstyringssted \> Opsætning \> Frigiv til lagersted \> Politikker for forsendelseskonsolidering**.
1. Angiv feltet **Politiktype** til *Salgsordrer*.
1. Gå til handlingsruden, og vælg **Ny** for at oprette en politik, der har følgende indstillinger:

    - **Politiknavn:** *Krydsordre*
    - **Politikbeskrivelse:** *Konsolidering på tværs af ordrer for bestemte lagersteder*

1. Lad indstillingen **Konsolider med åbne forsendelser** være angivet til *Nej*.
1. Vælg **Gem** i handlingsruden.
1. Gå til oversigtspanelet **Konsolideringsfelter** i feltet **Resterende felter**, vælg række, hvor feltet **Feltnavn** er indstillet til *Leveringsmåde*.
1. Vælg knappen **Tilføj** ![Højre pil](media/forward-button.png) for at flytte feltet til listen **Valgte felter**.
1. Vælg **Rediger forespørgsel** i handlingsruden.
1. Gå til dialogboksen for forespørgselseditor på fanen **Område**, og find den række, hvor feltet **Felt** er indstillet til *Lagersted*, og indstil feltet **Kriterier** for den pågældende række til *61, 63*.
1. Vælg **OK** for at lukke dialogboksen.

### <a name="set-the-order"></a>Angive ordre

Nu, hvor du har oprettet alle politikker, skal du oprette den ordre, som de skal anvendes i. Hvis du vil bruge en pyramidelignende fremgangsmåde, hvor de politikker, der har de fleste betingelser, evalueres med den højeste prioritet, skal du følge disse trin.

1. Gå til **Lagerstyringssted \> Opsætning \> Frigiv til lagersted \> Politikker for forsendelseskonsolidering**.
1. Angiv feltet **Politiktype** til *Salgsordrer*.
1. Vælg de politikker, der vises i venstre kolonne, og brug derefter knapperne **Flyt op** og **Flyt ned** i handlingsruden til at arrangere politikkerne i følgende rækkefølge:

    1. Kundetilstand
    1. Varetype
    1. Kundeordrenr.
    1. Ordrepulje
    1. Krydsordre
    1. Standard

## <a name="example-scenarios-of-how-to-use-shipment-consolidation-policies"></a><a name="example-scenarios"></a> Eksempelscenarier for, hvordan du kan bruge politikker for forsendelseskonsolidering

Følgende scenarier illustrerer, hvordan du kan bruge de politikker for forsendelseskonsolidering, som du oprettede under læsning af dette emne. Hvert scenarie viser dig en forsendelseskonsolideringsproces, hvor der bruges politikker for forsendelseskonsolidering under automatiseret eller manuel frigivelse til lagerstedet:

- Scenarie 1: [Konsolidere leverancer, når de frigives til lagerstedet, ved hjælp af automatisk frigivelse af salgsordrer](../warehousing/consolidate-shipments-automatic.md)
- Scenarie 2: [Konsolidere forsendelser, når politikken for forsendelseskonsolidering tilsidesættes fra siden Frigiv til lager](../warehousing/consolidate-shipments-release-to-warehouse-override.md)
- Scenarie 3: [Konsolidere forsendelser ved at bruge Frigiv til lagersted fra panelet for lastplanlægning](../warehousing/consolidate-shipments-load-planning-workbench.md)
- Scenarie 4: [Konsolidere forsendelserne ved hjælp af panelet for forsendelseskonsolidering](../warehousing/consolidate-shipments-manual-workbench.md)
- Scenarie 5: [Konsolidere forsendelser manuelt ved hjælp af siden Konsolider forsendelser](../warehousing/consolidate-shipments-manual-form.md)


## <a name="additional-resources"></a>Yderligere ressourcer

- [Forsendelseskonsolideringspolitikker](about-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]