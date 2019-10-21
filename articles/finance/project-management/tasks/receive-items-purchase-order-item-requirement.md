---
title: Modtage varer på indkøbsordre ud fra varebehov
description: I dette emne beskrives, hvordan du modtager varer i en indkøbsordre fra et varebehov.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7afdae65c5ae7e3196c6b9f142dd87aec39b5ea3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174414"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Modtage varer på indkøbsordre ud fra varebehov

[!include [task guide banner](../../includes/task-guide-banner.md)]

I dette emne beskrives, hvordan du modtager varer i en indkøbsordre fra et varebehov.

Når du bruger et varebehov i stedet for en varepostering, kan du planlægge leveringen, så den finder sted, umiddelbart før varen faktisk skal bruges. Du kan oprette en indkøbsordre, lade varen indgå i samhandelsaftaler og lade varebehovet indgå i produktionsplanlægningen. 

Denne opgave bruger USSI-datasættet.

1. Gå i navigationsruden til **Moduler > Projektstyring og regnskab > Projekter > Alle projekter**.
2. Vælg linket i den ønskede række på listen.
3. Vælg **Plan** i handlingsruden.
4. Vælg **Varebehov**.
5. Vælg **Ny**.
6. Indtast eller vælg en værdi i feltet **Varenummer** i den nye række.
7. Angiv et tal i feltet **Antal**.
8. Vælg **Gem**.
9. Vælg **Administrer** i handlingsruden.
10. Vælg **Funktioner**.
11. Vælg **Opret indkøbsordre**.
12. Marker afkrydsningsfeltet **Medtag alle**.
13. Indtast eller vælg en værdi i feltet **Kreditorkonto**.
14. Vælg **OK**.
15. I navigationsruden skal du gå til **Moduler > Kreditor > Indkøbsordrer > Alle indkøbsordrer**.
16. Vælg linket i den ønskede række på listen.
17. Klik på **Køb** i handlingsruden.
18. Vælg **Bekræft**.
19. Vælg **Modtag** i handlingsruden.
20. Vælg **Produktkvittering**.
21. Skriv en værdi i feltet **Produktkvittering**.
22. Vælg **OK**.

