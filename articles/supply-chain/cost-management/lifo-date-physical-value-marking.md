---
title: LIFO-dato med fysisk værdi og mærkning
description: LIFO (Last In, First Out) er en lagermodel, hvor de seneste (nyeste) tilgange udstedes først. Afgange fra lageret udlignes mod de seneste tilgange på lageret baseret på datoen for lagerposteringen. Hvis der ikke er nogen tilgang før afgangen i forbindelse med LIFO-dato, udlignes afgangen mod en hvilken som helst tilgang efter afgangsdatoen. Flere afgange på samme dato kan udlignes i rækkefølgen seneste afgang, seneste modtagelse.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 51592
ms.assetid: d9f13274-3268-444f-85c8-b686fd39286d
ms.search.region: Global
ms.search.industry: Retail
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f11870d6271fa3635b7be9dabb3999e78c0e8b6c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201680"
---
# <a name="lifo-date-with-physical-value-and-marking"></a>LIFO-dato med fysisk værdi og mærkning

[!include [banner](../includes/banner.md)]

LIFO (Last In, First Out) er en lagermodel, hvor de seneste (nyeste) tilgange udstedes først. Afgange fra lageret udlignes mod de seneste tilgange på lageret baseret på datoen for lagerposteringen. Hvis der ikke er nogen tilgang før afgangen i forbindelse med LIFO-dato, udlignes afgangen mod en hvilken som helst tilgang efter afgangsdatoen. Flere afgange på samme dato kan udlignes i rækkefølgen seneste afgang, seneste modtagelse. 

Når du bruger lagermodellen LIFO-dato (Last in, First out), og der ikke er nogen tilgang før afgangen i forbindelse med LIFO-dato, udlignes afgangen mod en hvilken som helst tilgang efter afgangsdatoen. Flere afgange på samme dato kan udlignes i rækkefølgen seneste afgang, seneste modtagelse. Når du bruger LIFO-dato, behøver du ikke at bruge LIFO-datoreglen. I stedet kan du markere lagerposteringer, så en specifik varetilgang udlignes mod en specifik afgang. 

Det anbefales, at du udfører en periodevis lagerlukning, når du bruger LIFO-dato-lagermodellen. 

I følgende eksempler vises virkningen ved at bruge LIFO-dato i tre forskellige konfigurationer:

-   LIFO-dato uden markering af indstillingen **Medtag fysisk værdi**
-   LIFO-dato med markering af indstillingen **Medtag fysisk værdi**
-   LIFO-dato med afmærkning

## <a name="lifo-date-without-the-include-physical-value-option"></a>LIFO-dato uden markering af indstillingen Medtag fysisk værdi
I dette eksempel er det ikke angivet, at varemodelgruppen skal medtage fysisk værdi. I følgende illustration vises disse posteringer:

-   1a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
-   1b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
-   2a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
-   2b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
-   3a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 25,00 pr. stk.
-   4a. Fysisk lagerafgang for et antal på 1 til en kostpris af kr. 15,00 pr. styk (det løbende gennemsnit af økonomisk opdaterede posteringer).
-   4b. Økonomisk lagerafgang for et antal på 1 til en kostpris af kr. 15,00 pr. styk (det løbende gennemsnit af økonomisk opdaterede posteringer).
-   5a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
-   5b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
-   6. Lagerlukningen udføres. På baggrund af LIFO-datometoden udlignes den seneste økonomisk opdaterede afgang med den seneste økonomisk opdaterede tilgang efter dato. Der foretages en regulering på kr. 5,00 på afgangsposteringen. Disse posteringer udligner med hinanden.

Den nye løbende gennemsnitskostpris afspejler gennemsnittet af de økonomisk opdaterede posteringer på kr. 15,00. 

Følgende illustration viser effekten af LIFO-datolagermodellen, når indstillingen **Medtag fysisk værdi** ikke bruges. ![LIFO-dato med Medtag fysisk værdi](./media/lifodatewithoutincludephysicalvalue.gif) 

**Forklaring til diagram**

