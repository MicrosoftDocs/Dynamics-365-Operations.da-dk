---
title: Føje anbefalinger til transaktionsskærmen
description: Denne artikel beskriver, hvordan du tilføjer et kontrolelement med anbefalinger til transaktionsskærmbilledet på en POS-enhed (point of sale) ved hjælp af skærmlayoutdesigneren i Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4748ade8d6693666b58cbded2123d3449d191509
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862066"
---
# <a name="add-recommendations-to-the-transaction-screen"></a>Føje anbefalinger til transaktionsskærmen

[!include [banner](includes/banner.md)]


Denne artikel beskriver, hvordan du tilføjer et kontrolelement med anbefalinger til transaktionsskærmbilledet på en POS-enhed (point of sale) ved hjælp af skærmlayoutdesigneren i Microsoft Dynamics 365 Commerce. Hvis du ønsker yderligere oplysninger om produktanbefalinger, kan du læse [produktanbefalingerne i POS-dokumentation](product.md).


Du kan få vist produktanbefalinger på POS-enheden, når du bruger Commerce. For at få vist produktanbefalinger skal du føje et kontrolelement til transaktionsskærmen ved hjælp af skærmlayoutdesigneren. 

## <a name="open-layout-designer"></a>Åbn layoutdesigner

1. Gå til **Retail og Commerce** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS** &gt; **Skærmlayout**.
2. Brug Quick Filter til at finde det skærmbillede, du vil føje kontrolelementet til. Filtrer for eksempel på feltet **Skærmlayout-id** ved hjælp af værdien **F2CP16:9M**.
3. Find og vælg den ønskede post på listen. Vælg for eksempel **Navn: F2CP16:9M skærmlayout-ID: F2CP16:9M**.
4. Klik på **Layoutdesigner**.
5. Følg vejledningen for at starte layoutdesigneren. Når du bliver bedt om legitimationsoplysninger, skal du angive de legitimationsoplysninger, der var i brug, da layoutdesigneren blev startet fra siden **Skærmlayout**.
6. Når du logger på, vises en side, der ligner den nedenfor. Layoutet er forskelligt, afhængigt af de tilpasninger, der er foretaget for din butik.


    [![Layoutdesigner.](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>Vælg en visningsindstilling

Der findes to konfigurationsindstillinger. Vælg den indstilling, der passer bedst til din butik, og følg derefter vejledningen for at afslutte opsætningen af kontrolelementet. Der er følgende to indstillinger:

- Anbefalingerne er altid synlige.
- Fanen **Anbefalinger** vises i gitteret i højre side af skærmen.

### <a name="make-recommendations-always-visible"></a>Gøre anbefalinger synlige permanent


1. Reducer højden af området med detaljer for transaktionslinjer, så det har samme højde som kundepanelet til venstre.


    [![Højden på området med transaktionslinjedetaljer er reduceret.](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. I menuen til venstre skal du trække og slippe kontrolelementet med anbefalinger til mellem området med transaktionslinjedetaljer og knapmatricen nederst i midten af transaktionsskærmbilledet. Rediger størrelsen på kontrolelementet, så det passer i det pågældende område.

    [![Kontrolelement til anbefalinger er føjet til layoutet.](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)


3. Klik på **X** for at lukke og afslutte layoutdesigneren.
4. I Commerce gå til **Retail og Commerce** &gt; **Retail og Commerce IT** &gt; **Distributionsplaner**.
5. Vælg **1090, kasseapparater** på listen.
6. Klik på **Kør nu**.


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Tilføj fanen Anbefalinger i gitteret nederst i højre side af skærmen

1. Højreklik på det tomme område under den sidste fane i knapmatricen i højre side af siden.

2. Klik på **Tilpas**.

    [![Dialogboksen Tilpasning - fanekontrolelement.](./media/pic-5.png)](./media/pic-5.png)

3. Klik på fanen **Ny**.
4. Find den nye fane, du lige har tilføjet. Du skal muligvis rulle ned.
5. I rullemenuen **Indhold** skal du vælge **Anbefalede produkter**.

    [![Vælge Anbefalede produkter i feltet Indhold.](./media/pic-6.png)](./media/pic-6.png)

6. I feltet **Etiket** skal du angive et navn til fanen Anbefalinger. Skriv f.eks. 'Anbefalede produkter'.
7. Vælg det billede, der skal vises på fanen, i feltet **Billede**.
8. Klik på **OK**. Den nye fane vises i knapmatricen.
9. Klik på **X** for at lukke og afslutte layoutdesigneren.
10. I Commerce gå til **Retail og Commerce** &gt; **Retail og Commerce IT** &gt; **Distributionsplaner**.
11. Vælg **1090, kasseapparater** på listen.
12. Klik på **Kør nu**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over produktanbefalinger](product-recommendations.md)

[Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktivér produktanbefalinger](enable-product-recommendations.md)

[Aktivere tilpassede anbefalinger](personalized-recommendations.md)

[Fravælge tilpassede anbefalinger](personalization-gdpr.md)

[Aktivere anbefalinger af "Køb tilsvarende"](shop-similar-looks.md)

[Tilføje produktanbefalinger på POS](product.md)

[Justere resultater for AI-ML-anbefalinger](modify-product-recommendation-results.md)

[Oprette overvågede anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Oprette anbefalinger med demonstrationsdata](product-recommendations-demo-data.md)

[Ofte stillede spørgsmål om produktanbefalinger](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]