---
title: LIFO med fysisk værdi og afmærkning
description: LIFO (Last in, First out) er en lagermodel, hvor de senest anskaffede (nyeste) tilgange afgår først. Afgange fra lageret udlignes mod de seneste tilgange på lageret baseret på datoen for lagertransaktioner.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55021
ms.assetid: 49c492b0-b018-44e0-928f-9671e54eee20
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dcac72a60eac6abb29a017eb4ce02a71dca572d3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344538"
---
# <a name="lifo-with-physical-value-and-marking"></a>LIFO med fysisk værdi og afmærkning

[!include [banner](../includes/banner.md)]

LIFO (Last in, First out) er en lagermodel, hvor de senest anskaffede (nyeste) tilgange afgår først. Afgange fra lageret udlignes mod de seneste tilgange på lageret baseret på datoen for lagertransaktioner. 

I LIFO-lagermodellen (Last In, First Out) udstedes de seneste (nyeste) tilgange først. Afgange fra lageret udlignes mod de seneste tilgange på lageret, baseret på datoen for lagertransaktionerne. Når du bruger LIFO, behøver du ikke at bruge LIFO-reglen. I stedet kan du markere lagerposteringer, så en specifik vareafgang udlignes mod en specifik tilgang. Det anbefales, at du udfører en periodevis lagerlukning, når du bruger LIFO-lagermodellen. 

I følgende eksempler vises virkningen ved at bruge LIFO i tre forskellige konfigurationer:

-   LIFO uden indstillingen **Medtag fysisk værdi**
-   LIFO med indstillingen **Medtag fysisk værdi**
-   LIFO med afmærkning

## <a name="lifo-without-the-include-physical-value-option"></a>LIFO uden indstillingen Medtag fysisk værdi
I dette eksempel er det ikke angivet, at varemodelgruppen skal medtage fysisk værdi. I følgende illustration vises disse posteringer:

-   1a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
-   1b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 10,00 pr. stk.
-   2a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
-   2b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 20,00 pr. stk.
-   3a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 25,00 pr. stk.
-   4a. Fysisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
-   4b. Økonomisk lagertilgang for et antal på 1 til en kostpris a kr. 30,00 pr. stk.
-   5a. Fysisk lagerafgang for et antal på 1 til en kostpris af kr. 20,00 pr. stk. (løbende gennemsnit af økonomisk opdaterede posteringer).
-   5b. Økonomisk lagerafgang for et antal på 1 til en kostpris af kr. 20,00 pr. stk. (løbende gennemsnit af økonomisk opdaterede posteringer).
-   6. Lagerlukningen udføres. På baggrund af LIFO-metoden udlignes den seneste økonomisk opdaterede afgang mod den seneste økonomisk opdaterede tilgang. Der foretages en regulering på kr. 10,00 på afgangsposteringen.

Den nye løbende gennemsnitskostpris afspejler gennemsnittet af de økonomisk opdaterede posteringer, kr. 15,00. Følgende illustration viser effekten af LIFO-lagermodellen på denne række posteringer, når indstillingen **Medtag fysisk værdi** ikke bruges. 

![LIFO uden Medtag fysisk værdi.](./media/lifowithoutincludephysicalvalue.gif) 

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

## <a name="lifo-with-the-include-physical-value-option"></a>LIFO med indstillingen Medtag fysisk værdi
Hvis afkrydsningsfeltet **Medtag fysisk værdi** er markeret for en vare på siden **Varemodelgrupper**, bruger systemet både fysiske og økonomiske tilgangsposteringer til beregning af den løbende gennemsnitskostpris. Hvis det er relevant, udfører systemet også justeringer i den fysisk opdaterede afgangstransaktion. Når afkrydsningsfeltet **Medtag fysisk værdi** ikke er markeret, vil lagerlukning med lagermodellen LIFO kun gennemføre udligninger af økonomisk opdaterede posteringer. 

I følgende illustration vises disse posteringer:

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
-   7. Lagerlukningen udføres. På baggrund af LIFO-metoden reguleres eller udlignes den seneste afgangspostering mod den senest opdaterede tilgang.

Posteringen i 6a reguleres i forhold til tilgangspostering i 4b. Systemet udligner ikke disse posteringer, da tilgangen kun opdateres fysisk, men ikke økonomisk. Der bogføres i stedet kun en regulering på kr. 8,75 for den fysiske afgangspostering. Posteringen i 5b reguleres i forhold til fysisk tilgangspostering i 3a. Disse posteringer udlignes ikke, da de begge ikke opdateres økonomisk. Der sker i stedet kun en regulering på kr. - 3,75 for denne afgangspostering. Den nye løbende gennemsnitskostpris afspejler gennemsnittet af de økonomisk og fysisk opdaterede transaktioner på kr. 20,00. 

Følgende illustration viser effekten af LIFO-lagermodellen på denne række posteringer, når indstillingen **Medtag fysisk værdi** bruges. 

![LIFO med Medtag fysisk værdi.](./media/lifowithincludephysicalvalue.gif) 

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

## <a name="lifo-with-marking"></a>LIFO med afmærkning
Afmærkning er en proces, som giver dig mulighed for at tilknytte – eller afmærke – en afgangspostering til en tilgangspostering. Afmærkning kan ske enten før eller efter, at en postering er bogført. Du kan bruge afmærkning, når du vil være sikker på den nøjagtige kostpris for lageret, når posteringen bogføres eller når lagerlukningen udføres. Antag f.eks., at kundeserviceafdelingen har modtaget en hasteordre fra en vigtig kunde. Da denne ordre er en hasteordre, skal du betale mere for denne vare for at kunne imødekomme kundens efterspørgsel. 

Du skal være sikker på, at kostprisen på denne lagervare afspejles i dækningsbidraget eller i vareforbruget for denne salgsordrefaktura. Når indkøbsordren bogføres, modtages lagervarerne til et kostpris på kr. 120,00. Hvis dette salgsordredokument afmærkes til indkøbsordren, før følgesedlen eller fakturaen bogføres, vil vareforbruget være kr. 120,00 og ikke den aktuelle løbende gennemsnitskostpris for varen. Hvis følgesedlen eller fakturaen for salgsordren bogføres, før afmærkningen finder sted, bogføres vareforbruget til den løbende gennemsnitskostpris. 

Før lagerlukningen udføres, kan disse to transaktioner afmærkes til hinanden. 

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
-   7. Lagerlukningen udføres. Da den økonomisk opdaterede FIFO-postering er afmærket til en eksisterende tilgang, udlignes disse posteringer mod hinanden, og der udføres ingen justeringer.

Den nye løbende gennemsnitskostpris afspejler gennemsnittet af de økonomisk og fysisk opdaterede transaktioner på kr. 27,50. 

I følgende illustration vises effekterne af LIFO-lagermodellen på denne række af posteringer, når afmærkning mellem afgange og tilgange anvendes. 

![LIFO med afmærkning.](./media/lifowithmarking.gif) 

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