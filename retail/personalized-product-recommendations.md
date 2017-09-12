---
title: Oversigt over tilpassede produktanbefalinger
description: "I Dynamics 365 for Retail kan produktanbefalinger vises på POS-enheden. Anbefalingerne er varer, som kunden muligvis er interesseret i baseret på deres købshistorik, varer i deres ønskeseddel og varer, som andre kunder har købt online og i fysiske butikker. For detailhandlere med store kataloger hjælper anbefalingerne kunden med opdagelse af produkter. Gennem fremvisning af produkter, der er målrettet mod en kundes interesser og købsvaner, kan produktanbefalinger hjælpe detailhandlere med mersalg og krydssalg, og de kan forbedre fastholdelsen af kunderne. I Dynamics 365 for Retail er produktanbefalinger understøttet af Cognitive Services og Microsoft Azure Machine Learning."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611, Retail Version
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: a3a3b5e87a797c29c13b180c248d1782805c4c31
ms.contentlocale: da-dk
ms.lasthandoff: 06/29/2017


---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="b6ba0-107">Oversigt over tilpassede produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="b6ba0-107">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="b6ba0-108">I Dynamics 365 for Retail kan produktanbefalinger vises på POS-enheden.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-108">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="b6ba0-109">Anbefalingerne er varer, som kunden muligvis er interesseret i baseret på deres købshistorik, varer i deres ønskeseddel og varer, som andre kunder har købt online og i fysiske butikker.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-109">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="b6ba0-110">For detailhandlere med store kataloger hjælper anbefalingerne kunden med opdagelse af produkter.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-110">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="b6ba0-111">Gennem fremvisning af produkter, der er målrettet mod en kundes interesser og købsvaner, kan produktanbefalinger hjælpe detailhandlere med mersalg og krydssalg, og de kan forbedre fastholdelsen af kunderne.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-111">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="b6ba0-112">I Dynamics 365 for Retail er produktanbefalinger understøttet af Cognitive Services og Microsoft Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-112">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>

<a name="scenarios"></a><span data-ttu-id="b6ba0-113">Scenarier</span><span class="sxs-lookup"><span data-stu-id="b6ba0-113">Scenarios</span></span>
---------

<span data-ttu-id="b6ba0-114">Produktanbefalinger er aktiveret for følgende POS-scenarier.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-114">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="b6ba0-115">De er tilgængelige i Cloud POS eller Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="b6ba0-115">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="b6ba0-116">På siden **Produktdetaljer**:</span><span class="sxs-lookup"><span data-stu-id="b6ba0-116">On the **Product details** page:</span></span>

-   <span data-ttu-id="b6ba0-117">Hvis en butiksansat går ind på siden **Produktdetaljer**, når vedkommende ser på tidligere transaktioner på tværs af forskellige kanaler, foreslår anbefalingsprogrammet yderligere varer, det er sandsynligt at købe sammen.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-117">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="b6ba0-118">Hvis den butiksansatte føjer en kunde til transaktionen og derefter besøger derefter siden **Produktdetaljer**, giver anbefalingsprogrammet tilpassede anbefalinger ved hjælp af kundens transaktionshistorik.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-118">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="b6ba0-119">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="b6ba0-119">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="b6ba0-120">På siden **Transaktion**:</span><span class="sxs-lookup"><span data-stu-id="b6ba0-120">On the **Transaction** page:</span></span>

-   <span data-ttu-id="b6ba0-121">Anbefalingsprogrammet foreslår varer baseret på hele listen over varer i indkøbskurven.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-121">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="b6ba0-122">Hvis den butiksansatte føjer en kunde til transaktionen, giver anbefalingsprogrammet personlige anbefalinger ved hjælp af kundens transaktionshistorik og listen over varer i indkøbskurven.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-122">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

