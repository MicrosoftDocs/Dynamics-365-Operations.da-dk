---
title: Gennemsnitskostdato
description: Gennemsnitskostdato er en lagermodel, der er baseret på princippet for vægtet gennemsnit, hvor lagerafgange værdisættes til den gennemsnitlige værdi af de varer, der modtages på lageret, for hver enkelt dag i lagerlukningsperioden.
author: AndersGirke
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 28991
ms.assetid: 945d5088-a99d-4e54-bc42-d2bd61c61e22
ms.search.region: Global
ms.search.industry: Retail
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9963c17d8ac1854a42cac2a0e19615f13e8cc006
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543623"
---
# <a name="weighted-average-date"></a>Gennemsnitskostdato

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Gennemsnitskostdatoen er en lagermodel, der er baseret på princippet om vægtet gennemsnit. For princippet om vægtet princip værdisættes afgange fra lageret til gennemsnitsværdien for de varer, der modtages på lageret hver enkelt dag i lagerlukningsperioden. 

Når du kører en lagerlukning ved brug af vægtet gennemsnitsdato, udlignes alle daglige tilgange mod en virtuel afgang. Denne virtuelle afgang indeholder den samlede modtagne mængde og værdi for denne dag. Denne virtuelle afgang har en tilsvarende virtuel tilgang, som tilgangene udlignes mod. På denne måde opnår alle afgange derfor samme gennemsnitskostpris. Den virtuelle afgang og virtuelle tilgang kan betragtes som en virtuel overførsel, som kaldes *lagerlukningsoverførsel efter vægtet gennemsnit*. 

Hvis der kun har været én tilgang til og med denne dato, er det ikke nødvendigt at vurdere gennemsnittet. Det er fordi, at alle tilgange udlignes fra den tilgang, og der oprettes ikke en virtuel overførsel. Hvis der kun forekommer afgange på denne dato, vil der ligeledes ikke være nogen tilgange, som gennemsnittet kan vurderes fra, og der oprettes ikke en virtuel overførsel. Når du bruger vægtet gennemsnit, kan du vælge at markere lagertransaktioner, så en specifik varetilgang udlignes mod en specifik afgang. I dette tilfælde bruger du ikke reglen om vægtet gennemsnitsdato. Det anbefales at bruge en månedlig lagerlukning, når du bruger lagermodellen for gennemsnitskostdato. 

Følgende formel bruges til at beregne det vægtede gennemsnit for datoefterkalkulationsmetoden: 

Vægtet gennemsnit = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q*n* × P*n*\]) ÷ (Q1 + Q2 + Q*n*) 

Under lagerlukning udføres beregningen dagligt gennem lukningsperioden, som vist i nedenstående illustration. 

![Daglig beregningsmodel med vægtet gennemsnit ud fra dato](./media/weightedaveragedatedailycalculationmodel.gif) 

Lagerposteringer, der forlader lageret, f.eks. salgsordrer, lagerkladder og produktionsordrer, vil blive udført til en forkalkuleret kostpris på bogføringsdatoen. Den forkalkulerede kostpris kaldes også den løbende gennemsnitskostpris. På lagerlukningsdatoen analyserer systemet lagertransaktionerne for tidligere perioder, tidligere dage og den aktuelle dag. Denne analyse bruges til at bestemme, hvilket af følgende lukningsprincipper der skal bruges:

-   Direkte udligning
-   Opsummeret udligning

Udligninger er lagerlukningsbogføringer, der bruges til at justere afgangene til det korrekte vægtede gennemsnit fra og med lukningsdatoen. 

**Bemærk:** Se artikel om lagerlukning for yderligere oplysninger om udligninger. I følgende eksempler illustreres virkningen af at bruge vægtet gennemsnit i fem konfigurationer:

