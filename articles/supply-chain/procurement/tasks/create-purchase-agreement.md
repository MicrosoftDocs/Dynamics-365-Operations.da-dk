---
title: Oprette en købsaftale
description: Dette emne fører dig gennem oprettelsen af en købsaftale.
author: RichardLuan
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92c9b429a05a2c25672cc14a0c9ee7adfef42631
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016825"
---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="fa614-103">Oprette en købsaftale</span><span class="sxs-lookup"><span data-stu-id="fa614-103">Create a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fa614-104">Dette emne fører dig gennem oprettelsen af en købsaftale.</span><span class="sxs-lookup"><span data-stu-id="fa614-104">This topic guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="fa614-105">Dette vil normalt ske ved en indkøbschef.</span><span class="sxs-lookup"><span data-stu-id="fa614-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="fa614-106">Du kan bruge denne procedure på USMF-demodatafirmaet eller dine egne data.</span><span class="sxs-lookup"><span data-stu-id="fa614-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="fa614-107">Du skal have oprettet købsaftaleklassifikationer, før du starter.</span><span class="sxs-lookup"><span data-stu-id="fa614-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="fa614-108">Når du har oprettet en aftale, du kan bruge den, når du opretter en Indkøbsordre, og denne handling kopierer køb aftale betingelserne til hovedet og linjer i ordren, der berøres af aftalen.</span><span class="sxs-lookup"><span data-stu-id="fa614-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="fa614-109">Opret en ny købsaftale</span><span class="sxs-lookup"><span data-stu-id="fa614-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="fa614-110">Gå til **Navigationsruden > Moduler > Indkøb og forsyning > Købsaftaler > Købsaftaler**.</span><span class="sxs-lookup"><span data-stu-id="fa614-110">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase agreements > Purchase agreements**.</span></span>
2. <span data-ttu-id="fa614-111">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="fa614-111">Click **New**.</span></span>
3. <span data-ttu-id="fa614-112">Vælg rækken med den ønskede post fra rullemenuen i feltet **Kreditorkonto**.</span><span class="sxs-lookup"><span data-stu-id="fa614-112">In the **Vendor account** field, select the drop-down menu and select the row of the desired record.</span></span>
4. <span data-ttu-id="fa614-113">Vælg rækken med den ønskede post fra rullemenuen i feltet **Købsaftaleklassifikation**.</span><span class="sxs-lookup"><span data-stu-id="fa614-113">In the **Purchase agreement classification** field, select the drop-down menu and select the row of the desired record.</span></span>
5. <span data-ttu-id="fa614-114">Udvid oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="fa614-114">Expand the **General** FastTab.</span></span>
6. <span data-ttu-id="fa614-115">Indtast en dato i feltet **Udløbsdato**.</span><span class="sxs-lookup"><span data-stu-id="fa614-115">In the **Expiration date** field, enter a date.</span></span>

    - <span data-ttu-id="fa614-116">Denne udløbsdato er standard for alle tilsagnslinjer og bestemmer, hvor længe hvert specifikt tilsagn er gyldigt.</span><span class="sxs-lookup"><span data-stu-id="fa614-116">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  

