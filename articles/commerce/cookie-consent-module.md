---
title: Modul til cookie-samtykke
description: Denne artikel omhandler cookie-samtykkemoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.openlocfilehash: 8ca4cc1ffcf8229589591dce6e4666b78bba3890
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276260"
---
# <a name="cookie-consent-module"></a>Modul til cookie-samtykke

[!include [banner](includes/banner.md)]

Denne artikel omhandler cookie-samtykkemoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

Cookie-samtykkemodulet beder brugerne af webstedet om udtrykkeligt at give samtykke til at tillade cookies for enhver funktion eller ethvert modul, der registrerer browsercookies. Samtykket kræves, første gang en bruger besøger et websted i en ny browsersession. Når samtykke er modtaget, registreres det, og brugeren bliver ikke bedt om samtykke igen. Du kan få flere oplysninger under [Cookieoverholdelse](cookie-compliance.md).

Hvis webstedets cookie-samtykke ikke modtages fra en bruger, gengives alle funktioner eller moduler, der kræver cookie-samtykke, ikke på siden. F.eks. kræver betalingsmodulet, modulet til social deling og funktionen foretrukken butik alle cookie-samtykke og gengives ikke, hvis webstedets brugersamtykke ikke modtages. 

Der kan konfigureres et cookie-samtykkemodul i sidens sidehovedfragment, så det kan gennemtvinges, når siden indlæses. Modulet til cookie-samtykke skal have en klar meddelelse, der oplyser brugeren om cookie-anvendelse på webstedet, og skal indeholde et link til webstedets side om beskyttelse af personlige oplysninger.

I følgende illustration fremhæves et eksempel på en meddelelse om cookie-samtykke med et link til webstedets side med politik om beskyttelse af personlige oplysninger, der vises i sidehovedet på en webside.
![Eksempel på et modul til cookie-samtykke.](./media/ecommerce-cookieconsent.png)

## <a name="cookie-consent-module-properties"></a>Egenskaber for cookie-samtykkemodul

| Egenskabsbetegnelse             | Værdi                 | Betegnelse |
|---------------------------|-----------------------|-------------|
| RTF                  | RTF | Angiver en RTF-besked til webstedsbrugere om, at webstedet bruger browsercookies, og at brugerne skal acceptere brugen af cookies, så webstedet fungerer fuldt ud. |
| Links | URL | En eller flere links kan føjes til et websteds oplysninger om beskyttelse af personlige oplysninger, der beskriver de typer cookies, der spores på webstedet. |

## <a name="add-a-cookie-consent-module-to-site-pages"></a>Tilføje et modul til cookie-samtykke på websider

Hvis du effektivt vil føje et modul til cookie-samtykke til flere websider, kan det føjes til et delt sidehovedfragment. Når sidehovedet er føjet til alle websiderne, gengives der automatisk en besked om cookie-samtykke, første gang en webstedsbruger navigerer til en webside.

Yderligere oplysninger om sidehovedfragmenter og moduler finder du i [Sidehovedmodul](author-header-module.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over modulbibliotek](starter-kit-overview.md)

[Overskriftsmodul](author-header-module.md) 

[Cookieoverholdelse](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
