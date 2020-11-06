---
title: Webstedsvælgermodul
description: Dette emne omhandler webstedsvælgermodulet og beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: bd54695f54b501631f916328c05bfd47e538d50d
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055824"
---
# <a name="site-selector-module"></a>Webstedsvælgermodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emne omhandler webstedsvælgermodulet og beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Når en virksomhed har forskellige websteder på tværs af markeder, områder og landestandarder, skal webstedsbrugere have en nem metode til at skifte mellem websteder og vælge deres foretrukne indkøbssted. For at tage højde for dette scenario kan brugere gennemse flere websteder ved at bruge modulet til valg af websted.

Modulet til valg af websted skal konfigureres med listen over websteder (markeder, områder eller landestandarder), som brugerne kan gennemse.

> [!NOTE]
> Modulet til valg af websted er tilgængeligt i Dynamics 365 Commerce version 10.0.14.

I følgende illustration vises et eksempel på et modul til valg af websted, der findes i overskriften på en webside.

![Eksempel på et modul til valg af websted i en overskrift på en webside](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a>Egenskaber for webstedsvælgermodulet

| Egenskabsbetegnelse | Værdi                 | Betegnelse |
|---------------|-----------------------|-------------|
| Overskrift       | Tekst                  | Overskrift for modulet. |
| Webstedsindstillinger  | Navn, billede, URL-adresse      | Denne egenskab specificerer et navn, et link til webstedets startside og et valgfrit billede, der skal vises for hvert websted, der er medtaget i modulet. Billedet kan være et flag eller en vis repræsentation af et marked, område eller en landestandard. |

## <a name="add-a-site-selector-module-to-a-page"></a>Føje et webstedsvælgermodul til en side

Webstedsvælgermodulet kan føjes til [overskriftsmodulet](author-header-module.md) under pladsen for webstedsvælgeren. Når det er tilføjet, kan du definere moduloverskriften og indstillinger for webstedet.

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Overskriftsmodul](author-header-module.md)

[Brødkrummemodul](add-breadcrumb.md)

[Navigationsmenumodul](nav-menu-module.md)