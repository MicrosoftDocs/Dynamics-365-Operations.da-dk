---
title: Anlægsaktiver i den offentlige sektor
description: I denne artikel beskrives de funktioner til anlægsaktiver, der er tilgængelige for den offentlige sektor.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTransfer
audience: Application User
ms.reviewer: roschlom
ms.custom: 20891
ms.assetid: 552c7969-f044-4774-82ec-080aeae8cf3f
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e521243684d5ff3dd0ff643b53b769e26245204
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258157"
---
# <a name="fixed-assets-in-the-public-sector"></a><span data-ttu-id="ad0c3-103">Anlægsaktiver i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="ad0c3-103">Fixed assets in the public sector</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad0c3-104">I denne artikel beskrives de funktioner til anlægsaktiver, der er tilgængelige for den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-104">This article describes the fixed assets functionality that is available for public sector.</span></span> 

<a name="what-do-i-need-to-know-about-disposing-of-fixed-assets"></a><span data-ttu-id="ad0c3-105">Værd at vide om salg af anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="ad0c3-105">What do I need to know about disposing of fixed assets?</span></span>
-------------------------------------------------------

<span data-ttu-id="ad0c3-106">Offentlige organisationer kan bruge spild og salgsforslag til at råde over mere end et enkelt anlægsaktiv ad gangen.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-106">Public sector organizations can use scrap and sales proposals to dispose of more than one fixed asset at a time.</span></span>

## <a name="why-do-i-have-to-enter-transfer-from-and-transfer-to-accounts-when-i-transfer-fixed-assets-between-funds"></a><span data-ttu-id="ad0c3-107">Hvorfor er det nødvendigt at angive Overflyt fra og Overflyt til konti, når jeg overfører anlægsaktiver mellem midler?</span><span class="sxs-lookup"><span data-stu-id="ad0c3-107">Why do I have to enter transfer-from and transfer-to accounts when I transfer fixed assets between funds?</span></span>
<span data-ttu-id="ad0c3-108">Offentlige organisationer kræver typisk afstemte poster for den økonomiske dimension, der bruges til at angive midler.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-108">Public sector organizations typically require balanced entries for the financial dimension used to designate funds.</span></span> <span data-ttu-id="ad0c3-109">Når du overfører anlægsaktiver mellem midler, og middeldimensionen kræver afstemte poster, er felterne Overflyt fra og Overflyt til-konto på siden til aktivoverførsel påkrævet.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-109">When you transfer fixed assets between funds, if the fund dimension requires balanced entries, the transfer-from and transfer-to account fields on the asset transfer page are required.</span></span> 

> [!NOTE] 
> <span data-ttu-id="ad0c3-110">Dette er ikke en egenskab ved anlægsaktiver eller midler.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-110">This is not a property of fixed assets or of funds.</span></span> <span data-ttu-id="ad0c3-111">Det er derimod en egenskab for den økonomiske dimension.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-111">Rather, it’s a property of the financial dimension.</span></span> <span data-ttu-id="ad0c3-112">Når du overfører et anlægsaktiv, og økonomiske dimensioner, som er tilknyttet aktivet, kræver afstemte poster, er Overflyt fra og Overflyt til-konto påkrævet.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-112">When you transfer a fixed asset, if any financial dimension associated with the asset requires balanced entries, the transfer-from and transfer-to accounts are required.</span></span> 

<span data-ttu-id="ad0c3-113">Overflyt fra og Overflyt til-konti er ikke de konti, hvor anlægsaktivets bogførte nettoværdi er indeholdt.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-113">The transfer-from and transfer-to accounts are not the accounts in which the fixed asset’s net book value is held.</span></span> <span data-ttu-id="ad0c3-114">Overflyt fra og Overflyt til-kontiene er derimod de hovedkonti, der bruges til at afstemme poster i økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-114">Rather, the transfer-from and transfer-to accounts are the main accounts used to balance entries in financial dimensions.</span></span> <span data-ttu-id="ad0c3-115">De bruges kun, når en økonomisk dimension for anlægsaktivet kræver afstemning.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-115">They are used only when a financial dimension for the fixed asset requires balancing.</span></span> <span data-ttu-id="ad0c3-116">Overfør fra-kontoen har en debetpost, og overfør til-kontoen har en kreditpost.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-116">The transfer-from account will have a debit entry, and the transfer-to account will have a credit entry.</span></span>

<span data-ttu-id="ad0c3-117">Du kan få flere oplysninger i [Midler i den offentlige sektor](funds-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="ad0c3-117">For details, see [Funds in the public sector](funds-public-sector.md).</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]