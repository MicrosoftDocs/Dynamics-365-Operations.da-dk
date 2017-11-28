---
title: "Vægtet gennemsnit med fysisk værdi og afmærkning"
description: "Vægtet gennemsnit er en lagermodel, der er baseret på princippet for vægtet gennemsnit, hvor afgange fra lager værdisættes til gennemsnitsværdien for varer, der er modtaget på lager i lagerlukningsperioden, samt en eventuel disponibel lagerbeholdning fra forrige periode."
author: AndersGirke
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 65501
ms.assetid: 25041ff0-bafe-484d-a94a-e1772ad43204
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 69876a9d1daec4e6980728527c784a5404239cc2
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="weighted-average-with-physical-value-and-marking"></a>Vægtet gennemsnit med fysisk værdi og afmærkning

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

Vægtet gennemsnit er en lagermodel, der er baseret på princippet for vægtet gennemsnit, hvor afgange fra lager værdisættes til gennemsnitsværdien for varer, der er modtaget på lager i lagerlukningsperioden, samt en eventuel disponibel lagerbeholdning fra forrige periode.

Når du kører en lagerlukning, udlignes alle tilgange mod en virtuel afgang, der indeholder den samlede modtagne mængde og værdi. Denne virtuelle afgang har en tilsvarende virtuel tilgang, som tilgangene vil blive udlignet fra. På denne måde opnår alle afgange samme gennemsnitskostpris. Den virtuelle afgang og tilgang kan ses som en virtuel overførsel, som kaldes "lagerlukningsoverførsel efter vægtet gennemsnit".

Hvis der kun er én tilgang, kan alle afgange udlignes fra den, og der oprettes ikke en virtuel overførsel. 

Når du bruger vægtet gennemsnit, kan du vælge at markere lagertransaktioner, så en specifik varetilgang udlignes mod en specifik afgang, i stedet for at bruge reglen om vægtet gennemsnit. 

Det anbefales at bruge månedlig lagerlukning, når du bruger lagermodellen for vægtet gennemsnit. 

Det vægtede gennemsnit for lagerlukningsmetoden beregnes efter følgende formel:
-   Vægtet gennemsnit = (Q1\*P1 + Q2\*P2 + Qn\*Pn) / (Q1 + Q2 + Qn)

Lagerposteringer ud af lageret. Dette omfatter salgsordrer, lagerkladder, indkøbskreditnotaer og produktionsordrer. Udføres til en forkalkuleret kostpris på bogføringsdatoen. Den estimerede kostpris kaldes også det løbende gennemsnit. På tidspunktet for lagerlukning analyserer systemet lagertransaktionerne for at se, om der tidligere og aktuelle perioder, og for at bestemme, hvilken af følgende lukningsprincipper der skal bruges.
-   Direkte udligning
-   Opsummeret udligning

Udligninger er lagerlukningsbogføringer, der bruges til at justere afgangene til det korrekte vægtede gennemsnit fra og med lukningsdatoen. I følgende eksempler illustreres virkningen af at bruge vægtet gennemsnit i fem forskellige konfigurationer:
-   Direkte udligning for vægtet gennemsnit uden indstillingen Medtag fysisk værdi
-   Opsummeret udligning for vægtet gennemsnit uden indstillingen Medtag fysisk værdi
-   Direkte udligning for vægtet gennemsnit med indstillingen Medtag fysisk værdi
-   Opsummeret udligning for vægtet gennemsnit med indstillingen Medtag fysisk værdi
-   Vægtet gennemsnit med afmærkning

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Direkte udligning for vægtet gennemsnit uden indstillingen Medtag fysisk værdi
Princippet for direkte udligning er det samme, der bruges til vægtet gennemsnit i tidligere versioner. Systemet udligner direkte mellem tilgange og afgange. Systemet bruger dette udligningsprincip i bestemte situationer:
-   Der er blevet bogført én tilgang og en eller flere afgange i perioden
-   I perioden er der kun blevet bogført afgange, og der er disponible varer på lager fra en tidligere lukning

