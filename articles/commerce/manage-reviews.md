---
title: Administrere vurderinger og anmeldelser
description: I dette emne beskrives, hvordan du kan administrere vurderinger og anmeldelser ved hjælp af Microsofts Dynamics 365 Commerce-vurderings- og anmeldelsesværktøj.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: e9becdce5ae36ac637043b9d0febfbbff2392aa9
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698020"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="124b3-103">Administrere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="124b3-103">Manage ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="124b3-104">I dette emne beskrives, hvordan du kan administrere vurderinger og anmeldelser ved hjælp af Microsofts Dynamics 365 Commerce-vurderings- og anmeldelsesværktøj.</span><span class="sxs-lookup"><span data-stu-id="124b3-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="124b3-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="124b3-105">Overview</span></span>

<span data-ttu-id="124b3-106">Dynamics 365 Commerce bruger Microsoft Azure Cognitive Services til automatisk at moderere tekst i anmeldelser ved at bortredigere krænkende ord og udtryk.</span><span class="sxs-lookup"><span data-stu-id="124b3-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="124b3-107">Derudover kan redaktører bruge redigeringsværktøjet til vurderinger og anmeldelser til følgende manuelle opgaver:</span><span class="sxs-lookup"><span data-stu-id="124b3-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="124b3-108">Moderere anmeldelser ved at reagere på dem eller fjerne dem.</span><span class="sxs-lookup"><span data-stu-id="124b3-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="124b3-109">Slette en kundes anmeldelser på kundens anmodning.</span><span class="sxs-lookup"><span data-stu-id="124b3-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="124b3-110">Masseimportere vurderings- og anmeldelsesdata for alle produkter i en Microsoft Power BI-skabelon, så tendenser for vurderinger og anmeldelser kan analyseres.</span><span class="sxs-lookup"><span data-stu-id="124b3-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="124b3-111">Læse en anmeldelse</span><span class="sxs-lookup"><span data-stu-id="124b3-111">Read a review</span></span> 