<span data-ttu-id="b6ba0-123">**Bemærk!** For at få vist anbefalinger på siden **Transaktion** skal forhandleren opdatere skærmlayoutet i Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-123">**Note**  To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="b6ba0-124">Kontrolelementet **Anbefalinger** skal slippes på siden **Transaktion**.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-124">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="b6ba0-125">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="b6ba0-125">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="b6ba0-126">På siden **Kundeoplysninger**:</span><span class="sxs-lookup"><span data-stu-id="b6ba0-126">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="b6ba0-127">Anbefalingsprogrammet foreslår varer baseret på bruger-id'et og varer på kundens ønskeliste.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-127">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="b6ba0-128">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="b6ba0-128">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="b6ba0-129">Konfigurer Dynamics 365 for Retail til at aktivere POS-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="b6ba0-129">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="b6ba0-130">Hvis du vil konfigurere produktanbefalinger, skal du konfigurere følgende.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-130">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="b6ba0-131">Sørg for, at du har valgt den korrekte **juridiske enhed**.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-131">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="b6ba0-132">Gå til **Enhedslager**, vælg **Detailsalg**, og klik derefter på **Opdater**.** ** Derved anvendes demodataene (eller dine data) fra driftsdatabasen og flyttes til enhedslageret.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-132">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.** **This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="b6ba0-133">Valgfrit: For at få vist anbefalinger på skærmbilledet Transaktion, skal du gå til **Skærmlayout, **vælge dit skærmlayout, starte **skærmlayoutdesigneren**** **og derefter slippe **kontrolelementet med anbefalinger**, hvor der er behov for det.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-133">Optional: To display recommendations on the transaction screen, go to **Screen Layout, **choose your screen layout, launch the **Screen layout designer**,** **and then drop the **recommendations control **where needed.</span></span>
4.  <span data-ttu-id="b6ba0-134">Gå til **Detailparametre**, vælg **Maskinel indlæring** og vælg **Ja** under **Aktivér POS-anbefalinger**.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-134">Go to **Retail parameters**, select **Machine-learning**, select **Yes **under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="b6ba0-135">For at se anbefalinger på et POS skal du kører det globale konfigurationsjob **1110**.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-135">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="b6ba0-136">For at afspejle ændringer i POS-skærmlayoutdesigneren skal du køre kanalkonfigurationsjobbet **1070**.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-136">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="b6ba0-137">[]()Hvordan fungerer det?</span><span class="sxs-lookup"><span data-stu-id="b6ba0-137">[]()How does it work?</span></span>
<span data-ttu-id="b6ba0-138">Når du opdaterer enheden **Enhedslager**, udføres følgende handlinger.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-138">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="b6ba0-139">Dataene i det format, der kræves af Cognitive Services, udtrækkes fra driftsdatabasen i Dynamics-365 for Retail og sendes til enhedslageret.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-139">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="b6ba0-140">Dataene bruges til at rense dataene ved hjælp af Hive-scripts som en del af ADF-aktiviteterne i Azure Data Factory (ADF).</span><span class="sxs-lookup"><span data-stu-id="b6ba0-140">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="b6ba0-141">Rengjorte data gemmes i blob-lager.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-141">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="b6ba0-142">Data fra blob-lager bruges af API'en i Cognitive Services til at træne en anbefalingsmodel.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-142">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="b6ba0-143">Når du aktiverer **Aktivér anbefalinger** og kører konfigurationsjobbene, udføres følgende handlinger.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-143">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="b6ba0-144">Legitimationsoplysninger og id for modellen hentes fra API'en og gemmes i driftsdatabasen i Dynamics-365 for Retail i web.config til AOS og også i detailserveren.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-144">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="b6ba0-145">Legitimationsoplysninger og id for modellen er gjort tilgængelige for CRT, så kald til produktanbefalinger fra Cloud POS og MPOS i onlinetilstand kan opfyldes.</span><span class="sxs-lookup"><span data-stu-id="b6ba0-145">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>


<a name="see-also"></a><span data-ttu-id="b6ba0-146">Se også</span><span class="sxs-lookup"><span data-stu-id="b6ba0-146">See also</span></span>
--------

[<span data-ttu-id="b6ba0-147">Føj et kontrolelement med anbefalinger til transaktionssiden på en POS-enhed</span><span class="sxs-lookup"><span data-stu-id="b6ba0-147">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




