---
title: Konfigurere et menupunkt på en mobilenhed til at udføre arbejde af typen indkøbsordre
description: Denne fremgangsmåde viser, hvordan du konfigurerer et menupunkt for en mobilenhed.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 707fc9c798da8eac30cc9f56c158be3d96b271d6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847105"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a><span data-ttu-id="e31fc-103">Konfigurere et menupunkt på en mobilenhed til at udføre arbejde af typen indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="e31fc-103">Set up a mobile device menu item for completing work of type Purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e31fc-104">Denne fremgangsmåde viser, hvordan du konfigurerer et menupunkt for en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="e31fc-104">This procedure shows how to set up a Mobile device menu item.</span></span> <span data-ttu-id="e31fc-105">I dette eksempel bruges menupunktet til at udføre arbejde af typen Indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="e31fc-105">In this example, the menu item is used for performing work of type Purchase order.</span></span> <span data-ttu-id="e31fc-106">Det arbejde, der er gyldigt, bestemmes af den arbejdsklasse, der er knyttet til menupunktet.</span><span class="sxs-lookup"><span data-stu-id="e31fc-106">The work class that’s associated with the menu item determines which work is valid.</span></span> <span data-ttu-id="e31fc-107">Du kan bruge denne guide i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="e31fc-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="e31fc-108">Denne procedure udføres typisk af en lagerstedschef.</span><span class="sxs-lookup"><span data-stu-id="e31fc-108">This procedure is typically carried out by a warehouse manager.</span></span>


## <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="e31fc-109">Oprette et menupunkt på en mobilenhed</span><span class="sxs-lookup"><span data-stu-id="e31fc-109">Create a mobile device menu item</span></span>
1. <span data-ttu-id="e31fc-110">Gå til menupunkter i mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="e31fc-110">Go to Mobile device menu items.</span></span>
2. <span data-ttu-id="e31fc-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e31fc-111">Click New.</span></span>
3. <span data-ttu-id="e31fc-112">Skriv en værdi i feltet Menupunktnavn.</span><span class="sxs-lookup"><span data-stu-id="e31fc-112">In the Menu item name field, type a value.</span></span>
    * <span data-ttu-id="e31fc-113">Angiv en entydig værdi.</span><span class="sxs-lookup"><span data-stu-id="e31fc-113">Enter a unique value.</span></span> <span data-ttu-id="e31fc-114">Du kan for eksempel skrive POMove.</span><span class="sxs-lookup"><span data-stu-id="e31fc-114">For example, you could type POMove.</span></span> <span data-ttu-id="e31fc-115">Husk værdien, du skal bruge den senere.</span><span class="sxs-lookup"><span data-stu-id="e31fc-115">Remember the value, you'll need it later.</span></span>  
4. <span data-ttu-id="e31fc-116">Skriv en værdi i feltet Titel.</span><span class="sxs-lookup"><span data-stu-id="e31fc-116">In the Title field, type a value.</span></span>
    * <span data-ttu-id="e31fc-117">Dette er den titel, der vises på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="e31fc-117">This is the title which will be displayed on the mobile device.</span></span> <span data-ttu-id="e31fc-118">Du kan for eksempel skrive PO Move.</span><span class="sxs-lookup"><span data-stu-id="e31fc-118">For example, you could type PO Move.</span></span>  
5. <span data-ttu-id="e31fc-119">Vælg "Arbejde" i feltet Tilstand.</span><span class="sxs-lookup"><span data-stu-id="e31fc-119">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="e31fc-120">Vælg Ja i feltet Brug eksisterende arbejde.</span><span class="sxs-lookup"><span data-stu-id="e31fc-120">Select Yes in the Use existing work field.</span></span>
    * <span data-ttu-id="e31fc-121">Dette menupunkt på mobilenheden bruges til at udføre eksisterende arbejde.</span><span class="sxs-lookup"><span data-stu-id="e31fc-121">This mobile device menu item is used to perform existing work.</span></span> <span data-ttu-id="e31fc-122">Derfor skal du indstille værdien til Ja.</span><span class="sxs-lookup"><span data-stu-id="e31fc-122">Therefore you must set this value to Yes.</span></span>  
    * <span data-ttu-id="e31fc-123">Feltet Vis lagerstatus bestemmer, om lagerstatus for den disponible lagerbeholdning vises for lagermedarbejderen på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="e31fc-123">The Display inventory status field determines whether the inventory status of the on-hand inventory will be displayed to the warehouse worker on the mobile device.</span></span>  
