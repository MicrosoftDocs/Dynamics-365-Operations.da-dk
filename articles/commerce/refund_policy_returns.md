---
title: Oprette og opdatere en politik for returneringer og refusioner for en kanal
description: Dette emne forklarer, hvordan du opretter en politik for returneringer og refusioner for en kanal.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: 89e8fe78414e73053317ebe19e3afcc89231d440
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979697"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="0ed78-103">Oprette og opdatere en politik for returneringer og refusioner for en kanal</span><span class="sxs-lookup"><span data-stu-id="0ed78-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="0ed78-104">Oversigt</span><span class="sxs-lookup"><span data-stu-id="0ed78-104">Overview</span></span>

<span data-ttu-id="0ed78-105">Med politikken for kanalreturnering i Dynamics 365 Commerce kan detailhandlere angive de håndhævelser, hvor betalingsmidler kan tillades, for at behandle en returvare på et POS.</span><span class="sxs-lookup"><span data-stu-id="0ed78-105">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="0ed78-106">Dette emne forklarer, hvordan du opretter en politik for returneringer og refusioner for en kanal.</span><span class="sxs-lookup"><span data-stu-id="0ed78-106">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="0ed78-107">Politikkens omfang er i øjeblikket begrænset til at angive de betalingsmidler, der kan tillades for en kanal.</span><span class="sxs-lookup"><span data-stu-id="0ed78-107">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="0ed78-108">Listen "tilladt" er baseret på de betalingsmetoder, der bruges til at foretage købet.</span><span class="sxs-lookup"><span data-stu-id="0ed78-108">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="0ed78-109">F.eks.:</span><span class="sxs-lookup"><span data-stu-id="0ed78-109">For example:</span></span>

- <span data-ttu-id="0ed78-110">Hvis et er foretaget køb med et gavekort, er butikspolitikken kun at behandle refusioner til et nyt gavekort eller for at give butikskredit.</span><span class="sxs-lookup"><span data-stu-id="0ed78-110">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="0ed78-111">Hvis et salg foretages ved hjælp af kontanter, vil de indstillinger, der er tilladt for refusionen, være kontant, gavekort og kundekonto, men ikke kreditkort.</span><span class="sxs-lookup"><span data-stu-id="0ed78-111">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="0ed78-112">Aktivere returneringspolitik</span><span class="sxs-lookup"><span data-stu-id="0ed78-112">Enable return policy</span></span>

<span data-ttu-id="0ed78-113">Benyt følgende fremgangsmåde for at aktivere funktionaliteten af kanalreturneringspolitik:</span><span class="sxs-lookup"><span data-stu-id="0ed78-113">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="0ed78-114">Gå til arbejdsområdet **Administration af funktioner** i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0ed78-114">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="0ed78-115">Søg efter funktionen **Aktivér kanalreturneringspolitikker** på listen over funktionsnavne.</span><span class="sxs-lookup"><span data-stu-id="0ed78-115">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="0ed78-116">Vælg **Aktiver nu**.</span><span class="sxs-lookup"><span data-stu-id="0ed78-116">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="0ed78-117">Konfigurere returneringspolitik</span><span class="sxs-lookup"><span data-stu-id="0ed78-117">Configure return policy</span></span>

