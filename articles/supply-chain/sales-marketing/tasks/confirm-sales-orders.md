---
title: Bekræfte salgsordrer
description: Denne fremgangsmåde viser, hvordan du bekræfter salgsordrer.
author: omulvad
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6383576302789d268d64edcbbe05305b03e956d0
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148694"
---
# <a name="confirm-sales-orders"></a><span data-ttu-id="a1c0f-103">Bekræfte salgsordrer</span><span class="sxs-lookup"><span data-stu-id="a1c0f-103">Confirm sales orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a1c0f-104">Denne fremgangsmåde viser, hvordan du bekræfter salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-104">This procedure demonstrates how to confirm sales orders.</span></span> <span data-ttu-id="a1c0f-105">Du får vist, hvordan du bekræfter en enkelt ordre, og hvordan du bekræfter flere ordrer på én gang.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-105">You'll be shown how to confirm a single order, and how to confirm multiple orders at once.</span></span> <span data-ttu-id="a1c0f-106">Disse opgaver udføres normalt af en salgsordrebehandler.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-106">These tasks would typically be carried out by a sales order processor.</span></span> <span data-ttu-id="a1c0f-107">Du kan bruge denne procedure på USMF-demodatafirmaet eller dine egne data.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="a1c0f-108">Kontrollér, at der er flere åbne salgsordrer for samme debitor, før du starter.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-108">Before you start, make sure there are several open sales orders for the same customer.</span></span> <span data-ttu-id="a1c0f-109">Hvis du bruger USMF, kan du bruge debitor US-027.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-109">If you're using USMF, you can use customer US-027.</span></span>


## <a name="confirm-a-single-sales-order"></a><span data-ttu-id="a1c0f-110">Bekræft en enkelt salgsordre</span><span class="sxs-lookup"><span data-stu-id="a1c0f-110">Confirm a single sales order</span></span>
1. <span data-ttu-id="a1c0f-111">Gå til **Navigationsrude > Moduler > Salg og marketing > Salgsordrer > Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-111">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="a1c0f-112">På listen skal du finde og vælge den ordre, du vil bekræfte.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-112">In the list, find and select the order that you want to confirm.</span></span>
3. <span data-ttu-id="a1c0f-113">Klik på linket på salgsordrenummeret for at åbne den valgte ordre.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-113">Click the link on the sales order number to open the selected order.</span></span>
4. <span data-ttu-id="a1c0f-114">Klik på **Sælg** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-114">On the **Action Pane**, click **Sell**.</span></span>
5. <span data-ttu-id="a1c0f-115">Klik på **Bekræft salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-115">Click **Confirm sales order**.</span></span>
6. <span data-ttu-id="a1c0f-116">Udvid sektionen **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-116">Expand the **Parameters** section.</span></span> <span data-ttu-id="a1c0f-117">Kontroller, at indstillingen **Bogføring** er indstillet til 'Ja'.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-117">Make sure that the **Posting** option is set to 'Yes'.</span></span>  
7. <span data-ttu-id="a1c0f-118">Sæt indstillingen **Udskrivning af bekræftelse** til 'Ja'.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-118">Set the **Print confirmation option** to 'Yes'.</span></span> <span data-ttu-id="a1c0f-119">Feltet **Kontrollér kreditmaks** angiver den metode, der bruges til at beregne en kundes resterende kredit.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-119">The **Check credit limit** field specifies the method that's used to calculate a customer's remaining credit.</span></span> <span data-ttu-id="a1c0f-120">Koden kopieres som standard fra siden konti Debitorparametre.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-120">By default, it's copied from the Accounts receivable parameters page.</span></span> <span data-ttu-id="a1c0f-121">Hvis du vil springe kontrollen af kreditmaksimum over, når du bekræfter en bestemt salgsordre, kan du indstille **Kontrollér kreditmaks.** til 'Ingen'.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-121">If you want to skip the credit limit check when confirming a specific sales order, set the **Check credit limit** to 'None'.</span></span> <span data-ttu-id="a1c0f-122">Du skal dog være opmærksom på, at selv hvis dette felt er indstillet til 'Ingen', bliver Kontrollér kreditmaks. stadig udført, hvis indstillingen **Tvungen kreditmaks** er valgt i kundens masterdata.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-122">However, you should be aware that even with if this field is set to 'None', the credit limit check will still be performed if the **Mandatory credit limit** option is selected on the customer master data.</span></span> 
8. <span data-ttu-id="a1c0f-123">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-123">Click **OK**.</span></span>
9. <span data-ttu-id="a1c0f-124">Klik på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-124">Click **Yes**.</span></span>
10. <span data-ttu-id="a1c0f-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-125">Close the page.</span></span>
11. <span data-ttu-id="a1c0f-126">Klik på **Indstillinger** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-126">On the **Action Pane**, click **Options**.</span></span>
12. <span data-ttu-id="a1c0f-127">Klik på **Skift visning**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-127">Click **Change view**.</span></span>
13. <span data-ttu-id="a1c0f-128">Klik på **Overskriftsvisning**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-128">Click **Header view**.</span></span> <span data-ttu-id="a1c0f-129">Når en ordre er bekræftet, angives **Dokumentstatus** til 'Bekræftelse'.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-129">When an order is confirmed, the **Document status** is set to 'Confirmation'.</span></span> 
14. <span data-ttu-id="a1c0f-130">Klik på **Sælg** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-130">On the **Action Pane**, click **Sell**.</span></span>
15. <span data-ttu-id="a1c0f-131">Klik på **Salgsordrebekræftelse**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-131">Click **Sales order confirmation**.</span></span>
16. <span data-ttu-id="a1c0f-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-132">Close the page.</span></span>

