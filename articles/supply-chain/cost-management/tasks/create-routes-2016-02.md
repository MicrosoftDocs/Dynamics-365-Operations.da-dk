--- 
title: Oprette ruter (kun februar 2016)
description: "Denne opgave drejer sig om oprettelse af produktionsruter for et færdigt produkt og et halvfabrikatprodukt."
author: BibiSp
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 0f8d6a45589886a611fc3a9179b50a8b1ac1c7f4
ms.contentlocale: da-dk
ms.lasthandoff: 07/28/2017

---
# <a name="create-routes-february-2016-only"></a>Oprette ruter (kun februar 2016)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne opgave drejer sig om oprettelse af produktionsruter for et færdigt produkt og et halvfabrikatprodukt. Det er den femte opgave i styklisteberegningsserien. Det demodatafirma, der bruges til at oprette denne opgave, er USMF.


## <a name="create-a-route-for-a-semi-finished-product"></a>Opret en rute for et halvfabrikatprodukt.
1. Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.
2. Klik op linket i den valgte række på listen.
    * Vælg varenummer BOM_2.  
3. Klik på Tekniker i handlingsruden.
4. Klik på Rute.
5. Klik på Ny.
6. Klik på Rute og ruteversion.
7. Skriv en værdi i feltet Beskrivelse.
    * I dette eksempel skal du skrive ROUTE_2.  
8. Indtast eller vælg en værdi i feltet Lokation.
    * Skriv eller vælg Sted 1 i dette eksempel.  
9. Klik på OK.
10. Klik på Ny.
11. Indtast eller vælg en værdi i feltet Handling.
    * Vælg Assembly i dette eksempel.  
12. Angiv et tal i feltet Procestid.
    * Skriv for eksempel 1. Kørselstider er ofte en del af den pris, der beregnes for en vare.  
13. Indtast eller vælg en værdi i feltet Rutegruppe.
    * Vælg Std. i dette eksempel.  
14. Klik på fanen Opsætning.
15. Indtast eller vælg en værdi i feltet Opstillingsart.
    * Vælg Assembly i dette eksempel.  
16. Klik på fanen Tider.
17. Angiv et tal i feltet Opstillingstid.
    * I dette eksempel skal du skrive 1. Opstillingstider er ofte en del af den pris, der beregnes for en vare.  
18. Klik på Ruteversion i handlingsruden.
19. Klik på Godkend.
20. Vælg Ja til Vil du også godkende ruten? .
21. Klik på OK.
22. Klik på Ruteversion i handlingsruden.
23. Klik på Aktiver.
24. Luk siden.
25. Luk siden.

## <a name="create-a-route-for-a-finished-product"></a>Oprette en rute for et færdigt produkt
1. Klik op linket i den valgte række på listen.
    * Vælg varenummeret BOM_1.  
2. Klik på Tekniker i handlingsruden.
3. Klik på Rute.
4. Klik på Ny.
5. Klik på Rute og ruteversion.
6. Skriv en værdi i feltet Beskrivelse.
    * I dette eksempel skal du skrive ROUTE_1.  
7. Indtast eller vælg en værdi i feltet Lokation.
    * Skriv eller vælg Sted 1 i dette eksempel.  
8. Klik på OK.
9. Klik på Ny.
10. Indtast eller vælg en værdi i feltet Handling.
    * Vælg Emballage i dette eksempel.  
11. Angiv et tal i feltet Procestid.
    * I dette eksempel skal du skrive 1.  
12. Indtast eller vælg en værdi i feltet Rutegruppe.
    * Vælg Std. i dette eksempel.  
13. Klik på fanen Opsætning.
14. Indtast eller vælg en værdi i feltet Opstillingsart.
    * Vælg Emballage i dette eksempel.  
15. Klik på fanen Tider.
16. Angiv et tal i feltet Opstillingstid.
    * I dette eksempel skal du skrive 1.  
17. Klik på Ruteversion i handlingsruden.
18. Klik på Godkend.
19. Klik på OK.
20. Klik på Ruteversion i handlingsruden.
21. Klik på Aktiver.
22. Luk siden.
23. Luk siden.

## <a name="enable-automatic-consumption-of-setup-time"></a>Aktiver automatisk forbrug af opstillingstid
1. Gå til Produktionsstyring > Konfiguration > Ruter > Rutegrupper.
2. Find og vælg den ønskede post på listen.
    * Vælg Std. på listen.  
3. Klik på Rediger.
4. Vælg Ja i feltet Opstillingstid.
    * Opstillingstider er ofte en del af den pris, der beregnes for en vare.  
5. Klik på Gem.
6. Luk siden.


