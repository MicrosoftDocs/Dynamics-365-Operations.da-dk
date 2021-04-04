---
title: Konfigurer parametrene for et ER-format for hver juridisk enhed
description: I dette emne forklares det, hvordan du kan konfigurere parametrene for det Elektroniske rapporteringsformat, der er angivet for den enkelte juridiske enhed.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: eebca6575a0b23f75baabbb91727f498de44d9cb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570704"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a><span data-ttu-id="dc866-103">Konfigurer parametrene for et ER-format for hver juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="dc866-103">Set up the parameters of an ER format per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="dc866-104">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="dc866-104">Prerequisites</span></span>

<span data-ttu-id="dc866-105">For at fuldføre disse trin, skal du først fuldføre trinnene i emnet [Konfigurer ER-formaterne for at bruge de parametre, der er angivet for hver juridiske enhed](er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="dc866-105">To complete these steps, you must first complete the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span>

<span data-ttu-id="dc866-106">For at fuldføre eksemplerne i dette emne, skal du have adgang til Microsoft Dynamics 365 Finance (Finance) i en af følgende roller:</span><span class="sxs-lookup"><span data-stu-id="dc866-106">To complete the examples in this topic, you must have access to Microsoft Dynamics 365 Finance (Finance) for one of the following roles:</span></span>

- <span data-ttu-id="dc866-107">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="dc866-107">Electronic reporting developer</span></span>
- <span data-ttu-id="dc866-108">Funktionel konsulent i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="dc866-108">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="dc866-109">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="dc866-109">System administrator</span></span>

## <a name="import-er-configurations"></a><span data-ttu-id="dc866-110">Importér ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="dc866-110">Import ER configurations</span></span>

1.  <span data-ttu-id="dc866-111">Log på dit miljø.</span><span class="sxs-lookup"><span data-stu-id="dc866-111">Sign in to your environment.</span></span>
2.  <span data-ttu-id="dc866-112">Vælg **Elektronisk rapportering** på standarddashboardet.</span><span class="sxs-lookup"><span data-stu-id="dc866-112">On the default dashboard, select **Electronic reporting**.</span></span>
3.  <span data-ttu-id="dc866-113">Vælg **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="dc866-113">Select **Reporting configurations**.</span></span>
4.  <span data-ttu-id="dc866-114">Importerer de konfigurationer, du har eksporteret fra Regulatory Configuration Services (RCS), til den aktuelle forekomst af Finance, mens du fuldførte trinnene i emnet [Konfigurer ER-formater, så du kan bruge de parametre, der er angivet for hver juridiske enhed](er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="dc866-114">Import, into the current instance of Finance, the configurations that you exported from Regulatory Configuration Services (RCS) while you were completing the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span> <span data-ttu-id="dc866-115">Benyt følgende fremgangsmåde for hver enkelt konfiguration af Elektronisk rapportering (ER) i følgende rækkefølge: datamodel, modeltilknytning og formater.</span><span class="sxs-lookup"><span data-stu-id="dc866-115">Follow these steps for each Electronic reporting (ER) configuration, in the following order: data model, model mapping, and formats.</span></span>

    1. <span data-ttu-id="dc866-116">Vælg **Udveksling \> Indlæs fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="dc866-116">Select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="dc866-117">Vælg **Gennemse** for at vælge filen til den krævede ER-konfiguration i XML-format.</span><span class="sxs-lookup"><span data-stu-id="dc866-117">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="dc866-118">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc866-118">Select **OK**.</span></span>
    
    <span data-ttu-id="dc866-119">I følgende illustration vises de konfigurationer, du skal have, når du er færdig.</span><span class="sxs-lookup"><span data-stu-id="dc866-119">The following illustration shows the configurations that you must have when you've finished.</span></span>

    ![Siden ER-konfigurationer](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a><span data-ttu-id="dc866-121">Angiv parametrene for DEMF-firmaet</span><span class="sxs-lookup"><span data-stu-id="dc866-121">Set up parameters for the DEMF company</span></span>

<span data-ttu-id="dc866-122">Du kan bruge ER-strukturen til at konfigurere programspecifikke parametre for et ER-format.</span><span class="sxs-lookup"><span data-stu-id="dc866-122">You can use the ER framework to set up application-specific parameters for an ER format.</span></span>

1.  <span data-ttu-id="dc866-123">Vælg den juridiske enhed **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="dc866-123">Select the **DEMF** legal entity.</span></span>
2.  <span data-ttu-id="dc866-124">I konfigurationstræet skal du vælge elementet **Format for at lære, hvordan man slår LE-data op**.</span><span class="sxs-lookup"><span data-stu-id="dc866-124">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
3.  <span data-ttu-id="dc866-125">I handlingsruden på fanen **Konfigurationer** skal du i gruppen **Programspecifikke parametre** vælge **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="dc866-125">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>

    ![Siden med ER-programspecifikke parametre](./media/GER-AppSpecParms-LookupForm.PNG)
    
    <span data-ttu-id="dc866-127">På siden **Programspecifikke parametre** kan du konfigurere reglerne for datakilden **Vælger** for formatet **Format til at lære, hvordan man leder efter LE-data**.</span><span class="sxs-lookup"><span data-stu-id="dc866-127">On the **Application specific parameters** page, you can configure the rules for the **Selector** data source of the **Format to learn how to lookup LE data** format.</span></span>
    
    <span data-ttu-id="dc866-128">Hvis basis-ER-formatet indeholder flere datakilder af typen **Opslag**, skal du vælge den ønskede datakilde i oversigtspanelet **Opslag**, før du kan konfigurere regelsættet for datakilden.</span><span class="sxs-lookup"><span data-stu-id="dc866-128">If the base ER format will contain several data sources of the **Lookup** type, you must select the desired data source on the **Lookups** FastTab before you can start to configure the set of rules for the data source.</span></span>
    
    <span data-ttu-id="dc866-129">For hver datakilde kan du konfigurere separate regler for hver version af det valgte ER-format.</span><span class="sxs-lookup"><span data-stu-id="dc866-129">For each data source, you can configure separate rules for each version of the selected ER format.</span></span>
    
    <span data-ttu-id="dc866-130">Hele regelsættet for alle opslagsdatakilder, der er tilgængelige i den valgte version af basis-ER-formatet, udgør de programspecifikke parametre for ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="dc866-130">The whole set of rules for all lookup data sources that are available in the selected version of the base ER format makes up the application-specific parameters for the ER format.</span></span>

4.  <span data-ttu-id="dc866-131">Vælg version **1.1.1** af ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="dc866-131">Select version **1.1.1** of the ER format.</span></span>
5.  <span data-ttu-id="dc866-132">Vælg **Tilføj** i oversigtspanelet **Betingelser**.</span><span class="sxs-lookup"><span data-stu-id="dc866-132">On the **Conditions** FastTab, select **Add**.</span></span>
6.  <span data-ttu-id="dc866-133">I feltet **Kode** for den nye post skal du vælge rullelistens pil for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="dc866-133">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="dc866-134">Opslaget viser listen over de momskoder, der kan vælges.</span><span class="sxs-lookup"><span data-stu-id="dc866-134">The lookup presents the list of tax codes for selection.</span></span> <span data-ttu-id="dc866-135">Denne liste returneres af datakilden **Model.Data.Moms**, der er konfigureret i basis-ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="dc866-135">This list is returned by the **Model.Data.Tax** data source that has been configured in the base ER format.</span></span> <span data-ttu-id="dc866-136">Da denne datakilde indeholder feltet **Navn**, vises navnet på hver momskode i opslaget.</span><span class="sxs-lookup"><span data-stu-id="dc866-136">Because this data source contains the **Name** field, the name of each tax code appears in the lookup.</span></span>

    ![Siden med ER-programspecifikke parametre](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  <span data-ttu-id="dc866-138">Vælg momskoden **MOMS19**.</span><span class="sxs-lookup"><span data-stu-id="dc866-138">Select the **VAT19** tax code.</span></span>
8.  <span data-ttu-id="dc866-139">I feltet **Opslagsresultat** for den nye post skal du vælge rullelistens pil for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="dc866-139">In the **Lookup result** field of the new record, select the drop-down arrow to open the lookup.</span></span> <span data-ttu-id="dc866-140">Opslaget viser listen over værdier for fasttekstformatet Beskatningsniveau, som du kan markere.</span><span class="sxs-lookup"><span data-stu-id="dc866-140">The lookup presents the list of values for the TaxationLevel format enumeration for selection.</span></span>

    <span data-ttu-id="dc866-141">Bemærk, at hvis tysk er valgt som det foretrukne sprog for den bruger, du er logget på som, vil etiketterne for værdierne i opslaget være på tysk, hvis de er blevet oversat i basis-ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="dc866-141">Note that, if German is selected as the preferred language of the user that you're signed in as, the labels of the values in the lookup will be in German, provided that they have been translated in the base ER format.</span></span> <span data-ttu-id="dc866-142">Hvis etiketten for en opslagsdatakilde er oversat, vil denne etiket endvidere blive vist på brugerens foretrukne sprog under fanen **Opslag**.</span><span class="sxs-lookup"><span data-stu-id="dc866-142">Additionally, if the label of a lookup data source has been translated, that label will appear in the user's preferred language on the **Lookups** tab.</span></span>

    ![Siden med ER-programspecifikke parametre](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  <span data-ttu-id="dc866-144">Vælg værdien for **Almindelig moms**.</span><span class="sxs-lookup"><span data-stu-id="dc866-144">Select the **Regular taxation** value.</span></span>

    <span data-ttu-id="dc866-145">Når du tilføjer denne post, skal du definere følgende regel: Når der anmodes om opslagsdatakilden **Vælger**, og momskoden **MOMS19** sendes som et argument, returneres **Almindelig beskatning** som det ønskede beskatningsniveau.</span><span class="sxs-lookup"><span data-stu-id="dc866-145">By adding this record, you define the following rule: Whenever the **Selector** lookup data source is requested, and the **VAT19** tax code is passed as an argument, **Regular taxation** will be returned as the requested taxation level.</span></span>

10. <span data-ttu-id="dc866-146">Vælg **Tilføj**, og følg derefter følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="dc866-146">Select **Add**, and then follow these steps:</span></span>

    1. <span data-ttu-id="dc866-147">I feltet **Kode** skal du vælge momskoden **InMOMS19**.</span><span class="sxs-lookup"><span data-stu-id="dc866-147">In the **Code** field, select the **InVAT19** tax code.</span></span>
    2. <span data-ttu-id="dc866-148">I feltet **Opslagsresultat** skal du vælge værdien **Almindelig beskatning**.</span><span class="sxs-lookup"><span data-stu-id="dc866-148">In the **Lookup result** field, select the **Regular taxation** value.</span></span>
    
11. <span data-ttu-id="dc866-149">Vælg **Tilføj** igen, og følg derefter følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="dc866-149">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="dc866-150">I feltet **Kode** skal du vælge momskoden **MOMS7**.</span><span class="sxs-lookup"><span data-stu-id="dc866-150">In the **Code** field, select the **VAT7** tax code.</span></span>
    2. <span data-ttu-id="dc866-151">I feltet **Opslagsresultat** skal du vælge værdien **Reduceret beskatning**.</span><span class="sxs-lookup"><span data-stu-id="dc866-151">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
12. <span data-ttu-id="dc866-152">Vælg **Tilføj** igen, og følg derefter følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="dc866-152">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="dc866-153">I feltet **Kode** skal du vælge momskoden **InMOMS7**.</span><span class="sxs-lookup"><span data-stu-id="dc866-153">In the **Code** field, select the **InVAT7** tax code.</span></span>
    2. <span data-ttu-id="dc866-154">I feltet **Opslagsresultat** skal du vælge værdien **Reduceret beskatning**.</span><span class="sxs-lookup"><span data-stu-id="dc866-154">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
13. <span data-ttu-id="dc866-155">Vælg **Tilføj** igen, og følg derefter følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="dc866-155">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="dc866-156">I feltet **Kode** skal du vælge momskoden **TREDJE**.</span><span class="sxs-lookup"><span data-stu-id="dc866-156">In the **Code** field, select the **THIRD** tax code.</span></span>
    2. <span data-ttu-id="dc866-157">I feltet **Opslagsresultat** skal du vælge værdien **Ingen beskatning**.</span><span class="sxs-lookup"><span data-stu-id="dc866-157">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
14. <span data-ttu-id="dc866-158">Vælg **Tilføj** igen, og følg derefter følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="dc866-158">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="dc866-159">I feltet **Kode** skal du vælge momskoden **InMOMS0**.</span><span class="sxs-lookup"><span data-stu-id="dc866-159">In the **Code** field, select the **InVAT0** tax code.</span></span>
    2. <span data-ttu-id="dc866-160">I feltet **Opslagsresultat** skal du vælge værdien **Ingen beskatning**.</span><span class="sxs-lookup"><span data-stu-id="dc866-160">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
15. <span data-ttu-id="dc866-161">Vælg **Tilføj** igen, og følg derefter følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="dc866-161">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="dc866-162">I feltet **Kode** skal du vælge indstillingen **\*Ikke tom\***.</span><span class="sxs-lookup"><span data-stu-id="dc866-162">In the **Code** field, select the **\*Not blank\*** option.</span></span>
    2. <span data-ttu-id="dc866-163">I feltet **Opslagsresultat** skal du vælge værdien **Andet**.</span><span class="sxs-lookup"><span data-stu-id="dc866-163">In the **Lookup result** field, select the **Other** value.</span></span>
    
    <span data-ttu-id="dc866-164">Når du tilføjer denne sidste post, skal du definere følgende regel: Når den momskode, der er videregivet som argument, ikke opfylder nogle af de tidligere regler, vil opslagsdatakilden returnere **Andet** som det ønskede beskatningsniveau.</span><span class="sxs-lookup"><span data-stu-id="dc866-164">By adding this last record, you define the following rule: Whenever the tax code that is passed as an argument doesn't satisfy any of the previous rules, the lookup data source will return **Other** as the requested taxation level.</span></span>

    ![Siden med ER-programspecifikke parametre](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. <span data-ttu-id="dc866-166">I feltet **Tilstand** skal du vælge **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="dc866-166">In the **State** field, select **Completed**.</span></span>

    <span data-ttu-id="dc866-167">Når du kører en version af ER-formatet, der har status som enten **Fuldført** eller **delt**, skal dette regelsæt være i tilstanden **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="dc866-167">When you run an ER format version that has a status of either **Completed** or **Shared**, this set of rules must be in the **Completed** state.</span></span> <span data-ttu-id="dc866-168">Ellers vil udførelsen af basis-ER-formatet blive afbrudt, når formatet forsøger at indlæse data fra dette regelsæt, mens opslagsdatakilden **Vælger** køres.</span><span class="sxs-lookup"><span data-stu-id="dc866-168">Otherwise, execution of the base ER format will be interrupted when the format tries to load data from this set of rules while the **Selector** lookup data source is being run.</span></span>
    
    <span data-ttu-id="dc866-169">Når du kører en version af ER-formatet, der har statussen **Kladde**, har basis-ER-formatet adgang til dette regelsæt, uanset dets tilstand.</span><span class="sxs-lookup"><span data-stu-id="dc866-169">When you run an ER format version that has a status of **Draft**, the base ER format can access this set of rules, regardless of its state.</span></span>
    
17. <span data-ttu-id="dc866-170">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="dc866-170">Select **Save**.</span></span>
18. <span data-ttu-id="dc866-171">Luk siden med **Programspecifikke parametre**.</span><span class="sxs-lookup"><span data-stu-id="dc866-171">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-demf-company"></a><span data-ttu-id="dc866-172">Kør ER-formatet i DEMF-firmaet</span><span class="sxs-lookup"><span data-stu-id="dc866-172">Run the ER format in the DEMF company</span></span>

1.  <span data-ttu-id="dc866-173">I konfigurationstræet skal du vælge elementet **Format for at lære, hvordan man slår LE-data op**.</span><span class="sxs-lookup"><span data-stu-id="dc866-173">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="dc866-174">Vælg **Kør** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="dc866-174">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="dc866-175">Vælg **OK** i dialogboksen, der vises.</span><span class="sxs-lookup"><span data-stu-id="dc866-175">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="dc866-176">Hent den opgørelse, der genereres, og gem den lokalt.</span><span class="sxs-lookup"><span data-stu-id="dc866-176">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="dc866-177">I den genererede opgørelse bemærker du, at opsummeringen af momskoden **InMOMS7** er sat til niveauet **Reduceret**, og opsummeringerne af momskoderne **MOMS19** og **InMOMS19** er sat til niveauet **Almindelig**.</span><span class="sxs-lookup"><span data-stu-id="dc866-177">In the generated statement, notice that the summary of the **InVAT7** tax code has been put on the **Reduced** level, and the summaries of the **VAT19** and **InVA19** tax codes have been put on the **Regular** level.</span></span> <span data-ttu-id="dc866-178">Denne funktionsmåde bestemmes af konfigurationen i det regelsæt, der er afhængig af den juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="dc866-178">This behavior is determined by the configuration in the legal entity–dependent set of rules.</span></span>
    
5.  <span data-ttu-id="dc866-179">Gå til **Moms \> Indirekte skatter \> Moms \> Momskoder**.</span><span class="sxs-lookup"><span data-stu-id="dc866-179">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.</span></span>
6.  <span data-ttu-id="dc866-180">Vælg momskoden **InMOMS7**.</span><span class="sxs-lookup"><span data-stu-id="dc866-180">Select the **InVAT7** tax code.</span></span>
7.  <span data-ttu-id="dc866-181">I handlingspanelet skal du på fanen **Momskode** i gruppen **Forespørgsler** vælge **Bogført moms** for at få vist oplysninger om momsværdien og den anvendte momssats per momskode.</span><span class="sxs-lookup"><span data-stu-id="dc866-181">On the Action Pane, on the **Sales tax code** tab, in the **Inquiries** group, select **Posted sales tax** to view information about the tax value and applied tax rate per tax code.</span></span>

    ![Siden Bogført moms](./media/GER-AppSpecParms-Statement.PNG)

8.  <span data-ttu-id="dc866-183">Luk siden Bogført moms.</span><span class="sxs-lookup"><span data-stu-id="dc866-183">Close the Posted sales tax page.</span></span>

## <a name="set-up-parameters-for-the-usmf-company"></a><span data-ttu-id="dc866-184">Angiv parametrene for USMF-firmaet</span><span class="sxs-lookup"><span data-stu-id="dc866-184">Set up parameters for the USMF company</span></span>

1.  <span data-ttu-id="dc866-185">Vælg den juridiske enhed **USMF**.</span><span class="sxs-lookup"><span data-stu-id="dc866-185">Select the **USMF** legal entity.</span></span>
2.  <span data-ttu-id="dc866-186">Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="dc866-186">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3.  <span data-ttu-id="dc866-187">I konfigurationstræet skal du udvide elementet **Model til at lære parameteriserede kald**, udvide elementet **Format til at lære parameteriserede kald** og vælge formatet **Format til at lære, hvordan man leder efter LE-data**.</span><span class="sxs-lookup"><span data-stu-id="dc866-187">In the configurations tree, expand the **Model to learn parameterized calls** item, expand the **Format to learn parameterized calls** item, and select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="dc866-188">I handlingsruden på fanen **Konfigurationer** skal du i gruppen **Programspecifikke parametre** vælge **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="dc866-188">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="dc866-189">Vælg version **1.1.1** af det valgte ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="dc866-189">Select version **1.1.1** of the selected ER format.</span></span>
6.  <span data-ttu-id="dc866-190">Vælg **Tilføj** i oversigtspanelet **Betingelser**.</span><span class="sxs-lookup"><span data-stu-id="dc866-190">On the **Conditions** FastTab, select **Add**.</span></span>
7.  <span data-ttu-id="dc866-191">I feltet **Kode** for den nye post skal du vælge rullelistens pil for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="dc866-191">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="dc866-192">Opslaget indeholder nu listen over momskoder for den **USMF**-virksomhedsmoms, der skal vælges.</span><span class="sxs-lookup"><span data-stu-id="dc866-192">The lookup now presents the list of tax codes for the **USMF** company tax for selection.</span></span>

    ![Siden med ER-programspecifikke parametre](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  <span data-ttu-id="dc866-194">Vælg momskoden **UNDTAGET**.</span><span class="sxs-lookup"><span data-stu-id="dc866-194">Select the **EXEMPT** tax code.</span></span>
9.  <span data-ttu-id="dc866-195">I feltet **Opslagsresultat** for den nye post skal du vælge værdien **Ingen beskatning**.</span><span class="sxs-lookup"><span data-stu-id="dc866-195">In the **Lookup resul** t field of the new record, select the **No taxation** value.</span></span>
10. <span data-ttu-id="dc866-196">Vælg **Tilføj** igen.</span><span class="sxs-lookup"><span data-stu-id="dc866-196">Select **Add** again.</span></span>
11. <span data-ttu-id="dc866-197">I feltet **Kode** for den nye post skal du vælge indstillingen **\*Ikke tom\***.</span><span class="sxs-lookup"><span data-stu-id="dc866-197">In the **Code** field of the new record, select the **\*Not blank\*** option.</span></span>
12. <span data-ttu-id="dc866-198">I feltet **Opslagsresultat** for den nye post skal du vælge værdien **Almindelig beskatning**.</span><span class="sxs-lookup"><span data-stu-id="dc866-198">In the **Lookup result** field of the new record, select the **Regular taxation** value.</span></span>
13. <span data-ttu-id="dc866-199">I feltet **Tilstand** skal du vælge **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="dc866-199">In the **State** field, select **Completed**.</span></span>
14. <span data-ttu-id="dc866-200">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="dc866-200">Select **Save**.</span></span>

    ![Siden med ER-programspecifikke parametre](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. <span data-ttu-id="dc866-202">Luk siden med **Programspecifikke parametre**.</span><span class="sxs-lookup"><span data-stu-id="dc866-202">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-usmf-company"></a><span data-ttu-id="dc866-203">Kør ER-formatet i USMF-firmaet</span><span class="sxs-lookup"><span data-stu-id="dc866-203">Run the ER format in the USMF company</span></span>

1.  <span data-ttu-id="dc866-204">I konfigurationstræet skal du vælge elementet **Format for at lære, hvordan man slår LE-data op**.</span><span class="sxs-lookup"><span data-stu-id="dc866-204">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="dc866-205">Vælg **Kør** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="dc866-205">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="dc866-206">Vælg **OK** i dialogboksen, der vises.</span><span class="sxs-lookup"><span data-stu-id="dc866-206">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="dc866-207">Hent den opgørelse, der genereres, og gem den lokalt.</span><span class="sxs-lookup"><span data-stu-id="dc866-207">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="dc866-208">Bemærk, at du nu har genbrugt det samme ER-format for en anden juridisk enhed i den genererede opgørelse, men uden at foretage nogle justeringer af ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="dc866-208">In the generated statement, notice that you've now reused the same ER format for a different legal entity, but without making any adjustments to the ER format.</span></span>

## <a name="reuse-legal-entitydependent-parameters"></a><span data-ttu-id="dc866-209">Genbrug de juridisk enhedsafhængige parametre</span><span class="sxs-lookup"><span data-stu-id="dc866-209">Reuse legal entity–dependent parameters</span></span>

### <a name="export-parameters"></a><span data-ttu-id="dc866-210">Eksporter parametre</span><span class="sxs-lookup"><span data-stu-id="dc866-210">Export parameters</span></span>

1.  <span data-ttu-id="dc866-211">Gå til **Virksomhedsadministration \> Arbejdsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="dc866-211">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2.  <span data-ttu-id="dc866-212">Vælg **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="dc866-212">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="dc866-213">I konfigurationstræet skal du vælge elementet **Format for at lære, hvordan man slår LE-data op**.</span><span class="sxs-lookup"><span data-stu-id="dc866-213">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="dc866-214">I handlingsruden på fanen **Konfigurationer** skal du i gruppen **Programspecifikke parametre** vælge **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="dc866-214">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="dc866-215">Vælg version **1.1.1** af ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="dc866-215">Select version **1.1.1** of the ER format.</span></span>
6.  <span data-ttu-id="dc866-216">Vælg **Eksporter** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="dc866-216">On the Action Pane, select **Export**.</span></span>
7.  <span data-ttu-id="dc866-217">Hent den fil, der genereres, og gem den lokalt.</span><span class="sxs-lookup"><span data-stu-id="dc866-217">Download the file that is generated and store it locally.</span></span>

    <span data-ttu-id="dc866-218">Det konfigurerede sæt af programspecifikke parametre er nu eksporteret som en XML-fil.</span><span class="sxs-lookup"><span data-stu-id="dc866-218">The configured set of application-specific parameters has now been exported as an XML file.</span></span>

### <a name="import-parameters"></a><span data-ttu-id="dc866-219">Importer parametre</span><span class="sxs-lookup"><span data-stu-id="dc866-219">Import parameters</span></span>

1.  <span data-ttu-id="dc866-220">Vælg version **1.1.2** af ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="dc866-220">Select version **1.1.2** of the ER format.</span></span>
2.  <span data-ttu-id="dc866-221">Vælg **Importér** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="dc866-221">On the Action Pane, select **Import**.</span></span>
3.  <span data-ttu-id="dc866-222">Vælg **Ja** for at bekræfte, at du vil overskrive de eksisterende programspecifikke parametre for denne formatversion.</span><span class="sxs-lookup"><span data-stu-id="dc866-222">Select **Yes** to confirm that you want to override the existing application-specific parameters for this format version.</span></span>
4.  <span data-ttu-id="dc866-223">Vælg **Gennemse** for at finde den fil, der indeholder de eksporterede programspecifikke parametre for version **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="dc866-223">Select **Browse** to find the file that contains the exported application-specific parameters for version **1.1.1**.</span></span>
5.  <span data-ttu-id="dc866-224">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc866-224">Select **OK**.</span></span>

    <span data-ttu-id="dc866-225">Version **1.1.2** af ER-formatet har nu de samme programspecifikke parametre, som du oprindeligt konfigurerede for version **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="dc866-225">Version **1.1.2** of the ER format now has the same application-specific parameters that you originally configured for version **1.1.1**.</span></span>
    
    <span data-ttu-id="dc866-226">Bemærk, at de programspecifikke parametre i et ER-format er juridisk enhedsafhængige.</span><span class="sxs-lookup"><span data-stu-id="dc866-226">Note that the application-specific parameters of an ER format are legal entity–dependent.</span></span> <span data-ttu-id="dc866-227">Hvis du vil genbruge de programspecifikke parametre, der er konfigureret for én juridisk enhed i en anden juridisk enhed, skal du eksportere dem, mens du er logget på den første juridiske enhed, og derefter importere dem, når du har logget på den anden juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="dc866-227">To reuse the application-specific parameters that were configured for one legal entity in a different legal entity, you must export them while you're signed in to the first legal entity and then import them after you sign in to the other legal entity.</span></span>

    <span data-ttu-id="dc866-228">Du kan også bruge denne fremgangsmåde til at overføre et ER-format, der er tilknyttet programspecifikke parametre, som oprindeligt blev konfigureret i én Finance-forekomst til en anden Finance-forekomst.</span><span class="sxs-lookup"><span data-stu-id="dc866-228">You can also use this approach to transfer an ER format related application-specific parameters that were originally configured in one instance of Finance to another instance of Finance.</span></span>

    <span data-ttu-id="dc866-229">Bemærk, at hvis du konfigurerer programspecifikke parametre for en version af et ER-format og importerer en nyere version af det samme format til den aktuelle Finance-forekomst, anvendes de eksisterende programspecifikke parametre ikke for den importerede version.</span><span class="sxs-lookup"><span data-stu-id="dc866-229">Be aware that if you configure application-specific parameters for one version of an ER format and import a higher version of the same format into the current Finance instance, the existing application-specific parameters won't be applied for the imported version.</span></span>
    
    <span data-ttu-id="dc866-230">Bemærk også, at når du vælger en fil til import, sammenlignes strukturen for de programspecifikke parametre i den pågældende fil med strukturen i den tilsvarende datakilde for typen **Opslag** i det ER-formatet, der er valgt til import.</span><span class="sxs-lookup"><span data-stu-id="dc866-230">Also be aware that, when you select a file for import, the structure of the application-specific parameters in that file is compared with the structure of the corresponding data source of the **Lookup** type in the ER format that is selected for import.</span></span> <span data-ttu-id="dc866-231">Importen udføres, når strukturen af de programspecifikke parametre stemmer overens med strukturen i den tilsvarende datakilde i det ER-format, der er valgt til import.</span><span class="sxs-lookup"><span data-stu-id="dc866-231">The import is done when the structure of each application-specific parameter matches the structure of the corresponding data source in the ER format that is selected for import.</span></span> <span data-ttu-id="dc866-232">Hvis strukturerne ikke stemmer overens, får du vist en advarselsmeddelelse, der angiver, at importen ikke kan udføres.</span><span class="sxs-lookup"><span data-stu-id="dc866-232">If the structures don't match, you receive a warning message that states that the import can't be done.</span></span> <span data-ttu-id="dc866-233">Hvis du gennemtvinger importen, vil de eksisterende programspecifikke parametre for det valgte ER-format blive ryddet op, og du skal konfigurere dem påny.</span><span class="sxs-lookup"><span data-stu-id="dc866-233">If you force the import to be done, the existing application-specific parameters for the selected ER format will be cleaned up, and you must set them up from the beginning.</span></span>

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a><span data-ttu-id="dc866-234">Relation mellem programspecifikke parametre og et ER-format</span><span class="sxs-lookup"><span data-stu-id="dc866-234">Relationship between application-specific parameters and an ER format</span></span>

<span data-ttu-id="dc866-235">Relationen mellem et ER-format og dens programspecifikke parametre fastlægges af ER-formatets forekomst-uafhængige entydig identifikationskode.</span><span class="sxs-lookup"><span data-stu-id="dc866-235">The relationship between an ER format and its application-specific parameters is established by the ER format's instance-independent unique identification code.</span></span> <span data-ttu-id="dc866-236">Når du fjerner et ER-format fra Finance, bevares de programspecifikke parametre, der er konfigureret for ER-formatet, derfor i den aktuelle forekomst af Finance.</span><span class="sxs-lookup"><span data-stu-id="dc866-236">Therefore, when you remove an ER format from Finance, the application-specific parameters that are configured for the ER format are kept in the current instance of Finance.</span></span> <span data-ttu-id="dc866-237">Du kan få adgang til dem, når basis-ER-format, importeres igen til denne forekomst af Finance.</span><span class="sxs-lookup"><span data-stu-id="dc866-237">They can be accessed whenever the base ER format is reimported into this instance of Finance.</span></span>

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a><span data-ttu-id="dc866-238">Få adgang til programspecifikke parametre ved hjælp af ER-strukturen</span><span class="sxs-lookup"><span data-stu-id="dc866-238">Access application-specific parameters by using the ER framework</span></span>

<span data-ttu-id="dc866-239">I det foregående eksempel fik du adgang til programspecifikke parametre for et ER-format ved hjælp af ER-strukturen.</span><span class="sxs-lookup"><span data-stu-id="dc866-239">In the preceding example, you have accessed application-specific parameters of an ER format by using the ER framework.</span></span> <span data-ttu-id="dc866-240">Denne fremgangsmåde giver dig ikke mulighed for at begrænse adgangen til de programspecifikke parametre for et bestemt ER-format.</span><span class="sxs-lookup"><span data-stu-id="dc866-240">This approach doesn't let you restrict access to the application-specific parameters of a specific ER format.</span></span> <span data-ttu-id="dc866-241">Hvis du skal anvende sådanne begrænsninger, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="dc866-241">If you must apply such restrictions, follow these steps.</span></span> 

1.  <span data-ttu-id="dc866-242">Du kan enten genbrug en eksisterende **ERSolutionAppSpecificParametersDesigner**-menu eller implementere dit eget **ERSolutionAppSpecificParametersDesigner**-menuelement.</span><span class="sxs-lookup"><span data-stu-id="dc866-242">Either reuse an existing **ERSolutionAppSpecificParametersDesigner** menu item, or implement your own **ERSolutionAppSpecificParametersDesigner** menu item.</span></span>

    ![Siden Visual studio](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  <span data-ttu-id="dc866-244">Udfør ét af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="dc866-244">Follow one of these steps:</span></span>

    1.  <span data-ttu-id="dc866-245">Opret en ny menuknap, og sammenkæd den med den tilsvarende post fra tabellen **ERSolutionTable** ved at angive dens egenskab **Datakilde** til **ERSolutionTable**.</span><span class="sxs-lookup"><span data-stu-id="dc866-245">Create a new menu item button, and link it to the corresponding record from the **ERSolutionTable** table by setting its **Data Source** property to **ERSolutionTable**.</span></span>
    
        ![Siden Visual studio](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  <span data-ttu-id="dc866-247">Opret en enkel knap, og overskriv metoden **Klikket på**, som vist i følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="dc866-247">Create a simple button, and override the **Clicked** method as shown in the following example.</span></span>
    
        <span data-ttu-id="dc866-248">Ved hjælp af denne fremgangsmåde kan du angive et entydigt løsnings-ID (defineret via værdien **GUID**) for kun at give adgang til de programspecifikke parametre for et bestemt ER-format og de underordnede kopier, der er afledt af den.</span><span class="sxs-lookup"><span data-stu-id="dc866-248">By using this approach, you can specify a unique solution ID (defined via the **GUID** value) to allow access to the application-specific parameters of only a specific ER format and descendant copies that have been derived from it.</span></span>
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a><span data-ttu-id="dc866-249">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="dc866-249">Additional resources</span></span>

[<span data-ttu-id="dc866-250">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="dc866-250">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="dc866-251">Konfigurer ER-formater for at bruge de parametre, der er angivet for den enkelte juridiske enhed</span><span class="sxs-lookup"><span data-stu-id="dc866-251">Configure ER formats to use parameters that are specified per legal entity</span></span>](er-app-specific-parameters-configure-format.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]