-   Direkte udligning for gennemsnitskostdato, når indstillingen **Medtag fysisk værdi** ikke bruges
-   Opsummeret udligning for gennemsnitskostdato, når indstillingen **Medtag fysisk værdi** ikke bruges
-   Direkte udligning for gennemsnitskostdato, når indstillingen **Medtag fysisk værdi** bruges
-   Opsummeret udligning for gennemsnitskostdato, når indstillingen **Medtag fysisk værdi** bruges
-   Dato for vægtet gennemsnit, når afmærkning bruges

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Direkte udligning for gennemsnitskostdato, når indstillingen Medtag fysisk værdi ikke bruges
Den aktuelle version bruger det samme princip for direkte udligning, der blev brugt til vægtet gennemsnit i tidligere versioner. Systemet udligner direkte mellem tilgange og afgange. Systemet bruger dette direkte udligningsprincip i bestemte situationer:

-   Der er blevet bogført én tilgang og en eller flere afgange i perioden.
-   I perioden er der kun blevet bogført afgange, og der er disponible varer på lager fra en tidligere lukning.

I følgende scenarie er der bogført en økonomisk opdateret tilgang og afgang. Ved lagerlukningen udligner systemet tilgangen direkte mod afgangen, og det er ikke nødvendigt af justere kostprisen ved afgangen. 

Følgende illustration viser disse posteringer:

-   1a. Fysisk lagertilgang er opdateret for et antal på 5 til en kostpris a kr. 10,00 pr. stk.
-   1b. Økonomisk lagertilgang er opdateret for et antal på 5 til en kostpris af kr. 10,00 pr. stk.
-   2a. Fysisk lagerafgang er opdateret for et antal på 2 til en kostpris af kr. 10,00 pr. stk.
-   2b. Økonomisk lagerafgang er opdateret for et antal på 2 til en kostpris af kr. 10,00 pr. stk.
-   3. Lagerlukningen er udført ved brug af den direkte udligningsmetode for at udligne den økonomiske lagertilgang med den økonomiske lagerafgang.

![Direkte udligning for gennemsnitskostdato uden indstillingen Medtag fysisk værdi](./media/weightedaveragedatedirectsettlementwithoutincludephysicalvalue.gif) 

**Nøgle til illustrationen:**

-   Lagertransaktioner vises som lodrette pile.
-   Lagertilgange vises som lodrette pile over tidslinjen.
-   Lagerafgange vises som lodrette pile under tidslinjen.
-   Over eller under hver enkelt lodret pil angives værdien af lagertransaktionen i formatet *Antal*@*stykpris*.
-   Hvis en lagerposteringsværdi er omgivet af parenteser, bogføres lagerposteringen fysisk på lageret.
-   Hvis en lagerposteringsværdi ikke er omgivet af parenteser, bogføres lagerposteringen økonomisk på lageret.
-   Hver enkelt ny tilgangs- eller afgangspostering er markeret med en ny etiket.
-   Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Id'erne angiver rækkefølgen af lagertransaktionsbogføringer på tidslinjen.
-   Lagerlukninger angives med en rød, lodret stiplet linje og etiketten *Lagerlukning*.
-   Udligninger, der foretages ved lagerlukningen, angives med stiplede røde pile, der går diagonalt fra en tilgang til en afgang.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Opsummeret udligning for gennemsnitskostdato, når indstillingen Medtag fysisk værdi ikke bruges
Det vægtede gennemsnit er baseret på princippet om, at alle tilgange i en lukningsperiode opsummeres i en ny lageroverførselspost. Denne postering kaldes*Lagerlukning for vægtet gennemsnit*. Alle dagens tilgange udlignes mod afgangen i den nyoprettede lageroverførselspostering. Alle dagens afgange udlignes mod tilgangen i den nye lageroverførselspostering. Hvis den disponible lagerbeholdning er positiv efter lagerlukningen, opsummeres denne disponible lagerbeholdning og værdien af lageret i den nye lageroverførselsposteringstilgang. Hvis den disponible lagerbeholdning er negativ efter lagerlukningen, udgør den disponible lagerbeholdning og værdien af lageret summen af individuelle afgange, der ikke er blevet fuldt udlignet. 

