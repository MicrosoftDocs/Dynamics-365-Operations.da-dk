---
title: Administrere vurderinger og anmeldelser
description: I dette emne beskrives, hvordan du kan håndtere vurderinger og anmeldelser i Microsoft Dynamics 365 Commerce-webstedsgenerator.
author: gvrmohanreddy
manager: annbe
ms.date: 10/09/2020
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
ms.openlocfilehash: 3fc88bc5a5868dce7c0539bf3f0ddc5b751e7b75
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411102"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="c4318-103">Administrere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="c4318-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c4318-104">I dette emne beskrives, hvordan du kan håndtere vurderinger og anmeldelser i Microsoft Dynamics 365 Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="c4318-104">This topic explains how to manage ratings and reviews in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="c4318-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="c4318-105">Overview</span></span>

<span data-ttu-id="c4318-106">Dynamics 365 Commerce bruger Microsoft Azure Cognitive Services til automatisk at moderere tekst i anmeldelser ved at bortredigere krænkende ord og udtryk.</span><span class="sxs-lookup"><span data-stu-id="c4318-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="c4318-107">Derudover kan redaktører bruge Dynamics 365 Commerce-webstedsgenerator til at implementere følgende manuelle opgaver:</span><span class="sxs-lookup"><span data-stu-id="c4318-107">In addition, moderators can use Dynamics 365 Commerce site builder to implement the following manual tasks:</span></span>

- <span data-ttu-id="c4318-108">Moderere anmeldelser ved at reagere på dem eller fjerne dem.</span><span class="sxs-lookup"><span data-stu-id="c4318-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="c4318-109">Slette en kundes anmeldelser på kundens anmodning.</span><span class="sxs-lookup"><span data-stu-id="c4318-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="c4318-110">Masseimportere vurderings- og anmeldelsesdata for alle produkter i en Microsoft Power BI-skabelon, så tendenser for vurderinger og anmeldelser kan analyseres.</span><span class="sxs-lookup"><span data-stu-id="c4318-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="c4318-111">Læse en anmeldelse</span><span class="sxs-lookup"><span data-stu-id="c4318-111">Read a review</span></span> 

<span data-ttu-id="c4318-112">Følg disse trin for at læse en anmeldelse i Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="c4318-112">To read to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c4318-113">Gå til **Startside \> Anmeldelser \> Redigering**.</span><span class="sxs-lookup"><span data-stu-id="c4318-113">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="c4318-114">Brug søgefeltet øverst til højre på siden til at filtrere de anmeldelser, der vises efter produkt-id, produktnavn eller anmeldelsestekst.</span><span class="sxs-lookup"><span data-stu-id="c4318-114">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="c4318-115">Yderligere filtre giver dig mulighed for at begrænse anmeldelserne efter status periode, vurdering, kanal eller problem (fjernet, besvaret eller rapporteret).</span><span class="sxs-lookup"><span data-stu-id="c4318-115">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Startside for redigering](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="c4318-117">Besvare en anmeldelse</span><span class="sxs-lookup"><span data-stu-id="c4318-117">Respond to a review</span></span> 

<span data-ttu-id="c4318-118">Kunder, der har købt et produkt, giver jævnligt udtryk for deres tilfredshed eller utilfredshed, eller angiver i nogle tilfælde, at de ikke forstår, hvordan produktet skal bruges.</span><span class="sxs-lookup"><span data-stu-id="c4318-118">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="c4318-119">Som redaktør kan du sende et svar på en anmeldelse.</span><span class="sxs-lookup"><span data-stu-id="c4318-119">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="c4318-120">Dette svar vises sammen med anmeldelsen på webstedet.</span><span class="sxs-lookup"><span data-stu-id="c4318-120">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="c4318-121">Følg disse trin for at reagere på en anmeldelse i Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="c4318-121">To respond to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c4318-122">Gå til **Startside \> Anmeldelser \> Redigering**.</span><span class="sxs-lookup"><span data-stu-id="c4318-122">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="c4318-123">Find og vælg den anmeldelse, der kræver et svar.</span><span class="sxs-lookup"><span data-stu-id="c4318-123">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="c4318-124">Vælg **Tilføj et svar** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="c4318-124">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="c4318-125">Angiv svarteksten og det navn, der skal vises for respondenten.</span><span class="sxs-lookup"><span data-stu-id="c4318-125">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="c4318-126">Respondentens navn er som standard **Redaktør**.</span><span class="sxs-lookup"><span data-stu-id="c4318-126">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="c4318-127">Vælg **Send svar**, når du er færdig.</span><span class="sxs-lookup"><span data-stu-id="c4318-127">When you've finished, select **Post response**.</span></span>

