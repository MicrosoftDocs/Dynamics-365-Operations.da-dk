--- 
title: " Detailprisjusteringer"
description: "Denne procedure gennemgår oprettelse af en detailprisjustering."
author: josaw1
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: ab13aced30f90c4d7c8b96f30340fff6e3eee927
ms.contentlocale: da-dk
ms.lasthandoff: 07/28/2017

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

