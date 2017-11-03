---
title: "Opgradering for enkelt bilag og værdiregulering af valuta"
description: "Nogle organisationer angiver kladder, der indeholder et enkelt bilag, der har mere end én debitor eller kreditor, og de kører også processen til værdiregulering af udenlandsk valuta for debitorer eller kreditorer. I dette emne beskrives den fremgangsmåde, som disse organisationer skal følge, når de opgraderer til Microsoft Dynamics 365 Operations version 1611."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7e0cd0c96ad0f30d56eefdc46a0a69160d864175
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a><span data-ttu-id="ae0aa-104">Opgradering for enkelt bilag og værdiregulering af valuta</span><span class="sxs-lookup"><span data-stu-id="ae0aa-104">Single voucher and currency revaluation upgrade</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ae0aa-105">Nogle organisationer angiver kladder, der indeholder et enkelt bilag, der har mere end én debitor eller kreditor, og de kører også processen til værdiregulering af udenlandsk valuta for debitorer eller kreditorer.</span><span class="sxs-lookup"><span data-stu-id="ae0aa-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="ae0aa-106">I dette emne beskrives den fremgangsmåde, som disse organisationer skal følge, når de opgraderer til Microsoft Dynamics 365 Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="ae0aa-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="ae0aa-107">Følg disse trin, når du opgraderer til Microsoft Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="ae0aa-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="ae0aa-108">Før du opgraderer til Dynamics 365 for Operations, skal du køre processerne til værdiregulering af udenlandsk valuta for debitorer og kreditorer.</span><span class="sxs-lookup"><span data-stu-id="ae0aa-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="ae0aa-109">Angiv feltet **Metode** til **Fakturadato**.</span><span class="sxs-lookup"><span data-stu-id="ae0aa-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="ae0aa-110">Der oprettes en værdireguleringspostering, der tilbagefører den sidste værdiregulering af udenlandsk valuta.</span><span class="sxs-lookup"><span data-stu-id="ae0aa-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="ae0aa-111">Derfor værdiansættes de åbne posteringer til deres oprindelige regnskabsvaluta.</span><span class="sxs-lookup"><span data-stu-id="ae0aa-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="ae0aa-112">Opgrader til Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="ae0aa-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="ae0aa-113">Kør processerne til værdiregulering af udenlandsk valuta for debitorer og kreditorer igen.</span><span class="sxs-lookup"><span data-stu-id="ae0aa-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="ae0aa-114">Denne gang skal feltet **Metode** angives til **Standard**.</span><span class="sxs-lookup"><span data-stu-id="ae0aa-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="ae0aa-115">Der oprettes en ny værdireguleringspostering, der er baseret på de aktuelle valutakurser.</span><span class="sxs-lookup"><span data-stu-id="ae0aa-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="ae0aa-116">Denne transaktion registrerer urealiseret gevinst eller tab og den korrekte samlefinanskonto.</span><span class="sxs-lookup"><span data-stu-id="ae0aa-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>





