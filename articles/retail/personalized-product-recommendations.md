---
title: Tilpassede produktanbefalinger
description: "Dette emne indeholder oplysninger om Dynamics 365 for Retail-produktanbefalingerne, der kan vises på POS-enheden."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: d20bc3519096f1035d26f89d42aa7e8f0fc368cd
ms.openlocfilehash: 7925a37c595f5ffa040747462d3ea60a3da41858
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2018

---

# <a name="personalized-product-recommendations"></a><span data-ttu-id="a8b8f-103">Tilpassede produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="a8b8f-103">Personalized product recommendations</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="a8b8f-104">Vi vil fjerne den aktuelle version af produktanbefalingstjenesten, fordi vi ændrer denne funktion og giver den en bedre algoritme og nyere detailrelaterede funktioner.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="a8b8f-105">Du kan finde flere oplysninger i [Fjernede eller forældede funktioner](../dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="a8b8f-105">For more information see [Removed or deprecated features](../dev-itpro/migration-upgrade/deprecated-features.md).</span></span> 

<span data-ttu-id="a8b8f-106">I Dynamics 365 for Retail kan produktanbefalinger vises på POS-enheden.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-106">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="a8b8f-107">Anbefalingerne er varer, som kunden muligvis er interesseret i baseret på deres købshistorik, varer i deres ønskeseddel og varer, som andre kunder har købt online og i fysiske butikker.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-107">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="a8b8f-108">For detailhandlere med store kataloger hjælper anbefalingerne kunden med opdagelse af produkter.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-108">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="a8b8f-109">Gennem fremvisning af produkter, der er målrettet mod en kundes interesser og købsvaner, kan produktanbefalinger hjælpe detailhandlere med mersalg og krydssalg, og de kan forbedre fastholdelsen af kunderne.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-109">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="a8b8f-110">I Dynamics 365 for Retail er produktanbefalinger understøttet af Cognitive Services og Microsoft Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-110">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="a8b8f-111">Scenarier</span><span class="sxs-lookup"><span data-stu-id="a8b8f-111">Scenarios</span></span>
---------

<span data-ttu-id="a8b8f-112">Produktanbefalinger er aktiveret for følgende POS-scenarier.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-112">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="a8b8f-113">De er tilgængelige i Cloud POS eller Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="a8b8f-113">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="a8b8f-114">På siden **Produktdetaljer**:</span><span class="sxs-lookup"><span data-stu-id="a8b8f-114">On the **Product details** page:</span></span>

-   <span data-ttu-id="a8b8f-115">Hvis en butiksansat går ind på siden **Produktdetaljer**, når vedkommende ser på tidligere transaktioner på tværs af forskellige kanaler, foreslår anbefalingsprogrammet yderligere varer, det er sandsynligt at købe sammen.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-115">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="a8b8f-116">Hvis den butiksansatte føjer en kunde til transaktionen og derefter besøger derefter siden **Produktdetaljer**, giver anbefalingsprogrammet tilpassede anbefalinger ved hjælp af kundens transaktionshistorik.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-116">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="a8b8f-117">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="a8b8f-117">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="a8b8f-118">På siden **Transaktion**:</span><span class="sxs-lookup"><span data-stu-id="a8b8f-118">On the **Transaction** page:</span></span>

-   <span data-ttu-id="a8b8f-119">Anbefalingsprogrammet foreslår varer baseret på hele listen over varer i indkøbskurven.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-119">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="a8b8f-120">Hvis den butiksansatte føjer en kunde til transaktionen, giver anbefalingsprogrammet personlige anbefalinger ved hjælp af kundens transaktionshistorik og listen over varer i indkøbskurven.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-120">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="a8b8f-121">For at få vist anbefalinger på siden **Transaktion** skal forhandleren opdatere skærmlayoutet i Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-121">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="a8b8f-122">Kontrolelementet **Anbefalinger** skal slippes på siden **Transaktion**.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-122">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="a8b8f-123">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="a8b8f-123">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="a8b8f-124">På siden **Kundeoplysninger**:</span><span class="sxs-lookup"><span data-stu-id="a8b8f-124">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="a8b8f-125">Anbefalingsprogrammet foreslår varer baseret på bruger-id'et og varer på kundens ønskeliste.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-125">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="a8b8f-126">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="a8b8f-126">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="a8b8f-127">Konfigurer Dynamics 365 for Retail til at aktivere POS-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="a8b8f-127">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="a8b8f-128">Hvis du vil konfigurere produktanbefalinger, skal du konfigurere følgende.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-128">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="a8b8f-129">Sørg for, at du har valgt den korrekte **juridiske enhed**.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-129">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="a8b8f-130">Gå til **Enhedslager**, vælg **Detailsalg**, og klik derefter på **Opdater**.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-130">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.</span></span> <span data-ttu-id="a8b8f-131">Dette bruger demodataene (eller dine data) fra driftsdatabasen operationelle og flytter dem til enhedslageret.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-131">This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="a8b8f-132">Valgfrit: For at få vist anbefalinger på skærmbilledet Transaktion, skal du gå til **Skærmlayout**, vælge dit skærmlayout, starte **skærmlayoutdesigneren** og derefter slippe kontrolelementet med **anbefalinger**, hvor der er behov for det.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-132">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>

