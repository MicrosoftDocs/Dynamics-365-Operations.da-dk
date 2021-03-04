---
title: Ordrebekræftelsesmodul
description: Dette emne omhandler ordrebekræftelsesmoduler og beskriver, hvordan du kan bruge dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bf33ebf9c0c5136f40fcd7e1012988d186c4169b
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/07/2020
ms.locfileid: "4411243"
---
# <a name="order-confirmation-module"></a>Ordrebekræftelsesmodul

[!include [banner](includes/banner.md)]

Dette emne omhandler ordrebekræftelsesmoduler og beskriver, hvordan du kan bruge dem i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Ordrebekræftelsesmodulet bruges til at vise ordrebekræftelsesoplysningerne, når en ordre er afgivet. Det viser ordrebekræftelses-id, ordrekontaktoplysninger og andre ordreoplysninger, f.eks. de varer, der er købt, afhentningsoplysninger og forsendelsesmåde.

## <a name="order-confirmation-module-properties"></a>Egenskaber for ordrebekræftelsesmodul

| Egenskabsnavn  | Værdier | Beskrivelse |
|----------------|--------|-------------|
| Overskrift        | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Ordrebekræftelsesmodulet kan have en overskrift. Overskrift koden **H2** bruges som standard til overskriften. Koden kan dog ændres, så den opfylder tilgængelighedskravene. |
| Kontaktnummer | Text | Der kan angives et kontaktnummer for ordrerelaterede spørgsmål. |
| Vis oplysninger om tidsinterval for afhentning | Sand eller falsk | Denne egenskab er tilgængelig i Dynamics 365 Commerce 10.0.15 og nyere. Hvis sand, vises de afhentede oplysninger om tidsintervallet for afhentningen, hvis de er tilgængelige for en vare, der skal afhentes|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a>Moduler, der kan bruges på en ordrebekræftelsesside

Når du opretter en ordrebekræftelsesside, kan du tilføje andre relevante moduler udover ordrebekræftelsesmodulet. Her er nogle eksempler:

- **Anbefalingsmodul** – Anbefalingsmodulet kan tilføjes på ordrebekræftelsessiden for at foreslå andre produkter til kunden.
- **Marketingmoduler** – Ethvert marketingmodul kan føjes til ordrebekræftelsessiden for at vise marketingindhold.

## <a name="add-an-order-confirmation-module-to-a-page"></a>Føj et ordrebekræftelsesmodul til en side

Hvis du vil føje et ordrebekræftelsesmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.
1. Angiv navnet **Ordrebekræftelsesskabelon** under **Skabelonnavn** i dialogboksen **Ny skabelon**, og vælg derefter **OK**.
1. På pladsen **Brødtekst** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Standardside** og derefter **OK**.
1. På pladsen **Hoved** i modulet **Standardside** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Ordrebekræftelse** og derefter **OK**.
1. Vælg **Gem** og derefter **Vis** for at få vist skabelonen. Ordrebekræftelsesmodulet bliver ikke gengivet, fordi det kræver ordrebekræftelsesnummerets kontekst.
1. Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.
1. Gå til **Sider**, og vælg **Ny** for at oprette en ny side.
1. I dialogboksen **Vælg en skabelon** skal du vælge **Ordrebekræftelsesskabelon**. Under **Sidenavn** skal du angive **Ordrebekræftelsesside** og derefter vælge **OK**.
1. På pladsen **Hoved** i modulet **Standardside** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Ordrebekræftelse** og derefter **OK**.
1. Vælg **Overskrift** ud for blyantsymbolet i egenskabsruden for ordrebekræftelsesmodulet.
1. Angiv overskriftsteksten **Ordrebekræftelse** i feltet **Overskriftstekst** i dialogboksen **Overskrift**, og vælg derefter **OK**.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Indkøbskurvsmodul](add-cart-module.md)

[Ikonmodul for indkøbskurv](cart-icon-module.md)

[Betalingsmodul](add-checkout-module.md)

[Betalingsmodul](payment-module.md)

[Leveringsadressemodul](ship-address-module.md)

[Leveringsindstillingsmodul](delivery-options-module.md)

[Modul med afhentningsoplysninger](pickup-info-module.md)

[Gavekortsmodul](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]