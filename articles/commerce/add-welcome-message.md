---
title: Tilføj en velkomstmeddelelse
description: Dette emne beskriver, hvordan du føjer en velkomstmeddelelse til dit Microsoft Dynamics 365 Commerce-websted.
author: psimolin
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4e9deeeaf491b77700ba0833e429f05d376a4392
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914510"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="2af21-103">Tilføj en velkomstmeddelelse</span><span class="sxs-lookup"><span data-stu-id="2af21-103">Add a welcome message</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2af21-104">Dette emne beskriver, hvordan du føjer en velkomstmeddelelse til dit Microsoft Dynamics 365 Commerce-websted.</span><span class="sxs-lookup"><span data-stu-id="2af21-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="2af21-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="2af21-105">Overview</span></span>

<span data-ttu-id="2af21-106">En velkomstmeddelelse på dit e-handelswebsted kan informere de besøgende om igangværende salg, webstedsopdateringer, eller at sæsonens kollektioner er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="2af21-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="2af21-107">Velkomstmeddelelsen konfigureres ved hjælp af påmindelsesmodulet.</span><span class="sxs-lookup"><span data-stu-id="2af21-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="2af21-108">Påmindelsesmodulet skal føjes til pladsen **Fejl-/oplysningsmeddelelser** i sidehovedfragmentet.</span><span class="sxs-lookup"><span data-stu-id="2af21-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="2af21-109">Med påmindelsesmodulet kan du angive den tekst, der skal vises, tekstfarven og justeringen.</span><span class="sxs-lookup"><span data-stu-id="2af21-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="2af21-110">Det giver dig også mulighed for at angive, om besøgende på webstedet skal kunne afvise meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="2af21-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="2af21-111">Når en velkomstmeddelelse føjes til et delt sidehovedfragment, vises det på hver side, der bruger den skabelon, hvor det delte sidehovedfragment bruges.</span><span class="sxs-lookup"><span data-stu-id="2af21-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="2af21-112">Hvis du vil føje en velkomstmeddelelse til dit websted, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="2af21-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="2af21-113">Gå til dit websted i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2af21-113">In Dynamics 365 Commerce, go to your site.</span></span>
1. <span data-ttu-id="2af21-114">Vælg **Fragmenter**.</span><span class="sxs-lookup"><span data-stu-id="2af21-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="2af21-115">Vælg det sidehovedfragment, som meddelelsen skal føjes til.</span><span class="sxs-lookup"><span data-stu-id="2af21-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="2af21-116">Udvid **Fejl-/oplysningsmeddelelser** i dispositionstræet.</span><span class="sxs-lookup"><span data-stu-id="2af21-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="2af21-117">Vælg påmindelsesmodulet.</span><span class="sxs-lookup"><span data-stu-id="2af21-117">Select the alert module.</span></span>

    <span data-ttu-id="2af21-118">Hvis der endnu ikke findes et påmindelsesmodul, skal du vælge ellipseknappen (**...**) ud for **Fejl-/oplysningsmeddelelser** og derefter vælge **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="2af21-118">If an alert module doesn't yet exist, select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span> <span data-ttu-id="2af21-119">Vælg påmindelsesmodulet, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="2af21-119">Select the alert module, and then select **OK**.</span></span>

1. <span data-ttu-id="2af21-120">Vælg **Tilføj datakilde** under fanen **Data** i egenskabsruden til højre, og vælg derefter **Indhold**.</span><span class="sxs-lookup"><span data-stu-id="2af21-120">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="2af21-121">Skriv teksten til velkomstmeddelelsen i feltet **Inputtekst**.</span><span class="sxs-lookup"><span data-stu-id="2af21-121">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="2af21-122">Gem sidehovedfragmentet, check det ind, og publicer det.</span><span class="sxs-lookup"><span data-stu-id="2af21-122">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="2af21-123">Velkomstmeddelelsen vises nu øverst på alle de webstedssider, der bruger det valgte sidehovedfragment.</span><span class="sxs-lookup"><span data-stu-id="2af21-123">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2af21-124">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2af21-124">Additional resources</span></span>

[<span data-ttu-id="2af21-125">Tilføj et logo</span><span class="sxs-lookup"><span data-stu-id="2af21-125">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="2af21-126">Vælg et tema for webstedet</span><span class="sxs-lookup"><span data-stu-id="2af21-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="2af21-127">Arbejd med CSS-tilsidesættelsesfiler</span><span class="sxs-lookup"><span data-stu-id="2af21-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="2af21-128">Tilføj en favicon</span><span class="sxs-lookup"><span data-stu-id="2af21-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="2af21-129">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="2af21-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="2af21-130">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="2af21-130">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="2af21-131">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="2af21-131">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

