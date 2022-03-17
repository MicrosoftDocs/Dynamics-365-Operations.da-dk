---
title: Vægtet gennemsnit med fysisk værdi og afmærkning
description: Vægtet gennemsnit er en lagermodel, der er baseret på princippet for vægtet gennemsnit, hvor afgange fra lager værdisættes til gennemsnitsværdien for varer, der er modtaget på lager i lagerlukningsperioden, samt en eventuel disponibel lagerbeholdning fra forrige periode.
author: AndersGirke
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65501
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c124716b70be837573506a738ef2034397f2bda
ms.sourcegitcommit: addae271ddfc5a8b0721c23337f69916153db4cd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/21/2022
ms.locfileid: "8330220"
---
# <a name="weighted-average-with-physical-value-and-marking"></a>Vægtet gennemsnit med fysisk værdi og afmærkning

[!include [banner](../includes/banner.md)]

Det vægtede gennemsnit er en lagermodel, der er baseret på et gennemsnit, der er resultatet af multiplikationen af hver komponent (varetransaktion) med en faktor (kostpris), der afspejler vigtigheden (antallet). Man kan også sige, at vægtet gennemsnit er en lagermodel, der tildeler omkostningen ved afgangsposteringer på basis af middelværdien af alle de lagervarer, der modtages i perioden, plus en eventuel disponibel lagerbeholdning fra forrige periode.

Når du kører en lagerlukning ved hjælp af lagermodellen for vægtet gennemsnit, kan der oprettes en udligning på to måder. Typisk udlignes alle tilgange mod en virtuel afgang, der indeholder den samlede modtagne mængde og værdi. Denne virtuelle afgang har en tilsvarende virtuel tilgang, som tilgangene vil blive udlignet fra. På denne måde opnår alle afgange samme gennemsnitskostpris. Den virtuelle afgang og tilgang kan ses som en virtuel overførsel, som kaldes *lagerlukningsoverførsel efter vægtet gennemsnit*. Denne udligningsmetode kaldes en *opsummeret udligning for vægtet gennemsnit*. Hvis der kun er én tilgang, kan alle afgange udlignes fra den, og der oprettes ikke en virtuel overførsel. Denne udligningsmetode kaldes en *direkte udligning*. Alle de lagerbeholdninger, der er disponible efter lagerlukningen, værdisættes ved det vægtede gennemsnit fra forrige periode og medtages i beregningen af vægtet gennemsnit i den næste periode.

Du kan tilsidesætte princippet for vægtet gennemsnit ved at markere lagerposteringer, så en specifik varetilgang udlignes mod en specifik afgang. Der kræves en periodisk lagerlukning, når du bruger lagermodellen vægtet gennemsnit til at oprette udligninger og regulere værdien af afgange i henhold til princippet for vægtet gennemsnit. Indtil du kører lagerlukningsprocessen, værdisættes afgangsposteringerne med det løbende gennemsnit, når de fysiske og økonomiske opdateringer finder sted. Medmindre du bruger afmærkning, beregnes det løbende gennemsnit, når den fysiske eller økonomiske opdatering udføres.

Det vægtede gennemsnit for lagerlukningsmetoden beregnes efter følgende formel:

- Vægtet gennemsnit = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q *n* × P *n*\]) ÷ (Q1 + Q2 + Q *n*)

Q = antal af transaktionen  
P = pris for transaktionen

Udligninger er lagerlukningsbogføringer, der bruges til at justere afgangene til det korrekte vægtede gennemsnit fra og med lukningsdatoen. I følgende eksempler illustreres virkningen af at bruge vægtet gennemsnit i fem forskellige konfigurationer:

- Direkte udligning for vægtet gennemsnit uden indstillingen **Medtag fysisk værdi**
- Opsummeret udligning for vægtet gennemsnit uden indstillingen **Medtag fysisk værdi**
- Direkte udligning for vægtet gennemsnit med indstillingen **Medtag fysisk værdi**
- Opsummeret udligning for vægtet gennemsnit med indstillingen **Medtag fysisk værdi**
- Vægtet gennemsnit med afmærkning

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Direkte udligning for vægtet gennemsnit uden indstillingen Medtag fysisk værdi

Med princippet for direkte udligning oprettes der udligninger direkte mellem tilgange og afgange uden at oprette flere lagerposteringer. Systemet bruger dette udligningsprincip i følgende situationer:

- Der er blevet bogført én tilgang og en eller flere afgange i perioden.
- I perioden er der kun blevet bogført afgange, og der er disponible varer på lager fra en tidligere lukning.

