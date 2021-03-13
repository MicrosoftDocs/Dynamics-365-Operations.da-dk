---
title: Undgå tekstafkortning i stillingshierarkiet, og eksportér til Visio
description: I denne artikel beskrives det, hvordan du kan løse et problem, hvor navnene på personer og stillinger afkortes, når kunder får vist stillingshierarkiet i Microsoft Dynamics 365 Human Resources. Afkortning af tekst kan gøre det svært at tage et skærmbillede eller udskrive hierarkiet.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0dc91d3165f14c165f75756dc63a3dc8f63149aa
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111918"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a><span data-ttu-id="38fe8-104">Undgå afkortning af teksten i stillingshierarkiet og eksportere til Visio</span><span class="sxs-lookup"><span data-stu-id="38fe8-104">Avoid text truncation on the position hierarchy and export to Visio</span></span>

<span data-ttu-id="38fe8-105">**Afgang**</span><span class="sxs-lookup"><span data-stu-id="38fe8-105">**Issue**</span></span>

<span data-ttu-id="38fe8-106">Når en kunde får vist stillingshierarkiet i Microsoft Dynamics 365 Human Resources, afkortes navnene på personer og stillinger.</span><span class="sxs-lookup"><span data-stu-id="38fe8-106">When a customer views the position hierarchy in Microsoft Dynamics 365 Human Resources, the names of individuals and positions are truncated.</span></span> <span data-ttu-id="38fe8-107">Derfor kan det være svært at tage et skærmbillede eller udskrive og distribuere hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="38fe8-107">Therefore, it can be difficult to take a screenshot, or to print and distribute the hierarchy.</span></span>

![Stillingshierarki](media/position-h.png)

<span data-ttu-id="38fe8-109">**Årsag**</span><span class="sxs-lookup"><span data-stu-id="38fe8-109">**Cause**</span></span>

<span data-ttu-id="38fe8-110">Denne funktionsmåde er tilsigtet.</span><span class="sxs-lookup"><span data-stu-id="38fe8-110">This behavior is by design.</span></span>

<span data-ttu-id="38fe8-111">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="38fe8-111">**Resolution**</span></span>

<span data-ttu-id="38fe8-112">Desværre kan brugere ikke nemt ændre størrelsen af teksten.</span><span class="sxs-lookup"><span data-stu-id="38fe8-112">Unfortunately, users can't easily change the size of the text.</span></span> <span data-ttu-id="38fe8-113">Du kan dog eksportere stillingshierarkiet fra Human Resources og derefter importere det til Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="38fe8-113">However, you can export the position hierarchy out of Human Resources and then import it into Microsoft Visio.</span></span> <span data-ttu-id="38fe8-114">Selvom følgende artikel er skrevet til Microsoft Dynamics AX 2012, gælder processen stadig for Human Resources: [Eksportere et stillingshierarki til Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span><span class="sxs-lookup"><span data-stu-id="38fe8-114">Although the following article was written for Microsoft Dynamics AX 2012, the process still applies to Human Resources: [Export a position hierarchy to Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span></span>

<span data-ttu-id="38fe8-115">Følg disse trin for at eksportere til Visio.</span><span class="sxs-lookup"><span data-stu-id="38fe8-115">Follow these steps to export to Visio.</span></span>

1. <span data-ttu-id="38fe8-116">Åbn listesiden **Stillinger** i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="38fe8-116">In Human Resources, open the **Positions** list page.</span></span>

    <span data-ttu-id="38fe8-117">Hvis du vil medtage flere oplysninger i organisationsstrukturdiagrammet, skal du tilføje felter på listen **Stillinger**, så de er tilgængelige, når du bruger guiden senere i denne procedure.</span><span class="sxs-lookup"><span data-stu-id="38fe8-117">To include more information in the organization structure diagram, add fields to the **Positions** list, so that they are available when you use the wizard later in this procedure.</span></span>

2. <span data-ttu-id="38fe8-118">I handlingsruden skal du vælge knappen **Åbn i Microsoft Office**, og derefter skal du under **Eksportér til Excel** vælge **Stillinger**.</span><span class="sxs-lookup"><span data-stu-id="38fe8-118">On the Action Pane, select the **Open in Microsoft Office** button, and then, under **Export to Excel**, select **Positions**.</span></span> <span data-ttu-id="38fe8-119">Du kan også trykke på Ctrl + T.</span><span class="sxs-lookup"><span data-stu-id="38fe8-119">Alternatively, press Ctrl+T.</span></span>

    ![Eksportere listesiden Stillinger til Excel](media/org-admin.png)

3. <span data-ttu-id="38fe8-121">Gem Excel-filen, der eksporteres.</span><span class="sxs-lookup"><span data-stu-id="38fe8-121">Save the Excel file that is exported.</span></span>

    ![Dialogboksen Eksportér til Excel](media/export-excel.png)

4. <span data-ttu-id="38fe8-123">I Visio skal du vælge **Visio - Opret ny** og vælge skabelonkategorien **Forretning**.</span><span class="sxs-lookup"><span data-stu-id="38fe8-123">In Visio, select **Visio - Create New**, and select the **Business** template category.</span></span>

    ![Nyt diagram](media/new.png)

