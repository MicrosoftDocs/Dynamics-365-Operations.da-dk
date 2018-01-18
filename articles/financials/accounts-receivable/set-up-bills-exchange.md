---
title: Oprette veksler
description: I dette emne beskrives trinnene til oprettelse af veksler.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustBillOfExchangeJour
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4dfc6cc2fcbca18f3dde833917ae68a5f254643b
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-bills-of-exchange"></a>Oprette veksler

[!include[banner](../includes/banner.md)]


I dette emne beskrives trinnene til oprettelse af veksler.

En veksel er en skriftlig eller elektronisk anvisning fra en kunde, der angiver, at en anden part, normalt en bank, skal betale et angivet beløb til firmaet. Når du bruger en veksel som betaling for en salgsordrefaktura eller fritekstfaktura, krediterer du debitorkontoen. Denne kreditering sikres af vekslen, indtil kunden betaler vekslen til banken. Du udligner som regel fakturaen med vekslen på forfaldsdatoen. Når du modtager besked fra banken om, at vekslen er accepteret, kan du lukke vekslen. Du kan udstede en veksel via banken på et af følgende tidspunkter:

-   På forfaldsdatoen. Denne metode kaldes remitter til rykker.
-   Før forfaldsdatoen og som regel på den rabatdato, der er angivet i de betalingsbetingelser, der er oprettet for kunden. Når du bogfører posteringen, bogføres rabatbeløbet på en udgiftskonto. Det resterende beløb er en gæld til dig, indtil banken modtager betaling fra debitoren. Denne metode kaldes remitter til rabat.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Angive posteringsprofiler for veksler
Brug siden **Debitor, posteringsprofiler** til at oprette posteringsprofiler, du kan bruge sammen med veksler, til at protestere mod veksler, remitteringer til rykker og remitteringer til rabat: Vælg den samlekonto, du vil bogføre vekselbeløb på, i feltet **Samlekonto**. Denne konto debiteres eller krediteres, afhængigt af typen af vekselposteringen:
-   I forbindelse med veksler debiteres denne konto, når der bogføres en veksel, og den krediteres, når der bogføres en remittering til rabat eller en remittering til rykker.
-   I forbindelse med protesterede veksler debiteres denne konto, når der bogføres en protesteret veksel.
-   I forbindelse med remitteringer til rykker debiteres denne konto, når der bogføres en remittering til rykker.
-   I forbindelse med remitteringer til rabat debiteres denne konto, når der bogføres en remittering til rabat.

Vælg den afregningskonto, du vil bogføre vekselbeløb på, i feltet **Afregn konto**. Denne konto debiteres, når en veksel udlignes. Vælg i feltet **Momsforudbetalinger** den samlekonto, du vil bogføre momsbeløb på, når veksler bruges til forudbetalinger. Vælg den konto, som du vil bogføre rabatbeløbet for remitteringer til rabat på, i feltet **Passiver for rabatkonto**. Denne konto krediteres, når der bogføres en remittering til rabat.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Angiv debitorparametre for veksler
På siden **Debitorparametre** er standardposteringsprofilerne for veksler angivet under fanen **Finans og moms**. Nummerserier er defineret under fanen **Nummerserier**. Angive kladdenavne for veksler
------------------------------------------

Opret mindst fem kladdenavne, der kan bruges til veksler på siden **Kladdenavne**. Her er kladdetyperne:
-   **Debitorudstedelse af veksel** – Opret et kladdenavn til kladden til udstedelse af veksel.
-   **Debitorprotest af veksel** – Opret et kladdenavn til kladden til protest af veksel.
-   **Debitorgenudstedelse af veksel** – Opret et kladdenavn til kladden til genudstedelse af veksel.
-   **Debitorbankremittering** – Opret et kladdenavn til remitteringskladden.
-   **Debitorudligning af veksel** – Opret et kladdenavn til kladden til udligning af veksel.

På siden Kladdebilag for hver vekselkladde, kan du angive oplysninger om vekslen under fanen **Veksel**. Når vekselkladdelinjerne er bogført, kan du se dem på siden **Forespørgsel på vekselkladde** og siden **Vekselstatistik**.
Angive betalingsmåder for veksler
-----------------------------------------------

På siden **Betalingsmåder** side skal du angive mindst én betalingsmåde for veksler. Hvis du gør forretninger med mere end én bank, skal du konfigurere en betalingsmåde, der svarer til det remitteringsformat, som hver enkelt bank kræver for veksler.
Angive betalingsgebyrer for veksler
-----------------------------------------

Et betalingsgebyr er et tillæg, der er tilknyttet processen til opkrævning af betalinger fra kunder. Der kan knyttes flere opsætningslinjer for betalingsgebyrer til hvert betalingsgebyr. Du kan bruge opsætningslinjer til at styre, hvordan standardbeløb for betalingsgebyrer beregnes. Du kan f.eks. oprette opsætningslinjer for betalingsmåder, betalingsspecifikationer, valutaer og tidsperioder. Du kan også oprette opsætningslinjer for en procentdel eller et beløb baseret på dagsintervaller. Du kan f.eks. angive en renteprocent, der er baseret på, hvor længe en betaling har været forfalden til betaling. Hvis banken opkræver forskellige gebyrer for forskellige remitteringstyper, som f.eks. **Inkasso** eller **Rabat**, skal du oprette en separat betalingsgebyrlinje for hver remitteringstype.
Konfigurere remitteringsgebyrer for bankremitteringsfiler
------------------------------------------------

På siden **Bankkonti** kan du konfigurere remitteringsgebyrer, der opkræves af en bank for de enkelte remitteringsfiler, der oprettes. Remitteringsgebyrerne bogføres, når remitteringen er bekræftet, og de realiserede gebyrbeløb er kendt. Remitteringsgebyrer er forskellige fra betalingsgebyrer, som indsamles fra debitorer og knyttes til kladdelinjer.
Angive dokumentlayout for veksler
---------------------------------------------

På siden **Bankkonti** skal du klikke på **Bankkonti** og angive det dokumentlayout, der kræves ved de enkelte bankkonti, du opretter udskrevne vekseldokumenter for.
Angive debitorer for veksler
--------------------------------------

På siden **Debitorer** kan du for alle debitorer, der har accepteret at betale med en veksel, angive en standardbetalingsmåde for veksler under fanen **Betalingsstandarder**.






