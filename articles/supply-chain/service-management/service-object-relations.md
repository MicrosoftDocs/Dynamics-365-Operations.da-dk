---
title: Serviceobjektrelationer
description: Du kan oprette serviceobjektrelationer mellem et serviceobjekt og en serviceaftale eller en serviceordre.
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectRelation
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
ms.openlocfilehash: 90c16653dee0614beaad8e4693c012b67a54b297
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="service-object-relations"></a><span data-ttu-id="6f640-103">Serviceobjektrelationer</span><span class="sxs-lookup"><span data-stu-id="6f640-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f640-104">Du kan oprette serviceobjektrelationer mellem et serviceobjekt og en serviceaftale eller en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="6f640-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="6f640-105">Når du opretter en relation, knyttes serviceobjektet til serviceaftalen eller serviceordren.</span><span class="sxs-lookup"><span data-stu-id="6f640-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="6f640-106">Når relationen er oprettet, kan du knytte serviceobjektet til alle linjer i serviceaftalen eller serviceordren.</span><span class="sxs-lookup"><span data-stu-id="6f640-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="6f640-107">Styklisteskabeloner</span><span class="sxs-lookup"><span data-stu-id="6f640-107">Template BOMs</span></span>

<span data-ttu-id="6f640-108">Du kan også angive en styklisteskabelon til objektrelationen.</span><span class="sxs-lookup"><span data-stu-id="6f640-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="6f640-109">Styklisteskabelonen er en stykliste til det objekt, service udføres for.</span><span class="sxs-lookup"><span data-stu-id="6f640-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="6f640-110">Hvis du erstatter en komponentgruppe i serviceobjektet under et servicebesøg, kan du registrere denne ændring i servicestyklisten ved at bruge formen Serviceobjekter.</span><span class="sxs-lookup"><span data-stu-id="6f640-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="6f640-111">Eksempel</span><span class="sxs-lookup"><span data-stu-id="6f640-111">Example</span></span>

