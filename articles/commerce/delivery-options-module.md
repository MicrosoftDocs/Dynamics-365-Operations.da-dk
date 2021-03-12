---
title: Leveringsindstillingsmodul
description: Dette emne omhandler leveringsindstillingsmoduler og forklarer, hvordan du kan konfigurere dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
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
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 9d8945348cbe3255ecc497f129d125ad11e9ceab
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000843"
---
# <a name="delivery-options-module"></a>Leveringsindstillingsmodul

[!include [banner](includes/banner.md)]

Dette emne omhandler leveringsindstillingsmoduler og forklarer, hvordan du kan konfigurere dem i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Leveringsindstillingsmoduler gør det muligt for kunderne at vælge en leveringsmåde, f.eks. forsendelse eller afhentning af deres onlineordre. Der skal angives en leveringsadresse for at bestemme leveringsmåden. Hvis leveringsadressen ændres, skal leveringsindstillingerne hentes igen. Hvis en ordre kun omfatter varer, der afhentes i en butik, skjules dette modul automatisk.

Du kan finde flere oplysninger om, hvordan du konfigurerer leveringsmåder, i [Konfiguration af onlinekanaler](channel-setup-online.md) og [Konfigurer leveringsmåder](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Hver leveringsmåde kan være tilknyttet et gebyr. Du kan få flere oplysninger om, hvordan du konfigurer gebyrer for en onlinebutik, i [Avancerede automatiske gebyrer for omni-kanal](omni-auto-charges.md).

I Commerce version 10.0.13 er leveringsindstillingsmodulet opdateret til at understøtte funktionerne **Hovedgebyrer uden forholdsberegning** og **Levering som et linjegebyr**. Hvis forholdsberegning er deaktiveret, forventes det, at e-Commerce-arbejdsprocessen ikke tillader en blandet leveringsmåde for varerne i indkøbsvognen (dvs. at nogle varer er valgt til levering, mens andre er valgt til afhentning). Funktionen **Hovedgebyrerne uden forholdsberegning** kræver, at flaget **Aktivér ensartet leveringsmåde i kanal** er aktiveret i Commerce Headquarters. Når dette flag er aktiveret, tilskrives der forsendelsesgebyrer enten på hovedniveauet eller linjeniveauet, afhængigt af konfigurationen i Commerce Headquarters.

Fabrikam-temaet understøtter en blandet leveringsmåde, hvor nogle varer er valgt til levering, men andre er valgt til afhentning. I denne tilstand anvendes der forholdsberegning til forsendelsesgebyrer for alle varer, der er valgt til leveringsmåden for forsendelse. For at blandet leveringsmåde kan fungere korrekt, skal du først konfigurere funktionen **Hovedgebyrer med forholdsberegning** i Commerce Headquarters. Yderligere oplysninger om denne konfiguration finder du i [Beregne hovedgebyrer forholdsmæssigt på matchende salgslinjer](pro-rate-charges-matching-lines.md).

Hvis der gælder forsendelsesgebyrer for linjeelementer, kan de vises på indkøbslinjen for hver vare. Denne funktion kræver, at egenskaben **Vis forsendelsesgebyrer på linjeelement** er aktiveret både for indkøbsvognmodulet og betalingsmodulet. Yderligere oplysninger finder du i [Vognmodul](add-cart-module.md) og [Betalingsmodul](add-checkout-module.md).

Følgende illustration viser et eksempel på et leveringsindstillingsmodul på en betalingsside.

![Eksempel på et leveringsindstillingsmodul på en betalingsside](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a>Egenskaber for leveringsindstillingsmodul

| Egenskab | Værdier | Betegnelse |
|----------|--------|-------------|
| Overskrift | Overskriftstekst og en overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | En valgfri overskrift til leveringsindstillingsmodulet. |
| Brugerdefineret CSS-klassenavn | Tekst | Et brugerdefineret klassenavn for overlappende typografiark (CSS), der bruges til at gengive dette modul, hvis det er relevant. |
| Indstilling til filtreret leveringstilstand | **Filtrér ikke** eller **Ingen forsendelsestilstand** | En værdi, der angiver, om leveringsindstillingsmodulet skal filtrere alle leveringsmåder, der ikke er forsendelser. |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a>Føje et leveringsindstillingsmodul til en betalingsside og angive de krævede egenskaber

Et leveringsindstillingsmodul kan kun føjes til et betalignsmodul. Du kan finde flere oplysninger om, hvordan du konfigurerer leveringsindstillingsmodulet og føjer det til en betalingsside, i [Betalingsmodul](add-checkout-module.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Indkøbskurvsmodul](add-cart-module.md)

[Betalingsmodul](add-checkout-module.md)

[Betalingsmodul](payment-module.md)

[Leveringsadressemodul](ship-address-module.md)

[Modul med afhentningsoplysninger](pickup-info-module.md)

[Ordredetaljer-modul](order-confirmation-module.md)

[Gavekortsmodul](add-giftcard.md)

[Konfiguration af onlinekanal](channel-setup-online.md)

[Avancerede automatiske gebyrer for omni-kanal](omni-auto-charges.md)

[Beregne hovedgebyrer forholdsmæssigt på matchende salgslinjer](pro-rate-charges-matching-lines.md)

[Konfigurer leveringsmåder](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
