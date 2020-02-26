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
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024950"
---
# <a name="enable-product-recommendations"></a>Aktivér produktanbefalinger

[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du kan lave produktanbefalinger, der er baseret på kunstig intelligens-maskinel læring (AI-ML), som er tilgængelig for Microsoft Dynamics 365 Commerce-kunder. Yderligere oplysninger om lister over produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Forhåndscheck af anbefalinger

Før du aktiverer anbefalinger, skal du vide, at produktanbefalingerne kun understøttes for Commerce-kunder, som har overført deres lager for at bruge Azure Data Lake Storage (ADLS). 

Du kan se trinnene til at aktivere i [Sådan aktiveres ADLS i et Dynamics 365-miljø](enable-ADLS-environment.md).

Derudover skal du kontrollere, at RetailSale-målinger er aktiveret. Du kan få mere at vide om denne opsætningsproces [her.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)


## <a name="turn-on-recommendations"></a>Aktivere anbefalinger

Benyt følgende fremgangsmåde for at aktivere produktanbefalinger.

1. Gå til **Retail og Commerce &gt; Produktanbefalinger &gt; Anbefalingsparametre**.
1. Vælg **Anbefalingslister** på listen over delte parametre.
1. Vælg **Ja** i indstillingen **Aktivér anbefalinger**.

![Aktivere produktanbefalinger](./media/enableproductrecommendations.png)

> [!NOTE]
> Denne procedure starter processen til oprettelse af produktanbefalingslister. Der kan være op til flere timer, før listerne er tilgængelige og kan ses på POS eller i Dynamics 365 Commerce.

## <a name="configure-recommendation-list-parameters"></a>Konfigurere parametre for anbefalingslister

Den AI-ML-baserede produktanbefalingsliste angiver som standard foreslåede værdier. Du kan ændre de foreslåede standardværdier, så de passer til dit firmas flow. Hvis du vil vide mere om, hvordan du ændrer standardparametrene, skal du gå til [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Vise anbefalinger på POS-enheder

Når anbefalingerne er aktiveret i Commerce-administrationen, skal anbefalingspanelet føjes til kontrolelementets POS-skærm ved hjælp af layoutværktøjet. Du kan få mere at vide om denne proces i [Føje et kontrolelement med anbefalinger til posteringsskærmen på POS-enheder](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Aktivere personlige anbefalinger

Yderligere oplysninger om, hvordan du modtager tilpassede anbefalinger, finder du i [Aktivere personlige anbefalinger](personalized-recommendations.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over produktanbefalinger](product-recommendations.md)

[Aktivere personlige anbefalinger](personalized-recommendations.md)

[Tilføje lister med produktanbefalinger på sider](add-reco-list-to-page.md)

[Føje anbefalingspanel til POS-enheder](add-recommendations-control-pos-screen.md)

[Oversigt over modulet Produktsamling](product-collection-module-overview.md)

[Aktivere ADLS i Dynamics 365-miljøet](enable-ADLS-environment.md)

