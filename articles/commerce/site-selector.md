---
title: Webstedsvælgermodul
description: Dette emne omhandler modulet webstedsvælger og beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/04/2022
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
ms.openlocfilehash: a1954f6b2fea35d5138218e6a2a23ab1fd04c8fc
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710297"
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

Webstedsvælgermodulet kan føjes til pladsen **Webstedsvælger** i [overskriftsmodulet](author-header-module.md). Når et webstedsvælgermodul er tilføjet, kan du definere moduloverskriften og indstillinger for webstedet. Et overskriftsmodul findes generelt i et overskriftsfragment, der kan deles på tværs af e-handelssider for et websted. 

Følg disse trin for at føje et webstedsvælgermodul til et sidehovedmodul.

1. På pladsen **Webstedsvælger** i sidehovedfragmentets sidehovedmodul skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du tilføje et **Webstedsvælger**-modul og derefter vælge **OK**.
1. Vælg **Tilføj liste over webstedsindstillinger** i ruden med egenskaber for **Webstedsvælger**. Der vises en **Liste over webstedsindstillinger**, der kan redigeres.
1. Vælg **Liste over webstedsindstillinger**. Dialogboksen **Liste over webstedsindstillinger** vises.
1. Angiv den tekst for webstedsnavnet, der skal vises på rullelisten til webstedsvælger, under **Navn på sted**.
1. Vælg **Tilføj et link** under **URL-adresse til omdirigeret til websted**. Ruden **Tilføj et link** vises.
1. Vælg **Brugerdefineret side** i ruden **Tilføj et link**, og vælg derefter **Næste**.
1. På listen over URL-adresser skal du vælge URL-adressen med den sti, du oprettede, da du føjer kanalen til webstedet (f.eks. `www.adventure-works.com/fr-ca`), og vælg derefter **Anvend**.
1. Vælg **OK**.
1. Vælg **Gem**, og vælg derefter **Afslut redigering**.
1. Vælg **Publicer** for at publicere siden.

I følgende eksempel er webstedsvælgermodulet føjet til pladsen **Webstedsvælger** i et overskriftsmodul, der er indeholdt i et overskriftsfragment med navnet **HeaderContainer**.

![Eksempel på et modul til valg af websted i et overskriftsfragment.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Sidehovedmodul](author-header-module.md)

[Brødkrummemodul](add-breadcrumb.md)

[Navigationsmenumodul](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
