---
title: Nummerserie i transportstyring
description: Dette emne beskriver, hvordan du konfigurerer nummerserier til transportstyring.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3da757cbf47e0e1af781b720d17a673e19aeb3b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807674"
---
# <a name="transportation-management-number-sequence"></a><span data-ttu-id="05bb4-103">Nummerserie i transportstyring</span><span class="sxs-lookup"><span data-stu-id="05bb4-103">Transportation management number sequence</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05bb4-104">Brug siden **Nummerserier** i modulet transportstyring til at konfigurere forskellige pro-numre.</span><span class="sxs-lookup"><span data-stu-id="05bb4-104">Use the **Number sequences** page in the transportation management module to set up various pro numbers.</span></span> <span data-ttu-id="05bb4-105">Pro-numre bruges af fragtmænd til at organisere og spore forløbet for hver forsendelse.</span><span class="sxs-lookup"><span data-stu-id="05bb4-105">Pro numbers are used by carriers to organize and track the progress of each shipment.</span></span>

## <a name="create-a-number-sequence-for-a-pro-number"></a><span data-ttu-id="05bb4-106">Oprette en nummerserie til et pro-nummer</span><span class="sxs-lookup"><span data-stu-id="05bb4-106">Create a number sequence for a pro number</span></span>

<span data-ttu-id="05bb4-107">Benyt følgende fremgangsmåde for at oprette en nummerserie til et pro-nummer:</span><span class="sxs-lookup"><span data-stu-id="05bb4-107">To create a number sequence for a pro number, do the following:</span></span>

1. <span data-ttu-id="05bb4-108">Gå til **Transportstyring \> Opsætning \> Fragtmænd \> Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="05bb4-108">Go to **Transportation management \> Setup \> Carriers \> Number sequences**.</span></span>
1. <span data-ttu-id="05bb4-109">Vælg **Ny** for at oprette en ny nummerserie.</span><span class="sxs-lookup"><span data-stu-id="05bb4-109">Select **New** to create a new number sequence.</span></span>
1. <span data-ttu-id="05bb4-110">Angiv et entydigt id og et sigende navn for nummerserien.</span><span class="sxs-lookup"><span data-stu-id="05bb4-110">Enter a unique ID and descriptive name for the number sequence.</span></span>
1. <span data-ttu-id="05bb4-111">I feltet **Nummerserietype** er *Pro-nummer* den eneste valgmulighed.</span><span class="sxs-lookup"><span data-stu-id="05bb4-111">In the **Number sequence type** field, *Pro number* is the only option.</span></span>
1. <span data-ttu-id="05bb4-112">I feltet **Kontrolciffer** er *Kontrolciffer* den eneste mulighed og er konfigureret som et generisk program.</span><span class="sxs-lookup"><span data-stu-id="05bb4-112">In the **Check digit** field, *Check digit* is the only option and is set up as a generic engine.</span></span>
1. <span data-ttu-id="05bb4-113">Angiv oplysninger om serien i oversigtspanelet **Sekvens**.</span><span class="sxs-lookup"><span data-stu-id="05bb4-113">On the **Sequence** FastTab, provide information about the sequence.</span></span>
1. <span data-ttu-id="05bb4-114">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="05bb4-114">Close the page.</span></span>

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a><span data-ttu-id="05bb4-115">Knytte en nummerserie til en fragtmand</span><span class="sxs-lookup"><span data-stu-id="05bb4-115">Link a number sequence to a shipping carrier</span></span>

<span data-ttu-id="05bb4-116">Benyt følgende fremgangsmåde for at knytte en nummerserie til en fragtmand:</span><span class="sxs-lookup"><span data-stu-id="05bb4-116">To link a number sequence to a carrier, do the following:</span></span>

1. <span data-ttu-id="05bb4-117">Gå til **Transportstyring \> Opsætning \> Fragtmænd \> Fragtmænd**.</span><span class="sxs-lookup"><span data-stu-id="05bb4-117">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="05bb4-118">Vælg en fragtmand.</span><span class="sxs-lookup"><span data-stu-id="05bb4-118">Select a shipping carrier.</span></span>
1. <span data-ttu-id="05bb4-119">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="05bb4-119">Select **Edit**.</span></span>
1. <span data-ttu-id="05bb4-120">Vælg en indstilling i feltet **Pro-nummerserie** i oversigtspanelet **Oversigt**.</span><span class="sxs-lookup"><span data-stu-id="05bb4-120">On the **Overview** FastTab, select an option in the **Pro number sequence** field.</span></span>
1. <span data-ttu-id="05bb4-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="05bb4-121">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]