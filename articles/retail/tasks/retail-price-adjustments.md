---
title: " Detailprisjusteringer"
description: Denne procedure gennemgår oprettelse af en detailprisjustering.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailDiscountPriceGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9427d3955e5442e301c416e2960e071ca5d85a3c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "366299"
---
# <a name="retail-price-adjustments"></a> Detailprisjusteringer

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne procedure gennemgår oprettelse af en detailprisjustering. En detailprisjustering kan angive en vares salgspris direkte eller ændre dens basissalgspris eller salgspris ifølge samhandelsaftale. Proceduren bruger USRT-demodatafirmaet.

1. Klik på Styring af prissætning og rabatter.
2. Klik på fanen Prisjusteringer.
3. Klik på Ny.
    * Her kan du oprette alle de mest almindeligt anvendte pris- og rabatregler, herunder detailrabatter, prisjusteringer, samhandelskladder og kategoriprissætningregler.  
4. Klik på Prisjustering.
5. Skriv en værdi i feltet Navn.
6. Udvid sektionen Linjer.
7. Klik på Tilføj.
    * I dette eksempel skal du skrive "81126" i feltet Produkt.    Angiv derefter "10,0" i feltet Rabatprocent.  
    * En prisjustering af typen rabatprocent vil reducere en basissalgspris eller salgspris ifølge samhandelsaftale.  
8. Klik på Tilføj.
    * I dette eksempel skal du skrive "81125" i feltet Produkt.    Vælg derefter "Kasserabatbeløb" i feltet Rabatmetode.    Skriv til sidst "5,0" i feltet Kasserabatbeløb.  
    * En rabat af typen kasserabatbeløb er et beløb taget fra en basispris eller en pris ifølge samhandelsaftale.  
9. Klik på Prisgrupper.
    * Vælg "RP-Houston"' i feltet Prisgruppe.  
    * Dette vil knytte prisjusteringen til Houston-butikken.  
10. Klik på Gem.
11. Luk siden.
12. Vælg "Aktiveret" i feltet Status.
13. Klik på Gem.
14. Luk siden.
15. Opdater siden.

