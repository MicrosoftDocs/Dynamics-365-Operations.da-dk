--- 
title: "Oprette en købsaftale"
description: "Denne procedure føres du gennem oprettelsen af en købsaftale."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0d0cc6508071bea3f622bc21f06aa55d2b757b6f
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="0bafe-103">Oprette en købsaftale</span><span class="sxs-lookup"><span data-stu-id="0bafe-103">Create a purchase agreement</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0bafe-104">Denne procedure føres du gennem oprettelsen af en købsaftale.</span><span class="sxs-lookup"><span data-stu-id="0bafe-104">This procedure guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="0bafe-105">Dette vil normalt ske ved en indkøbschef.</span><span class="sxs-lookup"><span data-stu-id="0bafe-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="0bafe-106">Du kan bruge denne procedure på USMF-demodatafirmaet eller dine egne data.</span><span class="sxs-lookup"><span data-stu-id="0bafe-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="0bafe-107">Du skal have oprettet købsaftaleklassifikationer, før du starter.</span><span class="sxs-lookup"><span data-stu-id="0bafe-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="0bafe-108">Når du har oprettet en aftale, du kan bruge den, når du opretter en Indkøbsordre, og denne handling kopierer køb aftale betingelserne til hovedet og linjer i ordren, der berøres af aftalen.</span><span class="sxs-lookup"><span data-stu-id="0bafe-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="0bafe-109">Opret en ny købsaftale</span><span class="sxs-lookup"><span data-stu-id="0bafe-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="0bafe-110">Gå til Indkøb og forsyning > Købsaftaler > Købsaftaler.</span><span class="sxs-lookup"><span data-stu-id="0bafe-110">Go to Procurement and sourcing > Purchase agreements > Purchase agreements.</span></span>
2. <span data-ttu-id="0bafe-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0bafe-111">Click New.</span></span>
3. <span data-ttu-id="0bafe-112">Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="0bafe-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0bafe-113">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="0bafe-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="0bafe-114">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0bafe-114">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="0bafe-115">Klik på rullelisten i feltet Købsaftaleklassifikation for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="0bafe-115">In the Purchase agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0bafe-116">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="0bafe-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="0bafe-117">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0bafe-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0bafe-118">Udvid sektionen Generelt.</span><span class="sxs-lookup"><span data-stu-id="0bafe-118">Expand the General section.</span></span>
10. <span data-ttu-id="0bafe-119">Indtast en dato i feltet Udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="0bafe-119">In the Expiration date field, enter a date.</span></span>
    * <span data-ttu-id="0bafe-120">Denne udløbsdato er standard for alle tilsagnslinjer og bestemmer, hvor længe hvert specifikt tilsagn er gyldigt.</span><span class="sxs-lookup"><span data-stu-id="0bafe-120">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  
11. <span data-ttu-id="0bafe-121">Indtast et navn for købsaftalen i feltet Dokumenttitel.</span><span class="sxs-lookup"><span data-stu-id="0bafe-121">In the Document title field, type a name for your purchase agreement.</span></span>
    * <span data-ttu-id="0bafe-122">Lad feltet Standardtilsagn være angivet til Bundet produktantal (eller ændr det, hvis det er ikke er angivet til dette).</span><span class="sxs-lookup"><span data-stu-id="0bafe-122">Leave the Default commitment field set to Product quantity commitment (or change it if it’s not set to this).</span></span>  
    * <span data-ttu-id="0bafe-123">Værdien for standardtilsagnet angiver dine indstillinger på aftalelinjerne.</span><span class="sxs-lookup"><span data-stu-id="0bafe-123">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="0bafe-124">Hvis du har brug for en ny tilsagnstype, når du opretter aftalelinjer, skal du ændre standardtilsagnet i overskriften.</span><span class="sxs-lookup"><span data-stu-id="0bafe-124">If you need a new commitment type when you’re creating the agreement lines, you need to change the default commitment on the header.</span></span>  <span data-ttu-id="0bafe-125">Der er 4 typer tilsagn: Bundet produktantal – for en bestemt mængde af et produkt, Værditilsagn om produkt – for et bestemt valutabeløb af et produkt, Værditilsagn om produktkategori – for et bestemt valutabeløb i en indkøbskategori, hvor beløbet kan være for en katalogvare eller en vare uden for kataloget, Værditilsagn – for et bestemt valutabeløb, som kan opfyldes ved et produkt eller en indkøbskategori.</span><span class="sxs-lookup"><span data-stu-id="0bafe-125">There are 4 types of commitments: Product quantity commitment - for a specific quantity of a product; Product value commitment - for a specific currency amount of a product; Product category value commitment - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; Value commitment - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  
