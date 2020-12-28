---
title: Glidende gennemsnit, reserveomkostningssekvens
description: Dette emne indeholder oplysninger om reserveomkostninger til glidende gennemsnitsberegninger i Microsoft Dynamics 365 Supply Chain Management.
author: AndersGirke
manager: tfehr
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 0538701588b9c71dff4c538711606913a359de6a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424815"
---
# <a name="moving-average-fallback-cost-sequence"></a><span data-ttu-id="846ab-103">Glidende gennemsnit, reserveomkostningssekvens</span><span class="sxs-lookup"><span data-stu-id="846ab-103">Moving average fallback cost sequence</span></span>

<span data-ttu-id="846ab-104">Den ene måde, du kan beregne kostprisen på lageret på, er ved at bruge et _glidende gennemsnit_.</span><span class="sxs-lookup"><span data-stu-id="846ab-104">One way that you can calculate the cost of your inventory is by using a _moving average_.</span></span> <span data-ttu-id="846ab-105">Du kan knytte op til tre omkostningsværdier til hver lagervare:</span><span class="sxs-lookup"><span data-stu-id="846ab-105">Up to three cost values can be associated with each inventory item:</span></span>

- <span data-ttu-id="846ab-106">**Sidste afgang** – den sidste afgangsomkostning, der er tildelt, før lageret blev negativt</span><span class="sxs-lookup"><span data-stu-id="846ab-106">**Last issue** – The last issue cost that was assigned before inventory went negative</span></span>
- <span data-ttu-id="846ab-107">**Aktiv omkostning** – De seneste omkostninger, der er aktiveret i en efterkalkulationsversion</span><span class="sxs-lookup"><span data-stu-id="846ab-107">**Active cost** – The latest cost that was activated in a costing version</span></span>
- <span data-ttu-id="846ab-108">**Varepris** – Den omkostning, der er angivet for det frigivne produkt</span><span class="sxs-lookup"><span data-stu-id="846ab-108">**Item price** – The cost that is specified for the released product</span></span>

<span data-ttu-id="846ab-109">Systemet bruger en _reserveomkostningssekvens_ til at fastlægge værdiernes prioritetsrækkefølge for at afgøre, hvilke af disse omkostningsværdier der skal bruges i forbindelse med beregning af det glidende gennemsnit.</span><span class="sxs-lookup"><span data-stu-id="846ab-109">To determine which of these cost values should be used in moving average calculations, the system uses a _fallback cost sequence_ to establish the order of preference for the values.</span></span> <span data-ttu-id="846ab-110">Hvis værdien for den foretrukne kostpris ikke er tilgængelig, bruger systemet den næste foretrukne værdi osv.</span><span class="sxs-lookup"><span data-stu-id="846ab-110">If the preferred cost value isn't available, the system uses the next-preferred value, and so on.</span></span>

<span data-ttu-id="846ab-111">I tidligere versioner af Microsoft Dynamics 365 Supply Chain Management har systemet brugt en fast reserveomkostningssekvens (_Sidste afgang – Aktiv omkostning – Varepris_).</span><span class="sxs-lookup"><span data-stu-id="846ab-111">In previous versions of Microsoft Dynamics 365 Supply Chain Management, the system used a fixed fallback cost sequence (_Last issue – Active cost – Item price_).</span></span> <span data-ttu-id="846ab-112">I version 10.0.11 er denne sekvens stadig standardrækkefølgen.</span><span class="sxs-lookup"><span data-stu-id="846ab-112">In version 10.0.11, this sequence is still the default sequence.</span></span> <span data-ttu-id="846ab-113">Du kan dog også slå en funktion til, der giver dig mulighed for at vælge mellem tre tilgængelige reserveomkostningssekvenser.</span><span class="sxs-lookup"><span data-stu-id="846ab-113">However, you can also turn on a feature that lets you select among three available fallback cost sequences.</span></span> <span data-ttu-id="846ab-114">Denne funktion kan især være nyttig for organisationer, der regelmæssigt bruger negative lagerværdier.</span><span class="sxs-lookup"><span data-stu-id="846ab-114">This feature can be especially useful for organizations that regularly use negative inventory values.</span></span>

<span data-ttu-id="846ab-115">Hvis du vil gøre vælgeren for reserveomkostningssekvens tilgængelig, skal du (eller en administrator) bruge [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at slå den funktion til, som hedder _Glidende gennemsnitlig reserveomkostningssekvens_.</span><span class="sxs-lookup"><span data-stu-id="846ab-115">To make the selector for the fallback cost sequence available, you (or an admin) must use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named _Moving average fallback cost sequence_.</span></span>

<span data-ttu-id="846ab-116">Udfør følgende trin for at vælge reserveomkostningssekvensen til beregning af glidende gennemsnit.</span><span class="sxs-lookup"><span data-stu-id="846ab-116">To select the fallback cost sequence for moving average calculations, follow these steps.</span></span>

1. <span data-ttu-id="846ab-117">Åbn siden **Parametre**:</span><span class="sxs-lookup"><span data-stu-id="846ab-117">Open the **Parameters** page.</span></span>
2. <span data-ttu-id="846ab-118">Angiv en af følgende værdier i feltet **Reserveomkostningssekvens** på fanen **Lagerregnskab** i afsnittet **Glidende gennemsnit**:</span><span class="sxs-lookup"><span data-stu-id="846ab-118">On the **Inventory accounting** tab, in the **Moving average** section, set the **Fallback cost sequence** field to one of the following values:</span></span>

    - <span data-ttu-id="846ab-119">**Sidste afgang – Aktiv kostpris – Varepris** – Denne sekvens er standardrækkefølgen.</span><span class="sxs-lookup"><span data-stu-id="846ab-119">**Last issue – Active cost – Item price** – This sequence is the default sequence.</span></span> <span data-ttu-id="846ab-120">Det er den samme rækkefølge, som bruges, hvis funktionen _Glidende gennemsnit, reserveomkostningssekvens_ ikke er slået til.</span><span class="sxs-lookup"><span data-stu-id="846ab-120">It's the same sequence that is used if the _Moving average fallback cost sequence_ feature isn't turned on.</span></span>
    - <span data-ttu-id="846ab-121">**Aktiv omkostning – Sidste afgang**</span><span class="sxs-lookup"><span data-stu-id="846ab-121">**Active cost – Last issue**</span></span>
    - <span data-ttu-id="846ab-122">**Aktiv kostpris – Varepris** – Organisationer kan opleve problemer med ydeevnen, hvis de bruger forretningsprocesser, hvor lageret regelmæssigt er negativt, og transaktionsmængden samtidigt er høj.</span><span class="sxs-lookup"><span data-stu-id="846ab-122">**Active cost – Item price** – Organizations might experience performance issues if they use business processes where inventory regularly goes negative and, at the same time, the transaction volume is high.</span></span> <span data-ttu-id="846ab-123">Denne indstilling kan hjælpe med at reducere disse ydeevneproblemer.</span><span class="sxs-lookup"><span data-stu-id="846ab-123">This setting can help mitigate those performance issues.</span></span>

<span data-ttu-id="846ab-124">![Parametre til Lagerregnskab](media/inventory-accounting-parameters.png "Parametre til Lagerregnskab")</span><span class="sxs-lookup"><span data-stu-id="846ab-124">![Inventory accounting parameters](media/inventory-accounting-parameters.png "Inventory accounting parameters")</span></span>
