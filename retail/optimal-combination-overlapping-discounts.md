---
title: "Fastslå den optimale kombination af overlappende rabatter"
description: "Når rabatter overlapper hinanden, skal du bestemme kombinationen af overlappende rabatter, der resulterer i de laveste samlede transaktion eller den højeste samlede rabat. Når rabatbeløbet afhænger af prisen på de produkter, der købes, sådan som fælles &quot;køber 1, få 1 X procent rabat&quot; detailrabat (BOGO), denne proces bliver et problem for optimering af combinatorial."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.region: global
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 31e5104045ed5b8fbfa3677a7f5702d551de4231
ms.lasthandoff: 03/31/2017


---

# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a>Fastslå den optimale kombination af overlappende rabatter

Når rabatter overlapper hinanden, skal du bestemme kombinationen af overlappende rabatter, der resulterer i de laveste samlede transaktion eller den højeste samlede rabat. Når rabatbeløbet afhænger af prisen på de produkter, der købes, sådan som fælles "køber 1, få 1 X procent rabat" detailrabat (BOGO), denne proces bliver et problem for optimering af combinatorial.

Denne artikel gælder for Microsoft Dynamics AX 2012 R3 med KB 3105973 (udgivet 2 November 2015) eller nyere, og til februar-2016 slippe af Microsoft Dynamics AX. Du kan se de kombination overlappende rabatter udlignes i tide og fortsat store discounting funktionalitet, der er tilgængelige i Microsoft Dynamics AX for Retail, har vi introduceret en metode til anvendelse af overlappende rabatter. Vi kalder denne nye metode **marginale værdi rangordning**. Rangordning af marginale værdi bruges, når den tid, der kræves for at vurdere de mulige kombinationer af overlappende rabatter overstiger en tærskel, der kan konfigureres på den **Retail parametre** side i Dynamics AX. I den marginale værdi rangering metode, beregnes en værdi for hver overlappende rabat ved hjælp af den rabatværdi for de produkter, der er delt. Overlappende rabatterne anvendes derefter fra den højeste relative værdi til den laveste relative værdi. Se afsnittet "Marginale værdi" senere i denne artikel for at få oplysninger om den nye metode. Rangordning af marginale værdi bruges ikke, når rabatbeløbene for et produkt ikke er berørt af et andet produkt i transaktionen. Denne metode er ikke bruges til to enkle rabatter eller til en simpel rabat og et enkelt produkt mængderabat.

## <a name="discount-examples"></a>Rabat eksempler
Du kan oprette et ubegrænset antal retail rabatter på et fælles sæt af produkter i Dynamics AX. Men fordi der er ingen grænse, problemer med ydeevnen kan opstå, når du forsøger at beregne de rabatter, der skal bruges på de forskellige produkter. Følgende eksempler illustrerer problemet mere detaljeret. Vi starter med to produkter og to overlappende rabatter i eksempel 1. Derefter i eksempel 2 viser vi hvordan problemet udvikles der føjes flere produkter.

### <a name="example-1-two-products-and-two-discounts"></a>Eksempel 1: To produkter og to rabatter

I dette eksempel to produkter, der er nødvendige for at kunne opnå hver rabat og rabatter kan ikke kombineres. Rabatter i dette eksempel er **bedste pris** rabatter. Begge produkter opfylder betingelserne for begge rabatter. Her er de to rabatter. [![Overlappende rabat combo 01](./media/overlapping-discount-combo-01.jpg)](./media/overlapping-discount-combo-01.jpg) For to produkterne, jo bedre af disse to rabatter, afhænger af priserne på de to produkter. Når prisen på begge produkter er lig med eller næsten lig, er rabat 1 bedre. Når prisen på en vare er betydeligt mindre end prisen på det pågældende produkt, er rabatten 2 bedre. Her er den matematiske regel for at vurdere disse to rabatter mod hinanden: [![Overlapping rabat combo 02](./media/overlapping-discount-combo-02.jpg)](./media/overlapping-discount-combo-02.jpg) Bemærk, når prisen på produktet 1 er lig med to tredjedele af prisen på produktet 2, de to rabatter er ens. I dette eksempel varierer effektive rabatprocent for rabat 1 fra et par procent (når priserne på de to produkter er langt fra hinanden) til maksimalt 25 procent (når de to produkter har den samme pris). Effektiv rabatprocent for rabat 2 er løst. Det er altid 20 procent. Da den effektive rabatprocent for rabat 1 har et område, der kan være større eller mindre end rabat 2, afhænger af den bedste rabat priserne på de to produkter, der skal tilbagediskonteres. I dette eksempel er beregningen udført hurtigt, fordi kun to rabatter på kun to produkter. Der er kun to mulige kombinationer: et program for rabat 1 eller en rabat på 2. Der er ingen permutationer til at beregne. Værdien af hver rabat beregnes ved hjælp af begge produkter, og den bedste rabat bruges.

### <a name="example-2-four-products-and-two-discounts"></a>Eksempel 2: Fire produkter og to rabatter

Derefter skal bruge vi fire produkter og de samme to rabatter. Alle fire produkter opfylder betingelserne for begge rabatter. Der er tolv mulige kombinationer. I sidste ende, to rabatter gælder for posteringen i en af tre kombinationer: to programmer rabatprocent 1, to programmer af rabat 2 eller en anvendelse af rabat 1 og en anvendelse af rabat 2. For at illustrere de mulige kombinationer, ser vi nærmere på to forskellige sæt af fire produkter, der har forskellige priser:

