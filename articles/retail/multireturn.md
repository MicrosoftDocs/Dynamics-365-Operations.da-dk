---
title: Returnere varer på tværs af flere kundeordrer og fakturaer
description: Dette emne beskriver den funktionalitet, der muliggør returneringer på tværs af flere kundeordrer og fakturaer i Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 25a1081e5f903076e23089c41dda7437f8a70124
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017983"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="f502e-103">Returnere varer på tværs af flere kundeordrer og fakturaer</span><span class="sxs-lookup"><span data-stu-id="f502e-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="f502e-104">Returneringer kan foretages på tværs af flere kundeordrer og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="f502e-104">Returns can be made across multiple orders and invoices.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="f502e-105">Konfigurere Retail til at understøtte returneringer på tværs af flere kundeordre og fakturaer</span><span class="sxs-lookup"><span data-stu-id="f502e-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="f502e-106">Gå til **Detailparametre \> Kundeordrer**.</span><span class="sxs-lookup"><span data-stu-id="f502e-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="f502e-107">Aktivér parameteren **Aktivér returneringer af flere ordrer**.</span><span class="sxs-lookup"><span data-stu-id="f502e-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="f502e-108">Behandl returneringerne</span><span class="sxs-lookup"><span data-stu-id="f502e-108">Process returns</span></span>

<span data-ttu-id="f502e-109">Når parameteren er aktiveret, og ændringerne synkroniseres til butikkerne, kan kassereren i butikken kan vælge flere salgsordrer til en kunde til deres returnering.</span><span class="sxs-lookup"><span data-stu-id="f502e-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="f502e-110">Når ordrerne markeres, vises en liste over alle produkter, der kan returneres, på tværs af alle fakturaer for ordrerne.</span><span class="sxs-lookup"><span data-stu-id="f502e-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="f502e-111">Kassereren kan derefter vælge de produkter, der skal returneres.</span><span class="sxs-lookup"><span data-stu-id="f502e-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="f502e-112">Der oprettes en enkelt returordre for alle de valgte produkter.</span><span class="sxs-lookup"><span data-stu-id="f502e-112">A single return order will be created for all the selected products.</span></span>
