---
title: Angiv tilføj produkt til indstillinger for indkøbsvogn
description: Dette emne omhandler indstillinger for "Tilføj produkt til indkøbsvogn" og beskriver, hvordan du kan angiver dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 55b81e7c644f884b052853206f312ac796031600
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479426"
---
# <a name="apply-add-product-to-cart-settings"></a>Angiv tilføj produkt til indstillinger for indkøbsvogn

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emne omhandler indstillinger for **Tilføj produkt til indkøbsvogn** og beskriver, hvordan du kan angiver dem i Microsoft Dynamics 365 Commerce.

Forskellige arbejdsgange understøttes, når et produkt føjes til indkøbsvognen på et Dynamics 365 Commerce-e-handelswebsted. Webstedsbrugeren kan f.eks. blive taget med til indkøbsvognssiden. Alternativt kan brugeren forblive på den aktuelle side, men modtage en besked om, at produktet er føjet til indkøbsvognen.

For at understøtte de forskellige arbejdsgange er feltet **Tilføj produkt til indkøbsvogn** tilgængeligt på **Indstillinger \> Udvidelser** i Commerce-webstedsgenerator. Vælg en af følgende indstillinger for implementering af den tilsvarende arbejdsgang:

- **Naviger til side for indkøbsvogn**, når brugere tilføjer en vare til indkøbsvognen, føres de til siden med indkøbsvogn.
- **Vis besked** - Når brugere tilføjer en vare til indkøbsvognen, vises en bekræftelsesmeddelelse, og de kan fortsætte med at søge på siden produktdetaljer (PDP).
- **Vis min. indkøbsvogn** – Når brugerne føjer en vare til indkøbsvognen, vises indholdet af min indkøbsvogn. Brugerne kan gennemse alle varerne i indkøbsvognen, og de kan fortsætte til kassen, hvis de er klar.
- **Vis beskeder ved hjælp af modulet Beskeder** – Når brugere føjer en vare til indkøbsvognen, bruges beskedmodulet til at vise en bekræftelsesbesked. Hvis denne indstillingsindstilling skal fungere, skal modulet med beskeder føjes til sidehovedet.
- **Naviger ikke til side for indkøbsvogn**, når brugere tilføjer en vare til indkøbsvognen, forbliver de på den aktuelle side.

I følgende illustration vises et eksempel på indstillingerne for **Tilføj produkt til indkøbsvogn** i Site Builder.

![Eksempel på indstillinger for indstillinger for Tilføjelse af produkt til indkøbsvogn i Site Builder](./media/AW_sitesettings.PNG)

> [!IMPORTANT]
> - Indstillingerne for webstedet **Føj produkt til indkøbskurv** er tilgængelige fra Dynamics 365 Commerce version 10.0.11. Hvis du opdaterer fra en ældre version af Dynamics 365 Commerce, skal du opdatere filen appsettings.json manuelt. Oplysninger om opdatering af filen appsettings.json finder du under [Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).
> - Indstillingen **Vis indkøbsvogn** er tilgængelig fra Dynamics 365 Commerce version 10.0.20. Hvis du opdaterer fra en ældre version af Dynamics 365 Commerce, skal du opdatere filen appsettings.json manuelt. Oplysninger om opdatering af filen appsettings.json finder du under [Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

Det følgende billede viser et eksempel på en besked med bekræftelse af handlingen "Føjet til indkøbsvogn" på Fabrikam-webstedet.

![Det følgende billede viser et eksempel på en besked med bekræftelse af handlingen "Føjet til indkøbsvogn" på Fabrikam-webstedet.](./media/ecommerce-addtocart-notifications.PNG)

Det følgende billede viser et eksempel på en besked med bekræftelse af handlingen "Føjet til indkøbsvogn" på Adventure Works-webstedet.

![Det følgende billede viser et eksempel på en besked med bekræftelse af handlingen "Føjet til indkøbsvogn" på Adventure Works-webstedet.](./media/AW_minicart.PNG)

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Boksmodul til køb](add-buy-box.md)

[Butiksvælgermodul](store-selector.md)
