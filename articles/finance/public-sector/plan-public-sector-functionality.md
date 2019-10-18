---
title: Planlæg funktioner til den offentlige sektor
description: I denne artikel foreslås de første trin i opsætningen af funktioner til den offentlige sektor.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 19851
ms.assetid: 877eabf3-19c7-4897-b33e-c5a8a319cb35
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3ed0ffa94af0b7a0e12b19f2a72bca37d8ed513a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183507"
---
# <a name="plan-for-public-sector-functionality"></a><span data-ttu-id="d60cf-103">Planlægge funktioner til den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="d60cf-103">Plan for public sector functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d60cf-104">I denne artikel foreslås de første trin i opsætningen af funktioner til den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="d60cf-104">This article suggests the first steps to setting up Public sector functionality.</span></span>

<a name="what-should-i-do-first"></a><span data-ttu-id="d60cf-105">Hvad skal jeg først gøre?</span><span class="sxs-lookup"><span data-stu-id="d60cf-105">What should I do first?</span></span>
-----------------------

<span data-ttu-id="d60cf-106">Før du begynder at justere indstillingerne og angive dine data, bør du overveje, hvilke moduler du skal konfigurere til din offentlige organisation.</span><span class="sxs-lookup"><span data-stu-id="d60cf-106">Before you begin to adjust the settings and input your data, you should consider which modules you’ll need to set up for your Public sector organization.</span></span> <span data-ttu-id="d60cf-107">Funktioner til den offentlige sektor er integreret med følgende Dynamics 365 Finance-moduler og Microsoft-produkter.</span><span class="sxs-lookup"><span data-stu-id="d60cf-107">Public sector functionality is integrated with the following Dynamics 365 Finance modules and Microsoft products.</span></span>

### <a name="accounts-payable"></a><span data-ttu-id="d60cf-108">Kreditor</span><span class="sxs-lookup"><span data-stu-id="d60cf-108">Accounts payable</span></span>

<span data-ttu-id="d60cf-109">Forside til betalingsrapporten Indkøbsordrelinjebeløb</span><span class="sxs-lookup"><span data-stu-id="d60cf-109">Cover page for payments report Purchase order line amounts</span></span>

### <a name="accounts-receivable"></a><span data-ttu-id="d60cf-110">Debitor</span><span class="sxs-lookup"><span data-stu-id="d60cf-110">Accounts receivable</span></span>

<span data-ttu-id="d60cf-111">Faktureringsklassifikationer Brugerdefinerede felter til faktureringskoder Faktureringskoder Brugerdefinerede felter til fritekstfakturalinje Rentelinjer Samhandelspartnerkoder</span><span class="sxs-lookup"><span data-stu-id="d60cf-111">Billing classifications Billing code custom fields Billing codes Free text invoice line custom fields Interest lines Trading partner codes</span></span>

### <a name="budgeting"></a><span data-ttu-id="d60cf-112">Budgetlægning</span><span class="sxs-lookup"><span data-stu-id="d60cf-112">Budgeting</span></span>

<span data-ttu-id="d60cf-113">Budgetanalyse Budgetanalyse for reviderede budgetter Budgetanalyse for faktiske udgifter Budgetanalyse for behæftelser Budgetanalyse for budgetreservationer</span><span class="sxs-lookup"><span data-stu-id="d60cf-113">Budget analysis Budget analysis for revised budgets Budget analysis for actual expenditures Budget analysis for encumbrances Budget analysis for pre-encumbrances</span></span>

### <a name="french-regulatory-options"></a><span data-ttu-id="d60cf-114">Indstillinger for franske myndighedskrav</span><span class="sxs-lookup"><span data-stu-id="d60cf-114">French regulatory options</span></span>

<span data-ttu-id="d60cf-115">**Bemærk!** Du kan finde oplysninger om indstillinger for franske myndighedskrav i [Kontering for den offentlige sektor i Frankrig](../localizations/emea-fra-public-sector-accounting.md).</span><span class="sxs-lookup"><span data-stu-id="d60cf-115">**Note** For information about French regulatory options, see [Public sector accounting in France](../localizations/emea-fra-public-sector-accounting.md).</span></span> <span data-ttu-id="d60cf-116">Følgende sider er kun tilgængelige, hvis følgende betingelser er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="d60cf-116">The following pages are available only if the following conditions are met:</span></span>

-   <span data-ttu-id="d60cf-117">Konfigurationsnøglen **Offentlig sektor** er valgt.</span><span class="sxs-lookup"><span data-stu-id="d60cf-117">The **Public sector** configuration key is selected.</span></span>
-   <span data-ttu-id="d60cf-118">Konfigurationsundernøglen **Franske myndighedskrav** er valgt.</span><span class="sxs-lookup"><span data-stu-id="d60cf-118">The **French regulatory** configuration subkey is selected.</span></span>
-   <span data-ttu-id="d60cf-119">Indstillingen **Brug konteringsreglerne for den franske offentlige sektor** er valgt på siden **Budgetparametre**.</span><span class="sxs-lookup"><span data-stu-id="d60cf-119">The **Use French Public sector accounting rules** option is selected on the **Budget parameters** page.</span></span>

<span data-ttu-id="d60cf-120">Saldooversigt Tilsagn Tilsagn lukket Vedligehold mandats de paiement Vedligehold titres de recette Købsaftale, afdelingsadgang Købsaftaletræ Forbrugsgrænser efter kategori Hold-historik for kreditorfakturabetaling</span><span class="sxs-lookup"><span data-stu-id="d60cf-120">Balance summary Commitment Commitment close Maintain mandats de paiement Maintain titres de recette Purchase agreement department access Purchase agreement tree Spending thresholds by category Vendor invoice payment hold history</span></span>

### <a name="general-ledger"></a><span data-ttu-id="d60cf-121">Finans</span><span class="sxs-lookup"><span data-stu-id="d60cf-121">General ledger</span></span>

<span data-ttu-id="d60cf-122">Avancerede finansposter Tilknyt afledte økonomiske hierarkier Afledte økonomiske hierarkier Filterresultater Finansieringskildetyper Midler Gennemse ultimofinanstransaktioner</span><span class="sxs-lookup"><span data-stu-id="d60cf-122">Advanced ledger entries Associate derived financial hierarchies Derived financial hierarchies Filter results Fund types Funds Preview year end general ledger transactions</span></span>

### <a name="procurement-and-sourcing"></a><span data-ttu-id="d60cf-123">Indkøb og forsyning</span><span class="sxs-lookup"><span data-stu-id="d60cf-123">Procurement and sourcing</span></span>

<span data-ttu-id="d60cf-124">Certificeringstype Bekræfter IO-koder Beløb på indkøbsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="d60cf-124">Certification type Confirming PO codes Purchase order line amounts</span></span>



<a name="additional-resources"></a><span data-ttu-id="d60cf-125">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="d60cf-125">Additional resources</span></span>
--------

[<span data-ttu-id="d60cf-126">Funktioner til den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="d60cf-126">Public sector functionality</span></span>](public-sector-functionality.md)



