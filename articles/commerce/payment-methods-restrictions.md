---
title: Begrænse betalingsmetoder for returneringer uden kvittering
description: I dette emne beskrives, hvordan der kan være begrænsede refusionsmuligheder for bestemte betalingstyper, hvis varerne returneres uden kvittering.
author: rapraj
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: dfc49e3c3132fe2687ea71e5da75fe31753d57f9
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022058"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="848d4-103">Begrænse betalingsmetoder for returneringer uden kvittering</span><span class="sxs-lookup"><span data-stu-id="848d4-103">Restrict payment methods for returns without a receipt</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="848d4-104">De enkelte betalingstyper, som en detailhandlende accepterer, skal konfigureres, når systemet konfigureres.</span><span class="sxs-lookup"><span data-stu-id="848d4-104">Each payment type that a retailer accepts must be configured when the system is set up.</span></span> <span data-ttu-id="848d4-105">I dette emne beskrives, hvordan der kan være begrænsede refusionsmuligheder for bestemte betalingstyper, hvis varerne returneres uden kvittering.</span><span class="sxs-lookup"><span data-stu-id="848d4-105">This topic describes how certain payment types can be restricted for refund if the returns are made without a receipt.</span></span>

## <a name="set-up-payment-methods"></a><span data-ttu-id="848d4-106">Oprette betalingsmåder</span><span class="sxs-lookup"><span data-stu-id="848d4-106">Set up payment methods</span></span>

<span data-ttu-id="848d4-107">Når du vil konfigurere betalingsmetoder, skal følgende opgaver være fuldført.</span><span class="sxs-lookup"><span data-stu-id="848d4-107">To set up payment methods, the following tasks must be completed.</span></span>
1. <span data-ttu-id="848d4-108">Opret de betalingsmetoder, der accepteres af hele organisationen.</span><span class="sxs-lookup"><span data-stu-id="848d4-108">Create the payment methods that are accepted by the entire organization.</span></span>
2. <span data-ttu-id="848d4-109">Oprettelse af korttyper og kortnumre i hele organisationen.</span><span class="sxs-lookup"><span data-stu-id="848d4-109">Create organization-wide card types and card numbers.</span></span> <span data-ttu-id="848d4-110">Hvis der skal accepteres kredit- eller debetkort, skal du oprette én betalingsmetode for kort og derefter oprette korttyper og kortnumre, der gælder for hele organisationen.</span><span class="sxs-lookup"><span data-stu-id="848d4-110">If credit cards or debit cards are accepted, you must create one payment method for cards, and then create the organization-wide card types and card numbers.</span></span>
3. <span data-ttu-id="848d4-111">Konfigurer betalingsmetoder for butikken.</span><span class="sxs-lookup"><span data-stu-id="848d4-111">Set up store payment methods.</span></span> <span data-ttu-id="848d4-112">Tilknyt betalingsmetoder til de enkelte butikker, og angiv derefter butiksspecifikke indstillinger for de enkelte betalingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="848d4-112">Associate payment methods with each store, and then enter the store-specific settings for each payment method.</span></span>
4. <span data-ttu-id="848d4-113">Konfigurer betalingsmetoder for butikker.</span><span class="sxs-lookup"><span data-stu-id="848d4-113">Set up card payment methods for stores.</span></span> <span data-ttu-id="848d4-114">For alle kortbetalingsmetoder, som butikken accepterer, skal du udføre kortopsætningen.</span><span class="sxs-lookup"><span data-stu-id="848d4-114">For any card payment methods that the store accepts, complete the card setup.</span></span>

<span data-ttu-id="848d4-115">![Butiksopsætning](media/NoReceiptReturns1.png "Konfiguration af Retail Store")</span><span class="sxs-lookup"><span data-stu-id="848d4-115">![Store Setup](media/NoReceiptReturns1.png "Retail Store Setup")</span></span> 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="848d4-116">Begrænse betalingsmetoder for returneringer uden kvittering</span><span class="sxs-lookup"><span data-stu-id="848d4-116">Restrict payment methods for returns without a receipt</span></span>

<span data-ttu-id="848d4-117">For hver betalingsmetode i en butik skal du på siden **Butiksstyring** under **Returneringer uden kvittering** indstille **Begræns for returneringer uden kvittering** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="848d4-117">For each store payment method, on the **Store management** page, under **Non receipt returns**, set **Restrict for refunds without receipt** to **Yes**.</span></span> 

<span data-ttu-id="848d4-118">Standardværdien for ja/nej-knappen er **Nej**, hvilket sikrer, at betalingsmetoden er tilladt for refusioner.</span><span class="sxs-lookup"><span data-stu-id="848d4-118">The default value of the toggle is **No**, which ensures that the payment method is allowed for refunds.</span></span> 

<span data-ttu-id="848d4-119">Når **Begræns for returneringer uden kvittering** er indstillet til **Ja**, er den valgte betalingsmetode ikke tilladt for refusioner.</span><span class="sxs-lookup"><span data-stu-id="848d4-119">When **Restrict for refunds without receipt** is set to **Yes**, the selected payment method will not be allowed for refunds.</span></span> 

<span data-ttu-id="848d4-120">![Gemme betalingsmetode](media/NoReceiptReturns3.png "Betalingsmetode for Retail Store")</span><span class="sxs-lookup"><span data-stu-id="848d4-120">![Store payment method](media/NoReceiptReturns3.png "Retail Store Payment Method")</span></span> 

> [!NOTE]
> <span data-ttu-id="848d4-121">Når en kasserer vælger en betalingsmåde, hvor der er begrænsede refusionsmuligheder uden kvittering, vises en meddelelse til kontrol af godkendte betalingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="848d4-121">When a cashier selects a payment method that is restricted for refund without a receipt, a message displays to verify the acceptable payment methods.</span></span>

<span data-ttu-id="848d4-122">![Acceptable betalingsmetoder](media/NoReceiptReturns4.png "Acceptable betalingsmetoder")</span><span class="sxs-lookup"><span data-stu-id="848d4-122">![Acceptable payment methods](media/NoReceiptReturns4.png "Acceptable payment methods")</span></span> 

<span data-ttu-id="848d4-123">Hvis en transaktion har både en returnering med kvittering og en returnering uden kvittering, gennemtvinges begrænsningsbetingelserne ikke, fordi transaktionen bliver en returneringsarbejdsgang med en kvittering.</span><span class="sxs-lookup"><span data-stu-id="848d4-123">If a transaction has both a receipted return and a return without a receipt, the restriction conditions will not be enforced because the transaction will be a return workflow with a receipt.</span></span> 

