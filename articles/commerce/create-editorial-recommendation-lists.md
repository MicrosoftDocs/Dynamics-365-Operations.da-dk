---
title: Oprette overvågede anbefalinger manuelt
description: I dette emne beskrives, hvordan detailhandlere manuelt kan oprette og administrere produktlister til Microsoft Dynamics 365 Commerce-kunder.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 00f7d076d745cb750dbfdd3a95130196edd888bc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795756"
---
# <a name="manually-create-curated-recommendations"></a>Oprette overvågede anbefalinger manuelt

[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan detailhandlere manuelt kan oprette og administrere produktanbefalinger til Microsoft Dynamics 365 Commerce-kunder.

Overvågede lister er samlinger af individuelt indhold, der er oprettet og overvåges af personer.  

## <a name="create-a-new-list"></a>Opret en ny liste

Hvis du vil oprette en overvåget liste med produktanbefalinger, skal du følge disse trin.

1. Gå til **Retail og Commerce &gt; Produktanbefalinger &gt; Anbefalingslister**.
1. Vælg **Ny**.
1. Angiv en værdi i feltet **Liste-id**.
1. Angiv en værdi i feltet **Listenavn**.
    - **Listenavn** er titlen på den liste, der vil blive vist i sektionen med overvågede lister i modulet **Produktsamling**.
1. Hvis du vil føje produkter til listen, skal du vælge **Tilføj produkter**.
1. Hvis du vil ændre rækkefølgen af produkterne på listen, skal du angive en værdi i kolonnen **Visningsrækkefølge**.
    - Hvis to produkter har samme værdi for visningsrækkefølge, kan den endelige rækkefølge af disse to resultater afvige fra administrationens.
1. Vælg **Gem** for at gemme listen.

## <a name="example-list"></a>Eksempelliste

![Eksempel på overvåget liste i administrationen](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over produktanbefalinger](product-recommendations.md)

[Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktivér produktanbefalinger](enable-product-recommendations.md)

[Aktivere tilpassede anbefalinger](personalized-recommendations.md)

[Fravælge tilpassede anbefalinger](personalization-gdpr.md)

[Aktivere anbefalinger af "Køb tilsvarende"](shop-similar-looks.md)

[Tilføje produktanbefalinger på POS](product.md)

[Føje anbefalinger til transaktionsskærmen](add-recommendations-control-pos-screen.md)

[Justere resultater for AI-ML-anbefalinger](modify-product-recommendation-results.md)

[Oprette anbefalinger med demonstrationsdata](product-recommendations-demo-data.md)

[Ofte stillede spørgsmål om produktanbefalinger](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]