---
title: Oprette veksler
description: I dette emne beskrives trinnene til oprettelse af veksler.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: abruer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ce2142d946085d8bfc577accf1bb31a89ea29156
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bills-of-exchange"></a>Oprette veksler

I dette emne beskrives trinnene til oprettelse af veksler.

En veksel er en skriftlig eller elektronisk anvisning fra en kunde, der angiver, at en anden part, normalt en bank, skal betale et angivet beløb til firmaet. Når du bruger en veksel som betaling for en salgsordrefaktura eller fritekstfaktura, krediterer du debitorkontoen. Denne kreditering sikres af vekslen, indtil kunden betaler vekslen til banken. Du udligner som regel fakturaen med vekslen på forfaldsdatoen. Når du modtager besked fra banken om, at vekslen er accepteret, kan du lukke vekslen. Du kan udstede en veksel via banken på et af følgende tidspunkter:

-   På forfaldsdatoen. Denne metode kaldes remitter til rykker.
-   Før forfaldsdatoen, typisk på den rabatdato, der er angivet i de betalingsbetingelser, der er konfigureret for kunden. Når du bogfører posteringen, bogføres rabatbeløbet på en udgiftskonto. Det resterende beløb er en gæld til dig, indtil banken modtager betaling fra debitoren. Denne metode kaldes remitter til rabat.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Angive posteringsprofiler for veksler
Brug af **debitorposteringsprofiler** side til at konfigurere posteringsprofiler, der kan bruges med veksler, protestere mod veksler, remitteringer til rykker og remitteringer til rabat. I den **samlekonto** skal du vælge det tilfælde sumkontoen vekselbeløb skal bogføres på. Denne konto debiteres eller krediteres afhængigt af veksel transaktion:
-   Veksler debiteres denne konto, når der bogføres en veksel, og den krediteres, når der bogføres en remittering til rabat eller en remittering til rykker.
-   I forbindelse med protesterede veksler debiteres denne konto, når der bogføres en protesteret veksel.
-   I forbindelse med remitteringer til rykker debiteres denne konto, når der bogføres en remittering til rykker.
-   I forbindelse med remitteringer til rabat debiteres denne konto, når der bogføres en remittering til rabat.

I den **udligne konto** skal du vælge den kontantkonto vekselbeløb skal bogføres på. Denne konto debiteres, når en veksel udlignes. I den **moms forudbetalinger** skal du vælge den samlekonto, du vil bogføre momsbeløb på, når veksler bruges til forudbetalinger. I den **finanskonto til rabatpassiver**, skal du vælge den konto, du vil bogføre rabatbeløbet for remitteringer til rabat til. Denne konto krediteres, når der bogføres en remittering til rabat.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Angive debitorparametre for veksler
På den **Accounts receivable parameters** side, standard posteringsprofiler for veksler, der er angivet på den **Finans og moms** tab. Nummerserier, der er defineret på den **nummerserier** tab.
Angive kladdenavne for veksler
------------------------------------------

På den **kladder navne** skal du oprette mindst fem kladdenavne, der skal bruges til veksler. Her er kladdetyper:
-   **Tegning af veksler** – Opret et kladdenavn til Udsted veksel kladden.
-   **Debitorprotest af veksel** – Opret et kladdenavn i kladden til Protest af veksler.
-   **Debitorgenudstedelse af veksel** – Opret et kladdenavn for den genudstedelse af veksler.
-   **Kunden bankremittering** – Opret et kladdenavn til remitteringskladde.
-   **Udligning af veksler** – Opret et kladdenavn i kladden til udligning af veksler.

Angiv oplysninger om vekslen på siden kladden bilag for hver veksler de **veksel** under fanen. Når kladdelinjerne vekslen er bogført, kan du se dem på den **veksel journal undersøgelse** side og den **veksler statistik** side.
Angive betalingsmåder for veksler
-----------------------------------------------

På den **betalingsmåder** side, der er angivet mindst én betalingsmåde for veksler. Hvis du gør forretning med mere end én bank, skal du konfigurere en betalingsmåde, der svarer til remitteringsformat, som de enkelte banker kræver for veksler.
Angive betalingsgebyrer for veksler
-----------------------------------------

Et betalingsgebyr er et tillæg, der er tilknyttet processen til opkrævning af betalinger fra kunder. Flere opsætning af betalingsgebyr linjer kan være tilknyttet de enkelte betalingsgebyrer. Du kan bruge opsætningslinjer til at styre, hvordan standardbeløb for betalingsgebyrer beregnes. Du kan f.eks. oprette opsætningslinjer for betalingsmåder, betalingsspecifikationer, valutaer og tidsperioder. Du kan også oprette opsætningslinjer for en procentdel eller et beløb baseret på dagsintervaller. For eksempel kan du angive en renteprocent, der er baseret på længden af tid, der er forfaldne til betaling. Hvis banken opkræver forskellige gebyrer for forskellige remitteringstyper, f.eks. **samling** eller **rabat**, oprette en separat betaling gebyr linje for hver remitteringstype.
Konfigurere remitteringsgebyrer for bankremitteringsfiler
------------------------------------------------

På den **bankkonti** side, du kan konfigurere remitteringsgebyrer, som en bank opkræver for de enkelte remitteringsfiler, der oprettes. Remitteringsgebyrerne bogføres, når remitteringen er bekræftet, og de realiserede gebyrbeløb er kendt. Remitteringsgebyrerne er forskellige fra betalingsgebyrer, som indsamles fra debitorer og knyttet til kladdelinjer.
Angive dokumentlayout for veksler
---------------------------------------------

På den **bankkonti** skal du klikke på **angive**, og Angiv det dokumentlayout, der kræves for hver bankkonto, du opretter udskrevne veksler dokumenter til.
Angive debitorer for veksler
--------------------------------------

På den **kunder** side, for hver debitor, der har accepteret at betale med en veksel, kan du oprette en standardbetalingsmåde for veksler på de **betaling standarder** tab.




