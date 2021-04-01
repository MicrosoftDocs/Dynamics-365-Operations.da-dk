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
ms.openlocfilehash: 44fd02d37ec4e6431ca25dc980ed1d1785e45fac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239344"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="eb6df-103">Konfigurer et indkøbskategorihierarki</span><span class="sxs-lookup"><span data-stu-id="eb6df-103">Set up a procurement category hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eb6df-104">Denne fremgangsmåde viser, hvordan du opretter nye noder i et indkøbskategorihierarki, og hvordan du konfigurerer en indkøbskategori, der skal bruges i en indkøbsproces.</span><span class="sxs-lookup"><span data-stu-id="eb6df-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="eb6df-105">Disse opgaver udføres normalt af en indkøbschef.</span><span class="sxs-lookup"><span data-stu-id="eb6df-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="eb6df-106">Før du starter denne procedure, skal der være en kategorihierarki af typen Indkøb.</span><span class="sxs-lookup"><span data-stu-id="eb6df-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="eb6df-107">Hvis du bruger et demodatafirma, kan du køre denne procedure i USMF-firmaet.</span><span class="sxs-lookup"><span data-stu-id="eb6df-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="eb6df-108">Tilføj en ny indkøbskategori</span><span class="sxs-lookup"><span data-stu-id="eb6df-108">Add a new procurement category</span></span>
1. <span data-ttu-id="eb6df-109">Gå til **Navigationsrude > Moduler > Indkøb og forsyning > Konsignation > Indkøbskategorier**.</span><span class="sxs-lookup"><span data-stu-id="eb6df-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="eb6df-110">Gå til handlingsruden, og vælg **Rediger kategorihierarki**.</span><span class="sxs-lookup"><span data-stu-id="eb6df-110">On the Action Pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="eb6df-111">Det aktuelle indkøbskategorihierarki vises i venstre side af siden.</span><span class="sxs-lookup"><span data-stu-id="eb6df-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="eb6df-112">Du er ved at ændre hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="eb6df-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="eb6df-113">Vælg **Ny kategorinode** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="eb6df-113">On the Action Pane, select **New category node**.</span></span> <span data-ttu-id="eb6df-114">Systemet vælger øverste node som standard.</span><span class="sxs-lookup"><span data-stu-id="eb6df-114">The system selects the top node by default.</span></span> <span data-ttu-id="eb6df-115">Hvis du kører denne procedure som en opgaveguide, kan du klikke på knappen Lås op og vælge en anden overordnet node for at indsætte en ny node.</span><span class="sxs-lookup"><span data-stu-id="eb6df-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="eb6df-116">Når det er gjort, skal du låse opgaveguiden igen og derefter klikke på Ny kategorinode.</span><span class="sxs-lookup"><span data-stu-id="eb6df-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="eb6df-117">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="eb6df-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="eb6df-118">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="eb6df-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="eb6df-119">Indtast en værdi i feltet **Brugervenligt navn**.</span><span class="sxs-lookup"><span data-stu-id="eb6df-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="eb6df-120">Det fulde navn er valgfrit.</span><span class="sxs-lookup"><span data-stu-id="eb6df-120">The friendly name is optional.</span></span> <span data-ttu-id="eb6df-121">Det vises i kategoriopslag sammen med navnet på kategorien.</span><span class="sxs-lookup"><span data-stu-id="eb6df-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="eb6df-122">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="eb6df-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="eb6df-123">Føj produkter til den nye indkøbskategori</span><span class="sxs-lookup"><span data-stu-id="eb6df-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="eb6df-124">Gå til **Indkøb og forsyning > Konsignation > Indkøbskategorier**.</span><span class="sxs-lookup"><span data-stu-id="eb6df-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="eb6df-125">Vælg den node, du lige har tilføjet.</span><span class="sxs-lookup"><span data-stu-id="eb6df-125">Select the node you just added.</span></span> <span data-ttu-id="eb6df-126">Hvis du kører denne procedure som en opgaveguide, skal du eventuelt låse opgaveguiden op for at vælge noden.</span><span class="sxs-lookup"><span data-stu-id="eb6df-126">If you're running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="eb6df-127">Slå udvidelsen af sektionen **Produkter** til/fra.</span><span class="sxs-lookup"><span data-stu-id="eb6df-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="eb6df-128">Vælg **Tilføj** for at knytte produkter til indkøbskategorien.</span><span class="sxs-lookup"><span data-stu-id="eb6df-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="eb6df-129">Vælg de produkter, der skal føjes til indkøbskategorien.</span><span class="sxs-lookup"><span data-stu-id="eb6df-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="eb6df-130">Vælg pilen for at tilføje produkter i tabellen **Valgte**.</span><span class="sxs-lookup"><span data-stu-id="eb6df-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="eb6df-131">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="eb6df-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]