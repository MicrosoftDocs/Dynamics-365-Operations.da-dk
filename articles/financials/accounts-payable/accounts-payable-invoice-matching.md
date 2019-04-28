---
title: Fakturasammenholdelse for Kreditor
description: Fakturasammenholdelse for kreditorer er den proces, hvor kreditorfakturaen, indkøbsordren og produktkvitteringen sammenholdes.
author: abruer
manager: AnnBe
ms.date: 02/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 27361
ms.assetid: 9f3dace7-05d8-4974-8f85-aca2e224876c
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74a1f7e16064a954bb22dc233a77bf28747f7f11
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/25/2019
ms.locfileid: "896942"
---
# <a name="accounts-payable-invoice-matching"></a>Fakturasammenholdelse for Kreditor

[!include [banner](../includes/banner.md)]

Fakturasammenholdelse for kreditorer er den proces, hvor kreditorfakturaen, indkøbsordren og produktkvitteringen sammenholdes.

Når du sammenholder dokumenter, kaldes forskelle mellem disse dokumenter sammenholdelsesafvigelser. Matchningsafvigelser sammenlignes med de angivne tolerancer. Hvis en matchningafvigelse overskrider toleranceprocenten eller -beløbet, vises ikoner for matchafvigelse på siden Kreditorfaktura og på siden Detaljer om fakturasammenholdelse. 

Det kan f.eks. være, at du indtaster en indkøbsordre med ét linjeelement til 1.000 batterier til en pris på 1,00 pr. stk. Indkøbsordren godkendes og sendes til leverandøren. Leverandøren afsender 1.000 batterier, og du indtaster en produktkvittering for 1.000 batterier til en pris på 1,00 pr. stk. Lageromkostningen for batterierne opdateres med denne pris. 

Der modtages en faktura for 1.000 batterier til en pris af 1,10 pr. stk. Ifølge din juridiske enhedspolitik tillades en tolerance for nettoenhedspris på 5 procent for denne varekategori. En pris på 1,05 ville være acceptabel, men det er 1,10 ikke. Når du indtaster fakturaoplysningerne, identificeres en matchningafvigelse i pris, og du kan gemme fakturaen, indtil uoverensstemmelsen er løst.

Du kan bruge følgende typer fakturasammenholdelse for kreditorer:

-   Sammenholdelse af fakturatotaler – sammenlign de samlede beløb på fakturaen med de samlede beløb på indkøbsordren. Denne type fakturasammenholdelse involverer færrest detaljer, så du kan bruge denne indstilling til at definere kontrolelementer, der minimerer den tid, personalet skal bruge på at gennemgå oplysninger om fakturasammenholdelse.
-   Tovejs-sammenholdelse – sammenlign prisoplysningerne på fakturaen med prisoplysningerne på indkøbsordren.
-   Trevejs-sammenholdelse – sammenlign prisoplysningerne på fakturaen med prisoplysningerne på indkøbsordren. Sammenlign også oplysninger om antal på fakturaen med oplysningerne om antal på de produktkvitteringer, der er valgt til fakturaen.
-   Sammenholdelse af tillæg – sammenlign oplysninger om tillæg (beløb) på fakturaen med oplysningerne om tillæg (beløb) på indkøbsordren.

> [!NOTE]
> Der kan udføres andre former for fakturavalidering med brug af politikker for kreditorfakturaer. 

Ved tovejs- og trevejs-sammenholdelse sammenlignes prisoplysninger altid med enhedsprisen. Du kan også konfigurere disse sammenholdelsespolitikker, så du kan sammenligne prisoplysninger med den samlede pris.
-   Sammenholdelse af nettoenhedspris – sammenlign prisoplysninger for tovejs- eller trevejs sammenholdelse ved at sammenligne nettoenhedsprisen for hver linje på fakturaen med den tilsvarende nettoenhedspris på indkøbsordren. Nettoenhedsprisen bestemmes af følgende formel: Nettobeløbet for linjen/antallet på linjen
-   Sammenholdelse af samlede priser – sammenlign prisoplysninger for tovejs- eller trevejs sammenholdelse ved at sammenligne nettobeløbet (den samlede pris) for hver linje på fakturaen med det tilsvarende nettobeløb på indkøbsordren. Nettobeløbet bestemmes af følgende formel: *(Enhedspris \* linjeantal) + linjetillæg - linjerabatter*. Når du sammenholder pristotaler med procentdel, sammenligner systemet værdier ved hjælp af transaktionsvalutaen. Når du sammenholder pristotaler med beløb, sammenligner systemet værdierne ved hjælp regnskabsvalutaen.

