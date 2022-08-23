---
title: Sidefodsmodul
description: Denne artikel omhandler sidefodsmoduler og beskriver, hvordan du kan oprette dem i Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: fefeed37ba0d0e800b9cd3cefcf207cde9a625d8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282951"
---
# <a name="footer-module"></a>Sidefodsmodul  

[!include [banner](includes/banner.md)]

Denne artikel omhandler sidefodsmoduler og beskriver, hvordan du kan oprette dem i Microsoft Dynamics 365 Commerce.

Sidefodsmodulet er en særlig container, der bruges som vært for de moduler, der vises i sidefoden. Det kan f.eks. indeholde hyperlinks til forskellige sider på tværs af webstedet, som f.eks. siderne **Kontakt os** og **Butikspolitikker**.

Det følgende billede viser et eksempel på et sidefodsmodul på en webstedside.

![Eksempel på et sidefodsmodul.](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>Egenskaber for sidefodsmodul 

Som de fleste containere understøtter et sidefodsmodul egenskaber for overskriften og bredden. Det understøtter også tilføjelse af flere sidefodskategorimoduler. Hver af de sidefodskategorimodul, der tilføjes, gengives som en kolonne i sidefodsmodulet.

## <a name="modules-available-in-a-footer-module"></a>Moduler, der er tilgængelige i et sidefodsmodul

**Sidefodselement** – Et sidefodselementmodul kan indeholde enten en overskrift eller et link. Overskriften bruges normalt som en titel til sidefodssektionen.  Alle links i sidefoden kan konfigureres, så de kun har tekst (f.eks. links som "Kontakt os" og "Beskyttelse af personlige oplysninger"), eller så det indeholder både tekst og et billede (f.eks. sociale medielinks). Hvis der både er angivet en overskrift og et link, har overskriftsegenskaben forrang over linket. 

**Tilbage til toppen** – Et tilbage til toppen-modul indeholder et link til hurtig navigation til toppen af siden. Der skal angives en destination. Standarddestinationsværdien er \#, som fører brugeren op til toppen af siden.

## <a name="create-a-footer-module"></a>Opret et sidefodsmodul

1. Gå til **Fragmenter**, og vælg **Nyt** for at oprette et nyt fragment.
1. I dialogboksen **Vælg et fragment** skal du vælge modulet **Container**, angive et navn for fragmentet og derefter vælge **OK**.
1. På pladsen **Standardcontainer** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Sidefodskategori** og derefter **OK**.
1. På pladsen **Sidefodskategori** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Sidefodselement** og derefter **OK**.
1. Vælg pladsen **Sidefodselement**, og konfigurer overskriften, linket og linkteksten samt billede som påkrævet, i egenskabsruden til højre.
1. Gentag hver gang trin 5-7 for at tilføje flere sidefodselementer.
1. Hvis du vil føje et "Tilbage til toppen"-link til din sidefod, skal du vælge ellipsen (**...**) på pladsen **Sidefodskategori** og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Tilbage til toppen** og derefter **OK**.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
