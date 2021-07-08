---
title: Produktet er på hold for transaktioner
description: Når du har autoriseret ordreforslag, modtager du en fejlmeddelelse om, at en vare er på hold for transaktioner.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6654e6437a088218db116b955631be4c7e62de5f
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301273"
---
# <a name="product-is-on-hold-for-transactions"></a><span data-ttu-id="ca2fb-103">Produktet er på hold for transaktioner</span><span class="sxs-lookup"><span data-stu-id="ca2fb-103">Product is on hold for transactions</span></span>

<span data-ttu-id="ca2fb-104">Fejlkode: SYS13295</span><span class="sxs-lookup"><span data-stu-id="ca2fb-104">Error code: SYS13295</span></span>

## <a name="symptoms"></a><span data-ttu-id="ca2fb-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="ca2fb-105">Symptoms</span></span>

<span data-ttu-id="ca2fb-106">Når du autoriserer ordreforslag, får du vist følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="ca2fb-106">After you firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="ca2fb-107">Varen %1 er spærret for bevægelser i %2.</span><span class="sxs-lookup"><span data-stu-id="ca2fb-107">Item %1 is on hold for transactions in %2.</span></span>

## <a name="cause"></a><span data-ttu-id="ca2fb-108">Årsag</span><span class="sxs-lookup"><span data-stu-id="ca2fb-108">Cause</span></span>

<span data-ttu-id="ca2fb-109">Når spærrede varer beskrives, bruger systemet begreberne *spærret*, *stoppet* og *på hold* som synonymer.</span><span class="sxs-lookup"><span data-stu-id="ca2fb-109">When describing blocked items, system uses the terms *blocked*, *stopped*, and *on hold* interchangeably.</span></span> <span data-ttu-id="ca2fb-110">Denne fejl betyder, at varen er angivet som **Stoppet** i standardordreindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="ca2fb-110">This error means that the item is set as **Stopped** in its default order settings.</span></span>

<span data-ttu-id="ca2fb-111">Hvis en vare er spærret, og du føjer den til en indkøbsordre- eller salgsordrelinje, får du vist en advarsel.</span><span class="sxs-lookup"><span data-stu-id="ca2fb-111">If an item is blocked, and you add it to a purchase order or sales order line, you receive a warning message.</span></span> <span data-ttu-id="ca2fb-112">Når en vare er spærret, kan lagertransaktioner med relation til indkøbsordre- eller salgsordrelinjen ikke ændres, når du for eksempel bogfører en følgeseddel eller en faktura.</span><span class="sxs-lookup"><span data-stu-id="ca2fb-112">When an item is blocked, inventory transactions that are related to the purchase order or sales order line can't be modified (for example, when you post a packing slip or an invoice).</span></span> <span data-ttu-id="ca2fb-113">Du kan spærre en købt vare og samtidigt sælge varen.</span><span class="sxs-lookup"><span data-stu-id="ca2fb-113">You can block a purchased item, and, at the same time, sell the item.</span></span> <span data-ttu-id="ca2fb-114">I så fald er afkrydsningsfelt **Stoppet** markeret på en indkøbsordre, men varen er ikke spærret på lageret eller på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="ca2fb-114">In this case, the **Stopped** check box is selected on a purchase order, but the item isn't blocked in inventory or on a sales order.</span></span>

<span data-ttu-id="ca2fb-115">Her er nogle af de betingelser, der kan medføre, at et varenummer spærres, så varen ikke kan sælges:</span><span class="sxs-lookup"><span data-stu-id="ca2fb-115">Here are some of the conditions that can cause an item number to be blocked from being sold:</span></span>

- <span data-ttu-id="ca2fb-116">Varen stadig er under udvikling eller i produktion.</span><span class="sxs-lookup"><span data-stu-id="ca2fb-116">The item is still under development or manufacture.</span></span> <span data-ttu-id="ca2fb-117">Du ønsker derfor ikke, at den sælges eller reserveres.</span><span class="sxs-lookup"><span data-stu-id="ca2fb-117">Therefore, you don't want it to be sold or reserved.</span></span>
- <span data-ttu-id="ca2fb-118">Du har modtaget mange fejlbehæftede varer, og fejlene skal rettes, før varen kan sælges.</span><span class="sxs-lookup"><span data-stu-id="ca2fb-118">You've received many defective items, and the defects must be corrected before the item can be sold.</span></span>

<span data-ttu-id="ca2fb-119">I den slags tilfælde kan du spærre varen, indtil problemerne er løst.</span><span class="sxs-lookup"><span data-stu-id="ca2fb-119">In cases of this type, you can block the item until the issue is resolved.</span></span>

<span data-ttu-id="ca2fb-120">Hvis en vare er spærret, og du opretter en returordrelinje, modtager du en meddelelse.</span><span class="sxs-lookup"><span data-stu-id="ca2fb-120">If an item is blocked, and you create a return order line, you receive a message.</span></span> <span data-ttu-id="ca2fb-121">Du kan ikke spærre en vareserie eller et vareparti.</span><span class="sxs-lookup"><span data-stu-id="ca2fb-121">You can't block a series or a lot of an item.</span></span> <span data-ttu-id="ca2fb-122">Hvis dele af en vare skal spærres, kan du gøre det ved at flytte lagerbeholdning eller spærre hele beholdningen af varen i den pågældende periode.</span><span class="sxs-lookup"><span data-stu-id="ca2fb-122">If parts of an item must be blocked, you can block them by moving inventory or by blocking the full stock of the item for that period.</span></span>

## <a name="resolution"></a><span data-ttu-id="ca2fb-123">Løsning</span><span class="sxs-lookup"><span data-stu-id="ca2fb-123">Resolution</span></span>

- <span data-ttu-id="ca2fb-124">Åbn siden **Standardindstillinger for ordre** for varen, og fjern markeringen i afkrydsningsfeltet **Stoppet**.</span><span class="sxs-lookup"><span data-stu-id="ca2fb-124">Open the **Default order settings** page for the item, and clear the **Stopped** checkbox.</span></span>
