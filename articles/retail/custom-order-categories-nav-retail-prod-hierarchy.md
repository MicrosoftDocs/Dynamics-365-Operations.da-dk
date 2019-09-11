---
title: Ændre sorteringsrækkefølgen for merchandisingenheder
description: I dette emne forklares de begreber, der er relateret til styring af visningsrækkefølgen for forskellige merchandising-relaterede enheder i Microsoft Dynamics 365 for Retail.
author: ashishharchwani
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2be3c1198ac6fff851be1bead2f0995202f1f0e7
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2019
ms.locfileid: "1866155"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Ændre sorteringsrækkefølgen for merchandisingenheder

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Detailhandlere regner produktopdagelse for et primært værktøj til kundeinteraktion på tværs af alle detailkanaler. Forskellige funktioner kan hjælpe kunderne med at finde produkter på en nem måde. De kan f.eks. gennemse kategorier, søge og filtrere.

I dette emne forklares de begreber, der er relateret til styring af visningsrækkefølgen for forskellige merchandising-relaterede enheder. Det forklarer også, hvordan sorteringsrækkefølgen ændres.

## <a name="overview"></a>Overblik

Understøttelsen af sortering af forskellige merchandising-relaterede enheder er blevet forbedret. Denne understøttelse er nu bedre tilpasset eksisterende kundescenarier, der tidligere krævede udvidelser fra implementeringspartnere.

I versioner af Microsoft Dynamics 365 for Retail, der er ældre end version 10.0.5, var sorteringsrækkefølgen for kategorierne i navigationshierarkiet alfabetisk. Den nye brugerdefinerede funktion til sorteringsrækkefølge gør det muligt for merchandising-chefer at konfigurere sorteringsrækkefølgen for forskellige merchandising-relaterede enheder på tværs af alle slutbrugerklienter. Disse klienter omfatter hovedkontorer og callcentre.

## <a name="configure-the-display-order-for-categories-in-the-retail-product-hierarchy"></a>Konfigurere visningsrækkefølgen for kategorier i detailprodukthierarkiet

Før du kan udføre denne procedure, skal demodata være installeret i dit miljø.

1. Gå til **Retail \> Produkter og kategorier \> Detailprodukthierarki**.
2. Klik på **Rediger kategorihierarki**.
3. Klik på **Rediger**.
4. Udvid **ALL \> Action Sports** i træet.
5. Udvid **ALL \> Team Sports** i træet.
6. Angiv et tal i feltet **Visningsrækkefølge**. (Tallet kan være negativt).
7. Gentag trin 4 til 6 for eventuelle yderligere kategorier, du vil ændre rækkefølgen af.

Visningsrækkefølgen for hierarkiet til kanalnavigation vil blive afspejlet i hovedkontoret for detailprodukthierarkiet og frigivne produkter efter kategori.

![Detailprodukthierarki sorteret med negative værdier](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Frigivne produkter efter kategori sorteret på basis af detailprodukthierarkiet](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>Konfigurere visningsrækkefølgen for kategorier i navigationshierarki for kanal

Før du kan udføre denne procedure, skal demodata være installeret i dit miljø.

1. Gå til **Detail \> Produkter og kategorier \> Navigationskategorier for kanal**.
2. Vælg hierarkiet **Fashion navigation** på listen.
3. Klik på **Rediger kategorihierarki**.
4. Klik på **Rediger**.
5. Vælg **Fashion \> Womenswear \> Womens Shoes** i træet.
6. Angiv et tal i feltet **Visningsrækkefølge**.
7. Vælg **Fashion \> Womenswear \> Tops** i træet.

    På samme måde kan du definere sorteringsrækkefølgen for underkategorierne.

8. Vælg **Fashion \> Menswear \> Casual Shirts** i træet.
9. Angiv et tal i feltet **Visningsrækkefølge**.
10. Vælg **Fashion \> Menswear \> Coats & Jackets** i træet.
11. Angiv et tal i feltet **Visningsrækkefølge**.
12. Gentag for eventuelle yderligere kategorier, du vil ændre rækkefølgen af.

Visningsrækkefølgen i navigationshierarkiet for kanal afspejles i hovedkontoret, kataloget og detailkanaler.

![Brugersorteret navigationshierarki for kanal](./media/ChannelNavCustomSorted.png)

![Brugersorteret navigationshierarki for kanal baseret på kanalnavigationshierarkiet](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS med brugerdefinerede sorterede kategorier](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> Funktionen for brugerdefineret sorteringsrækkefølge er som standard slået fra. Du kan få mere at vide om, hvordan du aktiverer denne og andre funktioner, under [Administration af funktioner](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).
