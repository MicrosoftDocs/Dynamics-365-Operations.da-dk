---
title: Siden kreditkortindtastning viser en fejl ved kassen
description: Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe dig med, når afsnittet Betalingsmetode ikke indlæses, og viser en fejlmeddelelse.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ea9105481e6c5812565f0d3604906c905bcb5443
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018500"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="f7b2a-103">Siden kreditkortindtastning viser en fejl ved kassen</span><span class="sxs-lookup"><span data-stu-id="f7b2a-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7b2a-104">Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe dig med, når afsnittet **Betalingsmetode** ikke indlæses, og viser en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="f7b2a-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="f7b2a-105">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="f7b2a-105">Description</span></span>

<span data-ttu-id="f7b2a-106">Når du åbner siden til betaling ved kassen i en onlinebutik, er sektionen **Betalingsmetode** ikke indlæst, og følgende fejlmeddelelse vises: "Noget gik galt.</span><span class="sxs-lookup"><span data-stu-id="f7b2a-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="f7b2a-107">Prøv igen senere."</span><span class="sxs-lookup"><span data-stu-id="f7b2a-107">Please try again later."</span></span>

![Betalingsmodulfejl](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="f7b2a-109">Løsning</span><span class="sxs-lookup"><span data-stu-id="f7b2a-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="f7b2a-110">Vent, indtil commerce Scale Unit-cachen udløber</span><span class="sxs-lookup"><span data-stu-id="f7b2a-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="f7b2a-111">Betalingstjenestens indstillinger på betalingstjenestesiden ved kassen i onlinebutikken cachelagres på Commerce Scale Unit og kan tage op til 15 minutter, før de vises på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="f7b2a-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="f7b2a-112">Disse indstillinger for betalingstjeneste omfatter ændringer af forhandlerkonto-id, API-nøgle i skyen og forskellige konfigurationsindstillinger, der er relateret til betalingsmåden.</span><span class="sxs-lookup"><span data-stu-id="f7b2a-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f7b2a-113">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f7b2a-113">Additional resources</span></span>

[<span data-ttu-id="f7b2a-114">Konfigurere en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="f7b2a-114">Set up an online channel</span></span>](../channel-setup-online.md)
