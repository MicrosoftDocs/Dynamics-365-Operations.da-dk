---
title: Oprette en salgsordre for et konfigurerbart produkt
description: Denne procedure viser, hvordan du anvender en konfigurationsskabelon til et produkt på en salgsordre.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d9a9b60fbcf6de5377b44ca03d4ffc792a6a78f4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206985"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="d7d8f-103">Oprette en salgsordre for et konfigurerbart produkt</span><span class="sxs-lookup"><span data-stu-id="d7d8f-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7d8f-104">Denne procedure viser, hvordan du anvender en konfigurationsskabelon til et produkt på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="d7d8f-105">I dette eksempel bruges modellen D0006-højttaler i demodatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="d7d8f-106">En salgsordrebehandler bruger normalt denne procedure.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="d7d8f-107">Oprette en salgsordre</span><span class="sxs-lookup"><span data-stu-id="d7d8f-107">Create a sales order</span></span>
1. <span data-ttu-id="d7d8f-108">Klik på Salgsordrebehandling og -forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="d7d8f-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-109">Click New.</span></span>
3. <span data-ttu-id="d7d8f-110">Klik på Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-110">Click Sales order.</span></span>
4. <span data-ttu-id="d7d8f-111">Vælg US-001 i feltet Debitorkonto.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="d7d8f-112">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-112">Click OK.</span></span>
6. <span data-ttu-id="d7d8f-113">I feltet Varenummer skal du vælge D0006.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="d7d8f-114">Til denne opgave skal du vælge et produkt, der kan konfigureres.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="d7d8f-115">Klik på Produkt og forsyning.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-115">Click Product and supply.</span></span>
8. <span data-ttu-id="d7d8f-116">Klik på Konfigurer linje.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-116">Click Configure line.</span></span>
    * <span data-ttu-id="d7d8f-117">Bemærk, at prisen er ændret, baseret på den konfiguration, der blev valgt, og at feltet Medtag kabel nu er angivet til Sand.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="d7d8f-118">Bemærk standardprisen og de indstillinger, der er valgt til kablet.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="d7d8f-119">Klik på Indlæs skabelon..</span><span class="sxs-lookup"><span data-stu-id="d7d8f-119">Click Load template.</span></span>
    * <span data-ttu-id="d7d8f-120">Dette eksempel viser, hvordan du kan bruge en skabelon til at vælge en foruddefineret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="d7d8f-121">Hvis du bruger denne procedure som en opgaveguide, og du ønsker at se de andre attributværdier, der er tilgængelige, skal du klikke på knappen Lås op.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="d7d8f-122">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-122">Click OK.</span></span>
11. <span data-ttu-id="d7d8f-123">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-123">Click OK.</span></span>
12. <span data-ttu-id="d7d8f-124">Vis eller skjul sektionen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="d7d8f-125">Klik på fanen Produkt.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-125">Click the Product tab.</span></span>
    * <span data-ttu-id="d7d8f-126">Konfigurationen af varen vises nu under produktdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="d7d8f-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="d7d8f-128">Vælg produktkonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-128">Select the product configuration</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]