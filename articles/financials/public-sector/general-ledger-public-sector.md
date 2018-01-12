---
title: Finans i den offentlige sektor
description: "I dette emne beskrives de finansfunktioner, som er tilgængelige for den offentlige sektor."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AdvancedLedgerEntry, JournalizingDefinition, LedgerDerivedFinHierarchies, LedgerFundType, LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 27211
ms.assetid: d737c743-e224-4a30-b4c3-e9568eaddd8c
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 47336a19899b1fad0e63265173fd7fd02fc74ec3
ms.openlocfilehash: c917cc91d47e4461f884a2bf59358e92e5d8a011
ms.contentlocale: da-dk
ms.lasthandoff: 01/12/2018

---

# <a name="general-ledger-in-the-public-sector"></a><span data-ttu-id="5e6ff-103">Finans i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="5e6ff-103">General ledger in the public sector</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5e6ff-104">I dette emne beskrives de finansfunktioner, som er tilgængelige for den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-104">This topic describes the General ledger functionality that is available for the public sector.</span></span>

<a name="how-do-general-ledger-parameters-need-to-be-set-for-public-sector-organizations"></a><span data-ttu-id="5e6ff-105">Hvordan skal Finansparametre indstilles til offentlige organisationer?</span><span class="sxs-lookup"><span data-stu-id="5e6ff-105">How do General ledger parameters need to be set for public sector organizations?</span></span>
--------------------------------------------------------------------------------

<span data-ttu-id="5e6ff-106">De fleste Finansparametre angives på samme måde for offentlige og private organisationer.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-106">Most General ledger parameters are set the same way for public sector and private sector organizations.</span></span> <span data-ttu-id="5e6ff-107">Der er desuden offentlige parametre, der bruges til årsafslutningsprocessen i forbindelse med midler.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-107">In addition, there are public sector parameters that are used for the year-end process for funds.</span></span> <span data-ttu-id="5e6ff-108">Indstil disse parametre på siden **Finansparametre** i afsnittet **Finans** i **Årsafslutning**-oversigtspanelet:</span><span class="sxs-lookup"><span data-stu-id="5e6ff-108">Set these parameters on the **General ledger parameters** page, in the **Ledger** section, on the **Fiscal year close** FastTab:</span></span>

