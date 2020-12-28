---
title: " Definere bonuspoint for fordelskunde"
description: Denne procedure gennemgår definition af fordelskundebelønningspoint.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e40ebcbf3ab1befc641ae34571a8b974bd0425a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411123"
---
# <a name="define-loyalty-reward-points"></a><span data-ttu-id="d4ec2-103"> Definere bonuspoint for fordelskunde</span><span class="sxs-lookup"><span data-stu-id="d4ec2-103">Define loyalty reward points</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4ec2-104">Denne procedure gennemgår definition af fordelskundebelønningspoint.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-104">This procedure walks through defining loyalty reward points.</span></span> <span data-ttu-id="d4ec2-105">Du bør definere fordelskundebelønningspoint, før du konfigurerer et fordelskundeprogram.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-105">You should set up loyalty reward points before you set up a loyalty program.</span></span> <span data-ttu-id="d4ec2-106">Proceduren bruger USRT-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="d4ec2-107">Gå til Retail og Commerce > Kunder > Loyalitet > Fordelskundebelønningspoint.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-107">Go to Retail and Commerce > Customers > Loyalty > Loyalty reward points.</span></span>
2. <span data-ttu-id="d4ec2-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-108">Click New.</span></span>
3. <span data-ttu-id="d4ec2-109">Indtast en værdi i feltet Belønningspoint-id.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-109">In the Reward point ID field, type a value.</span></span>
4. <span data-ttu-id="d4ec2-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d4ec2-111">Vælg en indstilling i feltet Belønningspointtype.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-111">In the Reward point type field, select an option.</span></span>
    * <span data-ttu-id="d4ec2-112">Vælg antal, hvis belønningspointene skal afrundes til nærmeste heltal.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-112">Select Quantity if you want the reward points to be rounded to the nearest integer.</span></span> <span data-ttu-id="d4ec2-113">Vælg Beløb, hvis belønningspointene skal afrundes i overensstemmelse med reglerne for valutaafrunding.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-113">Select Amount if you want the reward points to be rounded according to currency rounding rules.</span></span> <span data-ttu-id="d4ec2-114">Hvis du vælger Antal, kan du springe næste trin i denne procedure over.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-114">If you select Quantity, skip the next step of this procedure..</span></span>  
6. <span data-ttu-id="d4ec2-115">Skriv en værdi i feltet Valuta.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-115">In the Currency field, type a value.</span></span>
    * <span data-ttu-id="d4ec2-116">For belønningspoint af typen Beløb får alle udstedte point den valgte valuta.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-116">For Amount type reward points, all points issued will have the selected currency.</span></span> <span data-ttu-id="d4ec2-117">For belønningspoint af typen Antal gælder dette felt ikke. Spring dette trin over.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-117">For Quantity type reward points, this field doesn't apply—skip this step.</span></span>  
7. <span data-ttu-id="d4ec2-118">Markér eller fjern markeringen af afkrydsningsfeltet Kan indløses.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-118">Check or uncheck the Redeemable checkbox.</span></span>
8. <span data-ttu-id="d4ec2-119">Angiv et tal i feltet Indløs rangering.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-119">In the Redeem ranking field, enter a number.</span></span>
    * <span data-ttu-id="d4ec2-120">Indløs rangering bruges, når to eller flere indløselige belønningspoint kan bruges til at betale for produkter.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-120">Redeem ranking is used when two or more redeemable reward points can be used to pay for products.</span></span> <span data-ttu-id="d4ec2-121">Hvis to belønningspoint har samme indløsningsrangering, anvendes det, der skal sænke antallet af point.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-121">If the two reward points have the same redeem ranking, then the one that needs to lower number of points will be used.</span></span>  
9. <span data-ttu-id="d4ec2-122">Angiv et tal i feltet Værdi for udløbstidspunkt.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-122">In the Expiration time value field, enter a number.</span></span>
    * <span data-ttu-id="d4ec2-123">Belønningspoint udløber det angivne antal dage, måneder eller år efter, at pointene blev udstedt.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-123">The reward points will expire the specified number of days, months, or years after when the points are issued.</span></span> <span data-ttu-id="d4ec2-124">En værdi på "0" betyder, at fordelskundebelønningspoint aldrig udløber.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-124">A value of '0' means the loyalty reward points will never expire.</span></span>  
10. <span data-ttu-id="d4ec2-125">Vælg en indstilling i feltet Enhed for udløbstidspunkt.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-125">In the Expiration time unit field, select an option.</span></span>
11. <span data-ttu-id="d4ec2-126">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d4ec2-126">Click Save.</span></span>

