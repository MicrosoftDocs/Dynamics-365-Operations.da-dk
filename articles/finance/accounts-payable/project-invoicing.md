---
title: Projektfakturering
description: Dette emne indeholder en oversigt over projektfakturering for tids- og materialeprojekter og fastprisprojekter. Det omfatter oplysninger om fakturaforslag (foreløbig fakturaer), fakturastyring, acontofakturering, kreditorfakturering og kreditnotaer.
author: TaylorVH
manager: AnnBe
ms.date: 07/10/2020
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
ms.search.validFrom: 2020-07-06
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: eab7523296996709dfe7407c582e61e28b7d4f23
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/03/2020
ms.locfileid: "3651586"
---
# <a name="project-invoicing"></a>Projektfakturering

[!include [banner](../includes/banner.md)]

Dette emne indeholder en oversigt over projektfakturering for tids- og materialeprojekter og fastprisprojekter. Det omfatter oplysninger om fakturaforslag (foreløbig fakturaer), fakturastyring, acontofakturering, kreditorfakturering og kreditnotaer.

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

Du kan oprette fakturaforslag ved manuelt at vælge en transaktion på en liste over tilgængelige transaktioner for et bestemt projekt. Du kan også konfigurere faktureringsregler, der angiver, hvornår der automatisk skal oprettes et fakturaforslag. Du kan f.eks. oprette en faktureringsregel for at oprette et fakturaforslag, når der er udført 25 %, 50 %, 75 % og 100 % af arbejdet på et projekt. 

Du kan oprette fakturaforslag til følgende posteringer:

-   Timer, udgifter og andre projektposteringer
-   Beløb, der er tilbageholdt af kunder på tidligere projektfakturaer
-   Kreditnotaer
-   Beløb, som en kunde betaler til dig, før et projekt startes

> [!NOTE]
> Funktionen **Aktivér sortering efter ressource under oprettelse af projektfakturaforslag** gør det muligt for projektbogholderen at sortere de projekttransaktioner, der er tilgængelige for fakturering af ressourcen, når der oprettes et nyt projektfakturaforslag. Det gitter, der viser de tilgængelige projekttransaktioner, vil have separate felter for **Ressource-id** og **Ressource**. Du kan bruge disse felter til at filtrere og sortere efter ressourcenavnet. Denne funktion er som standard slået fra. Den kan aktiveres ved hjælp af **Funktionsstyring**-siden (**Arbejdsområder > Funktionsstyring**). Kontakt systemadministratoren for at få hjælp til at aktivere denne funktion.

Du kan oprette gebyrposteringer i et fakturaforslag. Du kan også ændre salgsprisen på posteringer i forhold til timer, udgifter, varer og gebyrer. Når du bogfører et fakturaforslag, føjes de opdaterede priser og posteringer til projektrapporter og posteringsoversigten. 

Hvis du vil oprette flere debitorfakturaer for et projekt, skal du oprette et fakturaforslag for hver faktura. Du kan f.eks. oprette fakturaer baseret på posteringstypen. Hvis du vil angive timer på én debitorfaktura og varer på en anden, skal du oprette separate fakturaforslag for timeposteringer og gebyrposteringer. 

Hvis et projekt har mere end én finansieringskilde, kan du oprette et separat fakturaforslag for hver finansieringskilde. På siden **Fordeling af finansieringsregler** kan du angive procentdelen af posteringsbeløbet, der skal fordeles til hver finansieringskilde, og kilden, der skal bogføres afrundingsforskelle til.

### <a name="creating-customer-invoices-from-invoice-proposals"></a>Oprette debitorfakturaer ud fra fakturaforslag

Når du opretter og bogfører et fakturaforslag, oprettes der automatisk en debitorfaktura for de posteringer, der er inkluderet i fakturaforslaget. 

Inden du bogfører et fakturaforslag, kan du tilføje eller slette posteringer i det. Du kan f.eks. fjerne udgiftsposteringer, der er bogført til et projekt, men kan ikke faktureres til kunden. 

Hvis din organisation kræver, at fakturaforslag gennemgås, før de bogføres, skal det muligvis godkendes via arbejdsprocessen "Gennemse projektfakturaforslag", før det bliver bogført.

### <a name="view-grant-information-on-project-invoice-list-pages"></a>Se tilskudsoplysninger på sider med projektfakturalister

Brugere af den offentlige sektor kan føje **Tilskuds-id** og **Tilskudsnavn** til listesiderne **Projektfakturaforslag** og **Projektfakturaer**. Disse kolonner er aktiveret ved hjælp af funktionen **Tilføj tilskudsoplysninger på projektfakturalistesider**. Denne funktion er som standard deaktiveret og kan aktiveres i **Arbejdsområder > Administration af funktioner**. Kontakt systemadministratoren for at få hjælp til at aktivere denne funktion.

