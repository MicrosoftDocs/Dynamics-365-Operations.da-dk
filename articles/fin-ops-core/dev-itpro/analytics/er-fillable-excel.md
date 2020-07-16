---
title: Designe en konfiguration til generering af dokumenter i Excel-format
description: Dette emne giver oplysninger om, hvordan du kan designe et ER-format (Electronic reporting) til at udfylde en Excel-skabelon og derefter generere udgående Excel-formatdokumenter.
author: NickSelin
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e889b08f10c5d0c95fed7c9e422340706bdd154a
ms.sourcegitcommit: 67ce81c57194afb26a04ae4c0b7509e0efa32afc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/14/2020
ms.locfileid: "3375807"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a><span data-ttu-id="f6c4e-103">Designe en konfiguration til generering af dokumenter i Excel-format</span><span class="sxs-lookup"><span data-stu-id="f6c4e-103">Design a configuration for generating documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f6c4e-104">Du kan designe en formatkonfiguration [ER (Electronic reporting)](general-electronic-reporting.md), der har et ER-[formatkomponent](general-electronic-reporting.md#FormatComponentOutbound), som du kan konfigurere til at generere et udgående dokument i et Microsoft Excel-projektmappeformat.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) format configuration that has an ER [format component](general-electronic-reporting.md#FormatComponentOutbound) that you can configure to generate an outbound document in a Microsoft Excel workbook format.</span></span> <span data-ttu-id="f6c4e-105">Specifikke ER-formatkomponenter skal bruges til dette formål.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-105">Specific ER format components must be used for this purpose.</span></span>

