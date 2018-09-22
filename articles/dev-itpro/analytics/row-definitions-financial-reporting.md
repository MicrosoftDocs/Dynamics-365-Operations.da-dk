---
title: "Rækkedefinitioner i Designer til økonomirapporter"
description: "En rækkedefinition er en rapportkomponent, eller dokumentkomponent, der angiver indholdet af hver række i en økonomirapport. En rækkedefinition kan kombineres med kolonnedefinitioner, rapporteringstrædefinitioner og rapportdefinitioner, så de danner en komponentgruppe, der kan bruges af flere firmaer."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: c829af1da1b3109f4687c9a2536dd156339d5c76
ms.contentlocale: da-dk
ms.lasthandoff: 08/13/2018

---

# <a name="row-definitions-in-financial-report-designer"></a><span data-ttu-id="9bf23-104">Rækkedefinitioner i Designer til økonomirapporter</span><span class="sxs-lookup"><span data-stu-id="9bf23-104">Row definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9bf23-105">En rækkedefinition er en rapportkomponent, eller dokumentkomponent, der angiver indholdet af hver række i en økonomirapport.</span><span class="sxs-lookup"><span data-stu-id="9bf23-105">A row definition is a report component, or building block, that specifies the contents of each row on a financial report.</span></span> <span data-ttu-id="9bf23-106">En rækkedefinition kan kombineres med kolonnedefinitioner, rapporteringstrædefinitioner og rapportdefinitioner, så de danner en komponentgruppe, der kan bruges af flere firmaer.</span><span class="sxs-lookup"><span data-stu-id="9bf23-106">A row definition can be combined with column definitions, reporting tree definitions, and report definitions to create a building block group that can be used by multiple companies.</span></span>

## <a name="create-a-row-definition"></a><span data-ttu-id="9bf23-107">Oprette en ny definition</span><span class="sxs-lookup"><span data-stu-id="9bf23-107">Create a row definition</span></span>

