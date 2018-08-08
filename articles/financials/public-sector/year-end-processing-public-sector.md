---
title: "Årsafslutningen i den offentlige sektor"
description: "Denne artikel indeholder oplysninger om årsafslutningen for organisationer i den offentlige sektor."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchYearEndClose
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 19601
ms.assetid: ba9a7abc-bd18-47c2-b745-96cdcec8ac98
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: b9a89bd38feac2e580c3d1511d3bee8eca04115d
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---

# <a name="year-end-processing-in-the-public-sector"></a><span data-ttu-id="b9db6-103">Årsafslutningen i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="b9db6-103">Year-end processing in the public sector</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9db6-104">Denne artikel indeholder oplysninger om årsafslutningen for organisationer i den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="b9db6-104">This article provides information about year-end processing for a public sector organizations.</span></span>

<span data-ttu-id="b9db6-105">I dette emne beskrives de årsafslutningsfunktioner, som er tilgængelige for den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="b9db6-105">This topic describes the year-end functionality available for the public sector.</span></span> <span data-ttu-id="b9db6-106">Ved udgangen af regnskabsåret skal du generere ultimoposter og forberede alle konti til det næste regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="b9db6-106">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span>  <span data-ttu-id="b9db6-107">Kunder i den offentlige sektor har følgende muligheder:</span><span class="sxs-lookup"><span data-stu-id="b9db6-107">Public sector clients have the following capabilities:</span></span>

-   <span data-ttu-id="b9db6-108">Vælg konti efter midler for ultimo ved årsafslutning.</span><span class="sxs-lookup"><span data-stu-id="b9db6-108">Select accounts by fund for year-end closing.</span></span>
-   <span data-ttu-id="b9db6-109">Luk midler til forskellige konti.</span><span class="sxs-lookup"><span data-stu-id="b9db6-109">Close funds to different accounts.</span></span> <span data-ttu-id="b9db6-110">For eksempel kan du lukke nominelle konti, der er knyttet til statslige midler til pengebalancer.</span><span class="sxs-lookup"><span data-stu-id="b9db6-110">For example, you can close nominal accounts that are associated with governmental funds to fund balances.</span></span> <span data-ttu-id="b9db6-111">Du kan også lukke nominelle konti, der er forbundet med egne midler til overførte resultater.</span><span class="sxs-lookup"><span data-stu-id="b9db6-111">You can also close nominal accounts that are associated with proprietary funds to retained earnings.</span></span>
-   <span data-ttu-id="b9db6-112">Angive ultimo ved årsafslutning for alle midler og ikke-midler.</span><span class="sxs-lookup"><span data-stu-id="b9db6-112">Set up year-end closing for all funds and non-funds.</span></span> <span data-ttu-id="b9db6-113">Ikke-midler har ikke dimensionen midler i kontostrukturen.</span><span class="sxs-lookup"><span data-stu-id="b9db6-113">Non-funds don't have a fund dimension in the account structure.</span></span>
-   <span data-ttu-id="b9db6-114">Konfigurere flere ultimoperioder for at adskille forskellige former for ultimoposter, f.eks. generel lukning i forbindelse med ultimo ved årsafslutning og revisionsjusteringer.</span><span class="sxs-lookup"><span data-stu-id="b9db6-114">Set up multiple closing periods to segregate different types of closing entries, such as general year-end closing and audit adjustments.</span></span>

## <a name="can-the-year-end-process-be-run-more-than-one-time-on-the-same-data"></a><span data-ttu-id="b9db6-115">Kan årsafslutningsprocessen køres mere end én gang med de samme data?</span><span class="sxs-lookup"><span data-stu-id="b9db6-115">Can the year-end process be run more than one time on the same data?</span></span>
<span data-ttu-id="b9db6-116">Ja, årsafslutningsprocessen kan køres flere gange for det samme sæt af data.</span><span class="sxs-lookup"><span data-stu-id="b9db6-116">Yes, the year-end process can be run multiple times for the same set of data.</span></span> <span data-ttu-id="b9db6-117">Typisk, hvis flere transaktioner skal behandles, når der er kørt en årsafslutningsproces for Finans, kan årsafslutningsprocessen køres igen for at lukke de nominelle konti og angive startsaldiene korrekt i det nye år.</span><span class="sxs-lookup"><span data-stu-id="b9db6-117">Typically, if additional transactions must be processed after a general ledger year-end process is run, the year-end process can be run again to close out the nominal accounts and correctly set the opening balances in the new year.</span></span>

