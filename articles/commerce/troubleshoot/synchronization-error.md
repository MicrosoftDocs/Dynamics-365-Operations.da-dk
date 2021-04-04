---
title: Fejl ved ordresynkronisering i forbindelse med standardbetalingstjeneste
description: Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe med at rette en fejl, der kan opstå, når en onlineordre synkroniseres.
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
ms.openlocfilehash: dd7c400f26b6fc7fbe1d4fec43a52295eb363333
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585243"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="c0f1f-103">Fejl ved ordresynkronisering i forbindelse med standardbetalingstjeneste</span><span class="sxs-lookup"><span data-stu-id="c0f1f-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c0f1f-104">Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe med at rette en fejl, der kan opstå, når en onlineordre synkroniseres.</span><span class="sxs-lookup"><span data-stu-id="c0f1f-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="c0f1f-105">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="c0f1f-105">Description</span></span>

<span data-ttu-id="c0f1f-106">Når du synkroniserer en onlineordre, modtager du følgende fejlmeddelelse: "Der skal være en standardbetalingstjeneste til behandling af kreditkorttransaktioner".</span><span class="sxs-lookup"><span data-stu-id="c0f1f-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![Manglende fejl i standardbetalingstjenesten](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="c0f1f-108">Løsning</span><span class="sxs-lookup"><span data-stu-id="c0f1f-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="c0f1f-109">Bekræft eller angiv standardbetalingstjenesten i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="c0f1f-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="c0f1f-110">Følg disse trin for at bekræfte eller angive standardbetalingstjenesten i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="c0f1f-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="c0f1f-111">Gå til **Debitor \> Betalingsopsætning \> Betalingstjenester**.</span><span class="sxs-lookup"><span data-stu-id="c0f1f-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="c0f1f-112">Sørg for, at indstillingen **Standardprocessoren for den nye kreditkort** er angivet til **Ja** for én betalingstjeneste.</span><span class="sxs-lookup"><span data-stu-id="c0f1f-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c0f1f-113">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c0f1f-113">Additional resources</span></span>

[<span data-ttu-id="c0f1f-114">Opsætning, godkendelse og verifikation af kreditkort</span><span class="sxs-lookup"><span data-stu-id="c0f1f-114">Credit card setup, authorization, and capture</span></span>](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)
