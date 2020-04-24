---
title: Dokumenttilstande og -livscyklus
description: Dette emne omhandler de forskellige dokumenttilstande for sideelementer i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4a00f1c363e5ecb0e3e64637a8f487c48df2df72
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261507"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="7a2cf-103">Dokumenttilstande og -livscyklus</span><span class="sxs-lookup"><span data-stu-id="7a2cf-103">Document states and lifecycle</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7a2cf-104">Dette emne omhandler de forskellige dokumenttilstande for sideelementer i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="7a2cf-105">Beskrivelser af dokumenttilstande</span><span class="sxs-lookup"><span data-stu-id="7a2cf-105">Document state descriptions</span></span>

<span data-ttu-id="7a2cf-106">Emnelisten i [Sideelementer](page-elements-overview.md) indeholder forskellige dokumenttyper i CMS (Content Management System).</span><span class="sxs-lookup"><span data-stu-id="7a2cf-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="7a2cf-107">Disse dokumenttyper kan have flere forskellige tilstande i oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="7a2cf-108">Dokumenttilstandene hjælper med at forhindre datakonflikter og gennemtvinge versionskontrol.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="7a2cf-109">De bestemmer, hvem der kan ændre dokumenterne, hvornår dokumenterne kan ændres, og hvornår ændringer kan ses af andre personer.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="7a2cf-110">I følgende tabel vises de mulige dokumenttilstande for sideelementer i Commerce.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="7a2cf-111">Dokumenttilstand</span><span class="sxs-lookup"><span data-stu-id="7a2cf-111">Document state</span></span>      | <span data-ttu-id="7a2cf-112">Webstedsgeneratorhandling</span><span class="sxs-lookup"><span data-stu-id="7a2cf-112">Site builder action</span></span>        | <span data-ttu-id="7a2cf-113">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="7a2cf-113">Description</span></span>                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="7a2cf-114">Tjekket ud</span><span class="sxs-lookup"><span data-stu-id="7a2cf-114">Checked out</span></span>         | <span data-ttu-id="7a2cf-115">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-115">Select **Edit**.</span></span>           | <span data-ttu-id="7a2cf-116">Det ønskede dokument er tjekket ud til dig.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-116">The applicable document is checked out to you.</span></span> <span data-ttu-id="7a2cf-117">Mens et dokument er i denne tilstand, kan det ikke ændres af andre godkendte systembrugere, og eventuelle ændringer, du foretager i dokumentet, er kun synlige for dig.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-117">While a document is in this state, it can't be changed by other authenticated system users, and any changes that you make to the document are visible only to you.</span></span> |
| <span data-ttu-id="7a2cf-118">Gemt</span><span class="sxs-lookup"><span data-stu-id="7a2cf-118">Saved</span></span>               | <span data-ttu-id="7a2cf-119">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-119">Select **Save**.</span></span>           | <span data-ttu-id="7a2cf-120">Ændringer, der er foretaget i et dokument, der er tjekket ud, gemmes i databasen, men dokumentet er endnu ikke tjekket ind eller udgivet.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-120">Changes that have been made to a checked-out document are saved to the database, but the document isn't yet checked in or published.</span></span> <span data-ttu-id="7a2cf-121">De gemte ændringer er ikke synlige for andre godkendte systembrugere, før forfatteren vælger **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-121">The saved changes aren't visible to other authenticated system users until the author selects **Finish editing**.</span></span> <span data-ttu-id="7a2cf-122">De er ikke synlige for eksterne brugere, før elementet er publiceret.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-122">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="7a2cf-123">Kasseret udcheckning</span><span class="sxs-lookup"><span data-stu-id="7a2cf-123">Discarded check out</span></span> | <span data-ttu-id="7a2cf-124">Vælg **Kassér redigeringer**.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-124">Select **Discard edits**.</span></span>  | <span data-ttu-id="7a2cf-125">Alle ændringer af dokumentet, der er tjekket ud, slettes, og varen vender tilbage til den seneste version, der blev tjekket ind.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-125">All changes to the checked-out document are discarded, and the item reverts to the last version that was checked in.</span></span> |
| <span data-ttu-id="7a2cf-126">Tjekket ind</span><span class="sxs-lookup"><span data-stu-id="7a2cf-126">Checked in</span></span>          | <span data-ttu-id="7a2cf-127">Vælg **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-127">Select **Finish editing**.</span></span> | <span data-ttu-id="7a2cf-128">Det redigerede dokument er tjekket ind.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-128">The edited document is checked in.</span></span> <span data-ttu-id="7a2cf-129">Alle ændringer er synlige for andre godkendte systembrugere, og disse brugere kan derefter redigere dokumentet.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-129">All changes are visible to other authenticated system users, and those users can then edit the document.</span></span> <span data-ttu-id="7a2cf-130">Ved hver check-ind oprettes en dokumentversionspost i elementets historik.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-130">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="7a2cf-131">Udgivet</span><span class="sxs-lookup"><span data-stu-id="7a2cf-131">Published</span></span>           | <span data-ttu-id="7a2cf-132">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-132">Select **Publish**.</span></span>        | <span data-ttu-id="7a2cf-133">Dokumentet udgives, og ændringerne føres til dit direkte websted og bliver synlige for eksterne brugere.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-133">The document is published, and the changes are pushed to your live site and become discoverable by external users.</span></span> <span data-ttu-id="7a2cf-134">Varer kan kun udgives, hvis de først er tjekket ind ved at vælge **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="7a2cf-134">Items can be published only if they have first been checked in by selecting **Finish editing**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="7a2cf-135">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7a2cf-135">Additional resources</span></span>

[<span data-ttu-id="7a2cf-136">Metoder til at tilføje indhold</span><span class="sxs-lookup"><span data-stu-id="7a2cf-136">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="7a2cf-137">Ordliste til sidemodel</span><span class="sxs-lookup"><span data-stu-id="7a2cf-137">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="7a2cf-138">Arbejd med publiceringsgrupper</span><span class="sxs-lookup"><span data-stu-id="7a2cf-138">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="7a2cf-139">Arbejde med moduler</span><span class="sxs-lookup"><span data-stu-id="7a2cf-139">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="7a2cf-140">Arbejde med fragmenter</span><span class="sxs-lookup"><span data-stu-id="7a2cf-140">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="7a2cf-141">Oversigt over skabeloner og layout</span><span class="sxs-lookup"><span data-stu-id="7a2cf-141">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="7a2cf-142">Tilpasse navigation på webstedet</span><span class="sxs-lookup"><span data-stu-id="7a2cf-142">Customize site navigation</span></span>](customize-site-navigation.md)
