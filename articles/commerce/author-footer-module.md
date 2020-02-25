---
title: Sidefodsmodul
description: Dette emne omhandler sidefodsmoduler og beskriver, hvordan du kan oprette dem i Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f8e0290b5af9d0c1fc9ad0279b0d7f81c9feb2fc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001129"
---
# <a name="footer-module"></a>Sidefodsmodul  


[!include [banner](includes/banner.md)]

Dette emne omhandler sidefodsmoduler og beskriver, hvordan du kan oprette dem i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Sidefodsmodulet er en særlig container, der bruges som vært for de moduler, der vises i sidefoden. Det kan f.eks. indeholde hyperlinks til forskellige sider på tværs af webstedet, som f.eks. siderne **Kontakt os** og **Butikspolitikker**.

## <a name="footer-module-properties"></a>Egenskaber for sidefodsmodul 

Som de fleste containere understøtter et sidefodsmodul egenskaber for overskrift og bredde. Det understøtter også tilføjelse af flere sidefodskategorimoduler. Hver af de sidefodskategorimodul, der tilføjes, gengives som en kolonne i sidefodsmodulet.

## <a name="modules-available-in-a-footer-module"></a>Moduler, der er tilgængelige i et sidefodsmodul

**Sidefodselementer** – Et sidefodselementmodul kan indeholde en overskrift, et billede og et link. Overskriften kan enten bruges alene eller sammen med et billede og et link. Alle links i sidefoden kan konfigureres, så de kun har tekst (f.eks. links som "Kontakt os" og "Beskyttelse af personlige oplysninger"), eller så det indeholder både tekst og et billede (f.eks. sociale medielinks).

**Tilbage til toppen** – Et tilbage til toppen-modul indeholder et link til hurtig navigation til toppen af siden. Der skal angives en destination. Standarddestinationsværdien er #, som fører brugeren op til toppen af siden.

## <a name="author-a-footer-module"></a>Oprette et sidefodsmodul

1. Vælg **Fragmenter** i navigationsruden, og vælg derefter **Nyt sidefragment**.
1. Vælg sidefodsmodulet i dialogboksen **Nyt sidefodsfragment**, angiv et navn til sidefragmentet, og vælg derefter **OK**.
1. Vælg dispositionstræet til venstre, vælg ellipseknappen (**...**) for sidefodsmodulet, og vælg derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge sidefodskategorimodulet og derefter vælge **OK**.
1. Vælg dispositionstræet, vælg ellipseknappen for sidefodskategorien, og vælg derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge sidefodselementmodulet og derefter vælge **OK**.
1. Vælg sidefodselementmodulet i dispositionstræet. I egenskabsruden til højre skal du derefter konfigurere overskriften, linket og linkteksten og billedet, som du ønsker.
1. Gentag trin 5 til 7 for at tilføje flere sidefodselementer.
1. Hvis du vil føje et "Tilbage til toppen"-link til din sidefod, skal du vælge ellipseknappen for sidefodskategorien og derefter vælge **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge Tilbage til toppen-modulet og derefter vælge **OK**.
1. Vælg Tilbage til toppen-modulet i dispositionstræet. Derefter skal du konfigurere Tilbage til toppen-modulet efter behov i egenskabsruden til højre.
1. Gem sidefragmentet, check det ind, og publicer det.

Udfør følgende trin på hver sideskabelon, der er oprettet til webstedet.

1. Tilføj det sidefodsfragment, du har oprettet, i sidefodsmodulet sidefod på **Hoved**-pladsen på standardsiden.
1. Gem skabelonen, tjek den ind, og publicer den.

Ved at føje sidefragmentet til sideskabeloner kan du sikre, at sidefoden gengives på alle sider.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Modulet Container](add-container-module.md)

[Købefeltmodul](add-buy-box.md)

[Indkøbsvognmodul](add-cart-module.md)

[Betalingsmodul](add-checkout-module.md)

[Ordrebekræftelsesmodul](order-confirmation-module.md)

[Sidehovedmodul](author-header-module.md)

[Sidefodsmodul](author-footer-module.md)
