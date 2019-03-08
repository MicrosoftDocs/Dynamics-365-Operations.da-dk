---
title: Konfigurere tillægsgebyrer og tilbehørsmastere for hub
description: Denne fremgangsmåde viser, hvordan du opretter en tillægsmaster for en hub og bruger denne master til at oprette et gebyr for hubtillæg.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9959c20f9a8fd07cbf0cfd76f7760b44d7b5cae1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "331891"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="da018-103">Konfigurere tillægsgebyrer og tilbehørsmastere for hub</span><span class="sxs-lookup"><span data-stu-id="da018-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da018-104">Denne fremgangsmåde viser, hvordan du opretter en tillægsmaster for en hub og bruger denne master til at oprette et gebyr for hubtillæg.</span><span class="sxs-lookup"><span data-stu-id="da018-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="da018-105">Proceduren bruger USMF-datasættet.</span><span class="sxs-lookup"><span data-stu-id="da018-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="da018-106">Denne konfiguration vil normalt blive udført af en transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="da018-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="da018-107">Konfigurer en hubmaster</span><span class="sxs-lookup"><span data-stu-id="da018-107">Set up a hub master</span></span>
1. <span data-ttu-id="da018-108">Gå til Transportstyring > Opsætning > Klassificering > Tilbehørsmastere.</span><span class="sxs-lookup"><span data-stu-id="da018-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="da018-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="da018-109">Click New.</span></span>
3. <span data-ttu-id="da018-110">Skriv en værdi i feltet Tilbehørsmaster.</span><span class="sxs-lookup"><span data-stu-id="da018-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="da018-111">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="da018-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="da018-112">Vælg "Hub" i feltet Tilbehørstype.</span><span class="sxs-lookup"><span data-stu-id="da018-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="da018-113">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="da018-113">Click Save.</span></span>
7. <span data-ttu-id="da018-114">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="da018-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="da018-115">Konfigurer et gebyr for hubtillæg</span><span class="sxs-lookup"><span data-stu-id="da018-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="da018-116">Gå til Transportstyring > Opsætning > Klassificering > Gebyrer for hubtillæg.</span><span class="sxs-lookup"><span data-stu-id="da018-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="da018-117">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="da018-117">Click New.</span></span>
3. <span data-ttu-id="da018-118">Indtast en værdi i feltet Id for hubtilbehør.</span><span class="sxs-lookup"><span data-stu-id="da018-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="da018-119">Klik på rullelisten i feltet Hub for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="da018-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="da018-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="da018-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="da018-121">Vælg en indstilling i feltet Hubposition.</span><span class="sxs-lookup"><span data-stu-id="da018-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="da018-122">Du kan enten oprette gebyret som en afhentning eller levering.</span><span class="sxs-lookup"><span data-stu-id="da018-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="da018-123">Afhængigt af dit valg anvendes gebyret på det tilsvarende transportsegment på ruten.</span><span class="sxs-lookup"><span data-stu-id="da018-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="da018-124">Klik på rullelisten i feltet Tilbehørsmaster for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="da018-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="da018-125">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="da018-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="da018-126">Vælg den master, du lige oprettet.</span><span class="sxs-lookup"><span data-stu-id="da018-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="da018-127">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="da018-127">Click Save.</span></span>
10. <span data-ttu-id="da018-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="da018-128">Close the page.</span></span>