7. <span data-ttu-id="fa614-117">Indtast et navn for købsaftalen i feltet **Dokumenttitel**.</span><span class="sxs-lookup"><span data-stu-id="fa614-117">In the **Document title** field, type a name for your purchase agreement.</span></span>

    - <span data-ttu-id="fa614-118">Lad feltet **Standardtilsagn** være angivet til **Bundet produktantal** (eller ret det, hvis det ikke er angivet til dette).</span><span class="sxs-lookup"><span data-stu-id="fa614-118">Leave the **Default commitment** field set to **Product quantity commitment** (or change it if it's not set to this).</span></span>  
    - <span data-ttu-id="fa614-119">Værdien for standardtilsagnet angiver dine indstillinger på aftalelinjerne.</span><span class="sxs-lookup"><span data-stu-id="fa614-119">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="fa614-120">Hvis du har brug for en ny tilsagnstype, når du opretter aftalelinjer, skal du ændre standardtilsagnet i overskriften.</span><span class="sxs-lookup"><span data-stu-id="fa614-120">If you need a new commitment type when you're creating the agreement lines, you need to change the default commitment on the header.</span></span> <span data-ttu-id="fa614-121">Der er 4 typer tilsagn: **Bundet produktantal** – for en bestemt mængde af et produkt, **Værditilsagn om produkt** – for et bestemt valutabeløb af et produkt, **Værditilsagn om produktkategori** – for et bestemt valutabeløb i en indkøbskategori, hvor beløbet kan være for en katalogvare eller en vare uden for kataloget, **Værditilsagn** – for et bestemt valutabeløb, som kan opfyldes af et produkt eller en indkøbskategori.</span><span class="sxs-lookup"><span data-stu-id="fa614-121">There are 4 types of commitments: **Product quantity commitment** - for a specific quantity of a product; **Product value commitment** - for a specific currency amount of a product; **Product category value commitment** - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; **Value commitment** - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  

8. <span data-ttu-id="fa614-122">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fa614-122">Select **OK**.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="fa614-123">Tilføj et tilsagn</span><span class="sxs-lookup"><span data-stu-id="fa614-123">Add a commitment</span></span>
1. <span data-ttu-id="fa614-124">Vælg **Tilføj linje**.</span><span class="sxs-lookup"><span data-stu-id="fa614-124">Select **Add line**.</span></span>
2. <span data-ttu-id="fa614-125">Vælg den ønskede post på rullemenuen i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="fa614-125">In the **Item number** field, select the desired record from the drop-down menu.</span></span>
3. <span data-ttu-id="fa614-126">Angiv et tal i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="fa614-126">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="fa614-127">Dette er den samlede mængde, som du har aftalt at købe fra din kreditor.</span><span class="sxs-lookup"><span data-stu-id="fa614-127">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
4. <span data-ttu-id="fa614-128">Angiv et tal i feltet **Enhedspris**.</span><span class="sxs-lookup"><span data-stu-id="fa614-128">In the **Unit price** field, enter a number.</span></span>
5. <span data-ttu-id="fa614-129">Vis eller skjul sektionen **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="fa614-129">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="fa614-130">Sæt indstillingen **Maks. gennemtvinges** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fa614-130">Set the **Max is enforced** option to **Yes**.</span></span> <span data-ttu-id="fa614-131">Indstillingen **Maks. gennemtvinges** begrænser brugen af forpligtelsen.</span><span class="sxs-lookup"><span data-stu-id="fa614-131">The **Max is enforced** option limits the use of the commitment.</span></span> <span data-ttu-id="fa614-132">Du kan kun købe op til det antal, der er angivet i feltet **Antal** for linjen.</span><span class="sxs-lookup"><span data-stu-id="fa614-132">You can only purchase up to the quantity that's specified in the **Quantity** field for the line.</span></span>  

## <a name="add-header-conditions"></a><span data-ttu-id="fa614-133">Tilføj hovedbetingelser</span><span class="sxs-lookup"><span data-stu-id="fa614-133">Add header conditions</span></span>
1. <span data-ttu-id="fa614-134">Vælg **Indstillinger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="fa614-134">On the Action Pane, select **Options**.</span></span>
2. <span data-ttu-id="fa614-135">Vælg **Skift visning**.</span><span class="sxs-lookup"><span data-stu-id="fa614-135">Select **Change view**.</span></span>
3. <span data-ttu-id="fa614-136">Vælg **Overskriftsvisning**.</span><span class="sxs-lookup"><span data-stu-id="fa614-136">Select **Header view**.</span></span>
4. <span data-ttu-id="fa614-137">Udvid afsnittet **Betingelser**.</span><span class="sxs-lookup"><span data-stu-id="fa614-137">Expand the **Terms** section.</span></span>
5. <span data-ttu-id="fa614-138">I feltet **Betalingsmåde** skal du vælge den ønskede post i rullemenuen.</span><span class="sxs-lookup"><span data-stu-id="fa614-138">In the **Method of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="fa614-139">Betalingsbetingelserne fra kreditorkontoen vises her som standard.</span><span class="sxs-lookup"><span data-stu-id="fa614-139">The payment terms from the vendor account are shown here by default.</span></span>  
6. <span data-ttu-id="fa614-140">I feltet **Leveringsmåde** skal du vælge den ønskede post i rullemenuen.</span><span class="sxs-lookup"><span data-stu-id="fa614-140">In the **Mode of delivery** field, select the desired record in the drop-down menu.</span></span>
7. <span data-ttu-id="fa614-141">Vælg rullelisten i feltet **Leveringsbetingelse** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="fa614-141">In the **Delivery terms** field, select the drop-down button to open the lookup.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="fa614-142">Bekræft og aktivér aftalen</span><span class="sxs-lookup"><span data-stu-id="fa614-142">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="fa614-143">Klik på **Købsaftale** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="fa614-143">On the Action Pane, select **Purchase agreement**.</span></span>
2. <span data-ttu-id="fa614-144">Vælg **Bekræftelse**.</span><span class="sxs-lookup"><span data-stu-id="fa614-144">Select **Confirmation**.</span></span> <span data-ttu-id="fa614-145">Angiv indstillingen **Markér aftale som gældende** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fa614-145">Set the **Mark agreement as effective** option to **Yes**.</span></span>  
3. <span data-ttu-id="fa614-146">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fa614-146">Select **OK**.</span></span>
4. <span data-ttu-id="fa614-147">Klik på **Købsaftale** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="fa614-147">On the Action Pane, select **Purchase agreement**.</span></span>
5. <span data-ttu-id="fa614-148">Vælg **Bekræftelser af købsaftaler**.</span><span class="sxs-lookup"><span data-stu-id="fa614-148">Select **Purchase agreement confirmations**.</span></span> <span data-ttu-id="fa614-149">Med indstillingen **Vis/udskriv** kan du oprette et dokument for købsaftalen, som du kan udskrive eller sende til kreditoren.</span><span class="sxs-lookup"><span data-stu-id="fa614-149">The **Preview/Print** option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="fa614-150">Hvis du opdaterer aftalen senere og bekræfter den igen, vises begge versioner her.</span><span class="sxs-lookup"><span data-stu-id="fa614-150">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="fa614-151">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="fa614-151">Close the page.</span></span>

