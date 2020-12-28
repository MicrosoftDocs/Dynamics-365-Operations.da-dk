---
title: Introduktion til omkostningsregnskabstjenesten (privat visning)
description: Dette emne indeholder licensoplysninger og installationsinstruktioner til omkostningsregnskabstjenesten.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: a82af9e8ec1806f470103897389d0316d33a4a06
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424529"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a><span data-ttu-id="4eca6-103">Introduktion til omkostningsregnskabstjenesten (privat visning)</span><span class="sxs-lookup"><span data-stu-id="4eca6-103">Get started with the cost accounting service (private preview)</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="4eca6-104">De funktioner, der er anført i dette emne, er tilgængelige som en del af en privat prøveversion.</span><span class="sxs-lookup"><span data-stu-id="4eca6-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="4eca6-105">Indholdet af dette emne og den funktionalitet, det beskriver, kan ændres.</span><span class="sxs-lookup"><span data-stu-id="4eca6-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="4eca6-106">Du kan finde flere oplysninger om prøveversioner i [Ofte stillede spørgsmål om One Version-tjenesteopdateringer](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="4eca6-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="4eca6-107">Med tjenesten til omkostningsregnskab kan du udføre flere lagerregnskaber i de finansposter for driftsregnskab, som du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="4eca6-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="4eca6-108">Du skal knytte hver finanspost for driftsregnskab til en *konvention*.</span><span class="sxs-lookup"><span data-stu-id="4eca6-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="4eca6-109">En konvention er en samling af følgende typer regnskabspolitikker:</span><span class="sxs-lookup"><span data-stu-id="4eca6-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="4eca6-110">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="4eca6-110">Cost object</span></span>
- <span data-ttu-id="4eca6-111">Basis for inputmåling</span><span class="sxs-lookup"><span data-stu-id="4eca6-111">Input measurement basis</span></span>
- <span data-ttu-id="4eca6-112">Forudsætning for omkostningsforløb</span><span class="sxs-lookup"><span data-stu-id="4eca6-112">Cost flow assumption</span></span>
- <span data-ttu-id="4eca6-113">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="4eca6-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="4eca6-114">Selv efter at du har slået omkostningsregnskabstjenesten til, kan du stadig udføre lagerregnskab i Microsoft Dynamics 365 Supply Chain Management som normalt.</span><span class="sxs-lookup"><span data-stu-id="4eca6-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="4eca6-115">Omkostningsregnskabstjenesten er et tilføjelsesprogram.</span><span class="sxs-lookup"><span data-stu-id="4eca6-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="4eca6-116">For at gøre dets funktioner tilgængelige skal du installere det fra Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="4eca6-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="4eca6-117">Derfor kan du vælge at evaluere det i et testmiljø, før du slår det til i produktionsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="4eca6-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="4eca6-118">Omkostningsregnskabstjenesten understøtter i øjeblikket ikke alle de funktioner til omkostningsstyring, der er indbygget i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4eca6-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="4eca6-119">Det er derfor vigtigt, at du evaluerer, om det funktionssæt, der aktuelt er tilgængeligt, opfylder dine behov.</span><span class="sxs-lookup"><span data-stu-id="4eca6-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a><span data-ttu-id="4eca6-120">Sådan får du omkostningsregnskabstjenesten (privat visning)</span><span class="sxs-lookup"><span data-stu-id="4eca6-120">How to get the cost accounting service (private preview)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4eca6-121">Hvis du vil bruge omkostningsregnskabstjenesten, skal du have et LCS-aktiveret miljø med høj tilgængelighed (ikke et OneBox-miljø), og du skal køre Dynamics 365 Supply Chain Management version 10.0.11 eller senere.</span><span class="sxs-lookup"><span data-stu-id="4eca6-121">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="4eca6-122">Hvis du vil tilmelde dig den private visning af omkostningsregnskabstjenesten, skal du sende dit LCS-miljø-ID med e-mail til [Omkostningsregnskabstjeneste (privat visning)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span><span class="sxs-lookup"><span data-stu-id="4eca6-122">To sign up for the cost accounting service private preview, please send your LCS environment ID by email to [Cost accounting service (private preview)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span></span> <span data-ttu-id="4eca6-123">Når vi godkender dig til programmet, sender vi dig en opfølgnings-e-mail, der indeholder en betanøgle til omkostningsregnskabstjenesten.</span><span class="sxs-lookup"><span data-stu-id="4eca6-123">On approving you for the program, we will send you a follow up email that contains a cost accounting service beta key.</span></span> <span data-ttu-id="4eca6-124">Når du modtager betanøglen, kan du fortsætte ved at [installere tilføjelsesprogrammet](#install).</span><span class="sxs-lookup"><span data-stu-id="4eca6-124">On receiving the beta key, you can proceed by [installing the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="4eca6-125">Licensering</span><span class="sxs-lookup"><span data-stu-id="4eca6-125">Licensing</span></span>

<span data-ttu-id="4eca6-126">Omkostningsregnskabstjenesten er givet i licens sammen med standardfunktionerne i lagerregnskabet, der er tilgængelige for Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4eca6-126">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="4eca6-127">Du behøver ikke at købe en ekstra licens for at bruge tjenesten til omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="4eca6-127">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="4eca6-128">Installer tilføjelsesprogrammet</span><span class="sxs-lookup"><span data-stu-id="4eca6-128">Install the add-in</span></span>

