---
title: Betalinger udlignes automatisk, før ordrer faktureres eller afsendes
description: Dette emne indeholder en vejledning til fejlfinding, der kan hjælpe, når en betaling udlignes i portalen Adyen umiddelbart efter, at en ordre er afgivet, selvom salgsordren ikke er blevet faktureret eller afsendt.
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
ms.openlocfilehash: 788854a3119eb9ffaf839beb93a5bc15cdcd6387
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585249"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="ac045-103">Betalinger udlignes automatisk, før ordrer faktureres eller afsendes</span><span class="sxs-lookup"><span data-stu-id="ac045-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ac045-104">Dette emne indeholder en vejledning til fejlfinding, der kan hjælpe, når en betaling udlignes i portalen Adyen umiddelbart efter, at en ordre er afgivet, selvom salgsordren ikke er blevet faktureret eller afsendt.</span><span class="sxs-lookup"><span data-stu-id="ac045-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="ac045-105">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="ac045-105">Description</span></span>

<span data-ttu-id="ac045-106">Når en ordre er afgivet, håndteres betalingen med det samme i portalen Adyen, selvom salgsordren ikke er blevet faktureret eller afsendt.</span><span class="sxs-lookup"><span data-stu-id="ac045-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="ac045-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="ac045-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="ac045-108">Konfigurere manuel hentning af e-handelsbetalinger på Adyen-portalen</span><span class="sxs-lookup"><span data-stu-id="ac045-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="ac045-109">Følg disse trin for af konfigurere manuel hentning af e-handelsbetalinger på Adyen-portalen.</span><span class="sxs-lookup"><span data-stu-id="ac045-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="ac045-110">Log på Adyen-portalen.</span><span class="sxs-lookup"><span data-stu-id="ac045-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="ac045-111">Øverst til højre kan du vælge den handlendes konto for e-handelskanalen.</span><span class="sxs-lookup"><span data-stu-id="ac045-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="ac045-112">På den øverste navigationslinje skal du vælge **Konto** og derefter **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="ac045-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="ac045-113">Vælg **manuel** i feltet **Hent forsinkelse**.</span><span class="sxs-lookup"><span data-stu-id="ac045-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![Indstillingen Hent forsinkelse i Adyen-portalen](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="ac045-115">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ac045-115">Additional resources</span></span>

[<span data-ttu-id="ac045-116">Adyen-betalingsregistrering</span><span class="sxs-lookup"><span data-stu-id="ac045-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="ac045-117">Dynamics 365-betalingsconnector til Adyen</span><span class="sxs-lookup"><span data-stu-id="ac045-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="ac045-118">Konfigurer Adyen-betalingsconnector til Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ac045-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
