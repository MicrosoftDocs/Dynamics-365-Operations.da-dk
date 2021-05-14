---
title: Understøttelse af momsfunktion til flytteordrer
description: Dette emne forklarer den nye understøttelse af momsfunktionen til flytteordrer ved hjælp af tjenesten til beregning af moms.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d1b99046b0e439c9dadbb240050e270a7b2a6914
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920949"
---
# <a name="tax-feature-support-for-transfer-orders"></a><span data-ttu-id="6c602-103">Understøttelse af momsfunktion til flytteordrer</span><span class="sxs-lookup"><span data-stu-id="6c602-103">Tax feature support for transfer orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6c602-104">Dette emne indeholder oplysninger om momsberegning og bogføringsintegration i flytteordrer.</span><span class="sxs-lookup"><span data-stu-id="6c602-104">This topic provides information about tax calculation and posting integration in transfer orders.</span></span> <span data-ttu-id="6c602-105">Denne funktionalitet giver dig mulighed for at konfigurere momsberegning og bogføring i flytteordrer til lageroverførsler.</span><span class="sxs-lookup"><span data-stu-id="6c602-105">This functionality lets you set up tax calculation and posting in transfer orders for stock transfers.</span></span> <span data-ttu-id="6c602-106">I henhold til EU's regler om moms betragtes lageroverførsler som fællesskabsforsyninger og -anskaffelser inden for EU.</span><span class="sxs-lookup"><span data-stu-id="6c602-106">Under European Union (EU) value-added tax (VAT) regulations, stock transfers are considered intra-community supply and intra-community acquisitions.</span></span>

<span data-ttu-id="6c602-107">Hvis du vil konfigurere og bruge denne funktion, skal du udføre tre hovedtrin:</span><span class="sxs-lookup"><span data-stu-id="6c602-107">To configure and use this functionality, you must complete three main steps:</span></span>

1. <span data-ttu-id="6c602-108">**RCS-konfiguration:** I Regulatory Configuration Service skal du konfigurere momsfunktionen, momskoder og momskoders anvendelighed for bestemmelse af momskode i flytteordrer.</span><span class="sxs-lookup"><span data-stu-id="6c602-108">**RCS setup:** In Regulatory Configuration Service, set up the tax feature, tax codes, and tax codes applicability for tax code determination in transfer orders.</span></span>
2. <span data-ttu-id="6c602-109">**Finance-opsætning:** I Microsoft Dynamics 365 Finance kan du aktivere funktionen **Moms i flytteordre**, konfigurere parametrene for momstjenesten til lageret og konfigurere kernemomsparametre.</span><span class="sxs-lookup"><span data-stu-id="6c602-109">**Finance setup:** In Microsoft Dynamics 365 Finance, turn on the **Tax in transfer order** feature, set up the tax service parameters for inventory, and set up core tax parameters.</span></span>
3. <span data-ttu-id="6c602-110">**Lageropsætning:** Konfigurer lagerkonfigurationen for flytteordreposteringer.</span><span class="sxs-lookup"><span data-stu-id="6c602-110">**Inventory setup:** Set up the inventory configuration for transfer order transactions.</span></span>

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a><span data-ttu-id="6c602-111">Konfigurere RCS til moms- og flytteordretransaktioner</span><span class="sxs-lookup"><span data-stu-id="6c602-111">Set up RCS for tax and transfer order transactions</span></span>

<span data-ttu-id="6c602-112">Benyt følgende fremgangsmåde for at konfigurere momsen for en flytteordre.</span><span class="sxs-lookup"><span data-stu-id="6c602-112">Follow these steps to set up the tax that is involved in a transfer order.</span></span> <span data-ttu-id="6c602-113">I det eksempel, der vises her, er flytteordren fra Nederlandene til Belgien.</span><span class="sxs-lookup"><span data-stu-id="6c602-113">In the example that is shown here, the transfer order is from the Netherlands to Belgium.</span></span>

1. <span data-ttu-id="6c602-114">Vælg kladdefunktionsversionen under fanen **Versioner** på siden **Momsfunktioner**, og vælg derefter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="6c602-114">On the **Tax features** page, on the **Versions** tab, select the draft feature version, and then select **Edit**.</span></span>

    ![Vælge Rediger](../media/image1.png)