- Lagertransaktioner vises som lodrette pile.
- Lagertilgange vises som lodrette pile over tidslinjen.
- Lagerafgange vises som lodrette pile under tidslinjen.
- Over (eller under) hver enkelt lodret pil angives værdien af lagertransaktionen i formatet Antal@stykpris.
- En lagerposteringsværdi, der er omgivet af parenteser, angiver, at lagerposteringen bogføres fysisk på lageret.
- En lagerposteringsværdi, der ikke er omgivet af parenteser, angiver, at lagerposteringen bogføres økonomisk på lageret.
- Hver enkelt ny tilgangs- eller afgangspostering er markeret med en ny etiket.
- Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Identifikatorerne angiver rækkefølgen af lagerposteringsbogføringer på tidslinjen.
- Lagerlukninger angives med en rød, lodret stiplet linje og etiketten *Lagerlukning*.
- Udligninger, der foretages ved lagerlukning, angives med stiplede, røde pile, der går diagonalt fra en tilgang til en afgang.

## <a name="lifo-date-with-the-include-physical-value-option"></a>LIFO-dato med markering af indstillingen Medtag fysisk værdi
Du kan markere afkrydsningsfeltet **Medtag fysisk værdi** for en vare på siden **Varemodelgrupper**. I dette tilfælde bruger systemet både de fysisk opdaterede transaktioner og økonomisk opdaterede transaktioner til at beregne den løbende gennemsnitskostpris. Hvis det er relevant, udfører systemet også justeringer i den fysisk opdaterede afgangstransaktion. Når afkrydsningsfeltet **Medtag fysisk værdi** ikke er markeret, vil lagerlukning, der bruger med lagermodellen LIFO-dato, kun gennemføre udligninger af økonomisk opdaterede posteringer. 

I dette eksempel er det angivet, at varemodelgruppen skal medtage fysisk værdi. 

I følgende illustration vises disse posteringer:

-   1a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
-   1b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
-   2a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
-   2b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
-   3a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 25,00 pr. stk.
-   4a. Fysisk lagerafgang for et antal på 1 til en kostpris af kr. 18,33 pr. stk. (løbende gennemsnit af økonomisk opdaterede transaktioner).
-   4b. Økonomisk lagerafgang for et antal på 1 til en kostpris af kr. 18,33 pr. styk (det løbende gennemsnit af økonomisk opdaterede posteringer).
-   5a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
-   5b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
-   6. Lagerlukningen udføres. På baggrund af LIFO-datometoden justeres eller udlignes den seneste opdaterede afgang med den seneste økonomisk opdaterede tilgang efter dato. Disse posteringer udlignes ikke efter hinanden, da den økonomiske tilgangspostering justeres til en postering for en fysisk opdatering. I stedet vil der kun blive udført en justering på kr. 6,67 på afgangsposteringen.

Den nye løbende gennemsnitskostpris afspejler gennemsnittet af de økonomisk opdaterede posteringer på kr. 20,00. 

Følgende illustration viser effekten af LIFO-lagermodellen, når indstillingen **Medtag fysisk værdi** bruges. ![LIFO-dato med Medtag fysisk værdi](./media/lifodatewithincludephysicalvalue.gif) 

**Forklaring til diagram**

- Lagertransaktioner vises som lodrette pile.
- Lagertilgange vises som lodrette pile over tidslinjen.
- Lagerafgange vises som lodrette pile under tidslinjen.
- Over (eller under) hver enkelt lodret pil angives værdien af lagertransaktionen i formatet Antal@stykpris.
- En lagerposteringsværdi, der er omgivet af parenteser, angiver, at lagerposteringen bogføres fysisk på lageret.
- En lagerposteringsværdi, der ikke er omgivet af parenteser, angiver, at lagerposteringen bogføres økonomisk på lageret.
- Hver enkelt ny tilgangs- eller afgangspostering er markeret med en ny etiket.
- Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Identifikatorerne angiver rækkefølgen af lagerposteringsbogføringer på tidslinjen.
- Lagerlukninger angives med en rød, lodret stiplet linje og etiketten *Lagerlukning*.
- Udligninger, der foretages ved lagerlukning, angives med stiplede, røde pile, der går diagonalt fra en tilgang til en afgang.

## <a name="lifo-date-with-marking"></a>LIFO-dato med afmærkning
Afmærkning er en proces, som giver dig mulighed for at tilknytte – eller afmærke – en afgangspostering til en tilgangspostering. Afmærkning kan ske enten før eller efter, at en postering er bogført. Du kan bruge afmærkning, når du vil være sikker på den nøjagtige kostpris for lageret, når posteringen bogføres eller når lagerlukningen udføres. 

