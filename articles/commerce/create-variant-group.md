---
title: Opret en variantgruppe
description: Dette emne beskriver, hvordan du opretter en størrelses-, typografi- eller farvevariantgruppe for et produkt i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b47f38375fc8925288db36f066ed7820bab3fe9b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353150"
---
# <a name="create-a-variant-group"></a>Oprette en variantgruppe


[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du opretter en størrelses-, typografi- eller farvevariantgruppe for et produkt i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Dynamics 365 Commerce understøtter flere varianter for produkter. Det er ideelt at konfigurere variantgrupper for forskellige produktkategorier. Der kan f.eks. oprettes en størrelsesgruppe for t-shirts med størrelserne extra small, small, medium, large og extra large, eller der oprettes en farvegruppe for at medtage alle de tilgængelige farver for et produkt. Variantgrupper skal tilføjes, før der tilføjes produkter.

I dette emne oprettes og konfigureres en størrelsesgruppe. Lignende procedurer kan bruges til at tilføje og konfigurere typografigrupper og farvegrupper.

## <a name="create-a-size-group"></a>Oprette en størrelsesgruppe

Du kan oprette størrelsesgruppe ved at følge disse trin.
 
1. Gå til **Moduler \> Retail og Commerce \> Produkter og kategorier \> Variantgrupper \> Størrelsesgrupper** i navigationsruden.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv et navn til størrelsesgruppen i feltet **Størrelsesgruppe**.
1. Angiv eventuelt en passende beskrivelse i feltet **Beskrivelse**.
1. Gå til handlingsruden, og vælg **Gem**.

## <a name="add-attributes-to-the-size-group"></a>Føje attributter til størrelsesgruppen

Følg disse trin for at føje attributter til en størrelsesgruppe.

1. Gå til **Moduler \> Retail og Commerce \> Produkter og kategorier \> Variantgrupper \> Størrelsesgrupper** i navigationsruden.
1. Vælg en størrelsesgruppe i navigationsruden.
1. Vælg **Tilføj** under **Størrelsesgruppelinjer** .
1. Angiv en streng, der repræsenterer størrelsen (f.eks. "XL"), i feltet **Størrelse**.
1. Angiv et navn til størrelsen (f.eks. "Extra Large") i feltet **Størrelse**.
1. Angiv et nummer, der repræsenterer genopfyldningsvægten, i feltet **Genopfyldningsvægt**.
1. Angiv et nummer, der repræsenterer stregkoden, i feltet **Nummer i stregkode**.
1. Angiv et nummer, der repræsenterer visningsrækkefølgen, i feltet **Visningsrækkefølge**.
1. Vælg **Gem** i handlingsruden, når du er færdig med at tilføje størrelser.

Følgende billede viser et eksempel på en størrelsesgruppe til "størrelser på fritids-t-shirt".

![Oprette størrelsesgruppe.](media/create-variant-group.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over produktoplysninger](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[Konfigurere detailprodukter](set-up-retail-products.md)

[Produktdimensioner](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]