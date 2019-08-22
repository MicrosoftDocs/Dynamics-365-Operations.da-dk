---
title: Projektfakturering
description: Denne artikel indeholder en oversigt over projektfakturering for tids- og materialeprojekter og fastprisprojekter. Det omfatter oplysninger om fakturaforslag (foreløbig fakturaer), fakturastyring, acontofakturering, kreditorfakturering og kreditnotaer.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjInvoiceCashFlow, ProjInvoiceControl, ProjInvoiceListPage, ProjInvoiceProposalDetail, ProjInvoiceProposalListPage
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23111
ms.assetid: 1812d6f2-8b34-4258-8f5f-dcf12281547f
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3d91f6b1ccc3254e2c04d24c5f9bf2014c64e50
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837222"
---
# <a name="project-invoicing"></a>Projektfakturering

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over projektfakturering for tids- og materialeprojekter og fastprisprojekter. Det omfatter oplysninger om fakturaforslag (foreløbig fakturaer), fakturastyring, acontofakturering, kreditorfakturering og kreditnotaer.

Projekttypen bestemmer, hvilken faktureringsproces der anvendes. Det er kun de to eksterne projekttyper, Tid og materialer og Fast pris, der kan faktureres. Tids- og materialeprojekter og fastprisprojekter er altid knyttet til en projektkontrakt.

-   **Fastprisprojekter** – Beløbet på debitorfakturaen er baseret på faktureringsplaner. Fakturering sker via en acontoopsætning, der også kaldes en faktureringsplan. Fastprisprojekter kan faktureres pr. projekt eller pr. projektkontrakt.
-   **Tids- og materialeprojekter** – Beløbet på debitorfakturaen er baseret på transaktionslinjer, der er angivet for projekter. Transaktioner kan faktureres pr. projekt eller pr. projektkontrakt.

Der er tre måder at tilknytte tids- og materialeprojekter og fastprisprojekter til fakturaprojekterne på:

-   **Acontofakturering** – Tids- og materialeprojekter og fastprisprojekter kan faktureres aconto. Der kræves to typer acontoopsætninger, en til hver projekttype.
-   **Fakturering i det periodiske område** – Via de periodiske funktioner kan posteringer faktureres på tværs af projekter. De periodiske funktioner giver et overblik over de posteringer, der skal faktureres.
-   **Brug af kreditnotaer ved fakturering** – Der kan oprettes en kreditnota til både tids- og materialeprojekter og til fastprisprojekter.

## <a name="invoice-proposals"></a>Fakturaforslag
Før du opretter en debitorfaktura for et projekt, kan du oprette en foreløbig faktura eller et fakturaforslag. Du kan vælge projektposteringer, der skal medtages i en projektfaktura, i et fakturaforslag. Du kan derefter se fakturaoplysningerne, før du bogfører projektfakturaen og sender den til kunden eller anden finansieringskilde.

### <a name="creating-invoice-proposals"></a>Danner fakturaforslag

Du kan oprette fakturaforslag ved manuelt at vælge på en liste over posteringer for et bestemt projekt. Du kan også konfigurere faktureringsregler, der angiver, hvornår der automatisk skal oprettes et fakturaforslag. Du kan f.eks. oprette en faktureringsregel for at oprette et fakturaforslag, når der er udført 25 %, 50%, 75% og 100 % af arbejdet på et projekt. 

Du kan oprette fakturaforslag til følgende posteringer:

-   Timer, udgifter og andre projektposteringer
-   Beløb, der er tilbageholdt af kunder på tidligere projektfakturaer
-   Kreditnotaer
-   Beløb, som en kunde betaler til dig, før et projekt startes

Du kan oprette gebyrposteringer i et fakturaforslag. Du kan også ændre salgsprisen på posteringer i forhold til timer, udgifter, varer og gebyrer. Når du bogfører et fakturaforslag, føjes de opdaterede priser og posteringer til projektrapporter og posteringsoversigten. 

Hvis du vil oprette flere debitorfakturaer for et projekt, skal du oprette et fakturaforslag for hver faktura. Du kan f.eks. oprette fakturaer baseret på posteringstypen. Hvis du vil angive timer på én debitorfaktura og varer på en anden, skal du oprette separate fakturaforslag for timeposteringer og gebyrposteringer. 

Hvis et projekt har mere end én finansieringskilde, kan du oprette et separat fakturaforslag for hver finansieringskilde. På siden **Fordeling af finansieringsregler** kan du angive procentdelen af posteringsbeløbet, der skal fordeles til hver finansieringskilde, og kilden, der skal bogføre afrundingsforskelle.

### <a name="creating-customer-invoices-from-invoice-proposals"></a>Oprette debitorfakturaer ud fra fakturaforslag

Når du opretter og bogfører et fakturaforslag, oprettes der automatisk en debitorfaktura for de posteringer, der er inkluderet i fakturaforslaget. 

Inden du bogfører et fakturaforslag, kan du tilføje eller slette posteringer i det. Du kan f.eks. fjerne udgiftsposteringer, der er bogført til et projekt, men som ikke kan faktureres til kunden. 

Hvis organisationen kræver, at fakturaforslag gennemgås, før de bogføres, skal fakturaforslaget muligvis godkendes via arbejdsgangen "Gennemse projektfakturaforslag", før det bliver bogført.

## <a name="on-account-invoicing"></a>Acontofakturering
Det beløb, du angiver for et projekt på en acontofaktura for et projekt, er baseret på timingen, færdiggørelsesgraden og andre faktureringsbetingelser, der er angivet i den relaterede projektkontrakt. Beløbet beregnes ikke ud fra timer, varer, udgifter eller gebyrer, der er bogført til projektet. 

