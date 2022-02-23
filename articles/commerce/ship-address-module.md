---
title: Leveringsadressemodul
description: Dette emne omhandler leveringsadressemodulet og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: aeaa410fde29b285fdbbdd6acac19b0c4e917aa5
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/07/2020
ms.locfileid: "4411241"
---
# <a name="shipping-address-module"></a>Leveringsadressemodul

[!include [banner](includes/banner.md)]

Dette emne beskriver leveringsadressemodulet og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Leveringsadressemodulet giver kunder mulighed for at tilføje eller vælge leveringsadressen for en ordre i betalingsflowet. Hvis en kunde er logget på, vises adresser, der tidligere er blevet gemt for den pågældende kunde, og kunden kan vælge mellem dem. Kunden kan også tilføje en ny adresse. Leveringsadressemodulet bruges til alle varer i en ordre, som kræver levering.

Der kan angives leveringsadresseformater i Commerce Headquarters for hvert land eller område, og leveringsadressemodulet gennemtvinger de lande/områdespecifikke regler.

Når kunder angiver en leveringsadresse i betalingsflowet, har de mulighed for at gemme adressen som en primær adresse. Denne indstilling vises kun, hvis en kunde er logget på.

Selvom leveringsadressemodulet ikke indeholder adressevalidering, kan denne funktion implementeres gennem tilpasning.

Følgende illustration viser et eksempel på et nyt leveringsadressemodul på en betalingsside.

![Eksempel på et leveringsadressemodul på en betalingsside](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>Modulegenskaber

| Egenskabsbetegnelse | Værdier | Betegnelse |
|---------------|--------|-------------|
| Overskrift | Overskriftstekst og en overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | En valgfri overskrift til leveringsadressemodulet. |
| Vis adressetype | **Sand** eller **Falsk** | Hvis denne valgfrie egenskab er angivet til **Sand**, vises en adressetype som f.eks **Privat** eller **Virksomhed**. Hvis der ikke er angivet en adressetype, vil adressen automatisk blive gemt som **Type**=**Anden**. |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a>Føje et leveringsadressemodul til en betalingsside og angive de krævede egenskaber

Et leveringsadressemodul kan kun føjes til et betalignsmodul. Du kan finde flere oplysninger om, hvordan du konfigurerer leveringsadressemodulet og føjer det til en betalingsside, i [Betalingsmodul](add-checkout-module.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Indkøbskurvsmodul](add-cart-module.md)

[Ikonmodul for indkøbskurv](cart-icon-module.md)

[Betalingsmodul](add-checkout-module.md)

[Betalingsmodul](payment-module.md)

[Leveringsindstillingsmodul](delivery-options-module.md)

[Modul med afhentningsoplysninger](pickup-info-module.md)

[Ordredetaljer-modul](order-confirmation-module.md)

[Gavekortsmodul](add-giftcard.md)
