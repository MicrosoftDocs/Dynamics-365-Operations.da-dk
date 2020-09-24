---
title: Returnere varer på tværs af flere kundeordrer og fakturaer
description: Dette emne beskriver den funktionalitet, der muliggør returneringer på tværs af flere kundeordrer og fakturaer i Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
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
ms.openlocfilehash: e95f06ffaaf2d250b02a8458faa2d9e0b5ef5631
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760244"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="808c0-103">Returnere varer på tværs af flere kundeordrer og fakturaer</span><span class="sxs-lookup"><span data-stu-id="808c0-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="808c0-104">I denne artikel beskrives to funktioner, der optimerer kundeordrereturneringer over flere fakturaer.</span><span class="sxs-lookup"><span data-stu-id="808c0-104">This article describes two features that optimize customer order returns over multiple invoices.</span></span> 

## <a name="enable-refunds-over-multiple-captures"></a><span data-ttu-id="808c0-105">Aktivér refusioner via flere opsamlinger</span><span class="sxs-lookup"><span data-stu-id="808c0-105">Enable refunds over multiple captures</span></span>

<span data-ttu-id="808c0-106">Denne funktion giver mulighed for flere sammenkædede refusioner i forhold til den samme kundeordre.</span><span class="sxs-lookup"><span data-stu-id="808c0-106">This feature enables multiple linked refunds against the same customer order.</span></span> 

1. <span data-ttu-id="808c0-107">Gå til arbejdsområdet **Funktionsstyring**, og søg efter **Aktivér refusioner via flere opsamlinger**.</span><span class="sxs-lookup"><span data-stu-id="808c0-107">Go to the **Feature management** workspace and search for **Enable refunds over multiple captures**.</span></span>
2. <span data-ttu-id="808c0-108">Vælg **Aktivér refusioner via flere opsamlinger**, og klik derefter på **Aktivér**.</span><span class="sxs-lookup"><span data-stu-id="808c0-108">Select **Enable refunds over multiple orders** and then click **Enable**.</span></span> 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a><span data-ttu-id="808c0-109">Aktivér beregning af passende moms for returneringer med delvist antal</span><span class="sxs-lookup"><span data-stu-id="808c0-109">Enable proper tax calculation for returns with partial quantity</span></span>

<span data-ttu-id="808c0-110">Denne funktion sikrer, at momsen i sidste ende er lig med det oprindeligt opkrævede momsbeløb, når en ordre returneres ved hjælp af flere fakturaer.</span><span class="sxs-lookup"><span data-stu-id="808c0-110">This feature ensures that when an order is returned using multiple invoices, the taxes will ultimately be equal to the tax amount originally charged.</span></span> 

1. <span data-ttu-id="808c0-111">Gå til arbejdsområdet **Funktionsstyring**, og søg efter **Aktivér beregning af passende moms for returneringer med delvist antal**.</span><span class="sxs-lookup"><span data-stu-id="808c0-111">Go to the **Feature management** workspace and search for **Enable proper tax calculation for returns with partial quantity**.</span></span>
2. <span data-ttu-id="808c0-112">Vælg **Aktivér beregning af passende moms for returneringer med delvist antal**, og klik derefter på **Aktivér**.</span><span class="sxs-lookup"><span data-stu-id="808c0-112">Select **Enable proper tax calculation for returns with partial quantity** and then click **Enable**.</span></span> 


## <a name="process-returns"></a><span data-ttu-id="808c0-113">Behandl returneringerne</span><span class="sxs-lookup"><span data-stu-id="808c0-113">Process returns</span></span>

<span data-ttu-id="808c0-114">Når disse funktioner er aktiveret, og ændringerne synkroniseres til butikkerne, kan kassereren i butikken kan vælge flere salgsordrer til en kunde til deres returnering.</span><span class="sxs-lookup"><span data-stu-id="808c0-114">After these features are turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="808c0-115">Når ordrerne markeres, vises en liste over alle produkter, der kan returneres, på tværs af alle fakturaer for ordrerne.</span><span class="sxs-lookup"><span data-stu-id="808c0-115">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="808c0-116">Kassereren kan derefter vælge de produkter, der skal returneres.</span><span class="sxs-lookup"><span data-stu-id="808c0-116">The cashier can then select the products to return.</span></span> <span data-ttu-id="808c0-117">Der oprettes en enkelt returordre for alle de valgte produkter.</span><span class="sxs-lookup"><span data-stu-id="808c0-117">A single return order will be created for all the selected products.</span></span>

<span data-ttu-id="808c0-118">Hvis ordren returneres fuldt ud, er det beløb, der returneres til kunden, lig med det momsbeløb, der oprindeligt blev opkrævet.</span><span class="sxs-lookup"><span data-stu-id="808c0-118">If the order is fully returned, the amount of taxes returned to the customer will be equal to the amount of tax originally charged.</span></span>