2. <span data-ttu-id="6c602-116">Vælg **Tilføj** under fanen **Momskoder** på siden **Konfiguration af momsfunktioner** for at oprette nye momskoder.</span><span class="sxs-lookup"><span data-stu-id="6c602-116">On the **Tax features setup** page, on the **Tax codes** tab, select **Add** to create new tax codes.</span></span> <span data-ttu-id="6c602-117">I dette eksempel er der oprettet tre momskoder: **NL-Exempt**, **BE-RC-21** og **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="6c602-117">For this example, three tax codes are created: **NL-Exempt**, **BE-RC-21**, and **BE-RC+21**.</span></span>

    - <span data-ttu-id="6c602-118">Når en flytteordre afsendes fra et lagersted i Nederlandene, anvendes Nederlandenes momsfritagelseskode (**NL-Exempt**).</span><span class="sxs-lookup"><span data-stu-id="6c602-118">When a transfer order is shipped from a warehouse in the Netherlands, the Netherlands VAT exempted tax code (**NL-Exempt**) is applied.</span></span>
      
        <span data-ttu-id="6c602-119">Opret momskoden **NL-Exempt**.</span><span class="sxs-lookup"><span data-stu-id="6c602-119">Create the tax code **NL-Exempt**.</span></span>
        1. <span data-ttu-id="6c602-120">Vælg **Tilføj**, og angiv **NL-Exempt** i feltet **Momskode**.</span><span class="sxs-lookup"><span data-stu-id="6c602-120">Select **Add**, enter **NL-Exempt** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="6c602-121">Vælg **Efter nettobeløb** i feltet **Momskomponent**.</span><span class="sxs-lookup"><span data-stu-id="6c602-121">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="6c602-122">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6c602-122">Select **Save**.</span></span>
        4. <span data-ttu-id="6c602-123">Vælg **Tilføj** i tabellen **Sats**.</span><span class="sxs-lookup"><span data-stu-id="6c602-123">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="6c602-124">Skift **Er momsfri** til **Ja** i afsnittet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="6c602-124">Swtich **Is Exempt** to **Yes** in the **General** section.</span></span>

        ![NL-Exempt momskode](../media/image2.png)

    - <span data-ttu-id="6c602-126">Når en flytteordre modtages på et lagersted i Belgien, anvendes modtagermomsmekanismen med momskoderne **BE-RC-21** og **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="6c602-126">When a transfer order is received at a Belgium warehouse, the reverse charge mechanism is applied by using the **BE-RC-21** and **BE-RC+21** tax codes.</span></span>
        
        <span data-ttu-id="6c602-127">Opret momskoden **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="6c602-127">Create the tax code **BE-RC-21**.</span></span>      
        1. <span data-ttu-id="6c602-128">Vælg **Tilføj**, og angiv **BE-RC-21** i feltet **Momskode**.</span><span class="sxs-lookup"><span data-stu-id="6c602-128">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="6c602-129">Vælg **Efter nettobeløb** i feltet **Momskomponent**.</span><span class="sxs-lookup"><span data-stu-id="6c602-129">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="6c602-130">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6c602-130">Select **Save**.</span></span>
        4. <span data-ttu-id="6c602-131">Vælg **Tilføj** i tabellen **Sats**.</span><span class="sxs-lookup"><span data-stu-id="6c602-131">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="6c602-132">Angiv **-21** i feltet **Momssats**.</span><span class="sxs-lookup"><span data-stu-id="6c602-132">Enter **-21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="6c602-133">Skift **Er modtagermoms** til **Ja** i afsnittet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="6c602-133">Swtich **Is Reverse Charge** to **Yes** in the **General** section.</span></span>
        7. <span data-ttu-id="6c602-134">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6c602-134">Select **Save**.</span></span>

        ![BE-RC-21-momskode for modtagermoms](../media/image3.png)
        
        <span data-ttu-id="6c602-136">Opret momskoden **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="6c602-136">Create the tax code **BE-RC+21**.</span></span>
        1. <span data-ttu-id="6c602-137">Vælg **Tilføj**, og angiv **BE-RC-21** i feltet **Momskode**.</span><span class="sxs-lookup"><span data-stu-id="6c602-137">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="6c602-138">Vælg **Efter nettobeløb** i feltet **Momskomponent**.</span><span class="sxs-lookup"><span data-stu-id="6c602-138">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="6c602-139">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6c602-139">Select **Save**.</span></span>
        4. <span data-ttu-id="6c602-140">Vælg **Tilføj** i tabellen **Sats**.</span><span class="sxs-lookup"><span data-stu-id="6c602-140">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="6c602-141">Angiv **21** i feltet **Momssats**.</span><span class="sxs-lookup"><span data-stu-id="6c602-141">Enter **21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="6c602-142">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6c602-142">Select **Save**.</span></span>

        ![BE-RC+21-momskode for modtagermoms](../media/image4.png)

