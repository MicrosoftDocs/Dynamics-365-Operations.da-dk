---
title: "Ordrer på hold"
description: "Dette emne beskriver tilbageholdte ordrer ved hjælp af Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8b4c8ecbef1dc667d3b60411a53f0c63686529c2
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="order-holds"></a><span data-ttu-id="78ff4-103">Ordrer på hold</span><span class="sxs-lookup"><span data-stu-id="78ff4-103">Order holds</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="78ff4-104">Dette emne beskriver tilbageholdte ordrer ved hjælp af Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="78ff4-104">This topic describes holds on orders using Dynamics 365 for Retail.</span></span>

<span data-ttu-id="78ff4-105">En ordre kan holdes tilbage af forskellige årsager.</span><span class="sxs-lookup"><span data-stu-id="78ff4-105">An order can be put on hold for various reasons.</span></span> <span data-ttu-id="78ff4-106">Du kan for eksempel holde en ordre tilbage, indtil debitoradressen eller betalingsmetoden er kontrolleret, eller indtil en chef leder kan gennemse debitorens kreditmaksimum.</span><span class="sxs-lookup"><span data-stu-id="78ff4-106">For example, you might put an order on hold until the customer address or payment method can be verified, or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="78ff4-107">I løbet af salgsprocessen er der tidspunkter, hvor salgsordrer skal holdes tilbage.</span><span class="sxs-lookup"><span data-stu-id="78ff4-107">During the sales process, there are times when sales orders must be put on hold.</span></span> <span data-ttu-id="78ff4-108">En salgsordre kan for eksempel holdes tilbage på grund af problemer med en debitorbetaling, der skyldes mistanke om svig, eller fordi en chef skal gennemgå ordren.</span><span class="sxs-lookup"><span data-stu-id="78ff4-108">For example, a sales order might be put on hold because of issues with a customer payment, because of suspected fraud, or because a manager must review the order.</span></span> <span data-ttu-id="78ff4-109">Når en salgsordre holdes tilbage, tildeles en ordretilbageholdelseskode til salgsordren for at angive årsagen til tilbageholdelsen.</span><span class="sxs-lookup"><span data-stu-id="78ff4-109">When a sales order is put on hold, an order hold code is assigned to the sales order to indicate the reason for the hold.</span></span> <span data-ttu-id="78ff4-110">Koder for tilbageholdelse af salgsordrer er konfigureret under **Salg og marketing** &gt; **Konfiguration** &gt; **Salgsordrer** &gt; **Koder for ordrer på hold**.</span><span class="sxs-lookup"><span data-stu-id="78ff4-110">Sales order hold codes are configured at **Sales and marketing** &gt; **Setup** &gt; **Sales orders** &gt; **Order holds codes**.</span></span> <span data-ttu-id="78ff4-111">En salgsordre kan tilbageholdes manuelt på tidspunktet for oprettelse af ordren eller senere.</span><span class="sxs-lookup"><span data-stu-id="78ff4-111">A sales order can be put on hold manually at the time of order creation or later.</span></span> <span data-ttu-id="78ff4-112">Desuden kan en ordre automatisk tilbageholdes baseret på reglerne for svig.</span><span class="sxs-lookup"><span data-stu-id="78ff4-112">Additionally, an order can be put on hold automatically, based on fraud rules.</span></span> <span data-ttu-id="78ff4-113">Når en salgsordre tilbageholdes, kan det være nødvendigt at opdatere den med yderligere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="78ff4-113">While a sales order is on hold, you might have to update it with more information.</span></span> <span data-ttu-id="78ff4-114">Alternativt kan det være en god ide at tjekke salgsordren, når du fortsætter med at arbejde på den.</span><span class="sxs-lookup"><span data-stu-id="78ff4-114">Alternatively, you might want to check out the sales order as you continue to work on it.</span></span> <span data-ttu-id="78ff4-115">Du kan tjekke en salgsordre ud, tjekke den tilbage igen og endda tilsidesætte en anden brugers udtjekning ved hjælp af panelet for tilbageholdte ordrer (**Detail** &gt; **Kunder** &gt; **Ordrer på hold**).</span><span class="sxs-lookup"><span data-stu-id="78ff4-115">You can check out a sales order, check it back in, and even override the checkout of another user by using the order hold workbench (**Retail** &gt; **Customers** &gt; **Order holds**).</span></span> <span data-ttu-id="78ff4-116">Når en ordre er klar til at blive fuldført, skal du fjerne hold, før du kan fuldføre bestillingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="78ff4-116">When an order is ready to be completed, you must remove the hold before you can complete the order process.</span></span>




