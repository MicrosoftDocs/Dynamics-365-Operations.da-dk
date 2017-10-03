--- 
title: Oprette en salgsordre for et konfigurerbart produkt
description: "Denne procedure viser, hvordan du anvender en konfigurationsskabelon til et produkt på en salgsordre."
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 6546d504a2fda255cb5183408dfe84a3074543ab
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Oprette en salgsordre for et konfigurerbart produkt

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du anvender en konfigurationsskabelon til et produkt på en salgsordre. I dette eksempel bruges modellen D0006-højttaler i demodatafirmaet USMF. En salgsordrebehandler bruger normalt denne procedure.


## <a name="create-a-sales-order"></a>Oprette en salgsordre
1. Klik på Salgsordrebehandling og -forespørgsel.
2. Klik på Ny.
3. Klik på Salgsordre.
4. Vælg US-001 i feltet Debitorkonto. 
5. Klik på OK.
6. I feltet Varenummer skal du vælge D0006.
    * Til denne opgave skal du vælge et produkt, der kan konfigureres.  
7. Klik på Produkt og forsyning.
8. Klik på Konfigurer linje.
    * Bemærk, at prisen er ændret, baseret på den konfiguration, der blev valgt, og at feltet Medtag kabel nu er angivet til Sand.  
    * Bemærk standardprisen og de indstillinger, der er valgt til kablet.  
9. Klik på Indlæs skabelon..
    * Dette eksempel viser, hvordan du kan bruge en skabelon til at vælge en foruddefineret konfiguration. Hvis du bruger denne procedure som en opgaveguide, og du ønsker at se de andre attributværdier, der er tilgængelige, skal du klikke på knappen Lås op.  
10. Klik på OK.
11. Klik på OK.
12. Vis eller skjul sektionen Linjedetaljer.
13. Klik på fanen Produkt.
    * Konfigurationen af varen vises nu under produktdimensionerne.  
14. Luk siden.

## <a name="select-the-product-configuration"></a>Vælg produktkonfigurationen.


