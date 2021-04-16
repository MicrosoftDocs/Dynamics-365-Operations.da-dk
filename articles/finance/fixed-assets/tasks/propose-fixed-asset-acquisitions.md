---
title: Foreslå anskaffelser af anlægsaktiver
description: I dette emne beskrives, hvordan du henter et anlægsaktiv ved hjælp af anskaffelsesforslaget i Anlægsaktivkladden.
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d529cd53b41827a78b282afd4d2c69d2f2db555e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817154"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="3a5cc-103">Foreslå anskaffelser af anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="3a5cc-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3a5cc-104">I dette emne beskrives, hvordan du henter et anlægsaktiv ved hjælp af anskaffelsesforslaget i Anlægsaktivkladden.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="3a5cc-105">Den bruger rollen Revisor og demodata for den juridiske enhed USMF.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="3a5cc-106">Hvis du vil erhverve et anlægsaktiv via en forslagskladde, skal du først oprette anlægsaktivposten og derefter definere anskaffelsesprisen i anlægskartoteket.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

## <a name="create-an-asset-acquisition-proposal"></a><span data-ttu-id="3a5cc-107">Oprette et forslag til anskaffelse af aktiver</span><span class="sxs-lookup"><span data-stu-id="3a5cc-107">Create an asset acquisition proposal</span></span>

<span data-ttu-id="3a5cc-108">Gennemfør følgende trin for at oprette et forslag til anskaffelse af et aktiv.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-108">Complete the following steps to create an asset acquisition proposal.</span></span> 

1. <span data-ttu-id="3a5cc-109">I navigationsruden skal du gå til **Moduler > Anlægsaktiver > Kladdeposteringer > Anlægsaktivkladde**.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-109">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="3a5cc-110">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-110">Select **New**.</span></span>
3. <span data-ttu-id="3a5cc-111">Indtast eller vælg en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="3a5cc-112">Gå til handlingsruden, og vælg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-112">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="3a5cc-113">Vælg **Forslag**.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-113">Select **Proposals**.</span></span>
6. <span data-ttu-id="3a5cc-114">Vælg **Anskaffelsesforslag**.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-114">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="3a5cc-115">Vælg **Filter**.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-115">Select **Filter**.</span></span> <span data-ttu-id="3a5cc-116">Vælg **Nulstil** for at rydde tidligere værdier.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-116">Select **Reset** to clear previous values.</span></span>
8. <span data-ttu-id="3a5cc-117">Vælg rækken **Anlægsaktivnummer**.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-117">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="3a5cc-118">Indtast eller vælg en værdi i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-118">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="3a5cc-119">Angiv de resterende kriterier for anlægsaktiverne, du vil hente med dette forslag.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-119">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="3a5cc-120">Vælg **OK** to gange for at forlade ruden.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-120">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="3a5cc-121">Bekræft, at transaktionslinjerne er oprettet.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-121">Verify that the transaction lines are created.</span></span>  
- <span data-ttu-id="3a5cc-122">Kun anlægsaktiver med anskaffelsesdatoen og anskaffelsesprisen angivet i bogen medtages i anskaffelsesforslaget.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-122">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="3a5cc-123">Vælg fanen **Bøger** på siden.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-123">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="3a5cc-124">Vælg **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-124">Select **Post**.</span></span>

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a><span data-ttu-id="3a5cc-125">Medtage økonomiske standarddimensioner i et anskaffelsesforslag</span><span class="sxs-lookup"><span data-stu-id="3a5cc-125">Include default financial dimensions in an acquisition proposal</span></span>

<span data-ttu-id="3a5cc-126">Anskaffelsestransaktionen kan oprettes ved hjælp af tilføjelsesprogrammet Excel ved at gå til **Anlægsaktiver > Kladdeposteringer > Anlægsaktivkladde**.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-126">The acquisition transaction can be created using Excel add-ins, by going to **Fixed assets > Journal entries > Fixed asset journal**.</span></span> <span data-ttu-id="3a5cc-127">Opret en ny kladde, og flyt til sektionen **Linjer** på siden, vælg Excel-ikonet, og vælg derefter en kladdelinje for anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-127">Create a new journal and move to the **Lines** section on the page and select the Excel icon, and then select a Fixed asset journal line.</span></span> <span data-ttu-id="3a5cc-128">Systemet opretter og åbner en Excel-skabelon, der repræsenterer kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-128">The system will create and open an Excel template representing journal lines.</span></span> <span data-ttu-id="3a5cc-129">Du kan føje data til de kladdelinjer, du føjer til skabelonen, og derefter publicere disse oplysninger tilbage i systemet.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-129">You can add data for the journal lines you're adding into the template, and then publish that information back into the system.</span></span> 

<span data-ttu-id="3a5cc-130">Hvis der er konfigureret standarddimensioner for det valgte anlægskartotek og de tilsvarende anlægsaktiver, der er angivet i Excel-skabelonen, vil de økonomiske standarddimensioner blive kaldt fra masterdata i anlægskartoteket, når kladden publiceres fra Excel til systemet.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-130">If default dimensions have been set up for the selected asset book and the corresponding fixed assets that were entered in the Excel template, the default financial dimensions will be called from the asset book master data when the journal is published from the Excel to the system.</span></span> <span data-ttu-id="3a5cc-131">Hvis der automatisk skal indgå økonomiske dimensioner i et anlægskartotek, når anlægsaktivkladden udgives fra tilføjelsesprogrammet Excel, skal standarddimensionerne være konfigureret på forhånd.</span><span class="sxs-lookup"><span data-stu-id="3a5cc-131">To include financial dimensions on an asset book automatically while publishing the fixed asset journal from the Excel add-in, the default dimensions must be set up in advance.</span></span>  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
