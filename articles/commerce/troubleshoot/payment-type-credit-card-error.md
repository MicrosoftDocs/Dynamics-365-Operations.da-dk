---
title: Betalingstypen skal være kreditkortfejl på salgsordresiden
description: Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når der vises en fejlmeddelelse på salgsordresiden, efter at en ordre er synkroniseret.
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
ms.openlocfilehash: 20f18507dee330fd1affedeee092b3dfa7cc10bc
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585250"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a><span data-ttu-id="df3d3-103">"Betalingstypen skal være kreditkortfejl" på salgsordresiden</span><span class="sxs-lookup"><span data-stu-id="df3d3-103">"Payment type must be credit card" error on the sales order page</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="df3d3-104">Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når der vises en fejlmeddelelse på salgsordresiden, efter at en ordre er synkroniseret.</span><span class="sxs-lookup"><span data-stu-id="df3d3-104">This topic provides troubleshooting guidance that can help when an error message is shown on the sales order page after an order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="df3d3-105">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="df3d3-105">Description</span></span>

<span data-ttu-id="df3d3-106">Når du åbner salgsordresiden, efter at du har synkroniseret en ordre, får du følgende fejlmeddelelse: "Betalingstypen skal være kreditkort, da kreditkortnummeret er angivet".</span><span class="sxs-lookup"><span data-stu-id="df3d3-106">When you open the sales order page after you sync an order, you receive the following error message: "The payment type must be credit card, since the credit card number has been specified."</span></span>

![Betalingstypen skal være kreditkortfejl](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a><span data-ttu-id="df3d3-108">Løsning</span><span class="sxs-lookup"><span data-stu-id="df3d3-108">Resolution</span></span>

### <a name="set-the-payment-type-in-commerce-headquarters"></a><span data-ttu-id="df3d3-109">Angive betalingstypen i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="df3d3-109">Set the payment type in Commerce headquarters</span></span>

1. <span data-ttu-id="df3d3-110">Gå til **Debitor \> Betalingsopsætning \> Betalingsbetingelser**.</span><span class="sxs-lookup"><span data-stu-id="df3d3-110">Go to **Accounts receivable \> Payment setup \> Terms of payment**.</span></span>
1. <span data-ttu-id="df3d3-111">Vælg betalingsbetingelserne i den venstre navigationsrude.</span><span class="sxs-lookup"><span data-stu-id="df3d3-111">In the left navigation, select your terms of payment.</span></span>
1. <span data-ttu-id="df3d3-112">Kontroller, at **Kreditkort** er valgt i feltet **Betalingstype**.</span><span class="sxs-lookup"><span data-stu-id="df3d3-112">In the **Payment type** field, make sure that **Credit card** is selected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df3d3-113">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="df3d3-113">Additional resources</span></span>

[<span data-ttu-id="df3d3-114">Bogføre onlinesalg og -betalinger</span><span class="sxs-lookup"><span data-stu-id="df3d3-114">Posting of online sales and payments</span></span>](../tasks/posting-online-sales-payments.md)
