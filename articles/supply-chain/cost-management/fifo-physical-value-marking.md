---
title: FIFO med fysisk værdi og afmærkning
description: FIFO (First in, First out) er en lagermodel, hvor de først anskaffede tilgange afgår først. Økonomisk opdaterede afgange fra lageret udlignes mod de første økonomisk opdaterede tilgange til lageret på baggrund af den økonomiske dato for lagertransaktionen.
author: AndersGirke
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.assetid: dc0e2855-83a0-41a7-a398-3c7852597d1a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e2a8b9badcca82c8041158a9911f8d91b7d54d773610054361b7e1cc232ca5e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769581"
---
# <a name="fifo-with-physical-value-and-marking"></a>FIFO med fysisk værdi og afmærkning

[!include [banner](../includes/banner.md)]

FIFO (First in, First out) er en lagermodel, hvor de først anskaffede tilgange afgår først. Økonomisk opdaterede afgange fra lageret udlignes mod de første økonomisk opdaterede tilgange til lageret på baggrund af den økonomiske dato for lagertransaktionen. 

Når du bruger FIFO, behøver du ikke at bruge FIFO-reglen. I stedet kan du markere lagerposteringer, så en specifik varetilgang udlignes mod en specifik afgang. Det anbefales, at du udfører en periodevis lagerlukning, når du bruger FIFO-lagermodellen. I følgende eksempler vises virkningen ved at bruge FIFO i tre forskellige konfigurationer:

-   FIFO uden indstillingen **Medtag fysisk værdi**
-   FIFO med indstillingen **Medtag fysisk værdi**
-   FIFO med afmærkning

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO uden indstillingen Medtag fysisk værdi
I dette eksempel er det ikke angivet, at varemodelgruppen skal medtage fysisk værdi. I følgende illustration vises disse posteringer:

-   1a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
-   1b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
-   2a. Fysisk lagertilgang for et antal på 2 til en kostpris a kr. 10,00 pr. stk.
-   2b. Økonomisk lagertilgang for et antal på 2 til en kostpris a kr. 10,00 pr. stk.
-   3a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 25,00 pr. stk.
-   4a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
-   4b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
-   5a. Fysisk lagerafgang for et antal på 1 til en kostpris af kr. 20,00 pr. stk. (løbende gennemsnit af økonomisk opdaterede posteringer).
-   5b. Økonomisk lagerafgang for et antal på 1 til en kostpris af kr. 15,00 pr. stk. (løbende gennemsnit af økonomisk opdaterede posteringer).
-   6. Lagerlukningen udføres. På baggrund af FIFO-metoden udlignes den første økonomisk opdaterede afgang mod den første økonomisk opdaterede tilgang. Der foretages en regulering på USD -5,00 på afgangsposteringen.

Den nye løbende gennemsnitskostpris afspejler gennemsnittet af de økonomisk opdaterede posteringer. Følgende illustrationer viser effekten af FIFO-lagermodellen på denne række posteringer, når indstillingen **Medtag fysisk værdi** ikke bruges. 

![FIFO uden Medtag fysisk værdi.](./media/fifowithoutincludephysicalvalue.gif) 

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

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO med indstillingen Medtag fysisk værdi
Hvis afkrydsningsfeltet **Medtag fysisk værdi** er markeret for en vare på siden **Varemodelgruppe**, bruger systemet både fysiske og økonomiske tilgangsposteringer til beregning af den løbende gennemsnitskostpris. Hvis det er relevant, udfører systemet også justeringer i den fysisk opdaterede afgangstransaktion. Når afkrydsningsfeltet **Medtag fysisk værdi** ikke er markeret, vil lagerlukning med lagermodellen FIFO kun gennemføre udligninger af økonomisk opdaterede posteringer. I følgende illustration vises disse posteringer:

-   1a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
-   1b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
-   2a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
-   2b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
-   3a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 25,00 pr. stk.
-   4a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
-   4b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
-   5a. Fysisk lagerafgang for et antal på 1 til en kostpris af kr. 21,25 pr. styk (det løbende gennemsnit af økonomisk og fysisk opdaterede posteringer).
-   5b. Økonomisk lagerafgang for et antal på 1 til en kostpris af kr. 21,25 pr. stk. (løbende gennemsnit af økonomisk og fysisk opdaterede posteringer).
-   6a. Fysisk lagerafgang for et antal på 1 til en kostpris a kr. 21,25 pr. stk.
-   7. Lagerlukningen udføres. På baggrund af FIFO-metoden reguleres eller udlignes den første økonomiske afgangspostering mod den første opdaterede tilgang, uanset om den er økonomisk eller fysisk.

