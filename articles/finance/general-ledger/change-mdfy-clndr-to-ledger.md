---
title: Ændre eller tildele en finanskalender igen
description: I dette emne beskrives, hvordan du kan ændre den kalender, der aktuelt er knyttet til finans, og hvordan du tildeler en ny kalender til finans.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 052b8944c0a015187d1d7c4ba3db878c52faeeea
ms.sourcegitcommit: 905a8c7a0c1bc06ada2acfba913dfe5f7b44ea16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/14/2021
ms.locfileid: "6039944"
---
# <a name="change-or-reassign-a-ledger-calendar"></a><span data-ttu-id="ca368-103">Ændre eller tildele en finanskalender igen</span><span class="sxs-lookup"><span data-stu-id="ca368-103">Change or reassign a ledger calendar</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca368-104">I dette emne beskrives, hvordan du kan ændre den kalender, der aktuelt er knyttet til finans, og hvordan du tildeler en ny kalender til finans.</span><span class="sxs-lookup"><span data-stu-id="ca368-104">This topic explains how to change the calendar that is currently assigned to a ledger, and how to assign a new calendar to the ledger.</span></span>

## <a name="issue"></a><span data-ttu-id="ca368-105">Emne</span><span class="sxs-lookup"><span data-stu-id="ca368-105">Issue</span></span>

<span data-ttu-id="ca368-106">Nogen gange skal virksomheder ændre den eksisterende kalender, der er knyttet til finans, eller tildele en ny kalender.</span><span class="sxs-lookup"><span data-stu-id="ca368-106">Sometime, companies must either change the existing calendar that is assigned to a ledger or assign a new calendar.</span></span>

## <a name="resolution"></a><span data-ttu-id="ca368-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="ca368-107">Resolution</span></span>

<span data-ttu-id="ca368-108">Der er to scenarier til at ændre eller knytte en kalender igen til finans.</span><span class="sxs-lookup"><span data-stu-id="ca368-108">There are two scenarios for changing or reassigning a ledger calendar.</span></span> <span data-ttu-id="ca368-109">Det første scenario omfatter ændring af en eksisterende kalender, der allerede er tilknyttet finans.</span><span class="sxs-lookup"><span data-stu-id="ca368-109">The first scenario involves changing an existing calendar that is already assigned to the ledger.</span></span> <span data-ttu-id="ca368-110">Det andet scenario omfatter oprettelse af en ny kalender og tildeling af den til finans.</span><span class="sxs-lookup"><span data-stu-id="ca368-110">The second scenario involves creating a new calendar and assigning it to the ledger.</span></span> <span data-ttu-id="ca368-111">Begge ændringer kan udføres når som helst, også efter at der er bogført transaktioner i finans.</span><span class="sxs-lookup"><span data-stu-id="ca368-111">Both changes can be done at any time, even after transactions have been posted to the ledger.</span></span>

### <a name="change-an-existing-fiscal-calendar"></a><span data-ttu-id="ca368-112">Ændre en eksisterende regnskabskalender</span><span class="sxs-lookup"><span data-stu-id="ca368-112">Change an existing fiscal calendar</span></span>

<span data-ttu-id="ca368-113">Hvis du vil ændre en eksisterende kalender, der er knyttet til finans, skal du gå til **Finans \> Finansopsætning \> Finans** og vælge linket til regnskabskalenderen for at åbne siden **Finanskalendere**.</span><span class="sxs-lookup"><span data-stu-id="ca368-113">To change an existing calendar that is assigned to your ledger, go to **General ledger \> Ledger setup \> Ledger**, and select the link for the fiscal calendar to open the **Ledger calendars** page.</span></span>

<span data-ttu-id="ca368-114">Der er grænser for, hvilke ændringer du kan foretage i en kalender.</span><span class="sxs-lookup"><span data-stu-id="ca368-114">There are limits to the changes that can be made to a calendar.</span></span> <span data-ttu-id="ca368-115">Du kan f.eks. ændre start- og slutdatoerne for *perioderne* i et år, men du kan ikke ændre start- og slutdatoerne for et *år* i kalenderen.</span><span class="sxs-lookup"><span data-stu-id="ca368-115">For example, you can change the start and end dates of the *periods* in a year, but you can't change the start and end dates of a *year* in the calendar.</span></span>