3. <span data-ttu-id="6c602-144">Definer anvendeligheden af momskoderne.</span><span class="sxs-lookup"><span data-stu-id="6c602-144">Define the applicability of the tax codes.</span></span>

    1. <span data-ttu-id="6c602-145">Vælg **Administrer kolonner**, og vælg derefter kolonner, der skal bruges til at opbygge anvendelighedstabellen.</span><span class="sxs-lookup"><span data-stu-id="6c602-145">Select **Manage columns**, and then select columns that should be used to build the applicability table.</span></span>

        > [!NOTE]
        > <span data-ttu-id="6c602-146">Sørg for at føje kolonnerne **Forretningsproces** og **Momsretninger** til tabellen.</span><span class="sxs-lookup"><span data-stu-id="6c602-146">Be sure to add the **Business process** and **Tax directions** columns to the table.</span></span> <span data-ttu-id="6c602-147">Begge kolonner er vigtige for momsfunktionen i flytteordrer.</span><span class="sxs-lookup"><span data-stu-id="6c602-147">Both columns are essential to the functionality for tax in transfer orders.</span></span>

    2. <span data-ttu-id="6c602-148">Tilføj anvendelighedsregler.</span><span class="sxs-lookup"><span data-stu-id="6c602-148">Add applicability rules.</span></span> <span data-ttu-id="6c602-149">Lad ikke felterne **Momskoder**, **Momsgruppe** og **Varemomsgruppe** være tomme.</span><span class="sxs-lookup"><span data-stu-id="6c602-149">Don't leave the **Tax codes**, **Tax group**, and **Item tax group** fields blank.</span></span>
        
        <span data-ttu-id="6c602-150">Tilføj en ny regel for forsendelse af flytteordre.</span><span class="sxs-lookup"><span data-stu-id="6c602-150">Add a new rule for transfer order shipment.</span></span>
        1. <span data-ttu-id="6c602-151">Vælg **Tilføj** i tabellen **Anvendelighedsregler**.</span><span class="sxs-lookup"><span data-stu-id="6c602-151">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="6c602-152">Vælg **Lager** i feltet **Forretningsproces** for at gøre reglen gældende for en flytteordre.</span><span class="sxs-lookup"><span data-stu-id="6c602-152">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="6c602-153">I feltet **Afsend fra land/område** skal du angive **NLD**.</span><span class="sxs-lookup"><span data-stu-id="6c602-153">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="6c602-154">I feltet **Levér til land/område** skal du angive **BEL**.</span><span class="sxs-lookup"><span data-stu-id="6c602-154">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="6c602-155">Vælg **Output** i feltet **Momsretning** for at gøre reglen gældende for forsendelse af flytteordre.</span><span class="sxs-lookup"><span data-stu-id="6c602-155">In the **Tax direction** field, select **Output** to make the rule applicable to transfer order shipment.</span></span>
        6. <span data-ttu-id="6c602-156">Vælg **NL-Exempt** i feltet **Momskoder**.</span><span class="sxs-lookup"><span data-stu-id="6c602-156">In the **Tax codes** field, select **NL-Exempt**.</span></span>
        7. <span data-ttu-id="6c602-157">Angiv den relaterede momsgruppe og varemomsgruppe, der er defineret i dit Finance-system, i feltet **Momsgruppe** og **Varemomsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="6c602-157">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>
        
        <span data-ttu-id="6c602-158">Tilføj en ny regel for modtagelse af flytteordre.</span><span class="sxs-lookup"><span data-stu-id="6c602-158">Add another rule for transfer order receipt.</span></span>
        1. <span data-ttu-id="6c602-159">Vælg **Tilføj** i tabellen **Anvendelighedsregler**.</span><span class="sxs-lookup"><span data-stu-id="6c602-159">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="6c602-160">Vælg **Lager** i feltet **Forretningsproces** for at gøre reglen gældende for en flytteordre.</span><span class="sxs-lookup"><span data-stu-id="6c602-160">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="6c602-161">I feltet **Afsend fra land/område** skal du angive **NLD**.</span><span class="sxs-lookup"><span data-stu-id="6c602-161">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="6c602-162">I feltet **Levér til land/område** skal du angive **BEL**.</span><span class="sxs-lookup"><span data-stu-id="6c602-162">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="6c602-163">Vælg **Input** i feltet **Momsretning** for at gøre reglen gældende for modtagelse af flytteordre.</span><span class="sxs-lookup"><span data-stu-id="6c602-163">In the **Tax direction** field, select **Input** to make the rule applicable to transfer order receipt.</span></span>
        6. <span data-ttu-id="6c602-164">Vælg **BE-RC+21** og **BE-RC-21** i feltet **Momskoder**.</span><span class="sxs-lookup"><span data-stu-id="6c602-164">In the **Tax codes** field, select **BE-RC+21** and **BE-RC-21**.</span></span>
        7. <span data-ttu-id="6c602-165">Angiv den relaterede momsgruppe og varemomsgruppe, der er defineret i dit Finance-system, i feltet **Momsgruppe** og **Varemomsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="6c602-165">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>

        ![Anvendelighedsregler](../media/image5.png)