4.  <span data-ttu-id="a8b8f-133">Gå til **Detailparametre**, vælg **Maskinel indlæring** og vælg **Ja** under **Aktivér POS-anbefalinger**.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-133">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="a8b8f-134">For at se anbefalinger på et POS skal du kører det globale konfigurationsjob **1110**.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-134">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="a8b8f-135">For at afspejle ændringer i POS-skærmlayoutdesigneren skal du køre kanalkonfigurationsjobbet **1070**.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-135">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="a8b8f-136">Hvordan fungerer det?</span><span class="sxs-lookup"><span data-stu-id="a8b8f-136">How does it work?</span></span>
<span data-ttu-id="a8b8f-137">Når du opdaterer enheden **Enhedslager**, udføres følgende handlinger.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-137">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="a8b8f-138">Dataene i det format, der kræves af Cognitive Services, udtrækkes fra driftsdatabasen i Dynamics-365 for Retail og sendes til enhedslageret.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-138">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="a8b8f-139">Dataene bruges til at rense dataene ved hjælp af Hive-scripts som en del af ADF-aktiviteterne i Azure Data Factory (ADF).</span><span class="sxs-lookup"><span data-stu-id="a8b8f-139">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="a8b8f-140">Rengjorte data gemmes i blob-lager.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-140">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="a8b8f-141">Data fra blob-lager bruges af API'en i Cognitive Services til at træne en anbefalingsmodel.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-141">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="a8b8f-142">Når du aktiverer **Aktivér anbefalinger** og kører konfigurationsjobbene, udføres følgende handlinger.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-142">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="a8b8f-143">Legitimationsoplysninger og id for modellen hentes fra API'en og gemmes i driftsdatabasen i Dynamics-365 for Retail i web.config til AOS og også i detailserveren.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-143">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="a8b8f-144">Legitimationsoplysninger og id for modellen er gjort tilgængelige for CRT, så kald til produktanbefalinger fra Cloud POS og MPOS i onlinetilstand kan opfyldes.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-144">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>

> ## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="a8b8f-145">Foretage fejlfinding af problemer, hvor produktanbefalingerne allerede er aktiveret</span><span class="sxs-lookup"><span data-stu-id="a8b8f-145">Troubleshoot issues where you have Product recommendations already enabled</span></span> 
> - <span data-ttu-id="a8b8f-146">Gå til **Detailparametre** > **Maskinel indlæring** > **Deaktiver produktanbefalinger**, og kør **Globalt konfigurationsjob [1110]**.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-146">Navigate to **Retail Parameters** > **Machine learning** > **Disable product recommendations** and run **Global configuration job [1110]**.</span></span> <span data-ttu-id="a8b8f-147">Hvis du ikke kan finde fanen **Maskinel indlæring**, skal du kontakte Dynamics Support.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-147">If you are not able to locate **Machine learning** tab, please contact Dynamics Support.</span></span> 
> 
> - <span data-ttu-id="a8b8f-148">Hvis du har føjet **Kontrolelement til anbefalinger** til din transaktionsskærm ved hjælp af **Designer for skærmlayout**, skal du også fjerne det.</span><span class="sxs-lookup"><span data-stu-id="a8b8f-148">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span> 



<a name="additional-resources"></a><span data-ttu-id="a8b8f-149">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a8b8f-149">Additional resources</span></span>
--------

[<span data-ttu-id="a8b8f-150">Føj et kontrolelement med anbefalinger til transaktionssiden på en POS-enhed</span><span class="sxs-lookup"><span data-stu-id="a8b8f-150">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




