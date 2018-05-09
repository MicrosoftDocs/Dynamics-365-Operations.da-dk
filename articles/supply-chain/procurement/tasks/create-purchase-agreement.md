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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f060346308e7ee1191d0769664648cfe72c22b21
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="6779a-103">Oprette en købsaftale</span><span class="sxs-lookup"><span data-stu-id="6779a-103">Create a purchase agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6779a-104">Denne procedure føres du gennem oprettelsen af en købsaftale.</span><span class="sxs-lookup"><span data-stu-id="6779a-104">This procedure guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="6779a-105">Dette vil normalt ske ved en indkøbschef.</span><span class="sxs-lookup"><span data-stu-id="6779a-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="6779a-106">Du kan bruge denne procedure på USMF-demodatafirmaet eller dine egne data.</span><span class="sxs-lookup"><span data-stu-id="6779a-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="6779a-107">Du skal have oprettet købsaftaleklassifikationer, før du starter.</span><span class="sxs-lookup"><span data-stu-id="6779a-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="6779a-108">Når du har oprettet en aftale, du kan bruge den, når du opretter en Indkøbsordre, og denne handling kopierer køb aftale betingelserne til hovedet og linjer i ordren, der berøres af aftalen.</span><span class="sxs-lookup"><span data-stu-id="6779a-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="6779a-109">Opret en ny købsaftale</span><span class="sxs-lookup"><span data-stu-id="6779a-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="6779a-110">Gå til Indkøb og forsyning > Købsaftaler > Købsaftaler.</span><span class="sxs-lookup"><span data-stu-id="6779a-110">Go to Procurement and sourcing > Purchase agreements > Purchase agreements.</span></span>
2. <span data-ttu-id="6779a-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6779a-111">Click New.</span></span>
3. <span data-ttu-id="6779a-112">Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="6779a-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6779a-113">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6779a-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="6779a-114">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6779a-114">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="6779a-115">Klik på rullelisten i feltet Købsaftaleklassifikation for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="6779a-115">In the Purchase agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="6779a-116">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6779a-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="6779a-117">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6779a-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="6779a-118">Udvid sektionen Generelt.</span><span class="sxs-lookup"><span data-stu-id="6779a-118">Expand the General section.</span></span>
10. <span data-ttu-id="6779a-119">Indtast en dato i feltet Udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="6779a-119">In the Expiration date field, enter a date.</span></span>
    * <span data-ttu-id="6779a-120">Denne udløbsdato er standard for alle tilsagnslinjer og bestemmer, hvor længe hvert specifikt tilsagn er gyldigt.</span><span class="sxs-lookup"><span data-stu-id="6779a-120">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  
11. <span data-ttu-id="6779a-121">Indtast et navn for købsaftalen i feltet Dokumenttitel.</span><span class="sxs-lookup"><span data-stu-id="6779a-121">In the Document title field, type a name for your purchase agreement.</span></span>
    * <span data-ttu-id="6779a-122">Lad feltet Standardtilsagn være angivet til Bundet produktantal (eller ændr det, hvis det er ikke er angivet til dette).</span><span class="sxs-lookup"><span data-stu-id="6779a-122">Leave the Default commitment field set to Product quantity commitment (or change it if it’s not set to this).</span></span>  
    * <span data-ttu-id="6779a-123">Værdien for standardtilsagnet angiver dine indstillinger på aftalelinjerne.</span><span class="sxs-lookup"><span data-stu-id="6779a-123">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="6779a-124">Hvis du har brug for en ny tilsagnstype, når du opretter aftalelinjer, skal du ændre standardtilsagnet i overskriften.</span><span class="sxs-lookup"><span data-stu-id="6779a-124">If you need a new commitment type when you’re creating the agreement lines, you need to change the default commitment on the header.</span></span>  <span data-ttu-id="6779a-125">Der er 4 typer tilsagn: Bundet produktantal – for en bestemt mængde af et produkt, Værditilsagn om produkt – for et bestemt valutabeløb af et produkt, Værditilsagn om produktkategori – for et bestemt valutabeløb i en indkøbskategori, hvor beløbet kan være for en katalogvare eller en vare uden for kataloget, Værditilsagn – for et bestemt valutabeløb, som kan opfyldes ved et produkt eller en indkøbskategori.</span><span class="sxs-lookup"><span data-stu-id="6779a-125">There are 4 types of commitments: Product quantity commitment - for a specific quantity of a product; Product value commitment - for a specific currency amount of a product; Product category value commitment - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; Value commitment - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  