Beregninger af fakturasammenholdelse udføres som regel automatisk, når du redigerer kreditorfakturaer på siden Kreditorfaktura. Alternativt kan fakturasammenholdelse udføres efter behov. Fakturasammenholdelse ved behov styres for den juridiske enhed af Opdater status for fakturahoved automatisk på siden kontiene Kreditorparametre under fanen Fakturavalidering. Fakturasammenholdelse kan også udføres som del af en fakturavalidering. Du kan få vist resultaterne af fakturasammenholdelse på siden Kreditorfaktura og relaterede fakturasammenholdelsesformularer.

## <a name="invoice-totals-matching"></a>Sammenholdelse af fakturatotaler
Du kan bruge sammenholdelse af fakturatotaler til at sikre, at de samlede fakturabeløb ikke afviger fra forventede beløb med mere end en acceptabel afvigelse. Seks totaler sammenholdes siden Fakturatotalers tilsvarende oplysninger, som vist i følgende tabel. Hvis den tilladte tolerance for sammenholdelse af fakturatotaler er 20 %, anses afvigelsesprocenten på 100 for det samlede rabatbeløb for at være en matchningafvigelse.

| Feltet Total    | Faktisk fakturatotal | Forventet fakturatotal | Afvigelsespct. | Matchstatus |
|----------------|----------------------|------------------------|---------------------|--------------|
| Saldo        | 495,00               | 495,00                 | 0 %                  | Bestået       |
| Slutrabat | 0,00                 | 9,90                   | 100 %                | Mislykkedes       |
| Tillæg        | 64,90                | 64,90                  | 0 %                  | Bestået       |
| Moms      | 139,98               | 137,50                 | 2 %                  | Bestået       |
| Afrunding      | 0,00                 | 0,00                   | 0 %                  | Bestået       |
| Fakturabeløb | 699,88               | 687,50                 | 2 %                  | Bestået       |

Sammenholdelse af fakturatotaler styres for den juridiske enhed af knappen Afstem fakturatotaler på siden Kreditorparametre. Sammenholdelse udføres på de forventede og faktiske fakturatotaler. De forventede fakturatotaler beregnes på grundlag af priser, tillæg og momsoplysninger fra indkøbsordren og antallene fra fakturaen.

## <a name="two-way-price-totals-matching"></a>Tovejs-sammenholdelse af pristotaler
Brug tovejs-sammenholdelse til at sikre, at afvigelsen mellem prisoplysningerne på indkøbsordren og fakturaen ligger inden for acceptable tolerancer. Du kan sammenligne prisoplysninger for nettobeløbet på hver linje på fakturaen og alle ventende og tidligere bogførte fakturalinjer med nettobeløbet på den tilsvarende indkøbsordrelinje. Dette kaldes sammenholdelse af pristotaler. 

Sammenholdelse af pristotaler kan være baseret på en procent, et beløb eller en procent og et beløb. 

Hvis der er angivet en toleranceprocent for en indkøbspristotal, sammenlignes fem felter som vist i følgende tabel. Da toleranceprocenten for indkøbspristotalen er 10, repræsenterer afvigelsesprocenten for pristotalen på 50 en matchningafvigelse.

| Matchstatus | Nettobeløb på faktura | Forventet nettobeløb | Procent for uafstemt indkøbspristotal (afvigelsesbeløb) | Procent for uafstemt indkøbspristotal (afvigelsesprocent) | Toleranceprocent for indkøbspristotaler |
|--------------|--------------------|---------------------|--------------------------------------------------|-----------------------------------------------------------------|----------------------------------------|
| Bestået       | 105,00             | 100,00              | 5,00                                             | 5 %                                                              | 10 %                                    |
| Mislykkedes       | 150,00             | 100,00              | 50,00                                            | 50 %                                                             | 10 %                                    |

Hvis der er angivet et tolerancebeløb for en indkøbspristotal, sammenlignes fem felter som vist i følgende tabel. Da tolerancebeløbet for indkøbspristotalen er 100,00, repræsenterer afvigelsesbeløbet for pristotalen på 105,00 en matchningafvigelse.

