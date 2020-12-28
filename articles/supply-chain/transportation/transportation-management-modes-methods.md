---
title: Måder og metoder i transportstyring
description: I dette emne beskrives, hvordan du kan konfigurere transportmåder og -metoder.
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
ms.openlocfilehash: ceb3930cdb7764f846e88edfff6906b902a7f5fa
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/29/2020
ms.locfileid: "4425093"
---
# <a name="transportation-management-modes-and-methods"></a><span data-ttu-id="7c05e-103">Måder og metoder i transportstyring</span><span class="sxs-lookup"><span data-stu-id="7c05e-103">Transportation management modes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c05e-104">Transportstyringsmåden repræsenterer den transporttype, som fragtmanden bruger til fragtleverancer, f.eks. LTL (Less than Load), truckload (TL) eller pakke.</span><span class="sxs-lookup"><span data-stu-id="7c05e-104">The transportation management  mode represents the type of transport that the carrier uses for freight deliveries, such as less than load (LTL), truckload (TL), or parcel.</span></span> <span data-ttu-id="7c05e-105">Transportmetoden repræsenterer den transportform, som fragtmanden bruger til fragtleverancer, f.eks. fly, landevej, hav eller jernbane.</span><span class="sxs-lookup"><span data-stu-id="7c05e-105">The transportation method represents the form of transport that the carrier uses for freight deliveries, such as air, ground, ocean, or rail.</span></span>

<span data-ttu-id="7c05e-106">Måder og transportmetoder bruges i flere kontekster.</span><span class="sxs-lookup"><span data-stu-id="7c05e-106">Modes and transportation methods are used in several contexts.</span></span> <span data-ttu-id="7c05e-107">Der bruges kun måder i ruteplaner, mens både måder og transportmetoder bruges til opsætning af fragtmænd og fragttjenester.</span><span class="sxs-lookup"><span data-stu-id="7c05e-107">Only modes are used in route plans, while both modes and transportation methods are used when setting up shipping carriers and carrier services.</span></span> <span data-ttu-id="7c05e-108">Der findes ingen eksplicit relation eller hierarki mellem måder og transportmetoder.</span><span class="sxs-lookup"><span data-stu-id="7c05e-108">No explicit relationship or hierarchy exists between modes and transportation methods.</span></span>

## <a name="create-a-mode"></a><span data-ttu-id="7c05e-109">Oprette en transportmåde</span><span class="sxs-lookup"><span data-stu-id="7c05e-109">Create a mode</span></span>

<span data-ttu-id="7c05e-110">Følg disse trin for at oprette en transportmåde:</span><span class="sxs-lookup"><span data-stu-id="7c05e-110">To create a mode, follow these steps:</span></span>

1. <span data-ttu-id="7c05e-111">Gå til **Transportstyring \> Opsætning \> Fragtmænd \> Tilstand**.</span><span class="sxs-lookup"><span data-stu-id="7c05e-111">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="7c05e-112">Vælg **Ny** for at oprette en ny tilstand.</span><span class="sxs-lookup"><span data-stu-id="7c05e-112">Select **New** to create a new mode.</span></span>
1. <span data-ttu-id="7c05e-113">Angiv et entydigt id og et sigende navn for måden.</span><span class="sxs-lookup"><span data-stu-id="7c05e-113">Enter a unique ID and a descriptive name for the mode.</span></span>
1. <span data-ttu-id="7c05e-114">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7c05e-114">Close the page.</span></span>

## <a name="create-a-transportation-method"></a><span data-ttu-id="7c05e-115">Oprette en transportmetode</span><span class="sxs-lookup"><span data-stu-id="7c05e-115">Create a transportation method</span></span>

<span data-ttu-id="7c05e-116">Følg disse trin for at oprette en transportmetode:</span><span class="sxs-lookup"><span data-stu-id="7c05e-116">To create a transportation method, follow these steps:</span></span>

1. <span data-ttu-id="7c05e-117">Gå til **Transportstyring \> Opsætning \> Fragtmænd \> Transportmetoder**.</span><span class="sxs-lookup"><span data-stu-id="7c05e-117">Go to **Transportation management \> Setup \> Carriers \> Transportation methods**.</span></span>
1. <span data-ttu-id="7c05e-118">Vælg **Ny** for at oprette en ny transportmetode.</span><span class="sxs-lookup"><span data-stu-id="7c05e-118">Select **New** to create a new transportation method.</span></span>
1. <span data-ttu-id="7c05e-119">Angiv et entydigt id og et sigende navn for transportmetoden.</span><span class="sxs-lookup"><span data-stu-id="7c05e-119">Enter a unique ID and descriptive name for the transportation method.</span></span>
1. <span data-ttu-id="7c05e-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7c05e-120">Close the page.</span></span>
