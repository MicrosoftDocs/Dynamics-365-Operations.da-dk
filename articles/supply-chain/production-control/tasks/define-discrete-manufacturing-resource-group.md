---
title: Definere ressourcegruppe for diskret produktion
description: En ressourcegruppe er et sæt operationsressourcer, der normalt svarer til den fysiske organisation af arbejdsceller, som defineret af gule streger på produktionen.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95a8e1c6daa78250118a8a16010ef4cc1b1ae693
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811528"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="f108f-103">Definere ressourcegruppe for diskret produktion</span><span class="sxs-lookup"><span data-stu-id="f108f-103">Define discrete manufacturing resource group</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f108f-104">En ressourcegruppe er et sæt operationsressourcer, der normalt svarer til den fysiske organisation af arbejdsceller, som defineret af gule streger på produktionen.</span><span class="sxs-lookup"><span data-stu-id="f108f-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="f108f-105">Denne fremgangsmåde viser, hvordan du definerer en ressourcegruppe til brug i separat produktion.</span><span class="sxs-lookup"><span data-stu-id="f108f-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="f108f-106">Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="f108f-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="f108f-107">Gå til Ressourcegrupper.</span><span class="sxs-lookup"><span data-stu-id="f108f-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="f108f-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f108f-108">Click New.</span></span>
3. <span data-ttu-id="f108f-109">Indtast en værdi i feltet Ressourcegruppe.</span><span class="sxs-lookup"><span data-stu-id="f108f-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="f108f-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f108f-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f108f-111">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="f108f-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="f108f-112">Indtast eller vælg en værdi i feltet Produktionsenhed.</span><span class="sxs-lookup"><span data-stu-id="f108f-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="f108f-113">Definer standardoperationsparametre</span><span class="sxs-lookup"><span data-stu-id="f108f-113">Define default operational parameters</span></span>
1. <span data-ttu-id="f108f-114">Udvid sektionen Handling.</span><span class="sxs-lookup"><span data-stu-id="f108f-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="f108f-115">Angiv et tal i feltet Spildprocent.</span><span class="sxs-lookup"><span data-stu-id="f108f-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="f108f-116">Indtast eller vælg en værdi i feltet Opstillingsart.</span><span class="sxs-lookup"><span data-stu-id="f108f-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="f108f-117">Indtast eller vælg en værdi i feltet procestidsart.</span><span class="sxs-lookup"><span data-stu-id="f108f-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="f108f-118">Angiv et tal i feltet Grovplanlægningsprocent.</span><span class="sxs-lookup"><span data-stu-id="f108f-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="f108f-119">Definer operationstimer</span><span class="sxs-lookup"><span data-stu-id="f108f-119">Define operating hours</span></span>
1. <span data-ttu-id="f108f-120">Udvid sektionen Kalendere.</span><span class="sxs-lookup"><span data-stu-id="f108f-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="f108f-121">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f108f-121">Click Add.</span></span>
3. <span data-ttu-id="f108f-122">Indtast eller vælg en værdi i feltet Kalender.</span><span class="sxs-lookup"><span data-stu-id="f108f-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="f108f-123">Tilføj operationsressourcer</span><span class="sxs-lookup"><span data-stu-id="f108f-123">Add operations resources</span></span>
1. <span data-ttu-id="f108f-124">Udvid sektionen Ressourcer.</span><span class="sxs-lookup"><span data-stu-id="f108f-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="f108f-125">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f108f-125">Click Add.</span></span>
3. <span data-ttu-id="f108f-126">Indtast eller vælg en værdi i feltet Ressource.</span><span class="sxs-lookup"><span data-stu-id="f108f-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="f108f-127">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f108f-127">Click Add.</span></span>
5. <span data-ttu-id="f108f-128">Indtast eller vælg en værdi i feltet Ressource.</span><span class="sxs-lookup"><span data-stu-id="f108f-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="f108f-129">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f108f-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f108f-130">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f108f-130">In the list, click the link in the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]