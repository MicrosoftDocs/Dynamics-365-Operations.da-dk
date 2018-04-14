--- 
title: Oprette en status for produktlivscyklus for at udelukke produkter fra varedisponering
description: "Denne fremgangsmåde viser, hvordan du opretter en ny status for produktlivscyklus, der udelukker produkterne fra varedisponering og styklisteniveauberegning."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 57b84e62b259e5dcbf68ee447b9627443d932476
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a><span data-ttu-id="937af-103">Oprette en status for produktlivscyklus for at udelukke produkter fra varedisponering</span><span class="sxs-lookup"><span data-stu-id="937af-103">Create a product lifecycle state to exclude products from Master planning</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="937af-104">Denne fremgangsmåde viser, hvordan du opretter en ny status for produktlivscyklus, der udelukker produkterne fra varedisponering og styklisteniveauberegning.</span><span class="sxs-lookup"><span data-stu-id="937af-104">This procedure shows how to create a new product lifecycle state that excludes the products from Master planning and BOM-level calculation.</span></span>


## <a name="create-an-obsolete-state"></a><span data-ttu-id="937af-105">Oprette en forældet tilstand</span><span class="sxs-lookup"><span data-stu-id="937af-105">Create an obsolete state</span></span>
1. <span data-ttu-id="937af-106">Gå til Administration af produktoplysninger > Konfiguration > Status for produktlivscyklus.</span><span class="sxs-lookup"><span data-stu-id="937af-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="937af-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="937af-107">Click New.</span></span>
3. <span data-ttu-id="937af-108">Skriv en værdi i feltet Status.</span><span class="sxs-lookup"><span data-stu-id="937af-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="937af-109">Vælg Nej i feltet Er aktiv for planlægning.</span><span class="sxs-lookup"><span data-stu-id="937af-109">Select No in the Is active for planning field.</span></span>
5. <span data-ttu-id="937af-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="937af-110">In the Description field, type a value.</span></span>

## <a name="associate-the-obsolete-state-to-a-released-product"></a><span data-ttu-id="937af-111">Knytte den forældede tilstand til en frigivet produkt</span><span class="sxs-lookup"><span data-stu-id="937af-111">Associate the obsolete state to a released product</span></span>
1. <span data-ttu-id="937af-112">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="937af-112">Close the page.</span></span>
2. <span data-ttu-id="937af-113">Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="937af-113">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="937af-114">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="937af-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="937af-115">Du kan for eksempel filtrere på feltet Søgenavn med værdien 'M00'.</span><span class="sxs-lookup"><span data-stu-id="937af-115">For example, filter on the Search name field with a value of 'M00'.</span></span>
4. <span data-ttu-id="937af-116">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="937af-116">Click Edit.</span></span>
5. <span data-ttu-id="937af-117">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="937af-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="937af-118">Indtast eller vælg en værdi i feltet Status for produktlivscyklus.</span><span class="sxs-lookup"><span data-stu-id="937af-118">In the Product lifecycle state field, enter or select a value.</span></span>