I følgende scenarie er flere økonomisk opdaterede tilgange og afgange blevet bogført i perioden. Ved lagerlukningen evaluerer systemet hver enkelt dag for at bestemme, hvordan den enkelte dag skal behandles ved lukningen. 

Følgende illustration viser disse posteringer: 

**Dag 1:**

-   1a. Fysisk lagertilgang er opdateret for et antal på 3 til en kostpris af kr. 15,00 pr. stk.
-   1b. Økonomisk lagertilgang er opdateret for et antal på 3 til en kostpris af kr. 15,00 pr. stk.
-   2a. Fysisk lagerafgang for et antal på 1 til en løbende gennemsnitskostpris af kr. 15,00 pr. styk
-   2b. Økonomisk lagerafgang for et antal på 1 til en løbende gennemsnitskostpris af kr. 15,00 pr. styk

Systemet bruger direkte udligning for dag 1. 

**Dag 2:**

-   3a. Fysisk lagerafgang for et antal på 1 til en løbende gennemsnitskostpris af kr. 15,00 pr. styk
-   3b. Økonomisk lagerafgang for et antal på 1 til en løbende gennemsnitskostpris af kr. 15,00 pr. styk

Systemet bruger direkte udligning for dag 2. 

**Dag 3:**

-   4a. Fysisk lagerafgang for et antal på 1 til en løbende gennemsnitskostpris af kr. 15,00 pr. styk
-   4b. Økonomisk lagerafgang for et antal på 1 til en løbende gennemsnitskostpris af kr. 15,00 pr. styk
-   5a. Fysisk lagertilgang for et antal på 1 til en kostpris af kr. 17,00 pr. styk
-   5b. Økonomisk lagertilgang for et antal på 1 til en kostpris af kr. 17,00 pr. styk

Lagerlukningen udføres. Der skal benyttes direkte udligning, fordi der er flere tilgange, der krydser flere dage.

-   7a. Der oprettes en økonomisk afgang for lagerlukningspostering for et antal på 2 til kr. 32,00 pr. stk. for at opsummere udligninger af alle økonomiske lagertilgange på en dato, hvor der ikke er udført lukning.
-   7b. Der oprettes en økonomisk tilgang for lagerlukningstransaktion for at modpostering for 7a.

Systemet genererer og bogfører den summerede lageroverførselspostering. Systemet udligner også alle dagens tilgange og disponible lagerbeholdning for tidligere dage mod den opsummerede lageroverførselsafgangspostering. Alle dagens afgange udlignes mod den opsummerede lageroverførselstilgangspostering. Den vægtede gennemsnitskostpris beregnes til at være kr. 16,00. Afgangen vil have en justering på kr. 1,00 for justere den til den vægtede gennemsnitskostpris. Den nye løbende gennemsnitskostpris er kr. 16,00. 

I følgende illustration viser denne række posteringer, og effekterne ved at vælge lagermodellen for vægtet gennemsnit og princippet for opsummeret udligning, men uden brug af indstillingen **Medtag fysisk værdi**. 

![Opsummeret udligning for gennemsnitskostdato uden indstillingen Medtag fysisk værdi](./media/weightedaveragedatesummarizedsettlementwithoutincludephysicalvalue.gif) 

**Nøgle til illustrationen**

