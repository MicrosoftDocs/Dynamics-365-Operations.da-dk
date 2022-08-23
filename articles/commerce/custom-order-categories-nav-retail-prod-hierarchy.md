---
title: Ændre sorteringsrækkefølgen for merchandisingenheder
description: Denne artikel forklarer de begreber, der er relateret til styring af visningsrækkefølgen for forskellige merchandising-relaterede enheder i Dynamics 365 Commerce.
author: josaw1
ms.date: 08/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 80586597f4f60476b341e4cf1cfd90f3681e15c0
ms.sourcegitcommit: 52e31b1ef2b3ed8675de931d06090cd57e057fc2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9265830"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Ændre sorteringsrækkefølgen for merchandisingenheder


[!Include [banner](includes/banner.md)]

Detailhandlere regner produktopdagelse for et primært værktøj til kundeinteraktion på tværs af alle kanaler. Der er flere funktioner, der kan gøre det nemmere for kunderne at finde produkter. De kan f.eks. gennemse kategorier, søge og filtrere.

Denne artikel forklarer de begreber, der er relateret til styring af visningsrækkefølgen for forskellige merchandising-relaterede enheder. Det forklarer også, hvordan sorteringsrækkefølgen ændres.

## <a name="overview"></a>Overblik

I Commerce tilpasses sortering af forskellige merchandiserelaterede enheder efter eksisterende kundescenarier og kræver ikke længere udvidelser fra implementeringspartnere.

I Commerce version 10.0.5 og tidligere var sorteringsrækkefølgen for kategorierne i navigationshierarkiet alfabetisk. Den aktuelle brugerdefinerede funktion til sorteringsrækkefølge gør det muligt for merchandisechefer at konfigurere sorteringsrækkefølgen for forskellige merchandiserelaterede enheder på tværs af alle slutbrugerklienter. Disse klienter omfatter hovedkontorer og callcentre.

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a>Konfigurere visningsrækkefølgen for kategorier i produkthierarkiet

Før du kan udføre denne procedure, skal demodata være installeret i dit miljø.

1. Gå til **Detail og handel \> Produkter og kategorier \> Commerce-produkthierarki**.
2. Klik på **Rediger kategorihierarki**.
3. Klik på **Rediger**.
4. Udvid **ALL \> Action Sports** i træet.
5. Udvid **ALL \> Team Sports** i træet.
6. Angiv et tal i feltet **Visningsrækkefølge**. (Tallet kan være negativt).
7. Gentag trin 4 til 6 for eventuelle yderligere kategorier, du vil ændre rækkefølgen af.

Visningsrækkefølgen for hierarkiet til kanalnavigation vil blive afspejlet i hovedkontoret for handelsprodukthierarkiet og frigivne produkter efter kategori.

![Produkhierarki sorteret med negative værdier.](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Frigivne produkter efter kategori sorteret på basis af produkthierarkiet.](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>Konfigurere visningsrækkefølgen for kategorier i navigationshierarki for kanal

Før du kan udføre denne procedure, skal demodata være installeret i dit miljø.

1. Gå til **Retail og Commerce \> Produkter og kategorier \> Navigationskategorier for kanal**.
2. Vælg hierarkiet **Fashion navigation** på listen.
3. Klik på **Rediger kategorihierarki**.
4. Klik på **Rediger**.
5. Vælg **Fashion \> Womenswear \> Women's Shoes** i træet.
6. Angiv et tal i feltet **Visningsrækkefølge**.
7. Vælg **Fashion \> Womenswear \> Tops** i træet.

På samme måde kan du definere sorteringsrækkefølgen for underkategorierne.

8. Vælg **Fashion \> Menswear \> Casual Shirts** i træet.
9. Angiv et tal i feltet **Visningsrækkefølge**.
10. Vælg **Fashion \> Menswear \> Coats & Jackets** i træet.
11. Angiv et tal i feltet **Visningsrækkefølge**.
12. Gentag for eventuelle yderligere kategorier, du vil ændre rækkefølgen af.

Visningsrækkefølgen i navigationshierarkiet for kanal afspejles i hovedkontoret, kataloget og kanaler.

![Brugersorteret navigationshierarki for kanal.](./media/ChannelNavCustomSorted.png)

![Brugersorteret navigationshierarki for kanal baseret på kanalnavigationshierarkiet.](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS med brugerdefinerede sorterede kategorier.](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> Som standard er funktionen **Aktivér visningsrækkefølge for merchandising-enheder** deaktiveret. Brug [Funktionsstyring](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere den. Derefter skal du køre **Global konfiguration -1110** CDX-job fra distributionsplanen.
> Hvis dine kategorier i POS ikke opdateres, skal du genaktivere enheden. Kategorioplysninger hentes, når enhedsaktivering indtræffer, så enheden kan derfor være nødt til at hente kategorioplysningerne igen med opdaterede visningsrækkefølger. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