![Besvare en anmeldelse](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="c4318-129">Fjerne en anmeldelse</span><span class="sxs-lookup"><span data-stu-id="c4318-129">Take down a review</span></span> 

<span data-ttu-id="c4318-130">Nogle gange kan redaktører være berettigede til at fjerne kunders anmeldelser af forretningsmæssige årsager.</span><span class="sxs-lookup"><span data-stu-id="c4318-130">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="c4318-131">Følg disse trin for at fjerne en anmeldelse i Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="c4318-131">To take down a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c4318-132">Gå til **Startside \> Anmeldelser \> Redigering**.</span><span class="sxs-lookup"><span data-stu-id="c4318-132">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="c4318-133">Find og vælg den anmeldelse, der skal fjernes.</span><span class="sxs-lookup"><span data-stu-id="c4318-133">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="c4318-134">Vælg en årsag til fjernelsen under **Fjern anmeldelse** i egenskabsruden til højre, og vælg derefter **Fjern**.</span><span class="sxs-lookup"><span data-stu-id="c4318-134">In the properties pane on the right, select a takedown reason under **Takedown Review**, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="c4318-135">Slette en kundes anmeldelser på kundens anmodning</span><span class="sxs-lookup"><span data-stu-id="c4318-135">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="c4318-136">Nogle gange ønsker kunderne, at deres vurderings- og anmeldelsesdata slettes permanent fra et e-handelswebsted.</span><span class="sxs-lookup"><span data-stu-id="c4318-136">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="c4318-137">En redaktør, der modtager en anmodning om fjernelse fra en kunde, kan fjerne kundens data ved hjælp af funktionen sletning af anmeldelser.</span><span class="sxs-lookup"><span data-stu-id="c4318-137">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="c4318-138">Hvis du vil søge efter og slette en kundes data, skal redaktøren bruge den e-mailadresse, som kunden har brugt til at logge på og skrive anmeldelser.</span><span class="sxs-lookup"><span data-stu-id="c4318-138">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="c4318-139">Hvis du vil finde og slette kundedata i Commerce-webstedsgenerator, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="c4318-139">To find and delete customer data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c4318-140">Gå til **Startside \> Anmeldelser \> Slet**.</span><span class="sxs-lookup"><span data-stu-id="c4318-140">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="c4318-141">Angiv kundens mailadresse i feltet **Søg efter brugere vha. mailadresse**, og vælg derefter **Søg**.</span><span class="sxs-lookup"><span data-stu-id="c4318-141">In the **Search for users by email address** box, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="c4318-142">Hvis kunden har anmeldelsesaktivitet (f.eks. indsendelse af anmeldelser, tilkendegivelser om nytten af andre kunders anmeldelser eller kommentarer til en anden kundes anmeldelse), vises resultaterne.</span><span class="sxs-lookup"><span data-stu-id="c4318-142">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="c4318-143">Knappen **Slet** vises for hvert element.</span><span class="sxs-lookup"><span data-stu-id="c4318-143">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="c4318-144">Vælg **Slet** for hvert element, der skal slettes.</span><span class="sxs-lookup"><span data-stu-id="c4318-144">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="c4318-145">Når du bliver bedt om at bekræfte, skal du vælge **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c4318-145">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Slette kundedata](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="c4318-147">Det kan tage op til syv dage, før data er fjernet fuldstændigt fra systemet.</span><span class="sxs-lookup"><span data-stu-id="c4318-147">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="c4318-148">Redaktører skal give kunderne besked om denne forsinkelse.</span><span class="sxs-lookup"><span data-stu-id="c4318-148">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="c4318-149">Hvis kunderne har ændret deres navn i deres kontoindstillinger, kan der blive vist flere elementer i søgeresultaterne.</span><span class="sxs-lookup"><span data-stu-id="c4318-149">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="c4318-150">Hvis redaktøren i sådanne tilfælde vil slette kundens data fuldstændigt, skal han eller hun vælge **Slet** for hvert element.</span><span class="sxs-lookup"><span data-stu-id="c4318-150">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="c4318-151">Hente vurderings- og anmeldelsesdata</span><span class="sxs-lookup"><span data-stu-id="c4318-151">Download ratings and reviews data</span></span>

<span data-ttu-id="c4318-152">Med Commerce-webstedsgenerator kan redaktører importere vurderings- og anmeldelsesdata samlet, så de kan analysere tendenser.</span><span class="sxs-lookup"><span data-stu-id="c4318-152">Commerce site builder lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="c4318-153">En Power BI-skabelon, der indeholder grundlæggende metrikværdier, er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="c4318-153">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="c4318-154">Redaktører kan bruge denne skabelon til at forbinde masseimporterede data med hinanden og få vist et dashboard.</span><span class="sxs-lookup"><span data-stu-id="c4318-154">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="c4318-155">Det er ikke nødvendigt at oprette et brugerdefineret dashboard.</span><span class="sxs-lookup"><span data-stu-id="c4318-155">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="c4318-156">Redaktører kan også tilpasse Power BI-skabelonen, så den opfylder deres specifikke behov.</span><span class="sxs-lookup"><span data-stu-id="c4318-156">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="c4318-157">Hvis du vil downloade vurderings- og anmeldelsesdata i Commerce-webstedsgenerator, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="c4318-157">To download ratings and reviews data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c4318-158">Gå til **Startside \> Anmeldelser \> Rapportering**.</span><span class="sxs-lookup"><span data-stu-id="c4318-158">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="c4318-159">Vælg **Hent anmeldelsesdata** for at hente vurderings- og anmeldelsesdata samlet i CSV-format (semikolonseparerede værdier).</span><span class="sxs-lookup"><span data-stu-id="c4318-159">Select **Download review data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="c4318-160">Se vurderings- og anmeldelsestendenser</span><span class="sxs-lookup"><span data-stu-id="c4318-160">View ratings and reviews trends</span></span>

<span data-ttu-id="c4318-161">Redaktører kan hente Power BI-skabelonen, så de kan få vist tendenser i et dashboard.</span><span class="sxs-lookup"><span data-stu-id="c4318-161">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="c4318-162">Hvis du vil se vurderings- og anmeldelsestendenser i Commerce-webstedsgenerator, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="c4318-162">To view ratings and reviews trends in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c4318-163">Gå til **Startside \> Anmeldelser \> Rapportering**.</span><span class="sxs-lookup"><span data-stu-id="c4318-163">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="c4318-164">Vælg **Power BI-skabelon** for at hente skabelonen.</span><span class="sxs-lookup"><span data-stu-id="c4318-164">Select **PowerBI template** to download the template.</span></span>

    ![Hent Power BI-skabelonen](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="c4318-166">Åbn den hentede skabelon ved hjælp af Power BI-appen.</span><span class="sxs-lookup"><span data-stu-id="c4318-166">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="c4318-167">Luk dialogboksen **Adgang til webindhold**, der vises, og luk derefter fejlmeddelelsen "Opdater", der vises.</span><span class="sxs-lookup"><span data-stu-id="c4318-167">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="c4318-168">Gå til **Startside**, vælg **Rediger forespørgsler**, og vælg derefter **indstillinger for datakilde**.</span><span class="sxs-lookup"><span data-stu-id="c4318-168">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="c4318-169">Vælg **Skift kilde** i dialogboksen **Indstillinger for datakilde**.</span><span class="sxs-lookup"><span data-stu-id="c4318-169">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="c4318-170">I feltet **URL-adresse** skal du angive stien til de anmeldelsesdata, du hentede i den forrige procedure (f.eks **C:\\Anmeldelser\\Anmeldelsesdata.csv**).</span><span class="sxs-lookup"><span data-stu-id="c4318-170">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![Felt med URL-adresse i dialogboksen Kommaseparerede værdier](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="c4318-172">Vælg **OK**, og vælg derefter **Anvende ændringer**.</span><span class="sxs-lookup"><span data-stu-id="c4318-172">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="c4318-173">Det tager ét til to minutter at anvende ændringerne på datakilden.</span><span class="sxs-lookup"><span data-stu-id="c4318-173">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="c4318-174">Vælg **Tendensark** for at få vist tendenser for vurderinger og anmeldelser.</span><span class="sxs-lookup"><span data-stu-id="c4318-174">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Tendenser i vurderinger og anmeldelser](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="c4318-176">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c4318-176">Additional resources</span></span>

[<span data-ttu-id="c4318-177">Oversigt over vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="c4318-177">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="c4318-178">Tilvælge brug af vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="c4318-178">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="c4318-179">Konfigurere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="c4318-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="c4318-180">Synkronisere produktvurderinger i Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="c4318-180">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
