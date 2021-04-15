---
title: Tilføje analyser til arbejdsområder ved hjælp af Power BI Embedded
description: Dette emne viser, hvordan du kan integrere en Power BI-rapport under fanen Analyser i et arbejdsområde.
author: RichdiMSFT
ms.date: 06/21/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 8e82c9a5ff4b6d7db1a808e5a94206628cdf0930
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754592"
---
# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a><span data-ttu-id="31b07-103">Tilføje analyser til arbejdsområder ved hjælp af Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="31b07-103">Add analytics to workspaces by using Power BI Embedded</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="31b07-104">Denne funktion understøttes i Finance and Operations (version 7.2 og nyere).</span><span class="sxs-lookup"><span data-stu-id="31b07-104">This feature is supported in Finance and Operations (version 7.2 and later).</span></span>

## <a name="introduction"></a><span data-ttu-id="31b07-105">Introduktion</span><span class="sxs-lookup"><span data-stu-id="31b07-105">Introduction</span></span>
<span data-ttu-id="31b07-106">Dette emne viser, hvordan du kan integrere en Microsoft Power BI-rapport under fanen **Analyser** i et arbejdsområde.</span><span class="sxs-lookup"><span data-stu-id="31b07-106">This topic shows how to embed a Microsoft Power BI report on the **Analytics** tab of a workspace.</span></span> <span data-ttu-id="31b07-107">I det eksempel, der er angivet her, skal vi udvide arbejdsområdet **Reservationsstyring** i Flådeadministration-programmet for at integrere et analysearbejdsområde under fanen **Analyser**.</span><span class="sxs-lookup"><span data-stu-id="31b07-107">For the example that is given here, we will extend the **Reservation management** workspace in the Fleet Management application to embed an analytical workspace on an **Analytics** tab.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="31b07-108">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="31b07-108">Prerequisites</span></span>
+ <span data-ttu-id="31b07-109">Adgang til et udviklermiljø, der kører platformsopdatering 8 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="31b07-109">Access to a developer environment that runs Platform update 8 or later.</span></span>
+ <span data-ttu-id="31b07-110">En analyserapport (.pbix-fil), der er oprettet ved hjælp af Microsoft Power BI Desktop, og som har en datamodel, der leveres fra databasen Enhedslager.</span><span class="sxs-lookup"><span data-stu-id="31b07-110">An analytical report (.pbix file) that was created by using Microsoft Power BI Desktop, and that has a data model that is sourced from the Entity store database.</span></span>

## <a name="overview"></a><span data-ttu-id="31b07-111">Overblik</span><span class="sxs-lookup"><span data-stu-id="31b07-111">Overview</span></span>
<span data-ttu-id="31b07-112">Uanset om du udvider et eksisterende arbejdsområde i et program eller indfører et nyt arbejdsområde, du selv har oprettet, kan du bruge integrerede analysevisninger til at levere nyttig indsigt og interaktive visninger af dine forretningsdata.</span><span class="sxs-lookup"><span data-stu-id="31b07-112">Whether you extend an existing application workspace or introduce a new workspace of your own, you can use embedded analytical views to deliver insightful and interactive views of your business data.</span></span> <span data-ttu-id="31b07-113">Tilføjelse af en fane til analyse i et arbejdsområdet består af fire trin.</span><span class="sxs-lookup"><span data-stu-id="31b07-113">The process for adding an analytical workspace tab has four steps.</span></span>

1. <span data-ttu-id="31b07-114">Tilføj en .pbix-fil som en Dynamics 365-ressource.</span><span class="sxs-lookup"><span data-stu-id="31b07-114">Add a .pbix file as a Dynamics 365 resource.</span></span>
2. <span data-ttu-id="31b07-115">Definer en analysefane i et arbejdsområde.</span><span class="sxs-lookup"><span data-stu-id="31b07-115">Define an analytical workspace tab.</span></span>
3. <span data-ttu-id="31b07-116">Integrer .pbix-ressourcen under fanen i arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="31b07-116">Embed the .pbix resource on the workspace tab.</span></span>
4. <span data-ttu-id="31b07-117">Valgfrit: Tilføj udvidelser for at tilpasse visningen.</span><span class="sxs-lookup"><span data-stu-id="31b07-117">Optional: Add extensions to customize the view.</span></span>