| Matchstatus | Nettobeløb på faktura | Forventet nettobeløb | Procent for uafstemt indkøbspristotal (afvigelsesbeløb) | Uafstemt indkøbspristotal i regnskabsvalutaen (afvigelsesbeløb) | Tolerance for indkøbspristotaler |
|--------------|--------------------|---------------------|--------------------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| Bestået       | 150,00             | 100,00              | 50,00                                            | 50,00                                                                   | 100,00                         |
| Mislykkedes       | 205,00             | 100,00              | 105,00                                           | 105,00                                                                  | 100,00                         |

Hvis der er konfigureret sammenholdelse af pristotaler med en procenttolerance og et tolerancebeløb, også kaldet et beløb, der ikke må overskrides, tages der højde for begge tolerancer, når det evalueres, om en linje har en matchningafvigelse. Hvis enten procenten eller beløbet overstiger tolerancen som vist på linjerne 150,00 og 205,00 i følgende tabel, har linjen en matchningafvigelse.

| Matchstatus | Nettobeløb på faktura | Forventet nettobeløb | Procent for uafstemt indkøbspristotal (afvigelsesprocent) | Toleranceprocent for indkøbspristotaler | Uafstemt indkøbspristotal i regnskabsvalutaen (afvigelsesbeløb) | Tolerance for indkøbspristotaler |
|--------------|--------------------|---------------------|-----------------------------------------------------------------|----------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| Bestået       | 105,00             | 100,00              | 5 %                                                              | 10 %                                    | 5,00                                                                    | 100,00                         |
| Mislykkedes       | 150,00             | 100,00              | 50 %                                                             | 10 %                                    | 50,00                                                                   | 100,00                         |
| Mislykkedes       | 205,00             | 100,00              | 105 %                                                            | 10 %                                    | 105,00                                                                  | 100,00                         |

Tovejs-sammenholdelsespolitik styres for den juridiske enhed af feltet Sammenholdelsespolitik for linjer på siden Kreditorparametre. Afhængigt af det, der er valgt i feltet Tillad overstyring af sammenholdelsespolitik, kan du vælge tovejs-sammenholdelse for en bestemt leverandør, vare eller kombination af vare og leverandør på siden Sammenholdelsespolitik og for en bestemt indkøbsordre på siden Indkøbsordre.

Sammenholdelse af pristotaler styres for den juridiske enhed af feltet Afstem pristotaler på siden Kreditorparametre. Toleranceprocenten og tolerancebeløbet for indkøbspristotalen (beløb, der ikke må overskrides) er også angivet på denne side.

## <a name="two-way-net-unit-price-matching"></a>Tovejs-sammenholdelse af nettoenhedspris
Brug tovejs-sammenholdelse til at sikre, at afvigelsen mellem prisoplysningerne på indkøbsordren og fakturaen ligger inden for acceptable tolerancer. Du kan sammenligne prisoplysninger for nettoenhedsprisen for hver vare på fakturaen. Dette kaldes sammenholdelse af nettoenhedspris. 

Ni linjebeløb sammenholdes siden Detaljer om fakturasammenholdelse, som vist i følgende tabel. Hvis den tilladte pristolerance for sammenholdelse af nettoenhedspris er 10 %, anses afvigelsen på 22,61 % for nettoenhedsprisen for at være en matchningafvigelse.

| Feltet Linje                    | Fakturaværdi | Værdi af indkøbsordre | Afvigelsespct. | Matchstatus |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Enhedspris                    | 55,40         | 55,38                | 0 %                  | Bestået       |
| Prisenhed                    | 1,00          | 1,00                 | 0 %                  | Bestået       |
| Indkøbsgebyrer          | 50,00         | 0,00                 | 100 %                | Mislykkedes       |
| Rabat                      | 0,00          | 0,00                 | 0 %                  | Bestået       |
| Rabatprocentdel              | 0,00          | 0,00                 | 0 %                  | Bestået       |
| Samkøbsrabat            | 0,00          | 0,00                 | 0 %                  | Bestået       |
| Samkøbsrabatprocent | 0,00          | 0,00                 | 0 %                  | Bestået       |
| Nettobeløb                    | 271,60        | 221,52               | 22,61 %              | Mislykkedes       |
| Nettoenhedspris                | 67,9000       | 55,3800              | 22,61 %              | Mislykkedes       |

Tovejs-sammenholdelsespolitik styres for den juridiske enhed af feltet Sammenholdelsespolitik for linjer på siden Kreditorparametre. Afhængigt af det, der er valgt i feltet Tillad overstyring af sammenholdelsespolitik, kan du vælge tovejs-sammenholdelse for en bestemt leverandør, vare eller kombination af vare og leverandør på siden Sammenholdelsespolitik og for en bestemt indkøbsordre på siden Indkøbsordre. 