I dette eksempel er markeringen i afkrydsningsfeltet **Medtag fysisk værdi** fjernet i **Varemodelgruppe** for det frigivne produkt. I følgende illustration vises disse posteringer:

- 1a. Fysisk lagertilgang for et antal på 10 til en kostpris a kr. 10,00 pr. stk.
- 1b. Økonomisk lagertilgang for et antal på 10 til en kostpris a kr. 10,00 pr. stk.
- 2a. Fysisk lagertilgang for et antal på 10 til en kostpris a kr. 20,00 pr. stk.
- 3a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 10,00 (løbende gennemsnit af økonomisk bogførte posteringer).
- 3b. Økonomisk lagerafgang for et antal på 1 til en kostpris af USD 10,00 (løbende gennemsnit af økonomisk bogførte posteringer).
- 4a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 10,00 hver (løbende gennemsnit af økonomisk bogførte posteringer).
- 4b. Økonomisk lagerafgang for et antal på 1 til en kostpris af USD 10,00 hver (løbende gennemsnit af økonomisk bogførte posteringer).
- 5a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 10,00 hver (løbende gennemsnit af økonomisk bogførte posteringer).
- 6\. Lagerlukningen udføres. På baggrund af metoden for vægtet gennemsnit bruger systemet den direkte udligningsmetode, da der kun er én tilgang, der er økonomisk opdateret i perioden. I dette eksempel oprettes der én udligning mellem 1b og 3b og en anden mellem 1b og 4b. Der foretages ingen regulering, fordi det løbende gennemsnit er det samme som det vægtede gennemsnit.

I følgende diagram illustreres denne række posteringer med effekterne ved at vælge lagermodellen for vægtet gennemsnit og princippet for direkte udligning uden indstillingen **Medtag fysisk værdi**.

![Direkte udligning for vægtet gennemsnit uden Medtag fysisk værdi.](media/weighted-average-direct-settlement-without-include-physical-value.png)

**Forklaring til diagram**

- Lagertransaktioner vises som lodrette pile.
- Fysiske posteringer vises med kortere, lysegrå pile.
- Økonomiske posteringer vises med længere sorte pile.
- Lagertilgange vises som lodrette pile over aksen.
- Lagerafgange vises som lodrette pile under aksen.
- Hver enkelt ny tilgangs- eller afgangspostering er markeret med en ny etiket.
- Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Identifikatorerne angiver rækkefølgen af lagerposteringsbogføringer på tidslinjen.
- Hver dato i diagrammet er adskilt af en tynd sort lodret linje. Datoen angives nederst i diagrammet.
- Lagerlukninger angives med en rød lodret stiplet linje.
- Udligninger, der foretages ved lagerlukning, angives med stiplede, røde pile, der går diagonalt fra en tilgang til en afgang.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Opsummeret udligning for vægtet gennemsnit uden indstillingen Medtag fysisk værdi

Når der er flere tilgange i en periode, bruger vægtet gennemsnit det opsummerede udligningsprincip, hvor alle tilgange i en lukningsperiode opsummeres i en transaktion, der kaldes *lagerlukning for vægtet gennemsnit*. Alle periodens tilgange udlignes mod afgangen i den nyoprettede lagertransaktion. Alle periodens afgange udlignes mod tilgangen i den nye lagertransaktion. Hvis der er en resterende disponibel lagerbeholdning efter lagerlukningen, medtages denne disponible lagerbeholdning i tilgangstransaktionen for lagerlukningstransaktionen med det vægtede gennemsnit.

De efterfølgende posteringer illustreres i følgende grafik:

- 1a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
- 1b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
- 2a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
- 2b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 22,00 pr. stk.
- 3a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 16,00 (løbende gennemsnit af økonomisk bogførte posteringer).
- 3b. Økonomisk lagerafgang for et antal på 1 til en kostpris af USD 16,00 (løbende gennemsnit af økonomisk bogførte posteringer).
- 4a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 25,00 pr. stk.
- 5a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
- 5b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
- 6a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 23,00 (løbende gennemsnit af økonomisk bogførte posteringer).
- 7\. Lagerlukningen udføres.
- 7a. Der oprettes en økonomisk afgang af typen lagerlukningstransaktion for vægtet gennemsnit for at opsummere udligningerne for alle økonomiske lagertilgange.
  - Transaktion 1b udlignes for et antal på 1 med et udlignet beløb af USD 10,00.
  - Transaktion 2b udlignes for et antal på 1 med et udlignet beløb af USD 22,00.
  - Transaktion 5b udlignes for et antal på 1 med et udlignet beløb af USD 30,00.
  - Transaktion 7a. oprettes for et antal på 3 med et udlignet beløb af USD 62,00. Denne transaktion modregner summen af de tre tilgangsposteringer, der er økonomisk opdateret i perioden.
