--- 
title: Definere ressourcegruppe for diskret produktion
description: "En ressourcegruppe er et sæt operationsressourcer, der normalt svarer til den fysiske organisation af arbejdsceller, som defineret af gule streger på produktionen."
author: sorenva
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e1be950a7d1d7548aced041a189222b472d767cf
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="f90cf-103">Definere ressourcegruppe for diskret produktion</span><span class="sxs-lookup"><span data-stu-id="f90cf-103">Define discrete manufacturing resource group</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f90cf-104">En ressourcegruppe er et sæt operationsressourcer, der normalt svarer til den fysiske organisation af arbejdsceller, som defineret af gule streger på produktionen.</span><span class="sxs-lookup"><span data-stu-id="f90cf-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="f90cf-105">Denne fremgangsmåde viser, hvordan du definerer en ressourcegruppe til brug i separat produktion.</span><span class="sxs-lookup"><span data-stu-id="f90cf-105">This procedure shows you how to define a resource group for use in discrete production.</span></span> <span data-ttu-id="f90cf-106">Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="f90cf-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="f90cf-107">Gå til Ressourcegrupper.</span><span class="sxs-lookup"><span data-stu-id="f90cf-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="f90cf-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f90cf-108">Click New.</span></span>
3. <span data-ttu-id="f90cf-109">Indtast en værdi i feltet Ressourcegruppe.</span><span class="sxs-lookup"><span data-stu-id="f90cf-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="f90cf-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f90cf-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f90cf-111">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="f90cf-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="f90cf-112">Indtast eller vælg en værdi i feltet Produktionsenhed.</span><span class="sxs-lookup"><span data-stu-id="f90cf-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="f90cf-113">Definer standardoperationsparametre</span><span class="sxs-lookup"><span data-stu-id="f90cf-113">Define default operational parameters</span></span>
1. <span data-ttu-id="f90cf-114">Udvid sektionen Handling.</span><span class="sxs-lookup"><span data-stu-id="f90cf-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="f90cf-115">Angiv et tal i feltet Spildprocent.</span><span class="sxs-lookup"><span data-stu-id="f90cf-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="f90cf-116">Indtast eller vælg en værdi i feltet Opstillingsart.</span><span class="sxs-lookup"><span data-stu-id="f90cf-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="f90cf-117">Indtast eller vælg en værdi i feltet procestidsart.</span><span class="sxs-lookup"><span data-stu-id="f90cf-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="f90cf-118">Angiv et tal i feltet Grovplanlægningsprocent.</span><span class="sxs-lookup"><span data-stu-id="f90cf-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="f90cf-119">Definer operationstimer</span><span class="sxs-lookup"><span data-stu-id="f90cf-119">Define operating hours</span></span>
1. <span data-ttu-id="f90cf-120">Udvid sektionen Kalendere.</span><span class="sxs-lookup"><span data-stu-id="f90cf-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="f90cf-121">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f90cf-121">Click Add.</span></span>
3. <span data-ttu-id="f90cf-122">Indtast eller vælg en værdi i feltet Kalender.</span><span class="sxs-lookup"><span data-stu-id="f90cf-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="f90cf-123">Tilføj operationsressourcer</span><span class="sxs-lookup"><span data-stu-id="f90cf-123">Add operations resources</span></span>
1. <span data-ttu-id="f90cf-124">Udvid sektionen Ressourcer.</span><span class="sxs-lookup"><span data-stu-id="f90cf-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="f90cf-125">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f90cf-125">Click Add.</span></span>
3. <span data-ttu-id="f90cf-126">Indtast eller vælg en værdi i feltet Ressource.</span><span class="sxs-lookup"><span data-stu-id="f90cf-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="f90cf-127">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f90cf-127">Click Add.</span></span>
5. <span data-ttu-id="f90cf-128">Indtast eller vælg en værdi i feltet Ressource.</span><span class="sxs-lookup"><span data-stu-id="f90cf-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="f90cf-129">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f90cf-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f90cf-130">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f90cf-130">In the list, click the link in the selected row.</span></span>


