---
title: Oprette en salgsordre for et konfigurerbart produkt
description: Denne procedure viser, hvordan du anvender en konfigurationsskabelon til et produkt på en salgsordre.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8607de5705354aa58c985fb536f3e1d52acd1f37
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921283"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="94dfb-103">Oprette en salgsordre for et konfigurerbart produkt</span><span class="sxs-lookup"><span data-stu-id="94dfb-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="94dfb-104">Denne procedure viser, hvordan du anvender en konfigurationsskabelon til et produkt på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="94dfb-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="94dfb-105">I dette eksempel bruges modellen D0006-højttaler i demodatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="94dfb-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="94dfb-106">En salgsordrebehandler bruger normalt denne procedure.</span><span class="sxs-lookup"><span data-stu-id="94dfb-106">Typically, a sales order processor uses this procedure.</span></span>

## <a name="create-a-sales-order"></a><span data-ttu-id="94dfb-107">Oprette en salgsordre</span><span class="sxs-lookup"><span data-stu-id="94dfb-107">Create a sales order</span></span>

1. <span data-ttu-id="94dfb-108">Gå til **Salg og marketing \> Arbejdsområder \> Salgsordrebehandling og -forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="94dfb-108">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="94dfb-109">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="94dfb-109">Select **New**.</span></span>
1. <span data-ttu-id="94dfb-110">Vælg **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="94dfb-110">Select **Sales order**.</span></span>
1. <span data-ttu-id="94dfb-111">Vælg **US-001** i feltet *Debitorkonto*.</span><span class="sxs-lookup"><span data-stu-id="94dfb-111">In the **Customer account** field, select *US-001*.</span></span> 
1. <span data-ttu-id="94dfb-112">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="94dfb-112">Select **OK**.</span></span>
1. <span data-ttu-id="94dfb-113">Vælg **D0006** i feltet *Varenummer*.</span><span class="sxs-lookup"><span data-stu-id="94dfb-113">In the **Item number** field, select *D0006*.</span></span>
    * <span data-ttu-id="94dfb-114">Til denne opgave skal du vælge et produkt, der kan konfigureres.</span><span class="sxs-lookup"><span data-stu-id="94dfb-114">For this task, you must select a configurable product.</span></span>  
1. <span data-ttu-id="94dfb-115">Vælg **Produkt og forsyning**.</span><span class="sxs-lookup"><span data-stu-id="94dfb-115">Select **Product and supply**.</span></span>
1. <span data-ttu-id="94dfb-116">Vælg **Konfigurer linje**.</span><span class="sxs-lookup"><span data-stu-id="94dfb-116">Select **Configure line**.</span></span>
    * <span data-ttu-id="94dfb-117">Bemærk, at prisen er ændret, baseret på den valgte konfiguration, og at feltet **Medtag kabel** nu er angivet til *Sand*.</span><span class="sxs-lookup"><span data-stu-id="94dfb-117">Note that the price has changed, based on the configuration that was selected, and that the **Include cable** field is now set to *True*.</span></span>  
    * <span data-ttu-id="94dfb-118">Bemærk standardprisen og de indstillinger, der er valgt til kablet.</span><span class="sxs-lookup"><span data-stu-id="94dfb-118">Note the default price and the settings that are selected for the cable.</span></span>  
1. <span data-ttu-id="94dfb-119">Vælg **Indlæs skabelon**.</span><span class="sxs-lookup"><span data-stu-id="94dfb-119">Select **Load template**.</span></span>
    * <span data-ttu-id="94dfb-120">Dette eksempel viser, hvordan du kan bruge en skabelon til at vælge en foruddefineret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="94dfb-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="94dfb-121">Hvis du bruger denne procedure som en opgaveguide, og du ønsker at se de andre attributværdier, der er tilgængelige, skal du vælge knappen **Lås op**.</span><span class="sxs-lookup"><span data-stu-id="94dfb-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must select the **Unlock** button.</span></span>  
1. <span data-ttu-id="94dfb-122">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="94dfb-122">Select **OK**.</span></span>
1. <span data-ttu-id="94dfb-123">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="94dfb-123">Select **OK**.</span></span>
1. <span data-ttu-id="94dfb-124">Vis eller skjul sektionen **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="94dfb-124">Expand the **Line details** section.</span></span>
1. <span data-ttu-id="94dfb-125">Vælg fanen **Produkt**.</span><span class="sxs-lookup"><span data-stu-id="94dfb-125">Select the **Product** tab.</span></span>
    * <span data-ttu-id="94dfb-126">Konfigurationen af varen vises nu under produktdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="94dfb-126">The configuration of the item is now listed under the product dimensions.</span></span>  
1. <span data-ttu-id="94dfb-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="94dfb-127">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]