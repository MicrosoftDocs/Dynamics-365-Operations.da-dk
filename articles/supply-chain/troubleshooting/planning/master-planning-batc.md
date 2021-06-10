---
title: Du kan ikke filtrere varedisponeringsvarer efter deres relaterede disponeringsgruppeværdier
description: Du kan ikke filtrere varedisponeringsvarer efter deres relaterede disponeringsgruppeværdier.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049459"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a><span data-ttu-id="57c66-103">Du kan ikke filtrere varedisponeringsvarer efter deres relaterede disponeringsgruppeværdier</span><span class="sxs-lookup"><span data-stu-id="57c66-103">You can't filter master planning items by their related coverage group values</span></span>

<span data-ttu-id="57c66-104">KB-nummer: 4612572</span><span class="sxs-lookup"><span data-stu-id="57c66-104">KB number: 4612572</span></span>

## <a name="symptoms"></a><span data-ttu-id="57c66-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="57c66-105">Symptoms</span></span>

<span data-ttu-id="57c66-106">Du vil filtrere de varer, der skal medtages i en varedisponeringsbatch, baseret på værdierne for relaterede poster fra varedisponeringstabellen.</span><span class="sxs-lookup"><span data-stu-id="57c66-106">You want to filter the items that will be included in a master planning batch job, based on the values of related records from the item coverage table.</span></span> <span data-ttu-id="57c66-107">(Du vil f.eks. filtrere varer efter deres værdi i **kreditor**- og/eller **disponeringsgruppen**).</span><span class="sxs-lookup"><span data-stu-id="57c66-107">(For example, you want to filter items by their **Vendor** and/or **Coverage group** value).</span></span> <span data-ttu-id="57c66-108">Med filteropsætningen for batchjobbet kan du oprette en joinforbindelse fra tabellen **Varer** til tabellen **Varedisponering** og derefter angive feltværdier fra varedisponeringstabellen i forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="57c66-108">The filter setup for the batch job lets you create a join from the **Items** table to the **Item coverage** table, and then specify field values from the item coverage table in your query.</span></span> <span data-ttu-id="57c66-109">Men når du har fuldført denne opsætning, opretter systemet stadig ordreforslag for hele varedisponeringen, ikke kun for de varer, der svarer til de angivne feltværdier fra varedisponeringstabellen.</span><span class="sxs-lookup"><span data-stu-id="57c66-109">However, after you complete this setup, the system still creates planned orders for the whole item coverage, not just for the items that match the specified field values from the item coverage table.</span></span>

## <a name="resolution"></a><span data-ttu-id="57c66-110">Løsning</span><span class="sxs-lookup"><span data-stu-id="57c66-110">Resolution</span></span>

<span data-ttu-id="57c66-111">Filteret for batchjobbet kan kun filtrere efter varer.</span><span class="sxs-lookup"><span data-stu-id="57c66-111">The batch job filter can filter only on items.</span></span> <span data-ttu-id="57c66-112">Du kan føje en joinforbindelse til tabellen **Varedisponering**, men de filterindstillinger, du foretager i forhold til den pågældende tabel, påvirker ikke forespørgselsoutputtet.</span><span class="sxs-lookup"><span data-stu-id="57c66-112">Although you can add a join to the **Item coverage** table, filter settings that you make against that table won't affect the query output.</span></span> <span data-ttu-id="57c66-113">På kørselstidspunktet kører systemet planlægning for alle disponeringsgrupper og alle de variationer, som de filtrerede varer har.</span><span class="sxs-lookup"><span data-stu-id="57c66-113">At runtime, the system runs planning for all the coverage groups and all the variations that the filtered items have.</span></span> <span data-ttu-id="57c66-114">Når en vare allerede er inkluderet i kørslen, påvirker eventuelle disponeringsgrupper, der er inkluderet i varefilter A, ikke outputtet for planlægning.</span><span class="sxs-lookup"><span data-stu-id="57c66-114">After an item is already included in the run, any coverage groups that are included in the item filter a won't affect the planning output.</span></span>