Sammenholdelse af nettoenhedspris styres for den juridiske enhed af feltet Aktivér validering af fakturasammenholdelse på siden Kreditorparametre. Toleranceprocenter for nettoenhedsprisen kan konfigureres for varer, varegrupper, leverandører, leverandørgrupper, kombinationer af vare og leverandør eller juridisk enhed på siden Pristolerancer.

## <a name="two-way-price-totals-matching-and-net-unit-price-matching"></a>Tovejs-sammenholdelse af pristotaler og sammenholdelse af nettoenhedspris
Du kan bruge sammenholdelse af pristotaler og sammenholdelse af nettoenhedspris sammen. I dette eksempel forudsættes følgende konfiguration:

-   Tolerancen for nettoenhedsprisen for USB-drevelementet er 10 %.
-   Tolerancen for sammenholdelse af pristotaler for den juridiske enhed er 15 % eller 500,00.

Indkøbsordren indeholder følgende linje:

| Varenummer | Antal | Enhedspris | Nettobeløb |
|-------------|----------|------------|------------|
| USB-drev   | 1.000    | 10,00      | 10.000,00  |

Der indtastes tre fakturaer som vist i følgende tabel. Der er en uoverensstemmelse for fakturasammenholdelse for Faktura 3, fordi afvigelsen på 1.880,00 overstiger tolerancebeløbet for indkøbspristotalen på 500,00. For sammenholdelse af pristotaler omfatter fakturanettobeløbet alle tidligere bogførte fakturaer ud over den faktura, du aktuelt arbejder med.

| Varenummer          | Antal | Enhedspris | Nettobeløb | Prisafstemning | Pristotalafstemning |
|----------------------|----------|------------|------------|-------------|-------------------|
| Faktura 1: USB-drev | 800      | 10,80      | 8.640,00   | Bestået      | Bestået            |
| Faktura 2: USB-drev | 100      | 10,80      | 1.080,00   | Bestået      | Bestået            |
| Faktura 3: USB-drev | 200      | 10,80      | 2.160,00   | Bestået      | Mislykkedes            |
| I alt                |          |            | 11.880,00  |             |                   |

## <a name="three-way-matching"></a>Trevejs-sammenholdelse

Brug trevejs-sammenholdelse til at sikre, at afvigelsen mellem prisoplysningerne på indkøbsordren og fakturaen ligger inden for acceptable tolerancer og for at sikre, at antallet på fakturaen svarer til antallet på de tilsvarende produktkvitteringer.

Der sammenlignes samme linjebeløb på siden Detaljer om fakturasammenholdelse som ved tovejs-sammenholdelse. Derudover sammenlignes antallet på fakturaen med antallene på de produktkvitteringer, der er modtaget. Hvis fakturaantallet er forskelligt fra det sammenlignede antal på produktkvitteringen, er der fejl i sammenholdelsen af antal.

| Feltet Linje                    | Fakturaværdi | Værdi af indkøbsordre | Afvigelsespct. | Matchstatus |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Enhedspris                    | 55,40         | 55,38                | 0 %                  | Bestået       |
| Prisenhed                    | 1,00          | 1,00                 | 0 %                  | Bestået       |
| Indkøbsgebyrer          | 50,00         | 0,00                 | 100 %                | Mislykkedes       |
| Rabat                      | 0,00          | 0,00                 | 0 %                  | Bestået       |
| Rabatprocentdel              | 0,00          | 0,00                 | 0 %                  | Bestået       |
| Samkøbsrabat            | 0,00          | 0,00                 | 0 %                  | Bestået       |
| Samkøbsrabatprocent | 0,00          | 0,00                 | 0 %                  | Bestået       |
| Nettobeløb                    | 271,60        | 221,52               | 22,61 %              | Mislykkedes       |
| Nettoenhedspris                | 67,9000       | 55,3800              | 22,61 %              | Mislykkedes       |

| Feltet Linje                     | Fakturaværdi | Matchstatus |
|--------------------------------|---------------|--------------|
| Fakturaantal               | 4,00          |              |
| Sum af afstemte produktkvitteringer | 0,00          | Mislykkedes       |

