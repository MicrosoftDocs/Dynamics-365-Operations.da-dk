---
title: Aktivér produktanbefalinger
description: I dette emne beskrives, hvordan du kan lave produktanbefalinger, der er baseret på kunstig intelligens-maskinel læring (AI-ML), som er tilgængelig for Microsoft Dynamics 365 Commerce-kunder.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
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
ms.openlocfilehash: d8a579be5df3c5e7718a6fb4720341f3bd01a64c
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154407"
---
# <a name="enable-product-recommendations"></a>Aktivér produktanbefalinger

[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du kan lave produktanbefalinger, der er baseret på kunstig intelligens-maskinel læring (AI-ML), som er tilgængelig for Microsoft Dynamics 365 Commerce-kunder. Yderligere oplysninger om lister over produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Forhåndscheck af anbefalinger

Før du aktiverer anbefalinger, skal du vide, at produktanbefalingerne kun understøttes for Commerce-kunder, som har overført deres lager for at bruge Azure Data Lake Storage (ADLS). 

Du kan se trinnene til at aktivere i [Sådan aktiveres ADLS i et Dynamics 365-miljø](enable-ADLS-environment.md).

Derudover skal du kontrollere, at RetailSale-målinger er aktiveret. Du kan få mere at vide om denne opsætningsproces [her.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)


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

[Aktivere ADLS i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktivere tilpassede anbefalinger](personalized-recommendations.md)

[Fravælge tilpassede anbefalinger](personalization-gdpr.md)

[Tilføje produktanbefalinger på POS](product.md)

[Føje anbefalinger til transaktionsskærmen](add-recommendations-control-pos-screen.md)

[Justere resultater for AI-ML-anbefalinger](modify-product-recommendation-results.md)

[Oprette overvågede anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Oprette anbefalinger med demonstrationsdata](product-recommendations-demo-data.md)

[Ofte stillede spørgsmål om produktanbefalinger](faq-recommendations.md)

