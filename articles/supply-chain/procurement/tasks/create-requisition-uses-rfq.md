---
title: Oprette en rekvisition, der bruger en tilbudsanmodning
description: Dette emne forklarer, hvordan du føjer pris- og leverandøroplysninger til en indkøbsrekvisition fra en tilbudsanmodningsproces.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: abe6745682030766eabcd4411121866c9d890be0
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149614"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="a2000-103">Oprette en rekvisition, der bruger en tilbudsanmodning</span><span class="sxs-lookup"><span data-stu-id="a2000-103">Create a requisition that uses an RFQ</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a2000-104">Dette emne forklarer, hvordan du føjer pris- og leverandøroplysninger til en indkøbsrekvisition fra en tilbudsanmodningsproces.</span><span class="sxs-lookup"><span data-stu-id="a2000-104">This topic explains how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="a2000-105">Eksemplet i denne vejledning kan bruges i USMF-demodatafirmaet, og du skal være logget på som administrator for at fuldføre alle trin.</span><span class="sxs-lookup"><span data-stu-id="a2000-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="a2000-106">Opgaverne i denne vejledning udføres normalt af indkøbsmedarbejderne.</span><span class="sxs-lookup"><span data-stu-id="a2000-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="a2000-107">Opret en rekvisition</span><span class="sxs-lookup"><span data-stu-id="a2000-107">Create a requisition</span></span>
1. <span data-ttu-id="a2000-108">Gå i navigationsruden til **Moduler > Indkøb og forsyning > Indkøbsrekvisitioner > Indkøbsrekvisitioner, der er udarbejdet af mig**.</span><span class="sxs-lookup"><span data-stu-id="a2000-108">In the navigation pane, go to **Modules > Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me**.</span></span>
2. <span data-ttu-id="a2000-109">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a2000-109">Select **New**.</span></span>
3. <span data-ttu-id="a2000-110">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a2000-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="a2000-111">Angiv en dato i feltet **Ønsket dato**.</span><span class="sxs-lookup"><span data-stu-id="a2000-111">In the **Requested date** field, enter a date.</span></span>
5. <span data-ttu-id="a2000-112">Angiv en dato i feltet **Regnskabsdato**.</span><span class="sxs-lookup"><span data-stu-id="a2000-112">In the **Accounting date** field, enter a date.</span></span>
6. <span data-ttu-id="a2000-113">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2000-113">Select **OK**.</span></span>
7. <span data-ttu-id="a2000-114">Indtast eller vælg en værdi i feltet **Årsag**.</span><span class="sxs-lookup"><span data-stu-id="a2000-114">In the **Reason** field, enter or select a value.</span></span>
8. <span data-ttu-id="a2000-115">Vælg **Tilføj linje**.</span><span class="sxs-lookup"><span data-stu-id="a2000-115">Select **Add line**.</span></span>
9. <span data-ttu-id="a2000-116">Vælg en kategori i træet i feltet **Indkøbskategori**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2000-116">In the **Procurement category** field, select a category in the tree, and then select **OK**.</span></span>
10. <span data-ttu-id="a2000-117">Skriv en værdi i feltet **Produktnavn**.</span><span class="sxs-lookup"><span data-stu-id="a2000-117">In the **Product name** field, type a value.</span></span>
11. <span data-ttu-id="a2000-118">Angiv et tal i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="a2000-118">In the **Quantity** field, enter a number.</span></span>
12. <span data-ttu-id="a2000-119">Indtast eller vælg en værdi i feltet **Enhed**.</span><span class="sxs-lookup"><span data-stu-id="a2000-119">In the **Unit** field, enter or select a value.</span></span>
13. <span data-ttu-id="a2000-120">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a2000-120">Select **Save**.</span></span>
14. <span data-ttu-id="a2000-121">Vælg **Arbejdsgang** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="a2000-121">Select **Workflow** to open the drop dialog.</span></span>
15. <span data-ttu-id="a2000-122">Vælg **Send**.</span><span class="sxs-lookup"><span data-stu-id="a2000-122">Select **Submit**.</span></span>
16. <span data-ttu-id="a2000-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a2000-123">Close the page.</span></span>
17. <span data-ttu-id="a2000-124">Vælg **Send**.</span><span class="sxs-lookup"><span data-stu-id="a2000-124">Select **Submit**.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="a2000-125">Tildel en opgave i en arbejdsgang til en anden</span><span class="sxs-lookup"><span data-stu-id="a2000-125">Reassign a workflow task</span></span>
<span data-ttu-id="a2000-126">Den næste opgave er at oprette en tilbudsanmodning for at få tilbud på produktet fra leverandører.</span><span class="sxs-lookup"><span data-stu-id="a2000-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="a2000-127">I demodataene for USMF er arbejdsgangen for indkøbsrekvisitionen konfigureret med en regel, at hvis en leverandør ikke er markeret, eller hvis prisen er 0 for en linje, tildeles der en opgave til en bestemt arbejder om at oprette en tilbudsanmodning.</span><span class="sxs-lookup"><span data-stu-id="a2000-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="a2000-128">For at fortsætte med denne vejledning skal du gentildele opgaven til en anden bruger (dig selv).</span><span class="sxs-lookup"><span data-stu-id="a2000-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="a2000-129">Det kan du kun gøre, hvis du er logget på som administrator.</span><span class="sxs-lookup"><span data-stu-id="a2000-129">You can only do this if you are logged in as an Admin.</span></span>  

