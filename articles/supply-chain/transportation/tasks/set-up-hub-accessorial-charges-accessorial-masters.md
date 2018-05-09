--- 
title: "Konfigurere tillægsgebyrer og tilbehørsmastere for hub"
description: "Denne fremgangsmåde viser, hvordan du opretter en tillægsmaster for en hub og bruger denne master til at oprette et gebyr for hubtillæg."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 61a506b3824fa220d052ca667199edac526c1cbc
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="6255d-103">Konfigurere tillægsgebyrer og tilbehørsmastere for hub</span><span class="sxs-lookup"><span data-stu-id="6255d-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6255d-104">Denne fremgangsmåde viser, hvordan du opretter en tillægsmaster for en hub og bruger denne master til at oprette et gebyr for hubtillæg.</span><span class="sxs-lookup"><span data-stu-id="6255d-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="6255d-105">Proceduren bruger USMF-datasættet.</span><span class="sxs-lookup"><span data-stu-id="6255d-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="6255d-106">Denne konfiguration vil normalt blive udført af en transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="6255d-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="6255d-107">Konfigurer en hubmaster</span><span class="sxs-lookup"><span data-stu-id="6255d-107">Set up a hub master</span></span>
1. <span data-ttu-id="6255d-108">Gå til Transportstyring > Opsætning > Klassificering > Tilbehørsmastere.</span><span class="sxs-lookup"><span data-stu-id="6255d-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="6255d-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6255d-109">Click New.</span></span>
3. <span data-ttu-id="6255d-110">Skriv en værdi i feltet Tilbehørsmaster.</span><span class="sxs-lookup"><span data-stu-id="6255d-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="6255d-111">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6255d-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="6255d-112">Vælg "Hub" i feltet Tilbehørstype.</span><span class="sxs-lookup"><span data-stu-id="6255d-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="6255d-113">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="6255d-113">Click Save.</span></span>
7. <span data-ttu-id="6255d-114">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6255d-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="6255d-115">Konfigurer et gebyr for hubtillæg</span><span class="sxs-lookup"><span data-stu-id="6255d-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="6255d-116">Gå til Transportstyring > Opsætning > Klassificering > Gebyrer for hubtillæg.</span><span class="sxs-lookup"><span data-stu-id="6255d-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="6255d-117">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6255d-117">Click New.</span></span>
3. <span data-ttu-id="6255d-118">Indtast en værdi i feltet Id for hubtilbehør.</span><span class="sxs-lookup"><span data-stu-id="6255d-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="6255d-119">Klik på rullelisten i feltet Hub for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="6255d-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="6255d-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6255d-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="6255d-121">Vælg en indstilling i feltet Hubposition.</span><span class="sxs-lookup"><span data-stu-id="6255d-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="6255d-122">Du kan enten oprette gebyret som en afhentning eller levering.</span><span class="sxs-lookup"><span data-stu-id="6255d-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="6255d-123">Afhængigt af dit valg anvendes gebyret på det tilsvarende transportsegment på ruten.</span><span class="sxs-lookup"><span data-stu-id="6255d-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="6255d-124">Klik på rullelisten i feltet Tilbehørsmaster for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="6255d-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="6255d-125">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6255d-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6255d-126">Vælg den master, du lige oprettet.</span><span class="sxs-lookup"><span data-stu-id="6255d-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="6255d-127">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="6255d-127">Click Save.</span></span>
10. <span data-ttu-id="6255d-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6255d-128">Close the page.</span></span>


