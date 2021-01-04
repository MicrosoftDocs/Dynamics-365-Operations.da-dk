---
title: Afstemte kladder for regnskab mellem enheder
description: Denne artikel viser, hvordan en kladde automatisk afstemmes, når en udlignende økonomisk dimension er valgt på siden Finans.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e84d96b5467b38e07a9ed31f142c27b638289284
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441447"
---
# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="b8ba6-103">Afstemte kladder for regnskab mellem enheder</span><span class="sxs-lookup"><span data-stu-id="b8ba6-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8ba6-104">Denne artikel viser, hvordan en kladde automatisk afstemmes, når en udlignende økonomisk dimension er valgt på siden Finans.</span><span class="sxs-lookup"><span data-stu-id="b8ba6-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="b8ba6-105">Hvis kontoposter ikke afstemmes på samme niveau som de økonomiske dimensionsværdier, oprettes der automatisk flere poster for at afstemme kladden.</span><span class="sxs-lookup"><span data-stu-id="b8ba6-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="b8ba6-106">Disse kontoposter bruger bogføringstyperne **Internt mellem enheder - debet** og **Internt mellem enheder - kredit** på siden **Konti til automatisk posteringer** til at bestemme hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="b8ba6-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="b8ba6-107">Virksomhedsenhed, som er det andet segment på finanskontoen, vælges f.eks. som den afstemmende økonomiske dimension, og følgende regnskabsposter er ved at blive oprettet.</span><span class="sxs-lookup"><span data-stu-id="b8ba6-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="b8ba6-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="b8ba6-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="b8ba6-109">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="b8ba6-109">100.00 DR</span></span> |
| <span data-ttu-id="b8ba6-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="b8ba6-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="b8ba6-111">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="b8ba6-111">100.00 DR</span></span> |
| <span data-ttu-id="b8ba6-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="b8ba6-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="b8ba6-113">200,00 CR</span><span class="sxs-lookup"><span data-stu-id="b8ba6-113">200.00 CR</span></span> |

<span data-ttu-id="b8ba6-114">I så fald bestemmes følgende saldi:</span><span class="sxs-lookup"><span data-stu-id="b8ba6-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="b8ba6-115">Til forretningsenhed MSP = 100,00 CR</span><span class="sxs-lookup"><span data-stu-id="b8ba6-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="b8ba6-116">Til forretningsenhed NY = 100,00 DR</span><span class="sxs-lookup"><span data-stu-id="b8ba6-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="b8ba6-117">Følgende regnskabsposter oprettes derfor automatisk, så denne kladde afstemmes på niveauet for de økonomiske dimensionsværdier.</span><span class="sxs-lookup"><span data-stu-id="b8ba6-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="b8ba6-118">(Internt mellem enheder - debet) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="b8ba6-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="b8ba6-119">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="b8ba6-119">100.00 DR</span></span> |
| <span data-ttu-id="b8ba6-120">(Internt mellem enheder - kredit) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="b8ba6-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="b8ba6-121">100,00 CR</span><span class="sxs-lookup"><span data-stu-id="b8ba6-121">100.00 CR</span></span> |