## <a name="confirm-multiple-sales-orders-at-once"></a><span data-ttu-id="a1c0f-133">Bekræft flere salgsordrer på samme tid</span><span class="sxs-lookup"><span data-stu-id="a1c0f-133">Confirm multiple sales orders at once</span></span>
1. <span data-ttu-id="a1c0f-134">Gå til **Salg og marketing > Salgsordrer > Ordrebekræftelse > Bekræft salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-134">Go to **Sales and marketing > Sales orders > Order confirmation > Confirm sales order**.</span></span>
2. <span data-ttu-id="a1c0f-135">Klik på **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-135">Click **Select**.</span></span>
3. <span data-ttu-id="a1c0f-136">På listen under fanen **Interval** skal du finde og vælge den post, der henviser til feltet **Debitorkonto**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-136">In the list on the **Range** tab, find and select the record that references the **Customer account** field.</span></span>
4. <span data-ttu-id="a1c0f-137">Klik på rullelisten i feltet **Kriterier** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-137">In the **Criteria** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a1c0f-138">På listen skal du finde og vælge den debitorkonto med flere ordrer, du vil massebekræfte.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-138">In the list, find and select the customer account that has multiple orders which you want to mass confirm.</span></span> <span data-ttu-id="a1c0f-139">Hvis du bruger USMF, kan du vælge kontoen US-027.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-139">If you're using USMF, you can select account US-027.</span></span>  
6. <span data-ttu-id="a1c0f-140">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-140">Click **OK**.</span></span>
    - <span data-ttu-id="a1c0f-141">Fanen **Oversigt** viser en liste over de ordrer, der opfylder søgekriterierne.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-141">The **Overview** tab displays a list of the orders that match the query criteria.</span></span> <span data-ttu-id="a1c0f-142">Disse medtages i bekræftelsen.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-142">These will be included in the confirmation.</span></span>  
    - <span data-ttu-id="a1c0f-143">Feltet **Samleopdatering for** i afsnittet **Parametre** angiver parameteren, som flere ordrer skal opsummeres i, i et enkelt bekræftelsesdokument.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-143">The **Summary update for** field in the **Parameters** section specifies the parameter by which multiple orders are to be summarized into one confirmation document.</span></span> <span data-ttu-id="a1c0f-144">Indstillingen kopieres som standard fra indstillingen **Standardværdier for samleopdatering** på siden **Debitorparametre**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-144">By default, the option is copied from the D**efault values for summary update setting** on the **Accounts receivable parameters** page.</span></span>  
7. <span data-ttu-id="a1c0f-145">Vælg "Ordre" i **Samleopdatering for** felt.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-145">In the **Summary update for** field, select 'Order'.</span></span> <span data-ttu-id="a1c0f-146">Minimumsparametrene, der er påkrævet til at oprette samleopdateringer, er **Fakturakonto** og **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-146">The minimum parameters that are required to create summary updates are **Invoice account** and **Currency**.</span></span> <span data-ttu-id="a1c0f-147">Det betyder, at samleopdateringer, der har forskellige fakturakonti og forskellige valutaer, ikke er tilladt.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-147">This means that summary updates that have different invoice accounts and different currencies are not allowed.</span></span> <span data-ttu-id="a1c0f-148">Yderligere parametre kan konfigureres på siden **Samleopdateringsparametre**, der er tilgængelig fra siden **Debitorparametre**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-148">Additional parameters can be set up in the **Summary update parameters** page which is accessible from the **Accounts receivable parameters** page.</span></span> 
8. <span data-ttu-id="a1c0f-149">Klik på rullelisten i feltet **Salgsordrer** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-149">In the **Sales order** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="a1c0f-150">Vælg det ordrenummer, der skal udgøre salgsordren, på listen.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-150">In the list, select the order number that you want to be the summary order.</span></span>
10. <span data-ttu-id="a1c0f-151">Klik på **Arranger**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-151">Click **Arrange**.</span></span>
11. <span data-ttu-id="a1c0f-152">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-152">Click **OK**.</span></span>
12. <span data-ttu-id="a1c0f-153">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="a1c0f-153">Click **OK**.</span></span>

