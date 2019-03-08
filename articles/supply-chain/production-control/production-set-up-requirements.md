---
title: Krav til produktionsopsætning
description: Denne artikel indeholder oplysninger om opsætningskrav, før du kan arbejde med Produktionsstyring.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b811c11271097f4bb7910c34f7775955abba526d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "366621"
---
# <a name="production-setup-requirements"></a><span data-ttu-id="141b2-103">Krav til produktionsopsætning</span><span class="sxs-lookup"><span data-stu-id="141b2-103">Production setup requirements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="141b2-104">Denne artikel indeholder oplysninger om opsætningskrav, før du kan arbejde med Produktionsstyring.</span><span class="sxs-lookup"><span data-stu-id="141b2-104">This article provides information about setup requirements before you can work with Production control.</span></span> 

<span data-ttu-id="141b2-105">Produktionsstyring er integreret med funktioner i andre moduler.</span><span class="sxs-lookup"><span data-stu-id="141b2-105">Production control is integrated with features in other modules.</span></span> <span data-ttu-id="141b2-106">Denne integration giver dig mulighed for at ændre produktionsordrer og sikre, at de automatisk opdateres i alle andre relaterede processer og beregninger i systemet.</span><span class="sxs-lookup"><span data-stu-id="141b2-106">This interconnectivity lets you change production orders and make sure that they are automatically updated in all other related processes and calculations in the system.</span></span> <span data-ttu-id="141b2-107">Følgende opsætningsprocesser er angivet i den rækkefølge, du skal udføre dem i.</span><span class="sxs-lookup"><span data-stu-id="141b2-107">The following setup processes are listed in the order that you should complete them in.</span></span>

## <a name="required-baseline-setup-in-other-modules"></a><span data-ttu-id="141b2-108">Nødvendig grundlæggende opsætning i andre moduler</span><span class="sxs-lookup"><span data-stu-id="141b2-108">Required baseline setup in other modules</span></span>
<span data-ttu-id="141b2-109">Der skal angives oplysninger i andre moduler, før du kan arbejde i Produktionsstyring.</span><span class="sxs-lookup"><span data-stu-id="141b2-109">Information in other modules must be set up before you can work with Production control.</span></span> <span data-ttu-id="141b2-110">Opsætningen omfatter følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="141b2-110">This setup includes the following tasks:</span></span>

-   <span data-ttu-id="141b2-111">Opsætning af generelle firmaoplysninger.</span><span class="sxs-lookup"><span data-stu-id="141b2-111">Set up general company information.</span></span>
-   <span data-ttu-id="141b2-112">Opsætning af finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="141b2-112">Set up the general ledger.</span></span>
-   <span data-ttu-id="141b2-113">Definition af varegrupper.</span><span class="sxs-lookup"><span data-stu-id="141b2-113">Define item groups.</span></span>
-   <span data-ttu-id="141b2-114">Opsætning af finanskonti for varegrupper.</span><span class="sxs-lookup"><span data-stu-id="141b2-114">Set up ledger accounts for item groups.</span></span>
-   <span data-ttu-id="141b2-115">Opsætning af lagervaretabellen i Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="141b2-115">Set up the inventory item table in Inventory management.</span></span>
-   <span data-ttu-id="141b2-116">Oprette styklister og styklisteversioner i Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="141b2-116">Create bills of materials (BOMs) and BOM versions in Inventory management.</span></span>

## <a name="required-calendar-and-resource-setup"></a><span data-ttu-id="141b2-117">Krævet kalender- og ressourceopsætning</span><span class="sxs-lookup"><span data-stu-id="141b2-117">Required calendar and resource setup</span></span>
<span data-ttu-id="141b2-118">Før du bruger Produktionsstyring, skal du åbne Virksomhedsadministration og oprette og definere kalender- og operationsressourcer i følgende rækkefølge:</span><span class="sxs-lookup"><span data-stu-id="141b2-118">Before you use Production control, open Organization administration, and create and define the calendar and operations resources in the following order:</span></span>

