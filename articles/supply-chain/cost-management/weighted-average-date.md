---
title: Gennemsnitskostdato med fysisk værdi og afmærkning
description: Gennemsnitskostdato er en lagermodel, der er baseret på princippet for vægtet gennemsnit, hvor lagerafgange værdisættes til den gennemsnitlige værdi af de varer, der modtages på lageret, for hver enkelt dag i lagerlukningsperioden.
author: AndersGirke
ms.date: 03/04/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28991
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3cf2206863d891eceb9c65ff879da3f9f72032b1
ms.sourcegitcommit: fcded93fc6c27768a24a3d3dc5cc35e1b4eff22b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/07/2022
ms.locfileid: "8391995"
---
# <a name="weighted-average-date-with-include-physical-value-and-marking"></a>Gennemsnitskostdato med fysisk værdi og afmærkning

[!include [banner](../includes/banner.md)]

*Gennemsnitskostdato* er en lagermodel, der er baseret på et gennemsnit, der beregnes ved at gange hver komponent (varetransaktion) med en faktor (kostpris), der afspejler vigtigheden (antallet), for hver dag i perioden. Med andre ord tildeler denne lagermodel omkostningen ved afgangsposteringer på basis af middelværdien af alle de lagervarer, der modtages hver dag, plus en eventuel disponibel lagerbeholdning fra dagen før.

Når du kører en lagerlukning ved hjælp af lagermodellen for gennemsnitskostdato, kan der bruges to metoder til at oprette en udligning. Typisk udlignes alle tilgange mod en virtuel afgang, der indeholder den samlede modtagne mængde og værdi. Denne virtuelle afgang har en tilsvarende virtuel tilgang, som tilgangene vil blive udlignet fra. På denne måde opnår alle afgange samme gennemsnitskostpris hver dag. Den virtuelle afgang og den virtuelle tilgang kan betragtes som en virtuel overførsel. Denne virtuelle overførsel kaldes *lagerlukningsoverførsel efter vægtet gennemsnit*. Denne udligningsmetode kaldes derfor en *opsummeret udligning for vægtet gennemsnit*. Hvis der kun er én tilgang, kan alle afgange udlignes fra den, og der oprettes ikke en virtuel overførsel. Denne udligningsmetode kaldes en *direkte udligning*. Alle de lagerbeholdninger, der er disponible efter lagerlukningen, værdisættes ved det vægtede gennemsnit fra den sidste dag i den forrige periode og medtages i beregningen af gennemsnitskostdatoen i den næste periode.

Du kan tilsidesætte princippet for gennemsnitskostdato ved at markere lagerposteringer, så en specifik varetilgang udlignes mod en specifik afgang. Der kræves en periodisk lagerlukning, når du bruger lagermodellen gennemsnitskostdato til at oprette udligninger og regulere værdien af afgange i henhold til princippet for gennemsnitskostdato. Indtil du kører lagerlukningen, værdisættes afgangsposteringerne med det løbende gennemsnit, når de fysiske og økonomiske opdateringer finder sted. Medmindre du bruger afmærkning, beregnes det løbende gennemsnit, når den fysiske eller økonomiske opdatering udføres.

Lagerlukningsmetoden gennemsnitskostdato beregnes efter følgende formel hver dag:

