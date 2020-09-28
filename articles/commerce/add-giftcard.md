---
title: Gavekortmodul
description: I dette emne dækkes gavekortmoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4cc947b9d6f3cfa51bce2155170c49e9529d0f7d
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761075"
---
# <a name="gift-card-module"></a>Gavekortmodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

I dette emne dækkes gavekortmoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Gavekortmoduler kan bruges i betalingsmoduler til at acceptere gavekort og er en almindelig betalingsform i e-handelstransaktioner. Gavekortmodulet understøtter Dynamics 365-, SVS- og Givex-gavekort. SVS- og Givex-gavekort indløses via betalingsudbyderen Adyen. Du kan se flere oplysninger om understøttelse af eksterne gavekort som f.eks. SVS og Givex i emnet [Understøttelse af eksterne gavekort](./dev-itpro/gift-card.md).

Der er to tilgængelige gavekortmoduler:

- **Gavekort** - Dette modul kan bruges på en betalingsside til at indløse et gavekort som betalingsmiddel. 
- **Saldokontrol af gavekort** – Dette modul kan bruges på en hvilken som helst side til at kontrollere saldoen på et gavekort. Dette modul er tilgængeligt i Commerce version 10.0.14 og nyere.

Det følgende billede viser et eksempel på et gavekortmodul på en betalingsside.

![Eksempel på et gavekortmodul](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>Modulegenskaber

- **Vis yderligere felter** – Denne egenskab definerer, hvilke felter der skal vises for gavekort ud over gavekortnummeret, der altid vises som standard. Nogle gavekort understøtter f.eks. visning af en pinkode, og andre understøtter visning af en pinkode og udløbsdato. Denne egenskab kan også angives til "Ingen", hvilket kun viser gavekortnummeret og ingen yderligere felter.

Understøttede værdier:
-   Pinkode
-   Udløbsdato
-   Pinkode og udløbsdato 
-   None

## <a name="site-settings-for-gift-card-modules"></a>Indstillinger for websted for gavekortmoduler

I Commerce-webstedsgenerator under **Indstillinger for websted \> Udvidelser**er der en indstilling for gavekortmodulet, der kaldes **Understøttet gavekorttype**. Denne indstilling understøtter tre værdier:
- **Dynamics 365-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet kun indløsningen af Dynamics 365-gavekort. Denne indstilling understøttes kun for brugere, der er logget på e-handelswebstedet.
- **SVS- og Givex-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet kun indløsningen af SVS- og Givex-gavekort. Denne indstilling understøttes for anonyme brugere og brugere, der er logget på e-handelswebstedet.
- **Dynamics 365-, SVS- og Givex-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet indløsningen af Dynamics 365-, Givex- og SVS-gavekort. Denne indstilling understøttes kun for brugere, der er logget på e-handelswebstedet.

## <a name="add-a-gift-card-module-to-a-page"></a>Føje et gavekortmodul til en side

Du kan få flere oplysninger om, hvordan du føjer et gavekortmodul til en betalingsside og angiver de påkrævede egenskaber, i [Betalingsmodul](add-checkout-module.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Indkøbskurvsmodul](add-cart-module.md)

[Ikonmodul for indkøbskurv](cart-icon-module.md)

[Betalingsmodul](add-checkout-module.md)

[Betalingsmodul](payment-module.md)

[Leveringsadressemodul](ship-address-module.md)

[Leveringsindstillingsmodul](delivery-options-module.md)

[Ordredetaljer-modul](order-confirmation-module.md)

[Understøttelse af eksterne gavekort](./dev-itpro/gift-card.md)
