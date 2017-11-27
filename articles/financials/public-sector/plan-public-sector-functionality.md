---
title: "Planlæg funktioner til den offentlige sektor"
description: "I denne artikel angives de første trin til opsætning af funktioner til den offentlige sektor i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 19851
ms.assetid: 877eabf3-19c7-4897-b33e-c5a8a319cb35
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8c020a590af5bed91be4ba2860e39a32117aed09
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="plan-for-public-sector-functionality"></a><span data-ttu-id="08efc-103">Planlægge funktioner til den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="08efc-103">Plan for public sector functionality</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="08efc-104">I denne artikel angives de første trin til opsætning af funktioner til den offentlige sektor i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="08efc-104">This article suggests the first steps to setting up Public sector functionality in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<a name="what-should-i-do-first"></a><span data-ttu-id="08efc-105">Hvad skal jeg først gøre?</span><span class="sxs-lookup"><span data-stu-id="08efc-105">What should I do first?</span></span>
-----------------------

<span data-ttu-id="08efc-106">Før du begynder at justere indstillingerne og angive dine data, bør du overveje, hvilke Finance and Operations-moduler du skal konfigurere til din offentlige organisation.</span><span class="sxs-lookup"><span data-stu-id="08efc-106">Before you begin to adjust the settings and input your data, you should consider which Finance and Operations modules you’ll need to set up for your Public sector organization.</span></span> <span data-ttu-id="08efc-107">Funktioner til den offentlige sektor er integreret med følgende Finance and Operations-moduler og Microsoft-produkter.</span><span class="sxs-lookup"><span data-stu-id="08efc-107">Public sector functionality is integrated with the following Finance and Operations modules and Microsoft products.</span></span>

### <a name="accounts-payable"></a><span data-ttu-id="08efc-108">Kreditor</span><span class="sxs-lookup"><span data-stu-id="08efc-108">Accounts payable</span></span>

<span data-ttu-id="08efc-109">Forside til betalingsrapporten Indkøbsordrelinjebeløb</span><span class="sxs-lookup"><span data-stu-id="08efc-109">Cover page for payments report Purchase order line amounts</span></span>

### <a name="accounts-receivable"></a><span data-ttu-id="08efc-110">Debitor</span><span class="sxs-lookup"><span data-stu-id="08efc-110">Accounts receivable</span></span>

<span data-ttu-id="08efc-111">Faktureringsklassifikationer Brugerdefinerede felter til faktureringskoder Faktureringskoder Brugerdefinerede felter til fritekstfakturalinje Rentelinjer Samhandelspartnerkoder</span><span class="sxs-lookup"><span data-stu-id="08efc-111">Billing classifications Billing code custom fields Billing codes Free text invoice line custom fields Interest lines Trading partner codes</span></span>

### <a name="budgeting"></a><span data-ttu-id="08efc-112">Budgetlægning</span><span class="sxs-lookup"><span data-stu-id="08efc-112">Budgeting</span></span>

<span data-ttu-id="08efc-113">Budgetanalyse Budgetanalyse for reviderede budgetter Budgetanalyse for faktiske udgifter Budgetanalyse for behæftelser Budgetanalyse for budgetreservationer</span><span class="sxs-lookup"><span data-stu-id="08efc-113">Budget analysis Budget analysis for revised budgets Budget analysis for actual expenditures Budget analysis for encumbrances Budget analysis for pre-encumbrances</span></span>

### <a name="french-regulatory-options"></a><span data-ttu-id="08efc-114">Indstillinger for franske myndighedskrav</span><span class="sxs-lookup"><span data-stu-id="08efc-114">French regulatory options</span></span>

<span data-ttu-id="08efc-115">**Bemærk!** Du kan finde oplysninger om indstillinger for franske myndighedskrav i [Kontering for den offentlige sektor i Frankrig](../localizations/emea-fra-public-sector-accounting.md).</span><span class="sxs-lookup"><span data-stu-id="08efc-115">**Note** For information about French regulatory options, see [Public sector accounting in France](../localizations/emea-fra-public-sector-accounting.md).</span></span> <span data-ttu-id="08efc-116">Følgende sider er kun tilgængelige, hvis følgende betingelser er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="08efc-116">The following pages are available only if the following conditions are met:</span></span>

-   <span data-ttu-id="08efc-117">Konfigurationsnøglen **Offentlig sektor** er valgt.</span><span class="sxs-lookup"><span data-stu-id="08efc-117">The **Public sector** configuration key is selected.</span></span>
-   <span data-ttu-id="08efc-118">Konfigurationsundernøglen **Franske myndighedskrav** er valgt.</span><span class="sxs-lookup"><span data-stu-id="08efc-118">The **French regulatory** configuration subkey is selected.</span></span>
-   <span data-ttu-id="08efc-119">Indstillingen **Brug konteringsreglerne for den franske offentlige sektor** er valgt på siden **Budgetparametre**.</span><span class="sxs-lookup"><span data-stu-id="08efc-119">The **Use French Public sector accounting rules** option is selected on the **Budget parameters** page.</span></span>

<span data-ttu-id="08efc-120">Saldooversigt Tilsagn Tilsagn lukket Vedligehold mandats de paiement Vedligehold titres de recette Købsaftale, afdelingsadgang Købsaftaletræ Forbrugsgrænser efter kategori Hold-historik for kreditorfakturabetaling</span><span class="sxs-lookup"><span data-stu-id="08efc-120">Balance summary Commitment Commitment close Maintain mandats de paiement Maintain titres de recette Purchase agreement department access Purchase agreement tree Spending thresholds by category Vendor invoice payment hold history</span></span>

### <a name="general-ledger"></a><span data-ttu-id="08efc-121">Finans</span><span class="sxs-lookup"><span data-stu-id="08efc-121">General ledger</span></span>

<span data-ttu-id="08efc-122">Avancerede finansposter Tilknyt afledte økonomiske hierarkier Afledte økonomiske hierarkier Filterresultater Finansieringskildetyper Midler Gennemse ultimofinanstransaktioner</span><span class="sxs-lookup"><span data-stu-id="08efc-122">Advanced ledger entries Associate derived financial hierarchies Derived financial hierarchies Filter results Fund types Funds Preview year end general ledger transactions</span></span>

### <a name="procurement-and-sourcing"></a><span data-ttu-id="08efc-123">Indkøb og forsyning</span><span class="sxs-lookup"><span data-stu-id="08efc-123">Procurement and sourcing</span></span>

<span data-ttu-id="08efc-124">Certificeringstype Bekræfter IO-koder Beløb på indkøbsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="08efc-124">Certification type Confirming PO codes Purchase order line amounts</span></span>

 

<a name="see-also"></a><span data-ttu-id="08efc-125">Se også</span><span class="sxs-lookup"><span data-stu-id="08efc-125">See also</span></span>
--------

[<span data-ttu-id="08efc-126">Funktioner til den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="08efc-126">Public sector functionality</span></span>](public-sector-functionality.md)