12. <span data-ttu-id="0bafe-126">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0bafe-126">Click OK.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="0bafe-127">Tilføj et tilsagn</span><span class="sxs-lookup"><span data-stu-id="0bafe-127">Add a commitment</span></span>
1. <span data-ttu-id="0bafe-128">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="0bafe-128">Click Add line.</span></span>
2. <span data-ttu-id="0bafe-129">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0bafe-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="0bafe-130">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="0bafe-130">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0bafe-131">Vælg det produkt, du vil føje et tilsagn til.</span><span class="sxs-lookup"><span data-stu-id="0bafe-131">Select the product you want to add a commitment for.</span></span>
5. <span data-ttu-id="0bafe-132">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0bafe-132">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="0bafe-133">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="0bafe-133">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="0bafe-134">Dette er den samlede mængde, som du har aftalt at købe fra din kreditor.</span><span class="sxs-lookup"><span data-stu-id="0bafe-134">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
7. <span data-ttu-id="0bafe-135">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="0bafe-135">In the Unit price field, enter a number.</span></span>
8. <span data-ttu-id="0bafe-136">Vis eller skjul sektionen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="0bafe-136">Expand the Line details section.</span></span>
9. <span data-ttu-id="0bafe-137">Sæt indstillingen Maks. gennemtvinges til Ja.</span><span class="sxs-lookup"><span data-stu-id="0bafe-137">Set the Max is enforced option to Yes.</span></span>
    * <span data-ttu-id="0bafe-138">Maksimale gennemtvinges indstilling begrænser brugen af forpligtelsen.</span><span class="sxs-lookup"><span data-stu-id="0bafe-138">The Max is enforced option limits the use of the commitment.</span></span> <span data-ttu-id="0bafe-139">Du kan kun købe op til det antal, der er angivet i feltet Antal for linjen.</span><span class="sxs-lookup"><span data-stu-id="0bafe-139">You can only purchase up to the quantity that's specified in the Quantity field for the line.</span></span>  
10. <span data-ttu-id="0bafe-140">Skjul sektionen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="0bafe-140">Collapse the Line details section.</span></span>

## <a name="add-header-conditions"></a><span data-ttu-id="0bafe-141">Tilføj hovedbetingelser</span><span class="sxs-lookup"><span data-stu-id="0bafe-141">Add header conditions</span></span>
1. <span data-ttu-id="0bafe-142">Klik på Indstillinger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0bafe-142">On the Action Pane, click Options.</span></span>
2. <span data-ttu-id="0bafe-143">Klik på Skift visning.</span><span class="sxs-lookup"><span data-stu-id="0bafe-143">Click Change view.</span></span>
3. <span data-ttu-id="0bafe-144">Klik på Overskriftsvisning.</span><span class="sxs-lookup"><span data-stu-id="0bafe-144">Click Header view.</span></span>
4. <span data-ttu-id="0bafe-145">Udvid afsnittet Betingelser.</span><span class="sxs-lookup"><span data-stu-id="0bafe-145">Expand the Terms section.</span></span>
5. <span data-ttu-id="0bafe-146">Klik på rullelisten i feltet Betalingsmåde for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="0bafe-146">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0bafe-147">Betalingsbetingelserne fra kreditorkontoen vises her som standard.</span><span class="sxs-lookup"><span data-stu-id="0bafe-147">The payment terms from the vendor account are shown here by default.</span></span>       
6. <span data-ttu-id="0bafe-148">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="0bafe-148">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="0bafe-149">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0bafe-149">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="0bafe-150">Klik på rullelisten i feltet Leveringsmåde for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="0bafe-150">In the Mode of delivery field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="0bafe-151">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0bafe-151">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="0bafe-152">Klik på rullelisten i feltet Leveringsbetingelse for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="0bafe-152">In the Delivery terms field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="0bafe-153">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0bafe-153">In the list, click the link in the selected row.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="0bafe-154">Bekræft og aktivér aftalen</span><span class="sxs-lookup"><span data-stu-id="0bafe-154">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="0bafe-155">Klik på Købsaftale i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0bafe-155">On the Action Pane, click Purchase agreement.</span></span>
2. <span data-ttu-id="0bafe-156">Klik på Bekræftelse.</span><span class="sxs-lookup"><span data-stu-id="0bafe-156">Click Confirmation.</span></span>
    * <span data-ttu-id="0bafe-157">Angiv indstillingen Markér aftale som gældende til Ja.</span><span class="sxs-lookup"><span data-stu-id="0bafe-157">Set the Mark agreement as effective option to Yes.</span></span>  
3. <span data-ttu-id="0bafe-158">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0bafe-158">Click OK.</span></span>
4. <span data-ttu-id="0bafe-159">Klik på Købsaftale i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0bafe-159">On the Action Pane, click Purchase agreement.</span></span>
5. <span data-ttu-id="0bafe-160">Klik på Bekræftelser af købsaftale.</span><span class="sxs-lookup"><span data-stu-id="0bafe-160">Click Purchase agreement confirmations.</span></span>
    * <span data-ttu-id="0bafe-161">Med indstillingen Vis/udskriv kan du oprette et dokument for købsaftalen, som du kan udskrive eller sende til kreditoren.</span><span class="sxs-lookup"><span data-stu-id="0bafe-161">The Preview/Print option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="0bafe-162">Hvis du opdaterer aftalen senere og bekræfter den igen, vises begge versioner her.</span><span class="sxs-lookup"><span data-stu-id="0bafe-162">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="0bafe-163">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0bafe-163">Close the page.</span></span>