1. <span data-ttu-id="124b3-112">Gå til **Startside \> Anmeldelser \> Redigering**.</span><span class="sxs-lookup"><span data-stu-id="124b3-112">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="124b3-113">Brug søgefeltet øverst til højre på siden til at filtrere de anmeldelser, der vises efter produkt-id, produktnavn eller anmeldelsestekst.</span><span class="sxs-lookup"><span data-stu-id="124b3-113">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="124b3-114">Yderligere filtre giver dig mulighed for at begrænse anmeldelserne efter status periode, vurdering, kanal eller problem (fjernet, besvaret eller rapporteret).</span><span class="sxs-lookup"><span data-stu-id="124b3-114">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Startside for redigering](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="124b3-116">Besvare en anmeldelse</span><span class="sxs-lookup"><span data-stu-id="124b3-116">Respond to a review</span></span> 

<span data-ttu-id="124b3-117">Kunder, der har købt et produkt, giver jævnligt udtryk for deres tilfredshed eller utilfredshed, eller angiver i nogle tilfælde, at de ikke forstår, hvordan produktet skal bruges.</span><span class="sxs-lookup"><span data-stu-id="124b3-117">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="124b3-118">Som redaktør kan du sende et svar på en anmeldelse.</span><span class="sxs-lookup"><span data-stu-id="124b3-118">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="124b3-119">Dette svar vises sammen med anmeldelsen på webstedet.</span><span class="sxs-lookup"><span data-stu-id="124b3-119">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="124b3-120">Benyt følgende fremgangsmåde for at besvare en anmeldelse.</span><span class="sxs-lookup"><span data-stu-id="124b3-120">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="124b3-121">Gå til **Startside \> Anmeldelser \> Redigering**.</span><span class="sxs-lookup"><span data-stu-id="124b3-121">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="124b3-122">Find og vælg den anmeldelse, der kræver et svar.</span><span class="sxs-lookup"><span data-stu-id="124b3-122">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="124b3-123">Vælg **Tilføj et svar** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="124b3-123">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="124b3-124">Angiv svarteksten og det navn, der skal vises for respondenten.</span><span class="sxs-lookup"><span data-stu-id="124b3-124">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="124b3-125">Respondentens navn er som standard **Redaktør**.</span><span class="sxs-lookup"><span data-stu-id="124b3-125">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="124b3-126">Vælg **Send svar**, når du er færdig.</span><span class="sxs-lookup"><span data-stu-id="124b3-126">When you've finished, select **Post response**.</span></span>

![Besvare en anmeldelse](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="124b3-128">Fjerne en anmeldelse</span><span class="sxs-lookup"><span data-stu-id="124b3-128">Take down a review</span></span> 

<span data-ttu-id="124b3-129">Nogle gange kan redaktører være berettigede til at fjerne kunders anmeldelser af forretningsmæssige årsager.</span><span class="sxs-lookup"><span data-stu-id="124b3-129">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="124b3-130">Benyt følgende fremgangsmåde for at fjerne en anmeldelse.</span><span class="sxs-lookup"><span data-stu-id="124b3-130">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="124b3-131">Gå til **Startside \> Anmeldelser \> Redigering**.</span><span class="sxs-lookup"><span data-stu-id="124b3-131">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="124b3-132">Find og vælg den anmeldelse, der skal fjernes.</span><span class="sxs-lookup"><span data-stu-id="124b3-132">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="124b3-133">Vælg en årsag til fjernelsen i egenskabsruden til højre, og vælg derefter **Fjern**.</span><span class="sxs-lookup"><span data-stu-id="124b3-133">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="124b3-134">Slette en kundes anmeldelser på kundens anmodning</span><span class="sxs-lookup"><span data-stu-id="124b3-134">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="124b3-135">Nogle gange ønsker kunderne, at deres vurderings- og anmeldelsesdata slettes permanent fra et e-handelswebsted.</span><span class="sxs-lookup"><span data-stu-id="124b3-135">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="124b3-136">En redaktør, der modtager en anmodning om fjernelse fra en kunde, kan fjerne kundens data ved hjælp af funktionen sletning af anmeldelser.</span><span class="sxs-lookup"><span data-stu-id="124b3-136">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="124b3-137">Hvis du vil søge efter og slette en kundes data, skal redaktøren bruge den e-mailadresse, som kunden har brugt til at logge på og skrive anmeldelser.</span><span class="sxs-lookup"><span data-stu-id="124b3-137">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="124b3-138">Benyt følgende fremgangsmåde for at finde og slette kundedata.</span><span class="sxs-lookup"><span data-stu-id="124b3-138">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="124b3-139">Gå til **Startside \> Anmeldelser \> Slet**.</span><span class="sxs-lookup"><span data-stu-id="124b3-139">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="124b3-140">Angiv kundens e-mailadresse i feltet **Søg efter brugere vha. e-mailadresse**, og vælg derefter **Søg**.</span><span class="sxs-lookup"><span data-stu-id="124b3-140">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="124b3-141">Hvis kunden har anmeldelsesaktivitet (f.eks. indsendelse af anmeldelser, tilkendegivelser om nytten af andre kunders anmeldelser eller kommentarer til en anden kundes anmeldelse), vises resultaterne.</span><span class="sxs-lookup"><span data-stu-id="124b3-141">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="124b3-142">Knappen **Slet** vises for hvert element.</span><span class="sxs-lookup"><span data-stu-id="124b3-142">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="124b3-143">Vælg **Slet**for hvert element, der skal slettes.</span><span class="sxs-lookup"><span data-stu-id="124b3-143">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="124b3-144">Når du bliver bedt om at bekræfte, skal du vælge **Ja**.</span><span class="sxs-lookup"><span data-stu-id="124b3-144">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Slette kundedata](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="124b3-146">Det kan tage op til syv dage, før data er fjernet fuldstændigt fra systemet.</span><span class="sxs-lookup"><span data-stu-id="124b3-146">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="124b3-147">Redaktører skal give kunderne besked om denne forsinkelse.</span><span class="sxs-lookup"><span data-stu-id="124b3-147">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="124b3-148">Hvis kunderne har ændret deres navn i deres kontoindstillinger, kan der blive vist flere elementer i søgeresultaterne.</span><span class="sxs-lookup"><span data-stu-id="124b3-148">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="124b3-149">Hvis redaktøren i sådanne tilfælde vil slette kundens data fuldstændigt, skal han eller hun vælge **Slet** for hvert element.</span><span class="sxs-lookup"><span data-stu-id="124b3-149">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="124b3-150">Hente vurderings- og anmeldelsesdata</span><span class="sxs-lookup"><span data-stu-id="124b3-150">Download ratings and reviews data</span></span>

<span data-ttu-id="124b3-151">Med redigeringsværktøjet til vurderinger og anmeldelser kan redaktører importere vurderings- og anmeldelsesdata samlet, så de kan analysere tendenser.</span><span class="sxs-lookup"><span data-stu-id="124b3-151">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="124b3-152">En Power BI-skabelon, der indeholder grundlæggende metrikværdier, er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="124b3-152">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="124b3-153">Redaktører kan bruge denne skabelon til at forbinde masseimporterede data med hinanden og få vist et dashboard.</span><span class="sxs-lookup"><span data-stu-id="124b3-153">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="124b3-154">Det er ikke nødvendigt at oprette et brugerdefineret dashboard.</span><span class="sxs-lookup"><span data-stu-id="124b3-154">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="124b3-155">Redaktører kan også tilpasse Power BI-skabelonen, så den opfylder deres specifikke behov.</span><span class="sxs-lookup"><span data-stu-id="124b3-155">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="124b3-156">Hvis du vil hente vurderings- og anmeldelsesdata, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="124b3-156">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="124b3-157">Gå til **Startside \> Anmeldelser \> Rapportering**.</span><span class="sxs-lookup"><span data-stu-id="124b3-157">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="124b3-158">Vælg **Hent anmeldelsesdata** for at hente vurderings- og anmeldelsesdata samlet i CSV-format (semikolonseparerede værdier).</span><span class="sxs-lookup"><span data-stu-id="124b3-158">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="124b3-159">Se vurderings- og anmeldelsestendenser</span><span class="sxs-lookup"><span data-stu-id="124b3-159">View ratings and reviews trends</span></span>

<span data-ttu-id="124b3-160">Redaktører kan hente Power BI-skabelonen, så de kan få vist tendenser i et dashboard.</span><span class="sxs-lookup"><span data-stu-id="124b3-160">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="124b3-161">Hvis du vil se vurderings- og anmeldelsestendenser, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="124b3-161">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="124b3-162">Gå til **Startside \> Anmeldelser \> Rapportering**.</span><span class="sxs-lookup"><span data-stu-id="124b3-162">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="124b3-163">Vælg **Power BI-skabelon** for at hente skabelonen.</span><span class="sxs-lookup"><span data-stu-id="124b3-163">Select **PowerBI template** to download the template.</span></span>

    ![Hente Power BI-skabelonen](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="124b3-165">Åbn den hentede skabelon ved hjælp af Power BI-appen.</span><span class="sxs-lookup"><span data-stu-id="124b3-165">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="124b3-166">Luk dialogboksen **Adgang til webindhold**, der vises, og luk derefter fejlmeddelelsen "Opdater", der vises.</span><span class="sxs-lookup"><span data-stu-id="124b3-166">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="124b3-167">Gå til **Startside**, vælg **Rediger forespørgsler**, og vælg derefter **indstillinger for datakilde**.</span><span class="sxs-lookup"><span data-stu-id="124b3-167">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="124b3-168">Vælg **Skift kilde** i dialogboksen **Indstillinger for datakilde**.</span><span class="sxs-lookup"><span data-stu-id="124b3-168">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="124b3-169">I feltet **URL-adresse** skal du angive stien til de anmeldelsesdata, du hentede i den forrige procedure (f.eks **C:\\Anmeldelser\\Anmeldelsesdata.csv**).</span><span class="sxs-lookup"><span data-stu-id="124b3-169">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![Felt med URL-adresse i dialogboksen Kommaseparerede værdier](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="124b3-171">Vælg **OK**, og vælg derefter **Anvende ændringer**.</span><span class="sxs-lookup"><span data-stu-id="124b3-171">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="124b3-172">Det tager ét til to minutter at anvende ændringerne på datakilden.</span><span class="sxs-lookup"><span data-stu-id="124b3-172">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="124b3-173">Vælg **Tendensark** for at få vist tendenser for vurderinger og anmeldelser.</span><span class="sxs-lookup"><span data-stu-id="124b3-173">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Tendenser i vurderinger og anmeldelser](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="124b3-175">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="124b3-175">Additional resources</span></span>

[<span data-ttu-id="124b3-176">Oversigt over vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="124b3-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="124b3-177">Tilvælge brug af vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="124b3-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="124b3-178">Konfigurere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="124b3-178">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="124b3-179">Synkronisere produktvurderinger i Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="124b3-179">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
