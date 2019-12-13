---
title: Aktivér produktanbefalinger
description: I dette emne beskrives, hvordan du kan lave produktanbefalinger, der er baseret på kunstig intelligens-maskinel læring (AI-ML), som er tilgængelig for Microsoft Dynamics 365 Commerce-kunder.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770133"
---
# <a name="enable-product-recommendations"></a>Aktivér produktanbefalinger

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du kan lave produktanbefalinger, der er baseret på kunstig intelligens-maskinel læring (AI-ML), som er tilgængelig for Microsoft Dynamics 365 Commerce-kunder. Yderligere oplysninger om lister over produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Forhåndscheck af anbefalinger
Før du aktiverer anbefalinger, skal du vide, at produktanbefalingerne kun understøttes for Finance and Operations-kunder med 10.0.6, og som har overført deres lager for at bruge BDL. 

Derudover skal du kontrollere, at RetailSale-målinger er aktiveret. Du kan få mere at vide om denne opsætningsproces [her.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)


## <a name="turn-on-recommendations"></a>Aktivere anbefalinger

Benyt følgende fremgangsmåde for at aktivere produktanbefalinger.

1. Gå til **Detail** &gt; **Produktanbefalinger** &gt; **Anbefalingsparametre**.
1. Vælg **Anbefalingslister** på listen over delte detailparametre.
1. Vælg **Ja** i indstillingen **Aktivér anbefalinger**.

![Aktivere produktanbefalinger](./media/enableproductrecommendations.png)

> [!NOTE]
> Denne procedure starter processen til oprettelse af produktanbefalingslister. Der kan være op til flere timer, før listerne er tilgængelige og kan ses på POS eller i Dynamics 365 for Commerce.

## <a name="configure-recommendation-list-parameters"></a>Konfigurere parametre for anbefalingslister
Den AI-ML-baserede produktanbefalingsliste angiver som standard foreslåede værdier. Du kan ændre de foreslåede standardværdier, så de passer til dit firmas flow. Hvis du vil vide mere om, hvordan du ændrer standardparametrene, skal du gå til [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Vise anbefalinger på POS-enheder
Når anbefalingerne er aktiveret i bagkontoret, skal anbefalingspanelet føjes til kontrolpanelet kontrolelementets POS-skærm via layoutværktøjet. Du kan få mere at vide om denne proces [her.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over produktanbefalinger](product-recommendations.md)

[Tilføje lister med produktanbefalinger på sider](add-reco-list-to-page.md)

[Føje anbefalingspanel til POS-enheder](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