1.  <span data-ttu-id="141b2-119">**Arbejdstidsskabeloner** – Opret arbejdstidsskabeloner for at definere de tider, der er tilgængelige til produktionsplanlægning.</span><span class="sxs-lookup"><span data-stu-id="141b2-119">**Working time templates** – Set up working time templates to define the times that are available for production scheduling.</span></span>
2.  <span data-ttu-id="141b2-120">**Kalendere** – Opret arbejdstidskalendere for at definere, hvilke dage i året der er tilgængelige for produktionsplanlægning.</span><span class="sxs-lookup"><span data-stu-id="141b2-120">**Calendars** – Set up working time calendars to define the days of the year that are available for production scheduling.</span></span>
3.  <span data-ttu-id="141b2-121">**Ressourcegrupper**– Opret ressourcegrupper til gruppering af operationsressourcer, så du kan få et overblik over eventuel ledig kapacitet, når du kører planlægning.</span><span class="sxs-lookup"><span data-stu-id="141b2-121">**Resource groups** – Set up resource groups to group the operations resources, so that you can get an overview of any free capacity when you run scheduling.</span></span> <span data-ttu-id="141b2-122">Du behøver ikke at oprette ressourcegrupper, før du opretter operationsressourcer.</span><span class="sxs-lookup"><span data-stu-id="141b2-122">You don't have to set up resource groups before you set up operations resources.</span></span> <span data-ttu-id="141b2-123">Det anbefales dog, at du forstår, hvordan du kan gruppere ressourcer, når du konfigurerer Produktionsstyring.</span><span class="sxs-lookup"><span data-stu-id="141b2-123">However, we recommend that you understand how to group resources when you set up Production control.</span></span>
4.  <span data-ttu-id="141b2-124">**Ressourcer** – Opret operationsressourcer for at definere de forskellige ressourcer, der skal bruges til at fuldføre produktionsprocessen og til at planlægge med henblik på kapacitet.</span><span class="sxs-lookup"><span data-stu-id="141b2-124">**Resources** – Set up operations resources to define the resources that are used to complete the production process and plan for capacity.</span></span>

## <a name="required-production-parameters-setup"></a><span data-ttu-id="141b2-125">Nødvendig opsætning af produktionsparametre</span><span class="sxs-lookup"><span data-stu-id="141b2-125">Required production parameters setup</span></span>
<span data-ttu-id="141b2-126">**Produktionsstyringsparametre** – Konfigurer grundlæggende produktionsparametre for at definere, hvordan systemet skal håndtere og behandle produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="141b2-126">**Production control parameters** – Set up basic production parameters to define how the system handles and processes production orders.</span></span> <span data-ttu-id="141b2-127">Angive, hvordan produktionsordrer oprettes, forkalkuleres, planlægges og forbruges.</span><span class="sxs-lookup"><span data-stu-id="141b2-127">Define how production orders are created, estimated, scheduled, and consumed.</span></span> <span data-ttu-id="141b2-128">Du kan også vælge, hvilken form for feedback du ønsker, og hvordan omkostningsregnskabet skal udføres.</span><span class="sxs-lookup"><span data-stu-id="141b2-128">You can also select what kind of feedback you want and how cost accounting is done.</span></span>

## <a name="required-journal-name-identification"></a><span data-ttu-id="141b2-129">Nødvendigt id for kladdenavn</span><span class="sxs-lookup"><span data-stu-id="141b2-129">Required journal name identification</span></span>
<span data-ttu-id="141b2-130">**Produktionskladdenavne** – Angiv de produktionskladdenavne, der bruges til at registrere og bogføre posteringer.</span><span class="sxs-lookup"><span data-stu-id="141b2-130">**Production journal names** – Specify the production journal names that are used to record and post transactions.</span></span>

## <a name="setup-if-you-use-operations"></a><span data-ttu-id="141b2-131">Opsætning, hvis du bruger operationer</span><span class="sxs-lookup"><span data-stu-id="141b2-131">Setup if you use operations</span></span>
<span data-ttu-id="141b2-132">Operationer repræsenterer de bestemte aktiviteter, der udføres for at producere færdigvaren.</span><span class="sxs-lookup"><span data-stu-id="141b2-132">Operations represent the specific activities that are completed to produce the finished product.</span></span> <span data-ttu-id="141b2-133">**Bemærk!** Du skal kende de aktivitetstyper, der er nødvendige for at producere varen, og rækkefølgen og prioriteter for disse aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="141b2-133">**Note:** You must know the types of activities that are required in order to produce your item, and the order and priorities of those activities.</span></span> <span data-ttu-id="141b2-134">Du skal også vide, hvilke ressourcer der er involveret, og hvor mange.</span><span class="sxs-lookup"><span data-stu-id="141b2-134">You must also know which resources are involved, and how many.</span></span>

1.  <span data-ttu-id="141b2-135">**Operationer** – Angiv parametre, der repræsenterer de opgaver, som skal udføres for at producere færdigvaren.</span><span class="sxs-lookup"><span data-stu-id="141b2-135">**Operations** – Set up operations to represent the tasks that must be completed to produce the finished item.</span></span>
2.  <span data-ttu-id="141b2-136">**Relationer** – Opret operationsrelationer for at angive detaljerede egenskaber.</span><span class="sxs-lookup"><span data-stu-id="141b2-136">**Relations** – Set up operation relations to establish detailed properties.</span></span> <span data-ttu-id="141b2-137">Hvis du vil definere operationsrelationer, skal du klikke på **Relationer** på siden **Operationer**.</span><span class="sxs-lookup"><span data-stu-id="141b2-137">To define operation relations, click **Relations** on the **Operations** page.</span></span>

