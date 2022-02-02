---
title: Tilføj en copyright-meddelelse
description: I dette emne beskrives det, hvordan du føjer en copyrightmeddelelse til e-handelswebstedet.
author: psimolin
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4a9a7fed4393f9c35b0bdc765fe7d0723c193f89
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/12/2022
ms.locfileid: "7964750"
---
# <a name="add-a-copyright-notice"></a>Tilføj en copyright-meddelelse

[!include [banner](includes/banner.md)]

I dette emne beskrives det, hvordan du føjer en copyrightmeddelelse til e-handelswebstedet.

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
