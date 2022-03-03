---
title: Webstedsvælgermodul
description: Dette emne omhandler modulet webstedsvælger og beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 381163fdd6180a76def2e1bfb733f597b611c517
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109700"
---
# <a name="site-picker-module"></a>Webstedsvælgermodul

[!include [banner](includes/banner.md)]

Dette emne omhandler modulet webstedsvælger og beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.

Når en virksomhed har forskellige websteder på tværs af markeder, områder og landestandarder, skal webstedsbrugere have en nem metode til at skifte mellem websteder og vælge deres foretrukne indkøbssted. For at tage højde for dette scenario kan brugere gennemse flere websteder ved at bruge modulet til valg af websted.

Modulet til valg af websted skal konfigureres med listen over websteder (markeder, områder eller landestandarder), som brugerne kan gennemse.

> [!NOTE]
> Modulet til valg af websted er tilgængeligt i Dynamics 365 Commerce version 10.0.14.

I følgende illustration vises et eksempel på et modul til valg af websted, der findes i overskriften på en webside.

![Eksempel på et modul til valg af websted i en overskrift på en webside.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>Egenskaber for webstedsvælgermodulet

| Egenskabsbetegnelse | Værdi                 | Beskrivelse |
|---------------|-----------------------|-------------|
| Overskrift       | Tekst                  | Overskrift for modulet. |
| Webstedsindstillinger  | Navn, billede, URL-adresse      | Denne egenskab specificerer et navn, et link til webstedets startside og et valgfrit billede, der skal vises for hvert websted, der er medtaget i modulet. Billedet kan være et flag eller en vis repræsentation af et marked, område eller en landestandard. |

## <a name="add-a-site-picker-module-to-a-page"></a>Føje et webstedsvælgermodul til en side

Webstedsvælgermodulet kan føjes til pladsen **Webstedsvælger** i [overskriftsmodulet](author-header-module.md). Når et webstedsvælgermodul er tilføjet, kan du definere moduloverskriften og indstillinger for webstedet. Et overskriftsmodul findes generelt i et overskriftsfragment, der kan deles på tværs af e-handelssider for et websted. I følgende eksempel er webstedsvælgermodulet føjet til pladsen **Webstedsvælger** i et overskriftsmodul, der er indeholdt i et overskriftsfragment med navnet **HeaderContainer**.

![Eksempel på et modul til valg af websted i et overskriftsfragment.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Sidehovedmodul](author-header-module.md)

[Brødkrummemodul](add-breadcrumb.md)

[Navigationsmenumodul](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
