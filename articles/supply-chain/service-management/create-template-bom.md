---
title: Oprette en styklisteskabelon
description: Du kan oprette en skabelonstykliste ved hjælp af forskellige fremgangsmåder.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5afcb8171b674281faf8100d5c01fdff8d6ff764
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470756"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="d27ca-103">Oprette en styklisteskabelon</span><span class="sxs-lookup"><span data-stu-id="d27ca-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d27ca-104">Du kan oprette en skabelonstykliste ved hjælp af følgende fremgangsmåder.</span><span class="sxs-lookup"><span data-stu-id="d27ca-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="d27ca-105">Uanset hvilken fremgangsmåde du vælger, er felterne **Fra dato** og **Til dato** valgfrie og kan kun bruges som ekstra oplysninger.</span><span class="sxs-lookup"><span data-stu-id="d27ca-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="d27ca-106">Oprette en styklisteskabelon manuelt</span><span class="sxs-lookup"><span data-stu-id="d27ca-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="d27ca-107">Gå til **Servicestyring** \> **Opsætning** \> **Serviceobjekter** \> **Styklisteskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-107">Go to **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="d27ca-108">Vælg **Ny** for at åbne formularen **Opret styklisteskabelon**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-108">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="d27ca-109">Under **Kopier styklistelinjer fra reference** skal du vælge indstillingen **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="d27ca-110">Angiv en vare af typen **Stykliste** i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="d27ca-111">Angiv et navn til skabelonen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="d27ca-112">Angiv det datointerval, hvor styklisteskabelonen skal gælde, i felterne **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="d27ca-113">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-113">Select **OK**.</span></span>

<span data-ttu-id="d27ca-114">Der oprettes en ny tom styklisteskabelon.</span><span class="sxs-lookup"><span data-stu-id="d27ca-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="d27ca-115">Oprette en styklisteskabelon ud fra en anden styklisteskabelon</span><span class="sxs-lookup"><span data-stu-id="d27ca-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="d27ca-116">Vælg **Servicestyring** \> **Opsætning** \> **Serviceobjekter** \> **Styklisteskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-116">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="d27ca-117">Vælg **Ny** for at åbne formularen **Opret styklisteskabelon**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-117">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="d27ca-118">Under **Kopier styklistelinjer fra reference** skal du vælge indstillingen **Styklisteskabelon**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="d27ca-119">I feltet **Referencenummer** skal du vælge en eksisterende styklisteskabelon, som skal kopieres til den nye styklisteskabelon.</span><span class="sxs-lookup"><span data-stu-id="d27ca-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="d27ca-120">Angiv et navn til skabelonen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="d27ca-121">Angiv det datointerval, hvor styklisteskabelonen skal gælde, i felterne **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="d27ca-122">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-122">Select **OK**.</span></span>

<span data-ttu-id="d27ca-123">Der oprettes en ny styklisteskabelon med linjer, der svarer til linjerne i den oprindelige styklisteskabelon.</span><span class="sxs-lookup"><span data-stu-id="d27ca-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="d27ca-124">Oprette en styklisteskabelon ud fra en varestykliste</span><span class="sxs-lookup"><span data-stu-id="d27ca-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="d27ca-125">Vælg **Servicestyring** \> **Opsætning** \> **Serviceobjekter** \> **Styklisteskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-125">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="d27ca-126">Vælg **Ny** for at åbne formularen **Opret styklisteskabelon**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-126">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="d27ca-127">Under **Kopier styklistelinjer fra reference** skal du vælge **Stykliste**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="d27ca-128">I feltet **Referencenummer** skal du vælge en styklisteversion.</span><span class="sxs-lookup"><span data-stu-id="d27ca-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="d27ca-129">En vare af typen stykliste kopieres til feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="d27ca-130">Angiv et navn til skabelonen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="d27ca-131">Angiv det datointerval, hvor styklisteskabelonen skal gælde, i felterne **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="d27ca-132">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-132">Select **OK**.</span></span>

<span data-ttu-id="d27ca-133">Der oprettes en ny styklisteskabelon vha. de linjer, der svarer til linjerne i den stykliste, der er vist i **Styklister**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="d27ca-134">Oprette en styklisteskabelon ud fra en produktionsstykliste</span><span class="sxs-lookup"><span data-stu-id="d27ca-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="d27ca-135">Vælg **Servicestyring** \> **Opsætning** \> **Serviceobjekter** \> **Styklisteskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-135">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="d27ca-136">Vælg **Ny** for at åbne formularen **Opret styklisteskabelon**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-136">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="d27ca-137">Under **Kopier styklistelinjer fra reference** skal du vælge **Produktion**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="d27ca-138">I feltet **Referencenummer** skal du vælge en produktionsstykliste.</span><span class="sxs-lookup"><span data-stu-id="d27ca-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="d27ca-139">Angiv et navn til skabelonen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="d27ca-140">Angiv det datointerval, hvor styklisteskabelonen skal gælde, i felterne **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="d27ca-141">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-141">Select **OK**.</span></span>

<span data-ttu-id="d27ca-142">Der oprettes en ny styklisteskabelon vha. de linjer, der svarer til linjerne i den stykliste, der er vist i **Stykliste**.</span><span class="sxs-lookup"><span data-stu-id="d27ca-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="d27ca-143">Se også</span><span class="sxs-lookup"><span data-stu-id="d27ca-143">See also</span></span>

[<span data-ttu-id="d27ca-144">Styklisteskabeloner</span><span class="sxs-lookup"><span data-stu-id="d27ca-144">Template BOMs</span></span>](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]