1. <span data-ttu-id="a2000-130">Vælg **Arbejdsgang** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="a2000-130">Select **Workflow** to open the drop dialog.</span></span>
2. <span data-ttu-id="a2000-131">Vælg **Vis historik**.</span><span class="sxs-lookup"><span data-stu-id="a2000-131">Select **View history**.</span></span>
3. <span data-ttu-id="a2000-132">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="a2000-132">Refresh the page.</span></span>
4. <span data-ttu-id="a2000-133">Udvid sektionen **Sporingsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="a2000-133">Expand the **Tracking details** section.</span></span>
5. <span data-ttu-id="a2000-134">Vælg den linje, der starter med "Arbejdsgang for linjeelement aktiveret den" i træet.</span><span class="sxs-lookup"><span data-stu-id="a2000-134">In the tree, select the line that starts with "Line workflow activated on".</span></span>
6. <span data-ttu-id="a2000-135">Vælg **Vis detaljer for arbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="a2000-135">Select **View workflow details**.</span></span>
7. <span data-ttu-id="a2000-136">Udvid sektionen **Workflowopgaver**.</span><span class="sxs-lookup"><span data-stu-id="a2000-136">Expand the **Work items** section.</span></span>
8. <span data-ttu-id="a2000-137">Vælg **Tildel igen**.</span><span class="sxs-lookup"><span data-stu-id="a2000-137">Select **Reassign**.</span></span>
9. <span data-ttu-id="a2000-138">Vælg **Administrator** i feltet **Bruger**.</span><span class="sxs-lookup"><span data-stu-id="a2000-138">In the **User** field, select **Admin**.</span></span>
10. <span data-ttu-id="a2000-139">Vælg **Tildel igen**.</span><span class="sxs-lookup"><span data-stu-id="a2000-139">Select **Reassign**.</span></span>
11. <span data-ttu-id="a2000-140">Luk de to sider.</span><span class="sxs-lookup"><span data-stu-id="a2000-140">Close the two pages.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="a2000-141">Opret en tilbudsanmodning</span><span class="sxs-lookup"><span data-stu-id="a2000-141">Create an RFQ</span></span>

