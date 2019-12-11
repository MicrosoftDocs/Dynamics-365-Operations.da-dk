---
title: Ordrebekræftelsesmodul
description: Dette emne omhandler ordrebekræftelsesmoduler og beskriver, hvordan du kan oprette dem i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698320"
---
# <a name="order-confirmation-module"></a>Ordrebekræftelsesmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne omhandler ordrebekræftelsesmoduler og beskriver, hvordan du kan oprette dem i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Et ordrebekræftelsesmodul bruges til at vise en bekræftelsesmeddelelse på en ordrebekræftelsesside, når en ordre er afgivet. Ordrebekræftelsesmodulet viser ordrebekræftelsesnummeret og den kundemailadresse, der blev oplyst under betalingen.

Når en ordre afgives under betalingen, overføres ordrebekræftelsesnummeret og kundens mailadresse til ordrebekræftelsessiden som en forespørgselsstreng i sidens URL-adresse. Ordrebekræftelsesmodulet modtager disse oplysninger og gengiver ordrestatus på ordrebekræftelsessiden. Ordrebekræftelsesmodulet kræver, at denne sidekontekst angiver ordrens status.

## <a name="order-confirmation-module-properties"></a>Egenskaber for ordrebekræftelsesmodul

| Egenskabsbetegnelse | Værdier | Beskrivelse |
|---------------|--------|-------------|
| Overskrift       | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Ordrebekræftelsesmodulet kan have en overskrift. Overskrift koden **H2** bruges som standard til overskriften. Koden kan dog ændres, så den opfylder tilgængelighedskravene. |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a>Moduler, der kan bruges i et ordrebekræftelsessidemodul 

- **Anbefalinger** – Anbefalingsmodulet kan placeres på ordrebekræftelsessiden for at foreslå andre produkter til kunden.
- **Marketing** – Marketingmodulet kan føje marketingindhold til ordrebekræftelsessiden.

## <a name="create-an-order-confirmation-page-module"></a>Oprette et ordrebekræftelsessidemodul

1. Opret en sideskabelon med navnet **ordrebekræftelsesskabelon**.
1. Tilføj et ordrebekræftelsesmodul på **Hoved**-pladsen på standardsiden.
1. Tilføj et anbefalingsmodul i ordrebekræftelsesmodulet.
1. Gem skabelonen, og se forhåndsvisningen af den. Ordrebekræftelsesmodulet skal ikke gengives, fordi det kræver ordrebekræftelsesnummerets kontekst.
1. Tjek skabelonen ind, og publicer den.
1. Brug den ordrebekræftelsesskabelon, som du netop har oprettet, til at oprette en side med navnet **ordrebekræftelsesside**.
1. Føj standardsiden til sidedispositionen.
1. Tilføj et sidehovedfragment på pladsen **Sidehoved**.
1. Tilføj et sidefodsfragment på pladsen **Sidefod**.
1. Tilføj et ordrebekræftelsesmodul på **Hoved**-pladsen.
1. Tilføj overskriften **Ordrebekræftelse** i egenskabsruden i ordrebekræftelsesmodulet.
1. Tilføj et anbefalingsmodul under ordrebekræftelsesmodulet, og konfigurer det, så det bruger indstillingerne **Ny** og **Bedst sælgende**.
1. Gem siden, og se en forhåndsvisning af den, check den ind, og publicer den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Modulet Container](add-container-module.md)

[Købefeltmodul](add-buy-box.md)

[Indkøbskurvsmodul](add-cart-module.md)

[Betalingsmodul](add-checkout-module.md)

[Sidehovedmodul](author-header-module.md)

[Sidefodsmodul](author-footer-module.md)