<span data-ttu-id="0ed78-118">Udfør følgende trin for at konfigurere en returneringspolitik for en detailbutik eller en onlinedetailkanal.</span><span class="sxs-lookup"><span data-stu-id="0ed78-118">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="0ed78-119">Gå til **Retail og Commerce** \> **Konfiguration af kanal** \> **Returneringer** \> **Kanalreturneringspolitik**.</span><span class="sxs-lookup"><span data-stu-id="0ed78-119">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="0ed78-120">Vælg **Ny** for at oprette en ny skabelon for returneringspolitik.</span><span class="sxs-lookup"><span data-stu-id="0ed78-120">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="0ed78-121">Hvis du vil bruge en eksisterende skabelon, skal du vælge skabelonen i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="0ed78-121">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="0ed78-122">I forbindelse med nye skabeloner skal du tilføje et navn og en beskrivelse, der kan hjælpe dig med at identificere politikken, når den anvendes på kanalen.</span><span class="sxs-lookup"><span data-stu-id="0ed78-122">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="0ed78-123">![Tilføje ny returneringspolitik](media/Return-policy-page1.png "Tilføje ny returneringspolitik")</span><span class="sxs-lookup"><span data-stu-id="0ed78-123">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="0ed78-124">Definer **Tilladte** returneringsbetalingsmidler, der er specifikke for de enkelte betalingsmåder, i sektionen **Tilladte betalingsmetoder for refundering**.</span><span class="sxs-lookup"><span data-stu-id="0ed78-124">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="0ed78-125">![Tilføje betalingsmetoder](media/Return-policy-page2.PNG "Angive tilladte betalingsmetoder pr. betalingstype")</span><span class="sxs-lookup"><span data-stu-id="0ed78-125">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="0ed78-126">Betalingsmetoderne afledes af de betalingsmetoder, der er defineret for organisationen.</span><span class="sxs-lookup"><span data-stu-id="0ed78-126">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="0ed78-127">Hvis du tilføjer en tilladt betalingsmiddeltype for hver angivet betalingsmåde, sikrer du, at der kan foretages returneringer til den tilladte betalingsmiddeltype for returneringer.</span><span class="sxs-lookup"><span data-stu-id="0ed78-127">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="0ed78-128">Knyt skabelonen for returneringspolitik til de butikker, hvor den vil blive brugt.</span><span class="sxs-lookup"><span data-stu-id="0ed78-128">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="0ed78-129">Vælg **Tilføj** under fanen **Detailkanaler**, og tilknyt de tilgængelige kanaler.</span><span class="sxs-lookup"><span data-stu-id="0ed78-129">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="0ed78-130">Vælg de butikker, områder og organisationer, skabelonen skal knyttes til, i dialogboksen **Vælg organisationsnoder**.</span><span class="sxs-lookup"><span data-stu-id="0ed78-130">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="0ed78-131">Der kan kun knyttes én skabelon for returneringspolitik til hver butik.</span><span class="sxs-lookup"><span data-stu-id="0ed78-131">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="0ed78-132">Brug pileknapperne til at vælge butikker, områder eller organisationer.</span><span class="sxs-lookup"><span data-stu-id="0ed78-132">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="0ed78-133">Gyldighedsdatoen for politikken er den dato, hvor politikkerne anvendes på kanalerne, og kanaljobbene køres.</span><span class="sxs-lookup"><span data-stu-id="0ed78-133">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="0ed78-134">![Dialogboksen Vælg organisationsnoder](media/Return-policy-page3.PNG "Dialogboksen Vælg organisationsnoder")</span><span class="sxs-lookup"><span data-stu-id="0ed78-134">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="0ed78-135">På siden **Distributionsplan** skal du køre jobbet **1070** for at gøre kanalreturneringspolitikken tilgængelig for POS.</span><span class="sxs-lookup"><span data-stu-id="0ed78-135">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="0ed78-136">Se kanalreturneringspolitikken i POS</span><span class="sxs-lookup"><span data-stu-id="0ed78-136">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="0ed78-137">Følg trinnene i et af følgende eksempler for at få vist de tilladte betalingsmiddeltyper for returneringer i POS.</span><span class="sxs-lookup"><span data-stu-id="0ed78-137">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="0ed78-138">Log på POS som kasserer eller leder.</span><span class="sxs-lookup"><span data-stu-id="0ed78-138">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="0ed78-139">Vælg **Vis kladde** under **Skift og kasseapparat**.</span><span class="sxs-lookup"><span data-stu-id="0ed78-139">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="0ed78-140">Vælg den transaktion, der er en del af returneringen.</span><span class="sxs-lookup"><span data-stu-id="0ed78-140">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="0ed78-141">Vælg de varer, der skal refunderes, og vælg betalingsmåden.</span><span class="sxs-lookup"><span data-stu-id="0ed78-141">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="0ed78-142">Hvis det valgte betalingsmiddel er på den tilladte liste over betalingsmiddeltyper for returnering, kan kassereren fuldføre transaktionen.</span><span class="sxs-lookup"><span data-stu-id="0ed78-142">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="0ed78-143">Hvis det valgte betalingsmiddel ikke er tilladt, vises der en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="0ed78-143">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="0ed78-144">Vælg **Skyldigt beløb** for at få vist en liste over alle tilladte betalingsmiddeltyper for returnering.</span><span class="sxs-lookup"><span data-stu-id="0ed78-144">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="0ed78-145">-eller-</span><span class="sxs-lookup"><span data-stu-id="0ed78-145">-or-</span></span>

1. <span data-ttu-id="0ed78-146">Log på POS som kasserer eller leder.</span><span class="sxs-lookup"><span data-stu-id="0ed78-146">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="0ed78-147">Vælg **Returtransaktion**, og angiv kvitterings-id'et ved hjælp af en scanning af stregkode eller manuel indtastning.</span><span class="sxs-lookup"><span data-stu-id="0ed78-147">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="0ed78-148">Vælg den transaktion, der er en del af returneringen.</span><span class="sxs-lookup"><span data-stu-id="0ed78-148">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="0ed78-149">Vælg de varer, der skal refunderes, og vælg betalingsmåden.</span><span class="sxs-lookup"><span data-stu-id="0ed78-149">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="0ed78-150">Hvis det valgte betalingsmiddel er på den tilladte liste over betalingsmiddeltyper for returnering, kan kassereren fuldføre transaktionen.</span><span class="sxs-lookup"><span data-stu-id="0ed78-150">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="0ed78-151">Hvis det valgte betalingsmiddel ikke er tilladt, vises der en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="0ed78-151">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="0ed78-152">Vælg **Skyldigt beløb** for at få vist en liste over alle tilladte betalingsmiddeltyper for returnering.</span><span class="sxs-lookup"><span data-stu-id="0ed78-152">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="0ed78-153">![Refusion er ikke tilladt](media/Return-policy-page6.png "Refusionstype er ikke tilladt")</span><span class="sxs-lookup"><span data-stu-id="0ed78-153">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="0ed78-154">![Liste over betalingsmetoder](media/Return-policy-page5.PNG "Refusionstyper er tilladt")</span><span class="sxs-lookup"><span data-stu-id="0ed78-154">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>
