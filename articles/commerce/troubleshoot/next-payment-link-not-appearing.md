---
title: Gem til min næste betalingsindstilling vises ikke
description: Dette emne indeholder vejledning i fejlfinding, der kan hjælpe, når afkrydsningsfeltet Gem til min næste betaling ikke vises under Betalingsmetode på e-handelswebstedet ved kassen.
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
ms.openlocfilehash: af19a3abd78d543d82f7a8d017e2dc413115a6d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018428"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a><span data-ttu-id="8f3aa-103">Indstillingen "Gem til min næste betaling" vises ikke</span><span class="sxs-lookup"><span data-stu-id="8f3aa-103">"Save for my next payment" option doesn't appear</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8f3aa-104">Dette emne indeholder vejledning i fejlfinding, der kan hjælpe, når afkrydsningsfeltet **Gem til min næste betaling** ikke vises under **Betalingsmetode** på e-handelswebstedet ved kassen.</span><span class="sxs-lookup"><span data-stu-id="8f3aa-104">This topic provides troubleshooting guidance that can help when the **Save for my next payment** check box doesn't appear under **Payment method** on an e-commerce site's checkout page.</span></span>

## <a name="description"></a><span data-ttu-id="8f3aa-105">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="8f3aa-105">Description</span></span>

<span data-ttu-id="8f3aa-106">Afkrydsningsfeltet **Gem til min næste betaling** vises ikke i afsnittet **Betalingsmåde** på e-handelswebstedet ved kassen.</span><span class="sxs-lookup"><span data-stu-id="8f3aa-106">The **Save for my next payment** check box doesn't appear in the **Payment method** section on an e-commerce site's checkout page.</span></span>

<span data-ttu-id="8f3aa-107">I følgende illustration vises et eksempel på en side til betaling ved kassen, hvor afkrydsningsfeltet **Gem til min næste betaling** vises.</span><span class="sxs-lookup"><span data-stu-id="8f3aa-107">The following illustration shows an example of a checkout page that includes the **Save for my next payment** check box.</span></span>

![Gem til min næste betalingsafkrydsningsfelt i betalingsmodulet](media/payment-module-save-payment.jpg)

## <a name="resolution"></a><span data-ttu-id="8f3aa-109">Løsning</span><span class="sxs-lookup"><span data-stu-id="8f3aa-109">Resolution</span></span>

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a><span data-ttu-id="8f3aa-110">Kontroller, at Dynamics 365 Payment Connector til Adyen er konfigureret korrekt i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="8f3aa-110">Verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters</span></span>

<span data-ttu-id="8f3aa-111">Følg disse trin for at kontrollere, at Dynamics 365 Payment Connector til Anøgle er konfigureret korrekt i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="8f3aa-111">To verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="8f3aa-112">Gå til **Retail og Commerce \> Kanaler \> Onlinebutikker**.</span><span class="sxs-lookup"><span data-stu-id="8f3aa-112">Go to **Retail and Commerce \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="8f3aa-113">Vælg onlinebutikken.</span><span class="sxs-lookup"><span data-stu-id="8f3aa-113">Select the online store.</span></span>
1. <span data-ttu-id="8f3aa-114">I oversigtspanelet **Betalingskonti** skal du sørge for, at betalingsoplysningerne i feltet **Tillad lagring af betalingsoplysninger under e-handel** er angivet til **Sand**.</span><span class="sxs-lookup"><span data-stu-id="8f3aa-114">On the **Payment accounts** FastTab, make sure that the **Allow saving payment information in e-commerce** field is set to **True**.</span></span>

![Tillad lagring af betalingsoplysninger i feltet e-handel i Commerce Headquarters](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a><span data-ttu-id="8f3aa-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="8f3aa-116">Additional resources</span></span>

[<span data-ttu-id="8f3aa-117">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="8f3aa-117">Payment module</span></span>](../payment-module.md)

[<span data-ttu-id="8f3aa-118">Gemme onlinebetalingsmidler med Adyen-connector</span><span class="sxs-lookup"><span data-stu-id="8f3aa-118">Saving online payment instruments with the Adyen connector</span></span>](../dev-itpro/adyen-connector-listPI.md)
