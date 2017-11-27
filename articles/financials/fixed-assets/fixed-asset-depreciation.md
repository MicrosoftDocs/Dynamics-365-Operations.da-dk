---
title: "Afskrivning af anlægsaktiv"
description: "Dette emne indeholder en oversigt over afskrivning af anlægsaktiver."
author: twheeloc
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e362d80f5c4a33ad604c717333777e7c5fdef489
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="fixed-asset-depreciation"></a><span data-ttu-id="b5f2a-103">Afskrivning af anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="b5f2a-103">Fixed asset depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b5f2a-104">Dette emne indeholder en oversigt over afskrivning af anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-104">This topic provides an overview of depreciation for fixed assets.</span></span>

<span data-ttu-id="b5f2a-105">Afskrivning er en periodisk transaktion, der normalt reducerer anlægsaktivets værdi i balancen og faktureres som en udgift på driftskontoen (resultatopgørelsen).</span><span class="sxs-lookup"><span data-stu-id="b5f2a-105">Depreciation is a periodic transaction that typically reduces the value of the fixed asset on the balance sheet, and is charged as an expenditure to a profit and loss account.</span></span> <span data-ttu-id="b5f2a-106">Derfor bruges en hovedkonto normalt til kreditering af den periodiske afskrivning i balancen.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-106">Therefore, a main account is typically used to credit the periodic depreciation on the balance sheet.</span></span> <span data-ttu-id="b5f2a-107">En modkonto er en konto på driftskontodelen af kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-107">An offset account is an account in the profit and loss part of the chart of accounts.</span></span>

## <a name="depreciation-adjustment"></a><span data-ttu-id="b5f2a-108">Afskrivningsregulering</span><span class="sxs-lookup"><span data-stu-id="b5f2a-108">Depreciation adjustment</span></span>
<span data-ttu-id="b5f2a-109">Normalt er det kun en regulering af en allerede bogført afskrivningspostering, der bogføres som en afskrivningsjustering.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-109">Usually, only a correction to a posted depreciation transaction is posted as a depreciation adjustment.</span></span> <span data-ttu-id="b5f2a-110">Derfor er både hovedkontoen og modkontoen konfigureret som konti til afskrivning.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-110">Therefore, both the main account and the offset account are set up just like the accounts for depreciation.</span></span> <span data-ttu-id="b5f2a-111">En afskrivningsregulering kan være et positivt eller negativt beløb, men funktionen af hovedkontoen (som en statuskonto) og funktionen af modkontoen (normalt som en driftskonto) forbliver den samme.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-111">A depreciation adjustment can be either a positive amount or a negative amount, but the functionality of the main account (as a balance sheet account) and the functionality of the offset account (usually as a profit and loss account) remain the same.</span></span>

## <a name="extraordinary-depreciation"></a><span data-ttu-id="b5f2a-112">Ekstraordinær afskrivning</span><span class="sxs-lookup"><span data-stu-id="b5f2a-112">Extraordinary depreciation</span></span>
<span data-ttu-id="b5f2a-113">Ekstraordinær afskrivning fungerer ligesom grundlæggende afskrivning.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-113">Extraordinary depreciation works like basic depreciation.</span></span> <span data-ttu-id="b5f2a-114">Derfor bruges en hovedkonto til kreditering af afskrivningsbeløbet på balancen og reducering af værdien af anlægsaktivet.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-114">Therefore, a main account is used to credit the depreciation amount to the balance sheet and reduce the value of the fixed asset.</span></span> <span data-ttu-id="b5f2a-115">En modkonto er en driftskonto, hvor den afskrivning, der beregnes for regnskabsperioden, opkræves som en udgift.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-115">An offset account is a profit and loss account, where the depreciation that is calculated for the fiscal period is charged as an expenditure.</span></span> 

<span data-ttu-id="b5f2a-116">Ekstraordinær afskrivning fungerer uafhængigt af grundlæggende afskrivning.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-116">Extraordinary depreciation works independently of basic depreciation.</span></span> <span data-ttu-id="b5f2a-117">Fordi ekstraordinær afskrivning er en separat posteringstype, kan du bogføre og rapportere ekstraordinær afskrivning separat fra den grundlæggende afskrivning.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-117">By having extraordinary depreciation as a separate transaction type, you can post and report the extraordinary depreciation separately from the basic depreciation.</span></span>

