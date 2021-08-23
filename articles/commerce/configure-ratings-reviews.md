---
title: Konfigurere vurderinger og anmeldelser
description: I dette emne beskrives, hvordan du konfigurerer dit e-handels-websted, så det kan vise kundevurderinger og -anmeldelser i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fe40807338c32fbaff2df11975bbcb2d7fefeb842f5fd85d7421552556465178
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718750"
---
# <a name="configure-ratings-and-reviews"></a>Konfigurere vurderinger og anmeldelser

[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du konfigurerer dit e-handels-websted, så det kan vise kundevurderinger og -anmeldelser i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Vurderinger og anmeldelser på e-Commerce-websteder gør det lettere for kunder at få oplysninger om produkter, før de træffer en beslutning om køb, fordi de kan se, hvad andre kunder mener om disse produkter. På e-handelswebsteder fungerer vurderinger og anmeldelser også som en mekanisme til indsamling af kundefeedback om produkter. 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Konfigurere et websted til visning af vurderinger og anmeldelser

Konfigurationsværdier for vurderinger og anmeldelser, f.eks. leje-ID, anmeldelsers tekstlængde og længden af titler på anmeldelser, konfigureres på webstedsniveau. 

Udfør følgende trin for at konfigurere et websted til at vise vurderinger og anmeldelser. 

1. Gå til **Startside \> Websteder**.
1. Vælg navnet på dit websted. 
1. Gå til **Webstedsindstillinger \> Udvidelser**. 
1. Angiv det maksimale antal tegn som anmeldelsesteksten må have (f.eks. **1000**) i feltet **Anmeldelsens maksimale tekstlængde**. 
1. Angiv det maksimale antal tegn som anmeldelsestitler må have (f.eks. **55**) i feltet **Maksimal længde af anmeldelsestitel**. 
1. Vælg **Gem og udgiv**. 

I følgende illustration vises, hvordan denne konfiguration ser ud i Dynamics 365 Commerce.

![Konfiguration af et websted til visning af vurderinger og anmeldelser.](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>Sammenkæde en produktvurdering med anmeldelsessektionen på en PDP

En produktvurdering vises under produkttitlen øverst på PDP. Produktvurderingen kan konfigureres, så den sammenkædes med sektionen **Anmeldelser** på samme PDP. 

Hvis du vil knytte en produktvurdering til sektionen **Anmeldelser** på PDP'en, skal du følge disse trin.

1. Åbn PDP-skabelonen. 
1. Gå til **Indstillinger for købefeltcontainermodul**.
1. Vælg **Produktvurderinger** under **Købefelt**, og markér derefter afkrydsningsfeltet **Sammenkæd klik til modul med hele anmeldelsen**.

I følgende illustration vises, hvordan denne konfiguration ser ud i Dynamics 365 Commerce.

![Sammenkædning af en produktvurdering med anmeldelsessektionen på en PDP.](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>Konfigurere linket til siden til beskyttelse af personlige oplysninger og politik

Følg disse trin for at konfigurere linket til siden om beskyttelse af personlige oplysninger og politik.

1. Gå til **Startside \> Websteder**.
1. Vælg navnet på dit websted. 
1. Gå til **Webstedsindstillinger \> Udvidelser**.
1. Vælg **Tilføj et link** under **RNR - beskyttelse af personlige oplysninger og politik** under fanen **Ruter**. Hvis der allerede er angivet et link, og du vil erstatte det, skal du markere linket. 
1. Vælg linket til siden om beskyttelse af personlige oplysninger og politik i dialogboksen **Tilføj et link**, og vælg derefter **OK**. 
1. Vælg **Gem og udgiv**. 

I følgende illustration vises, hvordan denne konfiguration ser ud i Dynamics 365 Commerce.

![Konfiguration af linket til siden til beskyttelse af personlige oplysninger og politik.](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a>Konfigurer vurderings- og anmeldelsesmoduler på sider med produktdetaljer

For yderligere oplysninger om konfiguration af vurderings- og anmeldelsesmoduler på sider med produktdetaljer se [Vurderings- og anmeldelsesmoduler](ratings-reviews-modules.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over vurderinger og anmeldelser](ratings-reviews-overview.md)

[Tilvælge brug af vurderinger og anmeldelser](opt-in-ratings-reviews.md)

[Administrere vurderinger og anmeldelser](manage-reviews.md)

[Konfigurer vurderings- og anmeldelsesmoduler på sider med produktdetaljer](ratings-reviews-modules.md)

[Synkronisere produktvurderinger i Dynamics 365 Retail](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]