1. <span data-ttu-id="a2000-142">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="a2000-142">Refresh the page.</span></span>
2. <span data-ttu-id="a2000-143">Vælg **Tilbudsanmodning**.</span><span class="sxs-lookup"><span data-stu-id="a2000-143">Select **Request for quotation**.</span></span>
3. <span data-ttu-id="a2000-144">Vælg **USMF** i feltet **Juridisk indkøbsenhed**.</span><span class="sxs-lookup"><span data-stu-id="a2000-144">In the **Buying legal entity** field, select **USMF**.</span></span> <span data-ttu-id="a2000-145">Du skal vælge den samme juridiske enhed som den, der er på rekvisitionslinjen.</span><span class="sxs-lookup"><span data-stu-id="a2000-145">You must select the same legal entity that's on the requisition line.</span></span>  
4. <span data-ttu-id="a2000-146">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a2000-146">In the list, mark the selected row.</span></span> <span data-ttu-id="a2000-147">Hvis du havde flere linjer på indkøbsrekvisitionen, kan du vælge alle de linjer, du vil føje til tilbudsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="a2000-147">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="a2000-148">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2000-148">Select **OK**.</span></span>
6. <span data-ttu-id="a2000-149">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="a2000-149">Refresh the page.</span></span>
7. <span data-ttu-id="a2000-150">Åbn faktaboksen, og udvid derefter sektionen **Relaterede dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="a2000-150">Ensure that the FactBox is open, then expand the **Related documents** section.</span></span>
8. <span data-ttu-id="a2000-151">Vælg linket i feltet **Tilbudsanmodning** for at åbne den tilbudsanmodning, der netop er blevet oprettet.</span><span class="sxs-lookup"><span data-stu-id="a2000-151">Select the link in the **Request for quotation** field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="a2000-152">Vælg **Hoved**.</span><span class="sxs-lookup"><span data-stu-id="a2000-152">Select **Header**.</span></span>
10. <span data-ttu-id="a2000-153">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="a2000-153">Select **Add**.</span></span>
11. <span data-ttu-id="a2000-154">Indtast eller vælg en værdi i feltet **Kreditorkonto**.</span><span class="sxs-lookup"><span data-stu-id="a2000-154">In the **Vendor account** field, enter or select a value.</span></span>
12. <span data-ttu-id="a2000-155">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="a2000-155">Select **Add**.</span></span>
13. <span data-ttu-id="a2000-156">Indtast eller vælg en værdi i feltet **Kreditorkonto**.</span><span class="sxs-lookup"><span data-stu-id="a2000-156">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="a2000-157">Vælg **Send**.</span><span class="sxs-lookup"><span data-stu-id="a2000-157">Select **Send**.</span></span>
15. <span data-ttu-id="a2000-158">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2000-158">Select **OK**.</span></span>
16. <span data-ttu-id="a2000-159">Vælg **Indtast svar**.</span><span class="sxs-lookup"><span data-stu-id="a2000-159">Select **Enter reply**.</span></span>
17. <span data-ttu-id="a2000-160">Vælg **Svar** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a2000-160">On the Action Pane, select **Reply**.</span></span>
18. <span data-ttu-id="a2000-161">Vælg **Kopiér data til svar**.</span><span class="sxs-lookup"><span data-stu-id="a2000-161">Select **Copy data to reply**.</span></span> <span data-ttu-id="a2000-162">Derved kopieres data, f.eks. antal og datoer, fra tilbudsanmodningen til svaret.</span><span class="sxs-lookup"><span data-stu-id="a2000-162">This copies data, such as the quantity and dates, from the RFQ to the reply.</span></span>  
19. <span data-ttu-id="a2000-163">Angiv et tal i feltet **Enhedspris**.</span><span class="sxs-lookup"><span data-stu-id="a2000-163">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="a2000-164">Det er den pris, du har modtaget fra leverandøren.</span><span class="sxs-lookup"><span data-stu-id="a2000-164">This is the price that you've received from the vendor.</span></span> <span data-ttu-id="a2000-165">Du kan også angive yderligere oplysninger fra leverandøren.</span><span class="sxs-lookup"><span data-stu-id="a2000-165">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="a2000-166">Vælg **Accepter**.</span><span class="sxs-lookup"><span data-stu-id="a2000-166">Select **Accept**.</span></span>
21. <span data-ttu-id="a2000-167">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2000-167">Select **OK**.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="a2000-168">Kontrollér, at leverandøren og prisen er blevet overført til rekvisitionen</span><span class="sxs-lookup"><span data-stu-id="a2000-168">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="a2000-169">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a2000-169">Close the page.</span></span>
2. <span data-ttu-id="a2000-170">Vælg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="a2000-170">Select **Lines**.</span></span>
3. <span data-ttu-id="a2000-171">Vælg **Relaterede oplysninger**.</span><span class="sxs-lookup"><span data-stu-id="a2000-171">Select **Related information**.</span></span>
4. <span data-ttu-id="a2000-172">Vælg **Indkøbsrekvisition**.</span><span class="sxs-lookup"><span data-stu-id="a2000-172">Select **Purchase requisition**.</span></span>
5. <span data-ttu-id="a2000-173">Vælg den linje, der blev overført til tilbudsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="a2000-173">Select the line that was transferred to the RFQ.</span></span> <span data-ttu-id="a2000-174">Kontrollér, at prisen og leverandøren er blevet kopieret til rekvisitionen.</span><span class="sxs-lookup"><span data-stu-id="a2000-174">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="a2000-175">Vælg **Arbejdsgang** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="a2000-175">Select **Workflow** to open the drop dialog.</span></span>
7. <span data-ttu-id="a2000-176">Vælg Fuldfør.</span><span class="sxs-lookup"><span data-stu-id="a2000-176">Select Complete.</span></span>
8. <span data-ttu-id="a2000-177">Vælg siden.</span><span class="sxs-lookup"><span data-stu-id="a2000-177">Select the page.</span></span>
9. <span data-ttu-id="a2000-178">Vælg Fuldfør.</span><span class="sxs-lookup"><span data-stu-id="a2000-178">Select Complete.</span></span>