<span data-ttu-id="f6c4e-106">Hvis du vil vide mere om denne funktion, skal du følge trinnene i emnet, [Designe en konfiguration til generering af rapporter i OPENXML-format](tasks/er-design-reports-openxml-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f6c4e-106">To learn more about this feature, follow the steps in the topic, [Design a configuration for generating reports in OPENXML format](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="add-a-new-er-format"></a><span data-ttu-id="f6c4e-107">Tilføj et nyt ER-format</span><span class="sxs-lookup"><span data-stu-id="f6c4e-107">Add a new ER format</span></span>

<span data-ttu-id="f6c4e-108">Når du tilføjer en ny ER-formatkonfiguration for at generere et udgående dokument i et Excel-projektmappeformat, skal du enten vælge **Excel**-værdien for attributten **Formattype** for formatet eller lade attributten **Formattype** være tom.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-108">When you add a new ER format configuration to generate an outbound document in an Excel workbook format, you must either select the **Excel** value for the **Format type** attribute of the format or leave the **Format type** attribute blank.</span></span>

- <span data-ttu-id="f6c4e-109">Hvis du vælger **Excel**, kan du konfigurere formatet til kun at oprette et udgående dokument i Excel-format.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-109">If you select **Excel**, you can configure the format to generate an outbound document only in Excel format.</span></span>
- <span data-ttu-id="f6c4e-110">Hvis du lader attributten være tom, kan du konfigurere formatet til at generere et udgående dokument i et hvilket som helst format, der understøttes af ER-strukturen.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-110">If you leave the attribute blank, you can configure the format to generate an outbound document in any format that is supported by the ER framework.</span></span>

<span data-ttu-id="f6c4e-111">Hvis du vil konfigurere ER-formatkomponenten af konfigurationen, skal du vælge **Designer** i handlingsruden og åbne ER-formatkomponenten for redigering i ER-operationsdesigner.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-111">To configure the ER format component of the configuration, select **Designer** on the Action Pane, and open the ER format component for editing in the ER Operation designer.</span></span>

![Siden Konfigurationer](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a><span data-ttu-id="f6c4e-113">Excel-filkomponent</span><span class="sxs-lookup"><span data-stu-id="f6c4e-113">Excel file component</span></span>

### <a name="manual-entry"></a><span data-ttu-id="f6c4e-114">Manuel indtastning</span><span class="sxs-lookup"><span data-stu-id="f6c4e-114">Manual entry</span></span>

<span data-ttu-id="f6c4e-115">Du skal føje en **Excel \\Fil**-komponent til det konfigurerede ER-format, hvis du vil generere et udgående dokument i Excel-format.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-115">You must add an **Excel\\File** component to the configured ER format to generate an outbound document in Excel format.</span></span>

![Excel-filkomponent](./media/er-excel-format-add-file-component.png)

<span data-ttu-id="f6c4e-117">Hvis du vil angive layoutet for det udgående dokument, skal du vedhæfte en Excel-projektmappe med filtypenavnet .xlsx til **Excel-\\fil**-komponenten som skabelon til udgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-117">To specify the layout of the outbound document, attach an Excel workbook that has the .xlsx extension to the **Excel\\File** component as the template for outbound documents.</span></span>

> [!NOTE]
> <span data-ttu-id="f6c4e-118">Når du manuelt tilknytter en skabelon, skal du bruge en [dokumenttype](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types), der er konfigureret til dette formål i [ER-parametrene](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span><span class="sxs-lookup"><span data-stu-id="f6c4e-118">When you manually attach a template, you must use a [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) that has been configured for that purpose in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span></span>

![Føje en tilknytning til Excel\Fil-komponenten](./media/er-excel-format-add-file-component2.png)

<span data-ttu-id="f6c4e-120">Hvis du vil angive, hvordan den tilknyttede skabelon skal udfyldes, når du kører det konfigurerede ER-format, skal du føje indlejrede komponenter **Ark**, **Område** og **Celle** til komponenten **Excel\\Fil**.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-120">To specify how the attached template will be filled in when you run the configured ER format, you must add nested **Sheet**, **Range**, and **Cell** components to the **Excel\\File** component.</span></span> <span data-ttu-id="f6c4e-121">Alle indlejrede komponenter skal knyttes til et navngivet element i Excel.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-121">Each nested component must be associated with an Excel named item.</span></span>

### <a name="template-import"></a><span data-ttu-id="f6c4e-122">Skabelonimport</span><span class="sxs-lookup"><span data-stu-id="f6c4e-122">Template import</span></span>

<span data-ttu-id="f6c4e-123">Du kan vælge **Importér fra Excel** under fanen **Importer** i handlingsruden for at importere en ny skabelon til et tomt ER-format.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-123">You can select **Import from Excel** on the **Import** tab of the Action Pane to import a new template into a blank ER format.</span></span> <span data-ttu-id="f6c4e-124">I dette eksempel oprettes der automatisk en **Excel\\Fil**-komponent, og den importerede skabelon knyttes til den.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-124">In this example, an **Excel\\File** component will be created automatically, and the imported template will be attached to it.</span></span> <span data-ttu-id="f6c4e-125">Alle nødvendige ER-komponenter oprettes automatisk, baseret på listen over de Excel-navngivne elementer, der registreres.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-125">All required ER components will also be created automatically, based on the list of Excel named items that are discovered.</span></span>

![Vælge Importér fra Excel](./media/er-excel-format-import-template.png)

> [!NOTE]
> <span data-ttu-id="f6c4e-127">Hvis du vil oprette det valgfrie **Ark**-element i det redigerbare ER-format, skal du angive indstillingen **Opret Excel-arkformatelement** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-127">If you want to create the optional **Sheet** element in the editable ER format, set the **Create Excel Sheet format element** option to **Yes**.</span></span>

## <a name="sheet-component"></a><span data-ttu-id="f6c4e-128">Arkkomponent</span><span class="sxs-lookup"><span data-stu-id="f6c4e-128">Sheet component</span></span>

<span data-ttu-id="f6c4e-129">**A**-komponenten angiver et regneark i den tilknyttede Excel-projektmappe, der skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-129">The **Sheet** component indicates a worksheet of the attached Excel workbook that must be filled in.</span></span> <span data-ttu-id="f6c4e-130">Navnet på regnearket i en Excel-skabelon er defineret i egenskaben **Ark** for denne komponent.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-130">The name of the worksheet in an Excel template is defined in the **Sheet** property of this component.</span></span>

> [!NOTE]
> <span data-ttu-id="f6c4e-131">Denne komponent er valgfri for Excel-projektmapper, der indeholder et enkelt regneark.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-131">This component is optional for Excel workbooks that contain a single worksheet.</span></span>

<span data-ttu-id="f6c4e-132">Under fanen **Tilknytning** i ER-operationsdesigneren kan du konfigurere egenskaben **Aktiveret** for en **Ark**-komponent for at angive, om komponenten skal placeres i et genereret dokument:</span><span class="sxs-lookup"><span data-stu-id="f6c4e-132">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Sheet** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="f6c4e-133">Hvis et udtryk af egenskaben **Aktiveret** er konfigureret til at returnere **Sand** på kørselstidspunktet, eller, hvis der slet ikke er konfigureret et udtryk, vil det relevante regneark blive taget med i det genererede dokument.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-133">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate worksheet will be put in the generated document.</span></span>
- <span data-ttu-id="f6c4e-134">Hvis et udtryk af egenskaben **Aktiveret** er konfigureret til at returnere **Falsk** på kørselstidspunktet, indeholder det genererede dokument ikke et regneark.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-134">If an expression of the **Enabled** property is configured to return **False** at runtime, the generated document won't contain a worksheet.</span></span>

![Eksempel på en arkkomponent](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a><span data-ttu-id="f6c4e-136">Områdekomponent</span><span class="sxs-lookup"><span data-stu-id="f6c4e-136">Range component</span></span>

<span data-ttu-id="f6c4e-137">Komponenten **Område** angiver et Excel-område, der skal styres af denne ER-komponent.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-137">The **Range** component indicates an Excel range that must be controlled by this ER component.</span></span> <span data-ttu-id="f6c4e-138">Navnet på området er defineret i **Excel-området** for denne komponent.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-138">The name of the range is defined in the **Excel range** property of this component.</span></span>

<span data-ttu-id="f6c4e-139">Egenskaben **Replikeringsretning** angiver, om og hvordan området skal gentages i et genereret dokument:</span><span class="sxs-lookup"><span data-stu-id="f6c4e-139">The **Replication direction** property specifies whether and how the range will be repeated in a generated document:</span></span>

- <span data-ttu-id="f6c4e-140">Hvis egenskaben **Replikeringsretning** er angivet til **Ingen replikering**, gentages det relevante Excel-område ikke i det genererede dokument.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-140">If the **Replication direction** property is set to **No replication**, the appropriate Excel range won't be repeated in the generated document.</span></span>
- <span data-ttu-id="f6c4e-141">Hvis egenskaben **Replikeringsretning** er angivet til **Lodret**, gentages det relevante Excel-område i det genererede dokument.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-141">If the **Replication direction** property is set to **Vertical**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="f6c4e-142">Alle replikerede områder placeres under det oprindelige område i en Excel-skabelon.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-142">Every replicated range is put below the original range in an Excel template.</span></span> <span data-ttu-id="f6c4e-143">Antallet af gentagelser defineres af antallet af poster i en datakilde for den **Postlistetype**, der er bundet til denne ER-komponent.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-143">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>
- <span data-ttu-id="f6c4e-144">Hvis egenskaben **Replikeringsretning** er angivet til **Vandret**, gentages det relevante Excel-område i det genererede dokument.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-144">If the **Replication direction** property is set to **Horizontal**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="f6c4e-145">Alle replikerede områder placeres til højre for det oprindelige område i en Excel-skabelon.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-145">Every replicated range is put to the right of the original range in an Excel template.</span></span> <span data-ttu-id="f6c4e-146">Antallet af gentagelser defineres af antallet af poster i en datakilde for den **Postlistetype**, der er bundet til denne ER-komponent.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-146">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>

<span data-ttu-id="f6c4e-147">Hvis du vil vide mere om vandret replikering, skal du følge trinnene i [Brug vandrette, udvidelige områder til dynamisk at tilføje kolonner i Excel-rapporter](tasks/er-horizontal-1.md).</span><span class="sxs-lookup"><span data-stu-id="f6c4e-147">To learn more about horizontal replication, follow the steps in [Use horizontally expandable ranges to dynamically add columns in Excel reports](tasks/er-horizontal-1.md).</span></span>

<span data-ttu-id="f6c4e-148">Komponenten **Område** kan have andre indlejrede ER-komponenter, der bruges til at angive værdier i de relevante navngivne Excel-områder.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-148">The **Range** component can have other nested ER components that are used to enter values in the appropriate Excel named ranges.</span></span>

- <span data-ttu-id="f6c4e-149">Hvis en komponent i gruppen **Tekst** bruges til at angive værdier, indtastes værdien i et Excel-område som en tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-149">If any component of the **Text** group is used to enter values, the value is entered in an Excel range as a text value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f6c4e-150">Du kan bruge dette mønster til at formatere angivne værdier på basis af den landestandard, der er defineret i programmet.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-150">Use this pattern to format entered values based on the locale that is defined in the application.</span></span>

- <span data-ttu-id="f6c4e-151">Hvis komponenten **Celle** i gruppen **Excel** bruges til at angive værdier, indtastes værdien i et Excel-område som en værdi af den datatype, der er defineret af bindingen for den pågældende **Celle**-komponent (f.eks. **Streng**, **Reelt tal** eller **Heltal**).</span><span class="sxs-lookup"><span data-stu-id="f6c4e-151">If the **Cell** component of the **Excel** group is used to enter values, the value is entered in an Excel range as a value of the data type that is defined by the binding of that **Cell** component (for example, **String**, **Real**, or **Integer**).</span></span>

    > [!NOTE]
    > <span data-ttu-id="f6c4e-152">Brug dette mønster til at gøre Excel-programmet i stand til at formatere angivne værdier på basis af landestandarden på den lokale computer, der åbner det udgående dokument.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-152">Use this pattern to enable the Excel application to format entered values based on the locale of the local computer that opens the outbound document.</span></span>

<span data-ttu-id="f6c4e-153">Under fanen **Tilknytning** i ER-operationsdesigneren kan du konfigurere egenskaben **Aktiveret** for en **Område**-komponent for at angive, om komponenten skal placeres i et genereret dokument:</span><span class="sxs-lookup"><span data-stu-id="f6c4e-153">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Range** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="f6c4e-154">Hvis et udtryk af egenskaben **Aktiveret** er konfigureret til at returnere **Sand** på kørselstidspunktet, eller, hvis der slet ikke er konfigureret et område, vil det relevante område blive udfyldt i det genererede dokument.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-154">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate range will be filled in in the generated document.</span></span>
- <span data-ttu-id="f6c4e-155">Hvis et udtryk af egenskaben **Aktiveret** er konfigureret til at returnere **Falsk** på kørselstidspunktet, og hvis dette område ikke repræsenterer rækker eller kolonner i deres helhed, vil det relevante område ikke blive udfyldt i det genererede dokument.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-155">If an expression of the **Enabled** property is configured to return **False** at runtime, and if this range doesn't represent the entire rows or columns, the appropriate range won't be filled in in the generated document.</span></span>
- <span data-ttu-id="f6c4e-156">Hvis et udtryk af egenskaben **Aktiveret** er konfigureret til at returnere **Falsk** på kørselstidspunktet, og hvis dette område repræsenterer rækker eller kolonner i deres helhed, vil det generede dokument indeholde disse rækker og kolonner som skjulte rækker og kolonner.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-156">If an expression of the **Enabled** property is configured to return **False** at runtime, and this range represents the entire rows or columns, the generated document will contain those rows and columns as hidden rows and columns.</span></span>

## <a name="cell-component"></a><span data-ttu-id="f6c4e-157">Cellekomponent</span><span class="sxs-lookup"><span data-stu-id="f6c4e-157">Cell component</span></span>

<span data-ttu-id="f6c4e-158">Komponenten **Celle** bruges til at udfylde navngivne Excel-celler, -figurer og -billeder.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-158">The **Cell** component is used to fill in Excel named cells, shapes, and pictures.</span></span> <span data-ttu-id="f6c4e-159">Hvis du vil angive, at et navngivet Excel-objekt skal være udfyldt af **Celle** ER-komponent, skal du angive navnet på det pågældende objekt i egenskaben **Excel-område** for komponenten **Celle**.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-159">To indicate an Excel named object that must be filled in by a **Cell** ER component, you must specify the name of that object in the **Excel range** property of the **Cell** component.</span></span>

<span data-ttu-id="f6c4e-160">Under fanen **Tilknytning** i ER-operationsdesigneren kan du konfigurere egenskaben **Aktiveret** for en **Celle**-komponent for at angive, om objektet skal udfyldes i et genereret dokument:</span><span class="sxs-lookup"><span data-stu-id="f6c4e-160">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Cell** component to specify whether the object must be filled in in a generated document:</span></span>

- <span data-ttu-id="f6c4e-161">Hvis et udtryk af egenskaben **Aktiveret** er konfigureret til at returnere **Sand** på kørselstidspunktet, eller, hvis der slet ikke er konfigureret et objekt, vil det relevante område blive udfyldt i det genererede dokument.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-161">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate object will be filled in in the generated document.</span></span> <span data-ttu-id="f6c4e-162">Bindingen for denne **Celle**-komponent angiver en værdi, der placeres i det relevante objekt.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-162">The binding of this **Cell** component specifies a value that is put in the appropriate object.</span></span>
- <span data-ttu-id="f6c4e-163">Hvis et udtryk af egenskaben **Aktiveret** er konfigureret til at returnere **Falsk** på kørselstidspunktet, udfyldes det relevante objekt ikke i det genererede dokument.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-163">If an expression of the **Enabled** property is configured to return **False** at runtime, the appropriate object won't be filled in in the generated document.</span></span>

<span data-ttu-id="f6c4e-164">Når en **Celle**-komponent er konfigureret til at angive en værdi i en celle, kan den bindes til en datakilde, der returnerer værdien af en primitiv datatype (f.eks. **Streng**, **Reelt tal** eller **Heltal**).</span><span class="sxs-lookup"><span data-stu-id="f6c4e-164">When a **Cell** component is configured to enter a value in a cell, it can be bound with a data source that returns the value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="f6c4e-165">I dette tilfælde indtastes værdien i cellen som en værdi af samme datatype.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-165">In this case, the value is entered in the cell as a value of the same data type.</span></span>

<span data-ttu-id="f6c4e-166">Når en **Celle**-komponent er konfigureret til at angive en værdi i Excel-figur, kan den bindes til en datakilde, der returnerer en værdi af en primitiv datatype (f.eks. **Streng**, **Reelt tal** eller **Heltal**).</span><span class="sxs-lookup"><span data-stu-id="f6c4e-166">When a **Cell** component is configured to enter a value in an Excel shape, it can be bound with a data source that returns a value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="f6c4e-167">I dette tilfælde indtastes værdien i Excel-figuren som tekst med dem pågældende figur.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-167">In this case, the value is entered in the Excel shape as the text of that shape.</span></span> <span data-ttu-id="f6c4e-168">Når det gælder værdier af datatyper, der ikke er **strenge**, udføres konverteringen til tekst automatisk.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-168">For values of data types that aren't **String**, the conversion to text is done automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="f6c4e-169">Du kan konfigurere en **Celle**-komponent, så den kun udfyldes på en figur i de tilfælde, hvor egenskaben figurtekst understøttes.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-169">You can configure a **Cell** component to fill in a shape only in cases where a shape text property is supported.</span></span>

<span data-ttu-id="f6c4e-170">Når en **Celle**-komponent er konfigureret til at angive en værdi i et Excel-billede, kan den bindes til en datakilde, der returnerer en værdi af en datatype **Container**, der repræsenterer et billede i binært format.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-170">When a **Cell** component is configured to enter a value in an Excel picture, it can be bound with a data source that returns a value of the **Container** data type that represents an image in binary format.</span></span> <span data-ttu-id="f6c4e-171">I dette tilfælde angives værdien i Excel-billedet som et billede.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-171">In this case, the value is entered in the Excel picture as an image.</span></span>

> [!NOTE]
> <span data-ttu-id="f6c4e-172">Alle Excel-billeder og -figurer betragtes som forankret af dets øverste venstre hjørne til en bestemt Excel-celle eller et specifikt celleområde.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-172">Every Excel picture and shape is considered to be anchored by its upper-left corner to a specific Excel cell or range.</span></span> <span data-ttu-id="f6c4e-173">Hvis du vil replikere et Excel-billede eller -figur, skal du konfigurere den celle eller det område, det eller den er forankret til, som en replikeret celle eller et celleområde.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-173">If you want to replicate an Excel picture or shape, you must configure the cell or range that it's anchored to as a replicated cell or range.</span></span>

<span data-ttu-id="f6c4e-174">Du kan få mere at vide om, hvordan du integrerer billeder og figurer, under [Integrere billeder og figurer i et dokumenter, du genererer ved hjælp af ER](electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="f6c4e-174">To learn more about how to embed images and shapes, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="page-break-component"></a><span data-ttu-id="f6c4e-175">Komponenten Sideskift</span><span class="sxs-lookup"><span data-stu-id="f6c4e-175">Page break component</span></span>

<span data-ttu-id="f6c4e-176">Komponenten **Sideskift** tvinger Excel til at starte en ny side.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-176">The **PageBreak** component forces Excel to start a new page.</span></span> <span data-ttu-id="f6c4e-177">Denne komponent er ikke påkrævet, når du vil bruge Excels standardsideinddeling, men du bør bruge den, når du vil have, at Excel skal følge dit ER-format til opbygning af sideinddeling.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-177">This component isn't required when you want to use Excel's default paging, but you should use it when you want Excel to follow your ER format to structure paging.</span></span>

## <a name="edit-an-added-er-format"></a><span data-ttu-id="f6c4e-178">Redigere et tilføjet ER-format</span><span class="sxs-lookup"><span data-stu-id="f6c4e-178">Edit an added ER format</span></span>

### <a name="update-a-template"></a><span data-ttu-id="f6c4e-179">Opdatere en skabelon</span><span class="sxs-lookup"><span data-stu-id="f6c4e-179">Update a template</span></span>

<span data-ttu-id="f6c4e-180">Du kan vælge **Opdater fra Excel** under fanen **Importer** i handlingsruden for at importere en opdateret skabelon til et redigerbart ER-format.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-180">You can select **Update from Excel** on the **Import** tab of the Action Pane to import an updated template into an editable ER format.</span></span> <span data-ttu-id="f6c4e-181">Under denne proces erstattes en skabelon for den valgte komponent **Excel\\Fil** med en ny skabelon.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-181">During this process, a template of the selected **Excel\\File** component will be replaced by a new template.</span></span> <span data-ttu-id="f6c4e-182">Indholdet af det redigerbare ER-format synkroniseres med indholdet af den opdaterede ER-skabelon.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-182">The content of the editable ER format will be synced with the content of the updated ER template.</span></span>

- <span data-ttu-id="f6c4e-183">Der oprettes automatisk en ny ER-formatkomponent for alle Excel-navne, hvis ER-formatkomponenten ikke findes i det redigerbare format.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-183">A new ER format component will automatically be created for every Excel name if the ER format component isn't found in the editable format.</span></span>
- <span data-ttu-id="f6c4e-184">Alle ER-formatkomponenter slettes fra det redigerbare ER-format, hvis det rette Excel-navn ikke findes.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-184">Every ER format component will be deleted from the editable ER format if the appropriate Excel name isn't found for it.</span></span>

> [!NOTE]
> <span data-ttu-id="f6c4e-185">Angiv indstillingen **Opret Excel-arkformatelement** til **Ja**, hvis du vil oprette det valgfri **Ark**-element i det redigerbare ER-format.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-185">Set the **Create Excel Sheet format element** option to **Yes** if you want to create the optional **Sheet** element in the editable ER format.</span></span>
>
> <span data-ttu-id="f6c4e-186">Hvis det redigerbare ER-format oprindeligt indeholdte **Ark**-elementer, anbefales det, at du angiver indstillingen **Opret Excel-arkformatelement** til **Ja**, når du importerer en opdateret skabelon.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-186">If the editable ER format originally contained **Sheet** elements, we recommend that you set the **Create Excel Sheet format element** option to **Yes** when you import an updated template.</span></span> <span data-ttu-id="f6c4e-187">Ellers oprettes alle indlejrede elementer i det oprindelige **Ark**-element fra bunden.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-187">Otherwise, all nested elements of the original **Sheet** element will be created from scratch.</span></span> <span data-ttu-id="f6c4e-188">Derfor går alle bindinger af de genoprettede formatelementer tabt i det opdaterede ER-format.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-188">Therefore, all bindings of the re-created format elements will be lost in the updated ER format.</span></span>

![Indstillingen Opret Excel-arkformatelement i dialogboksen Opdater fra Excel](./media/er-excel-format-update-template.png)

<span data-ttu-id="f6c4e-190">Hvis du vil vide mere om denne funktion, skal du udføre trinnene i [Redigere elektronisk rapporteringsformat ved at genanvende Excel-skabeloner](modify-electronic-reporting-format-reapply-excel-template.md).</span><span class="sxs-lookup"><span data-stu-id="f6c4e-190">To learn more about this feature, follow the steps in [Modify Electronic reporting formats by reapplying Excel templates](modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

## <a name="validate-an-er-format"></a><span data-ttu-id="f6c4e-191">Validere et ER-format</span><span class="sxs-lookup"><span data-stu-id="f6c4e-191">Validate an ER format</span></span>

<span data-ttu-id="f6c4e-192">Når du validerer et ER-format, der kan redigeres, sker der en konsistenskontrol for at sikre, at Excel-navnet findes i den Excel-skabelon, der aktuelt bruges.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-192">When you validate an ER format that can be edited, a consistency check is done to make sure that the Excel name is present in the Excel template that is currently used.</span></span> <span data-ttu-id="f6c4e-193">Du får besked om eventuelle uoverensstemmelser.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-193">You will be notified about any inconsistencies.</span></span> <span data-ttu-id="f6c4e-194">Ved visse inkonsistenser tilbydes muligheden for at rette problemer automatisk.</span><span class="sxs-lookup"><span data-stu-id="f6c4e-194">For some inconsistencies, the option to automatically fix issues will be offered.</span></span>

![Validering og fejlmeddelelse](./media/er-excel-format-validate.png)


## <a name="additional-resources"></a><span data-ttu-id="f6c4e-196">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f6c4e-196">Additional resources</span></span>

[<span data-ttu-id="f6c4e-197">Oversigt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="f6c4e-197">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="f6c4e-198">Designe en konfiguration til generering af rapporter i OPENXML-format</span><span class="sxs-lookup"><span data-stu-id="f6c4e-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks\er-design-reports-openxml-2016-11.md)

[<span data-ttu-id="f6c4e-199">Redigere elektroniske rapporteringsformater ved at genanvende Excel-skabeloner</span><span class="sxs-lookup"><span data-stu-id="f6c4e-199">Modify Electronic reporting formats by reapplying Excel templates</span></span>](modify-electronic-reporting-format-reapply-excel-template.md)

[<span data-ttu-id="f6c4e-200">Brug vandrette områder, der kan udvides, til at tilføje kolonner i Excel-rapporter dynamisk</span><span class="sxs-lookup"><span data-stu-id="f6c4e-200">Use horizontally expandable ranges to dynamically add columns in Excel reports</span></span>](tasks/er-horizontal-1.md)

[<span data-ttu-id="f6c4e-201">Integrere billeder og figurer i de dokumenter, du opretter ved hjælp af ER</span><span class="sxs-lookup"><span data-stu-id="f6c4e-201">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md)

[<span data-ttu-id="f6c4e-202">Konfigurer Elektronisk rapportering (ER) for at trække data over i Power BI</span><span class="sxs-lookup"><span data-stu-id="f6c4e-202">Configure Electronic reporting (ER) to pull data into Power BI</span></span>](general-electronic-reporting-report-configuration-get-data-powerbi.md)