Antag f.eks., at kundeserviceafdelingen har modtaget en hasteordre fra en vigtig kunde. Da denne ordre er en hasteordre, skal du betale mere for denne vare for at kunne imødekomme kundens forespørgsel. Du skal være sikker på, at kostprisen på denne lagervare afspejles i dækningsbidraget eller i vareforbruget for denne salgsordrefaktura. 

Når indkøbsordren bogføres, modtages lagervarerne til et kostpris på kr. 120,00. Hvis dette salgsordredokument afmærkes til indkøbsordren, før følgesedlen eller fakturaen bogføres, vil vareforbruget være kr. 120,00 og ikke den aktuelle løbende gennemsnitskostpris for varen. Hvis følgesedlen eller fakturaen for salgsordren bogføres, før afmærkningen finder sted, bogføres vareforbruget til den løbende gennemsnitskostpris. 

Før lagerlukningen udføres, kan disse to transaktioner afmærkes til hinanden. 

En tilgangspostering afmærkes f.eks. til en afgangspostering. I dette tilfælde ses der bort fra den vurderingsmetode, der er valgt for varens varemodelgruppe, og systemet udligner disse poster med hinanden. 

Du kan afmærke en afgangspostering til en tilgang, før posteringen bogføres. Du kan gøre dette fra en salgsordrelinje på siden **Oplysninger om salgsordre**. Du kan få vist de åbne tilgangsposteringer på siden **Afmærkning**. 

Du kan også afmærke en afgangspostering til en tilgang, efter posteringen bogføres. Du kan matche eller afmærke en afgangspostering for en åben tilgangspostering for en lagerført vare fra en bogført lagerreguleringskladde. 

I følgende illustration vises disse posteringer:

-   1a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
-   1b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
-   2a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
-   2b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
-   3a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 25,00 pr. stk.
-   4a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
-   4b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
-   5a. Fysisk lagerafgang for et antal på 1 til en kostpris af kr. 21,25 pr. styk (det løbende gennemsnit af økonomisk og fysisk opdaterede posteringer).
-   5b. Økonomisk lagerafgang for et antal på 1 afmærkes til lagertilgang 2b, inden transaktionen bogføres. Posteringen bogføres til en kostpris af kr. 20,00 pr. styk.
-   6a. Fysisk lagerafgang for et antal på 1 til en kostpris a kr. 21,25 pr. stk.
-   7. Lagerlukningen udføres. Da den økonomisk opdaterede FIFO-transaktion (First in, First out) er afmærket til en eksisterende tilgang, udlignes disse transaktioner mod hinanden, og der udføres ingen justeringer.

Den nye løbende gennemsnitskostpris afspejler gennemsnittet af de økonomisk og fysisk opdaterede posteringer på kr. 27,50. 

I følgende illustration vises virkningerne af at vælge lagermodellen for LIFO, når der bruges afmærkning mellem afgange og tilgange. ![LIFO-dato med afmærkning](./media/lifodatewithmarking.gif) 

**Forklaring til diagram**

- Lagertransaktioner vises som lodrette pile.
- Lagertilgange vises som lodrette pile over tidslinjen.
- Lagerafgange vises som lodrette pile under tidslinjen.
- Over (eller under) hver enkelt lodret pil angives værdien af lagertransaktionen i formatet Antal@stykpris.
- En lagerposteringsværdi, der er omgivet af parenteser, angiver, at lagerposteringen bogføres fysisk på lageret.
- En lagerposteringsværdi, der ikke er omgivet af parenteser, angiver, at lagerposteringen bogføres økonomisk på lageret.
- Hver enkelt ny tilgangs- eller afgangspostering er markeret med en ny etiket.
- Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Identifikatorerne angiver rækkefølgen af lagerposteringsbogføringer på tidslinjen.
- Lagerlukninger angives med en rød, lodret stiplet linje og etiketten *Lagerlukning*.
- Udligninger, der foretages ved lagerlukning, angives med stiplede, røde pile, der går diagonalt fra en tilgang til en afgang.




