---
title: Statusser for transportstyring
description: I dette emne forklares, hvordan du kan oprette en transportstatus og knytte den pågældende status til en fragtmands status.
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
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: fb0d98729046330037f96ab7e13a1bf897e35a1e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233337"
---
# <a name="transportation-management-statuses"></a><span data-ttu-id="9a8bd-103">Statusser for transportstyring</span><span class="sxs-lookup"><span data-stu-id="9a8bd-103">Transportation management statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a8bd-104">Konfigurer masterkoder for transportstatusser for at fortolke koder, der er leveret af dine fragtmænd.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-104">Set up master codes for transportation statuses to interpret codes that are provided by your shipping carriers.</span></span> <span data-ttu-id="9a8bd-105">På denne måde kan du integrere med fragtmænd for at angive status.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-105">This lets you integrate with shipping carriers to provide a status.</span></span> <span data-ttu-id="9a8bd-106">Den transportstatus, som du angiver for en transportmasterstatuskode, kan hjælpe dig med at spore statussen for en last, forsendelse eller container.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-106">The transportation status that you provide for a transportation master status code can help you track the status of a load, shipment, or container.</span></span> <span data-ttu-id="9a8bd-107">Den specifikke transportstatus for en last, forsendelse eller container kan kun opdateres via dataintegration og ikke manuelt via brugergrænsefladen.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-107">The specific transportation status for a load, shipment, or container can only be updated through data integration and not manually through the user interface.</span></span>

## <a name="create-a-transportation-status"></a><span data-ttu-id="9a8bd-108">Oprette en transportstatus</span><span class="sxs-lookup"><span data-stu-id="9a8bd-108">Create a transportation status</span></span>

<span data-ttu-id="9a8bd-109">Følg disse trin for at oprette en transportstatus:</span><span class="sxs-lookup"><span data-stu-id="9a8bd-109">To create a transportation status, follow these steps:</span></span>

1. <span data-ttu-id="9a8bd-110">Gå til **Transportstyring \> Opsætning \> Master for transportstatus**.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-110">Go to **Transportation management \> Setup \> Transportation status masters**.</span></span>
1. <span data-ttu-id="9a8bd-111">Vælg **Ny** for at oprette en transportstatusmaster.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-111">Select **New** to create a transportation status master.</span></span>
1. <span data-ttu-id="9a8bd-112">Angiv en entydig kode for transportstatussen i feltet **Master for transportstatus**.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-112">In the **Transportation status master** field, enter a unique code for the transportation status.</span></span>
1. <span data-ttu-id="9a8bd-113">Vælg enten *Fragtmand* eller *Hub* som transporttype i feltet **Transporttype**.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-113">In the **Transportation type** field, select either *Shipping carrier* or *Hub* as the type of transportation.</span></span>
1. <span data-ttu-id="9a8bd-114">Angiv et navn og en transportstatus.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-114">Enter a name and transportation status.</span></span>
1. <span data-ttu-id="9a8bd-115">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-115">Close the page.</span></span>

## <a name="map-a-transportation-status-to-a-carrier-status"></a><span data-ttu-id="9a8bd-116">Knytte en transportstatus til en fragtmands status</span><span class="sxs-lookup"><span data-stu-id="9a8bd-116">Map a transportation status to a carrier status</span></span>

<span data-ttu-id="9a8bd-117">Hvis du vil knytte en transportstatus til en fragtmands status, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="9a8bd-117">To map a transportation status to a carrier status, follow these steps:</span></span>

1. <span data-ttu-id="9a8bd-118">Gå til **Transportstyring \> Opsætning \> Fragtmænd \> Transportstatus for fragtmand**.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-118">Go to **Transportation management \> Setup \> Carriers \> Carrier transportation status**.</span></span>
1. <span data-ttu-id="9a8bd-119">Vælg **Ny** for at knytte en kode fra en fragtmand til en transportstatusmasterkode.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-119">Select **New** to map a code from a shipping carrier to a transportation status master code.</span></span>
1. <span data-ttu-id="9a8bd-120">Vælg det entydige id for fragtmanden og fragttjenesten.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-120">Select the unique ID for the shipping carrier and the carrier service.</span></span>
1. <span data-ttu-id="9a8bd-121">Vælg den transportstatuskode, du vil knytte til den valgte fragtmands kode.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-121">Select the transportation status code that you want to map to the selected shipping carrier's code.</span></span>
1. <span data-ttu-id="9a8bd-122">Angiv den eksterne kode, der bruges af fragtmanden.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-122">Enter the external code that is used by the shipping carrier.</span></span>
1. <span data-ttu-id="9a8bd-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-123">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]