---
title: " Konfigurere regler og parametre for cross-docking og centraliseret indkøb"
description: Denne procedure viser trinnene til oprettelse af opfyldningsregler.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d4cd276283483340f1dc0bc995cc9073a8aa9c0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232683"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="e40f6-103"> Konfigurere regler og parametre for cross-docking og centraliseret indkøb</span><span class="sxs-lookup"><span data-stu-id="e40f6-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e40f6-104">Denne procedure viser trinnene til oprettelse af opfyldningsregler.</span><span class="sxs-lookup"><span data-stu-id="e40f6-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="e40f6-105">Opfyldningsregler kan bruges til at styre, hvordan produkter fordeles til butikkerne, når du bruger cross-docking og bestilling efter ordre.</span><span class="sxs-lookup"><span data-stu-id="e40f6-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="e40f6-106">Opfyldningsregler kan konfigureres til butikker eller butiksgrupper.</span><span class="sxs-lookup"><span data-stu-id="e40f6-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="e40f6-107">Den vægt, der er defineret for hver linje i en regel, bestemmer, hvordan mængderne af produkter vil blive fordelt mellem butikkerne, når der bruges opfyldningsregler som fordelingsmetode i cross-docking eller bestilling efter ordre.</span><span class="sxs-lookup"><span data-stu-id="e40f6-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="e40f6-108">Denne procedure bruger demofirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="e40f6-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="e40f6-109">Gå til Opfyldningsregler.</span><span class="sxs-lookup"><span data-stu-id="e40f6-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="e40f6-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e40f6-110">Click New.</span></span>
3. <span data-ttu-id="e40f6-111">Skriv en værdi i feltet Opfyldningsregel.</span><span class="sxs-lookup"><span data-stu-id="e40f6-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="e40f6-112">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e40f6-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e40f6-113">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e40f6-113">Click Save.</span></span>
6. <span data-ttu-id="e40f6-114">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="e40f6-114">Click Add.</span></span>
7. <span data-ttu-id="e40f6-115">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e40f6-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e40f6-116">Du kan vælge Opfyldningshierarki eller Kanal som typen.</span><span class="sxs-lookup"><span data-stu-id="e40f6-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="e40f6-117">Værdien kontrollerer, om valget i Navn vil være et hierarki af kanaler eller en bestemt kanal.</span><span class="sxs-lookup"><span data-stu-id="e40f6-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="e40f6-118">I dette eksempel skal lade den være angivet som Opfyldningshierarki.</span><span class="sxs-lookup"><span data-stu-id="e40f6-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="e40f6-119">Vælg en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e40f6-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="e40f6-120">Standardvægtværdien udfyldes fra den vægt, der er defineret for lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="e40f6-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="e40f6-121">Denne vægt kan bruges til opfyldningsreglen, eller du kan angive en ny vægt i feltet Vægt.</span><span class="sxs-lookup"><span data-stu-id="e40f6-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="e40f6-122">Angiv et tal i feltet Vægt.</span><span class="sxs-lookup"><span data-stu-id="e40f6-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="e40f6-123">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="e40f6-123">Click Add.</span></span>
11. <span data-ttu-id="e40f6-124">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e40f6-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="e40f6-125">Vælg "Kanal" i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="e40f6-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="e40f6-126">Indtast eller vælg en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e40f6-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="e40f6-127">Angiv et tal i feltet Vægt.</span><span class="sxs-lookup"><span data-stu-id="e40f6-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="e40f6-128">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e40f6-128">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]