I eksemplerne i følgende afsnit er der bogført en økonomisk opdateret tilgang og afgang. Ved lagerlukningen udligner systemet tilgangen direkte mod afgangen, og det er ikke nødvendigt af justere kostprisen ved afgangen. Følgende posteringer illustreres i nedenstående grafik.
-   1a. Fysisk lagertilgang opdateret for et antal på 5 til en kostpris a kr. 10,00 pr. stk.
-   1b. Økonomisk lagertilgang opdateret for et antal på 5 til en kostpris a kr. 10,00 pr. stk.
-   2a. Fysisk lagertilgang opdateret for et antal på 2 til en kostpris a kr. 10,00 pr. stk.
-   2b. Økonomisk lagertilgang opdateret for et antal på 2 til en kostpris a kr. 10,00 pr. stk.
-   3. Lagerlukningen er udført ved brug af den direkte udligningsmetode for at udligne den økonomiske lagertilgang med den økonomiske lagerafgang.

I følgende diagram illustreres denne række posteringer med effekterne ved at vælge lagermodellen for vægtet gennemsnit og princippet for direkte udligning uden indstillingen Medtag fysisk værdi. 

![Direkte udligning for vægtet gennemsnit uden indstillingen Medtag fysisk værdi](./media/weightedaveragedirectsettlementwithoutincludephysicalvalue.gif) 

**Forklaring til diagram**
-   Lagertransaktioner vises som lodrette pile.
-   Lagertilgange vises som lodrette pile over tidslinjen.
-   Lagerafgange vises som lodrette pile under tidslinjen.
-   Over eller under hver enkelt lodret pil angives værdien af lagertransaktionen i formatet Quantity@Unitprice.
-   En lagertransaktionsværdi, der er omgivet af kantede parenteser, angiver, at lagertransaktionen bogføres fysisk på lageret.
-   En lagertransaktionsværdi, der ikke er omgivet af kantede parenteser, angiver, at lagertransaktionen bogføres økonomisk på lageret.
-   Hver enkelt ny tilgangs- eller afgangstransaktion er markeret med en ny etiket.
-   Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Id'erne angiver rækkefølgen af lagertransaktionsbogføringer på tidslinjen.
-   Lagerlukninger angives med en rød stiplet linje og etiketten Lagerlukning.
-   Udligninger, der foretages ved lagerlukningen, angives med stiplede røde pile, der går diagonalt fra en tilgang til en afgang.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Opsummeret udligning for vægtet gennemsnit uden indstillingen Medtag fysisk værdi
Vægtet gennemsnit bruger det udligningsprincip, at alle tilgange i en lukningsperiode opsummeres i en ny postering, der kaldes Lagerlukning for vægtet gennemsnit. Alle periodens tilgange udlignes mod afgangen i den nyoprettede lageroverførselspost. Alle periodens afgange udlignes mod tilgangen i den nye lageroverførselspost. Hvis den disponible lagerbeholdning er positiv efter lagerlukningen, opsummeres denne disponible lagerbeholdning og værdien af lageret i den nye lageroverførselspost (tilgang). Hvis den disponible lagerbeholdning er negativ efter lagerlukningen, udgør den disponible lagerbeholdning og værdien af lageret summen af individuelle afgange, der ikke er blevet fuldt udlignet. I eksemplet nedenfor er der bogført flere økonomisk opdaterede tilgange og én afgang. 

Under lagerlukningen genererer og bogfører systemet den summerede lageroverførselspostering og udligner tilgangene i perioden mod den opsummerede afgang i lageroverførselsposten. Alle afgange, der er bogført i perioden, udlignes mod den summerede tilgang i lageroverførselsposten. Det vægtede gennemsnit beregnes til at være kr. 15,00. Afgangen blev oprindeligt bogført med en forkalkuleret kostpris på kr. 14,67. Derfor oprettes der en negativ regulering på kr. 0,33, som bogføres på afgangen. På datoen for lagerlukningen er den disponible lagerbeholdning 3 stk. med en værdi på kr. 45,00. 

