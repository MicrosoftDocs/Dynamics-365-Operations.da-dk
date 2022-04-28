---
title: Webstedsvælgermodul
description: Dette emne omhandler modulet webstedsvælger og beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/06/2022
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
ms.openlocfilehash: ad4d4d5f950d0631059d8f509e9e808a9106eb98
ms.sourcegitcommit: 4861ec2d3ae24cc9dd4ad3ac748fd05be3d80c70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/06/2022
ms.locfileid: "8551688"
---
# <a name="site-picker-module"></a>Webstedsvælgermodul

[!include [banner](includes/banner.md)]

Dette emne omhandler modulet webstedsvælger og beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.

Når en virksomhed har forskellige websteder på tværs af markeder, områder og landestandarder, skal webstedsbrugere have en nem metode til at skifte mellem websteder og vælge deres foretrukne indkøbssted. For at tage højde for dette scenario kan brugere gennemse flere websteder ved at bruge modulet til valg af websted. En webstedsvælger anbefales også, når der er implementeret [geografisk registrering og omdirigering](geo-detection-redirection.md) til dit e-handelswebsted, så kunderne kan tilsidesætte den præference for websted, som de angiver ved hjælp af modulet [land/områdevælger](country-region-picker-module.md). 

Modulet til valg af websted skal konfigureres med listen over websteder (markeder, områder eller landestandarder), som brugerne kan gennemse. I følgende illustration vises et eksempel på et modul til valg af websted, der findes i overskriften på en webside.

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
