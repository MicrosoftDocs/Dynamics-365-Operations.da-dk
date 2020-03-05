---
title: " Oprette økonomiske dimensioner for POS-kasseapparater og konfigurere dimensionsværdier for registre"
description: Denne procedure hjælper med at oprette økonomiske dimensioner for POS-kasseapparater og demonstrerer, hvordan du konfigurerer økonomiske dimensionsværdier for kasseapparaterne.
author: jashanno
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e04af04de3d18d375ce3609ab4cd53f652c2fbc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022000"
---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="bcde5-103"> Oprette økonomiske dimensioner for POS-kasseapparater og konfigurere dimensionsværdier for registre</span><span class="sxs-lookup"><span data-stu-id="bcde5-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="bcde5-104">Denne procedure hjælper med at oprette økonomiske dimensioner for POS-kasseapparater og demonstrerer, hvordan du konfigurerer økonomiske dimensionsværdier for kasseapparaterne.</span><span class="sxs-lookup"><span data-stu-id="bcde5-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="bcde5-105">Proceduren indeholder ikke andre relaterede trin, f.eks. oprettelse af dimensionssæt og kontostrukturer.</span><span class="sxs-lookup"><span data-stu-id="bcde5-105">This procedure doesn’t include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="bcde5-106">Disse opgaver findes i andre emner.</span><span class="sxs-lookup"><span data-stu-id="bcde5-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="bcde5-107">Denne registrering anvender demofirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="bcde5-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="bcde5-108">Gå til Finans > Kontoplan > Dimensioner > Økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="bcde5-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="bcde5-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="bcde5-109">Click New.</span></span>
3. <span data-ttu-id="bcde5-110">Vælg en indstilling i feltet Brug værdier fra.</span><span class="sxs-lookup"><span data-stu-id="bcde5-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="bcde5-111">Skriv en værdi i feltet Dimensionsnavn.</span><span class="sxs-lookup"><span data-stu-id="bcde5-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="bcde5-112">Klik på Aktiver.</span><span class="sxs-lookup"><span data-stu-id="bcde5-112">Click Activate.</span></span>
6. <span data-ttu-id="bcde5-113">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="bcde5-113">Click Close.</span></span>
7. <span data-ttu-id="bcde5-114">Klik på Aktiver.</span><span class="sxs-lookup"><span data-stu-id="bcde5-114">Click Activate.</span></span>
8. <span data-ttu-id="bcde5-115">Klik på Dimensionsværdier.</span><span class="sxs-lookup"><span data-stu-id="bcde5-115">Click Dimension values.</span></span>
9. <span data-ttu-id="bcde5-116">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bcde5-116">Close the page.</span></span>
10. <span data-ttu-id="bcde5-117">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="bcde5-117">Click Save.</span></span>
11. <span data-ttu-id="bcde5-118">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bcde5-118">Close the page.</span></span>
12. <span data-ttu-id="bcde5-119">Gå til Retail og Commerce> Konfiguration af kanal > POS-opsætning > Kasseapparater.</span><span class="sxs-lookup"><span data-stu-id="bcde5-119">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="bcde5-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="bcde5-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="bcde5-121">Slå udvidelsen af sektionen Økonomiske dimensioner til/fra.</span><span class="sxs-lookup"><span data-stu-id="bcde5-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="bcde5-122">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="bcde5-122">Click Edit.</span></span>
16. <span data-ttu-id="bcde5-123">Klik på rullelisten i feltet Terminal for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="bcde5-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="bcde5-124">Find og vælg på listen dimensionsværdien for kasseapparatet, der opdateres.</span><span class="sxs-lookup"><span data-stu-id="bcde5-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="bcde5-125">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="bcde5-125">Click Save.</span></span>
