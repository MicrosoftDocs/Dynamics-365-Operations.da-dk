---
title: Undgå afkortning af teksten i stillingshierarkiet og eksportere til Visio
description: I dette emne beskrives, hvordan du kan løse et problem, hvor navnene på personer og stillinger afkortes, når kunder får vist stillingshierarkiet i Microsoft Dynamics 365 for Talent. Afkortning af tekst kan gøre det svært at tage et skærmbillede eller udskrive hierarkiet.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 87d1c1994b14fac45fa305a9223ed45ee363a70c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517582"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a><span data-ttu-id="7f60d-104">Undgå afkortning af teksten i stillingshierarkiet og eksportere til Visio</span><span class="sxs-lookup"><span data-stu-id="7f60d-104">Avoid text truncation on the position hierarchy and export to Visio</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7f60d-105">**Afgang**</span><span class="sxs-lookup"><span data-stu-id="7f60d-105">**Issue**</span></span>

<span data-ttu-id="7f60d-106">Når en kunde får vist stillingshierarkiet i Microsoft Dynamics 365 for Talent, afkortes navnene på personer og stillinger.</span><span class="sxs-lookup"><span data-stu-id="7f60d-106">When a customer views the position hierarchy in Microsoft Dynamics 365 for Talent, the names of individuals and positions are truncated.</span></span> <span data-ttu-id="7f60d-107">Derfor kan det være svært at tage et skærmbillede eller udskrive og distribuere hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="7f60d-107">Therefore, it can be difficult to take a screenshot, or to print and distribute the hierarchy.</span></span>

![Stillingshierarki](media/position-h.png)

<span data-ttu-id="7f60d-109">**Årsag**</span><span class="sxs-lookup"><span data-stu-id="7f60d-109">**Cause**</span></span>

<span data-ttu-id="7f60d-110">Denne funktionsmåde er tilsigtet.</span><span class="sxs-lookup"><span data-stu-id="7f60d-110">This behavior is by design.</span></span>

<span data-ttu-id="7f60d-111">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="7f60d-111">**Resolution**</span></span>

<span data-ttu-id="7f60d-112">Desværre kan brugere ikke nemt ændre størrelsen af teksten.</span><span class="sxs-lookup"><span data-stu-id="7f60d-112">Unfortunately, users can't easily change the size of the text.</span></span> <span data-ttu-id="7f60d-113">Du kan dog eksportere stillingshierarkiet fra Talent og derefter importere det til Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="7f60d-113">However, you can export the position hierarchy out of Talent and then import it into Microsoft Visio.</span></span> <span data-ttu-id="7f60d-114">Selvom følgende artikel er skrevet til Microsoft Dynamics AX 2012, gælder processen stadig for Talent: [Eksportere et stillingshierarki til Microsoft Visio](https://docs.microsoft.com/en-us/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span><span class="sxs-lookup"><span data-stu-id="7f60d-114">Although the following article was written for Microsoft Dynamics AX 2012, the process still applies to Talent: [Export a position hierarchy to Microsoft Visio](https://docs.microsoft.com/en-us/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span></span>

<span data-ttu-id="7f60d-115">Følg disse trin for at eksportere til Visio.</span><span class="sxs-lookup"><span data-stu-id="7f60d-115">Follow these steps to export to Visio.</span></span>

1. <span data-ttu-id="7f60d-116">Åbn listesiden **Stillinger** i Talent.</span><span class="sxs-lookup"><span data-stu-id="7f60d-116">In Talent, open the **Positions** list page.</span></span>

    <span data-ttu-id="7f60d-117">Hvis du vil medtage flere oplysninger i organisationsstrukturdiagrammet, skal du tilføje felter på listen **Stillinger**, så de er tilgængelige, når du bruger guiden senere i denne procedure.</span><span class="sxs-lookup"><span data-stu-id="7f60d-117">To include more information in the organization structure diagram, add fields to the **Positions** list, so that they are available when you use the wizard later in this procedure.</span></span>

2. <span data-ttu-id="7f60d-118">I handlingsruden skal du vælge knappen **Åbn i Microsoft Office**, og derefter skal du under **Eksportér til Excel** vælge **Stillinger**.</span><span class="sxs-lookup"><span data-stu-id="7f60d-118">On the Action Pane, select the **Open in Microsoft Office** button, and then, under **Export to Excel**, select **Positions**.</span></span> <span data-ttu-id="7f60d-119">Du kan også trykke på Ctrl + T.</span><span class="sxs-lookup"><span data-stu-id="7f60d-119">Alternatively, press Ctrl+T.</span></span>

    ![Eksportere listesiden Stillinger til Microsoft Excel](media/org-admin.png)

3. <span data-ttu-id="7f60d-121">Gem Excel-filen, der eksporteres.</span><span class="sxs-lookup"><span data-stu-id="7f60d-121">Save the Excel file that is exported.</span></span>

    ![Dialogboksen Eksportér til Excel](media/export-excel.png)

4. <span data-ttu-id="7f60d-123">I Visio skal du vælge **Visio - Opret ny** og vælge skabelonkategorien **Forretning**.</span><span class="sxs-lookup"><span data-stu-id="7f60d-123">In Visio, select **Visio - Create New**, and select the **Business** template category.</span></span>

    ![Nyt diagram](media/new.png)

