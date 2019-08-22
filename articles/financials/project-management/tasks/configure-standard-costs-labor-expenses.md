---
title: Konfigurere standardomkostninger for arbejdskraft og udgifter
description: Denne procedure viser, hvordan du konfigurerer standardomkostninger for arbejdskraft og udgifter for et projekt.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b76956e9b1ce1a1e977aaa7c4974e73754e0d261
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845877"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Konfigurere standardomkostninger for arbejdskraft og udgifter

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du konfigurerer standardomkostninger for arbejdskraft og udgifter for et projekt. Denne opgave bruger USSI-datasættet.

1. Gå til Projektstyring og regnskab > Opsætning > Priser > Salgspris (time).
2. Klik på Ny.
3. Angiv en dato i feltet Ikrafttrædelsesdato.
4. Angiv et tal i feltet Kostpris.
    * Du kan definere en standardkostpris for projektkategorien, eller du kan definere en kostpris pr. arbejdernummer, projektnummer, kategori, dato eller en kombination af disse. Den kostpris, der anvendes, vil være den mest detaljerede kostpris.  
5. Klik på Gem.
6. Luk siden.
7. Gå til Projektstyring og regnskab > Opsætning > Priser > Salgspris (time).
8. Klik på Ny.
9. Angiv en dato i feltet Ikrafttrædelsesdato.
10. Vælg en indstilling i feltet Gyldig.
11. Angiv et tal i feltet Prissætning.
    * Du kan definere en standardsalgspris for timeposteringer eller for en projektkategori. Du kan også definere salgspriser pr. arbejdernummer, projektnummer, kategori, posteringsdato eller en kombination af disse. Den faktiske salgspris, som anvendes, når en arbejder angiver en postering i timekladden, er salgsprisen med den højeste detaljeringsgrad. Hvis der f.eks. både er oprettet en generel salgspris og en arbejderspecifik salgspris, bruges den arbejderspecifikke salgspris.  
12. Klik på Gem.
13. Luk siden.
14. Gå til Projektstyring og regnskab > Opsætning > Priser > Kostpris (udgift).
15. Klik på Ny.
16. Angiv en dato i feltet Ikrafttrædelsesdato.
17. Angiv et tal i feltet Kostpris.
    * Der kan udfyldes flere felter, men dette er det minimum, der er nødvendigt for at gemme posten.  
18. Klik på Gem.
19. Luk siden.
20. Gå til Projektstyring og regnskab > Opsætning > Priser > Salgspris (udgift).
21. Klik på Ny.
22. Angiv en dato i feltet Ikrafttrædelsesdato.
23. Vælg en indstilling i feltet Gyldig.
24. Angiv et tal i feltet Prissætning.
    * Den faktiske salgspris, som anvendes, når en medarbejder angiver posteringer i en udgiftskladde, er den salgspris, der har det højeste detaljeringsniveau. Hvis der f.eks. både er oprettet en generel salgspris og en arbejderspecifik salgspris, anvendes den arbejderspecifikke salgspris.  
25. Klik på Gem.

