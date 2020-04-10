---
title: Konfigurere standardomkostninger for arbejdskraft og udgifter
description: Dette emne forklarer, hvordan du konfigurerer standardomkostninger for arbejdskraft og udgifter for et projekt.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
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
ms.openlocfilehash: 51bbe52d70bae11cb0c95e9544f951f0fcc605f5
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140087"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Konfigurere standardomkostninger for arbejdskraft og udgifter

[!include [banner](../../includes/banner.md)]

Dette emne forklarer, hvordan du konfigurerer standardomkostninger for arbejdskraft og udgifter for et projekt. Denne opgave bruger USSI-datasættet.

1. Gå i navigationsruden til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Kostpris (time)**.
2. Vælg **Ny**.
3. Angiv en dato i feltet **Ikrafttrædelsesdato**.
4. Angiv et tal i feltet **Kostpris**. Du kan definere en standardkostpris for projektkategorien, eller du kan definere en kostpris pr. arbejdernummer, projektnummer, kategori, dato eller en kombination af disse. Den kostpris, der anvendes, vil være den mest detaljerede kostpris.  
5. Vælg **Gem**.
6. Gå i navigationsruden til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Salgspris (time)**.
7. Vælg **Ny**.
8. Angiv en dato i feltet **Ikrafttrædelsesdato**.
9. Vælg en indstilling i feltet **Gælder for**.
10. Angiv et tal i feltet **Prissætning**. Du kan definere en standardsalgspris for timeposteringer eller for en projektkategori. Du kan også definere salgspriser pr. arbejdernummer, projektnummer, kategori, posteringsdato eller en kombination af disse. Den faktiske salgspris, som anvendes, når en arbejder angiver en postering i timekladden, er salgsprisen med den højeste detaljeringsgrad. Hvis der f.eks. både er oprettet en generel salgspris og en arbejderspecifik salgspris, bruges den arbejderspecifikke salgspris.  
11. Vælg **Gem**.
12. Luk siden.
13. Gå i navigationsruden til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Kostpris (udgift)**.
14. Vælg **Ny**.
15. Angiv en dato i feltet **Ikrafttrædelsesdato**.
16. Angiv et tal i feltet **Kostpris**. Der kan udfyldes flere felter, men dette er det minimum, der er nødvendigt for at gemme posten.  
17. Vælg **Gem**.
18. Gå i navigationsruden til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Salgspris (udgift)**.
19. Vælg **Ny**.
20. Angiv en dato i feltet **Ikrafttrædelsesdato**.
21. Vælg en indstilling i feltet **Gælder for**.
22. Angiv et tal i feltet **Prissætning**. Den faktiske salgspris, som anvendes, når en medarbejder angiver posteringer i en udgiftskladde, er den salgspris, der har det højeste detaljeringsniveau. Hvis der f.eks. både er oprettet en generel salgspris og en arbejderspecifik salgspris, anvendes den arbejderspecifikke salgspris.  
23. Vælg **Gem**.