1. <span data-ttu-id="9bf23-108">Klik på **Rækkedefinitioner** i navigationsruden i Report Designer.</span><span class="sxs-lookup"><span data-stu-id="9bf23-108">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="9bf23-109">Klik på **Ny** i menuen **Filer**, og klik derefter på **Rækkedefinition**.</span><span class="sxs-lookup"><span data-stu-id="9bf23-109">On the **File** menu, click **New**, and then click **Row Definition**.</span></span> <span data-ttu-id="9bf23-110">Der er flere oplysninger om indholdet af hver celle under [Redigere rækkedefinitionsceller](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="9bf23-110">For more information about the content of each cell, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="open-a-row-definition"></a><span data-ttu-id="9bf23-111">Åbn en rækkedefinition</span><span class="sxs-lookup"><span data-stu-id="9bf23-111">Open a row definition</span></span>
1. <span data-ttu-id="9bf23-112">Klik på **Rækkedefinitioner** i navigationsruden i Report Designer.</span><span class="sxs-lookup"><span data-stu-id="9bf23-112">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="9bf23-113">Dobbeltklik på navnet på den rækkedefinition, du vil åbne.</span><span class="sxs-lookup"><span data-stu-id="9bf23-113">Double-click the name of the row definition to open.</span></span>
3. <span data-ttu-id="9bf23-114">For at få vist de komponenter, der hører til rækkedefinitionen, skal du højreklikke på rækkedefinitionen, og derefter vælge **Tilknytninger**.</span><span class="sxs-lookup"><span data-stu-id="9bf23-114">To view any building blocks that are associated with the row definition, right-click the row definition, and then select **Associations**.</span></span>

## <a name="contents-of-a-row-definition"></a><span data-ttu-id="9bf23-115">Indholdet af en rækkedefinition</span><span class="sxs-lookup"><span data-stu-id="9bf23-115">Contents of a row definition</span></span>
<span data-ttu-id="9bf23-116">En rækkedefinition kan indeholde op til 20.000 rækker med økonomiske dimensioner og kan indeholde følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="9bf23-116">A row definition can contain up to 20,000 financial dimension rows and can include the following information:</span></span>

- <span data-ttu-id="9bf23-117">Beskrivende tekst i form af afsnitsoverskrifter, linjer og mellemrum, der har en forklarende funktion i rapporten, f.eks. **Kontanter** eller **Samlet omsætning**.</span><span class="sxs-lookup"><span data-stu-id="9bf23-117">Descriptive text that adds meaning to the report by creating section headings, lines, and spaces, such as **Cash** or **Total Revenue**</span></span>
- <span data-ttu-id="9bf23-118">Links til økonomiske data, der kan omfatte dimensionsværdier i Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9bf23-118">Links to financial data, which can include dimension values in the Microsoft Dynamics 365 for Finance and Operations</span></span>

    > [!NOTE]
    > <span data-ttu-id="9bf23-119">Du kan konfigurere en rækkedefinition, der henter data fra det økonomiske dimensionssystem, hver gang rapporten genereres.</span><span class="sxs-lookup"><span data-stu-id="9bf23-119">You can set up a row definition to pull data from the financial dimensions system every time that the report is generated.</span></span>

- <span data-ttu-id="9bf23-120">Rækketotaler og formler, der er baseret på de tilknyttede økonomiske data</span><span class="sxs-lookup"><span data-stu-id="9bf23-120">Row totals and formulas that are based on the linked financial data</span></span>

<span data-ttu-id="9bf23-121">Hver række i en rækkedefinition indeholder normalt en af følgende typer oplysninger:</span><span class="sxs-lookup"><span data-stu-id="9bf23-121">Usually, each row in a row definition contains one of the following types of information:</span></span>

- <span data-ttu-id="9bf23-122">Henvisninger til systemet med økonomiske dimensioner</span><span class="sxs-lookup"><span data-stu-id="9bf23-122">References to the financial dimensions system</span></span>
- <span data-ttu-id="9bf23-123">Totaler eller beregninger, der er baseret på dataene</span><span class="sxs-lookup"><span data-stu-id="9bf23-123">Totals or calculations that are based on the data</span></span>
- <span data-ttu-id="9bf23-124">Formattering</span><span class="sxs-lookup"><span data-stu-id="9bf23-124">Formatting</span></span>

<span data-ttu-id="9bf23-125">Der er to metoder til at angive oplysninger i en rækkedefinition:</span><span class="sxs-lookup"><span data-stu-id="9bf23-125">There are two methods for entering information in a row definition:</span></span>

- <span data-ttu-id="9bf23-126">Du kan indtaste rækkeoplysninger manuelt i en ny rækkedefinition.</span><span class="sxs-lookup"><span data-stu-id="9bf23-126">Manually enter row information in a new row definition.</span></span> <span data-ttu-id="9bf23-127">Yderligere oplysninger finder du under [Redigere rækkedefinitionsceller](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="9bf23-127">For more information, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>
- <span data-ttu-id="9bf23-128">Du kan bruge rapportdesigneren til at trække oplysninger direkte fra de økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="9bf23-128">Use report designer to pull row information directly from the financial dimensions.</span></span> <span data-ttu-id="9bf23-129">Du kan finde flere oplysninger i afsnittet "Relaterede formler/rækker/enheder" i [Ændre rækkedefinitionsceller](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="9bf23-129">For more information, see the "Related formulas/rows/units" section in [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="add-dimensions-in-a-row-definition"></a><span data-ttu-id="9bf23-130">Tilføje dimensioner i en rækkedefinition</span><span class="sxs-lookup"><span data-stu-id="9bf23-130">Add dimensions in a row definition</span></span>
<span data-ttu-id="9bf23-131">En dimension er et skæringspunkt for data og værdier.</span><span class="sxs-lookup"><span data-stu-id="9bf23-131">A dimension is an intersection of data and values.</span></span> <span data-ttu-id="9bf23-132">Du kan gruppere data og værdier i Report Designer.</span><span class="sxs-lookup"><span data-stu-id="9bf23-132">You can group data and values in report designer.</span></span> <span data-ttu-id="9bf23-133">Du kan derefter klassificere og analysere posteringer i flere detaljer.</span><span class="sxs-lookup"><span data-stu-id="9bf23-133">You can then classify and analyze transactions in more detail.</span></span> <span data-ttu-id="9bf23-134">Du kan bruge dialogboksen **Indsæt rækker fra dimensioner** til at føje flere rækker til en rækkedefinition på samme tid.</span><span class="sxs-lookup"><span data-stu-id="9bf23-134">You can use the **Insert Rows from Dimensions** dialog box to add multiple rows to a row definition at the same time.</span></span> <span data-ttu-id="9bf23-135">Dialogboksen indeholder én kolonne for hver dimension.</span><span class="sxs-lookup"><span data-stu-id="9bf23-135">The dialog box displays one column for each dimension.</span></span> <span data-ttu-id="9bf23-136">Følgende tabel beskriver de oplysninger, du kan angive for hver dimension.</span><span class="sxs-lookup"><span data-stu-id="9bf23-136">The following table describes the information that you can specify for each dimension.</span></span>

| <span data-ttu-id="9bf23-137">Indstilling</span><span class="sxs-lookup"><span data-stu-id="9bf23-137">Option</span></span>                | <span data-ttu-id="9bf23-138">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9bf23-138">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="9bf23-139">Dimension</span><span class="sxs-lookup"><span data-stu-id="9bf23-139">Dimension</span></span>             | <span data-ttu-id="9bf23-140">Det mønster, der identificerer den dimension, der skal føjes til rækkedefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9bf23-140">The pattern that identifies the dimension to add to the row definition.</span></span> <span data-ttu-id="9bf23-141">Dette mønster indeholder et (&) eller et nummertegn (\#) for hver enkelt position i dimensionerne.</span><span class="sxs-lookup"><span data-stu-id="9bf23-141">This pattern contains one ampersand (&) or number sign (\#) for each position in the dimensions.</span></span> <span data-ttu-id="9bf23-142">Generelt skal du bruge alle plustegn for hovedkontodimensionen og alle nummertegn til andre dimensioner.</span><span class="sxs-lookup"><span data-stu-id="9bf23-142">Generally, use all ampersands for the Main Account dimension and all number signs for other dimensions.</span></span> |
| <span data-ttu-id="9bf23-143">Start på dimensionsområde</span><span class="sxs-lookup"><span data-stu-id="9bf23-143">Dimension Range Start</span></span> | <span data-ttu-id="9bf23-144">Den første værdi for denne dimension, der skal føjes til rækkedefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9bf23-144">The first value for this dimension to add to the row definition.</span></span> |
| <span data-ttu-id="9bf23-145">Slut på dimensionsområde</span><span class="sxs-lookup"><span data-stu-id="9bf23-145">Dimension Range End</span></span>   | <span data-ttu-id="9bf23-146">Den sidste værdi for den dimension, der skal føjes til rækkedefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9bf23-146">The last value for this dimension to add to the row definition.</span></span> |

<span data-ttu-id="9bf23-147">Udfør følgende trin for at føje dimensioner til en rækkedefinition.</span><span class="sxs-lookup"><span data-stu-id="9bf23-147">To add dimensions to a row definition, follow these steps.</span></span>

1. <span data-ttu-id="9bf23-148">Klik på **Rækkedefinitioner** i Report Designer, og åbn derefter den rækkedefinition, der skal ændres.</span><span class="sxs-lookup"><span data-stu-id="9bf23-148">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="9bf23-149">I menuen **Rediger** skal du klikke på **Indsæt rækker fra dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="9bf23-149">On the **Edit** menu, click **Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="9bf23-150">I dialogboksen **Indsæt rækker fra dimensioner** i rækken **Dimensioner** skal du markere cellen for den dimension, der skal overføres til rækkedefinitionen, og derefter klikke på **Alle &&&**.</span><span class="sxs-lookup"><span data-stu-id="9bf23-150">In the **Insert Rows from Dimensions** dialog box, in the **Dimensions** row, select the cell for the dimension to transfer to the row definition, and then click **All &&&**.</span></span>
4. <span data-ttu-id="9bf23-151">For at begrænse rækkedefinitionen til et bestemt område af dimensionsværdier skal du angive startdimensionsværdien i cellen **Start på dimensionsområde** og derefter angive slutdimensionsværdien i cellen **Slut på dimensionsområde**.</span><span class="sxs-lookup"><span data-stu-id="9bf23-151">To limit the row definition to a specific range of dimension values, enter the starting dimension value in the **Dimension Range Start** cell, and then enter the ending dimension value in the **Dimension Range End** cell.</span></span> <span data-ttu-id="9bf23-152">Hvis du vil medtage alle værdier for den valgte dimension, skal du lade disse celler være tomme.</span><span class="sxs-lookup"><span data-stu-id="9bf23-152">To include all values for the selected dimension, leave these cells empty.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9bf23-153">Jokertegn (\* eller ?) i områder med dimensioner returnerer muligvis ikke alle de resultater, du ønsker, afhængigt af hvordan ERP-databasen samler data.</span><span class="sxs-lookup"><span data-stu-id="9bf23-153">Wildcard characters (\* or ?) in dimension ranges might not return all the results that you want, depending on how the ERP database collates data.</span></span>

5. <span data-ttu-id="9bf23-154">I feltet **Startrækkekode** skal du angive rækkekoden for den første dimensionsværdi, der skal føjes til rækkedefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9bf23-154">In the **Starting row code** field, specify the row code for the first dimension value to add to the row definition.</span></span>
6. <span data-ttu-id="9bf23-155">I feltet **Forøg hver række med** skal du angive afstanden mellem på hinanden følgende rækkekoder.</span><span class="sxs-lookup"><span data-stu-id="9bf23-155">In the **Increment each row by** field, specify the gap between consecutive row codes.</span></span> <span data-ttu-id="9bf23-156">Hvis den første rækkekode er 100, og den stigende værdi er 30, har de første nye rækker koderne 100, 130, 160, 190 og 220.</span><span class="sxs-lookup"><span data-stu-id="9bf23-156">For example, if the first row code is 100, and the increment value is 30, the first new rows have the codes 100, 130, 160, 190, and 220.</span></span> <span data-ttu-id="9bf23-157">Brug en forøgelsesværdi, der indeholder tilstrækkelig plads til at indsætte nye formater og formelrækker.</span><span class="sxs-lookup"><span data-stu-id="9bf23-157">Use an increment value that provides enough space to insert new format and formula rows.</span></span>
7. <span data-ttu-id="9bf23-158">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9bf23-158">Click **OK**.</span></span> <span data-ttu-id="9bf23-159">Der tilføjes én linje for hver af de valgte dimensionsværdier i rækkedefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9bf23-159">For each of the selected dimension values, one line is added to the row definition.</span></span>

## <a name="adjust-rounding-in-a-row-definition"></a><span data-ttu-id="9bf23-160">Justere afrunding i en rækkedefinition</span><span class="sxs-lookup"><span data-stu-id="9bf23-160">Adjust rounding in a row definition</span></span>
<span data-ttu-id="9bf23-161">Hvis du har en balance, hvor beløbene er afrundede, stemmer totalerne muligvis ikke.</span><span class="sxs-lookup"><span data-stu-id="9bf23-161">If you have a balance sheet where the amounts are rounded, the totals might not balance.</span></span> <span data-ttu-id="9bf23-162">Dette problem kan opstå, hvis du f.eks. bruger afrundingsindstillingen på en balancerapport og rapportdefinitionen angiver også afrunding.</span><span class="sxs-lookup"><span data-stu-id="9bf23-162">This issue can occur if, for example, you use the rounding option on a balance sheet report and the report definition also specifies rounding.</span></span> <span data-ttu-id="9bf23-163">Du kan bruge indstillingen **Afrundingsdifference** i rækkedefinitionen for at afbalancere beløbene i balancer.</span><span class="sxs-lookup"><span data-stu-id="9bf23-163">You can use the **Rounding adjustment** option in the row definition to balance the amounts in the balance sheets.</span></span> <span data-ttu-id="9bf23-164">Du kan slå afrunding fra eller ændre det under fanen **Indstillinger** i rapportdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9bf23-164">You can turn rounding off or modify it on the **Settings** tab of the report definition.</span></span> <span data-ttu-id="9bf23-165">I følgende tabel vises, hvordan beløb afrundes.</span><span class="sxs-lookup"><span data-stu-id="9bf23-165">The following table shows how amounts are rounded.</span></span> <span data-ttu-id="9bf23-166">I denne tabel afviger totalerne for række 100 og 200, når afrunding er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="9bf23-166">In this table, the totals of rows 100 and 200 differ when rounding is turned on.</span></span>

| <span data-ttu-id="9bf23-167">Rækkekode</span><span class="sxs-lookup"><span data-stu-id="9bf23-167">Row code</span></span> | <span data-ttu-id="9bf23-168">Beløb uden afrunding</span><span class="sxs-lookup"><span data-stu-id="9bf23-168">Amounts without rounding</span></span> | <span data-ttu-id="9bf23-169">Beløb med afrunding til hele tusinder</span><span class="sxs-lookup"><span data-stu-id="9bf23-169">Amount with rounding to whole thousands</span></span> |
|----------|--------------------------|-----------------------------------------|
| <span data-ttu-id="9bf23-170">100</span><span class="sxs-lookup"><span data-stu-id="9bf23-170">100</span></span>      | <span data-ttu-id="9bf23-171">3,600</span><span class="sxs-lookup"><span data-stu-id="9bf23-171">3,600</span></span>                    | <span data-ttu-id="9bf23-172">4</span><span class="sxs-lookup"><span data-stu-id="9bf23-172">4</span></span>                                       |
| <span data-ttu-id="9bf23-173">200</span><span class="sxs-lookup"><span data-stu-id="9bf23-173">200</span></span>      | <span data-ttu-id="9bf23-174">3,700</span><span class="sxs-lookup"><span data-stu-id="9bf23-174">3,700</span></span>                    | <span data-ttu-id="9bf23-175">4</span><span class="sxs-lookup"><span data-stu-id="9bf23-175">4</span></span>                                       |
| <span data-ttu-id="9bf23-176">I alt</span><span class="sxs-lookup"><span data-stu-id="9bf23-176">Total</span></span>    | <span data-ttu-id="9bf23-177">7,300</span><span class="sxs-lookup"><span data-stu-id="9bf23-177">7,300</span></span>                    | <span data-ttu-id="9bf23-178">8</span><span class="sxs-lookup"><span data-stu-id="9bf23-178">8</span></span>                                       |

<span data-ttu-id="9bf23-179">Hvis du vil justere afrunding i en balance, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="9bf23-179">To adjust rounding in a balance sheet, follow these steps.</span></span>

1. <span data-ttu-id="9bf23-180">Klik på **Rækkedefinitioner** i Report Designer, og åbn derefter den rækkedefinition, der skal ændres.</span><span class="sxs-lookup"><span data-stu-id="9bf23-180">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="9bf23-181">Klik på **Afrundingsdifference** i menuen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="9bf23-181">On the **Edit** menu, click **Rounding Adjustment**.</span></span>
3. <span data-ttu-id="9bf23-182">I dialogboksen **Regulering af afrunding** skal du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="9bf23-182">In the **Rounding Adjustments** dialog box, enter the following values:</span></span>

    - <span data-ttu-id="9bf23-183">**Række til regulering af afrunding** – rækkekoden for den række, der skal reguleres for at afstemme balancen.</span><span class="sxs-lookup"><span data-stu-id="9bf23-183">**Rounding adjustment row** – The row code for the row that should be adjusted to balance the balance sheet.</span></span>
    - <span data-ttu-id="9bf23-184">**Række for samlede aktiver** – rækkekoden for den række i balancen, der indeholder de samlede aktiver.</span><span class="sxs-lookup"><span data-stu-id="9bf23-184">**Total assets row** – The row code for the row in the balance sheet that contains the total assets.</span></span>
    - <span data-ttu-id="9bf23-185">**Række for samlede passiver og egenkapital** – rækkekoden for den række i balancen, der indeholder de samlede passiver og egenkapital.</span><span class="sxs-lookup"><span data-stu-id="9bf23-185">**Total liabilities and equity row** – The row code for the row in the balance sheet that contains the total liabilities and equity.</span></span>
    - <span data-ttu-id="9bf23-186">**Reguleringsbeløbsgrænse** – et positivt heltal, der angiver grænsen for automatiske reguleringer.</span><span class="sxs-lookup"><span data-stu-id="9bf23-186">**Adjustment amount limit** – A positive whole number that specifies the limit on automatic adjustments.</span></span> <span data-ttu-id="9bf23-187">Dette beløb sammenlignes med den absolutte værdi for den faktiske afrundingsdifference.</span><span class="sxs-lookup"><span data-stu-id="9bf23-187">This amount is compared with the absolute value of the actual rounding difference.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9bf23-188">Rækkekoderne skal være knyttet til dine økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="9bf23-188">These row codes must be linked to your financial data.</span></span> <span data-ttu-id="9bf23-189">Rækken skal med andre ord have en dimensionsværdi i cellen **Link til økonomiske dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="9bf23-189">In other words, the row must have a dimension value in its **Link to Financial Dimensions** cell.</span></span> <span data-ttu-id="9bf23-190">Henvis **ikke** en beskrivelsesrække (**DESC**), beregnet række (**CALC**) eller sammenlagt (**TOT**) række.</span><span class="sxs-lookup"><span data-stu-id="9bf23-190">Do **not** reference a description (**DESC**), calculated (**CALC**), or totaled (**TOT**) row.</span></span>

<span data-ttu-id="9bf23-191">Beløbene i din balance er nu afstemt, hvis afrunding er slået til.</span><span class="sxs-lookup"><span data-stu-id="9bf23-191">The amounts in your balance sheet will now balance evenly when rounding is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="9bf23-192">Justeringsgrænsen anvendes baseret på indstillingen **Nøjagtighed i afrunding** for rapportdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9bf23-192">The adjustment limit is applied based on the **Rounding precision** option that is specified for the report definition.</span></span> <span data-ttu-id="9bf23-193">Hvis du for eksempel vælger at afrunde rapporten til tusinder og angiver **2** i feltet **Reguleringsbeløbsgrænse**, vises en advarselsmeddelelse, når værdien i feltet **Række til regulering af afrunding** øges eller reduceres med mere end $2.000.</span><span class="sxs-lookup"><span data-stu-id="9bf23-193">For example, if you round your report to thousands and enter **2** in the **Adjustment amount limit** field, you receive a warning message when the value in the **Rounding adjustment row** field increases or decreases by more than 2,000.</span></span>

## <a name="format-row-and-column-text"></a><span data-ttu-id="9bf23-194">Formatere række og kolonnetekst</span><span class="sxs-lookup"><span data-stu-id="9bf23-194">Format row and column text</span></span>
<span data-ttu-id="9bf23-195">Du kan tilpasse udseendet af dine rapporter ved at ændre skrifttyper og formatere tekst.</span><span class="sxs-lookup"><span data-stu-id="9bf23-195">You can customize the appearance of your reports by changing fonts and formatting text.</span></span> <span data-ttu-id="9bf23-196">I følgende afsnit beskrives, hvordan du kan formatere udseendet af rækker og kolonner i rapporter.</span><span class="sxs-lookup"><span data-stu-id="9bf23-196">The following sections explain how to format the appearance of rows and columns on reports.</span></span>

### <a name="manage-font-styles"></a><span data-ttu-id="9bf23-197">Administrere typografier</span><span class="sxs-lookup"><span data-stu-id="9bf23-197">Manage font styles</span></span>

<span data-ttu-id="9bf23-198">Du kan oprette og ændre typografier for rapporten.</span><span class="sxs-lookup"><span data-stu-id="9bf23-198">You can create and modify font styles for your report.</span></span> <span data-ttu-id="9bf23-199">Du kan derefter anvende disse typografier i dokumentet eller på en bestemt række eller kolonne i en rapport.</span><span class="sxs-lookup"><span data-stu-id="9bf23-199">You can then apply those styles to the document, or to a specific row or column on a report.</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="9bf23-200"><strong>Oprette en typografi</strong></span><span class="sxs-lookup"><span data-stu-id="9bf23-200"><strong>Create a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="9bf23-201">I menuen <strong>Formater</strong> i Report Designer skal du klikke på <strong>Typografier og formatering</strong>.</span><span class="sxs-lookup"><span data-stu-id="9bf23-201">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="9bf23-202">Klik på <strong>Ny</strong> i dialogboksen <strong>Typografier og formatering</strong>, og angiv derefter et entydigt navn for den nye typografi.</span><span class="sxs-lookup"><span data-stu-id="9bf23-202">In the <strong>Styles and Formatting</strong> dialog box, click <strong>New</strong>, and then enter a unique name for the new style.</span></span></li>
<li><span data-ttu-id="9bf23-203">Vælg de ønskede indstillinger for skrifttypen, og klik derefter på <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="9bf23-203">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="9bf23-204"><strong>Redigere en typografi</strong></span><span class="sxs-lookup"><span data-stu-id="9bf23-204"><strong>Modify a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="9bf23-205">I menuen <strong>Formater</strong> i Report Designer skal du klikke på <strong>Typografier og formatering</strong>.</span><span class="sxs-lookup"><span data-stu-id="9bf23-205">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="9bf23-206">Vælg en typografi, som du vil ændre, i dialogboksen <strong>Typografier og formatering</strong>, og klik derefter på <strong>Rediger</strong>.</span><span class="sxs-lookup"><span data-stu-id="9bf23-206">In the <strong>Styles and Formatting</strong> dialog box, select a style to modify, and then click <strong>Modify</strong>.</span></span></li>
<li><span data-ttu-id="9bf23-207">Vælg de ønskede indstillinger for skrifttypen, og klik derefter på <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="9bf23-207">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="9bf23-208"><strong>Anvende en typografi</strong></span><span class="sxs-lookup"><span data-stu-id="9bf23-208"><strong>Apply a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="9bf23-209">I Report Designer i en definition eller kolonnedefinition eller i sidehoveder og sidefødder skal du vælge en eller flere celler.</span><span class="sxs-lookup"><span data-stu-id="9bf23-209">In Report Designer, in a definition or column definition, or in headers and footers, select one or more cells.</span></span></li>
<li><span data-ttu-id="9bf23-210">Vælg en typografi på listen <strong>Type</strong> på værktøjslinjen.</span><span class="sxs-lookup"><span data-stu-id="9bf23-210">In the <strong>Style</strong> list on the toolbar, select a font style.</span></span></li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a><span data-ttu-id="9bf23-211">Formatere rækketekst</span><span class="sxs-lookup"><span data-stu-id="9bf23-211">Format row text</span></span>

<span data-ttu-id="9bf23-212">Den formatering, der er angivet i rækkedefinitionen, tilsidesætter den formatering, der er angivet i kolonnedefinitionen og rapportdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9bf23-212">The formatting that is specified in the row definition overrides any formatting that is specified in the column definition and the report definition.</span></span> <span data-ttu-id="9bf23-213">Du kan ændre tekstformatet ved hjælp af kontrolelementerne på formateringsværktøjslinjen.</span><span class="sxs-lookup"><span data-stu-id="9bf23-213">You can modify the text format by using the controls on the formatting toolbar.</span></span> <span data-ttu-id="9bf23-214">Disse kontrolelementer er standardkontrolelementer til Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9bf23-214">These controls are standard Microsoft Windows controls.</span></span>

1. <span data-ttu-id="9bf23-215">Åbn den rækkedefinition, der skal ændres, i Report Designer.</span><span class="sxs-lookup"><span data-stu-id="9bf23-215">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="9bf23-216">Marker de celler, der skal formateres.</span><span class="sxs-lookup"><span data-stu-id="9bf23-216">Select the cells to format.</span></span> <span data-ttu-id="9bf23-217">Du kan markere flere celler ved at holde Ctrl-tasten nede, mens du markerer cellen.</span><span class="sxs-lookup"><span data-stu-id="9bf23-217">To select multiple cells, hold down the Ctrl key while you select the cell.</span></span>
3. <span data-ttu-id="9bf23-218">Klik på værktøjslinjeknappen for det format, du vil anvende.</span><span class="sxs-lookup"><span data-stu-id="9bf23-218">Click the toolbar button of the format to apply.</span></span> <span data-ttu-id="9bf23-219">Hvis du for eksempel vil indrykke en række, skal du markere rækken og derefter klikke på **Forøg indrykning** ![Forøg indrykning](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Forøg indrykning") på værktøjslinjen.</span><span class="sxs-lookup"><span data-stu-id="9bf23-219">For example, to indent a row, select the row, and then click **Increase Indent** ![Increase Indent](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Increase Indent") on the toolbar.</span></span>

### <a name="adjust-columns-while-you-design-reports"></a><span data-ttu-id="9bf23-220">Justere kolonner, mens du designer rapporter</span><span class="sxs-lookup"><span data-stu-id="9bf23-220">Adjust columns while you design reports</span></span>

<span data-ttu-id="9bf23-221">For at gøre det lettere at få vist de kolonner, du arbejder på i rækkedefinitionen, kan du også justere bredden på en kolonne og skjule (minimere) eller vise kolonner i visningsruden.</span><span class="sxs-lookup"><span data-stu-id="9bf23-221">To make it easier to view the columns that you're working on in the row definition, you can adjust the width of a column, and can also hide (minimize) or show columns in the view pane.</span></span> <span data-ttu-id="9bf23-222">De ændringer, du foretager, påvirker kun visningen på skærmen af kolonnerne.</span><span class="sxs-lookup"><span data-stu-id="9bf23-222">The modifications that you make affect only the on-screen appearance of the columns.</span></span> <span data-ttu-id="9bf23-223">De påvirker ikke kolonneformateringen i rapporter.</span><span class="sxs-lookup"><span data-stu-id="9bf23-223">They don't affect the column formatting on reports.</span></span>

### <a name="change-the-width-of-a-column-in-the-view-pane"></a><span data-ttu-id="9bf23-224">Ændre bredden på en kolonne i visningsruden</span><span class="sxs-lookup"><span data-stu-id="9bf23-224">Change the width of a column in the view pane</span></span>

1. <span data-ttu-id="9bf23-225">Åbn den rækkedefinition, der skal ændres, i Report Designer.</span><span class="sxs-lookup"><span data-stu-id="9bf23-225">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="9bf23-226">Vælg **Kolonnebredde** i menuen **Formater**.</span><span class="sxs-lookup"><span data-stu-id="9bf23-226">On the **Format** menu, select **Column Width**.</span></span>
3. <span data-ttu-id="9bf23-227">Angiv en værdi i dialogboksen **Kolonnebredde**, og klik derefter på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9bf23-227">In the **Column Width** dialog box, enter a value, and then click **OK**.</span></span> <span data-ttu-id="9bf23-228">Du kan også trække i højre kant af cellen med kolonneoverskriften for at ændre kolonnens bredde.</span><span class="sxs-lookup"><span data-stu-id="9bf23-228">Alternatively, you can drag the right boundary of a column heading cell to change the width of the column.</span></span>

### <a name="hide-columns-in-the-view-pane"></a><span data-ttu-id="9bf23-229">Skjule kolonner i visningsruden</span><span class="sxs-lookup"><span data-stu-id="9bf23-229">Hide columns in the view pane</span></span>

1. <span data-ttu-id="9bf23-230">Åbn den rækkedefinition, der skal ændres, i Report Designer.</span><span class="sxs-lookup"><span data-stu-id="9bf23-230">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="9bf23-231">Markér den eller de kolonner, der skal minimeres.</span><span class="sxs-lookup"><span data-stu-id="9bf23-231">Select the column or columns to minimize.</span></span>
3. <span data-ttu-id="9bf23-232">Højreklik, og klik derefter på **Skjul**.</span><span class="sxs-lookup"><span data-stu-id="9bf23-232">Right-click, and then click **Hide**.</span></span>

### <a name="show-all-hidden-columns-in-the-view-pane"></a><span data-ttu-id="9bf23-233">Få vist alle skjulte kolonner i visningsruden</span><span class="sxs-lookup"><span data-stu-id="9bf23-233">Show all hidden columns in the view pane</span></span>

1. <span data-ttu-id="9bf23-234">Åbn den rækkedefinition, der skal ændres, i Report Designer.</span><span class="sxs-lookup"><span data-stu-id="9bf23-234">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="9bf23-235">Højreklik på den minimerede kolonne, der skal vises, og klik derefter på **Vis**.</span><span class="sxs-lookup"><span data-stu-id="9bf23-235">Right-click the minimized column to display, and then click **Unhide**.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="9bf23-236">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9bf23-236">Additional resources</span></span>

[<span data-ttu-id="9bf23-237">Økonomirapportering</span><span class="sxs-lookup"><span data-stu-id="9bf23-237">Financial reporting</span></span>](financial-reporting-intro.md)

