---
title: Muligheder for at forhindre rabatter for detailprodukter
description: Der er forskellige grunde til, at detailhandlere ønsker at forhindre, at der kan ydes rabat på nogle produkter, enten fra en kampagne eller under et salg på POS.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f5037067917290f21f681d2446a0e1ab0e31228c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231194"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="94725-103">Muligheder for at forhindre rabatter for detailprodukter</span><span class="sxs-lookup"><span data-stu-id="94725-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="94725-104">Der er forskellige grunde til, at detailhandlere ønsker at forhindre, at der kan ydes rabat på nogle produkter, enten fra en kampagne eller under et salg på POS.</span><span class="sxs-lookup"><span data-stu-id="94725-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="94725-105">Følgende indstillinger, som findes under fanen **Commerce** for frigivne produkter, tillader, at produktet konfigureres til at forhindre alle eller manuelle rabatter.</span><span class="sxs-lookup"><span data-stu-id="94725-105">The following options, which can be found on the **Commerce** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="94725-106">Indstillingerne kan også angives på kategoriniveau fra kategorihierarkiet.</span><span class="sxs-lookup"><span data-stu-id="94725-106">The settings can also be specified at the category level from the category hierarchy.</span></span>

- <span data-ttu-id="94725-107">**Forhindre alle rabatter** – Vælg denne indstilling for at forhindre, at alle typer rabatter kan anvendes på dette produkt.</span><span class="sxs-lookup"><span data-stu-id="94725-107">**Prevent all discounts** – Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="94725-108">Dette omfatter kampagner, f.eks. mix og match, mængde- og tærskelrabatter samt manuelle linje- og transaktionsrabatter, der anvendes under et salg af en POS-bruger.</span><span class="sxs-lookup"><span data-stu-id="94725-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>
- <span data-ttu-id="94725-109">**Forhindre manuelle rabatter** – Vælg denne indstilling for kun at forhindre de manuelle linje- eller transaktionsrabatter, der anvendes under et salg af en POS-bruger.</span><span class="sxs-lookup"><span data-stu-id="94725-109">**Prevent manual discounts** – Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="94725-110">Produkter, hvor denne indstilling er valgt, er stadig berettiget til kampagner, f.eks. mix og match, og mængde- og tærskelrabatter.</span><span class="sxs-lookup"><span data-stu-id="94725-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

> [!NOTE]
> <span data-ttu-id="94725-111">Disse indstillinger begrænser ikke pristilsidesættelsen, fordi dette indstiller basisprisen og bliver ikke behandlet som en rabat.</span><span class="sxs-lookup"><span data-stu-id="94725-111">These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>

<span data-ttu-id="94725-112">[![Felt til forhindring af rabatter](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span><span class="sxs-lookup"><span data-stu-id="94725-112">[![Prevent discounts field](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]