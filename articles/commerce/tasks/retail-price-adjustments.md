---
title: " Detailprisjusteringer"
description: Denne procedure gennemgår oprettelse af en prisjustering for handel.
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
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7443f69473c0aad478d47f80f284b1156bad9c24
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4962979"
---
# <a name="retail-price-adjustments"></a> Detailprisjusteringer

[!include [banner](../includes/banner.md)]

Denne procedure gennemgår oprettelse af en prisjustering for handel. En prisjustering kan angive en vares salgspris direkte eller ændre dens basissalgspris eller salgspris ifølge samhandelsaftale. Proceduren bruger USRT-demodatafirmaet.

1. Klik på Styring af prissætning og rabatter.
2. Klik på fanen Prisjusteringer.
3. Klik på Ny.
    * Her kan du oprette alle de mest almindeligt anvendte pris- og rabatregler, herunder rabatter, prisjusteringer, samhandelskladder og prissætningsregler for kategori.  
4. Klik på Prisjustering.
5. Skriv en værdi i feltet Navn.
6. Udvid sektionen Linjer.
7. Klik på Tilføj.
    * I dette eksempel skal du skrive "81126" i feltet Produkt. Angiv derefter "10,0" i feltet Rabatprocent.  
    * En prisjustering af typen rabatprocent vil reducere en basissalgspris eller salgspris ifølge samhandelsaftale.  
8. Klik på Tilføj.
    * I dette eksempel skal du skrive "81125" i feltet Produkt. Vælg derefter "Kasserabatbeløb" i feltet Rabatmetode.    Skriv til sidst "5,0" i feltet Kasserabatbeløb.  
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]