5. <span data-ttu-id="7f60d-125">Vælg **Guiden Organisationsdiagram**, og vælg derefter **Opret**.</span><span class="sxs-lookup"><span data-stu-id="7f60d-125">Select **Organization Chart Wizard**, and then select **Create**.</span></span>

    ![Dialogboksen Guiden Organisationsdiagram](media/orgchart-wizard.png)

6. <span data-ttu-id="7f60d-127">Vælg **Oplysninger, der allerede er gemt i en fil eller database**, og vælg derefter **Næste**.</span><span class="sxs-lookup"><span data-stu-id="7f60d-127">Select **Information that's already stored in a file or database**, and then select **Next**.</span></span>

    ![Guiden Organisationsdiagram 1](media/orgchart-wizard7.png)

7. <span data-ttu-id="7f60d-129">Vælg **En tekstfil, Org Plus (\*.txt) eller en Excel-fil**, og vælg derefter **Næste**.</span><span class="sxs-lookup"><span data-stu-id="7f60d-129">Choose **A text, Org Plus (\*.txt), or Excel file**, and then select **Next**.</span></span>

    ![Guiden Organisationsdiagram 2](media/orgchart-wizard3.png)

8. <span data-ttu-id="7f60d-131">Gennemse for at vælge den eksporterede Excel-fil, der indeholder stillingshierarkiet, og vælg derefter **Næste**.</span><span class="sxs-lookup"><span data-stu-id="7f60d-131">Browse to select the exported Excel file that contains the position hierarchy, and then select **Next**.</span></span>

    ![Guiden Organisationsdiagram 3](media/orgchart-wizard2.png)

9. <span data-ttu-id="7f60d-133">Indstil feltet **Navn** til **Stilling**, indstil feltet **Rapportér til** til **Rapporterer til stilling**, og vælg derefter **Næste**.</span><span class="sxs-lookup"><span data-stu-id="7f60d-133">Set the **Name** field to **Position**, set the **Reports to** field to **Reports to position**, and then select **Next**.</span></span>

    ![Guiden Organisationsdiagram 4](media/orgchart-wizard1.png)

10. <span data-ttu-id="7f60d-135">Vælg de felter, der skal vises på hver node, og vælg derefter **Næste**.</span><span class="sxs-lookup"><span data-stu-id="7f60d-135">Select the fields that should be shown on each node, and then select **Next**.</span></span>

    ![Guiden Organisationsdiagram 5](media/orgchart-wizard5.png)

11. <span data-ttu-id="7f60d-137">Føj kolonnen **Stilling** til listen **Figurdatafelter**, og vælg derefter **Næste**.</span><span class="sxs-lookup"><span data-stu-id="7f60d-137">Add the **Position** column to the **Shape Data fields** list, and then select **Next**.</span></span>

    ![Guiden Organisationsdiagram 6](media/orgchart-wizard6.png)

12. <span data-ttu-id="7f60d-139">Der er ingen tilgængelige billeder i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="7f60d-139">Pictures aren't currently available.</span></span> <span data-ttu-id="7f60d-140">Vælg derfor **Næste** på den næste side.</span><span class="sxs-lookup"><span data-stu-id="7f60d-140">Therefore, on the next page, select **Next**.</span></span>
13. <span data-ttu-id="7f60d-141">Vælg **Guiden skal automatisk opdele organisationsdiagrammet på tværs af sider**.</span><span class="sxs-lookup"><span data-stu-id="7f60d-141">Select **I want the wizard to automatically break my organization chart across pages**.</span></span>

    ![Guiden Organisationsdiagram 7](media/orgchart-wizard4.png)

14. <span data-ttu-id="7f60d-143">Vælg **Udfør**.</span><span class="sxs-lookup"><span data-stu-id="7f60d-143">Select **Finish**.</span></span>

    <span data-ttu-id="7f60d-144">Hvis der eventuelt er stillinger, der ikke findes i strukturen, bliver du bedt om at medtage dem i diagrammet.</span><span class="sxs-lookup"><span data-stu-id="7f60d-144">If there are any positions that aren't in the structure, you're asked to include them in the diagram.</span></span>

<span data-ttu-id="7f60d-145">Det diagram, der er oprettet i Visio, viser hver enkelt leder i et separat regneark.</span><span class="sxs-lookup"><span data-stu-id="7f60d-145">The diagram that is generated in Visio shows each manager on a separate worksheet.</span></span>

<span data-ttu-id="7f60d-146">Baseret på de felter, du har valgt at medtage i diagrammet, viser hver node de relevante oplysninger, når Visio-filen genereres.</span><span class="sxs-lookup"><span data-stu-id="7f60d-146">Based on the fields that you selected to include in the diagram, each node shows the appropriate information when the Visio file is generated.</span></span>

![Hierarkidiagram](media/hierarchy.png)

<span data-ttu-id="7f60d-148">**Flere indstillinger**</span><span class="sxs-lookup"><span data-stu-id="7f60d-148">**Additional option**</span></span>

<span data-ttu-id="7f60d-149">I Talent kan du muligvis også bruge arbejdsområdet **Personer** til at få vist visse oplysninger i forbindelse med hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="7f60d-149">In Talent, you might also be able to use the **People** workspace to view some hierarchy-related information.</span></span>
