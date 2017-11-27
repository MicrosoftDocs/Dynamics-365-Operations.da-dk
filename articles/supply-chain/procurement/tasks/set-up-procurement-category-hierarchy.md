--- 
title: "Konfigurer et indkøbskategorihierarki"
description: "Denne fremgangsmåde viser, hvordan du opretter nye noder i et indkøbskategorihierarki, og hvordan du konfigurerer en indkøbskategori, der skal bruges i en indkøbsproces."
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6ad5c8552a6989e9093d0b1325754bc0f6d19372
ms.openlocfilehash: 4541d029c9c3be3ee42332e5d8ff183dd503f13e
ms.contentlocale: da-dk
ms.lasthandoff: 11/06/2017

---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="5fa82-103">Konfigurer et indkøbskategorihierarki</span><span class="sxs-lookup"><span data-stu-id="5fa82-103">Set up a procurement category hierarchy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5fa82-104">Denne fremgangsmåde viser, hvordan du opretter nye noder i et indkøbskategorihierarki, og hvordan du konfigurerer en indkøbskategori, der skal bruges i en indkøbsproces.</span><span class="sxs-lookup"><span data-stu-id="5fa82-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="5fa82-105">Disse opgaver udføres normalt af en indkøbschef.</span><span class="sxs-lookup"><span data-stu-id="5fa82-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="5fa82-106">Før du starter denne procedure, skal der være en kategorihierarki af typen Indkøb.</span><span class="sxs-lookup"><span data-stu-id="5fa82-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="5fa82-107">Hvis du bruger et demodatafirma, kan du køre denne procedure i USMF-firmaet.</span><span class="sxs-lookup"><span data-stu-id="5fa82-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="5fa82-108">Tilføj en ny indkøbskategori</span><span class="sxs-lookup"><span data-stu-id="5fa82-108">Add a new procurement category</span></span>
1. <span data-ttu-id="5fa82-109">Gå til Indkøb og forsyning > Indkøbskategorier.</span><span class="sxs-lookup"><span data-stu-id="5fa82-109">Go to Procurement and sourcing > Procurement categories.</span></span>
2. <span data-ttu-id="5fa82-110">Klik på Rediger kategorihierarkityper.</span><span class="sxs-lookup"><span data-stu-id="5fa82-110">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="5fa82-111">Det aktuelle indkøbskategorihierarki vises i venstre side af siden.</span><span class="sxs-lookup"><span data-stu-id="5fa82-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="5fa82-112">Du er ved at ændre hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="5fa82-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="5fa82-113">Klik på Ny kategorinode.</span><span class="sxs-lookup"><span data-stu-id="5fa82-113">Click New category node.</span></span>
    * <span data-ttu-id="5fa82-114">Systemet vælger øverste node som standard.</span><span class="sxs-lookup"><span data-stu-id="5fa82-114">The system selects the top node by default.</span></span> <span data-ttu-id="5fa82-115">Hvis du kører denne procedure som en opgaveguide, kan du klikke på knappen Lås op og vælge en anden overordnet node for at indsætte en ny node.</span><span class="sxs-lookup"><span data-stu-id="5fa82-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="5fa82-116">Når det er gjort, skal du låse opgaveguiden igen og derefter klikke på Ny kategorinode.</span><span class="sxs-lookup"><span data-stu-id="5fa82-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="5fa82-117">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="5fa82-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="5fa82-118">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="5fa82-118">In the Description field, type a value.</span></span>
