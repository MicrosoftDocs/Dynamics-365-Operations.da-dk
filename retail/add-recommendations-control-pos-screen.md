---
title: "Tilføje et kontrolelement med anbefalinger til siden transaktion på POS-enhed"
description: "Dette emne beskriver, hvordan du tilføjer et kontrolelement med anbefalinger til skærmbilledet transaktion vedrørende et salg (POS) enhed ved hjælp af layoutdesigneren skærm i Microsoft Dynamics 365 for operationer."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2377b1639a3c95fe6bba4754c4069cc12043e3d3
ms.lasthandoff: 03/31/2017


---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>Tilføje et kontrolelement med anbefalinger til siden transaktion på POS-enhed

Dette emne beskriver, hvordan du tilføjer et kontrolelement med anbefalinger til skærmbilledet transaktion vedrørende et salg (POS) enhed ved hjælp af layoutdesigneren skærm i Microsoft Dynamics 365 for operationer.

Du kan få vist produkt anbefalinger på POS-enheden, når du bruger Microsoft Dynamics 365 for operationer. *Anbefalinger* er varer, som kunden er interesseret i at baseret på deres købshistorik, varer i deres ønskeseddel og varer, som andre kunder har købt online og i mursten og mørtel butikker. For at få vist produkt anbefalinger, skal du føje et kontrolelement til skærmbilledet transaktion ved hjælp af skærmen layoutdesigneren.

## <a name="open-layout-designer"></a>Åbn layoutdesigneren
1.  Gå til **detail- og commerce**&gt;**kanal setup**&gt;**POS installationsprogrammet**&gt;**POS**&gt;**skærmlayout**.
2.  Brug af Quick Filter til at finde det skærmbillede, du vil føje kontrolelementet til. Filtrere for eksempel på den **skærm layout-ID** ved hjælp af en værdi på 'F2CP16:9M'.
3.  Find og vælg den ønskede post på listen. For eksempel vælge ' navn: F2CP16:9M skærm Layout-ID: F2CP16:9M'.
4.  Klik på **layoutdesigneren**.
5.  Følg vejledningen for at starte layoutdesigneren. Når bedt om legitimationsoplysninger, skal du angive de samme legitimationsoplysninger, der er i brug, når layoutdesigneren blev startet fra **skærmlayout** side.
6.  Når du logger på, vises en side, der ligner den nedenfor. Layoutet vil være forskellige, afhængigt af de tilpasninger, der er foretaget for din butik.

[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Vælg en visningsindstilling
-----------------------

Der er to konfigurationer indstillinger. Vælg den indstilling, der passer bedst til din butik, og følg derefter vejledningen for at afslutte opsætningen af kontrolelementet. Der er to indstillinger:
-   Anbefalingerne er altid synlig.
-   A **anbefalinger** fane, der vises i gitteret på højre side af skærmen.

#### <a name="to-make-recommendations-always-visible"></a>At fremsætte anbefalinger altid synlig

1.  Reducere højden af området transaktion linjer detaljer, så det er samme højde som kunden panelet til venstre. [](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)
2.  I menuen til venstre, træk og slip kontrolelementet anbefalinger til mellem området transaktion linje detaljer og knapmatricen center nederst i skærmbilledet transaktion. Ændre størrelsen på kontrolelementet, så den passer i det pågældende område. [](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)
3.  Klik på den **X** at gemme og afslutte layoutdesigneren.
4.  Dynamics 365 for operationer, gå til **detail- og commerce**&gt;**Retail IT**&gt;**distributionsplaner**.
5.  Vælg på listen **1090 registrerer**.
6.  Klik på **kører nu**.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Føje en fane med anbefalinger til knapmatricen på højre side af skærmen

1.  Højreklik på det tomme område under fanen sidste i knapmatricen placeret på højre side af siden.
2.  Klik på **tilpasse**. [![pic-5](./media/pic-5.png)](./media/pic-5.png)
3.  Klik på **ny fane**.
4.  Find den nye fane, du lige har tilføjet. Du skal muligvis rulle ned.
5.  I den **indhold** ned, skal du vælge **anbefalede produkter**. [![PIC-6](./media/pic-6.png)](./media/pic-6.png)
6.  I den **etiket** skal du skrive et navn til fanen anbefalinger. Skriv eksempelvis 'Anbefalede produkter'.
7.  I den **billede** skal du vælge billedet, der vises under fanen.
8.  Click **OK**. Den nye fane vises i knapmatricen.
9.  Klik på den **X** at gemme og afslutte layoutdesigneren.
10. Dynamics 365 for operationer, gå til **detail- og commerce**&gt;**Retail IT**&gt;**distributionsplaner**.
11. Vælg på listen **1090 registrerer**.
12. Klik på **kører nu**.


<a name="see-also"></a>Se også
--------

[Personlige anbefalinger produktoversigt](personalized-product-recommendations.md)


