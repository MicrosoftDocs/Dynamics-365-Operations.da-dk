---
title: LIFO-dato med fysisk værdi og mærkning
description: LIFO-dato (Last In, First Out) er en lagermodel der er baseret på LIFO-princippet. Afgange fra lageret udlignes mod de seneste tilgange på lageret baseret på datoen for lagertransaktioner. Hvis der ikke er nogen tilgang før afgangen i forbindelse med LIFO-dato, udlignes afgangen mod en hvilken som helst tilgang efter afgangsdatoen. Flere afgange på samme dato kan udlignes i rækkefølgen seneste afgang, seneste modtagelse.
author: JennySong-SH
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 51592
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ca344e6ca81814e787046f6ece97625d035346d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671444"
---
# <a name="lifo-date-with-physical-value-and-marking"></a>LIFO-dato med fysisk værdi og mærkning

[!include [banner](../includes/banner.md)]

LIFO-dato (Last in, First out) er en metode til lagerstyring og værdiansættelse, hvor lager, der fremstilles eller anskaffes sidst, sælges, bruges eller kasseres først. Under lagerlukningen i Microsoft Dynamics 365 Supply Chain Management opretter systemet udligninger, hvor den sidste tilgang sammenholdes med den første afgang for hver given dato med den ældste dato først osv. Når du bruger lagermodellen LIFO-dato (Last in, First out), og der ikke er nogen tilgang før afgangen i forbindelse med LIFO-dato, udlignes afgangen mod en hvilken som helst tilgang efter afgangsdatoen. Udlignings- og sammenholdelsesprincippet er baseret på den økonomiske dato for lagerposteringerne. Når der er flere afgange på samme dato, udlignes de i rækkefølgen seneste afgang, seneste modtagelse. Der kan udføres en foreløbig vurdering af udligninger og reguleringer ved at køre lagergenberegningsprocessen.

Du kan tilsidesætte LIFO-datoprincippet ved at markere lagerposteringer, så en specifik varetilgang udlignes mod en specifik afgang. Der kræves en periodisk lagerlukning, når du bruger LIFO-datolagermodellen til at oprette udligninger og regulere værdien af afgange i henhold til LIFO-princippet. Indtil du kører lagerlukningsprocessen, værdisættes afgangsposteringerne med det løbende gennemsnit, når de fysiske og økonomiske opdateringer finder sted. Medmindre du bruger afmærkning, beregnes det løbende gennemsnit, når den fysiske eller økonomiske opdatering udføres.

Det anbefales, at du udfører en periodevis lagerlukning, når du bruger LIFO-datolagermodellen.

I følgende eksempler vises virkningen ved at bruge LIFO-dato i tre forskellige konfigurationer:

- LIFO-dato uden markering af indstillingen **Medtag fysisk værdi**
- LIFO-dato med markering af indstillingen **Medtag fysisk værdi**
- LIFO-dato med markering

## <a name="lifo-date-without-the-include-physical-value-option"></a>LIFO-dato uden markering af indstillingen Medtag fysisk værdi

I dette eksempel er det ikke angivet, at varemodelgruppen skal medtage fysisk værdi. I følgende illustration vises disse posteringer:

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
- 7\. Lagerlukningen udføres. På baggrund af LIFO-datometoden udlignes den første økonomisk opdaterede afgang mod den sidste økonomisk opdaterede tilgang med start den første dato osv. I dette eksempel oprettes der én udligning mellem 3b og 2b. Der foretages en regulering på USD 6,00 til 3b, og den endelige omkostning bliver USD 22,00.

Følgende illustration viser effekten af LIFO-datolagermodellen, når indstillingen **Medtag fysisk værdi** ikke bruges.

![LIFO-dato uden markering af indstillingen Medtag fysisk værdi.](media/lifo-date-without-include-physical-value.png)

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

## <a name="lifo-date-with-the-include-physical-value-option"></a>LIFO-dato med markering af indstillingen Medtag fysisk værdi

Hvis afkrydsningsfeltet **Medtag fysisk værdi** er markeret for en vare på siden **Varemodelgrupper**, bruger systemet både fysiske og økonomiske tilgangsposteringer til beregning af den løbende gennemsnitskostpris. Hvis det er relevant, regulerer systemet også den fysisk opdaterede afgangstransaktion. Når afkrydsningsfeltet **Medtag fysisk værdi** ikke er markeret, vil lagerlukning, der bruger med lagermodellen LIFO-dato, kun gennemføre udligninger af økonomisk opdaterede posteringer.

I dette eksempel er det angivet, at varemodelgruppen skal medtage fysisk værdi. 

