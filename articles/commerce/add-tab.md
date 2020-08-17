---
title: Fanemodul
description: Dette emne omhandler fanemoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: b4187dfd704c78d506d7840b04c986687fe807a3
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621007"
---
# <a name="tab-module"></a><span data-ttu-id="a23e9-103">Fanemodul</span><span class="sxs-lookup"><span data-stu-id="a23e9-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a23e9-104">Dette emne omhandler fanemoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a23e9-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a23e9-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="a23e9-105">Overview</span></span>

<span data-ttu-id="a23e9-106">Fanemoduler er containeragtige moduler, som bruges til at organisere oplysningerne på en webstedsside på faner.</span><span class="sxs-lookup"><span data-stu-id="a23e9-106">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="a23e9-107">De kan bruges på alle sider, hvor oplysninger skal vises under faner.</span><span class="sxs-lookup"><span data-stu-id="a23e9-107">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="a23e9-108">Inde i hvert fanemodul kan et eller flere faneelementmoduler tilføjes.</span><span class="sxs-lookup"><span data-stu-id="a23e9-108">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="a23e9-109">De enkelte faneelementmoduler repræsenterer en enkelt fane. I hvert faneelementmodul kan et eller flere moduler tilføjes.</span><span class="sxs-lookup"><span data-stu-id="a23e9-109">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="a23e9-110">Der er ingen begrænsninger for de typer moduler, der kan føjes til et faneelementmodul.</span><span class="sxs-lookup"><span data-stu-id="a23e9-110">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="a23e9-111">Det følgende billede viser et eksempel på et fanemodul på en webstedside.</span><span class="sxs-lookup"><span data-stu-id="a23e9-111">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="a23e9-112">I dette eksempel er fanen **Levering** valgt.</span><span class="sxs-lookup"><span data-stu-id="a23e9-112">In this example, the **Shipping** tab selected.</span></span>

