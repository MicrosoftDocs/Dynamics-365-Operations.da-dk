---
title: Sidefodsmodul
description: Dette emne omhandler sidefodsmoduler og beskriver, hvordan du kan oprette dem i Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: e81617979a945274500c9f4ceaa8078d8dfd79e8
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686712"
---
# <a name="footer-module"></a>Sidefodsmodul  

[!include [banner](includes/banner.md)]

Dette emne omhandler sidefodsmoduler og beskriver, hvordan du kan oprette dem i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Sidefodsmodulet er en særlig container, der bruges som vært for de moduler, der vises i sidefoden. Det kan f.eks. indeholde hyperlinks til forskellige sider på tværs af webstedet, som f.eks. siderne **Kontakt os** og **Butikspolitikker**.

Det følgende billede viser et eksempel på et sidefodsmodul på en webstedside.

![Eksempel på et sidefodsmodul](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>Egenskaber for sidefodsmodul 

Som de fleste containere understøtter et sidefodsmodul egenskaber for overskriften og bredden. Det understøtter også tilføjelse af flere sidefodskategorimoduler. Hver af de sidefodskategorimodul, der tilføjes, gengives som en kolonne i sidefodsmodulet.

## <a name="modules-available-in-a-footer-module"></a>Moduler, der er tilgængelige i et sidefodsmodul

**Sidefodselementer** – Et sidefodselementmodul kan indeholde en overskrift, et billede og et link. Overskriften kan enten bruges alene eller sammen med et billede og et link. Alle links i sidefoden kan konfigureres, så de kun har tekst (f.eks. links som "Kontakt os" og "Beskyttelse af personlige oplysninger"), eller så det indeholder både tekst og et billede (f.eks. sociale medielinks).

**Tilbage til toppen** – Et tilbage til toppen-modul indeholder et link til hurtig navigation til toppen af siden. Der skal angives en destination. Standarddestinationsværdien er \#, som fører brugeren op til toppen af siden.

## <a name="create-a-footer-module"></a>Opret et sidefodsmodul

1. Gå til **Fragmenter**, og vælg **Nyt** for at oprette et nyt fragment.
1. I dialogboksen **Nyt sidefragment** skal du vælge modulet **Container**, angive et navn for sidefragmentet og derefter vælge **OK**.
1. På pladsen **Standardcontainer** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Sidefodskategori** og derefter **OK**.
1. På pladsen **Sidefodskategori** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Sidefodselement** og derefter **OK**.
1. Vælg pladsen **Sidefodselement**, og konfigurer overskriften, linket og linkteksten samt billede som påkrævet, i egenskabsruden til højre.
1. Gentag hver gang trin 5-7 for at tilføje flere sidefodselementer.
1. Hvis du vil føje et "Tilbage til toppen"-link til din sidefod, skal du vælge ellipsen (**...**) på pladsen **Sidefodskategori** og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Tilbage til toppen** og derefter **OK**.
1. Vælg pladsen **Tilbage til toppen**, og konfigurer teksten og andre modulegenskaber som påkrævet, i egenskabsruden til højre.
1. Vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.

Du kan medvirke til at sikre, at der vises et sidehoved på hver side, ved at følge disse trin i hver sideskabelon, der oprettes for webstedet.

1. På pladsen **Sidefod** i modulet **Standardside** skal du tilføje det sidefodsfragment, som du har oprettet.
1. Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.

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