I følgende illustration vises disse posteringer:

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
- 7\. Lagerlukningen udføres. På baggrund af LIFO-datometoden udlignes den første økonomisk opdaterede afgang mod den sidste økonomisk opdaterede tilgang for hver dato med start den første dato osv. I dette eksempel oprettes der én udligning mellem 2b og 3b. Der foretages en regulering på USD 6,00 til 3b, og den endelige omkostning bliver USD 22,00. Desuden bliver posteringen i 6a reguleret i forhold til tilgangsposteringens omkostning for 5b. Systemet udligner ikke disse posteringer, da tilgangen kun opdateres fysisk, men ikke økonomisk. Der bogføres i stedet kun en regulering på USD 6,33 i den fysiske afgangspostering, og den regulerede omkostning bliver USD 30,00.

Følgende illustration viser effekten af LIFO-lagermodellen, når indstillingen **Medtag fysisk værdi** bruges.

![LIFO-dato med markering af indstillingen Medtag fysisk værdi.](media/lifo-date-with-include-physical-value.png)

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

## <a name="lifo-date-with-marking"></a>LIFO-dato med markering

Afmærkning er en proces, som giver dig mulighed for at tilknytte – eller afmærke – en afgangspostering til en tilgangspostering. Afmærkning kan ske enten før eller efter, at en postering er bogført. Du kan bruge afmærkning, når du vil være sikker på den nøjagtige kostpris for lageret, når posteringen bogføres eller når lagerlukningen udføres. Antag f.eks., at kundeserviceafdelingen har modtaget en hasteordre fra en vigtig kunde. Da denne ordre er en hasteordre, skal du betale mere for denne vare for at kunne imødekomme kundens efterspørgsel.

Du skal være sikker på, at kostprisen på denne lagervare afspejles i dækningsbidraget eller i vareforbruget for salgsordrefakturaen. Når indkøbsordren bogføres, modtages lagervarerne til et kostpris på kr. 120,00. Hvis dette salgsordredokument afmærkes til indkøbsordren, før følgesedlen eller fakturaen bogføres, vil vareforbruget være kr. 120,00 og ikke den aktuelle løbende gennemsnitskostpris for varen. Hvis følgesedlen eller fakturaen for salgsordren bogføres, før afmærkningen finder sted, bogføres vareforbruget til den løbende gennemsnitskostpris.

Før lagerlukningen udføres, kan disse to transaktioner afmærkes til hinanden.

Du kan afmærke en afgangspostering til en tilgang, før posteringen bogføres. Du kan markere dette fra en salgsordrelinje på siden **Oplysninger om salgsordrer** ved at vælge **Lager \> Markering** i oversigtspanelet **Salgsordrelinjer**. Du kan få vist de åbne tilgangsposteringer på siden **Afmærkning**.

Du kan også afmærke en afgangspostering til en tilgang, efter posteringen bogføres. Du kan matche eller afmærke en afgangspostering for en åben tilgangspostering for en lagerført vare fra en bogført lagerreguleringskladde.

I følgende illustration vises disse posteringer:

- 1a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
- 1b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
- 2a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
- 2b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 22,00 pr. stk.
- 3a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 16,00 (løbende gennemsnit af økonomisk bogførte posteringer).
- 3b. Økonomisk lagerafgang for et antal på 1 til en kostpris af USD 16,00 (løbende gennemsnit af økonomisk bogførte posteringer).
- 3c. Økonomisk lagerafgang for 3b er afmærket til økonomisk lagerafgang for 1b.
- 4a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 25,00 pr. stk.
- 5a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
- 5b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
- 6a. Fysisk lagerafgang for et antal på 1 til en kostpris af USD 23,00 (løbende gennemsnit af økonomisk bogførte posteringer)
- 7\. Lagerlukningen udføres. På baggrund af afmærkningsprincippet, der bruger LIFO-datometoden, udlignes de markerede posteringer mod hinanden. I dette eksempel udlignes 3b mod 1b, og der bogføres en regulering på USD -6,00 for 3b for at få værdien til at blive USD 10,00. I dette eksempel foretages der ingen yderligere udligninger, da lukningen kun opretter udligninger for økonomisk opdaterede posteringer.

I følgende illustration vises virkningerne af at vælge lagermodellen for LIFO-dato, når der bruges afmærkning mellem afgange og tilgange. 

![LIFO-dato med markering.](media/lifo-date-with-marking.png)

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
- Udligninger og afmærkninger, der foretages ved lagerlukning, angives med stiplede, røde pile, der går diagonalt fra en tilgang til en afgang.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
