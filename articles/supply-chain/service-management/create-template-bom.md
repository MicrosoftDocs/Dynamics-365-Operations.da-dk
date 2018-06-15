---
title: Oprette en styklisteskabelon
description: "Du kan oprette en skabelonstykliste ved hjælp af forskellige fremgangsmåder."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATemplateBOMTable
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
ms.openlocfilehash: a80cf596a3e7c7f08d493a0fb7350fad62d38c3e
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="create-a-template-bom"></a><span data-ttu-id="a4aa9-103">Oprette en styklisteskabelon</span><span class="sxs-lookup"><span data-stu-id="a4aa9-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a4aa9-104">Du kan oprette en skabelonstykliste ved hjælp af følgende fremgangsmåder.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="a4aa9-105">Uanset hvilken fremgangsmåde du vælger, er felterne **Fra dato** og **Til dato** valgfrie og kan kun bruges som ekstra oplysninger.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="a4aa9-106">Oprette en styklisteskabelon manuelt</span><span class="sxs-lookup"><span data-stu-id="a4aa9-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="a4aa9-107">Klik på **Servicestyring** \> **Opsætning** \> **Serviceobjekter** \> **Styklisteskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="a4aa9-108">Tryk på CTRL+N for at åbne formularen **Opret styklisteskabelon**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="a4aa9-109">Under **Kopier styklistelinjer fra reference** skal du vælge indstillingen **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="a4aa9-110">Angiv en vare af typen **Stykliste** i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="a4aa9-111">Angiv et navn til skabelonen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="a4aa9-112">Angiv det datointerval, hvor styklisteskabelonen skal gælde, i felterne **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="a4aa9-113">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-113">Click **OK**.</span></span>

<span data-ttu-id="a4aa9-114">Der oprettes en ny tom styklisteskabelon.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="a4aa9-115">Oprette en styklisteskabelon ud fra en anden styklisteskabelon</span><span class="sxs-lookup"><span data-stu-id="a4aa9-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="a4aa9-116">Klik på **Servicestyring** \> **Opsætning** \> **Serviceobjekter** \> **Styklisteskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="a4aa9-117">Tryk på CTRL+N for at åbne formularen **Opret styklisteskabelon**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="a4aa9-118">Under **Kopier styklistelinjer fra reference** skal du vælge indstillingen **Styklisteskabelon**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="a4aa9-119">I feltet **Referencenummer** skal du vælge en eksisterende styklisteskabelon, som skal kopieres til den nye styklisteskabelon.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="a4aa9-120">Angiv et navn til skabelonen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="a4aa9-121">Angiv det datointerval, hvor styklisteskabelonen skal gælde, i felterne **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="a4aa9-122">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-122">Click **OK**.</span></span>

<span data-ttu-id="a4aa9-123">Der oprettes en ny styklisteskabelon med linjer, der svarer til linjerne i den oprindelige styklisteskabelon.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="a4aa9-124">Oprette en styklisteskabelon ud fra en varestykliste</span><span class="sxs-lookup"><span data-stu-id="a4aa9-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="a4aa9-125">Klik på **Servicestyring** \> **Opsætning** \> **Serviceobjekter** \> **Styklisteskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="a4aa9-126">Tryk på CTRL+N for at åbne formularen **Opret styklisteskabelon**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="a4aa9-127">Under **Kopier styklistelinjer fra reference** skal du vælge **Stykliste**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="a4aa9-128">I feltet **Referencenummer** skal du vælge en styklisteversion.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="a4aa9-129">En vare af typen stykliste kopieres til feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="a4aa9-130">Angiv et navn til skabelonen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="a4aa9-131">Angiv det datointerval, hvor styklisteskabelonen skal gælde, i felterne **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="a4aa9-132">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-132">Click **OK**.</span></span>

<span data-ttu-id="a4aa9-133">Der oprettes en ny styklisteskabelon vha. de linjer, der svarer til linjerne i den stykliste, der er vist i **Styklister**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="a4aa9-134">Oprette en styklisteskabelon ud fra en produktionsstykliste</span><span class="sxs-lookup"><span data-stu-id="a4aa9-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="a4aa9-135">Klik på **Servicestyring** \> **Opsætning** \> **Serviceobjekter** \> **Styklisteskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="a4aa9-136">Tryk på CTRL+N for at åbne formularen **Opret styklisteskabelon**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="a4aa9-137">Under **Kopier styklistelinjer fra reference** skal du vælge **Produktion**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="a4aa9-138">I feltet **Referencenummer** skal du vælge en produktionsstykliste.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="a4aa9-139">Angiv et navn til skabelonen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="a4aa9-140">Angiv det datointerval, hvor styklisteskabelonen skal gælde, i felterne **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="a4aa9-141">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-141">Click **OK**.</span></span>

<span data-ttu-id="a4aa9-142">Der oprettes en ny styklisteskabelon vha. de linjer, der svarer til linjerne i den stykliste, der er vist i **Stykliste**.</span><span class="sxs-lookup"><span data-stu-id="a4aa9-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4aa9-143">Se også</span><span class="sxs-lookup"><span data-stu-id="a4aa9-143">See also</span></span>

[<span data-ttu-id="a4aa9-144">Styklisteskabeloner</span><span class="sxs-lookup"><span data-stu-id="a4aa9-144">Template BOMs</span></span>](template-boms.md)

  


