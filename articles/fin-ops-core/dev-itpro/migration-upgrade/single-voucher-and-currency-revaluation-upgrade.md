---
title: Opgradere enkeltbilagskladder og værdireguleringer af valuta
description: Dette emne beskriver, hvordan du opgraderer enkeltbilagskladder og værdireguleringer af valuta.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fb4eca4933716105789d3bbc21dd374395211d1d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559515"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="86a9e-103">Opgradere enkeltbilagskladder og værdireguleringer af valuta</span><span class="sxs-lookup"><span data-stu-id="86a9e-103">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86a9e-104">Nogle organisationer angiver kladder, der indeholder et enkelt bilag, der har mere end én debitor eller kreditor, og de kører også processen til værdiregulering af udenlandsk valuta for debitorer eller kreditorer.</span><span class="sxs-lookup"><span data-stu-id="86a9e-104">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="86a9e-105">I dette emne beskrives den fremgangsmåde, som disse organisationer skal følge, når de opgraderer til Microsoft Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="86a9e-105">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="86a9e-106">Følg disse trin, når du opgraderer til Microsoft Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="86a9e-106">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="86a9e-107">Før du opgraderer til Finance and Operations, skal du køre processerne til værdiregulering af udenlandsk valuta for debitorer og kreditorer.</span><span class="sxs-lookup"><span data-stu-id="86a9e-107">Before you upgrade to Finance and Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="86a9e-108">Angiv feltet **Metode** til **Fakturadato**.</span><span class="sxs-lookup"><span data-stu-id="86a9e-108">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="86a9e-109">Der oprettes en værdireguleringspostering, der tilbagefører den sidste værdiregulering af udenlandsk valuta.</span><span class="sxs-lookup"><span data-stu-id="86a9e-109">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="86a9e-110">Derfor værdiansættes de åbne posteringer til deres oprindelige regnskabsvaluta.</span><span class="sxs-lookup"><span data-stu-id="86a9e-110">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="86a9e-111">Opgrader til version 1611.</span><span class="sxs-lookup"><span data-stu-id="86a9e-111">Upgrade to version 1611.</span></span>
3.  <span data-ttu-id="86a9e-112">Kør processerne til værdiregulering af udenlandsk valuta for debitorer og kreditorer igen.</span><span class="sxs-lookup"><span data-stu-id="86a9e-112">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="86a9e-113">Denne gang skal feltet **Metode** angives til **Standard**.</span><span class="sxs-lookup"><span data-stu-id="86a9e-113">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="86a9e-114">Der oprettes en ny værdireguleringspostering, der er baseret på de aktuelle valutakurser.</span><span class="sxs-lookup"><span data-stu-id="86a9e-114">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="86a9e-115">Denne transaktion registrerer urealiseret gevinst eller tab og den korrekte samlefinanskonto.</span><span class="sxs-lookup"><span data-stu-id="86a9e-115">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]