- 7b. Der oprettes en økonomisk tilgang for lagerlukningstransaktion med vægtet gennemsnit som modpostering for økonomisk bogførte afgange.
  - Transaktion 3b udlignes for et antal på 1 med et udlignet beløb af USD 20,67. Denne transaktion reguleres med USD 4,67 for at sætte den oprindelige værdi af USD 16,00 til 20,67, som er det vægtede gennemsnit af økonomisk bogførte transaktioner for perioden.
  - Transaktion 7b. oprettes for et antal på 1 med et udlignet beløb af USD 20,67 til modregning 3b. Denne transaktion modregner summen af én tilgangstransaktion, der er økonomisk opdateret i perioden.

I følgende diagram illustreres denne række posteringer med effekterne ved at vælge lagermodellen for vægtet gennemsnit og princippet for opsummerede udligning uden indstillingen **Medtag fysisk værdi**.

![Opsummeret udligning for vægtet gennemsnit uden Medtag fysisk værdi.](media/weighted-average-summarized-settlement-without-include-physical-value.png)

**Forklaring til diagram**

- Lagertransaktioner vises som lodrette pile.
- Fysiske posteringer vises med kortere, lysegrå pile.
- Økonomiske posteringer vises med længere sorte pile.
- Lagertilgange vises som lodrette pile over aksen.
- Lagerafgange vises som lodrette pile under aksen.
- Hver enkelt ny tilgangs- eller afgangspostering er markeret med en ny etiket.
- Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Identifikatorerne angiver rækkefølgen af lagerposteringsbogføringer på tidslinjen.
- Hver dato i diagrammet er adskilt af en tynd sort lodret linje. Datoen angives nederst i diagrammet.
- Lagerlukninger angives med en rød lodret stiplet linje.
- Udligninger, der foretages ved lagerlukning, angives med stiplede, røde pile, der går diagonalt fra en tilgang til en afgang.

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Direkte udligning for vægtet gennemsnit med indstillingen Medtag fysisk værdi

Parameteren **Medtag fysisk værdi** fungerer anderledes for lagermodellen for vægtet gennemsnit end i tidligere versioner af produktet. Hvis du vælger indstillingen **Medtag fysisk værdi** for en vare i formularen **Varemodelgruppe**, bruger systemet fysisk opdaterede tilgange, når det beregner den forkalkulerede afgangskostpris eller løbende gennemsnit. Afgangene posteres på basis af denne forkalkulerede kostpris i løbet af perioden. Under lagerlukningen tages kun økonomisk opdaterede tilgange i betragtning ved beregning af det vægtede gennemsnit.

De efterfølgende posteringer illustreres i følgende grafik:

- 1a. Fysisk lagertilgang for et antal på 10 til en kostpris a kr. 10,00 pr. stk.
- 1b. Økonomisk lagertilgang for et antal på 10 til en kostpris a kr. 10,00 pr. stk.
- 2a. Fysisk lagertilgang for et antal på 10 til en kostpris a kr. 20,00 pr. stk.
- 3a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 15,00 (løbende gennemsnit af økonomisk og fysisk opdaterede posteringer).
- 3b. Økonomisk lagerafgang for et antal på 1 til en kostpris af USD 15,00 (løbende gennemsnit af økonomisk og fysisk opdaterede posteringer).
- 4a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 15,00 hver (løbende gennemsnit af økonomisk og fysisk opdaterede posteringer).
- 4b. Økonomisk lagerafgang for et antal på 1 til en kostpris af USD 15,00 hver (løbende gennemsnit af økonomisk og fysisk opdaterede posteringer).
- 5a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 15,00 hver (løbende gennemsnit af økonomisk og fysisk opdaterede posteringer).
- 6\. Lagerlukningen udføres. På baggrund af metoden for vægtet gennemsnit bruger systemet den direkte udligningsmetode, da der kun er én tilgang, der er økonomisk opdateret i perioden. I dette eksempel oprettes der én udligning mellem 1b og 3b og en anden mellem 1b og 4b. Transaktion 3b og 4b reguleres hver med USD -5,00 for at få værdien USD 10,00.

I følgende diagram illustreres denne række posteringer med effekterne ved at vælge lagermodellen for vægtet gennemsnit og princippet for direkte udligning med indstillingen **Medtag fysisk værdi**.

![Direkte udligning for vægtet gennemsnit med Medtag fysisk værdi.](media/weighted-average-direct-settlement-with-include-physical-value.png)

