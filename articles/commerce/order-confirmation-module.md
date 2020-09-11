---
title: Modulet Ordredetaljer
description: Dette emne omhandler ordredetaljemoduler og beskriver, hvordan du bruger dem i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 06/18/2020
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
ms.openlocfilehash: 5876b953a3b3d960c106acf37731fde13b93f8e7
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661166"
---
# <a name="order-details-module"></a>Modulet Ordredetaljer

[!include [banner](includes/banner.md)]

Dette emne omhandler ordredetaljemoduler og beskriver, hvordan du bruger dem i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Modulet Ordredetaljer bruges til at vise ordrebekræftelsesoplysningerne, når en ordre er afgivet. Det viser ordrebekræftelses-id, ordrekontaktoplysninger og andre ordreoplysninger, f.eks. de varer, der er købt, betalingsoplysninger og forsendelsesmåde.

## <a name="order-details-module-properties"></a>Egenskaber for ordredetaljemodul

| Egenskabsbetegnelse  | Værdier | Beskrivende tekst |
|----------------|--------|-------------|
| Overskrift        | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Ordredetaljemodulet kan have en overskrift. Overskrift koden **H2** bruges som standard til overskriften. Koden kan dog ændres, så den opfylder tilgængelighedskravene. |
| Kontaktnummer | Text | Der kan angives et kontaktnummer for ordrerelaterede spørgsmål. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Moduler, der kan bruges på en side med ordredetaljer

Når du opretter en side med ordredetaljer, kan du tilføje andre relevante moduler udover modulet Ordredetaljer. Her er nogle eksempler:

- **Anbefalingsmodul** – Anbefalingsmodulet kan tilføjes på ordredetaljesiden for at foreslå andre produkter til kunden.
- **Marketingmoduler** – Ethvert marketingmodul kan føjes til siden Ordredetaljer for at vise marketingindhold.

## <a name="add-an-order-details-module-to-a-page"></a>Føj et ordredetaljemodul til en side

Hvis du vil føje et ordredetaljemodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.
1. Angiv navnet **Ordredetaljeskabelon** under **Skabelonnavn** i dialogboksen **Ny skabelon**, og vælg derefter **OK**.
1. På pladsen **Brødtekst** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Standardside** og derefter **OK**.
1. På pladsen **Hoved** i modulet **Standardside** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Ordredetaljer** og derefter **OK**.
1. Vælg **Gem** og derefter **Vis** for at få vist skabelonen. Ordredetaljemodulet skal ikke gengives, fordi det kræver ordrebekræftelsesnummerets kontekst.
1. Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.
1. Gå til **Sider**, og vælg **Ny** for at oprette en ny side.
1. I dialogboksen **Vælg en skabelon** skal du vælge **Ordredetaljeskabelon**. Under **Sidenavn** skal du angive **Ordredetaljeside** og derefter vælge **OK**.
1. På pladsen **Hoved** i modulet **Standardside** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Ordredetaljer** og derefter **OK**.
1. Vælg **Overskrift** ud for blyantsymbolet i egenskabsruden for ordredetaljemodulet.
1. Angiv overskriftsteksten **Ordredetaljer** i feltet **Overskriftstekst** i dialogboksen **Overskrift**, og vælg derefter **OK**.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Indkøbskurvsmodul](add-cart-module.md)

[Ikonmodul for indkøbskurv](cart-icon-module.md)

[Betalingsmodul](add-checkout-module.md)

[Betalingsmodul](payment-module.md)

[Leveringsadressemodul](ship-address-module.md)

[Leveringsindstillingsmodul](delivery-options-module.md)

[Gavekortsmodul](add-giftcard.md)
