---
title: Oprette råvarer (februar 2016)
description: Denne opgave drejer sig om oprettelse af færdige produkter og halvfabrikataprodukter.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 091b6edaf43e86e6e3665bf79871648473e284c7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552664"
---
# <a name="create-raw-materials-february-2016"></a>Oprette råvarer (februar 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne opgave drejer sig om oprettelse af færdige produkter og halvfabrikataprodukter. Det er den tredje opgave i styklisteberegningsserien. Det demodatafirma, der bruges til at oprette denne opgave, er USMF.


## <a name="create-the-first-material"></a>Opret det første materiale
1. Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.
2. Klik på Ny.
3. Skriv en værdi i feltet Produktnummer.
    * Skriv ITEM_A i dette eksempel.  
4. Indtast eller vælg en værdi i feltet Varemodelgruppe.
    * Vælg STD. STD står for standardomkostninger og er den mest almindeligt anvendte model, når du arbejder med omkostningsberegninger.  
5. Indtast eller vælg en værdi i feltet Varegruppe.
    * Vælg f.eks. Lyd. Dette har ingen indflydelse på omkostningsberegninger.  
6. Indtast eller vælg en værdi i feltet Lagringsdimensionsgruppe.
    * Vælg SiteWH. Kun lokation og lagersted bruges til demonstrationen.  
7. Indtast eller vælg en værdi i feltet Sporingsdimensionsgruppe.
    * Sporingsdimensioner bliver ikke brugt i dette eksempel. Vælg Ingen.  
8. Klik på OK.
9. Klik på Styr lager i handlingsruden.
10. Klik på Standardindstillinger for ordre.
11. Indtast eller vælg en værdi i feltet Købssted.
    * I dette eksempel skal du vælge Sted 1.  
12. Indtast eller vælg en værdi i feltet Sted for lager.
    * I dette eksempel skal du vælge Sted 1.  
13. Indtast eller vælg en værdi i feltet Salgssted.
    * I dette eksempel skal du vælge Sted 1.  
14. Luk siden.
15. Luk siden.
16. Klik op linket i den valgte række på listen.
    * Klik på ITEM_A.  
17. Udvid sektionen Administrer omkostninger.
18. Skriv en værdi i feltet Omkostningsgruppe.
    * I dette eksempel skal du skrive M2.  
19. Klik på Administrer omkostninger i handlingsruden.
20. Klik på Varepris.
21. Klik på Ny.
22. Indtast eller vælg en værdi i feltet Version.
    * I dette eksempel skal du vælge 10, som er en omkostningstype for standardomkostninger.  
23. Indtast eller vælg en værdi i feltet Lokation.
    * I dette eksempel skal du vælge Sted 1.  
24. Angiv et tal i feltet Pris.
    * I dette eksempel skal du skrive 10.  
25. Klik på Gem.
26. Klik på Aktivér afventende pris(er).
27. Luk siden.
28. Luk siden.

## <a name="create-the-second-material"></a>Opret det andet materiale
1. Klik på Ny.
2. Skriv en værdi i feltet Produktnummer.
    * I dette eksempel skal du skrive ITEM_B.  
3. Indtast eller vælg en værdi i feltet Varemodelgruppe.
    * Vælg STD. STD står for standardomkostninger og er den mest almindeligt anvendte model, når du arbejder med omkostningsberegninger.  
4. Indtast eller vælg en værdi i feltet Varegruppe.
    * Vælg f.eks. Lyd. Dette har ingen indflydelse på omkostningsberegninger.  
5. Indtast eller vælg en værdi i feltet Lagringsdimensionsgruppe.
    * Vælg SiteWH. Kun lokalitet og lagersted bruges til dette eksempel.  
6. Indtast eller vælg en værdi i feltet Sporingsdimensionsgruppe.
    * Sporingsdimensioner bliver ikke brugt i dette eksempel. Vælg Ingen.  
7. Klik på OK.
8. Klik på Styr lager i handlingsruden.
9. Klik på Standardindstillinger for ordre.
10. Indtast eller vælg en værdi i feltet Købssted.
    * I dette eksempel skal du vælge Sted 1.  
11. Indtast eller vælg en værdi i feltet Sted for lager.
    * I dette eksempel skal du vælge Sted 1.  
12. Indtast eller vælg en værdi i feltet Salgssted.
    * I dette eksempel skal du vælge Sted 1.  
13. Luk siden.
14. Luk siden.
15. Klik op linket i den valgte række på listen.
    * Klik på ITEM_B.  
16. Udvid sektionen Administrer omkostninger.
17. Skriv en værdi i feltet Omkostningsgruppe.
    * I dette eksempel skal du skrive M2.  
18. Klik på Administrer omkostninger i handlingsruden.
19. Klik på Varepris.
20. Klik på Ny.
21. Indtast eller vælg en værdi i feltet Version.
    * I dette eksempel skal du vælge 10. Dette er omkostningstypen for standardomkostninger  
22. Indtast eller vælg en værdi i feltet Lokation.
    * I dette eksempel skal du vælge Sted 1.  
23. Angiv et tal i feltet Pris.
    * Skriv 10 i demonstrationen.  
24. Klik på Gem.
25. Klik på Aktivér afventende pris(er).
26. Luk siden.
27. Luk siden.

## <a name="create-the-third-material"></a>Opret det tredje materiale
1. Klik på Ny.
2. Skriv en værdi i feltet Produktnummer.
    * Skriv ITEM_C i demonstrationen  
3. Indtast eller vælg en værdi i feltet Varemodelgruppe.
    * Vælg STD. STD står for standardomkostninger og er den mest almindeligt anvendte model, når du arbejder med omkostningsberegninger.  
4. Indtast eller vælg en værdi i feltet Varegruppe.
    * Vælg f.eks. Lyd. Dette har ingen indflydelse på omkostningsberegninger.  
5. Indtast eller vælg en værdi i feltet Lagringsdimensionsgruppe.
    * Vælg SiteWH. Kun lokation og lagersted bruges til demonstrationen.  
6. Indtast eller vælg en værdi i feltet Sporingsdimensionsgruppe.
    * Sporingsdimensioner bliver ikke brugt i dette eksempel. Vælg Ingen.  
7. Klik på OK.
8. Klik på Styr lager i handlingsruden.
9. Klik på Standardindstillinger for ordre.
10. Indtast eller vælg en værdi i feltet Købssted.
    * I dette eksempel skal du vælge Sted 1.  
11. Indtast eller vælg en værdi i feltet Sted for lager.
    * I dette eksempel skal du vælge Sted 1.  
12. Indtast eller vælg en værdi i feltet Salgssted.
    * I dette eksempel skal du vælge Sted 1.  
13. Luk siden.
14. Luk siden.
15. Klik op linket i den valgte række på listen.
    * Klik på ITEM_C.  
16. Udvid sektionen Administrer omkostninger.
17. Skriv en værdi i feltet Omkostningsgruppe.
    * I dette eksempel skal du skrive M1.  
18. Klik på Administrer omkostninger i handlingsruden.
19. Klik på Varepris.
20. Klik på Ny.
21. Indtast eller vælg en værdi i feltet Version.
    * I dette eksempel skal du vælge 10. Dette er omkostningstypen for standardomkostninger  
22. Indtast eller vælg en værdi i feltet Lokation.
    * I dette eksempel skal du vælge Sted 1.  
23. Angiv et tal i feltet Pris.
    * I dette eksempel skal du skrive 10.  
24. Klik på Gem.
25. Klik på Aktivér afventende pris(er).
26. Luk siden.
27. Luk siden.

