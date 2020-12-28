---
title: Handling for tilbagekald af ordre i POS
description: Dette emne indeholder en beskrivelse af de funktionsegenskaber, der er tilgængelige på forbedrede sider med tilbagekaldsordrer i POS.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 42b11ff16757d633b868dfdf248341193a44378f
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665292"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="16bdd-103">Handling for tilbagekald af ordre i POS</span><span class="sxs-lookup"><span data-stu-id="16bdd-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="16bdd-104">Handlingen **Tilbagekald af ordre** i Commerce POS indeholder har opdaterede søge- og filtreringsfunktioner for ordren samt ordrespecifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="16bdd-104">The **Recall order** operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="16bdd-105">Denne funktion er tilgængelig i Commerce version 10.0.15 og nyere.</span><span class="sxs-lookup"><span data-stu-id="16bdd-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="16bdd-106">Hvis du vil aktivere denne funktion, skal du deaktivere **Forbedret handling for ordretilbagekald i POS**-funktionen i arbejdsområdet **Funktionsstyring** i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="16bdd-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="16bdd-107">Når du har aktiveret funktionen, bør du overveje at opdatere [skærmlayout](pos-screen-layouts.md) i POS for at udnytte nogle af de ændrede muligheder.</span><span class="sxs-lookup"><span data-stu-id="16bdd-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="16bdd-108">Konfigurationen af handlingsknappen **Tilbagekald ordre** giver organisationer mulighed for at implementere handlingen med en foruddefineret skærm.</span><span class="sxs-lookup"><span data-stu-id="16bdd-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![Konfiguration af knapmatrix](media/recallorderbuttongrid.png)

<span data-ttu-id="16bdd-110">Der findes følgende skærmindstillinger.</span><span class="sxs-lookup"><span data-stu-id="16bdd-110">The display options are as follows.</span></span>
- <span data-ttu-id="16bdd-111">**Ingen** – Denne indstilling installerer handlingen uden en bestemt visning.</span><span class="sxs-lookup"><span data-stu-id="16bdd-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="16bdd-112">Når en bruger åbner handlingen med denne konfiguration, vil de blive bedt om at søge efter og finde ordrer eller vælge fra et foruddefineret ordrefilter.</span><span class="sxs-lookup"><span data-stu-id="16bdd-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="16bdd-113">**Ordrer, der skal opfyldes** – Når en bruger starter handlingen, køres der automatisk en forespørgsel for at søge efter og få vist en liste over ordrer, der skal opfyldes af butikken.</span><span class="sxs-lookup"><span data-stu-id="16bdd-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the store.</span></span> <span data-ttu-id="16bdd-114">Disse ordrer er konfigureret til butiksafhentning eller butiksafsendelse, og linjerne i disse ordrer er endnu ikke plukket eller pakket.</span><span class="sxs-lookup"><span data-stu-id="16bdd-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="16bdd-115">**Ordrer, der skal afhentes** – Når en bruger starter handlingen, køres der automatisk en forespørgsel for at søge efter og få vist en liste over ordrer, der er konfigureret til afhentning i brugerens aktuelle butik.</span><span class="sxs-lookup"><span data-stu-id="16bdd-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="16bdd-116">**Ordrer, der skal leveres** – Når en bruger starter handlingen, køres der automatisk en forespørgsel for at søge efter og få vist en liste over ordrer, der er konfigureret til levering fra brugerens aktuelle butik.</span><span class="sxs-lookup"><span data-stu-id="16bdd-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="16bdd-117">Når du starter handlingen **Tilbagekald ordre** fra POS, hvis visningen er konfigureret til **Ingen**, kan brugeren søge efter og hente ordrer på en af følgende måder.</span><span class="sxs-lookup"><span data-stu-id="16bdd-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="16bdd-118">Scan ordrestregkoder.</span><span class="sxs-lookup"><span data-stu-id="16bdd-118">Scan order barcodes.</span></span> <span data-ttu-id="16bdd-119">Dette søger efter match i felter med ordrenummer, kanalreference og kvitterings-id.</span><span class="sxs-lookup"><span data-stu-id="16bdd-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="16bdd-120">Vælg ikonet **Søg efter ordrer** eller **Søg og filtrer** på applinjen for at bruge filtreringsmekanismen til at finde ordrer, der opfylder filterkriterierne.</span><span class="sxs-lookup"><span data-stu-id="16bdd-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="16bdd-121">Vælg mellem et foruddefineret filter fra rullemenuen **Vis ordrer** (ordrer, der skal opfyldes, ordrer, der skal afhentes, eller ordrer, der skal leveres).</span><span class="sxs-lookup"><span data-stu-id="16bdd-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![RecallOrderMainMenu](media/recallordermain.png)

<span data-ttu-id="16bdd-123">Når søgekriterierne er anvendt, vises der en liste over tilsvarende salgsordrer i programmet.</span><span class="sxs-lookup"><span data-stu-id="16bdd-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span>

![RecallOrderDetail](media/orderrecalldetail.png)

<span data-ttu-id="16bdd-125">En bruger kan vælge en ordre på listen for at få vist flere detaljer.</span><span class="sxs-lookup"><span data-stu-id="16bdd-125">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="16bdd-126">I panelet med oplysninger i højre side af skærmen vises der oplysninger om den valgte ordre, herunder ordrelinjedetaljer, leveringsdetaljer og oplysninger om opfyldning.</span><span class="sxs-lookup"><span data-stu-id="16bdd-126">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="16bdd-127">Fra applinjen kan en bruger vælge en operation.</span><span class="sxs-lookup"><span data-stu-id="16bdd-127">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="16bdd-128">Afhængigt af status for ordren er det ikke sikkert, at bestemte handlinger er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="16bdd-128">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="16bdd-129">**Returner** – Udfører en returnering for en eller flere fakturaer, der er relateret til den valgte kundeordre.</span><span class="sxs-lookup"><span data-stu-id="16bdd-129">**Return** – Executes a return for one or more invoices related to the selected customer order.</span></span>

- <span data-ttu-id="16bdd-130">**Annuller** – Udsted en fuld annullering af den valgte salgsordre.</span><span class="sxs-lookup"><span data-stu-id="16bdd-130">**Cancel** – Issue a full cancellation of the selected sales order.</span></span>

- <span data-ttu-id="16bdd-131">**Opfyld** – Overfører brugeren til siden med ordreopfyldning, som er filtreret for den valgte ordre.</span><span class="sxs-lookup"><span data-stu-id="16bdd-131">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="16bdd-132">Det er kun de ordrelinjer, der er åbne for opfyldelse af brugerens butik for den valgte ordre, der vises.</span><span class="sxs-lookup"><span data-stu-id="16bdd-132">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="16bdd-133">**Rediger** – Giver brugerne mulighed for at foretage ændringer i den valgte kundeordre.</span><span class="sxs-lookup"><span data-stu-id="16bdd-133">**Edit** – Allows users to make changes to the selected customer order.</span></span>

- <span data-ttu-id="16bdd-134">**Afhent** – Starter afhentningsflowet, hvilket giver brugeren mulighed for at vælge de produkter, der skal afhentes, og opretter salgsposteringen for afhentning.</span><span class="sxs-lookup"><span data-stu-id="16bdd-134">**Pick up** – Launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>
