--- 
title: "Konfigurere tillægstildelinger"
description: "Denne procedure viser, hvordan du opretter en tilbehørstildeling."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 31787aa180639b934b837b98dc170070d33fd56f
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-accessorial-assignments"></a><span data-ttu-id="5c929-103">Konfigurere tillægstildelinger</span><span class="sxs-lookup"><span data-stu-id="5c929-103">Set up accessorial assignments</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5c929-104">Denne procedure viser, hvordan du opretter en tilbehørstildeling.</span><span class="sxs-lookup"><span data-stu-id="5c929-104">This procedure shows how to set up an accessorial assignment.</span></span> <span data-ttu-id="5c929-105">Denne konfiguration vil normalt blive udført af en transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="5c929-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="5c929-106">Før du kan bruge denne vejledning skal du køre guiden "Konfigurer gebyrer for hubtillæg og tillægsmastere".</span><span class="sxs-lookup"><span data-stu-id="5c929-106">Before you use this guide you need to run the "Set up hub accessorial charges and accessorial masters" guide.</span></span>


## <a name="set-up-accessorial-assignment"></a><span data-ttu-id="5c929-107">Konfigurer Tilbehørstildeling</span><span class="sxs-lookup"><span data-stu-id="5c929-107">Set up Accessorial assignment</span></span>
1. <span data-ttu-id="5c929-108">Gå til Transportstyring > Opsætning > Klassificering > Tildelinger af tillæg.</span><span class="sxs-lookup"><span data-stu-id="5c929-108">Go to Transportation management > Setup > Rating > Accessorial assignments.</span></span>
2. <span data-ttu-id="5c929-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="5c929-109">Click New.</span></span>
3. <span data-ttu-id="5c929-110">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="5c929-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="5c929-111">Slå udvidelsen af sektionen afsnittet Detaljer til/fra.</span><span class="sxs-lookup"><span data-stu-id="5c929-111">Toggle the expansion of the Details section.</span></span>
5. <span data-ttu-id="5c929-112">Klik på rullelisten i feltet Hub for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="5c929-112">In the Hub field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="5c929-113">Vælg den pågældende Hub, du har oprettet en tillægsmaster for, når du har kørt guiden "Konfigurer gebyrer for hubtillæg og tillægsmastere" på listen.</span><span class="sxs-lookup"><span data-stu-id="5c929-113">In the list, select the Hub that you created an accessorial master for when you ran the "Set up hub accessorial charges and accessorial masters" guide.</span></span> 
7. <span data-ttu-id="5c929-114">Klik på rullelisten i feltet Id for hubtilbehør for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="5c929-114">In the Hub accessorial ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="5c929-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="5c929-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="5c929-116">Slå udvidelsen af Sektionen Kriterier til/fra.</span><span class="sxs-lookup"><span data-stu-id="5c929-116">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="5c929-117">I sektionen Kriterier kan du vælge de nøjagtige kriterier for, hvornår gebyret skal gælde, baseret på de forskellige værdier, der tilbydes her.</span><span class="sxs-lookup"><span data-stu-id="5c929-117">In the Criteria section you can choose the exact criteria for when the charge should apply, based on the different values offered here.</span></span>  
10. <span data-ttu-id="5c929-118">Angiv indstillingen Anvend altid til Ja.</span><span class="sxs-lookup"><span data-stu-id="5c929-118">Set the Always apply option to Yes.</span></span>
11. <span data-ttu-id="5c929-119">Vælg en indstilling i feltet Tilbehørstildelingsniveau.</span><span class="sxs-lookup"><span data-stu-id="5c929-119">In the Accessorial assignment level field, select an option.</span></span>
12. <span data-ttu-id="5c929-120">Slå udvidelsen af sektionen Beregning til/fra.</span><span class="sxs-lookup"><span data-stu-id="5c929-120">Toggle the expansion of the Calculation section.</span></span>
13. <span data-ttu-id="5c929-121">Vælg "Fast" i feltet Gebyrtype for tillæg.</span><span class="sxs-lookup"><span data-stu-id="5c929-121">In the Accessorial fee type field, select 'Flat'.</span></span>
    * <span data-ttu-id="5c929-122">Gebyrtype for tillæg bestemmer, hvordan det faktiske gebyr beregnes.</span><span class="sxs-lookup"><span data-stu-id="5c929-122">The Accessorial fee type determines how to calculate the actual charge.</span></span> <span data-ttu-id="5c929-123">I dette eksempel er det et fast gebyr.</span><span class="sxs-lookup"><span data-stu-id="5c929-123">In this example it's a flat charge.</span></span>  
14. <span data-ttu-id="5c929-124">Angiv et tal i feltet Gebyr for tillæg.</span><span class="sxs-lookup"><span data-stu-id="5c929-124">In the Accessorial fee field, enter a number.</span></span>
15. <span data-ttu-id="5c929-125">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="5c929-125">Click Save.</span></span>