4. <span data-ttu-id="6c602-167">Fuldfør og publicer den nye momsfunktionsversion.</span><span class="sxs-lookup"><span data-stu-id="6c602-167">Complete and publish the new tax feature version.</span></span>

    <span data-ttu-id="6c602-168">[![Ændre status for den nye version](../media/image6.png)](../media/image6.png)</span><span class="sxs-lookup"><span data-stu-id="6c602-168">[![Changing the status of the new version](../media/image6.png)](../media/image6.png)</span></span>

## <a name="set-up-finance-for-transfer-order-transactions"></a><span data-ttu-id="6c602-169">Konfigurere Finance til moms- og flytteordretransaktioner</span><span class="sxs-lookup"><span data-stu-id="6c602-169">Set up Finance for transfer order transactions</span></span>

<span data-ttu-id="6c602-170">Hvis du vil aktivere og konfigurere moms til flytteordrer, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="6c602-170">Follow these steps to enable and set up taxes for transfer orders.</span></span>

1. <span data-ttu-id="6c602-171">Gå i Finance til **Arbejdsområder** \> **Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="6c602-171">In Finance, go to **Workspaces** \> **Feature management**.</span></span>
2. <span data-ttu-id="6c602-172">Find og vælg funktionen **Moms i flytteordre** på listen, og vælg derefter **Aktivér nu** for at aktivere den.</span><span class="sxs-lookup"><span data-stu-id="6c602-172">In the list, find and select the **Tax in transfer order** feature, and then select **Enable now** to turn it on.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="6c602-173">Funktionen **Moms i flytteordre** er fuldstændig afhængig af momstjenesten.</span><span class="sxs-lookup"><span data-stu-id="6c602-173">The **Tax in transfer order** feature is fully dependent on the tax service.</span></span> <span data-ttu-id="6c602-174">Du kan derfor kun aktivere den, når du har installeret momstjenesten.</span><span class="sxs-lookup"><span data-stu-id="6c602-174">Therefore, it can be turned on only after you've installed the tax service.</span></span>

    ![Funktionen Moms i flytteordre](../media/image7.png)

3. <span data-ttu-id="6c602-176">Aktivér momstjenesten, og vælg forretningsprocessen **Lager**.</span><span class="sxs-lookup"><span data-stu-id="6c602-176">Enable the tax service, and select the **Inventory** business process.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="6c602-177">Du skal udføre dette trin for hver juridiske enhed i Finance, hvor momstjenesten og funktionerne for moms i flytteordrer skal være tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="6c602-177">You must complete this step for each legal entity in Finance where you want the tax service and the functionality for tax in transfer orders to be available.</span></span>

    1. <span data-ttu-id="6c602-178">Gå til **Moms** \> **Konfiguration** \> **Momskonfiguration** \> **Konfiguration af momstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="6c602-178">Go to **Tax** \> **Setup** \> **Tax configuration** \> **Tax service setup**.</span></span>
    2. <span data-ttu-id="6c602-179">Vælg **Lager** i feltet **Forretningsproces**.</span><span class="sxs-lookup"><span data-stu-id="6c602-179">In the **Business process** field, select **Inventory**.</span></span>

    ![Angive feltet Forretningsproces](../media/image8.png)