7. <span data-ttu-id="e31fc-124">Vælg "Systemgruppering" i feltet Ledet af.</span><span class="sxs-lookup"><span data-stu-id="e31fc-124">In the Directed by field, select 'System grouping'.</span></span>
    * <span data-ttu-id="e31fc-125">Når du markerer noget i feltet Ledet af, vises der flere felter i sektionen Generelt på denne side.</span><span class="sxs-lookup"><span data-stu-id="e31fc-125">When you select something in the Directed by field, additional fields appear in the General section on this page.</span></span> <span data-ttu-id="e31fc-126">De felter, der vises, afhænger af, hvad du har valgt.</span><span class="sxs-lookup"><span data-stu-id="e31fc-126">The fields that appear depend on what you selected.</span></span> <span data-ttu-id="e31fc-127">Når du vælger Systemgruppering, tilføjes der to nye felter.</span><span class="sxs-lookup"><span data-stu-id="e31fc-127">When you select System grouping, two new fields are added.</span></span> <span data-ttu-id="e31fc-128">De beskrives nedenfor.</span><span class="sxs-lookup"><span data-stu-id="e31fc-128">These are explained below.</span></span>  
8. <span data-ttu-id="e31fc-129">Vælg 'WorkPoolId' i feltet Systemgrupperingsfelt.</span><span class="sxs-lookup"><span data-stu-id="e31fc-129">In the System grouping field, select 'WorkPoolId'.</span></span>
    * <span data-ttu-id="e31fc-130">Når lagermedarbejderne åbner dette menupunkt, bliver de bedt om at scanne et arbejdspulje-id.</span><span class="sxs-lookup"><span data-stu-id="e31fc-130">When warehouse workers open this menu item, they’ll be asked to scan a Work pool ID.</span></span> <span data-ttu-id="e31fc-131">Alle arbejdsordrer med dette arbejdspulje-id og åbne arbejdsordrelinjer med en af arbejdsklasserne føjet til dette menupunkt bliver overført til brugeren.</span><span class="sxs-lookup"><span data-stu-id="e31fc-131">All work orders with this Work pool ID and open work order lines with one of the work classes added to this menu item will be pushed to the user.</span></span>  
9. <span data-ttu-id="e31fc-132">Skriv en værdi i feltet Systemgrupperingslabel.</span><span class="sxs-lookup"><span data-stu-id="e31fc-132">In the System grouping label field, type a value.</span></span>
    * <span data-ttu-id="e31fc-133">Dette er den tekst, der vises for brugeren på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="e31fc-133">This is the text displayed to the user on the mobile device.</span></span> <span data-ttu-id="e31fc-134">Du kan for eksempel skrive Arbejdspulje.</span><span class="sxs-lookup"><span data-stu-id="e31fc-134">For example, you could type Work pool.</span></span>  
10. <span data-ttu-id="e31fc-135">Vælg Ja i feltet Tilsidesæt nummerplade under læg på lager.</span><span class="sxs-lookup"><span data-stu-id="e31fc-135">Select Yes in the Override license plate during put field.</span></span>
    * <span data-ttu-id="e31fc-136">Denne indstilling gør det muligt for lagermedarbejderne at tilsidesætte målnummerplade, når varer anbringes på en nummerpladestyret lokalitet.</span><span class="sxs-lookup"><span data-stu-id="e31fc-136">This option allows warehouse workers to override the target license plate when items are put down on a license plate controlled location.</span></span>  
11. <span data-ttu-id="e31fc-137">Vælg Ja i feltet Gruppér vareplacering.</span><span class="sxs-lookup"><span data-stu-id="e31fc-137">Select Yes in the Group put away field.</span></span>
    * <span data-ttu-id="e31fc-138">Hvis alle læg på lager-linjerne i arbejdsordren deler den samme lokalitet, modtager brugeren en kombineret læg på lager-instruktion for alle linjer.</span><span class="sxs-lookup"><span data-stu-id="e31fc-138">If all the Put lines on the work order share the same location, the user will receive one combined Put instruction for all lines.</span></span>  
    * <span data-ttu-id="e31fc-139">Id for arbejdsrevisionsskabelon: En arbejdsskabelon gør det muligt at angive, at arbejdsprocessen for et menupunkt skal afbrydes, så en anden handling kan udføres.</span><span class="sxs-lookup"><span data-stu-id="e31fc-139">Audit template ID: A work audit template allows you to specify that the work process for a menu item should be interrupted so that another operation can be performed.</span></span> <span data-ttu-id="e31fc-140">Hvis dette menupunkt f.eks. er for indgående arbejde, kan revisionsskabelonen kræve, at arbejderen kontrollerer temperaturen.</span><span class="sxs-lookup"><span data-stu-id="e31fc-140">For example, if this menu item is for inbound work, the audit template might require that the worker checks the temperature.</span></span> <span data-ttu-id="e31fc-141">Det tidspunkt, hvor processen afbrydes, er angivet på revisionsskabelonen og kan f.eks. være, når arbejdet startes eller afsluttes, eller når status ændres.</span><span class="sxs-lookup"><span data-stu-id="e31fc-141">The point at which the process is interrupted is specified on the audit template and can be, for example, when work is started or completed, or when its status changes.</span></span>  