De efterfølgende posteringer illustreres i nedenstående grafik:
-   1a. Fysisk lagertilgang opdateret for et antal på 2 til en kostpris a kr. 11,00 pr. stk.
-   1b. Økonomisk lagertilgang opdateret for et antal på 2 til en kostpris a kr. 14,00 pr. stk.
-   2a. Fysisk lagertilgang opdateret for et antal på 1 til en kostpris a kr. 12,00 pr. stk.
-   2b. Økonomisk lagertilgang opdateret for et antal på 1 til en kostpris a kr. 16,00 pr. stk.
-   3a. Fysisk lagerafgang opdateret for et antal på 1 til en kostpris a kr. 14,67 pr. stk. (løbende gennemsnit).
-   3b. Økonomisk lagerafgang opdateret for et antal på 1 til en kostpris a kr. 14,67 pr. stk. (løbende gennemsnit).
-   4a. Fysisk lagertilgang opdateret for et antal på 1 til en kostpris a kr. 14,00 pr. stk.
-   4b. Økonomisk lagertilgang opdateret for et antal på 1 til en kostpris a kr. 16,00 pr. stk.
-   5. Lagerlukningen udføres.
-   6a. Der oprettes en økonomisk afgang af typen lagerlukningstransaktion for vægtet gennemsnit for at opsummere udligningerne for alle økonomiske lagertilgange.
-   6b. Der oprettes en økonomisk tilgang af typen for lagerlukningstransaktion for vægtet gennemsnit for modpostering for 5a.

I følgende diagram illustreres denne række posteringer med effekterne ved at vælge lagermodellen for vægtet gennemsnit og princippet for opsummerede udligning uden indstillingen Medtag fysisk værdi. 

![Opsummeret udligning for vægtet gennemsnit uden indstillingen Medtag fysisk værdi](./media/weightedaveragesummarizedsettlementwithoutincludephysicalvalue.gif) 

**Forklaring til diagram**
-   Lagertransaktioner vises som lodrette pile.
-   Lagertilgange vises som lodrette pile over tidslinjen.
-   Lagerafgange vises som lodrette pile under tidslinjen.
-   Over eller under hver enkelt lodret pil angives værdien af lagertransaktionen i formatet Quantity@Unitprice.
-   En lagertransaktionsværdi, der er omgivet af kantede parenteser, angiver, at lagertransaktionen bogføres fysisk på lageret.
-   En lagertransaktionsværdi, der ikke er omgivet af kantede parenteser, angiver, at lagertransaktionen bogføres økonomisk på lageret.
-   Hver enkelt ny tilgangs- eller afgangstransaktion er markeret med en ny etiket.
-   Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Id'erne angiver rækkefølgen af lagertransaktionsbogføringer på tidslinjen.
-   Lagerlukninger angives med en rød stiplet linje og etiketten Lagerlukning.
-   Udligninger, der foretages ved lagerlukningen, angives med stiplede røde pile, der går diagonalt fra en tilgang til en afgang.
-   Røde pile illustrerer den tilgangspostering, som udlignes mod den afgangspostering, der oprettes af systemet.
-   Den grønne pil illustrerer den systemgenererede tilgangsmodpostering, som den oprindeligt bogførte afgangspostering udlignes mod.

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Direkte udligning for vægtet gennemsnit med indstillingen Medtag fysisk værdi
Parameteren Medtag fysisk værdi fungerer anderledes for lagermodellen for vægtet gennemsnit end i tidligere versioner af produktet. Markér feltet Medtag fysisk værdi for en vare i formen Varemodelgruppe. Derefter bruger systemet fysisk opdaterede tilgange ved beregning af den forkalkulerede kostpris eller det løbende gennemsnit. Afgangene posteres på basis af denne forkalkulerede kostpris i løbet af perioden. Under lagerlukningen tages kun økonomisk opdaterede tilgange i betragtning ved beregning af det vægtede gennemsnit. Det anbefales at bruge en månedlig lagerlukning, når du bruger lagermodellen for vægtet gennemsnit. I dette eksempel med direkte udligning for vægtet gennemsnit er varemodelgruppen markeret, så den medtager den fysiske værdi. 

