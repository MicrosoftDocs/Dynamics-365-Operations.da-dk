---
title: Serviceobjektgrupper
description: Objektgrupper kan bruges til at sortere og filtrere data om objekter til rapporter og statistikker.
author: YuyuScheller
manager: AnnBe
ms.date: 05/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectGroups
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
ms.openlocfilehash: 2ab3ed8a8f36f980473b17b5dfed8cb3d0054253
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="service-object-groups"></a><span data-ttu-id="45921-103">Serviceobjektgrupper</span><span class="sxs-lookup"><span data-stu-id="45921-103">Service object groups</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45921-104">Objektgrupper kan bruges til at sortere og filtrere data om objekter til rapporter og statistikker.</span><span class="sxs-lookup"><span data-stu-id="45921-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="45921-105">Du kan f.eks. gruppere objekter efter geografisk placering eller type.</span><span class="sxs-lookup"><span data-stu-id="45921-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="45921-106">Gruppere efter geografisk placering</span><span class="sxs-lookup"><span data-stu-id="45921-106">Group by geographical location</span></span>

<span data-ttu-id="45921-107">Du kan bruge denne grupperingsmetode til at vise, hvor de forskellige objekter, som dit firma servicerer, er beliggende.</span><span class="sxs-lookup"><span data-stu-id="45921-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="45921-108">Gruppering af objekter efter geografisk placering kan også være nyttigt, hvis du f.eks. har brug for at identificere objekter, som dit firma allerede leverer service til i et bestemt land eller område.</span><span class="sxs-lookup"><span data-stu-id="45921-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="45921-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="45921-109">Example</span></span>

<span data-ttu-id="45921-110">En kunde fra Belgien kontakter dit servicecenter og ønsker at indgå en serviceaftale vedrørende et objekt, ABC.</span><span class="sxs-lookup"><span data-stu-id="45921-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="45921-111">Du har knyttet en objektgruppe for geografisk placering, Belgien, til alle objekter, der serviceres i Belgien.</span><span class="sxs-lookup"><span data-stu-id="45921-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="45921-112">Ved at bruge denne gruppe som filter kan du hurtigt finde ud af, om ABC allerede findes som en post i programmet, eller du skal definere et nyt objekt.</span><span class="sxs-lookup"><span data-stu-id="45921-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="45921-113">Gruppere efter type</span><span class="sxs-lookup"><span data-stu-id="45921-113">Group by type</span></span>

<span data-ttu-id="45921-114">Du kan bruge denne grupperingsmetode til at vise de typer af objekter, som dit firma servicerer.</span><span class="sxs-lookup"><span data-stu-id="45921-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="45921-115">Gruppering af objekter efter type kan også være nyttigt, hvis du f.eks. vil oprette et nyt objekt ud fra lignende eksisterende objekter i programmet.</span><span class="sxs-lookup"><span data-stu-id="45921-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="45921-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="45921-116">Example</span></span>

<span data-ttu-id="45921-117">En kunde ringer for at indgå en serviceaftale vedrørende et klimaanlæg, HIJ.</span><span class="sxs-lookup"><span data-stu-id="45921-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="45921-118">Du har ikke i forvejen nogen post til dette anlæg.</span><span class="sxs-lookup"><span data-stu-id="45921-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="45921-119">Du har derimod oprettet en objektgruppe med navnet Klimaanlæg, og du har knyttet denne gruppe til alle klimaanlægsobjekter.</span><span class="sxs-lookup"><span data-stu-id="45921-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="45921-120">Derfor kan du hurtigt søge efter og identificere alle andre klimaanlæg og bruge skabelonoplysningerne fra disse objekter som grundlag for serviceaftalelinjerne til HIJ.</span><span class="sxs-lookup"><span data-stu-id="45921-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="45921-121">Ved at bruge objektgrupper på denne måde sparer du tid, når du skal oprette nye objekter og finde ud af, hvilke serviceopgaver der skal udføres på dem.</span><span class="sxs-lookup"><span data-stu-id="45921-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 

## <a name="create-service-object-groups"></a><span data-ttu-id="45921-122">Oprette serviceobjektgrupper</span><span class="sxs-lookup"><span data-stu-id="45921-122">Create service object groups</span></span>

<span data-ttu-id="45921-123">Opret grupper, som du kan tildele serviceobjekter til.</span><span class="sxs-lookup"><span data-stu-id="45921-123">Create groups that you can assign service objects to.</span></span> <span data-ttu-id="45921-124">Serviceobjekter er lagervarer og andre produkter, der udføres serviceydelser for.</span><span class="sxs-lookup"><span data-stu-id="45921-124">Service objects are inventory items and other products for which services are performed.</span></span> <span data-ttu-id="45921-125">Ved at gruppere serviceobjekter kan du oprette rapporter for lignende og relaterede serviceobjekter.</span><span class="sxs-lookup"><span data-stu-id="45921-125">By grouping service objects, you can create reports for similar and related service objects.</span></span> <span data-ttu-id="45921-126">For eksempel kan en serviceobjektgruppe bestå af to serviceobjekter: ét serviceobjekt er en pakke, og det andet serviceobjekt er tjenesten, der skal installere pakken.</span><span class="sxs-lookup"><span data-stu-id="45921-126">For example, a service object group might consist of two service objects: One service object is a kit, and the second service object is the service to install the kit.</span></span>

<span data-ttu-id="45921-127">Hvis du vil oprette serviceobjektgrupper, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="45921-127">To create service object groups, follow these steps:</span></span>

1. <span data-ttu-id="45921-128">Klik på **Servicestyring > Opsætning > Serviceobjekter > Serviceobjektgrupper**.</span><span class="sxs-lookup"><span data-stu-id="45921-128">Click **Service management > Setup > Service objects > Service object groups**.</span></span>

2. <span data-ttu-id="45921-129">Klik på **Ny** for at oprette en ny serviceobjektgruppe.</span><span class="sxs-lookup"><span data-stu-id="45921-129">Click **New** to create a new service object group.</span></span>

3. <span data-ttu-id="45921-130">Angiv et entydigt navn for serviceobjektgruppen og evt. en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="45921-130">Enter a unique name for the service object group and, optionally, a description.</span></span>

<span data-ttu-id="45921-131">Du kan tildele serviceobjekter til gruppen ved hjælp af formularen **Serviceobjekter**.</span><span class="sxs-lookup"><span data-stu-id="45921-131">You can assign service objects to the group by using the **Service objects** form.</span></span> 

## <a name="see-also"></a><span data-ttu-id="45921-132">Se også</span><span class="sxs-lookup"><span data-stu-id="45921-132">See also</span></span>

[<span data-ttu-id="45921-133">Oprette serviceobjekter</span><span class="sxs-lookup"><span data-stu-id="45921-133">Create service objects</span></span>](create-service-objects.md)