<span data-ttu-id="6f640-112">Du opretter en serviceaftale for servicering af to elevatorer hos en kunde.</span><span class="sxs-lookup"><span data-stu-id="6f640-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="6f640-113">Serviceaftalen her id'et ID SAL-001.</span><span class="sxs-lookup"><span data-stu-id="6f640-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="6f640-114">Elevatorerne er i formen Serviceobjekter angivet som objekter, EL-S/1000 og EL-L/1000.</span><span class="sxs-lookup"><span data-stu-id="6f640-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="6f640-115">Du knytter serviceobjekterne, EL-S/1000 og EL-L/1000, til serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="6f640-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="6f640-116">Du ønsker at registrere ændringer i styklisten for serviceobjektet, mens du erstatter komponentdelene i objektet, og derfor knytter du en servicestykliste til serviceobjektrelationen som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="6f640-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="6f640-117">serviceobjekt</span><span class="sxs-lookup"><span data-stu-id="6f640-117">Service object</span></span> | <span data-ttu-id="6f640-118">Relation – serviceaftale</span><span class="sxs-lookup"><span data-stu-id="6f640-118">Relation – Service agreement</span></span> | <span data-ttu-id="6f640-119">Servicestykliste</span><span class="sxs-lookup"><span data-stu-id="6f640-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="6f640-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="6f640-120">EL-S/1000</span></span>      | <span data-ttu-id="6f640-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="6f640-121">ID SAL-001</span></span>                   | <span data-ttu-id="6f640-122">Stykliste-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="6f640-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="6f640-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="6f640-123">EL-L/1000</span></span>      | <span data-ttu-id="6f640-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="6f640-124">ID SAL-001</span></span>                   | <span data-ttu-id="6f640-125">Stykliste-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="6f640-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="6f640-126">Da der findes serviceobjektrelationer til aftalen, kan du nu oprette serviceaftalelinjer med disse objekter som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="6f640-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="6f640-127">Konteringstype</span><span class="sxs-lookup"><span data-stu-id="6f640-127">Transaction type</span></span> | <span data-ttu-id="6f640-128">Kategori</span><span class="sxs-lookup"><span data-stu-id="6f640-128">Category</span></span>           | <span data-ttu-id="6f640-129">serviceobjekt</span><span class="sxs-lookup"><span data-stu-id="6f640-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="6f640-130">Time</span><span class="sxs-lookup"><span data-stu-id="6f640-130">Hour</span></span>             | <span data-ttu-id="6f640-131">Inspektion</span><span class="sxs-lookup"><span data-stu-id="6f640-131">Inspection</span></span>         | <span data-ttu-id="6f640-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="6f640-132">EL-S/1000</span></span>      |
| <span data-ttu-id="6f640-133">Time</span><span class="sxs-lookup"><span data-stu-id="6f640-133">Hour</span></span>             | <span data-ttu-id="6f640-134">Rensning af gearkasse</span><span class="sxs-lookup"><span data-stu-id="6f640-134">Gear box cleaning</span></span>  | <span data-ttu-id="6f640-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="6f640-135">EL-S/1000</span></span>      |
| <span data-ttu-id="6f640-136">Vare</span><span class="sxs-lookup"><span data-stu-id="6f640-136">Item</span></span>             | <span data-ttu-id="6f640-137">Materialer til rensning</span><span class="sxs-lookup"><span data-stu-id="6f640-137">Cleaning materials</span></span> | <span data-ttu-id="6f640-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="6f640-138">EL-S/1000</span></span>      |
| <span data-ttu-id="6f640-139">Time</span><span class="sxs-lookup"><span data-stu-id="6f640-139">Hour</span></span>             | <span data-ttu-id="6f640-140">Inspektion</span><span class="sxs-lookup"><span data-stu-id="6f640-140">Inspection</span></span>         | <span data-ttu-id="6f640-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="6f640-141">EL-L/1000</span></span>      |
| <span data-ttu-id="6f640-142">Time</span><span class="sxs-lookup"><span data-stu-id="6f640-142">Hour</span></span>             | <span data-ttu-id="6f640-143">Rensning af gearkasse</span><span class="sxs-lookup"><span data-stu-id="6f640-143">Gearbox cleaning</span></span>   | <span data-ttu-id="6f640-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="6f640-144">EL-L/1000</span></span>      |
| <span data-ttu-id="6f640-145">Vare</span><span class="sxs-lookup"><span data-stu-id="6f640-145">Item</span></span>             | <span data-ttu-id="6f640-146">Materialer til rensning</span><span class="sxs-lookup"><span data-stu-id="6f640-146">Cleaning materials</span></span> | <span data-ttu-id="6f640-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="6f640-147">EL-L/1000</span></span>      |

<span data-ttu-id="6f640-148">Under et servicebesøg er du nødt til at udskift gearkassen til elevator EL-S/1000.</span><span class="sxs-lookup"><span data-stu-id="6f640-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="6f640-149">Når en komponentdel i objektet skal udskiftes, kan du få adgang til styklistedesigneren ved at bruge den serviceobjektrelation, du har angivet for den aktuelle serviceaftale.</span><span class="sxs-lookup"><span data-stu-id="6f640-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="6f640-150">Få adgang til styklistedesigneren ved brug af en serviceobjektrelation</span><span class="sxs-lookup"><span data-stu-id="6f640-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="6f640-151">Serviceaftaler</span><span class="sxs-lookup"><span data-stu-id="6f640-151">Service agreements</span></span>
2. <span data-ttu-id="6f640-152">Dobbeltklik på en serviceaftale, eller klik på Serviceaftale for at oprette en ny serviceaftale.</span><span class="sxs-lookup"><span data-stu-id="6f640-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="6f640-153">Klik på fanen Opsætning.</span><span class="sxs-lookup"><span data-stu-id="6f640-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="6f640-154">Hvis du vil knytte en styklisteskabelon til serviceaftalen, skal du klikke på Serviceobjekter.</span><span class="sxs-lookup"><span data-stu-id="6f640-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="6f640-155">Klik på Designer for at åbne formen Designer og redigere styklisteskabelonen, i formen Serviceobjekter.</span><span class="sxs-lookup"><span data-stu-id="6f640-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="6f640-156">Automatisk oprettede serviceordrer</span><span class="sxs-lookup"><span data-stu-id="6f640-156">Automatically created service orders</span></span>

<span data-ttu-id="6f640-157">Hvis serviceordrer oprettes automatisk for en serviceaftale, oprettes serviceobjektrelationerne i aftalen også i serviceordrerne.</span><span class="sxs-lookup"><span data-stu-id="6f640-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>


