---
title: Konfigurere BOPIS i et  Dynamics 365 Commerce-evalueringsmiljø
description: Dette emne forklarer, hvordan du konfigurerer køb online, afhent i butikken (BOPIS) i et Microsoft Dynamics 365 Commerce-evalueringsmiljø, efter at det er blevet klargjort.
author: rubendel
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 219504da62fd4637ed01f9acbab32f873cef81b0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795949"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="935b3-103">Konfigurere BOPIS i et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="935b3-103">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="935b3-104">Dette emne forklarer, hvordan du konfigurerer køb online, afhent i butikken (BOPIS) i et Microsoft Dynamics 365 Commerce-evalueringsmiljø, efter at miljøet er blevet klargjort.</span><span class="sxs-lookup"><span data-stu-id="935b3-104">This topic explains how to configure buy online, pickup in store (BOPIS) in a Microsoft Dynamics 365 Commerce evaluation environment after the environment has been provisioned.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="935b3-105">Forudsætning</span><span class="sxs-lookup"><span data-stu-id="935b3-105">Prerequisite</span></span>

<span data-ttu-id="935b3-106">Fuldfør kun procedurerne i dette emne, efter dit Commerce-evalueringsmiljø er klargjort og konfigureret.</span><span class="sxs-lookup"><span data-stu-id="935b3-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned and configured.</span></span> <span data-ttu-id="935b3-107">Oplysninger om, hvordan du klargør og konfigurerer dit miljø, finder du under [Klargøre et Dynamics 365 Commerce-evalueringsmiljø](provisioning-guide.md) og [Konfigurere et Dynamics 365 Commerce-evalueringsmiljø](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span><span class="sxs-lookup"><span data-stu-id="935b3-107">For information about how to provision and configure your environment, see [Provision a Dynamics 365 Commerce evaluation environment](provisioning-guide.md) and [Configure a Dynamics 365 Commerce evaluation environment](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span></span>

<span data-ttu-id="935b3-108">Når Commerce-miljøet er blevet klargjort og konfigureret fra ende til anden, kan du bruge dette emne til at aktivere BOPIS-scenarier.</span><span class="sxs-lookup"><span data-stu-id="935b3-108">After your Commerce environment has been provisioned and configured end to end, you can use this topic to enable BOPIS scenarios.</span></span>

## <a name="configure-the-pos"></a><span data-ttu-id="935b3-109">Konfigurere POS</span><span class="sxs-lookup"><span data-stu-id="935b3-109">Configure the POS</span></span>

### <a name="configure-modern-pos"></a><span data-ttu-id="935b3-110">Konfigurere Modern POS</span><span class="sxs-lookup"><span data-stu-id="935b3-110">Configure Modern POS</span></span>

<span data-ttu-id="935b3-111">BOPIS-scenarier, der involverer en kreditkortbetaling, kræver en hardwarestation.</span><span class="sxs-lookup"><span data-stu-id="935b3-111">BOPIS scenarios that involve a credit card payment require a hardware station.</span></span> <span data-ttu-id="935b3-112">Hardwarestationen er indbygget i Modern POS til Windows og Android-klienter.</span><span class="sxs-lookup"><span data-stu-id="935b3-112">The hardware station is built into Modern POS for Windows and Android clients.</span></span> <span data-ttu-id="935b3-113">Hvis du bruger Cloud POS eller Modern POS til iOS, skal POS-klienten kombineres med en delt hardwarestation.</span><span class="sxs-lookup"><span data-stu-id="935b3-113">If you're using Cloud POS or Modern POS for iOS, the point of sale (POS) client must be paired with a shared hardware station.</span></span> <span data-ttu-id="935b3-114">Dette emne forklarer, hvordan du kan konfigurere BOPIS til Windows- og Android-klienter.</span><span class="sxs-lookup"><span data-stu-id="935b3-114">This topic explains how to configure BOPIS for Windows and Android clients.</span></span> <span data-ttu-id="935b3-115">Du kan finde oplysninger om, hvordan du konfigurerer en delt hardwarestationen, under [Konfigurere og installere Retail-hardwarestation](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span><span class="sxs-lookup"><span data-stu-id="935b3-115">For information about how to set up a shared hardware station, see [Configure and install Retail hardware station](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span></span>

