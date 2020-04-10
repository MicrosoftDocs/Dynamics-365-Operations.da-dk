---
title: Konfigurere dispositionskoder
description: Denne fremgangsmåde fokuserer på oprettelsen af en dispositionskode, der kan bruges på en mobil enhed for returordren modtager proces.
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
ms.openlocfilehash: ec353ecffdc457e1502cfad24e7a50ae31048647
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146048"
---
# <a name="set-up-dispositions-codes"></a><span data-ttu-id="3a0af-103">Konfigurere dispositionskoder</span><span class="sxs-lookup"><span data-stu-id="3a0af-103">Set up dispositions codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3a0af-104">Denne fremgangsmåde fokuserer på oprettelsen af en dispositionskode, der kan bruges på en mobil enhed for returordren modtager proces.</span><span class="sxs-lookup"><span data-stu-id="3a0af-104">This procedure focuses on the setup of a disposition code that can be used on a mobile device for the return order receiving process.</span></span> <span data-ttu-id="3a0af-105">Dispositionskoder er en samling regler, der kan bruges, når der modtages varer.</span><span class="sxs-lookup"><span data-stu-id="3a0af-105">Disposition codes are a collection of rules that can be used when items are received.</span></span> <span data-ttu-id="3a0af-106">For eksempel når en arbejder bruger en mobilenhed til at modtage varer, der blev beskadiget, skal brugeren scanne en dispositionskode for beskadigede varer.</span><span class="sxs-lookup"><span data-stu-id="3a0af-106">For example, when a work user uses a mobile device to receive items that were damaged, the user must scan a disposition code for damaged items.</span></span> <span data-ttu-id="3a0af-107">Lagerstatus for varerne, der modtages, skabelonen arbejde og direktivet placering kan bestemmes ud fra den scannede dispositionskode.</span><span class="sxs-lookup"><span data-stu-id="3a0af-107">The inventory status of the goods received, the work template, and the location directive can be determined from the scanned disposition code.</span></span> <span data-ttu-id="3a0af-108">For den indkøbsordre, der er modtaget proces og rapporten produktion ordre som færdig proces, er brugen af en dispositionskode valgfrit.</span><span class="sxs-lookup"><span data-stu-id="3a0af-108">For the purchase order receiving process and the production order report as finished process, the use of a disposition code is optional.</span></span> <span data-ttu-id="3a0af-109">For salgsordren modtagende returvareprocessen, hvis varerne er registreret ved hjælp af en mobil enhed, er brug af dispositionskoden obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="3a0af-109">For the sales order return receiving process, if the items are registered using a mobile device, the use of disposition code is mandatory.</span></span>  <span data-ttu-id="3a0af-110">Denne vejledning blev oprettet ved hjælp af demodatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="3a0af-110">This guide was created using the demo data company USMF.</span></span> <span data-ttu-id="3a0af-111">Denne procedure er beregnet til lagerchefen.</span><span class="sxs-lookup"><span data-stu-id="3a0af-111">This procedure is intended for the warehouse manager.</span></span> 

1. <span data-ttu-id="3a0af-112">Gå til Lagerstyring > Opsætning > Mobilenhed > Dispositionskoder.</span><span class="sxs-lookup"><span data-stu-id="3a0af-112">Go to Warehouse management > Setup > Mobile device > Disposition codes.</span></span>
2. <span data-ttu-id="3a0af-113">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3a0af-113">Click New.</span></span>
    * <span data-ttu-id="3a0af-114">Opret en ny dispositionskode til brug til returneringer fra debitorer.</span><span class="sxs-lookup"><span data-stu-id="3a0af-114">Create a new disposition code to use for customer returns.</span></span>  
3. <span data-ttu-id="3a0af-115">Indtast en værdi i feltet Dispositionskode.</span><span class="sxs-lookup"><span data-stu-id="3a0af-115">In the Disposition code field, type a value.</span></span>
4. <span data-ttu-id="3a0af-116">Vælg en lagerstatus i feltet Lagerstatus, hvis der er en lagerblokering.</span><span class="sxs-lookup"><span data-stu-id="3a0af-116">In the Inventory status field, select an inventory status where there is inventory blocking.</span></span>
    * <span data-ttu-id="3a0af-117">Hvis du bruger USMF, skal du markere "Spærring".</span><span class="sxs-lookup"><span data-stu-id="3a0af-117">If you're using USMF, select 'Blocking'.</span></span> <span data-ttu-id="3a0af-118">Du kan føje en lagerstatus til dispositionskoden for at tilsidesætte den standardstatus, der er på ordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="3a0af-118">You can add an inventory status to the disposition code to override the default status that's on the order lines.</span></span>  
5. <span data-ttu-id="3a0af-119">Indtast en værdi i feltet Arbejdsskabelon.</span><span class="sxs-lookup"><span data-stu-id="3a0af-119">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="3a0af-120">Valgfrit: Vælg en skabelonkode, der er tilknyttet en returordre.</span><span class="sxs-lookup"><span data-stu-id="3a0af-120">Optional: Select a work template code that is associated with a return order.</span></span> <span data-ttu-id="3a0af-121">Hvis ingen værdi er angivet, kan skabelonen arbejde vil blive løst ved hjælp af standardregler, der er konfigureret i systemet.</span><span class="sxs-lookup"><span data-stu-id="3a0af-121">If no value is provided, the work template will be resolved using the standard rules configured in your system.</span></span> <span data-ttu-id="3a0af-122">At vælge en skabelon til arbejde vil begrænse denne dispositionskode kan bruges sammen med processerne.</span><span class="sxs-lookup"><span data-stu-id="3a0af-122">Selecting a work template will limit the processes this disposition code can be used with.</span></span> <span data-ttu-id="3a0af-123">For eksempel, hvis en dispositionskode har en arbejde-skabelon med en arbejdsordre af typen indkøbsordre, kan den ikke bruges til at registrere varer, der returneres af kunder.</span><span class="sxs-lookup"><span data-stu-id="3a0af-123">For example, if a disposition code has a work template with a work order of type purchase order, it can't be used to register items that are returned by customers.</span></span>  
6. <span data-ttu-id="3a0af-124">Indtast en værdi i feltet Returdispositionskode.</span><span class="sxs-lookup"><span data-stu-id="3a0af-124">In the Return disposition code field, type a value.</span></span>
    * <span data-ttu-id="3a0af-125">Returdispositionskoden bestemmer resten af returordreprocessen for de varer, der er registreret.</span><span class="sxs-lookup"><span data-stu-id="3a0af-125">The return disposition code determines the remainder of the return order process for the items registered.</span></span> <span data-ttu-id="3a0af-126">I dette eksempel bør debitoren modtage en kreditnota.</span><span class="sxs-lookup"><span data-stu-id="3a0af-126">In this example, the customer should receive a credit note.</span></span> <span data-ttu-id="3a0af-127">Tilføj en returdispositionskode, der indeholder handlingen Kredit.</span><span class="sxs-lookup"><span data-stu-id="3a0af-127">Add a returns disposition code that contains an action Credit.</span></span>  