## <a name="how-do-i-set-up-funds-for-year-end-processing"></a><span data-ttu-id="b9db6-118">Hvordan konfigurerer jeg midler til behandling af årsafslutning?</span><span class="sxs-lookup"><span data-stu-id="b9db6-118">How do I set up funds for year-end processing?</span></span>
<span data-ttu-id="b9db6-119">Behandling af årsafslutningen for finanskonti styres af konfigurationsindstillingerne for midler på to steder:</span><span class="sxs-lookup"><span data-stu-id="b9db6-119">Year-end processing of general ledger balances is controlled by fund configuration settings in two places:</span></span>

-   <span data-ttu-id="b9db6-120">Årsafslutningsprocessen for ultimofinanssaldi i det gamle regnskabsår og oprettelse af startsaldi for det nye år sker ved hjælp af siden **Primoposter** side.</span><span class="sxs-lookup"><span data-stu-id="b9db6-120">The year-end process of closing ledger balances in the old year and establishing opening balances in the new year is done by using the **Opening transactions** page.</span></span> <span data-ttu-id="b9db6-121">Et enkelt middel eller en række af midler, der kræves til behandling.</span><span class="sxs-lookup"><span data-stu-id="b9db6-121">A single fund or range of funds is required for processing.</span></span>
-   <span data-ttu-id="b9db6-122">Årsafslutningens behandlingsindstilling for behæftelser for indkøbsordrer angives på siden **Proces for indkøbsordrers årsafslutning**.</span><span class="sxs-lookup"><span data-stu-id="b9db6-122">The year-end processing option for purchase order encumbrances is set on the **Purchase order year-end process** page.</span></span> <span data-ttu-id="b9db6-123">Du kan tilsidesætte indstillingen for bestemte midler, forudsat at de finansparametrene er indstillet til at tillade tilsidesættelse.</span><span class="sxs-lookup"><span data-stu-id="b9db6-123">You can override the option on a specific fund, provided that the general ledger parameters have been set to allow for overrides.</span></span> <span data-ttu-id="b9db6-124">Hvis du vil vide mere om parameterindstillingerne, skal du se under [Finans i den offentlige sektor](general-ledger-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="b9db6-124">To learn more about the parameter settings, see [General ledger in the public sector](general-ledger-public-sector.md).</span></span>

## <a name="how-do-i-set-up-main-accounts-for-year-end-processing"></a><span data-ttu-id="b9db6-125">Hvordan konfigurerer jeg hovedkonti til behandling af årsafslutning?</span><span class="sxs-lookup"><span data-stu-id="b9db6-125">How do I set up main accounts for year-end processing?</span></span>
<span data-ttu-id="b9db6-126">Du skal vælge en lukketype for hver konto i din kontoplan.</span><span class="sxs-lookup"><span data-stu-id="b9db6-126">You must select a close type for every account in your chart of accounts.</span></span> <span data-ttu-id="b9db6-127">Lukketypen bestemmer, hvordan årsafslutningsprocessen håndterer denne hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="b9db6-127">The close type determines how the year-end process handles that main account.</span></span> <span data-ttu-id="b9db6-128">Der findes fire lukketyper:</span><span class="sxs-lookup"><span data-stu-id="b9db6-128">There are four close types:</span></span>

-   <span data-ttu-id="b9db6-129">**Real** – Saldoen bruges til at etablere primosaldoer i det nye år.</span><span class="sxs-lookup"><span data-stu-id="b9db6-129">**Real** – The balance is used to establish opening balances in the new year.</span></span>
-   <span data-ttu-id="b9db6-130">**Nominel** – Kontoen lukkes af årsafslutningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="b9db6-130">**Nominal** – The account is closed by the year-end process.</span></span>
-   <span data-ttu-id="b9db6-131">**Nominel – luk ikke** – Kontoen administreres af andre processer til lukning, som behæftelseskonti for indkøbsordrelukning.</span><span class="sxs-lookup"><span data-stu-id="b9db6-131">**Nominal – no close** – The account is managed by other closing processes, such as encumbrance accounts for purchase order close.</span></span>
-   <span data-ttu-id="b9db6-132">**Ikke relevant** – Kontoen medtages ikke i årsafslutningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="b9db6-132">**Not applicable** – The account isn't included in year-end processing.</span></span>

<span data-ttu-id="b9db6-133">Bogføringsdefinitioner styrer de regnskaber, der forekommer på ultimoposterne, og de hjælper også oprette primoposterne for det nye år.</span><span class="sxs-lookup"><span data-stu-id="b9db6-133">Posting definitions govern the accounting that occurs on the closing entries, and they also help create the opening transactions for the new year.</span></span> <span data-ttu-id="b9db6-134">Hvis du vil vide mere, kan du se under [Bogføringsdefinitioner i den offentlige sektor](posting-definitions-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="b9db6-134">To learn more, see [Posting definitions in the public sector](posting-definitions-public-sector.md).</span></span>