12. <span data-ttu-id="e31fc-142">Udvid sektionen Arbejdsklasser.</span><span class="sxs-lookup"><span data-stu-id="e31fc-142">Expand the Work classes section.</span></span>
13. <span data-ttu-id="e31fc-143">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e31fc-143">Click New.</span></span>
14. <span data-ttu-id="e31fc-144">Skriv "Køb" i feltet Arbejdsklasse-id.</span><span class="sxs-lookup"><span data-stu-id="e31fc-144">In the Work class ID field, type 'Purchase'.</span></span>
    * <span data-ttu-id="e31fc-145">Arbejdspuljen begrænser det arbejde, som menupunktet kan bruges til.</span><span class="sxs-lookup"><span data-stu-id="e31fc-145">The work pool restricts the work that the menu item can be used for.</span></span> <span data-ttu-id="e31fc-146">I dette tilfælde bruges den til åbne arbejdsordrelinjer, der har købets arbejdsklasse-id.</span><span class="sxs-lookup"><span data-stu-id="e31fc-146">In this case it will be used for open work order lines that have the Purchase work class ID.</span></span>  
15. <span data-ttu-id="e31fc-147">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e31fc-147">Click Save.</span></span>

## <a name="set-up-work-confirmation"></a><span data-ttu-id="e31fc-148">Konfigurer arbejdsbekræftelse</span><span class="sxs-lookup"><span data-stu-id="e31fc-148">Set up work confirmation</span></span>
1. <span data-ttu-id="e31fc-149">Klik på Konfiguration af arbejdsbekræftelse.</span><span class="sxs-lookup"><span data-stu-id="e31fc-149">Click Work confirmation setup.</span></span>
2. <span data-ttu-id="e31fc-150">Vælg "Pluk" i feltet Arbejdstype.</span><span class="sxs-lookup"><span data-stu-id="e31fc-150">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="e31fc-151">Marker afkrydsningsfeltet Bekræft automatisk.</span><span class="sxs-lookup"><span data-stu-id="e31fc-151">Select the Auto confirm check box.</span></span>
    * <span data-ttu-id="e31fc-152">Arbejdsinstruktionen med arbejdstypen Pluk bliver bekræftet automatisk.</span><span class="sxs-lookup"><span data-stu-id="e31fc-152">The work instruction with work type Pick will be auto-confirmed.</span></span> <span data-ttu-id="e31fc-153">Denne instruktion vises ikke for brugeren.</span><span class="sxs-lookup"><span data-stu-id="e31fc-153">This instruction will not be presented to the user.</span></span>  
4. <span data-ttu-id="e31fc-154">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e31fc-154">Click New.</span></span>
5. <span data-ttu-id="e31fc-155">Vælg 'Læg på lager' i feltet Arbejdstype.</span><span class="sxs-lookup"><span data-stu-id="e31fc-155">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="e31fc-156">Marker afkrydsningsfeltet Bekræftelse af lokation.</span><span class="sxs-lookup"><span data-stu-id="e31fc-156">Select the Location confirmation check box.</span></span>
    * <span data-ttu-id="e31fc-157">Lagermedarbejderen bliver bedt om at udføre en bekræftelsesscanning af lokaliteten, når varen anbringes.</span><span class="sxs-lookup"><span data-stu-id="e31fc-157">The warehouse worker will be asked to perform a confirmation scan of the location, when the item is put down.</span></span>  
7. <span data-ttu-id="e31fc-158">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e31fc-158">Click Save.</span></span>
8. <span data-ttu-id="e31fc-159">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e31fc-159">Close the page.</span></span>
9. <span data-ttu-id="e31fc-160">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e31fc-160">Close the page.</span></span>

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="e31fc-161">Føje menupunktet til en mobilenhedsmenu</span><span class="sxs-lookup"><span data-stu-id="e31fc-161">Add the menu item to a mobile device menu</span></span>
1. <span data-ttu-id="e31fc-162">Gå til menuen Mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="e31fc-162">Go to Mobile device menu.</span></span>
2. <span data-ttu-id="e31fc-163">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="e31fc-163">Click Edit.</span></span>
3. <span data-ttu-id="e31fc-164">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="e31fc-164">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e31fc-165">For eksempel kan du filtrere på feltet Navn med værdien 'indgående'.</span><span class="sxs-lookup"><span data-stu-id="e31fc-165">For example, filter on the Name field with a value of 'inbound'.</span></span>
    * <span data-ttu-id="e31fc-166">Du vil finde den menu, du bruger til indgående menupunkter.</span><span class="sxs-lookup"><span data-stu-id="e31fc-166">You want to find the menu you use for inbound menu items.</span></span> <span data-ttu-id="e31fc-167">I USMF kaldes dette felt Indgående.</span><span class="sxs-lookup"><span data-stu-id="e31fc-167">In USMF this is called Inbound.</span></span>  
4. <span data-ttu-id="e31fc-168">Vælg 'en værdi' i træet.</span><span class="sxs-lookup"><span data-stu-id="e31fc-168">In the tree, select 'a value'.</span></span>
5. <span data-ttu-id="e31fc-169">Klik på den pil, der peger mod højre.</span><span class="sxs-lookup"><span data-stu-id="e31fc-169">Click on the arrow that points to the right.</span></span>
6. <span data-ttu-id="e31fc-170">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e31fc-170">Click Save.</span></span>
7. <span data-ttu-id="e31fc-171">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e31fc-171">Close the page.</span></span>

