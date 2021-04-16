---
title: Oprette et udviklingsmiljø til e-handel for at fejlfinde en Retail Server virtuel maskine på niveau 1
description: Dette emne beskriver oprettelse af et udviklingsmiljø til e-handel for at fejlfinde en Retail Server virtuel maskine på niveau 1 (VM).
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5ef286aa28ff459befb72b0178f308e5fb85ec44
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801477"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a><span data-ttu-id="18d29-103">Oprette et udviklingsmiljø til e-handel for at fejlfinde en Retail Server virtuel maskine på niveau 1</span><span class="sxs-lookup"><span data-stu-id="18d29-103">Set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="18d29-104">Dette emne beskriver oprettelse af et udviklingsmiljø til e-handel for at fejlfinde en Retail Server virtuel maskine på niveau 1 (VM).</span><span class="sxs-lookup"><span data-stu-id="18d29-104">This topic explains how to set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine (VM).</span></span>

## <a name="description"></a><span data-ttu-id="18d29-105">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="18d29-105">Description</span></span>

<span data-ttu-id="18d29-106">Microsoft Dynamics 365 Commerce Lag 1-miljøer implementeres typisk til udvikling af commerce runtime (CRT) og POS-udvidelse.</span><span class="sxs-lookup"><span data-stu-id="18d29-106">Microsoft Dynamics 365 Commerce Tier 1 environments are typically deployed for Commerce runtime (CRT) and point of sale (POS) extension development.</span></span> <span data-ttu-id="18d29-107">De er enkeltstående miljøer.</span><span class="sxs-lookup"><span data-stu-id="18d29-107">They are standalone environments.</span></span> <span data-ttu-id="18d29-108">På grund af arkitekturens art (a service as a service, inkluderer de ikke komponenter til e-handel).</span><span class="sxs-lookup"><span data-stu-id="18d29-108">Because of the software as a service (SaaS) nature of the architecture, they don't include e-commerce components.</span></span>

<span data-ttu-id="18d29-109">I visse scenarier kan det være en god ide at teste kald til udvidelser i et Lag 1-miljø, så du kan fejlfinde udvidelser fra e-handelskomponenter.</span><span class="sxs-lookup"><span data-stu-id="18d29-109">In some scenarios, you might want to test calls to extensions in a Tier 1 environment, so that you can debug extensions from e-commerce components.</span></span> <span data-ttu-id="18d29-110">De generelle instruktioner findes i [Foretage fejlfinding i forhold til et niveau 1 Commerce-udviklingsmiljø](../e-commerce-extensibility/debug-tier-1.md).</span><span class="sxs-lookup"><span data-stu-id="18d29-110">For general instructions, see [Debug against a Tier 1 Commerce development environment](../e-commerce-extensibility/debug-tier-1.md).</span></span>

<span data-ttu-id="18d29-111">Når du bruger fejlfinding i et Niveau 1-miljø, kan krydsserverkald på tværs af servere forårsage forskellige fejl, der er relateret til sikkerhedspolitiken for indhold, da webstedet nu kalder en anden Retail Server.</span><span class="sxs-lookup"><span data-stu-id="18d29-111">When you debug against a Tier 1 environment, because the site is now calling a different Retail Server, cross-server calls might cause various errors that are related to the content security policy.</span></span>

<span data-ttu-id="18d29-112">I følgende illustration vises et eksempel på en fejl, der kan forekomme, når der er valgt en variant på en side med produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="18d29-112">The following illustration shows an example of an error that might occur when a variant is selected on a product details page.</span></span>

![Fejl, når der er valgt en variant på en side med produktdetaljer](media/unhandled-rejection-error.jpg)

<span data-ttu-id="18d29-114">I følgende illustration vises et eksempel på en lignende fejl i en browsers fejlfindingsværktøjer (F12 Developer Tools).</span><span class="sxs-lookup"><span data-stu-id="18d29-114">The following illustration shows an example of a similar error in a browser's debugger tools (F12 Developer Tools).</span></span> <span data-ttu-id="18d29-115">Fejlmeddelelsen nævner overtrædelse af sikkerhedspolitikdirektiverne for indhold.</span><span class="sxs-lookup"><span data-stu-id="18d29-115">The error message mentions violation of the content security policy directive.</span></span>

![Fejl i fejlfindingsværktøjer](media/debugger-tools-error.JPG)

## <a name="resolution"></a><span data-ttu-id="18d29-117">Løsning</span><span class="sxs-lookup"><span data-stu-id="18d29-117">Resolution</span></span>

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a><span data-ttu-id="18d29-118">Deaktivere politikken for indholdssikkerhed for webstedet i Commerce Site Builder</span><span class="sxs-lookup"><span data-stu-id="18d29-118">Disable the content security policy for the site in Commerce site builder</span></span>

1. <span data-ttu-id="18d29-119">Vælg det sted, du arbejder på.</span><span class="sxs-lookup"><span data-stu-id="18d29-119">Select the site that you're working on.</span></span>
1. <span data-ttu-id="18d29-120">Vælg **Indstillinger**, og vælg derefter **Udvidelse**.</span><span class="sxs-lookup"><span data-stu-id="18d29-120">Select **Settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="18d29-121">Vælg **Deaktiver indholdssikkerhedspolitik** under fanen **Indholdssikkerhedspolitik**.</span><span class="sxs-lookup"><span data-stu-id="18d29-121">On the **Content security policy** tab, select **Disable content security policy**.</span></span>
1. <span data-ttu-id="18d29-122">Vælg **Gem og udgiv**.</span><span class="sxs-lookup"><span data-stu-id="18d29-122">Select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="18d29-123">Det er ikke muligt at logge på business-to-consumer (B2C) i et lokalt udviklingsmiljø.</span><span class="sxs-lookup"><span data-stu-id="18d29-123">Business-to-consumer (B2C) sign-in won't work in a local development environment.</span></span> <span data-ttu-id="18d29-124">Du kan dog bruge gæsteudbetaling eller build-side-id'er til at simulere en brugers logon efter behov.</span><span class="sxs-lookup"><span data-stu-id="18d29-124">However, you can use guest checkouts or build page mocks to simulate a user sign-in as required.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18d29-125">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="18d29-125">Additional resources</span></span>

[<span data-ttu-id="18d29-126">Introduktion til e-handelonlineudvidelsesudvikling</span><span class="sxs-lookup"><span data-stu-id="18d29-126">Get started with e-commerce online extensibility development</span></span>](../e-commerce-extensibility/sdk-getting-started.md)

[<span data-ttu-id="18d29-127">Administrere sikkerhedspolitik for indhold (CSP) på e-handelswebsted</span><span class="sxs-lookup"><span data-stu-id="18d29-127">Manage content security policy (CSP) on e-commerce site</span></span>](../manage-csp.md)
