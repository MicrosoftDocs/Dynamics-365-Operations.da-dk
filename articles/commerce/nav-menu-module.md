---
title: Navigationsmenumodul
description: Denne artikel omhandler navigationsmenumoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d58d3957749fa961b7be164a0a474ac90a23321f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281502"
---
# <a name="navigation-menu-module"></a>Navigationsmenumodul

[!include [banner](includes/banner.md)]

Denne artikel omhandler navigationsmenumoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

Det primære formål med navigationsmenumoduler er at give brugerne af webstedet mulighed for at gennemse produkter og websider i henhold til det kanalnavigationshierarki, der er defineret i Dynamics 365 Commerce Headquarters. Elementer, der er konfigureret i et navigationsmenumodul, vises som navigation i webstedets sidehoved. Moduler til navigationsmenuer understøtter også statiske menupunkter med links til andre sider på et e-handels-websted.

Modulet til genvejsmenuen kan føjes til sidens sidehovedmodul. I Fabrikam-temaet viser navigationsmenuen som standard to niveauer. I Starter-temaet viser navigationsmenuen som standard tre niveauer. Hvis du vil ændre antallet af niveauer, skal du bruge en visningsudvidelse på temaet.

I følgende illustration vises et eksempel på en navigationsmenu for Fabrikam-webstedet med to niveauer af kategorihierarki og nogle statiske menupunkter.
![Eksempel på et navigationsmenumodul.](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Egenskaber for navigationsmenumodul

| Egenskabsbetegnelse             | Værdi                 | Betegnelse |
|---------------------------|-----------------------|-------------|
| Kildetekst                  | **Detail**, **Manuel oprettelse**, **Detail og manuel oprettelse** | **Detail**-værdien giver mulighed for at få vist kanalnavigationshierarkiet fra Commerce Headquarters i navigationsmenuen. Værdien af **Manuel oprettelse** tillader, at statiske menupunkter overvåges. Værdien af **Detail og manuel oprettelse** tillader en blanding af begge dele. |
| Vise kategoribilleder | **Sand** eller **Falsk**    | Når denne egenskab er aktiveret, viser kategoribilleder i den navigationsmenu, som er defineret i Commerce Headquarters for hver kategori. Tilføjet i Commerce version 10.0.14. |
| Vis kampagnebilleder | **Sand** eller **Falsk** | Når denne egenskab er aktiveret, kan kampagner konfigureres ved hjælp af billeder, links og tekst. Denne egenskab blev tilføjet i Commerce version 10.0.17-udgaven. |
|Tilføje kategorikampagneindhold | Tekst, billede eller link | Når egenskaben **Vis kampagnebilleder** er aktiveret, kan du tilføje tekst, et billede eller et link som kampagneindhold i navigationsmenuen. |
| Aktivere navigationsmenu på flere niveauer | **Sand** eller **Falsk** | Når denne egenskab er aktiveret, kan navigationsmenuen vise flere niveauer i navigationshierarkiet. Denne funktion er tilgængelig i Commerce version 10.0.15-udgaven. |
| Antal niveauer | heltal | Denne egenskab definerer antallet af niveauer, der skal vises, hvis egenskaben **Aktiver navigationsmenu på flere niveauer** er indstillet til **Sand**. |
| Statisk menupunkt| Matrix af værdier| Statiske menupunkter, der knytter et menupunkts navn til et link til en statisk webside. Du kan oprette menupunkter under andre menupunkter. Som standard vises statiske menuer på rodniveau, og de føjes til kanalnavigationshierarkiet, hvis det findes. |
| Vis rodmenu | **Sand** eller **Falsk** | Når denne egenskab er aktiveret, kan navigationsmenuen defineres under en brugerdefineret rod (f.eks. **Køb nu**). Denne funktion er tilgængelig i version 10.0.15 af Dynamics 365 Commerce. |
| Rodmenu | streng | Denne egenskab kan bruges til at definere tekst for en brugerdefineret rod, hvis egenskaben **Vis rodmenu** er indstillet til **Sand**. |

I følgende illustration vises et eksempel på et kategoribillede, der vises i navigationsmenuen for Fabrikam-webstedet.
![Eksempel på et navigationsmenumodul med kategoribilleder.](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Tilføje et navigationsmenumodul i et sidehovedmodul

Du kan finde flere oplysninger om, hvordan du føjer et navigationsmenumodul til et sidehovedmodul, under [Sidehovedmodul](author-header-module.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Brødkrummemodul](add-breadcrumb.md)

[Webstedsvælgermodul](site-selector.md)

[Boksmodul til køb](add-buy-box.md)

[Cookieoverholdelse](cookie-compliance.md)

[Sidehovedmodul](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
