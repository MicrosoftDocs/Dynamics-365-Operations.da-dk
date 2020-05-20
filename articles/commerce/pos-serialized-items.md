---
title: Arbejde med serienummererede varer i POS
description: Dette emne forklarer, hvordan du kan håndtere serienummererede varer i POS-programmet.
author: boycezhu
manager: annbe
ms.date: 04/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 1e0d6aa7cd5576578378e70c6ee808833314aff3
ms.sourcegitcommit: 919620b4aca425e6a1248ee12f50a622d2531e58
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2020
ms.locfileid: "3290764"
---
# <a name="work-with-serialized-items-in-the-pos"></a><span data-ttu-id="94490-103">Arbejde med serienummererede varer i POS</span><span class="sxs-lookup"><span data-stu-id="94490-103">Work with serialized items in the POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="94490-104">Mange detailhandlere sælger produkter, der kræver en seriel kontrol.</span><span class="sxs-lookup"><span data-stu-id="94490-104">Many retailers sell products that require serial control.</span></span> <span data-ttu-id="94490-105">Disse varer kaldes *serienummererede varer*.</span><span class="sxs-lookup"><span data-stu-id="94490-105">These items are referred to as *serialized items*.</span></span> <span data-ttu-id="94490-106">Nogle detailhandlere kan få brug for at bevare serienumre til sporingsformål.</span><span class="sxs-lookup"><span data-stu-id="94490-106">Some retailers might want to maintain serial numbers for tracking purposes.</span></span> <span data-ttu-id="94490-107">Andre detailhandlere kan få brug for at registrere serienumre under salgsprocessen mht. service- og garantiformål.</span><span class="sxs-lookup"><span data-stu-id="94490-107">Other retailers might want to capture serial numbers during the sales process, for service and warranty purposes.</span></span> <span data-ttu-id="94490-108">Dette emne forklarer, hvordan du kan håndtere serienummererede varer i Microsoft Dynamics 365 Commerce POS-programmet.</span><span class="sxs-lookup"><span data-stu-id="94490-108">This topic explains how you can manage serialized items in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

## <a name="serial-number-configurations"></a><span data-ttu-id="94490-109">Serienummerkonfigurationer</span><span class="sxs-lookup"><span data-stu-id="94490-109">Serial number configurations</span></span>

<span data-ttu-id="94490-110">En vare betragtes som en serienummereret vare, hvis den er tildelt en sporingsdimensionsgruppe, der er konfigureret til at tillade serienumre.</span><span class="sxs-lookup"><span data-stu-id="94490-110">An item is considered a serialized item if it's assigned a tracking dimension group that is set up to allow for serial numbers.</span></span> <span data-ttu-id="94490-111">Vælg indstillingen **Aktiv** i Commerce Headquarters på siden **Sporingsdimensionsgrupper** for at aktivere serienumre for lagerprocessen.</span><span class="sxs-lookup"><span data-stu-id="94490-111">In Commerce headquarters, on the **Tracking dimension groups** page, select the **Active** option to enable serial numbers for the inventory process.</span></span> <span data-ttu-id="94490-112">Hvis du vil aktivere serienumre for salgsprocessen, skal du vælge indstillingen **Aktiv i salgsproces**.</span><span class="sxs-lookup"><span data-stu-id="94490-112">To enable serial numbers for the sales process, select the **Active in sales process** option.</span></span>

<span data-ttu-id="94490-113">Hvis indstillingen **Blank tilgang tilladt** er slået til på oversigtspanelet **Sporingsdimensioner**, er serienummeret et valgfrit input under lagertilgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="94490-113">On the **Tracking dimensions** FastTab, if the **Blank receipt allowed** option is turned on, the serial number is an optional input during the inventory receipt process.</span></span> <span data-ttu-id="94490-114">Hvis indstillingen er deaktiveret, er et serienummer påkrævet.</span><span class="sxs-lookup"><span data-stu-id="94490-114">If the option is turned off, the serial number is required.</span></span>

<span data-ttu-id="94490-115">Hvis indstillingen **Serienummerkontrol** er aktiveret på oversigtspanelet **Serienumre**, skal serienummeret være entydigt pr. enhed.</span><span class="sxs-lookup"><span data-stu-id="94490-115">On the **Serial numbers** FastTab, if the **Serial number control** option is turned on, the serial number must be unique per unit.</span></span> <span data-ttu-id="94490-116">Det vil sige, at duplikerede serienumre ikke er tilladt.</span><span class="sxs-lookup"><span data-stu-id="94490-116">In other words, duplicated serial numbers aren't allowed.</span></span>

