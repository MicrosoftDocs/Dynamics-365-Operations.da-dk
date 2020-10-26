---
title: Oprette varebehov til serviceordrer
description: Hvis du vil reservere bestemte varer til en serviceordre, kan du oprette lager lagervarebehov for den.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 18484b637723cef43cad288c08ddfe53cddf9e03
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978477"
---
# <a name="create-item-requirements-for-service-orders"></a><span data-ttu-id="3df1f-103">Oprette varebehov til serviceordrer</span><span class="sxs-lookup"><span data-stu-id="3df1f-103">Create item requirements for service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3df1f-104">Du kan oprette en serviceordre for at spore og administrere ydelser, du leverer til dine debitorer.</span><span class="sxs-lookup"><span data-stu-id="3df1f-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="3df1f-105">Hvis du vil reservere bestemte varer til en serviceordre, kan du oprette lager lagervarebehov for den.</span><span class="sxs-lookup"><span data-stu-id="3df1f-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="3df1f-106">Et varebehov kan forbruges straks fra lageret, eller det kan starte en produktionsordre for varen.</span><span class="sxs-lookup"><span data-stu-id="3df1f-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="3df1f-107">Når du bruger et varebehov i stedet for en varepostering, kan du planlægge leveringen, så den finder sted, umiddelbart før varen faktisk skal bruges. Du kan oprette en indkøbsordre, lade varen indgå i samhandelsaftaler og lade varebehovet indgå i produktionsplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="3df1f-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="3df1f-108">Varebehov til serviceordrer behandles løbende igennem et projekt.</span><span class="sxs-lookup"><span data-stu-id="3df1f-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="3df1f-109">Hvis du vil oprette et varebehov på en serviceordre, skal serviceordren knyttes til et projekt.</span><span class="sxs-lookup"><span data-stu-id="3df1f-109">To create an item requirement on a service order, the service order must be assigned to a project.</span></span> <span data-ttu-id="3df1f-110">Når du opretter et varebehov for en serviceordre, kan du få vist varebehovet i formularen **Projekter** for det valgte projekt.</span><span class="sxs-lookup"><span data-stu-id="3df1f-110">After you create an item requirement for a service order, you can view the item requirement in the **Projects** form for the selected project.</span></span>

## <a name="create-an-item-requirement-for-a-service-order"></a><span data-ttu-id="3df1f-111">Opret et varebehov for en serviceordre</span><span class="sxs-lookup"><span data-stu-id="3df1f-111">Create an item requirement for a service order</span></span>

1.  <span data-ttu-id="3df1f-112">Klik på **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="3df1f-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="3df1f-113">Vælg den serviceordre, som du vil oprette et varebehov til.</span><span class="sxs-lookup"><span data-stu-id="3df1f-113">Select the service order that you want to create an item requirement for.</span></span>

3.  <span data-ttu-id="3df1f-114">Klik på **Varebehov** under fanen **Ekspedition** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="3df1f-114">On the **Action Pane**, on the **Dispatch** tab, click **Item requirement**.</span></span>

4.  <span data-ttu-id="3df1f-115">Angiv oplysningerne til den påkrævede vare i formularen **Varebehov**.</span><span class="sxs-lookup"><span data-stu-id="3df1f-115">In the **Item requirements** form, enter information for the required item.</span></span> <span data-ttu-id="3df1f-116">Du kan finde flere oplysninger om de forskellige felter i formularen under [Varebehov (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="3df1f-116">For more information about the specific fields, see [Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).</span></span>

## <a name="create-an-item-requirement-for-a-service-agreement"></a><span data-ttu-id="3df1f-117">Opret et varebehov til en serviceaftale</span><span class="sxs-lookup"><span data-stu-id="3df1f-117">Create an item requirement for a service agreement</span></span>

1.  <span data-ttu-id="3df1f-118">Klik på **Servicestyring** \> **Almindelige** \> **Serviceaftaler** \> **Serviceaftaler**.</span><span class="sxs-lookup"><span data-stu-id="3df1f-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="3df1f-119">Åbn den serviceaftale, hvortil du vil oprette et varebehov.</span><span class="sxs-lookup"><span data-stu-id="3df1f-119">Open the service agreement for which you want to create an item requirement.</span></span>

3.  <span data-ttu-id="3df1f-120">I oversigtspanelet **Linjer** skal du klikke på **Tilføj** for at oprette en ny linje.</span><span class="sxs-lookup"><span data-stu-id="3df1f-120">On the **Lines** FastTab, click **Add** to create a new line.</span></span>

4.  <span data-ttu-id="3df1f-121">Vælg **Care** i feltet **Transaktionstype**.</span><span class="sxs-lookup"><span data-stu-id="3df1f-121">In the **Transaction type** field, select **Item**.</span></span>

5.  <span data-ttu-id="3df1f-122">I feltet **Vareopsætning** skal du vælge **Varebehov**.</span><span class="sxs-lookup"><span data-stu-id="3df1f-122">In the **Item setup** field, select **Item requirement**.</span></span>

6.  <span data-ttu-id="3df1f-123">I feltet **Varenummer** skal du markere den vare, der kræves til serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="3df1f-123">In the **Item number** field, select the item that is required for the service agreement.</span></span>

7.  <span data-ttu-id="3df1f-124">I oversigtspanelet **Linjedetaljer** under fanen **Produktdimensioner** skal du i feltet **Sted** vælge lagerstedet for varen.</span><span class="sxs-lookup"><span data-stu-id="3df1f-124">On the **Line details** FastTab, on the **Product dimensions** tab, in the **Site** field, select the inventory site for the item.</span></span>

8.  <span data-ttu-id="3df1f-125">Hvis du vil oprette en serviceordre i aftalelinjen, skal du i oversigtspanelet **Linjer** klikke på **Opret serviceordrer** og derefter angive de relevante oplysninger i formularen **Opret serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="3df1f-125">To create a service order from the agreement line, on the **Lines** FastTab, click **Create service orders**, and then enter the relevant information in the **Create service orders** form.</span></span> 


## <a name="see-also"></a><span data-ttu-id="3df1f-126">Se også</span><span class="sxs-lookup"><span data-stu-id="3df1f-126">See also</span></span>

<span data-ttu-id="3df1f-127">[Oprette serviceordrer automatisk](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="3df1f-127">[Create service orders automatically](create-service-orders-automatically.md).</span></span>

  