*Omkostning* = \[(*A*<sub>*b*</sub> × *P*<sub>*b*</sub>) + &#x2211;<sub>*n*</sub>(*A*<sub>*n*</sub> × *P*<sub>*n*</sub>)\] ÷ (*A*<sub>*b*</sub> + &#x2211;<sub>*n*</sub>*A*<sub>*n*</sub>)

- *A* = antal for transaktionen
- *P* = pris for transaktionen

Med andre ord er den vægtede gennemsnitskostpris lig med startantallet gange startprisen plus summen af hvert tilgangsantal gange tilgangsprisen divideret med startantallet plus summen af tilgangsantallet.

Under lagerlukning udføres beregningen dagligt i lukningsperioden.

> [!NOTE]
> Du finder flere oplysninger om udligninger under [Lagerlukning](inventory-close.md).

I følgende eksempler illustreres virkningen af at bruge gennemsnitskostdato med fem konfigurationer:

- Direkte udligning for gennemsnitskostdato, når indstillingen **Medtag fysisk værdi** ikke bruges
- Opsummeret udligning for gennemsnitskostdato, når indstillingen **Medtag fysisk værdi** ikke bruges
- Direkte udligning for gennemsnitskostdato, når indstillingen **Medtag fysisk værdi** bruges
- Opsummeret udligning for gennemsnitskostdato, når indstillingen **Medtag fysisk værdi** bruges
- Dato for vægtet gennemsnit, når afmærkning bruges

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Direkte udligning for gennemsnitskostdato, når indstillingen Medtag fysisk værdi ikke bruges

Med princippet for direkte udligning oprettes der udligninger direkte mellem tilgange og afgange uden at oprette flere lagerposteringer. Systemet bruger dette udligningsprincip i følgende situationer:

- Der er blevet bogført én tilgang og en eller flere afgange i perioden.
- I perioden er der kun blevet bogført afgange, og der er disponible varer på lager fra en tidligere lukning.

I dette eksempel er markeringen i afkrydsningsfeltet **Medtag fysisk værdi** fjernet på siden **Varemodelgruppe** for det frigivne produkt. I følgende diagram vises disse posteringer:

**Dag 1:**

- 1a. Fysisk lagertilgang for et antal på 10 til en kostpris a kr. 10,00 pr. stk.
- 1b. Økonomisk lagertilgang for et antal på 10 til en kostpris a kr. 10,00 pr. stk.
- 2a. Fysisk lagertilgang for et antal på 10 til en kostpris a kr. 20,00 pr. stk.
- 3a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 10,00 (løbende gennemsnit af økonomisk bogførte posteringer).
- 3b. Økonomisk lagerafgang for et antal på 1 til en kostpris af USD 10,00 (løbende gennemsnit af økonomisk bogførte posteringer).

**Dag 2:**

- 4a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 25,00 pr. stk.
- 5a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
- 5b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
- 6a. Økonomisk lagerafgang for et antal på 1 til en kostpris af USD 20,00 hver (løbende gennemsnit af økonomisk bogførte posteringer).

**Dag 3:**

- 7\. Lagerlukningen udføres. På baggrund af metoden for gennemsnitskostdato bruger systemet den direkte udligningsmetode for 30. december (30-12), da der kun er én tilgang, der er økonomisk opdateret den 30-12. I dette eksempel oprettes der én udligning mellem transaktionerne 1b og 3b. Der foretages USD 10,00 regulering for at få værdien af transaktion 3b op til 20,00. Der foretages ingen regulering eller udligning den 31. december (31-12), fordi der ikke er nogen økonomisk opdaterede afregninger 31-12.

I følgende diagram vises denne række posteringer med effekterne ved at vælge lagermodellen for vægtet gennemsnit og princippet for direkte udligning uden indstillingen **Medtag fysisk værdi**.

![Direkte udligning for gennemsnitskostdato uden indstillingen Medtag fysisk værdi.](media/weighted-average-date-direct-settlement-without-include-physical-value.png)

**Forklaring til diagram:**

- Lagertransaktioner vises som lodrette pile.
- Fysiske posteringer vises med kortere, lysegrå pile.
- Økonomiske posteringer vises med længere sorte pile.
- Lagertilgange vises som lodrette pile over aksen.
- Lagerafgange vises som lodrette pile under aksen.
- Hver enkelt ny tilgangs- eller afgangspostering er markeret med en ny etiket.
- Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Identifikatorerne angiver rækkefølgen af lagerposteringsbogføringer på tidslinjen.
- Datoer er adskilt af tynde sorte lodrette linjer. Datoerne angives nederst i diagrammet.
- Lagerlukninger angives med røde lodrette stiplede linjer.
- Udligninger, der foretages ved lagerlukning, angives med stiplede, røde pile, der går diagonalt fra en tilgang til en afgang.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Opsummeret udligning for gennemsnitskostdato, når indstillingen Medtag fysisk værdi ikke bruges

Når der er flere tilgange i en periode, bruger vægtet gennemsnit det opsummerede udligningsprincip, hvor alle tilgange på en enkelt dag opsummeres i en transaktion, der kaldes *lagerlukning for vægtet gennemsnit*. Alle dagens tilgange udlignes mod afgangen i den nyoprettede lagertransaktion. Alle dagens afgange udlignes mod tilgangen i den nye lagertransaktion. Hvis der er en resterende disponibel lagerbeholdning efter lagerlukningen, medtages denne disponible lagerbeholdning i tilgangstransaktionen for lagerlukningstransaktionen med det vægtede gennemsnit.

I følgende diagram vises disse posteringer:

**Dag 1:**

- 1a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
- 1b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
- 2a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
- 2b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 22,00 pr. stk.
- 3a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 16,00 (løbende gennemsnit af økonomisk bogførte posteringer).
- 3b. Økonomisk lagerafgang for et antal på 1 til en kostpris af USD 16,00 (løbende gennemsnit af økonomisk bogførte posteringer).

**Dag 2:**

- 4a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 25,00 pr. stk.
- 5a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
- 5b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
- 6a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 23,00 (løbende gennemsnit af økonomisk bogførte posteringer).

**Dag 3:**

- 7\. Lagerlukningen udføres.
- 7a. Der oprettes en økonomisk afgang af typen lagerlukningstransaktion for vægtet gennemsnit for at opsummere udligningerne for alle økonomiske lagertilgange.

    - Transaktion 1b udlignes for et antal på 1 med et udlignet beløb af USD 10,00.
    - Transaktion 2b udlignes for et antal på 1 med et udlignet beløb af USD 22,00.
    - Transaktion 7a oprettes for et antal på 2 med et udlignet beløb af USD 32,00. Denne transaktion modregner summen af de to tilgangsposteringer, der er økonomisk opdateret i perioden.

- 7b. Der oprettes en økonomisk tilgang for lagerlukningstransaktion med vægtet gennemsnit som modpostering for økonomisk bogførte afgange.

    - Transaktion 3b udlignes for et antal på 1 med et udlignet beløb af USD 16,00. Denne transaktion reguleres ikke, da den er det vægtede gennemsnit af økonomisk bogførte transaktioner d. 1. december (1-12).
    - Transaktionen 7b oprettes for et antal på 2 med et økonomisk beløb af USD 32,00 og et udlignet beløb på USD 16,00 for modpostering 3b. Denne transaktion modregner summen af én tilgangstransaktion, der er økonomisk opdateret i perioden. Posteringen forbliver åben, fordi der stadig er én på lager.

I følgende diagram vises denne række posteringer, og effekterne ved at vælge lagermodellen for vægtet gennemsnit og princippet for opsummeret udligning, men uden brug af indstillingen **Medtag fysisk værdi**.

![Opsummeret udligning for gennemsnitskostdato uden indstillingen Medtag fysisk værdi.](media/weighted-average-date-summarized-settlement-without-include-physical-value.png)

**Forklaring til diagram:**

- Lagertransaktioner vises som lodrette pile.
- Fysiske posteringer vises med kortere, lysegrå pile.
- Økonomiske posteringer vises med længere sorte pile.
- Lagertilgange vises som lodrette pile over aksen.
- Lagerafgange vises som lodrette pile under aksen.
- Hver enkelt ny tilgangs- eller afgangspostering er markeret med en ny etiket.
- Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Identifikatorerne angiver rækkefølgen af lagerposteringsbogføringer på tidslinjen.
- Datoer er adskilt af tynde sorte lodrette linjer. Datoerne angives nederst i diagrammet.
- Lagerlukninger angives med røde lodrette stiplede linjer.
- Udligninger, der foretages ved lagerlukning, angives med stiplede, røde pile, der går diagonalt fra en tilgang til en afgang.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Direkte udligning for gennemsnitskostdato, når indstillingen Medtag fysisk værdi bruges

I den aktuelle version af produktet fungerer **Medtag fysisk værdi** anderledes for lagermodellen gennemsnitskostdato end i tidligere versioner. Hvis du markerer afkrydsningsfeltet **Medtag fysisk værdi** for en vare på siden **Varemodelgruppe**, bruger systemet fysisk opdaterede tilgange, når det beregner den forkalkulerede afgangskostpris eller løbende gennemsnit. Afgangene posteres på basis af denne forkalkulerede kostpris i løbet af perioden. Under lagerlukningen vil kun økonomisk opdaterede tilgange blive taget i betragtning i beregningen af det vægtede gennemsnit.

I følgende diagram vises disse posteringer:

**Dag 1:**

- 1a. Fysisk lagertilgang for et antal på 10 til en kostpris a kr. 10,00 pr. stk.
- 1b. Økonomisk lagertilgang for et antal på 10 til en kostpris a kr. 10,00 pr. stk.
- 2a. Fysisk lagertilgang for et antal på 10 til en kostpris a kr. 20,00 pr. stk.
- 3a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 15,00 (løbende gennemsnit af økonomisk og fysisk opdaterede posteringer).
- 3b. Økonomisk lagerafgang for et antal på 1 til en kostpris af USD 15,00 (løbende gennemsnit af økonomisk og fysisk opdaterede posteringer).

**Dag 2:**

- 4a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 25,00 pr. stk.
- 5a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
- 5b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
- 6a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 21,25 hver (løbende gennemsnit af økonomisk og fysisk opdaterede posteringer).

**Dag 3:**

- 7\. Lagerlukningen udføres. På baggrund af metoden for gennemsnitskostdato bruger systemet den direkte udligningsmetode for 30. december (30-12), da der kun er én tilgang, der er økonomisk opdateret den 30-12. I dette eksempel oprettes der én udligning mellem transaktionerne 1b og 3b. Afgangen justeres ikke den 30-12. Der foretages heller ingen regulering eller udligning den 31. december (31-12), fordi der ikke er nogen økonomisk opdaterede afregninger 31-12.

I følgende diagram vises denne række posteringer med effekterne ved at vælge lagermodellen for vægtet gennemsnit og princippet for direkte udligning med indstillingen **Medtag fysisk værdi**.

![Direkte udligning for vægtet gennemsnit med indstillingen Medtag fysisk værdi.](media/weighted-average-date-direct-settlement-with-include-physical-value.png)

**Forklaring til diagram:**

- Lagertransaktioner vises som lodrette pile.
- Fysiske posteringer vises med kortere, lysegrå pile.
- Økonomiske posteringer vises med længere sorte pile.
- Lagertilgange vises som lodrette pile over aksen.
- Lagerafgange vises som lodrette pile under aksen.
- Hver enkelt ny tilgangs- eller afgangspostering er markeret med en ny etiket.
- Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Identifikatorerne angiver rækkefølgen af lagerposteringsbogføringer på tidslinjen.
- Datoer er adskilt af tynde sorte lodrette linjer. Datoerne angives nederst i diagrammet.
- Lagerlukninger angives med røde lodrette stiplede linjer.
- Udligninger, der foretages ved lagerlukning, angives med stiplede, røde pile, der går diagonalt fra en tilgang til en afgang.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Opsummeret udligning for gennemsnitskostdato, når indstillingen Medtag fysisk værdi bruges

I den aktuelle version af produktet fungerer **Medtag fysisk værdi** anderledes med vægtet gennemsnit end i tidligere versioner. Hvis du markerer afkrydsningsfeltet **Medtag fysisk værdi** for en vare på siden **Varemodelgruppe**, bruger systemet fysisk opdaterede tilgange, når det beregner den forkalkulerede kostpris eller løbende gennemsnit. Afgangene posteres på basis af denne forkalkulerede kostpris i løbet af perioden. Under lagerlukningen vil kun økonomisk opdaterede tilgange blive taget i betragtning i beregningen af det vægtede gennemsnit. Du anbefales at bruge en månedlig lagerlukning, når du bruger lagermodellen for vægtet gennemsnit. I dette eksempel med opsummeret udligning for gennemsnitskostdato er lagermodellen markeret, så den medtager den fysiske værdi.

I følgende diagram vises disse posteringer:

**Dag 1:**

- 1a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
- 1b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
- 2a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
- 2b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 22,00 pr. stk.
- 3a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 16,00 (løbende gennemsnit af økonomisk og fysisk opdaterede posteringer).
- 3b. Økonomisk lagerafgang for et antal på 1 til en kostpris af USD 16,00 (løbende gennemsnit af økonomisk og fysisk opdaterede posteringer).

**Dag 2:**

- 4a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 25,00 pr. stk.
- 5a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
- 5b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
- 6a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 23,67 (løbende gennemsnit af økonomisk og fysisk opdaterede posteringer).

**Dag 3:**

- 7\. Lagerlukningen udføres.
- 7a. Der oprettes en økonomisk afgang af typen lagerlukningstransaktion for vægtet gennemsnit for at opsummere udligningerne for alle økonomiske lagertilgange.

    - Transaktion 1b udlignes for et antal på 1 med et udlignet beløb af USD 10,00.
    - Transaktion 2b udlignes for et antal på 1 med et udlignet beløb af USD 22,00.
    - Transaktion 7a oprettes for et antal på 2 med et udlignet beløb af USD 32,00. Denne transaktion modregner summen af de to tilgangsposteringer, der er økonomisk opdateret i perioden.

- 7b. Der oprettes en økonomisk tilgang for lagerlukningstransaktion med vægtet gennemsnit som modpostering for økonomisk bogførte afgange.

    - Transaktion 3b udlignes for et antal på 1 med et udlignet beløb af USD 16,00. Denne transaktion reguleres ikke, da den er det vægtede gennemsnit af økonomisk bogførte transaktioner d. 1. december (1-12).
    - Transaktionen 7b oprettes for et antal på 2 med et økonomisk beløb af USD 32,00 og et udlignet beløb på USD 16,00 for modpostering 3b. Denne transaktion modregner summen af én tilgangstransaktion, der er økonomisk opdateret i perioden. Posteringen forbliver åben, fordi der stadig er én på lager.

I følgende diagram vises denne række posteringer med effekterne ved at vælge lagermodellen for vægtet gennemsnit og princippet for opsummeret udligning uden indstillingen **Medtag fysisk værdi**.

![Opsummeret udligning for vægtet gennemsnit med Medtag fysisk værdi.](media/weighted-average-date-summarized-settlement-with-include-physical-value.png)

**Forklaring til diagram:**

- Lagertransaktioner vises som lodrette pile.
- Fysiske posteringer vises med kortere, lysegrå pile.
- Økonomiske posteringer vises med længere sorte pile.
- Lagertilgange vises som lodrette pile over aksen.
- Lagerafgange vises som lodrette pile under aksen.
- Hver enkelt ny tilgangs- eller afgangspostering er markeret med en ny etiket.
- Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Identifikatorerne angiver rækkefølgen af lagerposteringsbogføringer på tidslinjen.
- Datoer er adskilt af tynde sorte lodrette linjer. Datoerne angives nederst i diagrammet.
- Lagerlukninger angives med røde lodrette stiplede linjer.
- Udligninger, der foretages ved lagerlukning, angives med stiplede, røde pile, der går diagonalt fra en tilgang til en afgang.

## <a name="weighted-average-date-when-marking-is-used"></a>Dato for vægtet gennemsnit, når afmærkning bruges

Afmærkning er en proces, som giver dig mulighed for at tilknytte – eller afmærke – en afgangspostering til en tilgangspostering. Afmærkning kan ske enten før eller efter, at en postering er bogført. Du kan bruge afmærkning, når du vil være sikker på den nøjagtige kostpris for lageret, når posteringen bogføres, eller når lagerlukningen udføres.

Antag f.eks., at firmaets kundeserviceafdeling har modtaget en hasteordre fra en vigtig kunde. Da dette er en hasteordre, vil du skulle betale mere for denne vare for at kunne imødekomme kundens forespørgsel. Du skal være sikker på, at kostprisen på denne lagervare afspejles i dækningsbidraget eller i vareforbruget for denne salgsordrefaktura.

Når indkøbsordren bogføres, modtages lagervarerne til et kostpris på kr. 120,00. Hvis salgsordredokumentet afmærkes til indkøbsordren, før følgesedlen eller fakturaen bogføres, vil vareforbruget være USD 120,00 i stedet for den aktuelle løbende gennemsnitskostpris for varen. Hvis følgesedlen eller fakturaen for salgsordren bogføres, før afmærkningen finder sted, bogføres vareforbruget til den løbende gennemsnitskostpris.

Før lagerlukningen udføres, kan disse to posteringer afmærkes til hinanden.

Når en tilgangstransaktion er afmærket til en afgangstransaktion, vil den værdiansættelsesmetode, der er valgt for varens modelgruppe, blive tilsidesat, og systemet udligner disse transaktioner mod hinanden.

Du kan afmærke en afgangspostering til en tilgang, før posteringen bogføres. Du afmærke dette fra en salgsordrelinje på siden **Oplysninger om salgsordre**. Du kan se de åbne tilgangsposteringer på siden **Afmærkning**.

Du kan også afmærke en afgangspostering til en tilgang, efter posteringen bogføres. Du kan matche eller afmærke en afgangspostering for en åben tilgangspostering for en lagerført vare fra en bogført lagerreguleringskladde.

I følgende diagram vises disse posteringer:

**Dag 1:**

- 1a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
- 1b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
- 2a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
- 2b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 22,00 pr. stk.
- 3a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 16,00 (løbende gennemsnit af økonomisk bogførte posteringer).
- 3b. Økonomisk lagerafgang for et antal på 1 til en kostpris af USD 16,00 (løbende gennemsnit af økonomisk bogførte posteringer).
- 3c. Økonomisk lagerafgang for transaktion 3b er afmærket til økonomisk lagerafgang for transaktion 2b.

**Dag 2:**

- 4a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 25,00 pr. stk.
- 5a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
- 5b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
- 6a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 23,00 (løbende gennemsnit af økonomisk bogførte posteringer).

**Dag 3:**

- 7\. Lagerlukningen udføres. På baggrund af afmærkningsprincippet, der bruger metoden for vægtet gennemsnit, udlignes de markerede posteringer mod hinanden. I dette eksempel udlignes transaktion 3b mod transaktion 2b, og der bogføres en regulering på USD 6,00 for transaktion 3b for at få værdien til at blive USD 22,00. I dette eksempel foretages der ingen yderligere udligninger, da lukningen kun opretter udligninger for økonomisk opdaterede posteringer.

I følgende diagram vises denne serie af posteringer, og virkningerne af at vælge lagermodellen for vægtet gennemsnitsdato med afmærkning.

![Vægtet gennemsnit med afmærkning.](media/weighted-average-date-with-marking.png)

**Forklaring til diagram:**

- Lagertransaktioner vises som lodrette pile.
- Fysiske posteringer vises med kortere, lysegrå pile.
- Økonomiske posteringer vises med længere sorte pile.
- Lagertilgange vises som lodrette pile over aksen.
- Lagerafgange vises som lodrette pile under aksen.
- Hver enkelt ny tilgangs- eller afgangspostering er markeret med en ny etiket.
- Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Identifikatorerne angiver rækkefølgen af lagerposteringsbogføringer på tidslinjen.
- Datoer er adskilt af tynde sorte lodrette linjer. Datoerne angives nederst i diagrammet.
- Lagerlukninger angives med røde lodrette stiplede linjer.
- Udligninger, der foretages ved lagerlukning, angives med stiplede, røde pile, der går diagonalt fra en tilgang til en afgang.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
