---
title: Aktivere og konfigurere automatiske gebyrer efter kanal
description: I dette emne beskrives, hvordan du aktiverer og konfigurerer automatiske gebyrer efter kanal i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 834d90c8ec8515c6bced2d8a4fabc79b4e4e4c3e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211267"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a><span data-ttu-id="1e662-103">Aktivere og konfigurere automatiske gebyrer efter kanal</span><span class="sxs-lookup"><span data-stu-id="1e662-103">Enable and configure auto charges by channel</span></span>

<span data-ttu-id="1e662-104">I dette emne beskrives, hvordan du aktiverer og konfigurerer automatiske gebyrer (autogebyr) efter kanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1e662-104">This topic explains how to enable and configure automatic charges (auto charges) by channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1e662-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="1e662-105">Overview</span></span>

<span data-ttu-id="1e662-106">Der kan være tilfælde, hvor du skal anvende genbrugsgebyrer eller andre gebyrer på en gruppe af produkter, der sælges i alle eller nogle butikker i en bestemt stat (f.eks. Californien).</span><span class="sxs-lookup"><span data-stu-id="1e662-106">You might have scenarios where recycling fees or other fees must be applied to a group of products that are sold in all or some stores in a specific state (for example, California).</span></span> <span data-ttu-id="1e662-107">Funktionen **Aktivér filtrering af automatiske gebyrer efter kanal** i Commerce giver dig mulighed for at angive automatiske gebyrer efter kanal (f.eks. en specifik fysisk vare- og en fysisk kanal).</span><span class="sxs-lookup"><span data-stu-id="1e662-107">The **Enable filter auto charges by channel** feature in Commerce lets you specify auto charges by channel (for example, a specific brick-and-mortar channel).</span></span> <span data-ttu-id="1e662-108">Denne funktion er tilgængelig i Dynamics 365 Commerce version 10.0.10 og nyere.</span><span class="sxs-lookup"><span data-stu-id="1e662-108">This feature is available in Dynamics 365 Commerce version 10.0.10 and later.</span></span>

<span data-ttu-id="1e662-109">Hvis du vil aktivere og konfigurere automatiske gebyrer efter kanal, skal du udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="1e662-109">To enable and configure auto charges by channel, you must complete the following tasks:</span></span>

- <span data-ttu-id="1e662-110">Slå funktionen **Aktivér filtrering af automatiske gebyrer efter kanal** til.</span><span class="sxs-lookup"><span data-stu-id="1e662-110">Turn on the **Enable filter auto charges by channel** feature.</span></span>
- <span data-ttu-id="1e662-111">Konfigurer formålet med organisationshierarkier.</span><span class="sxs-lookup"><span data-stu-id="1e662-111">Configure the organization hierarchy purpose.</span></span>
- <span data-ttu-id="1e662-112">Definer automatiske gebyrer efter kanal.</span><span class="sxs-lookup"><span data-stu-id="1e662-112">Define auto charges by channel.</span></span>