## <a name="serialized-items-in-the-receiving-process"></a><span data-ttu-id="94490-117">Serienummererede varer i tilgangsprocessen</span><span class="sxs-lookup"><span data-stu-id="94490-117">Serialized items in the receiving process</span></span>

<span data-ttu-id="94490-118">Operationen **Indgående lager** i POS-programmet giver brugere mulighed for at udføre følgende opgaver for serienummererede varer:</span><span class="sxs-lookup"><span data-stu-id="94490-118">The **Inbound inventory** operation in the POS application lets users perform the following tasks for serialized items:</span></span>

- <span data-ttu-id="94490-119">Registrér serienumre i forhold til serienummererede varer, når disse varer modtages i butikken via en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="94490-119">Register serial numbers against serialized items when those items are received in the store via a purchase order.</span></span>
- <span data-ttu-id="94490-120">Valider serienumre, der er registreret på forhånd, i forhold til serienummererede varer, når disse varer modtages i butikken via en indkøbsordre eller flytteordre.</span><span class="sxs-lookup"><span data-stu-id="94490-120">Validate preregistered serial numbers against serialized items when those items are received in the store via a purchase order or transfer order.</span></span>

> [!NOTE]
> <span data-ttu-id="94490-121">Hvis du vil bruge operationen **Indgående lager** til at registrere eller validere en serienummereret vare, skal varen tildeles en sporingsdimensionsgruppe, der er konfigureret til at tillade serienumre for indstillingen **Aktiv** og ikke for indstillingen **Aktiv i salgsproces**.</span><span class="sxs-lookup"><span data-stu-id="94490-121">To use the **Inbound inventory** operation to register or validate a serialized item, the item must be assigned a tracking dimension group that is set up to allow for serial numbers for the **Active** option, not the **Active in sales process** option.</span></span>

<span data-ttu-id="94490-122">Du kan gå i gang med tilgangsprocessen ved at starte med at scanne varens stregkode eller ved at angive vare-id'et i visningen **Modtag nu** i operationen **Indgående lager**.</span><span class="sxs-lookup"><span data-stu-id="94490-122">To begin the receiving process, in the **Inbound inventory** operation, you can start in the **Receiving now** view by scanning the item bar code or entering the item ID.</span></span> <span data-ttu-id="94490-123">Du kan også starte i visningen **Fuld ordreliste** ved manuelt at vælge varen.</span><span class="sxs-lookup"><span data-stu-id="94490-123">Alternatively, you can start in the **Full order list** view by manually selecting the item.</span></span>

<span data-ttu-id="94490-124">Hvis den vare, der vælges eller modtages, er en serienummereret vare, indeholder ruden **Detaljer** for varen linket **Administrer serienummer**, der åbner siden **Administration af serienumre**.</span><span class="sxs-lookup"><span data-stu-id="94490-124">If the item that is being selected or received is a serialized item, the **Details** pane for the item contains a **Manage serial number** link that opens the **Serial number management** page.</span></span> <span data-ttu-id="94490-125">Du kan også åbne siden **Administration af serienumre** ved at vælge **Serienummer** på applinjen i visningen med ordredetaljer eller ved at vælge **Administrer serienummer** i den dialogboks, der vises under tilgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="94490-125">Alternatively, you can open the **Serial number management** page either by selecting **Serial number** on the app bar of the order details view or by selecting **Manage serial number** in the dialog box that prompts you during the receiving process.</span></span> <span data-ttu-id="94490-126">Siden **Administration af serienumre** viser alle åbne serienummerlinjer, der afventer registrering eller validering.</span><span class="sxs-lookup"><span data-stu-id="94490-126">The **Serial number management** page lists all open serial number lines that are pending registration or validation.</span></span> <span data-ttu-id="94490-127">Der kan være to faner på denne side: en for den aktuelle vare og en for alle de serienummererede varer i ordren.</span><span class="sxs-lookup"><span data-stu-id="94490-127">There might be two tabs on this page: one for the current item and one for all the serialized items in the order.</span></span>

<span data-ttu-id="94490-128">Feltet **Status** på siden **Administration af serienumre** indeholder oplysninger om den aktuelle status for hvert serienummer:</span><span class="sxs-lookup"><span data-stu-id="94490-128">The **Status** field on the **Serial number management** page provides information about the current stage that each serial number is in:</span></span>