1. <span data-ttu-id="935b3-116">Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> Kasseapparater**.</span><span class="sxs-lookup"><span data-stu-id="935b3-116">Go to **Retail and Commerce \> Channel setup \> POS setup \> Registers**.</span></span>
2. <span data-ttu-id="935b3-117">Vælg kasseapparatet **SANFRAN-5**, og vælg derefter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="935b3-117">Select register **SANFRAN-5**, and then select **Edit**.</span></span>
3. <span data-ttu-id="935b3-118">Rediger værdien i feltet **Hardwareprofil** fra **HW002** til **HW001**, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="935b3-118">Change the value of the **Hardware profile** field from **HW002** to **HW001**, and then select **Save**.</span></span>
4. <span data-ttu-id="935b3-119">Gå til **Retail og Commerce \> Retail og CommerceIT \> Distributionsplan** for at synkronisere ændringerne.</span><span class="sxs-lookup"><span data-stu-id="935b3-119">To synchronize the changes, go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="935b3-120">Vælg distributionsplanen **1090**, og vælg derefter **Kør nu** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="935b3-120">Select distribution schedule **1090**, and then, on the Action Pane, select **Run now**.</span></span>
6. <span data-ttu-id="935b3-121">Vælg **Ja** og derefter **OK** for at starte datasynkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="935b3-121">Select **Yes** and then **OK** to initiate data synchronization.</span></span> 

### <a name="install-modern-pos"></a><span data-ttu-id="935b3-122">Installere Modern POS</span><span class="sxs-lookup"><span data-stu-id="935b3-122">Install Modern POS</span></span>

1. <span data-ttu-id="935b3-123">Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> Enheder**.</span><span class="sxs-lookup"><span data-stu-id="935b3-123">Go to **Retail and Commerce \> Channel setup \> POS setup \> Devices**.</span></span>
2. <span data-ttu-id="935b3-124">Vælg enheden **SANFRANCIS-5**.</span><span class="sxs-lookup"><span data-stu-id="935b3-124">Select device **SANFRANCIS-5**.</span></span>
3. <span data-ttu-id="935b3-125">I handlingsruden skal du vælge **Download** og derefter vælge **Konfigurationsfil**.</span><span class="sxs-lookup"><span data-stu-id="935b3-125">On the Action Pane, select **Download**, and then select **Configuration file**.</span></span>
4. <span data-ttu-id="935b3-126">Vælg **Download**, og vælg derefter **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="935b3-126">Select **Download**, and then select **Retail Modern POS**.</span></span> 
5. <span data-ttu-id="935b3-127">Når overførslen af filen **ModernPOSSetup.exe** er fuldført, skal du vælge **Åbn fil**.</span><span class="sxs-lookup"><span data-stu-id="935b3-127">When download of the **ModernPOSSetup.exe** file is completed, select **Open file**.</span></span>

    ![Åbn fil](./dev-itpro/media/PAYMENTS/openfile.png)

6. <span data-ttu-id="935b3-129">Vælg **Næste** for at gennemgå installationsprocessen.</span><span class="sxs-lookup"><span data-stu-id="935b3-129">Select **Next** to go through the installation process.</span></span> <span data-ttu-id="935b3-130">Vælg **Luk**, når installationen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="935b3-130">When installation is completed, select **Close**.</span></span>

### <a name="activate-modern-pos"></a><span data-ttu-id="935b3-131">Aktivere Modern POS</span><span class="sxs-lookup"><span data-stu-id="935b3-131">Activate Modern POS</span></span>