![Eksempel på et fanemodul](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="a23e9-114">Fanemodulegenskaber</span><span class="sxs-lookup"><span data-stu-id="a23e9-114">Tab module properties</span></span>

| <span data-ttu-id="a23e9-115">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="a23e9-115">Property name</span></span> | <span data-ttu-id="a23e9-116">Værdier</span><span class="sxs-lookup"><span data-stu-id="a23e9-116">Values</span></span> | <span data-ttu-id="a23e9-117">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="a23e9-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="a23e9-118">Overskrift</span><span class="sxs-lookup"><span data-stu-id="a23e9-118">Heading</span></span> | <span data-ttu-id="a23e9-119">Tekst</span><span class="sxs-lookup"><span data-stu-id="a23e9-119">Text</span></span> | <span data-ttu-id="a23e9-120">Denne egenskab specificerer en valgfri tekstoverskrift i fanemodulet.</span><span class="sxs-lookup"><span data-stu-id="a23e9-120">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="a23e9-121">Aktiv fane-indeks</span><span class="sxs-lookup"><span data-stu-id="a23e9-121">Active Tab Index</span></span> | <span data-ttu-id="a23e9-122">Tal</span><span class="sxs-lookup"><span data-stu-id="a23e9-122">Number</span></span> | <span data-ttu-id="a23e9-123">Denne egenskab specificerer den fane, der skal være aktiv som standard, når en side indlæses.</span><span class="sxs-lookup"><span data-stu-id="a23e9-123">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="a23e9-124">Hvis der ikke angives en værdi, er det første faneelement som standard aktivt.</span><span class="sxs-lookup"><span data-stu-id="a23e9-124">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="a23e9-125">Faneelementmodulegenskaber</span><span class="sxs-lookup"><span data-stu-id="a23e9-125">Tab item module properties</span></span>

| <span data-ttu-id="a23e9-126">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="a23e9-126">Property name</span></span> | <span data-ttu-id="a23e9-127">Værdier</span><span class="sxs-lookup"><span data-stu-id="a23e9-127">Values</span></span> | <span data-ttu-id="a23e9-128">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="a23e9-128">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="a23e9-129">Stilling</span><span class="sxs-lookup"><span data-stu-id="a23e9-129">Title</span></span> | <span data-ttu-id="a23e9-130">Tekst</span><span class="sxs-lookup"><span data-stu-id="a23e9-130">Text</span></span> | <span data-ttu-id="a23e9-131">Denne egenskab specificerer titelteksten for faneelementmodulet.</span><span class="sxs-lookup"><span data-stu-id="a23e9-131">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="a23e9-132">Føje et fanemodul til en side</span><span class="sxs-lookup"><span data-stu-id="a23e9-132">Add a tab module to a page</span></span>

<span data-ttu-id="a23e9-133">Hvis du vil føje et fanemodul til en side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="a23e9-133">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="a23e9-134">Brug Fabrikam-marketingskabelonen (eller en skabelon uden begrænsninger) til at oprette en ny side, der hedder **Gem side med politikker**.</span><span class="sxs-lookup"><span data-stu-id="a23e9-134">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="a23e9-135">På pladsen **Hoved** på **Standardsiden** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="a23e9-135">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a23e9-136">I dialogboksen **Tilføj modul** skal du vælge modulet **Container** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a23e9-136">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a23e9-137">På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="a23e9-137">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a23e9-138">I dialogboksen **Tilføj modul** skal du vælge modulet **Fane** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a23e9-138">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a23e9-139">Vælg **Overskrift** ud for blyantsymbolet i egenskabsruden for fanemodulet.</span><span class="sxs-lookup"><span data-stu-id="a23e9-139">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="a23e9-140">I dialogboksen **Overskrift** under **Overskrifttekst** skal du angive en overskrifttekst (f.eks. **Politikker**).</span><span class="sxs-lookup"><span data-stu-id="a23e9-140">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="a23e9-141">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a23e9-141">Then select **OK**.</span></span>
1. <span data-ttu-id="a23e9-142">På pladsen **Fane** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="a23e9-142">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a23e9-143">I dialogboksen **Tilføj modul** skal du vælge modulet **Faneelement** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a23e9-143">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a23e9-144">l egenskabsruden for faneelementmodulet under **Titel** skal du angive titelteksten (f.eks. **Levering**).</span><span class="sxs-lookup"><span data-stu-id="a23e9-144">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="a23e9-145">På pladsen **Faneelement** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="a23e9-145">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a23e9-146">I dialogboksen **Tilføj modul** skal du vælge modulet **Tekstblok** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a23e9-146">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a23e9-147">I egenskabsruden for tekstblokmodulet under **RTF-tekst** skal du angive et tekstafsnit.</span><span class="sxs-lookup"><span data-stu-id="a23e9-147">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="a23e9-148">På pladsen **Fane** skal du tilføje flere faneelementmoduler, der har titler.</span><span class="sxs-lookup"><span data-stu-id="a23e9-148">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="a23e9-149">Tilføj et tekstblokmodul med indhold i hvert faneelementmodul.</span><span class="sxs-lookup"><span data-stu-id="a23e9-149">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="a23e9-150">Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.</span><span class="sxs-lookup"><span data-stu-id="a23e9-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="a23e9-151">På siden vises et fanemodul, der indeholder faneelementmoduler med det indhold, du har tilføjet.</span><span class="sxs-lookup"><span data-stu-id="a23e9-151">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="a23e9-152">Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="a23e9-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a23e9-153">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a23e9-153">Additional resources</span></span>

[<span data-ttu-id="a23e9-154">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="a23e9-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a23e9-155">Container-modul</span><span class="sxs-lookup"><span data-stu-id="a23e9-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="a23e9-156">Harmonikamodul</span><span class="sxs-lookup"><span data-stu-id="a23e9-156">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="a23e9-157">Tekstblokmodul</span><span class="sxs-lookup"><span data-stu-id="a23e9-157">Text block module</span></span>](add-content-rich-block.md)
