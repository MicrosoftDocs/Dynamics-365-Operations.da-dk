---
title: Siden kreditkortindtastning viser en fejl ved kassen
description: Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe dig med, når afsnittet Betalingsmetode ikke indlæses, og viser en fejlmeddelelse.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: f0751fc76e6eb4320f766886b4c1efcb1042e996
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585244"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="fa4b8-103">Siden kreditkortindtastning viser en fejl ved kassen</span><span class="sxs-lookup"><span data-stu-id="fa4b8-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fa4b8-104">Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe dig med, når afsnittet **Betalingsmetode** ikke indlæses, og viser en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="fa4b8-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="fa4b8-105">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="fa4b8-105">Description</span></span>

<span data-ttu-id="fa4b8-106">Når du åbner siden til betaling ved kassen i en onlinebutik, er sektionen **Betalingsmetode** ikke indlæst, og følgende fejlmeddelelse vises: "Noget gik galt.</span><span class="sxs-lookup"><span data-stu-id="fa4b8-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="fa4b8-107">Prøv igen senere."</span><span class="sxs-lookup"><span data-stu-id="fa4b8-107">Please try again later."</span></span>

![Betalingsmodulfejl](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="fa4b8-109">Løsning</span><span class="sxs-lookup"><span data-stu-id="fa4b8-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="fa4b8-110">Vent, indtil commerce Scale Unit-cachen udløber</span><span class="sxs-lookup"><span data-stu-id="fa4b8-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="fa4b8-111">Betalingstjenestens indstillinger på betalingstjenestesiden ved kassen i onlinebutikken cachelagres på Commerce Scale Unit og kan tage op til 15 minutter, før de vises på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="fa4b8-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="fa4b8-112">Disse indstillinger for betalingstjeneste omfatter ændringer af forhandlerkonto-id, API-nøgle i skyen og forskellige konfigurationsindstillinger, der er relateret til betalingsmåden.</span><span class="sxs-lookup"><span data-stu-id="fa4b8-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fa4b8-113">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="fa4b8-113">Additional resources</span></span>

[<span data-ttu-id="fa4b8-114">Konfigurere en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="fa4b8-114">Set up an online channel</span></span>](../channel-setup-online.md)