1. <span data-ttu-id="935b3-132">Vælg knappen **Start** på skrivebordet i Windows, og angiv **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="935b3-132">On the Windows desktop, select the **Start** button, and enter **Retail Modern POS**.</span></span>
2. <span data-ttu-id="935b3-133">Vælg **Retail Modern POS**-programmet for at starte aktivering.</span><span class="sxs-lookup"><span data-stu-id="935b3-133">Select the **Retail Modern POS** application to initiate activation.</span></span>
3. <span data-ttu-id="935b3-134">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="935b3-134">Select **Next**.</span></span> <span data-ttu-id="935b3-135">Felterne **Serverens URL-adresse**, **Enheds-id** og **Kassenummer** skal forudindstilles ved hjælp af oplysningerne fra den konfigurationsfil, du har downloadet i den foregående procedure.</span><span class="sxs-lookup"><span data-stu-id="935b3-135">The **Server URL**, **Device ID**, and **Register number** fields should be preset by using information from the configuration file that you downloaded in the previous procedure.</span></span>
4. <span data-ttu-id="935b3-136">Vælg **Aktivér**.</span><span class="sxs-lookup"><span data-stu-id="935b3-136">Select **Activate**.</span></span>
5. <span data-ttu-id="935b3-137">Der vises en godkendelsesdialogboks.</span><span class="sxs-lookup"><span data-stu-id="935b3-137">An authentication dialog box appears.</span></span> <span data-ttu-id="935b3-138">Vælg den konto, der bruger den mailadresse, der tidligere er knyttet til arbejderen **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="935b3-138">Select the account that uses the email address that was previously associated with worker **000713 - Andrew Collette**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="935b3-139">Hvis du endnu ikke har knyttet en arbejder til din identitet, lykkes aktiveringen ikke.</span><span class="sxs-lookup"><span data-stu-id="935b3-139">If you haven't yet associated a worker with your identity, activation will be unsuccessful.</span></span> <span data-ttu-id="935b3-140">I dette tilfælde skal du følge trinnene i afsnittet "Knytte en arbejder til din identitet" under emnet [Konfigurere et Dynamics 365 Commerce-evalueringsmiljø](cpe-post-provisioning.md#associate-a-worker-with-your-identity).</span><span class="sxs-lookup"><span data-stu-id="935b3-140">In this case, follow the steps under the "Associate a worker with your identity" section in the [Configure a Dynamics 365 Commerce evaluation environment](cpe-post-provisioning.md#associate-a-worker-with-your-identity) topic.</span></span>
    
6. <span data-ttu-id="935b3-141">Når du bliver bedt om at lade din organisation administrere enheden, skal du vælge **Kun denne app**.</span><span class="sxs-lookup"><span data-stu-id="935b3-141">When you're prompted to let your organization manage the device, select **This app only**.</span></span>
7. <span data-ttu-id="935b3-142">Vælg **Kom i gang**, når aktiveringen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="935b3-142">When activation is completed, select **Get started**.</span></span>

### <a name="enable-bopis-in-modern-pos"></a><span data-ttu-id="935b3-143">Aktivere BOPIS i Modern POS</span><span class="sxs-lookup"><span data-stu-id="935b3-143">Enable BOPIS in Modern POS</span></span>

1. <span data-ttu-id="935b3-144">Log på Modern POS med **000713** som operatør-id og **123** som adgangskode.</span><span class="sxs-lookup"><span data-stu-id="935b3-144">Sign in to Modern POS by using **000713** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="935b3-145">Mens videoen med gennemgang af introduktion afspilles, skal du markere de to afkrydsningsfelter i nederste venstre hjørne af dialogboksen og derefter lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="935b3-145">While the introductory walkthrough video is playing, select the two check boxes in the lower-left corner of the dialog box, and then close the dialog box.</span></span>
3. <span data-ttu-id="935b3-146">Hvis du ikke bliver bedt om at lukke skiftet, skal du rulle til højre på **velkomstsiden**, vælge **Luk skifte** og derefter logge på POS igen.</span><span class="sxs-lookup"><span data-stu-id="935b3-146">If you aren't prompted to close the shift, scroll to the right on the **Welcome** page, select **Close shift**, and then sign back in to the POS.</span></span>
4. <span data-ttu-id="935b3-147">Når du er logget på, skal du vælge **Udfør handling uden om kasseskuffe**, når du bliver bedt om det.</span><span class="sxs-lookup"><span data-stu-id="935b3-147">After you're signed in, when you're prompted, select **Perform a non-drawer operation**.</span></span>
5. <span data-ttu-id="935b3-148">Rul til højre på **velkomstsiden**, og vælg handlingen **Vælg hardwarestation**.</span><span class="sxs-lookup"><span data-stu-id="935b3-148">On the **Welcome** page, scroll to the right, and select the **Select hardware station** operation.</span></span>
6. <span data-ttu-id="935b3-149">Vælg **Administrer**, angiv indstillingen **Brug hardwarestation** til **Slået til**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="935b3-149">Select **Manage**, set the **Use hardware station** option to **On**, and then select **OK**.</span></span>
7. <span data-ttu-id="935b3-150">Log af POS, og log derefter på igen.</span><span class="sxs-lookup"><span data-stu-id="935b3-150">Sign out of the POS, and then sign back in.</span></span>
8. <span data-ttu-id="935b3-151">Når du er logget på, skal du vælge **Åbn et nyt skifte** og derefter vælge **Kasseskuffe**.</span><span class="sxs-lookup"><span data-stu-id="935b3-151">After you're signed in, select **Open a new shift**, and then select **Drawer**.</span></span>