- <span data-ttu-id="94490-129">**Ikke registreret** – serienummeret er ikke leveret, eller det allerede registrerede serienummer er endnu ikke valideret.</span><span class="sxs-lookup"><span data-stu-id="94490-129">**Not registered** – The serial number hasn't been provided, or the preregistered serial number hasn't yet been validated.</span></span>
- <span data-ttu-id="94490-130">**Registreret** – serienummeret er registreret og gemt lokalt i butikkens kanaldatabase, eller det allerede registrerede serienummer er blevet valideret.</span><span class="sxs-lookup"><span data-stu-id="94490-130">**Registering** – The serial number has been registered and saved locally to the store's channel database, or the preregistered serial number has been validated.</span></span> <span data-ttu-id="94490-131">Der sendes kun serienumre, der har status som **Registreret**, til Commerce Headquarters, når du er færdig med tilgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="94490-131">Only serial numbers that have a status of **Registering** will be submitted to Commerce headquarters when you finish receiving.</span></span>

### <a name="register-serial-numbers-against-serialized-items"></a><span data-ttu-id="94490-132">Registrere serienumre i forhold til serienummererede varer</span><span class="sxs-lookup"><span data-stu-id="94490-132">Register serial numbers against serialized items</span></span>

<span data-ttu-id="94490-133">I forbindelse med en indkøbsordre indeholder en dialogboks, der vises under tilgangsprocessen for en serienummereret vare, indstillingen **Administrer serienummer**.</span><span class="sxs-lookup"><span data-stu-id="94490-133">For a purchase order, a dialog box that prompts you during the receiving process of a serialized item offers the **Manage serial number** option.</span></span> <span data-ttu-id="94490-134">Du kan vælge denne indstilling for at åbne siden **Administration af serienumre** og begynde at registrere serienumre.</span><span class="sxs-lookup"><span data-stu-id="94490-134">You can select that option to open the **Serial number management** page and start to register serial numbers.</span></span> <span data-ttu-id="94490-135">Du kan også springe dette trin over under tilgangsprocessen og angive dette input senere, før tilgangen bogføres.</span><span class="sxs-lookup"><span data-stu-id="94490-135">You can also skip this step during the receiving process and provide the input later, before the receipt is posted.</span></span>

<span data-ttu-id="94490-136">Fanen for den aktuelle vare vises som standard.</span><span class="sxs-lookup"><span data-stu-id="94490-136">By default, the tab for the current item is shown.</span></span> <span data-ttu-id="94490-137">Alle serienummerlinjer har en tom serienummerværdi og statussen **Ikke registreret**.</span><span class="sxs-lookup"><span data-stu-id="94490-137">All serial number lines have an empty serial number value and a status of **Not registered**.</span></span> <span data-ttu-id="94490-138">Du kan scanne serienummerstregkoder, eller du kan vælge **Serienummer** på applinjen for at angive serienumre i dialogboksen flere gange.</span><span class="sxs-lookup"><span data-stu-id="94490-138">You can scan serial number bar codes, or you can select **Serial number** on the app bar to continuously enter serial numbers in the dialog box.</span></span> <span data-ttu-id="94490-139">De serienumre, du angiver, vises på listen, og statussen på serienummerlinjerne ændres til **Registreret**.</span><span class="sxs-lookup"><span data-stu-id="94490-139">The serial numbers that you enter appear in the list, and the status of the serial number lines is changed to **Registering**.</span></span> <span data-ttu-id="94490-140">Det maksimale antal serienumre, du kan registrere på listen, er lig med tilgangsantallet.</span><span class="sxs-lookup"><span data-stu-id="94490-140">The maximum number of serial numbers that you can register in the list equals the receiving quantity.</span></span> <span data-ttu-id="94490-141">Hvis du laver en fejl, kan du vælge **Rediger** eller **Ryd** i ruden **Detaljer** for at ændre de angivne serienumre.</span><span class="sxs-lookup"><span data-stu-id="94490-141">If you make a mistake, you can select **Edit** or **Clear** in the **Details** pane to make changes to the serial numbers that you entered.</span></span>

<span data-ttu-id="94490-142">Du kan også registrere serienumre på fanen **Alle serienummererede varer** på siden **Administration af serienumre**.</span><span class="sxs-lookup"><span data-stu-id="94490-142">You can also register serial numbers on the **All serialized items** tab of the **Serial number management** page.</span></span> <span data-ttu-id="94490-143">På listen skal du vælge den vare, du vil registrere serienumre for.</span><span class="sxs-lookup"><span data-stu-id="94490-143">In the list, select the item that you want to register serial numbers against.</span></span>