4. <span data-ttu-id="6c602-181">Kontrollér, at modtagermomsmekanisme er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="6c602-181">Verify that the reverse charge mechanism is set up.</span></span> <span data-ttu-id="6c602-182">Gå til **Finans** \> **Konfiguration** \> **Parametre**, og sørg for, at fanen **Modtagermoms** har indstillingen **Aktivér modtagermoms** angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6c602-182">Go to **General ledger** \> **Setup** \> **Parameters**, and then, on the **Reverse charge** tab, verify that the **Enable reverse charge** option is set to **Yes**.</span></span>

    ![Aktivere indstilling for modtagermoms](../media/image9.png)

5. <span data-ttu-id="6c602-184">Kontrollér, at de relaterede momskoder, momsgrupper, varemomsgrupper og momsregistreringsnumre er konfigureret i Finance i overensstemmelse med vejledningerne for momstjenesten.</span><span class="sxs-lookup"><span data-stu-id="6c602-184">Verify that the related tax codes, tax groups, item tax groups, and VAT registration numbers have been set up in Finance according to the tax service guidance.</span></span>
6. <span data-ttu-id="6c602-185">Konfigurere en konto til foreløbig transit.</span><span class="sxs-lookup"><span data-stu-id="6c602-185">Set up an interim transit account.</span></span> <span data-ttu-id="6c602-186">Dette trin er kun påkrævet, når den moms, der anvendes på en flytteordre, ikke gælder for en momsfritagelses eller modtagermomsmekanisme.</span><span class="sxs-lookup"><span data-stu-id="6c602-186">This step is required only when the tax that is applied to a transfer order isn't applicable to a tax exempted or reverse charge mechanism.</span></span>

    1. <span data-ttu-id="6c602-187">Gå til **Moms** \> **Konfiguration** \> **Moms** \> **Finanskonteringsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="6c602-187">Go to **Tax** \> **Setup** \> **Sales tax** \> **Ledger posting groups**.</span></span>
    2. <span data-ttu-id="6c602-188">Vælg en finanskonto i feltet **Foreløbig transit**.</span><span class="sxs-lookup"><span data-stu-id="6c602-188">In the **Interim transit** field, select a ledger account.</span></span>

    ![Vælge en konto til foreløbig transit](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a><span data-ttu-id="6c602-190">Konfigurere basislager flytteordretransaktioner</span><span class="sxs-lookup"><span data-stu-id="6c602-190">Set up basic inventory for transfer order transactions</span></span>

<span data-ttu-id="6c602-191">Benyt følgende fremgangsmåde for at konfigurere basislager for at aktivere flytteordretransaktioner.</span><span class="sxs-lookup"><span data-stu-id="6c602-191">Follow these steps to set up basic inventory to enable transfer order transactions.</span></span>

1. <span data-ttu-id="6c602-192">Opret afsendelse fra- og afsendelse til-steder for lagersteder i forskellige lande eller områder, og tilføj den primære adresse for hvert sted.</span><span class="sxs-lookup"><span data-stu-id="6c602-192">Create ship-from and ship-to sites for your warehouses in different countries or regions, and add the primary address for each site.</span></span>

    1. <span data-ttu-id="6c602-193">Gå til **Lokationsstyring** \> **Konfiguration** \> **Lagersted** \> **Sted**.</span><span class="sxs-lookup"><span data-stu-id="6c602-193">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Sites**.</span></span>
    2. <span data-ttu-id="6c602-194">Vælg **Ny** for at oprette det sted, du vil tildele et lagersted senere.</span><span class="sxs-lookup"><span data-stu-id="6c602-194">Select **New** to create the site that you will assign to a warehouse later.</span></span>
    3. <span data-ttu-id="6c602-195">Gentag trin 2 for alle de andre steder, du skal oprette.</span><span class="sxs-lookup"><span data-stu-id="6c602-195">Repeat step 2 for all the other sites that you must create.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6c602-196">Et af de steder, du opretter, skal kaldes **Transit**.</span><span class="sxs-lookup"><span data-stu-id="6c602-196">One of the sites that you create should be named **Transit**.</span></span> <span data-ttu-id="6c602-197">I senere trin af denne procedure skal du tildele dette sted til transitlagerstedet, så momsrelaterede lagerbilag kan bogføres i "afsendelses"- og "modtagelses"-transaktioner for flytteordrer.</span><span class="sxs-lookup"><span data-stu-id="6c602-197">In later steps of this procedure, you will assign this site to the transit warehouse, so that tax-related inventory vouchers can be posted in "ship" and "receive" transactions for transfer orders.</span></span> <span data-ttu-id="6c602-198">Adressen på transitstedet er irrelevant for momsberegningen.</span><span class="sxs-lookup"><span data-stu-id="6c602-198">The address of the transit site is irrelevant to tax calculation.</span></span> <span data-ttu-id="6c602-199">Du kan derfor lade feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="6c602-199">Therefore, you can leave it blank.</span></span>

    ![Konfigurere steder](../media/image11.png)

2. <span data-ttu-id="6c602-201">Opret afsend fra-, transit- og afsend til-lagersteder.</span><span class="sxs-lookup"><span data-stu-id="6c602-201">Create ship-from, transit, and ship-to warehouses.</span></span> <span data-ttu-id="6c602-202">Alle adresseoplysninger, der vedligeholdes på et lagersted, tilsidesætter stedadressen under momsberegningen.</span><span class="sxs-lookup"><span data-stu-id="6c602-202">Any address information that is maintained in a warehouse will override the site address during tax calculation.</span></span>

    1. <span data-ttu-id="6c602-203">Gå til **Lokationsstyring** \> **Konfiguration** \> **Lagersted** \> **Lagersteder**.</span><span class="sxs-lookup"><span data-stu-id="6c602-203">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Warehouses**.</span></span>
    2. <span data-ttu-id="6c602-204">Vælg **Ny** for at oprette et lagersted og tildele det tilhørende sted.</span><span class="sxs-lookup"><span data-stu-id="6c602-204">Select **New** to create a warehouse, and assign it to the corresponding site.</span></span>
    3. <span data-ttu-id="6c602-205">Gentag trin 2 for at oprette et lagersted for hvert sted efter behov.</span><span class="sxs-lookup"><span data-stu-id="6c602-205">Repeat step 2 to create a warehouse for each site as required.</span></span>

    ![Konfigurere lagersteder](../media/image12.png)

    > [!NOTE]
    > <span data-ttu-id="6c602-207">I forbindelse med et afsendelse fra-lagersted skal der vælges et transitlagersted i feltet **Transitlagersted** for flytteordretransaktioner.</span><span class="sxs-lookup"><span data-stu-id="6c602-207">For a ship-from warehouse, a transit warehouse must be selected in the **Transit warehouse** field for transfer order transactions.</span></span>
    >
    > ![Vælge et transitlagersted](../media/image13.png)

3. <span data-ttu-id="6c602-209">Sørg for, at lagerbogføringen er konfigureret for flytteordretransaktioner.</span><span class="sxs-lookup"><span data-stu-id="6c602-209">Verify that the inventory posting configuration is set up for transfer order transactions.</span></span>

    1. <span data-ttu-id="6c602-210">Gå til **Lagerstyring** \> **Konfiguration** \> **Bogføring** \> **Bogføring**.</span><span class="sxs-lookup"><span data-stu-id="6c602-210">Go to **Inventory management** \> **Setup** \> **Posting** \> **Posting**.</span></span>
    2. <span data-ttu-id="6c602-211">Kontrollér, at der er konfigureret en finanskonto til både **Lagerafgang** og **Lagertilgang** under fanen **Lager**.</span><span class="sxs-lookup"><span data-stu-id="6c602-211">On the **Inventory** tab, verify that a ledger account is set up for both **Inventory issue** and **Inventory receipt** posting.</span></span>

        ![Konfigurere bogføring af lagertilgang og lagerafgang](../media/image14.png)

    3. <span data-ttu-id="6c602-213">Kontrollér, at der er konfigureret en finanskonto til bogføring af **Intern kreditor**.</span><span class="sxs-lookup"><span data-stu-id="6c602-213">Verify that a ledger account is set up for **Inter-unit payable** posting.</span></span>

        ![Konfigurere bogføring af intern kreditor](../media/image15.png)

    4. <span data-ttu-id="6c602-215">Kontrollér, at der er konfigureret en finanskonto til bogføring af **Intern debitor**.</span><span class="sxs-lookup"><span data-stu-id="6c602-215">Verify that a ledger account is set up for **Inter-unit receivable** posting.</span></span>

        ![Konfigurere bogføring af intern debitor](../media/image16.png)
