---
title: Få vist omkostningsværdier for disponibel lagerbeholdning
description: Brug formularen Regulering af disponibel lagerbeholdning til at regulere kostværdien af det disponible lagerantal, efter at der er gennemført en lagerlukning.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1fc97db0f0b637e27ece904fe24e91a92044bc17
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208794"
---
# <a name="adjust-on-hand-inventory-cost-values"></a><span data-ttu-id="753ba-103">Få vist omkostningsværdier for disponibel lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="753ba-103">Adjust on-hand inventory cost values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="753ba-104">Brug formularen Regulering af disponibel lagerbeholdning til at regulere kostværdien af det disponible lagerantal, efter at der er gennemført en lagerlukning.</span><span class="sxs-lookup"><span data-stu-id="753ba-104">Use the Adjustment of on-hand inventory page to adjust the cost value of the on-hand inventory quantities after an inventory close process is run.</span></span>

<span data-ttu-id="753ba-105">Du kan bruge siden **Regulering af disponibel lagerbeholdning** til at regulere kostværdien af de disponible lagerantal, efter at der er gennemført en lagerlukning.</span><span class="sxs-lookup"><span data-stu-id="753ba-105">You can use the **Adjustment of on-hand inventory** page to adjust the cost value of on-hand inventory quantities after an inventory close process is run.</span></span> <span data-ttu-id="753ba-106">**Bemærk!** Hvis du vil åbne siden **Regulering af disponibel lagerbeholdning** på siden **Lukning og regulering**, skal du vælge posten for en fuldført lagerlukningsproces og derefter klikke på **Regulering** &gt; **Disponibel**.</span><span class="sxs-lookup"><span data-stu-id="753ba-106">**Note:** To open the **Adjustment of on-hand inventory** page, on the **Closing and adjustment** page, select the record of a completed inventory close process, and then click **Adjustment** &gt; **On-hand**.</span></span> <span data-ttu-id="753ba-107">**Eksempel:** Du har følgende posteringer i februar:</span><span class="sxs-lookup"><span data-stu-id="753ba-107">**Example:** You have the following transactions in February:</span></span>

-   <span data-ttu-id="753ba-108">1. februar: en økonomisk lagertilgang for et antal på 2 til en kostpris af kr. 10,00</span><span class="sxs-lookup"><span data-stu-id="753ba-108">February 1: An inventory financial receipt for a quantity of 2 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="753ba-109">5. februar: en økonomisk lagertilgang for et antal på 1 til en kostpris af kr. 13,00</span><span class="sxs-lookup"><span data-stu-id="753ba-109">February 5: An inventory financial receipt for a quantity of 1 at a cost of USD 13.00</span></span>
-   <span data-ttu-id="753ba-110">19. februar: en økonomisk lagerafgang for et antal på 1 til en løbende gennemsnitskostpris af kr. 11,00 pr. styk</span><span class="sxs-lookup"><span data-stu-id="753ba-110">February 19: An inventory financial issue for a quantity of 1 at a running average cost of USD 11.00</span></span>

<span data-ttu-id="753ba-111">Denne vare blev konfigureret med lagermodellen FIFO (First In, First Out), og lagerlukningen blev udført pr. 28. februar.</span><span class="sxs-lookup"><span data-stu-id="753ba-111">This item was set up with the first in, first out (FIFO) inventory model, and inventory close was performed as of February 28.</span></span> <span data-ttu-id="753ba-112">Den økonomiske afgangspostering på kr. 11,00 udlignes mod den økonomiske tilgang, der er dateret 1. februar, og der udføres en regulering på kr. 1,00.</span><span class="sxs-lookup"><span data-stu-id="753ba-112">The financial issue transaction of USD 11.00 will be settled against the financial receipt that is dated February 1, and an adjustment of USD 1.00 will be made.</span></span> <span data-ttu-id="753ba-113">Følgende lagertilgange indeholder åbne lagerantal:</span><span class="sxs-lookup"><span data-stu-id="753ba-113">The following inventory receipts will then contain open inventory quantities:</span></span>

-   <span data-ttu-id="753ba-114">1. februar: en mængde på 1 til kr. 10,00</span><span class="sxs-lookup"><span data-stu-id="753ba-114">February 1: A quantity of 1 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="753ba-115">5. februar: en mængde på 1 til kr. 13,00</span><span class="sxs-lookup"><span data-stu-id="753ba-115">February 5: A quantity of 1 at a cost of USD 13.00</span></span>

<span data-ttu-id="753ba-116">Hvis du vil angive kostprisen for disse to varer til kr. 15,00, skal du bruge indstillingen Regulering af disponibel lagerbeholdning til at regulere de åbne disponible lagerantal med virkning fra den sidste lagerlukningsperiode.</span><span class="sxs-lookup"><span data-stu-id="753ba-116">To set the cost of these two items to USD 15.00, use the on-hand adjustment option to adjust the open on-hand quantities as of the last inventory close period.</span></span> <span data-ttu-id="753ba-117">**Bemærk!** Bogføringsdatoen for reguleringen af den disponible lagerbeholdning vil være datoen for den sidste lagerlukning.</span><span class="sxs-lookup"><span data-stu-id="753ba-117">**Note:** The posting date of the on-hand adjustment transaction will be the date of the last inventory close.</span></span> <span data-ttu-id="753ba-118">Denne dato kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="753ba-118">This date can't be modified.</span></span>