Postering 5b udlignes mod tilgangspostering 1b. Der foretages en regulering på USD -11,25 på afgangsposteringen. Den nye løbende gennemsnitskostpris afspejler gennemsnittet af de økonomisk og fysisk opdaterede transaktioner på kr. 27,50. Følgende illustration viser effekten af FIFO-lagermodellen på denne række posteringer, når indstillingen **Medtag fysisk værdi** bruges. 

![FIFO med Medtag fysisk værdi.](./media/fifowithincludephysicalvalue.gif) 

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

## <a name="fifo-with-marking"></a>FIFO med afmærkning
Afmærkning er en proces, som giver dig mulighed for at tilknytte – eller afmærke – en afgangspostering til en tilgangspostering. Afmærkning kan ske enten før eller efter, at en postering er bogført. Du kan bruge afmærkning, når du vil være sikker på den nøjagtige kostpris for lageret, når posteringen bogføres eller når lagerlukningen udføres. Antag f.eks., at kundeserviceafdelingen har modtaget en hasteordre fra en vigtig kunde. Da denne ordre er en hasteordre, skal du betale mere for denne vare for at kunne imødekomme kundens efterspørgsel. Du skal være sikker på, at kostprisen på denne lagervare afspejles i dækningsbidraget eller i vareforbruget for denne salgsordrefaktura. Når indkøbsordren bogføres, modtages lagervarerne til et kostpris på kr. 120,00. Hvis dette salgsordredokument afmærkes til indkøbsordren, før følgesedlen eller fakturaen bogføres, vil vareforbruget være kr. 120,00 og ikke den aktuelle løbende gennemsnitskostpris for varen. Hvis følgesedlen eller fakturaen for salgsordren bogføres, før afmærkningen finder sted, bogføres vareforbruget til den løbende gennemsnitskostpris. Før lagerlukningen udføres, kan disse to transaktioner afmærkes til hinanden. Når en tilgangstransaktion matcher en afgangstransaktion, vil den værdiansættelsesmetode, der er defineret i varens modelgruppe, blive tilsidesat, og systemet udligner disse transaktioner mod hinanden. Du kan afmærke en afgangspostering til en tilgang, før posteringen bogføres. Du kan gøre dette fra en salgsordrelinje på siden **Oplysninger om salgsordre**. Du kan få vist de åbne tilgangsposteringer på siden **Afmærkning**. Du kan også afmærke en afgangspostering til en tilgang, efter posteringen bogføres. Du kan matche eller afmærke en afgangspostering for en åben tilgangspostering for en lagerført vare fra en bogført lagerreguleringskladde. I følgende illustration vises disse posteringer:

-   1a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
-   1b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
-   2a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
-   2b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
-   3a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 25,00 pr. stk.
-   4a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
-   4b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
-   5a. Fysisk lagerafgang for et antal på 1 til en kostpris af kr. 21,25 pr. styk (det løbende gennemsnit af økonomisk og fysisk opdaterede posteringer).
-   5b. Økonomisk lagerafgang for et antal på 1 afmærkes til lagertilgang 2b, inden transaktionen bogføres. Transaktionen bogføres til en kostpris af kr. 20,00 pr. styk.
-   6a. Fysisk lagerafgang for et antal på 1 til en kostpris a kr. 21,25 pr. stk.
-   7. Lagerlukningen udføres. Da den økonomisk opdaterede FIFO-postering er afmærket til en eksisterende tilgang, udlignes disse posteringer mod hinanden, og der udføres ingen justeringer.

Den nye løbende gennemsnitskostpris afspejler gennemsnittet af de økonomisk og fysisk opdaterede transaktioner på kr. 27,50. I følgende illustration vises effekterne af FIFO-lagermodellen på denne række af posteringer, når afmærkning mellem afgange og tilgange anvendes. 

![FIFO med afmærkning.](./media/fifowithmarking.gif) 

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






[!INCLUDE[footer-include](../../includes/footer-banner.md)]