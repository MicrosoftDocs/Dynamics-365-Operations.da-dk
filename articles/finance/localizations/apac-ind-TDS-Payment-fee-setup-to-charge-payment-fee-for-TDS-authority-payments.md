---
title: Angive betalingsgebyrer til skattemyndighedsbetalinger
description: Dette emne forklarer, hvordan du kan angive de betalingsgebyrer, der opkræves af myndighederne i forbindelse med kildeskat (TDS – Tax Deducted at Source).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 8917abfea73045d57d55d7338a313f414d479b11
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407580"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a>Angive betalingsgebyrer til skattemyndighedsbetalinger

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du kan angive de betalingsgebyrer, der opkræves af myndighederne i forbindelse med kildeskat (TDS – Tax Deducted at Source).

1. Gå til **Kreditor \> Betalingsopsætning \> Betalingsgebyr**.

    [![Siden Betalingsgebyr.](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)

2. Vælg **Ny** for at oprette et betalingsgebyr, og angive de krævede oplysninger.
3. Vælg typen af betalignsgebyr i feltet **Gebyrtype**:

    - **None**
    - **Renter** – Der opkræves renter af forsinkede betalinger til skattemyndighedskreditoren.
    - **Andre** – Der opkræves andre gebyrer for forsinkede betalinger til skattemyndighedskreditoren.

    Hvis du vælger **Renter** eller **Andre**, angives feltet **Gebyr** automatisk til **Finans**.

4. Hvis du har valgt **Renter** eller **Andre** i feltet **Felttype**, skal du vælge den finanskonto i feltet **Hovedkonto**, som renter eller andre gebyrer skal bogføres til.
5. Angiv de øvrige krævede oplysninger.
6. Vælg **Opsætning af betalingsgebyr** i handlingsruden for at åbne siden **Opsætning af betalingsgebyr**, hvor du kan definere betalingsgebyrer for forskellige kombinationer af banker, betalingsmåder, betalingsspecifikationer, valutaer og datointervaller.

    [![Siden Opsætning af betalingsgebyr.](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)

7. Under fanen **Oversigt** i feltet **Grupperinger** kan du angive, hvilke banker du angiver betalingsgebyret for:

    - **Tabel** – Gebyret gælder for en bestemt bankkonto.
    - **Gruppe** – Gebyret gælder for en bestemt bankgruppe.
    - **Alle** – Gebyret er gyldigt for alle bankkonti.

8. Hvis du har valgt **Tabel** eller **Gruppe** i feltet **Grupperinger**, skal du vælge den specifikke bankkonto eller bankgruppe, du konfigurerer betalingsgebyret for, i feltet **Bankrelation**.
9. Vælg den betalingsmåde, der skal bruges til betaling af betalingsgebyret, i feltet **Betalingsmetode**.
10. I feltet **Betalingsspecifikation** skal du vælge eller indtaste den betalingsspecifikationskode, der blev genereret på siden **Betalingsspecifikation**.
    - Betalingsspecifikationen bruges med elektronisk pengeoverførsel som betalingsmåde.
12. Vælg den valuta, der aktiverer gebyret, i feltet **Betalingsvaluta**. Det er kun transaktioner, der bruger den valgte valuta, som kan aktivere gebyret. Hvis dette felt ikke udfyldes, aktiverer alle valutaer gebyret.
13. Vælg beregningsmetoden i feltet **Procent/beløb**. Valgmulighederne er **Beløb**, **Procent** og **Interval**.
14. I feltet **Gebyrbeløb** skal du angive gebyrbeløbet som enten en procentdel af betalingen eller som beløbet for én betaling.
15. Angiv valutakoden for gebyret i feltet **Valuta for gebyr**.
16. Vælg fanen **Generelt** for at få vist eller redigere oplysningerne om den valgte bankkonto.

    [![Fanen Generelt.](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)

16. Angiv det minimale transaktionsbeløb, der aktiverer gebyret, i feltet **Minimum**.
17. Angiv det maksimale transaktionsbeløb, der aktiverer gebyret, i feltet **Maksimum**.
18. Definer et datointerval til beregning af gebyrer i felterne **Fra dato** og **Til dato**.
19. I feltet **Minimumgebyr** skal du angive gebyrbeløbet som enten en procentdel af betalingen eller som beløbet for én betaling.
20. Vælg den momsgruppe, der skal bruges til at beregne moms for gebyrbeløbet, i feltet **Momsgruppe**.
21. Vælg den varemomsgruppe, der skal bruges til at beregne varemoms for gebyrbeløbet, i feltet **Varemomsgruppe**.
22. Vælg fanen **Interval**. 

    [![Fanen Interval.](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)

23. Angiv antallet af dage mellem bogføringsdatoen (diskonteringsdatoen) for betalingen og forfaldsdatoen for egenvekslen i feltet **Dage**.
24. I feltet **Procent/beløb** skal du vælge, om specifikationen er en procent eller et angivet beløb.
25. I feltet **Gebyrbeløb** skal du angive beløbet for gebyret som en procentdel af betalingen eller som beløbet for én betaling.
26. Luk siden **Opsætning af betalingsgebyr**.
27. Luk siden **Betalingsgebyr**.
