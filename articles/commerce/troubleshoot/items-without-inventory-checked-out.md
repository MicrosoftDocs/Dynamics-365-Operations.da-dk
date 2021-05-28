---
title: Varer uden lager kan checkes ud
description: Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når kunder kan føje varer, der ikke er på lager, til deres indkøbsvogn og gå videre til kassen.
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
ms.openlocfilehash: 4fa7769044c45faffd9ff61b3de8e6217a5e0354
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018452"
---
# <a name="items-without-inventory-can-be-checked-out"></a><span data-ttu-id="57121-103">Varer uden lager kan checkes ud</span><span class="sxs-lookup"><span data-stu-id="57121-103">Items without inventory can be checked out</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="57121-104">Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når kunder kan føje varer, der ikke er på lager, til deres indkøbsvogn og gå videre til kassen.</span><span class="sxs-lookup"><span data-stu-id="57121-104">This topic provides troubleshooting guidance that can help when customers can add out-of-stock items to their cart and proceed to checkout.</span></span>

## <a name="description"></a><span data-ttu-id="57121-105">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="57121-105">Description</span></span>

<span data-ttu-id="57121-106">Brugerne kan føje en vare til deres indkøbsvogn, selvom der ikke er nogen lagerbeholdning i butikken, og derefter gå videre til kassen.</span><span class="sxs-lookup"><span data-stu-id="57121-106">Users can add an item to their cart, even though there is no on-hand inventory in the store, and then proceed to the checkout page.</span></span>

## <a name="resolution"></a><span data-ttu-id="57121-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="57121-107">Resolution</span></span>

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a><span data-ttu-id="57121-108">Aktiver egenskaben Vis fejl for lagerfejl i Commerce site builder</span><span class="sxs-lookup"><span data-stu-id="57121-108">Enable the Show Out Of Stock Errors property in Commerce site builder</span></span>

<span data-ttu-id="57121-109">Aktiver egenskaben **Vis fejl for lagerfejl** i Commerce site builder ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="57121-109">To enable the **Show Out Of Stock Errors** property in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="57121-110">Vælg det sted, du arbejder på.</span><span class="sxs-lookup"><span data-stu-id="57121-110">Select the site that you're working on.</span></span>
1. <span data-ttu-id="57121-111">Vælg **Sider** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="57121-111">In the left navigation, select **Pages**.</span></span>
1. <span data-ttu-id="57121-112">Vælg **CartPage** for at åbne den.</span><span class="sxs-lookup"><span data-stu-id="57121-112">Select **CartPage** to open it.</span></span>
1. <span data-ttu-id="57121-113">Marker afkrydsningsfeltet **Indkøbsvogn 1**, vælg **Rediger**, og marker derefter afkrydsningsfeltet **Vis lagerfejl** i egenskabsruden.</span><span class="sxs-lookup"><span data-stu-id="57121-113">Select the **Cart 1** slot, select **Edit**, and then, in the properties pane, select the **Show Out Of Stock Errors** check box.</span></span>
1. <span data-ttu-id="57121-114">Gem og publicer siden.</span><span class="sxs-lookup"><span data-stu-id="57121-114">Save and publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="57121-115">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="57121-115">Additional resources</span></span>

[<span data-ttu-id="57121-116">Anvend lagerindstillinger</span><span class="sxs-lookup"><span data-stu-id="57121-116">Apply inventory settings</span></span>](../inventory-settings.md)

[<span data-ttu-id="57121-117">Beregne lagertilgængelighed for detailkanaler</span><span class="sxs-lookup"><span data-stu-id="57121-117">Calculate inventory availability for retail channels</span></span>](../calculated-inventory-retail-channels.md)

[<span data-ttu-id="57121-118">Konfigurere lagerbuffere og lagerniveauer</span><span class="sxs-lookup"><span data-stu-id="57121-118">Configure inventory buffers and inventory levels</span></span>](../inventory-buffers-levels.md)
