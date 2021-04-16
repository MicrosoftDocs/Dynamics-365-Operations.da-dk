---
title: Global A-skat
description: Dette emne indeholder oplysninger om den globale funktion for A-skat og opsætningen af den. Funktionen til global A-skat er forbedret for leverandør- og debitorposteringer, så A-skat beregnes på vareniveau.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 9a73d34fb4fbf007cbb5a996cfa6e9719532869c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826660"
---
# <a name="global-withholding-tax"></a><span data-ttu-id="1a3f6-104">Global A-skat</span><span class="sxs-lookup"><span data-stu-id="1a3f6-104">Global withholding tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a3f6-105">Dette emne indeholder oplysninger om den globale funktion for A-skat og forklarer opsætningen af den.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-105">This topic provides information about global withholding tax functionality and explains how to set it up.</span></span> <span data-ttu-id="1a3f6-106">Den nye funktionalitet er tilgængelig i version 10.0.17 og nyere.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-106">The new functionality is available in version 10.0.17 and later.</span></span>

<span data-ttu-id="1a3f6-107">Funktionen til global A-skat er forbedret for leverandør- og debitorposteringer, så A-skat beregnes på vareniveau.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-107">Global withholding tax functionality is enhanced for vendor and customer transactions, so that withholding tax is calculated at the item level.</span></span> <span data-ttu-id="1a3f6-108">Saldoen på kontoen for A-skat fra købsposteringer kan udlignes ved at køre betalingsjobbet for A-skat mod afregningskontoen for A-skat.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-108">The balance in the withholding tax account from purchase transactions can be settled by running the withholding tax payment job against the withholding tax settlement account.</span></span>

> [!NOTE]
> <span data-ttu-id="1a3f6-109">Global A-skat understøtter ikke funktionen **Vedligehold gebyrer** på indkøbsordre-, kreditorfaktura- og salgsordresiderne.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-109">Global withholding tax doesn't support the **Maintain charges** function on the purchase order, vendor invoice, and sales order pages.</span></span>

## <a name="turn-on-global-withholding-tax"></a><span data-ttu-id="1a3f6-110">Aktivere global A-skat</span><span class="sxs-lookup"><span data-stu-id="1a3f6-110">Turn on global withholding tax</span></span>

1. <span data-ttu-id="1a3f6-111">I området **Funktionsstyring** skal du vælge **Global A-skat** og derefter **Aktivér nu**.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-111">In the **Feature management** workspace, select **Global withholding tax**, and then select **Enable now**.</span></span>
2. <span data-ttu-id="1a3f6-112">Gå til **Moms \> Opsætning \> Parametre \> Finansparametre**, og under fanen **A-skat** skal du angive **Ja** option to **Aktiver global A-skat**.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-112">Go to **Tax \> Setup \> Parameters \> General ledger parameters**, and then, on the **Withholding tax** tab, set the **Enable global withholding tax** option to **Yes**.</span></span>
3. <span data-ttu-id="1a3f6-113">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-113">Select **Save**.</span></span>
4. <span data-ttu-id="1a3f6-114">Opdater siden i webbrowseren.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-114">Refresh the page in your web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="1a3f6-115">Funktioner for global A-skat kan ikke være aktiveret for lande/områder, hvor der allerede findes lokale løsninger for A-skat.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-115">Global withholding tax functionality can’t be turned on for countries/regions where localized withholding tax solutions already exist.</span></span> <span data-ttu-id="1a3f6-116">Disse områder omfatter, men er ikke begrænset til Indien, Brasilien, Thailand, Saudi-Arabien, Irland, Storbritannien og USA.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-116">These areas include but are not restricted to India, Brazil, Thailand, Saudi Arabia, Ireland, Great Britain and the United States.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]