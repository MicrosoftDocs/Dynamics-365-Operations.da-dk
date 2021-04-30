---
title: Økonomiske dimensionsopsætninger
description: I dette emne beskrives økonomiske dimensionsopsætninger, og du kan få tip til optimering af deres brug.
author: yukonpeegs
manager: AnnBe
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b719d8eb868cb1722b470be4443d01181078ce21
ms.sourcegitcommit: 97ada5d52ed1829dcf030dad254096cd8df25da8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/06/2021
ms.locfileid: "5864406"
---
# <a name="financial-dimension-sets"></a><span data-ttu-id="b38fb-103">Økonomiske dimensionsopsætninger</span><span class="sxs-lookup"><span data-stu-id="b38fb-103">Financial dimension sets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b38fb-104">I dette emne beskrives økonomiske dimensionsopsætninger, og du kan få tip til optimering af deres brug.</span><span class="sxs-lookup"><span data-stu-id="b38fb-104">This topic describes financial dimension sets and provides some tips for optimizing their use.</span></span>

<span data-ttu-id="b38fb-105">En dimensionsopsætning er en ordnet liste over økonomiske dimensioner, der kan bruges til at opsummere finansdata på en brugerdefineret måde.</span><span class="sxs-lookup"><span data-stu-id="b38fb-105">A dimension set is an ordered list of financial dimensions that can be used to summarize General ledger data in a user-defined way.</span></span> <span data-ttu-id="b38fb-106">Dimensionssæt bruges primært til at definere en råbalance.</span><span class="sxs-lookup"><span data-stu-id="b38fb-106">A primary use of dimension sets is to define a trial balance.</span></span>

<span data-ttu-id="b38fb-107">Den eneste standarddimensionsopsætning er den dimensionsopsætning, der kun indeholder hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="b38fb-107">The only standard dimension set is the dimension set that contains only the main account.</span></span>

<span data-ttu-id="b38fb-108">Du kan bruge siden **Økonomiske dimensionsopsætninger** til at oprette og administrere økonomiske dimensionsopsætninger.</span><span class="sxs-lookup"><span data-stu-id="b38fb-108">You use the **Financial dimension sets** page to create and manage financial dimension sets.</span></span>

## <a name="dimension-set-balances"></a><span data-ttu-id="b38fb-109">Saldi for dimensionsopsætninger</span><span class="sxs-lookup"><span data-stu-id="b38fb-109">Dimension set balances</span></span>

<span data-ttu-id="b38fb-110">En dimensionsopsætning kan have saldi, der er baseret på dens økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="b38fb-110">A dimension set can have balances that are based on its financial dimensions.</span></span> <span data-ttu-id="b38fb-111">Saldi findes i Finans og er baseret på definitionen af dimensionsopsætning.</span><span class="sxs-lookup"><span data-stu-id="b38fb-111">The balances exist in General ledger and are based on the dimension set definition.</span></span> <span data-ttu-id="b38fb-112">Saldi opsummeres ud fra finansdataene for at forbedre ydeevnen, når de hentes (f.eks. når der genereres en råbalance).</span><span class="sxs-lookup"><span data-stu-id="b38fb-112">The balances are summarized from the General ledger data to help improve performance when they are retrieved (for example, when a trial balance is generated).</span></span>

## <a name="create-balances"></a><span data-ttu-id="b38fb-113">Oprette saldi</span><span class="sxs-lookup"><span data-stu-id="b38fb-113">Create balances</span></span>

<span data-ttu-id="b38fb-114">Brug knappen **Opret saldi** til at initialisere saldi for en dimensionsopsætning, der ikke aktuelt har saldi.</span><span class="sxs-lookup"><span data-stu-id="b38fb-114">Use the **Create balances** button to initialize the balances for a dimension set that doesn't currently have balances.</span></span>

> [!NOTE]
> <span data-ttu-id="b38fb-115">Det anbefales, at du begrænser antallet af dimensionsopsætninger, der har saldi, da saldoopdateringer påvirker alle finanskonteringsaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="b38fb-115">We recommend that you limit the number of dimension sets that have balances, because balance updates affect all General ledger posting activities.</span></span>

## <a name="update-balances"></a><span data-ttu-id="b38fb-116">Opdatere saldi</span><span class="sxs-lookup"><span data-stu-id="b38fb-116">Update balances</span></span>

