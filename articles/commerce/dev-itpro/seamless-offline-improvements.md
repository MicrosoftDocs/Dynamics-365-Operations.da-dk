---
title: Problemfrit offline skift til gavekort- og kreditnotahandlinger
description: Dette emne indeholder en oversigt over forbedringer, der giver en problemfri offline skift til bestemte betalingstyper.
author: rubendel
manager: AnnBe
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 1ea46ae90dedcc3ad3c3b305bddeb4d98827353a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230662"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a><span data-ttu-id="b934b-103">Problemfrit offline skift til gavekort- og kreditnotahandlinger</span><span class="sxs-lookup"><span data-stu-id="b934b-103">Seamless offline switch for gift card and credit memo operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b934b-104">Hvis en kasse enhed mister forbindelsen til kanaldatabasen, kan de fleste POS-handlinger og -transaktioner, der var i gang, fortsætte, når kassereren har modtaget en advarselsmeddelelse om tab af forbindelsen.</span><span class="sxs-lookup"><span data-stu-id="b934b-104">If a point of sale (POS) device loses its connection to the channel database, most POS operations and transactions that were in progress can proceed after the cashier receives a warning message about the loss of connectivity.</span></span> <span data-ttu-id="b934b-105">I nogle tilfælde har transaktioner dog elementer, der er afhængige af realtids-service, og disse elementer understøttes ikke, når kasseapparatet er offline.</span><span class="sxs-lookup"><span data-stu-id="b934b-105">However, in some cases, transactions have elements that rely on the real-time service, and those elements aren't supported when the POS is offline.</span></span> <span data-ttu-id="b934b-106">I dette emne beskrives nogle funktioner, der hjælper med at reducere virkningen af tabte forbindelser i disse scenarier.</span><span class="sxs-lookup"><span data-stu-id="b934b-106">This topic describes some functionality that helps reduce the impact of lost connectivity in these scenarios.</span></span>

## <a name="completing-gift-card-transactions-in-offline-mode"></a><span data-ttu-id="b934b-107">Afslutning af gavekorttransaktioner i offlinetilstand</span><span class="sxs-lookup"><span data-stu-id="b934b-107">Completing gift card transactions in offline mode</span></span>

<span data-ttu-id="b934b-108">Interne gavekort afhænger af realtidsservice, fordi saldoen for gavekortene skal vedligeholdes centralt i Microsoft Dynamics 365 Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="b934b-108">Internal gift cards depend on the real-time service, because the balance for the gift cards must be centrally maintained in Microsoft Dynamics 365 Commerce Headquarters.</span></span> <span data-ttu-id="b934b-109">Gavekort låses, så snart de føjes til en transaktion, for at hjælpe med at forhindre svindel eller andre synkroniseringsproblemer.</span><span class="sxs-lookup"><span data-stu-id="b934b-109">To help prevent fraud or other synchronization issues, gift cards are locked as soon as they are added to a transaction.</span></span> <span data-ttu-id="b934b-110">Låsningsfunktionen sikrer, at et gavekort ikke kan bruges på flere terminaler på samme tid.</span><span class="sxs-lookup"><span data-stu-id="b934b-110">The locking function ensures that a gift card can't be used on multiple terminals at the same time.</span></span> <span data-ttu-id="b934b-111">Når en transaktion er gennemført, opdateres og låses gavekortet op.</span><span class="sxs-lookup"><span data-stu-id="b934b-111">When a transaction is completed, the gift card is updated and unlocked.</span></span>

<span data-ttu-id="b934b-112">Hvis kasseapparatet imidlertid mister forbindelsen, når et gavekort er blevet føjet til en transaktion, kan gavekortet måske ikke bruges.</span><span class="sxs-lookup"><span data-stu-id="b934b-112">However, if the POS loses connectivity after a gift card has been added to a transaction, the gift card can become unusable.</span></span> <span data-ttu-id="b934b-113">Dynamics 365 Commerce har en parameter, der gør det muligt at fuldføre transaktioner, der omfatter en gavekortserie, mens kasseapparatet er offline, så denne situation forhindres.</span><span class="sxs-lookup"><span data-stu-id="b934b-113">To help prevent this situation, Dynamics 365 Commerce has a parameter that enables transactions that include a gift card line to be completed while the POS is offline.</span></span> <span data-ttu-id="b934b-114">Når denne parameter er slået til, vil gavekorttransaktioner, der er tvunget offline, blive gemt sammen med offline transaktioner, og de vil blive synkroniseret til Commerce Headquarters, når offline transaktionerne synkroniseres.</span><span class="sxs-lookup"><span data-stu-id="b934b-114">When this parameter is turned on, gift card transactions that are forced offline will be saved together with offline transactions, and they will be synced to Commerce Headquarters when the offline transactions are synced.</span></span> <span data-ttu-id="b934b-115">Synkroniseringen låser også gavekortet, så det kan bruges i en anden terminal.</span><span class="sxs-lookup"><span data-stu-id="b934b-115">The synchronization will also unlock the gift card so that it can be used at another terminal.</span></span>