> [!NOTE]
> <span data-ttu-id="31b07-118">Du kan finde flere oplysninger om oprettelse af analyserapporter i [Introduktion til Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="31b07-118">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span></span> <span data-ttu-id="31b07-119">Denne side er en fremragende kilde til indsigt, der kan hjælpe dig med at oprette effektive analyserapporteringsløsninger.</span><span class="sxs-lookup"><span data-stu-id="31b07-119">This page is a great source for insights that can help you create compelling analytical reporting solutions.</span></span>

## <a name="add-a-pbix-file-as-a-resource"></a><span data-ttu-id="31b07-120">Tilføje en .pbix-fil som en ressource</span><span class="sxs-lookup"><span data-stu-id="31b07-120">Add a .pbix file as a resource</span></span>
<span data-ttu-id="31b07-121">Før du begynder, skal du oprette eller anskaffe den Power BI-rapport, du vil integrere i arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="31b07-121">Before you begin, you must create or obtain the Power BI report that you will embed in the workspace.</span></span> <span data-ttu-id="31b07-122">Du kan finde flere oplysninger om oprettelse af analyserapporter i [Introduktion til Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="31b07-122">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span></span>

<span data-ttu-id="31b07-123">Følg disse trin for at tilføje en .pbix-fil som en Visual Studio-projektgenstand.</span><span class="sxs-lookup"><span data-stu-id="31b07-123">Follow these steps to add a .pbix file as a Visual Studio project artifact.</span></span>

1. <span data-ttu-id="31b07-124">Opret et nyt projekt i den relevante model.</span><span class="sxs-lookup"><span data-stu-id="31b07-124">Create a new project in the appropriate model.</span></span>
2. <span data-ttu-id="31b07-125">Vælg projektet i Solution Explorer, højreklik og vælg derefter **Tilføj** \> **Nyt element**.</span><span class="sxs-lookup"><span data-stu-id="31b07-125">In Solution Explorer, select the project, right-click, and then select **Add** \> **New Item**.</span></span>
3. <span data-ttu-id="31b07-126">I dialogboksen **Tilføj nyt element** under **Operationsgenstande** skal du vælge skabelonen **Ressource**.</span><span class="sxs-lookup"><span data-stu-id="31b07-126">In the **Add New Item** dialog box, under **Operations Artifacts**, select the **Resource** template.</span></span>
4. <span data-ttu-id="31b07-127">Angiv et navn, der skal bruges til at referere til rapporten i X ++-metadata, og klik derefter på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="31b07-127">Enter a name that will be used to reference the report in X++ metadata, and then click **Add**.</span></span>

    ![Dialogboksen Tilføj nyt element](media/analytical-workspace-add.png)

5. <span data-ttu-id="31b07-129">Find .pbix filen med definitionen af analyserapporten, og klik derefter på **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="31b07-129">Find the .pbix file that contains the definition of the analytical report, and then click **Open**.</span></span>

    ![Dialogboksen Vælg en ressourcefil](media/analytical-workspace-select-resource.png)

<span data-ttu-id="31b07-131">Nu, hvor du har tilføjet .pbix filen som en ressource i Dynamics 365, kan du integrere rapporterne i arbejdsområder og tilføje direkte hyperlinks ved hjælp af menupunkter.</span><span class="sxs-lookup"><span data-stu-id="31b07-131">Now that you've added the .pbix file as a Dynamics 365 resource, you can embed the reports in workspaces and add direct links by using menu items.</span></span>

## <a name="add-a-tab-control-to-an-application-workspace"></a><span data-ttu-id="31b07-132">Føje et fanekontrolelement til et arbejdsområde i et program</span><span class="sxs-lookup"><span data-stu-id="31b07-132">Add a tab control to an application workspace</span></span>
<span data-ttu-id="31b07-133">I dette eksempel skal vi udvide arbejdsområdet **Reservationsstyring** i Flådeadministration-modellen ved at tilføje fanen **Analyser** til definitionen af formularen **FMClerkWorkspace**.</span><span class="sxs-lookup"><span data-stu-id="31b07-133">In this example, we will extend the **Reservation management** workspace in the Fleet Management model by adding the **Analytics** tab to the definition of the **FMClerkWorkspace** form.</span></span>

<span data-ttu-id="31b07-134">Følgende illustration viser, hvordan formularen **FMClerkWorkspace** ser ud i designeren i Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="31b07-134">The following illustration shows what the **FMClerkWorkspace** form looks like in the designer in Microsoft Visual Studio.</span></span>

![FMClerkWorkspace-formular før ændringer](media/analytical-workspace-definition-before.png)

<span data-ttu-id="31b07-136">Følg disse trin for at udvide formulardefinitionen for arbejdsområdet **Reservationsstyring**.</span><span class="sxs-lookup"><span data-stu-id="31b07-136">Follow these steps to extend the form definition for the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="31b07-137">Åbn formulardesigneren for at udvide designdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="31b07-137">Open the form designer to extend the design definition.</span></span>
2. <span data-ttu-id="31b07-138">Vælg det øverste element **Design | Pattern: Workspace Operational** i designdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="31b07-138">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
3. <span data-ttu-id="31b07-139">Højreklik, og vælg derefter **Ny** \> **Fane** for at tilføje et nyt kontrolelement med navnet **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="31b07-139">Right-click, and then select **New** \> **Tab** to add a new control that is named **FormTabControl1**.</span></span>
4. <span data-ttu-id="31b07-140">Vælg **FormTabControl1** i formulardesigneren.</span><span class="sxs-lookup"><span data-stu-id="31b07-140">In the form designer, select **FormTabControl1**.</span></span>
5. <span data-ttu-id="31b07-141">Højreklik, og vælg derefter **New Tab Page** for at tilføje en ny fane.</span><span class="sxs-lookup"><span data-stu-id="31b07-141">Right-click, and then select **New Tab Page** to add a new tab page.</span></span>
6. <span data-ttu-id="31b07-142">Giv fanesiden et nyt, sigende navn, f.eks. **Arbejdsområde**.</span><span class="sxs-lookup"><span data-stu-id="31b07-142">Rename the tab page to something meaningful, such as **Workspace**.</span></span>
7. <span data-ttu-id="31b07-143">Vælg **FormTabControl1** i formulardesigneren.</span><span class="sxs-lookup"><span data-stu-id="31b07-143">In the form designer, select **FormTabControl1**.</span></span>
8. <span data-ttu-id="31b07-144">Højreklik, og vælg derefter **New Tab Page**.</span><span class="sxs-lookup"><span data-stu-id="31b07-144">Right-click, and then select **New Tab Page**.</span></span>
9. <span data-ttu-id="31b07-145">Giv fanesiden til et nyt, sigende navn, f.eks. **Analyse**.</span><span class="sxs-lookup"><span data-stu-id="31b07-145">Rename the tab page to something meaningful, such as **Analytics**.</span></span>
10. <span data-ttu-id="31b07-146">Vælg **Analytics (Tab Page)** i formulardesigneren.</span><span class="sxs-lookup"><span data-stu-id="31b07-146">In the form designer, select **Analytics (Tab Page)**.</span></span>
11. <span data-ttu-id="31b07-147">Indstil egenskaben **Caption** til **Analytics**, og indstil egenskaben **Auto-opgørelse** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="31b07-147">Set the **Caption** property to **Analytics**, and set the **Auto Declaration** property to **Yes**.</span></span>
12. <span data-ttu-id="31b07-148">Højreklik på kontrolelementet, og vælg derefter **Ny** \> **Gruppe** for at tilføje et nyt formulargruppekontrolelement.</span><span class="sxs-lookup"><span data-stu-id="31b07-148">Right-click the control, and then select **New** \> **Group** to add a new form group control.</span></span>
13. <span data-ttu-id="31b07-149">Giv formulargruppen et nyt, sigende navn, f.eks. **powerBIRapportGruppe**.</span><span class="sxs-lookup"><span data-stu-id="31b07-149">Rename the form group to something meaningful, such as **powerBIReportGroup**.</span></span>
14. <span data-ttu-id="31b07-150">I formulardesigneren skal du vælge **PanoramaBody (Tab)** og derefter trække kontrolelementet til fanen **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="31b07-150">In the form designer, select **PanoramaBody (Tab)**, and then drag the control onto the **Workspace** tab.</span></span>
15. <span data-ttu-id="31b07-151">Vælg det øverste element **Design | Pattern: Workspace Operational** i designdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="31b07-151">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
16. <span data-ttu-id="31b07-152">Højreklik, og vælg derefter **Remove pattern**.</span><span class="sxs-lookup"><span data-stu-id="31b07-152">Right-click, and then select **Remove pattern**.</span></span>
17. <span data-ttu-id="31b07-153">Højreklik igen, og vælg derefter **Tilføj mønster** \> **Faneopdelt arbejdsområde**.</span><span class="sxs-lookup"><span data-stu-id="31b07-153">Right-click again, and then select **Add pattern** \> **Workspace Tabbed**.</span></span>
18. <span data-ttu-id="31b07-154">Opret et build for at bekræfte ændringerne.</span><span class="sxs-lookup"><span data-stu-id="31b07-154">Perform a build to verify your changes.</span></span>

<span data-ttu-id="31b07-155">I følgende illustration vises designet, når disse ændringer er anvendt.</span><span class="sxs-lookup"><span data-stu-id="31b07-155">The following illustration shows what the design looks like after these changes are applied.</span></span>

![FMClerkWorkspace efter ændringer](media/analytical-workspace-definition-after.png)

<span data-ttu-id="31b07-157">Nu, hvor du har tilføjet de kontrolelementer til formularen, der skal bruges til at integrere arbejdsområderapporten, skal du definere størrelsen på det overordnede kontrolelement, så det kan rumme layoutet.</span><span class="sxs-lookup"><span data-stu-id="31b07-157">Now that you've added the form controls that will be used to embed the workspace report, you must define the size of the parent control so that it accommodates the layout.</span></span> <span data-ttu-id="31b07-158">Som standard er både siden **Filterrude** og siden **Fane** synlige i rapporten.</span><span class="sxs-lookup"><span data-stu-id="31b07-158">By default, both the **Filters Pane** page and the **Tab** page will be visible on the report.</span></span> <span data-ttu-id="31b07-159">Du kan dog ændre synligheden af disse kontrolelementer alt efter rapportens målforbruger.</span><span class="sxs-lookup"><span data-stu-id="31b07-159">However, you can change the visibility of these controls as appropriate for the target consumer of the report.</span></span>

> [!NOTE]
> <span data-ttu-id="31b07-160">Til integrerede arbejdsområder anbefaler vi, at du bruger udvidelser for at skjule både siden **Filterrude** og siden **Fane** med henblik på konsistens.</span><span class="sxs-lookup"><span data-stu-id="31b07-160">For embedded workspaces, we recommend that you use extensions to hide both the **Filters Pane** and **Tab** pages, for consistency.</span></span>

<span data-ttu-id="31b07-161">Du har nu fuldført udvidelsen af programformulardefinitionen.</span><span class="sxs-lookup"><span data-stu-id="31b07-161">You've now completed the task of extending the application form definition.</span></span> <span data-ttu-id="31b07-162">Du kan finde flere oplysninger om, hvordan du bruger udvidelser til at foretage tilpasninger, i [Tilpasning via udvidelse og overlejring](../extensibility/customization-overlayering-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="31b07-162">For more information about how to use extensions to do customizations, see [Customize through extension and overlayering](../extensibility/customization-overlayering-extensions.md).</span></span>

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a><span data-ttu-id="31b07-163">Tilføje X ++-forretningslogik for at integrere et fremviserkontrolelement</span><span class="sxs-lookup"><span data-stu-id="31b07-163">Add X++ business logic to embed a viewer control</span></span>
<span data-ttu-id="31b07-164">Følg disse trin for at tilføje forretningslogik, der initialiserer det kontrolelement til rapportfremvisningen, der er integreret i arbejdsområdet **Reservationsstyring**.</span><span class="sxs-lookup"><span data-stu-id="31b07-164">Follow these steps to add business logic that initializes the report viewer control that is embedded in the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="31b07-165">Åbn formulardesigneren **FMClerkWorkspace** for at udvide designdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="31b07-165">Open the **FMClerkWorkspace** form designer to extend the design definition.</span></span>
2. <span data-ttu-id="31b07-166">Tryk på F7 for at få adgang til koden bag ved kodedefinitionen.</span><span class="sxs-lookup"><span data-stu-id="31b07-166">Press F7 to access the code behind the code definition.</span></span>
3. <span data-ttu-id="31b07-167">Tilføj følgende X++-kode.</span><span class="sxs-lookup"><span data-stu-id="31b07-167">Add the following X++ code.</span></span>

    ```xpp
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                // initialize the PBI report control using shared helper
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
        }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. <span data-ttu-id="31b07-168">Opret et build for at bekræfte ændringerne.</span><span class="sxs-lookup"><span data-stu-id="31b07-168">Perform a build to verify your changes.</span></span>

<span data-ttu-id="31b07-169">Du har nu fuldført tilføjelsen af forretningslogik for at initialisere det integrerede rapportfremviserkontrolelement.</span><span class="sxs-lookup"><span data-stu-id="31b07-169">You've now completed the task of adding business logic to initialize the embedded report viewer control.</span></span> <span data-ttu-id="31b07-170">I følgende illustration vises arbejdsområdet, når disse ændringer er anvendt.</span><span class="sxs-lookup"><span data-stu-id="31b07-170">The following illustration shows what the workspace looks like after these changes are applied.</span></span>

![Rapport, der er integreret i arbejdsområdet](media/analytical-workspace-final.png)

> [!NOTE]
> <span data-ttu-id="31b07-172">Du kan åbne den eksisterende operationsvisning ved hjælp af fanerne i arbejdsområde under sidetitlen.</span><span class="sxs-lookup"><span data-stu-id="31b07-172">You can access the existing operational view by using the workspace tabs below the page title.</span></span>

## <a name="reference"></a><span data-ttu-id="31b07-173">Reference</span><span class="sxs-lookup"><span data-stu-id="31b07-173">Reference</span></span>

### <a name="pbireporthelperinitializereportcontrol-method"></a><span data-ttu-id="31b07-174">PBIReportHelper.initializeReportControl-metode</span><span class="sxs-lookup"><span data-stu-id="31b07-174">PBIReportHelper.initializeReportControl method</span></span>
<span data-ttu-id="31b07-175">Dette afsnit indeholder oplysninger om den hjælpeklasse, der bruges til at integrere en Power BI-rapport (.pbix-ressource) i et kontrolelement i formulargruppen.</span><span class="sxs-lookup"><span data-stu-id="31b07-175">This section provides information about the helper class that is used to embed a Power BI report (.pbix resource) in a form group control.</span></span>

#### <a name="syntax"></a><span data-ttu-id="31b07-176">Syntaks</span><span class="sxs-lookup"><span data-stu-id="31b07-176">Syntax</span></span>
```xpp
public static void initializeReportControl(
    str                 _resourceName,
    FormGroupControl    _formGroupControl,
    str                 _defaultPageName = '',
    boolean             _showFilterPane = false,
    boolean             _showNavPane = false,
    List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a><span data-ttu-id="31b07-177">Parametre</span><span class="sxs-lookup"><span data-stu-id="31b07-177">Parameters</span></span>

| <span data-ttu-id="31b07-178">Navn</span><span class="sxs-lookup"><span data-stu-id="31b07-178">Name</span></span>             | <span data-ttu-id="31b07-179">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="31b07-179">Description</span></span>                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31b07-180">resourceName</span><span class="sxs-lookup"><span data-stu-id="31b07-180">resourceName</span></span>     | <span data-ttu-id="31b07-181">Navnet på .pbix ressourcen.</span><span class="sxs-lookup"><span data-stu-id="31b07-181">The name of the .pbix resource.</span></span>                                                                              |
| <span data-ttu-id="31b07-182">formGroupControl</span><span class="sxs-lookup"><span data-stu-id="31b07-182">formGroupControl</span></span> | <span data-ttu-id="31b07-183">Kontrolelementet til formulargruppen, som Power BI-rapportkontrolelementet skal anvendes på.</span><span class="sxs-lookup"><span data-stu-id="31b07-183">The form group control to apply the Power BI report control to.</span></span>                                              |
| <span data-ttu-id="31b07-184">defaultPageName</span><span class="sxs-lookup"><span data-stu-id="31b07-184">defaultPageName</span></span>  | <span data-ttu-id="31b07-185">Standardsidenavnet.</span><span class="sxs-lookup"><span data-stu-id="31b07-185">The default page name.</span></span>                                                                                       |
| <span data-ttu-id="31b07-186">showFilterPane</span><span class="sxs-lookup"><span data-stu-id="31b07-186">showFilterPane</span></span>   | <span data-ttu-id="31b07-187">En boolesk værdi, der angiver, om filterruden skal vises (**true**) eller skjules (**false**).</span><span class="sxs-lookup"><span data-stu-id="31b07-187">A Boolean value that indicates whether the filter pane should be shown (**true**) or hidden (**false**).</span></span>     |
| <span data-ttu-id="31b07-188">showNavPane</span><span class="sxs-lookup"><span data-stu-id="31b07-188">showNavPane</span></span>      | <span data-ttu-id="31b07-189">En boolesk værdi, der angiver, om navigationsruden skal vises (**true**) eller skjules (**false**).</span><span class="sxs-lookup"><span data-stu-id="31b07-189">A Boolean value that indicates whether the navigation pane should be shown (**true**) or hidden (**false**).</span></span> |
| <span data-ttu-id="31b07-190">defaultFilters</span><span class="sxs-lookup"><span data-stu-id="31b07-190">defaultFilters</span></span>   | <span data-ttu-id="31b07-191">Standardfiltrene for Power BI-rapporten.</span><span class="sxs-lookup"><span data-stu-id="31b07-191">The default filters for the Power BI report.</span></span>                                                                 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]