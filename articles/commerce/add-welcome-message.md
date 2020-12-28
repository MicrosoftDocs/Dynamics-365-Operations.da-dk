---
title: Tilføj en velkomstmeddelelse
description: Dette emne beskriver, hvordan du føjer en velkomstmeddelelse til dit Microsoft Dynamics 365 Commerce-websted.
author: psimolin
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: d2a125b4e71016ad620f128af2e3c9f29aa04f4c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411032"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="59438-103">Tilføj en velkomstmeddelelse</span><span class="sxs-lookup"><span data-stu-id="59438-103">Add a welcome message</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="59438-104">Dette emne beskriver, hvordan du føjer en velkomstmeddelelse til dit Microsoft Dynamics 365 Commerce-websted.</span><span class="sxs-lookup"><span data-stu-id="59438-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="59438-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="59438-105">Overview</span></span>

<span data-ttu-id="59438-106">En velkomstmeddelelse på dit e-handelswebsted kan informere de besøgende om igangværende salg, webstedsopdateringer, eller at sæsonens kollektioner er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="59438-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="59438-107">Velkomstmeddelelsen konfigureres ved hjælp af påmindelsesmodulet.</span><span class="sxs-lookup"><span data-stu-id="59438-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="59438-108">Påmindelsesmodulet skal føjes til pladsen **Fejl-/oplysningsmeddelelser** i sidehovedfragmentet.</span><span class="sxs-lookup"><span data-stu-id="59438-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="59438-109">Med påmindelsesmodulet kan du angive den tekst, der skal vises, tekstfarven og justeringen.</span><span class="sxs-lookup"><span data-stu-id="59438-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="59438-110">Det giver dig også mulighed for at angive, om besøgende på webstedet skal kunne afvise meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="59438-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="59438-111">Når en velkomstmeddelelse føjes til et delt sidehovedfragment, vises det på hver side, der bruger den skabelon, hvor det delte sidehovedfragment bruges.</span><span class="sxs-lookup"><span data-stu-id="59438-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="59438-112">Hvis du vil føje en velkomstmeddelelse til dit websted, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="59438-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="59438-113">Naviger til dit websted i Commerce-webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="59438-113">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="59438-114">Vælg **Fragmenter**.</span><span class="sxs-lookup"><span data-stu-id="59438-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="59438-115">Vælg det sidehovedfragment, som meddelelsen skal føjes til.</span><span class="sxs-lookup"><span data-stu-id="59438-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="59438-116">Udvid **Fejl-/oplysningsmeddelelser** i dispositionstræet.</span><span class="sxs-lookup"><span data-stu-id="59438-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="59438-117">Vælg påmindelsesmodulet, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="59438-117">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="59438-118">Hvis der endnu ikke findes et påmindelsesmodul, skal du først vælge ellipseknappen (**...**) ud for **Fejl-/oplysningsmeddelelser** og derefter vælge **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="59438-118">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="59438-119">Vælg **Tilføj datakilde** under fanen **Data** i egenskabsruden til højre, og vælg derefter **Indhold**.</span><span class="sxs-lookup"><span data-stu-id="59438-119">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="59438-120">Skriv teksten til velkomstmeddelelsen i feltet **Inputtekst**.</span><span class="sxs-lookup"><span data-stu-id="59438-120">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="59438-121">Vælg **Gem**, vælg **Afslut redigering** for at tjekke sidehovedfragmentet ind, og vælg derefter **Publicer** for at publicere det.</span><span class="sxs-lookup"><span data-stu-id="59438-121">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="59438-122">Velkomstmeddelelsen vises nu øverst på alle de webstedssider, der bruger det valgte sidehovedfragment.</span><span class="sxs-lookup"><span data-stu-id="59438-122">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59438-123">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="59438-123">Additional resources</span></span>

[<span data-ttu-id="59438-124">Tilføj et logo</span><span class="sxs-lookup"><span data-stu-id="59438-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="59438-125">Vælg et tema for webstedet</span><span class="sxs-lookup"><span data-stu-id="59438-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="59438-126">Arbejd med CSS-tilsidesættelsesfiler</span><span class="sxs-lookup"><span data-stu-id="59438-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="59438-127">Tilføj en favicon</span><span class="sxs-lookup"><span data-stu-id="59438-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="59438-128">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="59438-128">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="59438-129">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="59438-129">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="59438-130">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="59438-130">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

