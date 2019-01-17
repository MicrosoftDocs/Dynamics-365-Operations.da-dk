---
title: Muligheder for at forhindre rabatter for detailprodukter
description: "Der er forskellige grunde til, at detailhandlere ønsker at forhindre, at der kan ydes rabat på nogle produkter, enten fra en kampagne eller under et salg på POS."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: c9d3e7af95dffddfddc34059d93a2a5a350d08e5
ms.contentlocale: da-dk
ms.lasthandoff: 01/16/2019

---

# <a name="options-for-preventing-discounts-for-retail-products"></a>Muligheder for at forhindre rabatter for detailprodukter

[!include [banner](includes/banner.md)]

Der er forskellige grunde til, at detailhandlere ønsker at forhindre, at der kan ydes rabat på nogle produkter, enten fra en kampagne eller under et salg på POS.

Følgende indstillinger, som findes under fanen **Retail** for frigivne produkter, tillader, at produktet konfigureres til at forhindre alle eller manuelle rabatter. Indstillingerne kan også angives på kategoriniveau fra detailkategorihierarkiet.

- **Forhindre alle rabatter** – Vælg denne indstilling for at forhindre, at alle typer rabatter kan anvendes på dette produkt. Dette omfatter kampagner, f.eks. mix og match, mængde- og tærskelrabatter samt manuelle linje- og transaktionsrabatter, der anvendes under et salg af en POS-bruger.
- **Forhindre manuelle rabatter** – Vælg denne indstilling for kun at forhindre de manuelle linje- eller transaktionsrabatter, der anvendes under et salg af en POS-bruger. Produkter, hvor denne indstilling er valgt, er stadig berettiget til kampagner, f.eks. mix og match, og mængde- og tærskelrabatter.

> [!NOTE]
> Disse indstillinger begrænser ikke pristilsidesættelsen, fordi dette indstiller basisprisen og bliver ikke behandlet som en rabat.

[![feltet forhindre rabatter](./media/prevent-discounts.png)](./media/prevent-discounts.png)

