---
title: Navigationsmenumodul
description: Dette emne omhandler navigationsmenumoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 91239bd1db3f5819b7ad8d45ccfd8ab0d88b1b41
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817868"
---
# <a name="navigation-menu-module"></a>Navigationsmenumodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emne omhandler navigationsmenumoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Det primære formål med navigationsmenumoduler er at give brugerne af webstedet mulighed for at gennemse produkter og websider i henhold til det kanalnavigationshierarki, der er defineret i Dynamics 365 Commerce Headquarters. Elementer, der er konfigureret i et navigationsmenumodul, vises som navigation i webstedets sidehoved. Moduler til navigationsmenuer understøtter også statiske menupunkter med links til andre sider på et e-handels-websted.

Modulet til genvejsmenuen kan føjes til sidens sidehovedmodul. I Fabrikam-temaet viser navigationsmenuen som standard to niveauer. I Starter-temaet viser navigationsmenuen som standard tre niveauer. Hvis du vil ændre antallet af niveauer, skal du bruge en visningsudvidelse på temaet.

I følgende illustration vises et eksempel på en navigationsmenu for Fabrikam-webstedet med to niveauer af kategorihierarki og nogle statiske menupunkter.
![Eksempel på et navigationsmenumodul](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Egenskaber for navigationsmenumodul

| Egenskabsbetegnelse             | Værdi                 | Beskrivelse |
|---------------------------|-----------------------|-------------|
| Kildetekst                  | **Detail**, **Manuel oprettelse**, **Detail og manuel oprettelse** | **Detail**-værdien giver mulighed for at få vist kanalnavigationshierarkiet fra Commerce Headquarters i navigationsmenuen. Værdien af **Manuel oprettelse** tillader, at statiske menupunkter overvåges. Værdien af **Detail og manuel oprettelse** tillader en blanding af begge dele. |
| Vise kategoribilleder | **Sand** eller **Falsk**    | Når denne egenskab er aktiveret, viser kategoribilleder i den navigationsmenu, som er defineret i Commerce Headquarters for hver kategori. Tilføjet i Commerce version 10.0.14. |
| Statisk menupunkt| Matrix af værdier| Statiske menupunkter, der knytter et menupunkts navn til et link til en statisk webside. Du kan oprette menupunkter under andre menupunkter. Som standard vises statiske menuer på rodniveau, og de føjes til kanalnavigationshierarkiet, hvis det findes. |

I følgende illustration vises et eksempel på et kategoribillede, der vises i navigationsmenuen for Fabrikam-webstedet.
![Eksempel på et navigationsmenumodul med kategoribilleder](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Tilføje et navigationsmenumodul i et sidehovedmodul

Du kan finde flere oplysninger om, hvordan du føjer et navigationsmenumodul til et sidehovedmodul, under [Sidehovedmodul](author-header-module.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over modulbibliotek](starter-kit-overview.md)

[Boksmodul til køb](add-buy-box.md)

[Cookieoverholdelse](cookie-compliance.md)

[Overskriftsmodul](author-header-module.md)
