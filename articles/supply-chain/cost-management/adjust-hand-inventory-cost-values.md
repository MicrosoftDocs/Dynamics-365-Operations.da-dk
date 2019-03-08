---
title: Få vist omkostningsværdier for disponibel lagerbeholdning
description: Brug formularen Regulering af disponibel lagerbeholdning til at regulere kostværdien af det disponible lagerantal, efter at der er gennemført en lagerlukning.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2417a278e58f4309873ab4d33b0d1f1686081951
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "335157"
---
# <a name="adjust-on-hand-inventory-cost-values"></a><span data-ttu-id="b6389-103">Få vist omkostningsværdier for disponibel lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="b6389-103">Adjust on-hand inventory cost values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6389-104">Brug formularen Regulering af disponibel lagerbeholdning til at regulere kostværdien af det disponible lagerantal, efter at der er gennemført en lagerlukning.</span><span class="sxs-lookup"><span data-stu-id="b6389-104">Use the Adjustment of on-hand inventory page to adjust the cost value of the on-hand inventory quantities after an inventory close process is run.</span></span>

<span data-ttu-id="b6389-105">Du kan bruge siden **Regulering af disponibel lagerbeholdning** til at regulere kostværdien af de disponible lagerantal, efter at der er gennemført en lagerlukning.</span><span class="sxs-lookup"><span data-stu-id="b6389-105">You can use the **Adjustment of on-hand inventory** page to adjust the cost value of on-hand inventory quantities after an inventory close process is run.</span></span> <span data-ttu-id="b6389-106">**Bemærk!** Hvis du vil åbne siden **Regulering af disponibel lagerbeholdning** på siden **Lukning og regulering**, skal du vælge posten for en fuldført lagerlukningsproces og derefter klikke på **Regulering** &gt; **Disponibel**.</span><span class="sxs-lookup"><span data-stu-id="b6389-106">**Note:** To open the **Adjustment of on-hand inventory** page, on the **Closing and adjustment** page, select the record of a completed inventory close process, and then click **Adjustment** &gt; **On-hand**.</span></span> <span data-ttu-id="b6389-107">**Eksempel:** Du har følgende posteringer i februar:</span><span class="sxs-lookup"><span data-stu-id="b6389-107">**Example:** You have the following transactions in February:</span></span>

-   <span data-ttu-id="b6389-108">1. februar: en økonomisk lagertilgang for et antal på 2 til en kostpris af kr. 10,00</span><span class="sxs-lookup"><span data-stu-id="b6389-108">February 1: An inventory financial receipt for a quantity of 2 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="b6389-109">5. februar: en økonomisk lagertilgang for et antal på 1 til en kostpris af kr. 13,00</span><span class="sxs-lookup"><span data-stu-id="b6389-109">February 5: An inventory financial receipt for a quantity of 1 at a cost of USD 13.00</span></span>
-   <span data-ttu-id="b6389-110">19. februar: en økonomisk lagerafgang for et antal på 1 til en løbende gennemsnitskostpris af kr. 11,00 pr. styk</span><span class="sxs-lookup"><span data-stu-id="b6389-110">February 19: An inventory financial issue for a quantity of 1 at a running average cost of USD 11.00</span></span>

<span data-ttu-id="b6389-111">Denne vare blev konfigureret med lagermodellen FIFO (First In, First Out), og lagerlukningen blev udført pr. 28. februar.</span><span class="sxs-lookup"><span data-stu-id="b6389-111">This item was set up with the first in, first out (FIFO) inventory model, and inventory close was performed as of February 28.</span></span> <span data-ttu-id="b6389-112">Den økonomiske afgangspostering på kr. 11,00 udlignes mod den økonomiske tilgang, der er dateret 1. februar, og der udføres en regulering på kr. 1,00.</span><span class="sxs-lookup"><span data-stu-id="b6389-112">The financial issue transaction of USD 11.00 will be settled against the financial receipt that is dated February 1, and an adjustment of USD 1.00 will be made.</span></span> <span data-ttu-id="b6389-113">Følgende lagertilgange indeholder åbne lagerantal:</span><span class="sxs-lookup"><span data-stu-id="b6389-113">The following inventory receipts will then contain open inventory quantities:</span></span>

-   <span data-ttu-id="b6389-114">1. februar: en mængde på 1 til kr. 10,00</span><span class="sxs-lookup"><span data-stu-id="b6389-114">February 1: A quantity of 1 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="b6389-115">5. februar: en mængde på 1 til kr. 13,00</span><span class="sxs-lookup"><span data-stu-id="b6389-115">February 5: A quantity of 1 at a cost of USD 13.00</span></span>

<span data-ttu-id="b6389-116">Hvis du vil angive kostprisen for disse to varer til kr. 15,00, skal du bruge indstillingen Regulering af disponibel lagerbeholdning til at regulere de åbne disponible lagerantal med virkning fra den sidste lagerlukningsperiode.</span><span class="sxs-lookup"><span data-stu-id="b6389-116">To set the cost of these two items to USD 15.00, use the on-hand adjustment option to adjust the open on-hand quantities as of the last inventory close period.</span></span> <span data-ttu-id="b6389-117">**Bemærk!** Bogføringsdatoen for reguleringen af den disponible lagerbeholdning vil være datoen for den sidste lagerlukning.</span><span class="sxs-lookup"><span data-stu-id="b6389-117">**Note:** The posting date of the on-hand adjustment transaction will be the date of the last inventory close.</span></span> <span data-ttu-id="b6389-118">Denne dato kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="b6389-118">This date can't be modified.</span></span>