## <a name="complete-a-bopis-scenario"></a><span data-ttu-id="935b3-152">Fuldføre et BOPIS-scenarie</span><span class="sxs-lookup"><span data-stu-id="935b3-152">Complete a BOPIS scenario</span></span>

### <a name="create-a-storefront-order-for-in-store-pickup"></a><span data-ttu-id="935b3-153">Oprette en butiksordre til afhentning i butikken</span><span class="sxs-lookup"><span data-stu-id="935b3-153">Create a storefront order for in-store pickup</span></span>

1. <span data-ttu-id="935b3-154">Gå til den URL-adresse, du har angivet i afsnittet [Initialisere e-handel](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) under konfigurationen af miljøet.</span><span class="sxs-lookup"><span data-stu-id="935b3-154">Go to the URL that you specified in the [Initialize e-Commerce](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) step during environment configuration.</span></span>
2. <span data-ttu-id="935b3-155">Vælg en vare, og vælg **Føj til indkøbsvogn**.</span><span class="sxs-lookup"><span data-stu-id="935b3-155">Select an item, and select **Add to cart**.</span></span>
3. <span data-ttu-id="935b3-156">Vælg **Afhent** for den ordrelinje, du lige har tilføjet, på siden med indkøbsposen.</span><span class="sxs-lookup"><span data-stu-id="935b3-156">On the shopping bag page, select **Pick this up** for the order line that you just added.</span></span>
4. <span data-ttu-id="935b3-157">Skriv **San Francisco** i dialogboksen **Vælg en butik**, og vælg derefter knappen **Søg**.</span><span class="sxs-lookup"><span data-stu-id="935b3-157">In the **Select a store** dialog box, enter **San Francisco**, and then select the **Search** button.</span></span>
5. <span data-ttu-id="935b3-158">Find San Francisco-butikken på listen med resultater, og vælg **Afhent her**.</span><span class="sxs-lookup"><span data-stu-id="935b3-158">In the list of results, find the San Francisco store, and select **Pick up here**.</span></span>
6. <span data-ttu-id="935b3-159">Vælg **Betal som gæst** på siden med indkøbsposen.</span><span class="sxs-lookup"><span data-stu-id="935b3-159">On the shopping bag page, select **Checkout as Guest**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="935b3-160">Hvis du vil fortsætte med betaling, skal du acceptere cookie-beskeden.</span><span class="sxs-lookup"><span data-stu-id="935b3-160">To continue with checkout, you must accept the cookie notice.</span></span> <span data-ttu-id="935b3-161">Denne meddelelse vises som et banner øverst på betalingssiden.</span><span class="sxs-lookup"><span data-stu-id="935b3-161">This notice appears as a banner at the top of the checkout page.</span></span>

