---
title: Forhindre rabatter for detailprodukter
description: "Der er forskellige grunde til, at detailhandlere ønsker at forhindre, at der kan ydes rabat på nogle produkter, enten fra en kampagne eller under et salg på POS."
author: jeffbl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: c124ecf104bdb3de786c9dd98c2b07a4c9c04041
ms.openlocfilehash: 0debfe984a83295dde145fe4b8c2deb836345cd6
ms.contentlocale: da-dk
ms.lasthandoff: 07/31/2017

---

# <a name="prevent-discounts-for-retail-products"></a>Forhindre rabatter for detailprodukter

[!include[banner](includes/banner.md)]

Der er forskellige grunde til, at detailhandlere ønsker at forhindre, at der kan ydes rabat på nogle produkter, enten fra en kampagne eller under et salg på POS.

Følgende indstillinger, som findes under fanen **Retail** for frigivne produkter, tillader, at produktet konfigureres til at forhindre alle eller manuelle rabatter. Indstillingerne kan også angives på kategoriniveau fra detailkategorihierarkiet.

**Forhindre alle rabatter**: Vælg denne indstilling for at forhindre, at alle typer rabatter kan anvendes på dette produkt. Dette omfatter kampagner, f.eks. mix og match, mængde- og tærskelrabatter samt manuelle linje- og transaktionsrabatter, der anvendes under et salg af en POS-bruger.

**Forhindre manuelle rabatter**: Vælg denne indstilling for kun at forhindre de manuelle linje- eller transaktionsrabatter, der anvendes under et salg af en POS-bruger. Produkter, hvor denne indstilling er valgt, er stadig berettiget til kampagner, f.eks. mix og match, og mængde- og tærskelrabatter.

**Bemærk**: Disse indstillinger begrænser ikke pristilsidesættelsen, fordi dette indstiller basisprisen og bliver ikke behandlet som en rabat.  

![feltet forhindre rabatter](/media/prevent-discounts.png)
