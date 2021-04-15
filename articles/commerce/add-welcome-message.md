---
title: Tilføje en velkomstmeddelelse
description: Dette emne beskriver, hvordan du føjer en velkomstmeddelelse til dit Microsoft Dynamics 365 Commerce-websted.
author: psimolin
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e61f43eca7d1343d020e1c01b5b1140f07b63c6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797377"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="b592f-103">Tilføje en velkomstmeddelelse</span><span class="sxs-lookup"><span data-stu-id="b592f-103">Add a welcome message</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b592f-104">Dette emne beskriver, hvordan du føjer en velkomstmeddelelse til dit Microsoft Dynamics 365 Commerce-websted.</span><span class="sxs-lookup"><span data-stu-id="b592f-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

<span data-ttu-id="b592f-105">En velkomstmeddelelse på dit e-handelswebsted kan informere de besøgende om igangværende salg, webstedsopdateringer, eller at sæsonens kollektioner er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="b592f-105">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="b592f-106">Velkomstmeddelelsen konfigureres ved hjælp af påmindelsesmodulet.</span><span class="sxs-lookup"><span data-stu-id="b592f-106">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="b592f-107">Påmindelsesmodulet skal føjes til pladsen **Fejl-/oplysningsmeddelelser** i sidehovedfragmentet.</span><span class="sxs-lookup"><span data-stu-id="b592f-107">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="b592f-108">Med påmindelsesmodulet kan du angive den tekst, der skal vises, tekstfarven og justeringen.</span><span class="sxs-lookup"><span data-stu-id="b592f-108">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="b592f-109">Det giver dig også mulighed for at angive, om besøgende på webstedet skal kunne afvise meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="b592f-109">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="b592f-110">Når en velkomstmeddelelse føjes til et delt sidehovedfragment, vises det på hver side, der bruger den skabelon, hvor det delte sidehovedfragment bruges.</span><span class="sxs-lookup"><span data-stu-id="b592f-110">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="b592f-111">Hvis du vil føje en velkomstmeddelelse til dit websted, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="b592f-111">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="b592f-112">Naviger til dit websted i Commerce-webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="b592f-112">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="b592f-113">Vælg **Fragmenter**.</span><span class="sxs-lookup"><span data-stu-id="b592f-113">Select **Fragments**.</span></span>
1. <span data-ttu-id="b592f-114">Vælg det sidehovedfragment, som meddelelsen skal føjes til.</span><span class="sxs-lookup"><span data-stu-id="b592f-114">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="b592f-115">Udvid **Fejl-/oplysningsmeddelelser** i dispositionstræet.</span><span class="sxs-lookup"><span data-stu-id="b592f-115">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="b592f-116">Vælg påmindelsesmodulet, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="b592f-116">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="b592f-117">Hvis der endnu ikke findes et påmindelsesmodul, skal du først vælge ellipseknappen (**...**) ud for **Fejl-/oplysningsmeddelelser** og derefter vælge **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="b592f-117">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="b592f-118">Vælg **Tilføj datakilde** under fanen **Data** i egenskabsruden til højre, og vælg derefter **Indhold**.</span><span class="sxs-lookup"><span data-stu-id="b592f-118">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="b592f-119">Skriv teksten til velkomstmeddelelsen i feltet **Inputtekst**.</span><span class="sxs-lookup"><span data-stu-id="b592f-119">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="b592f-120">Vælg **Gem**, vælg **Afslut redigering** for at tjekke sidehovedfragmentet ind, og vælg derefter **Publicer** for at publicere det.</span><span class="sxs-lookup"><span data-stu-id="b592f-120">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="b592f-121">Velkomstmeddelelsen vises nu øverst på alle de webstedssider, der bruger det valgte sidehovedfragment.</span><span class="sxs-lookup"><span data-stu-id="b592f-121">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b592f-122">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b592f-122">Additional resources</span></span>

[<span data-ttu-id="b592f-123">Tilføj et logo</span><span class="sxs-lookup"><span data-stu-id="b592f-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="b592f-124">Vælg et tema for webstedet</span><span class="sxs-lookup"><span data-stu-id="b592f-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="b592f-125">Arbejd med CSS-tilsidesættelsesfiler</span><span class="sxs-lookup"><span data-stu-id="b592f-125">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="b592f-126">Tilføj en favicon</span><span class="sxs-lookup"><span data-stu-id="b592f-126">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="b592f-127">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="b592f-127">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="b592f-128">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="b592f-128">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="b592f-129">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="b592f-129">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