<span data-ttu-id="ca368-116">Hvis du vil ændre perioderne i et år, skal du vælge den relevante kalender og det relevante år.</span><span class="sxs-lookup"><span data-stu-id="ca368-116">To change the periods in a year, select the appropriate calendar and year.</span></span> <span data-ttu-id="ca368-117">Du skal først bruge knappen **Slet periode** til at slette nogle eller alle de eksisterende driftsperioder.</span><span class="sxs-lookup"><span data-stu-id="ca368-117">First, use the use the **Delete period** button to delete some or all of the existing operating periods.</span></span> <span data-ttu-id="ca368-118">Alle driftsperioder undtagen den første kan slettes.</span><span class="sxs-lookup"><span data-stu-id="ca368-118">All operating periods except the first can be deleted.</span></span> <span data-ttu-id="ca368-119">Brug derefter knappen **Opdel periode** til at opdele den resterende periode eller perioder i nye perioder ved at angive en korrekt startdato for den næste periode.</span><span class="sxs-lookup"><span data-stu-id="ca368-119">Then use the **Divide period** button to divide the remaining period or periods into new periods by entering an appropriate start date for the next period.</span></span>

<span data-ttu-id="ca368-120">Når du har ændret perioderne i en kalender, skal du køre processen **Genberegn finansperioder** i alle juridiske enheder (virksomhed), som kalenderen er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="ca368-120">After you change the periods in a calendar, you must run the **Recalculate ledger periods** process in every legal entity (company) that the calendar is assigned to.</span></span> <span data-ttu-id="ca368-121">Selvom der ikke vises en advarsel, som minder dig om at udføre dette trin, skal genberegningsprocessen opdatere den periode, der er knyttet til hver bogført transaktion i Finans.</span><span class="sxs-lookup"><span data-stu-id="ca368-121">Although no warning message reminds you to complete this step, the recalculation process is required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="ca368-122">Hvis du vil køre genberegningsprocessen, skal du vælge **Genberegn finansperioder** på siden **Finansopsætning** i hvert enkelt regnskab.</span><span class="sxs-lookup"><span data-stu-id="ca368-122">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page in each company.</span></span>

<span data-ttu-id="ca368-123">Hvis genberegningsprocessen ikke køres, kan transaktionssaldi på en råbalance eller i regnskaber blive medtaget forkert i perioder.</span><span class="sxs-lookup"><span data-stu-id="ca368-123">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="ca368-124">I dette tilfælde kan du til enhver tid rette saldi ved at køre genberegningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="ca368-124">In this case, you can correct the balances at any time by running the recalculation process.</span></span>

### <a name="assign-a-new-fiscal-calendar"></a><span data-ttu-id="ca368-125">Tildele en ny regnskabskalender</span><span class="sxs-lookup"><span data-stu-id="ca368-125">Assign a new fiscal calendar</span></span>

<span data-ttu-id="ca368-126">Hvis du vil tildele en ny regnskabskalender, skal du gå til **Finans \> Finansopsætning \> Finans** og vælge **Rediger** for at sætte siden **Finans** i redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="ca368-126">To assign a new fiscal calendar, go to **General ledger \> Ledger setup \> Ledger**, and select **Edit** to put the **Ledger** page into edit mode.</span></span> <span data-ttu-id="ca368-127">Vælg derefter en ny regnskabskalender i feltet **Regnskabskalender**.</span><span class="sxs-lookup"><span data-stu-id="ca368-127">Then, in the **Fiscal calendar** field, select a new fiscal calendar.</span></span>

<span data-ttu-id="ca368-128">Når du har ændret regnskabskalenderen for en finans, skal du køre **Genberegn finansperioder**.</span><span class="sxs-lookup"><span data-stu-id="ca368-128">After you change the fiscal calendar for a ledger, you must run the **Recalculate ledger periods**.</span></span> <span data-ttu-id="ca368-129">Når du tildeler en ny regnskabskalender til en finanskonto, vises der en meddelelse, som minder dig om at udføre dette trin.</span><span class="sxs-lookup"><span data-stu-id="ca368-129">When you assign a new fiscal calendar to a ledger, a message reminds you to complete this step.</span></span> <span data-ttu-id="ca368-130">Selvom meddelelsen kan indikere, at genberegningsprocessen er valgfri, er den det ikke.</span><span class="sxs-lookup"><span data-stu-id="ca368-130">Although the message might seem to indicate that the recalculation process is optional, it isn't.</span></span> <span data-ttu-id="ca368-131">Den skal opdatere den periode, der er knyttet til hver bogført transaktion i Finans.</span><span class="sxs-lookup"><span data-stu-id="ca368-131">It's required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="ca368-132">Hvis du vil køre genberegningsprocessen, skal du vælge **Genberegn finansperioder** på siden **Finansopsætning**.</span><span class="sxs-lookup"><span data-stu-id="ca368-132">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page.</span></span>

<span data-ttu-id="ca368-133">Hvis genberegningsprocessen ikke køres, kan transaktionssaldi på en råbalance eller i regnskaber blive medtaget forkert i perioder.</span><span class="sxs-lookup"><span data-stu-id="ca368-133">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="ca368-134">I dette tilfælde kan du til enhver tid rette saldi ved at køre genberegningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="ca368-134">In this case, you can correct the balances at any time by running the recalculation process.</span></span>
