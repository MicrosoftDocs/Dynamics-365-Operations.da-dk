---
title: Afstemte kladder for regnskab mellem enheder
description: "Denne artikel viser, hvordan en kladde automatisk afstemmes, når en udlignende økonomisk dimension er valgt på siden Finans."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f45d180dc8dcafb0579e76b890dd5d516df5b8c0
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="8dca3-103">Afstemte kladder for regnskab mellem enheder</span><span class="sxs-lookup"><span data-stu-id="8dca3-103">Balanced journals for interunit accounting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8dca3-104">Denne artikel viser, hvordan en kladde automatisk afstemmes, når en udlignende økonomisk dimension er valgt på siden Finans.</span><span class="sxs-lookup"><span data-stu-id="8dca3-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="8dca3-105">Hvis kontoposter ikke afstemmes på samme niveau som de økonomiske dimensionsværdier, oprettes der automatisk flere poster for at afstemme kladden.</span><span class="sxs-lookup"><span data-stu-id="8dca3-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="8dca3-106">Disse kontoposter bruger bogføringstyperne **Internt mellem enheder - debet** og **Internt mellem enheder - kredit** på siden **Konti til automatisk posteringer** til at bestemme hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="8dca3-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="8dca3-107">Afdeling, som er det andet segment på finanskontoen, vælges f.eks. som den afstemmende økonomiske dimension, og følgende regnskabsposter er ved at blive oprettet.</span><span class="sxs-lookup"><span data-stu-id="8dca3-107">For example, Branch, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="8dca3-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="8dca3-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="8dca3-109">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="8dca3-109">100.00 DR</span></span> |
| <span data-ttu-id="8dca3-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="8dca3-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="8dca3-111">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="8dca3-111">100.00 DR</span></span> |
| <span data-ttu-id="8dca3-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="8dca3-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="8dca3-113">200,00 CR</span><span class="sxs-lookup"><span data-stu-id="8dca3-113">200.00 CR</span></span> |

<span data-ttu-id="8dca3-114">I så fald bestemmes følgende saldi:</span><span class="sxs-lookup"><span data-stu-id="8dca3-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="8dca3-115">For afdelingen MSP = 100,00 CR</span><span class="sxs-lookup"><span data-stu-id="8dca3-115">For Branch MSP = 100.00 CR</span></span>
-   <span data-ttu-id="8dca3-116">For afdelingen NY = 100,00 DR</span><span class="sxs-lookup"><span data-stu-id="8dca3-116">For Branch NY = 100.00 DR</span></span>

<span data-ttu-id="8dca3-117">Følgende regnskabsposter oprettes derfor automatisk, så denne kladde afstemmes på niveauet for de økonomiske dimensionsværdier.</span><span class="sxs-lookup"><span data-stu-id="8dca3-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="8dca3-118">(Internt mellem enheder - debet) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="8dca3-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="8dca3-119">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="8dca3-119">100.00 DR</span></span> |
| <span data-ttu-id="8dca3-120">(Internt mellem enheder - kredit) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="8dca3-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="8dca3-121">100,00 CR</span><span class="sxs-lookup"><span data-stu-id="8dca3-121">100.00 CR</span></span> |






