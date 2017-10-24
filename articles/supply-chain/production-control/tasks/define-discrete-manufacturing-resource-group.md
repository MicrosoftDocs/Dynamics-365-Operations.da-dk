--- 
title: Definere ressourcegruppe for diskret produktion
description: "En ressourcegruppe er et sæt operationsressourcer, der normalt svarer til den fysiske organisation af arbejdsceller, som defineret af gule streger på produktionen."
author: sorenva
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c2423fe91d1531a326080e3a584195ea864f2e3e
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="700d3-103">Definere ressourcegruppe for diskret produktion</span><span class="sxs-lookup"><span data-stu-id="700d3-103">Define discrete manufacturing resource group</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="700d3-104">En ressourcegruppe er et sæt operationsressourcer, der normalt svarer til den fysiske organisation af arbejdsceller, som defineret af gule streger på produktionen.</span><span class="sxs-lookup"><span data-stu-id="700d3-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="700d3-105">Denne fremgangsmåde viser, hvordan du definerer en ressourcegruppe til brug i separat produktion.</span><span class="sxs-lookup"><span data-stu-id="700d3-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="700d3-106">Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="700d3-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="700d3-107">Gå til Ressourcegrupper.</span><span class="sxs-lookup"><span data-stu-id="700d3-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="700d3-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="700d3-108">Click New.</span></span>
3. <span data-ttu-id="700d3-109">Indtast en værdi i feltet Ressourcegruppe.</span><span class="sxs-lookup"><span data-stu-id="700d3-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="700d3-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="700d3-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="700d3-111">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="700d3-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="700d3-112">Indtast eller vælg en værdi i feltet Produktionsenhed.</span><span class="sxs-lookup"><span data-stu-id="700d3-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="700d3-113">Definer standardoperationsparametre</span><span class="sxs-lookup"><span data-stu-id="700d3-113">Define default operational parameters</span></span>
1. <span data-ttu-id="700d3-114">Udvid sektionen Handling.</span><span class="sxs-lookup"><span data-stu-id="700d3-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="700d3-115">Angiv et tal i feltet Spildprocent.</span><span class="sxs-lookup"><span data-stu-id="700d3-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="700d3-116">Indtast eller vælg en værdi i feltet Opstillingsart.</span><span class="sxs-lookup"><span data-stu-id="700d3-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="700d3-117">Indtast eller vælg en værdi i feltet procestidsart.</span><span class="sxs-lookup"><span data-stu-id="700d3-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="700d3-118">Angiv et tal i feltet Grovplanlægningsprocent.</span><span class="sxs-lookup"><span data-stu-id="700d3-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="700d3-119">Definer operationstimer</span><span class="sxs-lookup"><span data-stu-id="700d3-119">Define operating hours</span></span>
1. <span data-ttu-id="700d3-120">Udvid sektionen Kalendere.</span><span class="sxs-lookup"><span data-stu-id="700d3-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="700d3-121">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="700d3-121">Click Add.</span></span>
3. <span data-ttu-id="700d3-122">Indtast eller vælg en værdi i feltet Kalender.</span><span class="sxs-lookup"><span data-stu-id="700d3-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="700d3-123">Tilføj operationsressourcer</span><span class="sxs-lookup"><span data-stu-id="700d3-123">Add operations resources</span></span>
1. <span data-ttu-id="700d3-124">Udvid sektionen Ressourcer.</span><span class="sxs-lookup"><span data-stu-id="700d3-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="700d3-125">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="700d3-125">Click Add.</span></span>
3. <span data-ttu-id="700d3-126">Indtast eller vælg en værdi i feltet Ressource.</span><span class="sxs-lookup"><span data-stu-id="700d3-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="700d3-127">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="700d3-127">Click Add.</span></span>
5. <span data-ttu-id="700d3-128">Indtast eller vælg en værdi i feltet Ressource.</span><span class="sxs-lookup"><span data-stu-id="700d3-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="700d3-129">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="700d3-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="700d3-130">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="700d3-130">In the list, click the link in the selected row.</span></span>


