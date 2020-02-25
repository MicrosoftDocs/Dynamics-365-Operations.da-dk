---
title: Administrere vurderinger og anmeldelser
description: I dette emne beskrives, hvordan du kan administrere vurderinger og anmeldelser ved hjælp af Microsofts Dynamics 365 Commerce-vurderings- og anmeldelsesværktøj.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a7fa2ae3124a0a68b3890987c5dce2730e5c2183
ms.sourcegitcommit: 1e6c8163da5818196769eb278afb3a2335d0cbe3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027236"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="d118b-103">Administrere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="d118b-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d118b-104">I dette emne beskrives, hvordan du kan administrere vurderinger og anmeldelser ved hjælp af Microsofts Dynamics 365 Commerce-vurderings- og anmeldelsesværktøj.</span><span class="sxs-lookup"><span data-stu-id="d118b-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="d118b-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="d118b-105">Overview</span></span>

<span data-ttu-id="d118b-106">Dynamics 365 Commerce bruger Microsoft Azure Cognitive Services til automatisk at moderere tekst i anmeldelser ved at bortredigere krænkende ord og udtryk.</span><span class="sxs-lookup"><span data-stu-id="d118b-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="d118b-107">Derudover kan redaktører bruge redigeringsværktøjet til vurderinger og anmeldelser til følgende manuelle opgaver:</span><span class="sxs-lookup"><span data-stu-id="d118b-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="d118b-108">Moderere anmeldelser ved at reagere på dem eller fjerne dem.</span><span class="sxs-lookup"><span data-stu-id="d118b-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="d118b-109">Slette en kundes anmeldelser på kundens anmodning.</span><span class="sxs-lookup"><span data-stu-id="d118b-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="d118b-110">Masseimportere vurderings- og anmeldelsesdata for alle produkter i en Microsoft Power BI-skabelon, så tendenser for vurderinger og anmeldelser kan analyseres.</span><span class="sxs-lookup"><span data-stu-id="d118b-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="access-ratings-and-reviews-moderation-features"></a><span data-ttu-id="d118b-111">Få adgang til ændringsfunktioner for vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="d118b-111">Access ratings and reviews moderation features</span></span>

<span data-ttu-id="d118b-112">Udfør følgende trin for at få adgang til ændringsfunktioner for vurderinger og anmeldelser i værktøjet til e-handelsadministration af websteder.</span><span class="sxs-lookup"><span data-stu-id="d118b-112">To access ratings and reviews moderation features in the e-Commerce site management tool, follow these steps.</span></span>

