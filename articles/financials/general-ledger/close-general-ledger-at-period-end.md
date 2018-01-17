---
title: Lukke Finans ved periodeafslutning
description: "I dette emne beskrives de opgaver, der typisk udføres, når du udfører en lukning af periode til Finans."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 2a94d94a702bce476e573b9137ca73bb36245000
ms.contentlocale: da-dk
ms.lasthandoff: 01/17/2018

---

# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="20df4-103">Lukke Finans ved periodeafslutning</span><span class="sxs-lookup"><span data-stu-id="20df4-103">Close the general ledger at period end</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="20df4-104">I dette emne beskrives de opgaver, der typisk udføres, når du udfører en lukning af periode til Finans.</span><span class="sxs-lookup"><span data-stu-id="20df4-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="20df4-105">I Finans kan du afslutte lukningsprocedurer for en periode eller et år.</span><span class="sxs-lookup"><span data-stu-id="20df4-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="20df4-106">Lukningsprocesser forberede systemet på en ny periode.</span><span class="sxs-lookup"><span data-stu-id="20df4-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="20df4-107">Når du skal forberede systemet på et nyt år, skal du køre årsafslutningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="20df4-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="20df4-108">Hver organisation har forskellige processer og trin, der udføres ved periodens udløb.</span><span class="sxs-lookup"><span data-stu-id="20df4-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="20df4-109">Her er nogle valgfrie trin for periodeudløb:</span><span class="sxs-lookup"><span data-stu-id="20df4-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="20df4-110">Udfør alle opgaverne for alle andre moduler, som f.eks. Debitor, Kreditor og Lager.</span><span class="sxs-lookup"><span data-stu-id="20df4-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="20df4-111">Kontroller, at alle kladder bogføres.</span><span class="sxs-lookup"><span data-stu-id="20df4-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="20df4-112">Kør værdiregulering af udenlandsk valuta for at generere eventuelle ikke-realiserede tab eller gevinster.</span><span class="sxs-lookup"><span data-stu-id="20df4-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="20df4-113">Udlign posteringer for hver finanskonti.</span><span class="sxs-lookup"><span data-stu-id="20df4-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="20df4-114">Behandl alle nødvendige fordelinger.</span><span class="sxs-lookup"><span data-stu-id="20df4-114">Process any required allocations.</span></span>
-   <span data-ttu-id="20df4-115">Bogfør manuelt justeringer for periodeafslutningen.</span><span class="sxs-lookup"><span data-stu-id="20df4-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="20df4-116">Journaliser posteringer, og gennemse rapporten **Finanskladde**.</span><span class="sxs-lookup"><span data-stu-id="20df4-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="20df4-117">Konsolider ved hjælp af et koncernselskab eller økonomisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="20df4-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="20df4-118">Generér regnskaber for periodeafslutningen ved hjælp af Økonomirapportering.</span><span class="sxs-lookup"><span data-stu-id="20df4-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="20df4-119">Angiv finansperioder til **På hold**, så der sker yderligere bogføring.</span><span class="sxs-lookup"><span data-stu-id="20df4-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="20df4-120">Du kan også begrænse en periode til en bestemt brugergruppe, mens der pågår aktiviteter i periodeafslutningen, for at have bedre kontrol.</span><span class="sxs-lookup"><span data-stu-id="20df4-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="20df4-121">Det er ikke en god ide at indstille perioder til **Permanent lukket**, fordi du ikke kan genåbne en periode, der er blevet lukket.</span><span class="sxs-lookup"><span data-stu-id="20df4-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="20df4-122">Den arbejdsområdet Afslutning på regnskabsperiode kan bruges til at organisere og spore de opgaver, der kræves til forskellige periodeafslutningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="20df4-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="20df4-123">Du kan finde flere oplysninger i følgende emner:</span><span class="sxs-lookup"><span data-stu-id="20df4-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="20df4-124">Arbejdsområde til afslutning på regnskabsperiode</span><span class="sxs-lookup"><span data-stu-id="20df4-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="20df4-125">Årsafslutning</span><span class="sxs-lookup"><span data-stu-id="20df4-125">Year end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="20df4-126">Masseafslutning af regnskabsperiode</span><span class="sxs-lookup"><span data-stu-id="20df4-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)