De efterfølgende posteringer illustreres i nedenstående grafik:
-   1a. Fysisk lagertilgang opdateret for et antal på 1 til en kostpris a kr. 11,00 pr. stk.
-   1b. Økonomisk lagertilgang opdateret for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
-   2a. Fysisk lagertilgang opdateret for et antal på 1 til en kostpris a kr. 15,00 pr. stk.
-   3a. Fysisk lagerafgang opdateret for et antal på 1 til en kostpris a kr. 12,50 pr. stk. (løbende gennemsnitskostpris, da den fysiske tilgangsværdi også skal overvejes).
-   3b. Økonomisk lagerafgang opdateret for et antal på 1 til en kostpris a kr. 12,50 pr. stk. (løbende gennemsnitskostpris, da den fysiske tilgangsværdi også skal overvejes).
-   4. Lagerlukningen udføres. I forbindelse med lagerlukningen ser systemet bort fra alle lagerposteringer, der kun er opdateret i fysisk forstand. I stedet anvendes princippet om direkte udligning, fordi der kun findes én økonomisk tilgang. En regulering på kr. 2,50 bogføres pr. lagerlukningsdatoen på den lagerpost, der er afgået i økonomisk forstand. Efter lagerlukningen vil den disponible lagerbeholdning være 1 med en løbende gennemsnitskostpris på kr. 15,00.

I følgende diagram illustreres denne række posteringer med effekterne ved at vælge lagermodellen for vægtet gennemsnit og princippet for direkte udligning med indstillingen Medtag fysisk værdi. 

![Direkte udligning for vægtet gennemsnit med indstillingen Medtag fysisk værdi](./media/weightedaveragedirectsettlementwithincludephysicalvalue.gif) 

**Forklaring til diagram**
-   Lagertransaktioner vises som lodrette pile.
-   Lagertilgange vises som lodrette pile over tidslinjen.
-   Lagerafgange vises som lodrette pile under tidslinjen.
-   Over eller under hver enkelt lodret pil angives værdien af lagertransaktionen i formatet Quantity@Unitprice.
-   En lagertransaktionsværdi, der er omgivet af kantede parenteser, angiver, at lagertransaktionen bogføres fysisk på lageret.
-   En lagertransaktionsværdi, der ikke er omgivet af kantede parenteser, angiver, at lagertransaktionen bogføres økonomisk på lageret.
-   Hver enkelt ny tilgangs- eller afgangstransaktion er markeret med en ny etiket.
-   Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Id'erne angiver rækkefølgen af lagertransaktionsbogføringer på tidslinjen.
-   Lagerlukninger angives med en rød stiplet linje og etiketten Lagerlukning.
-   Udligninger, der foretages ved lagerlukningen, angives med stiplede røde pile, der går diagonalt fra en tilgang til en afgang.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Opsummeret udligning for vægtet gennemsnit med indstillingen Medtag fysisk værdi
Parameteren Medtag fysisk værdi fungerer anderledes for vægtet gennemsnit end i tidligere versioner. Markér feltet Medtag fysisk værdi for en vare på siden Varemodelgruppe. Derefter bruger systemet fysisk opdaterede tilgange ved beregning af den forkalkulerede kostpris eller det løbende gennemsnit. Afgangene posteres på basis af denne forkalkulerede kostpris i løbet af perioden. Under lagerlukningen tages kun økonomisk opdaterede tilgange i betragtning i beregningen af det vægtede gennemsnit. Det anbefales at bruge en månedlig lagerlukning, når du bruger lagermodellen for vægtet gennemsnit. I dette eksempel med opsummeret udligning for vægtet gennemsnit er lagermodellen markeret, så den medtager den fysiske værdi. 