## <a name="on-account-invoicing"></a>Acontofakturering
Det beløb, du angiver for et projekt på en acontofaktura for et projekt, er baseret på timingen, færdiggørelsesgraden og andre faktureringsbetingelser, der er angivet i den relaterede projektkontrakt. Beløbet beregnes ikke ud fra timer, varer, udgifter eller gebyrer, der er bogført til projektet. 

Du skal oprette en aconto-transaktion for et tids- og materialeprojekt eller et fastprisprojekt, før du kan føje den pågældende aconto-transaktion til en projektfaktura. Angiv det beløb, der skal faktureres en debitor, på acontotransaktionen. Hvis du vil oprette en projektfaktura på beløbet, skal du oprette en foreløbig faktura (fakturaforslag). Vælg acontotransaktionen i fakturaforslaget. Du kan gennemse acontooplysningerne i fakturaforslaget, før du opretter en projektfaktura til det. 

### <a name="fixed-price-projects"></a>Fastprisprojekter
Når det gælder fastprisprojekter, er acontotransaktioner baseret på en aftalt milepæl, enhed for levering eller fakturering ud fra, hvor langt man er nået, som er angivet i en projektkontrakt. Der oprettes én linje for hver betaling, der skal modtages fra projektets debitor. Ingen fradrag er påkrævet.

### <a name="time-and-material-projects"></a>Tids- og materialeprojekter

Når det gælder tids- og materialeprojekter, kan du fakturere en debitor eller en anden finansieringskilde for et forudbetalingsbeløb ved hjælp af et acontofakturaforslag. Angiv aconto-transaktioner som en linje. Du kan også vælge at angive yderligere linjer som fradrag for at opveje eventuelle forudbetalinger, som debitoren allerede har foretaget. Hvis du vil oprette linjer til fradrag, skal du angive et minustegn foran beløbet.

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
Når du bestiller en vare fra en leverandør og tildeler varen til et projekt, bestemmer den linjeegenskab, du vælger for indkøbsordrelinjen til den pågældende vare, om den indkøbte vare faktureres til en kunde. Hvis du konfigurerer standardegenskaberne for linjer, vises de for varen på indkøbsordrelinjen (**Linjeoplysninger > Projekt Linjeegenskabsbeløb**). Der er to måder at ændre linjeegenskaben på:

-   Fakturer projektets kunde for varen. Gør det ved at angive linjeegenskaben for varen til en fakturerbar værdi på indkøbsordren, og fakturer derefter kunden ved hjælp af den korrekte projektfaktureringsmetode.
-   Fakturer ikke projektets kunde for varen. Hvis du vil gøre dette, skal du ikke vælge linjeegenskaben **Fakturerbar** på indkøbsordrelinjen for varen. Du kan derefter fakturere indkøbsordren, uden at du behøver foretage dig yderligere.

> [!NOTE] 
> Frigivne tilbageholdelseslinjer kan ikke faktureres som standard. Det betyder, at muligheden for at oprette et fakturaforslag til den frigivne tilbageholdelse ikke er aktiveret.

## <a name="credit-notes"></a>Kreditnotaer
Når et beløb i en debitorfaktura har en negativ værdi, klassificeres fakturaen som en kreditnota. Når dokumentet udskrives, har det titlen "Kreditnota". 

Når du opretter en kreditnota for at kreditere et beløb, der tidligere er faktureret, skal du først vælge det fakturabeløb, der skal krediteres. Derefter skal du oprette en kreditnota ved at følge den samme procedure som ved oprettelse af en almindelig debitorfaktura. Du skal vælge de transaktioner, der tidligere er bogført på en debitorfaktura, og derefter oprette og bogføre et kreditnotaforslag. 

Det samme dokument kan medtage posteringer, der er valgt til kreditering, kreditposteringer og posteringer, der er blevet bogført. Dokumentet klassificeres enten som en faktura eller en kreditnota, afhængigt af om totalbeløbet er positivt eller negativt. 

Hvis du vil kreditere et kreditnotabeløb, skal du først vælge det fakturabeløb, der skal krediteres, og derefter oprette en kreditnota. Du opretter en kreditnota ved at følge den samme procedure som ved oprettelse af en debitorfaktura. 

Du kan oprette en faktura, der har et negativt beløb, som bliver en faktura, der klassificeres som en kreditnota. Hvis du vil oprette og udskrive en kreditnota, skal du vælge de transaktioner, der tidligere er bogført for en debitorfaktura, og derefter redigere transaktionerne. Medmindre den primære adresse på en juridisk enhed er i Tyskland, er titlen på fakturaen "Rettelsesfaktura".