-   <span data-ttu-id="5e6ff-109">Vælg **Opret ultimoposteringer ved overførsel** for at generere ultimo- og startsaldoposterne.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-109">Select **Create closing transactions during transfer** to generate the closing and opening balance entries.</span></span> <span data-ttu-id="5e6ff-110">Når dette er valgt, sletter systemet i efterfølgende kørsler af denne proces posteringer fra tidligere kørsler og genererer nye ultimo- og startposter.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-110">When this is selected, on subsequent runs of this process, the system deletes transactions from previous runs and generates new closing and opening entries.</span></span> <span data-ttu-id="5e6ff-111">Hvis dette ikke er valgt, beregner systemet nettoændringen og generere kun den pågældende transaktion for ultimoposter og startsaldi.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-111">If this is not selected, the system will calculate the net change and generate only that transaction for closing entries and opening balances.</span></span> <span data-ttu-id="5e6ff-112">**Bemærk**! Denne indstilling kræver brug af bogføringsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-112">**Note**: This option requires the use of posting definitions.</span></span> <span data-ttu-id="5e6ff-113">Hvis du vil vide mere, kan du se under [Bogføringsdefinitioner i den offentlige sektor](posting-definitions-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="5e6ff-113">To learn more, see [Posting definitions in the public sector](posting-definitions-public-sector.md).</span></span>
-   <span data-ttu-id="5e6ff-114">Vælg **Brug dimensionen Middel til årsafslutningsposteringer** til at aktivere den offentlige version af siden **Primoposter**.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-114">Select **Use Fund dimension for year-end transactions** to enable the public sector version of the **Opening transactions** page.</span></span>
-   <span data-ttu-id="5e6ff-115">Vælg **Brug dimensionen Middel til at overføre indkøbsordrer** til at give mulighed for at angive indstillinger for behandling af årsafslutningen for specifikke midler.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-115">Select **Use Fund dimension to carry forward purchase orders** to enable the ability to set year-end processing options for specific funds.</span></span>

<span data-ttu-id="5e6ff-116">Hvis du vil vide mere om årsafslutningsprocessen for midler, skal du se under [Årsafslutningen i den offentlige sektor](year-end-processing-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="5e6ff-116">To learn more about the year-end process for funds, see [Year-end processing in the public sector](year-end-processing-public-sector.md).</span></span>

## <a name="what-fund-classes-and-fund-types-are-available"></a><span data-ttu-id="5e6ff-117">Hvad middelklasser og middeltyper er tilgængelige?</span><span class="sxs-lookup"><span data-stu-id="5e6ff-117">What fund classes and fund types are available?</span></span>
<span data-ttu-id="5e6ff-118">Middelklasserne offentlig, privat, formueforvaltning er tilgængelige for offentlige organisationer, sammen med en klasse af typen Notat.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-118">Governmental, proprietary, and fiduciary fund classes are available for public sector organizations, along with a Memo class.</span></span> <span data-ttu-id="5e6ff-119">Du skal oprette de middeltyper, organisationen har brug for.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-119">You’ll create the fund types your organization needs.</span></span> <span data-ttu-id="5e6ff-120">Hvis du vil vide mere, kan du se under [Midler i den offentlige sektor](funds-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="5e6ff-120">To learn more, see [Funds in the public sector](funds-public-sector.md).</span></span>

## <a name="how-are-financial-dimensions-used-with-funds"></a><span data-ttu-id="5e6ff-121">Hvordan bruges økonomiske dimensioner med midler?</span><span class="sxs-lookup"><span data-stu-id="5e6ff-121">How are financial dimensions used with funds?</span></span>
<span data-ttu-id="5e6ff-122">Middeltal bruges som dimensionsværdier i økonomiske kontonumre, hvor en dimension er knyttet til et middel.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-122">Fund numbers are used as dimension values in financial account numbers where a dimension has been mapped to a fund.</span></span> <span data-ttu-id="5e6ff-123">Offentlige organisationer kræver normalt afstemte poster for økonomiske dimensioner, der er relateret til midler.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-123">Public sector organizations usually require balanced entries for financial dimensions related to funds.</span></span>

## <a name="what-is-the-easiest-way-to-adjust-or-reverse-ledger-entries"></a><span data-ttu-id="5e6ff-124">Hvad er den nemmeste måde at justere eller tilbageføre posterne?</span><span class="sxs-lookup"><span data-stu-id="5e6ff-124">What is the easiest way to adjust or reverse ledger entries?</span></span>
<span data-ttu-id="5e6ff-125">Du kan bruge avancerede finansposter til at oprette, tilpasse og tilbageføre finansposter.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-125">You can use advanced ledger entries to create, adjust, and reverse ledger entries.</span></span> <span data-ttu-id="5e6ff-126">For eksempel kan avancerede finansposter bruges til at ompostere udgifter, hvis fakturaer fejlagtigt er blevet bogført til den forkerte konto eller det forkerte projekt.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-126">For example, advanced ledger entries can be used to reclassify expenditures if invoices are mistakenly posted to the wrong account or project.</span></span> <span data-ttu-id="5e6ff-127">Hvis du vil vide mere, skal du se [Avancerede finansposter i den offentlige sektor](advanced-ledger-entries-public-sector.md) og [Bogføringsdefinitioner i den offentlige sektor](posting-definitions-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="5e6ff-127">To learn more, see [Advanced ledger entries in the public sector](advanced-ledger-entries-public-sector.md) and [Posting definitions in the public sector](posting-definitions-public-sector.md).</span></span>

## <a name="why-should-i-use-posting-definitions"></a><span data-ttu-id="5e6ff-128">Hvorfor bruge bogføringsdefinitioner?</span><span class="sxs-lookup"><span data-stu-id="5e6ff-128">Why should I use posting definitions?</span></span>
<span data-ttu-id="5e6ff-129">Du kan bruge bogføringsdefinitioner til at oprette reskontrokladdelinjer til kildetransaktioner, der opfylder de valgte kriterier – f.eks. til at generere flere, afstemte finansposter baseret på attributter, som f.eks. transaktionstyper og konti.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-129">You can use posting definitions to create subledger journal lines for originating transactions that meet selected criteria - for example, to generate multiple balanced ledger entries based on attributes such as transaction types and accounts.</span></span> <span data-ttu-id="5e6ff-130">Bogføringsdefinitioner indeholder detaljeret kontrol med Finans-opdateringer, der er oprettet af kildedokumenter, i modsætning til almindeligt anvendte opdateringer af posteringsprofiler.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-130">Posting definitions provide granular control over the general ledger updates created by source documents in contrast to the broadly applied updates of posting profiles.</span></span> <span data-ttu-id="5e6ff-131">Bogføringsdefinitioner til Finans er påkrævede, hvis du bruger avancerede finansposter.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-131">General ledger posting definitions are required if you use advanced ledger entries.</span></span> <span data-ttu-id="5e6ff-132">Bogføringsdefinitioner bruges i forbindelse med ultimobehandling af finanskonti.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-132">Posting definitions are used in the year-end processing of general ledger accounts.</span></span> <span data-ttu-id="5e6ff-133">Bogføringsdefinitioner kan bruges til afslutning af konti til pengebalancer eller overførsel af årets resultat på basis af middelklassen og kontoens afslutningstype.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-133">Posting definitions can be used to close the accounts to fund balances or retained earnings, based on the fund class and the account close type.</span></span> <span data-ttu-id="5e6ff-134">Det er et krav, at der bruges bogføringsdefinitioner ved afslutning af finanskonti og til overførsel af saldi til primoperioden i det nye regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-134">Posting definitions are required to close the general ledger accounts and to transfer balances to the opening period in the new fiscal year.</span></span> <span data-ttu-id="5e6ff-135">Hvis du vil vide mere, kan du se under [Bogføringsdefinitioner i den offentlige sektor](posting-definitions-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="5e6ff-135">To learn more, see [Posting definitions in the public sector](posting-definitions-public-sector.md).</span></span>

## <a name="how-do-i-collect-and-analyze-data-to-meet-the-common-governmentwide-accounting-classification-cgac-requirements"></a><span data-ttu-id="5e6ff-136">Hvordan indsamler og analyserer jeg data for at opfylde CGAC-krav (Governmentwide Accounting Classification)?</span><span class="sxs-lookup"><span data-stu-id="5e6ff-136">How do I collect and analyze data to meet the Common Governmentwide Accounting Classification (CGAC) requirements?</span></span>
<span data-ttu-id="5e6ff-137">Du kan bruge afledte finansielle hierarkier til at indsamle og analysere data for bogførte transaktioner for bestemte tal i hovedkonto, fuld kontonumre og økonomiske dimensionsværdier.</span><span class="sxs-lookup"><span data-stu-id="5e6ff-137">You can use derived financial hierarchies to collect and analyze posted transaction data for specific main account numbers, full account numbers, and financial dimension values.</span></span> <span data-ttu-id="5e6ff-138">Du kan finde flere oplysninger under [Afledte finansielle hierarkier i den offentlige sektor](derived-financial-hierarchies-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="5e6ff-138">To learn more, see [Derived financial hierarchies in the public sector](derived-financial-hierarchies-public-sector.md).</span></span>

<a name="see-also"></a><span data-ttu-id="5e6ff-139">Se også</span><span class="sxs-lookup"><span data-stu-id="5e6ff-139">See also</span></span>
--------

[<span data-ttu-id="5e6ff-140">Finans</span><span class="sxs-lookup"><span data-stu-id="5e6ff-140">General ledger</span></span>](../general-ledger/general-ledger.md)




