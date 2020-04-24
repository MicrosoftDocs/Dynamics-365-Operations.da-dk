---
title: Opret en standardstatus for produktlivscyklus
description: Denne fremgangsmåde viser, hvordan du opretter en standardstatus for produktlivscyklus, samt hvordan standardstatussen tilknyttes frigivne produkter.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd346f338a14476960ab47db2e3013402f4c43af
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213164"
---
# <a name="create-a-default-product-lifecycle-state"></a><span data-ttu-id="3b86a-103">Opret en standardstatus for produktlivscyklus</span><span class="sxs-lookup"><span data-stu-id="3b86a-103">Create a default product lifecycle state</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3b86a-104">Denne fremgangsmåde viser, hvordan du opretter en standardstatus for produktlivscyklus, samt hvordan standardstatussen tilknyttes frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="3b86a-104">This procedure shows how to create a default product lifecycle state as well as how to associate the default state with released products.</span></span>


## <a name="create-a-default-lifecycle-state"></a><span data-ttu-id="3b86a-105">Opret en standardstatus for livscyklus</span><span class="sxs-lookup"><span data-stu-id="3b86a-105">Create a default lifecycle state</span></span>
1. <span data-ttu-id="3b86a-106">Gå til Administration af produktoplysninger > Konfiguration > Status for produktlivscyklus.</span><span class="sxs-lookup"><span data-stu-id="3b86a-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="3b86a-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3b86a-107">Click New.</span></span>
3. <span data-ttu-id="3b86a-108">Skriv en værdi i feltet Status.</span><span class="sxs-lookup"><span data-stu-id="3b86a-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="3b86a-109">Vælg Ja i feltet Standard ved frigivelse til juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="3b86a-109">Select Yes in the Default when released to legal entity field.</span></span>
5. <span data-ttu-id="3b86a-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3b86a-110">In the Description field, type a value.</span></span>
6. <span data-ttu-id="3b86a-111">Vælg Nej i feltet Er aktiv for planlægning.</span><span class="sxs-lookup"><span data-stu-id="3b86a-111">Select No in the Is active for planning field.</span></span>

> [!NOTE]
> <span data-ttu-id="3b86a-112">Hvis et nyt frigivet produkt ikke skal medtages i varedisponering, skal du vælge Nej.</span><span class="sxs-lookup"><span data-stu-id="3b86a-112">If a new released product should not be included in Master planning, select No.</span></span> <span data-ttu-id="3b86a-113">Hvis det skal medtages i varedisponering, skal kontrolelementet beholde standardværdien Ja.</span><span class="sxs-lookup"><span data-stu-id="3b86a-113">If it should be included in Master planning, leave the control at its default value Yes.</span></span>  

## <a name="create-a-new-released-product"></a><span data-ttu-id="3b86a-114">Opret et nyt frigivet produkt</span><span class="sxs-lookup"><span data-stu-id="3b86a-114">Create a new released product</span></span>
1. <span data-ttu-id="3b86a-115">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3b86a-115">Close the page.</span></span>
2. <span data-ttu-id="3b86a-116">Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="3b86a-116">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="3b86a-117">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3b86a-117">Click New.</span></span>
4. <span data-ttu-id="3b86a-118">Skriv en værdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="3b86a-118">In the Product number field, type a value.</span></span>
5. <span data-ttu-id="3b86a-119">Angiv en værdi i feltet Produktnavn.</span><span class="sxs-lookup"><span data-stu-id="3b86a-119">In the Product name field, type a value.</span></span>
6. <span data-ttu-id="3b86a-120">Angiv en værdi i feltet Søgenavn.</span><span class="sxs-lookup"><span data-stu-id="3b86a-120">In the Search name field, type a value.</span></span>
7. <span data-ttu-id="3b86a-121">Indtast eller vælg en værdi i feltet Varemodelgruppe.</span><span class="sxs-lookup"><span data-stu-id="3b86a-121">In the Item model group field, enter or select a value.</span></span>
8. <span data-ttu-id="3b86a-122">Indtast eller vælg en værdi i feltet Varegruppe.</span><span class="sxs-lookup"><span data-stu-id="3b86a-122">In the Item group field, enter or select a value.</span></span>
9. <span data-ttu-id="3b86a-123">Indtast eller vælg en værdi i feltet Lagringsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3b86a-123">In the Storage dimension group field, enter or select a value.</span></span>
10. <span data-ttu-id="3b86a-124">Indtast eller vælg en værdi i feltet Sporingsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3b86a-124">In the Tracking dimension group field, enter or select a value.</span></span>
11. <span data-ttu-id="3b86a-125">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3b86a-125">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="3b86a-126">Standardstatussen for produktlivscyklus er en global definition.</span><span class="sxs-lookup"><span data-stu-id="3b86a-126">The default product lifecycle state is a global definition.</span></span>  

## <a name="change-the-product-to-an-active-state"></a><span data-ttu-id="3b86a-127">Skift produktet til en aktiv tilstand</span><span class="sxs-lookup"><span data-stu-id="3b86a-127">Change the product to an active state</span></span>
1. <span data-ttu-id="3b86a-128">Indtast eller vælg en værdi i feltet Status for produktlivscyklus.</span><span class="sxs-lookup"><span data-stu-id="3b86a-128">In the Product lifecycle state field, enter or select a value.</span></span>

> [!NOTE]
> <span data-ttu-id="3b86a-129">Forudsat at du har oprettet en aktiv tilstand, kan du nu vælge den aktive tilstand for at tillade, at produktet bruges i varedisponering og styklisteniveauberegning.</span><span class="sxs-lookup"><span data-stu-id="3b86a-129">Assume that you have set up an active state, you can now select the active state to allow the product to be used in Master planning and BOM-level calculation.</span></span> <span data-ttu-id="3b86a-130">Selvfølgelig giver dette kun mening, hvis alle produktoplysningerne, der skal bruges til ensartet planlægning er angivet.</span><span class="sxs-lookup"><span data-stu-id="3b86a-130">Obviously, this only makes sense if all the product details that are required for consistent planning are specified.</span></span>  

