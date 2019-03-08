---
title: Serviceobjektrelationer
description: Du kan oprette serviceobjektrelationer mellem et serviceobjekt og en serviceaftale eller en serviceordre.
author: ShylaThompson
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 03047b3eccf3c90d4cf7426ddaec83f10dbea1b0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "314365"
---
# <a name="service-object-relations"></a><span data-ttu-id="b3ae2-103">Serviceobjektrelationer</span><span class="sxs-lookup"><span data-stu-id="b3ae2-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3ae2-104">Du kan oprette serviceobjektrelationer mellem et serviceobjekt og en serviceaftale eller en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="b3ae2-105">Når du opretter en relation, knyttes serviceobjektet til serviceaftalen eller serviceordren.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="b3ae2-106">Når relationen er oprettet, kan du knytte serviceobjektet til alle linjer i serviceaftalen eller serviceordren.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="b3ae2-107">Styklisteskabeloner</span><span class="sxs-lookup"><span data-stu-id="b3ae2-107">Template BOMs</span></span>

<span data-ttu-id="b3ae2-108">Du kan også angive en styklisteskabelon til objektrelationen.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="b3ae2-109">Styklisteskabelonen er en stykliste til det objekt, service udføres for.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="b3ae2-110">Hvis du erstatter en komponentgruppe i serviceobjektet under et servicebesøg, kan du registrere denne ændring i servicestyklisten ved at bruge formen Serviceobjekter.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="b3ae2-111">Eksempel</span><span class="sxs-lookup"><span data-stu-id="b3ae2-111">Example</span></span>