7. <span data-ttu-id="935b3-162">Angiv følgende oplysninger for kreditkortets betalingsmetode:</span><span class="sxs-lookup"><span data-stu-id="935b3-162">For the credit card payment method, enter the following details:</span></span>

    - <span data-ttu-id="935b3-163">**Kortindehaverens navn:** Angiv et navn.</span><span class="sxs-lookup"><span data-stu-id="935b3-163">**Cardholder name:** Enter any name.</span></span>
    - <span data-ttu-id="935b3-164">**Kortnummer:** Angiv **4111-1111-1111-1111**.</span><span class="sxs-lookup"><span data-stu-id="935b3-164">**Card number:** Enter **4111-1111-1111-1111**.</span></span>
    - <span data-ttu-id="935b3-165">**Udløbsdato:** Angiv **20-10**.</span><span class="sxs-lookup"><span data-stu-id="935b3-165">**Expiration date:** Enter **10/20**.</span></span>
    - <span data-ttu-id="935b3-166">**Værdi for kontrolnummer på kreditkort (CVV):** Angiv **737**.</span><span class="sxs-lookup"><span data-stu-id="935b3-166">**Card verification value (CVV) code:** Enter **737**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="935b3-167">Forsøg aldrig under nogen omstændigheder at bruge faktiske kreditkortoplysninger på testwebstedet.</span><span class="sxs-lookup"><span data-stu-id="935b3-167">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

8. <span data-ttu-id="935b3-168">Fortsæt med betaling ved at angive detaljer om faktureringsadressen, og vælg derefter **Gem og fortsæt**.</span><span class="sxs-lookup"><span data-stu-id="935b3-168">Continue with checkout by entering details of the billing address, and then select **Save and continue**.</span></span>
9. <span data-ttu-id="935b3-169">Vælg **Betaling ved kassen**, når ordren er klar til at blive afgivet.</span><span class="sxs-lookup"><span data-stu-id="935b3-169">When the order is ready to be placed, select **Checkout**.</span></span>

### <a name="synchronize-online-orders-to-the-back-office"></a><span data-ttu-id="935b3-170">Synkronisere onlineordrer til administrationen</span><span class="sxs-lookup"><span data-stu-id="935b3-170">Synchronize online orders to the back office</span></span>

