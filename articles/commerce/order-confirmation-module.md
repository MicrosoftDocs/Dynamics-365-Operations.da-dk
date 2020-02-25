---
title: Modulet Ordredetaljer
description: Dette emne omhandler ordredetaljemoduler og beskriver, hvordan du bruger dem i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026011"
---
# <a name="order-details-module"></a>Modulet Ordredetaljer


[!include [banner](includes/banner.md)]

Dette emne omhandler ordredetaljemoduler og beskriver, hvordan du bruger dem i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Modulet Ordredetaljer bruges til at vise ordrebekræftelsesoplysningerne, når en ordre er afgivet. Det viser ordrebekræftelses-id, ordrekontaktoplysninger og andre ordreoplysninger, f.eks. de varer, der er købt, betalingsoplysninger og forsendelsesmåde.

## <a name="order-confirmation-module-properties"></a>Egenskaber for ordrebekræftelsesmodul

| Egenskabsnavn  | Værdier | Beskrivelse |
|----------------|--------|-------------|
| Overskrift        | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Ordrebekræftelsesmodulet kan have en overskrift. Overskrift koden **H2** bruges som standard til overskriften. Koden kan dog ændres, så den opfylder tilgængelighedskravene. |
| Kontaktnummer | Text | Der kan angives et kontaktnummer for ordrerelaterede spørgsmål. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Moduler, der kan bruges på en side med ordredetaljer

Når du opretter en side med ordredetaljer, kan du tilføje andre relevante moduler udover modulet Ordredetaljer. Her er nogle eksempler:

- **Anbefalingsmodul** – Anbefalingsmodulet kan tilføjes på ordredetaljesiden for at foreslå andre produkter til kunden.
- **Marketingmoduler** – Ethvert marketingmodul kan føjes til siden Ordredetaljer for at vise marketingindhold.

## <a name="create-an-order-details-page-module"></a>Oprette et sidemodul med ordredetaljer

1. Opret en sideskabelon med navnet **Ordredetaljeskabelon**.
1. Tilføj et ordredetaljemodul på **Hoved**-pladsen på standardsiden.
1. Tilføj et anbefalingsmodul i ordredetaljemodulet.
1. Gem skabelonen, og se forhåndsvisningen af den. Ordredetaljemodulet skal ikke gengives, fordi det kræver ordrebekræftelsesnummerets kontekst.
1. Afslut redigeringen af skabelonen, og udgiv den.
1. Brug den ordredetaljeskabelon, som du netop har oprettet, til at oprette en side med navnet **ordredetaljeside**.
1. Føj standardsiden til sidedispositionen.
1. Tilføj et sidehovedfragment på pladsen **Sidehoved**.
1. Tilføj et sidefodsfragment på pladsen **Sidefod**.
1. Tilføj et ordredetaljemodul på **Hoved**-pladsen.
1. Tilføj overskriften **Ordredetaljer** i egenskabsruden i ordredetaljemodulet.
1. Tilføj et anbefalingsmodul under ordredetaljemodulet, og konfigurer det, så det bruger indstillingerne **Ny** og **Bedst sælgende**.
1. Gem siden, og se en forhåndsvisning af den.
1. Afslut redigeringen af siden, og udgiv den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Modulet Container](add-container-module.md)

[Købefeltmodul](add-buy-box.md)

[Indkøbskurvsmodul](add-cart-module.md)

[Betalingsmodul](add-checkout-module.md)

[Sidehovedmodul](author-header-module.md)

[Sidefodsmodul](author-footer-module.md)
