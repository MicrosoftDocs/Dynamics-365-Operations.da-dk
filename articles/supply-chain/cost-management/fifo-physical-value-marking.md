---
title: FIFO med fysisk værdi og afmærkning
description: FIFO (First in, First out) er en lagermodel, hvor de først anskaffede tilgange afgår først. Økonomisk opdaterede afgange fra lageret udlignes mod de første økonomisk opdaterede tilgange til lageret på baggrund af den økonomiske dato for lagertransaktionen.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5280498a23df26873dda1f380f686796f5e1055f
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092134"
---
# <a name="fifo-with-physical-value-and-marking"></a>FIFO med fysisk værdi og afmærkning

[!include [banner](../includes/banner.md)]


FIFO (First in, First out) er en metode til lagerstyring og værdiansættelse, hvor lager, der fremstilles eller anskaffes først, sælges, bruges eller kasseres først. Under lagerlukningen i Microsoft Dynamics 365 Supply Chain Management opretter systemet udligninger, hvor den første tilgang sammenholdes med den første afgang osv.

Udlignings- og sammenholdelsesprincippet er baseret på den økonomiske dato for lagerposteringerne. Der kan udføres en foreløbig vurdering af udligninger og reguleringer ved at køre lagergenberegningsprocessen.

Du kan tilsidesætte FIFO-princippet ved at markere lagerposteringer, så en specifik varetilgang udlignes mod en specifik afgang. Der kræves en periodisk lagerlukning, når du bruger FIFO-lagermodellen til at oprette udligninger og regulere værdien af afgange i henhold til FIFO-princippet. Indtil du kører lagerlukningsprocessen, værdisættes afgangsposteringerne med det løbende gennemsnit, når de fysiske og økonomiske opdateringer finder sted. Medmindre du bruger afmærkning, beregnes det løbende gennemsnit, når den fysiske eller økonomiske opdatering udføres. I følgende eksempler vises virkningen ved at bruge FIFO i tre forskellige konfigurationer:

- FIFO uden indstillingen **Medtag fysisk værdi**
- FIFO med indstillingen **Medtag fysisk værdi**
- FIFO med afmærkning

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO uden indstillingen Medtag fysisk værdi

I dette eksempel er markeringen i afkrydsningsfeltet **Medtag fysisk værdi** fjernet i varemodelgruppen for det frigivne produkt. I følgende illustration vises disse posteringer:

- 1a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
- 1b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
- 2a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
- 2b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 22,00 pr. stk.
- 3a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 16,00 (løbende gennemsnit af økonomisk bogførte posteringer).
- 3b. Økonomisk lagerafgang for et antal på 1 til en kostpris af USD 16,00 (løbende gennemsnit af økonomisk bogførte posteringer).
- 4a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 25,00 pr. stk.
- 5a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
- 5b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
- 6a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 23,00 (løbende gennemsnit af økonomisk bogførte posteringer)
- 7\. Lagerlukningen udføres. På baggrund af FIFO-metoden udlignes den første økonomisk opdaterede afgang mod den første økonomisk opdaterede tilgang osv. I dette eksempel oprettes der én udligning mellem 1b og 3b. Der foretages en regulering på USD –6,00 til 3b, og den endelige omkostning bliver USD 10,00.

Den nye løbende gennemsnitskostpris afspejler gennemsnittet af de økonomisk opdaterede posteringer. Følgende illustrationer viser effekten af FIFO-lagermodellen på denne række posteringer, når indstillingen **Medtag fysisk værdi** ikke bruges.

![FIFO uden indstillingen Medtag fysisk værdi.](./media/fifo-without-include-physical-value.png)

**Forklaring til diagram**

- Lagertransaktioner vises som lodrette pile.
- Fysiske posteringer vises med kortere, lysegrå pile.
- Økonomiske posteringer vises med længere sorte pile.
- Lagertilgange vises som lodrette pile over tidslinjen.
- Lagerafgange vises som lodrette pile under tidslinjen.
- Hver enkelt ny tilgangs- eller afgangspostering er markeret med en ny etiket.
- Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Identifikatorerne angiver rækkefølgen af lagerposteringsbogføringer på tidslinjen.
- Hver dato i diagrammet er adskilt af en tynd sort lodret linje. Datoen angives nederst i diagrammet.
- Lagerlukninger angives med en rød lodret stiplet linje.
- Udligninger, der foretages ved lagerlukning, angives med stiplede, røde pile, der går diagonalt fra en tilgang til en afgang.

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO med indstillingen Medtag fysisk værdi

Hvis afkrydsningsfeltet **Medtag fysisk værdi** er markeret for en vare på siden **Varemodelgruppe**, bruger systemet både fysiske og økonomiske tilgangsposteringer til beregning af den løbende gennemsnitskostpris. Hvis det er relevant, regulerer systemet også den fysisk opdaterede afgangstransaktion. Lagerlukning med FIFO-lagermodellen foretager kun udligninger af posteringer, der er økonomisk opdateret. I følgende illustration vises disse posteringer:

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
- 7\. Lagerlukningen udføres. På baggrund af FIFO-metoden udlignes den første økonomisk opdaterede afgang mod den første økonomisk opdaterede tilgang osv. I dette eksempel oprettes der én udligning mellem 1b og 3b. Der foretages en regulering på USD –6,00 til 3b, og den endelige omkostning bliver USD 10,00. Desuden bliver posteringen i 6a reguleret i forhold til tilgangsposteringens omkostning for 2b. Systemet udligner ikke disse posteringer, da tilgangen kun opdateres fysisk, men ikke økonomisk. Der bogføres i stedet kun en regulering på USD -1,67 i den fysiske afgangspostering, og den regulerede omkostning bliver USD 22,00.

