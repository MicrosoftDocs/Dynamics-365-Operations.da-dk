---
title: "Initialisere oprindelsesdata i et nyt detailmiljø"
description: I denne artikel beskrives de data, der er oprettet som en del af initialiseringen for Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: af2d01dcfddc11559c6c5b046dcac8cd8dc95e76
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a><span data-ttu-id="bb54f-103">Initialisere oprindelsesdata i et nyt detailmiljø</span><span class="sxs-lookup"><span data-stu-id="bb54f-103">Initialize seed data in a new Retail environment</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="bb54f-104">I denne artikel beskrives de data, der er oprettet som en del af initialiseringen for Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="bb54f-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="bb54f-105">Når detailløsningen er blevet installeret via Microsoft Dynamics livscyklus Services (LCS), skal du initialisere detailkonfigurationen for at oprette de grundlæggende konfigurationsdata.</span><span class="sxs-lookup"><span data-stu-id="bb54f-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span> <span data-ttu-id="bb54f-106">**Vigtigt::** Før du initialiserer detailkonfiguration, skal du kontrollere, at du har angivet et sprog og en postadresse for hver juridisk enhed, hvor du vil konfigurere detailbutikker.</span><span class="sxs-lookup"><span data-stu-id="bb54f-106">**Important:** Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="bb54f-107">Dette trin skal udføres for hver juridisk enhed, du bruger til detailsalg.</span><span class="sxs-lookup"><span data-stu-id="bb54f-107">This step must be completed for each legal entity that you use for retail.</span></span> <span data-ttu-id="bb54f-108">Hvis du vil initialisere detailkonfigurationen, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="bb54f-108">To initialize the retail configuration, follow these steps.</span></span>

1.  <span data-ttu-id="bb54f-109">Start Dynamics 365 for Retail-klienten.</span><span class="sxs-lookup"><span data-stu-id="bb54f-109">Start the Dynamics 365 for Retail client.</span></span>
2.  <span data-ttu-id="bb54f-110">Klik på **Detail** &gt; **Konfiguration af hovedkontor** &gt; **Parametre** &gt; **Detailparametre**.</span><span class="sxs-lookup"><span data-stu-id="bb54f-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3.  <span data-ttu-id="bb54f-111">Klik på **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="bb54f-111">Click **Initialize**.</span></span>

<span data-ttu-id="bb54f-112">Initialiseringen opretter følgende standardkonfigurationsdata:</span><span class="sxs-lookup"><span data-stu-id="bb54f-112">Initialization creates the following default configuration data:</span></span>

-   <span data-ttu-id="bb54f-113">Retail planlægger-job og -underjob</span><span class="sxs-lookup"><span data-stu-id="bb54f-113">Retail scheduler jobs and subjobs</span></span>
-   <span data-ttu-id="bb54f-114">Detailkanalskema</span><span class="sxs-lookup"><span data-stu-id="bb54f-114">Retail channel schema</span></span>
-   <span data-ttu-id="bb54f-115">Distributionstidsplaner for detail</span><span class="sxs-lookup"><span data-stu-id="bb54f-115">Retail distribution schedules</span></span>
-   <span data-ttu-id="bb54f-116">Standardskærmlayout, der indeholder knapmatrixer, billeder og temaer</span><span class="sxs-lookup"><span data-stu-id="bb54f-116">Default screen layouts, which include button grids, images, and themes</span></span>
-   <span data-ttu-id="bb54f-117">Oplysninger om tidszone</span><span class="sxs-lookup"><span data-stu-id="bb54f-117">Time zone information</span></span>
-   <span data-ttu-id="bb54f-118">POS-handlinger:</span><span class="sxs-lookup"><span data-stu-id="bb54f-118">Point-of-sale (POS) operations</span></span>
-   <span data-ttu-id="bb54f-119">POS-rettigheder</span><span class="sxs-lookup"><span data-stu-id="bb54f-119">POS permissions</span></span>
-   <span data-ttu-id="bb54f-120">Kanalrapporter</span><span class="sxs-lookup"><span data-stu-id="bb54f-120">Channel reports</span></span>
-   <span data-ttu-id="bb54f-121">Attributmetadata</span><span class="sxs-lookup"><span data-stu-id="bb54f-121">Attribute metadata</span></span>
-   <span data-ttu-id="bb54f-122">Skabeloner til validering af enheder</span><span class="sxs-lookup"><span data-stu-id="bb54f-122">Entity validation templates</span></span>
-   <span data-ttu-id="bb54f-123">Batchjob for at slette Commerce Data Exchange-sessionsoversigt</span><span class="sxs-lookup"><span data-stu-id="bb54f-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="bb54f-124">Derudover er logføring, der er relateret til betalingskortindustrien (PCI), aktiveret for Dynamics 365 for Retail-databasen.</span><span class="sxs-lookup"><span data-stu-id="bb54f-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span> <span data-ttu-id="bb54f-125">**Bemærk!** Der er en indstilling til at konfigurere Retail planlægger separat.</span><span class="sxs-lookup"><span data-stu-id="bb54f-125">**Note:** There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="bb54f-126">Denne indstilling gør det muligt at nulstille Retail planlægger-konfigurationen til dens standardindstillinger.</span><span class="sxs-lookup"><span data-stu-id="bb54f-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span> <span data-ttu-id="bb54f-127">Når initialiseringen er fuldført, skal du konfigurere yderligere detaildata.</span><span class="sxs-lookup"><span data-stu-id="bb54f-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="bb54f-128">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="bb54f-128">Here are some examples:</span></span>

-   <span data-ttu-id="bb54f-129">Detailparametre</span><span class="sxs-lookup"><span data-stu-id="bb54f-129">Retail parameters</span></span>
-   <span data-ttu-id="bb54f-130">Parametre for Retail planlægger</span><span class="sxs-lookup"><span data-stu-id="bb54f-130">Retail scheduler parameters</span></span>
-   <span data-ttu-id="bb54f-131">Detailkanaler</span><span class="sxs-lookup"><span data-stu-id="bb54f-131">Retail channels</span></span>
-   <span data-ttu-id="bb54f-132">Kasseapparater og enheder</span><span class="sxs-lookup"><span data-stu-id="bb54f-132">Registers and devices</span></span>
-   <span data-ttu-id="bb54f-133">Udvalg</span><span class="sxs-lookup"><span data-stu-id="bb54f-133">Assortments</span></span>