Du skal oprette en acontotransaktion for et tids- og materialeprojekt eller et fastprisprojekt, før du kan føje den pågældende acontotransaktion til en projektfaktura. Angiv det beløb, der skal faktureres en debitor, på acontotransaktionen. Hvis du vil oprette en projektfaktura på beløbet, skal du oprette en foreløbig faktura (fakturaforslag). Vælg acontotransaktionen i fakturaforslaget. Du kan gennemse acontooplysningerne i fakturaforslaget, før du opretter en projektfaktura til det.

### <a name="fixed-price-projects"></a>Fastprisprojekter

Når det gælder fastprisprojekter, er acontotransaktioner baseret på en aftalt milepæl, enhed for levering eller fakturering ud fra, hvor langt man er nået, som er angivet i en projektkontrakt. Der oprettes én linje for hver betaling, der skal modtages fra projektets debitor. Ingen fradrag er påkrævet.

### <a name="time-and-material-projects"></a>Tids- og materialeprojekter

Når det gælder tids- og materialeprojekter, kan du fakturere en debitor eller en anden finansieringskilde for et forudbetalingsbeløb ved hjælp af et acontofakturaforslag. Angiv aconto-transaktioner som en linje. Du kan også vælge at angive yderligere linjer som fradrag for at opveje eventuelle forudbetalinger, som debitoren allerede har foretaget. Hvis du vil oprette linjer til fradrag, skal du angive beløbet med negativt fortegn.

## <a name="invoice-control"></a>Fakturastyring
Du kan bruge fakturastyring til at spore både fakturerede og ikke-fakturerede transaktioner og til at analysere disse transaktioner mod tilbud, så du får en altomfattende oversigt over dine projekter lige fra tilbudsfasen til færdiggørelse. Du kan se, hvilke transaktioner der skal debiteres på et bestemt projekt, og hvilke linjer der er faktureret. Du kan også se de enkelte posteringer og transaktioner, så du kan justere dem, efter at de er bogført.

## <a name="invoicing-fixed-price-projects"></a>Fakturering af fastprisprojekter
Hvis du vil fakturere et fastprisprojekt, skal du definere en faktureringsplan og udføre faktureringsproceduren.

### <a name="billing-schedule"></a>Faktureringsplan

Du kan fakturere fastprisprojekter ud fra en faktureringsplan. Faktureringsplanen defineres som en eller flere milepæle i projektet. Du kan definere en bestemt dato, salgsvaluta, salgspris og aktivitet for hver milepæl. 

Du kan f.eks. konfigurere følgende faktureringsplan:

-   20 procent, når projektkontrakten underskrives
-   30 procent ved første levering
-   15 procent ved anden levering
-   35 procent ved endelig levering

### <a name="invoicing-procedure"></a>Faktureringsprocedure

Når milepælsbetalingerne er klar til at blive faktureret, skal du anvende proceduren til fakturering af acontobeløb.

## <a name="vendor-invoicing"></a>Kreditorfakturering
Når du bestiller en vare fra en leverandør og tildeler varen til et projekt, bestemmer den linjeegenskab, du vælger for indkøbsordrelinjen til den pågældende vare, om den indkøbte vare faktureres til en kunde. Hvis du konfigurerer standardegenskaberne for linjer, vises de for varen på indkøbsordrelinjen (Linjeoplysninger &gt; Projekt &gt; Linjeegenskab). Der er to måder at ændre linjeegenskaben på:

-   Fakturere projektets debitor for varen: Angiv linjeegenskaben for varen til en fakturerbar værdi på indkøbsordren, og fakturer derefter kunden ved hjælp af den korrekte projektfaktureringsmetode.
-   Ikke fakturere projektets debitor for varen: Vælg ikke linjeegenskaben **Fakturerbar** på indkøbsordrelinjen for varen. Du kan derefter fakturere indkøbsordren, uden at du behøver foretage dig yderligere.

## <a name="credit-notes"></a>Kreditnotaer
Når et beløb i en debitorfaktura har en negativ værdi, klassificeres fakturaen som en kreditnota. Når dokumentet udskrives, har det titlen "Kreditnota". 

Når du opretter en kreditnota for at kreditere et beløb, der tidligere er faktureret, skal du først vælge det fakturabeløb, der skal krediteres. Du skal derefter oprette en kreditnota ved at følge den samme procedure, som du ville bruge ved oprettelse af en almindelig debitorfaktura. Du skal med andre ord vælge de posteringer, der tidligere er bogført på en debitorfaktura, og derefter oprette og bogføre et kreditnotaforslag. 

Det samme dokument kan medtage posteringer, der er valgt til kreditering, kreditposteringer og posteringer, der er blevet bogført. Dokumentet klassificeres enten som en faktura eller en kreditnota, afhængigt af om totalbeløbet er positivt eller negativt. 

Hvis du vil kreditere et kreditnotabeløb, skal du først vælge det fakturabeløb, der skal krediteres, og derefter oprette en kreditnota. Du opretter en kreditnota ved at følge den samme procedure som ved oprettelse af en debitorfaktura. 

Du kan oprette en faktura, der har et negativt beløb, som bliver en faktura, der klassificeres som en kreditnota. Hvis du vil oprette og udskrive en kreditnota, skal du vælge de transaktioner, der tidligere er bogført for en debitorfaktura, og derefter redigere transaktionerne. Medmindre den primære adresse på en juridisk enhed er i Tyskland, er titlen på fakturaen "Rettelsesfaktura".