<span data-ttu-id="4eca6-129">Hvis du vil bruge omkostningsregnskabstjenesten, skal du installere tilføjelsesprogrammet med omkostningsregnskabstjenesten til Supply Chain Management som beskrevet i følgende procedure.</span><span class="sxs-lookup"><span data-stu-id="4eca6-129">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="4eca6-130">[Tilmeld dig](#sign-up) til omkostningsregnskabstjenesten (privat visning).</span><span class="sxs-lookup"><span data-stu-id="4eca6-130">[Sign up](#sign-up) for the cost accounting service (private preview).</span></span>

1. <span data-ttu-id="4eca6-131">Log på LCS.</span><span class="sxs-lookup"><span data-stu-id="4eca6-131">Sign in to LCS.</span></span>

1. <span data-ttu-id="4eca6-132">Gå til **Styring af prøveversionsfunktion**.</span><span class="sxs-lookup"><span data-stu-id="4eca6-132">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="4eca6-133">Vælg plustegnet (**+**).</span><span class="sxs-lookup"><span data-stu-id="4eca6-133">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="4eca6-134">I feltet **Kode** skal du angive betanøglen til tilføjelsesprogrammet for omkostningsregnskabstjenesten.</span><span class="sxs-lookup"><span data-stu-id="4eca6-134">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="4eca6-135">(Du skal have modtaget din nøgle pr. mail).</span><span class="sxs-lookup"><span data-stu-id="4eca6-135">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="4eca6-136">Vælg **Ophæv blokering**.</span><span class="sxs-lookup"><span data-stu-id="4eca6-136">Select **Unblock**.</span></span>

1. <span data-ttu-id="4eca6-137">Åbn det LCS-miljø, hvor du vil tilføje tjenesten.</span><span class="sxs-lookup"><span data-stu-id="4eca6-137">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="4eca6-138">Gå til **Alle detaljer**.</span><span class="sxs-lookup"><span data-stu-id="4eca6-138">Go to **Full details**.</span></span>

1. <span data-ttu-id="4eca6-139">Rul ned til oversigtspanelet **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="4eca6-139">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="4eca6-140">Vælg **Installer et nyt tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="4eca6-140">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="4eca6-141">Vælg **Omkostningsregnskabstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="4eca6-141">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="4eca6-142">Følg installationsvejledningen, og accepter vilkårene og betingelserne.</span><span class="sxs-lookup"><span data-stu-id="4eca6-142">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="4eca6-143">Vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="4eca6-143">Select **Install**.</span></span>

1. <span data-ttu-id="4eca6-144">I oversigtspanelet **Miljøtilføjelsesprogrammer** kan du se, at tjenesten til omkostningsregnskab er ved at blive installeret.</span><span class="sxs-lookup"><span data-stu-id="4eca6-144">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="4eca6-145">Efter nogle få minutter skal status ændres fra **Installerer** til **Installeret**.</span><span class="sxs-lookup"><span data-stu-id="4eca6-145">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="4eca6-146">(Du skal muligvis opdatere siden for at se ændringen). På dette tidspunkt er omkostningsregnskabstjenesten klar til brug.</span><span class="sxs-lookup"><span data-stu-id="4eca6-146">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="4eca6-147">Konfigurere integrationen</span><span class="sxs-lookup"><span data-stu-id="4eca6-147">Set up the integration</span></span>

<span data-ttu-id="4eca6-148">Sådan konfigurerer du integrationen mellem omkostningsregnskabstjenesten og Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="4eca6-148">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="4eca6-149">Gå til **Systemadministration > Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="4eca6-149">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="4eca6-150">Vælg **Søg efter opdateringer**.</span><span class="sxs-lookup"><span data-stu-id="4eca6-150">Select **Check for updates**.</span></span>

1. <span data-ttu-id="4eca6-151">Åbn fanen **Alle**, og søg efter funktionen ved navn *Omkostningsregnskabstjeneste*.</span><span class="sxs-lookup"><span data-stu-id="4eca6-151">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="4eca6-152">Vælg **Aktiver nu**.</span><span class="sxs-lookup"><span data-stu-id="4eca6-152">Select **Enable now**.</span></span>

1. <span data-ttu-id="4eca6-153">Gå til **Omkostningsstyring > Omkostningsregnskabstjeneste > Opsætning > Parametre for omkostningsregnskabstjeneste > Integrationsparametre**.</span><span class="sxs-lookup"><span data-stu-id="4eca6-153">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="4eca6-154">I feltet **Program-id** skal du angive følgende kode:</span><span class="sxs-lookup"><span data-stu-id="4eca6-154">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="4eca6-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="4eca6-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="4eca6-156">I feltet **Datatjenesteslutpunkt** skal du angive følgende URL-adresse:</span><span class="sxs-lookup"><span data-stu-id="4eca6-156">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="4eca6-157">I feltet **Slutpunkt for omkostningsregnskabstjeneste** skal du angive følgende URL-adresse:</span><span class="sxs-lookup"><span data-stu-id="4eca6-157">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="4eca6-158">Omkostningsregnskabstjenesten er nu klar til brug.</span><span class="sxs-lookup"><span data-stu-id="4eca6-158">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="4eca6-159">Tilknyttede ressourcer</span><span class="sxs-lookup"><span data-stu-id="4eca6-159">Related resources</span></span>

[<span data-ttu-id="4eca6-160">Startside for omkostningsregnskabstjeneste</span><span class="sxs-lookup"><span data-stu-id="4eca6-160">Cost accounting service home page</span></span>](cost-accounting-service-home.md)