![FIFO med indstillingen Medtag fysisk værdi.](./media/fifo-with-include-physical-value.png)

Bemærk, at resultatet af at køre lagerlukningsprocessen er det samme, uanset om du vælger indstillingen **Medtag fysisk værdi** på siden **Varemodelgruppe**. Indstillingen **Medtag fysisk værdi** påvirker kun det løbende gennemsnit.

**Forklaring til diagram**

- Lagertransaktioner vises som lodrette pile.
- Fysiske posteringer vises med kortere, lysegrå pile.
- Økonomiske posteringer vises med længere sorte pile.
- Lagertilgange vises som lodrette pile over tidslinjen.
- Lagerafgange vises som lodrette pile under tidslinjen.
- Hver enkelt ny tilgangs- eller afgangspostering er markeret med en ny etiket.
- Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Identifikatorerne angiver rækkefølgen af lagerposteringsbogføringer på tidslinjen.
- Hver dato i diagrammet er adskilt af en tynd sort lodret linje. Datoen angives nederst i diagrammet.
- Lagerlukninger angives med en rød lodret stiplet linje.
- Udligninger, der foretages ved lagerlukning, angives med stiplede, røde pile, der går diagonalt fra en tilgang til en afgang.

## <a name="fifo-with-marking"></a>FIFO med afmærkning

Afmærkning er en proces, som giver dig mulighed for at tilknytte – eller afmærke – en afgangspostering til en tilgangspostering. Afmærkning kan ske enten før eller efter, at en postering er bogført. Du kan bruge afmærkning, når du vil være sikker på den nøjagtige kostpris for lageret, når posteringen bogføres eller når lagerlukningen udføres.

Antag f.eks., at kundeserviceafdelingen har modtaget en hasteordre fra en vigtig kunde. Da denne ordre er en hasteordre, skal du betale mere for denne vare for at kunne imødekomme kundens efterspørgsel. Du skal være sikker på, at kostprisen på denne lagervare afspejles i dækningsbidraget eller i vareforbruget for salgsordrefakturaen. Når indkøbsordren bogføres, modtages lagervarerne til et kostpris på kr. 120,00. Hvis salgsordredokumentet afmærkes til indkøbsordren, før følgesedlen eller fakturaen bogføres, vil vareforbruget være USD 120,00 og ikke den aktuelle løbende gennemsnitskostpris for varen. Hvis følgesedlen eller fakturaen for salgsordren bogføres, før afmærkningen finder sted, bogføres vareforbruget til den løbende gennemsnitskostpris. Før lagerlukningen udføres, kan disse to posteringer afmærkes til hinanden.

Når en tilgangstransaktion er afmærket til en afgangstransaktion, vil den værdiansættelsesmetode, der er defineret i varens modelgruppe, blive tilsidesat, og systemet udligner disse transaktioner mod hinanden. Du kan markere en postering i forhold til en salgsordrelinje manuelt på siden **Oplysninger om salgsordrer** ved at vælge **Lager \> Markering** i oversigtspanelet **Salgsordrelinjer**. Du kan få vist de åbne tilgangsposteringer på siden **Afmærkning**. Du kan matche eller afmærke en afgangspostering for en åben tilgangspostering for en lagerført vare fra en bogført lagerreguleringskladde. I følgende illustration vises disse posteringer:

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
- 6a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 23,00 (løbende gennemsnit af økonomisk bogførte posteringer)
- 7\. Lagerlukningen udføres. På baggrund af afmærkningsprincippet, der bruger FIFO-metoden, udlignes de markerede posteringer mod hinanden. I dette eksempel udlignes 3b mod 2b, og der bogføres en regulering på USD 6,00 for 3b for at få værdien til at blive USD 22,00. I dette eksempel foretages der ingen yderligere udligninger, da lukningen kun opretter udligninger for økonomisk opdaterede posteringer.

I følgende illustration vises effekterne af FIFO-lagermodellen på denne række af posteringer, når afmærkning mellem afgange og tilgange anvendes.

![FIFO med afmærkning.](./media/fifo-with-marking.png)

**Forklaring til diagram**

- Lagertransaktioner vises som lodrette pile.
- Fysiske posteringer vises med kortere, lysegrå pile.
- Økonomiske posteringer vises med længere sorte pile.
- Lagertilgange vises som lodrette pile over tidslinjen.
- Lagerafgange vises som lodrette pile under tidslinjen.
- Hver enkelt ny tilgangs- eller afgangspostering er markeret med en ny etiket.
- Hver enkelt lodret pil er markeret med et sekvens-id, f.eks. *1a*. Identifikatorerne angiver rækkefølgen af lagerposteringsbogføringer på tidslinjen.
- Hver dato i diagrammet er adskilt af en tynd sort lodret linje. Datoen angives nederst i diagrammet.
- Lagerlukninger angives med en rød lodret stiplet linje.
- Udligninger og afmærkninger, der foretages ved lagerlukning, angives med stiplede, røde pile, der går diagonalt fra en tilgang til en afgang.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
