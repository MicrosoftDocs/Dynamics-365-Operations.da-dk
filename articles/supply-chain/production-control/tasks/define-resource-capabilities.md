---
title: Definere ressourceegenskaber
description: Ressourceegenskaber beskriver, hvad operationsressourcer kan gøre.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 072991e7b3844ad3583b7d0c575d426299f74e9f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828700"
---
# <a name="define-resource-capabilities"></a><span data-ttu-id="72952-103">Definere ressourceegenskaber</span><span class="sxs-lookup"><span data-stu-id="72952-103">Define resource capabilities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="72952-104">Ressourceegenskaber beskriver, hvad operationsressourcer kan gøre.</span><span class="sxs-lookup"><span data-stu-id="72952-104">Resource capabilities describe what operations resources can do.</span></span> <span data-ttu-id="72952-105">Under planlægningen sammenlignes krav i hvert enkelt job og handling med egenskaberne hos de tilgængelige ressourcer.</span><span class="sxs-lookup"><span data-stu-id="72952-105">During scheduling, the requirements of each job and operation are matched against the capabilities of the available resources.</span></span> <span data-ttu-id="72952-106">Denne opgaveguide hjælper dig med at oprette en ressourceegenskab og tildele den til en ressource.</span><span class="sxs-lookup"><span data-stu-id="72952-106">This task guide will help you create a resource capability and assign it to a resource.</span></span> <span data-ttu-id="72952-107">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="72952-107">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-resource-capability"></a><span data-ttu-id="72952-108">Opret en ny ressourceegenskab.</span><span class="sxs-lookup"><span data-stu-id="72952-108">Create a resource capability</span></span>
1. <span data-ttu-id="72952-109">Gå til Ressourceegenskaber.</span><span class="sxs-lookup"><span data-stu-id="72952-109">Go to Resource capabilities.</span></span>
2. <span data-ttu-id="72952-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="72952-110">Click New.</span></span>
3. <span data-ttu-id="72952-111">Skriv id'et for ressourcens egenskab i feltet Egenskab.</span><span class="sxs-lookup"><span data-stu-id="72952-111">In the Capability field, type the ID of the resource capability.</span></span>
    * <span data-ttu-id="72952-112">For en given operation kan du bruge egenskabs-id'et til at angive, at ressourcerne skal have denne egenskab for at udføre handlingen.</span><span class="sxs-lookup"><span data-stu-id="72952-112">For a given operation, you use the capability ID to specify that resources must have this capability to perform the operation.</span></span>  
4. <span data-ttu-id="72952-113">Skriv en beskrivelse af egenskaben i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="72952-113">In the Description field, enter a description of the capability.</span></span>

## <a name="assign-capability-to-a-resource"></a><span data-ttu-id="72952-114">Tildel egenskab til en ressource</span><span class="sxs-lookup"><span data-stu-id="72952-114">Assign capability to a resource</span></span>
1. <span data-ttu-id="72952-115">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="72952-115">Click Add.</span></span>
2. <span data-ttu-id="72952-116">Skriv id'et for ressourcen i feltet Ressource.</span><span class="sxs-lookup"><span data-stu-id="72952-116">In the Resource field, type the ID of the resource.</span></span>
    * <span data-ttu-id="72952-117">En ressourceegenskab kan tildeles til en eller flere ressourcer.</span><span class="sxs-lookup"><span data-stu-id="72952-117">A resource capability can be assigned to one or more resources.</span></span>  
3. <span data-ttu-id="72952-118">Angiv en dato i feltet Udløb.</span><span class="sxs-lookup"><span data-stu-id="72952-118">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="72952-119">Du kan bruge dette felt til at angive, at en ressource kun har egenskaben i et begrænset tidsrum.</span><span class="sxs-lookup"><span data-stu-id="72952-119">You can use this field to specify that a resource has the capability for only a limited time.</span></span>  
4. <span data-ttu-id="72952-120">Angiv et tal i feltet Prioritet.</span><span class="sxs-lookup"><span data-stu-id="72952-120">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="72952-121">Når du planlægger opgaver og operationer, kan du angive, om du vil vælge ressourcer efter prioritet.</span><span class="sxs-lookup"><span data-stu-id="72952-121">When you schedule jobs and operations, you can specify whether to select resources by priority.</span></span> <span data-ttu-id="72952-122">Hvis du vælger at gøre dette, og mere end én ressource kan udføre jobbet eller handlingen inden den ønskede dato, vælges ressourcen med den laveste prioritet med hensyn til den nødvendige egenskab.</span><span class="sxs-lookup"><span data-stu-id="72952-122">If you choose to do this, and more than one resource can perform the job or operation by the requested date, the resource that has the lowest priority with respect to the required capability is selected.</span></span>  
5. <span data-ttu-id="72952-123">Angiv et tal i feltet Niveau.</span><span class="sxs-lookup"><span data-stu-id="72952-123">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="72952-124">Når du angiver, at et job eller en handling kræver en bestemt egenskab, kan du også angive det krævede minimumsniveau.</span><span class="sxs-lookup"><span data-stu-id="72952-124">When you specify that a job or operation requires a particular capability, you can also specify the minimum level that is required.</span></span> <span data-ttu-id="72952-125">Brug egenskabsniveauet til at skelne mellem ressourcer, der kan udføre det samme job, men ved forskellige hastigheder, styrke, omfang og så videre.</span><span class="sxs-lookup"><span data-stu-id="72952-125">Use the capability level to differentiate resources that can perform the same job, but at different speeds, strengths, sizes, and so on.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]