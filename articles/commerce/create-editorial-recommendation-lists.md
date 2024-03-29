---
title: Oprette overvågede anbefalinger manuelt
description: Denne artikel beskriver, hvordan detailhandlere manuelt kan oprette og administrere produktlister til Microsoft Dynamics 365 Commerce-kunder.
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
ms.openlocfilehash: e1a1b402165c5cb35696cf1cf6630770ad07508a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892672"
---
# <a name="manually-create-curated-recommendations"></a>Oprette overvågede anbefalinger manuelt

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan detailhandlere manuelt kan oprette og administrere produktanbefalinger til Microsoft Dynamics 365 Commerce-kunder.

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

![Eksempel på overvåget liste i administrationen.](./media/examplecuratedrecolist.png)

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