<span data-ttu-id="94490-144">Under serienummerregistreringen på denne side udføres der en duplikeringsvalidering.</span><span class="sxs-lookup"><span data-stu-id="94490-144">During serial number registration on this page, duplication validation occurs.</span></span> <span data-ttu-id="94490-145">Hvis du forsøger at angive et duplikeret serienummer for en vare, som serienummerkontrolelementet er aktiveret for, vises der en fejlmeddelelse, og du skal angive et andet nummer.</span><span class="sxs-lookup"><span data-stu-id="94490-145">If you try to enter a duplicated serial number against an item that serial number control is turned on for, you receive an error message and must provide a different number.</span></span>

### <a name="validate-serial-numbers-on-serialized-items"></a><span data-ttu-id="94490-146">Validere serienumre for serienummererede varer</span><span class="sxs-lookup"><span data-stu-id="94490-146">Validate serial numbers on serialized items</span></span>

<span data-ttu-id="94490-147">I forbindelse med en flytteordre skal den udgående side forudregistrere serienumre for de serienummerede varer under forsendelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="94490-147">For a transfer order, the outbound side must preregister serial numbers on the serialized items during the shipment process.</span></span> <span data-ttu-id="94490-148">For en indkøbsordre kan leverandøren levere serienummeroplysninger via en Advance Shipping Notice (ASN), og du kan forudregistrere numrene på de varer, der skal sendes.</span><span class="sxs-lookup"><span data-stu-id="94490-148">For a purchase order, the supplier might provide serial number information through an Advance Shipment Notice (ASN), and you can preregister the numbers on the items that will be shipped.</span></span> <span data-ttu-id="94490-149">I begge tilfælde kendes serienumrene før tilgangen.</span><span class="sxs-lookup"><span data-stu-id="94490-149">In both cases, the serial numbers are known before the receipt.</span></span> <span data-ttu-id="94490-150">På den indgående side skal du derfor blot validere, at du har modtaget det, du skulle modtage.</span><span class="sxs-lookup"><span data-stu-id="94490-150">Therefore, on the inbound side, you just have to validate that you received what you were supposed to receive.</span></span>

<span data-ttu-id="94490-151">Hvis du vil validere serienumre, kan du åbne siden **Administration af serienumre** under tilgangsprocessen eller når som helst, før tilgangen bogføres.</span><span class="sxs-lookup"><span data-stu-id="94490-151">To validate serial numbers, you can open the **Serial number management** page either during the receiving process or at any time before the receipt is posted.</span></span> <span data-ttu-id="94490-152">For hver serienummereret vare, der forudregistrerede serienumre, angives alle serienumre automatisk til den indledende status **Ikke registreret** på denne side.</span><span class="sxs-lookup"><span data-stu-id="94490-152">For each serialized item that has preregistered serial numbers, all the serial numbers are automatically set to an initial status of **Not registered** on this page.</span></span> <span data-ttu-id="94490-153">Hvis du vil validere serienumre, kan du scanne eller angive dem.</span><span class="sxs-lookup"><span data-stu-id="94490-153">To validate serial numbers, you can scan or enter them.</span></span> <span data-ttu-id="94490-154">Når serienumre angives, validerer programmet, om de stemmer overens med de forudregistrerede serienumre.</span><span class="sxs-lookup"><span data-stu-id="94490-154">As serial number are entered, the application validates whether they match preregistered serial numbers.</span></span> <span data-ttu-id="94490-155">Hvis de stemmer overens, ændres deres status til **Registreret**.</span><span class="sxs-lookup"><span data-stu-id="94490-155">If they match, their status is changed to **Registering**.</span></span> <span data-ttu-id="94490-156">Ellers får du en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="94490-156">Otherwise, you receive an error message.</span></span> <span data-ttu-id="94490-157">Det maksimale antal serienumre, du kan validere på listen, er lig med tilgangsantallet.</span><span class="sxs-lookup"><span data-stu-id="94490-157">The maximum number of serial numbers that you can validate in the list equals to the receiving quantity.</span></span>

<span data-ttu-id="94490-158">Du kan også validere serienumre på fanen **Alle serienummererede varer** på siden **Administration af serienumre**.</span><span class="sxs-lookup"><span data-stu-id="94490-158">You can also validate serial numbers on the **All serialized items** tab of the **Serial number management** page.</span></span> <span data-ttu-id="94490-159">På listen skal du vælge den vare, du vil validere serienumre for.</span><span class="sxs-lookup"><span data-stu-id="94490-159">In the list, select the item that you want to validate serial numbers against.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="94490-160">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="94490-160">Additional resources</span></span>

[<span data-ttu-id="94490-161">Indgående lagerhandling i POS</span><span class="sxs-lookup"><span data-stu-id="94490-161">Inbound inventory operation in POS</span></span>](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)