**Forklaring til diagram**

- Lagertransaktioner vises som lodrette pile.
- Fysiske posteringer vises med kortere, lysegrå pile.
- Økonomiske posteringer vises med længere sorte pile.
- Lagertilgange vises som lodrette pile over aksen.
- Lagerafgange vises som lodrette pile under aksen.
- Hver enkelt ny tilgangs- eller afgangspostering er markeret med en ny etiket.
- Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Identifikatorerne angiver rækkefølgen af lagerposteringsbogføringer på tidslinjen.
- Hver dato i diagrammet er adskilt af en tynd sort lodret linje. Datoen angives nederst i diagrammet.
- Lagerlukninger angives med en rød lodret stiplet linje.
- Udligninger, der foretages ved lagerlukning, angives med stiplede, røde pile, der går diagonalt fra en tilgang til en afgang.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Opsummeret udligning for vægtet gennemsnit med indstillingen Medtag fysisk værdi

Parameteren **Medtag fysisk værdi** fungerer anderledes for vægtet gennemsnit end i tidligere versioner. Markér feltet **Medtag fysisk værdi** for en vare på siden **Varemodelgruppe**. Derefter bruger systemet fysisk opdaterede tilgange ved beregning af den forkalkulerede kostpris eller det løbende gennemsnit. Afgangene posteres på basis af denne forkalkulerede kostpris i løbet af perioden. Under lagerlukningen tages kun økonomisk opdaterede tilgange i betragtning ved beregning af det vægtede gennemsnit. Det anbefales at bruge en månedlig lagerlukning, når du bruger lagermodellen for vægtet gennemsnit. I dette eksempel med opsummeret udligning for vægtet gennemsnit er lagermodellen markeret, så den medtager den fysiske værdi.

De efterfølgende posteringer illustreres i følgende grafik:

- 1a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
- 1b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
- 2a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
- 2b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 22,00 pr. stk.
- 3a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 16,00 (løbende gennemsnit af økonomisk og fysisk opdaterede posteringer).
- 3b. Økonomisk lagerafgang for et antal på 1 til en kostpris af USD 16,00 (løbende gennemsnit af økonomisk og fysisk opdaterede posteringer).
- 4a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 25,00 pr. stk.
- 5a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
- 5b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
- 6a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 23,67 (løbende gennemsnit af økonomisk og fysisk opdaterede posteringer).
- 7\. Lagerlukningen udføres.
- 7a. Der oprettes en økonomisk afgang af typen lagerlukningstransaktion for vægtet gennemsnit for at opsummere udligningerne for alle økonomiske lagertilgange.
  - Transaktion 1b udlignes for et antal på 1 med et udlignet beløb af USD 10,00.
  - Transaktion 2b udlignes for et antal på 1 med et udlignet beløb af USD 22,00.
  - Transaktion 5b udlignes for et antal på 1 med et udlignet beløb af USD 30,00.
  - Transaktion 7a. oprettes for et antal på 3 med et udlignet beløb af USD 62,00.  
- 7b. Der oprettes en økonomisk tilgang for lagerlukningstransaktion med vægtet gennemsnit som modpostering for økonomisk lukkede afgangstransaktioner.
  - Transaktion 3b udlignes for et antal på 1 med et udlignet beløb af USD 20,67. Denne transaktion reguleres med USD 4,67 for at sætte den oprindelige værdi af USD 16,00 til 20,67, som er det vægtede gennemsnit af økonomisk bogførte transaktioner for perioden.
  - Transaktion 7b. oprettes for et antal på 1 med et udlignet beløb af USD 20,67 til modregning 3b.

I følgende diagram illustreres denne række posteringer med effekterne ved at vælge lagermodellen for vægtet gennemsnit og princippet for opsummerede udligning uden indstillingen **Medtag fysisk værdi**.

![Opsummeret udligning for vægtet gennemsnit med Medtag fysisk værdi.](media/weighted-average-summarized-settlement-with-include-physical-value.png)

**Forklaring til diagram**

- Lagertransaktioner vises som lodrette pile.
- Fysiske posteringer vises med kortere, lysegrå pile.
- Økonomiske posteringer vises med længere sorte pile.
- Lagertilgange vises som lodrette pile over aksen.
- Lagerafgange vises som lodrette pile under aksen.
- Hver enkelt ny tilgangs- eller afgangspostering er markeret med en ny etiket.
- Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Identifikatorerne angiver rækkefølgen af lagerposteringsbogføringer på tidslinjen.
- Hver dato i diagrammet er adskilt af en tynd sort lodret linje. Datoen angives nederst i diagrammet.
- Lagerlukninger angives med en rød lodret stiplet linje.
- Udligninger, der foretages ved lagerlukning, angives med stiplede, røde pile, der går diagonalt fra en tilgang til en afgang.

