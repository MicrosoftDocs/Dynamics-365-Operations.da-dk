---
title: Oprette serviceobjektrelationer
description: I dette emne beskrives, hvordan du opretter serviceobjektrelationer for en serviceaftale og en serviceordre.
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c27070436139f784af690900a3f1ab108a809d03
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="create-service-object-relations"></a><span data-ttu-id="a4407-103">Oprette serviceobjektrelationer</span><span class="sxs-lookup"><span data-stu-id="a4407-103">Create service object relations</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a4407-104">I dette emne beskrives, hvordan du opretter serviceobjektrelationer for en serviceaftale og en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="a4407-104">This topic describes how to create service object relations for a service agreement and a service order.</span></span> <span data-ttu-id="a4407-105">Når du opretter en serviceobjektrelation, knyttes serviceobjektet til en serviceaftale eller serviceordre.</span><span class="sxs-lookup"><span data-stu-id="a4407-105">When you a create service object relation, you associate the service object to a service agreement or service order.</span></span> <span data-ttu-id="a4407-106">Når en kunde anmoder om service for en vare, der er et serviceobjekt, kan du vælge serviceobjektet på listen over serviceobjektrelationer.</span><span class="sxs-lookup"><span data-stu-id="a4407-106">When a customer requests service for an item that is a service object, you can select the service object from the list of service object relations.</span></span>

## <a name="create-a-service-object-relation-for-a-service-agreement"></a><span data-ttu-id="a4407-107">Oprette en serviceobjektrelation for en serviceaftale</span><span class="sxs-lookup"><span data-stu-id="a4407-107">Create a service object relation for a service agreement</span></span>

<span data-ttu-id="a4407-108">Brug følgende trin til at oprette en serviceobjektrelation for en serviceaftale:</span><span class="sxs-lookup"><span data-stu-id="a4407-108">Use the following steps to create a service object relation for a service agreement:</span></span>

1.  <span data-ttu-id="a4407-109">Klik på **Servicestyring** \> **Almindelige** \> **Serviceaftaler** \> **Serviceaftaler**.</span><span class="sxs-lookup"><span data-stu-id="a4407-109">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="a4407-110">På listen **Serviceaftaler** skal du vælge en eksisterende serviceaftale eller klikke på **Ny** for at oprette en ny serviceaftale.</span><span class="sxs-lookup"><span data-stu-id="a4407-110">In the **Service agreements** list, select an existing service agreement, or click **New** to create a new service agreement.</span></span>

3.  <span data-ttu-id="a4407-111">Klik på **Serviceobjekter** i gruppen **Relationer** under fanen **Serviceaftale** i **Handlingsrude** i formularen **Serviceaftaler**.</span><span class="sxs-lookup"><span data-stu-id="a4407-111">In the **Service agreements** form, on the **Action Pane**, on the **Service agreement** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="a4407-112">I formularen **Serviceobjekter** skal du klikke på **Ny** og derefter vælge et serviceobjekt for denne serviceaftale.</span><span class="sxs-lookup"><span data-stu-id="a4407-112">In the **Service objects** form, click **New**, and then select a service object for this service agreement.</span></span>

5.  <span data-ttu-id="a4407-113">Hvis du vil tildele en styklisteskabelon til serviceaftalen, skal du klikke på **Funktioner** og derefter vælge **Vedhæft styklisteskabelon**.</span><span class="sxs-lookup"><span data-stu-id="a4407-113">To assign a template bill of materials (BOM) to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="a4407-114">Brug formularen **Vedhæft styklisteskabelon**, feltet **Styklisteskabelon** til at vælge en styklisteskabelon, og klik derefter på OK.</span><span class="sxs-lookup"><span data-stu-id="a4407-114">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 

## <a name="create-a-service-object-relation-for-a-service-order"></a><span data-ttu-id="a4407-115">Oprette en serviceobjektrelation for en serviceordre</span><span class="sxs-lookup"><span data-stu-id="a4407-115">Create a service object relation for a service order</span></span>

<span data-ttu-id="a4407-116">Brug følgende trin til at oprette en serviceobjektrelation for en serviceordre:</span><span class="sxs-lookup"><span data-stu-id="a4407-116">Use the following steps to create a service object relation for a service order:</span></span>

1.  <span data-ttu-id="a4407-117">Klik på **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="a4407-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="a4407-118">Vælg en eksisterende serviceordre på listen **Serviceordrer**, eller opret en ny serviceordre.</span><span class="sxs-lookup"><span data-stu-id="a4407-118">In the **Service orders** list, select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="a4407-119">Klik på **Serviceordrer** i gruppen **Relationer** under fanen **Serviceordre** i **Handlingsrude** i formularen **Serviceaftaler**.</span><span class="sxs-lookup"><span data-stu-id="a4407-119">In the **Service orders** form, on the **Action Pane**, on the **Service order** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="a4407-120">I formularen **Serviceobjekter** skal du klikke på **Ny** og derefter vælge et serviceobjekt for denne serviceordre.</span><span class="sxs-lookup"><span data-stu-id="a4407-120">In the **Service objects** form, click **New**, and then select a service object for this service order.</span></span>

5.  <span data-ttu-id="a4407-121">Hvis du vil tildele en styklisteskabelon til serviceaftalen, skal du klikke på **Funktioner** og derefter vælge **Vedhæft styklisteskabelon**.</span><span class="sxs-lookup"><span data-stu-id="a4407-121">To assign a template BOM to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="a4407-122">Brug formularen **Vedhæft styklisteskabelon**, feltet **Styklisteskabelon** til at vælge en styklisteskabelon, og klik derefter på OK.</span><span class="sxs-lookup"><span data-stu-id="a4407-122">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 


## <a name="see-also"></a><span data-ttu-id="a4407-123">Se også</span><span class="sxs-lookup"><span data-stu-id="a4407-123">See also</span></span>

[<span data-ttu-id="a4407-124">Serviceobjekter</span><span class="sxs-lookup"><span data-stu-id="a4407-124">Service objects</span></span>](service-objects.md)

[<span data-ttu-id="a4407-125">Serviceobjektrelationer</span><span class="sxs-lookup"><span data-stu-id="a4407-125">service object relations</span></span>](service-object-relations.md)

[<span data-ttu-id="a4407-126">Styklisteskabeloner</span><span class="sxs-lookup"><span data-stu-id="a4407-126">Template BOMs</span></span>](template-boms.md)

  


