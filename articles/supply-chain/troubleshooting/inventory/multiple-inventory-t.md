---
title: Flere lagertransaktioner for batchnumre, når Ved fysisk opdatering er deaktiveret
description: Flere lagertransaktioner oprettes, når du har reguleret en indkøbsordrelinje for varer, hvor indstillingen Ved fysisk opdatering for batchnummergruppen er indstillet til Nej.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026385"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a><span data-ttu-id="f2e5c-103">Flere lagertransaktioner for batchnumre, når Ved fysisk opdatering er deaktiveret</span><span class="sxs-lookup"><span data-stu-id="f2e5c-103">Multiple inventory transactions for batch numbers when On physical update is disabled</span></span>

<span data-ttu-id="f2e5c-104">KB-nummer: 4613390</span><span class="sxs-lookup"><span data-stu-id="f2e5c-104">KB number: 4613390</span></span>

## <a name="symptoms"></a><span data-ttu-id="f2e5c-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="f2e5c-105">Symptoms</span></span>

<span data-ttu-id="f2e5c-106">Flere lagertransaktioner oprettes, når du har reguleret en indkøbsordrelinje for varer, hvor indstillingen **Ved fysisk opdatering** for batchnummergruppen er indstillet til *Nej*.</span><span class="sxs-lookup"><span data-stu-id="f2e5c-106">Multiple inventory transactions are created after you adjust a purchase order line for items where the **On physical update** option of the batch number group is set to *No*.</span></span>

<span data-ttu-id="f2e5c-107">Når du opretter en vare, hvor indstillingen **Ved fysisk opdatering** for batchnummergruppen er indstillet til *Nej*, opretter systemet automatisk et nyt batchnummer, hvis du redigerer et antal på indkøbslinjen, og gemmer indkøbsordresiden.</span><span class="sxs-lookup"><span data-stu-id="f2e5c-107">When you create an item where the **On physical update** option of the batch number group is set to *No*, the system automatically creates a new batch number if you modify a purchase line quantity and save the purchase order page.</span></span>

## <a name="resolution"></a><span data-ttu-id="f2e5c-108">Løsning</span><span class="sxs-lookup"><span data-stu-id="f2e5c-108">Resolution</span></span>

<span data-ttu-id="f2e5c-109">Indstillingen **Ved fysisk opdatering** for batchnummergrupper fungerer på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="f2e5c-109">The **On physical update** setting for batch number groups works in the following way:</span></span>

- <span data-ttu-id="f2e5c-110">Når indstillingen er *Ja*, oprettes der først nye batchnumre, efter at der er sket en fysisk opdatering (f.eks. når der afsendes eller modtages varer).</span><span class="sxs-lookup"><span data-stu-id="f2e5c-110">When the option is set to *Yes*, new batch numbers are created only after a physical update (for example, when items are shipped or received).</span></span>
- <span data-ttu-id="f2e5c-111">Når indstillingen er *Nej*, oprettes der et nyt batchnummer, hver gang der finder en relevant opdatering sted (f.eks. når der føjes et nyt antal til en indkøbsordre).</span><span class="sxs-lookup"><span data-stu-id="f2e5c-111">When the option is set to *No*, a new batch number is created every time that an applicable update occurs (for example, when a new quantity is added to a purchase order).</span></span>
