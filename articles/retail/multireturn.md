---
title: Returnere varer på tværs af flere kundeordrer og fakturaer
description: Dette emne beskriver den funktionalitet, der muliggør returneringer på tværs af flere kundeordrer og fakturaer i Microsoft Dynamics 365 for Retail.
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
ms.openlocfilehash: d410fde2cd127f8d644e6a385937b6bc98d74576
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517028"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="2d694-103">Returnere varer på tværs af flere kundeordrer og fakturaer</span><span class="sxs-lookup"><span data-stu-id="2d694-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="2d694-104">I Dynamics 365 for Finance and Operations version 10.0 kan returneringer foretages på tværs af flere ordrer og fakturaer, men i versioner før 10.0 kan returneringer kun behandles for en enkelt faktura ad gangen.</span><span class="sxs-lookup"><span data-stu-id="2d694-104">In Dynamics 365 for Finance and Operations version 10.0, returns can be made across multiple orders and invoices, whereas in releases prior to 10.0, returns could only be processed by a single invoice at a time.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="2d694-105">Konfigurere Retail til at understøtte returneringer på tværs af flere kundeordre og fakturaer</span><span class="sxs-lookup"><span data-stu-id="2d694-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="2d694-106">Gå til **Detailparametre \> Kundeordrer**.</span><span class="sxs-lookup"><span data-stu-id="2d694-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="2d694-107">Aktivér parameteren **Aktivér returneringer af flere ordrer**.</span><span class="sxs-lookup"><span data-stu-id="2d694-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="2d694-108">Behandl returneringerne</span><span class="sxs-lookup"><span data-stu-id="2d694-108">Process returns</span></span>

<span data-ttu-id="2d694-109">Når parameteren er aktiveret, og ændringerne synkroniseres til butikkerne, kan kassereren i butikken kan vælge flere salgsordrer til en kunde til deres returnering.</span><span class="sxs-lookup"><span data-stu-id="2d694-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="2d694-110">Når ordrerne markeres, vises en liste over alle produkter, der kan returneres, på tværs af alle fakturaer for ordrerne.</span><span class="sxs-lookup"><span data-stu-id="2d694-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="2d694-111">Kassereren kan derefter vælge de produkter, der skal returneres.</span><span class="sxs-lookup"><span data-stu-id="2d694-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="2d694-112">Der oprettes en enkelt returordre for alle de valgte produkter.</span><span class="sxs-lookup"><span data-stu-id="2d694-112">A single return order will be created for all the selected products.</span></span>
