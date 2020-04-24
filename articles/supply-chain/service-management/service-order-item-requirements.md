---
title: Varebehov på serviceordre
description: Hvis du vil reservere bestemte varer til en serviceordre, kan du oprette lager lagervarebehov for den.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e31f58cf8782c715b97bdae0e89f684b15a76d2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215073"
---
# <a name="service-order-item-requirements"></a><span data-ttu-id="a8208-103">Varebehov på serviceordre</span><span class="sxs-lookup"><span data-stu-id="a8208-103">Service order item requirements</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a8208-104">Du kan oprette en serviceordre for at spore og administrere ydelser, du leverer til dine debitorer.</span><span class="sxs-lookup"><span data-stu-id="a8208-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="a8208-105">Hvis du vil reservere bestemte varer til en serviceordre, kan du oprette lager lagervarebehov for den.</span><span class="sxs-lookup"><span data-stu-id="a8208-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="a8208-106">Et varebehov kan forbruges straks fra lageret, eller det kan starte en produktionsordre for varen.</span><span class="sxs-lookup"><span data-stu-id="a8208-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="a8208-107">Når du bruger et varebehov i stedet for en varepostering, kan du planlægge leveringen, så den finder sted, umiddelbart før varen faktisk skal bruges. Du kan oprette en indkøbsordre, lade varen indgå i samhandelsaftaler og lade varebehovet indgå i produktionsplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="a8208-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="a8208-108">Varebehov til serviceordrer behandles løbende igennem et projekt.</span><span class="sxs-lookup"><span data-stu-id="a8208-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="a8208-109">Hvis du vil oprette et varebehov på en serviceordre, skal serviceordren knyttes til et projekt.</span><span class="sxs-lookup"><span data-stu-id="a8208-109">To create an item requirement on a service order, the service order must be attached to a project.</span></span>

<span data-ttu-id="a8208-110">I samme øjeblik et varebehov oprettes til en serviceordre, kan du få det vist fra **Projekt** i de enkelte serviceordrer eller via formularen **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="a8208-110">As soon as an item requirement is created for a service order, it can be viewed from **Project** in the individual service order or through the **Sales order** form.</span></span>

## <a name="view-an-item-requirement-from-a-service-order"></a><span data-ttu-id="a8208-111">Få vist et varebehov fra en serviceordre</span><span class="sxs-lookup"><span data-stu-id="a8208-111">View an item requirement from a service order</span></span>

1.  <span data-ttu-id="a8208-112">Klik på **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="a8208-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="a8208-113">Klik på **Ekspedition**, og klik derefter på **Varebehov** for at åbne formularen **Varebehov**.</span><span class="sxs-lookup"><span data-stu-id="a8208-113">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span>

3.  <span data-ttu-id="a8208-114">Klik på fanen **Projekt**, og marker feltet **Serviceordre** for at se serviceordrerne for varebehovet.</span><span class="sxs-lookup"><span data-stu-id="a8208-114">Click the **Project** tab, and check the **Service order** field to see the service orders of the item requirement.</span></span>

## <a name="delete-service-orders-with-item-requirements"></a><span data-ttu-id="a8208-115">Slette serviceordrer med varebehov</span><span class="sxs-lookup"><span data-stu-id="a8208-115">Delete service orders with item requirements</span></span>

<span data-ttu-id="a8208-116">Hvis der oprettes et varebehov på en serviceordre, kan du ikke slette serviceordren.</span><span class="sxs-lookup"><span data-stu-id="a8208-116">If an item requirement is created on a service order, you cannot delete the service order.</span></span> <span data-ttu-id="a8208-117">Du skal slette varebehovet, før du kan slette serviceordren.</span><span class="sxs-lookup"><span data-stu-id="a8208-117">You must delete the item requirement before you can delete the service order.</span></span>

1.  <span data-ttu-id="a8208-118">Klik på **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="a8208-118">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="a8208-119">Klik på **Ekspedition**, og klik derefter på **Varebehov** for at åbne formularen **Varebehov**.</span><span class="sxs-lookup"><span data-stu-id="a8208-119">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span> <span data-ttu-id="a8208-120">I denne form vises de varebehov, der er oprettet på serviceordren.</span><span class="sxs-lookup"><span data-stu-id="a8208-120">This form lists the item requirements that are created on the service order.</span></span>

3.  <span data-ttu-id="a8208-121">Vælg det varebehov, der skal slettes, og klik derefter på **Slet**.</span><span class="sxs-lookup"><span data-stu-id="a8208-121">Select the item requirement to delete, and then click **Delete**.</span></span>

<span data-ttu-id="a8208-122">–eller–</span><span class="sxs-lookup"><span data-stu-id="a8208-122">–or–</span></span>

1.  <span data-ttu-id="a8208-123">Klik på **Projektstyring og regnskab** \> **Generelt** \> **Projekter** \> **Alle projekter**.</span><span class="sxs-lookup"><span data-stu-id="a8208-123">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="a8208-124">Åbn det projekt, der har den serviceordre, hvor der er oprettet et varebehov.</span><span class="sxs-lookup"><span data-stu-id="a8208-124">Open the project that has the service order in which an item requirement is created.</span></span>

3.  <span data-ttu-id="a8208-125">Klik på **Varebehov** i højre rude i formularen **Projekter**.</span><span class="sxs-lookup"><span data-stu-id="a8208-125">In the **Projects** form, in the right pane, click **Item requirements**.</span></span> <span data-ttu-id="a8208-126">Formularen **Varebehov** viser en oversigt over de varebehov, der er knyttet til det valgte projekt.</span><span class="sxs-lookup"><span data-stu-id="a8208-126">The **Item requirements** form lists the item requirements that are associated with the selected project.</span></span>

4.  <span data-ttu-id="a8208-127">Vælg det varebehov, der skal slettes, og klik derefter på **Slet**.</span><span class="sxs-lookup"><span data-stu-id="a8208-127">Select the item requirement to delete, and then click **Delete**.</span></span>

## <a name="see-also"></a><span data-ttu-id="a8208-128">Se også</span><span class="sxs-lookup"><span data-stu-id="a8208-128">See also</span></span>

<span data-ttu-id="a8208-129">[Varebehov (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="a8208-129">[Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span></span>