-   Alle fire produkter har den samme pris, $15.00. I dette tilfælde er den bedste kombination af rabat to programmer rabatprocent 1. To produkter bliver fuld pris, og to vil være 50 procent fra. Totalbeløbet for posteringen er $45 (15 + 15 + 7,50 + 7,50), som er $15 (25 procent) fra de undiscounted samlede $60. Rabatten 2 er kun $12 (20 procent).
-   To produkter er $20 hver, ét produkt er $15, og et produkt er $5. I dette tilfælde er den bedste kombination af rabat ét program rabatten 2 og en anvendelse af rabat 1. Følgende tabeller viser rabatterne.

For at læse tabellerne, skal du bruge et produkt fra en række og ét produkt fra en kolonne. For eksempel i tabellen til rabat 1 kom når du kombinerer de to produkter i $20 du $10. I tabel 2 rabat, når du kombinerer $15 produktet og $5-produkt, får du $4. [![Overlappende rabat combo 03](./media/overlapping-discount-combo-03.jpg)](./media/overlapping-discount-combo-03.jpg) først skal vi finde den største rabat, der er tilgængelig fra to produkterne ved hjælp af enten rabat. De to tabeller vises rabatbeløbet for alle kombinationer af de to produkter. Skyggedele tabeller repræsenterer enten tilfælde, hvor et produkt er parret med sig selv, som vi ikke kan gøre, eller omvendt samparring af to produkter, der giver den samme rabatbeløb og kan ignoreres. Ved at kigge på tabellerne, kan du se, at rabatten 1 for de to $20 varer er den største rabat, der er tilgængelig for enten rabat på alle fire produkter. (Denne rabat er fremhævet med grønt i den første tabel.) Der lader $15 produktet og $5 produktet. Ved at kigge på de to tabeller igen, kan du se, at i disse to produkter, rabat 1 giver en rabat på $2.50, hvorimod rabatten 2 giver en rabat på $4. Derfor kan vi vælge rabat 2. Den samlede rabat er $14. For at gøre det nemmere at visualisere denne diskussion, er her to flere tabeller, der vises rabatprocenten, der er gældende for alle mulige kombinationer af to produkt til begge rabat 1 og rabat 2. Kun halvdelen oversigten over kombinationer er inkluderet, da disse to rabatter, den rækkefølge, hvori de to produkter bringes i rabatten ligegyldigt. Den højeste effektive rabat (25 procent) er fremhævet med grønt og den laveste effektive rabat (10 procent) er fremhævet med rødt. [![Overlappende rabat combo 04](./media/overlapping-discount-combo-04.jpg)](./media/overlapping-discount-combo-04.jpg)**Note:** når priser varierer, og to eller flere rabat konkurrere, er den eneste måde at sikre den bedste kombination af rabatter til at evaluere både rabatter og sammenligne dem.

## <a name="total-possible-combinations"></a>Samlede mulige kombinationer
Dette afsnit fortsætter med eksemplet fra den forrige sektion. Vi vil føje flere produkter og en anden rabat, og du kan se, hvor mange kombinationer, der skal beregnes og sammenlignes. Følgende tabel viser antallet af mulige rabatkombinationer som produkt antal øges. I tabel vises, hvad der sker, både når der er to overlappende rabatter, som i forrige eksempel, og når der er tre overlappende rabatter. Antallet af mulige rabatkombinationer, der skal evalueres overstiger hurtigst, hvad en hurtig computer kan beregne og sammenligne hurtigt nok til at være acceptabel for detailtransaktioner. [![Overlappende rabat combo 05](./media/overlapping-discount-combo-05.jpg)](./media/overlapping-discount-combo-05.jpg) selv når større mængder eller flere overlappende rabatter, det samlede antal mulige rabatkombinationer går hurtigt i millioner og den tid, der kræves for at vurdere og vælge den bedste mulige kombination hurtigt bliver mærkbar. Nogle optimeringer har udført i retail pris motoren til at reducere det samlede antal kombinationer, der skal evalueres. Men fordi de overlappende antal rabatter og mængder i en transaktion ikke er begrænset, har et stort antal kombinationer altid skal evalueres, når der er overlappende rabatter. Problemet er, som den marginale værdi rangering metode løser problemet.

## <a name="marginal-value-method"></a>Marginale værdi metode
For at løse problemet på en eksponentielt stigende antal kombinationer, der skal evalueres, findes en optimering, der beregner værdien pr. delt produkt for hver rabat på sættet af produkter, der kan anvendes to eller flere rabatter til. Vi henviser til denne værdi som den **marginale værdi** rabat for de produkter, der er delt. Den marginale værdi er gennemsnit pr. produkt stigning i det samlede rabatbeløb, når de delte produkter er inkluderet i hver rabat. Den marginale værdi beregnes ved at tage det samlede rabatbeløb (DTotal) fratrække rabatbeløbet uden delte produkter (DMinus\\ delt), og dividere forskellen med antallet af delte produkter (ProductsShared). [![Overlappende rabat combo 06](./media/overlapping-discount-combo-06.jpg)](./media/overlapping-discount-combo-06.jpg) efter den marginale værdi af hver rabat på et delt sæt produkter er beregnet, de rabatter på de produkter, der er delt i rækkefølge, omfattende, fra højeste marginale værdi til laveste marginale værdi. Denne metode er ikke alle resterende rabat muligheder sammenlignet med hver gang, når der anvendes en enkelt forekomst af en rabat. I stedet de overlappende rabatter sammenlignet én gang og derefter anvendes i rækkefølge. Ingen yderligere sammenligninger er færdig. Du kan konfigurere tærsklen for at skifte til den marginale værdi metode den **rabat** tab af den **Retail parametre** side. Acceptabel tid til at beregne den samlede rabat varierer på tværs af brancher for retail. Denne gang ligger dog generelt mellem titusindvis af millisekunder til en anden.


