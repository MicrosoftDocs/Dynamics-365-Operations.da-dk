---
title: Sidefodsmodul
description: Dette emne omhandler sidefodsmoduler og beskriver, hvordan du kan oprette dem i Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 038fee32cbf1ed6b4967f440faaf3c0d4fa583f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979941"
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
1. I dialogboksen **Nyt fragment** skal du vælge modulet **Container**, angive et navn for fragmentet og derefter vælge **OK**.
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

Ved at føje fragmentet til sideskabeloner kan du sikre, at sidefoden gengives på alle sider.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over modulbibliotek](starter-kit-overview.md)

[Container-modul](add-container-module.md)

[Boksmodul til køb](add-buy-box.md)

[Indkøbskurvsmodul](add-cart-module.md)

[Betalingsmodul](add-checkout-module.md)

[Ordrebekræftelsesmodul](order-confirmation-module.md)

[Sidehovedmodul](author-header-module.md)

[Sidefodsmodul](author-footer-module.md)