<span data-ttu-id="935b3-171">Du kan finde oplysninger om, hvordan du synkroniserer onlineordrer, under [Bogføre onlinesalg og -betalinger](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span><span class="sxs-lookup"><span data-stu-id="935b3-171">For information about how to synchronize online orders, see [Posting of online sales and payments](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span></span>

### <a name="pick-up-an-order-in-the-store"></a><span data-ttu-id="935b3-172">Afhente en ordre i butikken</span><span class="sxs-lookup"><span data-stu-id="935b3-172">Pick up an order in the store</span></span>

1. <span data-ttu-id="935b3-173">Log på POS'et.</span><span class="sxs-lookup"><span data-stu-id="935b3-173">Sign in to the POS.</span></span>
2. <span data-ttu-id="935b3-174">På **velkomstsiden** skal du vælge **Ordreopfyldning**</span><span class="sxs-lookup"><span data-stu-id="935b3-174">On the **Welcome** screen, select **Order fulfillment**</span></span>
3. <span data-ttu-id="935b3-175">Vælg linjen fra den ordre, der blev afgivet online, på listen over varer til afhentning.</span><span class="sxs-lookup"><span data-stu-id="935b3-175">In the list of items for pickup, select the line from the order that was placed online.</span></span>
4. <span data-ttu-id="935b3-176">Når ordrelinjen er valgt, skal du vælge **Afhent**.</span><span class="sxs-lookup"><span data-stu-id="935b3-176">While the order line is selected, select **Pick up**.</span></span>

    <span data-ttu-id="935b3-177">Linjevaren føjes til transaktionsskærmbilledet, og **$0,00** vises som den skyldige saldo.</span><span class="sxs-lookup"><span data-stu-id="935b3-177">The line item is added to the transaction screen, and **$0.00** is shown as the balance that is due.</span></span>

5. <span data-ttu-id="935b3-178">Vælg forfaldne saldo på **0,00**, eller vælg en betalingsmåde for at afslutte transaktionen.</span><span class="sxs-lookup"><span data-stu-id="935b3-178">Select the balance due of **$0.00**, or select any payment method to conclude the transaction.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="935b3-179">Fejlfinding</span><span class="sxs-lookup"><span data-stu-id="935b3-179">Troubleshooting</span></span>

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a><span data-ttu-id="935b3-180">Onlineordrer, der hentes i POS, har en forfaldssaldo på nul.</span><span class="sxs-lookup"><span data-stu-id="935b3-180">Online orders that are retrieved in the POS have a non-zero balance due</span></span>

<span data-ttu-id="935b3-181">Når der hentes en ordre for en butiksafhentning, og den forfaldne saldo ikke er 0 (nul), skal du sørge for, at Modern POS bruges, og at hardwarestationen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="935b3-181">When an order is retrieved for in-store pickup, if the balance due isn't 0 (zero), make sure that Modern POS is being used, and that the hardware station is active.</span></span> <span data-ttu-id="935b3-182">Hvis der bruges Cloud POS eller Modern POS til iOS, skal du kontrollere, at en delt hardwarestation er aktiv.</span><span class="sxs-lookup"><span data-stu-id="935b3-182">If Cloud POS or Modern POS for iOS is being used, make sure that a shared hardware station is active.</span></span> <span data-ttu-id="935b3-183">En form for aktiv hardwarestation kræves for at hente betalinger, der er foretaget online.</span><span class="sxs-lookup"><span data-stu-id="935b3-183">Some form of active hardware station is required to retrieve payments that were made online.</span></span>

### <a name="general-issues-with-payment-capture"></a><span data-ttu-id="935b3-184">Generelle problemer med betalingsregistrering</span><span class="sxs-lookup"><span data-stu-id="935b3-184">General issues with payment capture</span></span>

<span data-ttu-id="935b3-185">Ved alle generelle problemer skal du altid konsultere hændelseslogfilerne for hardwarestationen Modern POS eller Internet Information Services (IIS) som første trin.</span><span class="sxs-lookup"><span data-stu-id="935b3-185">For all general issues, you should always consult the Modern POS or Internet Information Services (IIS) Hardware Station event logs as a first step.</span></span> <span data-ttu-id="935b3-186">Du kan finde disse logfiler under følgende noder i hændelseslogfilen for Windows:</span><span class="sxs-lookup"><span data-stu-id="935b3-186">You can find these logs under the following nodes in the Windows event log:</span></span>

- <span data-ttu-id="935b3-187">Logfiler for programmer og tjenester \> Microsoft \> Dynamics \> Commerce-ModernPOS</span><span class="sxs-lookup"><span data-stu-id="935b3-187">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-ModernPOS</span></span>
- <span data-ttu-id="935b3-188">Logfiler for programmer og tjenester \> Microsoft \> Dynamics \> Commerce-Hardware Station</span><span class="sxs-lookup"><span data-stu-id="935b3-188">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Hardware Station</span></span>

## <a name="additional-resources"></a><span data-ttu-id="935b3-189">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="935b3-189">Additional resources</span></span>

[<span data-ttu-id="935b3-190">Oversigt over Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="935b3-190">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="935b3-191">Klargøre et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="935b3-191">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="935b3-192">Konfigurere valgfrie funktioner til et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="935b3-192">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="935b3-193">Ofte stillede spørgsmål om Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="935b3-193">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="935b3-194">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="935b3-194">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="935b3-195">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="935b3-195">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="935b3-196">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="935b3-196">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="935b3-197">Dynamics 365 Commerce-websted</span><span class="sxs-lookup"><span data-stu-id="935b3-197">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="935b3-198">Adyen-betalingsconnector</span><span class="sxs-lookup"><span data-stu-id="935b3-198">Adyen payment connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[<span data-ttu-id="935b3-199">Gemme onlinebetalingsmidler med Adyen-connector</span><span class="sxs-lookup"><span data-stu-id="935b3-199">Saving online payment instruments with the Adyen connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[<span data-ttu-id="935b3-200">Oversigt over omni-kanalbetalinger</span><span class="sxs-lookup"><span data-stu-id="935b3-200">Omni-channel payments overview</span></span>](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)


[!INCLUDE[footer-include](../includes/footer-banner.md)]