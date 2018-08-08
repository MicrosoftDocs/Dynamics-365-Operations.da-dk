---
title: Annuller serviceordrer
description: "Du kan annullere en serviceordre eller serviceordrelinje fra selve serviceordren, eller du kan annullere flere serviceordrer ved at køre et periodisk job."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 1495fa139ea2c3cb7f2450b402126822f5549f60
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---

# <a name="cancel-service-orders"></a><span data-ttu-id="70fe5-103">Annuller serviceordrer</span><span class="sxs-lookup"><span data-stu-id="70fe5-103">Cancel service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="70fe5-104">Du kan annullere en serviceordre eller serviceordrelinje fra selve serviceordren, eller du kan annullere flere serviceordrer ved at køre et periodisk job.</span><span class="sxs-lookup"><span data-stu-id="70fe5-104">You can cancel a service order or service order line from the service order itself, or you can cancel multiple service orders by running a periodic job.</span></span>


> [!NOTE]
> <P><span data-ttu-id="70fe5-105">Serviceordrer kan ikke annulleres, hvis stadiet i serviceordren ikke tillader annullering, hvis der er varebehov i serviceordren, eller hvis serviceordren allerede er bogført.</span><span class="sxs-lookup"><span data-stu-id="70fe5-105">Service orders cannot be canceled if the stage of the service order does not allow cancelation, if the service order has item requirements, or if the service order has already been posted.</span></span></P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a><span data-ttu-id="70fe5-106">Annullere en serviceordre i formen Serviceordrer</span><span class="sxs-lookup"><span data-stu-id="70fe5-106">Cancel a service order in the Service orders form</span></span>

1.  <span data-ttu-id="70fe5-107">Klik på **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="70fe5-107">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="70fe5-108">Vælg serviceordren, og klik på **Annuller ordre** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="70fe5-108">Select the service order, and on the Action Pane, click **Cancel order**.</span></span>

## <a name="cancel-a-service-order-line"></a><span data-ttu-id="70fe5-109">Annullere en serviceordrelinje</span><span class="sxs-lookup"><span data-stu-id="70fe5-109">Cancel a service order line</span></span>

1.  <span data-ttu-id="70fe5-110">Klik på **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="70fe5-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="70fe5-111">Dobbeltklik på den serviceordre, der indeholder den linje, du vil annullere.</span><span class="sxs-lookup"><span data-stu-id="70fe5-111">Double-click the service order that contains the line you want to cancel.</span></span>

2.  <span data-ttu-id="70fe5-112">Vælg den serviceordrelinje, du vil annullere, og klik derefter på **Annuller ordrelinje** for at ændre linjens status til **Annulleret**.</span><span class="sxs-lookup"><span data-stu-id="70fe5-112">Select the service order line that you want to cancel, and then click **Cancel order line** to change the status of the line to **Canceled**.</span></span>


> [!TIP]
> <P><span data-ttu-id="70fe5-113">Du kan tilbageføre annulleringen af en serviceordrelinje og ændre dens status tilbage til <STRONG>Oprettet</STRONG> ved at klikke på <STRONG>Fortryd annullering</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="70fe5-113">To reverse the cancellation of a service order line and change the status back to <STRONG>Created</STRONG>, click <STRONG>Revoke cancel</STRONG>.</span></span></P>


## <a name="cancel-multiple-service-orders"></a><span data-ttu-id="70fe5-114">Annullere flere serviceordrer</span><span class="sxs-lookup"><span data-stu-id="70fe5-114">Cancel multiple service orders</span></span>

1.  <span data-ttu-id="70fe5-115">Klik på **Servicestyring** \> **Periodisk** \> **Serviceordrer** \> **Annuller serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="70fe5-115">Click **Service management** \> **Periodic** \> **Service orders** \> **Cancel service orders**.</span></span>

2.  <span data-ttu-id="70fe5-116">Klik på knappen **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="70fe5-116">Click the **Select** button.</span></span>

3.  <span data-ttu-id="70fe5-117">Vælg de serviceordrer, du vil annullere, i kolonnen **Kriterier** i formularen **Forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="70fe5-117">In the **Inquiry** form, in the **Criteria** column, select the service orders that you want to cancel.</span></span>

4.  <span data-ttu-id="70fe5-118">Klik på **OK** for at lukke formularen **Forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="70fe5-118">Click **OK** to close the **Inquiry** form.</span></span>

5.  <span data-ttu-id="70fe5-119">Markér afkrydsningsfeltet **Vis infolog** for at generere en infolog, der viser de annullerede serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="70fe5-119">Select the **Show Infolog** check box to generate an Infolog that lists the canceled service orders.</span></span>

6.  <span data-ttu-id="70fe5-120">Markér afkrydsningsfeltet **Fortryd annullering**, hvis du vil fortryde statusangivelsen **Annulleret** for en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="70fe5-120">Select the **Revoke cancel** check box if you want to reverse the **Canceled** status of a service order.</span></span>

7.  <span data-ttu-id="70fe5-121">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="70fe5-121">Click **OK**.</span></span>

<span data-ttu-id="70fe5-122">De valgte serviceordrer annulleres, eller deres status **Annulleret** ændres til **Igangværende**.</span><span class="sxs-lookup"><span data-stu-id="70fe5-122">The selected service orders are either canceled or their progress status of **Canceled** has been reversed to **In process**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="70fe5-123">Hvis du markerer afkrydsningsfeltet <STRONG>Fortryd annullering</STRONG>, fortrydes statusangivelsen <STRONG>Annulleret</STRONG> for serviceordrerne, mens serviceordrer med statusangivelsen <STRONG>Igangværende</STRONG> ikke annulleres.</span><span class="sxs-lookup"><span data-stu-id="70fe5-123">If you select the <STRONG>Revoke cancel</STRONG> check box, service orders with a progress status of <STRONG>Canceled</STRONG> are reversed and service orders with a progress status of <STRONG>In process</STRONG> are not canceled.</span></span></P>


  



