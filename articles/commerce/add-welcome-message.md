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
ms.openlocfilehash: ca10b01268b5dcd4c6fe448d90cd0ebd65a2673b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001248"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="c56bc-103">Tilføj en velkomstmeddelelse</span><span class="sxs-lookup"><span data-stu-id="c56bc-103">Add a welcome message</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c56bc-104">Dette emne beskriver, hvordan du føjer en velkomstmeddelelse til dit Microsoft Dynamics 365 Commerce-websted.</span><span class="sxs-lookup"><span data-stu-id="c56bc-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="c56bc-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="c56bc-105">Overview</span></span>

<span data-ttu-id="c56bc-106">En velkomstmeddelelse på dit e-handelswebsted kan informere de besøgende om igangværende salg, webstedsopdateringer, eller at sæsonens kollektioner er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="c56bc-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="c56bc-107">Velkomstmeddelelsen konfigureres ved hjælp af påmindelsesmodulet.</span><span class="sxs-lookup"><span data-stu-id="c56bc-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="c56bc-108">Påmindelsesmodulet skal føjes til pladsen **Fejl-/oplysningsmeddelelser** i sidehovedfragmentet.</span><span class="sxs-lookup"><span data-stu-id="c56bc-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="c56bc-109">Med påmindelsesmodulet kan du angive den tekst, der skal vises, tekstfarven og justeringen.</span><span class="sxs-lookup"><span data-stu-id="c56bc-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="c56bc-110">Det giver dig også mulighed for at angive, om besøgende på webstedet skal kunne afvise meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="c56bc-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="c56bc-111">Når en velkomstmeddelelse føjes til et delt sidehovedfragment, vises det på hver side, der bruger den skabelon, hvor det delte sidehovedfragment bruges.</span><span class="sxs-lookup"><span data-stu-id="c56bc-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="c56bc-112">Hvis du vil føje en velkomstmeddelelse til dit websted, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="c56bc-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="c56bc-113">Gå til dit websted i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c56bc-113">In Dynamics 365 Commerce, go to your site.</span></span>
1. <span data-ttu-id="c56bc-114">Vælg **Fragmenter**.</span><span class="sxs-lookup"><span data-stu-id="c56bc-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="c56bc-115">Vælg det sidehovedfragment, som meddelelsen skal føjes til.</span><span class="sxs-lookup"><span data-stu-id="c56bc-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="c56bc-116">Udvid **Fejl-/oplysningsmeddelelser** i dispositionstræet.</span><span class="sxs-lookup"><span data-stu-id="c56bc-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="c56bc-117">Vælg påmindelsesmodulet.</span><span class="sxs-lookup"><span data-stu-id="c56bc-117">Select the alert module.</span></span>

    <span data-ttu-id="c56bc-118">Hvis der endnu ikke findes et påmindelsesmodul, skal du vælge ellipseknappen (**...**) ud for **Fejl-/oplysningsmeddelelser** og derefter vælge **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="c56bc-118">If an alert module doesn't yet exist, select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span> <span data-ttu-id="c56bc-119">Vælg påmindelsesmodulet, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="c56bc-119">Select the alert module, and then select **OK**.</span></span>

1. <span data-ttu-id="c56bc-120">Vælg **Tilføj datakilde** under fanen **Data** i egenskabsruden til højre, og vælg derefter **Indhold**.</span><span class="sxs-lookup"><span data-stu-id="c56bc-120">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="c56bc-121">Skriv teksten til velkomstmeddelelsen i feltet **Inputtekst**.</span><span class="sxs-lookup"><span data-stu-id="c56bc-121">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="c56bc-122">Gem sidehovedfragmentet, check det ind, og publicer det.</span><span class="sxs-lookup"><span data-stu-id="c56bc-122">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="c56bc-123">Velkomstmeddelelsen vises nu øverst på alle de webstedssider, der bruger det valgte sidehovedfragment.</span><span class="sxs-lookup"><span data-stu-id="c56bc-123">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c56bc-124">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c56bc-124">Additional resources</span></span>

[<span data-ttu-id="c56bc-125">Tilføj et logo</span><span class="sxs-lookup"><span data-stu-id="c56bc-125">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="c56bc-126">Vælg et tema for webstedet</span><span class="sxs-lookup"><span data-stu-id="c56bc-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="c56bc-127">Arbejd med CSS-tilsidesættelsesfiler</span><span class="sxs-lookup"><span data-stu-id="c56bc-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="c56bc-128">Tilføj en favicon</span><span class="sxs-lookup"><span data-stu-id="c56bc-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="c56bc-129">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="c56bc-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="c56bc-130">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="c56bc-130">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="c56bc-131">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="c56bc-131">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

