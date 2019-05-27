---
title: Oprette en postskabelon for at lette dataindtastning
description: Denne fremgangsmåde viser, hvordan du opretter en postskabelon, så feltværdier, som bruges ofte, ikke behøver at angives eksplicit for hver ny post.
author: margoc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 36d14c386322adab0cc0ba9b7b47c874aefbe519
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544246"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="d7abf-103">Oprette en postskabelon for at lette dataindtastning</span><span class="sxs-lookup"><span data-stu-id="d7abf-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d7abf-104">Denne fremgangsmåde viser, hvordan du opretter en postskabelon, så feltværdier, som bruges ofte, ikke behøver at angives eksplicit for hver ny post.</span><span class="sxs-lookup"><span data-stu-id="d7abf-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="d7abf-105">I denne procedure skal oprette en ny post til nye bærbare computere, der skal føjes til dine anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="d7abf-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="d7abf-106">Denne procedure bruger eksempelfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="d7abf-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="d7abf-107">Gå til Anlægsaktiver > Anlægsaktiver > Anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="d7abf-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="d7abf-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d7abf-108">Click New.</span></span>
3. <span data-ttu-id="d7abf-109">Skriv eller vælg en værdi i feltet Anlægsaktivgruppe.</span><span class="sxs-lookup"><span data-stu-id="d7abf-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="d7abf-110">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d7abf-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d7abf-111">Angiv f.eks. "Bærbar for potentiel kunde".</span><span class="sxs-lookup"><span data-stu-id="d7abf-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="d7abf-112">Angiv en værdi i feltet Søgenavn.</span><span class="sxs-lookup"><span data-stu-id="d7abf-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="d7abf-113">Du kan f.eks. skrive "bærbar".</span><span class="sxs-lookup"><span data-stu-id="d7abf-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="d7abf-114">Udvid sektionen Tekniske oplysninger.</span><span class="sxs-lookup"><span data-stu-id="d7abf-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="d7abf-115">Skriv en værdi i feltet Mærke.</span><span class="sxs-lookup"><span data-stu-id="d7abf-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="d7abf-116">Skriv en værdi i feltet Model.</span><span class="sxs-lookup"><span data-stu-id="d7abf-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="d7abf-117">Skriv en værdi i feltet Modelår.</span><span class="sxs-lookup"><span data-stu-id="d7abf-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="d7abf-118">Klik på Indstillinger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d7abf-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="d7abf-119">Klik på Postoplysninger.</span><span class="sxs-lookup"><span data-stu-id="d7abf-119">Click Record info.</span></span>
12. <span data-ttu-id="d7abf-120">Klik på Brugerskabelon.</span><span class="sxs-lookup"><span data-stu-id="d7abf-120">Click User template.</span></span>
13. <span data-ttu-id="d7abf-121">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d7abf-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d7abf-122">Du kan f.eks. skrive "Bærbar firmacomputer".</span><span class="sxs-lookup"><span data-stu-id="d7abf-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="d7abf-123">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d7abf-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="d7abf-124">Du kan f.eks. skrive "Bærbar firmacomputer".</span><span class="sxs-lookup"><span data-stu-id="d7abf-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="d7abf-125">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d7abf-125">Click OK.</span></span>
16. <span data-ttu-id="d7abf-126">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="d7abf-126">Click Close.</span></span>

