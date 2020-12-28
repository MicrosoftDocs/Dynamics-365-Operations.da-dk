---
title: Nummerserie i transportstyring
description: Dette emne beskriver, hvordan du konfigurerer nummerserier til transportstyring.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2c3f087ac76412cd2dce93dcb31b796ce2cb3bc4
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/29/2020
ms.locfileid: "4425092"
---
# <a name="transportation-management-number-sequence"></a><span data-ttu-id="3d4fb-103">Nummerserie i transportstyring</span><span class="sxs-lookup"><span data-stu-id="3d4fb-103">Transportation management number sequence</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d4fb-104">Brug siden **Nummerserier** i modulet transportstyring til at konfigurere forskellige pro-numre.</span><span class="sxs-lookup"><span data-stu-id="3d4fb-104">Use the **Number sequences** page in the transportation management module to set up various pro numbers.</span></span> <span data-ttu-id="3d4fb-105">Pro-numre bruges af fragtmænd til at organisere og spore forløbet for hver forsendelse.</span><span class="sxs-lookup"><span data-stu-id="3d4fb-105">Pro numbers are used by carriers to organize and track the progress of each shipment.</span></span>

## <a name="create-a-number-sequence-for-a-pro-number"></a><span data-ttu-id="3d4fb-106">Oprette en nummerserie til et pro-nummer</span><span class="sxs-lookup"><span data-stu-id="3d4fb-106">Create a number sequence for a pro number</span></span>

<span data-ttu-id="3d4fb-107">Benyt følgende fremgangsmåde for at oprette en nummerserie til et pro-nummer:</span><span class="sxs-lookup"><span data-stu-id="3d4fb-107">To create a number sequence for a pro number, do the following:</span></span>

1. <span data-ttu-id="3d4fb-108">Gå til **Transportstyring \> Opsætning \> Fragtmænd \> Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="3d4fb-108">Go to **Transportation management \> Setup \> Carriers \> Number sequences**.</span></span>
1. <span data-ttu-id="3d4fb-109">Vælg **Ny** for at oprette en ny nummerserie.</span><span class="sxs-lookup"><span data-stu-id="3d4fb-109">Select **New** to create a new number sequence.</span></span>
1. <span data-ttu-id="3d4fb-110">Angiv et entydigt id og et sigende navn for nummerserien.</span><span class="sxs-lookup"><span data-stu-id="3d4fb-110">Enter a unique ID and descriptive name for the number sequence.</span></span>
1. <span data-ttu-id="3d4fb-111">I feltet **Nummerserietype** er *Pro-nummer* den eneste valgmulighed.</span><span class="sxs-lookup"><span data-stu-id="3d4fb-111">In the **Number sequence type** field, *Pro number* is the only option.</span></span>
1. <span data-ttu-id="3d4fb-112">I feltet **Kontrolciffer** er *Kontrolciffer* den eneste mulighed og er konfigureret som et generisk program.</span><span class="sxs-lookup"><span data-stu-id="3d4fb-112">In the **Check digit** field, *Check digit* is the only option and is set up as a generic engine.</span></span>
1. <span data-ttu-id="3d4fb-113">Angiv oplysninger om serien i oversigtspanelet **Sekvens**.</span><span class="sxs-lookup"><span data-stu-id="3d4fb-113">On the **Sequence** FastTab, provide information about the sequence.</span></span>
1. <span data-ttu-id="3d4fb-114">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3d4fb-114">Close the page.</span></span>

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a><span data-ttu-id="3d4fb-115">Knytte en nummerserie til en fragtmand</span><span class="sxs-lookup"><span data-stu-id="3d4fb-115">Link a number sequence to a shipping carrier</span></span>

<span data-ttu-id="3d4fb-116">Benyt følgende fremgangsmåde for at knytte en nummerserie til en fragtmand:</span><span class="sxs-lookup"><span data-stu-id="3d4fb-116">To link a number sequence to a carrier, do the following:</span></span>

1. <span data-ttu-id="3d4fb-117">Gå til **Transportstyring \> Opsætning \> Fragtmænd \> Fragtmænd**.</span><span class="sxs-lookup"><span data-stu-id="3d4fb-117">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="3d4fb-118">Vælg en fragtmand.</span><span class="sxs-lookup"><span data-stu-id="3d4fb-118">Select a shipping carrier.</span></span>
1. <span data-ttu-id="3d4fb-119">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="3d4fb-119">Select **Edit**.</span></span>
1. <span data-ttu-id="3d4fb-120">Vælg en indstilling i feltet **Pro-nummerserie** i oversigtspanelet **Oversigt**.</span><span class="sxs-lookup"><span data-stu-id="3d4fb-120">On the **Overview** FastTab, select an option in the **Pro number sequence** field.</span></span>
1. <span data-ttu-id="3d4fb-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3d4fb-121">Close the page.</span></span>
