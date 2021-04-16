---
title: Konfigurere tillægsgebyrer og tilbehørsmastere for hub
description: Denne fremgangsmåde viser, hvordan du opretter en tillægsmaster for en hub og bruger denne master til at oprette et gebyr for hubtillæg.
author: ShylaThompson
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f4c0d3af96e6ef6735b01165a49c1450b3b633b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837555"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="da7e6-103">Konfigurere tillægsgebyrer og tilbehørsmastere for hub</span><span class="sxs-lookup"><span data-stu-id="da7e6-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="da7e6-104">Denne fremgangsmåde viser, hvordan du opretter en tillægsmaster for en hub og bruger denne master til at oprette et gebyr for hubtillæg.</span><span class="sxs-lookup"><span data-stu-id="da7e6-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="da7e6-105">Proceduren bruger USMF-datasættet.</span><span class="sxs-lookup"><span data-stu-id="da7e6-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="da7e6-106">Denne konfiguration vil normalt blive udført af en transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="da7e6-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="da7e6-107">Konfigurer en hubmaster</span><span class="sxs-lookup"><span data-stu-id="da7e6-107">Set up a hub master</span></span>
1. <span data-ttu-id="da7e6-108">Gå til Transportstyring > Opsætning > Klassificering > Tilbehørsmastere.</span><span class="sxs-lookup"><span data-stu-id="da7e6-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="da7e6-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="da7e6-109">Click New.</span></span>
3. <span data-ttu-id="da7e6-110">Skriv en værdi i feltet Tilbehørsmaster.</span><span class="sxs-lookup"><span data-stu-id="da7e6-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="da7e6-111">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="da7e6-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="da7e6-112">Vælg "Hub" i feltet Tilbehørstype.</span><span class="sxs-lookup"><span data-stu-id="da7e6-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="da7e6-113">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="da7e6-113">Click Save.</span></span>
7. <span data-ttu-id="da7e6-114">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="da7e6-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="da7e6-115">Konfigurer et gebyr for hubtillæg</span><span class="sxs-lookup"><span data-stu-id="da7e6-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="da7e6-116">Gå til Transportstyring > Opsætning > Klassificering > Gebyrer for hubtillæg.</span><span class="sxs-lookup"><span data-stu-id="da7e6-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="da7e6-117">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="da7e6-117">Click New.</span></span>
3. <span data-ttu-id="da7e6-118">Indtast en værdi i feltet Id for hubtilbehør.</span><span class="sxs-lookup"><span data-stu-id="da7e6-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="da7e6-119">Klik på rullelisten i feltet Hub for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="da7e6-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="da7e6-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="da7e6-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="da7e6-121">Vælg en indstilling i feltet Hubposition.</span><span class="sxs-lookup"><span data-stu-id="da7e6-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="da7e6-122">Du kan enten oprette gebyret som en afhentning eller levering.</span><span class="sxs-lookup"><span data-stu-id="da7e6-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="da7e6-123">Afhængigt af dit valg anvendes gebyret på det tilsvarende transportsegment på ruten.</span><span class="sxs-lookup"><span data-stu-id="da7e6-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="da7e6-124">Klik på rullelisten i feltet Tilbehørsmaster for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="da7e6-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="da7e6-125">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="da7e6-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="da7e6-126">Vælg den master, du lige oprettet.</span><span class="sxs-lookup"><span data-stu-id="da7e6-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="da7e6-127">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="da7e6-127">Click Save.</span></span>
10. <span data-ttu-id="da7e6-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="da7e6-128">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]