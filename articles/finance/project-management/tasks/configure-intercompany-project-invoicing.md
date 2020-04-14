---
title: Konfigurere intern projektfakturering
description: Dette emne viser, hvordan du opsætter projektfakturering mellem to firmaer i organisationen.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31dbae2d37aefe1841fe85cb6caf185c78596e55
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144273"
---
# <a name="configure-intercompany-project-invoicing"></a>Konfigurere intern projektfakturering

[!include [banner](../../includes/banner.md)]

Dette emne viser, hvordan du opsætter projektfakturering mellem to firmaer i organisationen. Denne opgave bruger USSI-datasættet.

1. Gå i navigationsruden til **Moduler > Kreditor > Kreditorer > Alle kreditorer**.
2. Find og vælg den ønskede post på listen **Alle kreditorer**.
3. Vælg **Generelt** i handlingsruden.
4. Vælg **Intern handel**.
5. Indstil **Aktiv** til **Ja** for at aktivere intern handel.
6. Indtast eller vælg en værdi i feltet **Kundens firma**.
7. Indtast eller vælg en værdi i feltet **Min konto**.
8. Vælg **Gem**.
9. Luk siderne for at vende tilbage til startsiden.
10. Gå i navigationsruden til **Moduler > Projektstyring og regnskab > Opsætning > Parametre for projektstyring og regnskab**.
11. Vælg fanen **Intern handel**.
12. Flyt skyderen til **Ja** for at aktivere intern ressourceplanlægning og timesedler.
13. Markér den valgte række på listen.
14. Vælg **Ny**.
15. Indtast eller vælg en værdi i feltet **Udlånt til (juridisk enhed)**.
16. Markér afkrydsningsfeltet **Periodiser omsætning**.
17. Indtast eller vælg en værdi i feltet **Standardtimeseddelkategori**.
18. Indtast eller vælg en værdi i feltet **Standardudgiftskategori**.
19. Vælg **Gem**.
20. Luk siden.
21. Gå i navigationsruden til **Moduler > Projektstyring og regnskab > Opsætning > Postering > Opsætning af finanskontering**.
22. Vælg en indstilling i feltet **Finanskontotyper**.
23. Vælg **Ny**.
24. Angiv de ønskede værdier i feltet **Hovedkonto** for den nye række.
25. Vælg **Gem**.
26. Luk siden.
27. Gå i navigationsruden til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Overfør pris**.
28. Vælg **Ny**.
29. Angiv en dato i feltet **Ikrafttrædelsesdato**.
30. Indtast eller vælg en værdi i feltet **Udlånt til (juridisk enhed)**.
31. Vælg en indstilling i feltet **Overfør prismodel**.
32. Angiv et tal i feltet **Prissætning**.
33. Vælg **Gem**.

