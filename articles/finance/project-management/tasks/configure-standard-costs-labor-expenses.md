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
ms.openlocfilehash: 60ab8eb94d4a8a0fb2c1e732ec7b25bfd5e7611e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185399"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Konfigurere standardomkostninger for arbejdskraft og udgifter

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

