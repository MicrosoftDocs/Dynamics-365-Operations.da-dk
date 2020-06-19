---
title: Harmonikamodul
description: Dette emne omhandler harmonikamoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e06a0e0289e8c0c718aff4beab2c7a6ceb0a8cb1
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417248"
---
# <a name="accordion-module"></a><span data-ttu-id="74760-103">Harmonikamodul</span><span class="sxs-lookup"><span data-stu-id="74760-103">Accordion module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="74760-104">Dette emne omhandler harmonikamoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="74760-104">This topic covers accordion modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="74760-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="74760-105">Overview</span></span>

<span data-ttu-id="74760-106">Harmonikamoduler er containerlignende moduler, der bruges til at organisere oplysningerne eller modulerne på en side ved hjælp af en skuffeagtig funktion, der kan skjules.</span><span class="sxs-lookup"><span data-stu-id="74760-106">Accordion modules are container-like modules that are used to organize the information or modules on a page by providing a collapsible drawer-like capability.</span></span> <span data-ttu-id="74760-107">Et harmonikamodul kan bruges på alle sider.</span><span class="sxs-lookup"><span data-stu-id="74760-107">An accordion module can be used on any page.</span></span>

<span data-ttu-id="74760-108">Inde i hvert harmonikamodul kan et eller flere harmonikaelementmoduler tilføjes.</span><span class="sxs-lookup"><span data-stu-id="74760-108">Inside every accordion module, one or more accordion item modules can be added.</span></span> <span data-ttu-id="74760-109">Hvert enkelt harmonikaelementmodul repræsenterer en skuffe, der kan skjules.</span><span class="sxs-lookup"><span data-stu-id="74760-109">Each accordion item module represents a collapsible drawer.</span></span> <span data-ttu-id="74760-110">Inde i hvert harmonikaelementmodul kan et eller flere moduler tilføjes.</span><span class="sxs-lookup"><span data-stu-id="74760-110">Inside every accordion item module, one or more modules can be added.</span></span> <span data-ttu-id="74760-111">Der er ingen begrænsninger for de typer moduler, der kan føjes til et harmonikaelementmodul.</span><span class="sxs-lookup"><span data-stu-id="74760-111">There are no restrictions on the types of modules that can be added to an accordion item module.</span></span>

<span data-ttu-id="74760-112">Følgende billede viser et eksempel på et harmonikamodul, der bruges til at organisere oplysninger på en butiks side med ofte stillede spørgsmål (FAQ).</span><span class="sxs-lookup"><span data-stu-id="74760-112">The following image shows an example of an accordion module that is used to organize information on a store's frequently asked questions (FAQ) page.</span></span>