-   Lagertransaktioner vises som lodrette pile.
-   Lagertilgange vises som lodrette pile over tidslinjen.
-   Lagerafgange vises som lodrette pile under tidslinjen.
-   Over eller under hver enkelt lodret pil angives værdien af lagertransaktionen i formatet *Antal*@*stykpris*.
-   Hvis en lagerposteringsværdi er omgivet af parenteser, bogføres lagerposteringen fysisk på lageret.
-   Hvis en lagerposteringsværdi ikke er omgivet af parenteser, bogføres lagerposteringen økonomisk på lageret.
-   Hver enkelt ny tilgangs- eller afgangspostering er markeret med en ny etiket.
-   Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Id'erne angiver rækkefølgen af lagertransaktionsbogføringer på tidslinjen.
-   Lagerlukninger angives med en rød, lodret stiplet linje og etiketten *Lagerlukning*.
-   Udligninger, der foretages ved lagerlukningen, angives med stiplede røde pile, der går diagonalt fra en tilgang til en afgang.
-   Helt udfyldte røde diagonale pile viser den tilgangspostering, der udlignes mod den afgangspostering, der oprettes af systemet.
-   Den helt grønne diagonale pil illustrerer den systemgenererede tilgangsmodpostering, som den oprindeligt bogførte afgangspostering udlignes til.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Direkte udligning for gennemsnitskostdato, når indstillingen Medtag fysisk værdi bruges
I denne aktuelle version bruges det samme princip for direkte udligning til vægtet gennemsnitsdato, som blev brugt tidligere versioner. Systemet udligner direkte mellem tilgange og afgange. Systemet bruger dette direkte udligningsprincip i bestemte situationer:

-   Der er blevet bogført én tilgang og en eller flere afgange i perioden.
-   I perioden er der kun blevet bogført afgange, og lageret indeholder disponibel lagerbeholdning fra en tidligere lukning.

Hvis du markerer afkrydsningsfeltet **Medtag fysisk værdi** for en vare på siden **Varemodelgruppe**, bruger systemet fysisk opdaterede tilgange, når det beregner den forkalkulerede kostpris eller løbende gennemsnit. Afgange posteres på basis af denne forkalkulerede kostpris i løbet af perioden. Under lagerlukningen vil kun økonomisk opdaterede tilgange blive taget i betragtning i beregningen af det vægtede gennemsnit.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Opsummeret udligning for gennemsnitskostdato, når indstillingen Medtag fysisk værdi bruges
Hvis du markerer afkrydsningsfeltet **Medtag fysisk værdi** for en vare på siden **Varemodelgruppe**, bruger systemet fysisk opdaterede tilgange, når det beregner den forkalkulerede kostpris eller løbende gennemsnit. Afgange posteres på basis af denne forkalkulerede kostpris i løbet af perioden. Under lagerlukningen vil kun økonomisk opdaterede tilgange blive taget i betragtning i beregningen af det vægtede gennemsnit. Den vægtede udligning baseres på det princip, at alle tilgange i en lukningsperiode opsummeres i en ny lageroverførselspostering, der kaldes *lagerlukning for vægtet gennemsnit*. Alle dagens tilgange udlignes mod afgangen i den nyoprettede lageroverførselspostering. Alle dagens afgange udlignes mod tilgangen i den nye lageroverførselspostering. Hvis den disponible lagerbeholdning er positiv efter lagerlukningen, opsummeres denne disponible lagerbeholdning og værdien af lageret i den nye lageroverførselspostering (tilgang). Hvis den disponible lagerbeholdning er negativ efter lagerlukningen, udgør den disponible lagerbeholdning og værdien af lageret summen af individuelle afgange, der ikke er blevet fuldt udlignet.

## <a name="weighted-average-date-when-marking-is-used"></a>Dato for vægtet gennemsnit, når afmærkning bruges
Afmærkning er en proces, som giver dig mulighed for at tilknytte en afgangspostering til en tilgangspostering. Afmærkning kan ske enten før eller efter, at en postering er bogført. Du kan bruge afmærkning, når du vil være sikker på den nøjagtige kostpris for lageret, når posteringen bogføres, eller når lagerlukningen udføres. 

Antag f.eks., at firmaets kundeserviceafdeling har modtaget en hasteordre fra en vigtig kunde. Da dette er en hasteordre, vil du skulle betale mere for denne vare for at kunne imødekomme debitorens forespørgsel. Du skal være sikker på, at kostprisen på denne lagervare er afspejlet i avancen eller i vareforbruget for denne salgsordrefaktura. Når indkøbsordren bogføres, modtages lagervarerne til et kostpris på kr. 120,00. Dette salgsordredokument afmærkes f.eks. til indkøbsordren, før følgesedlen eller fakturaen bogføres. Vareforbruget vil derefter være kr. 120,00 i stedet for den aktuelle løbende gennemsnitskostpris for varen. Hvis følgesedlen eller fakturaen for salgsordren bogføres, før afmærkningen finder sted, bogføres vareforbruget til den løbende gennemsnitskostpris. Før lagerlukningen udføres, kan disse to posteringer afmærkes til hinanden. Når en tilgangspostering er markeret til en afgangspostering, vil den værdiansættelsesmetode, der er defineret i varens varemodelgruppe, blive tilsidesat. I stedet for udligner systemet disse posteringer mod hinanden. 

