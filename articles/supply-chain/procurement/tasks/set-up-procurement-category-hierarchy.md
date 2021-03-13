---
title: Konfigurer et indkøbskategorihierarki
description: Denne fremgangsmåde viser, hvordan du opretter nye noder i et indkøbskategorihierarki, og hvordan du konfigurerer en indkøbskategori, der skal bruges i en indkøbsproces.
author: RichardLuan
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb37b2761708770b82f23cfbed86248d30a59410
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017310"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="080f2-103">Konfigurer et indkøbskategorihierarki</span><span class="sxs-lookup"><span data-stu-id="080f2-103">Set up a procurement category hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="080f2-104">Denne fremgangsmåde viser, hvordan du opretter nye noder i et indkøbskategorihierarki, og hvordan du konfigurerer en indkøbskategori, der skal bruges i en indkøbsproces.</span><span class="sxs-lookup"><span data-stu-id="080f2-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="080f2-105">Disse opgaver udføres normalt af en indkøbschef.</span><span class="sxs-lookup"><span data-stu-id="080f2-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="080f2-106">Før du starter denne procedure, skal der være en kategorihierarki af typen Indkøb.</span><span class="sxs-lookup"><span data-stu-id="080f2-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="080f2-107">Hvis du bruger et demodatafirma, kan du køre denne procedure i USMF-firmaet.</span><span class="sxs-lookup"><span data-stu-id="080f2-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="080f2-108">Tilføj en ny indkøbskategori</span><span class="sxs-lookup"><span data-stu-id="080f2-108">Add a new procurement category</span></span>
1. <span data-ttu-id="080f2-109">Gå til **Navigationsrude > Moduler > Indkøb og forsyning > Konsignation > Indkøbskategorier**.</span><span class="sxs-lookup"><span data-stu-id="080f2-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="080f2-110">Gå til handlingsruden, og vælg **Rediger kategorihierarki**.</span><span class="sxs-lookup"><span data-stu-id="080f2-110">On the Action Pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="080f2-111">Det aktuelle indkøbskategorihierarki vises i venstre side af siden.</span><span class="sxs-lookup"><span data-stu-id="080f2-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="080f2-112">Du er ved at ændre hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="080f2-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="080f2-113">Vælg **Ny kategorinode** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="080f2-113">On the Action Pane, select **New category node**.</span></span> <span data-ttu-id="080f2-114">Systemet vælger øverste node som standard.</span><span class="sxs-lookup"><span data-stu-id="080f2-114">The system selects the top node by default.</span></span> <span data-ttu-id="080f2-115">Hvis du kører denne procedure som en opgaveguide, kan du klikke på knappen Lås op og vælge en anden overordnet node for at indsætte en ny node.</span><span class="sxs-lookup"><span data-stu-id="080f2-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="080f2-116">Når det er gjort, skal du låse opgaveguiden igen og derefter klikke på Ny kategorinode.</span><span class="sxs-lookup"><span data-stu-id="080f2-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="080f2-117">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="080f2-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="080f2-118">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="080f2-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="080f2-119">Indtast en værdi i feltet **Brugervenligt navn**.</span><span class="sxs-lookup"><span data-stu-id="080f2-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="080f2-120">Det fulde navn er valgfrit.</span><span class="sxs-lookup"><span data-stu-id="080f2-120">The friendly name is optional.</span></span> <span data-ttu-id="080f2-121">Det vises i kategoriopslag sammen med navnet på kategorien.</span><span class="sxs-lookup"><span data-stu-id="080f2-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="080f2-122">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="080f2-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="080f2-123">Føj produkter til den nye indkøbskategori</span><span class="sxs-lookup"><span data-stu-id="080f2-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="080f2-124">Gå til **Indkøb og forsyning > Konsignation > Indkøbskategorier**.</span><span class="sxs-lookup"><span data-stu-id="080f2-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="080f2-125">Vælg den node, du lige har tilføjet.</span><span class="sxs-lookup"><span data-stu-id="080f2-125">Select the node you just added.</span></span> <span data-ttu-id="080f2-126">Hvis du kører denne procedure som en opgaveguide, skal du eventuelt låse opgaveguiden op for at vælge noden.</span><span class="sxs-lookup"><span data-stu-id="080f2-126">If you're running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="080f2-127">Slå udvidelsen af sektionen **Produkter** til/fra.</span><span class="sxs-lookup"><span data-stu-id="080f2-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="080f2-128">Vælg **Tilføj** for at knytte produkter til indkøbskategorien.</span><span class="sxs-lookup"><span data-stu-id="080f2-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="080f2-129">Vælg de produkter, der skal føjes til indkøbskategorien.</span><span class="sxs-lookup"><span data-stu-id="080f2-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="080f2-130">Vælg pilen for at tilføje produkter i tabellen **Valgte**.</span><span class="sxs-lookup"><span data-stu-id="080f2-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="080f2-131">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="080f2-131">Select **OK**.</span></span>
