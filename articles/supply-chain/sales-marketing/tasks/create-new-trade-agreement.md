---
title: Oprette en ny samhandelsaftale
description: Denne fremgangsmåde viser, hvordan du kan oprette en samhandelsaftale, hvor du registrerer en ny produktsalgspris, som du har aftalt med en bestemt debitor.
author: omulvad
manager: AnnBe
ms.date: 11/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e132cd20437b7929e81fcaa123d70bb57fb320c8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "323496"
---
# <a name="create-a-new-trade-agreement"></a>Oprette en ny samhandelsaftale

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du kan oprette en samhandelsaftale, hvor du registrerer en ny produktsalgspris, som du har aftalt med en bestemt debitor. Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data. Hvis du bruger dine egne data, før du starter denne vejledning, skal du sikre, at der findes et navn på en Samhandelskladde, hvor standardrelationen er indstillet til "Pris (salg)".


## <a name="create-and-post-a-new-trade-agreement-journal"></a>Opret og bogfør en ny samhandelsaftalekladde
1. Gå til Salg og marketing > Priser og rabatter > Samhandelskladder.
2. Klik på Ny.
3. Klik på rullelisten i feltet Navn for at åbne opslaget.
4. Find og vælg den ønskede post på listen.
5. Klik op linket i den valgte række på listen.
6. Klik på Linjer.
7. Vælg "Tabel" i feltet Kontokode.
    * I dette eksempel skal du opdatere prisen for en bestemt debitor, hvilket betyder, at du skal vælge Tabel. Hvis du har opdateret produktets listepris, skal du markere Alle, så den nye pris gælder alle debitorer. Hvis du differentierer priser mellem forskellige debitorsegmenter, skal du vælge Gruppe. Hvis du vil vælge Gruppe, skal du have indstillet Debitorprisgrupper.  
8. Klik på rullelisten i feltet Kontovalg for at åbne opslaget.
9. Find og vælg den ønskede post på listen.
10. Vælg "Tabel" i feltet Varekode.
    * Når du indtaster en samhandelsaftale af typen "Pris (salg)", skal du kun vælge "Tabel" i feltet Varekode. Det skyldes, at en pris er en absolut værdi og ikke kan være ens for alle produkter eller gruppe af produkter.  
11. Klik på rullelisten i feltet Varerelation for at åbne opslaget.
12. Vælg det produkt, der inkluderes i dokumentet, på listen.
    * Noter hvilket produkt, du har valgt.  
13. Klik op linket i den valgte række på listen.
14. Indtast en minimummængde i feltet Fra.
    * Hvis debitoren skal bestille et minimumsantal, før de kan blive kvalificeret til den nye pris, skal du angive antallet her.  
    * Angiv en værdi i feltet Til for at angive det maksimale antal, over hvilken aftalens pris ikke er gyldig. Hvis du tilbyder priser og rabatter, der er baseret på flere mængdereduktioner, skal du angive hver mængdekategori som et par med min. og maks. mængde i felterne henholdsvis "Fra" og "Til".  
15. Indtast en pris i feltet Beløb i valuta.
16. Indtast en dato, hvorfra denne aftale vil være gyldig, i feltet Fra dato.
17. Klik på Gem.
18. Klik på Valider.
19. Klik på Valider valgte linjer.
20. Klik på OK.
21. Klik på Bogfør.
22. Klik på OK.

## <a name="view-trade-agreements-for-a-product"></a>Få vist samhandelsaftaler for et produkt
1. Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.
2. På listen skal du finde og vælge produktet, hvis pris du netop har opdateret.
3. Klik på Sælg i handlingsruden.
4. Klik på Vis samhandelsaftaler.
    * Gennemse oplysningerne om samhandelsaftalens pris, som du lige har oprettet.    
5. Luk siden.

## <a name="additional-resources"></a>Yderligere ressourcer
### <a name="community-blogs"></a>Fællesskabsblogge
- [Salgspriser i Dynamics 365 for Finance and Operations](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)
