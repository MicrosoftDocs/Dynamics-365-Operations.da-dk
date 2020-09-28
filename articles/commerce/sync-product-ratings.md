---
title: Synkroniser produktvurderinger i Dynamics 365 Commerce
description: Dette emne beskriver, hvordan du synkroniserer produktvurderinger i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: dec87b548f3a218e1f833b752305f373e893b14c
ms.sourcegitcommit: 58d7133ae9909fa205730e3cf4c7fd5a1d5d0b75
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/10/2020
ms.locfileid: "3793581"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a><span data-ttu-id="32986-103">Synkroniser produktvurderinger i Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="32986-103">Sync product ratings in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="32986-104">Dette emne beskriver, hvordan du synkroniserer produktvurderinger i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="32986-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="32986-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="32986-105">Overview</span></span>

<span data-ttu-id="32986-106">Hvis du vil bruge produktvurderinger i omni-kanaler som f.eks. på POS og i callcentre, skal produktvurderinger fra vurderings- og anmeldelsestjenesten importeres til Commerce-kanalens database.</span><span class="sxs-lookup"><span data-stu-id="32986-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Commerce channel database.</span></span> <span data-ttu-id="32986-107">Når produktvurderinger stilles til rådighed i omni-kanaler, kan de hjælpe kunder indirekte under deres interaktioner med salgsmedarbejdere.</span><span class="sxs-lookup"><span data-stu-id="32986-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="32986-108">Dette emne beskriver følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="32986-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="32986-109">Konfigurer **Synkroniseringsjob for produktvurderinger** som et batchjob for at synkronisere produktvurderinger fra **Tjenesten Vurderinger og anmeldelser**.</span><span class="sxs-lookup"><span data-stu-id="32986-109">Configure **Product ratings sync job** as a batch job to synchronize product ratings from the **Ratings and Reviews service**.</span></span>
1. <span data-ttu-id="32986-110">Kontrollere, at batchjobbet til synkronisering af produktvurderinger er fuldført.</span><span class="sxs-lookup"><span data-stu-id="32986-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="32986-111">Gøre produktvurderinger tilgængelige ved POS.</span><span class="sxs-lookup"><span data-stu-id="32986-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a><span data-ttu-id="32986-112">Konfigurere et batchjob for at synkronisere produktvurderinger</span><span class="sxs-lookup"><span data-stu-id="32986-112">Configure a batch job to synchronize product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="32986-113">Før du går i gang, skal du kontrollere, at version 10.0.6 eller nyere af Dynamics 365 Commerce er installeret.</span><span class="sxs-lookup"><span data-stu-id="32986-113">Before you start, make sure that version 10.0.6 or later of Dynamics 365 Commerce is installed.</span></span>

### <a name="initialize-the-commerce-scheduler"></a><span data-ttu-id="32986-114">Initialisere Commerce-planlægger</span><span class="sxs-lookup"><span data-stu-id="32986-114">Initialize the commerce scheduler</span></span>

<span data-ttu-id="32986-115">Hvis du vil initialisere Commerce-planlæggeren, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="32986-115">To initialize the commerce scheduler, follow these steps.</span></span>

1. <span data-ttu-id="32986-116">Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-planlægger \> Initialiser Commerce-planlægger**.</span><span class="sxs-lookup"><span data-stu-id="32986-116">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Initialize commerce scheduler**.</span></span> <span data-ttu-id="32986-117">Du kan også søge efter "Initialiser Commerce-planlægger".</span><span class="sxs-lookup"><span data-stu-id="32986-117">Alternatively, search for "Initialize commerce scheduler."</span></span>
1. <span data-ttu-id="32986-118">I dialogboksen **Initialiser Commerce-planlægger** skal du kontrollere, at indstillingen **Slet eksisterende konfiguration** er angivet til **Nej**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="32986-118">In the **Initialize commerce scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="32986-119">Kontrollere RetailProductRating-underjobbet</span><span class="sxs-lookup"><span data-stu-id="32986-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="32986-120">Udfør følgende trin for at kontrollere, om **RetailProductRating**-underjobbet findes:</span><span class="sxs-lookup"><span data-stu-id="32986-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="32986-121">Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-planlægger \> Planlæggerunderjob**.</span><span class="sxs-lookup"><span data-stu-id="32986-121">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="32986-122">Du kan også søge efter "Planlæggerunderjob".</span><span class="sxs-lookup"><span data-stu-id="32986-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="32986-123">Find eller søg efter **RetailProductRating**-underjobbet på listen over underjob.</span><span class="sxs-lookup"><span data-stu-id="32986-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="32986-124">I følgende illustration vises et eksempel på siden detaljer om underjob i Commerce.</span><span class="sxs-lookup"><span data-stu-id="32986-124">The following illustration shows an example of the subjob details in Commerce.</span></span>