12. <span data-ttu-id="6779a-126">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6779a-126">Click OK.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="6779a-127">Tilføj et tilsagn</span><span class="sxs-lookup"><span data-stu-id="6779a-127">Add a commitment</span></span>
1. <span data-ttu-id="6779a-128">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="6779a-128">Click Add line.</span></span>
2. <span data-ttu-id="6779a-129">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6779a-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="6779a-130">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="6779a-130">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6779a-131">Vælg det produkt, du vil føje et tilsagn til.</span><span class="sxs-lookup"><span data-stu-id="6779a-131">Select the product you want to add a commitment for.</span></span>
5. <span data-ttu-id="6779a-132">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6779a-132">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="6779a-133">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="6779a-133">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="6779a-134">Dette er den samlede mængde, som du har aftalt at købe fra din kreditor.</span><span class="sxs-lookup"><span data-stu-id="6779a-134">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
7. <span data-ttu-id="6779a-135">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="6779a-135">In the Unit price field, enter a number.</span></span>
8. <span data-ttu-id="6779a-136">Vis eller skjul sektionen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="6779a-136">Expand the Line details section.</span></span>
9. <span data-ttu-id="6779a-137">Sæt indstillingen Maks. gennemtvinges til Ja.</span><span class="sxs-lookup"><span data-stu-id="6779a-137">Set the Max is enforced option to Yes.</span></span>
    * <span data-ttu-id="6779a-138">Maksimale gennemtvinges indstilling begrænser brugen af forpligtelsen.</span><span class="sxs-lookup"><span data-stu-id="6779a-138">The Max is enforced option limits the use of the commitment.</span></span> <span data-ttu-id="6779a-139">Du kan kun købe op til det antal, der er angivet i feltet Antal for linjen.</span><span class="sxs-lookup"><span data-stu-id="6779a-139">You can only purchase up to the quantity that's specified in the Quantity field for the line.</span></span>  
10. <span data-ttu-id="6779a-140">Skjul sektionen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="6779a-140">Collapse the Line details section.</span></span>

## <a name="add-header-conditions"></a><span data-ttu-id="6779a-141">Tilføj hovedbetingelser</span><span class="sxs-lookup"><span data-stu-id="6779a-141">Add header conditions</span></span>
1. <span data-ttu-id="6779a-142">Klik på Indstillinger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6779a-142">On the Action Pane, click Options.</span></span>
2. <span data-ttu-id="6779a-143">Klik på Skift visning.</span><span class="sxs-lookup"><span data-stu-id="6779a-143">Click Change view.</span></span>
3. <span data-ttu-id="6779a-144">Klik på Overskriftsvisning.</span><span class="sxs-lookup"><span data-stu-id="6779a-144">Click Header view.</span></span>
4. <span data-ttu-id="6779a-145">Udvid afsnittet Betingelser.</span><span class="sxs-lookup"><span data-stu-id="6779a-145">Expand the Terms section.</span></span>
5. <span data-ttu-id="6779a-146">Klik på rullelisten i feltet Betalingsmåde for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="6779a-146">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6779a-147">Betalingsbetingelserne fra kreditorkontoen vises her som standard.</span><span class="sxs-lookup"><span data-stu-id="6779a-147">The payment terms from the vendor account are shown here by default.</span></span>       
6. <span data-ttu-id="6779a-148">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6779a-148">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="6779a-149">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6779a-149">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="6779a-150">Klik på rullelisten i feltet Leveringsmåde for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="6779a-150">In the Mode of delivery field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="6779a-151">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6779a-151">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="6779a-152">Klik på rullelisten i feltet Leveringsbetingelse for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="6779a-152">In the Delivery terms field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="6779a-153">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6779a-153">In the list, click the link in the selected row.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="6779a-154">Bekræft og aktivér aftalen</span><span class="sxs-lookup"><span data-stu-id="6779a-154">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="6779a-155">Klik på Købsaftale i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6779a-155">On the Action Pane, click Purchase agreement.</span></span>
2. <span data-ttu-id="6779a-156">Klik på Bekræftelse.</span><span class="sxs-lookup"><span data-stu-id="6779a-156">Click Confirmation.</span></span>
    * <span data-ttu-id="6779a-157">Angiv indstillingen Markér aftale som gældende til Ja.</span><span class="sxs-lookup"><span data-stu-id="6779a-157">Set the Mark agreement as effective option to Yes.</span></span>  
3. <span data-ttu-id="6779a-158">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6779a-158">Click OK.</span></span>
4. <span data-ttu-id="6779a-159">Klik på Købsaftale i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6779a-159">On the Action Pane, click Purchase agreement.</span></span>
5. <span data-ttu-id="6779a-160">Klik på Bekræftelser af købsaftale.</span><span class="sxs-lookup"><span data-stu-id="6779a-160">Click Purchase agreement confirmations.</span></span>
    * <span data-ttu-id="6779a-161">Med indstillingen Vis/udskriv kan du oprette et dokument for købsaftalen, som du kan udskrive eller sende til kreditoren.</span><span class="sxs-lookup"><span data-stu-id="6779a-161">The Preview/Print option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="6779a-162">Hvis du opdaterer aftalen senere og bekræfter den igen, vises begge versioner her.</span><span class="sxs-lookup"><span data-stu-id="6779a-162">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="6779a-163">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6779a-163">Close the page.</span></span>


