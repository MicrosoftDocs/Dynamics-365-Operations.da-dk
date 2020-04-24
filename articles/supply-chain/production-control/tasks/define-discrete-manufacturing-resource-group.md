---
title: Definere ressourcegruppe for diskret produktion
description: En ressourcegruppe er et sæt operationsressourcer, der normalt svarer til den fysiske organisation af arbejdsceller, som defineret af gule streger på produktionen.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eaccb566c04d6d4b91ea8cb046931e750a4c6eed
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210680"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="6251e-103">Definere ressourcegruppe for diskret produktion</span><span class="sxs-lookup"><span data-stu-id="6251e-103">Define discrete manufacturing resource group</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6251e-104">En ressourcegruppe er et sæt operationsressourcer, der normalt svarer til den fysiske organisation af arbejdsceller, som defineret af gule streger på produktionen.</span><span class="sxs-lookup"><span data-stu-id="6251e-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="6251e-105">Denne fremgangsmåde viser, hvordan du definerer en ressourcegruppe til brug i separat produktion.</span><span class="sxs-lookup"><span data-stu-id="6251e-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="6251e-106">Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="6251e-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="6251e-107">Gå til Ressourcegrupper.</span><span class="sxs-lookup"><span data-stu-id="6251e-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="6251e-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6251e-108">Click New.</span></span>
3. <span data-ttu-id="6251e-109">Indtast en værdi i feltet Ressourcegruppe.</span><span class="sxs-lookup"><span data-stu-id="6251e-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="6251e-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="6251e-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6251e-111">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="6251e-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="6251e-112">Indtast eller vælg en værdi i feltet Produktionsenhed.</span><span class="sxs-lookup"><span data-stu-id="6251e-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="6251e-113">Definer standardoperationsparametre</span><span class="sxs-lookup"><span data-stu-id="6251e-113">Define default operational parameters</span></span>
1. <span data-ttu-id="6251e-114">Udvid sektionen Handling.</span><span class="sxs-lookup"><span data-stu-id="6251e-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="6251e-115">Angiv et tal i feltet Spildprocent.</span><span class="sxs-lookup"><span data-stu-id="6251e-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="6251e-116">Indtast eller vælg en værdi i feltet Opstillingsart.</span><span class="sxs-lookup"><span data-stu-id="6251e-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="6251e-117">Indtast eller vælg en værdi i feltet procestidsart.</span><span class="sxs-lookup"><span data-stu-id="6251e-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="6251e-118">Angiv et tal i feltet Grovplanlægningsprocent.</span><span class="sxs-lookup"><span data-stu-id="6251e-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="6251e-119">Definer operationstimer</span><span class="sxs-lookup"><span data-stu-id="6251e-119">Define operating hours</span></span>
1. <span data-ttu-id="6251e-120">Udvid sektionen Kalendere.</span><span class="sxs-lookup"><span data-stu-id="6251e-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="6251e-121">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="6251e-121">Click Add.</span></span>
3. <span data-ttu-id="6251e-122">Indtast eller vælg en værdi i feltet Kalender.</span><span class="sxs-lookup"><span data-stu-id="6251e-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="6251e-123">Tilføj operationsressourcer</span><span class="sxs-lookup"><span data-stu-id="6251e-123">Add operations resources</span></span>
1. <span data-ttu-id="6251e-124">Udvid sektionen Ressourcer.</span><span class="sxs-lookup"><span data-stu-id="6251e-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="6251e-125">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="6251e-125">Click Add.</span></span>
3. <span data-ttu-id="6251e-126">Indtast eller vælg en værdi i feltet Ressource.</span><span class="sxs-lookup"><span data-stu-id="6251e-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="6251e-127">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="6251e-127">Click Add.</span></span>
5. <span data-ttu-id="6251e-128">Indtast eller vælg en værdi i feltet Ressource.</span><span class="sxs-lookup"><span data-stu-id="6251e-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="6251e-129">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6251e-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="6251e-130">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6251e-130">In the list, click the link in the selected row.</span></span>

