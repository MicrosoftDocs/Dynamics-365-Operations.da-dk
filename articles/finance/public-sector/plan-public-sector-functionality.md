---
title: Planlægge funktioner til den offentlige sektor
description: I dette emne foreslås de første trin i opsætningen af funktioner til den offentlige sektor.
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
ms.openlocfilehash: 760bce7983e07e61940d5091049b1ad1ceee935b
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646298"
---
# <a name="plan-for-public-sector-functionality"></a><span data-ttu-id="722e1-103">Planlægge funktioner til den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="722e1-103">Plan for public sector functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="722e1-104">I dette emne foreslås de første trin i opsætningen af funktioner til den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="722e1-104">This topic suggests the first steps to setting up Public sector functionality.</span></span>

<a name="what-should-i-do-first"></a><span data-ttu-id="722e1-105">Hvad skal jeg først gøre?</span><span class="sxs-lookup"><span data-stu-id="722e1-105">What should I do first?</span></span>
-----------------------

<span data-ttu-id="722e1-106">Før du konfigurerer den offentlige sektor og begynder at tilføje dine data, bør du overveje, hvordan du vil bruge denne funktion.</span><span class="sxs-lookup"><span data-stu-id="722e1-106">Before you set up Public sector and begin adding your data, consider how you'll use this capability.</span></span> <span data-ttu-id="722e1-107">Din overvejelse skal identificere de moduler, der skal være indstillet til at bruge funktioner i den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="722e1-107">Your consideration should identify the modules that must be set up to use Public sector functionality.</span></span> <span data-ttu-id="722e1-108">Den offentlige sektor integreres med følgende:</span><span class="sxs-lookup"><span data-stu-id="722e1-108">Public sector integrates with the following:</span></span> 

### <a name="accounts-payable"></a><span data-ttu-id="722e1-109">Kreditor</span><span class="sxs-lookup"><span data-stu-id="722e1-109">Accounts payable</span></span>

<span data-ttu-id="722e1-110">Forside til betalingsrapporten Indkøbsordrelinjebeløb</span><span class="sxs-lookup"><span data-stu-id="722e1-110">Cover page for payments report Purchase order line amounts</span></span>

### <a name="accounts-receivable"></a><span data-ttu-id="722e1-111">Debitor</span><span class="sxs-lookup"><span data-stu-id="722e1-111">Accounts receivable</span></span>

<span data-ttu-id="722e1-112">Faktureringsklassifikationer Brugerdefinerede felter til faktureringskoder Faktureringskoder Brugerdefinerede felter til fritekstfakturalinje Rentelinjer Samhandelspartnerkoder</span><span class="sxs-lookup"><span data-stu-id="722e1-112">Billing classifications Billing code custom fields Billing codes Free text invoice line custom fields Interest lines Trading partner codes</span></span>

### <a name="budgeting"></a><span data-ttu-id="722e1-113">Budgetlægning</span><span class="sxs-lookup"><span data-stu-id="722e1-113">Budgeting</span></span>

<span data-ttu-id="722e1-114">Budgetanalyse Budgetanalyse for reviderede budgetter Budgetanalyse for faktiske udgifter Budgetanalyse for behæftelser Budgetanalyse for budgetreservationer</span><span class="sxs-lookup"><span data-stu-id="722e1-114">Budget analysis Budget analysis for revised budgets Budget analysis for actual expenditures Budget analysis for encumbrances Budget analysis for pre-encumbrances</span></span>

### <a name="french-regulatory-options"></a><span data-ttu-id="722e1-115">Indstillinger for franske myndighedskrav</span><span class="sxs-lookup"><span data-stu-id="722e1-115">French regulatory options</span></span>

<span data-ttu-id="722e1-116">**Bemærk!** Du kan finde oplysninger om indstillinger for franske myndighedskrav i [Kontering for den offentlige sektor i Frankrig](../localizations/emea-fra-public-sector-accounting.md).</span><span class="sxs-lookup"><span data-stu-id="722e1-116">**Note** For information about French regulatory options, see [Public sector accounting in France](../localizations/emea-fra-public-sector-accounting.md).</span></span> <span data-ttu-id="722e1-117">Følgende sider er kun tilgængelige, hvis følgende betingelser er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="722e1-117">The following pages are available only if the following conditions are met:</span></span>

-   <span data-ttu-id="722e1-118">Konfigurationsnøglen **Offentlig sektor** er valgt.</span><span class="sxs-lookup"><span data-stu-id="722e1-118">The **Public sector** configuration key is selected.</span></span>
-   <span data-ttu-id="722e1-119">Konfigurationsundernøglen **Franske myndighedskrav** er valgt.</span><span class="sxs-lookup"><span data-stu-id="722e1-119">The **French regulatory** configuration subkey is selected.</span></span>
-   <span data-ttu-id="722e1-120">Indstillingen **Brug konteringsreglerne for den franske offentlige sektor** er valgt på siden **Budgetparametre**.</span><span class="sxs-lookup"><span data-stu-id="722e1-120">The **Use French Public sector accounting rules** option is selected on the **Budget parameters** page.</span></span>

<span data-ttu-id="722e1-121">Saldooversigt Tilsagn lukket Vedligehold mandats de paiement Vedligehold titres de recette Købsaftale, afdelingsadgang Købsaftaletræ Forbrugsgrænser efter kategori Hold-historik for kreditorfakturabetaling</span><span class="sxs-lookup"><span data-stu-id="722e1-121">Balance summary Commitment close Maintain mandats de paiement Maintain titres de recette Purchase agreement department access Purchase agreement tree Spending thresholds by category Vendor invoice payment hold history</span></span>

### <a name="general-ledger"></a><span data-ttu-id="722e1-122">Finans</span><span class="sxs-lookup"><span data-stu-id="722e1-122">General ledger</span></span>

<span data-ttu-id="722e1-123">Avancerede finansposter Tilknyt afledte økonomiske hierarkier Afledte økonomiske hierarkier Filterresultater Finansieringskildetyper Midler Gennemse ultimofinanstransaktioner</span><span class="sxs-lookup"><span data-stu-id="722e1-123">Advanced ledger entries Associate derived financial hierarchies Derived financial hierarchies Filter results Fund types Funds Preview year end general ledger transactions</span></span>

### <a name="procurement-and-sourcing"></a><span data-ttu-id="722e1-124">Indkøb og forsyning</span><span class="sxs-lookup"><span data-stu-id="722e1-124">Procurement and sourcing</span></span>

<span data-ttu-id="722e1-125">Certificeringstype Bekræfter IO-koder Beløb på indkøbsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="722e1-125">Certification type Confirming PO codes Purchase order line amounts</span></span>



<a name="additional-resources"></a><span data-ttu-id="722e1-126">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="722e1-126">Additional resources</span></span>
--------

[<span data-ttu-id="722e1-127">Startside for offentlig sektor</span><span class="sxs-lookup"><span data-stu-id="722e1-127">Public sector home page</span></span>](public-sector-functionality.md)



