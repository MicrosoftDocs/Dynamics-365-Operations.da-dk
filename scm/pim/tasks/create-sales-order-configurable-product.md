--- 
title: Oprette en salgsordre for et konfigurerbart produkt
description: "Denne procedure viser, hvordan du anvender en konfigurationsskabelon til et produkt på en salgsordre."
author: BibiSp
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7084c3749f18e4fbe90fe4e04bdeac320cefeafa
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="c4d6b-103">Oprette en salgsordre for et konfigurerbart produkt</span><span class="sxs-lookup"><span data-stu-id="c4d6b-103">Create a sales order for a configurable product</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c4d6b-104">Denne procedure viser, hvordan du anvender en konfigurationsskabelon til et produkt på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="c4d6b-105">I dette eksempel bruges modellen D0006-højttaler i demodatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="c4d6b-106">En salgsordrebehandler bruger normalt denne procedure.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="c4d6b-107">Oprette en salgsordre</span><span class="sxs-lookup"><span data-stu-id="c4d6b-107">Create a sales order</span></span>
1. <span data-ttu-id="c4d6b-108">Klik på Salgsordrebehandling og -forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="c4d6b-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-109">Click New.</span></span>
3. <span data-ttu-id="c4d6b-110">Klik på Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-110">Click Sales order.</span></span>
4. <span data-ttu-id="c4d6b-111">Vælg US-001 i feltet Debitorkonto.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="c4d6b-112">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-112">Click OK.</span></span>
6. <span data-ttu-id="c4d6b-113">I feltet Varenummer skal du vælge D0006.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="c4d6b-114">Til denne opgave skal du vælge et produkt, der kan konfigureres.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="c4d6b-115">Klik på Produkt og forsyning.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-115">Click Product and supply.</span></span>
8. <span data-ttu-id="c4d6b-116">Klik på Konfigurer linje.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-116">Click Configure line.</span></span>
    * <span data-ttu-id="c4d6b-117">Bemærk, at prisen er ændret, baseret på den konfiguration, der blev valgt, og at feltet Medtag kabel nu er angivet til Sand.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="c4d6b-118">Bemærk standardprisen og de indstillinger, der er valgt til kablet.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="c4d6b-119">Klik på Indlæs skabelon..</span><span class="sxs-lookup"><span data-stu-id="c4d6b-119">Click Load template.</span></span>
    * <span data-ttu-id="c4d6b-120">Dette eksempel viser, hvordan du kan bruge en skabelon til at vælge en foruddefineret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="c4d6b-121">Hvis du bruger denne procedure som en opgaveguide, og du ønsker at se de andre attributværdier, der er tilgængelige, skal du klikke på knappen Lås op.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-121">If you’re using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="c4d6b-122">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-122">Click OK.</span></span>
11. <span data-ttu-id="c4d6b-123">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-123">Click OK.</span></span>
12. <span data-ttu-id="c4d6b-124">Vis eller skjul sektionen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="c4d6b-125">Klik på fanen Produkt.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-125">Click the Product tab.</span></span>
    * <span data-ttu-id="c4d6b-126">Konfigurationen af varen vises nu under produktdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="c4d6b-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="c4d6b-128">Vælg produktkonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="c4d6b-128">Select the product configuration</span></span>