De efterfølgende posteringer illustreres i nedenstående grafik:
-   1a. Fysisk lagertilgang opdateret for et antal på 2 til en kostpris a kr. 11,00 pr. stk.
-   1b. Økonomisk lagertilgang opdateret for et antal på 2 til en kostpris a kr. 14,00 pr. stk.
-   2. Fysisk lagertilgang opdateret for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
-   3a. Fysisk lagertilgang opdateret for et antal på 1 til en kostpris a kr. 12,00 pr. stk.
-   3b. Økonomisk lagertilgang opdateret for et antal på 1 til en kostpris a kr. 16,00 pr. stk.
-   4a. Fysisk lagerafgang opdateret for et antal på 1 til en kostpris a kr. 13,50 pr. stk. (løbende gennemsnitskostpris, da den fysiske tilgangsværdi også skal overvejes).
-   4b. Økonomisk lagerafgang opdateret for et antal på 1 til en kostpris a kr. 13,50 pr. stk. (løbende gennemsnitskostpris, da den fysiske tilgangsværdi også skal overvejes).
-   5a. Fysisk lagertilgang opdateret for et antal på 1 til en kostpris a kr. 14,00 pr. stk.
-   5b. Økonomisk lagertilgang opdateret for et antal på 1 til en kostpris a kr. 16,00 pr. stk.
-   6. Lagerlukningen udføres. I forbindelse med lagerlukningen ser systemet bort fra alle lagerposteringer, der kun er opdateret i fysisk forstand. I stedet anvendes princippet om opsummeret udligning, fordi der kun findes én økonomisk tilgang. En regulering på kr. 1,50 bogføres pr. lagerlukningsdatoen på den lagerpost, der er afgået i økonomisk forstand. Efter lagerlukningen vil den disponible lagerbeholdning være 3 med en løbende gennemsnitskostpris på kr. 15,00.
-   7a. Der oprettes en økonomisk afgang af typen lagerlukningstransaktion for vægtet gennemsnit for at opsummere udligningerne for alle økonomiske lagertilgange.
-   7b. Der oprettes en økonomisk tilgang af typen for lagerlukningstransaktion for vægtet gennemsnit for modpostering for 5a.

I følgende diagram illustreres denne række posteringer med effekterne ved at vælge lagermodellen for vægtet gennemsnit og princippet for opsummerede udligning uden indstillingen Medtag fysisk værdi. 

![Opsummeret udligning for vægtet gennemsnit med indstillingen Medtag fysisk værdi](./media/weightedaveragesummarizedsettlementwithincludephysicalvalue.gif) 

**Forklaring til diagram**
-   Lagertransaktioner vises som lodrette pile.
-   Lagertilgange vises som lodrette pile over tidslinjen.
-   Lagerafgange vises som lodrette pile under tidslinjen.
-   Over eller under hver enkelt lodret pil angives værdien af lagertransaktionen i formatet Quantity@Unitprice.
-   En lagertransaktionsværdi, der er omgivet af kantede parenteser, angiver, at lagertransaktionen bogføres fysisk på lageret.
-   En lagertransaktionsværdi, der ikke er omgivet af kantede parenteser, angiver, at lagertransaktionen bogføres økonomisk på lageret.
-   Hver enkelt ny tilgangs- eller afgangstransaktion er markeret med en ny etiket.
-   Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. 1a. Id'erne angiver rækkefølgen af lagertransaktionsbogføringer på tidslinjen.
-   Lagerlukninger angives med en rød stiplet linje og etiketten Lagerlukning.
-   Udligninger, der foretages ved lagerlukningen, angives med stiplede røde pile, der går diagonalt fra en tilgang til en afgang.
-   Røde pile illustrerer den tilgangspostering, som udlignes mod den afgangspostering, der oprettes af systemet.
-   Den grønne pil illustrerer den systemgenererede tilgangsmodpostering, som den oprindeligt bogførte afgangspostering udlignes mod

## <a name="weighted-average-with-marking"></a>Vægtet gennemsnit med afmærkning
Afmærkning er en proces, som giver dig mulighed for at tilknytte – eller afmærke – en afgangspostering til en tilgangspostering. Afmærkning kan ske enten før eller efter, at en postering er bogført. Du kan bruge afmærkning, når du vil være sikker på den nøjagtige kostpris for lageret, når posteringen bogføres, eller når lagerlukningen udføres. 