<span data-ttu-id="b3ae2-112">Du opretter en serviceaftale for servicering af to elevatorer hos en kunde.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="b3ae2-113">Serviceaftalen her id'et ID SAL-001.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="b3ae2-114">Elevatorerne er i formen Serviceobjekter angivet som objekter, EL-S/1000 og EL-L/1000.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="b3ae2-115">Du knytter serviceobjekterne, EL-S/1000 og EL-L/1000, til serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="b3ae2-116">Du ønsker at registrere ændringer i styklisten for serviceobjektet, mens du erstatter komponentdelene i objektet, og derfor knytter du en servicestykliste til serviceobjektrelationen som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="b3ae2-117">serviceobjekt</span><span class="sxs-lookup"><span data-stu-id="b3ae2-117">Service object</span></span> | <span data-ttu-id="b3ae2-118">Relation – serviceaftale</span><span class="sxs-lookup"><span data-stu-id="b3ae2-118">Relation – Service agreement</span></span> | <span data-ttu-id="b3ae2-119">Servicestykliste</span><span class="sxs-lookup"><span data-stu-id="b3ae2-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="b3ae2-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="b3ae2-120">EL-S/1000</span></span>      | <span data-ttu-id="b3ae2-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="b3ae2-121">ID SAL-001</span></span>                   | <span data-ttu-id="b3ae2-122">Stykliste-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="b3ae2-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="b3ae2-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="b3ae2-123">EL-L/1000</span></span>      | <span data-ttu-id="b3ae2-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="b3ae2-124">ID SAL-001</span></span>                   | <span data-ttu-id="b3ae2-125">Stykliste-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="b3ae2-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="b3ae2-126">Da der findes serviceobjektrelationer til aftalen, kan du nu oprette serviceaftalelinjer med disse objekter som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="b3ae2-127">Konteringstype</span><span class="sxs-lookup"><span data-stu-id="b3ae2-127">Transaction type</span></span> | <span data-ttu-id="b3ae2-128">Kategori</span><span class="sxs-lookup"><span data-stu-id="b3ae2-128">Category</span></span>           | <span data-ttu-id="b3ae2-129">serviceobjekt</span><span class="sxs-lookup"><span data-stu-id="b3ae2-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="b3ae2-130">Time</span><span class="sxs-lookup"><span data-stu-id="b3ae2-130">Hour</span></span>             | <span data-ttu-id="b3ae2-131">Inspektion</span><span class="sxs-lookup"><span data-stu-id="b3ae2-131">Inspection</span></span>         | <span data-ttu-id="b3ae2-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="b3ae2-132">EL-S/1000</span></span>      |
| <span data-ttu-id="b3ae2-133">Time</span><span class="sxs-lookup"><span data-stu-id="b3ae2-133">Hour</span></span>             | <span data-ttu-id="b3ae2-134">Rensning af gearkasse</span><span class="sxs-lookup"><span data-stu-id="b3ae2-134">Gear box cleaning</span></span>  | <span data-ttu-id="b3ae2-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="b3ae2-135">EL-S/1000</span></span>      |
| <span data-ttu-id="b3ae2-136">Vare</span><span class="sxs-lookup"><span data-stu-id="b3ae2-136">Item</span></span>             | <span data-ttu-id="b3ae2-137">Materialer til rensning</span><span class="sxs-lookup"><span data-stu-id="b3ae2-137">Cleaning materials</span></span> | <span data-ttu-id="b3ae2-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="b3ae2-138">EL-S/1000</span></span>      |
| <span data-ttu-id="b3ae2-139">Time</span><span class="sxs-lookup"><span data-stu-id="b3ae2-139">Hour</span></span>             | <span data-ttu-id="b3ae2-140">Inspektion</span><span class="sxs-lookup"><span data-stu-id="b3ae2-140">Inspection</span></span>         | <span data-ttu-id="b3ae2-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="b3ae2-141">EL-L/1000</span></span>      |
| <span data-ttu-id="b3ae2-142">Time</span><span class="sxs-lookup"><span data-stu-id="b3ae2-142">Hour</span></span>             | <span data-ttu-id="b3ae2-143">Rensning af gearkasse</span><span class="sxs-lookup"><span data-stu-id="b3ae2-143">Gearbox cleaning</span></span>   | <span data-ttu-id="b3ae2-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="b3ae2-144">EL-L/1000</span></span>      |
| <span data-ttu-id="b3ae2-145">Vare</span><span class="sxs-lookup"><span data-stu-id="b3ae2-145">Item</span></span>             | <span data-ttu-id="b3ae2-146">Materialer til rensning</span><span class="sxs-lookup"><span data-stu-id="b3ae2-146">Cleaning materials</span></span> | <span data-ttu-id="b3ae2-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="b3ae2-147">EL-L/1000</span></span>      |

<span data-ttu-id="b3ae2-148">Under et servicebesøg er du nødt til at udskift gearkassen til elevator EL-S/1000.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="b3ae2-149">Når en komponentdel i objektet skal udskiftes, kan du få adgang til styklistedesigneren ved at bruge den serviceobjektrelation, du har angivet for den aktuelle serviceaftale.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="b3ae2-150">Få adgang til styklistedesigneren ved brug af en serviceobjektrelation</span><span class="sxs-lookup"><span data-stu-id="b3ae2-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="b3ae2-151">Serviceaftaler</span><span class="sxs-lookup"><span data-stu-id="b3ae2-151">Service agreements</span></span>
2. <span data-ttu-id="b3ae2-152">Dobbeltklik på en serviceaftale, eller klik på Serviceaftale for at oprette en ny serviceaftale.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="b3ae2-153">Klik på fanen Opsætning.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="b3ae2-154">Hvis du vil knytte en styklisteskabelon til serviceaftalen, skal du klikke på Serviceobjekter.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="b3ae2-155">Klik på Designer for at åbne formen Designer og redigere styklisteskabelonen, i formen Serviceobjekter.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="b3ae2-156">Automatisk oprettede serviceordrer</span><span class="sxs-lookup"><span data-stu-id="b3ae2-156">Automatically created service orders</span></span>

<span data-ttu-id="b3ae2-157">Hvis serviceordrer oprettes automatisk for en serviceaftale, oprettes serviceobjektrelationerne i aftalen også i serviceordrerne.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>