6. <span data-ttu-id="5fa82-119">Indtast en værdi i feltet Brugervenligt navn.</span><span class="sxs-lookup"><span data-stu-id="5fa82-119">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="5fa82-120">Det fulde navn er valgfrit.</span><span class="sxs-lookup"><span data-stu-id="5fa82-120">The friendly name is optional.</span></span> <span data-ttu-id="5fa82-121">Det vises i kategoriopslag sammen med navnet på kategorien.</span><span class="sxs-lookup"><span data-stu-id="5fa82-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="5fa82-122">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="5fa82-122">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="5fa82-123">Føj produkter til den nye indkøbskategori</span><span class="sxs-lookup"><span data-stu-id="5fa82-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="5fa82-124">Gå til Indkøb og forsyning > Indkøbskategorier.</span><span class="sxs-lookup"><span data-stu-id="5fa82-124">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="5fa82-125">Vælg den node, du lige har tilføjet.</span><span class="sxs-lookup"><span data-stu-id="5fa82-125">Select the node you just added.</span></span> <span data-ttu-id="5fa82-126">Hvis du kører denne procedure som en opgaveguide, skal du eventuelt låse opgaveguiden op for at vælge noden.</span><span class="sxs-lookup"><span data-stu-id="5fa82-126">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="5fa82-127">Slå udvidelsen af sektionen Produkter til/fra.</span><span class="sxs-lookup"><span data-stu-id="5fa82-127">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="5fa82-128">Klik på Tilføj for at knytte produkter til indkøbskategorien.</span><span class="sxs-lookup"><span data-stu-id="5fa82-128">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="5fa82-129">Vælg det produkt, der skal føjes til indkøbskategorien.</span><span class="sxs-lookup"><span data-stu-id="5fa82-129">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="5fa82-130">Klik på pilen for at vælge produktet.</span><span class="sxs-lookup"><span data-stu-id="5fa82-130">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="5fa82-131">Vælg et andet produkt, der skal føjes til indkøbskategorien.</span><span class="sxs-lookup"><span data-stu-id="5fa82-131">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="5fa82-132">Klik på pilen for at vælge produktet.</span><span class="sxs-lookup"><span data-stu-id="5fa82-132">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="5fa82-133">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5fa82-133">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="5fa82-134">Tilføj godkendte og foretrukne kreditorer</span><span class="sxs-lookup"><span data-stu-id="5fa82-134">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="5fa82-135">Slå udvidelsen af sektionen Kreditorer til/fra.</span><span class="sxs-lookup"><span data-stu-id="5fa82-135">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="5fa82-136">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="5fa82-136">Click Add.</span></span>
    * <span data-ttu-id="5fa82-137">Du kan føje en kreditor til en indkøbskategori og angive, om en kreditor foretrækkes eller blot er godkendt for kategorien.</span><span class="sxs-lookup"><span data-stu-id="5fa82-137">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="5fa82-138">Når du sletter en leverandør i en kategori, slettes de historiske posteringer for leverandøren i kategorien ikke.</span><span class="sxs-lookup"><span data-stu-id="5fa82-138">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="5fa82-139">Vælg den kreditor, der skal føjes til kategorien.</span><span class="sxs-lookup"><span data-stu-id="5fa82-139">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="5fa82-140">Klik på pilen for at vælge kreditoren.</span><span class="sxs-lookup"><span data-stu-id="5fa82-140">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="5fa82-141">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5fa82-141">Click OK.</span></span>
6. <span data-ttu-id="5fa82-142">Vælg den kreditorrække, du vil redigere.</span><span class="sxs-lookup"><span data-stu-id="5fa82-142">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="5fa82-143">Vælg en indstilling i feltet Kreditorstatus.</span><span class="sxs-lookup"><span data-stu-id="5fa82-143">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="5fa82-144">Indstillingen til valg af kreditor i Politikregel for kategori bestemmer, om foretrukne, godkendte eller alle kreditorer er tilgængelige på indkøbsrekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="5fa82-144">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="5fa82-145">Føj yderligere oplysninger til kategorien</span><span class="sxs-lookup"><span data-stu-id="5fa82-145">Add additional information to the category</span></span>
1. <span data-ttu-id="5fa82-146">Slå udvidelsen af sektionen Kriteriegrupper for kreditorevaluering til/fra.</span><span class="sxs-lookup"><span data-stu-id="5fa82-146">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="5fa82-147">Denne fane giver dig mulighed for at definere, hvilke kriterier kreditorerne i indkøbskategorien skal bedømmes ud fra.</span><span class="sxs-lookup"><span data-stu-id="5fa82-147">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="5fa82-148">Det kan du gøre ved at klikke på Tilføj og derefter vælge en kreditorevalueringsgruppe, der indeholder de ønskede kriterier.</span><span class="sxs-lookup"><span data-stu-id="5fa82-148">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="5fa82-149">Slå udvidelsen af sektionen Spørgeskemaer til/fra.</span><span class="sxs-lookup"><span data-stu-id="5fa82-149">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="5fa82-150">Denne fane giver dig mulighed for at tilføje spørgeskemaer, der vises på rekvisitionen, så længe du angiver aktivitetstypen til "Rekvisition".</span><span class="sxs-lookup"><span data-stu-id="5fa82-150">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="5fa82-151">Anmoderen skal derefter udfylde et spørgeskema, før de kan sende en rekvisition for det eller de specifikke produkter i indkøbskategorien.</span><span class="sxs-lookup"><span data-stu-id="5fa82-151">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="5fa82-152">Slå udvidelsen af sektionen Varemomsgrupper til/fra.</span><span class="sxs-lookup"><span data-stu-id="5fa82-152">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="5fa82-153">Klik på rullelisten i feltet Varemomsgruppe: for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="5fa82-153">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="5fa82-154">Vælg en momsgruppe.</span><span class="sxs-lookup"><span data-stu-id="5fa82-154">Select a sales tax group.</span></span>
6. <span data-ttu-id="5fa82-155">Slå udvidelsen af afsnittet Kategoriside til/fra.</span><span class="sxs-lookup"><span data-stu-id="5fa82-155">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="5fa82-156">Kategorisider oprettes på siden Kategorihierarki.</span><span class="sxs-lookup"><span data-stu-id="5fa82-156">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="5fa82-157">De indeholder oplysninger om indkøbskategorien, f.eks. oplysninger om typen af produkter i en kategori, billeder af produkter i en kategori eller meddelelser, f.eks. rabatter i en kategori.</span><span class="sxs-lookup"><span data-stu-id="5fa82-157">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="5fa82-158">Oplysningerne på en kategoriside vises på indkøbsrekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="5fa82-158">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="5fa82-159">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5fa82-159">Close the page.</span></span>