![Detaljer om RetailProductRating-underjobbet](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="32986-126">Hvis du ikke kan finde **RetailProductRating**-underjobbet, har du måske allerede kørt jobbet **Synkroniser produktvurderinger** og **1040 CDX**-jobbet, før du initialiserede Commerce-planlæggeren.</span><span class="sxs-lookup"><span data-stu-id="32986-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the Commerce scheduler.</span></span> <span data-ttu-id="32986-127">I dette tilfælde skal du følge disse trin for at køre jobbet **Fuld datasynkronisering**.</span><span class="sxs-lookup"><span data-stu-id="32986-127">In this case, follow these steps to run the **Full data sync** job.</span></span>

> 1. <span data-ttu-id="32986-128">Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-planlægger \> Kanaldatabase**.</span><span class="sxs-lookup"><span data-stu-id="32986-128">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span> <span data-ttu-id="32986-129">Du kan også søge efter "Kanaldatabase".</span><span class="sxs-lookup"><span data-stu-id="32986-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="32986-130">Vælg den kanaldatabase, der skal synkroniseres.</span><span class="sxs-lookup"><span data-stu-id="32986-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="32986-131">Vælg **Fuld datasynkronisering** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="32986-131">On the action pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="32986-132">Vælg **1040 - produkter** i dialogboksen **Vælg en distributionsplan**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="32986-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="32986-133">Gentag trinnene i den forrige procedure for at kontrollere, at **RetailProductRating**-underjobbet er oprettet.</span><span class="sxs-lookup"><span data-stu-id="32986-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="32986-134">Importere produktvurderinger</span><span class="sxs-lookup"><span data-stu-id="32986-134">Import product ratings</span></span>

<span data-ttu-id="32986-135">Udfør følgende trin for at importere produktvurderinger til Commerce fra vurderings- og anmeldelsestjenesten.</span><span class="sxs-lookup"><span data-stu-id="32986-135">To import product ratings into Commerce from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="32986-136">Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-planlægger \> Synkroniser produktvurderingsjob**.</span><span class="sxs-lookup"><span data-stu-id="32986-136">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="32986-137">Du kan også søge efter "Synkroniser produktvurderingsjob".</span><span class="sxs-lookup"><span data-stu-id="32986-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="32986-138">Vælg **Gentages** i oversigtspanelet **Kør i baggrunden** i dialogboksen **Hent produktvurderinger**.</span><span class="sxs-lookup"><span data-stu-id="32986-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="32986-139">Angiv et gentagelsesmønster i dialogboksen **Definer gentagelse**.</span><span class="sxs-lookup"><span data-stu-id="32986-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="32986-140">(Den foreslåede værdi er to timer). Planlæg ikke en gentagelse, der er mindre end én time.</span><span class="sxs-lookup"><span data-stu-id="32986-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="32986-141">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="32986-141">Select **OK**.</span></span>
1. <span data-ttu-id="32986-142">Angiv indstillingen **Batchbehandling** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="32986-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="32986-143">Denne indstilling er med til at sikre, at du kan overvåge logfilerne og kontrollere status for batchjob, der kører.</span><span class="sxs-lookup"><span data-stu-id="32986-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="32986-144">Vælg **OK** for at planlægge batchjobbet.</span><span class="sxs-lookup"><span data-stu-id="32986-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="32986-145">I følgende illustration vises et eksempel på konfiguration af batchjob i Commerce.</span><span class="sxs-lookup"><span data-stu-id="32986-145">The following illustration shows an example of batch job configuration in Commerce.</span></span>

![Konfiguration af batchjobbet Synkroniser produktvurderinger](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="32986-147">Kontrollere, at batchjobbet til synkronisering af produktvurderinger er fuldført</span><span class="sxs-lookup"><span data-stu-id="32986-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="32986-148">Benyt følgende fremgangsmåde for at kontrollere, at batchjobbet **Synkroniser produktvurderinger** lykkedes.</span><span class="sxs-lookup"><span data-stu-id="32986-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="32986-149">Gå til **Retail og Commerce \> Systemadministrator \> Forespørgsler \> Batchjob** eller, hvis du bruger en ren Commerce-lagerbeholdning (SKU), **Retail og Commerce \> Forespørgsler og-rapporter \> Batchjob** i stedet.</span><span class="sxs-lookup"><span data-stu-id="32986-149">Go to **Retail and Commerce \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Commerce-only stock keeping unit (SKU), **Retail and Commerce \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="32986-150">Du kan også søge efter "Batchjob".</span><span class="sxs-lookup"><span data-stu-id="32986-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="32986-151">Hvis du vil have vist detaljerne om batchjobbet, skal du søge efter en beskrivelse, der indeholder "Hent produktvurderinger" i kolonnen **Jobbeskrivelse**, på batchjob-listen.</span><span class="sxs-lookup"><span data-stu-id="32986-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="32986-152">Vælg et job-id for at få vist oplysninger om batchjobbet, f.eks. planlagt startdato/tidspunkt og gentagelsesteksten.</span><span class="sxs-lookup"><span data-stu-id="32986-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="32986-153">I følgende illustration vises et eksempel på oplysningerne om batchjobbet i Commerce, når batchjobbet er planlagt til at køre med to timers intervaller.</span><span class="sxs-lookup"><span data-stu-id="32986-153">The following illustration shows an example of the batch job details in Commerce when the batch job is scheduled to run at two-hour intervals.</span></span>

![Detaljer om batchjobbet Synkroniser produktvurdering](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="32986-155">Gøre produktvurderinger tilgængelige ved POS</span><span class="sxs-lookup"><span data-stu-id="32986-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="32986-156">Vurderings- og anmeldelsesløsningen i Dynamics 365 Commerce er en omni-kanalløsning.</span><span class="sxs-lookup"><span data-stu-id="32986-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="32986-157">Produktvurderinger vises dog ikke som standard ved POS.</span><span class="sxs-lookup"><span data-stu-id="32986-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="32986-158">Hvis du vil hjælpe kunder i butikkerne med at se vurderinger og anmeldelser, når de bliver hjulpet af salgsassistenter, skal du aktivere produktvurderinger ved POS.</span><span class="sxs-lookup"><span data-stu-id="32986-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="32986-159">Hvis du vil aktivere produktvurderinger ved POS, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="32986-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="32986-160">Gå til **Retail og Commerce \> Konfiguration af Commerce \> Parametre \> Commerce-parametre**.</span><span class="sxs-lookup"><span data-stu-id="32986-160">Go to **Retail and Commerce \> Commerce setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="32986-161">Du kan også søge efter "Commerce-parametre".</span><span class="sxs-lookup"><span data-stu-id="32986-161">Alternatively, search for "Commerce parameters."</span></span>
1. <span data-ttu-id="32986-162">Vælg **Ny** under fanen **Konfigurationsparametre**.</span><span class="sxs-lookup"><span data-stu-id="32986-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="32986-163">Angiv et navn som f.eks **RatingsAndReviews.EnableProductRatingsForRetailStores**, og angiv værdien til **sand**.</span><span class="sxs-lookup"><span data-stu-id="32986-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="32986-164">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="32986-164">Select **Save**.</span></span>
1. <span data-ttu-id="32986-165">Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**.</span><span class="sxs-lookup"><span data-stu-id="32986-165">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span> <span data-ttu-id="32986-166">Du kan også søge efter "Distributionsplan".</span><span class="sxs-lookup"><span data-stu-id="32986-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="32986-167">På joblisten skal du vælge **1110** (**Global konfiguration**) og derefter vælge **Kør nu**.</span><span class="sxs-lookup"><span data-stu-id="32986-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="32986-168">Når jobbet er kørt korrekt, skal du kontrollere, at produktvurderinger nu vises ved POS.</span><span class="sxs-lookup"><span data-stu-id="32986-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="32986-169">I følgende illustration vises et eksempel på konfigurationen af Commerce-parametrene for at aktivere produktvurderinger ved POS.</span><span class="sxs-lookup"><span data-stu-id="32986-169">The following illustration shows an example of the configuration of the Commerce parameters to turn on product ratings at the POS.</span></span>

![Konfiguration af Commerce-parametre for produktvurderinger ved POS](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="32986-171">I følgende illustration vises et eksempel på produktvurderinger ved POS.</span><span class="sxs-lookup"><span data-stu-id="32986-171">The following illustration shows an example of product ratings at the POS.</span></span>

![Produktvurderinger ved POS](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="32986-173">I følgende illustration vises et eksempel på produktvurderinger i callcenter-kanaler.</span><span class="sxs-lookup"><span data-stu-id="32986-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![Produktvurderinger i en callcenter-kanal](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="32986-175">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="32986-175">Additional resources</span></span>

[<span data-ttu-id="32986-176">Oversigt over vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="32986-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="32986-177">Tilvælge brug af vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="32986-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="32986-178">Administrere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="32986-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="32986-179">Konfigurere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="32986-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)
