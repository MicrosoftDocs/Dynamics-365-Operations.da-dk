---
title: Hurtig visning-modul
description: Dette emne omhandler hurtig visning-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 5b9bb456659447697b685105fe64b083e01f690a
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351958"
---
# <a name="quick-view-module"></a>Modul til hurtig visning

[!include [banner](includes/banner.md)]

Dette emne omhandler hurtig visning-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

Modulet Hurtig visning giver brugerne mulighed for hurtigt at få vist produktoplysninger, når de gennemser produkter på en listeside, og føje et eller flere produkter til indkøbsvognen fra listesiden uden at skulle gå til siden med produktoplysninger (PDP). Modulet Hurtig visning indeholder en oversigt over de produktoplysninger, som brugerne skal bruge for at træffe en beslutning om tilføjelse af indkøbsvogn. Den giver også et link til PDP, så brugerne kan se yderligere produktoplysninger og købsindstillinger.

Modulet Til hurtig visning understøttes af modulerne [produktsamling](product-collection-module-overview.md) og [søgeresultater](search-result-module.md).

> [!IMPORTANT]
> Modulet Hurtig visning er tilgængeligt efter Commerce-version 10.0.17-udgaven.

Følgende illustration viser et eksempel på et hurtig visning-modul på en produktlisteside.

![Eksempel på et hurtig visning-modul på en produktlisteside.](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a>Modulegenskaber

Modulet Hurtig visning understøtter nogle af de samme funktioner som købsfeltmodulet. Egenskaberne for et modul til hurtig visning svarer derfor til egenskaberne for et købsfeltmodul.

| Egenskab | Værdier | Betegnelse |
|----------------|--------|-------------|
| Overskriftskode | **H1**, **H2**, **H3**, **H4**, **H5** eller **H6** | Denne egenskab definerer overskriftskoden for produkttitlen. Hvis hurtig visning-feltet vises øverst på siden, skal denne egenskab indstilles til **H1** for at overholde tilgængelighedsstandarder. |
| Tillad brugerdefineret pris | **Sand** eller **Falsk** | Hvis denne egenskab er angivet til **Sand**, kan brugeren angive en brugerdefineret pris. |
| Minimumpris | Heltal | Denne egenskab kan kun anvendes, hvis egenskaben **Tillad brugerdefinerede pris** er angivet til **Sand**. Den definerer den minimumspris, som brugeren kan angive (f.eks. $1). |
| Maksimumpris | Heltal | Denne egenskab kan kun anvendes, hvis egenskaben **Tillad brugerdefinerede pris** er angivet til **Sand**. Den definerer den maksimumpris, som brugeren kan angive (f.eks. $1,000). |

## <a name="commerce-site-builder-settings"></a>Indstillinger til Commerce-webstedsgenerator

Ligesom købsfelt-modulet overholder modulet til hurtig visning indstillingerne ved **Indstillinger for websted \> Udvidelser \> Tilføj produkt til indkøbsvogn**. Indstillingen for siden **Naviger til indkøbsvogn** ignoreres dog, da det ikke er i overensstemmelse med formålet med modulet Til hurtig visning, hvilket er at give brugerne mulighed for at gennemse flere produkter på en listeside og føje dem til indkøbsvognen uden at gå fra listesiden.

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a>Føje et hurtig visning-modul til produktsamlingsmodul

Et hurtig visning-modul kan tilføjes til modulerne produktsamling og søgeresultater.

Følg disse trin, hvis du til tilføje et hurtig visning-modul til et produktsamlingsmodul i Commerce-webstedsgenerator.

1. Gå til **Sider**, og vælg derefter startsiden for Fabrikam-webstedet.
1. Gå til **Produktsamling**-modul på startsiden, vælg ellipsen (**...**), og vælg derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Hurtig visning** og derefter **OK**.
1. Vælg **Overskrift** i egenskabsruden i modulet **Hurtig visning**. Angiv feltet **Overskriftsniveau** til **H2** i dialogboksen **Overskrift**, og vælg derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Boksmodul til køb](add-buy-box.md)

[Produktsamlingsmodul](product-collection-module-overview.md)

[Modul til søgeresultater](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
