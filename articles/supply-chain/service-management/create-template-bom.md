---
title: Oprette en styklisteskabelon
description: Du kan oprette en skabelonstykliste ved hjælp af forskellige fremgangsmåder.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89c5d45ac27a8678c51fb63c0326c2802a094596
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566576"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="9e44f-103">Oprette en styklisteskabelon</span><span class="sxs-lookup"><span data-stu-id="9e44f-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="9e44f-104">Du kan oprette en skabelonstykliste ved hjælp af følgende fremgangsmåder.</span><span class="sxs-lookup"><span data-stu-id="9e44f-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="9e44f-105">Uanset hvilken fremgangsmåde du vælger, er felterne **Fra dato** og **Til dato** valgfrie og kan kun bruges som ekstra oplysninger.</span><span class="sxs-lookup"><span data-stu-id="9e44f-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="9e44f-106">Oprette en styklisteskabelon manuelt</span><span class="sxs-lookup"><span data-stu-id="9e44f-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="9e44f-107">Klik på **Servicestyring** \> **Opsætning** \> **Serviceobjekter** \> **Styklisteskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="9e44f-108">Tryk på CTRL+N for at åbne formularen **Opret styklisteskabelon**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="9e44f-109">Under **Kopier styklistelinjer fra reference** skal du vælge indstillingen **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="9e44f-110">Angiv en vare af typen **Stykliste** i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="9e44f-111">Angiv et navn til skabelonen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="9e44f-112">Angiv det datointerval, hvor styklisteskabelonen skal gælde, i felterne **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="9e44f-113">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-113">Click **OK**.</span></span>

<span data-ttu-id="9e44f-114">Der oprettes en ny tom styklisteskabelon.</span><span class="sxs-lookup"><span data-stu-id="9e44f-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="9e44f-115">Oprette en styklisteskabelon ud fra en anden styklisteskabelon</span><span class="sxs-lookup"><span data-stu-id="9e44f-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="9e44f-116">Klik på **Servicestyring** \> **Opsætning** \> **Serviceobjekter** \> **Styklisteskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="9e44f-117">Tryk på CTRL+N for at åbne formularen **Opret styklisteskabelon**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="9e44f-118">Under **Kopier styklistelinjer fra reference** skal du vælge indstillingen **Styklisteskabelon**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="9e44f-119">I feltet **Referencenummer** skal du vælge en eksisterende styklisteskabelon, som skal kopieres til den nye styklisteskabelon.</span><span class="sxs-lookup"><span data-stu-id="9e44f-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="9e44f-120">Angiv et navn til skabelonen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="9e44f-121">Angiv det datointerval, hvor styklisteskabelonen skal gælde, i felterne **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="9e44f-122">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-122">Click **OK**.</span></span>

<span data-ttu-id="9e44f-123">Der oprettes en ny styklisteskabelon med linjer, der svarer til linjerne i den oprindelige styklisteskabelon.</span><span class="sxs-lookup"><span data-stu-id="9e44f-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="9e44f-124">Oprette en styklisteskabelon ud fra en varestykliste</span><span class="sxs-lookup"><span data-stu-id="9e44f-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="9e44f-125">Klik på **Servicestyring** \> **Opsætning** \> **Serviceobjekter** \> **Styklisteskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="9e44f-126">Tryk på CTRL+N for at åbne formularen **Opret styklisteskabelon**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="9e44f-127">Under **Kopier styklistelinjer fra reference** skal du vælge **Stykliste**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="9e44f-128">I feltet **Referencenummer** skal du vælge en styklisteversion.</span><span class="sxs-lookup"><span data-stu-id="9e44f-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="9e44f-129">En vare af typen stykliste kopieres til feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="9e44f-130">Angiv et navn til skabelonen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="9e44f-131">Angiv det datointerval, hvor styklisteskabelonen skal gælde, i felterne **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="9e44f-132">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-132">Click **OK**.</span></span>

<span data-ttu-id="9e44f-133">Der oprettes en ny styklisteskabelon vha. de linjer, der svarer til linjerne i den stykliste, der er vist i **Styklister**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="9e44f-134">Oprette en styklisteskabelon ud fra en produktionsstykliste</span><span class="sxs-lookup"><span data-stu-id="9e44f-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="9e44f-135">Klik på **Servicestyring** \> **Opsætning** \> **Serviceobjekter** \> **Styklisteskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="9e44f-136">Tryk på CTRL+N for at åbne formularen **Opret styklisteskabelon**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="9e44f-137">Under **Kopier styklistelinjer fra reference** skal du vælge **Produktion**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="9e44f-138">I feltet **Referencenummer** skal du vælge en produktionsstykliste.</span><span class="sxs-lookup"><span data-stu-id="9e44f-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="9e44f-139">Angiv et navn til skabelonen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="9e44f-140">Angiv det datointerval, hvor styklisteskabelonen skal gælde, i felterne **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="9e44f-141">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-141">Click **OK**.</span></span>

<span data-ttu-id="9e44f-142">Der oprettes en ny styklisteskabelon vha. de linjer, der svarer til linjerne i den stykliste, der er vist i **Stykliste**.</span><span class="sxs-lookup"><span data-stu-id="9e44f-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e44f-143">Se også</span><span class="sxs-lookup"><span data-stu-id="9e44f-143">See also</span></span>

[<span data-ttu-id="9e44f-144">Styklisteskabeloner</span><span class="sxs-lookup"><span data-stu-id="9e44f-144">Template BOMs</span></span>](template-boms.md)

  


