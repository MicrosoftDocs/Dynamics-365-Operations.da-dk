---
title: "Føje et kontrolelement med anbefalinger til transaktionssiden på en POS-enhed"
description: "I dette emne beskrives, hvordan du tilføjer et kontrolelement med anbefalinger til transaktionsskærmbilledet på en POS-enhed (point of sale) ved hjælp af skærmlayoutdesigneren i Microsoft Dynamics 365 for Retail."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: eac70614770189d1e45f347b282c94e645e95b00
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>Føje et kontrolelement med anbefalinger til transaktionssiden på en POS-enhed

[!include [banner](includes/banner.md)]

> [!NOTE]
> Vi vil fjerne den aktuelle version af produktanbefalingstjenesten, fordi vi ændrer denne funktion og giver den en bedre algoritme og nyere detailrelaterede funktioner. Du kan finde flere oplysninger i [Fjernede eller forældede funktioner](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features). 

I dette emne beskrives, hvordan du tilføjer et kontrolelement med anbefalinger til transaktionsskærmbilledet på en POS-enhed (point of sale) ved hjælp af skærmlayoutdesigneren i Microsoft Dynamics 365 for Retail.

Du kan få vist produktanbefalinger på POS-enheden, når du bruger Microsoft Dynamics 365 for Retail. *Anbefalinger* er varer, som kunden muligvis er interesseret i baseret på deres købshistorik, varer i deres ønskeseddel og varer, som andre kunder har købt online og i fysiske butikker. For at få vist produktanbefalinger skal du føje et kontrolelement til transaktionsskærmen ved hjælp af skærmlayoutdesigneren.

## <a name="open-layout-designer"></a>Åbn layoutdesigner
1.  Gå til **Retail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS** &gt; **Skærmlayout**.
2.  Brug Quick Filter til at finde det skærmbillede, du vil føje kontrolelementet til. Filtrer for eksempel på feltet **Skærmlayout-id** ved hjælp af værdien 'F2CP16:9M'.
3.  Find og vælg den ønskede post på listen. Vælg for eksempel 'Navn: F2CP16:9M skærmlayout-ID: F2CP16:9M'.
4.  Klik på **Layoutdesigner**.
5.  Følg vejledningen for at starte layoutdesigneren. Når du bliver bedt om legitimationsoplysninger, skal du angive de legitimationsoplysninger, der var i brug, da layoutdesigneren blev startet fra **Skærmlayout** siden.
6.  Når du logger på, vises en side, der ligner den nedenfor. Layoutet er forskelligt, afhængigt af de tilpasninger, der er foretaget for din butik.

[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Vælg en visningsindstilling
-----------------------

Der findes to konfigurationsindstillinger. Vælg den indstilling, der passer bedst til din butik, og følg derefter vejledningen for at afslutte opsætningen af kontrolelementet. Der er følgende to indstillinger:
-   Anbefalingerne er altid synlige.
-   Fanen **Anbefalinger** vises i gitteret på højre side af skærmen.

#### <a name="to-make-recommendations-always-visible"></a>Sådan gøres anbefalinger synlige altid

1.  Reducer højden af området med detaljer for transaktionslinjer, så det har samme højde som kundepanelet til venstre.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)
2.  I menuen til venstre skal du trække og slippe kontrolelementet med anbefalinger til mellem området med transaktionslinjedetaljer og knapmatricen nederst i midten af transaktionsskærmbilledet. Rediger størrelsen på kontrolelementet, så det passer i det pågældende område.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)
3.  Klik på **X** for at lukke og afslutte layoutdesigneren.
4.  I Dynamics 365 for Retail skal du gå til **Retail** &gt; **Retail it** &gt; **Distributionsplaner**.
5.  Vælg **1090, kasseapparater** på listen.
6.  Klik på **Kør nu**.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Sådan tilføjes fanen Anbefalinger i gitteret nederst i højre side af skærmen

1.  Højreklik på det tomme område under den sidste fane i knapmatricen i højre side af siden.
2.  Klik på **Tilpas**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)
3.  Klik på fanen **Ny**.
4.  Find den nye fane, du lige har tilføjet. Du skal muligvis rulle ned.
5.  I rullemenuen **Indhold** skal du vælge **Anbefalede produkter**. [![PIC-6](./media/pic-6.png)](./media/pic-6.png)
6.  I feltet **Etiket** skal du angive et navn til fanen Anbefalinger. Skriv f.eks. 'Anbefalede produkter'.
7.  Vælg det billede, der skal vises på fanen, i feltet **Billede**.
8.  Klik på **OK**. Den nye fane vises i knapmatricen.
9.  Klik på **X** for at lukke og afslutte layoutdesigneren.
10. I Dynamics 365 for Retail skal du gå til **Retail** &gt; **Retail it** &gt; **Distributionsplaner**.
11. Vælg **1090, kasseapparater** på listen.
12. Klik på **Kør nu**.


<a name="additional-resources"></a>Yderligere ressourcer
--------

[Oversigt over tilpassede produktanbefalinger](personalized-product-recommendations.md)