5. <span data-ttu-id="38fe8-125">Vælg **Guiden Organisationsdiagram**, og vælg derefter **Opret**.</span><span class="sxs-lookup"><span data-stu-id="38fe8-125">Select **Organization Chart Wizard**, and then select **Create**.</span></span>

    ![Dialogboksen Guiden Organisationsdiagram](media/orgchart-wizard.png)

6. <span data-ttu-id="38fe8-127">Vælg **Oplysninger, der allerede er gemt i en fil eller database**, og vælg derefter **Næste**.</span><span class="sxs-lookup"><span data-stu-id="38fe8-127">Select **Information that's already stored in a file or database**, and then select **Next**.</span></span>

    ![Guiden Organisationsdiagram 1](media/orgchart-wizard7.png)

7. <span data-ttu-id="38fe8-129">Vælg **En tekstfil, Org Plus (\*.txt) eller en Excel-fil**, og vælg derefter **Næste**.</span><span class="sxs-lookup"><span data-stu-id="38fe8-129">Choose **A text, Org Plus (\*.txt), or Excel file**, and then select **Next**.</span></span>

    ![Guiden Organisationsdiagram 2](media/orgchart-wizard3.png)

8. <span data-ttu-id="38fe8-131">Gennemse for at vælge den eksporterede Excel-fil, der indeholder stillingshierarkiet, og vælg derefter **Næste**.</span><span class="sxs-lookup"><span data-stu-id="38fe8-131">Browse to select the exported Excel file that contains the position hierarchy, and then select **Next**.</span></span>

    ![Guiden Organisationsdiagram 3](media/orgchart-wizard2.png)

9. <span data-ttu-id="38fe8-133">Indstil feltet **Navn** til **Stilling**, indstil feltet **Rapportér til** til **Rapporterer til stilling**, og vælg derefter **Næste**.</span><span class="sxs-lookup"><span data-stu-id="38fe8-133">Set the **Name** field to **Position**, set the **Reports to** field to **Reports to position**, and then select **Next**.</span></span>

    ![Guiden Organisationsdiagram 4](media/orgchart-wizard1.png)

10. <span data-ttu-id="38fe8-135">Vælg de felter, der skal vises på hver node, og vælg derefter **Næste**.</span><span class="sxs-lookup"><span data-stu-id="38fe8-135">Select the fields that should be shown on each node, and then select **Next**.</span></span>

    ![Guiden Organisationsdiagram 5](media/orgchart-wizard5.png)

11. <span data-ttu-id="38fe8-137">Føj kolonnen **Stilling** til listen **Figurdatafelter**, og vælg derefter **Næste**.</span><span class="sxs-lookup"><span data-stu-id="38fe8-137">Add the **Position** column to the **Shape Data fields** list, and then select **Next**.</span></span>

    ![Guiden Organisationsdiagram 6](media/orgchart-wizard6.png)

12. <span data-ttu-id="38fe8-139">Der er ingen tilgængelige billeder i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="38fe8-139">Pictures aren't currently available.</span></span> <span data-ttu-id="38fe8-140">Vælg derfor **Næste** på den næste side.</span><span class="sxs-lookup"><span data-stu-id="38fe8-140">Therefore, on the next page, select **Next**.</span></span>
13. <span data-ttu-id="38fe8-141">Vælg **Guiden skal automatisk opdele organisationsdiagrammet på tværs af sider**.</span><span class="sxs-lookup"><span data-stu-id="38fe8-141">Select **I want the wizard to automatically break my organization chart across pages**.</span></span>

    ![Guiden Organisationsdiagram 7](media/orgchart-wizard4.png)

14. <span data-ttu-id="38fe8-143">Vælg **Udfør**.</span><span class="sxs-lookup"><span data-stu-id="38fe8-143">Select **Finish**.</span></span>

    <span data-ttu-id="38fe8-144">Hvis der eventuelt er stillinger, der ikke findes i strukturen, bliver du bedt om at medtage dem i diagrammet.</span><span class="sxs-lookup"><span data-stu-id="38fe8-144">If there are any positions that aren't in the structure, you're asked to include them in the diagram.</span></span>

<span data-ttu-id="38fe8-145">Det diagram, der er oprettet i Visio, viser hver enkelt leder i et separat regneark.</span><span class="sxs-lookup"><span data-stu-id="38fe8-145">The diagram that is generated in Visio shows each manager on a separate worksheet.</span></span>

<span data-ttu-id="38fe8-146">Baseret på de felter, du har valgt at medtage i diagrammet, viser hver node de relevante oplysninger, når Visio-filen genereres.</span><span class="sxs-lookup"><span data-stu-id="38fe8-146">Based on the fields that you selected to include in the diagram, each node shows the appropriate information when the Visio file is generated.</span></span>

![Hierarkidiagram](media/hierarchy.png)

<span data-ttu-id="38fe8-148">**Flere indstillinger**</span><span class="sxs-lookup"><span data-stu-id="38fe8-148">**Additional option**</span></span>

<span data-ttu-id="38fe8-149">I Human Resources kan du muligvis også bruge arbejdsområdet **Personer** til at få vist visse oplysninger i forbindelse med hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="38fe8-149">In Human Resources, you might also be able to use the **People** workspace to view some hierarchy-related information.</span></span>