## <a name="special-depreciation-allowance"></a><span data-ttu-id="b5f2a-118">Særlig afskrivning</span><span class="sxs-lookup"><span data-stu-id="b5f2a-118">Special depreciation allowance</span></span>
<span data-ttu-id="b5f2a-119">Du kan bruge særlig afskrivning til ekstraafskrivningsbeløb det første år, hvor et anlægsaktiv tages i anvendelse og afskrives.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-119">You can use special depreciation allowances to take extra depreciation amounts during the first year that an asset is put in service and depreciated.</span></span> <span data-ttu-id="b5f2a-120">Særlig afskrivning skal foretages før eventuelle andre afskrivningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-120">Special depreciation allowances must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="b5f2a-121">Da særlige afskrivninger ofte er ukendt indtil senere i den samlede levetid for anlægsaktivet, er det bedst at bruge denne type afskrivning med en bog, der ikke bogføres i finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-121">Because special depreciation allowances are often unknown until later in the service life of the fixed asset, it's best to use this type of depreciation with a book that doesn't post to the general ledger.</span></span> <span data-ttu-id="b5f2a-122">Du kan bruge indstillingen Slet transaktioner, der ikke er bogført i Finans til at slette transaktionshistorikken for disse bøger.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-122">You can use the Delete transactions not posted to general ledger periodic function to delete the transaction history for these books.</span></span> <span data-ttu-id="b5f2a-123">Du kan derefter slette afskrivningshistorikken for anlægsaktivets bog, bogføre den særlige afskrivning, når den er kendt, og derefter bogføre de resterende afskrivningsposteringer for året.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-123">You can then delete the depreciation history for the fixed asset book, post the special depreciation allowance when it's known, and then post the remaining depreciation transactions for the year.</span></span> 

<span data-ttu-id="b5f2a-124">Du kan oprette et ubegrænset antal poster for særlig afskrivning.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-124">You can create an unlimited number of special depreciation allowance records.</span></span> <span data-ttu-id="b5f2a-125">Når du har tildelt aktivgruppebogen disse poster, anvendes de i aktivbogen.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-125">After you assign those records to an asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="b5f2a-126">Særlig afskrivning angives som enten en procentsats eller et fast beløb.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-126">A special depreciation allowance is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="b5f2a-127">Når du bogfører afskrivningsforslag, bogføres posteringerne for særlig afskrivning i bogen som posteringer, der er adskilt fra afskrivningsposteringer.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-127">When you post depreciation proposals, special depreciation allowance transactions are posted to the book as transactions that are separate from the depreciation transactions.</span></span>

## <a name="depreciation-calendars"></a><span data-ttu-id="b5f2a-128">Afskrivningskalendere</span><span class="sxs-lookup"><span data-stu-id="b5f2a-128">Depreciation calendars</span></span>
<span data-ttu-id="b5f2a-129">Hver bog har en kalender, der bruges ved afskrivning af anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-129">Each book has a calendar that is used when you depreciate fixed assets.</span></span> <span data-ttu-id="b5f2a-130">Hvis du ikke angiver en kalender på bogen, bruger bogen som standard finansregnskabskalenderen.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-130">By default, if you don't indicate a calendar on the book, the book uses the ledger fiscal calendar.</span></span> <span data-ttu-id="b5f2a-131">Du skal vælge en regnskabskalender til en bog, når den afskrivningsprofil, der er knyttet til bogen, bruger et regnskabsmæssigt afskrivningsår.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-131">You must select a fiscal calendar for a book when the depreciation profile that is associated with the book uses a fiscal depreciation year.</span></span> 

<span data-ttu-id="b5f2a-132">Du kan oprette delte kalendere ved hjælp af siden **Regnskabskalendere** i Finans.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-132">You can create shared calendars by using the **Fiscal calendars** page in General ledger.</span></span>

<span data-ttu-id="b5f2a-133">Du kan finde flere oplysninger under [Afskrivningsmetoder og -principper](depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="b5f2a-133">For more information, see [Depreciation methods and conventions](depreciation-methods-conventions.md).</span></span>




