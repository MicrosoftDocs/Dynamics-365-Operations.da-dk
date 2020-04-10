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
ms.openlocfilehash: 7be50eba098b7b28594c8e18c721579f4bb2e879
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140985"
---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="a99e6-103"> Oprette økonomiske dimensioner for POS-kasseapparater og konfigurere dimensionsværdier for registre</span><span class="sxs-lookup"><span data-stu-id="a99e6-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a99e6-104">Denne procedure hjælper med at oprette økonomiske dimensioner for POS-kasseapparater og demonstrerer, hvordan du konfigurerer økonomiske dimensionsværdier for kasseapparaterne.</span><span class="sxs-lookup"><span data-stu-id="a99e6-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="a99e6-105">Proceduren indeholder ikke andre relaterede trin, f.eks. oprettelse af dimensionssæt og kontostrukturer.</span><span class="sxs-lookup"><span data-stu-id="a99e6-105">This procedure doesn't include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="a99e6-106">Disse opgaver findes i andre emner.</span><span class="sxs-lookup"><span data-stu-id="a99e6-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="a99e6-107">Denne registrering anvender demofirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="a99e6-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="a99e6-108">Gå til Finans > Kontoplan > Dimensioner > Økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="a99e6-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="a99e6-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a99e6-109">Click New.</span></span>
3. <span data-ttu-id="a99e6-110">Vælg en indstilling i feltet Brug værdier fra.</span><span class="sxs-lookup"><span data-stu-id="a99e6-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="a99e6-111">Skriv en værdi i feltet Dimensionsnavn.</span><span class="sxs-lookup"><span data-stu-id="a99e6-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="a99e6-112">Klik på Aktiver.</span><span class="sxs-lookup"><span data-stu-id="a99e6-112">Click Activate.</span></span>
6. <span data-ttu-id="a99e6-113">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="a99e6-113">Click Close.</span></span>
7. <span data-ttu-id="a99e6-114">Klik på Aktiver.</span><span class="sxs-lookup"><span data-stu-id="a99e6-114">Click Activate.</span></span>
8. <span data-ttu-id="a99e6-115">Klik på Dimensionsværdier.</span><span class="sxs-lookup"><span data-stu-id="a99e6-115">Click Dimension values.</span></span>
9. <span data-ttu-id="a99e6-116">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a99e6-116">Close the page.</span></span>
10. <span data-ttu-id="a99e6-117">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a99e6-117">Click Save.</span></span>
11. <span data-ttu-id="a99e6-118">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a99e6-118">Close the page.</span></span>
12. <span data-ttu-id="a99e6-119">Gå til Retail og Commerce> Konfiguration af kanal > POS-opsætning > Kasseapparater.</span><span class="sxs-lookup"><span data-stu-id="a99e6-119">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="a99e6-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="a99e6-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="a99e6-121">Slå udvidelsen af sektionen Økonomiske dimensioner til/fra.</span><span class="sxs-lookup"><span data-stu-id="a99e6-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="a99e6-122">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="a99e6-122">Click Edit.</span></span>
16. <span data-ttu-id="a99e6-123">Klik på rullelisten i feltet Terminal for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a99e6-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="a99e6-124">Find og vælg på listen dimensionsværdien for kasseapparatet, der opdateres.</span><span class="sxs-lookup"><span data-stu-id="a99e6-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="a99e6-125">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a99e6-125">Click Save.</span></span>

