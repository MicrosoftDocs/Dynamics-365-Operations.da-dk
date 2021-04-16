---
title: Oprette serviceordrer automatisk
description: Du kan oprette serviceordrer for én serviceaftale eller flere serviceaftaler.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cc06536827320a35a691330d852ba64532604935
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817599"
---
# <a name="create-service-orders-automatically"></a><span data-ttu-id="d7f33-103">Oprette serviceordrer automatisk</span><span class="sxs-lookup"><span data-stu-id="d7f33-103">Create service orders automatically</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d7f33-104">Du kan oprette serviceordrer for én serviceaftale eller flere serviceaftaler.</span><span class="sxs-lookup"><span data-stu-id="d7f33-104">You can create service orders for one service agreement or for several service agreements.</span></span> <span data-ttu-id="d7f33-105">Når de er oprettet, kan du få vist dine serviceaftaler i formularen **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="d7f33-105">When they are created, you can view your service orders in the **Service orders** form.</span></span>

<span data-ttu-id="d7f33-106">Serviceordrer kan kun oprettes for den gyldighedsperiode, der er defineret i serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="d7f33-106">Service orders are created only for the valid period of the service agreement.</span></span> <span data-ttu-id="d7f33-107">Hvis du definerer et tidsrum i formularen **Opret serviceordrer**, der begynder før startdatoen eller slutter efter slutdatoen for serviceaftalen, oprettes serviceordrerne kun for den del af tidsrummet, der ligger inden for serviceaftalens datoer.</span><span class="sxs-lookup"><span data-stu-id="d7f33-107">If the interval that you specify in the **Create service orders** form is before the starting date or after the ending date of the service agreement, service orders are created only for the part of the interval that is within the service agreement dates.</span></span>

<span data-ttu-id="d7f33-108">Når du opretter serviceordrer manuelt eller automatisk fra serviceaftalelinjen, skal serviceordren ligge inden for det tidsinterval, der er angivet ved start- og slutdatoerne for linjen, medmindre du ikke angiver en slutdato på linjen.</span><span class="sxs-lookup"><span data-stu-id="d7f33-108">When you create service orders manually or automatically from the service agreement line, the service order must be in the time interval that is defined by the starting and ending dates for the line, unless you do not specify an ending date on the line.</span></span>

## <a name="create-service-orders-automatically-for-a-service-agreement"></a><span data-ttu-id="d7f33-109">Oprette serviceordrer for en serviceaftale automatisk</span><span class="sxs-lookup"><span data-stu-id="d7f33-109">Create service orders automatically for a service agreement</span></span>

1.  <span data-ttu-id="d7f33-110">Klik på **Servicestyring** \> **Almindelige** \> **Serviceaftaler** \> **Serviceaftaler**.</span><span class="sxs-lookup"><span data-stu-id="d7f33-110">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="d7f33-111">Vælg en serviceaftale.</span><span class="sxs-lookup"><span data-stu-id="d7f33-111">Select a service agreement.</span></span>

3.  <span data-ttu-id="d7f33-112">Klik på fanen **Levér**, og klik derefter på **Planlagte serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="d7f33-112">Click the **Deliver** tab, and then click **Planned service orders**.</span></span>

4.  <span data-ttu-id="d7f33-113">Angiv datoerne i felterne **Fra dato** og **Til dato** for at definere serviceperioden.</span><span class="sxs-lookup"><span data-stu-id="d7f33-113">Specify dates in the **From date** and **To date** fields to define the service period.</span></span>

5.  <span data-ttu-id="d7f33-114">Markér afkrydsningsfeltet **Vis infolog** for at få vist en liste over de serviceordrer, der er oprettet.</span><span class="sxs-lookup"><span data-stu-id="d7f33-114">Select the **Show Infolog** check box to display a list of the service orders that are created.</span></span>

6.  <span data-ttu-id="d7f33-115">Vælg transaktionstyperne i feltgruppen **Medtag posteringstyper**.</span><span class="sxs-lookup"><span data-stu-id="d7f33-115">Select transaction types in the **Include transaction types** field group.</span></span> <span data-ttu-id="d7f33-116">Transaktionstyperne er de linjer, der oprettes i en serviceaftale, og hver af de transaktionstyper, du vælger, genererer flere serviceordrer ud fra den serviceperiode, der er angivet i serviceaftalelinjen.</span><span class="sxs-lookup"><span data-stu-id="d7f33-116">The transaction types represent the lines that are created in the service agreement, and each transaction type that you select generates several service orders, depending on the service interval that is specified on the service agreement line.</span></span>

7.  <span data-ttu-id="d7f33-117">Markér afkrydsningsfeltet **Fortløbende**, hvis du vil oprette serviceordrer, der mangler i en fortløbende serie af serviceaftaler.</span><span class="sxs-lookup"><span data-stu-id="d7f33-117">To create any service orders that are missing from continuous series of service orders, select the **Continuous** check box.</span></span>

8.  <span data-ttu-id="d7f33-118">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="d7f33-118">Click **OK**.</span></span>

## <a name="create-service-orders-automatically-for-several-service-agreements"></a><span data-ttu-id="d7f33-119">Oprette serviceordrer automatisk for flere serviceaftaler</span><span class="sxs-lookup"><span data-stu-id="d7f33-119">Create service orders automatically for several service agreements</span></span>

1.  <span data-ttu-id="d7f33-120">Klik på **Servicestyring** \> **Periodisk** \> **Serviceordrer** \> **Opret serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="d7f33-120">Click **Service management** \> **Periodic** \> **Service orders** \> **Create service orders**.</span></span>

2.  <span data-ttu-id="d7f33-121">Klik på **Vælg** for at tilføje eller fjerne kriterier, som bruges til at oprette serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="d7f33-121">Click **Select** to make selections to add or remove criteria to use to create service orders.</span></span>

3.  <span data-ttu-id="d7f33-122">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="d7f33-122">Click **OK**.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7f33-123">Se også</span><span class="sxs-lookup"><span data-stu-id="d7f33-123">See also</span></span>

[<span data-ttu-id="d7f33-124">Serviceordrer</span><span class="sxs-lookup"><span data-stu-id="d7f33-124">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="d7f33-125">Oprette serviceordrer automatisk</span><span class="sxs-lookup"><span data-stu-id="d7f33-125">Automatically create service orders</span></span>](auto-create-service-orders.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]