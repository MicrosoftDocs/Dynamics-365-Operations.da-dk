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
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b9b548212c6f1f3faac56cd7ca182d84cc339bd2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973904"
---
# <a name="transportation-management-modes-and-methods"></a><span data-ttu-id="e2cb2-103">Måder og metoder i transportstyring</span><span class="sxs-lookup"><span data-stu-id="e2cb2-103">Transportation management modes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2cb2-104">Transportstyringsmåden repræsenterer den transporttype, som fragtmanden bruger til fragtleverancer, f.eks. LTL (Less than Load), truckload (TL) eller pakke.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-104">The transportation management  mode represents the type of transport that the carrier uses for freight deliveries, such as less than load (LTL), truckload (TL), or parcel.</span></span> <span data-ttu-id="e2cb2-105">Transportmetoden repræsenterer den transportform, som fragtmanden bruger til fragtleverancer, f.eks. fly, landevej, hav eller jernbane.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-105">The transportation method represents the form of transport that the carrier uses for freight deliveries, such as air, ground, ocean, or rail.</span></span>

<span data-ttu-id="e2cb2-106">Måder og transportmetoder bruges i flere kontekster.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-106">Modes and transportation methods are used in several contexts.</span></span> <span data-ttu-id="e2cb2-107">Der bruges kun måder i ruteplaner, mens både måder og transportmetoder bruges til opsætning af fragtmænd og fragttjenester.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-107">Only modes are used in route plans, while both modes and transportation methods are used when setting up shipping carriers and carrier services.</span></span> <span data-ttu-id="e2cb2-108">Der findes ingen eksplicit relation eller hierarki mellem måder og transportmetoder.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-108">No explicit relationship or hierarchy exists between modes and transportation methods.</span></span>

## <a name="create-a-mode"></a><span data-ttu-id="e2cb2-109">Oprette en transportmåde</span><span class="sxs-lookup"><span data-stu-id="e2cb2-109">Create a mode</span></span>

<span data-ttu-id="e2cb2-110">Følg disse trin for at oprette en transportmåde:</span><span class="sxs-lookup"><span data-stu-id="e2cb2-110">To create a mode, follow these steps:</span></span>

1. <span data-ttu-id="e2cb2-111">Gå til **Transportstyring \> Opsætning \> Fragtmænd \> Tilstand**.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-111">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="e2cb2-112">Vælg **Ny** for at oprette en ny tilstand.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-112">Select **New** to create a new mode.</span></span>
1. <span data-ttu-id="e2cb2-113">Angiv et entydigt id og et sigende navn for måden.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-113">Enter a unique ID and a descriptive name for the mode.</span></span>
1. <span data-ttu-id="e2cb2-114">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-114">Close the page.</span></span>

## <a name="create-a-transportation-method"></a><span data-ttu-id="e2cb2-115">Oprette en transportmetode</span><span class="sxs-lookup"><span data-stu-id="e2cb2-115">Create a transportation method</span></span>

<span data-ttu-id="e2cb2-116">Følg disse trin for at oprette en transportmetode:</span><span class="sxs-lookup"><span data-stu-id="e2cb2-116">To create a transportation method, follow these steps:</span></span>

1. <span data-ttu-id="e2cb2-117">Gå til **Transportstyring \> Opsætning \> Fragtmænd \> Transportmetoder**.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-117">Go to **Transportation management \> Setup \> Carriers \> Transportation methods**.</span></span>
1. <span data-ttu-id="e2cb2-118">Vælg **Ny** for at oprette en ny transportmetode.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-118">Select **New** to create a new transportation method.</span></span>
1. <span data-ttu-id="e2cb2-119">Angiv et entydigt id og et sigende navn for transportmetoden.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-119">Enter a unique ID and descriptive name for the transportation method.</span></span>
1. <span data-ttu-id="e2cb2-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-120">Close the page.</span></span>