> [!NOTE]
> <span data-ttu-id="1e662-113">Funktionen **Aktivér filtrering af automatiske gebyrer efter kanal** virker kun, hvis funktionen til avancerede automatiske gebyrer også er slået til.</span><span class="sxs-lookup"><span data-stu-id="1e662-113">The **Enable filter auto charges by channel** feature works only if the advanced auto charges feature is also turned on.</span></span> <span data-ttu-id="1e662-114">Du kan få flere oplysninger om, hvordan du aktiverer funktionen avancerede automatiske gebyrer, i [Avancerede automatiske gebyrer for omni-kanal](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="1e662-114">For information about how to turn on the advanced auto charges feature, see [Omni-channel advanced auto charges](omni-auto-charges.md).</span></span>

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a><span data-ttu-id="1e662-115">Slå funktionen Aktivér filtrering af automatiske gebyrer efter kanal til</span><span class="sxs-lookup"><span data-stu-id="1e662-115">Turn on the Enable filter auto charges by channel feature</span></span>

<span data-ttu-id="1e662-116">Hvis du vil aktivere automatiske gebyrer efter kanal i Commerce, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="1e662-116">To enable auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="1e662-117">Gå til **Systemadministrator \> Arbejdsområder \> Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="1e662-117">Go to **System administrator \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="1e662-118">Find og vælg **Aktivér filtrering af automatiske gebyrer efter kanal** i listen **Funktionsnavn** på fanen **Ikke aktiveret**.</span><span class="sxs-lookup"><span data-stu-id="1e662-118">On the **Not enabled** tab, in the **Feature name** list, find and select **Enable filter auto charges by channel**.</span></span>
1. <span data-ttu-id="1e662-119">Vælg **Aktivér nu** i nederste højre hjørne.</span><span class="sxs-lookup"><span data-stu-id="1e662-119">In the lower-right corner, select **Enable now**.</span></span> <span data-ttu-id="1e662-120">Når funktionen er slået til, vises den på listen under fanen **Alle**.</span><span class="sxs-lookup"><span data-stu-id="1e662-120">After the feature has been turned on, it will appear in the list on the **All** tab.</span></span>
1. <span data-ttu-id="1e662-121">Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**.</span><span class="sxs-lookup"><span data-stu-id="1e662-121">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="1e662-122">Find og vælg jobbet **1110** (**Global konfiguration**) i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="1e662-122">In the left pane, find and select the **1110** (**Global configuration**) job.</span></span>
1. <span data-ttu-id="1e662-123">Vælg **Kør nu** i handlingsruden for at overføre konfigurationsændringerne.</span><span class="sxs-lookup"><span data-stu-id="1e662-123">On the Action Pane, select **Run now** to propagate the configuration changes.</span></span>

> [!WARNING]
> <span data-ttu-id="1e662-124">Hvis du slår funktionen **Aktivér filtrering af automatiske gebyrer for kanal** fra, efter at du allerede har brugt den, vises feltet **Detailkanalrelation** under **Automatiske gebyrer** ikke længere, og du mister alle eksisterende konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="1e662-124">If you turn off the **Enable filter auto charges by channel** feature after you've already used it, the **Retail channel relation** field under **Auto charges** will no longer appear, and you will lose all existing configurations.</span></span> <span data-ttu-id="1e662-125">Hvis fjernelse af konfigurationerne af **Detailkanalrelationer** medfører, at automatiske gebyrregler duplikeres, vil et forsøg på at slå funktionen fra mislykkes.</span><span class="sxs-lookup"><span data-stu-id="1e662-125">If removal of the **Retail channel relation** configurations will cause auto charges rules to be duplicated, an attempt to turn off the feature will fail.</span></span> <span data-ttu-id="1e662-126">Før du slår for funktionen fra, skal du gennemgå alle regler for automatisk gebyrer og foretage eventuelle nødvendige ændringer.</span><span class="sxs-lookup"><span data-stu-id="1e662-126">Before you turn off the feature, be sure to review all auto charges rules and make any required changes.</span></span>

## <a name="configure-the-organization-hierarchy-purpose"></a><span data-ttu-id="1e662-127">Konfigurer formålet med organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="1e662-127">Configure the organization hierarchy purpose</span></span>

<span data-ttu-id="1e662-128">Der er oprettet et nyt formål med organisationshierarki, som hedder **Opkræv automatisk detailgebyr** for at administrere hierarkiet for automatiske gebyrer efter kanal.</span><span class="sxs-lookup"><span data-stu-id="1e662-128">A new organization hierarchy purpose that is named **Retail auto charge** has been created to manage the hierarchy for auto charges by channel.</span></span>

<span data-ttu-id="1e662-129">Hvis du vil tildele et standardhierarki til et formål med organisationshierarki i Commerce, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="1e662-129">To assign a default hierarchy to an organization hierarchy purpose in Commerce, follow these steps.</span></span>
        
1. <span data-ttu-id="1e662-130">Gå til **Organisationsadministration \> Organisationer \> Formål med organisationshierarkier**.</span><span class="sxs-lookup"><span data-stu-id="1e662-130">Go to **Organization administration \> Organizations \> Organization hierarchy purposes**.</span></span>
1. <span data-ttu-id="1e662-131">Vælg **Opkræv automatisk detailgebyr** i ruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="1e662-131">In the left pane, select **Retail auto charge**.</span></span>
1. <span data-ttu-id="1e662-132">Vælg **Tilføj** under **Tildelte hierarkier**.</span><span class="sxs-lookup"><span data-stu-id="1e662-132">Under **Assigned hierarchies**, select **Add**.</span></span>
1. <span data-ttu-id="1e662-133">Vælg et organisationshierarki f.eks. **Detailbutikker efter region** i dialogboksen **Organisationshierarkier**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e662-133">In the **Organization hierarchies** dialog box, select an organization hierarchy (for example, **Retail Stores by Region**), and then select **OK**.</span></span>
1. <span data-ttu-id="1e662-134">Vælg **Angiv som standard** under **Tildelte hierarkier**.</span><span class="sxs-lookup"><span data-stu-id="1e662-134">Under **Assigned hierarchies**, select **Set as default**.</span></span>
1. <span data-ttu-id="1e662-135">Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**.</span><span class="sxs-lookup"><span data-stu-id="1e662-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="1e662-136">Find og vælg jobbet **1040** (**Produkter**) i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="1e662-136">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="1e662-137">Vælg **Kør nu** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1e662-137">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="1e662-138">Gentag de forrige to trin for at køre jobbene **1070** (**Kanalkonfiguration**) og **1110** (**Global konfiguration**).</span><span class="sxs-lookup"><span data-stu-id="1e662-138">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>

![Konfiguration af formålet med organisationshierarkiet til automatisk debitering af detailvarer](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a><span data-ttu-id="1e662-140">Definer automatiske gebyrer efter kanal</span><span class="sxs-lookup"><span data-stu-id="1e662-140">Define auto charges by channel</span></span>

<span data-ttu-id="1e662-141">Når du har slået funktionen **Aktivér filtrering af automatiske gebyrer efter kanal** til og konfigureret formålet med organisationshierarkiet for **Detailbutikker efter region**, kan automatiske gebyrer defineres på ordrehovedniveau eller på ordrelinjeniveau.</span><span class="sxs-lookup"><span data-stu-id="1e662-141">After you've turned on the **Enable filter auto charges by channel** feature and configured the **Retail auto charge** organization hierarchy purpose, auto charges by channel can be defined at either the order header level or the order line level.</span></span>

<span data-ttu-id="1e662-142">Hvis du vil definere automatiske gebyrer efter kanal i Commerce, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="1e662-142">To define auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="1e662-143">Gå til **Debitor \> Konfiguration af gebyrer \> Automatiske gebyrer**.</span><span class="sxs-lookup"><span data-stu-id="1e662-143">Go to **Accounts receivable \> Charges setup \> Auto charges**.</span></span>
1. <span data-ttu-id="1e662-144">Vælg **Overskrift** eller **Linje** i feltet **Niveau** i ruden til venstre, afhængigt af firmaets krav.</span><span class="sxs-lookup"><span data-stu-id="1e662-144">In the left pane, in the **Level** field, select either **Header** or **Line**, depending on your business requirements.</span></span>
1. <span data-ttu-id="1e662-145">Vælg den relevante kanalkode (f.eks. **Tabel** eller **Gruppe**) i feltet **Detailkanalkode**.</span><span class="sxs-lookup"><span data-stu-id="1e662-145">In the **Retail channel code** field, select the appropriate channel code (for example, **Table** or **Group**).</span></span> <span data-ttu-id="1e662-146">Hvis standardindstillingen **Alle** bruges, anvendes gebyrreglerne på alle kanaler.</span><span class="sxs-lookup"><span data-stu-id="1e662-146">If the default setting, **All**, is used, charge rules are applied to all channels.</span></span>

    - <span data-ttu-id="1e662-147">Hvis du vælger **Gruppe**, skal du sikre dig, at der oprettes en gebyrgruppe for detailkanalen på **Retail og Commerce \> Opsætning af kanal \> Gebyrer \> Gebyrgrupper for detailkanal**.</span><span class="sxs-lookup"><span data-stu-id="1e662-147">If you select **Group**, make sure that a retail channel charges group is created at **Retail and Commerce \> Channel setup \> Charges \> Retail channel charge groups**.</span></span>
    - <span data-ttu-id="1e662-148">Hvis du vælger **Tabel**, kan du vælge en bestemt kanal (f.eks. **San Francisco**) i feltet **Detailkanalrelation**.</span><span class="sxs-lookup"><span data-stu-id="1e662-148">If you select **Table**, you can select a specific channel (for example, **San Francisco**) in the **Retail channel relation** field.</span></span>

1. <span data-ttu-id="1e662-149">Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**.</span><span class="sxs-lookup"><span data-stu-id="1e662-149">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="1e662-150">Find og vælg jobbet **1040** (**Produkter**) i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="1e662-150">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="1e662-151">Vælg **Kør nu** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1e662-151">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="1e662-152">Gentag de forrige to trin for at køre jobbene **1070** (**Kanalkonfiguration**) og **1110** (**Global konfiguration**).</span><span class="sxs-lookup"><span data-stu-id="1e662-152">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>
    
![Automatiske gebyrer defineret efter kanal](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a><span data-ttu-id="1e662-154">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="1e662-154">Example scenario</span></span>

<span data-ttu-id="1e662-155">I følgende eksempel beskrives de trin, der skal udføres for at konfigurere et produkt, så genbrugsgebyrer debiteres, når produktet sælges via en fysisk kanal i San Francisco.</span><span class="sxs-lookup"><span data-stu-id="1e662-155">The following example outlines the steps that are required to configure a product so that recycling fees are charged when the product is sold through a San Francisco brick-and-mortar channel.</span></span> <span data-ttu-id="1e662-156">I eksemplet vises også, hvordan de automatiske gebyrer vises i kasseprogrammet (POS) i Commerce.</span><span class="sxs-lookup"><span data-stu-id="1e662-156">The example also shows how the auto charges appear in the Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="1e662-157">Organisationen definerer en gebyrkode, der kaldes **GENBRUG**, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="1e662-157">The organization defines a charges code that is named **RECYCLE**, as shown in the following illustration.</span></span>

![GENBRUG-gebyrkode](media/Auto-charges-charge-code.png)

<span data-ttu-id="1e662-159">Der oprettes et automatisk gebyr på linjeniveau.</span><span class="sxs-lookup"><span data-stu-id="1e662-159">An auto charge is created at the line level.</span></span> <span data-ttu-id="1e662-160">Den har følgende konfiguration:</span><span class="sxs-lookup"><span data-stu-id="1e662-160">It has the following configuration:</span></span>

- <span data-ttu-id="1e662-161">Feltet **Kontokode** er angivet til **Alle**.</span><span class="sxs-lookup"><span data-stu-id="1e662-161">The **Account code** field is set to **All**.</span></span>
- <span data-ttu-id="1e662-162">Feltet **Varekode** er angivet til **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="1e662-162">The **Item code** field is set to **Table**.</span></span>
- <span data-ttu-id="1e662-163">Feltet **Varerelation** er angivet til produkt-id **91001**.</span><span class="sxs-lookup"><span data-stu-id="1e662-163">The **Item relation** field is set to product ID **91001**.</span></span>
- <span data-ttu-id="1e662-164">Feltet **Kode for leveringsmåde** er angivet til **Alle**.</span><span class="sxs-lookup"><span data-stu-id="1e662-164">The **Mode of delivery code** field is set to **All**.</span></span>
- <span data-ttu-id="1e662-165">Feltet **Detailkanalkode** er angivet til **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="1e662-165">The **Retail channel code** field is set to **Table**.</span></span>
- <span data-ttu-id="1e662-166">Feltet **Detailkanalrelation** er angivet til lageret i **San Francisco**.</span><span class="sxs-lookup"><span data-stu-id="1e662-166">The **Retail channel relation** field is set to the **San Francisco** store.</span></span>

<span data-ttu-id="1e662-167">Der oprettes en automatisk gebyrlinje.</span><span class="sxs-lookup"><span data-stu-id="1e662-167">An auto charges line is created.</span></span> <span data-ttu-id="1e662-168">Den har følgende konfiguration:</span><span class="sxs-lookup"><span data-stu-id="1e662-168">It has the following configuration:</span></span>

- <span data-ttu-id="1e662-169">Feltet **Valuta** er angivet til **USD**.</span><span class="sxs-lookup"><span data-stu-id="1e662-169">The **Currency** field is set to **USD**.</span></span>
- <span data-ttu-id="1e662-170">Feltet **Gebyrkode** er angivet til **GENBRUG**.</span><span class="sxs-lookup"><span data-stu-id="1e662-170">The **Charges code** field is set to **RECYCLE**.</span></span>
- <span data-ttu-id="1e662-171">Feltet **Kategori** er angivet til **Fast**.</span><span class="sxs-lookup"><span data-stu-id="1e662-171">The **Category** field is set to **Fixed**.</span></span>
- <span data-ttu-id="1e662-172">Feltet **Gebyrer** er angivet til **$6,25**.</span><span class="sxs-lookup"><span data-stu-id="1e662-172">The **Charges** field is set to **$6.25**.</span></span>

![Konfiguration af automatisk gebyrer for linjeniveau og den automatiske gebyrlinje](media/Auto-charges-recyclingfee-line-fee.png)

<span data-ttu-id="1e662-174">I kasseprogrammet oprettes der en salgsordre i lagerkanalen **San Francisco**.</span><span class="sxs-lookup"><span data-stu-id="1e662-174">In the POS application, a sales order is created in the **San Francisco** store channel.</span></span> <span data-ttu-id="1e662-175">Linjen **Gebyrer** viser genbrugsgebyret på **$6,25**.</span><span class="sxs-lookup"><span data-stu-id="1e662-175">The **Charges** line shows the recycling fee of **$6.25**.</span></span>

<span data-ttu-id="1e662-176">Når du vælger **Transaktionsindstillinger \> Gebyrer \> Administrer gebyrer** i kasseprogrammet, kan du få vist gebyrkoden og beskrivelsen for genbrugsgebyret.</span><span class="sxs-lookup"><span data-stu-id="1e662-176">By selecting **Transaction options \> Charges \> Manage charges** in the POS application, you can view the charges code and description for the recycling fee.</span></span>

![Genbrugsgebyr i kasseprogrammet](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a><span data-ttu-id="1e662-178">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="1e662-178">Additional resources</span></span>

[<span data-ttu-id="1e662-179">Avancerede automatiske gebyrer for omni-kanal</span><span class="sxs-lookup"><span data-stu-id="1e662-179">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="1e662-180">Beregne hovedgebyrer forholdsmæssigt på matchende salgslinjer</span><span class="sxs-lookup"><span data-stu-id="1e662-180">Prorate header charges to matching sales lines</span></span>](pro-rate-charges-matching-lines.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]