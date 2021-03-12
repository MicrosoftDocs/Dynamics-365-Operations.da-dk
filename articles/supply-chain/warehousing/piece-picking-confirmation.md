---
title: Bekræftelse af stykplukning
description: I dette emne beskrives, hvordan du kan konfigurere og anvende bekræftelse af stykplukning fra en mobilenhed.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66903d142ecb7228e4fdec56dbd45472acbdeb69
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989637"
---
# <a name="piece-picking-confirmation"></a><span data-ttu-id="fbe6b-103">Bekræftelse af stykplukning</span><span class="sxs-lookup"><span data-stu-id="fbe6b-103">Piece picking confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fbe6b-104">Stykplukning gør det muligt for dig at bekræfte hver enkelt lagervare via pluk og optællingsarbejde på en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-104">Piece picking allows you to confirm each piece of inventory through picking or counting work on a mobile device.</span></span> <span data-ttu-id="fbe6b-105">For pluk kan du bekræfte mængden af arbejde, der skal behandles, op til det antal, der er angivet på arbejde, der skal plukkes.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-105">For picks, you can confirm the quantity of work to be processed up to the quantity that is specified on work to be picked.</span></span> <span data-ttu-id="fbe6b-106">For optællingsarbejde kan du scanne det lager, du optæller, og spore det samlede beløb.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-106">For counting work, you can scan the inventory that you are counting and track the total amount.</span></span>

<span data-ttu-id="fbe6b-107">Når du aktiverer stykpluk, vælges bekræftelse af produkt automatisk.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-107">When you enable piece picking, product confirmation is automatically selected.</span></span> <span data-ttu-id="fbe6b-108">Ved pluk af arbejdstypen er det maksimale antal styk aktiveret.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-108">For work-type picks, a maximum number of pieces is enabled.</span></span> <span data-ttu-id="fbe6b-109">På denne måde kan du angive et maksimum for det antal enheder, der skal bekræftes under arbejdet.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-109">This allows you to set a maximum to the number of pieces that must be confirmed during the work process.</span></span> <span data-ttu-id="fbe6b-110">Det maksimale antal er baseret på den aktuelle arbejdsenhed, der behandles.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-110">The maximum quantity is based on the current work unit that is being processed.</span></span> <span data-ttu-id="fbe6b-111">Optællingsarbejdstypen tillader ikke et maksimum.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-111">The counting work type does not allow a maximum.</span></span>

<span data-ttu-id="fbe6b-112">Du kan også bruge det antal og den måleenhed, der er knyttet til en scannet stregkode.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-112">You can also use the quantity and unit of measure (UOM) that is associated with a scanned bar code.</span></span> <span data-ttu-id="fbe6b-113">Dette fungerer ved modtagelse af indgående flows, herunder modtagelse af blandede id'er, vare på indkøbsordre, vare på overførselsordre og varelast.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-113">This will work for receiving on inbound flows including mixed license plate receiving, purchase order item, transfer order item, and load item.</span></span> <span data-ttu-id="fbe6b-114">Det kan også bruges til stykplukning, hvor scanning af stregkoden føjer antallet til det samlede antal bekræftede styk og konverterer mellem måleenhed på stregkoden og arbejdsenheden.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-114">It also works for piece picking where scanning the bar code will add the quantity to the total number of confirmed pieces converting between the UOM on the bar code and the work unit.</span></span> <span data-ttu-id="fbe6b-115">Hvis det ved optælling måleenheden på stregkoden kan bekræftes, at antallet er tilladt ved optælling af seriegruppen, føjes antallet til den samlede optælling.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-115">If, when counting the UOM on the bar code, it is confirmed that the quantity is allowed for counting on the sequence group, the quantity will be added to the total count.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="fbe6b-116">Hvor det er relevant</span><span class="sxs-lookup"><span data-stu-id="fbe6b-116">Where it applies</span></span>

<span data-ttu-id="fbe6b-117">Stykpluk fungerer for alt optællingsarbejde og for det indledende pluk ved alle typer arbejde.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-117">Piece picking works for all counting work and for the initial pick for any type of work.</span></span> <span data-ttu-id="fbe6b-118">Stykpluk gælder ikke, hvis varen styres af serienumre, eller hvis det er et produktions- eller kanban-pluk fra en id-lokalitet, og varen er indstillet til midlertidig placering.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-118">Piece picking does not apply if the item is controlled by serial numbers or if it is a production or kanban pick from a license plate (LP) location and the item is set to staging.</span></span>

## <a name="set-up-piece-picking"></a><span data-ttu-id="fbe6b-119">Konfigurere stykplukning</span><span class="sxs-lookup"><span data-stu-id="fbe6b-119">Set up piece picking</span></span>

1.  <span data-ttu-id="fbe6b-120">I et menupunkt på en mobilenhed skal du åbne opsætningsformularen for arbejdsbekræftelse: Lokationsstyring > **Lokationsstyring** > **Opsætning** > **Mobilenhed** > **Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-120">On a mobile device menu item, open the setup form for work confirmation: Warehouse management > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span> 
2. <span data-ttu-id="fbe6b-121">Åbn Konfiguration af arbejdsbekræftelse fra menupunktet på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-121">From the mobile device menu item, open Work confirmation setup.</span></span>

<span data-ttu-id="fbe6b-122">Følgende indstillinger kan vælges, når arbejdstype pluk eller optælling.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-122">The following options become available for selection when the work type is pick or counting.</span></span>


|           <span data-ttu-id="fbe6b-123">Indstilling</span><span class="sxs-lookup"><span data-stu-id="fbe6b-123">Option</span></span>           |                                                                            <span data-ttu-id="fbe6b-124">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fbe6b-124">Description</span></span>                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbe6b-125">Bekræftelse af stykplukning</span><span class="sxs-lookup"><span data-stu-id="fbe6b-125">Piece picking confirmation</span></span> | <span data-ttu-id="fbe6b-126">Arbejdstyper, der kan vælges til pluk og optælling.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-126">Available for pick and counting work types.</span></span> <span data-ttu-id="fbe6b-127">Bekræftelse af produkt vælges automatisk.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-127">Product confirmation is automatically selected.</span></span> <span data-ttu-id="fbe6b-128">Gør det muligt for dig at bekræfte hver enkelt vare på lageret fra mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-128">Allows you to confirm each piece of inventory from the mobile device.</span></span> |
|  <span data-ttu-id="fbe6b-129">Maksimalt antal stykker</span><span class="sxs-lookup"><span data-stu-id="fbe6b-129">Maximum number of pieces</span></span>  |                   <span data-ttu-id="fbe6b-130">Tilgængelig for plukarbejde, hvis bekræftelse af stykpluk er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-130">Available for pick work if piece picking confirmation is enabled.</span></span> <span data-ttu-id="fbe6b-131">Angiver en grænse for det antal styk, du skal bekræfte.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-131">Sets a limit to the number of pieces that you must confirm.</span></span>                   |