## <a name="setup-if-you-use-routes"></a><span data-ttu-id="141b2-138">Opsætning, hvis du bruger ruter</span><span class="sxs-lookup"><span data-stu-id="141b2-138">Setup if you use routes</span></span>
<span data-ttu-id="141b2-139">Hvis du arbejder med ruter, skal der defineres operationer for hver produktionsrute, du opretter.</span><span class="sxs-lookup"><span data-stu-id="141b2-139">If you're working with routes, operations must be defined for every production route that you set up.</span></span> <span data-ttu-id="141b2-140">Ruten repræsenterer den sti, varen følger fra operation til operation, lige fra starten af produktionsprocessen til slutningen.</span><span class="sxs-lookup"><span data-stu-id="141b2-140">The route represents the path that the item takes from operation to operation, from the start of the production process to the end.</span></span>

1.  <span data-ttu-id="141b2-141">**Omkostningskategorier** – Opret omkostningsarter for at definere omkostningerne for hver time i de angive processer og opsætningstider.</span><span class="sxs-lookup"><span data-stu-id="141b2-141">**Cost categories** – Set up cost categories to define the cost per hour of specified processes and setup times.</span></span>
2.  <span data-ttu-id="141b2-142">**Kostprisgrupper** – Definer omkostningsgrupper for at oprette og vedligeholde forskellige typer af efterkalkulationer.</span><span class="sxs-lookup"><span data-stu-id="141b2-142">**Cost groups** – Set up cost groups to create and maintain different types of costing.</span></span>
3.  <span data-ttu-id="141b2-143">**Rutegrupper** – Opret rutegrupper for at definere parametre, der er relateret til rutegrupper.</span><span class="sxs-lookup"><span data-stu-id="141b2-143">**Route groups** – Set up route groups to define parameters that are related to groups of routes.</span></span> <span data-ttu-id="141b2-144">Du skal oprette rutegrupper, før du kan oprette produktionsruter.</span><span class="sxs-lookup"><span data-stu-id="141b2-144">You must set up route groups before you can create production routes.</span></span>
4.  <span data-ttu-id="141b2-145">**Ruter** – Opret produktionsruter, og definer standardindstillinger for at styre planlægning, efterkalkulation og prissætning af ruteoperationer og for at køre rapportering.</span><span class="sxs-lookup"><span data-stu-id="141b2-145">**Routes** – Set up production routes, and define default settings to control scheduling, costing, and pricing of route operations, and to control progress reporting.</span></span>
5.  <span data-ttu-id="141b2-146">**Ruter** – Opret ruteversioner for at muliggøre varevariationer i produktionen.</span><span class="sxs-lookup"><span data-stu-id="141b2-146">**Routes** – Set up route versions to enable item variations in production.</span></span>

## <a name="optional-advanced-settings"></a><span data-ttu-id="141b2-147">Valgfrie avancerede indstillinger</span><span class="sxs-lookup"><span data-stu-id="141b2-147">Optional advanced settings</span></span>
1.  <span data-ttu-id="141b2-148">**Produktionsgrupper** – Opret produktionsgrupper for at angive relationer mellem produktionsordren og finanskontiene.</span><span class="sxs-lookup"><span data-stu-id="141b2-148">**Production groups** – Set up production groups to establish relationships between the production order and ledger accounts.</span></span> <span data-ttu-id="141b2-149">Finanskontiene bruges til at bogføre eller gruppere ordrer til rapportering.</span><span class="sxs-lookup"><span data-stu-id="141b2-149">The ledger accounts are used to post or group orders for reporting.</span></span>
2.  <span data-ttu-id="141b2-150">**Produktionspuljer** – Opret produktionspuljer for at gruppere produktionsordrer til behandling af presserende produktionsordrer og for at slette og bogføre grupper af ordrer.</span><span class="sxs-lookup"><span data-stu-id="141b2-150">**Production pools** – Create production pools to group production orders so that you can process urgent production orders, or delete and post groups of orders.</span></span>
3.  <span data-ttu-id="141b2-151">**Egenskaber** – Definer egenskaber til at oprette specielle attributter, som du kan tildele ressourcer for at styre produktionsrækkefølgen.</span><span class="sxs-lookup"><span data-stu-id="141b2-151">**Properties** – Define properties to create special attributes that you can assign to your resources to control the order of productions.</span></span> <span data-ttu-id="141b2-152">Disse attributter er forbundet til arbejdstidsskabelonen.</span><span class="sxs-lookup"><span data-stu-id="141b2-152">These attributes are connected to the working time template.</span></span>