Trevejs-sammenholdelsespolitik styres for den juridiske enhed af feltet Sammenholdelsespolitik for linjer på siden Kreditorparametre. Afhængigt af det, der er valgt i feltet Tillad overstyring af sammenholdelsespolitik, kan du vælge trevejs-sammenholdelse for en bestemt leverandør, vare eller kombination af vare og leverandør på siden Sammenholdelsespolitik og for en bestemt indkøbsordre på siden Indkøbsordre.

## <a name="charges-matching"></a>Sammenholdelse af gebyrer
Du kan bruge sammenholdelse af tillæg til at sikre, at tillægsbeløb ikke afviger fra forventede beløb med mere end en acceptabel afvigelsesprocent. De samlede beløb for hver tillægskode, der anvendes til fakturaen og indkøbsordren, sammenlignes på siden Sammenlign gebyrværdier – Faktura: som vist i følgende tabel. Hvis den tilladte tolerance for tillægskoden er 25 %, anses afvigelsesprocenten på 99.999.999.999,99 for licenstillægskoden for at være en matchningafvigelse.

> [!NOTE] 
> En afvigelsesprocent på 99.999.999.999,99 betyder, at det forventede beløb baseret på indkøbsordren er nul, og det faktiske beløb på fakturaen er en positiv værdi. 

| Status for sammenholdelse af gebyrer | Fakturagebyrkode | Aktuel total beregnet værdi | Forventet total beregnet værdi | Afvigelsesbeløb | Afvigelsespct. | Toleranceprocent |
|----------------------|----------------------|-------------------------------|---------------------------------|-----------------|---------------------|----------------------|
| Mislykkedes               | Kørekort              | 25                            | 0                               | 25              | 99.999.999.999,99 %  | 25 %                  |
| Bestået               | Fragt              | 200                           | 200                             | 0               | 0 %                  | 25 %                  |
| Mislykkedes               | Fremskynd             | 4                             | 2                               | 2               | 100 %                | 25 %                  |

Sammenholdelse af gebyrer styres for den juridiske enhed af knappen Sammenhold gebyrer på siden Kreditorparametre. Du kan konfigurere procenter for afvigelsestolerance for gebyrer på siden Gebyrtolerancer.

> [!NOTE]
> Sammenholdelse af tillæg udføres kun på gebyrkoder, hvor knappen Sammenlign værdier på indkøbsordre og faktura er valgt på siden Gebyrkode.

## <a name="related-functionality"></a>Relaterede funktioner
Kreditorfakturaer er ofte baseret på produktkvitteringer, der repræsenterer de faktiske forsendelser i stedet for indkøbsordrer. Somme tider stemmer de fakturerede beløb ikke overens med beløbene på indkøbsordren, og somme tider stemmer de afsendte antal ikke overens med de fakturerede antal. Du kan styre disse oplysninger på følgende måder:
-   Opret en kreditorfaktura baseret på produktkvitteringer. Produktkvitteringer foreslås automatisk til fakturaer, og du kan vælge, hvilke produktkvitteringer du vil bruge. Du kan også vælge specifikke linjeelementer fra produktkvitteringer fra flere indkøbsordrer, hvis det er nødvendigt.
-   Få vist og godkende forskelle i antal mellem det fakturerede antal på fakturaen og det modtagne antal på produktkvitteringen. Hvis der er en forskel, kan du gemme fakturaen og senere sammenholde den med en anden produktkvittering eller ændre det fakturerede antal, så det svarer til det modtagne antal.
-   Angive fakturabeløb, der ikke var medtaget på den oprindelige indkøbsordre, så fakturaoplysningerne stemmer overens med den faktura, du har modtaget fra kreditoren. Du kan også sammenligne tillæggene for indkøbsordrer med tillæggene for fakturaer. Hvis det er nødvendigt, kan du føje tillæg til fakturaer og fordele dem til fakturalinjer.
-   Få vist og godkende uoverensstemmelser mellem nettoenhedsprisen på fakturaen og nettoenhedsprisen på indkøbsordren. Du kan konfigurere pristoleranceprocenter for juridiske enheder, leverandører og varer. Hvis prisen på en kreditorfakturalinje ikke ligger inden for den acceptable pristolerance, kan du gemme fakturaen, indtil den godkendes til bogføring, eller indtil du modtager en korrektion fra kreditoren.

Yderligere oplysninger finder du i [Trevejs-sammenholdelsespolitikker](three-way-matching-policies.md) og [Konfigurere validering af sammenholdelse af kreditorfakturaer](tasks/set-up-accounts-payable-invoice-matching-validation.md). 




