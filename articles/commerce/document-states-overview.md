---
title: Dokumenttilstande og -livscyklus
description: Dette emne omhandler de forskellige dokumenttilstande for sideelementer i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: b4f1c462f734b2d58843308f0f877fe18a4d9af7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002975"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="63ad7-103">Dokumenttilstande og -livscyklus</span><span class="sxs-lookup"><span data-stu-id="63ad7-103">Document states and lifecycle</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="63ad7-104">Dette emne omhandler de forskellige dokumenttilstande for sideelementer i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="63ad7-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="63ad7-105">Beskrivelser af dokumenttilstande</span><span class="sxs-lookup"><span data-stu-id="63ad7-105">Document state descriptions</span></span>

<span data-ttu-id="63ad7-106">Emnelisten i [Sideelementer](page-elements-overview.md) indeholder forskellige dokumenttyper i CMS (Content Management System).</span><span class="sxs-lookup"><span data-stu-id="63ad7-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="63ad7-107">Disse dokumenttyper kan have flere forskellige tilstande i oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="63ad7-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="63ad7-108">Dokumenttilstandene hjælper med at forhindre datakonflikter og gennemtvinge versionskontrol.</span><span class="sxs-lookup"><span data-stu-id="63ad7-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="63ad7-109">De bestemmer, hvem der kan ændre dokumenterne, hvornår dokumenterne kan ændres, og hvornår ændringer kan ses af andre personer.</span><span class="sxs-lookup"><span data-stu-id="63ad7-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="63ad7-110">I følgende tabel vises de mulige dokumenttilstande for sideelementer i Commerce.</span><span class="sxs-lookup"><span data-stu-id="63ad7-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="63ad7-111">Dokumenttilstand</span><span class="sxs-lookup"><span data-stu-id="63ad7-111">Document state</span></span> | <span data-ttu-id="63ad7-112">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="63ad7-112">Description</span></span> |
|---|---|
| <span data-ttu-id="63ad7-113">Checket ud</span><span class="sxs-lookup"><span data-stu-id="63ad7-113">Checked out</span></span> | <span data-ttu-id="63ad7-114">Når et CMS-element er checket ud til dig, kan det ikke redigeres af andre godkendte systembrugere.</span><span class="sxs-lookup"><span data-stu-id="63ad7-114">When a CMS item is checked out to you, it can't be edited by any other authenticated system users.</span></span> <span data-ttu-id="63ad7-115">De ændringer, du foretager af elementet, er kun synlige for dig.</span><span class="sxs-lookup"><span data-stu-id="63ad7-115">Any changes that you make to the item are visible only to you.</span></span> |
| <span data-ttu-id="63ad7-116">Checket ind</span><span class="sxs-lookup"><span data-stu-id="63ad7-116">Checked in</span></span> | <span data-ttu-id="63ad7-117">Når et CMS-element checkes ind, er alle ændringer synlige for andre godkendte systembrugere, og disse brugere kan derefter checke elementet ud og redigere det.</span><span class="sxs-lookup"><span data-stu-id="63ad7-117">When a CMS item is checked in, all changes are visible to other authenticated system users, and those users can then check out the item and edit it.</span></span> <span data-ttu-id="63ad7-118">Ved hver check-ind oprettes en dokumentversionspost i elementets historik.</span><span class="sxs-lookup"><span data-stu-id="63ad7-118">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="63ad7-119">Udgivet</span><span class="sxs-lookup"><span data-stu-id="63ad7-119">Published</span></span> | <span data-ttu-id="63ad7-120">Når et CMS-element udgives, flyttes det til dit aktive websted og kan registreres på internettet af ikke-godkendte eksterne brugere.</span><span class="sxs-lookup"><span data-stu-id="63ad7-120">When a CMS item is published, it's pushed to your live site and becomes discoverable on the internet by non-authenticated external users.</span></span> <span data-ttu-id="63ad7-121">Elementer kan kun udgives, hvis de er blevet checket ind.</span><span class="sxs-lookup"><span data-stu-id="63ad7-121">Items can be published only if they have been checked in.</span></span> |
| <span data-ttu-id="63ad7-122">Gemt</span><span class="sxs-lookup"><span data-stu-id="63ad7-122">Saved</span></span> | <span data-ttu-id="63ad7-123">Ændringer, der er foretaget af et element, der er checket ud, kan gemmes i CMS, før elementet tjekkes ind eller publiceres.</span><span class="sxs-lookup"><span data-stu-id="63ad7-123">Changes that have been made to a checked-out CMS item can be saved to the CMS before the item is checked in or published.</span></span> <span data-ttu-id="63ad7-124">Disse gemte ændringer er ikke synlige for andre godkendte systembrugere, før elementet er tjekket ind.</span><span class="sxs-lookup"><span data-stu-id="63ad7-124">These saved changes aren't visible to other authenticated system users until the item is checked in.</span></span> <span data-ttu-id="63ad7-125">De er ikke synlige for eksterne brugere, før elementet er publiceret.</span><span class="sxs-lookup"><span data-stu-id="63ad7-125">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="63ad7-126">Kasseret udcheckning</span><span class="sxs-lookup"><span data-stu-id="63ad7-126">Discarded check out</span></span> | <span data-ttu-id="63ad7-127">Når et element, der er checket ud af CMS, kasseres, slettes alle gemte ændringer, og elementet tilbageføres til den version, der senest blev checket ind.</span><span class="sxs-lookup"><span data-stu-id="63ad7-127">When a checked-out CMS item is discarded, all saved changes are deleted, and the item reverts to the version that was most recently checked in.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="63ad7-128">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="63ad7-128">Additional resources</span></span>

[<span data-ttu-id="63ad7-129">Metoder til at tilføje indhold</span><span class="sxs-lookup"><span data-stu-id="63ad7-129">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="63ad7-130">Ordliste til sidemodel</span><span class="sxs-lookup"><span data-stu-id="63ad7-130">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="63ad7-131">Arbejd med publiceringsgrupper</span><span class="sxs-lookup"><span data-stu-id="63ad7-131">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="63ad7-132">Arbejde med moduler</span><span class="sxs-lookup"><span data-stu-id="63ad7-132">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="63ad7-133">Arbejde med fragmenter</span><span class="sxs-lookup"><span data-stu-id="63ad7-133">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="63ad7-134">Oversigt over skabeloner og layout</span><span class="sxs-lookup"><span data-stu-id="63ad7-134">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="63ad7-135">Tilpasse navigation på webstedet</span><span class="sxs-lookup"><span data-stu-id="63ad7-135">Customize site navigation</span></span>](customize-site-navigation.md)