Du kan afmærke en afgangspostering til en tilgang, før posteringen bogføres. Du kan gøre dette fra en salgsordrelinje på siden **Oplysninger om salgsordre**. Du kan få vist de åbne tilgangsposteringer på siden **Afmærkning**. Du kan afmærke en afgangspostering til en tilgang, efter posteringen bogføres. Du kan matche eller afmærke en afgangspostering for en åben tilgangspostering for en lagerført vare fra en bogført lagerreguleringskladde. Følgende illustration viser disse posteringer:

-   1a. Fysisk lagertilgang for et antal på 1 til en kostpris af kr. 10,00 pr. styk
-   1b. Økonomisk lagertilgang for et antal på 1 til en kostpris af kr. 10,00 pr. styk
-   2a. Fysisk lagertilgang for et antal på 1 til en kostpris af kr. 20,00 pr. styk
-   2b. Økonomisk lagertilgang for et antal på 1 til en kostpris af kr. 20,00 pr. styk
-   3a. Fysisk lagertilgang for et antal på 1 til en kostpris af kr. 25,00 pr. styk
-   4a. Fysisk lagertilgang for et antal på 1 til en kostpris af kr. 30,00 pr. styk
-   4b. Økonomisk lagertilgang for et antal på 1 til en kostpris af kr. 30,00 pr. styk
-   5a. Fysisk lagerafgang for et antal på 1 til en kostpris af kr. 21,25 pr. stk. (det løbende gennemsnit af økonomisk og fysisk opdaterede posteringer).
-   5b. Økonomisk lagerafgang for et antal på 1 afmærkes til lagertilgangen 2b, inden posteringen bogføres. Transaktionen bogføres til en kostpris af kr. 20,00 pr. styk
-   6a. Fysisk lagerafgang for et antal på 1 til en kostpris af kr. 21,25.
-   7. Lagerlukningen udføres. Da den økonomisk opdaterede postering er afmærket til en eksisterende tilgang, udlignes disse posteringer mod hinanden, og der udføres ingen justeringer.

Den nye løbende gennemsnitskostpris afspejler gennemsnittet af de økonomisk og fysisk opdaterede posteringer på kr. 27,50. I følgende illustration vises denne serie af posteringer, og virkningerne af at vælge lagermodellen for vægtet gennemsnitsdato og afmærkning.

![Gennemsnitskostdato med afmærkning](./media/weightedaveragedatewithmarking.gif) 

**Nøgle til illustrationen:**

-   Lagertransaktioner vises som lodrette pile.
-   Lagertilgange vises som lodrette pile over tidslinjen.
-   Lagerafgange vises som lodrette pile under tidslinjen.
-   Over eller under hver enkelt lodret pil angives værdien af lagertransaktionen i formatet *Antal*@*stykpris*.
-   Hvis en lagerposteringsværdi er omgivet af parenteser, bogføres lagerposteringen fysisk på lageret.
-   Hvis en lagerposteringsværdi ikke er omgivet af parenteser, bogføres lagerposteringen økonomisk på lageret.
-   Hver enkelt ny tilgangs- eller afgangspostering er markeret med en ny etiket.
-   Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Id'erne angiver rækkefølgen af lagertransaktionsbogføringer på tidslinjen.
-   Lagerlukninger angives med en rød, lodret stiplet linje og etiketten *Lagerlukning*.
-   Udligninger, der foretages ved lagerlukningen, angives med stiplede røde pile, der går diagonalt fra en tilgang til en afgang.