<span data-ttu-id="b38fb-117">Brug knappen **Opdater saldi** til at medtage den seneste finanskonteringsaktivitet i saldi.</span><span class="sxs-lookup"><span data-stu-id="b38fb-117">Use the **Update balances** button to include the latest General ledger posting activity in the balances.</span></span> <span data-ttu-id="b38fb-118">Saldoopdateringer er lette operationer.</span><span class="sxs-lookup"><span data-stu-id="b38fb-118">Balance updates are light operations.</span></span> <span data-ttu-id="b38fb-119">De skal kun behandle den finanskonteringsaktivitet, der er opstået efter den seneste opdatering.</span><span class="sxs-lookup"><span data-stu-id="b38fb-119">They must process only the General ledger posting activity that has occurred since the last update.</span></span>

> [!NOTE]
> <span data-ttu-id="b38fb-120">Visningen af råbalancen fremtvinger en opdatering for at sikre, at de viste saldi er aktuelle.</span><span class="sxs-lookup"><span data-stu-id="b38fb-120">Display of the trial balance forces an update, to ensure that the balances that are shown are current.</span></span> <span data-ttu-id="b38fb-121">Overvej at bruge et tilbagevendende batchjob, så opdateringer af de ofte anvendte dimensionsopsætninger sker hurtigt.</span><span class="sxs-lookup"><span data-stu-id="b38fb-121">Consider using a recurring batch job so that updates to your most frequently used dimension sets are quick.</span></span> <span data-ttu-id="b38fb-122">På den måde er du med til at minimere den tid, som brugere af råbalance skal vente.</span><span class="sxs-lookup"><span data-stu-id="b38fb-122">In this way, you help minimize the time that trial balance users must wait.</span></span>

## <a name="rebuild-balances"></a><span data-ttu-id="b38fb-123">Gendanne saldi</span><span class="sxs-lookup"><span data-stu-id="b38fb-123">Rebuild balances</span></span>

<span data-ttu-id="b38fb-124">Du kan bruge knappen **Gendan saldi** til at gendanne saldi fra bunden.</span><span class="sxs-lookup"><span data-stu-id="b38fb-124">Use the **Rebuild balances** button to re-create the balances from scratch.</span></span> <span data-ttu-id="b38fb-125">På denne måde er du med til at sikre, at de svarer til dataene i Finans.</span><span class="sxs-lookup"><span data-stu-id="b38fb-125">In this way, you help ensure that they match the data in General ledger.</span></span> <span data-ttu-id="b38fb-126">En gendannelse af saldi kræver masser af behandling og bør normalt ikke være påkrævet.</span><span class="sxs-lookup"><span data-stu-id="b38fb-126">A rebuild of balances requires lots of processing and should not usually be required.</span></span>

> [!NOTE]
> <span data-ttu-id="b38fb-127">Hvis du har et scenario, der jævnligt kræver en gendannelse af saldi, anbefales det, at du kontakter kundesupport.</span><span class="sxs-lookup"><span data-stu-id="b38fb-127">If you have a scenario that regularly requires a rebuild of balances, we recommend that you contact customer support.</span></span> <span data-ttu-id="b38fb-128">Kundesupport kan hjælpe dig med at finde ud af, hvorfor saldi ikke stemmer overens med dataene i Finans.</span><span class="sxs-lookup"><span data-stu-id="b38fb-128">Customer support can help you determine why balances don't match the data in General ledger.</span></span>

## <a name="clear-balances"></a><span data-ttu-id="b38fb-129">Afstemme saldi</span><span class="sxs-lookup"><span data-stu-id="b38fb-129">Clear balances</span></span>

<span data-ttu-id="b38fb-130">Brug knappen **Afstem saldi** til at fjerne saldi og stoppe eventuelle yderligere opdateringer.</span><span class="sxs-lookup"><span data-stu-id="b38fb-130">Use the **Clear balances** button to remove the balances and stop any further updates.</span></span> <span data-ttu-id="b38fb-131">Dimensionsopsætningen har ikke længere indflydelse på bogføringsaktiviteterne i Finans.</span><span class="sxs-lookup"><span data-stu-id="b38fb-131">The dimension set will no longer have an impact on General ledger posting activities.</span></span>

<span data-ttu-id="b38fb-132">Du kan finde flere oplysninger under [Økonomiske dimensioner](financial-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="b38fb-132">For more information, see [Financial dimensions](financial-dimensions.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