<span data-ttu-id="b934b-116">Hvis du vil aktivere funktionaliteten til at indgå gavekorttransaktioner efter skift til offlinetilstand, skal du gå til fanen **Bogføring** på siden **Commerce-parametre**.</span><span class="sxs-lookup"><span data-stu-id="b934b-116">To enable the functionality to conclude gift card transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="b934b-117">Under denne fane skal du finde oversigtspanelet **Gavekort** og indstille **Tillad afslutning af gavekorttransaktioner i offlinetilstand** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b934b-117">On that tab, locate the **Gift card** fasttab and set **Allow concluding gift card transactions in offline mode** to **Yes**.</span></span>

![Indstillinger for et offline gavekort](../media/gift.png)

<span data-ttu-id="b934b-119">Commerce-parametrene lagres typisk i cachen.</span><span class="sxs-lookup"><span data-stu-id="b934b-119">Commerce parameters are typically cached.</span></span> <span data-ttu-id="b934b-120">Når indstillingen af denne parameter opdateres, og distributionsplanen er startet for at synkronisere ændringen til kanalen, kan ændringen derfor tage op til 24 timer for at træde i kraft.</span><span class="sxs-lookup"><span data-stu-id="b934b-120">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="b934b-121">Hvis ændringen skal træde i kraft øjeblikkeligt, skal du nulstille Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="b934b-121">To make the change effective immediately, reset Microsoft Internet Information Services (IIS).</span></span>

## <a name="completing-credit-memo-transactions-in-offline-mode"></a><span data-ttu-id="b934b-122">Afslutning af kreditnotatransaktioner i offlinetilstand</span><span class="sxs-lookup"><span data-stu-id="b934b-122">Completing credit memo transactions in offline mode</span></span>

<span data-ttu-id="b934b-123">Ligesom interne gavekort vedligeholdes kreditnotaer centralt i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="b934b-123">Like internal gift cards, credit memos are centrally maintained in Commerce Headquarters.</span></span> <span data-ttu-id="b934b-124">Commerce har en parameter, der giver mulighed for, at kreditnotatransaktioner kan afsluttes, mens kasseapparatet er offline.</span><span class="sxs-lookup"><span data-stu-id="b934b-124">Commerce has a parameter that enables credit memo transactions to be completed while the POS is offline.</span></span> <span data-ttu-id="b934b-125">Denne parameter fungerer på samme måde som den gavekortparameter, der blev nævnt i forrige afsnit.</span><span class="sxs-lookup"><span data-stu-id="b934b-125">This parameter works like the gift card parameter that was mentioned in the previous section.</span></span> <span data-ttu-id="b934b-126">Når parameteren er aktiveret, vil kreditnotatransaktioner, der er tvunget offline, blive synkroniseret tilbage til kanaldatabasen sammen med andre transaktioner, der blev udført, mens kasseapparatet var offline.</span><span class="sxs-lookup"><span data-stu-id="b934b-126">When the parameter is turned on, credit memo transactions that are forced offline will be synced back to the channel database, together with other transactions that were performed while the POS was offline.</span></span>

<span data-ttu-id="b934b-127">Hvis du vil aktivere funktionaliteten til at indgå kreditnotatransaktioner efter skift til offlinetilstand, skal du gå til fanen **Bogføring** på siden **Commerce-parametre**.</span><span class="sxs-lookup"><span data-stu-id="b934b-127">To enable the functionality to conclude credit memo transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="b934b-128">Under denne fane skal du finde oversigtspanelet **Kreditnota** og indstille **Tillad afslutning af kreditnotatransaktioner i offlinetilstand** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b934b-128">On that tab, locate the **Credit memo** fasttab and set **Allow concluding credit memo transactions in offline mode** to **Yes**.</span></span>

![Indstilling af offline kreditnota](../media/creditmemo.png)

<span data-ttu-id="b934b-130">Commerce-parametrene lagres typisk i cachen.</span><span class="sxs-lookup"><span data-stu-id="b934b-130">Commerce parameters are typically cached.</span></span> <span data-ttu-id="b934b-131">Når indstillingen af denne parameter opdateres, og distributionsplanen er startet for at synkronisere ændringen til kanalen, kan ændringen derfor tage op til 24 timer for at træde i kraft.</span><span class="sxs-lookup"><span data-stu-id="b934b-131">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="b934b-132">Nulstil IIS, hvis ændringen skal træde i kraft øjeblikkeligt.</span><span class="sxs-lookup"><span data-stu-id="b934b-132">To make the change effective immediately, reset IIS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b934b-133">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="b934b-133">Related topics</span></span>

- [<span data-ttu-id="b934b-134">Offline POS-funktionalitet (Point Of Sale)</span><span class="sxs-lookup"><span data-stu-id="b934b-134">Offline point of sale (POS) functionality</span></span>](https://docs.microsoft.com/dynamics365/retail/pos-offline-functionality)
- [<span data-ttu-id="b934b-135">POS-handlinger, online og offline</span><span class="sxs-lookup"><span data-stu-id="b934b-135">Online and offline point of sale (POS) operations</span></span>](https://docs.microsoft.com/dynamics365/retail/pos-operations)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]