---
title: Manglende feltindstillinger, når varemodelgrupper kopieres til en anden juridisk enhed
description: Der mangler feltindstillinger, når varemodelgrupper kopieres til en anden juridisk enhed.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f6fdfef0bc377418ed8a9c8830e74526a0b95eb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026366"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a><span data-ttu-id="a7751-103">Manglende feltindstillinger, når varemodelgrupper kopieres til en anden juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="a7751-103">Missing field settings when item model groups are copied to another legal entity</span></span>

<span data-ttu-id="a7751-104">KB-nummer: 4612800</span><span class="sxs-lookup"><span data-stu-id="a7751-104">KB number: 4612800</span></span>

## <a name="symptoms"></a><span data-ttu-id="a7751-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="a7751-105">Symptoms</span></span>

<span data-ttu-id="a7751-106">Når du kopierer varemodelgrupper til en anden juridisk enhed (firma) ved hjælp af enheden *Lagerpolitikker for varemodelgruppe*, mangler der nogle feltindstillinger (f.eks. lagermodellen og -beskrivelsen) i den nye modelgruppe i den juridiske destinationsenhed.</span><span class="sxs-lookup"><span data-stu-id="a7751-106">When you copy item model groups to another legal entity (company) by using the *Item model group inventory policies* entity, some field settings (for example, the inventory model and description) are missing in the new model group in the destination legal entity.</span></span>

## <a name="resolution"></a><span data-ttu-id="a7751-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="a7751-107">Resolution</span></span>

<span data-ttu-id="a7751-108">Hvis du vil oprette en komplet kopi af en varemodelgruppe til en anden juridisk enhed, skal du også vælge både de lagerpolitikker for varemodelgruppen (`InventInventoryPolicyEntity`) og forudsætningspolitikkerne for omkostningsforløb (`InventCostFlowAssumptionPolicyEntity`), der er knyttet til varemodelgruppen.</span><span class="sxs-lookup"><span data-stu-id="a7751-108">To create a complete copy of an item model group to another legal entity, you must also select both the item model group inventory policies (`InventInventoryPolicyEntity`) and the cost flow assumption policies (`InventCostFlowAssumptionPolicyEntity`) that are associated with the item model group.</span></span>