![Eksempel på et harmonikamodul](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a><span data-ttu-id="74760-114">Harmonikamodulegenskaber</span><span class="sxs-lookup"><span data-stu-id="74760-114">Accordion module properties</span></span>

| <span data-ttu-id="74760-115">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="74760-115">Property name</span></span> | <span data-ttu-id="74760-116">Værdier</span><span class="sxs-lookup"><span data-stu-id="74760-116">Values</span></span> | <span data-ttu-id="74760-117">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="74760-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="74760-118">Overskrift</span><span class="sxs-lookup"><span data-stu-id="74760-118">Heading</span></span> | <span data-ttu-id="74760-119">Tekst</span><span class="sxs-lookup"><span data-stu-id="74760-119">Text</span></span> | <span data-ttu-id="74760-120">Denne egenskab specificerer en valgfri tekstoverskrift i harmonikamodulet.</span><span class="sxs-lookup"><span data-stu-id="74760-120">This property specifies an optional text heading for the accordion module.</span></span> |
| <span data-ttu-id="74760-121">Udvid alle</span><span class="sxs-lookup"><span data-stu-id="74760-121">Expand All</span></span> | <span data-ttu-id="74760-122">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="74760-122">**True** or **False**</span></span> | <span data-ttu-id="74760-123">Hvis værdien er angivet til **Sand**, er funktionen Udvid/skjul slået til, så alle elementerne i harmonikamodulet kan udvides og skjules.</span><span class="sxs-lookup"><span data-stu-id="74760-123">If the value is set to **True**, expand/collapse functionality is turned on, so that all items in the accordion module can be expanded and collapsed.</span></span> |
| <span data-ttu-id="74760-124">Interaktionstypografi</span><span class="sxs-lookup"><span data-stu-id="74760-124">Interaction Style</span></span> | <span data-ttu-id="74760-125">**Uafhængig** eller **Udvid kun et element**</span><span class="sxs-lookup"><span data-stu-id="74760-125">**Independent** or **Expand one item only**</span></span> | <span data-ttu-id="74760-126">Denne egenskab definerer interaktionstypografien for harmonikaelementerne.</span><span class="sxs-lookup"><span data-stu-id="74760-126">This property defines the style of interaction for accordion items.</span></span> <span data-ttu-id="74760-127">Hvis værdien er angivet som **Uafhængig**, kan hver enkelt element udvides eller skjules uafhængigt.</span><span class="sxs-lookup"><span data-stu-id="74760-127">If the value is set to **Independent**, each accordion item can be expanded or collapsed independently.</span></span> <span data-ttu-id="74760-128">Hvis værdien er angivet til **Udvid kun et element**, kan kun et element udvides ad gangen.</span><span class="sxs-lookup"><span data-stu-id="74760-128">If the value is set to **Expand one item only**, only one item can be expanded at a time.</span></span> <span data-ttu-id="74760-129">Efterhånden som elementerne udvides, skjules tidligere udvidede elementer.</span><span class="sxs-lookup"><span data-stu-id="74760-129">As items are expanded, previously expanded items are collapsed.</span></span> |

## <a name="accordion-item-module-properties"></a><span data-ttu-id="74760-130">Egenskaber for harmonikaelementmoduler</span><span class="sxs-lookup"><span data-stu-id="74760-130">Accordion item module properties</span></span>

| <span data-ttu-id="74760-131">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="74760-131">Property name</span></span> | <span data-ttu-id="74760-132">Værdier</span><span class="sxs-lookup"><span data-stu-id="74760-132">Values</span></span> | <span data-ttu-id="74760-133">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="74760-133">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="74760-134">Stilling</span><span class="sxs-lookup"><span data-stu-id="74760-134">Title</span></span> | <span data-ttu-id="74760-135">Tekst</span><span class="sxs-lookup"><span data-stu-id="74760-135">Text</span></span> | <span data-ttu-id="74760-136">Denne egenskab specificerer titelteksten for harmonikaelementmodulet.</span><span class="sxs-lookup"><span data-stu-id="74760-136">This property specifies the title text for the accordion item module.</span></span> <span data-ttu-id="74760-137">Når du vælger titelområde, kan brugerne udvide eller skjule sektionen.</span><span class="sxs-lookup"><span data-stu-id="74760-137">By selecting the title region, users can expand or collapse the section.</span></span> |
| <span data-ttu-id="74760-138">Udvid som standard</span><span class="sxs-lookup"><span data-stu-id="74760-138">Expand by default</span></span> | <span data-ttu-id="74760-139">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="74760-139">**True** or **False**</span></span> | <span data-ttu-id="74760-140">Hvis værdien er angivet til **Sand**, udvides harmonikaelementet som standard, når siden indlæses.</span><span class="sxs-lookup"><span data-stu-id="74760-140">If the value is set to **True**, the accordion item is expanded by default when the page is loaded.</span></span> |

## <a name="add-an-accordion-module-to-a-faq-page"></a><span data-ttu-id="74760-141">Føje et harmonikamodul til en FAQ-side</span><span class="sxs-lookup"><span data-stu-id="74760-141">Add an accordion module to a FAQ page</span></span>

<span data-ttu-id="74760-142">Hvis du vil føje et harmonikamodul til en FAQ-side og angive dets egenskaber i webstedsgeneratoren, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="74760-142">To add an accordion module to a FAQ page and set its properties in site builder, follow these steps.</span></span>

1. <span data-ttu-id="74760-143">Gå til **Sider**, og brug Fabrikam-marketingskabelonen (eller en skabelon uden begrænsninger) til at oprette en ny side, der hedder **Gem ofte stillede spørgsmål**.</span><span class="sxs-lookup"><span data-stu-id="74760-143">Go to **Pages**, and use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store FAQ**.</span></span>
1. <span data-ttu-id="74760-144">På pladsen **Hoved** på **Standardsiden** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="74760-144">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="74760-145">I dialogboksen **Tilføj modul** skal du vælge modulet **Container** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="74760-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="74760-146">På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="74760-146">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="74760-147">I dialogboksen **Tilføj modul** skal du vælge modulet **Harmonika** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="74760-147">In the **Add Module** dialog box, select the **Accordion** module, and then select **OK**.</span></span>
1. <span data-ttu-id="74760-148">Vælg **Overskrift** ud for blyantsymbolet i egenskabsruden for harmonikamodulet.</span><span class="sxs-lookup"><span data-stu-id="74760-148">In the property pane of the accordion module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="74760-149">I dialogboksen **Overskrift** under **Overskriftstekst** skal du angive **Ofte stillede spørgsmål**.</span><span class="sxs-lookup"><span data-stu-id="74760-149">In the **Heading** dialog box, under **Heading Text**, enter **Frequently asked questions**.</span></span> <span data-ttu-id="74760-150">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="74760-150">Then select **OK**.</span></span>
1. <span data-ttu-id="74760-151">I egenskabsruden for harmonikamodulet skal du vælge afkrydsningsfeltet **Vis udvid alle** og derefter skal du i feltet **Interaktionstype** vælge **Uafhængig**.</span><span class="sxs-lookup"><span data-stu-id="74760-151">In the property pane of the accordion module, select the **Show expand all** check box, and then, in the **Interaction style** field, select **Independent**.</span></span>
1. <span data-ttu-id="74760-152">På pladsen **Harmonika** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="74760-152">In the **Accordion** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="74760-153">I dialogboksen **Tilføj modul** skal du vælge modulet **Harmonikaelement** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="74760-153">In the **Add Module** dialog box, select the **Accordion item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="74760-154">l egenskabsruden for harmonikaelementmodulet under **Titel** skal du angive titelteksten (f.eks. **Hvordan fungerer returneringer?**).</span><span class="sxs-lookup"><span data-stu-id="74760-154">In the property pane of the accordion item module, under **Title**, enter title text (for example, **How do returns work?**).</span></span>
1. <span data-ttu-id="74760-155">På pladsen **Harmonikaelement** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="74760-155">In the **Accordion item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="74760-156">I dialogboksen **Tilføj modul** skal du vælge modulet **Tekstblok** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="74760-156">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="74760-157">I egenskabsruden i tekstblokmodulet skal du angive et tekstafsnit (f.eks.: **Returneringer skal behandles via callcentret. Kontakt 1-800-FABRIKAM for returneringer. Produkterne har 30 dages returret. Returneringer skal indledes inden for denne tidsramme.**).</span><span class="sxs-lookup"><span data-stu-id="74760-157">In the property pane of the text block module, enter a paragraph of text (for example, **Returns must be processed via the call center. Contact 1-800-FABRIKAM for returns. Products have a 30-day return policy. Returns must be initiated within this time frame.**).</span></span>
1. <span data-ttu-id="74760-158">På pladsen **Harmonika** tilføjes nogle flere harmonikaelementmoduler.</span><span class="sxs-lookup"><span data-stu-id="74760-158">In the **Accordion** slot, add a few more accordion item modules.</span></span> <span data-ttu-id="74760-159">Tilføj et tekstblokmodul med indhold i hvert harmonikaelementmodul.</span><span class="sxs-lookup"><span data-stu-id="74760-159">In each accordion item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="74760-160">Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.</span><span class="sxs-lookup"><span data-stu-id="74760-160">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="74760-161">På siden vises et harmonikamodul med det indhold, du har tilføjet.</span><span class="sxs-lookup"><span data-stu-id="74760-161">The page will show an accordion module that has the content that you added.</span></span>
1. <span data-ttu-id="74760-162">Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="74760-162">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="74760-163">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="74760-163">Additional resources</span></span>

[<span data-ttu-id="74760-164">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="74760-164">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="74760-165">Container-modul</span><span class="sxs-lookup"><span data-stu-id="74760-165">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="74760-166">Fanemodul</span><span class="sxs-lookup"><span data-stu-id="74760-166">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="74760-167">Tekstblokmodul</span><span class="sxs-lookup"><span data-stu-id="74760-167">Text block module</span></span>](add-content-rich-block.md)
