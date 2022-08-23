---
title: Tilføje en copyright-meddelelse
description: Denne artikel beskriver, hvordan du føjer en copyrightmeddelelse til e-handelswebstedet.
author: josaw1
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 044fdd958a7233322553c8d9b03163c6ce5c4cb3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270423"
---
# <a name="add-a-copyright-notice"></a>Tilføje en copyright-meddelelse

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du føjer en copyrightmeddelelse til e-handelswebstedet.

## <a name="prerequisites"></a>Forudsætninger

Før du kan føje en meddelelse om ophavsret til webstedet, skal du have følgende elementer:

- En skabelon, der indeholder et delt sidefodsfragment.
- En side, hvor denne skabelon bruges.

## <a name="add-a-copyright-notice"></a>Tilføj en copyright-meddelelse

Hvis du vil tilføje en meddelelse om ophavsret nederst på alle de sider, der bruger en bestemt skabelon, skal du følge disse trin.

1. Gå til **Fragmenter**, og vælg derefter **Ny**.
1. Vælg modulet **Sidefod** i dialogboksen **Nyt fragment**, og navngiv fragmentet. Du kan f.eks. skrive **Sidefod-ophavsret**.
1. Vælg **OK**.
1. Vælg ellipseknappen (**...**) i navigationsruden ud for **Sidefod**, og vælg derefter **Tilføj modul**.
1. Vælg **Sidefodskategori** i dialogboksen, og vælg derefter **OK**.
1. Vælg ellipseknappen i navigationsruden ud for **Sidefodskategori**, og vælg derefter **Tilføj modul**.
1. Vælg **Tekstblok** i dialogboksen, og vælg derefter **OK**.
1. Vælg **Tekstblok** i navigationsruden.
1. Tilføj meddelelsen om ophavsret i egenskabsruden til højre i feltet **Afsnit**. Angiv f.eks. **(C) Fabrikam 2019**.
1. Vælg **Gem**, vælg **Afslut redigering**, og vælg derefter **Publicer**.
1. Gå til **Skabeloner**, vælg skabelonen, og vælg derefter **Rediger**.
1. Under **Sidedisposition** skal du udvide **Brødtekst** og derefter udvide **Standardside**.
1. Vælg ellipseknappen ud for **Sidefodsplads**, og vælg derefter **Tilføj fragment**.
1. Vælg det fragment, du oprettede tidligere, og vælg derefter **Vælg**.
1. Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.

Den sidefod, der indeholder meddelelsen om ophavsret, vises automatisk nederst på alle de sider, der bruger den valgte skabelon.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilføj et logo](add-logo.md)

[Vælge et tema for webstedet](select-site-theme.md)

[Arbejd med CSS-tilsidesættelsesfiler](css-override-files.md)

[Tilføje en favicon](add-favicon.md)

[Føje sprog til webstedet](add-languages-to-site.md)

[Tilføje scriptkode til sider på websteder for at understøtte telemetri](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
