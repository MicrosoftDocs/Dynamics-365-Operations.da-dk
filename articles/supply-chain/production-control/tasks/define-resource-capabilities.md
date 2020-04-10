---
title: Definere ressourceegenskaber
description: Ressourceegenskaber beskriver, hvad operationsressourcer kan gøre.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6bd3f2b1efc1e6a883ad2a25d127e74a8925de8f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146784"
---
# <a name="define-resource-capabilities"></a><span data-ttu-id="9ae23-103">Definere ressourceegenskaber</span><span class="sxs-lookup"><span data-stu-id="9ae23-103">Define resource capabilities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9ae23-104">Ressourceegenskaber beskriver, hvad operationsressourcer kan gøre.</span><span class="sxs-lookup"><span data-stu-id="9ae23-104">Resource capabilities describe what operations resources can do.</span></span> <span data-ttu-id="9ae23-105">Under planlægningen sammenlignes krav i hvert enkelt job og handling med egenskaberne hos de tilgængelige ressourcer.</span><span class="sxs-lookup"><span data-stu-id="9ae23-105">During scheduling, the requirements of each job and operation are matched against the capabilities of the available resources.</span></span> <span data-ttu-id="9ae23-106">Denne opgaveguide hjælper dig med at oprette en ressourceegenskab og tildele den til en ressource.</span><span class="sxs-lookup"><span data-stu-id="9ae23-106">This task guide will help you create a resource capability and assign it to a resource.</span></span> <span data-ttu-id="9ae23-107">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="9ae23-107">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-resource-capability"></a><span data-ttu-id="9ae23-108">Opret en ny ressourceegenskab.</span><span class="sxs-lookup"><span data-stu-id="9ae23-108">Create a resource capability</span></span>
1. <span data-ttu-id="9ae23-109">Gå til Ressourceegenskaber.</span><span class="sxs-lookup"><span data-stu-id="9ae23-109">Go to Resource capabilities.</span></span>
2. <span data-ttu-id="9ae23-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="9ae23-110">Click New.</span></span>
3. <span data-ttu-id="9ae23-111">Skriv id'et for ressourcens egenskab i feltet Egenskab.</span><span class="sxs-lookup"><span data-stu-id="9ae23-111">In the Capability field, type the ID of the resource capability.</span></span>
    * <span data-ttu-id="9ae23-112">For en given operation kan du bruge egenskabs-id'et til at angive, at ressourcerne skal have denne egenskab for at udføre handlingen.</span><span class="sxs-lookup"><span data-stu-id="9ae23-112">For a given operation, you use the capability ID to specify that resources must have this capability to perform the operation.</span></span>  
4. <span data-ttu-id="9ae23-113">Skriv en beskrivelse af egenskaben i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="9ae23-113">In the Description field, enter a description of the capability.</span></span>

## <a name="assign-capability-to-a-resource"></a><span data-ttu-id="9ae23-114">Tildel egenskab til en ressource</span><span class="sxs-lookup"><span data-stu-id="9ae23-114">Assign capability to a resource</span></span>
1. <span data-ttu-id="9ae23-115">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="9ae23-115">Click Add.</span></span>
2. <span data-ttu-id="9ae23-116">Skriv id'et for ressourcen i feltet Ressource.</span><span class="sxs-lookup"><span data-stu-id="9ae23-116">In the Resource field, type the ID of the resource.</span></span>
    * <span data-ttu-id="9ae23-117">En ressourceegenskab kan tildeles til en eller flere ressourcer.</span><span class="sxs-lookup"><span data-stu-id="9ae23-117">A resource capability can be assigned to one or more resources.</span></span>  
3. <span data-ttu-id="9ae23-118">Angiv en dato i feltet Udløb.</span><span class="sxs-lookup"><span data-stu-id="9ae23-118">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="9ae23-119">Du kan bruge dette felt til at angive, at en ressource kun har egenskaben i et begrænset tidsrum.</span><span class="sxs-lookup"><span data-stu-id="9ae23-119">You can use this field to specify that a resource has the capability for only a limited time.</span></span>  
4. <span data-ttu-id="9ae23-120">Angiv et tal i feltet Prioritet.</span><span class="sxs-lookup"><span data-stu-id="9ae23-120">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="9ae23-121">Når du planlægger opgaver og operationer, kan du angive, om du vil vælge ressourcer efter prioritet.</span><span class="sxs-lookup"><span data-stu-id="9ae23-121">When you schedule jobs and operations, you can specify whether to select resources by priority.</span></span> <span data-ttu-id="9ae23-122">Hvis du vælger at gøre dette, og mere end én ressource kan udføre jobbet eller handlingen inden den ønskede dato, vælges ressourcen med den laveste prioritet med hensyn til den nødvendige egenskab.</span><span class="sxs-lookup"><span data-stu-id="9ae23-122">If you choose to do this, and more than one resource can perform the job or operation by the requested date, the resource that has the lowest priority with respect to the required capability is selected.</span></span>  
5. <span data-ttu-id="9ae23-123">Angiv et tal i feltet Niveau.</span><span class="sxs-lookup"><span data-stu-id="9ae23-123">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="9ae23-124">Når du angiver, at et job eller en handling kræver en bestemt egenskab, kan du også angive det krævede minimumsniveau.</span><span class="sxs-lookup"><span data-stu-id="9ae23-124">When you specify that a job or operation requires a particular capability, you can also specify the minimum level that is required.</span></span> <span data-ttu-id="9ae23-125">Brug egenskabsniveauet til at skelne mellem ressourcer, der kan udføre det samme job, men ved forskellige hastigheder, styrke, omfang og så videre.</span><span class="sxs-lookup"><span data-stu-id="9ae23-125">Use the capability level to differentiate resources that can perform the same job, but at different speeds, strengths, sizes, and so on.</span></span>  

