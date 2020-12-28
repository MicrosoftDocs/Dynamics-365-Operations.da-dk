---
title: Dokumenttilstande og -livscyklus
description: Dette emne omhandler de forskellige dokumenttilstande for sideelementer i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
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
ms.openlocfilehash: 8aad7ef8425e46182c669686710dfc178abc418f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411085"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="0a739-103">Dokumenttilstande og -livscyklus</span><span class="sxs-lookup"><span data-stu-id="0a739-103">Document states and lifecycle</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0a739-104">Dette emne omhandler de forskellige dokumenttilstande for sideelementer i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0a739-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="0a739-105">Beskrivelser af dokumenttilstande</span><span class="sxs-lookup"><span data-stu-id="0a739-105">Document state descriptions</span></span>

<span data-ttu-id="0a739-106">Emnelisten i [Sideelementer](page-elements-overview.md) indeholder forskellige dokumenttyper i CMS (Content Management System).</span><span class="sxs-lookup"><span data-stu-id="0a739-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="0a739-107">Disse dokumenttyper kan have flere forskellige tilstande i oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="0a739-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="0a739-108">Dokumenttilstandene hjælper med at forhindre datakonflikter og gennemtvinge versionskontrol.</span><span class="sxs-lookup"><span data-stu-id="0a739-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="0a739-109">De bestemmer, hvem der kan ændre dokumenterne, hvornår dokumenterne kan ændres, og hvornår ændringer kan ses af andre personer.</span><span class="sxs-lookup"><span data-stu-id="0a739-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="0a739-110">I følgende tabel vises de mulige dokumenttilstande for sideelementer i Commerce.</span><span class="sxs-lookup"><span data-stu-id="0a739-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="0a739-111">Dokumenttilstand</span><span class="sxs-lookup"><span data-stu-id="0a739-111">Document state</span></span>      | <span data-ttu-id="0a739-112">Webstedsgeneratorhandling</span><span class="sxs-lookup"><span data-stu-id="0a739-112">Site builder action</span></span>        | <span data-ttu-id="0a739-113">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="0a739-113">Description</span></span>                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="0a739-114">Tjekket ud</span><span class="sxs-lookup"><span data-stu-id="0a739-114">Checked out</span></span>         | <span data-ttu-id="0a739-115">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="0a739-115">Select **Edit**.</span></span>           | <span data-ttu-id="0a739-116">Det ønskede dokument er tjekket ud til dig.</span><span class="sxs-lookup"><span data-stu-id="0a739-116">The applicable document is checked out to you.</span></span> <span data-ttu-id="0a739-117">Mens et dokument er i denne tilstand, kan det ikke ændres af andre godkendte systembrugere, og eventuelle ændringer, du foretager i dokumentet, er kun synlige for dig.</span><span class="sxs-lookup"><span data-stu-id="0a739-117">While a document is in this state, it can't be changed by other authenticated system users, and any changes that you make to the document are visible only to you.</span></span> |
| <span data-ttu-id="0a739-118">Gemt</span><span class="sxs-lookup"><span data-stu-id="0a739-118">Saved</span></span>               | <span data-ttu-id="0a739-119">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="0a739-119">Select **Save**.</span></span>           | <span data-ttu-id="0a739-120">Ændringer, der er foretaget i et dokument, der er tjekket ud, gemmes i databasen, men dokumentet er endnu ikke tjekket ind eller udgivet.</span><span class="sxs-lookup"><span data-stu-id="0a739-120">Changes that have been made to a checked-out document are saved to the database, but the document isn't yet checked in or published.</span></span> <span data-ttu-id="0a739-121">De gemte ændringer er ikke synlige for andre godkendte systembrugere, før forfatteren vælger **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="0a739-121">The saved changes aren't visible to other authenticated system users until the author selects **Finish editing**.</span></span> <span data-ttu-id="0a739-122">De er ikke synlige for eksterne brugere, før elementet er publiceret.</span><span class="sxs-lookup"><span data-stu-id="0a739-122">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="0a739-123">Kasseret udcheckning</span><span class="sxs-lookup"><span data-stu-id="0a739-123">Discarded check out</span></span> | <span data-ttu-id="0a739-124">Vælg **Kassér redigeringer**.</span><span class="sxs-lookup"><span data-stu-id="0a739-124">Select **Discard edits**.</span></span>  | <span data-ttu-id="0a739-125">Alle ændringer af dokumentet, der er tjekket ud, slettes, og varen vender tilbage til den seneste version, der blev tjekket ind.</span><span class="sxs-lookup"><span data-stu-id="0a739-125">All changes to the checked-out document are discarded, and the item reverts to the last version that was checked in.</span></span> |
| <span data-ttu-id="0a739-126">Tjekket ind</span><span class="sxs-lookup"><span data-stu-id="0a739-126">Checked in</span></span>          | <span data-ttu-id="0a739-127">Vælg **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="0a739-127">Select **Finish editing**.</span></span> | <span data-ttu-id="0a739-128">Det redigerede dokument er tjekket ind.</span><span class="sxs-lookup"><span data-stu-id="0a739-128">The edited document is checked in.</span></span> <span data-ttu-id="0a739-129">Alle ændringer er synlige for andre godkendte systembrugere, og disse brugere kan derefter redigere dokumentet.</span><span class="sxs-lookup"><span data-stu-id="0a739-129">All changes are visible to other authenticated system users, and those users can then edit the document.</span></span> <span data-ttu-id="0a739-130">Ved hver check-ind oprettes en dokumentversionspost i elementets historik.</span><span class="sxs-lookup"><span data-stu-id="0a739-130">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="0a739-131">Udgivet</span><span class="sxs-lookup"><span data-stu-id="0a739-131">Published</span></span>           | <span data-ttu-id="0a739-132">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="0a739-132">Select **Publish**.</span></span>        | <span data-ttu-id="0a739-133">Dokumentet udgives, og ændringerne føres til dit direkte websted og bliver synlige for eksterne brugere.</span><span class="sxs-lookup"><span data-stu-id="0a739-133">The document is published, and the changes are pushed to your live site and become discoverable by external users.</span></span> <span data-ttu-id="0a739-134">Varer kan kun udgives, hvis de først er tjekket ind ved at vælge **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="0a739-134">Items can be published only if they have first been checked in by selecting **Finish editing**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="0a739-135">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="0a739-135">Additional resources</span></span>

[<span data-ttu-id="0a739-136">Metoder til at tilføje indhold</span><span class="sxs-lookup"><span data-stu-id="0a739-136">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="0a739-137">Ordliste til sidemodel</span><span class="sxs-lookup"><span data-stu-id="0a739-137">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="0a739-138">Arbejde med publiceringsgrupper</span><span class="sxs-lookup"><span data-stu-id="0a739-138">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="0a739-139">Aktivere og bruge deling på tværs af kanaler</span><span class="sxs-lookup"><span data-stu-id="0a739-139">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="0a739-140">Arbejde med moduler</span><span class="sxs-lookup"><span data-stu-id="0a739-140">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="0a739-141">Arbejde med fragmenter</span><span class="sxs-lookup"><span data-stu-id="0a739-141">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="0a739-142">Oversigt over skabeloner og layout</span><span class="sxs-lookup"><span data-stu-id="0a739-142">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="0a739-143">Tilpasse navigation på webstedet</span><span class="sxs-lookup"><span data-stu-id="0a739-143">Customize site navigation</span></span>](customize-site-navigation.md)
