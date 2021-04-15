---
title: " Behandle reguleringer for kundefordelsbonuspoint"
description: Denne procedure viser, hvordan du søger efter oplysninger om fordelskundekort og regulerer fordelskundebelønningspoint.
author: scott-tucker
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailLoyaltyCards, RetailLoyaltyCardRewardPointTrans, RetailLoyaltyCardRewardPointAdjustment, RetailAffiliationLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7eae943985cc2bd706c0c3c4ec7b0470e3a54bff
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802617"
---
# <a name="process-loyalty-reward-point-adjustments"></a><span data-ttu-id="a72df-103"> Behandle reguleringer for kundefordelsbonuspoint</span><span class="sxs-lookup"><span data-stu-id="a72df-103">Process loyalty reward point adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a72df-104">Denne procedure viser, hvordan du søger efter oplysninger om fordelskundekort og regulerer fordelskundebelønningspoint.</span><span class="sxs-lookup"><span data-stu-id="a72df-104">This procedure demonstrates how to look up loyalty card information and adjust loyalty reward points.</span></span> <span data-ttu-id="a72df-105">Det demodatafirma, der bruges til at oprette denne opgave, er USRT.</span><span class="sxs-lookup"><span data-stu-id="a72df-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="a72df-106">Denne opgave er beregnet til Commerce-rollen som driftschef eller en Kundeservicechef-rolle.</span><span class="sxs-lookup"><span data-stu-id="a72df-106">This task is intended for the Commerce operations manager role or a Customer service manager role.</span></span>

1. <span data-ttu-id="a72df-107">Gå til Fordelskundekort.</span><span class="sxs-lookup"><span data-stu-id="a72df-107">Go to Loyalty cards.</span></span>
2. <span data-ttu-id="a72df-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="a72df-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a72df-109">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a72df-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a72df-110">Klik på Korttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="a72df-110">Click Card transactions.</span></span>
    * <span data-ttu-id="a72df-111">På denne side kan du se alle fordelskundetransaktioner for det valgte fordelskundekort.</span><span class="sxs-lookup"><span data-stu-id="a72df-111">On this page you can view all loyalty transactions for the selected loyalty card.</span></span>  
5. <span data-ttu-id="a72df-112">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a72df-112">Close the page.</span></span>
6. <span data-ttu-id="a72df-113">Klik på Kortreguleringer.</span><span class="sxs-lookup"><span data-stu-id="a72df-113">Click Card adjustments.</span></span>
7. <span data-ttu-id="a72df-114">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a72df-114">Click New.</span></span>
8. <span data-ttu-id="a72df-115">Indtast eller vælg en værdi i feltet Belønningspoint.</span><span class="sxs-lookup"><span data-stu-id="a72df-115">In the Reward point field, enter or select a value.</span></span>
9. <span data-ttu-id="a72df-116">Indtast et tal i feltet Beløb eller antal.</span><span class="sxs-lookup"><span data-stu-id="a72df-116">In the Amount or quantity field, enter a number.</span></span>
    * <span data-ttu-id="a72df-117">Du kan tilføje eller fjerne punkter fra fordelskundekortet ved hjælp af positive eller negative beløb.</span><span class="sxs-lookup"><span data-stu-id="a72df-117">You can add or remove points from the loyalty card by using positive or negative amounts.</span></span>  
10. <span data-ttu-id="a72df-118">Indtast eller vælg en værdi i feltet Fordelskundeprogram.</span><span class="sxs-lookup"><span data-stu-id="a72df-118">In the Loyalty program field, enter or select a value.</span></span>
11. <span data-ttu-id="a72df-119">Skriv en værdi i feltet Kommentar.</span><span class="sxs-lookup"><span data-stu-id="a72df-119">In the Comment field, type a value.</span></span>
12. <span data-ttu-id="a72df-120">Klik på Bogfør regulering.</span><span class="sxs-lookup"><span data-stu-id="a72df-120">Click Post adjustment.</span></span>
13. <span data-ttu-id="a72df-121">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="a72df-121">Click Yes.</span></span>
14. <span data-ttu-id="a72df-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a72df-122">Close the page.</span></span>
    * <span data-ttu-id="a72df-123">Normalt skal du på dette tidspunkt opdatere siden for at se resultatet af reguleringen af belønningspoint under fanen Oversigt over belønningspoint. Men hvis du kører dette som en opgaveguide, skal du ikke opdatere nu, fordi hvis du gør det, stopper opgaveguiden.</span><span class="sxs-lookup"><span data-stu-id="a72df-123">Normally at this point you'd refresh the page to see the result of the reward points adjustment in the Reward point summary tab. But if you are running this as a task guide, don't refresh now because if you do, the task guide will stop.</span></span>  
15. <span data-ttu-id="a72df-124">Klik på Korttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="a72df-124">Click Card transactions.</span></span>
16. <span data-ttu-id="a72df-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a72df-125">Close the page.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]