---
title: "Bogføringskonti for kassation af anlægsaktiver"
description: "I denne artikel beskrives det, hvordan du konfigurerer finansbogføringskonti ved kassation af anlægsaktiver."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0129eae177d44100b09c2b7bce553dd5bde5ce0c
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="89a01-103">Bogføringskonti for kassation af anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="89a01-103">Fixed asset disposal posting accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="89a01-104">I denne artikel beskrives det, hvordan du konfigurerer finansbogføringskonti ved kassation af anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="89a01-104">This article explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="89a01-105">På siden Posteringsprofiler for anlægsaktiver i oversigtspanelet Finanskonti skal du vælge Kassation - salg og Kassation - spild for at konfigurere bogføring til Finans.</span><span class="sxs-lookup"><span data-stu-id="89a01-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="89a01-106">I forbindelse med begge posteringstyper krediteres finanskontoen med anlægsaktivets kassationsværdi.</span><span class="sxs-lookup"><span data-stu-id="89a01-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="89a01-107">Debet bogføres på en modkonto, som f.eks. kan være en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="89a01-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="89a01-108">Hvis et anlægsaktiv sælges til en kunde, bruges debitorkontoen i stedet for modkontoen.</span><span class="sxs-lookup"><span data-stu-id="89a01-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="89a01-109">Klik på Kassation, klik på Salg eller Spil, og opret derefter detaljerede konti for at tilbageføre anlægsaktivets bogførte nettoværdi.</span><span class="sxs-lookup"><span data-stu-id="89a01-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="89a01-110">Du kan også angive oplysninger i felterne Efter-værdi og Salgsværdi på siden Kassationsparametre.</span><span class="sxs-lookup"><span data-stu-id="89a01-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="89a01-111">Kassationsposteringen for et aktiv i en pulje for småaktiver reducerer kun den bogførte nettoværdi af puljen for småaktiver med det beløbet for kassationen.</span><span class="sxs-lookup"><span data-stu-id="89a01-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="89a01-112">Hvis salget af aktivet overstiger den bogførte nettoværdi af puljen for småaktiver, nedskrives den bogførte nettoværdi til nul.</span><span class="sxs-lookup"><span data-stu-id="89a01-112">However, when the sale of an asset is exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>