## <a name="weighted-average-with-marking"></a>Vægtet gennemsnit med afmærkning

Afmærkning er en proces, som giver dig mulighed for at tilknytte – eller afmærke – en afgangspostering til en tilgangspostering. Afmærkning kan ske enten før eller efter, at en postering er bogført. Du kan bruge afmærkning, når du vil være sikker på den nøjagtige kostpris for lageret, når posteringen bogføres, eller når lagerlukningen udføres.

Antag f.eks., at firmaets kundeserviceafdeling har modtaget en hasteordre fra en vigtig kunde. Da dette er en hasteordre, vil du skulle betale mere for denne vare for at kunne imødekomme kundens forespørgsel. Du skal være sikker på, at kostprisen på denne lagervare afspejles i dækningsbidraget eller i vareforbruget for denne salgsordrefaktura.

Når indkøbsordren bogføres, modtages lagervarerne til et kostpris på kr. 120,00. Dette salgsordredokument afmærkes f.eks. til indkøbsordren, før følgesedlen eller fakturaen bogføres. Vareforbruget vil være kr. 120,00 i stedet for den aktuelle løbende gennemsnitskostpris for varen. Hvis følgesedlen eller fakturaen for salgsordren bogføres, før afmærkningen finder sted, bogføres vareforbruget til den løbende gennemsnitskostpris.

Før lagerlukningen udføres, kan disse to posteringer afmærkes til hinanden.

En tilgangspostering afmærkes til en afgangspostering. Derefter ses der bort fra den vurderingsmetode, der er valgt for varens varemodelgruppe, og i systemet udlignes disse poster i forhold til hinanden.

Du kan afmærke en afgangspostering til en tilgang, før posteringen bogføres. Du kan gøre dette fra en salgsordrelinje på siden **Oplysninger om salgsordre**. Du kan se de åbne tilgangsposteringer på siden **Afmærkning**.

Du kan afmærke en afgangspostering til en tilgang, efter at posteringen er bogført. Du kan matche eller afmærke en afgangspostering for en åben tilgangspostering for en lagerført vare fra en bogført lagerreguleringskladde.

De efterfølgende posteringer illustreres i følgende grafik:

- 1a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
- 1b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
- 2a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
- 2b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 22,00 pr. stk.
- 3a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 16,00 (løbende gennemsnit af økonomisk bogførte posteringer).
- 3b. Økonomisk lagerafgang for et antal på 1 til en kostpris af USD 16,00 (løbende gennemsnit af økonomisk bogførte posteringer).
- 3c. Økonomisk lagerafgang for 3b er afmærket til økonomisk lagerafgang for 2b.
- 4a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 25,00 pr. stk.
- 5a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
- 5b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
- 6a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 23,00 (løbende gennemsnit af økonomisk bogførte posteringer).
- 7\. Lagerlukningen udføres. På baggrund af afmærkningsprincippet, der bruger metoden for vægtet gennemsnit, udlignes de markerede posteringer mod hinanden. I dette eksempel udlignes 3b mod 2b, og der bogføres en regulering på USD 6,00 for 3b for at få værdien til at blive USD 22,00. I dette eksempel foretages der ingen yderligere udligninger, da lukningen kun opretter udligninger for økonomisk opdaterede posteringer.

I følgende diagram illustreres denne serie posteringer med virkningerne af at vælge lagermodellen for vægtet gennemsnit ved afmærkning.

![Vægtet gennemsnit med afmærkning.](media/weighted-average-with-marking.png)

**Forklaring til diagram**

- Lagertransaktioner vises som lodrette pile.
- Fysiske posteringer vises med kortere, lysegrå pile.
- Økonomiske posteringer vises med længere sorte pile.
- Lagertilgange vises som lodrette pile over aksen.
- Lagerafgange vises som lodrette pile under aksen.
- Hver enkelt ny tilgangs- eller afgangspostering er markeret med en ny etiket.
- Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Identifikatorerne angiver rækkefølgen af lagerposteringsbogføringer på tidslinjen.
- Hver dato i diagrammet er adskilt af en tynd sort lodret linje. Datoen angives nederst i diagrammet.
- Lagerlukninger angives med en rød lodret stiplet linje.
- Udligninger, der foretages ved lagerlukning, angives med stiplede, røde pile, der går diagonalt fra en tilgang til en afgang.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