Antag f.eks., at firmaets kundeserviceafdeling har modtaget en hasteordre fra en vigtig kunde. Da dette er en hasteordre, vil du skulle betale mere for denne vare for at kunne imødekomme kundens forespørgsel. Du skal være sikker på, at kostprisen på denne lagervare afspejles i dækningsbidraget eller i vareforbruget for denne salgsordrefaktura. 

Når indkøbsordren bogføres, modtages lagervarerne til et kostpris på kr. 120,00. Dette salgsordredokument afmærkes f.eks. til indkøbsordren, før følgesedlen eller fakturaen bogføres. Vareforbruget vil være kr. 120,00 i stedet for den aktuelle løbende gennemsnitskostpris for varen. Hvis følgesedlen eller fakturaen for salgsordren bogføres, før afmærkningen finder sted, bogføres vareforbruget til den løbende gennemsnitskostpris. 

Før lagerlukningen udføres, kan disse to posteringer afmærkes til hinanden. 

En tilgangspostering afmærkes til en afgangspostering. Derefter ses der bort fra den vurderingsmetode, der er valgt for varens varemodelgruppe, og i systemet udlignes disse poster i forhold til hinanden. 

Du kan afmærke en afgangspostering til en tilgang, før posteringen bogføres. Du kan gøre dette fra en salgsordrelinje på siden Oplysninger om salgsordre. Du kan få vist de åbne tilgangsposteringer på siden Afmærkning. 

Du kan afmærke en afgangspostering til en tilgang, efter at posteringen er bogført. Du kan matche eller afmærke en afgangspostering for en åben tilgangspostering for en lagerført vare fra en bogført lagerreguleringskladde. 

De efterfølgende posteringer illustreres i nedenstående grafik:
-   1a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
-   1b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
-   2a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
-   2b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
-   3a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 25,00 pr. stk.
-   4a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
-   4b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
-   5a. Fysisk lagerafgang for et antal på 1 til en kostpris a kr. 21,25 pr. stk. (det løbende gennemsnit af økonomisk og fysisk opdaterede posteringer).
-   5b. Økonomisk lagerafgang for et antal på 1 afmærkes til lagertilgangen 2b, inden posteringen bogføres. Denne postering bogføres med en kostpris på kr. 20,00.
-   6a. Fysisk lagerafgang for et antal på 1 til en kostpris a kr. 21,25 pr. stk.
-   7. Lagerlukningen udføres. Da den økonomisk opdaterede postering er afmærket til en eksisterende tilgang, udlignes disse posteringer mod hinanden, og der udføres ingen justeringer.

Den nye løbende gennemsnitskostpris afspejler gennemsnittet af de økonomisk og fysisk opdaterede posteringer på kr. 27,50. 

I følgende diagram illustreres denne serie posteringer med virkningerne af at vælge lagermodellen for vægtet gennemsnit ved afmærkning. 

![Vægtet gennemsnit med afmærkning](./media/weightedaveragewithmarking.gif) 

**Forklaring til diagram**
-   Lagertransaktioner vises som lodrette pile.
-   Lagertilgange vises som lodrette pile over tidslinjen.
-   Lagerafgange vises som lodrette pile under tidslinjen.
-   Over eller under hver enkelt lodret pil angives værdien af lagertransaktionen i formatet Quantity@Unitprice.
-   En lagertransaktionsværdi, der er omgivet af kantede parenteser, angiver, at lagertransaktionen bogføres fysisk på lageret.
-   En lagertransaktionsværdi, der ikke er omgivet af kantede parenteser, angiver, at lagertransaktionen bogføres økonomisk på lageret.
-   Hver enkelt ny tilgangs- eller afgangstransaktion er markeret med en ny etiket.
-   Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Id'erne angiver rækkefølgen af lagertransaktionsbogføringer på tidslinjen.
-   Lagerlukninger angives med en rød stiplet linje og etiketten Lagerlukning.
-   Udligninger, der foretages ved lagerlukningen, angives med stiplede røde pile, der går diagonalt fra en tilgang til en afgang.






