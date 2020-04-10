---
title: " Behandle reguleringer for kundefordelsbonuspoint"
description: Denne procedure viser, hvordan du søger efter oplysninger om fordelskundekort og regulerer fordelskundebelønningspoint.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyCards, RetailLoyaltyCardRewardPointTrans, RetailLoyaltyCardRewardPointAdjustment, RetailAffiliationLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bdbd9fa60fe4d000359e4695a9fb034fae3ca1b0
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140717"
---
# <a name="process-loyalty-reward-point-adjustments"></a><span data-ttu-id="b4178-103"> Behandle reguleringer for kundefordelsbonuspoint</span><span class="sxs-lookup"><span data-stu-id="b4178-103">Process loyalty reward point adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4178-104">Denne procedure viser, hvordan du søger efter oplysninger om fordelskundekort og regulerer fordelskundebelønningspoint.</span><span class="sxs-lookup"><span data-stu-id="b4178-104">This procedure demonstrates how to look up loyalty card information and adjust loyalty reward points.</span></span> <span data-ttu-id="b4178-105">Det demodatafirma, der bruges til at oprette denne opgave, er USRT.</span><span class="sxs-lookup"><span data-stu-id="b4178-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="b4178-106">Denne opgave er beregnet til Commerce-rollen som driftschef eller en Kundeservicechef-rolle.</span><span class="sxs-lookup"><span data-stu-id="b4178-106">This task is intended for the Commerce operations manager role or a Customer service manager role.</span></span>

1. <span data-ttu-id="b4178-107">Gå til Fordelskundekort.</span><span class="sxs-lookup"><span data-stu-id="b4178-107">Go to Loyalty cards.</span></span>
2. <span data-ttu-id="b4178-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b4178-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b4178-109">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b4178-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b4178-110">Klik på Korttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="b4178-110">Click Card transactions.</span></span>
    * <span data-ttu-id="b4178-111">På denne side kan du se alle fordelskundetransaktioner for det valgte fordelskundekort.</span><span class="sxs-lookup"><span data-stu-id="b4178-111">On this page you can view all loyalty transactions for the selected loyalty card.</span></span>  
5. <span data-ttu-id="b4178-112">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b4178-112">Close the page.</span></span>
6. <span data-ttu-id="b4178-113">Klik på Kortreguleringer.</span><span class="sxs-lookup"><span data-stu-id="b4178-113">Click Card adjustments.</span></span>
7. <span data-ttu-id="b4178-114">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="b4178-114">Click New.</span></span>
8. <span data-ttu-id="b4178-115">Indtast eller vælg en værdi i feltet Belønningspoint.</span><span class="sxs-lookup"><span data-stu-id="b4178-115">In the Reward point field, enter or select a value.</span></span>
9. <span data-ttu-id="b4178-116">Indtast et tal i feltet Beløb eller antal.</span><span class="sxs-lookup"><span data-stu-id="b4178-116">In the Amount or quantity field, enter a number.</span></span>
    * <span data-ttu-id="b4178-117">Du kan tilføje eller fjerne punkter fra fordelskundekortet ved hjælp af positive eller negative beløb.</span><span class="sxs-lookup"><span data-stu-id="b4178-117">You can add or remove points from the loyalty card by using positive or negative amounts.</span></span>  
10. <span data-ttu-id="b4178-118">Indtast eller vælg en værdi i feltet Fordelskundeprogram.</span><span class="sxs-lookup"><span data-stu-id="b4178-118">In the Loyalty program field, enter or select a value.</span></span>
11. <span data-ttu-id="b4178-119">Skriv en værdi i feltet Kommentar.</span><span class="sxs-lookup"><span data-stu-id="b4178-119">In the Comment field, type a value.</span></span>
12. <span data-ttu-id="b4178-120">Klik på Bogfør regulering.</span><span class="sxs-lookup"><span data-stu-id="b4178-120">Click Post adjustment.</span></span>
13. <span data-ttu-id="b4178-121">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="b4178-121">Click Yes.</span></span>
14. <span data-ttu-id="b4178-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b4178-122">Close the page.</span></span>
    * <span data-ttu-id="b4178-123">Normalt skal du på dette tidspunkt opdatere siden for at se resultatet af reguleringen af belønningspoint under fanen Oversigt over belønningspoint. Men hvis du kører dette som en opgaveguide, skal du ikke opdatere nu, fordi hvis du gør det, stopper opgaveguiden.</span><span class="sxs-lookup"><span data-stu-id="b4178-123">Normally at this point you'd refresh the page to see the result of the reward points adjustment in the Reward point summary tab. But if you are running this as a task guide, don't refresh now because if you do, the task guide will stop.</span></span>  
15. <span data-ttu-id="b4178-124">Klik på Korttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="b4178-124">Click Card transactions.</span></span>
16. <span data-ttu-id="b4178-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b4178-125">Close the page.</span></span>

