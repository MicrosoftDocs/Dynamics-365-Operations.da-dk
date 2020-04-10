---
title: Oprette en ny kanban-regel ved at duplikere en eksisterende kanban-regel
description: Denne procedure fokuserer på oprettelse en dublet af en eksisterende kanban-regel.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bc65dd80221cedd25890037afcb3d2617f22793
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149181"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="5a74f-103">Oprette en ny kanban-regel ved at duplikere en eksisterende kanban-regel</span><span class="sxs-lookup"><span data-stu-id="5a74f-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5a74f-104">Denne procedure fokuserer på oprettelse en dublet af en eksisterende kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="5a74f-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="5a74f-105">Dette er nyttigt, hvis du vil oprette nye kanban-regler baseret på eksisterende kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="5a74f-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="5a74f-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="5a74f-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5a74f-107">Denne procedure er beregnet til procesingeniøren eller værdistrømlederen, når de forbereder produktionen til et nyt produktionsflow eller en ny genopfyldningsregel.</span><span class="sxs-lookup"><span data-stu-id="5a74f-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="5a74f-108">Vælg en kanban-regel</span><span class="sxs-lookup"><span data-stu-id="5a74f-108">Select a kanban rule</span></span>
1. <span data-ttu-id="5a74f-109">Gå til kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="5a74f-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="5a74f-110">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="5a74f-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5a74f-111">Vælg kanban-regel 000017 for Produkt M0006.</span><span class="sxs-lookup"><span data-stu-id="5a74f-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="5a74f-112">Dupliker en kanban-regel</span><span class="sxs-lookup"><span data-stu-id="5a74f-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="5a74f-113">Klik på Dupliker kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="5a74f-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="5a74f-114">Når du kopierer en kanban-regel, er det muligt at ændre type, datoer, aktiviteter og produktvalg.</span><span class="sxs-lookup"><span data-stu-id="5a74f-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="5a74f-115">Skift produktet for denne procedure i næste trin.</span><span class="sxs-lookup"><span data-stu-id="5a74f-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="5a74f-116">Indtast eller vælg en værdi i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="5a74f-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="5a74f-117">Vælg M0007.</span><span class="sxs-lookup"><span data-stu-id="5a74f-117">Select M0007.</span></span>  
3. <span data-ttu-id="5a74f-118">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5a74f-118">Click OK.</span></span>
    * <span data-ttu-id="5a74f-119">Bemærk, at der oprettes en dublet af kanban-regel 000017.</span><span class="sxs-lookup"><span data-stu-id="5a74f-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    