1. <span data-ttu-id="d118b-113">Log på [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="d118b-113">Sign in to [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="d118b-114">Åbn det projekt, der indeholder det miljø, hvor du vil initialisere e-handel.</span><span class="sxs-lookup"><span data-stu-id="d118b-114">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="d118b-115">Vælg miljøet i sektionen **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="d118b-115">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="d118b-116">Under **Miljøfunktioner** skal du vælge **Retail administration**.</span><span class="sxs-lookup"><span data-stu-id="d118b-116">Under **Environment features**, select **Retail manage**.</span></span>
1. <span data-ttu-id="d118b-117">Under fanen **e-handel** skal du under **Links** vælge **Værktøj til administration af e-Commerce-websted**.</span><span class="sxs-lookup"><span data-stu-id="d118b-117">On the **e-Commerce** tab under **Links**, select **e-Commerce Site management tool**.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="d118b-118">Læse en anmeldelse</span><span class="sxs-lookup"><span data-stu-id="d118b-118">Read a review</span></span> 

1. <span data-ttu-id="d118b-119">Gå til **Startside \> Anmeldelser \> Redigering**.</span><span class="sxs-lookup"><span data-stu-id="d118b-119">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="d118b-120">Brug søgefeltet øverst til højre på siden til at filtrere de anmeldelser, der vises efter produkt-id, produktnavn eller anmeldelsestekst.</span><span class="sxs-lookup"><span data-stu-id="d118b-120">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="d118b-121">Yderligere filtre giver dig mulighed for at begrænse anmeldelserne efter status periode, vurdering, kanal eller problem (fjernet, besvaret eller rapporteret).</span><span class="sxs-lookup"><span data-stu-id="d118b-121">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Startside for redigering](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="d118b-123">Besvare en anmeldelse</span><span class="sxs-lookup"><span data-stu-id="d118b-123">Respond to a review</span></span> 

<span data-ttu-id="d118b-124">Kunder, der har købt et produkt, giver jævnligt udtryk for deres tilfredshed eller utilfredshed, eller angiver i nogle tilfælde, at de ikke forstår, hvordan produktet skal bruges.</span><span class="sxs-lookup"><span data-stu-id="d118b-124">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="d118b-125">Som redaktør kan du sende et svar på en anmeldelse.</span><span class="sxs-lookup"><span data-stu-id="d118b-125">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="d118b-126">Dette svar vises sammen med anmeldelsen på webstedet.</span><span class="sxs-lookup"><span data-stu-id="d118b-126">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="d118b-127">Benyt følgende fremgangsmåde for at besvare en anmeldelse.</span><span class="sxs-lookup"><span data-stu-id="d118b-127">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="d118b-128">Gå til **Startside \> Anmeldelser \> Redigering**.</span><span class="sxs-lookup"><span data-stu-id="d118b-128">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="d118b-129">Find og vælg den anmeldelse, der kræver et svar.</span><span class="sxs-lookup"><span data-stu-id="d118b-129">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="d118b-130">Vælg **Tilføj et svar** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="d118b-130">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="d118b-131">Angiv svarteksten og det navn, der skal vises for respondenten.</span><span class="sxs-lookup"><span data-stu-id="d118b-131">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="d118b-132">Respondentens navn er som standard **Redaktør**.</span><span class="sxs-lookup"><span data-stu-id="d118b-132">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="d118b-133">Vælg **Send svar**, når du er færdig.</span><span class="sxs-lookup"><span data-stu-id="d118b-133">When you've finished, select **Post response**.</span></span>

![Besvare en anmeldelse](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="d118b-135">Fjerne en anmeldelse</span><span class="sxs-lookup"><span data-stu-id="d118b-135">Take down a review</span></span> 

<span data-ttu-id="d118b-136">Nogle gange kan redaktører være berettigede til at fjerne kunders anmeldelser af forretningsmæssige årsager.</span><span class="sxs-lookup"><span data-stu-id="d118b-136">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="d118b-137">Benyt følgende fremgangsmåde for at fjerne en anmeldelse.</span><span class="sxs-lookup"><span data-stu-id="d118b-137">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="d118b-138">Gå til **Startside \> Anmeldelser \> Redigering**.</span><span class="sxs-lookup"><span data-stu-id="d118b-138">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="d118b-139">Find og vælg den anmeldelse, der skal fjernes.</span><span class="sxs-lookup"><span data-stu-id="d118b-139">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="d118b-140">Vælg en årsag til fjernelsen i egenskabsruden til højre, og vælg derefter **Fjern**.</span><span class="sxs-lookup"><span data-stu-id="d118b-140">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="d118b-141">Slette en kundes anmeldelser på kundens anmodning</span><span class="sxs-lookup"><span data-stu-id="d118b-141">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="d118b-142">Nogle gange ønsker kunderne, at deres vurderings- og anmeldelsesdata slettes permanent fra et e-handelswebsted.</span><span class="sxs-lookup"><span data-stu-id="d118b-142">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="d118b-143">En redaktør, der modtager en anmodning om fjernelse fra en kunde, kan fjerne kundens data ved hjælp af funktionen sletning af anmeldelser.</span><span class="sxs-lookup"><span data-stu-id="d118b-143">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="d118b-144">Hvis du vil søge efter og slette en kundes data, skal redaktøren bruge den e-mailadresse, som kunden har brugt til at logge på og skrive anmeldelser.</span><span class="sxs-lookup"><span data-stu-id="d118b-144">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="d118b-145">Benyt følgende fremgangsmåde for at finde og slette kundedata.</span><span class="sxs-lookup"><span data-stu-id="d118b-145">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="d118b-146">Gå til **Startside \> Anmeldelser \> Slet**.</span><span class="sxs-lookup"><span data-stu-id="d118b-146">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="d118b-147">Angiv kundens e-mailadresse i feltet **Søg efter brugere vha. e-mailadresse**, og vælg derefter **Søg**.</span><span class="sxs-lookup"><span data-stu-id="d118b-147">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="d118b-148">Hvis kunden har anmeldelsesaktivitet (f.eks. indsendelse af anmeldelser, tilkendegivelser om nytten af andre kunders anmeldelser eller kommentarer til en anden kundes anmeldelse), vises resultaterne.</span><span class="sxs-lookup"><span data-stu-id="d118b-148">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="d118b-149">Knappen **Slet** vises for hvert element.</span><span class="sxs-lookup"><span data-stu-id="d118b-149">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="d118b-150">Vælg **Slet**for hvert element, der skal slettes.</span><span class="sxs-lookup"><span data-stu-id="d118b-150">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="d118b-151">Når du bliver bedt om at bekræfte, skal du vælge **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d118b-151">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Slette kundedata](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="d118b-153">Det kan tage op til syv dage, før data er fjernet fuldstændigt fra systemet.</span><span class="sxs-lookup"><span data-stu-id="d118b-153">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="d118b-154">Redaktører skal give kunderne besked om denne forsinkelse.</span><span class="sxs-lookup"><span data-stu-id="d118b-154">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="d118b-155">Hvis kunderne har ændret deres navn i deres kontoindstillinger, kan der blive vist flere elementer i søgeresultaterne.</span><span class="sxs-lookup"><span data-stu-id="d118b-155">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="d118b-156">Hvis redaktøren i sådanne tilfælde vil slette kundens data fuldstændigt, skal han eller hun vælge **Slet** for hvert element.</span><span class="sxs-lookup"><span data-stu-id="d118b-156">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="d118b-157">Hente vurderings- og anmeldelsesdata</span><span class="sxs-lookup"><span data-stu-id="d118b-157">Download ratings and reviews data</span></span>

<span data-ttu-id="d118b-158">Med redigeringsværktøjet til vurderinger og anmeldelser kan redaktører importere vurderings- og anmeldelsesdata samlet, så de kan analysere tendenser.</span><span class="sxs-lookup"><span data-stu-id="d118b-158">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="d118b-159">En Power BI-skabelon, der indeholder grundlæggende metrikværdier, er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="d118b-159">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="d118b-160">Redaktører kan bruge denne skabelon til at forbinde masseimporterede data med hinanden og få vist et dashboard.</span><span class="sxs-lookup"><span data-stu-id="d118b-160">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="d118b-161">Det er ikke nødvendigt at oprette et brugerdefineret dashboard.</span><span class="sxs-lookup"><span data-stu-id="d118b-161">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="d118b-162">Redaktører kan også tilpasse Power BI-skabelonen, så den opfylder deres specifikke behov.</span><span class="sxs-lookup"><span data-stu-id="d118b-162">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="d118b-163">Hvis du vil hente vurderings- og anmeldelsesdata, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="d118b-163">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="d118b-164">Gå til **Startside \> Anmeldelser \> Rapportering**.</span><span class="sxs-lookup"><span data-stu-id="d118b-164">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="d118b-165">Vælg **Hent anmeldelsesdata** for at hente vurderings- og anmeldelsesdata samlet i CSV-format (semikolonseparerede værdier).</span><span class="sxs-lookup"><span data-stu-id="d118b-165">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="d118b-166">Se vurderings- og anmeldelsestendenser</span><span class="sxs-lookup"><span data-stu-id="d118b-166">View ratings and reviews trends</span></span>

<span data-ttu-id="d118b-167">Redaktører kan hente Power BI-skabelonen, så de kan få vist tendenser i et dashboard.</span><span class="sxs-lookup"><span data-stu-id="d118b-167">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="d118b-168">Hvis du vil se vurderings- og anmeldelsestendenser, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="d118b-168">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="d118b-169">Gå til **Startside \> Anmeldelser \> Rapportering**.</span><span class="sxs-lookup"><span data-stu-id="d118b-169">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="d118b-170">Vælg **Power BI-skabelon** for at hente skabelonen.</span><span class="sxs-lookup"><span data-stu-id="d118b-170">Select **PowerBI template** to download the template.</span></span>

    ![Hente Power BI-skabelonen](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="d118b-172">Åbn den hentede skabelon ved hjælp af Power BI-appen.</span><span class="sxs-lookup"><span data-stu-id="d118b-172">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="d118b-173">Luk dialogboksen **Adgang til webindhold**, der vises, og luk derefter fejlmeddelelsen "Opdater", der vises.</span><span class="sxs-lookup"><span data-stu-id="d118b-173">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="d118b-174">Gå til **Startside**, vælg **Rediger forespørgsler**, og vælg derefter **indstillinger for datakilde**.</span><span class="sxs-lookup"><span data-stu-id="d118b-174">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="d118b-175">Vælg **Skift kilde** i dialogboksen **Indstillinger for datakilde**.</span><span class="sxs-lookup"><span data-stu-id="d118b-175">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="d118b-176">I feltet **URL-adresse** skal du angive stien til de anmeldelsesdata, du hentede i den forrige procedure (f.eks **C:\\Anmeldelser\\Anmeldelsesdata.csv**).</span><span class="sxs-lookup"><span data-stu-id="d118b-176">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![Felt med URL-adresse i dialogboksen Kommaseparerede værdier](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="d118b-178">Vælg **OK**, og vælg derefter **Anvende ændringer**.</span><span class="sxs-lookup"><span data-stu-id="d118b-178">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="d118b-179">Det tager ét til to minutter at anvende ændringerne på datakilden.</span><span class="sxs-lookup"><span data-stu-id="d118b-179">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="d118b-180">Vælg **Tendensark** for at få vist tendenser for vurderinger og anmeldelser.</span><span class="sxs-lookup"><span data-stu-id="d118b-180">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Tendenser i vurderinger og anmeldelser](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="d118b-182">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="d118b-182">Additional resources</span></span>

[<span data-ttu-id="d118b-183">Oversigt over vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="d118b-183">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="d118b-184">Tilvælge brug af vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="d118b-184">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="d118b-185">Konfigurere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="d118b-185">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="d118b-186">Synkronisere produktvurderinger i Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="d118b-186">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
