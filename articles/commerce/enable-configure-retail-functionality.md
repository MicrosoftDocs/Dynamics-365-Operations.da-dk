---
title: Initialisere basisdata i nye Commerce-miljøer
description: I denne artikel beskrives de data, der er oprettet som en del af initialiseringen for Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a12bd7a178d8d40db8c919410a00fbf021625f50
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238744"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a><span data-ttu-id="10564-103">Initialisere basisdata i nye Commerce-miljøer</span><span class="sxs-lookup"><span data-stu-id="10564-103">Initialize seed data in new Commerce environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="10564-104">I denne artikel beskrives de data, der er oprettet som en del af initialiseringen for Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="10564-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="10564-105">Når Commerce-løsningen er blevet installeret via Microsoft Dynamics Lifecycle Services (LCS), skal du initialisere Commerce-konfigurationen for at oprette de grundlæggende konfigurationsdata.</span><span class="sxs-lookup"><span data-stu-id="10564-105">After the Commerce solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the Commerce configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10564-106">Før du initialiserer Commerce-konfigurationen, skal du kontrollere, at du har angivet et sprog og en postadresse for hver juridisk enhed, hvor du vil konfigurere butikker.</span><span class="sxs-lookup"><span data-stu-id="10564-106">Before you initialize the commerce configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up stores.</span></span> <span data-ttu-id="10564-107">Dette trin skal udføres for hver juridisk enhed, du bruger til handel.</span><span class="sxs-lookup"><span data-stu-id="10564-107">This step must be completed for each legal entity that you use for commerce.</span></span>

<span data-ttu-id="10564-108">Hvis du vil initialisere konfigurationen, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="10564-108">To initialize the configuration, follow these steps.</span></span>

1. <span data-ttu-id="10564-109">Start Commerce-klienten.</span><span class="sxs-lookup"><span data-stu-id="10564-109">Start the Commerce client.</span></span>
2. <span data-ttu-id="10564-110">Klik på **Retail og Commerce** &gt; **Konfiguration af hovedkontor** &gt; **Parametre** &gt; **Commerce-parametre**.</span><span class="sxs-lookup"><span data-stu-id="10564-110">Click **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
3. <span data-ttu-id="10564-111">Klik på **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="10564-111">Click **Initialize**.</span></span>

<span data-ttu-id="10564-112">Initialiseringen opretter følgende standardkonfigurationsdata:</span><span class="sxs-lookup"><span data-stu-id="10564-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="10564-113">Commerce planlæggerjob og -underjob</span><span class="sxs-lookup"><span data-stu-id="10564-113">Commerce scheduler jobs and subjobs</span></span>
- <span data-ttu-id="10564-114">Handelskanalskema</span><span class="sxs-lookup"><span data-stu-id="10564-114">Commerce channel schema</span></span>
- <span data-ttu-id="10564-115">Commerce-distributionstidsplaner</span><span class="sxs-lookup"><span data-stu-id="10564-115">Commerce distribution schedules</span></span>
- <span data-ttu-id="10564-116">Standardskærmlayout, der indeholder knapmatrixer, billeder og temaer</span><span class="sxs-lookup"><span data-stu-id="10564-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="10564-117">Oplysninger om tidszone</span><span class="sxs-lookup"><span data-stu-id="10564-117">Time zone information</span></span>
- <span data-ttu-id="10564-118">POS-handlinger:</span><span class="sxs-lookup"><span data-stu-id="10564-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="10564-119">POS-rettigheder</span><span class="sxs-lookup"><span data-stu-id="10564-119">POS permissions</span></span>
- <span data-ttu-id="10564-120">Kanalrapporter</span><span class="sxs-lookup"><span data-stu-id="10564-120">Channel reports</span></span>
- <span data-ttu-id="10564-121">Attributmetadata</span><span class="sxs-lookup"><span data-stu-id="10564-121">Attribute metadata</span></span>
- <span data-ttu-id="10564-122">Skabeloner til validering af enheder</span><span class="sxs-lookup"><span data-stu-id="10564-122">Entity validation templates</span></span>
- <span data-ttu-id="10564-123">Batchjob til fjernelse af Commerce Data Exchange-sessionshistorik</span><span class="sxs-lookup"><span data-stu-id="10564-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="10564-124">Derudover er logføring, der er relateret til betalingskortindustrien (PCI), aktiveret for Commerce-databasen.</span><span class="sxs-lookup"><span data-stu-id="10564-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Commerce database.</span></span>

> [!NOTE]
> <span data-ttu-id="10564-125">Der er en indstilling til at konfigurere Commerce-planlægger separat.</span><span class="sxs-lookup"><span data-stu-id="10564-125">There is an option to separately configure the Commerce scheduler.</span></span> <span data-ttu-id="10564-126">Denne indstilling gør det muligt at nulstille Commerce-planlæggerkonfigurationen til dens standardindstillinger.</span><span class="sxs-lookup"><span data-stu-id="10564-126">This option lets you reset the Commerce scheduler configuration to its default settings.</span></span>

<span data-ttu-id="10564-127">Når initialiseringen er fuldført, skal du konfigurere yderligere handelsdata.</span><span class="sxs-lookup"><span data-stu-id="10564-127">After initialization is completed, you must configure additional commerce data.</span></span> <span data-ttu-id="10564-128">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="10564-128">Here are some examples:</span></span>

- <span data-ttu-id="10564-129">Handelsparametre</span><span class="sxs-lookup"><span data-stu-id="10564-129">Commerce parameters</span></span>
- <span data-ttu-id="10564-130">Parametre for handelsplanlægger</span><span class="sxs-lookup"><span data-stu-id="10564-130">Commerce scheduler parameters</span></span>
- <span data-ttu-id="10564-131">Handelskanaler</span><span class="sxs-lookup"><span data-stu-id="10564-131">Commerce channels</span></span>
- <span data-ttu-id="10564-132">Kasseapparater og enheder</span><span class="sxs-lookup"><span data-stu-id="10564-132">Registers and devices</span></span>
- <span data-ttu-id="10564-133">Udvalg</span><span class="sxs-lookup"><span data-stu-id="10564-133">Assortments</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]